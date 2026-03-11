# Revenue Pipeline Review

## Objetivo
Revisar a saúde e qualidade do pipeline de receita, avaliar probabilidade de atingir targets, identificar gaps e definir ações corretivas. O pipeline review é o sistema de early warning mais importante para receita — problemas no pipeline hoje significam problemas de revenue em 30-90 dias.

## Agente Responsável
- **CMO Agent** — Ownership do pipeline health e demand generation

## Agentes de Suporte
- **CFO Agent** — Revenue forecast accuracy e financial targets
- **CEO Agent** — Strategic deals e key account relationships
- **CPO Agent** — Product gaps que afetam win rate
- **COO Agent** — Operational capacity para delivery

## Pré-requisitos
1. CRM atualizado com pipeline data (stages, values, close dates, probability)
2. Revenue targets por período (mensal/trimestral/anual)
3. Historical conversion rates por stage
4. Win/loss data dos últimos 90 dias
5. Marketing attribution data (source of pipeline)
6. Sales capacity model (reps, quota, productivity)

## Processo (step-by-step)

### Fase 1: Pipeline Data Analysis (1-2 dias)
1. Extrair snapshot completo do pipeline: total value, by stage, by segment, by rep
2. Calcular pipeline coverage ratio: pipeline value / revenue target (ideal: 3-4x)
3. Analisar stage distribution: pipeline está concentrado em early ou late stages?
4. Identificar deals "stuck" (sem movement por >2x average cycle time)
5. Calcular velocity metrics: average deal size, win rate, sales cycle length
6. Comparar pipeline metrics vs previous periods (MoM, QoQ, YoY)
7. Analisar pipeline por source: qual canal gera pipeline de maior qualidade?

### Fase 2: Quality Assessment (1-2 dias)
8. Audit top 20 deals: validate stage, close date, probability, next steps
9. Identificar deals com close dates que já passaram (pipeline hygiene)
10. Calcular weighted pipeline vs unweighted pipeline
11. Analisar win rate por: segment, deal size, source, rep, competitor
12. Identificar patterns de perda: quais são os top 3 loss reasons
13. Avaliar expansion pipeline: upsell e cross-sell opportunities em base existente
14. Calcular "pipeline creation rate" vs "pipeline consumption rate"

### Fase 3: Gap Analysis e Action Planning (1 dia)
15. Calcular gap entre pipeline weighted e revenue target
16. Identificar onde o gap está: top-of-funnel (leads), mid-funnel (conversion), bottom-of-funnel (close rate)
17. Para cada gap, definir ações corretivas específicas:
    - Top-of-funnel gap: increase demand gen, new channels, partnerships
    - Mid-funnel gap: improve qualification, better nurturing, product demos
    - Bottom-of-funnel gap: pricing, competitive positioning, executive alignment
18. Definir "must win" deals e executive actions para cada
19. Projetar pipeline needed para próximo quarter (work backwards from target)

### Fase 4: Review Meeting (60 minutos)
20. Apresentar pipeline health summary com key metrics
21. Review top deals com probabilidade e next steps
22. Discutir loss analysis e patterns
23. Alinhar ações corretivas com owners e deadlines
24. Atualizar revenue forecast baseado no pipeline review
25. Definir pipeline creation targets para próximo período

## Frameworks a Aplicar
- **Pipeline Coverage Ratio** — 3-4x coverage para healthy pipeline
- **Sales Velocity Formula** — (Deals x Win Rate x Deal Size) / Sales Cycle
- **Funnel Conversion Analysis** — Stage-to-stage conversion rates
- **MEDDIC/MEDDPICC** — Para qualification de deals (Metrics, Economic Buyer, Decision, etc)
- **Win/Loss Analysis** — Systematic review de deals ganhos e perdidos
- **Cohort Analysis** — Pipeline por cohort de criação para tracking de progression

## Checklists de Qualidade
- [ ] Pipeline data extraído e atualizado (max 24h lag)
- [ ] Coverage ratio calculado vs target
- [ ] Top 20 deals audited para accuracy
- [ ] Stuck deals identificados (>2x cycle time sem movement)
- [ ] Win rate calculado por segment, source, rep
- [ ] Loss reasons catalogados (top 3)
- [ ] Gap analysis completo (top/mid/bottom funnel)
- [ ] Ações corretivas definidas com owners
- [ ] Revenue forecast atualizado
- [ ] Pipeline creation targets definidos para próximo período
- [ ] Expansion pipeline incluído na análise

## Template de Entrega
```markdown
# Pipeline Review — [Period]

## Pipeline Summary
- **Total Pipeline:** [R$ X]
- **Weighted Pipeline:** [R$ Y]
- **Revenue Target:** [R$ Z]
- **Coverage Ratio:** [X.Xx] (target: 3-4x)
- **Pipeline vs Last Period:** [+/-X%]

## Pipeline by Stage
| Stage | # Deals | Value | Avg Size | Conversion Rate |
|-------|---------|-------|----------|-----------------|

## Velocity Metrics
| Metric | Current | Previous | Trend |
|--------|---------|----------|-------|
| Avg Deal Size | | | |
| Win Rate | | | |
| Sales Cycle (days) | | | |
| Sales Velocity | | | |

## Pipeline by Source
| Source | Pipeline Created | Win Rate | Avg Size | Cost per Opp |
|--------|-----------------|----------|----------|-------------|

## Top Deals
| Deal | Value | Stage | Close Date | Confidence | Next Step | Owner |
|------|-------|-------|------------|------------|-----------|-------|

## Loss Analysis
| Reason | # Deals | Value Lost | Action |
|--------|---------|------------|--------|

## Gap Analysis
- **Gap to Target:** [R$ X]
- **Gap Location:** [Top/Mid/Bottom funnel]
- **Root Cause:** [Analysis]

## Action Plan
| Action | Gap Addressed | Owner | Deadline | Expected Impact |
|--------|--------------|-------|----------|-----------------|

## Forecast Update
| Period | Previous Forecast | Updated Forecast | Confidence |
|--------|------------------|-----------------|------------|
```

## Registries para Atualizar
- `registries/metrics-log.md` — Pipeline metrics do período
- `registries/forecasts.md` — Revenue forecast atualizado
- `registries/action-items.md` — Ações corretivas com owners
- `registries/decisions-log.md` — Decisões de pricing ou strategy

## Critérios de Aceitação
1. Pipeline data 100% atualizado e auditado
2. Coverage ratio calculado com gap analysis
3. Top 20 deals revisados individualmente
4. Loss analysis com patterns identificados
5. Ações corretivas definidas com owners e deadlines
6. Revenue forecast atualizado e comunicado ao CFO
7. Pipeline creation targets definidos

## Dependências e Handoffs
- **Recebe de:** CRM Data, Marketing Attribution, Sales Reports
- **Entrega para:** Revenue Forecast (CFO), Demand Gen (Marketing), Product Feedback (CPO)
- **Cadência:** Semanal (light) + Mensal (deep)
- **Escalation path:** Coverage ratio <2x escala imediatamente para CEO
- **Integração:** Alimenta WBR (weekly) e MBR (monthly)
