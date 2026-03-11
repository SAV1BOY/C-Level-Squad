# Script: Gerador de Relatório Semanal

## Objetivo
Gerar automaticamente relatórios semanais de status para times ou projetos, consolidando métricas, progresso de OKRs, bloqueios e próximos passos. Reduz trabalho manual de reporting e garante consistência no formato.

## Inputs
| Input | Tipo | Obrigatório | Descrição |
|-------|------|:-----------:|-----------|
| `team_name` | string | Sim | Nome do time ou projeto |
| `period_start` | date | Sim | Início da semana (segunda-feira) |
| `period_end` | date | Sim | Fim da semana (sexta-feira) |
| `okrs` | JSON/YAML | Sim | OKRs do time com status atual |
| `metrics` | JSON/YAML | Não | Métricas-chave com valores atuais e anteriores |
| `highlights` | list | Não | Lista de destaques da semana |
| `blockers` | list | Não | Lista de bloqueios |
| `next_week` | list | Não | Plano para próxima semana |
| `template` | string | Não | Template customizado (default: padrão) |

## Outputs
- Relatório em Markdown formatado
- Versão compacta para Slack (opcional)
- Histórico de relatórios para comparação (append ao arquivo de histórico)

---

## Lógica do Script

### Fase 1: Coleta de Dados

```
1. CARREGAR configuração do time:
   - Nome e membros
   - OKRs do quarter atual
   - Métricas monitoradas e suas fontes

2. CARREGAR dados da semana:
   - SE fonte automática (Jira, Linear, GitHub):
     - CONSULTAR API para tasks completadas
     - CONSULTAR API para PRs merged
     - CALCULAR velocity / throughput
   - SE input manual:
     - CARREGAR do arquivo de input

3. CARREGAR dados da semana anterior (para comparação):
   - BUSCAR último relatório gerado
   - EXTRAIR métricas para calcular variação
```

### Fase 2: Processamento

```
PARA cada OKR do time:
  CALCULAR progresso atual (%)
  COMPARAR com semana anterior
  DETERMINAR status: On Track | At Risk | Off Track
  CALCULAR confiança de atingimento no prazo

PARA cada métrica monitorada:
  CALCULAR variação semana-sobre-semana
  DETERMINAR tendência: Subindo | Estável | Caindo
  COMPARAR com meta
  GERAR flag se variação > threshold (ex: >10%)

CONSOLIDAR highlights:
  SE fonte automática: EXTRAIR top entregas do tracking tool
  COMPLEMENTAR com inputs manuais

CONSOLIDAR bloqueios:
  CLASSIFICAR por severidade
  IDENTIFICAR owner para resolução
  CALCULAR dias bloqueado
```

### Fase 3: Geração do Relatório

```
APLICAR template:
  SUBSTITUIR variáveis por dados calculados
  FORMATAR tabelas com alinhamento
  ADICIONAR indicadores visuais (emojis/flags para status)
  GERAR versão compacta para Slack

SALVAR relatório:
  ARQUIVO: reports/{team}/{year}/week-{N}.md
  APPEND ao histórico: reports/{team}/history.md
```

---

## Template Padrão do Relatório

```markdown
# Relatório Semanal — {team_name}
**Semana {week_number}:** {period_start} a {period_end}
**Autor:** {author} | **Gerado em:** {generation_date}

---

## TL;DR
- **Status geral:** {overall_status}
- **Principal conquista:** {top_highlight}
- **Principal bloqueio:** {top_blocker}

---

## Métricas da Semana

| Métrica | Sem. Anterior | Esta Semana | Variação | Meta | Status |
|---------|:-:|:-:|:-:|:-:|:-:|
{PARA cada métrica:}
| {metric_name} | {previous_value} | {current_value} | {variation} | {target} | {status_flag} |

---

## Progresso OKRs — Q{quarter}

| Objective | KR | Target | Atual | % | Status | Var Semanal |
|-----------|-----|--------|-------|:-:|:------:|:-:|
{PARA cada OKR:}
| {objective} | {kr_description} | {target} | {current} | {progress}% | {status} | {weekly_change} |

---

## Destaques da Semana
{PARA cada highlight:}
- {highlight_description}

---

## Bloqueios
{SE bloqueios existem:}
| Bloqueio | Severidade | Dias Bloqueado | Owner | Ação Necessária |
|----------|:---------:|:-:|-------|----------------|
{PARA cada bloqueio:}
| {blocker_description} | {severity} | {days_blocked} | {owner} | {action_needed} |

{SE sem bloqueios:}
Nenhum bloqueio esta semana.

---

## Próxima Semana
{PARA cada item:}
- {next_week_item}

---

## Comparativo com Semana Anterior

| Dimensão | Semana Anterior | Esta Semana | Tendência |
|----------|:-:|:-:|:-:|
| Tasks concluídas | {prev_tasks} | {curr_tasks} | {trend} |
| PRs merged | {prev_prs} | {curr_prs} | {trend} |
| Bugs resolvidos | {prev_bugs} | {curr_bugs} | {trend} |
| Velocity (story points) | {prev_velocity} | {curr_velocity} | {trend} |
```

---

## Versão Compacta (Slack)

```
*{team_name} — Week {week_number}*
Status: {status_emoji} {overall_status}

Destaques:
• {highlight_1}
• {highlight_2}

Métricas: {metric_1_name}: {value} ({variation}) | {metric_2_name}: {value} ({variation})

OKRs: {ok_count}/{total_count} on track

{SE bloqueios:}
Bloqueio: {top_blocker} — precisamos de {action}

Full report: {link_to_full_report}
```

---

## Exemplo de Execução

```
$ ./weekly-report-generator.sh \
  --team "Time Pagamentos" \
  --start "2026-03-09" \
  --end "2026-03-13" \
  --format markdown+slack

Coletando dados...
  - Linear API: 23 tasks completadas, 8 PRs merged
  - OKRs: 3/4 on track
  - Métricas: 2 com variação significativa

Gerando relatório...
  - Full report: reports/pagamentos/2026/week-11.md
  - Slack version: reports/pagamentos/2026/week-11-slack.txt
  - Histórico atualizado: reports/pagamentos/history.md

Relatório gerado com sucesso.

Resumo:
  Status: On Track
  Tasks: 23 (+4 vs semana anterior)
  OKRs: 3/4 on track (KR2 do O2 at risk — churn acima do esperado)
  Bloqueios: 1 (integração com gateway bancário — aguardando resposta do parceiro)
```

---

## Configuração

```yaml
# config/weekly-report.yaml
team:
  name: "Time Pagamentos"
  members: ["Ana", "Bruno", "Carlos", "Diana"]
  
sources:
  tasks: "linear"  # ou "jira", "github_projects", "manual"
  metrics: "datadog"  # ou "manual"
  
metrics:
  - name: "Latência p99"
    source: "datadog"
    query: "avg:payment.latency.p99{env:production}"
    target: 200  # ms
    alert_threshold: 10  # % variação
  - name: "Taxa de sucesso"
    source: "datadog"
    query: "..."
    target: 99.5  # %

output:
  format: ["markdown", "slack"]
  directory: "reports/{team}/{year}/"
  slack_channel: "#pagamentos-updates"
```

---

## Dicas de Uso
- Automatize o máximo possível — menos trabalho manual = mais consistência
- Gere o relatório na sexta-feira à tarde ou segunda de manhã
- Versão Slack é para visibilidade rápida, link para relatório completo quando necessário
- Mantenha histórico — tendências são mais valiosas que snapshots
- Se o relatório nunca tem bloqueios, as pessoas não estão sendo honestas
- Customize métricas por time — cada time tem KPIs diferentes
