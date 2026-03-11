# Vendor Consolidation Review

## Objetivo
Revisar o portfólio de vendors de tecnologia, identificar oportunidades de consolidação e otimizar o total cost of ownership. Vendor sprawl gera complexidade, aumenta custos de gestão, fragmenta dados e enfraquece poder de negociação. Consolidação estratégica reduz custo e simplifica operações.

## Agente Responsável
- **CIO Agent** — Ownership de vendor management e consolidation

## Agentes de Suporte
- **CFO Agent** — Contract negotiation e financial analysis
- **CTO Agent** — Technical evaluation de consolidation options
- **COO Agent** — Operational impact assessment
- **CEO Agent** — Strategic vendor partnerships

## Pré-requisitos
1. Systems portfolio audit completo (ver `tasks/it-data/systems-audit.md`)
2. Vendor list com contracts, costs, renewal dates
3. Usage data por vendor/tool
4. Vendor performance data (uptime, support quality)
5. Integration dependencies entre vendor systems
6. Budget data para IT e SaaS spend

## Processo (step-by-step)

### Fase 1: Vendor Landscape Mapping (2-3 dias)
1. Compilar lista completa de vendors com: product, category, cost, contract end date
2. Agrupar vendors por categoria funcional: CRM, analytics, communication, security, etc.
3. Identificar overlap: múltiplos vendors na mesma categoria
4. Calcular total spend por categoria e per capita
5. Map vendor relationships: strategic partners vs. commodity suppliers
6. Identify contracts with renewal in next 6 months (negotiation opportunities)
7. Assess vendor concentration risk: single vendor dependency

### Fase 2: Consolidation Analysis (2-3 dias)
8. Para cada categoria com overlap, avaliar consolidation options
9. Calcular savings potential de consolidação: license reduction, negotiation leverage
10. Avaliar migration effort e cost para cada consolidation candidate
11. Identify vendors que podem expand scope (replace other vendors)
12. Evaluate platform vs. point solution strategy: quando consolidar vs. quando manter best-of-breed
13. Assess data migration complexity e risk
14. Calculate total consolidation ROI: savings - migration cost over 3 years

### Fase 3: Vendor Performance Review (1-2 dias)
15. Score each vendor: product quality, support, reliability, innovation, pricing fairness
16. Identify underperforming vendors: low satisfaction, frequent issues, poor support
17. Evaluate vendor financial health e long-term viability
18. Review contract terms: flexibility, termination clauses, price escalation
19. Benchmark pricing against market rates
20. Identify renegotiation opportunities (volume discounts, multi-year, bundling)

### Fase 4: Action Plan (1-2 dias)
21. Recommend consolidation actions: merge, replace, renegotiate, keep
22. Prioritize by: savings potential, effort, contract timing
23. Create vendor consolidation roadmap aligned with contract renewals
24. Prepare negotiation briefs for upcoming renewals
25. Define vendor governance framework going forward
26. Present recommendations to executive team

## Frameworks a Aplicar
- **Vendor Tiering** — Strategic, preferred, tactical, commodity classification
- **TCO Analysis** — Full cost including admin, integration, training, switching
- **Platform vs Best-of-Breed** — When to consolidate vs. when to keep specialized
- **Vendor Scorecard** — Standardized evaluation: quality, support, price, innovation
- **Contract Optimization** — Multi-year, volume, bundling negotiation strategies
- **Vendor Risk Framework** — Concentration risk, financial health, lock-in assessment

## Checklists de Qualidade
- [ ] Complete vendor inventory with costs and contracts
- [ ] Vendors grouped by category with overlap identified
- [ ] Savings potential calculated for each consolidation opportunity
- [ ] Migration effort estimated for consolidation candidates
- [ ] Vendor performance scored
- [ ] Contract renewal calendar created
- [ ] Negotiation briefs prepared for upcoming renewals
- [ ] Consolidation roadmap aligned with contract dates
- [ ] Vendor governance framework defined
- [ ] Executive team aligned on priorities

## Template de Entrega
```markdown
# Vendor Consolidation Review — [Date]

## Vendor Portfolio
- **Total Vendors:** [X]
- **Total Annual Spend:** [R$ X]
- **Categories with Overlap:** [X]
- **Savings Potential:** [R$ X/year]

## Vendor by Category
| Category | Vendors | Total Spend | Overlap? | Consolidation Opportunity |
|----------|---------|------------|---------|--------------------------|

## Consolidation Opportunities
| Opportunity | Current State | Target State | Savings/Year | Migration Cost | ROI (3Y) |
|------------|--------------|-------------|-------------|---------------|----------|

## Vendor Performance Scorecards
| Vendor | Quality | Support | Reliability | Innovation | Pricing | Overall |
|--------|---------|---------|------------|-----------|---------|---------|

## Contract Renewal Calendar
| Vendor | Contract End | Annual Value | Action | Negotiation Strategy |
|--------|------------|-------------|--------|---------------------|

## Recommendations
| Priority | Action | Vendors | Savings | Effort | Timeline |
|----------|--------|---------|---------|--------|----------|
| 1 | Consolidate [X into Y] | | | | |
| 2 | Renegotiate | | | | |
| 3 | Replace | | | | |

## Vendor Governance Framework
- **Tiering:** [Strategic / Preferred / Tactical / Commodity]
- **Review Cadence:** [Annual for strategic, bi-annual for others]
- **Approval Process:** [Thresholds for new vendor onboarding]
- **Performance SLAs:** [Expected standards]
```

## Registries para Atualizar
- `registries/vendor-registry.md` — Vendor details updated
- `registries/resource-allocation.md` — Budget adjustments
- `registries/decisions-log.md` — Consolidation decisions
- `registries/risk-register.md` — Vendor risks

## Critérios de Aceitação
1. Complete vendor inventory with spend data
2. Overlap identified across all categories
3. Savings potential quantified and validated
4. Vendor performance scored for strategic vendors
5. Consolidation roadmap created
6. Negotiation briefs prepared for next 6-month renewals
7. Governance framework defined

## Dependências e Handoffs
- **Recebe de:** Systems Audit, Contract Data (Finance), Usage Data
- **Entrega para:** Procurement, Budget Planning, Contract Negotiation
- **Cadência:** Anual (full review) + Triggered (before major renewals)
- **Escalation path:** Vendor failures impacting operations escalam para COO
- **Integração:** Alimenta Systems Audit e Budget Planning
