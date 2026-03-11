# Quarterly Review Builder

> Script para construção da revisão trimestral do C-Level Squad.

---

## Objetivo

Consolidar todos os dados, análises e insights de um trimestre numa revisão
abrangente que permita avaliar performance, recalibrar estratégia e definir
prioridades para o próximo trimestre.

---

## Timeline de Preparação

| Dia | Actividade | Responsável |
|-----|-----------|-------------|
| T-21 | Iniciar recolha de dados de todas as fontes | COO Orchestrator |
| T-14 | Primeiro draft de cada secção pelos owners | Todos os agentes |
| T-10 | Consolidação e cross-check de dados | COO Orchestrator |
| T-7 | Draft integrado completo para review | COO Orchestrator |
| T-5 | Review pelo Vision Chief e feedback | Vision Chief |
| T-3 | Versão final com ajustes | COO Orchestrator |
| T-2 | Distribuição aos participantes | COO Orchestrator |
| T-1 | Preparação de talking points e Q&A | Todos os agentes |
| T-0 | Quarterly Review Meeting | Full Squad |
| T+2 | Distribuição de minutes e action items | COO Orchestrator |
| T+5 | Plano do próximo trimestre finalizado | Full Squad |

---

## Data Collection — Recolha de Dados

### Fontes Automáticas
1. **Metrics Pack Builder**: métricas consolidadas do trimestre
2. **Initiative Health Tracker**: health scores de todas as iniciativas
3. **Decision Log**: todas as decisões tomadas no trimestre
4. **Forecast Accuracy**: precisão das previsões do trimestre
5. **Meeting Effectiveness**: eficácia das reuniões do trimestre
6. **Cross-Squad Effectiveness**: colaboração inter-squads
7. **Risk Register**: evolução dos riscos ao longo do trimestre

### Fontes Manuais
1. **Squad retrospectives**: input de cada agente sobre o trimestre
2. **Stakeholder feedback**: feedback recolhido de stakeholders-chave
3. **Market analysis**: análise de mercado e concorrência actualizada
4. **Strategic assessment**: avaliação do ambiente estratégico
5. **Culture pulse**: percepção da equipa sobre cultura e moral

---

## Estrutura da Quarterly Review

### Secção 1 — Executive Summary (2 páginas)
- Headline do trimestre (1 frase)
- 3-5 highlights principais
- 3-5 lowlights ou challenges
- Outlook para o próximo trimestre
- Key decisions needed

### Secção 2 — OKR Review (3-5 páginas)
Para cada Objective:
```
OBJECTIVE: [Descrição]
Status: [On Track | At Risk | Off Track | Achieved]

Key Results:
- KR1: [Descrição] — Target: [X] — Actual: [Y] — [%]
- KR2: [Descrição] — Target: [X] — Actual: [Y] — [%]
- KR3: [Descrição] — Target: [X] — Actual: [Y] — [%]

Commentary: [Análise do progresso, obstáculos, learnings]
Carry-forward: [O que transita para próximo trimestre]
```

### Secção 3 — Financial Review (3-5 páginas)
- Revenue performance vs budget e YoY
- Cost analysis e eficiência
- Cash flow e posição de caixa
- Unit economics evolution
- Financial forecast accuracy
- Budget proposal para próximo trimestre

### Secção 4 — Operational Performance (3-5 páginas)
- Key operational metrics trend
- Initiative portfolio health overview
- SLA compliance summary
- Incident summary e learnings
- Capacity utilization e planning
- Process improvements implementados

### Secção 5 — Strategic Assessment (2-3 páginas)
- Progresso na execução da estratégia
- Market position e competitive landscape
- Opportunities identificadas
- Threats emergentes
- Strategic pivots necessários (se algum)
- Alignment check com visão de longo prazo

### Secção 6 — People & Culture (2-3 páginas)
- Team composition e changes
- Engagement e satisfaction trends
- Key hires e departures
- Development e upskilling
- Culture observations
- Org design considerations

### Secção 7 — AI & Technology (2-3 páginas)
- AI tools adoption e ROI
- Technology infrastructure changes
- Tech debt evolution
- Security e compliance status
- Innovation pipeline
- Tech strategy alignment

### Secção 8 — Decision Quality & Effectiveness (2 páginas)
- Decision Quality Score trend
- Meeting Effectiveness Score trend
- Cross-Squad Effectiveness Score trend
- Forecast Accuracy trend
- Learnings sobre processo decisório

### Secção 9 — Risk Review (2 páginas)
- Top risks actuais vs início do trimestre
- Riscos materializados e como foram geridos
- Novos riscos identificados
- Risk appetite alignment
- Mitigation effectiveness

### Secção 10 — Next Quarter Plan (3-5 páginas)
- Proposed OKRs para próximo trimestre
- Top priorities (máximo 5)
- Resource allocation plan
- Key milestones e deadlines
- Dependencies e risks a monitorar
- Decision points antecipados

---

## Analysis Framework

### Performance Analysis
Para cada área, aplicar:
1. **What happened**: factos e dados
2. **Why it happened**: root cause analysis
3. **What we learned**: insights e learnings
4. **What we'll do differently**: acções para melhoria

### Trend Analysis
- Comparar trimestre actual com 3 trimestres anteriores
- Identificar tendências persistentes (positivas e negativas)
- Separar signal de noise (significância estatística)
- Projectar tendências para próximo trimestre

### Gap Analysis
- Comparar actual vs targets/OKRs
- Quantificar gaps em cada área
- Identificar root causes dos gaps
- Propor closing actions com timeline

---

## Presentation Format

### Para o C-Level Squad (Internal)
- Documento completo (20-30 páginas)
- Discussão de 3-4 horas
- Foco em analysis e decisões
- Ambiente aberto para debate

### Para Board / Stakeholders
- Versão condensada (10-15 páginas)
- Apresentação de 60-90 minutos
- Foco em resultados e outlook
- Decisões que requerem aprovação

---

## Post-Review Actions

1. **Minutes**: distribuir em 48h com todas as decisões e action items
2. **Decision log**: actualizar com decisões do quarterly review
3. **OKRs**: finalizar OKRs do próximo trimestre em 5 dias
4. **Communication**: cascade para squads e stakeholders
5. **Archive**: guardar pack completo com versão final

---

## Notas Técnicas

- Template base em `templates/quarterly-review-template.md`
- Dados compilados automaticamente via scripts de recolha
- Versões guardadas em `data/quarterly-reviews/YYYY-QN/`
- Historical comparison requer mínimo 4 trimestres de dados
- Integração com todos os scripts de tracking e analysis
