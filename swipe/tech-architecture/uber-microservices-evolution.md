# Análise: Evolução de Microservices do Uber

## Contexto
A jornada do Uber de monolito para microservices é uma das mais documentadas e instrutivas da indústria de tecnologia. Com milhares de microservices em produção, o Uber vivenciou tanto os benefícios quanto as dores extremas desta arquitetura, oferecendo lições valiosas sobre quando e como adotar microservices.

---

## 1. Linha do Tempo da Evolução

### Fase 1: Monolito (2010-2013)
- Aplicação monolítica em Python
- Um único banco de dados PostgreSQL
- Deploy como uma única unidade
- Equipe pequena (menos de 50 engenheiros)
- Funcionou bem para validar product-market fit
- Começou a mostrar limitações com o crescimento rápido

### Fase 2: SOA - Service-Oriented Architecture (2013-2015)
- Decomposição inicial em serviços maiores por domínio
- Dispatch (despacho), Trips (viagens), Payments (pagamentos)
- Comunicação via HTTP/REST entre serviços
- Cada serviço com seu próprio banco de dados
- Migração gradual do monolito (strangler fig pattern)
- Equipe cresceu para centenas de engenheiros

### Fase 3: Microservices Explosion (2015-2018)
- Mais de 2.000 microservices em produção
- Cada equipe criava seus próprios serviços com autonomia total
- Proliferação de linguagens: Python, Go, Java, Node.js
- Complexidade operacional cresceu exponencialmente
- Dificuldade crescente de entender dependências entre serviços
- Overhead de latência por cascata de chamadas entre serviços

### Fase 4: Consolidação e Domain-Oriented Architecture (2018+)
- DOMA (Domain-Oriented Microservice Architecture)
- Agrupamento de microservices em domínios lógicos
- Gateways por domínio para encapsular complexidade
- Padronização de stack e ferramentas entre equipes
- Foco em reduzir complexidade sem perder autonomia
- Investimento massivo em platform e developer experience

---

## 2. DOMA - Domain-Oriented Microservice Architecture

### Conceito Central
DOMA é a resposta do Uber à complexidade descontrolada de microservices. Organiza serviços em domínios de negócio com boundaries claras e interfaces bem definidas.

### Camadas do DOMA
1. **Layer 1 - Infrastructure**: Serviços de plataforma compartilhada (logging, metrics, messaging)
2. **Layer 2 - Business Logic**: Lógica de negócio organizada em domínios
3. **Layer 3 - API Gateway**: Interfaces externas (mobile, web, parceiros)
4. **Layer 4 - Edge**: Serviços de frontend e experiência do usuário

### Princípios do DOMA
- Cada domínio tem uma interface bem definida (gateway)
- Comunicação entre domínios apenas via interfaces públicas
- Dentro do domínio, serviços podem se comunicar livremente
- Cada domínio é owned por uma equipe ou grupo de equipes
- Domínios encapsulam complexidade interna
- Extensibilidade via eventos e hooks, não acoplamento direto

### Estrutura de um Domínio
```
+----------------------------------------------------+
|                    Domínio: Payments                |
|                                                     |
|  +--------+   +---------+   +-----------+          |
|  | Payment|   | Billing |   | Fraud     |          |
|  | Service|   | Service |   | Detection |          |
|  +--------+   +---------+   +-----------+          |
|       |             |              |                |
|  +--------+   +---------+   +-----------+          |
|  | Payment|   | Billing |   | Fraud     |          |
|  | DB     |   | DB      |   | DB        |          |
|  +--------+   +---------+   +-----------+          |
|                                                     |
|  [Payment Gateway - Interface Pública do Domínio]   |
+----------------------------------------------------+
```

---

## 3. Infraestrutura Construída

### Plataforma de Desenvolvimento
- **Monorepo**: Uber migrou para monorepo para simplificar dependências
- **Bazel**: Build system para compilação rápida em monorepo gigante
- **uDeploy**: Sistema de deploy interno com canary e rollback automático
- **Peloton**: Orquestrador de containers próprio (antes de adotar Kubernetes)
- **Cadence/Temporal**: Workflow engine para orquestração de processos

### Observabilidade
- **Jaeger**: Sistema de distributed tracing (open source pelo Uber)
- **M3**: Plataforma de métricas em escala massiva (open source)
- **uMonitor**: Alerting system com ML para detecção de anomalias
- **Service mesh**: Controle de tráfego, circuit breaking, rate limiting
- Dashboard de dependency graph para visualizar relações entre serviços

### Comunicação entre Serviços
- **gRPC**: Protocolo principal para comunicação síncrona
- **Apache Kafka**: Event streaming para comunicação assíncrona
- **Cherami**: Message queue proprietário (depois substituído por Kafka)
- **Schema registry**: Controle de evolução de contratos entre serviços
- **Circuit breakers**: Proteção contra falhas em cascata

---

## 4. Lições Aprendidas

### O que Funcionou
- Microservices permitiram escalar equipes independentemente
- Deploy independente acelerou velocity de cada equipe
- Ownership claro de serviços melhorou accountability
- Polyglot permitiu escolher melhor ferramenta por problema
- Event-driven architecture desacoplou domínios efetivamente

### O que Não Funcionou
- **Complexidade distribuída**: Debug e root cause analysis ficaram muito difíceis
- **Latency overhead**: Cascata de chamadas HTTP adicionou latência significativa
- **Data consistency**: Transações distribuídas são exponencialmente mais complexas
- **Testing**: Testes de integração entre centenas de serviços são quase impossíveis
- **Cognitive load**: Ninguém consegue entender o sistema completo
- **Operational overhead**: Cada serviço precisa de infra, monitoring, on-call
- **Dependency hell**: Ciclos de dependência entre serviços surgem organicamente

### Métricas de Complexidade
- Mais de 2.000 microservices
- Dezenas de milhões de RPCs por segundo entre serviços
- Centenas de bancos de dados
- Milhares de engenheiros com autonomia para criar serviços
- Grafo de dependências impossível de visualizar completamente

---

## 5. Aplicabilidade ao Nosso Contexto

### Quando Microservices Fazem Sentido
- Equipe grande (50+ engenheiros) com necessidade de autonomia
- Domínios de negócio claramente separáveis
- Necessidade de escalar componentes independentemente
- Deploy independente é critical path para velocidade
- Organização madura em DevOps e observabilidade

### Quando Microservices NÃO Fazem Sentido
- Equipe pequena (menos de 20 engenheiros)
- Produto ainda buscando product-market fit
- Domínios de negócio altamente acoplados
- Sem investimento em infraestrutura de suporte
- Complexidade de rede não justifica benefícios

### Recomendações Práticas
- [ ] Começar com monolito modular (boundaries claras, deploy único)
- [ ] Extrair serviços apenas quando dor concreta justificar
- [ ] Investir em observabilidade ANTES de distribuir
- [ ] Padronizar stack para reduzir carga cognitiva
- [ ] Usar DOMA como modelo se já tem muitos serviços
- [ ] Implementar contract testing entre serviços
- [ ] Medir latência end-to-end, não apenas por serviço
- [ ] Definir ownership claro para cada serviço com on-call
- [ ] Event-driven para desacoplamento entre domínios
- [ ] Manter monorepo ou tooling que simplifique gestão de repos
