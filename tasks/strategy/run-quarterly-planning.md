# Run Quarterly Planning Cycle

## Objetivo
Executar o ciclo completo de planejamento trimestral, traduzindo as strategic bets em OKRs trimestrais, alocando recursos, definindo milestones e garantindo alinhamento cross-functional. O resultado é um plano de execução de 13 semanas com accountability clara.

## Agente Responsável
- **COO Agent** — Orchestração do processo de planejamento e consolidação

## Agentes de Suporte
- **CEO Agent** — Aprovação final de OKRs e prioridades
- **CFO Agent** — Budget allocation e financial targets por área
- **CTO Agent** — Capacity planning técnico e trade-offs de engenharia
- **CPO Agent** — Product roadmap alignment
- **CMO Agent** — Marketing plan e pipeline targets
- **CHRO Agent** — Headcount planning e talent gaps
- **CIO Agent** — Systems e data readiness
- **CAI Agent** — AI initiatives integration

## Pré-requisitos
1. Strategic bets document atualizado (ver `tasks/strategy/define-vision-and-bets.md`)
2. Resultado do QBR do trimestre anterior (ver `tasks/operating-system/run-qbr.md`)
3. Financial actuals do trimestre anterior
4. Headcount atual e aprovado
5. Backlog de iniciativas priorizado por cada área
6. Customer feedback consolidado (NPS, churn, expansion data)
7. Competitive intelligence atualizada

## Processo (step-by-step)

### Fase 1: Retrospectiva e Context Setting (Dia 1-2)
1. Compilar resultados do trimestre anterior: OKR scores, financial performance, key wins/losses
2. Executar retrospectiva formal: o que funcionou, o que não funcionou, o que aprendemos
3. Atualizar o contexto estratégico: mudanças no mercado, novos dados, shifts competitivos
4. CEO apresenta prioridades atualizadas e qualquer ajuste nas strategic bets
5. CFO apresenta financial outlook e constraints de budget para o próximo trimestre

### Fase 2: OKR Drafting (Dia 3-5)
6. Cada C-Level drafta OKRs para sua área, alinhados às strategic bets
7. Limitar a 3-5 Objectives por área com 2-4 Key Results cada
8. Cada Key Result deve ser mensurável, com baseline, target e stretch goal
9. Identificar cross-functional dependencies entre OKRs de diferentes áreas
10. CFO valida que a soma dos investments nos OKRs cabe no budget
11. Documentar resource asks (headcount, budget, tools) por OKR

### Fase 3: Alignment e Negotiation (Dia 6-8)
12. Sessão de alignment cross-functional: cada líder apresenta seus OKRs
13. Identificar conflitos de recurso e dependências não resolvidas
14. Negociar trade-offs: o que entra, o que sai, o que muda de timeline
15. Aplicar stack ranking forçado: se só pudéssemos fazer 3 coisas, quais seriam?
16. COO facilita resolução de conflitos e documenta decisões
17. Garantir que pelo menos 20% de capacity está reservada para trabalho não planejado

### Fase 4: Detalhamento do Plano (Dia 9-11)
18. Quebrar cada OKR em milestones de 4 semanas (Week 4, Week 8, Week 12)
19. Definir owner para cada milestone (pessoa, não grupo)
20. Criar dependency map visual mostrando interdependências entre milestones
21. Definir early warning indicators para cada OKR (leading metrics)
22. Estabelecer cadência de check-ins: weekly para milestones, bi-weekly para OKRs
23. Documentar risks e mitigations para cada OKR

### Fase 5: Aprovação e Comunicação (Dia 12-13)
24. CEO faz review final e aprova o plano trimestral
25. CFO confirma budget allocation final
26. Preparar comunicação para toda a organização (all-hands deck)
27. Publicar OKRs em sistema acessível a todos
28. Cada líder faz kickoff com seu time nas primeiras 48h do trimestre
29. COO agenda todos os check-ins recorrentes no calendário

## Frameworks a Aplicar
- **OKR Framework (Doerr)** — Objectives and Key Results com scoring 0.0-1.0
- **RICE Scoring** — Reach, Impact, Confidence, Effort para priorização de iniciativas
- **Dependency Mapping** — Visualização de interdependências cross-functional
- **Capacity Planning Model** — 70/20/10 (core/adjacent/transformational)
- **Pre-Mortem por OKR** — Identificar riscos antes de commitar
- **Stack Ranking Forçado** — Priorização cruel para garantir foco

## Checklists de Qualidade
- [ ] Retrospectiva do trimestre anterior documentada com learnings
- [ ] Máximo de 5 Objectives por área, 2-4 KRs por Objective
- [ ] Cada KR tem baseline, target e stretch goal quantificados
- [ ] Cross-functional dependencies mapeadas e owners definidos
- [ ] Budget allocation aprovada pelo CFO
- [ ] Headcount plan alinhado com CHRO
- [ ] 20% buffer de capacity preservado para unplanned work
- [ ] Milestones de 4 semanas definidos com owners individuais
- [ ] Early warning indicators definidos para cada OKR
- [ ] Comunicação all-hands preparada e agenda de kickoffs definida
- [ ] Todos os check-ins recorrentes agendados
- [ ] Plano aprovado pelo CEO com sign-off documentado

## Template de Entrega
```markdown
# Quarterly Plan — Q[X] [Year]

## Context
- **Previous Quarter Score:** [0.0-1.0 average]
- **Key Learnings:** [Top 3 insights]
- **Strategic Bets Active:** [Lista]
- **Budget Available:** [R$ X]
- **Headcount:** [Current / Approved]

## Company OKRs
### O1: [Objective]
- KR1: [Metric] — Baseline: [X] → Target: [Y] → Stretch: [Z]
- KR1 Owner: [Nome] | Check-in: [Cadência]
- KR2: [Metric] — Baseline: [X] → Target: [Y] → Stretch: [Z]

## Area OKRs
### [Area Name]
- O1: [Objective] — Owner: [C-Level]
  - KR1-KR3 com baselines e targets

## Milestones (13-Week View)
| Week | Milestone | Owner | OKR | Status |
|------|-----------|-------|-----|--------|
| W4   |           |       |     |        |
| W8   |           |       |     |        |
| W12  |           |       |     |        |

## Resource Allocation
| Area | Budget | Headcount | Key Hires |
|------|--------|-----------|-----------|

## Dependencies Map
[Diagrama de dependências entre áreas]

## Risks and Mitigations
| Risk | Probability | Impact | Mitigation | Owner |
|------|-------------|--------|------------|-------|

## Approval
- [ ] CEO | [ ] COO | [ ] CFO
- Date: [YYYY-MM-DD]
```

## Registries para Atualizar
- `registries/okrs.md` — Registrar todos os OKRs do trimestre
- `registries/resource-allocation.md` — Atualizar alocação de budget e headcount
- `registries/decisions-log.md` — Documentar trade-offs e decisões de priorização
- `registries/risk-register.md` — Adicionar riscos identificados no planning
- `registries/initiatives.md` — Atualizar lista de iniciativas ativas

## Critérios de Aceitação
1. Plano trimestral completo e aprovado pelo CEO
2. OKRs publicados e acessíveis a toda organização
3. Budget alocado e aprovado pelo CFO
4. Dependency map criado e validado por todos os owners
5. Kickoffs de área realizados nas primeiras 48h do trimestre
6. Check-ins recorrentes agendados para as 13 semanas
7. Early warning indicators configurados em dashboards

## Dependências e Handoffs
- **Recebe de:** QBR, Strategic Bets, Financial Close, Board Feedback
- **Entrega para:** Weekly Business Reviews, Initiative Teams, Budget Owners
- **Blocking:** Quarterly planning deve estar completo antes do início do trimestre
- **Cadência:** Executado 2 semanas antes do início de cada trimestre
- **Escalation path:** Conflitos não resolvidos em 24h são escalados para CEO
