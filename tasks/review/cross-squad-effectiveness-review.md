# Cross-Squad Effectiveness Review

## Objetivo
Avaliar a eficácia da colaboração entre squads/equipes executivas, identificando silos, dependências problemáticas e oportunidades de melhoria na coordenação. A velocidade de uma organização é limitada pela velocidade das suas interfaces entre equipes.

## Agente Responsável
- **COO Agent** — Facilitação e análise de cross-squad effectiveness

## Agentes de Suporte
- **CEO Agent** — Resolução de conflitos de prioridade entre squads
- **CHRO Agent** — Team dynamics e collaboration culture
- **CTO Agent** — Technical cross-team dependencies
- **CPO Agent** — Product cross-team coordination

## Pré-requisitos
1. Cross-functional dependency map
2. Blocker log from WBRs (cross-team blockers)
3. Initiative delivery data (delays caused by cross-team dependencies)
4. Employee survey data on cross-team collaboration
5. Communication patterns data (if available)
6. Meeting load data per person/team

## Processo (step-by-step)

### Fase 1: Collaboration Assessment (2-3 dias)
1. Map all cross-squad dependencies: who depends on whom for what
2. Identify the most critical cross-squad interfaces (highest frequency + highest impact)
3. For each critical interface, assess: clarity of ownership, SLA adherence, communication quality
4. Analyze blocker log: how many blockers are cross-squad vs. intra-squad
5. Calculate cross-squad delay: average time added to delivery by cross-team dependencies
6. Survey teams on cross-squad collaboration quality (1-5 scale per interface)
7. Identify "collaboration tax": how much time teams spend coordinating vs. executing

### Fase 2: Pattern Analysis (1-2 dias)
8. Identify the most problematic cross-squad interfaces (highest delay, most complaints)
9. Root cause analysis for each problematic interface: unclear ownership, misaligned priorities, poor communication, process gaps
10. Identify bright spots: cross-squad interfaces that work exceptionally well — what can we learn?
11. Assess meeting effectiveness: are cross-squad meetings productive or wasteful?
12. Evaluate documentation and handoff quality between squads
13. Identify shadow work: informal coordination happening outside processes

### Fase 3: Improvement Design (1-2 dias)
14. For top 3 problematic interfaces, design specific improvements:
    - Ownership clarity: define clear owner for each handoff point
    - SLA definition: agree on response times and quality standards
    - Communication protocol: how and when to communicate across squads
    - Escalation path: clear path when things get stuck
15. Propose structural changes if interface problems are systemic (team restructuring, shared goals)
16. Design collaboration rituals: regular syncs, shared dashboards, joint planning
17. Define cross-squad effectiveness metrics for ongoing tracking

### Fase 4: Implementation e Monitoring (ongoing)
18. Implement improvements starting with highest-impact interfaces
19. Communicate changes to affected teams
20. Monitor effectiveness of changes (30-60-90 day check-ins)
21. Report findings and improvements to executive team
22. Share best practices organization-wide

## Frameworks a Aplicar
- **Dependency Matrix** — Map and classify all cross-team dependencies
- **Interface Quality Assessment** — Clarity, SLA, communication per interface
- **Collaboration Tax Calculation** — Time spent coordinating vs. executing
- **Team Topologies Interaction Modes** — Collaboration, X-as-a-Service, Facilitating
- **Conway's Law** — Org structure shapes system design and collaboration
- **Value Stream Mapping** — Identify waste in cross-squad handoffs

## Checklists de Qualidade
- [ ] All cross-squad dependencies mapped
- [ ] Critical interfaces identified and assessed
- [ ] Cross-squad blockers analyzed from WBR data
- [ ] Collaboration survey completed
- [ ] Problematic interfaces root-caused
- [ ] Bright spots identified with replicable practices
- [ ] Top 3 interfaces have improvement plans
- [ ] Metrics defined for ongoing tracking
- [ ] Changes communicated to affected teams
- [ ] Follow-up check-ins scheduled

## Template de Entrega
```markdown
# Cross-Squad Effectiveness Review — [Date]

## Summary
- **Cross-Squad Interfaces Mapped:** [X]
- **Critical Interfaces:** [X]
- **Problematic Interfaces:** [X]
- **Avg Cross-Squad Collaboration Score:** [X/5]
- **Cross-Squad Blockers (period):** [X]
- **Collaboration Tax:** [X% of time]

## Interface Assessment
| Interface | Squads | Frequency | Clarity | SLA | Quality | Score | Status |
|-----------|--------|-----------|---------|-----|---------|-------|--------|

## Problematic Interfaces
### [Interface Name]
- **Squads:** [A ↔ B]
- **Score:** [X/5]
- **Issues:** [Root cause]
- **Impact:** [Delay/cost]
- **Improvement Plan:** [Actions]

## Bright Spots
### [Interface Name]
- **What Works:** [Practices]
- **Replicable:** [How to apply elsewhere]

## Cross-Squad Blockers Analysis
| Category | Count | % | Avg Resolution Time |
|----------|-------|---|-------------------|
| Unclear Ownership | | | |
| Priority Misalignment | | | |
| Communication Gap | | | |
| Process Gap | | | |
| Resource Constraint | | | |

## Improvement Plan
| Interface | Improvement | Owner | Timeline | Expected Impact |
|-----------|------------|-------|----------|-----------------|

## Metrics
| Metric | Baseline | Target | Measurement |
|--------|----------|--------|-------------|
| Cross-squad collaboration score | | | Survey quarterly |
| Cross-squad blockers/month | | | WBR tracking |
| Cross-squad delay (avg days) | | | Delivery tracking |
```

## Registries para Atualizar
- `registries/metrics-log.md` — Cross-squad metrics
- `registries/action-items.md` — Improvement actions
- `registries/decisions-log.md` — Interface redesign decisions
- `registries/org-chart.md` — If structural changes recommended

## Critérios de Aceitação
1. All cross-squad dependencies mapped
2. Critical interfaces assessed with scores
3. Problematic interfaces root-caused with improvement plans
4. Bright spots documented for replication
5. Metrics defined for ongoing tracking
6. Executive team aligned on improvements
7. Follow-up review scheduled (90 days)

## Dependências e Handoffs
- **Recebe de:** WBR Blocker Data, Team Health Check, Delivery Metrics, Survey Data
- **Entrega para:** Org Design Review, Process Improvements, Team Topologies
- **Cadência:** Trimestral
- **Escalation path:** Persistent cross-squad dysfunction escala to CEO for structural decision
- **Integração:** Feeds Org Design Review, Team Health Check, Quarterly Planning
