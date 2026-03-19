# Workflow 20 — Postmortem and Learning Loop

> **Conduzir postmortems blameless após incidentes, falhas de projeto ou decisões que não performaram.**
> Organizações que aprendem vencem. Postmortem é o mecanismo de aprendizado.

---

## Objetivo

Estabelecer o processo completo de postmortem e learning loop para o C-Level Squad. O workflow garante que:

1. **Postmortems são blameless** — foco em sistema, não em pessoas
2. **Root cause é genuíno** — 5 Whys mínimo, não superficial
3. **Action items são executados** — não apenas listados
4. **Aprendizados são distribuídos** — toda a organização se beneficia
5. **Processos são ajustados** — o sistema melhora com cada postmortem

> **Princípio:** Errar é humano. Não aprender com o erro é organizacional. O postmortem transforma erro em evolução.

---

## Agentes Envolvidos

| Agente | Papel no Workflow |
|--------|-------------------|
| **COO Orchestrator** | Lead — facilita postmortem, garante follow-up de action items |
| **Vision Chief (CEO)** | Reviewer — incidentes estratégicos, decisões de investimento em prevenção |
| **CTO Architect** | Support — incidentes técnicos, falhas de plataforma |
| **CIO Engineer** | Support — incidentes de dados, sistemas, integração |
| **CAIO Architect** | Support — incidentes de IA, modelo failures |
| **CMO Architect** | Support — incidentes de marca, comunicação, mercado |
| **CFO Strategist** | Support — impacto financeiro, custo de incidentes |
| **Squad Coordinator** | Logística — scheduling, documentação, tracking |

---

## Trigger (quando iniciar)

### Triggers Obrigatórios
- Incidente de produção com severity ≥ P2 (resolvido)
- Projeto cancelado ou que falhou em entregar > 50% do escopo
- Decisão Type 1 com outcome MISS
- Perda de cliente estratégico
- Breach de segurança ou compliance
- Incidente cultural grave

### Triggers Recomendados
- Incidente P3 com pattern recorrente (3+ ocorrências)
- Projeto entregue com atraso > 50% do timeline original
- Decisão Type 2 com outcome MISS e impacto significativo
- Near-miss que poderia ter sido grave
- Sucesso significativo (postmortem positivo — o que deu certo?)

### Timeline para Iniciar
- P1/P2 incidents: iniciar em < 48h após resolução
- Project failures: iniciar em < 1 semana
- Decision reviews: integrado ao Workflow 18

---

## Pré-condições

- [ ] Incidente/falha resolvido (não fazer postmortem durante a crise)
- [ ] Timeline de eventos coletada (logs, comunicações, ações)
- [ ] Pessoas-chave envolvidas disponíveis para participar
- [ ] Espaço blameless estabelecido (cultura de segurança psicológica)
- [ ] Facilitador designado (preferencialmente alguém não diretamente envolvido)

---

## Processo (step-by-step)

### Stage 1: Postmortem Kickoff (1 dia)

**Owner**: COO Orchestrator

1. **Designar Facilitador**
   - Preferencialmente: COO ou agente não envolvido diretamente
   - Nunca: a pessoa mais senior envolvida (pode inibir honestidade)
   - Treinado em facilitação blameless

2. **Identificar Participantes**
   - Todos os envolvidos diretamente no incidente
   - Agentes afetados (squads, stakeholders)
   - Observer: alguém de fora para perspectiva externa

3. **Schedule Session**
   - Duração: 60-90 minutos
   - Prep: 30 min de leitura prévia
   - Formato: presencial preferred, remoto se necessário

4. **Prep Materials**
   - Timeline preliminar de eventos
   - Métricas de impacto
   - Contexto do incidente/falha
   - Ground rules blameless

### Stage 2: Timeline Reconstruction (durante a session, 20-30 min)

**Owner**: Facilitador

1. **Blameless Ground Rules**
   ```
   ┌──────────────────────────────────────────────────┐
   │           BLAMELESS POSTMORTEM RULES               │
   │                                                    │
   │ 1. Foco em sistema, não em pessoas                │
   │ 2. "Quem" fez é irrelevante; "por quê" aconteceu │
   │    é o que importa                                 │
   │ 3. Todos têm as melhores intenções                │
   │ 4. O ambiente permitiu que acontecesse             │
   │ 5. A pergunta é: como evitar que o SISTEMA         │
   │    permita novamente?                              │
   └──────────────────────────────────────────────────┘
   ```

2. **Reconstruir Timeline**
   - Cronológico: o que aconteceu, quando, por quem
   - Fatos, não interpretações (ainda)
   - Incluir: decisões tomadas, informações disponíveis, ações executadas
   - Identificar pontos de inflexão (moments where path changed)

3. **Documentar em Formato Structured**
   ```
   [TIMESTAMP] [EVENTO] [CONTEXTO] [DECISÃO/AÇÃO]
   ```

### Stage 3: Root Cause Analysis (durante a session, 20-30 min)

**Owner**: Facilitador + todos os participantes

1. **5 Whys**
   - Começar com o incidente/falha
   - Perguntar "por quê?" pelo menos 5 vezes
   - Cada "por quê?" deve ir mais fundo, não lateral
   - Parar quando chegar em algo que pode ser mudado

2. **Fishbone Diagram (Ishikawa)**
   - Categorias: People, Process, Technology, Information, Environment, Management
   - Para cada categoria: quais fatores contribuíram?
   - Identificar contributing factors vs root causes

3. **Classificar Root Causes**
   | Tipo | Exemplo | Ação Típica |
   |------|---------|-------------|
   | Process | Faltava checklist | Criar/atualizar checklist |
   | Technology | Sem monitoring | Implementar alertas |
   | Information | Dados incorretos | Melhorar data quality |
   | Communication | Escalation tardio | Ajustar escalation path |
   | Design | Single point of failure | Adicionar redundância |
   | External | Vendor outage | Diversificar vendors |

4. **Depth Check**
   - Root cause tem pelo menos 3 níveis de profundidade?
   - É acionável? (pode fazer algo sobre isso?)
   - É sistêmico? (afeta mais do que este caso?)

### Stage 4: Impact Assessment (10-15 min)

**Owner**: CFO Strategist + agentes relevantes

1. **Quantificar Impacto**
   - Financial: receita perdida, custo de resposta, custo de correção
   - Operacional: horas de downtime, tickets gerados, processos afetados
   - Reputacional: clientes afetados, mídia, brand impact
   - Organizacional: morale, trust, cultura

2. **Severity Classification**
   | Severity | Definição | Exemplo |
   |----------|-----------|---------|
   | Critical | Ameaça existencial ao negócio | Breach de dados massivo |
   | High | Impacto financeiro significativo | Outage > 24h em produção |
   | Medium | Impacto operacional significativo | Feature launch falho |
   | Low | Impacto limitado, aprendizado valioso | Near-miss detectado |

### Stage 5: Lessons Extraction (10-15 min)

**Owner**: Facilitador

1. **Para Cada Root Cause**
   - O que aprendemos?
   - O que não sabíamos que não sabíamos?
   - O que faríamos diferente?
   - O que funcionou bem apesar do incidente?

2. **Systemic Lessons**
   - Este tipo de problema pode acontecer em outro lugar?
   - Há padrão com incidentes anteriores?
   - O que este incidente revela sobre nosso sistema?

3. **Positive Lessons (o que deu certo)**
   - Detecção foi rápida?
   - Resposta foi coordenada?
   - Comunicação foi efetiva?
   - Recovery foi eficiente?

### Stage 6: Action Items Definition (15-20 min)

**Owner**: COO Orchestrator

1. **Para Cada Root Cause: Ação Preventiva**
   - Ação específica e mensurável
   - DRI (owner da ação)
   - Deadline (não "quando possível")
   - Critério de conclusão (como saber que está feito?)

2. **Classificar Ações**
   | Tipo | Timeline | Exemplo |
   |------|----------|---------|
   | Imediato | < 1 semana | Adicionar alerta de monitoring |
   | Quick fix | < 1 mês | Atualizar checklist ou processo |
   | Investimento | 1-3 meses | Implementar redundância, re-arquitetar |
   | Cultural | Contínuo | Training, mudança de prática |

3. **Priorizar**
   - Impacto × Esforço matrix
   - Ações que previnem recorrência primeiro
   - Quick wins para demonstrar progresso

### Stage 7: Process Updates (1-2 dias pós-session)

**Owner**: DRIs das ações

1. **Atualizar Documentação**
   - Checklists: adicionar items que teriam prevenido o incidente
   - Runbooks: adicionar scenarios e respostas
   - Frameworks: ajustar se gap de processo identificado
   - Escalation paths: ajustar se escalation foi tardio

2. **Implementar Ações Imediatas**
   - Deploy fixes técnicos
   - Comunicar mudanças de processo
   - Adicionar monitoring/alertas

3. **Registrar no Sistema**
   - Postmortem document finalizado
   - Action items no tracking
   - Lessons no registry

### Stage 8: Knowledge Distribution (1-2 dias)

**Owner**: COO Orchestrator + Squad Coordinator

1. **Postmortem Summary**
   - 1-pager com: o que aconteceu, root cause, lessons, action items
   - Distribuir para todos os agentes
   - Share com squads afetados

2. **Learning Broadcast**
   - Apresentar lessons em WBR (5 min) se relevante
   - Documentar em formato pesquisável para referência futura
   - Se pattern cross-squad: comunicar a todos os squads

3. **Training se Necessário**
   - Se root cause é knowledge gap → organizar training
   - Se root cause é skill gap → programa de desenvolvimento
   - Se root cause é cultural → intervenção via Workflow 19

### Stage 9: Follow-up Verification (30-60 dias depois)

**Owner**: COO Orchestrator

1. **Action Items Tracking**
   - Verificar status de cada action item
   - % de conclusão
   - Se atrasado: por quê? precisa de help?

2. **Effectiveness Check**
   - Incidente similar ocorreu novamente? (recurrence check)
   - Monitoring/alertas estão funcionando?
   - Processo atualizado está sendo seguido?

3. **Close Postmortem**
   - Se todos os action items concluídos e efetivos → close
   - Se incidente recorreu → novo postmortem com deep dive
   - Registrar aprendizado final no `data/registries/lessons-learned.yaml`

---

## Quality Gates

### Gate 1: Postmortem Session
- [ ] Facilitador blameless designado
- [ ] Todos os envolvidos participaram
- [ ] Timeline reconstruída com fatos
- [ ] 5 Whys executado com mínimo 3 níveis de profundidade

### Gate 2: Analysis Quality
- [ ] Root cause analysis completa (5 Whys + Fishbone)
- [ ] Impact assessment quantificado
- [ ] Lessons extraídas (pelo menos 3)
- [ ] Positive lessons incluídas

### Gate 3: Action Items
- [ ] Cada root cause tem ação preventiva
- [ ] Cada ação tem DRI e deadline
- [ ] Ações priorizadas por impacto
- [ ] Quick wins identificados

### Gate 4: Follow-up
- [ ] Action items tracked e verificados em 30 dias
- [ ] Recurrence check executado
- [ ] `checklists/ralphloop-quality.md` — PASS ✅
- [ ] Postmortem closed ou escalado

---

## Outputs

| Output | Template | Destino |
|--------|----------|---------|
| Postmortem Document | `templates/operational/retrospective.md` | All agents |
| Action Items | `templates/operational/action-items-tracker.md` | DRIs |
| Lessons Learned | `data/registries/lessons-learned.yaml` | All squads |
| 1-pager Summary | (custom) | Broad distribution |

---

## Registries Atualizados

| Registry | Quando Atualizar |
|----------|-----------------|
| `data/registries/lessons-learned.yaml` | Post-session + follow-up |
| `data/registries/decision-registry.yaml` | Decisões de investimento em prevenção |
| `data/registries/risk-registry.yaml` | Novos riscos identificados |

---

## Cross-Squad Handoffs

| Squad | Tipo | SLA | Owner |
|-------|------|-----|-------|
| Cyber | Security-related postmortems | 3 dias para participar | CIO |
| Data | Data-related root causes | 3 dias para análise | CIO |
| Qualquer squad afetado | Participação no postmortem | 2 dias para schedule | COO |

---

## Anti-Patterns (o que NÃO fazer)

| Anti-Pattern | Consequência | Correção |
|-------------|-------------|----------|
| Blame session | Pessoas param de reportar | Enforçar blameless rules |
| Shallow RCA | Problema recorre | Exigir 5 Whys mínimo |
| No follow-up | Action items viram teatro | Track com deadline e DRI |
| Only technical | Ignora processo e cultura | Fishbone com todas as categorias |
| Delay postmortem | Memória se perde | Iniciar em < 48h |
| Skip successes | Só aprende com falhas | Incluir positive postmortems |

---

## Referências Cruzadas

### Frameworks
- `frameworks/operating-system/escalation-ladders.md` — Escalonamento de incidentes
- `frameworks/operating-system/decision-memo-framework.md` — Documentar decisões

### Checklists
- `checklists/ralphloop-quality.md` — Quality gate de aprendizado
- `checklists/exec-decision-memo-quality.md` — Para decisões do postmortem

### Templates
- `templates/operational/retrospective.md` — Template de retrospectiva
- `templates/operational/action-items-tracker.md` — Tracker de ações

### Workflows Relacionados
- `workflows/11-incident-response-exec.md` — Resposta ao incidente (precede postmortem)
- `workflows/18-decision-quality-review.md` — Review de decisões
- `workflows/12-risk-review-cycle.md` — Novos riscos alimentam o risk register
- `workflows/19-culture-health-cycle.md` — Incidentes culturais
