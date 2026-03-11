# Moat Review

## Objetivo
Avaliar a força e durabilidade do moat competitivo da empresa, identificando áreas de erosão e oportunidades de fortalecimento. O moat é o que impede competidores de replicar nossa posição — sem um moat forte, qualquer vantagem é temporária.

## Agente Responsável
- **CEO Agent** — Ownership da avaliação estratégica do moat

## Agentes de Suporte
- **CTO Agent** — Technology moat e propriedade intelectual
- **CPO Agent** — Product moat, switching costs e network effects
- **CMO Agent** — Brand moat e market positioning
- **CFO Agent** — Cost advantages e economies of scale
- **COO Agent** — Operational excellence como moat
- **CAI Agent** — Data moat e AI capabilities como diferencial

## Pré-requisitos
1. Market thesis atualizada (ver `tasks/strategy/market-thesis-update.md`)
2. Competitive analysis recente
3. Customer retention e churn data
4. Product usage data e feature adoption metrics
5. Technology stack assessment
6. Brand perception data (awareness, preference, loyalty)
7. Financial benchmarks do setor

## Processo (step-by-step)

### Fase 1: Moat Inventory (2-3 dias)
1. Listar todos os potenciais moats da empresa usando o framework dos 7 tipos
2. Para cada moat candidato, documentar: descrição, evidência, força atual (1-10)
3. Coletar dados quantitativos que suportam cada moat: retention rates, pricing power, market share
4. Identificar moats que competidores estão tentando replicar ou erosionar
5. Mapear quais moats são defensáveis no curto prazo (1-2 anos) vs longo prazo (5+ anos)

### Fase 2: Strength Assessment (2-3 dias)
6. Para cada moat, avaliar: largura (quão difícil de cruzar), profundidade (quanto custa tentar) e durabilidade (quanto tempo dura)
7. Executar competitive benchmarking: nosso moat vs competidores diretos
8. Analisar tendências: o moat está ficando mais forte ou mais fraco nos últimos 12 meses
9. Identificar external forces que podem erosionar o moat (technology shifts, regulation, market changes)
10. Calcular o "cost to replicate" para cada moat — quanto custaria a um competidor replicar
11. Avaliar composability: moats que se reforçam mutuamente (flywheel effect)

### Fase 3: Vulnerability Analysis (1-2 dias)
12. Para cada moat, listar os top 3 scenarios de erosão
13. Avaliar probabilidade e timeline de cada scenario de erosão
14. Identificar early warning signals de erosão para cada moat
15. Mapear investimentos necessários para manter cada moat no nível atual
16. Calcular o "moat maintenance cost" — quanto investimos para preservar cada vantagem

### Fase 4: Strengthening Plan (1-2 dias)
17. Priorizar oportunidades de fortalecimento por impacto e viabilidade
18. Definir iniciativas específicas para fortalecer os moats mais críticos
19. Estimar investimento e timeline para cada iniciativa
20. Identificar novos moats potenciais que podemos construir
21. Documentar recomendações para o strategic bets process

## Frameworks a Aplicar
- **7 Powers (Helmer)** — Scale economies, network effects, counter-positioning, switching costs, branding, cornered resource, process power
- **Moat Width/Depth/Durability** — Avaliação tridimensional de cada moat
- **Flywheel Analysis** — Mapear como moats se reforçam mutuamente
- **Erosion Scenario Planning** — Modelar como cada moat pode ser atacado
- **Cost-to-Replicate Analysis** — Quantificar barreira de entrada para cada vantagem
- **Buffett Moat Framework** — Intangible assets, switching costs, network effect, cost advantages

## Checklists de Qualidade
- [ ] Todos os 7 Powers avaliados para a empresa
- [ ] Cada moat tem score de força (1-10) com evidência
- [ ] Trends de 12 meses documentados (fortalecendo vs enfraquecendo)
- [ ] Top 3 erosion scenarios para cada moat principal
- [ ] Early warning signals definidos e monitoráveis
- [ ] Cost-to-replicate estimado para cada moat
- [ ] Flywheel connections mapeadas entre moats
- [ ] Plano de fortalecimento com ações priorizadas
- [ ] Investment needed quantificado
- [ ] Comparação com competidores documentada

## Template de Entrega
```markdown
# Moat Review — [Date]

## Moat Portfolio Summary
| Moat Type | Present? | Strength (1-10) | Trend | Durability |
|-----------|----------|-----------------|-------|------------|
| Scale Economies | | | ↑↓→ | |
| Network Effects | | | ↑↓→ | |
| Counter-positioning | | | ↑↓→ | |
| Switching Costs | | | ↑↓→ | |
| Branding | | | ↑↓→ | |
| Cornered Resource | | | ↑↓→ | |
| Process Power | | | ↑↓→ | |

## Deep Dive per Moat
### [Moat Name]
- **Description:** [O que é e como funciona]
- **Evidence:** [Dados quantitativos]
- **Cost to Replicate:** [R$ / time estimate]
- **Erosion Risks:** [Top 3 scenarios]
- **Warning Signals:** [Leading indicators]
- **Strengthening Actions:** [Recommendations]

## Flywheel Map
[Diagrama mostrando como moats se reforçam]

## Competitive Comparison
| Moat | Us | Competitor A | Competitor B |
|------|-----|-------------|-------------|

## Vulnerability Assessment
| Moat | Erosion Scenario | Probability | Timeline | Mitigation |
|------|-----------------|-------------|----------|------------|

## Strengthening Roadmap
| Initiative | Moat Impacted | Investment | Timeline | Expected Impact |
|-----------|---------------|------------|----------|-----------------|

## Overall Moat Score: [X/10]
- Trend: [Strengthening / Stable / Weakening]
```

## Registries para Atualizar
- `registries/competitive-intelligence.md` — Atualizar com dados comparativos de moat
- `registries/strategic-bets.md` — Conectar bets ao fortalecimento de moats
- `registries/risk-register.md` — Adicionar riscos de erosão de moat
- `registries/decisions-log.md` — Registrar decisões de investimento em moats

## Critérios de Aceitação
1. Todos os 7 Powers avaliados com scores e evidências
2. Erosion scenarios documentados para cada moat principal
3. Early warning signals definidos e atribuídos a owners
4. Plano de fortalecimento com ações priorizadas e budgeted
5. Comparação competitiva completa
6. Overall moat score calculado com trend direction
7. Apresentação para C-Level team realizada

## Dependências e Handoffs
- **Recebe de:** Market Thesis, Competitive Intelligence, Product Analytics, Brand Data
- **Entrega para:** Strategic Bets, Annual Planning, Board Prep
- **Cadência:** Semestralmente (ou ad-hoc se trigger de erosão detectado)
- **Escalation path:** Moat score abaixo de 5/10 ou trend de queda escala para board
