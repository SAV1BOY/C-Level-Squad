# CTO Reliability Engineering — Estratégia de Confiabilidade em Nível CTO

## Origem e Contexto

Reliability engineering é a disciplina que garante que sistemas de software funcionem de forma
confiável, previsível e resiliente — mesmo sob falhas. Para o CTO, reliability não é um problema
de ops — é uma decisão estratégica que impacta receita, confiança do cliente e velocidade de
inovação.

Cada hora de downtime custa receita direta, confiança acumulada e moral do time. Mas reliability
excessiva também tem custo: 99.999% de uptime custa 100x mais que 99.9% e pode ser desnecessário.
O trabalho do CTO é definir o nível correto de reliability para cada serviço e alocar o budget de
engenharia de acordo.

Este framework se baseia nas práticas de Site Reliability Engineering (SRE) do Google, no conceito
de error budgets, nos princípios de chaos engineering da Netflix, e na teoria de sistemas resilientes.
Adaptado para CTOs que precisam equilibrar reliability com velocidade de delivery.

## Quando Usar

- Na definição de SLOs (Service Level Objectives) para serviços críticos
- Quando incidentes frequentes afetam clientes e moral do time
- Na implementação de práticas de SRE ou equivalentes
- Ao decidir quanto investir em reliability vs features
- Quando o negócio depende de alta disponibilidade para receita
- Na construção de cultura de incident response

## Quando NÃO Usar

- Para sistemas internos de baixo impacto (proporcionalidade)
- Quando o problema é de product-market fit, não de reliability
- Como desculpa para não lançar features (perfectionism mascarado)
- Em fase de validação (MVP pode ter reliability menor)

## Estrutura / Modelo

### Modelo SLO-Budget (Service Level Objectives + Error Budgets)

```
┌─────────────────────────────────────────────────────┐
│           RELIABILITY STRATEGY                       │
│                                                      │
│  ┌──────────┐   ┌──────────┐   ┌──────────┐       │
│  │   SLIs   │──→│   SLOs   │──→│  ERROR   │       │
│  │(indicador)│   │(objetivo)│   │ BUDGET   │       │
│  └──────────┘   └──────────┘   └────┬─────┘       │
│                                      │              │
│                    ┌─────────────────┼──────┐       │
│                    │                 │      │       │
│              ┌─────▼─────┐   ┌──────▼────┐ │       │
│              │  BUDGET   │   │  BUDGET   │ │       │
│              │  HEALTHY  │   │ DEPLETED  │ │       │
│              │→ Ship fast│   │→ Fix first│ │       │
│              └───────────┘   └───────────┘ │       │
│                                            │       │
│  ┌──────────────────────────────────────────┘       │
│  │  INCIDENT RESPONSE + CHAOS ENGINEERING           │
│  │  + DISASTER RECOVERY                             │
│  └──────────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────┘
```

### Hierarquia de SLIs/SLOs

| Nível | SLI | SLO Típico | Quem Define |
|-------|-----|-----------|-------------|
| **Business** | Revenue impact, customer satisfaction | <X% revenue loss per incident | CTO + CEO |
| **Service** | Availability, latency, error rate | 99.9% availability, p99 <500ms | CTO + Engineering |
| **Infrastructure** | Uptime, capacity, failover time | 99.99% uptime, failover <30s | Platform team |

### Custo de Reliability

| SLO | Downtime/ano | Custo Relativo | Adequado Para |
|-----|-------------|---------------|---------------|
| 99% | 3.65 dias | 1x | Ferramentas internas |
| 99.9% | 8.76 horas | 5x | SaaS standard |
| 99.95% | 4.38 horas | 10x | SaaS enterprise |
| 99.99% | 52.6 minutos | 50x | Infraestrutura crítica |
| 99.999% | 5.26 minutos | 100x | Pagamentos, saúde |

## Processo de Aplicação (step-by-step)

### Step 1: Classificar Serviços por Criticidade

| Tier | Descrição | SLO Target | Exemplo |
|------|-----------|-----------|---------|
| **Tier 0** | Revenue-critical, zero tolerance | 99.99% | Checkout, payment |
| **Tier 1** | Core user experience | 99.95% | API principal, auth |
| **Tier 2** | Important but degradable | 99.9% | Search, recommendations |
| **Tier 3** | Internal/non-critical | 99% | Admin tools, analytics |

### Step 2: Definir SLIs e SLOs

Para cada serviço, definir:

```
SERVICE SLO CARD
━━━━━━━━━━━━━━━━
Service: [nome]
Tier: [0/1/2/3]
Owner (DRI): [nome/time]

SLIs:
- Availability: % of successful requests (non-5xx)
- Latency: p50, p95, p99 response time
- Error Rate: % of requests returning errors

SLOs:
- Availability: >= 99.95% (rolling 30 days)
- Latency: p99 < 500ms
- Error Rate: < 0.1%

Error Budget (30 dias):
- 0.05% of requests = ~21.6 minutes of downtime
- Current burn rate: [X min consumed this month]
```

### Step 3: Implementar Error Budgets

Como operar com error budgets:

**Budget saudável** (>50% restante):
- Priorizar features e velocity
- Permitir deployments mais arriscados
- Encorajar experimentação

**Budget baixo** (<25% restante):
- Reduzir velocity, priorizar estabilidade
- Code freeze para mudanças de alto risco
- Focar em debt reduction e hardening

**Budget esgotado** (0% restante):
- Feature freeze até recuperar budget
- All-hands em reliability
- Post-mortem obrigatório para root causes

### Step 4: Incident Response Framework

Definir processo claro de resposta a incidentes:

```
INCIDENT SEVERITY LEVELS
━━━━━━━━━━━━━━━━━━━━━━━━
SEV-1 (Critical): Revenue impacted, all customers affected
  → Resposta: <5 min, War room, Comms every 30 min
SEV-2 (Major): Significant degradation, many customers
  → Resposta: <15 min, Incident channel, Comms every 1h
SEV-3 (Minor): Partial degradation, some customers
  → Resposta: <1h, Ticket + owner assigned
SEV-4 (Low): Cosmetic/minor, workaround available
  → Resposta: Next business day
```

**Roles durante incidente**:
- **Incident Commander**: coordena resposta, comunica stakeholders
- **Technical Lead**: lidera investigação e fix
- **Communications Lead**: status page, clientes, interno

### Step 5: Post-Mortem Culture

Post-mortem blameless para todo SEV-1 e SEV-2:

```
POST-MORTEM TEMPLATE
━━━━━━━━━━━━━━━━━━━━
Incident ID:
Date/Time:
Duration:
Impact: [customers affected, revenue impact]
Summary: [2-3 sentences]
Timeline: [detailed minute-by-minute]
Root Cause: [technical root cause]
Contributing Factors: [organizational/process factors]
What Went Well:
What Could Be Improved:
Action Items:
  - [action] — DRI: [nome] — Deadline: [data] — Priority: [P0/P1/P2]
Follow-up Review Date:
```

**Regra**: sem culpados. Foco em sistema, não em pessoas.

### Step 6: Chaos Engineering

Testar proativamente a resiliência:

1. **Game Days**: simulação de falha com time preparado
2. **Chaos Experiments**: injeção controlada de falhas em produção
3. **Disaster Recovery Drills**: teste de DR completo trimestral
4. **Load Testing**: simular picos de tráfego previstos

**Progressão**:
- Nível 1: kill um pod/container e verificar recovery
- Nível 2: simular falha de um serviço dependente
- Nível 3: simular falha de AZ/região
- Nível 4: simular falha do database/storage

### Step 7: Disaster Recovery

Definir e testar plano de DR:

| Métrica | Definição | Target por Tier |
|---------|-----------|----------------|
| **RTO** (Recovery Time Objective) | Tempo máximo para restaurar | Tier 0: <15min, Tier 1: <1h |
| **RPO** (Recovery Point Objective) | Perda máxima de dados | Tier 0: 0, Tier 1: <5min |
| **MTTR** (Mean Time to Recovery) | Tempo médio real de recovery | Track e melhorar continuamente |

## Exemplos Práticos

### Exemplo 1: SaaS com SLO de 99.95%

**Error budget mensal**: 21.6 minutos de downtime permitido
**Mês atual**: 2 incidentes consumiram 18 minutos
**Decisão**: budget baixo → feature freeze na última semana, foco em stability
**Ação**: fix 3 single points of failure identificados nos post-mortems

### Exemplo 2: E-commerce na Black Friday

**Preparação** (2 meses antes):
- Load test simulando 5x tráfego normal
- Chaos experiment: falha de CDN, falha de gateway de pagamento
- DR drill: failover para região secundária
- Runbook atualizado para cenários específicos de Black Friday
- War room staffed 24h durante o evento

## Armadilhas Comuns

1. **SLO como SLA**: confundir objetivos internos com compromissos contratuais
2. **100% uptime target**: impossível e caro demais de perseguir
3. **Blame culture**: culpar pessoas por incidentes mata aprendizado
4. **Heroics as normal**: depender de heróis em vez de sistemas resilientes
5. **Post-mortem sem follow-up**: escrever post-mortem e não executar action items
6. **Over-alerting**: tantos alertas que time ignora todos (alert fatigue)
7. **DR never tested**: plano de DR que nunca foi testado não é um plano
8. **Reliability as ops problem**: CTO delegando reliability sem ownership estratégico

## Integração com Outros Frameworks

| Framework | Relação |
|-----------|---------|
| `frameworks/cto-architect/cto-architecture-as-strategy.md` | Reliability como quality attribute |
| `frameworks/cto-architect/cto-engineering-excellence.md` | Qualidade de código impacta reliability |
| `frameworks/cto-architect/cto-developer-experience.md` | On-call experience como parte de DX |
| `frameworks/cto-architect/platform-strategy.md` | Platform reliability |
| `checklists/cto/platform-reliability-audit.md` | Auditoria de reliability |
| `checklists/cto/security-by-design-audit.md` | Security como pilar de reliability |

## Referências

- Betsy Beyer et al., "Site Reliability Engineering" (Google, O'Reilly, 2016)
- Niall Murphy et al., "The Site Reliability Workbook" (Google, O'Reilly, 2018)
- Casey Rosenthal & Nora Jones, "Chaos Engineering" (O'Reilly, 2020)
- John Allspaw, "Incident Analysis and Software Engineering" (Adaptive Capacity Labs)
- Will Larson, "An Elegant Puzzle" — SRE and engineering management
- Charity Majors, "Observability Engineering" (O'Reilly, 2022)
- C-Level Squad: `checklists/cto/platform-reliability-audit.md`
