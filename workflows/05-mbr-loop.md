# Workflow 05: MBR Loop — Monthly Business Review

## Objetivo

Executar o ciclo mensal de revisão estratégico-operacional: analisar tendências
do mês, avaliar saúde das iniciativas, identificar ajustes necessários na
estratégia, rebalancear recursos e garantir que a organização está no caminho
certo para atingir os OKRs trimestrais. O MBR é mais profundo que o WBR —
aqui analisamos padrões, não pontos.

> **Princípio**: O WBR olha a semana. O MBR olha o mês. Se o WBR é o pulso,
> o MBR é o check-up mensal.

---

## Agentes Envolvidos

| Agente | Papel no MBR | Presença |
|--------|-------------|----------|
| **COO Orchestrator** | Facilitador e owner do MBR | Obrigatória |
| **Vision Chief (CEO)** | Revisor estratégico, decisor | Obrigatória |
| **CMO Architect** | Reporta growth, pipeline, GTM | Obrigatória |
| **CTO Architect** | Reporta tech health, DORA, reliability | Obrigatória |
| **CIO Engineer** | Reporta IT health, data quality, sistemas | Sob demanda |
| **CAIO Architect** | Reporta IA portfolio, adoption, evals | Sob demanda |
| **CFO Strategist** | Reporta financeiro, burn, unit economics | Obrigatória |
| **Squad Coordinator** | Documenta, acompanha ações | Obrigatória |

---

## Trigger (quando iniciar)

- **Cadência**: Primeira semana de cada mês (dias 1-5)
- **Duração**: 90 minutos (MÁXIMO)
- **Preparação**: Inicia 3 dias úteis antes da reunião
- **Quem dispara**: COO Orchestrator (recorrente)
- **Cancelamento**: Apenas com aprovação do Vision Chief + justificativa

---

## Pré-condições

- [ ] 4 WBRs do mês anterior concluídos com atas
- [ ] Métricas mensais consolidadas e validadas
- [ ] OKR progress atualizado (% de cada KR)
- [ ] Initiative health cards atualizados
- [ ] Financeiro do mês fechado (receita, custos, burn)
- [ ] Agenda distribuída 48h antes
- [ ] Cada C-Level preparou seu bloco de 10 minutos

---

## Processo (step-by-step com decision points)

### PRE-MBR: Preparação (3 dias antes)

**Step 0.1 — Consolidação de Métricas Mensais**

- DRI: CIO Engineer + Squad Coordinator
- Framework: `frameworks/coo-orchestrator/coo-execution-engine.md`
- Processo:
  1. Consolidar métricas das 4 semanas anteriores
  2. Calcular tendências: MoM (month-over-month) para cada KPI
  3. Comparar com targets trimestrais (estamos on pace?)
  4. Projeção linear: se mantiver a tendência, atingimos o target?
  5. Identificar métricas que mudaram de faixa (verde→amarelo, etc.)
- Template: `templates/operational/status-report.md`
- Output: Monthly metrics pack

**Step 0.2 — Initiative Health Assessment**

- DRI: COO Orchestrator
- Processo:
  1. Para cada iniciativa ativa, atualizar health card:
     - Status: On Track / At Risk / Off Track / Completed
     - % de conclusão vs plano
     - Budget consumido vs alocado
     - Bloqueios ativos
     - Próximo milestone e previsão
  2. Classificar iniciativas por risco:
     - VERDE: On track em todas as dimensões
     - AMARELO: 1 dimensão at risk
     - VERMELHO: 2+ dimensões at risk ou qualquer off track
  3. Preparar recomendações para AMARELO e VERMELHO
- Template: `templates/operational/initiative-health-card.md`

**Step 0.3 — OKR Progress Update**

- DRI: COO Orchestrator
- Processo:
  1. Para cada KR, atualizar progresso:
     - Valor atual vs target
     - Projeção de atingimento ao final do trimestre
     - Confidence level: Alta / Média / Baixa
  2. Calcular OKR health score por Objective:
     - Score = média ponderada dos KRs
     - Alvo: >= 0.7 ao final do trimestre
  3. Identificar KRs com confidence level Baixa
- Registro: `data/registries/okr-registry.yaml`

**Step 0.4 — Preparação por Área**

- DRI: Cada C-Level prepara seu bloco
- Formato obrigatório (10 min por área):
  1. **Top 3 métricas do mês** (com tendência)
  2. **Wins**: O que funcionou e por quê
  3. **Misses**: O que não funcionou e root cause
  4. **Asks**: O que precisa dos outros para avançar
  5. **Alertas**: Riscos ou oportunidades emergentes

### MBR: Execução (90 minutos)

**Step 1 — Opening e Meta-Review (10 min)**

- DRI: COO Orchestrator
- Agenda:
  1. Revisão de action items do MBR anterior (5 min)
  2. Scorecard de saúde do sistema operacional:
     - WBRs realizados: X/4
     - Action item completion rate média do mês
     - Decisões tomadas vs pendentes
     - Meeting-to-decision ratio
  3. Tendência geral: melhorando, estável ou piorando?

**Step 2 — Financial Overview (10 min)**

- DRI: CFO Strategist
- Métricas:
  1. Revenue: MRR, ARR, new business, expansion, churn
  2. Unit economics: CAC, LTV, LTV/CAC ratio, payback period
  3. Burn rate: actual vs budget
  4. Runway: meses de operação restantes
  5. Cash flow: in vs out, projeção 3 meses
- **Decision Point**: Burn rate > 110% do budget?
  - **SIM** → Flag vermelho, revisão de alocação obrigatória
  - **NÃO** → Registrar e mover

**Step 3 — Growth & Revenue Deep Dive (15 min)**

- DRI: CMO Architect
- Framework: `frameworks/cmo-architect/cmo-full-funnel-architecture.md`
- Métricas:
  1. Funnel completo: awareness → consideration → trial → activation → revenue
  2. Conversion rates entre estágios (tendência MoM)
  3. CAC por canal (e tendência)
  4. NRR/GRR (Net/Gross Revenue Retention)
  5. Pipeline forecast: próximo mês e trimestre
- Análise:
  - Quais canais estão escalando?
  - Quais canais estão saturando?
  - Cohort analysis: retenção por mês de entrada
- **Decision Point**: Pipeline cobre target do próximo mês?
  - **SIM** → Manter estratégia
  - **NÃO** → Definir ação de aceleração (com DRI e prazo)

**Step 4 — Tech & Platform Health (15 min)**

- DRI: CTO Architect
- Framework: `frameworks/engineering-tech/dora-metrics.md`
- Métricas:
  1. DORA metrics: deployment frequency, lead time, MTTR, CFR
  2. Platform availability vs SLO
  3. Incidents: P1/P2 count, root cause trend
  4. Tech debt ratio: novo código vs refactoring
  5. Developer experience: survey score, onboarding time
- Análise:
  - Velocidade de entrega está acelerando ou desacelerando?
  - Reliability está melhorando?
  - Tech debt está sob controle?
- **Decision Point**: DORA metrics piorando por 2+ meses?
  - **SIM** → Acionar engineering health check
  - **NÃO** → Registrar e mover

**Step 5 — Initiative Health Review (20 min)**

- DRI: COO Orchestrator
- Processo:
  1. Overview: X verdes, Y amarelos, Z vermelhos
  2. Deep dive em VERMELHOS (5 min cada):
     - O que está off track e por quê?
     - Plano de recuperação realista?
     - Precisa de mais recursos?
     - Deve ir para kill review?
  3. Quick review de AMARELOS (2 min cada):
     - O que precisa para voltar para verde?
     - Owner tem plano?
  4. Para cada iniciativa problemática, definir ação
- **Decision Point**: Alguma iniciativa deve ir para kill review?
  - **SIM** → Agendar kill review → `workflows/03-kill-list-and-sunsetting.md`
  - **NÃO** → Manter monitoramento

**Step 6 — OKR Check-in (10 min)**

- DRI: COO Orchestrator
- Processo:
  1. Dashboard de OKR progress:
     - Empresa: X% dos KRs on track
     - Por área: distribution de health
  2. KRs com confidence Baixa:
     - Root cause
     - Ação corretiva
     - Novo forecast
  3. Projeção para o trimestre:
     - Se continuar no ritmo atual, onde chegamos?
     - Gap entre projeção e target: aceitável?
- **Decision Point**: Projeção mostra OKRs < 50% atingimento no final do Q?
  - **SIM** → Sessão de emergência para replanning
  - **NÃO** → Manter e ajustar incrementalmente

**Step 7 — Resource Rebalancing (5 min)**

- DRI: COO Orchestrator + CFO Strategist
- Processo:
  1. Com base nos steps anteriores:
     - Iniciativas que precisam de mais recursos?
     - Iniciativas que podem devolver recursos?
     - Novas necessidades não previstas?
  2. Propor realocação se necessário
  3. Vision Chief aprova
- Registro: `data/registries/decision-registry.yaml`

**Step 8 — Decisões e Action Items (5 min)**

- DRI: COO Orchestrator
- Processo:
  1. Consolidar todas as decisões do MBR
  2. Consolidar action items com DRI + prazo
  3. Confirmar entendimento de cada DRI
  4. Definir follow-up: quais items serão acompanhados no WBR?
- Output: Lista de decisões + action items

### POST-MBR: Follow-up

**Step 9 — Documentação e Distribuição**

- DRI: Squad Coordinator
- Processo:
  1. Registrar ata completa em `data/meeting-minutes/`
  2. Atualizar registries:
     - `data/registries/decision-registry.yaml`
     - `data/registries/initiative-registry.yaml`
     - `data/registries/okr-registry.yaml`
  3. Distribuir resumo executivo para toda a organização
  4. Comunicar decisões de rebalanceamento para squads afetados
- SLA: Até 24h após o MBR

**Step 10 — Cascata para Squads**

- DRI: COO Orchestrator
- Processo:
  1. Comunicar ajustes de recurso para squads afetados
  2. Atualizar roadmaps se necessário
  3. Garantir que WBR da semana seguinte reflete as mudanças
- SLA: Até 48h após o MBR

---

## Quality Gates

### Gate 1: Qualidade da Preparação

- [ ] Métricas mensais completas e validadas
- [ ] Initiative health cards atualizados
- [ ] OKR progress atualizado
- [ ] Financeiro do mês fechado
- [ ] Cada C-Level preparou seu bloco

### Gate 2: Qualidade da Execução

Aplicar `checklists/operating-review-quality.md`:
- [ ] MBR durou <= 90 minutos
- [ ] Análise de tendências (não apenas pontos)
- [ ] Correlação entre métricas analisada
- [ ] Iniciativas VERMELHAS receberam deep dive
- [ ] Decisões de rebalanceamento documentadas
- [ ] Todas as ações têm DRI + prazo

### Gate 3: Qualidade do Follow-up

- [ ] Ata publicada até 24h após MBR
- [ ] Registries atualizados
- [ ] Squads notificados de mudanças
- [ ] WBR seguinte reflete ajustes do MBR

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| Monthly metrics pack | Dashboard/YAML | `data/registries/metric-registry.yaml` | CIO |
| Initiative health cards | Markdown | `data/memos/` | COO |
| OKR progress report | YAML | `data/registries/okr-registry.yaml` | COO |
| Ata do MBR | Markdown | `data/meeting-minutes/` | Squad Coordinator |
| Action items | Markdown | `data/meeting-minutes/` | Squad Coordinator |
| Decisões de rebalanceamento | YAML | `data/registries/decision-registry.yaml` | COO |
| Resumo executivo | Markdown | `data/memos/` | COO |

---

## Registries Atualizados

- `data/registries/metric-registry.yaml` — Métricas mensais e tendências
- `data/registries/okr-registry.yaml` — OKR progress atualizado
- `data/registries/initiative-registry.yaml` — Health status atualizado
- `data/registries/decision-registry.yaml` — Decisões do MBR
- `data/registries/risk-registry.yaml` — Novos riscos identificados

---

## Próximos Passos

1. **Semanal**: WBRs continuam com ajustes do MBR → `workflows/04-wbr-loop.md`
2. **Mensal**: Próximo MBR (mesmo formato, primeiro dia útil do mês)
3. **Trimestral**: 3 MBRs alimentam o QBR → `workflows/06-qbr-loop.md`
4. **Se crise**: Escalar para sessão dedicada fora do MBR

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| Data Squad | COO + CIO | Monthly metrics pack | 2 dias antes do MBR |
| CFO | COO | Financeiro do mês | 2 dias antes do MBR |
| COO | Todos squads | Resumo executivo + ações | 24h pós MBR |
| COO | Squads com rebalanceamento | Mudanças de recurso | 48h pós MBR |
| Vision Chief | Advisory Board | Summary mensal (se aplicável) | 1 semana |

### Diferenças WBR vs MBR

| Dimensão | WBR | MBR |
|----------|-----|-----|
| Frequência | Semanal | Mensal |
| Duração | 60 min | 90 min |
| Foco | Exceções e ações | Tendências e ajustes |
| Profundidade | Rasa (pontos) | Profunda (padrões) |
| Participantes | COO + Vision Chief | Todos C-Level |
| Financeiro | Não | Sim (completo) |
| OKR review | Quick flag | Deep dive |
| Decisões | Táticas | Estratégico-operacionais |
| Resource rebalancing | Não | Sim (se necessário) |
