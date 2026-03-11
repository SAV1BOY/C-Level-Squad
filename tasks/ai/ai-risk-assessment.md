# AI Risk Assessment

## Objetivo
Avaliar e mitigar riscos associados ao uso de AI na organização, cobrindo dimensões de segurança, ética, compliance, operacional e reputacional. AI amplifica tanto benefícios quanto riscos — uma falha de AI pode ter consequências muito maiores e mais rápidas que uma falha de software tradicional.

## Agente Responsável
- **CAI Agent** — Ownership de AI risk management

## Agentes de Suporte
- **CTO Agent** — Technical security e robustness
- **CIO Agent** — Data protection e compliance
- **CEO Agent** — Reputational risk e strategic decisions
- **CFO Agent** — Financial risk e liability
- **CHRO Agent** — Workforce impact e ethical considerations

## Pré-requisitos
1. AI use cases inventory (deployed e planned)
2. Guardrails specification (ver `tasks/ai/eval-and-guardrails.md`)
3. Regulatory landscape (AI Act, LGPD, sector-specific)
4. Incident history (AI-related issues)
5. Current risk register
6. Industry AI risk benchmarks
7. Insurance coverage review

## Processo (step-by-step)

### Fase 1: Risk Identification (2-3 dias)
1. Para cada AI use case, identificar riscos em 6 categorias:
   - **Safety:** Outputs incorretos causando dano (healthcare, finance, safety-critical)
   - **Bias/Fairness:** Discriminação em decisões automatizadas
   - **Privacy:** Vazamento de dados pessoais, training data exposure
   - **Security:** Adversarial attacks, prompt injection, model theft
   - **Operational:** Model degradation, dependency on vendor, cost explosion
   - **Reputational:** Public backlash, customer trust erosion, brand damage
2. Document cada risco com: description, trigger, impact, affected stakeholders
3. Identify emerging risks from industry incidents e research
4. Map regulatory requirements per use case (current e anticipated regulation)
5. Assess workforce displacement risks e ethical implications

### Fase 2: Risk Assessment (2-3 dias)
6. Score cada risco: probability (1-5) × impact (1-5) = risk score
7. Classify risks: critical (>15), high (10-15), medium (5-9), low (<5)
8. Assess current mitigations in place for each risk
9. Calculate residual risk: risk score after considering existing mitigations
10. Identify risk interdependencies: one risk triggering another
11. Evaluate worst-case scenarios para critical risks
12. Benchmark against industry risk profile

### Fase 3: Mitigation Planning (1-2 dias)
13. For each critical e high risk, define mitigation strategy: avoid, reduce, transfer, accept
14. Design specific mitigation actions with owners e timelines
15. Estimate mitigation cost e effort
16. Define monitoring indicators: early warning signals for each risk
17. Create incident response plan for AI-specific incidents
18. Review insurance coverage for AI-related liabilities
19. Define escalation procedures for AI incidents

### Fase 4: Governance e Monitoring (1 dia)
20. Establish AI risk governance framework: roles, responsibilities, review cadence
21. Define AI risk appetite statement: what level of risk is acceptable
22. Create AI risk dashboard with key indicators
23. Schedule regular risk reviews (monthly monitoring, quarterly deep assessment)
24. Communicate risk profile to executive team e board
25. Document everything for regulatory audit readiness

## Frameworks a Aplicar
- **NIST AI Risk Management Framework** — Govern, Map, Measure, Manage
- **Risk Matrix (Probability × Impact)** — Standard risk scoring
- **AI Ethics Principles** — Fairness, accountability, transparency, safety, privacy
- **EU AI Act Risk Categories** — Unacceptable, high, limited, minimal risk
- **OWASP Top 10 for LLMs** — Security risks specific to language models
- **Responsible AI Maturity Model** — Assess organizational AI governance maturity

## Checklists de Qualidade
- [ ] All AI use cases assessed for risks in 6 categories
- [ ] Each risk scored (probability × impact)
- [ ] Critical and high risks have mitigation plans
- [ ] Regulatory requirements mapped per use case
- [ ] Incident response plan for AI-specific events
- [ ] Monitoring indicators defined for key risks
- [ ] AI risk appetite statement documented
- [ ] Insurance coverage reviewed
- [ ] Risk dashboard created
- [ ] Executive team briefed
- [ ] Audit-ready documentation prepared

## Template de Entrega
```markdown
# AI Risk Assessment — [Date]

## Risk Portfolio Summary
- **AI Use Cases Assessed:** [X]
- **Total Risks Identified:** [X]
- **Critical:** [X] | **High:** [X] | **Medium:** [X] | **Low:** [X]
- **Mitigation Coverage:** [X% of critical/high risks have active mitigations]

## Risk Heat Map
| Use Case | Safety | Bias | Privacy | Security | Operational | Reputational | Overall |
|----------|--------|------|---------|----------|------------|-------------|---------|

## Critical Risks
| Risk | Use Case | Probability | Impact | Score | Mitigation | Owner | Status |
|------|----------|-------------|--------|-------|-----------|-------|--------|

## Regulatory Compliance
| Regulation | Requirement | Status | Gap | Remediation | Deadline |
|-----------|------------|--------|-----|------------|----------|

## Monitoring Indicators
| Indicator | Threshold | Current | Frequency | Owner |
|-----------|-----------|---------|-----------|-------|

## Incident Response Plan
| Scenario | Severity | Response Steps | Owner | SLA |
|----------|----------|---------------|-------|-----|
| Model producing harmful output | P0 | 1. Disable 2. Investigate 3. Fix 4. Post-mortem | | <1h |
| Data privacy breach | P0 | 1. Contain 2. Notify 3. Investigate 4. Report | | <4h |

## AI Risk Appetite
[Statement of acceptable risk levels per category]

## Governance
- **Risk Owner:** [CAI Agent]
- **Review Cadence:** Monthly monitoring, quarterly deep assessment
- **Escalation:** Critical risks → CEO; regulatory → Legal + CEO
- **Board Reporting:** Quarterly AI risk summary
```

## Registries para Atualizar
- `registries/risk-register.md` — AI risks cataloged
- `registries/compliance-tracker.md` — AI compliance status
- `registries/decisions-log.md` — Risk acceptance decisions
- `registries/incidents-log.md` — AI incident history

## Critérios de Aceitação
1. All AI use cases risk-assessed across 6 categories
2. Risk scoring complete with probability × impact
3. Mitigation plans for all critical and high risks
4. Regulatory compliance mapped and gaps identified
5. Incident response plan documented and tested
6. Risk dashboard operational
7. Executive team and board briefed

## Dependências e Handoffs
- **Recebe de:** AI Use Cases, Guardrails, Deployment Data, Incident Data
- **Entrega para:** Risk Register, Board Reporting, Compliance Remediation, Insurance
- **Cadência:** Trimestral (deep assessment) + Mensal (monitoring)
- **Escalation path:** Critical AI risk escala imediatamente para CEO
- **Integração:** Feeds AI Guardrails review e Board Prep
