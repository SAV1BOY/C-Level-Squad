# Run Quarterly Business Review (QBR)

## Objetivo
Executar a Quarterly Business Review, a sessão mais profunda e abrangente de review operacional. O QBR avalia o trimestre completo, faz scoring final de OKRs, analisa saúde das strategic bets, revisa resource allocation e prepara o terreno para o próximo quarterly planning cycle.

## Agente Responsável
- **COO Agent** — Facilitação e consolidação do review completo

## Agentes de Suporte
- **CEO Agent** — Avaliação estratégica e direcionamento
- **CFO Agent** — Financial review completo e forecast anual update
- **CTO Agent** — Technology review e capacity assessment
- **CPO Agent** — Product review e roadmap retrospective
- **CMO Agent** — Growth review e market position assessment
- **CHRO Agent** — People review, org health, talent pipeline
- **CIO Agent** — Systems review e data quality assessment
- **CAI Agent** — AI initiatives review

## Pré-requisitos
1. Financial close do trimestre completo
2. OKR scoring final de todas as áreas
3. Strategic bets performance data
4. MBR reports dos 3 meses do trimestre
5. Initiative health assessments
6. Customer satisfaction data trimestral
7. Employee engagement data (se disponível)
8. Competitive landscape update

## Processo (step-by-step)

### Fase 1: Data Compilation (Semana 1 pós-trimestre)
1. CFO completa o financial close trimestral
2. Cada área faz scoring final dos seus OKRs com evidência para cada score
3. Compilar performance de cada strategic bet: metrics vs targets
4. Consolidar customer metrics: NPS, CSAT, churn, expansion rate
5. Compilar engineering metrics: DORA metrics, incidents, tech debt
6. Consolidar people metrics: attrition, hiring velocity, engagement
7. Preparar competitive position update

### Fase 2: Individual Area Reviews (Semana 1-2)
8. Cada C-Level prepara sua quarterly retrospective (template padronizado)
9. Retrospective inclui: wins, misses, learnings, surprises, asks for next quarter
10. Cada área faz self-assessment honesto: o que faríamos diferente?
11. CFO prepara variance analysis detalhada (budget vs actual por linha)
12. COO prepara cross-functional dependency review: o que funcionou, o que falhou

### Fase 3: QBR Meeting (Half-day: 4-5 horas)
13. **[0-30 min]** CEO abre com context setting estratégico
14. **[30-75 min]** Financial deep dive: P&L, cash flow, unit economics, forecast
15. **[75-120 min]** OKR scoring review: scores, patterns, learnings
16. **[120-150 min]** Strategic bets review: cada bet avaliada com dados
17. **[150-195 min]** Area retrospectives: highlights de cada C-Level (15 min each)
18. **[195-240 min]** Cross-functional review: dependencies, collaboration, bottlenecks
19. **[240-270 min]** Forward look: priorities e themes para próximo trimestre
20. **[270-300 min]** Decisions, action items e closing

### Fase 4: Post-QBR (Semana seguinte)
21. Publicar QBR report completo com todas as métricas e decisões
22. Atualizar annual forecast com dados do trimestre
23. Alimentar o quarterly planning process do próximo trimestre
24. Comunicar key insights para a organização
25. Atualizar strategic bets status e kill criteria
26. Preparar board update se aplicável

## Frameworks a Aplicar
- **OKR Scoring (0.0-1.0)** — Scoring padronizado com calibração cross-area
- **Retrospective (4Ls)** — Liked, Learned, Lacked, Longed for
- **Unit Economics Deep Dive** — CAC, LTV, payback period, margins por segmento
- **Strategic Bet Scorecard** — Framework específico para avaliar bets
- **Dependency Post-Mortem** — Avaliar onde cross-functional dependencies falharam
- **Velocity vs Quality Trade-off** — Avaliar se estamos otimizando corretamente

## Checklists de Qualidade
- [ ] Financial close completo com auditoria do CFO
- [ ] OKR scores finais com evidência documentada
- [ ] Strategic bets avaliadas com dados de performance
- [ ] Retrospectives de todas as áreas completas
- [ ] Cross-functional dependency review feito
- [ ] Customer metrics trimestral compilados
- [ ] QBR meeting realizado com todos os C-Levels
- [ ] Decisions documentadas com owners
- [ ] Annual forecast atualizado
- [ ] QBR report publicado em até 1 semana
- [ ] Inputs para quarterly planning preparados
- [ ] Board update preparado se aplicável

## Template de Entrega
```markdown
# QBR Report — Q[X] [Year]

## Quarter Summary
[Executive summary em 5-7 bullet points]

## Financial Performance
| Metric | Q Target | Q Actual | Variance | YTD | Annual Forecast |
|--------|----------|----------|----------|-----|-----------------|

## OKR Final Scores
| Objective | Score | Status | Key Learning |
|-----------|-------|--------|-------------|
| Company O1 | [0.X] | | |

### OKR Score Distribution
- Average Score: [0.X]
- % Achieved (>0.7): [X%]
- % Missed (<0.3): [X%]

## Strategic Bets Review
| Bet | Status | Confidence | Key Metric | Decision |
|-----|--------|------------|------------|----------|

## Area Retrospectives
### [Area Name]
- **Wins:** [Top 3]
- **Misses:** [Top 3]
- **Learnings:** [Top 3]
- **Asks for Next Q:** [Top 3]

## Cross-Functional Assessment
| Dependency | Areas | Worked? | Learning |
|-----------|-------|---------|----------|

## Decisions Made
| Decision | Rationale | Owner | Impact |
|----------|-----------|-------|--------|

## Inputs for Next Quarter Planning
- **Priorities:** [Top 3-5]
- **Resource Shifts:** [Any changes]
- **New Initiatives:** [Proposed]
- **Kill Candidates:** [Proposed]
```

## Registries para Atualizar
- `registries/okrs.md` — Scores finais do trimestre
- `registries/strategic-bets.md` — Status atualizado de cada bet
- `registries/metrics-log.md` — Métricas trimestrais consolidadas
- `registries/decisions-log.md` — Decisões do QBR
- `registries/forecasts.md` — Forecast anual atualizado
- `registries/lessons-learned.md` — Learnings do trimestre

## Critérios de Aceitação
1. QBR realizado até 2 semanas após fim do trimestre
2. Todas as áreas com OKR scores finais e retrospectives
3. Financial close completo com variance analysis
4. Strategic bets avaliadas com decisões (continue/adjust/kill)
5. QBR report publicado em até 1 semana após o meeting
6. Inputs para quarterly planning documentados
7. Annual forecast atualizado

## Dependências e Handoffs
- **Recebe de:** Financial Close, OKR Scores, MBR Reports, Initiative Data
- **Entrega para:** Quarterly Planning, Board Prep, Annual Forecast, Strategic Bets Review
- **Cadência:** Trimestral, nas primeiras 2 semanas após fim do trimestre
- **Escalation path:** QBR findings que impactam strategy escalam para board
- **Integração:** QBR é o input principal para o próximo quarterly planning cycle
