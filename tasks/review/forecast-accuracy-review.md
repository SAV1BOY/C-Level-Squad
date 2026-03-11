# Forecast Accuracy Review

## Objetivo
Avaliar a accuracy dos forecasts financeiros e operacionais, identificando padrões de viés e melhorando a capacidade preditiva da organização. Forecasts ruins levam a decisões ruins — over-forecasting causa overinvestment, under-forecasting causa missed opportunities.

## Agente Responsável
- **CFO Agent** — Ownership de forecast quality e financial planning accuracy

## Agentes de Suporte
- **COO Agent** — Operational forecast accuracy
- **CMO Agent** — Pipeline e revenue forecast inputs
- **CTO Agent** — Engineering capacity e delivery forecasts
- **CEO Agent** — Strategic planning accuracy

## Pré-requisitos
1. Historical forecast data (at least 4 quarters of forecasts + actuals)
2. Revenue forecast records by period
3. Expense forecast records by category
4. Pipeline forecast records
5. Headcount forecast records
6. Engineering delivery forecasts (roadmap vs. actual)

## Processo (step-by-step)

### Fase 1: Data Compilation (1-2 dias)
1. Compile all forecasts for the review period with corresponding actuals
2. Calculate variance (forecast - actual) / forecast for each metric
3. Categorize forecasts: revenue, expenses, pipeline, headcount, delivery, KPIs
4. Calculate MAPE (Mean Absolute Percentage Error) for each category
5. Track forecast accuracy over time: is it improving or deteriorating?
6. Identify forecast horizon impact: accuracy at 1-month vs. 3-month vs. 12-month

### Fase 2: Bias Analysis (1-2 dias)
7. Determine if forecasts are systematically biased: optimistic or pessimistic?
8. Analyze bias by category: which areas over-forecast vs. under-forecast?
9. Analyze bias by forecaster: do specific people or teams consistently miss in one direction?
10. Identify external factors that caused forecast misses (market changes, black swans)
11. Separate controllable misses (process issues) from uncontrollable misses (external events)
12. Assess confidence calibration: when forecasters say "high confidence," are they right?

### Fase 3: Root Cause Analysis (1-2 dias)
13. For top 5 largest forecast misses, conduct root cause analysis
14. Common causes to investigate: outdated assumptions, poor data, wishful thinking, sandbagging, methodology gaps
15. Assess forecast methodology: bottoms-up vs. top-down, statistical vs. judgmental
16. Evaluate data quality feeding into forecasts
17. Review forecast review process: are forecasts challenged before being committed?
18. Identify forecast dependencies: where one bad forecast cascades into others

### Fase 4: Improvement Plan (1 dia)
19. Recommend methodology improvements for weakest forecast areas
20. Propose process changes: more frequent updates, better data, improved assumptions
21. Define accuracy targets by category and horizon
22. Propose accountability mechanism: track who forecasts what and their accuracy
23. Present findings with specific, actionable improvements
24. Schedule follow-up to track improvement

## Frameworks a Aplicar
- **MAPE (Mean Absolute Percentage Error)** — Standard forecast accuracy metric
- **Bias Detection** — Systematic over/under forecasting patterns
- **Confidence Calibration** — Assess if stated confidence matches actual accuracy
- **Forecast Decomposition** — Break forecasts into components for diagnosis
- **Rolling Forecast** — Replace static annual forecasts with rolling updates
- **Scenario-Based Forecasting** — Multiple scenarios vs. single point estimates

## Checklists de Qualidade
- [ ] All forecasts compiled with corresponding actuals
- [ ] MAPE calculated by category
- [ ] Bias direction identified (optimistic/pessimistic)
- [ ] Accuracy trends over 4+ quarters analyzed
- [ ] Forecast horizon impact assessed
- [ ] Top 5 misses root-caused
- [ ] Methodology reviewed
- [ ] Data quality assessed
- [ ] Accuracy targets set for each category
- [ ] Improvement recommendations documented
- [ ] Accountability mechanism proposed

## Template de Entrega
```markdown
# Forecast Accuracy Review — [Period]

## Overall Accuracy
- **Revenue Forecast MAPE:** [X%]
- **Expense Forecast MAPE:** [X%]
- **Pipeline Forecast MAPE:** [X%]
- **Headcount Forecast MAPE:** [X%]
- **Delivery Forecast MAPE:** [X%]

## Accuracy by Category
| Category | MAPE | Bias Direction | Trend | Target |
|----------|------|---------------|-------|--------|
| Revenue | | Optimistic/Pessimistic | ↑↓→ | |
| Expenses | | | | |
| Pipeline | | | | |
| Headcount | | | | |
| Delivery | | | | |

## Accuracy by Horizon
| Horizon | MAPE | Usable? |
|---------|------|---------|
| 1 month | | |
| 3 months | | |
| 6 months | | |
| 12 months | | |

## Top 5 Forecast Misses
| Forecast | Predicted | Actual | Variance | Root Cause |
|----------|-----------|--------|----------|-----------|

## Bias Analysis
| Forecaster/Area | Direction | Magnitude | Pattern |
|----------------|-----------|-----------|---------|

## Improvement Recommendations
| Area | Issue | Recommendation | Expected Improvement |
|------|-------|---------------|---------------------|

## Accuracy Targets (Next Period)
| Category | Current MAPE | Target MAPE |
|----------|-------------|-------------|
```

## Registries para Atualizar
- `registries/forecasts.md` — Accuracy scores annotated
- `registries/metrics-log.md` — Forecast accuracy metrics
- `registries/decisions-log.md` — Methodology change decisions
- `registries/lessons-learned.md` — Forecast learnings

## Critérios de Aceitação
1. MAPE calculated for all forecast categories
2. Bias direction and magnitude identified
3. Accuracy trends over 4+ quarters documented
4. Top 5 misses root-caused
5. Improvement recommendations with expected impact
6. Accuracy targets set for next period
7. Executive team aligned on improvements

## Dependências e Handoffs
- **Recebe de:** Financial Actuals, Pipeline Data, Delivery Data, Headcount Data
- **Entrega para:** Forecast Process Improvements, Planning Cycles, Board Reporting
- **Cadência:** Trimestral
- **Escalation path:** MAPE >25% sustained escala to CEO
- **Integração:** Feeds Board Prep, Quarterly Planning, Budget Process
