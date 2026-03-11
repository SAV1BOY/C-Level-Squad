# AI Use Case Blocks — Blocos Reutilizáveis para Casos de Uso de AI

> Referência do C-Level Squad para documentar, avaliar e governar use cases de Inteligência Artificial.
> Agente primário: CAIO, com colaboração de CTO (infra), CIO (dados) e agente da área de negócio.

---

## 1. Use Case Description Block

### Propósito
Documentar um caso de uso de AI de forma completa, conectando problema de negócio a solução técnica.

### Template

```markdown
## AI Use Case: [Nome do Use Case]

### Metadados
- **ID:** [AI-YYYY-NNN]
- **Status:** [Ideação / Assessment / POC / Piloto / Produção / Descontinuado]
- **Business owner:** [Agente de negócio — quem tem o problema]
- **Technical owner:** [CAIO ou ML engineer]
- **Data de criação:** [YYYY-MM-DD]
- **Prioridade:** [P1 / P2 / P3]

### Problema de negócio
[Descrição clara do problema SEM mencionar AI. AI é a solução, não o problema.]

**Pergunta-chave:** [A pergunta que queremos que AI responda ou a tarefa que queremos automatizar]

**Impacto atual do problema:**
- Quantitativo: [R$ perdidos, horas gastas, taxa de erro atual]
- Qualitativo: [frustração de clientes, burnout do time, etc.]

### Solução proposta com AI
**Tipo de AI:**
- [ ] Classificação (categorizar inputs em classes predefinidas)
- [ ] Regressão (prever um valor numérico)
- [ ] Recomendação (sugerir itens relevantes)
- [ ] NLP / LLM (processar ou gerar texto)
- [ ] Computer Vision (processar imagens/vídeo)
- [ ] Anomaly Detection (detectar padrões incomuns)
- [ ] Forecasting (prever séries temporais)
- [ ] Generative AI (criar conteúdo — texto, imagem, código)
- [ ] Optimization (encontrar a melhor solução dado constraints)
- [ ] Outro: [especificar]

**Descrição da solução:**
[Como AI será usada para resolver o problema. Em linguagem que o business owner entende.]

**Interação humana:**
- [ ] Fully automated (AI decide sem humano)
- [ ] Human-in-the-loop (AI sugere, humano decide)
- [ ] Human-on-the-loop (AI decide, humano monitora e pode intervir)
- [ ] Augmentation (AI fornece informação, humano decide sem sugestão direta)

### Usuários finais
- **Quem usa:** [Role/persona que interage com o output de AI]
- **Como usa:** [Workflow: onde na jornada o output de AI aparece]
- **Volume de uso:** [X predições/classificações/recomendações por dia/mês]
- **Tolerância a erro:** [Alta: erros são OK se maioria certa / Baixa: cada erro é custoso]

### Alternativas consideradas (sem AI)
| Alternativa          | Prós                  | Contras               | Por que AI é melhor      |
|---------------------|----------------------|-----------------------|--------------------------|
| [Manual/regras]     | [prós]               | [contras]             | [razão]                  |
| [Outsourcing]       | [prós]               | [contras]             | [razão]                  |
| [Software sem AI]   | [prós]               | [contras]             | [razão]                  |
```

---

## 2. Data Requirements Block

### Propósito
Documentar todos os requisitos de dados para o use case, desde coleta até features para o modelo.

### Template

```markdown
## Data Requirements — [Use Case ID]

### Dados necessários

| # | Dataset               | Fonte           | Formato  | Volume   | Freshness necessária | Disponível? | Qualidade |
|---|-----------------------|-----------------|----------|----------|---------------------|-------------|-----------|
| 1 | [Dataset 1]           | [sistema/API]   | [CSV/API/DB] | [N rows] | [real-time/diário/etc] | [Sim/Não/Parcial] | [Alta/Média/Baixa] |
| 2 | [Dataset 2]           | [fonte]         | [formato]| [volume] | [freshness]         | [status]    | [qualidade]|

### Features esperadas (input do modelo)
| Feature              | Tipo        | Fonte/Cálculo               | Importância esperada |
|---------------------|-------------|------------------------------|---------------------|
| [feature 1]         | [numérica/categórica/texto] | [como é calculada]| [alta/média/baixa] |
| [feature 2]         | [tipo]      | [cálculo]                    | [importância]       |

### Target variable (output do modelo)
- **Nome:** [variável que o modelo prevê]
- **Tipo:** [contínua / binária / multi-classe / ranking]
- **Distribuição:** [balanceada / desbalanceada — se desbalanceada, ratio]
- **Histórico disponível:** [quantos meses/anos de histórico de target]

### Gaps de dados
| Gap                              | Impacto no modelo          | Plano para resolver           | Timeline | Owner |
|---------------------------------|---------------------------|-------------------------------|----------|-------|
| [Dado faltante 1]              | [como afeta performance]  | [coletar/comprar/proxy]       | [data]   | [DRI] |
| [Dado com qualidade ruim]      | [impacto]                 | [limpar/transformar]          | [data]   | [DRI] |

### Data pipeline necessário
```
[Fonte A] → [ETL/Transformação] → [Feature Store] → [Model Training]
[Fonte B] → [Real-time stream]  → [Feature Store] → [Model Serving]
```

### Considerações de privacidade (LGPD)
- [ ] Dados contêm PII (informação pessoal identificável)?
- [ ] Base legal para uso (consentimento / legítimo interesse / cumprimento legal)?
- [ ] Necessário anonimizar/pseudonimizar?
- [ ] Data retention policy definida?
- [ ] DPIA (Data Protection Impact Assessment) necessário?
```

---

## 3. Model Selection Block

### Propósito
Documentar a escolha do modelo/abordagem de AI, justificando a decisão técnica.

### Template

```markdown
## Model Selection — [Use Case ID]

### Abordagem escolhida: [Nome do modelo/framework]

### Opções consideradas

| Opção              | Tipo           | Complexidade | Performance esperada | Custo de operação | Explicabilidade |
|-------------------|----------------|-------------|---------------------|-------------------|-----------------|
| [Regras de negócio]| Heurística    | Baixa       | [baseline]          | Baixo             | Alta            |
| [Modelo 1]        | [tipo]         | [B/M/A]     | [estimativa]        | [custo]           | [B/M/A]         |
| [Modelo 2]        | [tipo]         | [B/M/A]     | [estimativa]        | [custo]           | [B/M/A]         |
| [LLM/GenAI]       | Foundation model| Alta       | [estimativa]        | Alto              | Baixa           |

### Justificativa da escolha
[Por que este modelo e não os outros? Balancear: performance, custo, explicabilidade, complexidade operacional, disponibilidade de dados]

### Abordagem de desenvolvimento

**Fase 1: Baseline (semana 1-2)**
- Implementar regra de negócio ou modelo simples como baseline
- Métricas de baseline servirão como comparação

**Fase 2: Modelo candidato (semana 3-6)**
- Treinar modelo escolhido
- Otimizar hiperparâmetros
- Validar com cross-validation

**Fase 3: Avaliação (semana 7-8)**
- Comparar com baseline
- Avaliar fairness e robustez
- Decidir se atende critérios mínimos

### Stack técnico
| Componente         | Ferramenta/Framework      | Justificativa            |
|-------------------|---------------------------|--------------------------|
| Training          | [Python/PyTorch/etc.]     | [razão]                  |
| Experiment tracking| [MLflow/W&B/etc.]        | [razão]                  |
| Feature store     | [Feast/Tecton/etc.]       | [razão]                  |
| Model serving     | [SageMaker/Vertex/etc.]   | [razão]                  |
| Monitoring        | [Evidently/Arize/etc.]    | [razão]                  |

### Retraining strategy
- **Frequência:** [Diário / Semanal / Mensal / Triggered by drift]
- **Trigger:** [Qual métrica/threshold dispara retraining]
- **Processo:** [Automático / Semi-automático / Manual]
- **Validação pré-deploy:** [Testes automáticos que o novo modelo deve passar]
```

---

## 4. Evaluation Criteria Block

### Propósito
Definir como o modelo será avaliado — métricas técnicas e de negócio.

### Template

```markdown
## Evaluation Criteria — [Use Case ID]

### Métricas técnicas

| Métrica              | Definição                                   | Target mínimo | Target ideal |
|---------------------|---------------------------------------------|---------------|-------------|
| [Accuracy/F1/AUC]   | [definição para este contexto]              | [valor]       | [valor]     |
| [Precision]          | [definição — importante se FP é custoso]    | [valor]       | [valor]     |
| [Recall]             | [definição — importante se FN é custoso]    | [valor]       | [valor]     |
| [Latência (P95)]     | Tempo de resposta do modelo                 | [Xms]         | [Yms]       |
| [Throughput]         | Predições por segundo                       | [X/s]         | [Y/s]       |

### Métricas de negócio

| Métrica              | Baseline (sem AI) | Target com AI  | Como medir              |
|---------------------|-------------------|----------------|-------------------------|
| [Receita incremental]| [atual]          | [target]       | [A/B test / comparação] |
| [Custo reduzido]    | [atual]          | [target]       | [medição direta]        |
| [Tempo economizado] | [atual]          | [target]       | [antes vs. depois]      |
| [Taxa de erro]      | [atual]          | [target]       | [auditoria]             |

### Critérios de fairness

| Dimensão            | Grupos avaliados          | Métrica        | Threshold aceitável    |
|--------------------|---------------------------|----------------|------------------------|
| [Gênero]           | [M/F/Outro]               | [Disparate impact ratio] | [≥0.8]         |
| [Região]           | [Regiões geográficas]     | [Equal opportunity diff] | [<0.05]        |
| [Faixa etária]     | [Grupos etários]          | [Predictive parity diff] | [<0.05]       |

### Critérios de aceitação para produção
- [ ] Performance técnica ≥ target mínimo em todas as métricas
- [ ] Performance de negócio demonstra melhoria vs. baseline
- [ ] Fairness dentro dos thresholds para todos os grupos
- [ ] Latência dentro do SLA
- [ ] Explicabilidade: top features fazem sentido do ponto de vista de negócio
- [ ] Robustez: performance estável com dados de diferentes períodos
- [ ] Edge cases documentados e tratados
```

---

## 5. Risk Assessment Block (AI-specific)

### Template

```markdown
## AI Risk Assessment — [Use Case ID]

### Classificação de risco do use case

| Fator                              | Score (1-5) | Justificativa                    |
|-----------------------------------|-------------|----------------------------------|
| Impacto em pessoas (se errar)     | [1-5]       | [ex: decisão financeira = alto]  |
| Autonomia do modelo               | [1-5]       | [fully auto = 5, human-in-loop = 2] |
| Sensibilidade dos dados           | [1-5]       | [PII = alto, agregado = baixo]   |
| Escala de impacto                 | [1-5]       | [# de pessoas/decisões afetadas] |
| Reversibilidade das decisões      | [1-5]       | [crédito negado = difícil reverter] |
| **Risk tier:**                    | **[Score total]** | **[Low <10 / Medium 10-18 / High >18]** |

### Riscos específicos de AI

| # | Risco                        | P | I | Score | Mitigação                           |
|---|------------------------------|---|---|-------|-------------------------------------|
| 1 | Viés/discriminação no modelo | [P]|[I]| [S]  | Fairness audit, dados balanceados   |
| 2 | Data drift em produção       | [P]|[I]| [S]  | Monitoring + alertas + retraining   |
| 3 | Adversarial attacks          | [P]|[I]| [S]  | Input validation, anomaly detection |
| 4 | Privacy/LGPD violation       | [P]|[I]| [S]  | DPIA, anonimização, consent management |
| 5 | Model hallucination (LLMs)   | [P]|[I]| [S]  | Grounding, RAG, fact-checking       |
| 6 | Over-reliance by users       | [P]|[I]| [S]  | Training, confidence scores visíveis|
| 7 | Vendor lock-in               | [P]|[I]| [S]  | Abstraction layer, multi-model      |
| 8 | Explainability gap           | [P]|[I]| [S]  | SHAP/LIME, model cards              |
| 9 | Cost escalation              | [P]|[I]| [S]  | Cost caps, usage monitoring         |
|10 | Reputational damage          | [P]|[I]| [S]  | Human review for sensitive cases    |

### Governança requerida por tier

| Tier   | Requisitos antes de produção                                    |
|--------|----------------------------------------------------------------|
| Low    | Model card + basic monitoring + owner definido                  |
| Medium | Tudo de Low + fairness audit + DPIA + human-in-the-loop para edge cases |
| High   | Tudo de Medium + external review + board notification + legal sign-off + continuous audit |
```

---

## 6. ROI Projection Block

### Template

```markdown
## ROI Projection — [Use Case ID]

### Investimento

| Categoria          | One-time    | Recorrente (anual) | Notas                    |
|--------------------|------------|-------------------|--------------------------|
| Desenvolvimento    | R$ [X]     | —                 | [detalhes]               |
| Dados/Infraestrutura| R$ [X]    | R$ [X]            | [cloud, storage, compute]|
| Talento            | R$ [X]     | R$ [X]            | [salários, contratação]  |
| Ferramentas/Licenças| R$ [X]    | R$ [X]            | [MLOps, APIs]            |
| **Total investimento**| **R$ [X]**| **R$ [X]/ano**  |                          |

### Retorno esperado

| Benefício                    | Valor estimado (anual) | Confiança | Como medir              |
|-----------------------------|----------------------|-----------|-------------------------|
| [Receita incremental]       | R$ [X]               | [A/M/B]   | [A/B test]              |
| [Custo evitado]             | R$ [X]               | [A/M/B]   | [comparação antes/depois]|
| [Produtividade]             | R$ [X]               | [A/M/B]   | [horas economizadas × custo/hora] |
| **Total retorno**           | **R$ [X]/ano**       |           |                         |

### Cenários de ROI

| Cenário     | Prob. | Retorno anual | ROI     | Payback |
|------------|-------|---------------|---------|---------|
| Otimista   | 20%   | R$ [X]        | [X]×    | [X] meses |
| Base       | 60%   | R$ [X]        | [X]×    | [X] meses |
| Pessimista | 20%   | R$ [X]        | [X]×    | [X] meses |
| **EMV**    |       | **R$ [X]**    | **[X]×**| **[X] meses** |

### Break-even analysis
- **Investimento total (ano 1):** R$ [X]
- **Retorno mensal esperado:** R$ [X]
- **Break-even em:** [X] meses
- **ROI em 12 meses:** [X]×
- **ROI em 24 meses:** [X]×
```

---

## 7. Deployment Plan Block

### Template

```markdown
## Deployment Plan — [Use Case ID]

### Estratégia de rollout

| Fase        | Escopo                  | Duração  | Critério para avançar          |
|-------------|------------------------|----------|-------------------------------|
| Shadow mode | Modelo roda em paralelo, sem afetar decisões | 2 semanas | Performance ≥ baseline         |
| Canary      | 5% do tráfego          | 2 semanas | Sem degradação em métricas de negócio |
| Beta        | 25% do tráfego         | 2 semanas | Métricas de negócio melhoram   |
| GA          | 100% do tráfego        | Ongoing  | Todas as métricas estáveis     |

### Checklist pré-deploy
- [ ] Model card preenchido e aprovado
- [ ] Testes automatizados passando (unit + integration)
- [ ] Performance validada em holdout dataset
- [ ] Fairness audit concluído e aprovado
- [ ] Monitoring configurado (performance, drift, latência)
- [ ] Alertas configurados com thresholds definidos
- [ ] Rollback plan testado
- [ ] Documentação de API atualizada
- [ ] Training para usuários finais (se human-in-the-loop)
- [ ] Legal/compliance sign-off (se High tier)
- [ ] Cost projection validada (API calls, compute)

### Rollback plan
**Trigger de rollback:** [Qual métrica/evento dispara rollback automático]
**Processo:** [Passo-a-passo para rollback — idealmente automatizado]
**Fallback:** [O que assume quando AI é desativada — regras, manual, modelo anterior]
**SLA de rollback:** [Tempo máximo para voltar ao estado anterior]

### Monitoring em produção
| Métrica monitored           | Frequência   | Threshold alerta | Threshold rollback |
|-----------------------------|-------------|------------------|--------------------|
| Model accuracy/F1           | Diária      | <[X] por 3 dias  | <[Y] por 1 dia    |
| Data drift (PSI/KL)         | Diária      | >[X]             | >[Y]               |
| Latência P95                | Real-time   | >[X]ms           | >[Y]ms             |
| Error rate                  | Real-time   | >[X]%            | >[Y]%              |
| Business metric impacted    | Semanal     | <baseline        | <baseline por 2sem |
```

---

## 8. Governance Block

### Template

```markdown
## AI Governance — [Use Case ID]

### Model Card

| Campo                    | Valor                                          |
|--------------------------|------------------------------------------------|
| Nome do modelo           | [nome]                                         |
| Versão                   | [v1.0]                                         |
| Tipo                     | [classificação/regressão/etc.]                 |
| Framework                | [PyTorch/TensorFlow/scikit-learn/etc.]         |
| Data de treinamento      | [YYYY-MM-DD]                                   |
| Dataset de treinamento   | [nome e versão]                                |
| Tamanho do dataset       | [N samples]                                    |
| Features principais      | [top 5-10 features]                            |
| Métricas de performance  | [AUC: X, F1: Y, etc.]                         |
| Limitações conhecidas    | [onde o modelo performa mal]                   |
| Vieses conhecidos        | [grupos onde performance é diferente]           |
| Uso pretendido           | [para que deve ser usado]                      |
| Uso não pretendido       | [para que NÃO deve ser usado]                  |
| Owner                    | [CAIO / ML engineer]                           |
| Próximo retraining       | [data ou trigger]                              |
| Review date              | [próxima revisão de governance]                |

### Audit trail
| Data       | Ação                    | Responsável | Notas                    |
|-----------|-------------------------|-------------|--------------------------|
| [data]    | Modelo treinado v1.0    | [pessoa]    | [notas]                  |
| [data]    | Fairness audit          | [pessoa]    | [resultado]              |
| [data]    | Deploy em produção      | [pessoa]    | [canary 5%]              |
| [data]    | Retraining v1.1         | [pessoa]    | [trigger: drift detected]|

### Responsible AI checklist
- [ ] Fairness: Avaliamos impacto em grupos protegidos
- [ ] Transparency: Usuários sabem que interagem com AI
- [ ] Accountability: Owner definido e acessível
- [ ] Privacy: LGPD compliant, DPIA realizado se necessário
- [ ] Safety: Edge cases testados, rollback disponível
- [ ] Human oversight: Nível adequado de supervisão humana
- [ ] Documentation: Model card completo e atualizado
```
