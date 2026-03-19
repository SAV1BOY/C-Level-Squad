# Workflow 09: Org Design — Redesenho Organizacional Estruturado

## Objetivo

Conduzir o processo completo de redesenho organizacional: avaliar estado atual,
definir o target operating model, analisar gaps, planejar a transição,
comunicar as mudanças e gerenciar o change management. Este workflow garante
que mudanças organizacionais são intencionais, baseadas em dados e executadas
com empatia e disciplina.

> **Princípio**: Estrutura segue estratégia. Se a estratégia mudou e a
> estrutura não, a organização está lutando contra si mesma.

---

## Agentes Envolvidos

| Agente | Papel | Responsabilidade |
|--------|-------|-----------------|
| **Vision Chief (CEO)** | Sponsor, decisor final | Aprova target model, comunica visão |
| **COO Orchestrator** | Líder do processo | Conduz análise, desenha modelo, executa transição |
| **CMO Architect** | Contribuidor de growth org | Estrutura de marketing e growth teams |
| **CTO Architect** | Contribuidor de tech org | Estrutura de engenharia e plataforma |
| **CIO Engineer** | Contribuidor de IT org | Estrutura de IT, dados e sistemas |
| **CAIO Architect** | Contribuidor de IA org | Estrutura de IA teams e governance |
| **CFO Strategist** | Validador financeiro | Impacto em headcount, compensation, budget |
| **Squad Coordinator** | Facilitador | Documentação, tracking, comunicação |

---

## Trigger (quando iniciar)

- **Cadência**: Revisão anual (parte do annual planning)
- **Evento excepcional**: Mudança significativa de estratégia ou bet
- **Evento excepcional**: Problemas de execução persistentes (bottlenecks)
- **Evento excepcional**: Crescimento rápido (headcount +50% em 6 meses)
- **Evento excepcional**: Fusão, aquisição ou spin-off
- **Quem dispara**: Vision Chief ou COO Orchestrator

---

## Pré-condições

- [ ] Estratégia e bets do período definidos
- [ ] Org chart atual documentado e atualizado
- [ ] Dados de performance por time/squad disponíveis
- [ ] Resultados da pesquisa de team health (se existir)
- [ ] Budget constraints definidos pelo CFO
- [ ] Feedback qualitativo de líderes e times coletado
- [ ] Benchmark de mercado sobre estruturas similares

---

## Processo (step-by-step com decision points)

### FASE 1: Current State Assessment (Semana 1-2)

**Step 1.1 — Mapeamento da Estrutura Atual**

- DRI: COO Orchestrator
- Framework: `frameworks/coo-orchestrator/coo-cross-functional-orchestration.md`
- Processo:
  1. Documentar org chart atual:
     - Hierarquia completa (quem reporta para quem)
     - Span of control (quantos reports diretos por líder)
     - Layers (quantos níveis entre CEO e IC)
     - Headcount por área
  2. Mapear responsabilidades reais (vs formais):
     - Quem realmente toma quais decisões?
     - Onde há sobreposição de responsabilidade?
     - Onde há vácuo de responsabilidade?
  3. Identificar informal networks:
     - Quem são os "conectores" informais?
     - Onde a informação flui bem/mal?
- Output: Current State Map

**Step 1.2 — Diagnóstico de Dores**

- DRI: COO Orchestrator
- Processo:
  1. Coletar dados quantitativos:
     - Tempo médio de decisão por tipo
     - Número de handoffs para completar processos-chave
     - Velocity de entrega por time
     - Turnover por área
     - Employee satisfaction por área
  2. Coletar dados qualitativos (entrevistas):
     - 1:1 com cada C-Level: "O que está travando?"
     - 1:1 com squad leads: "Onde a estrutura atrapalha?"
     - Survey anônimo: "O que mudaria na estrutura?"
  3. Categorizar dores:
     - Decision speed: muito lento?
     - Coordination cost: muitos handoffs?
     - Accountability gaps: ninguém é dono?
     - Scaling bottlenecks: não escala com growth?
     - Talent development: carreira travada?
- Output: Diagnóstico de Dores

**Step 1.3 — Análise de Alinhamento Estratégia-Estrutura**

- DRI: Vision Chief + COO Orchestrator
- Processo:
  1. Para cada bet estratégico:
     - A estrutura atual suporta este bet?
     - Quem é o DRI? Tem autoridade suficiente?
     - Os resources estão alocados corretamente?
  2. Para cada cadência operacional:
     - Os participantes certos estão na mesa?
     - A informação flui eficientemente?
  3. Para cada cross-squad handoff:
     - O handoff funciona? SLAs são cumpridos?
     - Os owners estão claros?
- **Decision Point**: A estrutura atual suporta a estratégia?
  - **SIM** → Ajustes incrementais, não redesenho completo
  - **NÃO** → Avançar para Fase 2 (Target Operating Model)

### FASE 2: Target Operating Model (Semana 2-3)

**Step 2.1 — Princípios de Design**

- DRI: Vision Chief + COO Orchestrator
- Processo:
  1. Definir princípios que guiarão o redesenho:
     - **Autonomia com accountability**: times decidem, mas medem
     - **Minimize handoffs**: menos dependências cross-team
     - **Clear ownership**: cada métrica tem 1 dono
     - **Career paths**: estrutura permite crescimento
     - **Scalability**: funciona com 2x o headcount atual
  2. Priorizar princípios (rank order)
  3. Vision Chief aprova princípios
- Output: Design Principles Document

**Step 2.2 — Opções de Modelo**

- DRI: COO Orchestrator
- Processo:
  1. Desenhar 2-3 opções de modelo:

| Modelo | Descrição | Prós | Contras |
|--------|-----------|------|---------|
| Funcional | Agrupado por função (eng, marketing, etc.) | Especialização, eficiência | Silos, lentidão |
| Produto | Agrupado por produto/cliente | Velocidade, ownership | Duplicação, inconsistência |
| Matrix | Dual reporting (função + produto) | Flexibilidade | Complexidade, conflito |
| Squad-based | Times autônomos cross-funcionais | Autonomia, velocidade | Alinhamento, re-use |
| Híbrido | Mix dos modelos acima | Balanceado | Complexidade de gestão |

  2. Para cada opção, avaliar contra princípios de design
  3. Para cada opção, avaliar impacto em:
     - Bets estratégicos
     - Cadência operacional
     - Cross-squad handoffs
     - Headcount e budget
     - Cultura e moral
  4. Preparar recomendação fundamentada
- Output: Options Analysis Document

**Step 2.3 — Seleção do Target Model**

- DRI: Vision Chief
- Participantes: Todos C-Level
- Duração: 2-3 horas (workshop)
- Processo:
  1. COO apresenta diagnóstico + opções
  2. Cada C-Level analisa impacto na sua área
  3. Discussão de trade-offs
  4. Vision Chief decide o target model
  5. Documentar racional da decisão
- Checklist: `checklists/org-design-quality.md`
- Registro: `data/registries/decision-registry.yaml`
- **Decision Point**: Consenso ou decisão do Vision Chief?
  - **Consenso** → Documentar e avançar
  - **Sem consenso** → Vision Chief decide (Type 1 decision)

### FASE 3: Gap Analysis (Semana 3-4)

**Step 3.1 — Mapeamento de Gaps**

- DRI: COO Orchestrator
- Processo:
  1. Comparar current state vs target model:

| Dimensão | Current | Target | Gap | Ação |
|----------|---------|--------|-----|------|
| Estrutura | X times, Y layers | A times, B layers | Delta | Reorganizar |
| Headcount | X FTEs | Y FTEs | +/- | Contratar/realocar |
| Skills | [lista] | [lista] | [lista] | Treinar/contratar |
| Processos | [lista] | [lista] | [lista] | Redesenhar |
| Tooling | [lista] | [lista] | [lista] | Implementar |
| Cultura | [atual] | [desejada] | [delta] | Change mgmt |

  2. Priorizar gaps por impacto e urgência
  3. Estimar esforço e custo para cada gap
- Output: Gap Analysis Document

**Step 3.2 — Impact Assessment**

- DRI: COO Orchestrator + CFO Strategist
- Processo:
  1. Quantificar impacto financeiro:
     - Custo de transição (one-time)
     - Mudança em headcount cost (ongoing)
     - Produtividade perdida durante transição
     - Investimentos em tooling/training
  2. Quantificar impacto em pessoas:
     - Quantas pessoas mudam de time?
     - Quantas mudam de gestor?
     - Quantas posições são eliminadas/criadas?
     - Risk of turnover during transition?
  3. Quantificar impacto em delivery:
     - Slowdown esperado durante transição
     - Timeline para atingir velocidade do target model
- Output: Impact Assessment Document

### FASE 4: Transition Plan (Semana 4-5)

**Step 4.1 — Sequenciamento da Transição**

- DRI: COO Orchestrator
- Processo:
  1. Definir fases da transição:
     - Fase 0: Comunicação (1 semana)
     - Fase 1: Quick wins (mudanças sem risco) — 2 semanas
     - Fase 2: Structural changes — 4-6 semanas
     - Fase 3: Stabilization — 4 semanas
     - Fase 4: Optimization — ongoing
  2. Para cada fase, definir:
     - O que muda
     - Quem é afetado
     - DRI da fase
     - Success criteria
     - Rollback plan (se der errado)
  3. Timeline total: 12-16 semanas típico
- Output: Transition Plan

**Step 4.2 — Risk Mitigation**

- DRI: COO Orchestrator
- Processo:
  1. Identificar riscos da transição:
     - Key person dependency durante a transição
     - Delivery slowdown impactando OKRs
     - Turnover de talentos-chave
     - Confusão sobre novas responsabilidades
     - Resistência à mudança
  2. Para cada risco, definir mitigação e contingência
  3. Definir "circuit breakers": quando pausar/reverter a transição
- Registro: `data/registries/risk-registry.yaml`

**Step 4.3 — Communication Plan**

- DRI: Vision Chief + COO Orchestrator
- Processo:
  1. Definir audiências e mensagens:

| Audiência | Mensagem | Canal | Timing |
|-----------|----------|-------|--------|
| C-Level | Full context + racional | Meeting | Semana 0 |
| Managers | Impacto + plano + FAQ | Meeting | Semana 0 |
| Todos colaboradores | Visão + timeline | All-hands | Semana 1 |
| Pessoas diretamente afetadas | 1:1 com novo gestor/papel | 1:1 | Semana 1 |
| Stakeholders externos | Se aplicável | Email/meeting | Semana 2 |

  2. Preparar FAQ (perguntas frequentes)
  3. Preparar talking points para cada audiência
  4. Definir canal de dúvidas e feedback
- Output: Communication Plan + FAQ

### FASE 5: Execução da Transição (Semana 5-16)

**Step 5.1 — Fase 0: Comunicação**

- DRI: Vision Chief
- Processo: Executar communication plan (Step 4.3)
- Tom: transparente, empático, focado no "por quê"
- **Regra**: Ninguém deve saber por fofoca. Comunicação formal primeiro.

**Step 5.2 — Fase 1: Quick Wins**

- DRI: COO Orchestrator
- Processo:
  1. Implementar mudanças de baixo risco:
     - Novos canais de comunicação
     - Ajustes de cadência
     - Clarificação de DRIs
  2. Demonstrar momentum positivo
- Timeline: 2 semanas

**Step 5.3 — Fase 2: Structural Changes**

- DRI: COO Orchestrator + cada C-Level
- Processo:
  1. Executar mudanças estruturais conforme transition plan
  2. Weekly check-in de progresso
  3. Monitorar riscos (Step 4.2)
  4. Ajustar se necessário
- Timeline: 4-6 semanas

**Step 5.4 — Fase 3: Stabilization**

- DRI: COO Orchestrator
- Processo:
  1. Monitorar indicadores de estabilidade:
     - Delivery velocity voltando ao normal?
     - Team satisfaction estável?
     - Handoffs funcionando?
     - Decision speed melhorando?
  2. Resolver issues emergentes
  3. Documentar aprendizados
- Timeline: 4 semanas

**Step 5.5 — Fase 4: Optimization**

- DRI: COO Orchestrator
- Processo:
  1. Fine-tune baseado em dados da estabilização
  2. Ajustar processos e cadências
  3. Confirmar que target model está funcionando
  4. Documentar novo estado como baseline
- Timeline: Ongoing

### FASE 6: Change Management Contínuo (Paralelo)

**Step 6.1 — Pulse Surveys**

- DRI: COO Orchestrator
- Cadência: Quinzenal durante transição
- Perguntas:
  - "De 1-5, quão claro é meu papel na nova estrutura?"
  - "De 1-5, quão bem a transição está sendo gerenciada?"
  - "O que melhoraria a transição?"
- Ação: Ajustar communication e support com base no feedback

**Step 6.2 — Support Structures**

- DRI: COO Orchestrator
- Processo:
  1. Office hours: COO disponível para dúvidas
  2. FAQ vivo: atualizado semanalmente
  3. Buddy system: pessoa experiente + pessoa em transição
  4. Coaching para líderes em novos papéis

---

## Quality Gates

### Gate 1: Qualidade da Análise

- [ ] Current state mapeado com dados (não apenas percepção)
- [ ] Dores categorizadas e priorizadas
- [ ] Alinhamento estratégia-estrutura avaliado
- [ ] 2-3 opções de modelo analisadas
- [ ] Trade-offs documentados

### Gate 2: Qualidade do Design

Aplicar `checklists/org-design-quality.md`:
- [ ] Target model alinhado com estratégia e bets
- [ ] Princípios de design definidos e respeitados
- [ ] Gap analysis completo com custos estimados
- [ ] Impact assessment financeiro e humano realizado
- [ ] Vision Chief aprovou formalmente

### Gate 3: Qualidade da Transição

- [ ] Transition plan com fases sequenciadas
- [ ] Communication plan com audiências e mensagens
- [ ] Risk mitigation com circuit breakers
- [ ] Rollback plan definido
- [ ] Timeline realista

### Gate 4: Qualidade do Change Management

Aplicar `checklists/people-culture/performance-system-quality.md`:
- [ ] Pulse surveys rodando quinzenalmente
- [ ] Support structures ativas
- [ ] Feedback sendo incorporado
- [ ] Delivery velocity monitorada
- [ ] Team satisfaction estável ou melhorando

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| Current State Map | Markdown | `data/memos/` | COO |
| Diagnóstico de Dores | Markdown | `data/memos/` | COO |
| Design Principles | Markdown | `data/memos/` | Vision Chief |
| Options Analysis | Markdown | `data/memos/` | COO |
| Target Model Decision | YAML | `data/registries/decision-registry.yaml` | Vision Chief |
| Gap Analysis | Markdown | `data/memos/` | COO |
| Transition Plan | Markdown | `data/memos/` | COO |
| Communication Plan + FAQ | Markdown | `data/memos/` | Vision Chief + COO |
| Org Design Brief | Markdown | `templates/org-people/org-design-brief.md` | COO |
| Pulse Survey Results | YAML | `data/registries/culture-registry.yaml` | COO |

---

## Registries Atualizados

- `data/registries/decision-registry.yaml` — Decisão de org design com racional
- `data/registries/risk-registry.yaml` — Riscos de transição
- `data/registries/culture-registry.yaml` — Pulse survey results
- `data/registries/hiring-registry.yaml` — Novas posições / gaps
- `data/registries/lessons-learned.yaml` — Aprendizados da transição

---

## Próximos Passos

1. **Imediato**: Comunicação e kick-off da transição
2. **Semanal**: Monitoramento de progresso no WBR → `workflows/04-wbr-loop.md`
3. **Mensal**: Review de transição no MBR → `workflows/05-mbr-loop.md`
4. **Se novas posições**: Acionar hiring → `workflows/08-exec-hiring-workflow.md`
5. **Se novos executivos**: Acionar onboarding → `workflows/10-30-60-90-onboarding.md`
6. **Trimestral**: Avaliar resultado no QBR → `workflows/06-qbr-loop.md`

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| Vision Chief | Toda organização | Comunicação de mudança | Dia 1 da Fase 0 |
| COO | Cada C-Level | Impacto na sua área + action items | 48h antes da comunicação |
| COO | Squad leads afetados | Detalhes de transição | 24h após comunicação |
| COO | Data Squad | Ajuste de métricas e dashboards | 1 semana |
| CIO | IT | Ajuste de acessos e tooling | Fase 1 |
| COO | Advisory Board | Briefing da mudança | 1 semana |
