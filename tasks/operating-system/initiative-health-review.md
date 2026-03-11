# Initiative Health Review

## Objetivo
Avaliar sistematicamente a saúde de todas as iniciativas ativas, identificando quais estão on track, quais precisam de intervenção e quais são candidatas a kill. Uma iniciativa sem health review regular é uma iniciativa que pode falhar silenciosamente, consumindo recursos sem gerar resultado.

## Agente Responsável
- **COO Agent** — Consolidação e facilitação do review

## Agentes de Suporte
- **CEO Agent** — Decisões sobre iniciativas estratégicas
- **CFO Agent** — Financial health e burn rate de cada iniciativa
- **CTO Agent** — Technical health e engineering velocity
- **CPO Agent** — Product health e adoption metrics
- **CMO Agent** — Growth initiatives health
- **CHRO Agent** — Team health e resource availability

## Pré-requisitos
1. Lista atualizada de todas as iniciativas ativas com owners
2. Métricas de performance definidas para cada iniciativa
3. Original business case ou thesis de cada iniciativa
4. Resource allocation atual (budget e headcount por iniciativa)
5. Timeline original vs progress atual
6. Dados de dependências entre iniciativas

## Processo (step-by-step)

### Fase 1: Data Collection (2-3 dias)
1. Para cada iniciativa ativa, coletar: metrics actuals, timeline progress, budget consumed
2. Cada initiative owner preenche o health assessment padronizado
3. Identificar iniciativas sem dados atualizados (red flag imediato)
4. Compilar dependency status: iniciativas que dependem de outras
5. Calcular velocity trend para cada iniciativa (acelerando ou desacelerando)

### Fase 2: Health Scoring (1-2 dias)
6. Aplicar o health scoring framework a cada iniciativa:
   - **Scope Health:** Escopo mudou? Está crescendo descontroladamente?
   - **Timeline Health:** On track vs original timeline? Quanto atraso?
   - **Budget Health:** Dentro do budget? Burn rate sustentável?
   - **Quality Health:** Entregas atendem padrão de qualidade?
   - **Team Health:** Equipe motivada e capaz? Turnover?
   - **Impact Health:** Métricas de impacto movendo na direção certa?
7. Classificar cada iniciativa como: Green (on track), Yellow (at risk), Red (off track)
8. Para iniciativas Yellow e Red, documentar root cause específico
9. Comparar health trend: melhorando, estável ou piorando

### Fase 3: Review Meeting (60-90 minutos)
10. Apresentar portfolio overview: quantas Green, Yellow, Red
11. Skip Green initiatives — só discutir se alguém questionar
12. Para cada Yellow: diagnóstico, plano de recovery, decisão (continue/adjust)
13. Para cada Red: diagnóstico, opções (recover/pivot/kill), decisão com deadline
14. Avaliar portfolio balance: não ter muitas iniciativas simultâneas
15. Identificar resource conflicts entre iniciativas

### Fase 4: Actions e Follow-up
16. Documentar decisões para cada iniciativa Yellow e Red
17. Atribuir recovery owners e deadlines para iniciativas em risco
18. Para iniciativas marcadas para kill, trigger o processo de kill-or-continue
19. Atualizar o initiative portfolio no registry
20. Comunicar decisões para initiative owners e teams

## Frameworks a Aplicar
- **Initiative Health Scorecard** — 6 dimensões: scope, timeline, budget, quality, team, impact
- **Traffic Light Classification** — Green/Yellow/Red com critérios objetivos
- **Portfolio Balance Check** — Garantir mix adequado de horizons e risk levels
- **Velocity Trend Analysis** — Analisar se a iniciativa está acelerando ou desacelerando
- **Resource Utilization Matrix** — Mapear alocação real vs planejada
- **Kill Criteria Check** — Verificar se kill criteria foram atingidos

## Checklists de Qualidade
- [ ] Todas as iniciativas ativas incluídas no review
- [ ] Health data atualizado para cada iniciativa (max 1 semana de lag)
- [ ] Scoring aplicado consistentemente usando os mesmos critérios
- [ ] Iniciativas sem dados atualizados flagged como red imediatamente
- [ ] Root cause documentado para cada Yellow e Red
- [ ] Decisões claras para cada iniciativa em risco
- [ ] Recovery plans com owners e deadlines definidos
- [ ] Portfolio balance avaliado (não overcommitted)
- [ ] Resource conflicts identificados e resolvidos
- [ ] Resultados comunicados para initiative owners

## Template de Entrega
```markdown
# Initiative Health Review — [Date]

## Portfolio Overview
- **Total Initiatives:** [X]
- **Green:** [X] ([%])
- **Yellow:** [X] ([%])
- **Red:** [X] ([%])
- **Total Investment:** [R$ X]
- **Total Headcount Allocated:** [X]

## Portfolio Health Trend
| Month | Green | Yellow | Red |
|-------|-------|--------|-----|

## Initiative Detail
### [Initiative Name]
- **Owner:** [Name]
- **Strategic Bet:** [Which bet it supports]
- **Status:** [Green/Yellow/Red]
- **Health Scores:**
  - Scope: [1-5] | Timeline: [1-5] | Budget: [1-5]
  - Quality: [1-5] | Team: [1-5] | Impact: [1-5]
- **Budget:** [Spent / Total] ([%])
- **Timeline:** [Original End] → [Current Forecast]
- **Key Metric:** [Target vs Actual]
- **Issue (if Yellow/Red):** [Root cause]
- **Decision:** [Continue/Adjust/Kill]
- **Action:** [Next steps with owner and deadline]

## Decisions Made
| Initiative | Decision | Rationale | Owner | Deadline |
|-----------|----------|-----------|-------|----------|

## Resource Conflicts
| Conflict | Initiatives Affected | Resolution |
|----------|---------------------|------------|

## Kill Candidates
| Initiative | Reason | Next Step |
|-----------|--------|-----------|
```

## Registries para Atualizar
- `registries/initiatives.md` — Status atualizado de cada iniciativa
- `registries/resource-allocation.md` — Ajustes de recurso decididos
- `registries/decisions-log.md` — Decisões de continue/adjust/kill
- `registries/risk-register.md` — Riscos de iniciativas em Yellow/Red

## Critérios de Aceitação
1. 100% das iniciativas ativas avaliadas
2. Health scoring consistente e baseado em dados
3. Decisões documentadas para todas as iniciativas Yellow e Red
4. Recovery plans com owners e deadlines para iniciativas em risco
5. Portfolio balance validado (não overcommitted)
6. Resultados comunicados em até 48h

## Dependências e Handoffs
- **Recebe de:** Initiative Owners, Financial Data, OKR Progress, WBR Metrics
- **Entrega para:** Kill or Continue Review, Quarterly Planning, Resource Allocation
- **Cadência:** Bi-weekly (a cada 2 semanas)
- **Escalation path:** Iniciativas Red sem recovery plan em 1 semana escalam para CEO
- **Integração:** Alimenta o MBR e QBR com initiative health data
