# Script: Gerador de Relatório de Risco

## Objetivo
Gerar automaticamente relatórios de gestão de risco consolidando riscos de todas as áreas da organização, tracking de mitigações e evolução da postura de risco ao longo do tempo. Alimenta reuniões de C-Level, board e comitês de risco.

## Inputs
| Input | Tipo | Obrigatório | Descrição |
|-------|------|:-----------:|-----------|
| `risk_register` | YAML/JSON | Sim | Registro completo de riscos |
| `period` | string | Sim | Período do relatório (ex: "Q1-2026" ou "Mar-2026") |
| `previous_report` | JSON | Não | Relatório anterior para comparação |
| `incidents` | JSON | Não | Incidentes ocorridos no período |
| `mitigations_status` | JSON | Não | Status das ações de mitigação |
| `audience` | string | Não | `clevel` | `board` | `operational` | `full` |

## Outputs
- Relatório de risco completo em Markdown
- Dashboard resumido (versão executiva)
- Heat map de riscos (representação em texto)
- Trend analysis (evolução dos riscos)
- Alertas para riscos novos ou escalados

---

## Lógica do Script

### Fase 1: Consolidação do Registro de Riscos

```
CARREGAR risk_register:
  PARA cada risco:
    VALIDAR campos obrigatórios:
      - id, título, categoria, probabilidade, impacto
      - owner, status, mitigação, data_identificação
    CALCULAR severidade = probabilidade x impacto
    CLASSIFICAR em quadrante do heat map

AGREGAR por categoria:
  - Estratégico: [riscos]
  - Operacional: [riscos]
  - Financeiro: [riscos]
  - Tecnológico: [riscos]
  - Legal/Regulatório: [riscos]
  - People: [riscos]
  - Reputacional: [riscos]

CALCULAR estatísticas:
  - Total de riscos ativos
  - Distribuição por severidade (Crítico/Alto/Médio/Baixo)
  - Distribuição por categoria
  - Riscos sem owner (flag como ERROR)
  - Mitigações atrasadas
```

### Fase 2: Análise de Evolução

```
SE previous_report disponível:
  COMPARAR com período anterior:
    - Riscos novos (apareceram neste período)
    - Riscos escalados (aumentaram de severidade)
    - Riscos mitigados (reduziram de severidade)
    - Riscos encerrados (removidos do registro)
    - Riscos materializados (se tornaram incidentes)
  
  CALCULAR tendência da postura de risco:
    risk_score_atual = soma(severidade de cada risco ativo)
    risk_score_anterior = soma do período anterior
    tendência = (risk_score_atual - risk_score_anterior) / risk_score_anterior

SE incidents disponível:
  CRUZAR incidentes com registro de riscos:
    - Incidentes que correspondem a riscos identificados: "Risk materializado"
    - Incidentes não previstos: "Blind spot" — criar novo risco
  CALCULAR taxa de predição = riscos materializados com mitigação / total materializados
```

### Fase 3: Geração de Alertas

```
GERAR alerta para:
  - Risco CRÍTICO novo: [CRITICAL] Novo risco crítico identificado
  - Risco escalou para CRÍTICO: [CRITICAL] Risco {id} escalou
  - Mitigação atrasada > 30 dias: [WARNING] Mitigação atrasada
  - Risco sem owner: [ERROR] Risco {id} sem responsável
  - Categoria com > 3 riscos altos: [WARNING] Concentração de risco
  - Risco materializado sem mitigação prévia: [ALERT] Blind spot

PRIORIZAR alertas por severidade e urgência
```

### Fase 4: Geração do Relatório

```
SELECIONAR template baseado em audience:
  board: Resumido, foco em top 5 riscos e postura geral
  clevel: Detalhado, com mitigações e ações
  operational: Completo, com todos os riscos e procedimentos
  full: Tudo acima combinado

GERAR seções:
  1. Dashboard executivo (sempre)
  2. Heat map visual (sempre)
  3. Top riscos detalhados (sempre)
  4. Evolução e tendência (se histórico disponível)
  5. Status de mitigações (clevel+)
  6. Incidentes relacionados (se dados disponíveis)
  7. Recomendações (sempre)
```

---

## Template do Relatório

```markdown
# Relatório de Gestão de Riscos — {period}
**Gerado em:** {date}
**Responsável:** {owner}
**Audiência:** {audience}

---

## Dashboard Executivo

**Postura de risco geral:** {posture} ({trend} vs período anterior)

| Severidade | Quantidade | Var vs Anterior |
|-----------|:---------:|:-:|
| Crítico | {n_critical} | {var} |
| Alto | {n_high} | {var} |
| Médio | {n_medium} | {var} |
| Baixo | {n_low} | {var} |
| **Total ativos** | **{total}** | **{var}** |

| Status | Quantidade |
|--------|:---------:|
| Novos neste período | {n_new} |
| Escalados | {n_escalated} |
| Mitigados/Reduzidos | {n_mitigated} |
| Encerrados | {n_closed} |
| Materializados | {n_materialized} |

---

## Heat Map

```
              │ Baixo Impacto │ Médio Impacto │ Alto Impacto │
──────────────┼───────────────┼───────────────┼──────────────┤
Alta Prob.    │   {risks}     │   {risks}     │  {risks}     │
──────────────┼───────────────┼───────────────┼──────────────┤
Média Prob.   │   {risks}     │   {risks}     │  {risks}     │
──────────────┼───────────────┼───────────────┼──────────────┤
Baixa Prob.   │   {risks}     │   {risks}     │  {risks}     │
──────────────┴───────────────┴───────────────┴──────────────┘
```

---

## Alertas

{PARA cada alerta:}
[{severity}] {risk_id}: {alert_message}

---

## Top 5 Riscos

{PARA cada top risco:}
### R{n}: {risk_title}

| Campo | Valor |
|-------|-------|
| Categoria | {category} |
| Severidade | {severity} |
| Probabilidade | {probability} ({justification}) |
| Impacto | {impact} ({quantification}) |
| Owner | {owner} |
| Status da mitigação | {mitigation_status} |
| Trigger | {trigger_indicator} |

**Mitigação:** {mitigation_description}
**Contingência:** {contingency_plan}
**Evolução:** {trend_vs_previous}

---

## Evolução da Postura de Risco

| Período | Risk Score | Críticos | Altos | Tendência |
|---------|:---------:|:--------:|:-----:|:---------:|
| {period_n-3} | {score} | {n} | {n} | — |
| {period_n-2} | {score} | {n} | {n} | {trend} |
| {period_n-1} | {score} | {n} | {n} | {trend} |
| **{period_atual}** | **{score}** | **{n}** | **{n}** | **{trend}** |

---

## Status das Mitigações

| Risco | Mitigação | Owner | Prazo | Status | Atraso |
|-------|----------|-------|-------|:------:|:------:|
{PARA cada mitigação:}
| {risk_id} | {action} | {owner} | {deadline} | {status} | {days_overdue} |

**Mitigações no prazo:** {n}/{total} ({pct}%)
**Mitigações atrasadas:** {n} — ação de follow-up necessária

---

## Recomendações

| # | Recomendação | Prioridade | Impacto | Owner Sugerido |
|---|-------------|:---------:|:------:|---------------|
| 1 | {recommendation} | {priority} | {impact} | {suggested_owner} |
| 2 | {recommendation} | {priority} | {impact} | {suggested_owner} |
| 3 | {recommendation} | {priority} | {impact} | {suggested_owner} |
```

---

## Registro de Riscos (Input Format)

```yaml
# risks/register.yaml
risks:
  - id: "R-001"
    title: "Perda de key engineer (arquiteto do core)"
    category: "people"
    probability: "alta"  # alta/media/baixa
    impact: "alto"  # alto/medio/baixo
    owner: "CTO — João Silva"
    status: "ativo"  # ativo/monitorando/mitigado/encerrado/materializado
    identified_date: "2026-01-15"
    trigger: "Engenheiro recebe oferta ou menciona insatisfação"
    mitigation: "Retention package + knowledge sharing sessions semanais"
    mitigation_status: "em_andamento"
    mitigation_deadline: "2026-02-28"
    contingency: "Contratar consultoria especializada + priorizar documentação"
    financial_impact: "R$ 500K (3 meses de atraso em roadmap)"
```

---

## Exemplo de Execução

```
$ ./risk-report-generator.sh \
  --register risks/register.yaml \
  --period "Q1-2026" \
  --previous reports/risks/q4-2025-report.json \
  --incidents data/incidents-q1.json \
  --audience clevel

Processando 28 riscos ativos...
  Críticos: 3 | Altos: 8 | Médios: 12 | Baixos: 5
  Novos: 4 | Escalados: 2 | Mitigados: 5 | Encerrados: 3
  Materializados: 1 (R-012: incidente de segurança — tinha mitigação parcial)

Alertas gerados: 4
  [CRITICAL] R-027: Novo risco crítico — regulação LGPD para AI features
  [WARNING] R-005: Mitigação atrasada 45 dias — renegociação de contrato cloud
  [ALERT] Blind spot: Incidente INC-2026-008 não corresponde a nenhum risco mapeado
  [WARNING] Categoria "tecnológico" com 4 riscos altos — concentração de risco

Relatório gerado: reports/risks/q1-2026-report.md
Postura de risco: Elevada (risk score: 47, anterior: 38, +24%)
```

---

## Cadência
- **Mensal:** Relatório operacional para C-Level
- **Trimestral:** Relatório completo para board
- **Ad-hoc:** Quando risco crítico novo é identificado

---

## Dicas de Uso
- Registro de riscos é documento vivo — atualize continuamente, não apenas para o relatório
- Risco sem owner é risco ignorado — TODOS devem ter responsável
- Mitigações atrasadas são tão perigosas quanto riscos novos — track rigorosamente
- Blind spots (incidentes não previstos) são os insights mais valiosos
- Postura de risco subindo trimestre após trimestre é sinal de alerta sério
- Para board, foque nos top 5 e na tendência — não apresente todos os 30+ riscos
