# Cross-Squad Contracts — SLAs, Handoffs, DoD/DoR

> Contratos de colaboração entre squads: Service Level Agreements, transferências e definições de qualidade.

---

## Objetivo

Definir formalmente as expectativas, responsabilidades e standards de qualidade
nas interacções entre squads e agentes. Contratos claros reduzem fricção,
previnem mal-entendidos e criam accountability mútua.

---

## Princípios dos Contratos

1. **Bilaterais**: ambas as partes concordam e beneficiam
2. **Explícitos**: nada é assumido, tudo é documentado
3. **Mensuráveis**: métricas claras de cumprimento
4. **Revisáveis**: actualizados trimestralmente ou quando necessário
5. **Razoáveis**: exigências devem ser alcançáveis com recursos disponíveis

---

## Service Level Agreements (SLAs)

### Estrutura de um SLA
```yaml
sla_id: "SLA-[squad_a]-[squad_b]-[tipo]"
parties:
  provider: "Squad que fornece"
  consumer: "Squad que consome"
service: "Descrição do serviço"
metrics:
  - name: "Response time"
    target: "4 horas úteis"
    measurement: "Tempo desde request até primeira resposta"
  - name: "Resolution time"
    target: "48 horas úteis"
    measurement: "Tempo desde request até resolução"
  - name: "Quality"
    target: "95% aceite na primeira entrega"
    measurement: "% de entregas sem rework"
escalation:
  level_1: "Squad lead — após 80% do SLA consumido"
  level_2: "C-Level sponsor — após SLA breach"
review: "Trimestral"
effective_date: "YYYY-MM-DD"
```

### SLAs Padrão por Tipo de Serviço
| Tipo | Response | Resolution | Quality |
|------|----------|-----------|---------|
| Information request | 4h | 24h | Completa e precisa |
| Deliverable | 8h (ack) | Conforme acordo | DoD cumprido |
| Review / Feedback | 4h (ack) | 48h | Actionable e específico |
| Technical support | 2h | 8h (P1), 24h (P2), 48h (P3) | Issue resolvido |
| Decision input | 4h | 24h | Perspectiva fundamentada |
| Data / Analytics | 4h | 24h (standard), 4h (urgent) | Dados validados |

### Medição de SLA Compliance
```
SLA Compliance Rate = requests_within_sla / total_requests × 100

Target geral: ≥85%
Alerta: <80%
Crítico: <70%
```

---

## Definition of Ready (DoR)

### O Que É
A DoR define os critérios que um pedido deve cumprir antes de ser aceite pelo
squad que vai executar. É a "porta de entrada" — se não cumpre, volta para
preparação.

### DoR Padrão para Pedidos Cross-Squad
- [ ] Objectivo claro e específico (o que precisa e porquê)
- [ ] Scope definido (o que está incluído e excluído)
- [ ] Acceptance criteria documentados (como saber que está feito)
- [ ] Prazo definido e acordado (quando é necessário)
- [ ] Owner identificado em ambos os lados
- [ ] Dependências mapeadas (o que mais é preciso)
- [ ] Prioridade classificada e acordada
- [ ] Dados/informação necessária disponível

### DoR por Tipo de Pedido
| Tipo | Critérios Adicionais |
|------|---------------------|
| Feature request | User stories, mockups, requisitos técnicos |
| Data request | Query definition, formato esperado, período |
| Review request | Documento completo, contexto, critérios de review |
| Support request | Reprodução do problema, impacto, urgência |
| Decision input | Contexto, opções identificadas, deadline |

---

## Definition of Done (DoD)

### O Que É
A DoD define os critérios que uma entrega deve cumprir para ser considerada
completa. É a "porta de saída" — se não cumpre, não está feita.

### DoD Padrão para Entregas Cross-Squad
- [ ] Todos os acceptance criteria cumpridos
- [ ] Quality check realizado (self-review)
- [ ] Documentação actualizada (se aplicável)
- [ ] Formato conforme acordo (template, estrutura)
- [ ] Entregue no canal e formato acordado
- [ ] Consumer confirmou recepção
- [ ] Decisões ou pressupostos documentados
- [ ] Handover completo (contexto transferido)

### DoD por Tipo de Entrega
| Tipo | Critérios Adicionais |
|------|---------------------|
| Código / Feature | Testes passam, review feito, deployed |
| Documento / Report | Formatado, spell-checked, approved |
| Dados / Analytics | Validados, fonte documentada, reproduzível |
| Decisão | Registada no log, comunicada, owner definido |
| Design / Mockup | Specs completos, assets exportados |

---

## Handoff Protocol — Protocolo de Transferência

### Regras de Handoff
1. **Responsabilidade transfere**: quem recebe é agora responsável
2. **Contexto acompanha**: toda a informação relevante é incluída
3. **Confirmação explícita**: receptor confirma que recebeu e entendeu
4. **Período de gracefulness**: 24h para perguntas de clarificação
5. **No ping-pong**: máximo 2 round-trips antes de reunião síncrona

### Template de Handoff
```markdown
# Handoff: [Título]
**De**: [Squad/Pessoa] → **Para**: [Squad/Pessoa]
**Data**: [YYYY-MM-DD]

## O que está a ser transferido
[Descrição clara]

## Estado actual
[Em que ponto está, o que foi feito, o que falta]

## Contexto necessário
[Background, decisões tomadas, pressupostos]

## Próximos passos esperados
[O que o receptor deve fazer]

## Materiais incluídos
- [Link/ficheiro 1]
- [Link/ficheiro 2]

## Contacto para dúvidas
[Pessoa disponível por 24h para clarificações]
```

---

## Resolução de Disputes

### Quando um SLA é Quebrado
1. **Registo**: breach é registado automaticamente
2. **Root cause**: provider identifica causa em 24h
3. **Remediation**: plano para evitar repetição
4. **Compensação**: se impacto significativo, priorização compensatória
5. **Escalação**: se recorrente (3+ breaches/mês), escala a C-Level

### Quando Partes Discordam
1. Tentativa de resolução directa entre squads
2. Se não resolvido em 48h: mediação pelo COO Orchestrator
3. Se não resolvido: decisão pelo Vision Chief
4. Decisão é final e registada no decision log

---

## Revisão de Contratos

### Frequência
- **Review trimestral**: todos os SLAs activos são revistos
- **Review ad hoc**: quando mudanças significativas ocorrem
- **Anual**: redesign completo se necessário

### Processo de Revisão
1. Recolher dados de SLA compliance dos últimos 3 meses
2. Recolher feedback de ambas as partes
3. Identificar SLAs que precisam de ajuste
4. Propor alterações com justificação
5. Acordo mútuo e documentação
6. Comunicação das alterações

---

## Registo de Contratos

Todos os contratos activos são mantidos em:
- Local: `data/contracts/`
- Formato: YAML por contrato
- Índice: `data/contracts/index.yaml`
- Histórico: versões anteriores arquivadas

---

## Notas Técnicas

- SLA tracking preferencialmente automatizado
- Alertas de SLA breach distribuídos via canais configurados
- Dashboard de SLA compliance visível a todos os squads
- Métricas de contrato são input para quarterly review
