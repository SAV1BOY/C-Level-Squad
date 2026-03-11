# Building Microservices — Sam Newman (2015, 2nd edition 2021)

## Resumo Executivo

Newman apresenta princípios e práticas para projetar, construir e operar sistemas baseados
em microservices. O livro é pragmático: não advoga microservices como solução universal,
mas oferece guidance para quando e como adotá-los efetivamente. Abrange desde modelagem
de serviços até deployment, testing, monitoring e migração de monólitos.

A tese central: microservices são um meio para um fim (independent deployability, team
autonomy, technology heterogeneity), não um fim em si mesmos.

## Conceitos-Chave

### O que são Microservices
- Serviços pequenos, independentemente deployáveis, que se comunicam via rede
- Cada serviço possui seu próprio data store (não compartilha database)
- Organizados ao redor de business capabilities (não camadas técnicas)
- Permitem que times diferentes evoluam serviços independentemente

### Key Benefits
- **Independent deployability**: Deploy sem coordenação com outros serviços
- **Technology heterogeneity**: Cada serviço pode usar a melhor tecnologia para seu contexto
- **Organizational alignment**: Serviços alinhados com times (Conway's Law)
- **Resilience**: Falha em um serviço não cascata para todo o sistema
- **Scaling**: Escalar apenas os serviços que precisam, não o sistema inteiro

### When NOT to Use Microservices
- Quando a equipe é pequena (overhead > benefício)
- Quando o domínio não é bem compreendido (decomposição prematura cria acoplamento)
- Quando não tem capacidade operacional (monitoring, deployment, debugging distribuído)
- Para startups em estágio inicial — monólito é quase sempre melhor para começar
- "Microservices are not a good default architecture choice"

### Domain-Driven Design (DDD) e Service Boundaries
- **Bounded Context**: Cada serviço encapsula um contexto delimitado do domínio
- **Aggregate**: Unidade de consistência dentro de um serviço
- **Context Map**: Mapa de relacionamentos entre bounded contexts
- Definir boundaries corretamente é a decisão arquitetural mais importante

### Communication Patterns
- **Synchronous** (request-response): REST, gRPC — simples, mas cria coupling
- **Asynchronous** (event-driven): Message queues, event streaming — loose coupling
- **Choreography**: Serviços reagem a eventos sem coordenador central
- **Orchestration**: Um serviço central coordena a sequência de chamadas
- Prefira choreography quando possível — menos single points of failure

### Data Ownership
- Cada serviço possui e gerencia seus próprios dados
- Shared database é anti-pattern — cria coupling entre serviços
- Consistência eventual (eventual consistency) em vez de transações distribuídas
- Sagas como pattern para transações que cruzam serviços

### Deployment Strategies
- **Independent deployment**: Cada serviço deployado separadamente (objetivo)
- **Blue-Green deployment**: Duas versões em paralelo, switch instantâneo
- **Canary releases**: Deploy gradual para subset de tráfego
- **Feature flags**: Ativar/desativar features em runtime sem deploy

### Observability
- **Logging**: Structured logging com correlation IDs entre serviços
- **Metrics**: Service-level metrics + business metrics
- **Distributed tracing**: Seguir request through multiple services (Jaeger, Zipkin)
- "If you can't observe it, you can't operate it"

### Migration Patterns (Monolith to Microservices)
- **Strangler Fig**: Interceptar chamadas ao monólito e redirecionar para novo serviço
- **Branch by Abstraction**: Criar abstração no monólito, implementar nova versão por trás
- **Parallel Run**: Executar ambas implementações e comparar resultados
- **Incremental migration**: Um serviço de cada vez, do menos arriscado ao mais

## Frameworks e Modelos

### Service Boundary Decision Framework
1. O serviço tem um bounded context claro no domínio?
2. Pode ser deployed independentemente?
3. O time pode operar o serviço end-to-end?
4. A comunicação entre serviços é através de APIs bem definidas?
5. Se a resposta a qualquer pergunta é "não", reconsidere a decomposição

### Migration Readiness Assessment
1. Temos observability adequada? (logging, metrics, tracing)
2. Temos CI/CD pipeline automatizada?
3. Temos capacidade de operar N serviços? (monitoring, alerting, on-call)
4. Entendemos o domínio bem o suficiente para definir boundaries?
5. O monólito está causando problemas reais? (não resolva problema que não existe)

## Aplicação ao C-Level Squad

### Para o CEO Agent
- Microservices são decisão de negócio (team autonomy, speed to market), não apenas técnica
- Validar que a motivação para microservices é clara: que problema de negócio resolve?
- Migração é investimento de longo prazo — alinhar expectativas de timeline e custo

### Para o CTO Agent
- Avaliar readiness antes de migrar — operational maturity é pré-requisito
- DDD como ferramenta de alinhamento negócio-tecnologia na definição de serviços
- "Start with the monolith" — decomponha apenas quando há razão clara de negócio
- Independent deployability como North Star da arquitetura

### Para o CFO Agent
- Custo operacional de microservices é maior que monólito (mais infra, mais complexity)
- O ROI vem de velocity (time to market) e resilience (menos downtime), não de custo menor
- Modelar TCO incluindo observability, deployment automation e operational overhead

### Para o CMO Agent
- Microservices permitem experimentação mais rápida em features de produto
- Feature flags habilitam A/B testing sem dependência de release cycles
- Independência de serviços permite que marketing-related features evoluam mais rápido

### Para o COO Agent
- Operational complexity aumenta significativamente com microservices
- Investir em observability e incident response antes de migrar
- Runbooks, alerting e on-call processes para N serviços vs. 1 monólito

## Takeaways Acionáveis (top 5)

1. **Start with the monolith** — Não comece com microservices. Comece monólito, entenda o
   domínio e decomponha quando houver razão clara de negócio ou escala.

2. **Define boundaries by domain** — Use DDD e bounded contexts para definir serviços.
   Boundaries por camada técnica (serviço de database, serviço de cache) é anti-pattern.

3. **Independent deployability é o objetivo** — Se precisa coordenar deploys entre serviços,
   não tem microservices — tem um "distributed monolith" (pior dos dois mundos).

4. **Invista em observability primeiro** — Antes de decompor, garanta logging estruturado,
   metrics e distributed tracing. Sem isso, debugging distribuído é pesadelo.

5. **Migre incrementalmente** — Strangler Fig pattern. Um serviço de cada vez. Comece pelo
   menos arriscado. Nunca "big bang migration".

## Citações-Chave

> "Microservices are not a free lunch."

> "If you can't build a well-structured monolith, what makes you think
> microservices are the answer?"

> "The golden rule: can you make a change to a service and deploy it by itself
> without changing anything else?"

> "Don't share databases. If you share databases, you're not doing microservices."

> "Microservices should be organized around business capabilities, not technical ones."

## Quando Consultar

- Ao avaliar decisão de migrar de monólito para microservices
- Na definição de service boundaries e architecture
- Ao escolher communication patterns entre serviços
- Para migration strategy (strangler fig, parallel run)
- Na definição de observability e operational requirements
- Quando "distributed monolith" está causando problemas

## Referências Cruzadas

- **Martin — Clean Architecture**: Princípios de design que se aplicam dentro de cada serviço
- **Skelton — Team Topologies**: Organização de times alinhada com service boundaries
- **Forsgren — Accelerate**: DORA metrics como validação de delivery performance
- **Kim — Phoenix Project**: DevOps practices necessárias para operar microservices
- **Goldratt — The Goal**: Throughput e flow como motivação para independent deployability
- **Weill — IT Governance**: Governance em ambientes distribuídos
