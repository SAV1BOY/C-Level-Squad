# Quality Gate Cascade — Sistema de Gates em Cascata

> **Este documento define como os quality gates operam em cascata dentro do C-Level Squad.**
> Cada transição — entre agentes, tasks, workflows e squads — possui um gate explícito.
> Nenhum output avança sem passar pelo gate correspondente.

---

## 1. VISÃO GERAL DO SISTEMA DE GATES

O C-Level Squad opera com **6 camadas de quality gates** em cascata:

```
┌──────────────────────────────────────────────────────┐
│  CAMADA 6: HRM GATE (Central Command / Board)        │
│  → Output final aprovado para stakeholders externos   │
├──────────────────────────────────────────────────────┤
│  CAMADA 5: CROSS-SQUAD GATE                          │
│  → Handoff validado entre squads                      │
├──────────────────────────────────────────────────────┤
│  CAMADA 4: SQUAD GATE (Chief Approval)               │
│  → Vision Chief ou COO aprovam output consolidado     │
├──────────────────────────────────────────────────────┤
│  CAMADA 3: WORKFLOW GATE                             │
│  → Transição entre estágios do workflow validada      │
├──────────────────────────────────────────────────────┤
│  CAMADA 2: TASK GATE                                 │
│  → Output da task validado contra checklist           │
├──────────────────────────────────────────────────────┤
│  CAMADA 1: AGENT GATE (Self-Check)                   │
│  → Agente valida próprio output antes de entregar     │
└──────────────────────────────────────────────────────┘
```

### Princípio Fundamental

> **Se não passou no gate, não avança. Se voltou, melhora. Se melhorou, re-submete.**

---

## 2. CAMADA 1: AGENT GATE (Auto-Verificação)

### O que é
Cada agente possui um **Layer 6: Meta-Cognitive** que funciona como gate pessoal. Antes de entregar qualquer output, o agente executa auto-verificação.

### Como funciona
1. O agente completa sua análise/output
2. Executa o checklist de auto-verificação do seu domínio
3. Verifica contra vieses cognitivos (Layer 6)
4. Se passa → entrega ao próximo estágio
5. Se não passa → re-trabalha antes de entregar

### Checklists por Agente
| Agente | Gate Primário | Gate Secundário |
|--------|--------------|-----------------|
| Vision Chief | `checklists/vision/vision-clarity-audit.md` | `checklists/strategy-memo-quality.md` |
| COO Orchestrator | `checklists/coo/coo-execution-rhythm-audit.md` | `checklists/operating-review-quality.md` |
| CMO Architect | `checklists/cmo/go-to-market-quality.md` | `checklists/cmo/funnel-integrity-audit.md` |
| CTO Architect | `checklists/tech-architecture-decision-quality.md` | `checklists/cto/platform-reliability-audit.md` |
| CIO Engineer | `checklists/cio/systems-portfolio-audit.md` | `checklists/cio/data-governance-audit.md` |
| CAIO Architect | `checklists/caio/model-eval-and-guardrails.md` | `checklists/caio/caio-ai-risk-assessment.md` |
| CFO Strategist | `checklists/finance/financial-health-audit.md` | `checklists/finance/unit-economics-audit.md` |

### Critério de Aprovação
- Todos os itens obrigatórios do checklist = ✅
- Nenhum anti-padrão detectado
- Output segue template padrão
- Vieses identificados e mitigados

---

## 3. CAMADA 2: TASK GATE (Validação por Task)

### O que é
Cada task possui checklists obrigatórios definidos no `config.yaml` routing. O output da task é validado contra esses checklists antes de ser registrado.

### Como funciona
1. Agente(s) completam a task
2. Output é verificado contra cada checklist listado na rota
3. Template de entrega é preenchido completamente
4. Registries são atualizados
5. Se passa → task marcada como concluída, registries atualizados
6. Se não passa → retorna ao agente responsável com feedback específico

### Exemplo: Task `define-vision-and-bets`
```yaml
# De config.yaml:
checklists:
  - checklists/strategy-memo-quality.md       # Gate 1
  - checklists/vision/vision-clarity-audit.md  # Gate 2
  - checklists/vision/strategic-bets-selection.md  # Gate 3
```
**Regra**: TODOS os 3 checklists devem passar. Falha em qualquer um = rework.

### Critério de Aprovação
- Todos os checklists da rota = ✅
- Template preenchido completamente (sem campos vazios)
- Registries atualizados com a decisão
- DRI (owner) atribuído

---

## 4. CAMADA 3: WORKFLOW GATE (Transição entre Estágios)

### O que é
Workflows são compostos de múltiplos estágios sequenciais. A transição entre estágios possui um gate intermediário.

### Como funciona
1. Estágio N é completado
2. Gate de transição verifica:
   - Output do estágio N está completo?
   - Pré-requisitos do estágio N+1 estão satisfeitos?
   - Algum risco foi introduzido?
   - Agentes do próximo estágio estão alinhados?
3. Se passa → avança para estágio N+1
4. Se não passa → volta para estágio N com itens pendentes

### Gate por Tipo de Workflow
| Workflow | Gate Crítico | Ponto de Decisão |
|----------|-------------|-------------------|
| 01: Vision → OKRs | Vision Chief aprova OKRs antes de cascatear | Entre definição e cascata |
| 04: WBR Loop | Métricas coletadas e validadas antes da review | Antes da reunião |
| 06: QBR Loop | OKR scoring completo antes de planejamento | Entre scoring e planning |
| 08: Exec Hiring | Scorecard aprovado antes de iniciar entrevistas | Antes do sourcing |
| 11: Incident Response | Severidade classificada antes de escalar | Após detecção |
| 14: AI Pipeline | POC validado antes de deploy em produção | Entre POC e rollout |
| 17: Board Prep | Deck revisado e dry-run antes da apresentação | Antes da entrega |

### Critério de Aprovação
- Output do estágio anterior verificável
- Inputs do próximo estágio disponíveis
- Nenhum bloqueio não resolvido
- Alignment confirmado entre agentes envolvidos

---

## 5. CAMADA 4: SQUAD GATE (Aprovação do Chief)

### O que é
Antes de qualquer output sair do squad para consumo externo (board, investidores, outros squads), o Chief do squad (Vision Chief ou COO, dependendo do tipo) valida.

### Como funciona
1. Output consolidado é preparado
2. Squad Coordinator organiza revisão
3. Chief revisa contra:
   - Alinhamento estratégico com tese/bets
   - Qualidade do output (GOLD/SOTA)
   - Consistência com decisões anteriores
   - Riscos não mitigados
4. Se aprovado → output é liberado
5. Se rejeitado → volta para o agente/workflow com feedback

### Quem Aprova o Quê
| Tipo de Output | Aprovador | Backup |
|---------------|-----------|--------|
| Decisão estratégica (Type 1) | Vision Chief | — (sem delegação) |
| Decisão operacional (Type 2) | Agente DRI | COO se conflito |
| Board material | Vision Chief + CFO | — |
| Cross-squad handoff | COO Orchestrator | Vision Chief |
| Comunicação externa | Vision Chief | CMO para marketing |
| Mudança organizacional | Vision Chief | COO para operacional |

### Gate Obrigatório: `checklists/exec-decision-memo-quality.md`
- Toda decisão que sai do squad deve passar por este gate
- Não é negociável — é constitucional (ARCHITECTURE.md §7.2 regra 4)

---

## 6. CAMADA 5: CROSS-SQUAD GATE (Handoff entre Squads)

### O que é
Quando o C-Level Squad entrega ou recebe trabalho de outros squads, um gate formal garante qualidade na transição.

### Como funciona
1. Squad de origem prepara output conforme DoD (Definition of Done)
2. Cross-squad handoff checklist é aplicado: `checklists/cross-squad-handoff-quality.md`
3. Squad de destino verifica DoR (Definition of Ready)
4. Se DoD + DoR = ✅ → handoff executado
5. Se falha → output retorna ao squad de origem

### Contrato de Handoff (de ARCHITECTURE.md §8.1)
```yaml
handoff:
  from: [squad de origem]
  to: [squad de destino]
  input: [o que está sendo entregue]
  format: [template/formato esperado]
  dod: [quando o input está "pronto"]
  dor: [quando o destino está "pronto para receber"]
  sla: [prazo máximo]
  owner: [DRI do handoff]
  escalation: [o que fazer se SLA estourar]
```

### Squads Integrados e SLAs
| Squad | Tipo de Handoff | SLA | Owner |
|-------|----------------|-----|-------|
| Brand | Briefing estratégico → brand guidelines | 5 dias | CMO |
| Copy | Positioning → messaging framework | 3 dias | CMO |
| Story | Narrativa estratégica → content plan | 5 dias | Vision Chief |
| Movement | Community strategy → execution plan | 5 dias | CMO |
| Traffic | Growth targets → acquisition plan | 3 dias | CMO |
| Design | Product requirements → UX/UI specs | 5 dias | CTO |
| Data | Metrics definition → dashboards | 3 dias | CIO |
| Cyber | Security requirements → compliance report | 5 dias | CIO |
| Advisory | Strategic question → advisory brief | 10 dias | Vision Chief |

### Gate de Retorno
Se o squad receptor identifica que o output não atende ao DoR:
1. Documenta gaps específicos
2. Retorna ao squad de origem via template de feedback
3. SLA de correção = 50% do SLA original
4. Se segundo retorno → COO Orchestrator intervém

---

## 7. CAMADA 6: HRM GATE (Central Command / Board)

### O que é
O gate mais alto no sistema — valida se o output do squad está em nível adequado para stakeholders finais (board, investidores, fundadores).

### Como funciona
1. Vision Chief submete output consolidado
2. Validação contra:
   - Padrão GOLD/SOTA de qualidade
   - Consistência com narrativa estratégica
   - Completude de dados e evidências
   - Riscos adequadamente comunicados
3. Board/Advisory review
4. Se aprovado → output é final
5. Se devolvido → volta ao squad com itens de melhoria

### Critério GOLD/SOTA
| Nível | Definição | Gate |
|-------|----------|------|
| **WEAK** | Output incompleto ou superficial | ❌ Bloqueado — rework obrigatório |
| **FAIR** | Output funcional mas sem profundidade | ⚠️ Condicional — pode passar para uso interno |
| **GOOD** | Output sólido com evidências | ✅ Aprovado para consumo interno |
| **GOLD** | Output excelente com insights originais | ✅ Aprovado para board/externo |
| **SOTA** | Output que define o padrão do mercado | ✅ Aprovado + documentado como referência |

---

## 8. LOOP DE MELHORIA (RalphLoop Integration)

### Quando o Gate Rejeita
Todo gate que rejeita um output dispara o seguinte loop:

```
REJEIÇÃO → FEEDBACK ESPECÍFICO → REWORK → RE-SUBMISSÃO → RE-AVALIAÇÃO
     ↑                                                          │
     └──── SE REJEITADO NOVAMENTE ────────────────────────────┘
```

### Regras do Loop
1. **Feedback deve ser específico** — "melhorar" não é feedback, "faltam dados de Q4 no slide 3" é
2. **Máximo de 3 loops** — após 3 rejeições, escala para o chief
3. **Cada loop reduz o SLA** — urgência aumenta a cada iteração
4. **Aprendizado é registrado** — `data/registries/lessons-learned.yaml`

### Checklist do RalphLoop: `checklists/ralphloop-quality.md`
Aplicado ao final de cada ciclo de gate para garantir que o aprendizado foi capturado:
- [ ] Decisão registrada no `data/registries/decision-registry.yaml`
- [ ] Outcome tracking definido (como e quando medir)
- [ ] Aprendizado documentado se houve rework
- [ ] Processo ajustado se padrão de rejeição identificado

---

## 9. MATRIZ DE GATES POR WORKFLOW

| Workflow | Agent Gate | Task Gate | Workflow Gate | Squad Gate | Cross-Squad Gate |
|----------|-----------|-----------|---------------|------------|-----------------|
| 00: Setup | ✅ | ✅ | ✅ | ✅ (Vision Chief) | — |
| 01: Vision→OKRs | ✅ | ✅ | ✅ (OKR approval) | ✅ (Vision Chief) | — |
| 04: WBR | ✅ | ✅ | ✅ (data validation) | ✅ (COO) | — |
| 06: QBR | ✅ | ✅ | ✅ (scoring + planning) | ✅ (Vision Chief) | — |
| 08: Hiring | ✅ | ✅ | ✅ (scorecard approval) | ✅ (Vision Chief) | — |
| 11: Incident | ✅ | ✅ | ✅ (severity check) | ✅ (Vision Chief) | ✅ (Cyber squad) |
| 14: AI Pipeline | ✅ | ✅ | ✅ (POC eval) | ✅ (CAIO + CTO) | ✅ (Data squad) |
| 16: Cross-Squad | ✅ | ✅ | ✅ | ✅ (COO) | ✅ (todos os squads) |
| 17: Board Prep | ✅ | ✅ | ✅ (dry run) | ✅ (Vision Chief) | — |
| 20: Postmortem | ✅ | ✅ | ✅ (RCA completeness) | ✅ (COO) | ✅ (se cross-squad) |

---

## 10. REFERÊNCIAS CRUZADAS

### Documentos Relacionados
- `ARCHITECTURE.md` — Constituição do squad (seções 7-8)
- `config.yaml` — Quality gates section + routing checklists
- `checklists/exec-decision-memo-quality.md` — Gate universal obrigatório
- `checklists/ralphloop-quality.md` — Gate de aprendizado
- `checklists/cross-squad-handoff-quality.md` — Gate de handoff
- `lib/patterns/escalation-pattern.md` — Padrão de escalonamento
- `lib/patterns/decision-routing-pattern.md` — Padrão de roteamento

### Scripts de Auditoria
- `scripts/audit/cross-reference-validator.md` — Validação de referências
- `scripts/audit/content-quality-audit.md` — Auditoria de qualidade
- `scripts/audit/repo-health-check.md` — Health check geral
