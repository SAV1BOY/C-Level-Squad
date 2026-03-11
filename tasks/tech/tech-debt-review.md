# Tech Debt Review and Prioritization

## Objetivo
Revisar o inventário de tech debt, avaliar impacto em velocity e reliability, e priorizar o que pagar agora vs. aceitar conscientemente. Tech debt não é inerentemente ruim — debt tomada conscientemente com plano de pagamento é alavancagem. Debt ignorada ou esquecida é risco.

## Agente Responsável
- **CTO Agent** — Ownership do tech debt inventory e priorização

## Agentes de Suporte
- **CPO Agent** — Trade-off entre features e debt paydown
- **CFO Agent** — Financial impact de tech debt (custo de manutenção, risco)
- **COO Agent** — Operational impact de debt em delivery velocity
- **CIO Agent** — Infrastructure e data debt components

## Pré-requisitos
1. Tech debt inventory existente (se houver)
2. Engineering velocity data (cycle time, throughput trends)
3. Incident data relacionado a debt (incidentes causados por código legado)
4. Code quality metrics (test coverage, complexity, dependency age)
5. Architecture review findings
6. Engineering team feedback sobre debt impact
7. Product roadmap (para avaliar trade-offs com features)

## Processo (step-by-step)

### Fase 1: Inventory e Discovery (3-5 dias)
1. Catalogar tech debt existente de todas as fontes: backlog, PRs, incident post-mortems
2. Solicitar input de cada engineering team: quais debts mais impactam seu dia-a-dia
3. Identificar debt não catalogada através de análise de: code complexity, test coverage gaps, dependency vulnerabilities
4. Classificar debt por tipo: code debt, architecture debt, infrastructure debt, test debt, documentation debt, dependency debt
5. Para cada debt item, documentar: description, age, owner (team/service), impact area
6. Estimar "interest rate" de cada debt: quanto custa mantê-la por quarter (incidents, slow down, workarounds)

### Fase 2: Impact Assessment (2-3 dias)
7. Calcular velocity impact: quanto a debt está desacelerando cada team
8. Correlacionar debt com incidents: quais debts causaram ou contribuíram para incidentes
9. Avaliar risk: quais debts representam security vulnerabilities ou compliance gaps
10. Calcular customer impact: debts que afetam user experience ou reliability
11. Estimar "cost of delay" de não pagar cada debt
12. Mapear debt que bloqueia ou dificulta product roadmap items
13. Calcular total "debt service" cost: quanto a organização gasta mantendo a debt

### Fase 3: Prioritization (1-2 dias)
14. Aplicar framework de priorização: Impact × Urgency / Effort
15. Classificar cada debt como: pay now, pay soon, pay later, accept (conscious decision)
16. Para "pay now" items: estimar effort e timeline
17. Para "accept" items: documentar racional e revisão date
18. Calcular capacity needed: quanto de engineering time dedicar a debt paydown
19. Propor "debt allocation": % de capacity por sprint dedicada a debt (sugestão: 15-20%)
20. Identificar debt que pode ser paga "along the way" (junto com features)

### Fase 4: Execution Planning (1-2 dias)
21. Criar debt paydown roadmap trimestral
22. Alocar debt items a teams com capacity e ownership
23. Definir success metrics: velocity improvement, incident reduction, DX improvement
24. Estabelecer tracking mechanism para debt paydown progress
25. Comunicar plano para engineering teams e product team

## Frameworks a Aplicar
- **Tech Debt Quadrant (Fowler)** — Reckless/Prudent × Deliberate/Inadvertent
- **Interest Rate Model** — Calcular o custo contínuo de manter a debt
- **Impact-Effort Matrix** — Priorizar pelo melhor ROI de paydown
- **Debt Allocation Policy** — % fixa de capacity para debt (15-20%)
- **Boy Scout Rule** — "Leave the code better than you found it" como cultura
- **Strangler Fig Pattern** — Para migrar sistemas legados incrementalmente

## Checklists de Qualidade
- [ ] Inventory completo com todos os debt items catalogados
- [ ] Cada debt classificada por tipo e severity
- [ ] Interest rate estimada para debt items significativos
- [ ] Velocity impact quantificado
- [ ] Incident correlation analysis feita
- [ ] Security e compliance debts priorizadas
- [ ] Debt allocation % definida e aprovada
- [ ] Paydown roadmap trimestral criado
- [ ] Success metrics definidos
- [ ] "Accept" decisions documentadas com revisão date
- [ ] Engineering teams aligned e bought-in

## Template de Entrega
```markdown
# Tech Debt Review — [Period]

## Debt Portfolio Summary
- **Total Debt Items:** [X]
- **Critical:** [X] | **High:** [X] | **Medium:** [X] | **Low:** [X]
- **Estimated Total Interest (per quarter):** [X engineering days]
- **Debt-Related Incidents (period):** [X]

## Debt by Type
| Type | Count | Interest/Quarter | Top Item |
|------|-------|-----------------|----------|
| Code | | | |
| Architecture | | | |
| Infrastructure | | | |
| Test | | | |
| Documentation | | | |
| Dependency | | | |

## Priority Queue
### Pay Now (This Quarter)
| Item | Type | Interest | Effort | Impact | Owner |
|------|------|----------|--------|--------|-------|

### Pay Soon (Next Quarter)
| Item | Type | Interest | Effort | Impact | Owner |
|------|------|----------|--------|--------|-------|

### Accept (Conscious Decision)
| Item | Rationale | Review Date | Owner |
|------|-----------|-------------|-------|

## Debt Allocation
- **Policy:** [X%] of engineering capacity per sprint
- **Equivalent:** [X days/week across org]

## Paydown Roadmap
| Quarter | Focus Areas | Items | Effort | Expected Impact |
|---------|------------|-------|--------|-----------------|

## Success Metrics
| Metric | Baseline | Target (EOQ) | Measurement |
|--------|----------|-------------|-------------|
| Engineering Velocity | | | |
| Incident Rate (debt-related) | | | |
| Test Coverage | | | |
| Dependency Age | | | |
```

## Registries para Atualizar
- `registries/tech-debt.md` — Full inventory atualizado
- `registries/decisions-log.md` — Debt acceptance decisions
- `registries/risk-register.md` — Debt-related risks
- `registries/resource-allocation.md` — Debt paydown allocation

## Critérios de Aceitação
1. Complete inventory of known tech debt
2. Each item classified by type and priority
3. Interest rate estimated for significant items
4. Velocity and incident impact quantified
5. Debt allocation policy defined and approved
6. Quarterly paydown roadmap created
7. "Accept" decisions documented with review dates

## Dependências e Handoffs
- **Recebe de:** Engineering Teams, Architecture Review, Incident Post-Mortems, Code Analysis
- **Entrega para:** Sprint Planning, Platform Roadmap, Budget Planning, Quarterly Planning
- **Cadência:** Trimestral (deep review) + Contínuo (new debt cataloging)
- **Escalation path:** Critical security debt escala imediatamente para CTO e CEO
- **Integração:** Alimenta Architecture Review e Engineering Health Check
