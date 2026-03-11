# Ciclo de Avaliação de Modelos AI

> Processo estruturado para avaliar, comparar e selecionar modelos de AI/ML
> para uso em produção, garantindo qualidade, custo-efetividade e alinhamento
> com requisitos de negócio.

## Objetivo

Garantir que os modelos de AI em uso (e candidatos a uso) atendem aos requisitos
de qualidade, performance, custo e ética da organização. Manter um ciclo
contínuo de avaliação para acompanhar a rápida evolução do mercado.

## Frequência

- **Avaliação de modelos em produção:** Trimestral
- **Benchmark de novos modelos:** Quando novos modelos relevantes são lançados
- **Avaliação pré-produção:** Antes de cada deploy de modelo novo
- **Monitoramento contínuo:** Drift detection automatizado

## Dimensões de Avaliação

### 1. Qualidade/Accuracy
- [ ] Métricas de accuracy no dataset de teste (precision, recall, F1)
- [ ] Performance em edge cases e cenários adversariais
- [ ] Comparação com baseline e modelo anterior
- [ ] Avaliação humana (sample de outputs revisados por especialistas)
- [ ] Consistency (mesmo input, output similar em múltiplas execuções)

### 2. Performance/Latência
- [ ] Latência de inferência (p50, p95, p99)
- [ ] Throughput (requests/segundo)
- [ ] Cold start time (se serverless)
- [ ] Utilização de recursos (GPU/CPU/memória)
- [ ] Performance sob carga (degradação graceful?)

### 3. Custo
- [ ] Custo por inferência
- [ ] Custo mensal projetado para volume esperado
- [ ] Comparação de custo entre provedores/modelos
- [ ] Total Cost of Ownership (infra + licenciamento + manutenção)
- [ ] Custo de fine-tuning vs prompt engineering

### 4. Segurança e Privacidade
- [ ] Dados sensíveis são enviados para terceiros?
- [ ] Modelo retém/treina com dados do cliente?
- [ ] Compliance com LGPD/GDPR
- [ ] Vulnerabilidades conhecidas (prompt injection, data leakage)
- [ ] Audit trail de inferências

### 5. Robustez
- [ ] Performance com inputs malformados ou adversariais
- [ ] Graceful degradation quando modelo não tem confiança
- [ ] Fallback behavior definido
- [ ] Handling de rate limits e erros de API
- [ ] Resiliência a mudanças no input distribution

## Processo de Avaliação

### Fase 1: Definir Critérios (Semana 1)
- [ ] Identificar requisitos de negócio para o modelo
- [ ] Definir métricas de sucesso e thresholds
- [ ] Criar dataset de avaliação (golden dataset)
- [ ] Definir budget de avaliação (tempo e custo)

### Fase 2: Benchmark (Semana 2-3)
- [ ] Rodar todos os modelos candidatos contra o golden dataset
- [ ] Coletar métricas de qualidade, latência e custo
- [ ] Avaliação humana de amostra de outputs (blind review)
- [ ] Testar edge cases e cenários adversariais
- [ ] Documentar resultados em formato padronizado

### Fase 3: Análise e Decisão (Semana 4)
- [ ] Compilar scorecard comparativo
- [ ] Análise de trade-offs (qualidade vs custo vs latência)
- [ ] Recomendação com justificativa
- [ ] Review com stakeholders técnicos e de negócio
- [ ] Decisão documentada como ADR

### Fase 4: Deployment e Monitoramento
- [ ] Shadow deployment (rodar novo modelo em paralelo)
- [ ] A/B test com % pequeno de tráfego
- [ ] Monitorar métricas de qualidade e performance
- [ ] Ramp-up gradual (10% → 50% → 100%)
- [ ] Rollback plan se métricas degradarem

## Template de Scorecard

```
MODEL EVALUATION SCORECARD
Data: [Data]
Use Case: [Descrição]
Avaliador: [Nome]

| Critério | Peso | Modelo A | Modelo B | Modelo C |
|----------|------|----------|----------|----------|
| Accuracy (F1) | 25% | | | |
| Latência p95 | 20% | | | |
| Custo/1K req | 15% | | | |
| Robustez | 15% | | | |
| Privacidade | 10% | | | |
| Facilidade de integração | 10% | | | |
| Vendor reliability | 5% | | | |
| TOTAL PONDERADO | 100% | | | |

Recomendação: [Modelo X]
Justificativa: [1-2 parágrafos]
Riscos: [Principais riscos da escolha]
```

## Monitoramento Contínuo Pós-Deploy

### Drift Detection
- [ ] Monitorar distribuição de inputs (data drift)
- [ ] Monitorar distribuição de outputs (prediction drift)
- [ ] Monitorar métricas de qualidade (concept drift)
- [ ] Alertas automatizados quando drift excede threshold

### Feedback Loop
- [ ] Coletar feedback humano sobre outputs do modelo
- [ ] Thumbs up/down ou rating em outputs
- [ ] Casos de erro documentados para melhoria
- [ ] Golden dataset atualizado com novos exemplos

### Dashboard de Saúde do Modelo
- Accuracy/quality metrics (trend)
- Latência e throughput (trend)
- Custo acumulado (budget tracking)
- Drift score
- User satisfaction score

## Considerações para LLMs (Modelos de Linguagem)

### Avaliação Específica de LLMs
- [ ] Benchmark em tasks relevantes (summarization, Q&A, classification)
- [ ] Teste de alucinação (factual accuracy)
- [ ] Teste de seguir instruções (instruction following)
- [ ] Teste de recusa adequada (não responder quando não deveria)
- [ ] Teste de consistência com persona/tom definido
- [ ] Avaliação de toxicidade e viés

### Build vs Buy para LLMs
| Aspecto | API de Terceiro (OpenAI, Anthropic) | Modelo Open-Source (Llama, Mistral) |
|---------|-------------------------------------|--------------------------------------|
| Custo inicial | Baixo (pay per use) | Alto (infra GPU) |
| Custo em escala | Alto (cresce linear) | Moderado (custo fixo) |
| Customização | Limitada (prompt + fine-tune) | Total (weights, architecture) |
| Privacidade | Dados saem da sua infra | Dados ficam na sua infra |
| Manutenção | Vendor cuida | Sua equipe cuida |
| Qualidade | State-of-art | Pode ser inferior |

## Referências

- "Machine Learning Design Patterns" - Lakshmanan, Robinson, Munn (O'Reilly)
- MLOps Community resources (mlops.community)
- "Designing Machine Learning Systems" - Chip Huyen (O'Reilly, 2022)
- Hugging Face Open LLM Leaderboard
- Stanford HELM Benchmark
