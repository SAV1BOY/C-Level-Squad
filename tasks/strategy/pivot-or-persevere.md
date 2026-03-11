# Pivot or Persevere Decision

## Objetivo
Executar um processo estruturado de decisão para determinar se uma strategic bet, produto ou direção deve ser mantida (persevere), ajustada (pivot) ou abandonada (kill). Esta é uma das decisões mais difíceis de um executive team — requer coragem para mudar de direção e disciplina para não mudar por razões erradas.

## Agente Responsável
- **CEO Agent** — Decisão final sobre pivot vs persevere

## Agentes de Suporte
- **COO Agent** — Dados operacionais e execution assessment
- **CFO Agent** — Financial analysis, runway impact e sunk cost clarity
- **CTO Agent** — Technical feasibility de alternativas
- **CPO Agent** — Product-market fit signals e customer data
- **CMO Agent** — Market signals e demand validation
- **CHRO Agent** — Team morale e capability assessment

## Pré-requisitos
1. Dados de performance da iniciativa em avaliação (mínimo 2 ciclos de medição)
2. Kill criteria originais definidos no momento da bet (ver `tasks/strategy/define-vision-and-bets.md`)
3. Customer feedback qualitativo e quantitativo
4. Financial actuals vs. projections
5. Competitive landscape update
6. Team assessment: capability e morale da equipe executando
7. Market thesis atualizada

## Processo (step-by-step)

### Fase 1: Evidence Gathering (2-3 dias)
1. Compilar todos os dados de performance da iniciativa desde o início
2. Comparar actual vs. projected para cada métrica chave (revenue, adoption, engagement)
3. Analisar a trajectory: as métricas estão melhorando, estáveis ou piorando?
4. Documentar customer signals: willingness to pay, usage patterns, feedback qualitativo
5. Calcular burn rate e runway restante para a iniciativa
6. Entrevistar o team lead: visão honesta de dentro (sem sugar-coating)
7. Coletar external signals: mercado validando a thesis ou contradizendo?

### Fase 2: Structured Analysis (2-3 dias)
8. Revisitar os kill criteria originais: algum foi atingido?
9. Aplicar o framework "4 Signals" para decidir: product-market fit evidence, unit economics trajectory, market timing, team capability
10. Calcular o "continuation cost" — quanto custa continuar por mais 1 quarter
11. Calcular o "opportunity cost" — o que faríamos com esses recursos se liberados
12. Avaliar se o problema é de execução (fixável) ou de thesis (fundamental)
13. Mapear pivots possíveis: quais ajustes poderiam mudar a trajectory
14. Para cada pivot candidato, estimar: probability of success, cost, timeline

### Fase 3: Decision Framework (1-2 dias)
15. Apresentar o case para o executive team com dados completos
16. Executar o "clean slate test": se estivéssemos começando do zero hoje, investiríamos nisso?
17. Executar o "sunk cost audit": estamos continuando por razões válidas ou por apego ao investido?
18. Pedir a cada C-Level sua recommendation independente (antes da discussão coletiva)
19. Facilitar debate estruturado: argumentos a favor e contra cada opção
20. Tomar a decisão: persevere (com que ajustes?), pivot (para o quê?), ou kill

### Fase 4: Execution do Resultado (3-5 dias)
21. Se PERSEVERE: documentar condições para próxima revisão e melhorias a implementar
22. Se PIVOT: definir a nova direção, realocação de recursos e novo timeline
23. Se KILL: executar wind-down plan (comunicação, realocação de pessoas, customer migration)
24. Comunicar decisão transparentemente para toda a organização
25. Documentar learnings independente da decisão tomada
26. Atualizar strategic bets e resource allocation

## Frameworks a Aplicar
- **Clean Slate Test** — "Sabendo o que sabemos hoje, começaríamos isso?"
- **Sunk Cost Audit** — Separar investimento passado de decisão futura
- **4 Signals Framework** — PMF evidence, unit economics, timing, team
- **Real Options Theory** — Tratar a decisão como exercício de opção financeira
- **Type 1 vs Type 2 Decision (Bezos)** — One-way door vs two-way door
- **Disagree and Commit Protocol** — Mecanismo para decisão quando não há consenso
- **Pre-Mortem Reverso** — Se der certo, o que terá sido o fator decisivo?

## Checklists de Qualidade
- [ ] Dados de performance compilados com mínimo 2 ciclos de medição
- [ ] Kill criteria originais revisitados explicitamente
- [ ] Trajectory analysis documentada (improving, stable, declining)
- [ ] Customer signals coletados (qualitativo e quantitativo)
- [ ] Continuation cost vs opportunity cost calculados
- [ ] Execução vs thesis problem diagnosticado
- [ ] Clean slate test e sunk cost audit executados
- [ ] Cada C-Level deu recommendation independente
- [ ] Debate estruturado realizado com argumentos registrados
- [ ] Decisão documentada com rationale completo
- [ ] Plano de execução definido (persevere/pivot/kill)
- [ ] Comunicação preparada para organização
- [ ] Learnings documentados

## Template de Entrega
```markdown
# Pivot or Persevere — [Initiative Name]

## Initiative Summary
- **Start Date:** [When launched]
- **Original Thesis:** [Why we believed]
- **Investment to Date:** [R$ and headcount]
- **Kill Criteria (Original):** [What we said would trigger kill]

## Performance Data
| Metric | Projected | Actual | Trajectory |
|--------|-----------|--------|------------|
| [Revenue/Users/etc] | | | ↑↓→ |

## Signal Assessment
| Signal | Score (1-5) | Evidence |
|--------|-------------|----------|
| Product-Market Fit | | |
| Unit Economics | | |
| Market Timing | | |
| Team Capability | | |

## Key Questions
- **Clean Slate Test:** [Would we start this today? Why/why not?]
- **Sunk Cost Check:** [Are we continuing for right reasons?]
- **Execution vs Thesis:** [Is the problem fixable or fundamental?]

## Options Analysis
| Option | Cost | Probability of Success | Timeline | Upside |
|--------|------|----------------------|----------|--------|
| Persevere (as-is) | | | | |
| Persevere (adjusted) | | | | |
| Pivot to [X] | | | | |
| Kill | | | | |

## C-Level Recommendations
| Agent | Recommendation | Key Argument |
|-------|---------------|--------------|

## Decision
- **Decision:** [Persevere / Pivot / Kill]
- **Rationale:** [Why this decision]
- **Disagree and Commit:** [Who disagreed, documented]

## Execution Plan
[Next steps based on decision]

## Learnings
[What we learned regardless of decision]
```

## Registries para Atualizar
- `registries/strategic-bets.md` — Atualizar status da bet (continue/pivoted/killed)
- `registries/decisions-log.md` — Registrar decisão com rationale completo
- `registries/resource-allocation.md` — Refletir realocação de recursos
- `registries/lessons-learned.md` — Documentar learnings
- `registries/risk-register.md` — Atualizar riscos conforme decisão

## Critérios de Aceitação
1. Análise completa com dados de no mínimo 2 ciclos de medição
2. Todos os frameworks de decisão aplicados e documentados
3. Decisão tomada com rationale claro e transparente
4. Plano de execução definido com owners e timeline
5. Comunicação realizada para stakeholders relevantes
6. Learnings documentados independente da decisão
7. Registries atualizados

## Dependências e Handoffs
- **Recebe de:** Initiative Health Review, Scorecard Data, Customer Feedback
- **Entrega para:** Strategic Bets Update, Resource Allocation, Quarterly Planning
- **Cadência:** Triggered por kill criteria ou scheduled review (quarterly minimum)
- **Escalation path:** Se equipe não converge em 48h, CEO decide unilateralmente
- **Time-box:** Decisão deve ser tomada em no máximo 10 dias úteis após trigger
