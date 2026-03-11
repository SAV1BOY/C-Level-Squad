# Decision Log Updater

> Script para actualização e manutenção do registo de decisões.

---

## Objetivo

Manter um registo centralizado, completo e actualizado de todas as decisões
relevantes tomadas pelo C-Level Squad. Este script define os triggers de
captura, campos obrigatórios, validação e processo de manutenção.

---

## Capture Triggers — Quando Registar

### Triggers Automáticos
Uma decisão deve ser registada quando:
1. **Reunião formal** (WBR, MBR, QBR, Board) produz deliberação
2. **Aprovação de budget** acima de threshold definido
3. **Mudança de prioridade** em iniciativa estratégica
4. **Contratação ou saída** de posição senior (Director+)
5. **Alteração de roadmap** que afecta timeline ou scope
6. **Política nova ou alterada** que afecta operações
7. **Escalação resolvida** que envolveu C-Level deliberation

### Triggers Manuais
Qualquer membro do squad pode registar uma decisão quando:
- Uma escolha significativa foi feita em reunião informal
- Um trade-off foi deliberadamente aceite
- Uma direcção foi definida que afecta múltiplas equipas
- Um precedente foi estabelecido para futuras decisões

### Critério de Relevância
Registar se pelo menos UM critério é verdadeiro:
- Impacto financeiro > threshold definido (ex: >10k EUR)
- Afecta mais de 1 squad ou departamento
- Tem implicações estratégicas ou de longo prazo
- Altera política ou processo existente
- É reversível apenas com custo significativo

---

## Required Fields — Campos Obrigatórios

### Campos Core
```yaml
decision_id: "DEC-YYYY-NNNN"          # ID único auto-gerado
title: "Título claro e descritivo"      # Max 100 caracteres
date: "YYYY-MM-DD"                      # Data da decisão
status: "active | superseded | revoked" # Estado actual
decision_maker: "Nome / Role"           # Quem tomou a decisão
decision_type: "strategic | tactical | operational"
context: "Descrição do contexto..."     # 2-5 frases
decision: "O que foi decidido..."       # Declaração clara
rationale: "Porquê esta opção..."       # Justificação
alternatives_considered:                 # Opções rejeitadas
  - option: "Alternativa A"
    reason_rejected: "Motivo"
  - option: "Alternativa B"
    reason_rejected: "Motivo"
impact:
  financial: "Estimativa de impacto"
  operational: "Mudanças operacionais"
  timeline: "Impacto no calendário"
review_date: "YYYY-MM-DD"              # Quando rever
tags: ["area", "squad", "tema"]
```

### Campos Opcionais
```yaml
related_decisions: ["DEC-YYYY-NNNN"]   # Decisões relacionadas
supporting_data: "link para dados"       # Evidência utilizada
meeting_ref: "Referência da reunião"     # Onde foi tomada
stakeholders_consulted: ["lista"]        # Quem foi consultado
dissenting_views: "Opiniões contrárias"  # Registar desacordos
implementation_owner: "Nome / Role"      # Quem implementa
success_criteria: "Como medir sucesso"   # Definição de sucesso
risk_accepted: "Riscos aceites"          # Riscos conhecidos
```

---

## Validation — Regras de Validação

### Validação Automática
Antes de gravar, o sistema valida:
1. **Completude**: todos os campos core preenchidos
2. **Formato**: decision_id segue padrão, datas em ISO
3. **Consistência**: review_date > date
4. **Duplicação**: título não duplica decisão existente (similarity >80%)
5. **Referências**: related_decisions existem no log
6. **Tags**: pelo menos 1 tag válida do vocabulário controlado

### Validação Humana
O decision owner deve confirmar:
- [ ] A decisão está correctamente descrita
- [ ] O contexto é suficiente para entender no futuro
- [ ] As alternativas consideradas estão registadas
- [ ] O impacto está razoavelmente estimado
- [ ] A review date é apropriada

---

## Processo de Actualização

### Workflow Regular
```
1. CAPTURA
   - Trigger detectado (automático ou manual)
   - Draft criado com campos disponíveis
   - Notificação ao decision maker para completar

2. COMPLETAR
   - Decision maker preenche campos em falta
   - Adiciona context e rationale detalhados
   - Define review date

3. VALIDAR
   - Validação automática executada
   - Se falha: notificar owner com campos a corrigir
   - Se passa: avançar para publicação

4. PUBLICAR
   - Decision registada no log central
   - Stakeholders notificados conforme relevância
   - Índice actualizado
   - Tags e cross-references processados

5. REVER
   - Na review date: notificar decision maker
   - Avaliar se decisão ainda é válida
   - Actualizar status se necessário
   - Definir próxima review date ou marcar como "reviewed"
```

### Actualizações de Status
| De | Para | Quando |
|----|------|--------|
| active | active (reviewed) | Review confirma validade |
| active | superseded | Nova decisão substitui esta |
| active | revoked | Decisão revertida |
| superseded | — | Estado final |
| revoked | active | Re-activação (raro, requer justificação) |

---

## Indexação e Pesquisa

### Índices Mantidos
- **Cronológico**: todas as decisões por data
- **Por squad**: decisões agrupadas por squad owner
- **Por tipo**: strategic / tactical / operational
- **Por status**: active / superseded / revoked
- **Por tag**: agrupadas por área temática
- **Por impacto**: ordenadas por magnitude de impacto

### Pesquisa
O log deve suportar pesquisa por:
- Texto livre em título, contexto e decisão
- Filtros combinados (squad + tipo + status + período)
- Decisões relacionadas (graph traversal)
- Timeline visual de decisões

---

## Reporting

### Dashboard de Decisões
- Total de decisões por período e tipo
- Decisões pendentes de review
- Distribuição por squad e área
- Tempo médio de captura (trigger → registo)
- Taxa de completude dos campos

### Alertas
- Decisão activa com review date ultrapassada
- Decisão sem alternatives_considered
- Cluster de decisões no mesmo tema (possível inconsistência)
- Decisão com impacto alto sem review date

---

## Integração com Outros Processos

- **Agenda Generator**: decision points resolvidos alimentam o log
- **Risk Scan**: decisões com risk_accepted alimentam o risk register
- **Initiative Tracker**: decisões que afectam iniciativas actualizam status
- **Meeting Effectiveness**: taxa de decisões por reunião é métrica
- **Quarterly Review**: histórico de decisões é input para análise

---

## Notas Técnicas

- Armazenamento: ficheiros YAML em `data/decisions/` com um ficheiro por decisão
- Índice central: `data/decisions/index.yaml` auto-gerado
- Backup: diário, retenção mínima de 5 anos
- Acesso: leitura para todo o squad, escrita para owners e admins
- Auditoria: todas as alterações são registadas com timestamp e autor
