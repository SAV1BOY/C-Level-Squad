# Marketing ROI Review

## Objetivo
Avaliar o retorno sobre investimento de todas as atividades de marketing, determinando quais investimentos estão gerando valor e quais são ineficientes. Este review garante que cada real investido em marketing contribui para growth de forma mensurável e sustentável.

## Agente Responsável
- **CMO Agent** — Ownership da análise de ROI e otimização

## Agentes de Suporte
- **CFO Agent** — Financial validation e budget analysis
- **CPO Agent** — Product-marketing alignment e conversion data
- **CEO Agent** — Strategic marketing investments approval
- **CIO Agent** — Marketing tech stack e data accuracy

## Pré-requisitos
1. Marketing spend data por categoria e campanha
2. Attribution data (first-touch, last-touch, multi-touch)
3. Revenue data atribuível a marketing efforts
4. Pipeline data por marketing source
5. Brand metrics (awareness, consideration, preference)
6. Customer acquisition data por canal e campanha
7. Marketing tech stack costs

## Processo (step-by-step)

### Fase 1: Data Compilation (2-3 dias)
1. Consolidar todo marketing spend por categoria: paid media, content, events, tools, headcount
2. Mapear spend para resultados: impressions, leads, MQLs, SQLs, opportunities, revenue
3. Calcular ROI por categoria: (revenue attributed - cost) / cost
4. Calcular blended CAC: total marketing spend / new customers acquired
5. Analisar time-to-impact: quanto tempo entre spend e revenue realization
6. Mapear marketing tech stack costs e utilization rates
7. Compilar brand metrics como leading indicators de future revenue

### Fase 2: Performance Analysis (1-2 dias)
8. Rank campaigns e programs por ROI (top to bottom)
9. Identificar top performers: o que têm em comum (audience, message, channel, timing)?
10. Identificar underperformers: o que falhou e por quê?
11. Analisar efficiency trends: ROI improving or declining over time?
12. Calcular marginal ROI: qual é o retorno do próximo real investido em cada canal?
13. Benchmarking: como nosso marketing efficiency compara com industry benchmarks?
14. Avaliar brand investment ROI: impacto de brand em conversion rates e pricing power

### Fase 3: Optimization Recommendations (1-2 dias)
15. Propor reallocation de budget para maximizar ROI total
16. Identificar areas de "waste": spend com ROI negativo ou immeasurable
17. Propor budget cuts em areas de baixo ROI com savings quantificados
18. Identificar high-ROI areas que estão underfunded
19. Recomendar mix optimization: brand vs. performance marketing
20. Definir targets de efficiency para próximo período
21. Propor melhorias em attribution e measurement capabilities

### Fase 4: Review e Decisão (1 dia)
22. Apresentar marketing ROI analysis para executive team
23. CFO valida financial accuracy dos cálculos
24. Discutir reallocation proposals e trade-offs
25. Aprovar budget adjustments
26. Definir ROI targets para próximo período

## Frameworks a Aplicar
- **Marketing ROI Formula** — (Revenue Attributed - Marketing Cost) / Marketing Cost
- **Attribution Modeling** — First-touch, last-touch, multi-touch, time-decay
- **Marginal ROI Analysis** — ROI do incremental dollar por canal
- **Marketing Funnel Efficiency** — Conversion rates stage-by-stage
- **Brand Equity Metrics** — Awareness, consideration, preference como leading indicators
- **Customer Journey Attribution** — Mapeamento completo do caminho do cliente

## Checklists de Qualidade
- [ ] Todo marketing spend catalogado por categoria
- [ ] Attribution model documentado e confiável
- [ ] ROI calculado por categoria, canal e campanha
- [ ] Blended CAC calculado e trended
- [ ] Top e bottom performers identificados com root cause
- [ ] Marginal ROI por canal calculado
- [ ] Industry benchmarks comparados
- [ ] Reallocation proposals com expected impact
- [ ] Waste areas identificadas com savings quantificados
- [ ] ROI targets definidos para próximo período
- [ ] Tech stack utilization reviewed

## Template de Entrega
```markdown
# Marketing ROI Review — [Period]

## Summary
- **Total Marketing Spend:** [R$ X]
- **Revenue Attributed:** [R$ Y]
- **Blended ROI:** [X:1]
- **Blended CAC:** [R$ X]
- **Marketing as % of Revenue:** [X%]

## ROI by Category
| Category | Spend | Revenue | ROI | Trend | Recommendation |
|----------|-------|---------|-----|-------|---------------|
| Paid Media | | | | | |
| Content | | | | | |
| Events | | | | | |
| Partnerships | | | | | |
| Brand | | | | | |
| Tools/Tech | | | | | |
| Headcount | | | | | |

## Top Performers
| Campaign/Program | Spend | Revenue | ROI | Learning |
|-----------------|-------|---------|-----|---------|

## Underperformers
| Campaign/Program | Spend | Revenue | ROI | Root Cause | Action |
|-----------------|-------|---------|-----|-----------|--------|

## Funnel Efficiency
| Stage | Volume | Conversion | Cost per | Benchmark |
|-------|--------|-----------|----------|-----------|
| Impressions | | | | |
| Leads | | | | |
| MQLs | | | | |
| SQLs | | | | |
| Opportunities | | | | |
| Customers | | | | |

## Reallocation Proposal
| From | To | Amount | Expected ROI Improvement |
|------|-----|--------|------------------------|

## Targets (Next Period)
| Metric | Current | Target | Improvement |
|--------|---------|--------|-------------|
| Blended ROI | | | |
| CAC | | | |
| Marketing % of Revenue | | | |
```

## Registries para Atualizar
- `registries/metrics-log.md` — Marketing ROI metrics
- `registries/resource-allocation.md` — Budget adjustments
- `registries/decisions-log.md` — Reallocation decisions
- `registries/experiments-log.md` — Test results e learnings

## Critérios de Aceitação
1. ROI calculado para todas as categorias de marketing spend
2. Attribution model documentado com confidence levels
3. Top e bottom performers identificados com learnings
4. Reallocation proposals com financial modeling
5. Budget adjustments aprovados pelo CFO
6. ROI targets definidos para próximo período
7. Measurement improvement plan se attribution gaps identificados

## Dependências e Handoffs
- **Recebe de:** Marketing Analytics, CRM Data, Financial Data (CFO)
- **Entrega para:** Budget Allocation, Channel Strategy, Quarterly Planning
- **Cadência:** Mensal (light) + Trimestral (deep)
- **Escalation path:** Marketing ROI <1x sustentado por 2+ meses escala para CEO
- **Integração:** Alimenta Channel Strategy Review e Pipeline Review
