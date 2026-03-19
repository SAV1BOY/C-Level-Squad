# SRE Basics — Site Reliability Engineering Essentials

> **Domínio:** Engineering & Tech
> **Autor de referência:** Google SRE (Ben Treynor Sloss), "Site Reliability Engineering" book
> **Uso primário:** Garantir confiabilidade de sistemas em produção com abordagem baseada em engenharia, não em operações heroicas.
> **Agente responsável:** cto-architect / cio-engineer

---

## Origem e Contexto

Site Reliability Engineering (SRE) foi criado por Ben Treynor Sloss no Google em 2003. A definição clássica: **"SRE é o que acontece quando você pede a um engenheiro de software para projetar uma função de operações."**

O princípio fundamental: confiabilidade é a feature mais importante de qualquer sistema. Se o sistema está fora do ar, nenhuma feature importa. Mas 100% de confiabilidade é impossível (e economicamente irracional). SRE resolve isso com conceitos quantitativos:

- **SLI (Service Level Indicator):** Métrica que mede a confiabilidade percebida pelo usuário. Ex.: % de requests < 200ms.
- **SLO (Service Level Objective):** Target para o SLI. Ex.: 99.9% dos requests < 200ms em janela de 30 dias.
- **SLA (Service Level Agreement):** Contrato com consequências financeiras se o SLO não for atingido. Ex.: créditos se uptime < 99.9%.
- **Error Budget:** A diferença entre 100% e o SLO. Se SLO = 99.9%, o error budget é 0.1% (43 minutos/mês). Esse budget pode ser "gasto" em deploys, experimentos e manutenção.

O insight revolucionário: **error budgets alinham desenvolvimento e operações.** Quando o budget está saudável, deploys rápidos são incentivados. Quando está esgotado, o time para e foca em estabilidade.

---

## Quando Usar

- Em QUALQUER sistema em produção que atende usuários (internos ou externos).
- Como framework de confiabilidade para a WBR — SLIs são métricas obrigatórias.
- Ao definir contratos com clientes (SLAs derivados de SLOs).
- Para resolver o eterno conflito entre "mover rápido" (dev) e "manter estável" (ops).
- Na priorização de investimento em infra e operações.

---

## Quando NÃO Usar

- Para sistemas de desenvolvimento/staging — SLOs são para produção.
- Como dogma — o Google tem 10K+ SREs. Uma startup com 20 devs não precisa do mesmo rigor.
- Para evitar deploys — error budget não é desculpa para parar de entregar.
- Sem buy-in de engenharia — SRE funciona quando devs e SREs são parceiros, não adversários.

---

## Estrutura / Modelo

### Hierarquia SLI → SLO → SLA → Error Budget

```
┌─────────────────────────────────────────────────────────────────────┐
│                   SRE RELIABILITY PYRAMID                            │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  SLA (Service Level Agreement)                                       │
│  └── Contrato com cliente. Consequências financeiras.               │
│  └── Ex.: "Uptime ≥ 99.9% ou crédito de 10%."                     │
│                                                                      │
│  SLO (Service Level Objective)    ← Internal target (mais rígido)   │
│  └── Meta interna. SLO deve ser mais rígido que SLA.               │
│  └── Ex.: "99.95% uptime" (quando SLA é 99.9%).                   │
│                                                                      │
│  SLI (Service Level Indicator)    ← Métrica observada               │
│  └── Medição real de confiabilidade percebida pelo usuário.        │
│  └── Ex.: "% de requests com latência < 200ms."                   │
│                                                                      │
│  Error Budget = 100% - SLO                                          │
│  └── Ex.: SLO 99.95% → Error budget = 0.05% = ~22 min/mês        │
│  └── Quando budget esgota → freeze de deploys, foco em             │
│      estabilidade. Quando saudável → velocidade máxima.            │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

### SLI Categories

| Categoria | SLI Típico | Medição |
|-----------|-----------|---------|
| **Availability** | % de requests com sucesso (não-5xx) | Load balancer logs |
| **Latency** | % de requests < threshold (ex.: 200ms) | APM / tracing |
| **Throughput** | Requests/segundo dentro da capacidade | Monitoring |
| **Correctness** | % de responses com dados corretos | Synthetic monitoring |
| **Freshness** | % de dados atualizados dentro do SLA | Data pipeline monitoring |

---

## Processo de Aplicação (step-by-step)

### Step 1: Identificar User Journeys Críticas
Antes de definir SLOs, mapear as jornadas mais importantes para o usuário:
- Login e autenticação.
- Ação principal do produto (ex.: criar pedido, gerar relatório).
- Pagamento/checkout.
- APIs consumidas por parceiros.

Cada user journey terá SLIs e SLOs específicos.

### Step 2: Definir SLIs
Para cada user journey, escolher 1-3 SLIs:
- **Availability:** O request funcionou?
- **Latency:** Quanto tempo demorou?
- **Correctness:** O resultado está certo?

Regra: medir do ponto de vista do USUÁRIO, não do servidor. Latência no load balancer > latência no app server.

### Step 3: Definir SLOs
Para cada SLI, definir target e janela:
- **Target:** 99.9%, 99.95%, 99.99% (quanto maior, mais caro).
- **Janela:** Rolling 30 dias é o padrão.
- **Começar conservador:** É mais fácil apertar o SLO depois do que relaxar.

Regra de ouro: **SLO deve refletir a expectativa real do usuário, não a capacidade técnica.** Se o usuário espera resposta em < 500ms, o SLO de latência é baseado nisso.

### Step 4: Calcular Error Budget
Error budget = (1 - SLO) × janela

| SLO | Error Budget (30 dias) | Significado |
|-----|----------------------|-------------|
| 99% | 7h 18min | ~2h de downtime por semana OK |
| 99.9% | 43min | ~10min de downtime por semana |
| 99.95% | 22min | ~5min de downtime por semana |
| 99.99% | 4.3min | Quase zero tolerance |

### Step 5: Definir Error Budget Policy
O que acontece quando o error budget se esgota:
- **Budget saudável (> 50%):** Deploy freely, experimentar, risk-on.
- **Budget consumed (< 25%):** Cautela. Canary deploys obrigatórios. Review de changes.
- **Budget esgotado (0%):** Freeze de feature deploys. Apenas bug fixes e reliability improvements.

### Step 6: Implementar Observability Stack
Para medir SLIs, é preciso observability:
- **Logs:** Structured logging (JSON), centralizado (ELK, Datadog, Loki).
- **Metrics:** Time-series (Prometheus, CloudWatch, Datadog).
- **Traces:** Distributed tracing (Jaeger, Zipkin, Datadog APM).
- **Dashboards:** SLI/SLO dashboard atualizado em real-time.
- **Alerting:** Alertas baseados em SLO burn rate, não em thresholds estáticos.

### Step 7: Incident Management
Quando algo quebra:
1. **Detect:** Alerta baseado em SLO burn rate dispara.
2. **Triage:** On-call classifica severidade (`frameworks/operating-system/escalation-ladders.md`).
3. **Mitigate:** Restaurar serviço (rollback, failover, scale).
4. **Resolve:** Corrigir root-cause.
5. **Postmortem:** Blameless postmortem para TODA incident SEV1/SEV2.

### Step 8: Toil Reduction
Toil = trabalho operacional manual, repetitivo e sem valor duradouro. SRE visa reduzir toil a < 50% do tempo:
- Automatizar deploys, rollbacks, scaling.
- Automatizar alerting e runbooks (auto-remediation).
- Eliminar toil via platform engineering (`frameworks/engineering-tech/platform-engineering.md`).

---

## Exemplos Práticos

### Exemplo: SaaS B2B com 5K Clientes

**SLOs definidos:**

| User Journey | SLI | SLO | Error Budget (30d) |
|-------------|-----|-----|-------------------|
| API Principal | Availability (non-5xx) | 99.95% | 22 min |
| API Principal | Latency (p99 < 500ms) | 99.9% | 43 min |
| Dashboard | Page Load < 3s | 99.5% | 3.6h |
| Webhooks | Delivery success | 99.9% | 43 min |

**Error Budget Policy:**
- > 50% remaining: deploy daily, feature flags.
- 25-50%: canary deploys, extended testing.
- < 25%: feature freeze, reliability sprint.
- 0%: war room, every engineer on reliability.

---

## Armadilhas Comuns

1. **SLO muito apertado:** 99.99% parece bom mas é caro demais para maioria dos serviços. Começar em 99.9%.
2. **SLO sem medição:** Definir SLO sem implementar observability. SLO sem medição é ficção.
3. **SLA = SLO:** SLA deve ser menos rígido que SLO. Se SLO = SLA, toda violação de SLO é violação contratual.
4. **Error budget como punição:** Error budget é ferramenta de alinhamento, não de blame.
5. **Medir métricas do servidor, não do usuário:** Latência no servidor != latência percebida pelo usuário. Medir end-to-end.
6. **Alert fatigue:** Muitos alertas triviais. Alertar baseado em SLO burn rate, não em thresholds arbitrários.
7. **Postmortem como blamefest:** Blameless postmortem é fundamental. Se as pessoas têm medo de reportar falhas, as falhas são escondidas.
8. **Toil aceito como normal:** "É assim que sempre foi" não é razão para manter toil. Automatizar é investimento.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/engineering-tech/dora-metrics.md` | MTTR é tanto DORA metric quanto SRE metric. SLOs complementam DORA. |
| `frameworks/engineering-tech/platform-engineering.md` | Plataforma entrega observability e incident tools como self-service. |
| `frameworks/engineering-tech/architecture-patterns.md` | Arquitetura impacta confiabilidade. Microservices requerem SLOs por serviço. |
| `frameworks/operating-system/escalation-ladders.md` | Incident severity classification alinha com escalation ladder. |
| `frameworks/operating-system/wbr-mbr-qbr.md` | SLIs e error budget status são métricas da WBR do CTO. |
| `frameworks/it-information/itil-light.md` | ITIL incident management complementa SRE incident process. |
| `checklists/incident-communication-quality.md` | Checklist para comunicação durante incidents. |

---

## Referências

- Beyer, B. et al. (2016). *Site Reliability Engineering: How Google Runs Production Systems*. O'Reilly.
- Beyer, B. et al. (2018). *The Site Reliability Workbook*. O'Reilly.
- Murphy, N. et al. (2020). *Building Secure and Reliable Systems*. O'Reilly.
- Google Cloud. "SRE Fundamentals." sre.google.
- Sloss, B. "SRE: The Most Important Feature." usenix.org.
