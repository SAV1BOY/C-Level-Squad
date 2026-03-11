# Run Monthly Business Review (MBR)

## Objetivo
Executar a Monthly Business Review, uma sessão de 90-120 minutos que analisa a performance mensal com profundidade maior que o WBR. O MBR é o mecanismo de course correction mensal — identifica trends que não são visíveis semanalmente e permite ajustes antes que problemas se tornem crises.

## Agente Responsável
- **COO Agent** — Facilitação e consolidação de dados

## Agentes de Suporte
- **CEO Agent** — Direção estratégica e decisões de priorização
- **CFO Agent** — Financial deep dive e forecast update
- **CTO Agent** — Engineering metrics e capacity review
- **CPO Agent** — Product metrics e roadmap progress
- **CMO Agent** — Marketing performance e pipeline health
- **CHRO Agent** — People metrics, hiring progress, attrition

## Pré-requisitos
1. Financial close do mês concluído (ou estimated close com >95% accuracy)
2. Todas as métricas mensais consolidadas no dashboard
3. OKR progress report atualizado (scoring parcial)
4. Initiative health status de cada área
5. WBR escalations acumuladas do mês
6. Forecast atualizado pelo CFO
7. Cada C-Level preparou seu 1-page monthly update

## Processo (step-by-step)

### Fase 1: Preparação (3-5 dias antes do MBR)
1. CFO fecha ou estima os números financeiros do mês
2. Cada área submete métricas mensais e 1-page update com formato padronizado
3. COO consolida todos os dados em um MBR dashboard unificado
4. Identificar trends mensais: métricas com 2+ semanas consecutivas fora do target
5. Compilar WBR escalations não resolvidas durante o mês
6. Preparar deep dive deck para 1-2 temas que requerem atenção especial
7. Distribuir MBR package com 48h de antecedência para pre-read

### Fase 2: Execução do MBR (90-120 minutos)
8. **[0-10 min]** Financial overview: P&L do mês, cash, forecast vs actual
9. **[10-25 min]** OKR progress review: scoring parcial, on track vs off track
10. **[25-40 min]** Growth review: funnel metrics, pipeline, conversion, churn
11. **[40-55 min]** Product & Tech review: roadmap progress, reliability, incidents
12. **[55-70 min]** People review: hiring, attrition, engagement signals
13. **[70-90 min]** Deep dive: 1-2 temas pré-selecionados que precisam de atenção executiva
14. **[90-110 min]** Decisões e course corrections: o que ajustar para o próximo mês
15. **[110-120 min]** Action items e encerramento

### Fase 3: Post-MBR (Até 48h depois)
16. Publicar MBR report com métricas, insights e decisões
17. Atualizar forecast se MBR revelou desvios significativos
18. Comunicar course corrections para as equipes afetadas
19. Atualizar OKR confidence levels baseado na discussão
20. Flag itens para QBR se necessário
21. Atualizar initiative health status conforme decisões do MBR

## Frameworks a Aplicar
- **Trend Analysis** — Analisar tendências de 3+ meses, não pontos isolados
- **Variance Analysis** — Budget vs actual com explanations para desvios >5%
- **OKR Health Check** — Scoring parcial com confidence level para cada KR
- **Funnel Analysis** — Para métricas de growth (top-of-funnel to revenue)
- **Cohort Analysis** — Para métricas de retention e engagement
- **Forecast Accuracy Tracking** — Comparar forecast anterior com actual

## Checklists de Qualidade
- [ ] Financial close completo (ou estimated com >95% accuracy)
- [ ] Todas as áreas submeteram métricas e 1-page updates
- [ ] MBR package distribuído com 48h de antecedência
- [ ] Trends de 3+ meses analisados (não apenas último mês)
- [ ] OKR progress com scoring parcial documentado
- [ ] WBR escalations do mês endereçados
- [ ] Deep dive preparado com dados e recomendações
- [ ] Decisões de course correction documentadas com owners
- [ ] Forecast atualizado se necessário
- [ ] MBR report publicado em até 48h

## Template de Entrega
```markdown
# MBR Report — [Month Year]

## Executive Summary
[3-5 bullet points com os highlights do mês]

## Financial Performance
| Metric | Budget | Actual | Variance | YTD |
|--------|--------|--------|----------|-----|
| Revenue | | | | |
| COGS | | | | |
| Gross Margin | | | | |
| OpEx | | | | |
| EBITDA | | | | |
| Cash | | | | |

## OKR Progress (Month X of Quarter)
| Objective | Progress | Confidence | Status |
|-----------|----------|------------|--------|
| O1 | [X%] | [High/Med/Low] | On/Off Track |

## Growth Metrics
| Metric | Target | Actual | MoM Change | Trend |
|--------|--------|--------|------------|-------|

## Product & Engineering
| Metric | Target | Actual | Commentary |
|--------|--------|--------|-----------|

## People
| Metric | Value | Trend | Action Needed |
|--------|-------|-------|---------------|
| Headcount | | | |
| Open Roles | | | |
| Attrition | | | |

## Deep Dive: [Topic]
[Analysis and recommendations]

## Course Corrections
| What | Why | New Target | Owner | Deadline |
|------|-----|------------|-------|----------|

## Action Items
| Item | Owner | Deadline |
|------|-------|----------|

## Escalations for QBR
[Items that need quarterly-level attention]
```

## Registries para Atualizar
- `registries/metrics-log.md` — Métricas mensais consolidadas
- `registries/okrs.md` — OKR progress scores atualizados
- `registries/decisions-log.md` — Decisões de course correction
- `registries/forecasts.md` — Forecast atualizado se revisado
- `registries/initiatives.md` — Status de iniciativas atualizado

## Critérios de Aceitação
1. MBR executado mensalmente até dia 10 do mês seguinte
2. Financial data com variância máxima de 5% vs close final
3. Todas as áreas representadas com dados atualizados
4. Course corrections documentadas com owners e deadlines
5. MBR report publicado em até 48h após o meeting
6. OKR confidence levels atualizados

## Dependências e Handoffs
- **Recebe de:** Financial Close (CFO), WBR Escalations, Area Updates, Dashboard Data
- **Entrega para:** Course correction owners, QBR (escalations), Forecast Updates
- **Cadência:** Mensal, entre dia 5-10 do mês seguinte
- **Escalation path:** Issues não resolvidos em 2 MBRs consecutivos escalam para QBR
- **Integração:** MBR informa o quarterly OKR scoring no final de cada trimestre
