# Workflow 06: QBR Loop — Quarterly Business Review

## Objetivo

Executar o ciclo trimestral de revisão estratégica: scoring de OKRs do
trimestre encerrado, avaliação de bets e iniciativas, revisão de kill list,
planejamento do próximo trimestre, alinhamento cross-squad e preparação
de board pack. O QBR é o momento mais importante do calendário do C-Level —
aqui a estratégia encontra a realidade.

> **Princípio**: O QBR é onde honestidade encontra accountability.
> Se o WBR é o pulso e o MBR é o check-up, o QBR é o exame completo.

---

## Agentes Envolvidos

| Agente | Papel no QBR | Presença |
|--------|-------------|----------|
| **Vision Chief (CEO)** | Líder estratégico, decisor final | Obrigatória |
| **COO Orchestrator** | Facilitador e owner operacional do QBR | Obrigatória |
| **CMO Architect** | Reporta growth, scoring de OKRs growth | Obrigatória |
| **CTO Architect** | Reporta tech, scoring de OKRs tech | Obrigatória |
| **CIO Engineer** | Reporta IT/dados, scoring de OKRs IT | Obrigatória |
| **CAIO Architect** | Reporta IA, scoring de OKRs IA | Obrigatória |
| **CFO Strategist** | Reporta financeiro, budget review | Obrigatória |
| **Squad Coordinator** | Documenta, facilita, acompanha | Obrigatória |

---

## Trigger (quando iniciar)

- **Cadência**: Última semana de cada trimestre (Q1=Mar, Q2=Jun, Q3=Set, Q4=Dez)
- **Duração**: 4 horas (dividido em 2 blocos de 2h se necessário)
- **Preparação**: Inicia 2 semanas antes
- **Quem dispara**: COO Orchestrator
- **Cancelamento**: NÃO cancelável. QBR é inegociável.

---

## Pré-condições

- [ ] 3 MBRs do trimestre concluídos com atas
- [ ] OKR scoring completo por todos os C-Level
- [ ] Financeiro do trimestre fechado
- [ ] Initiative health cards finais
- [ ] Kill list review preparada
- [ ] Board pack draft pronto (se aplicável)
- [ ] Pesquisa de team health realizada
- [ ] Cada C-Level preparou sua retrospectiva trimestral

---

## Processo (step-by-step com decision points)

### PRE-QBR: Preparação (2 semanas antes)

**Step 0.1 — OKR Self-Scoring**

- DRI: Cada C-Level (para seus OKRs de área)
- Framework: `frameworks/operating-system/okrs.md`
- Processo:
  1. Para cada Key Result, definir score final:
     - 0.0 — Nenhum progresso
     - 0.3 — Progresso mínimo
     - 0.5 — Halfway, abaixo do esperado
     - 0.7 — Progresso significativo (target esperado)
     - 1.0 — Full delivery ou above (excepcional)
  2. Para cada Objective, calcular score médio dos KRs
  3. Preparar narrativa: por que esse score? O que aprendemos?
  4. Identificar KRs que falharam e root cause
- Template: `templates/strategy/quarterly-plan.md`
- Registro: `data/registries/okr-registry.yaml`

**Step 0.2 — Compilação de Métricas Trimestrais**

- DRI: CIO Engineer + Squad Coordinator
- Processo:
  1. Consolidar métricas dos 3 meses
  2. Calcular tendências QoQ (quarter-over-quarter)
  3. Comparar com targets anuais: estamos on pace?
  4. Criar trend charts para KPIs estratégicos
  5. Preparar comparativo com trimestre anterior
- Template: `templates/strategy/quarterly-plan.md`

**Step 0.3 — Initiative Portfolio Review**

- DRI: COO Orchestrator
- Processo:
  1. Status final de cada iniciativa:
     - Completed (atingiu objetivo)
     - On Track (continua no próximo Q)
     - At Risk (precisa de intervenção)
     - Killed (encerrada durante o Q)
     - Stalled (sem progresso, precisa de decisão)
  2. Para cada iniciativa, documentar:
     - Budget consumido vs alocado
     - Timeline: adiantada, on time, atrasada
     - Valor entregue (métricas)
     - Aprendizados
  3. Preparar recomendações para o próximo trimestre
- Template: `templates/operational/initiative-health-card.md`

**Step 0.4 — Kill List Pre-Review**

- DRI: Vision Chief + COO Orchestrator
- Framework: `frameworks/vision-chief/vision-chief-kill-list.md`
- Checklist: `checklists/execution/kill-criteria-quality.md`
- Processo:
  1. Revisar todas as iniciativas ativas contra kill criteria
  2. Identificar candidatas a kill para o próximo Q
  3. Preparar análise para discussão no QBR
  4. Pré-alinhar com owners das iniciativas
- Output: Kill list draft para QBR

**Step 0.5 — Board Pack Preparation**

- DRI: Vision Chief + COO Orchestrator
- Template: `templates/operating-system/board-prep-pack.md`
- Checklist: `checklists/board-prep-quality.md`
- Processo:
  1. Preparar executive summary do trimestre
  2. Incluir: métricas, OKR scoring, financeiro, highlights, lowlights
  3. Preparar asks para o board (se aplicável)
  4. Preparar Q&A anticipado
- Output: Board pack draft (revisão final pós-QBR)

**Step 0.6 — Retrospectiva por Área**

- DRI: Cada C-Level
- Formato obrigatório (15 min por área):
  1. **OKR Scoring** — scores com narrativa
  2. **Top 3 Wins** — o que funcionou e por que é replicável
  3. **Top 3 Misses** — o que não funcionou e root cause
  4. **Surpresas** — o que não prevíamos (positivo e negativo)
  5. **Proposta para próximo Q** — OKRs, iniciativas, recursos

### QBR: Execução (4 horas)

#### BLOCO 1: Retrospectiva (2 horas)

**Step 1 — Opening e Contexto (10 min)**

- DRI: Vision Chief
- Agenda:
  1. Contexto de mercado: o que mudou no trimestre?
  2. Tese estratégica: ainda válida?
  3. Tone-setting: "Somos honestos sobre os resultados"

**Step 2 — Financial Review (20 min)**

- DRI: CFO Strategist
- Métricas trimestrais:
  1. Revenue: ARR/MRR actual vs target, growth rate QoQ
  2. Unit economics: CAC, LTV, payback, burn multiple
  3. Cash position: runway, cash flow
  4. Budget: actual vs planned, variance por área
  5. Projeção: forecast para próximo Q e ano
- **Decision Point**: Revenue < 80% do target?
  - **SIM** → Flag estratégico, revisão de bets obrigatória
  - **NÃO** → Registrar e mover

**Step 3 — OKR Scoring Round-Robin (40 min)**

- DRI: COO Orchestrator
- Processo:
  1. Cada C-Level apresenta OKR scoring da sua área (5-7 min cada)
  2. Grupo valida: "Esse score está honesto?"
  3. Consolidar OKR scorecard de empresa:
     - Média de scores
     - % de KRs que atingiram >= 0.7
     - % de Objectives com score >= 0.7
  4. Identificar padrões cross-área:
     - OKRs que falharam por dependência cross-area
     - OKRs que sobreviveram apesar de obstacles

**Step 4 — Initiative Portfolio Review (30 min)**

- DRI: COO Orchestrator
- Processo:
  1. Apresentar portfolio health: X completed, Y on track, Z at risk/killed
  2. Deep dive em iniciativas problemáticas
  3. Reconhecer iniciativas bem-sucedidas e o que aprendemos
  4. Decisões sobre iniciativas stalled
- **Decision Point**: Há iniciativas que devem ser matadas?
  - **SIM** → Agendar kill review formal → `workflows/03-kill-list-and-sunsetting.md`
  - **NÃO** → Confirmar continuidade com ajustes

**Step 5 — Kill List Review (20 min)**

- DRI: Vision Chief
- Processo:
  1. Apresentar kill list draft (do Step 0.4)
  2. Discutir cada candidata:
     - Kill criteria atingidos?
     - Teste de sunk cost: investiríamos de novo?
     - Custo de continuar vs matar?
  3. Decisões finais: KILL / PIVOT / CONTINUE
  4. Atualizar kill list oficial
- Registro: `data/registries/decision-registry.yaml`

#### BLOCO 2: Planejamento (2 horas)

**Step 6 — Strategy Assessment (20 min)**

- DRI: Vision Chief
- Framework: `frameworks/vision-strategy/strategy-choice-cascade.md`
- Processo:
  1. A tese estratégica ainda é válida? Evidências?
  2. Os bets estão entregando? Devemos mudar algum?
  3. A NSM está no caminho certo?
  4. Há mudanças de mercado que exigem adaptação?
  5. O moat está mais forte ou mais fraco?
- **Decision Point**: Tese precisa de atualização?
  - **SIM** → Sessão dedicada de strategy update (1 semana)
  - **NÃO** → Manter e avançar para planning

**Step 7 — Next Quarter OKR Definition (40 min)**

- DRI: Vision Chief + COO Orchestrator
- Processo:
  1. Com base nos resultados e aprendizados:
     - Quais OKRs continuam (com ajustes)?
     - Quais OKRs são novos?
     - Quais OKRs são descontinuados?
  2. Cada C-Level propõe 2-3 Objectives para o próximo Q
  3. Grupo alinha e resolve conflitos
  4. Vision Chief aprova o pacote
- Framework: `frameworks/operating-system/okrs.md`
- Checklist: `checklists/okr-quality.md`
- **Nota**: OKRs detalhados serão refinados no Workflow 01 pós-QBR

**Step 8 — Resource Planning (20 min)**

- DRI: COO Orchestrator + CFO Strategist
- Processo:
  1. Budget para próximo Q: disponível vs necessário
  2. Headcount: gaps, contratações, realocações
  3. Resource allocation por bet/iniciativa
  4. Trade-offs: se não cabe tudo, o que cortar?
  5. CFO valida viabilidade financeira
- Registro: `data/registries/decision-registry.yaml`

**Step 9 — Cross-squad Alignment (20 min)**

- DRI: COO Orchestrator
- Processo:
  1. Revisar SLAs cross-squad: foram cumpridos?
  2. Identificar handoffs que falharam e por quê
  3. Definir ajustes para próximo Q
  4. Confirmar owners de cada handoff
  5. Atualizar contratos cross-squad
- Referência: `config.yaml` → seção `cross_squad`

**Step 10 — Decisions e Action Items (20 min)**

- DRI: COO Orchestrator
- Processo:
  1. Consolidar todas as decisões do QBR
  2. Para cada decisão:
     - Descrição, racional, owner, prazo
     - Type 1 ou Type 2?
  3. Action items com DRI + prazo
  4. Definir timeline de execução pós-QBR
  5. Confirmar data do próximo QBR

### POST-QBR: Follow-up (1 semana)

**Step 11 — Documentação Completa**

- DRI: Squad Coordinator
- Processo:
  1. Ata completa do QBR em `data/meeting-minutes/`
  2. OKR scores finais em `data/registries/okr-registry.yaml`
  3. Decisões em `data/registries/decision-registry.yaml`
  4. Lessons learned em `data/registries/lessons-learned.yaml`
  5. Distribuir para toda a organização
- SLA: 48h após QBR

**Step 12 — Board Pack Finalização**

- DRI: Vision Chief
- Processo:
  1. Finalizar board pack com resultados do QBR
  2. Revisar com COO
  3. Enviar para board (se aplicável)
- Referência: `workflows/17-board-prep-and-delivery.md`

**Step 13 — Kick-off do Próximo Trimestre**

- DRI: COO Orchestrator
- Processo:
  1. Iniciar Workflow 01 (Vision-to-OKRs) para refinar OKRs
  2. Atualizar roadmaps (Workflow 02) com ajustes
  3. Comunicar direção do próximo Q para squads
  4. Configurar primeiro WBR do novo Q
- Timeline: Primeira semana do novo trimestre

---

## Quality Gates

### Gate 1: Qualidade da Preparação

- [ ] OKR self-scoring completo por todos os C-Level
- [ ] Métricas trimestrais consolidadas e validadas
- [ ] Initiative portfolio review completo
- [ ] Kill list pre-review realizado
- [ ] Board pack draft pronto
- [ ] Retrospectivas por área preparadas

### Gate 2: Qualidade da Retrospectiva

Aplicar `checklists/operating-review-quality.md`:
- [ ] OKR scoring honesto (não inflado)
- [ ] Root cause analysis para KRs que falharam
- [ ] Wins e misses documentados com aprendizados
- [ ] Kill list revisada com dados, não emoção
- [ ] Financeiro completo e reconciliado

### Gate 3: Qualidade do Planejamento

Aplicar `checklists/quarterly-planning-quality.md`:
- [ ] OKRs do próximo Q alinhados com tese e bets
- [ ] Resources realocados com base em resultados
- [ ] Cross-squad SLAs revisados e atualizados
- [ ] Timeline de execução definido
- [ ] Board pack finalizado (se aplicável)

### Gate 4: Qualidade da Documentação

- [ ] Ata completa publicada em 48h
- [ ] Todos os registries atualizados
- [ ] Lessons learned documentados
- [ ] Comunicação para organização distribuída
- [ ] Próximo Q kick-off agendado

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| OKR scorecard final | YAML | `data/registries/okr-registry.yaml` | COO |
| Quarterly metrics report | Dashboard | `data/registries/metric-registry.yaml` | CIO |
| Initiative portfolio status | Markdown | `data/memos/` | COO |
| Kill list decisions | YAML | `data/registries/decision-registry.yaml` | Vision Chief |
| Next Q OKRs (draft) | YAML | `data/registries/okr-registry.yaml` | Vision Chief |
| Board pack | Markdown | `data/memos/` | Vision Chief |
| QBR ata completa | Markdown | `data/meeting-minutes/` | Squad Coordinator |
| Lessons learned | YAML | `data/registries/lessons-learned.yaml` | Squad Coordinator |

---

## Registries Atualizados

- `data/registries/okr-registry.yaml` — Scores finais + novos OKRs draft
- `data/registries/initiative-registry.yaml` — Status final + novas iniciativas
- `data/registries/decision-registry.yaml` — Decisões estratégicas do Q
- `data/registries/metric-registry.yaml` — Métricas trimestrais
- `data/registries/risk-registry.yaml` — Riscos atualizados
- `data/registries/lessons-learned.yaml` — Aprendizados do trimestre

---

## Próximos Passos

1. **Imediato**: Finalizar board pack → `workflows/17-board-prep-and-delivery.md`
2. **Semana 1**: Refinar OKRs do próximo Q → `workflows/01-vision-to-okrs.md`
3. **Semana 2**: Atualizar roadmaps → `workflows/02-bets-to-roadmaps.md`
4. **Semana 3**: Kill list execution → `workflows/03-kill-list-and-sunsetting.md`
5. **Contínuo**: WBRs e MBRs do novo trimestre

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| Vision Chief | Advisory Board | Board pack + asks | 1 semana pós QBR |
| COO | Todos squads | Direção do próximo Q + OKRs | 48h pós QBR |
| COO | Data Squad | Novas métricas e targets | 48h |
| CMO | Traffic/Brand/Copy | Growth direction + budgets | 1 semana |
| CTO | Design Squad | Product direction + priorities | 1 semana |
| CIO | Cybersecurity | Updated risk/compliance needs | 1 semana |
| Vision Chief | Storytelling | Narrativa do próximo Q | 1 semana |
