# Integration Architecture — APIs, Eventos, iPaaS e Middleware Strategy

## Origem e Contexto

Arquitetura de integração é o design de como sistemas se comunicam e compartilham dados. Em
organizações modernas com dezenas a centenas de sistemas (SaaS, legados, custom builds),
integração é o tecido conectivo que determina se a organização opera como uma máquina coesa
ou como ilhas desconectadas que requerem trabalho manual para coordenar.

Historicamente, integração era sinônimo de ETL batch e middleware monolíticos (ESBs como
MuleSoft, TIBCO). A evolução trouxe APIs REST, event-driven architecture (Kafka, EventBridge),
iPaaS (Integration Platform as a Service — Workato, Tray.io), e GraphQL. O desafio moderno
não é falta de opções — é excesso. Cada padrão tem trade-offs, e a arquitetura errada gera
fragilidade, latência e custo exponencial de manutenção.

O princípio fundamental: integração é infraestrutura invisível — ninguém nota quando funciona,
todos notam quando falha. A qualidade da integração determina a velocidade com que a
organização pode mudar processos, adotar novos sistemas e escalar operações.

Referências: Gregor Hohpe ("Enterprise Integration Patterns"), Martin Fowler (event-driven
architecture), Thoughtworks (Technology Radar — integration patterns), APIGEE (API Management).

## Quando Usar

- No design de integração para novos sistemas ou plataformas
- Quando integrações existentes são frágeis, lentas ou caras de manter
- Ao consolidar stack de integração (muitas ferramentas, pouca coerência)
- Na preparação para event-driven architecture
- Ao avaliar iPaaS vs custom integration
- Em projetos de data platform que dependem de dados de múltiplos sistemas
- Na definição de API strategy para a organização

## Quando NÃO Usar

- Para integração pontual entre 2 sistemas (use a ferramenta mais simples disponível)
- Se há apenas 3-5 sistemas no total (custo de arquitetura formal não justifica)
- Como exercício teórico sem projetos de integração concretos
- Para impor padronização onde diversidade é saudável (nem toda integração precisa do mesmo padrão)

## Estrutura / Modelo

### Padrões de Integração

```
PADRÕES DE INTEGRAÇÃO
│
├── 1. API-LED (Síncrono)
│   ├── REST APIs: request-response, CRUD operations
│   ├── GraphQL: queries flexíveis, composição de dados
│   ├── gRPC: alto throughput, comunicação entre microservices
│   └── Trade-offs: acoplamento temporal, latência dependente do provider
│
├── 2. EVENT-DRIVEN (Assíncrono)
│   ├── Event Streaming: Kafka, Kinesis, Pulsar
│   ├── Event Bus: EventBridge, Google Pub/Sub, RabbitMQ
│   ├── CQRS: separação de leitura e escrita
│   └── Trade-offs: eventual consistency, complexidade de debug
│
├── 3. BATCH/ETL
│   ├── Scheduled jobs: cron, Airflow, dbt
│   ├── File transfer: SFTP, S3, blob storage
│   ├── CDC (Change Data Capture): Debezium, Fivetran
│   └── Trade-offs: latência (T+1), estado potencialmente desatualizado
│
├── 4. iPaaS (Integration Platform as a Service)
│   ├── Low-code: Workato, Tray.io, Make
│   ├── Enterprise: MuleSoft, Boomi
│   ├── Simple: Zapier, n8n
│   └── Trade-offs: vendor lock-in, custo em escala, limitações de customização
│
└── 5. HYBRID (Combinação)
    ├── API + Events: APIs para read, events para write
    ├── Sync + Async: síncrono para user-facing, async para background
    └── Custom + iPaaS: custom para core, iPaaS para long-tail
```

### Matriz de Decisão de Padrão

```
                    REAL-TIME NECESSÁRIO
                          │
     EVENT-DRIVEN         │     API (REST/GraphQL)
     (alta escala,        │     (request-response,
      desacoplado)        │      composição de dados)
                          │
──────────────────────────┼──────────────────────────
                          │
     BATCH/ETL            │     iPaaS / WEBHOOK
     (volume alto,        │     (simplicidade,
      latência OK)        │      poucos sistemas)
                          │
                    REAL-TIME NÃO NECESSÁRIO

     ALTA ESCALA/COMPLEXIDADE ←──→ BAIXA ESCALA/COMPLEXIDADE
```

### API Strategy Framework

```
API STRATEGY
│
├── 1. DESIGN PRINCIPLES
│   ├── API-First: API desenhada antes da implementação
│   ├── Contract-First: OpenAPI spec como contrato
│   ├── Versioning: semver, backward compatibility
│   └── Consistency: naming conventions, error formats, pagination
│
├── 2. API LAYERS
│   ├── System APIs: encapsulam sistemas individuais
│   ├── Process APIs: orquestram lógica de negócio cross-system
│   └── Experience APIs: otimizadas para consumidores específicos
│
├── 3. API MANAGEMENT
│   ├── API Gateway: auth, rate limiting, routing
│   ├── Developer Portal: docs, sandbox, keys
│   ├── Monitoring: latência, errors, usage
│   └── Lifecycle: versioning, deprecation, sunset
│
└── 4. API GOVERNANCE
    ├── API Review: toda nova API revisada antes de publish
    ├── Standards: guia de design com regras e exemplos
    ├── Catalog: inventário de todas as APIs disponíveis
    └── Ownership: cada API tem um time owner
```

### Integration Health Dashboard

```
SAÚDE DAS INTEGRAÇÕES
│
│ Integração       │ Padrão  │ SLA    │ Uptime │ Latência│ Erros/dia│ Status
│──────────────────┼─────────┼────────┼────────┼─────────┼──────────┼──────
│ CRM → Marketing  │ API     │ 99.9%  │ 99.95% │ 120ms   │ 12       │ ✓
│ ERP → Analytics  │ CDC     │ 99.5%  │ 99.8%  │ 4h lag  │ 3        │ ✓
│ Orders → Billing │ Events  │ 99.99% │ 99.99% │ 200ms   │ 0        │ ✓
│ HR → Payroll     │ Batch   │ 99%    │ 98.5%  │ T+1     │ 25       │ ⚠
│ Legacy → CRM     │ RPA     │ 95%    │ 93%    │ varies  │ 50       │ ✗
```

## Processo de Aplicação (step-by-step)

### Passo 1: Mapear Landscape de Integração (2-3 semanas)

- Inventariar todas as integrações existentes (incluindo informais)
- Para cada integração: sistemas conectados, padrão, volume, criticidade
- Identificar integrações frágeis (alta taxa de erro, manutenção frequente)
- Mapear dependências: o que quebra se esta integração falhar?
- Resultado: Integration Landscape Map

### Passo 2: Definir Princípios e Standards (1-2 semanas)

- Documentar princípios de integração (API-first, event-driven quando possível)
- Definir standards por tipo de integração (naming, auth, error handling, versioning)
- Escolher padrão default e exceções justificadas
- Publicar como Integration Design Guide

### Passo 3: Selecionar Stack (2-3 semanas)

- Avaliar necessidades: volume, latência, complexidade, skill do time
- Selecionar ferramentas por camada: API gateway, event broker, iPaaS, ETL
- Considerar: custo, lock-in, learning curve, ecossistema
- Documentar decisão como ADR

### Passo 4: Modernizar Integrações Críticas (3-6 meses)

- Priorizar integrações frágeis e de alta criticidade
- Migrar de RPA/batch para APIs/events quando possível
- Implementar monitoramento e alertas para integrações core
- Adicionar retry, circuit breaker e dead letter queue

### Passo 5: Implementar API Management (2-4 meses)

- API Gateway configurado (Kong, Apigee, AWS API Gateway)
- Developer Portal para documentação e onboarding
- API Catalog com todas as APIs internas e externas
- Processo de API review para novas APIs

### Passo 6: Governança Contínua (ongoing)

- Review mensal de Integration Health Dashboard
- API review para toda nova API ou mudança breaking
- Capacity planning para event broker e API gateway
- Deprecation process para APIs e integrações antigas

## Exemplos Práticos

### Exemplo 1: Evolução de Integration Stack (18 meses)

| Estado Atual | Problema | Estado Alvo | Timeline |
|-------------|---------|-------------|---------|
| 15 integrações por Zapier | Custo alto, sem visibilidade | Migrar core para n8n self-hosted | Q1-Q2 |
| CSV exports manuais entre ERP e BI | Dados desatualizados, erros | CDC com Debezium → data warehouse | Q2-Q3 |
| APIs sem gateway | Sem auth centralizada, sem metrics | Kong API Gateway | Q1 |
| Webhooks sem retry | Perda de dados quando receiver está down | Event queue (SQS) como buffer | Q2 |
| Point-to-point tudo | Espaguete de integrações | API-led com system/process/experience layers | Q3-Q4 |

### Exemplo 2: API Design Standards (resumo)

```
ENDPOINT: /api/v2/customers/{id}/orders
METHOD: GET
AUTH: Bearer token (OAuth 2.0)
RESPONSE FORMAT: JSON
PAGINATION: cursor-based (?cursor=abc&limit=50)
ERROR FORMAT: { "error": { "code": "NOT_FOUND", "message": "..." } }
RATE LIMIT: 100 req/min per client
VERSIONING: URL path (/v2/) com sunset policy de 12 meses
```

## Armadilhas Comuns

1. **Integration spaghetti**: Cada sistema integrado diretamente com todos os outros (N²).
2. **Over-architecting**: ESB enterprise para 5 integrações simples.
3. **iPaaS como solução universal**: iPaaS é ótimo para long-tail, ruim para high-throughput core.
4. **Ignorar idempotência**: Sem idempotência, retries criam dados duplicados.
5. **APIs sem versionamento**: Breaking change sem aviso = quebrar consumidores.
6. **Batch quando deveria ser real-time**: Dados T+1 para decisões que precisam ser real-time.
7. **Event-driven para tudo**: Eventual consistency é complexo; use só quando necessário.
8. **Sem monitoring**: Integração que falha silenciosamente = dados inconsistentes sem alerta.
9. **Vendor lock-in em iPaaS**: Migrar 200 workflows de um iPaaS para outro é custoso.
10. **Segurança como afterthought**: APIs sem autenticação adequada são vetor de ataque.

## Integração com Outros Frameworks

- **`frameworks/cio-engineer/cio-systems-rationalization.md`**: Integrações afetadas por racionalização
- **`frameworks/cio-engineer/cio-data-as-product.md`**: Integrações como source de data products
- **`frameworks/cio-engineer/cio-automation-first.md`**: Automação depende de integrações
- **`frameworks/cio-engineer/cloud-strategy.md`**: Cloud-native integration patterns
- **`frameworks/cto-architect/cto-architecture-as-strategy.md`**: Integration como decisão arquitetural
- **`frameworks/cto-architect/platform-strategy.md`**: Integration platform como componente
- **`frameworks/cio-engineer/security-posture.md`**: API security como pilar de security

## Referências

- Gregor Hohpe — "Enterprise Integration Patterns"
- Sam Newman — "Building Microservices" (capítulo de integração)
- Martin Fowler — "Event-Driven Architecture" (blog)
- Thoughtworks — "Technology Radar" (integration patterns)
- MuleSoft — "API-Led Connectivity" (whitepaper)
- Confluent — "Designing Event-Driven Systems" (ebook)
- Google Cloud — "API Design Guide"
- APIGEE — "Web API Design" (ebook)
