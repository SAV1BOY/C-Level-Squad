# Framework MLOps — Operacionalização de Machine Learning em Produção

## Propósito e Contexto

MLOps (Machine Learning Operations) é o conjunto de práticas para deploy, monitoring e gestão
de modelos de ML em produção de forma confiável e escalável. É a ponte entre o notebook do
data scientist e o sistema em produção que serve milhões de usuários. Sem MLOps, modelos ficam
presos em POCs, degradam silenciosamente em produção, e cada deploy é uma aventura manual.

O framework MLOps é para DevOps o que ML é para software — uma extensão que adiciona
complexidades específicas: dados mudam, modelos degradam, performance depende de distribuição
de inputs, e retraining é parte do ciclo de vida normal. Este framework adapta práticas de
MLOps para empresas em diferentes estágios de maturidade de AI.

## Quando Usar

- Ao preparar o primeiro modelo de ML para produção
- Quando modelos em produção degradam sem explicação
- Na padronização de processos entre múltiplos times de ML
- Ao escalar de 1-2 modelos para dezenas
- Na construção de ML Platform interna
- Ao reduzir time-to-production para novos modelos

## Componentes do Framework

### 1. MLOps Maturity Levels

**Level 0: Manual**
- Training manual em notebooks
- Deploy manual (copiar artefatos)
- Sem monitoring de performance
- Sem versionamento de dados ou modelos
- Adequado para: POCs, primeiros modelos

**Level 1: Pipeline Automation**
- Pipeline de training automatizado (trigger manual)
- Deploy automatizado via CI/CD
- Versionamento de modelos e dados
- Monitoring básico (uptime, latência)
- Adequado para: 1-5 modelos em produção

**Level 2: CI/CD for ML**
- Training automático com triggers (schedule, data drift)
- A/B testing de modelos em produção
- Feature store centralizado
- Monitoring de performance do modelo (accuracy, drift)
- Adequado para: 5-20 modelos em produção

**Level 3: Full Automation**
- Retraining automático baseado em drift detection
- Champion/challenger rollout automatizado
- Governance e audit trail completos
- Self-service para data scientists
- Adequado para: 20+ modelos, AI como core business

### 2. Componentes da ML Platform

```
EXPERIMENTAÇÃO          FEATURE STORE         TRAINING PIPELINE
├── Notebooks           ├── Feature            ├── Data Validation
│   (Jupyter, Colab)    │   Registry            ├── Feature Engineering
├── Experiment          ├── Online Serving     ├── Model Training
│   Tracking            │   (low-latency)      ├── Model Evaluation
│   (MLflow, W&B)       ├── Offline Serving    └── Model Registry
└── Colaboração         │   (batch)
                        └── Feature
                            Monitoring

SERVING                 MONITORING             GOVERNANCE
├── Model Serving       ├── Data Drift         ├── Model Cards
│   (TF Serving,        │   Detection          ├── Audit Trail
│    Seldon, BentoML)   ├── Performance        ├── Access Control
├── A/B Testing         │   Monitoring         ├── Lineage
├── Feature Flag        ├── Alerting           └── Compliance
│   Integration         └── Dashboards
└── Auto-scaling
```

### 3. Pipeline de ML (End-to-End)

```
DATA INGESTION → VALIDATION → TRANSFORM → TRAIN → EVALUATE → REGISTER → DEPLOY → MONITOR
      |              |            |          |         |           |          |         |
      v              v            v          v         v           v          v         v
   Schedule/     Schema +     Feature    Hyperpar.  Compare    Version    Canary/   Drift +
   Trigger       Stats        Engineer.  Tuning     baseline   + Tag      Shadow    Perf.
                 checks                                                   deploy    metrics
```

### 4. Feature Store

O feature store centraliza a engenharia e o serving de features:

**Benefícios:**
- Reutilização de features entre modelos e times
- Consistência: mesma feature em training e serving
- Descoberta: catálogo de features disponíveis
- Ponto-no-tempo: features históricas para training correto
- Monitoramento: drift detection por feature

**Componentes:**
- Feature Registry: catálogo de todas as features
- Online Store: serving low-latency para inference real-time
- Offline Store: dados históricos para training
- Transformation Pipeline: código que gera as features

## Processo Passo-a-Passo

### Fase 1: Foundation (Level 0→1) — 4-8 semanas
1. Padronizar ambientes de desenvolvimento (Docker, conda)
2. Implementar experiment tracking (MLflow ou W&B)
3. Versionamento de dados (DVC) e modelos
4. Primeiro pipeline automatizado (Airflow, Prefect, Dagster)
5. Model serving padronizado (API endpoint)
6. Monitoring básico (uptime, latência, error rate)

### Fase 2: Automation (Level 1→2) — 2-3 meses
1. CI/CD para pipelines de ML (test, validate, deploy)
2. Feature store (Feast, Tecton, ou custom)
3. A/B testing framework para modelos
4. Data validation automatizada (Great Expectations)
5. Performance monitoring (accuracy, drift metrics)
6. Model registry com approval workflow

### Fase 3: Optimization (Level 2→3) — 3-6 meses
1. Drift detection com retraining automático
2. Champion/challenger deployment automatizado
3. Governance: model cards, audit trail, lineage
4. Self-service platform para data scientists
5. Cost optimization (GPU scheduling, spot instances)
6. Multi-model management e orquestração

## Template de ML Pipeline Spec

```markdown
# ML Pipeline: [Nome do Modelo]

## Trigger
- Schedule: [cron expression]
- Data trigger: [quando novos dados chegam]
- Drift trigger: [quando drift > threshold]

## Data
- Source: [tabela/API/stream]
- Validation: [checks aplicados]
- Features: [lista de features do feature store]
- Training window: [período de dados para treinar]

## Training
- Algorithm: [tipo de modelo]
- Hyperparameters: [config ou search space]
- Compute: [GPU type, # instances]
- Duration estimada: [tempo]

## Evaluation
- Metrics: [lista com thresholds]
- Baseline comparison: [modelo atual vs. novo]
- Fairness checks: [métricas de bias]
- Auto-promote criteria: [quando deploy automático]

## Serving
- Endpoint: [URL]
- Latency SLA: [p99]
- Throughput: [requests/sec]
- Fallback: [comportamento quando modelo falha]

## Monitoring
- Drift metrics: [PSI, KS, etc.]
- Performance metrics: [accuracy, F1, business KPI]
- Alert thresholds: [quando alertar]
- Retraining trigger: [critério automático]
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Model deployment time | < 1 dia (Level 2+) | Por deploy |
| Pipeline success rate | > 95% | Semanal |
| Model serving latency (p99) | < SLA definido por modelo | Contínuo |
| Drift detection coverage | 100% dos modelos em produção | Contínuo |
| Feature reuse rate | > 30% das features usadas por 2+ modelos | Trimestral |
| Time-to-retrain | < 4 horas (automatizado) | Por retraining |
| Model rollback time | < 5 minutos | Por incidente |

## Referências Cruzadas

- `frameworks/caio-architect/ai-maturity-model.md` — Infra como dimensão de maturidade
- `frameworks/caio-architect/ai-product-development.md` — Ciclo de vida do produto AI
- `frameworks/caio-architect/responsible-ai.md` — Fairness monitoring em MLOps
- `frameworks/caio-architect/ai-governance.md` — Governance em pipelines de ML
- `frameworks/cto-architect/platform-strategy.md` — ML Platform como extensão da plataforma
- `frameworks/cto-architect/engineering-excellence.md` — CI/CD e práticas de engenharia para ML
- `frameworks/cio-engineer/cloud-strategy.md` — Infraestrutura cloud para ML
