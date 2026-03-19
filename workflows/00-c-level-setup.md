# Workflow 00: C-Level Squad Setup Inicial

## Objetivo

Realizar o bootstrapping completo do C-Level Squad: ativar todos os agentes,
definir missão e visão, atribuir DRIs, configurar cadências operacionais
(WBR/MBR/QBR), alinhar as primeiras 3 bets estratégicas e inicializar todos
os registries. Este workflow é executado **uma única vez** no início do
squad e serve como fundação para todos os demais workflows.

> **Princípio**: "Se não está escrito, não é decisão — é conversa."
> Este workflow garante que TUDO esteja escrito antes de operar.

---

## Agentes Envolvidos

| Agente | Papel neste Workflow | Responsabilidade Principal |
|--------|---------------------|---------------------------|
| **Vision Chief (CEO)** | Sponsor e decisor final | Define missão, visão, tese, bets iniciais |
| **COO Orchestrator** | Líder de execução do setup | Configura cadência, registries, accountability |
| **CMO Architect** | Contribuidor estratégico | Valida bets de growth, positioning inicial |
| **CTO Architect** | Contribuidor estratégico | Valida bets de tech, plataforma, arquitetura |
| **CIO Engineer** | Contribuidor estratégico | Configura tooling, data governance, sistemas |
| **CAIO Architect** | Contribuidor estratégico | Define portfólio IA inicial, readiness |
| **CFO Strategist** | Contribuidor financeiro | Valida budget, unit economics, alocação |
| **Squad Coordinator** | Facilitador operacional | Logística, documentação, follow-up |

---

## Trigger (quando iniciar)

- **Evento**: Criação de um novo C-Level Squad
- **Condição**: Decisão do founder/board de estruturar operação executiva
- **Frequência**: Uma única vez (pode ser re-executado em caso de reset estratégico)
- **Quem dispara**: Vision Chief ou Board

---

## Pré-condições

Antes de iniciar este workflow, verificar:

- [ ] Existe um founder/líder designado como Vision Chief
- [ ] Budget aprovado para operação do squad (mínimo 3 meses)
- [ ] Acesso ao repositório C-Level-Squad configurado
- [ ] Calendário corporativo disponível para reservar cadências
- [ ] Dados mínimos do negócio disponíveis: receita, clientes, burn rate
- [ ] Contexto de mercado documentado (mesmo que preliminar)
- [ ] Stack tecnológico atual mapeado (mesmo que alto nível)
- [ ] Time de liderança atual identificado (gaps incluídos)

---

## Processo (step-by-step com decision points)

### FASE 1: Ativação dos Agentes (Dia 1)

**Step 1.1 — Verificação de Integridade do Repositório**

- DRI: Squad Coordinator
- Ação: Validar que todos os arquivos de agentes existem em `agents/`
- Checklist:
  - [ ] `agents/vision-chief.md` presente e com 6 layers
  - [ ] `agents/coo-orchestrator.md` presente e com 6 layers
  - [ ] `agents/cmo-architect.md` presente e com 6 layers
  - [ ] `agents/cto-architect.md` presente e com 6 layers
  - [ ] `agents/cio-engineer.md` presente e com 6 layers
  - [ ] `agents/caio-architect.md` presente e com 6 layers
  - [ ] `agents/cfo-strategist.md` presente e com 6 layers
  - [ ] `agents/squad-coordinator.md` presente e com 6 layers
  - [ ] `config.yaml` validado contra `data/schemas/agent-config-schema.yaml`
- Output: Relatório de integridade do repositório
- Registro: `data/registries/system-registry.yaml`

**Step 1.2 — Atribuição de DRIs Iniciais**

- DRI: Vision Chief
- Ação: Designar pessoa/papel responsável por cada agente
- Framework: `frameworks/operating-system/rasi-dri.md`
- Tabela de atribuição:

| Agente | DRI (pessoa) | Backup | Início |
|--------|-------------|--------|--------|
| Vision Chief | [Nome] | N/A | Dia 1 |
| COO Orchestrator | [Nome] | [Nome] | Dia 1 |
| CMO Architect | [Nome] | [Nome] | Dia 1 |
| CTO Architect | [Nome] | [Nome] | Dia 1 |
| CIO Engineer | [Nome] | [Nome] | Dia 1 |
| CAIO Architect | [Nome] | [Nome] | Dia 1 |

- **Decision Point**: Algum papel está sem DRI?
  - **SIM** → Registrar gap em `data/registries/hiring-registry.yaml`, designar DRI interino
  - **NÃO** → Avançar para Step 1.3

**Step 1.3 — Calibração Inicial de Autoridade**

- DRI: Vision Chief + COO Orchestrator
- Ação: Revisar e confirmar as regras de autoridade (Type 1 vs Type 2)
- Framework: `frameworks/operating-system/rasi-dri.md`
- Referência: `authority/` (documentos de autoridade por agente)
- Output: Tabela de autoridade confirmada
- Registro: `data/registries/decision-registry.yaml`

### FASE 2: Definição de Missão e Visão (Dia 2-3)

**Step 2.1 — Workshop de Missão**

- DRI: Vision Chief
- Participantes: Todos os agentes
- Framework: `frameworks/vision-strategy/strategy-choice-cascade.md`
- Duração: 2-3 horas
- Processo:
  1. Vision Chief apresenta contexto de mercado e tese inicial
  2. Cada agente contribui com perspectiva do seu domínio
  3. Redação colaborativa da declaração de missão
  4. Teste de clareza: "Qualquer pessoa consegue explicar em 30 segundos?"
  5. Aprovação por consenso (Vision Chief tem veto)
- Output: Declaração de missão (1-2 frases)
- Template: `templates/strategy/strategy-one-pager.md`

**Step 2.2 — Definição da Visão (3-5 anos)**

- DRI: Vision Chief
- Framework: `frameworks/vision-strategy/three-horizons.md`
- Processo:
  1. Mapear estado atual (Horizonte 1)
  2. Identificar oportunidades emergentes (Horizonte 2)
  3. Definir visão transformacional (Horizonte 3)
  4. Redigir declaração de visão com timeframe
  5. Validar com cada agente: "Sua área consegue contribuir para isso?"
- **Decision Point**: A visão é ambiciosa mas alcançável?
  - **SIM** → Documentar e avançar
  - **NÃO** → Iterar até encontrar o ponto de tensão certo
- Output: Declaração de visão com timeline
- Registro: `data/registries/decision-registry.yaml`

**Step 2.3 — North Star Metric (NSM)**

- DRI: Vision Chief + COO Orchestrator
- Ação: Definir a métrica principal que reflete a saúde do negócio
- Critérios para NSM:
  - [ ] Reflete valor entregue ao cliente
  - [ ] Correlaciona com receita de longo prazo
  - [ ] Todos os times podem influenciar
  - [ ] Mensurável semanalmente
  - [ ] Simples de entender
- Output: NSM definida com baseline e target
- Registro: `data/registries/metric-registry.yaml`

### FASE 3: Tese e Bets Iniciais (Dia 4-5)

**Step 3.1 — Formulação da Tese Estratégica**

- DRI: Vision Chief
- Framework: `frameworks/vision-chief/vision-chief-strategic-thesis.md`
- Estrutura da tese:
  1. **Crença sobre o mercado**: O que acreditamos que é verdade e outros não?
  2. **Vantagem assimétrica**: Por que nós podemos vencer?
  3. **Timing**: Por que agora?
  4. **Evidências**: Que dados suportam isso?
  5. **Riscos**: O que mataria a tese?
- Output: Documento de tese estratégica (2-3 páginas)
- Checklist: `checklists/strategy-memo-quality.md`

**Step 3.2 — Seleção das 3 Bets Iniciais**

- DRI: Vision Chief
- Participantes: Todos os C-Level
- Framework: `frameworks/vision-chief/vision-chief-kill-list.md`
- Checklist: `checklists/vision/strategic-bets-selection.md`
- Processo:
  1. Brainstorm: listar 8-12 possíveis bets
  2. Filtrar: aplicar critérios de bet quality
     - Impacto potencial (1-10)
     - Probabilidade de sucesso (1-10)
     - Alinhamento com tese (1-10)
     - Capacidade de execução (1-10)
  3. Priorizar: selecionar top 3
  4. Para cada bet, definir:
     - Owner (DRI)
     - Timeline (trimestral ou semestral)
     - Budget alocado
     - Kill criteria (quando desistir)
     - Métricas de sucesso (leading + lagging)
  5. Vision Chief aprova seleção final
- **Decision Point**: As 3 bets estão diversificadas nos horizons?
  - **SIM** → Documentar e avançar
  - **NÃO** → Rebalancear entre H1 (core), H2 (adjacente), H3 (transformacional)
- Output: 3 Bet Cards preenchidos
- Registro: `data/registries/initiative-registry.yaml`

**Step 3.3 — Kill List Inicial**

- DRI: Vision Chief
- Ação: Definir explicitamente o que NÃO faremos
- Framework: `frameworks/vision-chief/vision-chief-kill-list.md`
- Processo:
  1. Listar atividades/iniciativas atuais
  2. Para cada uma: contribui para as 3 bets? SIM/NÃO
  3. NÃO → adicionar à kill list com justificativa
  4. Comunicar kill list a todos os agentes
- Output: Kill list documentada
- Registro: `data/registries/decision-registry.yaml`

### FASE 4: Configuração de Cadência (Dia 6-7)

**Step 4.1 — Definição do Ritmo Operacional**

- DRI: COO Orchestrator
- Framework: `frameworks/operating-system/wbr-mbr-qbr.md`
- Framework: `frameworks/coo-orchestrator/coo-operating-rhythm.md`
- Cadências a configurar:

| Cadência | Frequência | Duração | Participantes | DRI |
|----------|-----------|---------|--------------|-----|
| WBR | Semanal | 60 min | COO + Vision Chief + DRIs | COO |
| MBR | Mensal | 90 min | Todos C-Level | COO |
| QBR | Trimestral | 4h | Todos C-Level + Board prep | Vision Chief |
| Annual Planning | Anual | 2 dias | Todos C-Level | Vision Chief |
| Kill Review | Trimestral | 60 min | Vision Chief + COO | Vision Chief |
| C-Level Sync | Semanal | 30 min | Todos C-Level | COO |
| Cross-Squad Sync | Quinzenal | 45 min | COO + Squad leads | COO |

- Output: Calendário de cadências bloqueado
- Registro: `data/registries/decision-registry.yaml`

**Step 4.2 — Configuração de Templates de Reunião**

- DRI: COO Orchestrator
- Ação: Garantir que cada cadência tem template e agenda padrão
- Templates obrigatórios:
  - [ ] `templates/operating-system/wbr-template.md` — configurado
  - [ ] `templates/operating-system/mbr-template.md` — configurado
  - [ ] `templates/operating-system/qbr-template.md` — configurado
  - [ ] `templates/operating-system/meeting-agenda.md` — configurado
- Output: Templates validados e prontos para uso

**Step 4.3 — Definição de Métricas Pack**

- DRI: COO Orchestrator + CIO Engineer
- Ação: Definir o pack de métricas para cada cadência
- Framework: `frameworks/coo-orchestrator/coo-execution-engine.md`
- Métricas WBR (input metrics):
  - Pipeline de leads/oportunidades
  - Tasks completadas vs planejadas
  - Blockers ativos
  - Action items em aberto
- Métricas MBR (output metrics):
  - Revenue vs target
  - CAC / LTV
  - Initiative health
  - DORA metrics
- Métricas QBR (strategic metrics):
  - OKR progress
  - Bet status
  - Moat strength
  - Team health
- Output: Metrics pack por cadência
- Registro: `data/registries/metric-registry.yaml`

### FASE 5: Inicialização de Registries (Dia 8)

**Step 5.1 — Setup de Registries**

- DRI: Squad Coordinator + CIO Engineer
- Ação: Inicializar todos os registries com estrutura base
- Registries a inicializar:

| Registry | Arquivo | Conteúdo Inicial |
|----------|---------|-----------------|
| Decisões | `data/registries/decision-registry.yaml` | Decisões do setup |
| Iniciativas | `data/registries/initiative-registry.yaml` | 3 bets + kill list |
| OKRs | `data/registries/okr-registry.yaml` | OKRs Q1 (se definidos) |
| Métricas | `data/registries/metric-registry.yaml` | NSM + KPIs iniciais |
| Riscos | `data/registries/risk-registry.yaml` | Top 5 riscos iniciais |
| Sistemas | `data/registries/system-registry.yaml` | Stack atual |
| Hiring | `data/registries/hiring-registry.yaml` | Gaps de liderança |
| Cultura | `data/registries/culture-registry.yaml` | Valores declarados |
| IA | `data/registries/ai-use-case-registry.yaml` | Pipeline IA inicial |
| Lessons | `data/registries/lessons-learned.yaml` | Vazio (ready) |

- Checklist: `checklists/operating-system/project-execution-quality.md`
- Output: Todos os registries inicializados e válidos

**Step 5.2 — Validação de Schemas**

- DRI: CIO Engineer
- Ação: Garantir que todos os registries seguem os schemas definidos
- Referência: `data/schemas/`
- Processo:
  1. Validar cada registry contra seu schema
  2. Corrigir inconsistências
  3. Documentar exceções
- Output: Relatório de validação

### FASE 6: Primeira Sessão de Calibração (Dia 9-10)

**Step 6.1 — Sessão de Calibração do Squad**

- DRI: Vision Chief
- Participantes: Todos os C-Level
- Duração: 3-4 horas
- Agenda:
  1. **Revisão da Missão e Visão** (30 min)
     - Todos alinhados? Ajustes necessários?
  2. **Revisão das 3 Bets** (60 min)
     - Cada owner apresenta plano de 90 dias
     - Grupo valida/desafia
  3. **Revisão de Kill List** (30 min)
     - Alguma adição necessária?
  4. **Revisão de Cadência** (30 min)
     - Horários confirmados? Conflitos?
  5. **Cross-squad Contracts** (30 min)
     - SLAs iniciais definidos?
  6. **Riscos e Preocupações** (30 min)
     - Cada agente compartilha top 1 risco
  7. **Próximos Passos** (30 min)
     - Action items com DRI + prazo

**Step 6.2 — Documentação da Calibração**

- DRI: Squad Coordinator
- Ação: Registrar todas as decisões e action items
- Template: `templates/operating-system/meeting-agenda.md`
- Registro: `data/meeting-minutes/`
- Registries atualizados:
  - `data/registries/decision-registry.yaml`
  - `data/registries/risk-registry.yaml`

**Step 6.3 — Comunicação de Lançamento**

- DRI: Vision Chief + COO Orchestrator
- Ação: Comunicar formalmente o lançamento do C-Level Squad
- Audiência: Toda a organização / stakeholders
- Conteúdo:
  - Missão e visão
  - Quem são os membros e seus papéis
  - Cadência operacional
  - Como interagir com o squad
  - Primeiros 90 dias: o que esperar

---

## Quality Gates

### Gate 1: Completude do Setup

- [ ] Todos os 6+ agentes têm DRI designado
- [ ] Missão e visão documentadas e aprovadas
- [ ] NSM definida com baseline
- [ ] Tese estratégica redigida e aprovada
- [ ] 3 bets selecionadas com owners e kill criteria
- [ ] Kill list documentada
- [ ] Cadências configuradas no calendário
- [ ] Todos os registries inicializados
- [ ] Primeira calibração realizada

### Gate 2: Qualidade dos Artefatos

- [ ] Aplicar `checklists/strategy-memo-quality.md` na tese
- [ ] Aplicar `checklists/vision/vision-clarity-audit.md` na visão
- [ ] Aplicar `checklists/vision/strategic-bets-selection.md` nas bets
- [ ] Aplicar `checklists/okr-quality.md` nos OKRs iniciais (se definidos)
- [ ] Aplicar `checklists/operating-review-quality.md` na cadência

### Gate 3: Prontidão Operacional

- [ ] WBR pode ser executada na próxima semana
- [ ] Métricas pack está disponível (mesmo que parcial)
- [ ] Cada agente sabe seu papel e autoridade
- [ ] Canal de comunicação do squad está ativo
- [ ] Escalation path está claro para todos

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| Declaração de missão | Markdown | `templates/strategy/strategy-one-pager.md` | Vision Chief |
| Declaração de visão | Markdown | `templates/strategy/strategy-one-pager.md` | Vision Chief |
| Tese estratégica | Markdown | `data/memos/` | Vision Chief |
| 3 Bet Cards | YAML + Markdown | `data/registries/initiative-registry.yaml` | Vision Chief |
| Kill list | YAML | `data/registries/decision-registry.yaml` | Vision Chief |
| Tabela de DRIs | YAML | `data/registries/decision-registry.yaml` | COO |
| Calendário de cadências | Markdown | `data/meeting-minutes/` | COO |
| Metrics pack | YAML | `data/registries/metric-registry.yaml` | COO + CIO |
| Registries inicializados | YAML | `data/registries/` | Squad Coordinator |
| Ata da calibração | Markdown | `data/meeting-minutes/` | Squad Coordinator |
| Comunicação de lançamento | Markdown | `data/memos/` | Vision Chief |

---

## Registries Atualizados

- `data/registries/decision-registry.yaml` — Decisões do setup (missão, visão, bets, kill list)
- `data/registries/initiative-registry.yaml` — 3 bets iniciais com metadata
- `data/registries/metric-registry.yaml` — NSM + KPIs + métricas pack
- `data/registries/risk-registry.yaml` — Top 5 riscos iniciais
- `data/registries/hiring-registry.yaml` — Gaps de liderança identificados
- `data/registries/system-registry.yaml` — Stack e tooling atual
- `data/registries/culture-registry.yaml` — Valores e princípios
- `data/registries/ai-use-case-registry.yaml` — Pipeline IA (se aplicável)

---

## Próximos Passos

Após conclusão do Workflow 00:

1. **Imediato (Semana 1)**:
   - Executar primeiro WBR → `workflows/04-wbr-loop.md`
   - Iniciar Workflow 01 → `workflows/01-vision-to-okrs.md`
2. **Curto prazo (Semanas 2-4)**:
   - Executar Workflow 02 → `workflows/02-bets-to-roadmaps.md`
   - Primeiro MBR → `workflows/05-mbr-loop.md`
3. **Médio prazo (Mês 2-3)**:
   - Primeiro QBR → `workflows/06-qbr-loop.md`
   - Kill list review → `workflows/03-kill-list-and-sunsetting.md`
4. **Contínuo**:
   - Cadências operacionais mantidas
   - Registries atualizados a cada decisão
   - RalphLoop ativo: registrar → medir → retroalimentar

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| C-Level Squad | Brand Squad | Positioning thesis, missão, visão | 48h após setup |
| C-Level Squad | Copy Squad | Value proposition, ICP profiles | 1 semana |
| C-Level Squad | Data Squad | Metric definitions, NSM, KPIs | 48h após setup |
| C-Level Squad | Design Squad | Product strategy inicial | 1 semana |
| C-Level Squad | Traffic Squad | Budget allocation, channel constraints | 48h |
| C-Level Squad | Cybersecurity | Risk gates, compliance needs | 1 semana |
| C-Level Squad | Advisory Board | Tese, bets, questions estratégicas | 1 semana |
| C-Level Squad | Storytelling | Company narrative, founder story | 1 semana |
| C-Level Squad | Movement | Mission/values, culture thesis | 1 semana |

### Protocolo de Handoff

Para cada handoff acima, usar template: `templates/operational/cross-squad-handoff.md`

```yaml
handoff:
  from: c-level-squad
  to: [squad-destino]
  input: [artefato do setup]
  format: markdown
  dod: "Artefato revisado e aprovado pelo C-Level"
  dor: "Squad destino confirmou recebimento e capacidade"
  sla: "[conforme tabela acima]"
  owner: "[DRI do handoff]"
  escalation: "COO Orchestrator se SLA estourar"
```

---

## Checklist Final de Conclusão do Setup

- [ ] Todos os agentes ativados e com DRI
- [ ] Missão clara e comunicada
- [ ] Visão documentada com timeline
- [ ] NSM definida e mensurável
- [ ] Tese estratégica aprovada
- [ ] 3 bets com owners, metrics e kill criteria
- [ ] Kill list publicada
- [ ] Cadências no calendário
- [ ] Registries inicializados
- [ ] Calibração realizada
- [ ] Comunicação de lançamento enviada
- [ ] Primeiro WBR agendado
- [ ] Cross-squad handoffs iniciados
