# Systems Portfolio Audit

## Objetivo
Auditar o portfólio completo de sistemas e ferramentas da organização, avaliando utilização, custo, redundância e alinhamento estratégico. Empresas acumulam sistemas ao longo do tempo como sedimento — sem audit regular, a organização paga por ferramentas não utilizadas, mantém integrações frágeis e perde eficiência por falta de consolidação.

## Agente Responsável
- **CIO Agent** — Ownership do systems portfolio e IT governance

## Agentes de Suporte
- **CFO Agent** — Cost analysis e contract review
- **CTO Agent** — Technical integration e architecture alignment
- **COO Agent** — Operational workflows e process dependencies
- **CHRO Agent** — HR tech stack e people systems
- **CAI Agent** — AI/data platform systems

## Pré-requisitos
1. Lista de todos os sistemas e ferramentas em uso (licensed e shadow IT)
2. Contract data: vendor, cost, renewal dates, terms
3. Usage data: active users, adoption rate, login frequency
4. Integration map: quais sistemas se conectam com quais
5. Support ticket data por sistema
6. Data flow documentation (se existente)
7. Previous audit findings (se existente)

## Processo (step-by-step)

### Fase 1: Discovery e Inventário (3-5 dias)
1. Catalogar todos os sistemas licenciados: nome, vendor, categoria, custo anual
2. Identificar shadow IT: ferramentas adquiridas por áreas sem aprovação central
3. Mapear cada sistema por categoria: core business, productivity, communication, analytics, security, etc.
4. Coletar usage data: active users vs. licensed seats, login frequency, feature adoption
5. Documentar todos os contracts: valor, vigência, renewal date, termination clause
6. Mapear integrações entre sistemas: data flows, APIs, manual transfers
7. Classificar cada sistema: mission-critical, important, nice-to-have, redundant

### Fase 2: Health Assessment (2-3 dias)
8. Para cada sistema, avaliar: utilization rate (active users / licensed seats)
9. Calcular cost per active user para cada sistema
10. Identificar redundancies: múltiplas ferramentas fazendo a mesma coisa
11. Avaliar satisfaction score: NPS ou feedback dos usuários por sistema
12. Mapear security posture: SSO integration, data handling, compliance
13. Avaliar vendor health: financial stability, roadmap, support quality
14. Identificar integration fragilities: point-to-point connections, manual workarounds

### Fase 3: Optimization Analysis (2-3 dias)
15. Identificar cost saving opportunities: unused licenses, right-sizing, renegotiation
16. Propor consolidation candidates: sistemas que podem ser combinados ou substituídos
17. Identify security gaps que precisam de remediação
18. Propor integration improvements para eliminar manual workarounds
19. Avaliar contract negotiation opportunities (renewals próximos)
20. Calcular total savings potential

### Fase 4: Recommendations e Roadmap (1-2 dias)
21. Criar systems portfolio roadmap: keep, optimize, consolidate, replace, decommission
22. Priorizar ações por: cost savings, risk reduction, efficiency gain
23. Estimar effort e investment para cada ação
24. Definir timeline de execução com dependencies
25. Apresentar findings e recommendations para executive team

## Frameworks a Aplicar
- **TIME Model (Gartner)** — Tolerate, Invest, Migrate, Eliminate para cada sistema
- **Application Portfolio Management** — Quadrant: business value vs. technical health
- **Total Cost of Ownership (TCO)** — Custo real incluindo admin, integration, training
- **Shadow IT Discovery** — Metodologia para identificar ferramentas não autorizadas
- **Integration Architecture Review** — Point-to-point vs. middleware vs. iPaaS
- **SaaS Rationalization** — Eliminar redundâncias e otimizar licenças

## Checklists de Qualidade
- [ ] Inventário completo de todos os sistemas (inclusive shadow IT)
- [ ] Usage data coletado para cada sistema
- [ ] Cost per active user calculado
- [ ] Redundancies identificadas
- [ ] Contract renewal dates mapeadas
- [ ] Integration map atualizado
- [ ] Security assessment por sistema
- [ ] Vendor health avaliado
- [ ] Cost savings quantificados
- [ ] Consolidation roadmap criado
- [ ] Recommendations priorizadas por ROI

## Template de Entrega
```markdown
# Systems Portfolio Audit — [Date]

## Portfolio Summary
- **Total Systems:** [X]
- **Total Annual Cost:** [R$ X]
- **Mission-Critical:** [X] | **Important:** [X] | **Nice-to-have:** [X] | **Redundant:** [X]

## Systems Inventory
| System | Category | Vendor | Annual Cost | Active Users | Licensed | Utilization | Classification |
|--------|----------|--------|------------|-------------|----------|-------------|---------------|

## Cost Analysis
- **Total IT Spend:** [R$ X/year]
- **Cost per Employee:** [R$ X]
- **Unused Licenses Cost:** [R$ X]
- **Savings Potential:** [R$ X]

## Redundancy Map
| Function | Systems | Recommended Action | Savings |
|----------|---------|-------------------|---------|

## Integration Health
| Integration | Systems | Type | Health | Issues |
|------------|---------|------|--------|--------|

## Security Assessment
| System | SSO | MFA | Data Classification | Compliance | Gap |
|--------|-----|-----|--------------------|-----------|----|

## Recommendations
| # | Action | Systems Affected | Savings/Year | Effort | Timeline |
|---|--------|-----------------|-------------|--------|----------|
| 1 | Decommission | | | | |
| 2 | Consolidate | | | | |
| 3 | Renegotiate | | | | |
| 4 | Right-size | | | | |

## Roadmap
| Quarter | Actions | Expected Savings | Investment |
|---------|---------|-----------------|------------|
```

## Registries para Atualizar
- `registries/systems-inventory.md` — Full systems catalog updated
- `registries/vendor-registry.md` — Vendor details e contracts
- `registries/risk-register.md` — IT risks identified
- `registries/resource-allocation.md` — IT budget adjustments

## Critérios de Aceitação
1. 100% dos sistemas inventariados com usage data
2. Cost savings quantificados e validated by CFO
3. Redundancies identified com consolidation plan
4. Security gaps flagged com remediation timeline
5. Contract renewal calendar created
6. Roadmap com quarterly actions defined
7. Executive team briefed e aligned

## Dependências e Handoffs
- **Recebe de:** Finance (contract data), IT (usage data), Security (compliance data)
- **Entrega para:** Vendor Consolidation, Budget Planning, Security Remediation
- **Cadência:** Anual (full audit) + Semestral (light check)
- **Escalation path:** Security gaps escalam imediatamente; cost overruns escalam para CFO
- **Integração:** Alimenta Vendor Consolidation e Automation Opportunities
