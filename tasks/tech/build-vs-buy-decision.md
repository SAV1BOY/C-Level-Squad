# Build vs Buy Analysis

## Objetivo
Executar uma análise estruturada para decidir entre construir internamente (build) ou adquirir/licenciar solução de terceiros (buy) para uma necessidade de tecnologia. Esta decisão impacta budget, time-to-market, maintenance burden e strategic positioning — decisão errada custa anos e milhões.

## Agente Responsável
- **CTO Agent** — Ownership da análise técnica e recomendação

## Agentes de Suporte
- **CFO Agent** — TCO analysis e financial modeling
- **CIO Agent** — Integration requirements e vendor management
- **CPO Agent** — Product differentiation e customer impact
- **CEO Agent** — Strategic alignment e competitive positioning
- **COO Agent** — Operational readiness e support model
- **CAI Agent** — AI-specific build vs buy considerations

## Pré-requisitos
1. Clear definition do problema a ser resolvido
2. Requirements document (functional e non-functional)
3. Current state: como o problema é resolvido hoje (se aplicável)
4. Market scan de soluções disponíveis
5. Internal capability assessment (skills, capacity)
6. Budget constraints e timeline expectations
7. Strategic context: é core differentiator ou commodity?

## Processo (step-by-step)

### Fase 1: Requirements e Context (2-3 dias)
1. Documentar requirements: functional, non-functional, integration, security, compliance
2. Classificar a capability: core differentiator, context (necessary but not differentiating), ou commodity
3. Definir criticality: mission-critical, important, or nice-to-have
4. Estimar usage parameters: users, volume, growth rate, SLA requirements
5. Identificar integration points com sistemas existentes
6. Definir timeline: quando precisamos da capability ativa
7. Documentar constraints: budget, team availability, technology preferences

### Fase 2: Build Analysis (2-3 dias)
8. Estimar effort de build: design, development, testing, deployment (em person-months)
9. Definir team requirements: skills needed, availability, opportunity cost
10. Estimar timeline: from start to MVP, from MVP to production-ready
11. Calcular ongoing maintenance cost: bugs, updates, infrastructure, support (annual)
12. Identificar risks de build: scope creep, talent dependency, maintenance burden
13. Avaliar se build cria competitive advantage ou diferenciação
14. Estimar 5-year Total Cost of Ownership (TCO) para build

### Fase 3: Buy Analysis (2-3 dias)
15. Identificar top 3-5 vendor solutions no mercado
16. Avaliar cada solução contra requirements (feature fit score)
17. Obter pricing: license/subscription cost, implementation cost, training cost
18. Avaliar vendor viability: funding, customer base, roadmap, stability
19. Identificar integration effort e cost para cada solução
20. Avaliar lock-in risk: data portability, contract terms, switching cost
21. Calcular 5-year TCO para buy (license + implementation + integration + ongoing)
22. Identify customization needs e limits de cada solução

### Fase 4: Comparative Analysis (1-2 dias)
23. Criar comparison matrix: build vs top 2-3 buy options
24. Compare TCO (5-year) para cada opção
25. Compare time-to-value: quando cada opção entrega resultado
26. Compare risk profile: execution risk (build) vs vendor risk (buy)
27. Avaliar strategic fit: cada opção alinha com onde queremos estar em 5 anos?
28. Considerar hybrid option: buy base + build differentiating layer
29. Execute sensitivity analysis: como a decisão muda se assumptions mudarem

### Fase 5: Decision e Execution Plan (1 dia)
30. Apresentar análise para decision-making group
31. Documentar recomendação com rationale
32. Se BUILD: criar project plan com milestones
33. Se BUY: initiar procurement process e vendor negotiation
34. Se HYBRID: definir clear boundaries entre bought e built components
35. Definir success metrics e review checkpoint (6 meses após implementation)

## Frameworks a Aplicar
- **Core vs Context (Moore)** — Build core differentiators, buy context/commodity
- **TCO Analysis (5-year)** — Total Cost of Ownership incluindo hidden costs
- **Wardley Mapping** — Posicionar a capability na value chain e evolution axis
- **Decision Matrix** — Weighted scoring de build vs buy options
- **Risk-Adjusted ROI** — ROI ajustado por probabilidade de execução
- **Reversibility Test** — Quão fácil é reverter a decisão se der errado

## Checklists de Qualidade
- [ ] Requirements documentados (functional + non-functional)
- [ ] Capability classificada (core/context/commodity)
- [ ] Build effort estimado com confidence range
- [ ] Top 3+ vendor solutions avaliadas
- [ ] 5-year TCO calculado para build e buy options
- [ ] Integration effort estimado para cada option
- [ ] Vendor viability assessed
- [ ] Lock-in risk evaluated
- [ ] Strategic fit considered (5-year view)
- [ ] Hybrid option evaluated
- [ ] Sensitivity analysis performed
- [ ] Decision documented with rationale (ADR format)

## Template de Entrega
```markdown
# Build vs Buy Analysis — [Capability Name]

## Context
- **Problem:** [What we're solving]
- **Classification:** [Core / Context / Commodity]
- **Criticality:** [Mission-critical / Important / Nice-to-have]
- **Timeline:** [When needed]
- **Budget:** [Available]

## Requirements Summary
| Category | Requirements | Priority |
|----------|-------------|----------|
| Functional | | Must/Should/Could |
| Performance | | |
| Security | | |
| Integration | | |

## Build Option
- **Effort:** [X person-months]
- **Timeline:** [MVP: X months | Production: Y months]
- **Team:** [Skills needed, X people]
- **5-Year TCO:** [R$ X]
  - Development: [R$] | Maintenance: [R$] | Infrastructure: [R$]
- **Risks:** [Top 3]
- **Advantages:** [Customization, no vendor lock-in, etc.]

## Buy Options
| Criteria | Vendor A | Vendor B | Vendor C |
|----------|---------|---------|---------|
| Feature Fit | [X/10] | | |
| Annual Cost | [R$] | | |
| Implementation | [R$ + time] | | |
| 5-Year TCO | [R$] | | |
| Vendor Viability | [Score] | | |
| Lock-in Risk | [H/M/L] | | |
| Integration Effort | [weeks] | | |

## Comparison
| Factor | Weight | Build | Buy (Best) | Hybrid |
|--------|--------|-------|-----------|--------|
| Cost (5Y TCO) | [X%] | | | |
| Time to Value | [X%] | | | |
| Strategic Fit | [X%] | | | |
| Risk | [X%] | | | |
| Flexibility | [X%] | | | |
| **Weighted Score** | 100% | | | |

## Recommendation
- **Decision:** [Build / Buy / Hybrid]
- **Rationale:** [Key reasons]
- **Dissent:** [Alternative views]

## Execution Plan
[Next steps for chosen option]

## Review Checkpoint
- **Date:** [6 months post-implementation]
- **Success Metrics:** [How we'll know it was the right decision]
```

## Registries para Atualizar
- `registries/decisions-log.md` — Build vs buy decision with ADR
- `registries/resource-allocation.md` — Budget and team allocation
- `registries/vendor-registry.md` — If buy, vendor details registered
- `registries/tech-debt.md` — If build, maintenance tracked

## Critérios de Aceitação
1. Requirements clearly documented
2. Build effort estimated with confidence range
3. Top 3+ vendor solutions evaluated
4. 5-year TCO compared for all options
5. Decision documented as ADR with rationale
6. Execution plan defined with milestones
7. 6-month review checkpoint scheduled

## Dependências e Handoffs
- **Recebe de:** Product Requirements, Architecture Review, Market Scan
- **Entrega para:** Engineering (if build), Procurement (if buy), Architecture (ADR)
- **Cadência:** Ad-hoc (triggered by new capability need)
- **Timeline típico:** 2-3 weeks for analysis, decision in 1 session
- **Escalation path:** High-cost decisions (>R$ 500K TCO) require CEO approval
