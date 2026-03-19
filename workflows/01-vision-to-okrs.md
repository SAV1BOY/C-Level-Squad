# Workflow 01: Vision-to-OKRs — Da Visão Estratégica aos OKRs Executáveis

## Objetivo

Converter a visão e tese estratégica do Vision Chief em OKRs (Objectives and
Key Results) executáveis, cascateados e alinhados em todos os níveis da
organização. Este workflow garante que a direção estratégica se traduz em
metas mensuráveis com owners, timelines e critérios de sucesso claros.

> **Princípio**: Visão sem OKR é desejo. OKR sem visão é tarefa.
> Este workflow conecta os dois com rigor.

---

## Agentes Envolvidos

| Agente | Papel neste Workflow | Fase Principal |
|--------|---------------------|---------------|
| **Vision Chief (CEO)** | Define tese, bets e Objectives de empresa | Fase 1-2 |
| **COO Orchestrator** | Garante cascata, alinhamento e tracking | Fase 2-4 |
| **CMO Architect** | Define OKRs de growth e GTM | Fase 3 |
| **CTO Architect** | Define OKRs de tech e plataforma | Fase 3 |
| **CIO Engineer** | Define OKRs de IT, dados e sistemas | Fase 3 |
| **CAIO Architect** | Define OKRs de IA e automação | Fase 3 |
| **CFO Strategist** | Valida viabilidade financeira dos OKRs | Fase 4 |
| **Squad Coordinator** | Documenta, facilita e acompanha | Todas |

---

## Trigger (quando iniciar)

- **Cadência regular**: Início de cada trimestre (4 semanas antes do QBR)
- **Evento excepcional**: Mudança significativa de tese ou pivô estratégico
- **Pré-requisito**: Workflow 00 concluído (setup inicial)
- **Quem dispara**: Vision Chief ou COO Orchestrator

---

## Pré-condições

- [ ] Tese estratégica documentada e vigente
- [ ] Bets estratégicas definidas (1-3 bets ativas)
- [ ] NSM (North Star Metric) definida com baseline
- [ ] Dados de performance do período anterior disponíveis
- [ ] Resultados do QBR anterior (se não for o primeiro ciclo)
- [ ] Kill list atualizada
- [ ] Budget do período confirmado
- [ ] Todos os agentes com DRI ativo

---

## Processo (step-by-step com decision points)

### FASE 1: Revisão Estratégica (Semana 1)

**Step 1.1 — Revisão da Tese Estratégica**

- DRI: Vision Chief
- Framework: `frameworks/vision-chief/vision-chief-strategic-thesis.md`
- Processo:
  1. Reler tese vigente
  2. Avaliar evidências novas (mercado, competição, dados internos)
  3. Atualizar premissas se necessário
  4. Documentar mudanças em `data/registries/decision-registry.yaml`
- **Decision Point**: A tese mudou significativamente?
  - **SIM** → Convocar sessão extraordinária com todos C-Level, revisar bets
  - **NÃO** → Manter tese e avançar para Step 1.2

**Step 1.2 — Revisão dos Bets Ativos**

- DRI: Vision Chief
- Framework: `frameworks/vision-chief/vision-chief-kill-list.md`
- Checklist: `checklists/vision/strategic-bets-selection.md`
- Processo:
  1. Para cada bet ativo:
     - Status: On Track / At Risk / Off Track
     - Kill criteria: algum threshold atingido?
     - Aprendizados do período anterior
  2. Decisão por bet: Continuar / Ajustar / Matar
  3. Novos bets a adicionar? (máximo 3 ativos)
- **Decision Point**: Algum bet deve ser matado?
  - **SIM** → Acionar `workflows/03-kill-list-and-sunsetting.md`
  - **NÃO** → Avançar para Step 1.3

**Step 1.3 — Definição do OGSM de Empresa**

- DRI: Vision Chief
- Framework: `frameworks/vision-strategy/ogsm.md`
- Framework: `frameworks/vision-strategy/strategy-choice-cascade.md`
- Estrutura OGSM:

```
O — Objective (Objetivo qualitativo, inspiracional)
    "Ser a referência em [domínio] para [ICP]"

G — Goals (Metas quantitativas, 2-3 por Objective)
    "Atingir R$ XM em ARR"
    "Alcançar NPS > 70"

S — Strategies (Como vamos atingir — 3-5 alavancas)
    "Expandir para segmento Y"
    "Lançar produto Z"

M — Measures (Como sabemos se está funcionando)
    "Pipeline de R$ XM até mês 2"
    "10 clientes enterprise até mês 3"
```

- Output: OGSM de empresa para o trimestre
- Template: `templates/strategy/quarterly-plan.md`

### FASE 2: Definição de OKRs de Empresa (Semana 2)

**Step 2.1 — Tradução de OGSM em OKRs**

- DRI: Vision Chief + COO Orchestrator
- Framework: `frameworks/operating-system/okrs.md`
- Regras de OKR:
  1. **Máximo 3-5 Objectives por nível**
  2. **2-5 Key Results por Objective**
  3. **Key Results são mensuráveis** (número, %, data)
  4. **Objectives são qualitativos** (inspiracionais, direcionais)
  5. **Ambição calibrada**: 70% de atingimento = sucesso
  6. **Owner único** para cada Objective e cada KR
- Processo:
  1. Para cada Goal do OGSM, derivar 1-2 Objectives
  2. Para cada Objective, definir 2-4 Key Results
  3. Para cada KR, definir: baseline, target, stretch, owner
  4. Validar coerência: KRs somados = Objective atingido?
- Template: `templates/strategy/quarterly-plan.md`

**Step 2.2 — Scoring de Alinhamento**

- DRI: COO Orchestrator
- Processo:
  1. Para cada OKR de empresa, verificar:
     - [ ] Alinha com pelo menos 1 bet ativo
     - [ ] Contribui para a NSM
     - [ ] Tem owner claro
     - [ ] É mensurável semanalmente ou quinzenalmente
     - [ ] Não duplica outro OKR
  2. Score de alinhamento: cada OKR recebe nota 1-5
  3. OKRs com score < 3 → revisar ou eliminar
- **Decision Point**: Todos os OKRs passam no alinhamento?
  - **SIM** → Avançar para Fase 3
  - **NÃO** → Iterar com Vision Chief até atingir score >= 3

**Step 2.3 — Validação OGSM-OKR**

- DRI: Vision Chief
- Checklist: `checklists/okr-quality.md`
- Quality gate: OGSM alignment check
  - [ ] Cada Objective de empresa mapeia para pelo menos 1 Goal do OGSM
  - [ ] Cada Strategy do OGSM tem pelo menos 1 OKR que a sustenta
  - [ ] Não há Goals sem OKR correspondente
  - [ ] Não há OKRs "órfãos" (sem conexão com OGSM)
- Output: Matriz OGSM-OKR aprovada

### FASE 3: Cascata para Áreas (Semana 3)

**Step 3.1 — Workshop de Cascata**

- DRI: COO Orchestrator
- Participantes: Todos os C-Level
- Duração: 3-4 horas
- Framework: `frameworks/coo-orchestrator/coo-execution-engine.md`
- Processo:
  1. COO apresenta OKRs de empresa aprovados
  2. Cada agente recebe 30 min para definir OKRs da sua área
  3. Regras de cascata:
     - Cada OKR de área deve contribuir para pelo menos 1 OKR de empresa
     - Máximo 3 Objectives por área
     - Cada área identifica dependências cross-area
  4. Apresentação round-robin: cada agente apresenta seus OKRs
  5. Grupo valida alinhamento e identifica gaps

**Step 3.2 — OKRs por Área**

Cada agente define seus OKRs seguindo a estrutura:

**CMO Architect — Growth & GTM OKRs**
- Framework: `frameworks/cmo-architect/cmo-positioning-to-performance.md`
- Foco: Revenue, CAC, LTV, activation, retention
- Dependências: CTO (plataforma), CIO (dados), CAIO (IA para growth)

**CTO Architect — Tech & Platform OKRs**
- Framework: `frameworks/cto-architect/cto-architecture-as-strategy.md`
- Foco: DORA metrics, reliability, developer experience
- Dependências: CIO (integrações), CAIO (AI infra)

**CIO Engineer — IT & Data OKRs**
- Framework: `frameworks/cio-engineer/cio-data-as-product.md`
- Foco: System availability, data quality, integration health
- Dependências: CTO (arquitetura), CAIO (data pipelines)

**CAIO Architect — AI & Automation OKRs**
- Framework: `frameworks/caio-architect/caio-ai-portfolio-strategy.md`
- Foco: AI use case ROI, adoption rate, quality score
- Dependências: CTO (infra), CIO (dados), CMO (use cases)

**COO Orchestrator — Operations OKRs**
- Framework: `frameworks/coo-orchestrator/coo-operating-rhythm.md`
- Foco: Initiative completion, decision lead time, cadência health
- Dependências: Todos (accountability cross-funcional)

**Step 3.3 — Mapeamento de Dependências**

- DRI: COO Orchestrator
- Processo:
  1. Criar matriz de dependências: OKR x OKR
  2. Identificar dependências críticas (blocking)
  3. Definir SLAs para dependências cross-area
  4. Documentar em `data/registries/initiative-registry.yaml`
- **Decision Point**: Há dependências circulares ou impossíveis?
  - **SIM** → Resolver antes de avançar (redesenhar OKRs ou definir sequência)
  - **NÃO** → Avançar para Fase 4

**Step 3.4 — Mapeamento para Squads**

- DRI: COO Orchestrator
- Ação: Para cada OKR de área, identificar quais squads contribuem
- Referência: `config.yaml` → seção `cross_squad`
- Output: Tabela OKR → Squad(s) → Contribuição esperada

### FASE 4: Aprovação e Ativação (Semana 4)

**Step 4.1 — Sessão de Aprovação**

- DRI: Vision Chief
- Participantes: Todos C-Level + CFO Strategist
- Duração: 2 horas
- Agenda:
  1. Apresentação do pacote completo: OGSM → OKRs empresa → OKRs área
  2. CFO valida viabilidade financeira
  3. Revisão de dependências e riscos
  4. Ajustes finais
  5. Aprovação formal (Vision Chief)
- Checklist: `checklists/quarterly-planning-quality.md`
- **Decision Point**: Pacote aprovado?
  - **SIM** → Ativar OKRs
  - **NÃO** → Identificar bloqueios, resolver, reconvocar em 48h

**Step 4.2 — Registro e Ativação**

- DRI: Squad Coordinator
- Processo:
  1. Registrar todos os OKRs em `data/registries/okr-registry.yaml`
  2. Atualizar `data/registries/initiative-registry.yaml` com iniciativas derivadas
  3. Atualizar `data/registries/metric-registry.yaml` com novas métricas
  4. Configurar tracking semanal para KRs
- Template: `templates/strategy/quarterly-plan.md`

**Step 4.3 — Comunicação e Cascade**

- DRI: Vision Chief + COO Orchestrator
- Processo:
  1. Vision Chief comunica OKRs de empresa para organização
  2. Cada C-Level comunica OKRs da área para seus times
  3. COO garante que todos os squads receberam seus OKRs
  4. Deadline para squads definirem OKRs derivados: 1 semana
- Template: `templates/strategy/quarterly-plan.md`

**Step 4.4 — Setup de Tracking**

- DRI: COO Orchestrator + CIO Engineer
- Processo:
  1. Configurar dashboard de OKRs (semanal)
  2. Definir cadência de check-in por KR
  3. Definir alertas para KRs off-track
  4. Integrar com WBR metrics pack
- Output: Sistema de tracking ativo

---

## Quality Gates

### Gate 1: Qualidade dos OKRs (por OKR)

Aplicar `checklists/okr-quality.md`:

- [ ] Objective é qualitativo e inspiracional
- [ ] Objective é desafiador mas não impossível
- [ ] Key Results são mensuráveis (número, %, data)
- [ ] Key Results têm baseline documentado
- [ ] Key Results têm target e stretch target
- [ ] Cada KR tem DRI único designado
- [ ] Atingir todos os KRs = atingir o Objective
- [ ] Ambição calibrada: 70% atingimento = sucesso
- [ ] Não há mais de 5 Objectives por nível
- [ ] Não há mais de 5 KRs por Objective

### Gate 2: Alinhamento OGSM

- [ ] Cada Objective empresa → pelo menos 1 Goal OGSM
- [ ] Cada Strategy OGSM → pelo menos 1 OKR sustentando
- [ ] NSM refletida em pelo menos 1 KR top-level
- [ ] Cada bet ativo → pelo menos 1 Objective ou KR
- [ ] Kill list respeitada: nenhum OKR sobre item matado

### Gate 3: Cascata e Dependências

- [ ] Cada OKR de área → pelo menos 1 OKR de empresa
- [ ] Dependências mapeadas e SLAs definidos
- [ ] Nenhuma dependência circular
- [ ] Cada squad tem pelo menos 1 OKR contribuindo
- [ ] CFO validou viabilidade financeira

### Gate 4: Prontidão de Tracking

- [ ] Todos os KRs têm método de medição definido
- [ ] Baseline disponível para todos os KRs
- [ ] Dashboard configurado
- [ ] Cadência de check-in definida
- [ ] Alertas configurados para off-track

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| OGSM de empresa | Markdown | `data/memos/` | Vision Chief |
| OKRs de empresa (3-5) | YAML | `data/registries/okr-registry.yaml` | Vision Chief |
| OKRs por área (3 por área) | YAML | `data/registries/okr-registry.yaml` | C-Level respectivo |
| Matriz de dependências | Markdown | `data/memos/` | COO |
| Mapa OKR → Squad | Markdown | `data/memos/` | COO |
| Comunicação de OKRs | Markdown | `data/memos/` | Vision Chief |
| Dashboard de tracking | Config | `data/registries/metric-registry.yaml` | CIO |
| Quarterly Plan | Markdown | `templates/strategy/quarterly-plan.md` | Vision Chief |

---

## Registries Atualizados

- `data/registries/okr-registry.yaml` — Todos os OKRs do trimestre (empresa + área)
- `data/registries/initiative-registry.yaml` — Iniciativas derivadas dos OKRs
- `data/registries/metric-registry.yaml` — Novas métricas e KRs para tracking
- `data/registries/decision-registry.yaml` — Decisões de priorização e trade-offs
- `data/registries/risk-registry.yaml` — Riscos identificados durante o processo

---

## Próximos Passos

1. **Imediato**: Iniciar tracking semanal via WBR → `workflows/04-wbr-loop.md`
2. **Semana 1-2**: Converter OKRs em roadmaps → `workflows/02-bets-to-roadmaps.md`
3. **Mensal**: Revisar progresso de OKRs no MBR → `workflows/05-mbr-loop.md`
4. **Fim do trimestre**: Scoring de OKRs no QBR → `workflows/06-qbr-loop.md`
5. **Se bet muda**: Re-alinhar OKRs via sessão extraordinária

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| Vision Chief | Todos C-Level | OKRs de empresa aprovados | Dia da aprovação |
| Cada C-Level | Squads respectivos | OKRs de área + contribuição esperada | 48h após aprovação |
| COO | Data Squad | Metric definitions para tracking | 48h |
| COO | Todos squads | Matriz de dependências e SLAs | 1 semana |
| CMO | Traffic Squad | Growth OKRs e budget allocation | 48h |
| CMO | Brand Squad | Positioning e awareness OKRs | 48h |
| CTO | Design Squad | Product e UX OKRs | 48h |
| CIO | Data Squad | Data quality e governance OKRs | 48h |
| CIO | Cybersecurity | Compliance e security OKRs | 48h |

### Protocolo de Cascade para Squads

Cada squad recebe:
1. OKRs de empresa relevantes para seu domínio
2. OKRs de área do seu C-Level owner
3. Dependências que precisa entregar
4. SLAs e deadlines
5. Prazo de 1 semana para definir OKRs derivados e retornar para validação

```yaml
cascade_handoff:
  from: c-level-area
  to: squad
  input: "OKRs de área + contribuição esperada"
  format: "YAML (okr-template)"
  dod: "OKRs derivados do squad aprovados pelo C-Level owner"
  dor: "Squad tem dados e contexto para definir OKRs"
  sla: "1 semana para retorno"
  owner: "C-Level owner da área"
  escalation: "COO Orchestrator"
```
