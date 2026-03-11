# Decision Quality Review

## Objetivo
Avaliar a qualidade das decisões tomadas pelo executive team, identificando padrões de boas e más decisões e melhorando o processo decisório. Boas decisões repetidamente produzem bons resultados; o objetivo é melhorar o processo, não julgar decisões individuais com benefício de hindsight.

## Agente Responsável
- **COO Agent** — Facilitação do review e análise de processo

## Agentes de Suporte
- **CEO Agent** — Avaliação de decisões estratégicas e meta-decisões
- **CFO Agent** — Financial outcomes das decisões
- **CTO Agent** — Technical decision quality
- **CHRO Agent** — People decisions quality

## Pré-requisitos
1. Decisions log atualizado com decisões do período
2. Outcome data para decisões tomadas há >90 dias
3. Decision-making process documentation
4. Decision velocity data (time from identification to decision)
5. Stakeholder feedback on decision process

## Processo (step-by-step)

### Fase 1: Decision Inventory (1-2 dias)
1. Compilar todas as decisões significativas do período do decisions log
2. Classificar decisões por tipo: strategic, operational, financial, people, technical
3. Classify by reversibility: Type 1 (one-way door) vs. Type 2 (two-way door)
4. For decisions >90 days old, compile outcome data
5. Calculate decision velocity: average time from problem identification to decision
6. Identify decisions that were delayed or avoided (non-decisions)

### Fase 2: Quality Assessment (2-3 dias)
7. For each significant decision, assess process quality (not just outcome):
   - Was the right information available before deciding?
   - Were alternatives genuinely considered?
   - Were dissenting views heard and addressed?
   - Was the decision maker the right person?
   - Was the decision communicated clearly?
   - Was execution monitored?
8. Score each decision on process quality (1-5) independent of outcome
9. Assess outcome quality (1-5) for decisions with sufficient data
10. Create 2x2 matrix: good process + good outcome, good process + bad outcome, etc.
11. Identify decisions where bad process led to good outcomes (lucky) — these are risky patterns
12. Identify decisions where good process led to bad outcomes (unlucky) — validate process was genuinely good

### Fase 3: Pattern Analysis (1-2 dias)
13. Identify common decision biases observed: anchoring, sunk cost, groupthink, confirmation bias
14. Analyze decision velocity: are we too fast (not enough analysis) or too slow (analysis paralysis)?
15. Assess delegation patterns: are Type 2 decisions being escalated unnecessarily?
16. Evaluate diversity of input: are decisions informed by diverse perspectives?
17. Identify recurring decision types that could be systematized (decision rules, playbooks)
18. Assess disagree-and-commit effectiveness: do people truly commit after disagreeing?

### Fase 4: Improvement Plan (1 dia)
19. Recommend process improvements for top 3 decision quality gaps
20. Propose decision frameworks or checklists for recurring decision types
21. Recommend changes to delegation and decision rights
22. Define decision quality metrics for ongoing tracking
23. Present findings to executive team (with humility — not blame)

## Frameworks a Aplicar
- **Process vs. Outcome Matrix** — Separate decision quality from luck
- **Type 1 / Type 2 Decisions (Bezos)** — Match process rigor to reversibility
- **Pre-Mortem (Klein)** — Prospective analysis to improve decision quality
- **Cognitive Bias Checklist** — Systematic identification of biases
- **RAPID Decision Framework** — Clarity on who recommends, agrees, decides
- **Decision Journal** — Documenting context and reasoning at time of decision

## Checklists de Qualidade
- [ ] All significant decisions from the period compiled
- [ ] Decisions classified by type and reversibility
- [ ] Outcome data collected for decisions >90 days old
- [ ] Process quality scored independent of outcomes
- [ ] 2x2 matrix (process × outcome) created
- [ ] Decision biases identified
- [ ] Decision velocity analyzed
- [ ] Delegation patterns assessed
- [ ] Non-decisions (avoidance) identified
- [ ] Improvement recommendations documented
- [ ] Executive team debriefed with humility

## Template de Entrega
```markdown
# Decision Quality Review — [Period]

## Summary
- **Decisions Reviewed:** [X]
- **Avg Process Quality:** [X/5]
- **Avg Outcome Quality:** [X/5] (for decisions with data)
- **Avg Decision Velocity:** [X days]
- **Non-decisions Identified:** [X]

## Process-Outcome Matrix
| | Good Outcome | Bad Outcome |
|---|---|---|
| **Good Process** | [X decisions] (Deserved Success) | [X decisions] (Bad Luck) |
| **Bad Process** | [X decisions] (Good Luck) | [X decisions] (Deserved Failure) |

## Decision Velocity Analysis
| Type | Avg Time | Target | Status |
|------|----------|--------|--------|
| Type 1 (Irreversible) | [X days] | 1-2 weeks | |
| Type 2 (Reversible) | [X days] | 1-3 days | |

## Bias Patterns Observed
| Bias | Frequency | Examples | Mitigation |
|------|-----------|----------|-----------|
| Sunk Cost | | | |
| Groupthink | | | |
| Anchoring | | | |
| Confirmation | | | |

## Top Decision Learnings
### Best Decision: [Description]
- **Process:** [What we did right]
- **Learning:** [What to replicate]

### Worst Decision: [Description]
- **Process Gap:** [What went wrong]
- **Learning:** [What to improve]

## Improvement Recommendations
1. [Recommendation with expected impact]
2. [Recommendation with expected impact]
3. [Recommendation with expected impact]

## Decision Quality Metrics
| Metric | Baseline | Target | Measurement |
|--------|----------|--------|-------------|
```

## Registries para Atualizar
- `registries/decisions-log.md` — Annotate with quality scores
- `registries/lessons-learned.md` — Decision learnings
- `registries/risk-register.md` — Decision process risks

## Critérios de Aceitação
1. All significant decisions reviewed with process quality score
2. Outcome data collected for decisions with sufficient time elapsed
3. Decision biases identified with examples
4. Decision velocity analyzed
5. Top 3 improvement recommendations documented
6. Executive team debriefed
7. Decision quality metrics defined for tracking

## Dependências e Handoffs
- **Recebe de:** Decisions Log, Outcome Data, Stakeholder Feedback
- **Entrega para:** Decision Process Improvements, Training, Decision Frameworks
- **Cadência:** Trimestral
- **Escalation path:** Systemic decision quality issues escala to CEO and board
- **Integração:** Feeds into Board Prep, Quarterly Planning, Culture Audit
