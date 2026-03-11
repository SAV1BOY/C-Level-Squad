# Define Vision and Strategic Bets

## Objetivo
Definir ou atualizar a visão estratégica da empresa, identificar as apostas estratégicas prioritárias (strategic bets) e construir a kill list de iniciativas que devem ser descontinuadas para liberar recursos. Este processo garante alinhamento executivo sobre o futuro da organização e foco radical nas poucas coisas que realmente importam.

## Agente Responsável
- **CEO Agent** — Ownership final sobre visão e apostas estratégicas

## Agentes de Suporte
- **COO Agent** — Validação de capacidade operacional para executar as bets
- **CFO Agent** — Modelagem financeira e análise de investimento por bet
- **CTO Agent** — Viabilidade técnica e timeline de execução
- **CPO Agent** — Alinhamento com roadmap de produto
- **CMO Agent** — Validação de market fit e go-to-market viability
- **CHRO Agent** — Capacidade de talento para cada bet

## Pré-requisitos
1. Market thesis atualizada (ver `tasks/strategy/market-thesis-update.md`)
2. Dados financeiros do último trimestre consolidados
3. Análise competitiva recente (últimos 30 dias)
4. Input de clientes (NPS, churn analysis, feature requests)
5. Resultado do último moat review (ver `tasks/strategy/moat-review.md`)
6. Performance data das bets anteriores
7. Board feedback do último board meeting

## Processo (step-by-step)

### Fase 1: Diagnóstico do Estado Atual (2-3 dias)
1. Compilar performance das bets estratégicas vigentes usando o scorecard atual
2. Executar análise SWOT atualizada com dados quantitativos
3. Revisar market thesis e identificar mudanças materiais no mercado
4. Coletar input de cada C-Level sobre oportunidades e ameaças emergentes
5. Analisar portfolio atual de iniciativas com ROI realizado vs. projetado

### Fase 2: Definição de Visão (1-2 dias)
6. Articular a North Star da empresa para os próximos 3-5 anos
7. Definir o "winning aspiration" — qual é o estado de vitória
8. Validar se a visão atual ainda é relevante ou precisa de atualização
9. Documentar a narrativa estratégica: de onde viemos, onde estamos, para onde vamos
10. Criar o vision statement refinado com métricas de sucesso de longo prazo

### Fase 3: Identificação de Strategic Bets (2-3 dias)
11. Brainstorm de possíveis bets usando framework "Where to Play / How to Win"
12. Para cada bet candidata, documentar: thesis, TAM, right to win, investment needed
13. Aplicar filtros de priorização: strategic fit, financial return, feasibility, timing
14. Limitar a 3-5 bets máximas (foco radical)
15. Para cada bet selecionada, definir: owner, success metrics, kill criteria, timeline
16. Modelar cenários financeiros (bull/base/bear) para cada bet

### Fase 4: Construção da Kill List (1-2 dias)
17. Listar todas as iniciativas ativas que NÃO se alinham às bets selecionadas
18. Para cada candidata à kill list: calcular sunk cost, switching cost, opportunity cost
19. Identificar dependências e impactos de descontinuar cada iniciativa
20. Definir plano de wind-down para cada item na kill list (timeline, comunicação, realocação)
21. Calcular recursos liberados (budget, headcount, attention) pela kill list

### Fase 5: Validação e Alignment (1-2 dias)
22. Apresentar bets e kill list para o executive team em sessão de trabalho
23. Executar pre-mortem para cada bet: "se falhar, qual será a razão?"
24. Documentar disagreements e decisões tomadas (disagree and commit log)
25. Finalizar o Strategic Bets Document com sign-off de todos os C-Levels

## Frameworks a Aplicar
- **Playing to Win (Lafley/Martin)** — Where to Play + How to Win para cada bet
- **Conviction-Effort Matrix** — Plotar bets por nível de convicção vs. esforço necessário
- **Pre-Mortem Analysis** — Identificar modos de falha antes de commitar
- **Opportunity Cost Framework** — Garantir que cada bet vale mais que a segunda melhor alternativa
- **Kill Criteria Framework** — Definir antecipadamente quando uma bet deve ser abandonada
- **MECE Principle** — Garantir que as bets cobrem o espaço estratégico sem overlap

## Checklists de Qualidade
- [ ] Visão é clara, inspiradora e mensurável
- [ ] Máximo de 5 strategic bets definidas
- [ ] Cada bet tem owner, metrics, timeline e kill criteria
- [ ] Kill list documentada com plano de wind-down
- [ ] Modelagem financeira completa (bull/base/bear) para cada bet
- [ ] Pre-mortem executado para cada bet
- [ ] Todos os C-Levels fizeram sign-off (ou disagree-and-commit documentado)
- [ ] Recursos liberados pela kill list quantificados
- [ ] Narrativa estratégica coerente e comunicável
- [ ] Dependências entre bets mapeadas
- [ ] Impacto em headcount e budget modelado
- [ ] Timeline de execução realista validado pelo COO

## Template de Entrega
```markdown
# Strategic Bets Document — [Quarter/Year]

## Vision Statement
[North Star de 3-5 anos com métricas de sucesso]

## Strategic Narrative
[De onde viemos → Onde estamos → Para onde vamos]

## Strategic Bets

### Bet #1: [Nome]
- **Thesis:** [Por que acreditamos nisso]
- **Owner:** [C-Level responsável]
- **TAM:** [Total Addressable Market]
- **Investment:** [Budget + headcount necessário]
- **Success Metrics:** [KPIs com targets]
- **Kill Criteria:** [Quando abandonar]
- **Timeline:** [Milestones com datas]
- **Scenarios:** Bull: [X] | Base: [Y] | Bear: [Z]

### Bet #2-5: [Repetir estrutura]

## Kill List
| Iniciativa | Razão | Recursos Liberados | Wind-down Date | Owner |
|---|---|---|---|---|

## Disagree and Commit Log
| Decisão | Quem discordou | Razão | Status |
|---|---|---|---|

## Sign-off
- [ ] CEO | [ ] COO | [ ] CFO | [ ] CTO | [ ] CPO | [ ] CMO | [ ] CHRO
```

## Registries para Atualizar
- `registries/strategic-bets.md` — Atualizar com novas bets e kill list
- `registries/decisions-log.md` — Registrar decisões estratégicas tomadas
- `registries/okrs.md` — Alinhar OKRs com novas bets
- `registries/resource-allocation.md` — Refletir realocação de recursos
- `registries/risk-register.md` — Adicionar riscos associados a cada bet

## Critérios de Aceitação
1. Documento de Strategic Bets completo e aprovado por todos os C-Levels
2. Máximo de 5 bets com modelagem financeira detalhada
3. Kill list com plano de wind-down e timeline definido
4. Recursos liberados quantificados e realocados
5. Comunicação preparada para toda a organização
6. OKRs atualizados para refletir as novas bets
7. Próximos check-ins agendados (30/60/90 dias)

## Dependências e Handoffs
- **Recebe de:** Market Thesis Update, Moat Review, Board Feedback
- **Entrega para:** Quarterly Planning, OKR Setting, Resource Allocation
- **Blocking:** Nenhuma iniciativa nova deve ser aprovada até que as bets estejam definidas
- **Cadência de revisão:** Bets revisadas trimestralmente, visão revisada anualmente
- **Escalation path:** Se não houver consenso em 48h, CEO decide unilateralmente e documenta
