# Workflow 07: Annual Planning Cycle — Planejamento Anual Completo

## Objetivo

Executar o ciclo completo de planejamento anual: revisão da estratégia vigente,
cenários de futuro, seleção de bets para o ano, alocação de budget, definição
de OKRs anuais, criação de roadmaps e cascata de comunicação para toda a
organização. Este é o processo mais abrangente do C-Level Squad — onde
direção se traduz em compromisso.

> **Princípio**: Planejar não é prever o futuro. É decidir, com as melhores
> evidências disponíveis, onde concentrar recursos e atenção por 12 meses.

---

## Agentes Envolvidos

| Agente | Papel | Contribuição Principal |
|--------|-------|----------------------|
| **Vision Chief (CEO)** | Líder do processo | Tese, bets, visão de longo prazo, decisões finais |
| **COO Orchestrator** | Coordenador de execução | Timeline, dependencies, operating model |
| **CMO Architect** | Estratégia de growth | Market sizing, GTM plan, revenue targets |
| **CTO Architect** | Estratégia de tech | Platform roadmap, tech investments, capacity |
| **CIO Engineer** | Estratégia de IT/dados | Systems roadmap, data strategy, integrations |
| **CAIO Architect** | Estratégia de IA | AI portfolio, build vs buy AI, governance |
| **CFO Strategist** | Estratégia financeira | Budget, unit economics, scenarios financeiros |
| **Squad Coordinator** | Facilitador | Logística, documentação, comunicação |

---

## Trigger (quando iniciar)

- **Cadência**: Outubro-Novembro (para ano fiscal = ano civil)
- **Duração total**: 6-8 semanas de processo
- **Preparação**: Inicia com o QBR do Q3
- **Quem dispara**: Vision Chief + COO Orchestrator

---

## Pré-condições

- [ ] QBR do Q3 concluído com OKR scoring
- [ ] Resultados acumulados do ano disponíveis (9 meses)
- [ ] Análise competitiva atualizada
- [ ] Market research recente (últimos 3 meses)
- [ ] Financial close dos 3 primeiros trimestres
- [ ] Team health survey realizado
- [ ] Feedback do board (se aplicável)
- [ ] Macro trends e market outlook disponíveis

---

## Processo (step-by-step com decision points)

### FASE 1: Strategy Review (Semana 1-2)

**Step 1.1 — Retrospectiva do Ano Corrente**

- DRI: COO Orchestrator
- Framework: `frameworks/operating-system/wbr-mbr-qbr.md`
- Processo:
  1. Compilar resultados do ano:
     - OKR scores dos 3 trimestres (+ projeção Q4)
     - Revenue: actual vs plan, growth trajectory
     - Key wins e key misses
     - Bets: quais funcionaram, quais foram mortos
     - Kill list: o que matamos e aprendemos
  2. Cada C-Level prepara retrospectiva da sua área
  3. Consolidar em documento único: "Year in Review"
- Output: Year in Review document

**Step 1.2 — Tese Estratégica Deep Review**

- DRI: Vision Chief
- Framework: `frameworks/vision-chief/vision-chief-strategic-thesis.md`
- Framework: `frameworks/vision-strategy/strategy-choice-cascade.md`
- Processo:
  1. Reler tese vigente: ainda válida?
  2. O que mudou no mercado que impacta a tese?
  3. O que aprendemos no ano que invalida premissas?
  4. Onde estamos certos e dobramos a aposta?
  5. Onde erramos e precisamos ajustar?
- **Decision Point**: Tese precisa de revisão fundamental?
  - **SIM** → Dedicar 1 semana para redefinição de tese
  - **NÃO** → Iterar e refinar, manter core

**Step 1.3 — Competitive & Market Analysis**

- DRI: CMO Architect + Vision Chief
- Framework: `frameworks/vision-strategy/wardley-mapping.md`
- Framework: `frameworks/vision-strategy/scenario-planning.md`
- Processo:
  1. Atualizar mapa competitivo:
     - Novos entrantes
     - Movimentos de concorrentes
     - Mudanças regulatórias
     - Tendências tecnológicas
  2. Market sizing atualizado: TAM/SAM/SOM
  3. ICP (Ideal Customer Profile) review
  4. Identificar oportunidades e ameaças
- Checklist: `checklists/strategy/market-thesis-quality.md`
- Output: Market & Competitive Report

**Step 1.4 — Moat Assessment**

- DRI: Vision Chief
- Framework: `frameworks/reference-intellectual/collins-flywheel-effect.md`
- Checklist: `checklists/strategy/competitive-moat-quality.md`
- Processo:
  1. Avaliar força do moat em cada dimensão:
     - Network effects
     - Switching costs
     - Scale economies
     - Brand
     - Data advantage
     - Technology/IP
  2. Score de 1-10 em cada dimensão
  3. Comparar com ano anterior: fortaleceu ou enfraqueceu?
  4. Definir ações para fortalecer moat no próximo ano
- Output: Moat Scorecard

### FASE 2: Scenario Planning (Semana 3)

**Step 2.1 — Cenários Estratégicos**

- DRI: Vision Chief + CFO Strategist
- Framework: `frameworks/vision-strategy/scenario-planning.md`
- Processo:
  1. Definir 3 cenários para o próximo ano:
     - **Bull Case** (otimista): O que acontece se tudo der certo?
     - **Base Case** (realista): Projeção baseada em tendência atual
     - **Bear Case** (pessimista): O que acontece se o mercado piora?
  2. Para cada cenário, projetar:
     - Revenue e growth rate
     - Headcount e burn rate
     - Market position
     - Investimentos necessários
  3. Identificar "no-regret moves": ações boas em qualquer cenário
  4. Identificar "conditional bets": ações boas só em cenário específico
- Output: Scenario Planning Document

**Step 2.2 — Financial Modeling**

- DRI: CFO Strategist
- Processo:
  1. Modelar financeiro para cada cenário:
     - P&L projetada (12 meses)
     - Cash flow projection
     - Budget allocation por área
     - Headcount plan
     - Investment cases
  2. Calcular unit economics projetados:
     - CAC target
     - LTV target
     - Payback period
     - Burn multiple
  3. Definir budget envelope por cenário
- **Decision Point**: Qual cenário adotar como base para planning?
  - Recomendação: Base Case com "triggers" para ajustar para Bull/Bear
  - Vision Chief + CFO decidem

**Step 2.3 — Risk Scenario Analysis**

- DRI: COO Orchestrator
- Processo:
  1. Top 10 riscos para o próximo ano:
     - Probabilidade x Impacto
     - Mitigação planejada
     - Owner do risco
  2. "Pre-mortem": imaginar que o plano falhou — por quê?
  3. Incorporar mitigações no plano anual
- Registro: `data/registries/risk-registry.yaml`

### FASE 3: Bet Selection & Prioritization (Semana 4)

**Step 3.1 — Bet Brainstorm**

- DRI: Vision Chief
- Participantes: Todos C-Level
- Duração: 3-4 horas (workshop)
- Processo:
  1. Individual: cada C-Level propõe 3-5 bets potenciais
  2. Apresentação: each propõe seus bets (5 min cada)
  3. Agrupamento: consolidar bets similares
  4. Long list: ~15-20 bets potenciais
- Framework: `frameworks/vision-chief/vision-chief-bet-sizing.md`

**Step 3.2 — Bet Evaluation**

- DRI: Vision Chief + COO Orchestrator
- Checklist: `checklists/vision/strategic-bets-selection.md`
- Processo:
  1. Para cada bet, avaliar:
     - Alinhamento com tese (1-10)
     - Impacto potencial no NSM (1-10)
     - Capacidade de execução (1-10)
     - Investment required (R$)
     - Time to value (meses)
     - Risco de execução (alto/médio/baixo)
     - Kill criteria (o que define fracasso)
  2. Stack rank pela pontuação
  3. Aplicar filtro de recursos: o que cabe no budget?
  4. Selecionar top 3-5 bets para o ano
- **Decision Point**: Os bets estão balanceados nos Three Horizons?
  - **SIM** → Avançar para Step 3.3
  - **NÃO** → Rebalancear (70% H1, 20% H2, 10% H3)

**Step 3.3 — Bet Commitment**

- DRI: Vision Chief
- Processo:
  1. Para cada bet selecionado, formalizar:
     - Owner (DRI do C-Level)
     - Budget alocado
     - Headcount alocado
     - Timeline (anual ou semestral)
     - Kill criteria (trimestral check)
     - Primeiro milestone (Q1)
  2. Kill list: o que NÃO faremos este ano
  3. Aprovação formal do Vision Chief
- Template: `templates/strategy/annual-operating-plan.md`
- Registro: `data/registries/initiative-registry.yaml`

### FASE 4: OKR & Budget Definition (Semana 5-6)

**Step 4.1 — Annual OKRs**

- DRI: Vision Chief + COO Orchestrator
- Framework: `frameworks/operating-system/okrs.md`
- Framework: `frameworks/vision-strategy/ogsm.md`
- Processo:
  1. Definir OGSM anual (Objective, Goals, Strategies, Measures)
  2. Derivar 3-5 Annual Objectives de empresa
  3. Para cada Objective, definir Annual KRs
  4. Cada C-Level define Annual OKRs da área
  5. Validar cascata e alinhamento
- Checklist: `checklists/annual-planning-quality.md`
- **Nota**: OKRs trimestrais serão derivados no Workflow 01 a cada Q

**Step 4.2 — Budget Allocation**

- DRI: CFO Strategist + Vision Chief
- Processo:
  1. Alocar budget por área:
     - Growth (CMO): X%
     - Tech (CTO): Y%
     - IT/Data (CIO): Z%
     - AI (CAIO): W%
     - Operations (COO): V%
     - People/Hiring: U%
     - Reserve: T%
  2. Para cada bet, confirmar budget dedicado
  3. Definir "free budget" para oportunidades emergentes (5-10%)
  4. Definir triggers de realocação (quando rebalancear)
- Checklist: `checklists/capital-allocation-quality.md`
- Registro: `data/registries/decision-registry.yaml`

**Step 4.3 — Headcount Planning**

- DRI: COO Orchestrator + Vision Chief
- Processo:
  1. Headcount atual vs necessário por área
  2. Contratações planejadas (timeline e prioridade)
  3. Gaps de competência e plano de desenvolvimento
  4. Succession planning review
- Registro: `data/registries/hiring-registry.yaml`

### FASE 5: Roadmap Creation (Semana 6-7)

**Step 5.1 — Roadmaps por Área**

- DRI: Cada C-Level
- Processo: Executar `workflows/02-bets-to-roadmaps.md` para cada bet
- Foco: Roadmap anual com milestones trimestrais
- Output: 1 roadmap por bet/área

**Step 5.2 — Integrated Roadmap**

- DRI: COO Orchestrator
- Processo:
  1. Consolidar roadmaps de todas as áreas em visão integrada
  2. Identificar e resolver conflitos de timeline/resources
  3. Mapear dependências cross-area
  4. Definir caminho crítico anual
  5. Vision Chief aprova roadmap integrado
- Output: Integrated Annual Roadmap

### FASE 6: Communication Cascade (Semana 7-8)

**Step 6.1 — Board Presentation**

- DRI: Vision Chief
- Processo:
  1. Apresentar plano anual para board/advisors
  2. Coletar feedback e ajustar se necessário
  3. Obter aprovação formal
- Template: `templates/operating-system/board-prep-pack.md`

**Step 6.2 — All-Hands Communication**

- DRI: Vision Chief + COO Orchestrator
- Processo:
  1. Preparar apresentação all-hands:
     - Retrospectiva do ano
     - Visão para o próximo ano
     - Bets e prioridades
     - OKRs de empresa
     - O que NÃO faremos (kill list)
  2. Apresentar para toda a organização
  3. Q&A aberto
  4. Publicar documento escrito
- Framework: `frameworks/vision-chief/vision-chief-narrative-cascade.md`

**Step 6.3 — Squad-level Cascade**

- DRI: Cada C-Level
- Processo:
  1. Cada C-Level comunica para seus squads:
     - OKRs da área
     - Roadmap
     - Expectativas
     - Resources disponíveis
  2. Squads têm 2 semanas para definir OKRs derivados
  3. C-Level valida OKRs dos squads
- SLA: 2 semanas para cascade completa

---

## Quality Gates

### Gate 1: Qualidade da Análise Estratégica

Aplicar `checklists/strategy-memo-quality.md`:
- [ ] Retrospectiva do ano baseada em dados, não memória
- [ ] Tese estratégica revisada com evidências novas
- [ ] Análise competitiva atualizada
- [ ] Scenario planning com 3 cenários modelados
- [ ] Riscos top 10 identificados com mitigação

### Gate 2: Qualidade dos Bets

Aplicar `checklists/vision/strategic-bets-selection.md`:
- [ ] 3-5 bets selecionados com rigor
- [ ] Kill criteria definidos antes de iniciar
- [ ] Budget e headcount alocados
- [ ] Three Horizons balanceados
- [ ] Kill list clara: o que NÃO faremos

### Gate 3: Qualidade Financeira

Aplicar `checklists/capital-allocation-quality.md`:
- [ ] Budget modelado para 3 cenários
- [ ] Unit economics projetados são sustentáveis
- [ ] Reserve strategy definida (5-10%)
- [ ] Headcount plan realista e priorizado
- [ ] CFO sign-off formal

### Gate 4: Qualidade da Comunicação

- [ ] Board presentation aprovada
- [ ] All-hands realizado
- [ ] Documento escrito publicado
- [ ] Squads receberam cascade
- [ ] OKRs derivados dos squads coletados

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| Year in Review | Markdown | `data/memos/` | COO |
| Updated Strategic Thesis | Markdown | `data/memos/` | Vision Chief |
| Scenario Planning Document | Markdown | `data/memos/` | Vision Chief + CFO |
| Annual Bet Cards | YAML | `data/registries/initiative-registry.yaml` | Vision Chief |
| Annual OKRs | YAML | `data/registries/okr-registry.yaml` | Vision Chief |
| Annual Budget | YAML | `data/registries/decision-registry.yaml` | CFO |
| Integrated Annual Roadmap | Markdown | `data/memos/` | COO |
| Board Presentation | Markdown | `data/memos/` | Vision Chief |
| All-Hands Deck | Markdown | `data/memos/` | Vision Chief |
| Annual Operating Plan | Markdown | `templates/strategy/annual-operating-plan.md` | Vision Chief |

---

## Registries Atualizados

- `data/registries/decision-registry.yaml` — Decisões estratégicas do ano
- `data/registries/initiative-registry.yaml` — Bets e iniciativas anuais
- `data/registries/okr-registry.yaml` — OKRs anuais
- `data/registries/metric-registry.yaml` — Targets anuais
- `data/registries/risk-registry.yaml` — Riscos do ano
- `data/registries/hiring-registry.yaml` — Headcount plan

---

## Próximos Passos

1. **Imediato**: Kick-off Q1 → `workflows/01-vision-to-okrs.md`
2. **Q1**: Primeiro QBR do ano → `workflows/06-qbr-loop.md`
3. **Contínuo**: WBRs e MBRs mantêm cadência
4. **Mid-year (Q2)**: Strategy checkpoint — tese ainda válida?
5. **Q3**: Iniciar preparação para próximo annual planning

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| Vision Chief | Board/Advisory | Annual plan para aprovação | Semana 7 |
| Vision Chief | Toda organização | All-hands + documento | Semana 8 |
| Cada C-Level | Squads respectivos | OKRs + roadmaps de área | 2 semanas pós all-hands |
| CFO | Cada C-Level | Budget confirmado | 1 semana pós aprovação |
| COO | Data Squad | Novas métricas anuais | 1 semana pós aprovação |
| CMO | Traffic/Brand/Copy/Story | GTM plan anual | 2 semanas pós all-hands |
| CTO | Design Squad | Product roadmap anual | 2 semanas pós all-hands |
| COO | Cybersecurity | Annual compliance requirements | 2 semanas |
