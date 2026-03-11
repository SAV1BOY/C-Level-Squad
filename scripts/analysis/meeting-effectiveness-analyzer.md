# Meeting Effectiveness Analyzer

> Script para análise da eficácia de reuniões do C-Level Squad.

---

## Objetivo

Medir e melhorar a eficácia das reuniões, avaliando taxa de decisões tomadas,
conclusão de action items, utilização do tempo e satisfação dos participantes.
Reuniões são o principal mecanismo de coordenação — optimizá-las tem impacto
directo na velocidade de execução.

---

## Métricas de Eficácia

### 1. Decision Rate (Taxa de Decisão)
```
Decision Rate = decisões_tomadas / decisões_agendadas × 100

Targets:
- WBR: ≥80% das decisões agendadas resolvidas
- MBR: ≥75% das decisões agendadas resolvidas
- QBR: ≥70% das decisões agendadas resolvidas
- Ad hoc: ≥90% (reunião convocada para decidir)
```

**Breakdown detalhado:**
- Decisões tomadas na reunião
- Decisões adiadas (com motivo válido)
- Decisões adiadas (sem motivo claro) — flag de ineficiência
- Decisões delegadas para fora da reunião

### 2. Action Item Completion (Conclusão de Acções)
```
Completion Rate = actions_completed_on_time / actions_assigned × 100

Targets:
- Completion rate: ≥85%
- On-time rate: ≥75%
- Carry-over rate: ≤15% (itens que transitam para próxima reunião)
```

**Tracking detalhado:**
- Action items criados por reunião
- Action items concluídos no prazo
- Action items concluídos com atraso
- Action items cancelados ou reatribuídos
- Tempo médio de conclusão

### 3. Time Utilization (Utilização do Tempo)
```
Productive Time = tempo_em_decisões_e_discussão_relevante / tempo_total × 100

Categorias de tempo:
- Decisão: deliberação activa sobre decision points
- Informação: partilha de dados e contexto necessário
- Discussão: exploração de temas relevantes
- Overhead: admin, late starts, repetições, tangentes
```

**Targets:**
- Tempo produtivo (decisão + informação + discussão): ≥80%
- Overhead: ≤20%
- Início pontual: ≤5 min de atraso
- Fim pontual: ≤5 min de excesso

### 4. Participant Engagement
```
Engagement Score = média de indicadores de participação

Indicadores:
- Participação verbal: % de participantes que contribuem
- Preparação: % que leu pre-read materials
- Atenção: observação qualitativa (sem multitasking)
- Contribuição: qualidade das contribuições (peer-rated)
```

### 5. Meeting ROI
```
Meeting ROI = valor_das_decisões_e_alinhamento / custo_da_reunião

Custo = soma(salário_hora × duração) para todos os participantes
Valor = estimativa do impacto das decisões tomadas + alinhamento gerado
```

---

## Processo de Análise

### Dados Recolhidos por Reunião
```yaml
meeting_id: "MTG-YYYY-MM-DD-[tipo]"
type: "WBR | MBR | QBR | ad_hoc | standup"
date: "YYYY-MM-DD"
duration_planned: 60          # minutos
duration_actual: 67           # minutos
participants_expected: 6
participants_actual: 5
late_arrivals: 1
agenda_items: 5
agenda_items_covered: 4
decisions_agendable: 3
decisions_made: 2
decisions_deferred: 1
action_items_created: 7
action_items_from_previous: 10
action_items_completed: 8
pre_read_sent: true
pre_read_sent_hours_before: 26
facilitator: "Nome"
notes_captured: true
time_breakdown:
  decision: 25      # minutos
  information: 15
  discussion: 18
  overhead: 9
participant_satisfaction: 4.2  # escala 1-5
```

### Fontes de Dados
1. **Calendar/scheduling system**: duração, participantes, pontualidade
2. **Meeting notes**: agenda, decisões, action items
3. **Action tracking system**: completion rates
4. **Quick survey pós-reunião**: satisfação e feedback (30 segundos)
5. **Facilitator assessment**: observações qualitativas

---

## Quick Survey Pós-Reunião

Enviado automaticamente 5 minutos após o fim:

```
1. Esta reunião foi produtiva? [1-5 estrelas]
2. As decisões necessárias foram tomadas? [Sim/Não/Parcialmente]
3. O tempo foi bem utilizado? [Sim/Não]
4. Tinhas a informação necessária? [Sim/Não]
5. Uma palavra para descrever a reunião: [texto livre]
```

Tempo de resposta esperado: 30 segundos. Taxa de resposta target: >80%.

---

## Scoring e Classificação

### Meeting Effectiveness Score (MES)
```
MES = Decision_Rate(30%) + Action_Completion(25%) +
      Time_Utilization(25%) + Engagement(20%)
```

| MES | Classificação | Acção |
|-----|--------------|-------|
| 85-100 | Excelente | Manter formato |
| 70-84 | Boa | Minor tweaks |
| 55-69 | Aceitável | Rever estrutura |
| 40-54 | Fraca | Redesign necessário |
| 0-39 | Ineficaz | Cancelar ou reformatar |

---

## Padrões a Detectar

### Red Flags
- Mesma decisão adiada 2+ vezes → problema de preparação ou autoridade
- Action items com carry-over >30% → sobrecarga ou falta de accountability
- Overhead >30% do tempo → problemas de facilitação
- <50% dos participantes contribuem verbalmente → formato inadequado
- Satisfação consistentemente <3.0 → reunião percebida como inútil

### Green Flags
- Decision rate >90% → boa preparação e autoridade clara
- Action completion >90% → cultura de accountability forte
- Início e fim pontuais → respeito pelo tempo
- Alta satisfação com baixa duração → eficiência máxima

---

## Reporting

### Weekly Meeting Health Summary
- MES por tipo de reunião na semana
- Action item completion rate
- Alertas para reuniões com MES <55

### Monthly Meeting Effectiveness Report
```markdown
# Meeting Effectiveness — [Mês]

## Resumo
- Total de reuniões analisadas: [N]
- MES médio: [score]
- Horas em reunião: [total] ([média por pessoa por semana])
- Decisões tomadas: [N] (taxa: [%])
- Action items: [criados] / [concluídos] ([%])

## Por Tipo de Reunião
| Tipo | Quantidade | MES Médio | Decision Rate |
|------|-----------|-----------|---------------|
| WBR | [N] | [score] | [%] |
| MBR | [N] | [score] | [%] |
| Ad hoc | [N] | [score] | [%] |

## Tendências
- [Observação sobre tendência 1]
- [Observação sobre tendência 2]

## Recomendações
- [Acção 1]
- [Acção 2]
```

---

## Integração

- **Agenda Generator**: qualidade da agenda afecta effectiveness
- **Decision Log**: decisões de reuniões alimentam o log
- **Initiative Health**: reuniões são mecanismo de desbloqueio
- **Quarterly Review**: meeting effectiveness é input para review

---

## Notas Técnicas

- Dados armazenados em `data/meetings/`
- Survey automático via integração com calendar
- Dashboard actualizado em tempo real após cada reunião
- Análise de tendências requer mínimo 8 semanas de dados
- Confidencialidade: dados individuais apenas visíveis ao facilitador e squad lead
