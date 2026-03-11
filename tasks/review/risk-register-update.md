# Risk Register Update

## Objetivo
Atualizar o registro de riscos da organização, avaliando riscos existentes, identificando novos riscos e garantindo que mitigações estão em andamento. O risk register é o early warning system da organização — riscos não documentados e não monitorados são os que causam as maiores surpresas.

## Agente Responsável
- **COO Agent** — Consolidação e facilitação do risk review

## Agentes de Suporte
- **CEO Agent** — Strategic e existential risks
- **CFO Agent** — Financial e regulatory risks
- **CTO Agent** — Technical e security risks
- **CIO Agent** — Data e systems risks
- **CAI Agent** — AI-specific risks
- **CHRO Agent** — People e organizational risks
- **CMO Agent** — Market e reputational risks

## Pré-requisitos
1. Current risk register
2. Incident log from the period
3. Market and competitive updates
4. Regulatory updates
5. Financial health indicators
6. Technology and security scan results
7. People metrics (attrition, engagement)

## Processo (step-by-step)

### Fase 1: Existing Risk Review (1-2 dias)
1. Review each risk in the current register for status update
2. For each risk, update: probability, impact, trend (increasing/stable/decreasing)
3. Assess mitigation effectiveness: are mitigation actions working?
4. Identify risks that can be closed (mitigated or no longer relevant)
5. Identify risks that have materialized (became incidents) and document learnings
6. Re-score all active risks with updated information

### Fase 2: New Risk Identification (1-2 dias)
7. Each C-Level agent identifies new risks in their domain:
   - CEO: strategic, competitive, market, board/investor risks
   - CFO: financial, cash flow, regulatory, compliance risks
   - CTO: technical, security, architecture, reliability risks
   - CIO: data, systems, integration, vendor risks
   - CAI: AI safety, bias, compliance, vendor risks
   - CHRO: talent, culture, succession, legal risks
   - CMO: brand, reputation, market, customer risks
8. For each new risk, document: description, category, probability, impact, trigger indicators
9. Define mitigation strategy: avoid, reduce, transfer, or accept
10. Assign risk owner (individual, not team)

### Fase 3: Risk Prioritization (1 dia)
11. Calculate risk score for all risks: probability × impact
12. Create risk heat map: visual representation of risk portfolio
13. Identify top 10 risks by score
14. Ensure top 10 risks all have active mitigation plans
15. Assess risk portfolio balance: are we over-concentrated in any category?
16. Identify risk correlations: risks that could trigger each other

### Fase 4: Action Planning e Communication (1 dia)
17. For each top 10 risk, verify mitigation plan has owner, timeline, and budget
18. Define monitoring indicators (leading indicators that signal risk increasing)
19. Update risk dashboard
20. Present risk update to executive team
21. Prepare risk summary for board (if quarterly board meeting approaching)
22. Schedule next risk register update

## Frameworks a Aplicar
- **Risk Matrix (Probability × Impact)** — Standard risk scoring and heat map
- **Risk Category Taxonomy** — Strategic, financial, operational, technical, people, compliance
- **Bow-Tie Analysis** — Threats → Risk Event → Consequences with barriers
- **Monte Carlo Simulation** — For quantitative risk analysis of financial risks
- **Risk Appetite Framework** — Define acceptable risk levels per category
- **PESTLE Analysis** — External risk scanning: Political, Economic, Social, Tech, Legal, Environmental

## Checklists de Qualidade
- [ ] All existing risks reviewed and updated
- [ ] New risks identified from each domain
- [ ] Risk scores calculated (probability × impact)
- [ ] Heat map updated
- [ ] Top 10 risks have active mitigation plans
- [ ] Risk owners assigned for all critical risks
- [ ] Monitoring indicators defined for top risks
- [ ] Closed risks documented with rationale
- [ ] Materialized risks documented with learnings
- [ ] Dashboard updated
- [ ] Executive team briefed
- [ ] Board summary prepared (if applicable)

## Template de Entrega
```markdown
# Risk Register Update — [Date]

## Risk Portfolio Summary
- **Total Active Risks:** [X]
- **Critical:** [X] | **High:** [X] | **Medium:** [X] | **Low:** [X]
- **New Risks Added:** [X]
- **Risks Closed:** [X]
- **Risks Materialized:** [X]

## Risk Heat Map
|        | Low Impact | Med Impact | High Impact | Critical Impact |
|--------|-----------|------------|-------------|-----------------|
| **High Prob** | | | | |
| **Med Prob** | | | | |
| **Low Prob** | | | | |

## Top 10 Risks
| # | Risk | Category | Prob | Impact | Score | Trend | Owner | Mitigation Status |
|---|------|----------|------|--------|-------|-------|-------|------------------|

## New Risks
| Risk | Category | Prob | Impact | Score | Mitigation Plan | Owner |
|------|----------|------|--------|-------|-----------------|-------|

## Closed Risks
| Risk | Reason Closed | Date |
|------|--------------|------|

## Materialized Risks
| Risk | What Happened | Impact | Learning |
|------|--------------|--------|---------|

## Risk by Category
| Category | Count | Avg Score | Trend |
|----------|-------|-----------|-------|
| Strategic | | | |
| Financial | | | |
| Operational | | | |
| Technical | | | |
| People | | | |
| Compliance | | | |
| AI | | | |

## Monitoring Indicators
| Risk | Indicator | Current | Threshold | Action if Crossed |
|------|-----------|---------|-----------|-------------------|
```

## Registries para Atualizar
- `registries/risk-register.md` — Full register updated
- `registries/decisions-log.md` — Risk acceptance decisions
- `registries/incidents-log.md` — Materialized risks cross-referenced
- `registries/lessons-learned.md` — Learnings from materialized risks

## Critérios de Aceitação
1. All existing risks reviewed and scored
2. New risks identified from all domains
3. Top 10 risks have mitigation plans with owners
4. Risk heat map updated and presented
5. Monitoring indicators defined for critical risks
6. Executive team briefed
7. Board summary prepared if board meeting approaching

## Dependências e Handoffs
- **Recebe de:** Each C-Level (domain risks), Incident Log, Market Intelligence
- **Entrega para:** Board Prep, Strategic Planning, Insurance Review, Compliance
- **Cadência:** Mensal (update) + Trimestral (deep review)
- **Escalation path:** New critical risks escala imediatamente to CEO
- **Integração:** Feeds Board Prep, Strategic Bets Review, Quarterly Planning
