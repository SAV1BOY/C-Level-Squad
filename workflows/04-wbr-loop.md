# Workflow 04: WBR Loop — Weekly Business Review

## Objetivo

Executar o ciclo semanal de revisão do negócio inspirado no modelo Amazon WBR:
preparar dados, revisar métricas, identificar exceções, definir ações corretivas
e garantir accountability. O WBR é o batimento cardíaco do C-Level Squad — se
ele para, o sistema operacional para.

> **Princípio**: "Cadência é o sistema operacional. Sem cadência, sem controle."
> O WBR é semanal, inegociável, e baseado em dados — nunca em opiniões.

---

## Agentes Envolvidos

| Agente | Papel no WBR | Presença |
|--------|-------------|----------|
| **COO Orchestrator** | Facilitador e owner do WBR | Obrigatória |
| **Vision Chief (CEO)** | Revisor estratégico e decisor | Obrigatória |
| **CMO Architect** | Reporta métricas de growth | Sob demanda (quando há exceções) |
| **CTO Architect** | Reporta métricas de tech | Sob demanda (quando há exceções) |
| **CIO Engineer** | Reporta métricas de IT/dados | Sob demanda (quando há exceções) |
| **CAIO Architect** | Reporta métricas de IA | Sob demanda (quando há exceções) |
| **CFO Strategist** | Reporta métricas financeiras | Sob demanda (quando há exceções) |
| **Squad Coordinator** | Documenta, acompanha ações | Obrigatória |

---

## Trigger (quando iniciar)

- **Cadência**: Toda segunda-feira (ou primeiro dia útil da semana)
- **Horário fixo**: Mesmo horário toda semana (sugestão: 9h-10h)
- **Duração**: 60 minutos (MÁXIMO — disciplina de tempo)
- **Quem dispara**: COO Orchestrator (automático, recorrente)
- **Cancelamento**: Apenas Vision Chief pode cancelar, com justificativa

---

## Pré-condições

- [ ] Metrics pack da semana preparado (até sexta-feira anterior)
- [ ] Action items da semana anterior atualizados (status: done/in progress/blocked)
- [ ] Exceções identificadas e pré-analisadas
- [ ] Agenda distribuída 24h antes do WBR
- [ ] Dados disponíveis no dashboard (não em slides)

---

## Processo (step-by-step com decision points)

### PRE-WBR: Preparação de Dados (Sexta-feira anterior)

**Step 0.1 — Coleta de Métricas**

- DRI: Squad Coordinator + CIO Engineer
- Framework: `frameworks/coo-orchestrator/coo-operating-rhythm.md`
- Processo:
  1. Coletar input metrics (métricas de atividade/esforço):
     - Pipeline novo: leads, oportunidades, MQLs
     - Tasks completadas vs planejadas (por squad)
     - Deploys realizados (DORA deployment frequency)
     - Experimentos rodados e resultados
     - Content publicado, campanhas ativas
  2. Coletar output metrics (métricas de resultado):
     - Revenue: MRR, ARR, new business, churn
     - Growth: Sign-ups, activation, retention
     - Engineering: DORA metrics, incidents
     - Customer: NPS, CSAT, tickets
  3. Comparar com targets e semanas anteriores
  4. Identificar exceções: métrica > 10% acima ou abaixo do target
- Template: `templates/operating-system/wbr-template.md`
- Referência: `templates/operational/status-report.md`

**Step 0.2 — Pré-análise de Exceções**

- DRI: COO Orchestrator
- Processo:
  1. Para cada exceção identificada:
     - Classificar como POSITIVA (acima do target) ou NEGATIVA (abaixo)
     - Hipótese inicial de causa raiz
     - Impacto potencial se tendência continuar
     - Ação sugerida (se óbvia)
  2. Preparar "Exception Cards" (1 por exceção)
  3. Priorizar: quais exceções merecem discussão no WBR?
- **Regra**: Máximo 5 exceções discutidas por WBR

**Step 0.3 — Review de Action Items Anteriores**

- DRI: Squad Coordinator
- Processo:
  1. Puxar action items do WBR anterior
  2. Para cada item, atualizar status:
     - DONE — concluído
     - IN PROGRESS — em andamento (on track?)
     - BLOCKED — bloqueado (por quê? quem desbloqueia?)
     - MISSED — não feito (por quê? replanificar?)
  3. Calcular completion rate: % de items concluídos
  4. Destacar items BLOCKED e MISSED para discussão
- Output: Status report de action items

**Step 0.4 — Distribuição da Agenda**

- DRI: COO Orchestrator
- Processo:
  1. Montar agenda padrão com exceções do dia
  2. Enviar 24h antes do WBR
  3. Anexar: metrics pack + exception cards + action item status
- Template: `templates/operating-system/meeting-agenda.md`

### WBR: Execução (60 minutos)

**Step 1 — Opening e Action Item Review (10 min)**

- DRI: COO Orchestrator
- Agenda:
  1. Checkin rápido: alguma urgência não prevista? (2 min)
  2. Review de action items anteriores (8 min):
     - Items DONE → reconhecer, mover
     - Items BLOCKED → identificar owner do desbloqueio, prazo
     - Items MISSED → entender causa, replanificar ou escalar
  3. KPI de accountability: completion rate da semana
     - Target: >= 80% dos items concluídos no prazo
- **Decision Point**: Completion rate < 60%?
  - **SIM** → Flag de alerta, discussão de 5 min sobre causa sistêmica
  - **NÃO** → Mover para Step 2

**Step 2 — Metrics Review: Input Metrics (15 min)**

- DRI: COO Orchestrator
- Framework: `frameworks/operating-system/wbr-mbr-qbr.md`
- Processo:
  1. Apresentar dashboard de input metrics
  2. Foco em tendências (3+ semanas), não em pontos isolados
  3. Para cada métrica, regra do semáforo:
     - VERDE: On track (dentro de 10% do target)
     - AMARELO: At risk (10-20% abaixo do target)
     - VERMELHO: Off track (> 20% abaixo do target)
  4. Input metrics a cobrir:
     - Pipeline volume e velocidade
     - Feature velocity (stories/tasks concluídas)
     - Experiment throughput
     - Content/campaign execution rate
  5. Apenas discutir AMARELO e VERMELHO
- **Regra Amazon WBR**: "Why?" — não "what happened" mas "why did it happen?"

**Step 3 — Metrics Review: Output Metrics (15 min)**

- DRI: COO Orchestrator
- Processo:
  1. Apresentar dashboard de output metrics
  2. Mesma regra de semáforo
  3. Output metrics a cobrir:
     - Revenue: MRR trend, new vs expansion vs churn
     - Growth: Signup → Activation → Retention funnel
     - Engineering: DORA metrics, availability
     - Customer: NPS/CSAT, support ticket trend
  4. Correlacionar outputs com inputs:
     - Input OK + output ruim = lag ou problema de conversão
     - Input ruim + output OK = leading indicator de problema futuro
     - Input ruim + output ruim = problema sistêmico
- **Decision Point**: Há correlação input/output preocupante?
  - **SIM** → Adicionar como exceção para deep dive
  - **NÃO** → Mover para Step 4

**Step 4 — Exception Deep Dive (15 min)**

- DRI: COO Orchestrator
- Processo:
  1. Apresentar top 3-5 exceções (positivas e negativas)
  2. Para cada exceção:
     - Dados: o que os números mostram? (2 min)
     - Análise: por que aconteceu? Root cause (3 min)
     - Ação: o que vamos fazer? (2 min)
  3. Para ações definidas:
     - Owner (DRI)
     - Prazo (data específica)
     - Métrica de sucesso
     - Como saberemos se resolveu?
  4. Se exceção requer mais análise: designar owner + prazo para deep dive
- **Decision Point**: Exceção requer escalação para sessão separada?
  - **SIM** → Agendar sessão específica (não expandir o WBR)
  - **NÃO** → Mover para Step 5

**Step 5 — Decisões e Action Items (5 min)**

- DRI: COO Orchestrator
- Processo:
  1. Consolidar todas as ações definidas durante o WBR
  2. Para cada ação:
     - Descrição clara (1 frase)
     - DRI (nome)
     - Prazo (data)
     - Como medir sucesso
  3. Repetir em voz alta para confirmar entendimento
  4. Registrar em `data/meeting-minutes/`
- **Regra**: Toda ação precisa de DRI + prazo. Sem DRI = sem ação.

### POST-WBR: Follow-up (Mesmo dia)

**Step 6 — Documentação**

- DRI: Squad Coordinator
- Processo:
  1. Registrar ata em `data/meeting-minutes/`
  2. Atualizar action item tracker
  3. Atualizar `data/registries/decision-registry.yaml` (se decisões tomadas)
  4. Distribuir resumo para todos os participantes (e ausentes)
- Template: `templates/operating-system/wbr-template.md`
- Timeline: Até 2h após o WBR

**Step 7 — Cascata para Squads**

- DRI: COO Orchestrator
- Processo:
  1. Comunicar ações relevantes para squads afetados
  2. Atualizar dashboards compartilhados
  3. Escalar bloqueios cross-squad identificados
- SLA: Até final do mesmo dia

**Step 8 — Preparação para Próximo WBR**

- DRI: Squad Coordinator
- Processo:
  1. Abrir novo ciclo de coleta de métricas
  2. Configurar reminders para DRIs de action items
  3. Agendar data collection para sexta-feira
- Output: Ciclo reiniciado

---

## Quality Gates

### Gate 1: Qualidade da Preparação

- [ ] Metrics pack completo e atualizado (dados < 48h)
- [ ] Exception cards preparadas (máximo 5)
- [ ] Action items anteriores com status atualizado
- [ ] Agenda distribuída 24h antes
- [ ] Dashboard funcional (não slides estáticos)

### Gate 2: Qualidade da Execução

Aplicar `checklists/operating-review-quality.md`:
- [ ] WBR durou <= 60 minutos
- [ ] Dados foram apresentados, não opiniões
- [ ] Foco em exceções e tendências, não em reporting passivo
- [ ] "Why?" foi perguntado para cada exceção
- [ ] Correlação input/output foi analisada
- [ ] Todas as ações têm DRI + prazo

### Gate 3: Qualidade do Follow-up

Aplicar `checklists/operating-system/meeting-quality.md`:
- [ ] Ata publicada até 2h após WBR
- [ ] Action items distribuídos para DRIs
- [ ] Squads notificados de ações relevantes
- [ ] Decisions registradas em `decision-registry.yaml`
- [ ] Próximo ciclo de coleta iniciado

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| Metrics pack semanal | Dashboard/YAML | `data/registries/metric-registry.yaml` | CIO + Coordinator |
| Exception cards | Markdown | `data/meeting-minutes/` | COO |
| Ata do WBR | Markdown | `data/meeting-minutes/` | Squad Coordinator |
| Action items | Markdown | `data/meeting-minutes/` | Squad Coordinator |
| Decisões | YAML | `data/registries/decision-registry.yaml` | COO |

---

## Registries Atualizados

- `data/registries/metric-registry.yaml` — Métricas semanais atualizadas
- `data/registries/decision-registry.yaml` — Decisões tomadas no WBR
- `data/registries/initiative-registry.yaml` — Status de iniciativas (se mudou)
- `data/registries/risk-registry.yaml` — Novos riscos identificados

---

## Próximos Passos

1. **Semanal**: Próximo WBR (mesmo dia, mesma hora, toda semana)
2. **Mensal**: Tendências do WBR alimentam o MBR → `workflows/05-mbr-loop.md`
3. **Trimestral**: Padrões do WBR alimentam o QBR → `workflows/06-qbr-loop.md`
4. **Excepcional**: Se exceção grave → escalar para sessão dedicada

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| Data Squad | COO | Metrics pack semanal | Sexta-feira anterior |
| COO | Squads com ações | Action items + contexto | Mesmo dia do WBR |
| COO | Vision Chief | Resumo executivo (se ausente) | Mesmo dia |
| Squad Coordinator | Todos | Ata e action items | 2h pós WBR |

### Métricas do Próprio WBR (Meta-métricas)

| Métrica | Target | Medição |
|---------|--------|---------|
| WBR realizado sem cancelamento | 95%+ | Mensal |
| Duração <= 60 min | 90%+ | Semanal |
| Action item completion rate | >= 80% | Semanal |
| Decisões com DRI + prazo | 100% | Semanal |
| Ata publicada em 2h | 95%+ | Semanal |
| Métricas pack on time | 95%+ | Semanal |

### Anti-Padrões do WBR

1. **"Status update meeting"** → WBR não é para reporting, é para exceções e decisões
2. **"Discutir o verde"** → Só discutir amarelo e vermelho
3. **"Sem dados, com opiniões"** → Se não tem dados, não discuta
4. **"Expandir para 90 minutos"** → 60 min é sagrado, agendar sessão separada
5. **"Cancelar porque está tudo bem"** → WBR é inegociável, mesmo quando tudo está ok
6. **"Action items sem dono"** → Sem DRI = não existe
7. **"Mesma exceção toda semana"** → Se repete 3x, é problema sistêmico, não exceção
