# Metrics Pack Builder

> Script para construção automatizada de metrics packs para reuniões de revisão e reports executivos.

---

## Objetivo

O metrics pack é o documento central de dados que alimenta todas as revisões de negócio.
Este script automatiza a coleta, formatação, visualização e distribuição dos dados,
garantindo consistência e pontualidade em cada ciclo de revisão.

---

## Fontes de Dados

### Fontes Primárias
| Fonte | Tipo de Dado | Frequência | Responsável |
|-------|-------------|------------|-------------|
| Finance System | Revenue, P&L, cash flow, burn rate | Diário | CFO / Finance team |
| CRM | Pipeline, deals, churn, expansion | Diário | CRO / Sales ops |
| Product Analytics | WAU, DAU, activation, retention | Real-time | Product team |
| Engineering Dashboard | Uptime, deploys, incidents, velocity | Real-time | CTO / Engineering |
| HR System | Headcount, turnover, engagement | Semanal | CPO / People ops |
| Marketing Analytics | CAC, LTV, funnel, campaigns | Diário | CMO / Marketing ops |
| AI Platform | Model accuracy, adoption, cost per inference | Diário | CAIO / AI ops |

### Fontes Secundárias
- Pesquisas de NPS e satisfação do cliente
- Dados de mercado e competidores (fontes externas)
- Benchmarks de indústria atualizados trimestralmente
- Dados de compliance e regulatório

---

## Processo de Coleta

### Passo 1 — Data Extraction
- Conectar a cada fonte via API ou export automatizado
- Validar completude dos dados (não aceitar datasets com >5% de missing values)
- Aplicar transformações padronizadas (currency conversion, timezone normalization)
- Registrar timestamp de extração para auditoria

### Passo 2 — Data Validation
- Verificar consistência entre fontes (ex: revenue no CRM vs. Finance)
- Identificar outliers usando desvio padrão (flag se >2σ do histórico)
- Comparar contra períodos anteriores para detectar anomalias
- Gerar relatório de qualidade de dados com score de confiança

### Passo 3 — Cálculo de Métricas Derivadas
- Calcular taxas de crescimento (WoW, MoM, QoQ, YoY)
- Gerar projeções baseadas em tendência (linear e exponential smoothing)
- Calcular variance contra forecast e targets
- Determinar health scores compostos para cada área

---

## Formatação do Metrics Pack

### Estrutura Padrão
```
1. Executive Summary (1 página)
   - 5 métricas headline com tendência
   - Alertas críticos (vermelho)
   - Decisões necessárias

2. Financial Metrics (2-3 páginas)
   - Revenue breakdown
   - Unit economics
   - Cash position e runway

3. Growth Metrics (2-3 páginas)
   - User metrics (acquisition, activation, retention)
   - Funnel performance
   - Cohort analysis

4. Product & Engineering (2-3 páginas)
   - Reliability metrics
   - Velocity metrics
   - Tech debt indicators

5. People Metrics (1-2 páginas)
   - Headcount e hiring velocity
   - Engagement e retention
   - DEI progress

6. AI & Innovation (1-2 páginas)
   - AI adoption metrics
   - Model performance
   - Innovation pipeline
```

---

## Visualização

### Princípios de Design
- Usar sistema de cores consistente: verde (on-track), amarelo (at-risk), vermelho (off-track)
- Cada métrica deve ter: valor atual, target, variance, tendência (sparkline)
- Gráficos devem mostrar no mínimo 8 semanas de histórico para WBR, 12 meses para MBR
- Evitar gráficos 3D, pie charts e decorações desnecessárias
- Usar anotações para marcar eventos relevantes (launches, incidents, holidays)

### Tipos de Visualização por Métrica
| Tipo de Métrica | Visualização Recomendada |
|----------------|------------------------|
| Tendência temporal | Line chart com sparkline |
| Comparação de categorias | Horizontal bar chart |
| Distribuição | Histogram ou box plot |
| Composição | Stacked bar chart |
| Correlação | Scatter plot |
| Health score | Gauge ou traffic light |

---

## Distribuição

### Timing de Distribuição
| Tipo de Revisão | Quando Distribuir | Para Quem |
|-----------------|-------------------|-----------|
| WBR | Sexta-feira 18h (para reunião de segunda) | C-Level Squad + directs |
| MBR | 3 dias úteis antes da reunião | C-Level Squad + Board observers |
| Board Pack | 5 dias úteis antes do Board meeting | Board members + C-Level |
| Ad-hoc | Conforme solicitado | Stakeholders definidos |

### Canais de Distribuição
- Armazenamento principal: `data/metrics-packs/` com versionamento
- Notificação via canal dedicado do squad
- Link compartilhável com controle de acesso
- PDF para distribuição offline (Board meetings)

---

## Controle de Qualidade

Antes da distribuição, o metrics pack deve passar por:

1. **Automated checks**: validação de dados, formatação, completude
2. **Owner review**: responsável de cada seção revisa seus números
3. **COO review**: COO Orchestrator faz revisão final de consistência
4. **Version control**: pack é versionado e armazenado para referência futura

---

## Configuração

```yaml
metrics_pack:
  default_period: weekly
  data_freshness_max_hours: 24
  confidence_threshold: 0.95
  visualization_style: minimal
  distribution_format: [markdown, pdf]
  archive_retention_months: 24
```
