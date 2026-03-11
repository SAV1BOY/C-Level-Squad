# Risk Scan

> Script para detecção contínua de riscos, alertas e escalação.

---

## Objetivo

Identificar riscos de forma proactiva através de monitorização de sinais,
avaliar a sua severidade, gerar alertas quando thresholds são ultrapassados
e garantir escalação adequada quando necessário.

---

## Signal Detection — Detecção de Sinais

### Categorias de Sinais

#### 1. Sinais Financeiros
- Revenue abaixo do forecast por 2+ semanas consecutivas
- Burn rate acima do budget por >10%
- Cash runway abaixo de 6 meses
- Concentração de receita num cliente >30%
- Margem bruta em declínio por 3+ meses
- Contas a receber aging >90 dias a crescer
- Custo de aquisição de cliente (CAC) a aumentar >20% QoQ

#### 2. Sinais Operacionais
- Velocity de equipa em declínio por 3+ sprints
- Incidentes P1/P2 a aumentar em frequência
- SLA breaches acima de threshold
- Bloqueios cross-squad sem resolução >5 dias
- Reuniões de decisão canceladas ou adiadas repetidamente
- Action items overdue >50% do total
- Cycle time a aumentar consistentemente

#### 3. Sinais de Pessoas
- Attrition rate acima da média do sector
- Engagement scores em declínio
- Key person dependencies não mitigadas
- Posições críticas abertas >60 dias
- Feedback negativo recorrente em 1:1s
- Overtime consistente em equipas específicas
- Conflitos inter-equipa não resolvidos

#### 4. Sinais de Mercado
- Competitor lança produto concorrente
- Regulação nova que afecta operações
- Mudança significativa em customer behaviour
- Fornecedor crítico com problemas financeiros
- Tecnologia disruptiva emerge no sector
- Mudança macroeconómica afecta mercado-alvo
- Sentiment negativo crescente em social media

#### 5. Sinais Tecnológicos
- Tech debt ratio acima de threshold
- Security vulnerabilities não remediadas >30 dias
- System uptime abaixo de 99.5%
- Data quality scores em declínio
- Integration failures a aumentar
- Performance degradation em sistemas core
- Licenças ou contratos tech a expirar sem renovação

---

## Alerting Thresholds — Limiares de Alerta

### Matriz de Severidade
```
PROBABILIDADE × IMPACTO = SEVERIDADE

Probabilidade:
  5 = Quase certo (>90%)
  4 = Provável (60-90%)
  3 = Possível (30-60%)
  2 = Improvável (10-30%)
  1 = Raro (<10%)

Impacto:
  5 = Catastrófico (ameaça existencial)
  4 = Major (impacto estratégico significativo)
  3 = Moderado (impacto táctico relevante)
  2 = Minor (impacto operacional limitado)
  1 = Negligível (impacto mínimo)

Severidade = Probabilidade × Impacto
  20-25 = Critical (vermelho escuro)
  12-19 = High (vermelho)
  6-11  = Medium (amarelo)
  1-5   = Low (verde)
```

### Thresholds de Alerta
| Severidade | Tempo de Resposta | Escalação Automática |
|-----------|-------------------|---------------------|
| Critical | Imediato (<1h) | C-Level Squad + Board |
| High | Mesmo dia (<8h) | C-Level Squad |
| Medium | 48h | Squad Lead + Risk Owner |
| Low | Próxima revisão regular | Risk Owner |

---

## Escalation — Processo de Escalação

### Níveis de Escalação
```
Nível 0: Detecção automática
  → Registo no risk register
  → Notificação ao risk owner

Nível 1: Risk Owner (resposta: 24h low/medium, 8h high, 1h critical)
  → Avaliar e classificar
  → Definir mitigação ou aceitar
  → Se não consegue mitigar → Nível 2

Nível 2: Squad Lead
  → Realocar recursos se necessário
  → Escalar dependências cross-squad
  → Se impacto estratégico → Nível 3

Nível 3: C-Level Sponsor
  → Decisão sobre investimento em mitigação
  → Comunicação a stakeholders
  → Se ameaça existencial → Nível 4

Nível 4: Full C-Level Squad + Board
  → War room activado
  → Plano de contingência executado
  → Comunicação de crise iniciada
```

### Regras de Escalação Automática
- Risco sem owner atribuído após 24h → escala para Squad Lead
- Mitigação sem progresso após 1 semana → escala 1 nível
- Risco reclassificado para severidade superior → notifica novo nível
- Múltiplos riscos correlacionados detectados → alerta de cluster

---

## Risk Register — Formato do Registo

### Campos por Risco
```yaml
risk_id: "RISK-YYYY-NNNN"
title: "Descrição clara do risco"
category: "financial | operational | people | market | technology"
date_identified: "YYYY-MM-DD"
status: "open | mitigating | accepted | mitigated | closed"
probability: 1-5
impact: 1-5
severity: "calculated"
owner: "Nome / Role"
description: "Descrição detalhada do risco e contexto"
trigger_signals: ["sinais que indicam materialização"]
mitigation_plan: "Acções para reduzir probabilidade/impacto"
contingency_plan: "O que fazer se o risco se materializar"
related_initiatives: ["IDs de iniciativas afectadas"]
related_risks: ["IDs de riscos correlacionados"]
review_frequency: "weekly | biweekly | monthly"
last_reviewed: "YYYY-MM-DD"
history: [
  { date: "YYYY-MM-DD", change: "descrição da alteração" }
]
```

---

## Scanning Process — Processo de Scanning

### Scan Automático (Diário)
1. Recolher dados de todas as fontes de sinais
2. Comparar com thresholds definidos
3. Identificar novos sinais acima de threshold
4. Cruzar sinais para detectar correlações
5. Actualizar risk register com novos dados
6. Gerar alertas para sinais relevantes

### Scan Manual (Semanal)
1. Risk owners revêem os seus riscos
2. Actualizam probabilidade e impacto
3. Reportam progresso de mitigação
4. Identificam riscos novos não detectados automaticamente
5. Validam ou ajustam classificações automáticas

### Scan Profundo (Mensal)
1. Revisão completa do risk register pelo C-Level Squad
2. Análise de tendências e padrões
3. Identificação de riscos emergentes e sistémicos
4. Reavaliação de risk appetite organizacional
5. Actualização de thresholds se necessário

---

## Reporting

### Risk Dashboard
- Heatmap de riscos (probabilidade × impacto)
- Top 10 riscos por severidade
- Trend de riscos abertos ao longo do tempo
- Distribuição por categoria
- Tempo médio de mitigação
- Riscos vencidos (overdue review)

### Risk Report (Mensal)
- Novos riscos identificados no período
- Riscos mitigados ou fechados
- Mudanças de classificação significativas
- Eficácia das mitigações
- Risk appetite vs exposição actual
- Recomendações para o próximo período

---

## Notas Técnicas

- Risk register em `data/risks/`
- Sinais recolhidos via APIs e webhooks dos sistemas fonte
- Alertas distribuídos via Slack, email e SMS conforme severidade
- Histórico mantido por mínimo 3 anos
- Revisão anual dos thresholds e categorias de sinais
