# AI Vendor Evaluation

## Objetivo
Avaliar e selecionar vendors de AI (modelos, plataformas, ferramentas) de forma estruturada, garantindo que escolhemos parceiros que atendem requisitos técnicos, financeiros e de risco. O ecossistema de AI muda rapidamente — avaliação rigorosa evita lock-in em soluções que se tornam obsoletas.

## Agente Responsável
- **CAI Agent** — Ownership da avaliação e seleção de AI vendors

## Agentes de Suporte
- **CTO Agent** — Technical evaluation e integration requirements
- **CIO Agent** — Security, compliance e data governance
- **CFO Agent** — Financial analysis, contract negotiation
- **CEO Agent** — Strategic partnership decisions
- **COO Agent** — Operational requirements e support needs

## Pré-requisitos
1. AI use cases com requirements definidos
2. Current AI vendor landscape (what we already use)
3. Budget approved para AI tools/services
4. Security e compliance requirements checklist
5. Technical requirements: performance, latency, scale, integration
6. Data handling requirements (LGPD, residency, etc.)
7. Evaluation criteria aligned with stakeholders

## Processo (step-by-step)

### Fase 1: Market Scan (2-3 dias)
1. Define evaluation scope: model providers, platforms, tools, or specific capability
2. Scan market for relevant vendors: commercial, open source, emerging
3. Create long list of candidates (8-12 vendors)
4. Apply must-have filters to create short list (3-5 vendors):
   - Meets core functional requirements
   - Within budget range
   - Meets security/compliance baseline
   - Viable company (not going bankrupt)
5. Request demos or trial access from shortlisted vendors
6. Gather reference information from industry peers

### Fase 2: Deep Evaluation (3-5 dias)
7. Create weighted evaluation matrix with criteria:
   - Technical fit (capabilities, performance, accuracy)
   - Integration (APIs, SDKs, compatibility with our stack)
   - Security and compliance (certifications, data handling, audits)
   - Pricing model (per token, per user, per API call, enterprise)
   - Vendor viability (funding, revenue, customer base, team)
   - Support and SLAs (response time, coverage, escalation)
   - Roadmap alignment (where vendor is heading vs. where we need)
   - Lock-in risk (data portability, contract flexibility, standards)
8. Run technical POC with top 2-3 candidates using real use case data
9. Evaluate accuracy, latency, throughput on our specific workloads
10. Test integration with our existing systems
11. Verify security controls: encryption, authentication, data residency
12. Review contract terms: pricing escalation, termination, SLAs, liability

### Fase 3: Financial Analysis (1-2 dias)
13. Model total cost for each vendor at current e projected scale (1x, 3x, 10x)
14. Compare pricing models: which is cheaper at different scales?
15. Factor in integration and migration costs
16. Estimate switching cost if we need to change vendor later
17. Calculate 3-year TCO for each option
18. Negotiate pricing with preferred vendor(s)

### Fase 4: Decision e Contracting (1-2 dias)
19. Score vendors using weighted evaluation matrix
20. Present findings and recommendation to executive team
21. Select vendor with documented rationale
22. Negotiate final contract terms with procurement/legal
23. Define success criteria for first 90 days
24. Plan onboarding and integration
25. Document decision as ADR for future reference

## Frameworks a Aplicar
- **Weighted Scoring Matrix** — Criteria-based evaluation with stakeholder weights
- **POC Evaluation Protocol** — Structured technical proof of concept
- **TCO Analysis (3-year)** — Full cost including hidden and scaling costs
- **Vendor Viability Assessment** — Financial health, market position, team quality
- **Lock-in Risk Matrix** — Evaluate switching costs and portability
- **Reference Check Protocol** — Structured questions for vendor references

## Checklists de Qualidade
- [ ] Market scan completed with 8-12 candidates identified
- [ ] Short list of 3-5 vendors using must-have filters
- [ ] Weighted evaluation matrix created with stakeholder input
- [ ] Technical POC completed with top 2-3 candidates
- [ ] Security and compliance verified
- [ ] 3-year TCO calculated for each option
- [ ] Pricing negotiated with preferred vendor
- [ ] Contract terms reviewed by legal
- [ ] References checked
- [ ] Decision documented as ADR
- [ ] Onboarding plan created
- [ ] 90-day success criteria defined

## Template de Entrega
```markdown
# AI Vendor Evaluation — [Capability/Use Case]

## Evaluation Context
- **Need:** [What capability we're evaluating]
- **Use Cases:** [Which AI use cases this serves]
- **Timeline:** [When we need it]
- **Budget:** [Available]

## Long List
| Vendor | Category | Initial Fit | Pass Filter? |
|--------|----------|------------|-------------|

## Short List Evaluation
| Criteria | Weight | Vendor A | Vendor B | Vendor C |
|----------|--------|---------|---------|---------|
| Technical Fit | [X%] | [Score] | | |
| Integration | [X%] | | | |
| Security/Compliance | [X%] | | | |
| Pricing | [X%] | | | |
| Vendor Viability | [X%] | | | |
| Support/SLAs | [X%] | | | |
| Roadmap Alignment | [X%] | | | |
| Lock-in Risk | [X%] | | | |
| **Weighted Total** | 100% | | | |

## POC Results
| Test | Vendor A | Vendor B | Vendor C |
|------|---------|---------|---------|
| Accuracy | | | |
| Latency | | | |
| Throughput | | | |
| Integration Effort | | | |

## Financial Comparison
| Scale | Vendor A | Vendor B | Vendor C |
|-------|---------|---------|---------|
| Current (1x) | R$/month | | |
| Growth (3x) | R$/month | | |
| Scale (10x) | R$/month | | |
| 3-Year TCO | R$ | | |
| Switching Cost | R$ | | |

## Recommendation
- **Selected Vendor:** [Name]
- **Rationale:** [Top 3 reasons]
- **Trade-offs Accepted:** [What we're giving up]
- **Lock-in Mitigation:** [How we reduce vendor dependency]

## Onboarding Plan
| Step | Timeline | Owner |
|------|----------|-------|
| Contract signed | | |
| Integration started | | |
| First use case live | | |
| 90-day review | | |

## 90-Day Success Criteria
| Metric | Target |
|--------|--------|
```

## Registries para Atualizar
- `registries/vendor-registry.md` — AI vendor details
- `registries/decisions-log.md` — Vendor selection ADR
- `registries/resource-allocation.md` — AI vendor budget
- `registries/risk-register.md` — Vendor-related risks

## Critérios de Aceitação
1. Market scan with 8-12 candidates completed
2. Short list evaluated with weighted scoring matrix
3. Technical POC with top 2-3 vendors executed
4. 3-year TCO calculated and compared
5. Security and compliance verified
6. Vendor selected with documented rationale
7. Contract negotiated and signed

## Dependências e Handoffs
- **Recebe de:** AI Use Case Selection, Technical Requirements, Security Requirements
- **Entrega para:** AI Deployment, Procurement, Integration Planning
- **Cadência:** Ad-hoc (per vendor need) + Annual vendor re-evaluation
- **Escalation path:** Strategic vendor decisions (>R$ 500K) require CEO approval
- **Integração:** Feeds Model Evaluation, AI Deployment, Vendor Consolidation
