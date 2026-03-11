# Team Health Check

## Objetivo
Avaliar a saúde das equipes executivas e operacionais, identificando dinâmicas disfuncionais, conflitos não resolvidos e oportunidades de fortalecimento. Uma equipe doente produz resultados doentes — team health check é o exame preventivo que evita crises maiores.

## Agente Responsável
- **CHRO Agent** — Ownership de team effectiveness e organizational health

## Agentes de Suporte
- **CEO Agent** — Executive team health e intervention decisions
- **COO Agent** — Team performance data e operational effectiveness
- **CTO Agent** — Engineering team health e technical culture

## Pré-requisitos
1. Team composition e structure data
2. Team performance data (OKR scores, delivery metrics)
3. Employee engagement data por equipe
4. Attrition data por equipe (voluntary, involuntary)
5. 360 feedback data (if available)
6. Previous team health check results (if any)
7. Manager feedback about team dynamics

## Processo (step-by-step)

### Fase 1: Health Data Collection (1-2 semanas)
1. Deploy team health survey (Spotify model or similar) with dimensions:
   - Mission clarity: do we know why we exist and what success looks like?
   - Psychological safety: can we speak up, disagree, and fail safely?
   - Collaboration: do we work well together and with other teams?
   - Speed: do we deliver at the pace we should?
   - Learning: do we improve continuously?
   - Engagement: are we energized and motivated?
   - Fun: do we enjoy working together?
   - Support: does the organization support us to do our best work?
2. Collect attrition data per team (last 12 months)
3. Collect engagement scores per team
4. Collect delivery metrics per team (velocity, throughput, quality)
5. Gather manager observations about team dynamics

### Fase 2: Analysis (2-3 dias)
6. Score each team across all dimensions (Green/Yellow/Red or 1-5 scale)
7. Identify teams with multiple Yellow/Red dimensions (at-risk teams)
8. Identify patterns across teams: common strengths and common weaknesses
9. Correlate team health with team performance (do healthy teams deliver more?)
10. Identify manager effectiveness patterns: healthy teams often have effective managers
11. Compare results with previous health check (trends)
12. Identify bright spots: teams with exceptional health to learn from

### Fase 3: Intervention Planning (1-2 dias)
13. For at-risk teams: diagnose root cause (leadership, workload, clarity, conflict, skills)
14. Design specific interventions per at-risk team:
    - Leadership issue: coaching, training, or manager change
    - Workload issue: reprioritization, headcount, automation
    - Clarity issue: goal setting, role clarity workshop
    - Conflict issue: mediation, facilitated conversation
    - Skills issue: training, hiring, knowledge sharing
15. For healthy teams: identify what to preserve and amplify
16. For organization-wide patterns: propose systemic interventions
17. Define success metrics and check-in timeline for each intervention

### Fase 4: Execution e Follow-up (ongoing)
18. Brief team managers on findings (their team's results)
19. Execute interventions with CHRO support
20. Schedule follow-up health check in 90 days for at-risk teams
21. Share bright spots and best practices across organization
22. Report aggregate findings to executive team
23. Track intervention effectiveness over time

## Frameworks a Aplicar
- **Spotify Squad Health Check** — Multi-dimension team assessment with colored indicators
- **Lencioni 5 Dysfunctions** — Trust, conflict, commitment, accountability, results
- **Google Project Aristotle** — Psychological safety, dependability, structure, meaning, impact
- **Team Effectiveness Model** — Context, composition, dynamics, outcomes
- **Manager Effectiveness Assessment** — Coaching, support, clarity, development
- **Burnout Assessment** — Exhaustion, cynicism, inefficacy

## Checklists de Qualidade
- [ ] Team health survey deployed with >75% response rate
- [ ] All teams scored across health dimensions
- [ ] At-risk teams identified with root cause analysis
- [ ] Bright spot teams identified with best practices
- [ ] Patterns across teams analyzed
- [ ] Correlation with performance data completed
- [ ] Interventions designed for at-risk teams
- [ ] Managers briefed on their team results
- [ ] Follow-up check-in scheduled (90 days)
- [ ] Aggregate findings shared with executive team

## Template de Entrega
```markdown
# Team Health Check — [Date]

## Organization Summary
- **Teams Assessed:** [X]
- **Survey Response Rate:** [X%]
- **Healthy Teams:** [X] ([%])
- **At-Risk Teams:** [X] ([%])
- **Critical Teams:** [X] ([%])

## Health by Dimension (Organization Average)
| Dimension | Score | Status | Trend |
|-----------|-------|--------|-------|
| Mission Clarity | | | |
| Psychological Safety | | | |
| Collaboration | | | |
| Speed | | | |
| Learning | | | |
| Engagement | | | |
| Fun | | | |
| Support | | | |

## Team-Level Results
| Team | Manager | Overall | Worst Dimension | Best Dimension | Trend | Action |
|------|---------|---------|----------------|----------------|-------|--------|

## At-Risk Teams
### [Team Name]
- **Score:** [X/5]
- **Key Issues:** [Top 2-3 dimensions]
- **Root Cause:** [Analysis]
- **Intervention:** [Plan]
- **Follow-up:** [Date]

## Bright Spots
### [Team Name]
- **Score:** [X/5]
- **What They Do Well:** [Practices to share]
- **Best Practice to Replicate:** [Specific practice]

## Organization-Wide Patterns
| Pattern | Teams Affected | Root Cause | Systemic Fix |
|---------|---------------|-----------|-------------|

## Interventions Summary
| Team | Intervention | Owner | Timeline | Success Metric |
|------|-------------|-------|----------|----------------|

## Manager Effectiveness
| Manager | Team Health | Delivery | Attrition | Action |
|---------|-----------|----------|-----------|--------|
```

## Registries para Atualizar
- `registries/metrics-log.md` — Team health scores
- `registries/risk-register.md` — Team-related risks
- `registries/action-items.md` — Intervention actions
- `registries/org-chart.md` — Manager effectiveness data

## Critérios de Aceitação
1. Survey deployed with >75% response rate
2. All teams scored and classified
3. At-risk teams identified with intervention plans
4. Bright spots documented with replicable practices
5. Managers briefed on their team's results
6. Follow-up schedule defined (90 days for at-risk)
7. Executive summary delivered to leadership

## Dependências e Handoffs
- **Recebe de:** Engagement Survey, Performance Data, Attrition Data, Manager Feedback
- **Entrega para:** Interventions, Manager Coaching, Org Design, Resource Planning
- **Cadência:** Trimestral (survey) + Contínuo (interventions)
- **Escalation path:** Teams with critical health scores escala to CEO
- **Integração:** Feeds Culture Audit, Org Design, Engineering Health Check
