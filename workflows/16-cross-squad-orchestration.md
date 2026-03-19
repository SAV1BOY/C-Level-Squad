# Workflow 16 — Cross-Squad Orchestration

> **Orquestrar trabalho que envolve múltiplos squads, garantindo handoffs limpos, SLAs cumpridos e qualidade end-to-end.**
> Quando o trabalho cruza fronteiras de squad, a orquestração explícita é a diferença entre entrega e caos.

---

## Objetivo

Estabelecer o processo formal de orquestração de trabalho cross-squad no C-Level Squad. Quando uma iniciativa requer contribuição de múltiplos squads (Brand, Copy, Story, Movement, Traffic, Design, Data, Cyber, Advisory), este workflow garante que:

1. **Contratos de handoff são explícitos** — DoD e DoR definidos antes de iniciar
2. **SLAs são monitorados ativamente** — não post-mortem
3. **Dependências são mapeadas** — critical path identificado
4. **Qualidade é validada em cada transição** — gate de handoff rigoroso
5. **Escalations são automáticos** — não dependem de boa vontade

> **Princípio:** Cross-squad sem contrato é promessa sem compromisso. O contrato transforma intenção em execução.

---

## Agentes Envolvidos

| Agente | Papel no Workflow |
|--------|-------------------|
| **COO Orchestrator** | Lead — coordena cross-squad, monitora SLAs, intervém em bloqueios |
| **Vision Chief (CEO)** | Reviewer — aprovação de iniciativas cross-squad estratégicas |
| **CMO Architect** | Support — squads de marketing (Brand, Copy, Movement, Traffic) |
| **CTO Architect** | Support — squads técnicos (Design, engenharia) |
| **CIO Engineer** | Support — squads de dados (Data, Cyber) |
| **CAIO Architect** | Support — AI capabilities cross-squad |
| **CFO Strategist** | Support — budget allocation cross-squad |
| **Squad Coordinator** | Logística — tracking, meeting prep, status consolidation |

---

## Trigger (quando iniciar)

### Triggers Primários
- Projeto ou iniciativa identificada que requer 2+ squads
- Handoff request formal de um squad para outro
- Strategic bet que gera demanda cross-squad
- Board deliverable que requer input de múltiplos squads

### Triggers de Escalation
- SLA de handoff expirado sem entrega
- Conflito de prioridade entre squads
- Qualidade de handoff rejeitada (DoR não atendido)
- Recurso compartilhado com conflito de alocação

---

## Pré-condições

- [ ] RASI/DRI framework ativo (`frameworks/operating-system/rasi-dri.md`)
- [ ] Escalation ladders definidas (`frameworks/operating-system/escalation-ladders.md`)
- [ ] Cross-squad registry inicializado (`data/registries/cross-squad-registry.yaml`)
- [ ] Squad leads identificados e disponíveis
- [ ] Budget alocado para a iniciativa (se aplicável)

---

## Processo (step-by-step)

### Stage 1: Request e Scoping (1-2 dias)

**Owner**: Squad de origem + COO Orchestrator

1. **Submeter Cross-Squad Request**
   - Preencher template: `templates/cross-squad/cross-squad-briefing.md`
   - Definir: o que precisa, de quem, quando, por quê
   - Classificar urgência: critical / high / normal / low

2. **Scoping pelo COO**
   - Verificar se é realmente cross-squad ou pode ser resolvido internamente
   - Identificar todos os squads necessários
   - Mapear dependências entre squads (sequencial vs paralelo)
   - Estimar timeline total

3. **Registro**
   - Atualizar `data/registries/cross-squad-registry.yaml`
   - Status: `requested`
   - Atribuir ID único

### Stage 2: Squad Alignment (1-2 dias)

**Owner**: COO Orchestrator

1. **Kickoff Meeting**
   - Reunir leads de todos os squads envolvidos
   - Apresentar scope, timeline, urgência
   - Obter commitment de cada squad (ou negociar timeline)
   - Identificar riscos e dependências

2. **Priority Alignment**
   - Verificar se o trabalho cabe no capacity de cada squad
   - Se conflito de prioridade → escalation para Vision Chief
   - Se timeline não viável → negociar scope ou sequencing

3. **Assign DRIs**
   - DRI global da iniciativa: COO Orchestrator (ou Chief do squad de origem)
   - DRI por squad: lead de cada squad envolvido
   - DRI por handoff: owner da transição entre cada par de squads

### Stage 3: Contract Definition (1-2 dias)

**Owner**: COO Orchestrator + Squad leads

1. **Definir Contrato de Handoff para Cada Transição**
   ```yaml
   handoff:
     from: [squad de origem]
     to: [squad de destino]
     input: [o que está sendo entregue]
     format: [template/formato esperado]
     dod: [Definition of Done — quando o input está "pronto"]
     dor: [Definition of Ready — quando o destino está "pronto para receber"]
     sla: [prazo máximo para entrega]
     owner: [DRI do handoff]
     escalation: [o que fazer se SLA estourar]
   ```

2. **SLA Table**
   | Squad | Tipo de Handoff | SLA Padrão |
   |-------|----------------|-----------|
   | Brand | Briefing estratégico → brand guidelines | 5 dias |
   | Copy | Positioning → messaging framework | 3 dias |
   | Story | Narrativa estratégica → content plan | 5 dias |
   | Movement | Community strategy → execution plan | 5 dias |
   | Traffic | Growth targets → acquisition plan | 3 dias |
   | Design | Product requirements → UX/UI specs | 5 dias |
   | Data | Metrics definition → dashboards | 3 dias |
   | Cyber | Security requirements → compliance report | 5 dias |
   | Advisory | Strategic question → advisory brief | 10 dias |

3. **Quality Checklist por Handoff**
   - Aplicar `checklists/cross-squad-handoff-quality.md` para cada transição
   - Customizar se necessário para o caso específico

### Stage 4: Execution Tracking (duração da iniciativa)

**Owner**: COO Orchestrator + Squad Coordinator

1. **Status Tracking**
   - Squad Coordinator coleta status diário/semanal de cada squad
   - Dashboard consolidado de progresso
   - Milestone tracking contra timeline definido

2. **Dependency Monitoring**
   - Verificar se squads upstream estão on-track
   - Se bloqueio detectado → alert imediato para COO
   - Se SLA em risco → warning 48h antes do deadline

3. **Communication Cadence**
   - Standup cross-squad: 15min, 2-3x por semana para iniciativas critical
   - Standup cross-squad: 15min, 1x por semana para iniciativas normal
   - Status report consolidado: semanal para COO

4. **Issue Resolution**
   - Bloqueios resolvidos pelo COO em < 24h
   - Se COO não resolve → escalation para Vision Chief
   - Decisões de priorização documentadas no decision registry

### Stage 5: Handoff Validation (por transição)

**Owner**: DRI do handoff

1. **DoD Check (squad de origem)**
   - Squad de origem confirma que output atende DoD
   - Self-review contra checklist de qualidade
   - Entrega formal ao squad de destino

2. **DoR Check (squad de destino)**
   - Squad de destino revisa output contra DoR
   - Se atende → aceita e inicia trabalho
   - Se não atende → documenta gaps específicos

3. **Aplicar Gate de Handoff**
   - `checklists/cross-squad-handoff-quality.md`
   - Todos os critérios devem passar
   - Se falha → retorna ao squad de origem

4. **Rejeição e Rework**
   - Se rejeitado: feedback específico documentado
   - SLA de correção = 50% do SLA original
   - Se segunda rejeição → COO intervém diretamente
   - Se terceira rejeição → Vision Chief intervém

### Stage 6: Integration Check (1-2 dias)

**Owner**: COO Orchestrator

1. **Verificar Output Consolidado**
   - Todas as peças entregues por todos os squads
   - Outputs são consistentes entre si
   - Narrativa/mensagem é coerente end-to-end

2. **Quality Check Final**
   - `checklists/exec-decision-memo-quality.md` (se output vai para board)
   - Cross-check de dados entre squads
   - Visual consistency (se aplicável)

3. **Stakeholder Preview**
   - Apresentar output consolidado ao requestor
   - Feedback loop final antes de closure
   - Ajustes menores se necessário (< 2 dias)

### Stage 7: Closure (1 dia)

**Owner**: COO Orchestrator + Squad Coordinator

1. **Registrar Conclusão**
   - Atualizar `data/registries/cross-squad-registry.yaml`: status `completed`
   - Documentar timeline real vs planejado
   - Documentar issues encontrados e como foram resolvidos

2. **Feedback Collection**
   - Mini-retro com squad leads: o que funcionou? o que melhorar?
   - Ratings de handoff quality por transição
   - Registrar em `data/registries/lessons-learned.yaml`

3. **Process Improvement**
   - Se padrão de problema identificado → ajustar SLAs ou checklists
   - Se nova best practice identificada → documentar em playbook
   - Feed para RalphLoop

---

## Quality Gates

### Gate 1: Scoping → Execution
- [ ] Todos os squads confirmaram commitment
- [ ] Contratos de handoff definidos para cada transição
- [ ] DRIs atribuídos
- [ ] Timeline aceito por todos

### Gate 2: Handoff (por transição)
- [ ] `checklists/cross-squad-handoff-quality.md` — PASS ✅
- [ ] DoD atendido pelo squad de origem
- [ ] DoR confirmado pelo squad de destino
- [ ] SLA cumprido (ou escalation documentado)

### Gate 3: Closure
- [ ] Todos os handoffs completados
- [ ] Output consolidado revisado pelo COO
- [ ] Feedback coletado
- [ ] Registries atualizados

---

## Outputs

| Output | Template | Destino |
|--------|----------|---------|
| Cross-Squad Briefing | `templates/cross-squad/cross-squad-briefing.md` | Registry |
| Handoff Contracts | (inline por transição) | Squad leads |
| Status Reports | Dashboard consolidado | COO, Vision Chief |
| Retro/Lessons | `data/registries/lessons-learned.yaml` | All squads |

---

## Registries Atualizados

| Registry | Quando Atualizar |
|----------|-----------------|
| `data/registries/cross-squad-registry.yaml` | Cada stage transition |
| `data/registries/decision-registry.yaml` | Decisões de priorização |
| `data/registries/lessons-learned.yaml` | Closure retro |

---

## Cross-Squad Handoffs

Este workflow É o workflow de handoff. Todos os 9 squads integrados participam:

| Squad | Capabilities |
|-------|-------------|
| **Brand** | Brand guidelines, visual identity, brand strategy |
| **Copy** | Messaging, copywriting, tone of voice |
| **Story** | Narrativa, content strategy, storytelling |
| **Movement** | Community, engagement, advocacy |
| **Traffic** | Acquisition, paid media, growth |
| **Design** | UX/UI, product design, user research |
| **Data** | Analytics, dashboards, data engineering |
| **Cyber** | Security, compliance, risk |
| **Advisory** | Strategic advice, industry expertise |

---

## Escalation Path

```
Nível 1: DRI do handoff resolve diretamente (< 24h)
    ↓ se não resolver
Nível 2: COO Orchestrator intervém (< 24h)
    ↓ se não resolver
Nível 3: Vision Chief decide (< 24h)
    ↓ se recurso/budget necessário
Nível 4: CFO + Vision Chief alocam recursos
```

---

## Referências Cruzadas

### Frameworks
- `frameworks/operating-system/rasi-dri.md` — Modelo de responsabilidades
- `frameworks/operating-system/escalation-ladders.md` — Escalonamento
- `frameworks/operating-system/wbr-mbr-qbr.md` — Cadências de revisão

### Checklists
- `checklists/cross-squad-handoff-quality.md` — Gate de handoff
- `checklists/coo/coo-execution-rhythm-audit.md` — Ritmo de execução
- `checklists/exec-decision-memo-quality.md` — Decisões formais

### Templates
- `templates/cross-squad/cross-squad-briefing.md` — Briefing cross-squad

### Workflows Relacionados
- `workflows/04-wbr-loop.md` — Status tracking semanal
- `workflows/11-incident-response-exec.md` — Se handoff failure causa incidente
- `workflows/20-postmortem-and-learning.md` — Postmortem de falhas cross-squad
