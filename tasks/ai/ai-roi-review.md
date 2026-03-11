# AI ROI Review

## Objetivo
Avaliar o retorno sobre investimento das iniciativas de AI, determinando quais estão gerando valor e quais precisam de ajuste ou descontinuação. AI ROI é notoriamente difícil de medir — este processo garante que medimos corretamente e tomamos decisões baseadas em dados, não em hype.

## Agente Responsável
- **CAI Agent** — Ownership da análise de ROI de AI

## Agentes de Suporte
- **CFO Agent** — Financial validation e ROI methodology
- **COO Agent** — Operational impact measurement
- **CPO Agent** — Product AI impact e customer value
- **CEO Agent** — Strategic AI investment decisions

## Pré-requisitos
1. AI use cases deployed com métricas de sucesso definidas
2. Baseline data (pre-AI performance) para comparação
3. Cost data: infrastructure, models, team, tools
4. Adoption metrics por use case
5. Business impact data (time saved, revenue impact, cost reduction)
6. User satisfaction data

## Processo (step-by-step)

### Fase 1: Cost Compilation (1-2 dias)
1. Calcular total AI investment por use case: infrastructure, model costs, engineering time
2. Include overhead costs: management, governance, training, tooling
3. Separate one-time costs (development) from recurring costs (inference, monitoring)
4. Calculate cost per user, cost per query, cost per transaction
5. Compare actual costs with original projections
6. Benchmark AI spend against industry peers

### Fase 2: Value Measurement (2-3 dias)
7. For each use case, measure direct value: time saved, errors reduced, revenue generated
8. Calculate indirect value: faster decisions, better customer experience, competitive advantage
9. Measure adoption-adjusted value: actual value = theoretical value × adoption rate
10. Compare before/after metrics using baseline data
11. Account for attribution: isolate AI impact from other factors
12. Measure employee satisfaction change with AI tools
13. Measure customer satisfaction change with AI-powered features

### Fase 3: ROI Analysis (1-2 dias)
14. Calculate ROI per use case: (value generated - total cost) / total cost
15. Calculate payback period: when does cumulative value exceed cumulative cost
16. Compare ROI across use cases: which are the winners and losers
17. Analyze ROI trajectory: improving, stable, or declining
18. Calculate portfolio ROI: total AI investment vs total AI value
19. Project future ROI based on adoption trends and scale effects
20. Identify use cases below ROI threshold for potential kill

### Fase 4: Recommendations (1 dia)
21. Recommend: scale up, maintain, optimize, or kill each use case
22. Propose investment reallocation to higher-ROI use cases
23. Identify improvements that would increase ROI of underperformers
24. Define ROI targets for next review period
25. Present findings to executive team

## Frameworks a Aplicar
- **AI ROI Framework** — Direct value + indirect value - total cost
- **Payback Period Analysis** — Time to recover AI investment
- **Adoption-Adjusted Value** — Theoretical value × actual adoption rate
- **Attribution Analysis** — Isolate AI impact from confounding factors
- **AI Value Pyramid** — Efficiency → Quality → Innovation → Transformation
- **Portfolio ROI** — Aggregate view across all AI initiatives

## Checklists de Qualidade
- [ ] Total cost calculated per use case (including overhead)
- [ ] Direct value measured with data
- [ ] Indirect value estimated with methodology
- [ ] Adoption rates factored into value calculation
- [ ] Before/after comparison using baseline data
- [ ] ROI calculated per use case and portfolio
- [ ] Payback period calculated
- [ ] ROI trajectory analyzed (improving/declining)
- [ ] Underperformers identified with root cause
- [ ] Recommendations documented with rationale
- [ ] CFO validated financial methodology

## Template de Entrega
```markdown
# AI ROI Review — [Period]

## Portfolio Summary
- **Total AI Investment:** [R$ X]
- **Total Value Generated:** [R$ Y]
- **Portfolio ROI:** [X:1]
- **Payback Period:** [X months]
- **Use Cases Live:** [X]

## ROI by Use Case
| Use Case | Investment | Value | ROI | Payback | Adoption | Recommendation |
|----------|-----------|-------|-----|---------|----------|---------------|

## Cost Breakdown
| Category | Amount | % of Total |
|----------|--------|-----------|
| Infrastructure/Compute | | |
| Model API Costs | | |
| Engineering Time | | |
| Tools/Platforms | | |
| Training/Change Mgmt | | |
| Governance/Monitoring | | |

## Value Breakdown
| Use Case | Time Saved | Cost Reduced | Revenue Impact | Quality Improved |
|----------|-----------|-------------|---------------|-----------------|

## Trajectory Analysis
| Use Case | Q-2 ROI | Q-1 ROI | Current ROI | Trend |
|----------|---------|---------|-------------|-------|

## Recommendations
| Use Case | Action | Rationale | Expected Impact |
|----------|--------|-----------|-----------------|
| [Name] | Scale Up | High ROI, room to grow | +[X%] value |
| [Name] | Optimize | Good ROI but high cost | -[X%] cost |
| [Name] | Kill | Negative ROI, no path to positive | Save [R$ X] |

## Investment Reallocation
| From | To | Amount | Expected ROI Change |
|------|-----|--------|-------------------|

## Targets (Next Period)
| Metric | Current | Target |
|--------|---------|--------|
| Portfolio ROI | | |
| Adoption Rate | | |
| Cost per Query | | |
```

## Registries para Atualizar
- `registries/metrics-log.md` — AI ROI metrics
- `registries/decisions-log.md` — Scale/kill decisions
- `registries/resource-allocation.md` — AI budget adjustments
- `registries/initiatives.md` — AI initiative status updates

## Critérios de Aceitação
1. ROI calculated for all deployed AI use cases
2. Cost and value data validated by CFO
3. Adoption rates factored into analysis
4. Trajectory analysis showing trends
5. Clear recommendations per use case
6. Investment reallocation proposed if needed
7. Targets set for next review period

## Dependências e Handoffs
- **Recebe de:** AI Deployment Metrics, Financial Data, Adoption Data
- **Entrega para:** AI Use Case Selection (portfolio update), Budget Planning, Strategic Bets
- **Cadência:** Trimestral
- **Escalation path:** Portfolio ROI negative for 2+ quarters escala to CEO
- **Integração:** Feeds Select AI Use Cases e Quarterly Planning
