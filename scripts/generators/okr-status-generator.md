# Script: Gerador de Status de OKR

## Objetivo
Gerar automaticamente relatórios de status de OKRs com progresso, tendência e previsão de atingimento. Consolida dados de múltiplas fontes para dar visibilidade em tempo real do progresso estratégico.

## Inputs
| Input | Tipo | Obrigatório | Descrição |
|-------|------|:-----------:|-----------|
| `okr_definition` | YAML | Sim | Definição dos OKRs com targets |
| `current_values` | JSON | Sim | Valores atuais de cada KR |
| `period` | string | Sim | Quarter/período (ex: "Q1-2026") |
| `week_number` | int | Sim | Semana do quarter (1-13) |
| `previous_status` | JSON | Não | Status da semana anterior (para tendência) |
| `format` | string | Não | `full` | `compact` | `slack` | `board` |

## Outputs
- Relatório de status formatado (Markdown)
- Versão compacta para Slack
- Versão board (resumida com foco em impacto)
- Projeção de atingimento por KR
- Alertas para KRs em risco

---

## Lógica do Script

### Fase 1: Cálculo de Progresso

```
PARA cada Key Result:
  
  1. CALCULAR progresso atual:
     progress = (current_value - baseline) / (target - baseline) * 100
     SE KR é decrescente (reduzir churn):
       progress = (baseline - current_value) / (baseline - target) * 100
     LIMITAR entre 0% e 120% (permitir overshoot)
  
  2. CALCULAR progresso esperado:
     expected_progress = week_number / total_weeks * 100
     // Para KRs lineares
     // Para KRs não-lineares, usar curva customizada
  
  3. DETERMINAR status:
     SE progress >= expected_progress * 0.9: "On Track" (verde)
     SE progress >= expected_progress * 0.7: "At Risk" (amarelo)
     SE progress < expected_progress * 0.7: "Off Track" (vermelho)
  
  4. CALCULAR confiança de atingimento:
     // Baseado em progresso atual + velocidade de progresso
     velocity = (current_progress - last_week_progress)
     weeks_remaining = total_weeks - week_number
     projected_final = current_progress + (velocity * weeks_remaining)
     confidence = MIN(projected_final / 100, 1.0)
```

### Fase 2: Análise de Tendência

```
PARA cada Key Result:
  COMPARAR progresso com semanas anteriores (últimas 4)
  
  CALCULAR trend:
    SE velocity > 0 e acelerando: "Acelerando"
    SE velocity > 0 e constante: "Progredindo"
    SE velocity ~ 0: "Estagnado"
    SE velocity < 0: "Regredindo"
  
  GERAR projeção visual:
    [=====>-------|------] 45% (meta: semana 7/13 = 54%)
```

### Fase 3: Geração de Alertas

```
GERAR alerta SE:
  - KR muda de "On Track" para "At Risk" (ALERT)
  - KR muda de "At Risk" para "Off Track" (CRITICAL)
  - Progresso estagnado por 3+ semanas (WARNING)
  - Velocidade insuficiente para atingir target no prazo (WARNING)
  - KR atingiu 100% antes do prazo (CELEBRATION)

PRIORIZAR alertas por:
  1. Criticidade do OKR (empresa > time > individual)
  2. Severidade do alerta (critical > alert > warning)
  3. Tempo restante (menos tempo = mais urgente)
```

### Fase 4: Geração do Relatório

```
APLICAR template baseado no formato solicitado:
  full: Relatório completo com detalhes por KR
  compact: Tabela resumida com status
  slack: Versão para post em canal
  board: Versão executiva com impacto em negócio
```

---

## Templates de Output

### Full Report
```markdown
# Status OKRs — {period} — Semana {week}/{total_weeks}
**Gerado em:** {date}
**Score parcial:** {partial_score}/1.0

## Resumo
| Status | Quantidade | % |
|--------|:---------:|:-:|
| On Track | {n_green} | {pct}% |
| At Risk | {n_yellow} | {pct}% |
| Off Track | {n_red} | {pct}% |

## Alertas
{PARA cada alerta:}
- [{severity}] {kr_name}: {alert_message}

---

## Detalhamento

### O1: {objective_title}
**Owner:** {owner} | **Score parcial:** {score}

#### KR1: {kr_description}
| Campo | Valor |
|-------|-------|
| Baseline | {baseline} |
| Target | {target} |
| Atual | {current} |
| Progresso | {progress}% |
| Esperado (semana {week}) | {expected}% |
| Status | {status} |
| Tendência | {trend} |
| Confiança de atingir | {confidence}% |
| Projeção final | {projected_final} |

```
Progresso: [{bar}] {progress}%
Esperado:  [{expected_bar}] {expected}%
```

**Commentary:** {human_input_or_auto_generated}
```

### Compact Report (Slack)
```
*OKRs {period} — Semana {week}/{total_weeks}*

Score parcial: *{score}* | On Track: {green}/{total} | At Risk: {yellow} | Off Track: {red}

{PARA cada Objective:}
*{objective_emoji} O{n}: {title}* — {score}
  {PARA cada KR:}
  {status_emoji} KR{n}: {progress}% ({trend_arrow}) — {one_line_summary}

{SE alertas:}
Alertas: {alert_summary}
```

---

## Definição de OKRs (Exemplo de Input)

```yaml
# okrs/q1-2026.yaml
period: "Q1-2026"
total_weeks: 13
start_date: "2026-01-05"
end_date: "2026-03-27"

objectives:
  - id: "O1"
    title: "Tornar-nos a escolha padrão para PMEs de serviços"
    owner: "Maria Santos"
    key_results:
      - id: "KR1"
        description: "Aumentar ARR de R$ 35M para R$ 42M"
        baseline: 35000000
        target: 42000000
        type: "increasing"
        source: "stripe"
      - id: "KR2"
        description: "Reduzir churn MRR de 3% para 2%"
        baseline: 3.0
        target: 2.0
        type: "decreasing"
        source: "manual"
```

---

## Exemplo de Execução

```
$ ./okr-status-generator.sh \
  --okrs okrs/q1-2026.yaml \
  --values data/current-values.json \
  --week 7 \
  --format full+slack

Calculando progresso...
  O1: 0.68 | O2: 0.55 | O3: 0.72
  Score parcial: 0.65

Alertas:
  [ALERT] O2/KR2 mudou de On Track para At Risk
  [WARNING] O1/KR3 estagnado há 3 semanas

Gerando relatórios...
  Full: reports/okrs/q1-2026-week07.md
  Slack: reports/okrs/q1-2026-week07-slack.txt

Postando no Slack #strategy-updates... OK
```

---

## Cadência
- **Semanal:** Status completo gerado toda segunda-feira
- **Mid-quarter (semana 6-7):** Review profundo com análise de tendência
- **End of quarter (semana 13):** Score final com análise retrospectiva

---

## Dicas de Uso
- Automatize coleta de valores quando possível (Stripe, Datadog, CRM)
- Velocidade é mais importante que progresso absoluto — estagnação é red flag
- Mid-quarter review é o momento de ajustar, não de lamentar
- Alertas devem gerar AÇÃO, não apenas notificação
- Score parcial na semana 7 deveria ser ~0.35-0.50 para OKRs aspiracionais
- Use projeção para antecipar problemas — agir na semana 7 é melhor que na 13
