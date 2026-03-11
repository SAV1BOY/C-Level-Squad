# Forecast Accuracy Tracker

> Script para monitorização da precisão de previsões e calibração.

---

## Objetivo

Medir sistematicamente a precisão das previsões feitas pelo C-Level Squad,
comparando valores previstos com resultados reais, calculando scores de
calibração e identificando áreas onde o forecasting precisa de melhoria.

---

## Tipos de Forecasts Monitorizados

### 1. Financial Forecasts
- Revenue mensal e trimestral
- Custos operacionais
- Margem bruta e operacional
- Cash flow
- Budget utilization por departamento

### 2. Operational Forecasts
- Throughput de entregas (features, releases)
- Timeline de milestones
- Resource needs (headcount, contractors)
- Capacity utilization
- Incident volume

### 3. Market Forecasts
- Customer acquisition rate
- Churn rate
- Market share evolution
- Competitive moves
- Regulatory changes

### 4. People Forecasts
- Hiring timeline
- Attrition rate
- Engagement scores
- Training completion
- Productivity metrics

### 5. Strategic Forecasts
- OKR achievement
- Initiative completion dates
- ROI de investimentos
- Technology adoption rates
- Partnership outcomes

---

## Predicted vs Actual — Estrutura de Dados

### Registo de Forecast
```yaml
forecast_id: "FC-YYYY-NNNN"
date_made: "YYYY-MM-DD"              # Quando a previsão foi feita
forecaster: "Nome / Role / Squad"     # Quem fez a previsão
category: "financial | operational | market | people | strategic"
metric: "Nome da métrica"
period: "YYYY-MM | YYYY-QN"          # Período previsto
predicted_value: 1000000
predicted_range:                       # Intervalo de confiança
  low: 850000
  high: 1150000
confidence_level: 0.80                 # 80% de confiança
assumptions: ["lista de pressupostos"]
methodology: "Método utilizado"
actual_value: null                     # Preenchido quando disponível
actual_date: null                      # Data do registo actual
accuracy_score: null                   # Calculado automaticamente
```

---

## Métricas de Precisão

### 1. Absolute Error
```
Absolute Error = |actual - predicted|
Percentage Error = |actual - predicted| / actual × 100
```

### 2. Directional Accuracy
```
Correcto se:
- Previsão de crescimento E actual cresceu
- Previsão de declínio E actual declinou
- Previsão de estabilidade E actual variou <5%

Directional Accuracy = correct_direction / total_forecasts × 100
```

### 3. Range Accuracy
```
In Range = actual está dentro de [low, high]
Range Accuracy = in_range_count / total_forecasts × 100
```

### 4. Bias Detection
```
Bias = média(predicted - actual)
- Bias > 0: tendência optimista (over-forecasting)
- Bias < 0: tendência pessimista (under-forecasting)
- Bias ≈ 0: bem calibrado
```

### 5. Calibration Score
```
Para cada nível de confiança declarado:
- Se declaro 80% de confiança, o actual deve estar no range 80% das vezes

Calibration = 1 - |declared_confidence - actual_hit_rate|

Perfect calibration = 1.0
Over-confident: actual_hit_rate < declared_confidence
Under-confident: actual_hit_rate > declared_confidence
```

---

## Scoring System

### Score Individual por Forecast
| Métrica | Peso | Cálculo |
|---------|------|---------|
| Percentage Error | 40% | max(0, 100 - percentage_error × 2) |
| Directional Accuracy | 20% | 100 se correcto, 0 se incorrecto |
| Range Accuracy | 20% | 100 se in range, 0 se fora |
| Timeliness | 10% | 100 se forecast feito com antecedência adequada |
| Assumption Quality | 10% | Avaliação qualitativa dos pressupostos |

### Score Agregado por Forecaster
```
Forecaster Score = média ponderada dos últimos 12 forecasts
Trend = comparação com trimestre anterior
Ranking = posição relativa entre forecasters
```

### Score Agregado por Categoria
```
Category Score = média de todos os forecasts na categoria
Best Category = categoria com maior precisão
Worst Category = categoria que precisa mais melhoria
```

---

## Classificação de Precisão

| Score | Classificação | Acção |
|-------|--------------|-------|
| 90-100 | Excellent | Manter metodologia |
| 75-89 | Good | Minor adjustments |
| 60-74 | Acceptable | Rever pressupostos |
| 40-59 | Poor | Rever metodologia |
| 0-39 | Unreliable | Treino + nova abordagem |

---

## Processo de Tracking

### Captura de Forecasts
1. Sempre que um forecast é feito (em reunião, report, plano), registar
2. Incluir valor, range, confiança e pressupostos
3. Tag com categoria e período
4. Atribuir forecaster

### Recolha de Actuals
1. Quando o período previsto termina, recolher valor real
2. Fontes automáticas para métricas quantitativas
3. Input manual para previsões qualitativas
4. Prazo máximo de 5 dias úteis após fim do período

### Cálculo de Scores
1. Comparar predicted vs actual
2. Calcular todas as métricas de precisão
3. Actualizar scores individuais e agregados
4. Detectar bias e padrões
5. Gerar alertas se precisão degrada

### Review e Melhoria
1. Mensal: review de scores por categoria
2. Trimestral: análise de bias e calibração
3. Semestral: revisão de metodologias de forecasting
4. Anual: benchmark contra standards do sector

---

## Reporting

### Dashboard de Forecast Accuracy
- Score médio por categoria (gauge chart)
- Trend de accuracy ao longo do tempo (line chart)
- Calibration plot (predicted confidence vs actual hit rate)
- Bias chart por forecaster e categoria
- Distribution de errors (histogram)
- Leaderboard de forecasters mais precisos

### Report Mensal
```markdown
# Forecast Accuracy Report — [Mês YYYY]

## Summary
- Forecasts avaliados este mês: [N]
- Score médio: [valor]
- Melhor categoria: [nome] ([score])
- Pior categoria: [nome] ([score])

## Bias Analysis
- Bias geral: [optimista/pessimista/neutro]
- Maior bias: [categoria] — [detalhe]

## Calibration
- Confidence 80%: hit rate actual [X]%
- Confidence 90%: hit rate actual [X]%
- Calibração: [over/under/well]-confident

## Insights
- [Padrão identificado 1]
- [Padrão identificado 2]

## Recomendações
- [Acção 1]
- [Acção 2]
```

---

## Integração com Outros Processos

- **Metrics Pack**: accuracy scores incluídos nos packs executivos
- **Decision Quality**: forecasts informam qualidade das decisões
- **Quarterly Review**: accuracy trends são input para review trimestral
- **Risk Scan**: forecasts com baixa accuracy geram sinal de risco
- **Board Prep**: accuracy data reforça credibilidade de projecções

---

## Notas Técnicas

- Forecasts armazenados em `data/forecasts/`
- Actuals ligados automaticamente quando dados disponíveis
- Scores recalculados diariamente para forecasts com actuals novos
- Histórico mantido indefinidamente para análise de tendências
- Calibration training recomendado para forecasters com score <60
