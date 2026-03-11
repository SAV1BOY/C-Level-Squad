# Template: Model Card

## Propósito
Este template documenta modelos de machine learning em produção, seguindo as melhores práticas de ML Ops e AI governance. Model cards garantem transparência, reprodutibilidade e accountability para todos os modelos usados pela organização.

## Instruções de Uso
1. Crie um model card para cada modelo em produção ou pré-produção
2. Atualize a cada retrain significativo ou mudança de arquitetura
3. Revisão obrigatória de ML Lead + responsável de ética/compliance
4. Mantenha versionado junto ao código do modelo

---

## Informações do Modelo

| Campo | Valor |
|-------|-------|
| **Nome do Modelo** | [Nome único — ex: "churn-predictor-v3"] |
| **Versão** | [v1.0.0 — usar semver] |
| **Tipo** | [Classificação / Regressão / NLP / Geração / Recomendação / etc.] |
| **Framework** | [PyTorch / TensorFlow / scikit-learn / Hugging Face / API externa] |
| **Owner** | [Nome — Time] |
| **Data de Deploy** | [DD/MM/AAAA] |
| **Última Atualização** | [DD/MM/AAAA] |
| **Status** | [Desenvolvimento / Staging / Produção / Depreciado / Retirado] |
| **Repositório** | [URL do repositório de código] |
| **Registro do Modelo** | [URL no MLflow / Weights & Biases / etc.] |

---

## 1. Visão Geral

### 1.1 Propósito do Modelo
[Para que o modelo é usado — em linguagem acessível]

### 1.2 Usuários Pretendidos
- **Primários:** [Quem usa o output do modelo diretamente]
- **Secundários:** [Quem é impactado indiretamente pelas decisões do modelo]

### 1.3 Casos de Uso Aprovados
- [Uso aprovado 1]
- [Uso aprovado 2]

### 1.4 Casos de Uso NÃO Aprovados
- [Uso proibido 1 — ex: "Não usar para decisões de crédito sem supervisão humana"]
- [Uso proibido 2 — ex: "Não usar com dados de menores de idade"]

---

## 2. Dados de Treinamento

### 2.1 Datasets Utilizados

| Dataset | Fonte | Período | Volume | Descrição |
|---------|-------|---------|--------|-----------|
| [Dataset 1] | [Interno / Externo] | [Data início — fim] | [N registros] | [Breve descrição] |
| [Dataset 2] | [Fonte] | [Período] | [N registros] | [Descrição] |

### 2.2 Pré-processamento
- [Etapa 1 — ex: "Remoção de duplicatas (X% dos dados)"]
- [Etapa 2 — ex: "Normalização de features numéricas (z-score)"]
- [Etapa 3 — ex: "Tokenização com BPE (vocab size: 32K)"]

### 2.3 Distribuição dos Dados

| Split | Volume | Proporção |
|-------|--------|-----------|
| Treino | [N registros] | [X%] |
| Validação | [N registros] | [X%] |
| Teste | [N registros] | [X%] |

### 2.4 Limitações dos Dados
- [Limitação 1 — ex: "Dados apenas de clientes brasileiros — modelo pode não generalizar para LATAM"]
- [Limitação 2 — ex: "Sub-representação de empresas com < 10 funcionários"]
- [Limitação 3 — ex: "Dados de treino coletados até MM/AAAA — mudanças recentes não refletidas"]

---

## 3. Arquitetura e Treinamento

### 3.1 Arquitetura do Modelo
- **Tipo:** [Ex: "XGBoost com 500 árvores" / "Transformer fine-tuned" / "LLM via API"]
- **Hiperparâmetros principais:**
  - [Param 1]: [Valor]
  - [Param 2]: [Valor]
  - [Param 3]: [Valor]
- **Tamanho do modelo:** [N parâmetros / MB do artefato]

### 3.2 Features / Inputs

| Feature | Tipo | Descrição | Importância |
|---------|------|-----------|------------|
| [Feature 1] | [Numérica/Categórica/Texto] | [O que representa] | [Ranking de importância] |
| [Feature 2] | [Tipo] | [Descrição] | [Ranking] |
| [Feature 3] | [Tipo] | [Descrição] | [Ranking] |

### 3.3 Output
- **Formato:** [Classe / Score / Texto / Embedding]
- **Range:** [0-1 / Categorias / Texto livre]
- **Threshold de decisão:** [X — como foi definido e por quê]

### 3.4 Treinamento
- **Duração:** [Xh em Y GPUs]
- **Custo:** [R$ X]
- **Experimentos:** [N experimentos no MLflow — link]
- **Reprodutibilidade:** [Seed: X / Dados versionados: Sim/Não]

---

## 4. Performance

### 4.1 Métricas no Dataset de Teste

| Métrica | Valor | Baseline (regra/modelo anterior) | Melhoria |
|---------|-------|--------------------------------|----------|
| Accuracy | [X%] | [Y%] | [+Z pp] |
| Precision | [X%] | [Y%] | [+Z pp] |
| Recall | [X%] | [Y%] | [+Z pp] |
| F1 Score | [X%] | [Y%] | [+Z pp] |
| AUC-ROC | [X] | [Y] | [+Z] |
| Latência (p50/p99) | [Xms / Yms] | [N/A] | — |

### 4.2 Performance por Subgrupo (Fairness)

| Subgrupo | N Amostras | Accuracy | F1 | Análise |
|----------|-----------|---------|-----|---------|
| [Subgrupo A] | [N] | [X%] | [X%] | [Comentário sobre disparidade] |
| [Subgrupo B] | [N] | [X%] | [X%] | [Comentário] |
| [Subgrupo C] | [N] | [X%] | [X%] | [Comentário] |

### 4.3 Limitações Conhecidas
- [Limitação 1 — cenário onde o modelo performa mal]
- [Limitação 2 — tipo de input que gera resultados imprecisos]
- [Limitação 3 — condições onde não deve ser usado sem supervisão]

---

## 5. Deploy e Operação

### 5.1 Infraestrutura
- **Ambiente:** [AWS SageMaker / GCP Vertex / Self-hosted / API externa]
- **Compute:** [Tipo de instância / GPU]
- **Custo mensal de infra:** [R$ X]
- **Custo por inferência:** [R$ X]

### 5.2 Monitoramento

| Métrica Monitorada | Alerta | Threshold | Dashboard |
|-------------------|--------|-----------|-----------|
| Performance (accuracy/F1) | [PagerDuty/Slack] | [<X%] | [URL] |
| Data drift | [Canal] | [Score > X] | [URL] |
| Latência | [Canal] | [>X ms p99] | [URL] |
| Volume de inferências | [Canal] | [<X ou >Y /dia] | [URL] |
| Taxa de erro | [Canal] | [>X%] | [URL] |

### 5.3 Retrain
- **Frequência:** [Semanal / Mensal / Trimestral / Sob demanda]
- **Trigger automático:** [Data drift > X / Performance < Y / N novos dados]
- **Pipeline de retrain:** [URL do pipeline]
- **Processo de validação pós-retrain:** [Descrever]

---

## 6. Considerações Éticas

| Dimensão | Avaliação | Ações |
|----------|----------|-------|
| Viés | [Identificados viéses em X, Y, Z] | [Medidas tomadas] |
| Privacidade | [Usa dados pessoais? Quais?] | [Anonimização / Consentimento] |
| Transparência | [Explicável? SHAP/LIME disponível?] | [Como explicar decisões] |
| Impacto social | [Potenciais impactos negativos] | [Mitigações] |
| Contestabilidade | [Usuário pode contestar decisão?] | [Processo de recurso] |

---

## 7. Histórico de Versões

| Versão | Data | Mudanças | Performance | Motivo |
|--------|------|---------|------------|--------|
| v1.0 | [DD/MM] | [Modelo inicial] | [F1: X%] | [Launch] |
| v1.1 | [DD/MM] | [Adição de features X, Y] | [F1: X%] | [Melhoria de performance] |
| v2.0 | [DD/MM] | [Mudança de arquitetura] | [F1: X%] | [Retrain por drift] |

---

## Exemplo Preenchido (Resumo)

> **Modelo:** lead-scoring-v2 | **Tipo:** XGBoost classificação binária
> **Propósito:** Priorizar leads com maior probabilidade de conversão
> **Features:** 23 (comportamento no produto, firmográficos, engajamento marketing)
> **Performance:** F1 82%, AUC 0.91 (baseline com regras: F1 54%)
> **Retrain:** Mensal automático | **Latência:** 12ms p99
> **Limitação:** Performance degradada para empresas com <5 funcionários (poucas amostras)

---

## Dicas de Uso
- Model card é documentação obrigatória, não opcional — compliance exige
- Atualize em cada retrain — model card desatualizado é perigoso
- Performance por subgrupo é essencial — modelos podem discriminar sem você perceber
- Inclua limitações honestas — melhor documentar do que descobrir em produção
- Versione junto ao código — um commit, um model card atualizado
- Torne acessível para não-técnicos — PMs e líderes precisam entender
