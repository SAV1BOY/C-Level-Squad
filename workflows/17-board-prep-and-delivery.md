# Workflow 17 — Board Prep and Delivery

> **Preparar, revisar e entregar materiais de board meeting com qualidade GOLD/SOTA.**
> Board materials são a face externa do squad. Qualidade abaixo de GOLD não é aceitável.

---

## Objetivo

Estabelecer o processo completo de preparação e entrega de materiais para board meetings, investor updates e stakeholder presentations. O workflow garante que:

1. **Narrativa é consistente** — uma história coerente, não slides desconectados
2. **Dados são verificados** — todo número tem fonte e é auditável
3. **Design é profissional** — visual que transmite competência
4. **Dry run é obrigatório** — ninguém apresenta sem ensaiar
5. **Follow-up é rastreado** — action items do board não se perdem

> **Princípio:** Board meeting é performance. Preparação define resultado.

---

## Agentes Envolvidos

| Agente | Papel no Workflow |
|--------|-------------------|
| **Vision Chief (CEO)** | Lead — narrativa estratégica, apresentação final, approvals |
| **CFO Strategist** | Support — financial narrative, unit economics, projections |
| **COO Orchestrator** | Support — operational metrics, execution status |
| **CMO Architect** | Support — growth metrics, market positioning |
| **CTO Architect** | Support — technology roadmap, platform health |
| **CIO Engineer** | Support — data infrastructure, systems status |
| **CAIO Architect** | Support — AI portfolio status, innovation pipeline |
| **Squad Coordinator** | Logística — timeline management, data collection, deck assembly |

---

## Trigger (quando iniciar)

### Triggers Primários
- Board meeting agendado (tipicamente T-30 dias)
- Investor update solicitado
- Annual planning presentation
- Request especial do board/investidores

### Timeline Padrão
```
T-30: Kickoff
T-25: Data collection complete
T-20: Section drafts ready
T-15: First integrated draft
T-10: Financial review + fact check
T-7:  Design polish
T-3:  Dry run
T-1:  Final approval
T-0:  Delivery
T+3:  Follow-up memo
```

---

## Pré-condições

- [ ] Board meeting date confirmada
- [ ] Agenda/tópicos definidos (pelo board ou Vision Chief)
- [ ] Dados operacionais do período disponíveis
- [ ] Financials fechados e auditados pelo CFO
- [ ] Templates de apresentação atualizados

---

## Processo (step-by-step)

### Stage 1: Kickoff e Timeline (T-30, 1 dia)

**Owner**: Vision Chief + Squad Coordinator

1. **Definir Agenda**
   - Confirmar tópicos requeridos pelo board
   - Adicionar tópicos proativos (oportunidades, riscos)
   - Definir tempo por seção

2. **Atribuir Seções**
   - Cada seção tem um agente DRI
   - Típica distribuição:
     - Strategy & Vision → Vision Chief
     - Financials → CFO Strategist
     - Operations → COO Orchestrator
     - Growth/Market → CMO Architect
     - Technology → CTO Architect
     - AI/Innovation → CAIO Architect
     - Systems/Data → CIO Engineer

3. **Definir Timeline**
   - Milestones com deadlines
   - Buffer para revisão e rework
   - Dry run date locked

4. **Kickoff Communication**
   - Squad Coordinator envia briefing para todos os agentes
   - Template: `templates/finance/investor-deck-template.md`
   - Data requests para cada agente

### Stage 2: Data Collection (T-25, 5 dias)

**Owner**: Squad Coordinator + cada agente

1. **Cada Agente Coleta Dados da Sua Seção**
   - Métricas do período (from dashboards/registries)
   - Highlights e lowlights
   - Comparação vs targets/OKRs
   - Forward-looking projections

2. **CFO Consolida Financials**
   - P&L, cash flow, balance sheet highlights
   - Unit economics atualizado
   - Runway e burn rate
   - Budget vs actual variance

3. **Data Quality Check**
   - CIO valida integridade dos dados
   - CFO valida números financeiros
   - Fontes documentadas para cada métrica
   - Inconsistências resolvidas antes de prosseguir

### Stage 3: Section Drafting (T-20, 5 dias)

**Owner**: Cada agente (sua seção)

1. **Cada Agente Prepara Sua Seção**
   - Seguir template padrão
   - Máximo de slides definido por seção
   - Formato: insight → evidência → implicação → next step
   - Sem bullet point walls — dados visuais preferred

2. **Narrative Guidelines**
   - Honest but confident
   - Data-driven, not opinion-driven
   - Forward-looking, not just backward-reporting
   - Risks acknowledgeados com planos de mitigação

3. **Self-Review**
   - Cada agente aplica `checklists/exec-decision-memo-quality.md` à sua seção
   - Fact-check: todo número tem fonte?
   - So-what test: cada slide responde "e daí?"

### Stage 4: Narrative Integration (T-15, 2 dias)

**Owner**: Vision Chief

1. **Integrar Seções**
   - Vision Chief revisa todas as seções
   - Verifica consistência de narrativa
   - Elimina contradições entre seções
   - Cria intro e conclusão que conectam tudo

2. **Red Thread**
   - Qual é a história? (ex: "estamos acelerando com disciplina")
   - Cada seção reforça a mesma história?
   - Conclusão amarra tudo?

3. **Feedback para Agentes**
   - Seções que precisam de ajuste → feedback específico
   - SLA de rework: 2 dias
   - Se conflito de narrativa → Vision Chief decide

### Stage 5: Financial Review (T-10, 2 dias)

**Owner**: CFO Strategist

1. **Audit de Números**
   - Todo número financeiro é verificado contra fonte
   - Projeções têm assumptions documentadas
   - Variance analysis para desvios > 10%
   - Unit economics consistente entre seções

2. **Aplicar Checklist**
   - `checklists/finance/financial-health-audit.md`
   - Nenhum número sem fonte
   - Nenhuma projeção sem assumption
   - Cenários pessimista/base/otimista se relevante

3. **Sign-off do CFO**
   - CFO assina que todos os números financeiros são corretos
   - Se discorda de qualquer projeção → resolve com Vision Chief

### Stage 6: Design Polish (T-7, 3 dias)

**Owner**: Squad Coordinator + Design squad

1. **Cross-Squad Handoff**
   - Briefing para Design squad (se disponível)
   - SLA: 3 dias para polish visual
   - `checklists/cross-squad-handoff-quality.md`

2. **Visual Standards**
   - Consistency de cores, fontes, layouts
   - Gráficos legíveis e com labels claros
   - Sem typos ou inconsistências visuais
   - Appendix organizado e referenciado

3. **Version Control**
   - Draft numerado (v1, v2, v3...)
   - Cada mudança é trackada
   - Version final locked antes do dry run

### Stage 7: Dry Run (T-3, 1 dia)

**Owner**: Vision Chief + todos os agentes

1. **Rehearsal Completo**
   - Apresentação full-length com timer
   - Cada agente apresenta sua seção
   - Audiência: todos os agentes (peer review)

2. **Q&A Simulation**
   - Agentes fazem perguntas difíceis que o board faria
   - CFO desafia números
   - COO desafia execution claims
   - Vision Chief pratica respostas

3. **Feedback e Ajustes**
   - Timing ajustado (cortar se longo)
   - Slides confusos simplificados
   - Talking points para Q&A documentados
   - Weak points identificados e mitigados

### Stage 8: Final Approval (T-1, 1 dia)

**Owner**: Vision Chief

1. **Review Final**
   - Vision Chief faz review final completo
   - Aplica todos os quality gates
   - Verifica que feedback do dry run foi incorporado

2. **Approval Gate**
   - Vision Chief + CFO sign-off
   - Deck locked — nenhuma mudança após approval
   - Backup plan definido (tech issues, time changes)

3. **Prep Final**
   - Deck distribuído para o board (se protocol exigir)
   - Notes de apresentação finalizadas
   - Tech check (projetor, conexão, backup PDF)

### Stage 9: Delivery (T-0)

**Owner**: Vision Chief

1. **Apresentação**
   - Vision Chief lidera apresentação
   - Agentes disponíveis para deep-dive questions
   - Time management rigoroso
   - Notes de action items em real-time

2. **Q&A Management**
   - Perguntas direcionadas ao agente especialista
   - "Vou verificar e enviar follow-up" para perguntas sem resposta imediata
   - Nunca inventar ou especular com números

### Stage 10: Follow-up (T+3, 2 dias)

**Owner**: Squad Coordinator + Vision Chief

1. **Follow-up Memo**
   - Consolidar action items do board meeting
   - Atribuir DRI e deadline para cada item
   - Enviar para board em < 3 dias

2. **Feedback do Board**
   - Coletar feedback sobre a apresentação
   - Identificar tópicos para aprofundar
   - Registrar em `data/registries/lessons-learned.yaml`

3. **Registrar**
   - Atualizar `data/registries/decision-registry.yaml` com decisões do board
   - Arquivo do deck em `data/meeting-minutes/`
   - Update status dos action items no tracking

---

## Quality Gates

### Gate 1: Data Quality (T-25)
- [ ] Todos os dados coletados com fontes documentadas
- [ ] Financials validados pelo CFO
- [ ] Inconsistências entre seções resolvidas

### Gate 2: Narrative Quality (T-15)
- [ ] Red thread consistente
- [ ] `checklists/exec-decision-memo-quality.md` — PASS ✅
- [ ] Cada seção responde "so what?"

### Gate 3: Dry Run (T-3)
- [ ] Dry run executado com todos os agentes
- [ ] Timing dentro do limite
- [ ] Q&A preparado para perguntas difíceis
- [ ] Feedback incorporado

### Gate 4: Final Approval (T-1)
- [ ] Vision Chief + CFO sign-off
- [ ] Nível GOLD/SOTA de qualidade
- [ ] Zero números sem fonte
- [ ] Zero inconsistências

---

## Outputs

| Output | Template | Destino |
|--------|----------|---------|
| Board Deck | `templates/finance/investor-deck-template.md` | Board |
| Follow-up Memo | (inline) | Board |
| Action Items | (inline) | COO tracking |
| Meeting Notes | (inline) | `data/meeting-minutes/` |

---

## Registries Atualizados

| Registry | Quando Atualizar |
|----------|-----------------|
| `data/registries/decision-registry.yaml` | Decisões do board |
| `data/registries/lessons-learned.yaml` | Post-meeting retro |
| `data/registries/okr-registry.yaml` | Se OKRs ajustados |

---

## Cross-Squad Handoffs

| Squad | Tipo | SLA | Owner |
|-------|------|-----|-------|
| Story | Narrativa estratégica → content support | 5 dias | Vision Chief |
| Design | Deck content → visual polish | 3 dias | Squad Coordinator |
| Data | Metrics validation → verified dashboards | 3 dias | CIO |

---

## Referências Cruzadas

### Frameworks
- `frameworks/operating-system/decision-memo-framework.md` — Formato de decisão
- `frameworks/cfo-strategist/financial-modeling.md` — Projeções financeiras
- `frameworks/operating-system/wbr-mbr-qbr.md` — Dados de cadências

### Checklists
- `checklists/exec-decision-memo-quality.md` — Quality gate universal
- `checklists/finance/financial-health-audit.md` — Validação financeira

### Templates
- `templates/finance/investor-deck-template.md` — Template base do deck
- `templates/coo/operating-review-template.md` — Seção operacional

### Workflows Relacionados
- `workflows/06-qbr-loop.md` — QBR alimenta dados do board prep
- `workflows/13-stakeholder-comms.md` — Comunicação com stakeholders
- `workflows/18-decision-quality-review.md` — Review de decisões do board
