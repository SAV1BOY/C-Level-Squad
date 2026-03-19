# MLOps — Framework de Operacionalização do Ciclo de Vida de Machine Learning

## Origem e Contexto

MLOps (Machine Learning Operations) é a disciplina que aplica práticas de DevOps ao ciclo de vida
de machine learning, garantindo que modelos não apenas funcionem em notebooks, mas operem de forma
confiável, escalável e auditável em produção.

O problema central que MLOps resolve é o "ML deployment gap": a distância entre um modelo que funciona
no ambiente de desenvolvimento e um modelo que gera valor em produção de forma sustentável. Estima-se
que 87% dos modelos de ML nunca chegam a produção — e dos que chegam, muitos degradam sem monitoramento.

Este framework se baseia nas práticas de Google (MLOps maturity levels), Netflix (ML platform),
Uber (Michelangelo), e nos princípios de "Reliable Machine Learning" de Cathy Chen et al.
Adaptado para organizações de diferentes tamanhos e maturidades.

## Quando Usar

- Ao colocar qualquer modelo de ML em produção
- Na construção de uma platform de ML interna
- Quando modelos em produção degradam sem explicação
- Na padronização do ciclo de vida de ML entre times
- Ao escalar de 1-2 modelos para dezenas em produção
- Na definição de processos de retraining e monitoramento

## Quando NÃO Usar

- Para protótipos e POCs que não vão a produção
- Quando o overhead de MLOps é maior que o valor do modelo
- Em análises ad-hoc ou one-off predictions
- Como substituto para boas práticas de engenharia de software (MLOps complementa, não substitui)

## Estrutura / Modelo

### Ciclo de Vida MLOps

```
┌─────────────────────────────────────────────────────────────┐
│                    MLOps LIFECYCLE                            │
│                                                              │
│  ┌──────┐   ┌──────┐   ┌──────┐   ┌──────┐   ┌──────┐    │
│  │ DATA │──→│TRAIN │──→│ EVAL │──→│DEPLOY│──→│MONITOR│    │
│  │  ENG │   │      │   │      │   │      │   │      │     │
│  └──┬───┘   └──┬───┘   └──┬───┘   └──┬───┘   └──┬───┘    │
│     │          │          │          │          │           │
│  ┌──▼──────────▼──────────▼──────────▼──────────▼───┐      │
│  │           FEATURE STORE + MODEL REGISTRY          │      │
│  └──────────────────────┬────────────────────────────┘      │
│                         │                                    │
│  ┌──────────────────────▼────────────────────────────┐      │
│  │      CI/CD PIPELINE + INFRASTRUCTURE AS CODE       │      │
│  └───────────────────────────────────────────────────┘      │
│                                                              │
│  ◄─────────────── FEEDBACK LOOP ─────────────────────►      │
└─────────────────────────────────────────────────────────────┘
```

### Níveis de Maturidade MLOps

| Nível | Nome | Descrição | Indicadores |
|-------|------|-----------|-------------|
| **0** | Manual | Tudo manual: treinamento, deploy, monitoramento | Notebooks, deploy ad-hoc |
| **1** | Pipelines | Pipelines de treinamento automatizados | Orquestrador (Airflow/Prefect) |
| **2** | CI/CD para ML | Testes automatizados, deploy automatizado | Automated testing, staging env |
| **3** | Full MLOps | Monitoramento, retraining automático, feature store | Platform completa, self-service |

### Componentes Core

| Componente | Função | Ferramentas Exemplo |
|-----------|--------|---------------------|
| **Feature Store** | Centralizar e servir features | Feast, Tecton, Hopsworks |
| **Model Registry** | Versionar e catalogar modelos | MLflow, Weights & Biases, Vertex AI |
| **Experiment Tracking** | Registrar experimentos e resultados | MLflow, W&B, Neptune |
| **Pipeline Orchestration** | Orquestrar workflows de ML | Airflow, Prefect, Kubeflow |
| **Model Serving** | Servir predictions em produção | Seldon, BentoML, Vertex AI |
| **Monitoring** | Detectar drift e degradação | Evidently, Whylabs, Fiddler |
| **CI/CD** | Automatizar test/build/deploy | GitHub Actions, GitLab CI, Jenkins |

## Processo de Aplicação (step-by-step)

### Step 1: Data Engineering Pipeline

Estabelecer pipeline de dados confiável:

1. **Ingestão**: fontes de dados identificadas e conectadas
2. **Validação**: data quality checks automatizados (Great Expectations, Pandera)
3. **Transformação**: ETL/ELT padronizado e versionado
4. **Feature Engineering**: features computadas e armazenadas no Feature Store
5. **Versionamento**: datasets versionados (DVC, Delta Lake, lakeFS)

**Checklist de referência**: `checklists/ai/data-pipeline-checklist.md`

### Step 2: Experiment Tracking e Training

Padronizar o processo de experimentação:

```
EXPERIMENT RECORD
━━━━━━━━━━━━━━━━━━━━━
Experiment ID:
Hypothesis:
Dataset version:
Model architecture:
Hyperparameters:
Training time:
Metrics (eval set):
Metrics (test set):
Decision: promote / iterate / abandon
Author:
Date:
```

- Cada experimento registrado com parâmetros, métricas e artifacts
- Reprodutibilidade: qualquer experimento pode ser re-executado
- Comparação: side-by-side de experimentos para tomada de decisão

### Step 3: Model Evaluation e Validation

Antes de qualquer promoção a produção:

- **Performance gates**: métricas mínimas definidas e automatizadas
- **Regression tests**: modelo novo >= modelo atual em golden dataset
- **Bias/fairness checks**: métricas de fairness por subgrupo
- **Latency/resource tests**: modelo atende SLOs de performance
- **Integration tests**: modelo funciona no serving infrastructure

**Referência**: `frameworks/ai/evals-and-redteaming.md`

### Step 4: Model Registry e Versionamento

Gerenciar modelos como ativos versionados:

- **Staging → Production → Archived**: ciclo de vida claro
- **Model metadata**: lineage (dados → features → modelo → deployment)
- **Approval workflow**: quem aprova promoção para produção
- **Rollback**: capacidade de reverter para versão anterior em <5 min

### Step 5: Deployment Pipeline

CI/CD adaptado para ML:

```
┌────────┐    ┌────────┐    ┌────────┐    ┌────────┐
│  Code  │───→│  Test  │───→│ Stage  │───→│  Prod  │
│ Change │    │ Suite  │    │  Env   │    │ Deploy │
└────────┘    └────────┘    └────────┘    └────────┘
     │             │             │             │
     ├─ Unit tests ├─ Data tests ├─ Load test  ├─ Canary
     ├─ Lint       ├─ Model eval ├─ A/B test   ├─ Monitor
     └─ Type check └─ Bias check └─ Shadow     └─ Alerts
```

**Estratégias de deploy**:
- **Blue/Green**: duas versões, switch instantâneo
- **Canary**: novo modelo para % pequeno de tráfego, gradual rollout
- **Shadow**: modelo novo recebe tráfego real mas não serve respostas

### Step 6: Monitoramento em Produção

Dashboard de saúde do modelo:

| Métrica | Descrição | Threshold de Alerta |
|---------|-----------|---------------------|
| **Data Drift** | KL divergence ou PSI dos inputs | PSI > 0.2 |
| **Prediction Drift** | Distribuição dos outputs mudou | KS test p < 0.01 |
| **Performance** | Accuracy/F1 em produção (se labels disponíveis) | Queda > 5% |
| **Latency** | p50/p95/p99 de inferência | p99 > SLO |
| **Error Rate** | % de requests com erro | > 1% |
| **Resource Usage** | CPU, memory, GPU utilization | > 80% sustained |

### Step 7: Retraining Strategy

Definir quando e como retreinar:

- **Calendar-based**: retreinar a cada N dias/semanas
- **Drift-triggered**: retreinar quando data drift detectado
- **Performance-triggered**: retreinar quando performance cai abaixo do threshold
- **Event-triggered**: retreinar após mudança significativa no negócio

**Processo de retraining**:
1. Pipeline automatizado coleta dados frescos
2. Novo modelo treinado com dataset atualizado
3. Avaliação automática (gates de performance)
4. Se aprovado: deploy via canary
5. Se reprovado: alerta para time de ML

## Exemplos Práticos

### Exemplo 1: Startup com 1-3 Modelos

**Nível de maturidade alvo**: 1-2
**Stack recomendado**:
- Experiment tracking: MLflow (open-source)
- Pipeline: GitHub Actions
- Serving: FastAPI + Docker
- Monitoring: Evidently (open-source)
- Feature Store: não necessário ainda

**Foco**: automatizar training pipeline e deploy. Monitoramento básico.

### Exemplo 2: Scale-up com 10-30 Modelos

**Nível de maturidade alvo**: 2-3
**Stack recomendado**:
- Platform: Vertex AI ou SageMaker
- Feature Store: Feast
- Registry: MLflow ou plataforma nativa
- Monitoring: Whylabs ou Evidently
- Orchestration: Airflow ou Prefect

**Foco**: padronização entre times, self-service, monitoramento robusto.

## Armadilhas Comuns

1. **Platform antes de problema**: construir platform complexa antes de ter modelos em produção
2. **Ignorar data quality**: garbage in, garbage out — mesmo com MLOps perfeito
3. **Monitoramento cego**: monitorar sem saber o que fazer quando alerta dispara
4. **Retraining sem validação**: retreinar automaticamente sem gates de qualidade
5. **Feature store premature**: investir em feature store com 2 modelos
6. **Notebook como produção**: modelo rodando em notebook agendado como "produção"
7. **Ignorar custos**: GPU/TPU rodando sem controle de custo
8. **One-size-fits-all**: mesmo processo para modelo crítico e modelo de baixo risco

## Integração com Outros Frameworks

| Framework | Relação |
|-----------|---------|
| `frameworks/ai/ai-governance.md` | Governança dos modelos operacionalizados |
| `frameworks/ai/evals-and-redteaming.md` | Evals integrados no pipeline de MLOps |
| `frameworks/ai/ai-strategy.md` | MLOps como enabler da estratégia de IA |
| `frameworks/cto-architect/cto-reliability-engineering.md` | SLOs e confiabilidade para ML |
| `frameworks/cto-architect/cto-engineering-excellence.md` | Qualidade de código em ML |
| `checklists/ai/data-pipeline-checklist.md` | Qualidade do pipeline de dados |
| `checklists/ai/model-deployment-checklist.md` | Checklist de deploy de modelos |
| `checklists/caio/mlops-and-deployment-quality.md` | Qualidade geral de MLOps |

## Referências

- Google Cloud, "MLOps: Continuous delivery and automation pipelines in ML" (2020)
- Cathy Chen et al., "Reliable Machine Learning" (O'Reilly, 2022)
- Chip Huyen, "Designing Machine Learning Systems" (O'Reilly, 2022)
- D. Sculley et al., "Hidden Technical Debt in Machine Learning Systems" (Google, 2015)
- Netflix Technology Blog, "ML Infrastructure"
- Uber Engineering, "Michelangelo: Uber's Machine Learning Platform"
- MLflow documentation (open-source ML lifecycle management)
- C-Level Squad: `checklists/caio/mlops-and-deployment-quality.md`, `checklists/ai/data-pipeline-checklist.md`
