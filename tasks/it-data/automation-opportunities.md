# Identify Automation Opportunities

## Objetivo
Identificar e priorizar oportunidades de automação em processos operacionais, eliminando trabalho manual repetitivo e liberando capacity humana para trabalho de maior valor. Automação bem feita é um multiplicador de produtividade — automação mal feita é complexidade desnecessária.

## Agente Responsável
- **CIO Agent** — Ownership da estratégia de automação

## Agentes de Suporte
- **COO Agent** — Processos operacionais e workflow mapping
- **CTO Agent** — Technical feasibility e engineering support
- **CAI Agent** — AI-powered automation opportunities
- **CFO Agent** — ROI analysis e business case
- **CHRO Agent** — People impact e change management

## Pré-requisitos
1. Process inventory existente (ou time para discovery)
2. Time tracking ou estimates de effort por processo
3. Error rates e rework data por processo
4. Current automation tools e platforms disponíveis
5. Technical capability assessment (integration APIs, data access)
6. Budget disponível para automation investments
7. Team feedback sobre processos mais dolorosos

## Processo (step-by-step)

### Fase 1: Process Discovery (3-5 dias)
1. Mapear todos os processos repetitivos por área: operations, finance, HR, sales, support
2. Para cada processo, documentar: frequency, time per execution, error rate, owner
3. Identificar processos com alto volume e baixa complexidade (automação clássica)
4. Identificar processos com alto volume e alta complexidade (AI-powered automation)
5. Coletar feedback de teams: quais processos são mais dolorosos e repetitivos?
6. Estimar total hours/month gastos em trabalho manual automatizável
7. Mapear data flows necessários para cada automação potencial

### Fase 2: Opportunity Assessment (2-3 dias)
8. Para cada oportunidade, calcular: hours saved/month, error reduction, speed improvement
9. Classificar por automation approach: RPA, workflow automation, AI/ML, custom code, no-code
10. Estimar implementation effort: simple (days), moderate (weeks), complex (months)
11. Calcular ROI: (hours saved × cost per hour) / implementation cost
12. Avaliar technical feasibility: APIs disponíveis, data quality, integration complexity
13. Identificar dependencies: quais automações dependem de outras
14. Avaliar change management effort: training, process redesign, adoption

### Fase 3: Prioritization (1-2 dias)
15. Rank opportunities por ROI adjusted for feasibility
16. Identify quick wins: high ROI + low effort (implement first)
17. Identify strategic automations: high ROI + high effort (plan carefully)
18. Group automations by platform/tool para maximizar investment
19. Define automation roadmap com quarterly phases
20. Calculate total investment needed e expected ROI

### Fase 4: Execution Planning (1-2 dias)
21. Para quick wins: definir implementation plan (2-4 weeks each)
22. Para strategic automations: definir discovery phase antes de full implementation
23. Identify automation platform needs (tools, licenses, infrastructure)
24. Define testing e validation criteria para cada automação
25. Plan change management: communication, training, rollout
26. Define monitoring e maintenance plan post-implementation

## Frameworks a Aplicar
- **Automation ROI Calculator** — (Hours saved × hourly cost × 12 months) / Implementation cost
- **Complexity-Frequency Matrix** — Prioritize high-frequency, low-complexity first
- **Process Mining** — Data-driven discovery de processos e bottlenecks
- **Human-in-the-Loop Design** — Automação com supervisão humana para processos críticos
- **Build vs Buy for Automation** — RPA tools vs custom vs no-code platforms
- **Change Management (ADKAR)** — Awareness, Desire, Knowledge, Ability, Reinforcement

## Checklists de Qualidade
- [ ] Process inventory completo com volume e effort data
- [ ] Cada opportunity com ROI calculated
- [ ] Technical feasibility assessed
- [ ] Quick wins identified (implement in <4 weeks)
- [ ] Strategic automations identified (plan for next quarter)
- [ ] Automation platform needs defined
- [ ] Change management plan included
- [ ] Testing criteria defined
- [ ] Monitoring plan established
- [ ] Total investment e ROI calculated
- [ ] Roadmap created with quarterly phases

## Template de Entrega
```markdown
# Automation Opportunities — [Date]

## Summary
- **Processes Assessed:** [X]
- **Automation Candidates:** [X]
- **Total Hours Recoverable:** [X hours/month]
- **Estimated Annual Savings:** [R$ X]
- **Investment Required:** [R$ X]
- **Payback Period:** [X months]

## Opportunity Inventory
| Process | Area | Frequency | Hours/Month | Error Rate | Approach | ROI | Priority |
|---------|------|-----------|------------|-----------|----------|-----|----------|

## Quick Wins (This Quarter)
| Automation | Hours Saved | Implementation | ROI | Owner | Timeline |
|-----------|------------|---------------|-----|-------|----------|

## Strategic Automations (Next Quarters)
| Automation | Hours Saved | Complexity | Investment | ROI | Timeline |
|-----------|------------|-----------|------------|-----|----------|

## Platform Requirements
| Tool/Platform | Purpose | Cost | Automations Enabled |
|--------------|---------|------|-------------------|

## Roadmap
| Quarter | Automations | Investment | Expected Savings |
|---------|------------|------------|-----------------|
| Q1 | Quick wins: [list] | R$ X | R$ Y/month |
| Q2 | [Strategic batch 1] | R$ X | R$ Y/month |

## Change Management Plan
| Automation | Affected Teams | Training Needed | Communication |
|-----------|---------------|----------------|---------------|

## Risk Mitigation
| Risk | Mitigation |
|------|-----------|
| Over-automation | Keep human-in-the-loop for critical processes |
| Tool sprawl | Consolidate on 2-3 automation platforms |
| Adoption failure | Involve users early, iterate based on feedback |
```

## Registries para Atualizar
- `registries/initiatives.md` — Automation initiatives registered
- `registries/resource-allocation.md` — Automation investment
- `registries/decisions-log.md` — Automation platform decisions
- `registries/metrics-log.md` — Baseline metrics before automation

## Critérios de Aceitação
1. Process inventory with volume and effort data complete
2. ROI calculated for all automation candidates
3. Quick wins identified and implementation started
4. Automation roadmap with quarterly phases created
5. Platform needs defined and budgeted
6. Change management plan included
7. Executive team aligned on investment and priorities

## Dependências e Handoffs
- **Recebe de:** Systems Audit, Process Documentation, Team Feedback
- **Entrega para:** Implementation Teams, Budget Planning, Change Management
- **Cadência:** Semestral (opportunity scan) + Contínuo (implementation)
- **Escalation path:** Automation blocking critical processes escala para COO
- **Integração:** Alimenta AI Use Cases e Vendor Consolidation
