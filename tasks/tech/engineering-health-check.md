# Engineering Health Check (DORA)

## Objetivo
Avaliar a saúde geral da organização de engenharia usando DORA metrics e indicadores complementares, identificando áreas de excelência e áreas que precisam de investimento. Uma engenharia saudável é o engine de uma empresa de tecnologia — se o engine falha, todo o resto para.

## Agente Responsável
- **CTO Agent** — Ownership de engineering health e standards

## Agentes de Suporte
- **CHRO Agent** — Engineer satisfaction, retention, hiring
- **COO Agent** — Delivery velocity e operational metrics
- **CPO Agent** — Product delivery health e quality
- **CFO Agent** — Engineering efficiency e cost per delivery
- **CIO Agent** — Tooling e infrastructure health

## Pré-requisitos
1. DORA metrics data collection configured
2. Engineering team survey (satisfaction, engagement)
3. Hiring e retention data para engineering
4. Code quality metrics (test coverage, complexity, PR review time)
5. Delivery data (stories completed, cycle time, throughput)
6. Incident data e on-call metrics
7. Engineering budget e headcount data

## Processo (step-by-step)

### Fase 1: Metrics Collection (2-3 dias)
1. Calcular DORA metrics para cada team e aggregate:
   - **Deployment Frequency:** How often code deploys to production
   - **Lead Time for Changes:** Time from commit to production
   - **Change Failure Rate:** % of deployments causing failure
   - **Mean Time to Recovery:** Time to restore service after failure
2. Classificar cada metric: Elite, High, Medium, Low (per DORA benchmarks)
3. Coletar engineering productivity metrics: cycle time, throughput, WIP limits adherence
4. Medir code quality: test coverage, code review turnaround, merge frequency
5. Calcular developer satisfaction score (from survey)
6. Medir "maker time" ratio: % of time engineers spend in flow vs. meetings/context switches

### Fase 2: Team-Level Analysis (2-3 dias)
7. Analyze DORA metrics by team: identify top performing e underperforming teams
8. Identify patterns: what do high-performing teams do differently?
9. Assess team stability: turnover, ramp-up time for new members
10. Evaluate team autonomy: how much do teams depend on other teams?
11. Assess cognitive load: is each team's scope manageable?
12. Review on-call burden per team: pages, interruptions, toil
13. Calculate cost per story point or cost per deployment (efficiency metric)

### Fase 3: Organizational Health Assessment (1-2 dias)
14. Compile hiring metrics: time to hire, offer acceptance rate, quality of hire
15. Analyze retention: voluntary attrition rate, tenure distribution, regrettable attrition
16. Evaluate engineering career framework: clarity, progression, compensation competitiveness
17. Assess L&D investment: training hours, conference attendance, learning budget
18. Review diversity metrics (if tracked): representation, inclusion scores
19. Evaluate management span of control e manager effectiveness
20. Assess engineering culture: innovation time, hackathons, open source contributions

### Fase 4: Improvement Planning (1-2 dias)
21. Identify top 3 improvement areas based on data
22. For each area, define specific improvement initiatives
23. Estimate effort e investment for each initiative
24. Define success metrics e timeline
25. Present findings e plan to engineering leadership
26. Communicate relevant findings to executive team

## Frameworks a Aplicar
- **DORA Metrics** — The four key metrics for software delivery performance
- **SPACE Framework** — Satisfaction, Performance, Activity, Communication, Efficiency
- **Team Topologies** — Stream-aligned, platform, enabling, complicated-subsystem teams
- **Cognitive Load Theory** — Intrinsic, extraneous, germane load per team
- **Accelerate Book Model** — Capabilities that drive software delivery performance
- **Westrum Organizational Culture** — Pathological, bureaucratic, generative culture types

## Checklists de Qualidade
- [ ] DORA metrics calculated for all teams
- [ ] DORA classification applied (Elite/High/Medium/Low)
- [ ] Developer satisfaction survey completed
- [ ] Maker time ratio measured
- [ ] Team-level analysis completed (patterns identified)
- [ ] Hiring e retention metrics compiled
- [ ] Career framework assessed
- [ ] Cognitive load per team evaluated
- [ ] On-call burden assessed
- [ ] Top 3 improvement areas identified with action plans
- [ ] Engineering cost efficiency calculated
- [ ] Culture assessment completed

## Template de Entrega
```markdown
# Engineering Health Check — [Period]

## DORA Metrics (Aggregate)
| Metric | Value | Classification | Trend | Target |
|--------|-------|---------------|-------|--------|
| Deployment Frequency | | Elite/High/Med/Low | | |
| Lead Time for Changes | | Elite/High/Med/Low | | |
| Change Failure Rate | | Elite/High/Med/Low | | |
| Mean Time to Recovery | | Elite/High/Med/Low | | |

## DORA by Team
| Team | Deploy Freq | Lead Time | CFR | MTTR | Overall |
|------|------------|-----------|-----|------|---------|

## Productivity Metrics
| Metric | Value | Trend | Benchmark |
|--------|-------|-------|-----------|
| Cycle Time | | | |
| Throughput (stories/sprint) | | | |
| Maker Time Ratio | | | |
| PR Review Turnaround | | | |
| Test Coverage | | | |

## Team Health
| Team | Stability | Autonomy | Cognitive Load | On-Call Burden | Score |
|------|-----------|----------|---------------|----------------|-------|

## People Metrics
| Metric | Value | Benchmark | Trend |
|--------|-------|-----------|-------|
| Headcount | | | |
| Voluntary Attrition | | | |
| Time to Hire | | | |
| Offer Accept Rate | | | |
| Developer Satisfaction | | | |
| Maker Time Ratio | | | |

## Efficiency
| Metric | Value | Trend |
|--------|-------|-------|
| Cost per Deployment | | |
| Cost per Story Point | | |
| Revenue per Engineer | | |
| Infrastructure Cost per Engineer | | |

## Culture Assessment
- **Westrum Type:** [Pathological / Bureaucratic / Generative]
- **Innovation Time:** [X% of time]
- **Learning Investment:** [R$ per engineer per year]

## Top 3 Improvement Areas
### 1. [Area]
- **Current State:** [Data]
- **Target:** [Where we want to be]
- **Initiative:** [What we'll do]
- **Effort:** [Investment needed]
- **Timeline:** [When]

### 2. [Area]
[Same structure]

### 3. [Area]
[Same structure]

## Overall Engineering Health Score: [X/10]
- Trend: [Improving / Stable / Declining]
```

## Registries para Atualizar
- `registries/metrics-log.md` — DORA e engineering metrics
- `registries/risk-register.md` — Engineering health risks
- `registries/initiatives.md` — Improvement initiatives
- `registries/resource-allocation.md` — Engineering investment decisions

## Critérios de Aceitação
1. DORA metrics calculated and classified for all teams
2. Developer satisfaction measured
3. Team-level analysis completed
4. People metrics (hiring, retention) compiled
5. Top 3 improvement areas identified with action plans
6. Findings presented to engineering leadership
7. Executive summary shared with C-Level team

## Dependências e Handoffs
- **Recebe de:** CI/CD Systems, HR Data, Survey Data, Incident Data, Code Repos
- **Entrega para:** Platform Roadmap, People Planning, Budget Planning, Quarterly Planning
- **Cadência:** Trimestral
- **Escalation path:** DORA metrics declining for 2+ quarters escala para CEO
- **Integração:** Alimenta Reliability Review, Tech Debt Review, Org Design Review
