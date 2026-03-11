# Cross-Squad Effectiveness Analyzer

> Script para análise da eficácia da colaboração entre squads.

---

## Objetivo

Medir e melhorar a qualidade da colaboração entre squads, avaliando
cumprimento de SLAs, qualidade dos handoffs, satisfação mútua e eficiência
na resolução de dependências. Colaboração cross-squad é frequentemente o
maior bottleneck em organizações complexas.

---

## Dimensões de Análise

### 1. SLA Compliance (Cumprimento de SLAs)

#### Métricas
- **Response time SLA**: tempo desde pedido até primeira resposta
- **Resolution time SLA**: tempo desde pedido até resolução completa
- **Quality SLA**: % de entregas que passam no quality gate
- **Availability SLA**: disponibilidade dos serviços/recursos partilhados
- **Escalation SLA**: tempo de resposta a escalações

#### Medição
```yaml
sla_record:
  request_id: "REQ-YYYY-NNNN"
  requesting_squad: "Nome"
  providing_squad: "Nome"
  request_type: "information | deliverable | review | support | decision"
  sla_target:
    response_time: "4h"
    resolution_time: "48h"
  actual:
    response_time: "3h"
    resolution_time: "52h"
  sla_met: false
  breach_reason: "Dependência externa não prevista"
```

#### Targets por Tipo
| Tipo de Request | Response SLA | Resolution SLA | Quality Gate |
|----------------|-------------|---------------|-------------|
| Information | 4h | 24h | Completa e precisa |
| Deliverable | 8h | Conforme acordo | DoD cumprido |
| Review | 4h | 48h | Feedback actionable |
| Support | 2h | 8h | Issue resolvido |
| Decision | 4h | 24h | Decisão documentada |

### 2. Handoff Quality (Qualidade das Transferências)

#### Critérios de Qualidade
- **Completeness**: toda a informação necessária está incluída
- **Clarity**: o receptor entende sem perguntas adicionais
- **Timeliness**: entregue dentro do prazo acordado
- **Format compliance**: segue template/formato acordado
- **DoR/DoD adherence**: Definition of Ready/Done respeitada

#### Scoring de Handoff
```
Handoff Quality Score = Completeness(25%) + Clarity(25%) +
                        Timeliness(20%) + Format(15%) + DoR/DoD(15%)

Escala: 1-5 por critério
```

#### Problemas Comuns de Handoff
- Informação incompleta que gera round-trips
- Formato inconsistente que requer reprocessamento
- Contexto insuficiente que causa mal-entendidos
- Timing inadequado que bloqueia trabalho downstream
- Falta de ownership clara durante a transição

### 3. Satisfaction (Satisfação Mútua)

#### Survey Trimestral Inter-Squad
Cada squad avalia os squads com quem interage:

```
1. Qualidade geral da colaboração: [1-5]
2. Responsividade (tempo de resposta): [1-5]
3. Qualidade das entregas: [1-5]
4. Comunicação proactiva: [1-5]
5. Facilidade de trabalhar com este squad: [1-5]
6. O que funciona bem? [texto livre]
7. O que pode melhorar? [texto livre]
```

#### Net Collaboration Score (NCS)
```
NCS = (% promoters - % detractors) × 100
Promoters: satisfaction ≥ 4
Detractors: satisfaction ≤ 2
```

### 4. Dependency Resolution

#### Métricas
- **Dependency identification rate**: % de dependências identificadas no planeamento
- **Resolution time**: tempo médio para resolver dependência
- **Blocking time**: tempo total bloqueado por dependências
- **Re-escalation rate**: % de dependências que precisam de re-escalação
- **Preventable blocks**: bloqueios que podiam ter sido evitados

---

## Processo de Análise

### Data Collection (Contínuo)
1. Registar cada pedido cross-squad com timestamps
2. Tracking automático de SLA compliance
3. Handoff quality avaliado pelo receptor
4. Survey de satisfação trimestral
5. Log de dependências e bloqueios

### Analysis (Mensal)
1. Calcular SLA compliance rates por squad pair
2. Calcular handoff quality scores médios
3. Identificar padrões de incumprimento
4. Mapear bottlenecks recorrentes
5. Comparar com período anterior

### Deep Dive (Trimestral)
1. Análise completa de todas as dimensões
2. Survey de satisfação inter-squad
3. Identificação de melhorias sistémicas
4. Workshop de alinhamento (se necessário)
5. Actualização de SLAs e contratos

---

## Scoring Composto

### Cross-Squad Effectiveness Score (CSES)
```
CSES = SLA_Compliance(30%) + Handoff_Quality(25%) +
       Satisfaction(25%) + Dependency_Resolution(20%)
```

| CSES | Classificação | Acção |
|------|--------------|-------|
| 85-100 | Excelente | Manter e partilhar best practices |
| 70-84 | Boa | Melhorias incrementais |
| 55-69 | Aceitável | Plano de melhoria específico |
| 40-54 | Fraca | Intervenção necessária |
| 0-39 | Crítica | Redesign dos contratos inter-squad |

---

## Reporting

### Monthly Cross-Squad Report
```markdown
# Cross-Squad Effectiveness — [Mês]

## Resumo
- Requests cross-squad: [N]
- SLA compliance geral: [%]
- Handoff quality médio: [score/5]
- Bloqueios por dependências: [N] ([horas bloqueadas])

## Heatmap de SLA Compliance
| De ↓ / Para → | Squad A | Squad B | Squad C |
|---------------|---------|---------|---------|
| Squad A | — | [%] | [%] |
| Squad B | [%] | — | [%] |
| Squad C | [%] | [%] | — |

## Top Issues
1. [Issue com contexto e impacto]
2. [Issue com contexto e impacto]

## Wins
1. [Melhoria observada]
2. [Colaboração exemplar]

## Acções
- [Acção com owner e prazo]
```

### Quarterly Deep Dive
- Todas as métricas acima com trending
- Satisfaction survey results
- Dependency map visual
- Systemic improvement recommendations
- Contract/SLA revision proposals

---

## Integração

- **Cross-Squad Contracts**: SLAs definidos nos contratos são a referência
- **Initiative Health**: dependências afectam health das iniciativas
- **Risk Scan**: falhas cross-squad são sinais de risco
- **Meeting Effectiveness**: reuniões cross-squad têm métricas específicas
- **Quarterly Review**: CSES é input para review trimestral

---

## Notas Técnicas

- Dados armazenados em `data/cross-squad/`
- SLA tracking idealmente automatizado via ticketing system
- Handoff quality requer input manual do receptor
- Surveys distribuídos automaticamente no início de cada trimestre
- Dashboard actualizado semanalmente
