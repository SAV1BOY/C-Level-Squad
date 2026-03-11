# Select and Prioritize AI Use Cases

## Objetivo
Identificar, avaliar e priorizar use cases de AI para a organização, garantindo que investimentos em AI são direcionados para as oportunidades com maior impacto de negócio e maior feasibility técnica. AI sem use case claro é hype; AI com use case errado é desperdício.

## Agente Responsável
- **CAI Agent** — Ownership da seleção e priorização de AI use cases

## Agentes de Suporte
- **CEO Agent** — Strategic alignment e priorização de investimento
- **CTO Agent** — Technical feasibility e engineering capacity
- **CIO Agent** — Data readiness e infrastructure
- **CPO Agent** — Product AI features e customer-facing use cases
- **COO Agent** — Operational AI use cases e process optimization
- **CFO Agent** — ROI analysis e budget allocation

## Pré-requisitos
1. AI strategy document ou vision statement
2. Data governance review findings (ver `tasks/it-data/data-governance-review.md`)
3. Process inventory com automation opportunities
4. Product roadmap com AI feature candidates
5. Competitive AI adoption intelligence
6. Current AI capabilities (models, tools, skills in-house)
7. Budget disponível para AI initiatives

## Processo (step-by-step)

### Fase 1: Use Case Discovery (3-5 dias)
1. Facilitar workshops com cada área para brainstorm de AI use cases
2. Categorizar use cases por tipo: automation, augmentation, insight generation, creation
3. Categorizar por área: product (customer-facing), operations (internal), analytics (decision-support)
4. Para cada use case, documentar: problem statement, current process, expected outcome
5. Estimar impact potencial: time saved, revenue generated, cost reduced, quality improved
6. Coletar inspiração de peers e competitors: quais AI use cases já estão provados no mercado
7. Identificar use cases que poderiam ser quick wins vs. transformational bets

### Fase 2: Feasibility Assessment (2-3 dias)
8. Para cada use case, avaliar data readiness: dados disponíveis, quality, volume
9. Avaliar technical complexity: off-the-shelf model vs. custom training vs. fine-tuning
10. Estimar implementation effort: prototype (weeks), MVP (months), production (quarters)
11. Assess skill availability: temos as skills necessárias internamente?
12. Evaluate infrastructure needs: compute, storage, monitoring
13. Identify integration requirements: como AI se conecta com sistemas existentes
14. Assess risk profile: ethical, legal, reputational risks de cada use case

### Fase 3: Prioritization (1-2 dias)
15. Score cada use case em 4 dimensões: business impact, feasibility, strategic fit, risk
16. Plot use cases em matrix: impact × feasibility
17. Select top 5-8 use cases para próximos 12 meses
18. Classify selected: 2-3 quick wins (deliver in <3 months) + 2-3 strategic bets (6-12 months)
19. Estimate total investment for selected portfolio
20. Define sequencing based on dependencies e learnings cascade

### Fase 4: Business Case e Approval (1-2 dias)
21. Build business case para cada selected use case: problem, solution, ROI, timeline, risks
22. Define success metrics para cada use case (quantitative + qualitative)
23. Define MVP scope: smallest version that proves value
24. Present portfolio to executive team for approval
25. Secure budget e resource commitment
26. Define governance: review cadence, escalation, kill criteria

## Frameworks a Aplicar
- **AI Use Case Canvas** — Problem, data, approach, value, risk, feasibility per use case
- **Impact-Feasibility Matrix** — Prioritization visual para portfolio selection
- **AI Readiness Assessment** — Data, tech, skills, org readiness per use case
- **Build-Buy-Partner Matrix** — For each use case, best approach to implement
- **AI Ethics Checklist** — Bias, fairness, transparency, privacy per use case
- **Value-Effort Estimation** — Rough sizing for portfolio planning

## Checklists de Qualidade
- [ ] Use case workshops conducted with all areas
- [ ] Each use case has problem statement e expected outcome
- [ ] Data readiness assessed per use case
- [ ] Technical feasibility scored
- [ ] Business impact estimated (quantitative)
- [ ] Risk profile assessed (ethical, legal, reputational)
- [ ] Portfolio limited to 5-8 use cases
- [ ] Quick wins and strategic bets identified
- [ ] Business case built per selected use case
- [ ] Success metrics defined
- [ ] MVP scope defined
- [ ] Budget and resources approved

## Template de Entrega
```markdown
# AI Use Case Portfolio — [Period]

## Portfolio Summary
- **Total Use Cases Identified:** [X]
- **Selected for Implementation:** [X]
- **Quick Wins:** [X] | **Strategic Bets:** [X]
- **Total Investment:** [R$ X]
- **Expected Annual Value:** [R$ X]

## Selected Use Cases

### Use Case 1: [Name]
- **Category:** [Automation / Augmentation / Insight / Creation]
- **Area:** [Product / Operations / Analytics]
- **Problem:** [What problem it solves]
- **Solution Approach:** [Off-the-shelf / Fine-tune / Custom]
- **Data Readiness:** [High/Med/Low]
- **Impact Score:** [1-5]
- **Feasibility Score:** [1-5]
- **Investment:** [R$ X]
- **Expected ROI:** [X:1]
- **Timeline:** [MVP date, Production date]
- **Success Metrics:** [KPIs]
- **Risks:** [Top 3]
- **Kill Criteria:** [When to stop]

## Prioritization Matrix
[Impact vs Feasibility plot of all use cases]

## Implementation Roadmap
| Quarter | Use Cases | Investment | Expected Value |
|---------|----------|------------|---------------|

## Resource Requirements
| Resource | Need | Have | Gap | Plan |
|----------|------|------|-----|------|
| Data Engineers | | | | |
| ML Engineers | | | | |
| Compute/GPU | | | | |
| Data | | | | |

## Governance
- **Review Cadence:** [Monthly progress, Quarterly portfolio review]
- **Kill Criteria Review:** [When to assess]
- **Escalation Path:** [For blockers or pivots]
```

## Registries para Atualizar
- `registries/initiatives.md` — AI initiatives registered
- `registries/resource-allocation.md` — AI budget and team allocation
- `registries/decisions-log.md` — Use case selection decisions
- `registries/risk-register.md` — AI-specific risks

## Critérios de Aceitação
1. Comprehensive use case discovery across all areas
2. Feasibility assessed with data readiness scoring
3. Portfolio limited to 5-8 prioritized use cases
4. Business case built for each selected use case
5. Budget and resources approved
6. Implementation roadmap with quarterly milestones
7. Governance framework defined

## Dependências e Handoffs
- **Recebe de:** Data Governance Review, Automation Opportunities, Product Roadmap
- **Entrega para:** AI Deployment, Model Evaluation, AI ROI Review
- **Cadência:** Semestral (portfolio review) + Quarterly (progress check)
- **Escalation path:** Use case with ethical concerns escala for CEO + Legal review
- **Integração:** Feeds into Quarterly Planning and Budget Allocation
