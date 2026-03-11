# Plan and Execute Pricing Test

## Objetivo
Planejar e executar um teste de pricing estruturado para validar ou otimizar a estratégia de preços. Pricing é a alavanca mais poderosa de receita — um aumento de 1% no preço pode gerar 8-11% de aumento em profit. Testes mal desenhados, porém, podem destruir confiança do cliente e danificar a marca.

## Agente Responsável
- **CMO Agent** — Ownership do design e execução do teste

## Agentes de Suporte
- **CFO Agent** — Modelagem financeira e P&L impact analysis
- **CEO Agent** — Aprovação de pricing strategy e risk tolerance
- **CPO Agent** — Value metric alignment e product packaging
- **CTO Agent** — Technical implementation do teste (A/B infrastructure)
- **COO Agent** — Operational readiness para novos preços

## Pré-requisitos
1. Pricing atual documentado (tiers, features, prices, discounting rules)
2. Unit economics atualizados (CAC, LTV, gross margin por tier)
3. Competitive pricing intelligence
4. Customer willingness-to-pay data (surveys, win/loss data, churn reasons)
5. Technical capability para executar A/B test ou phased rollout
6. Legal review de pricing changes (se necessário)
7. Customer communication plan approval

## Processo (step-by-step)

### Fase 1: Hypothesis e Design (Semana 1)
1. Definir a hypothesis de pricing: o que acreditamos e por quê
2. Determinar o que testar: price point, packaging, value metric, discounting, freemium boundary
3. Definir segmentos de teste: new customers, existing customers, specific segments
4. Desenhar variações: control (current) vs treatment(s) — max 3 variações
5. Calcular sample size necessário para statistical significance
6. Definir duração mínima do teste (geralmente 4-8 semanas)
7. Definir success metrics: conversion rate, ARPU, churn impact, revenue per visitor

### Fase 2: Financial Modeling (Semana 1-2)
8. Modelar impacto financeiro de cada variação: revenue, margin, LTV
9. Calcular worst-case scenario: quanto revenue at risk no teste
10. Definir "guardrails": métricas que se cruzadas, param o teste automaticamente
11. Modelo de break-even: em quanto tempo o novo pricing paga o investimento do teste
12. Avaliar impacto em diferentes cohorts: SMB vs Enterprise, monthly vs annual
13. Calcular elasticidade de preço estimada baseada em dados históricos

### Fase 3: Implementation (Semana 2-3)
14. CTO implementa infraestrutura de teste (feature flags, A/B test framework)
15. Preparar pricing page variations
16. Configurar tracking e analytics para todas as métricas definidas
17. Treinar sales team em novos prices (talk tracks, objection handling, discounting authority)
18. Preparar customer communication para variações que afetam clientes existentes
19. Legal review final se houver termos contratuais impactados
20. QA completo: verificar que billing system processa corretamente

### Fase 4: Execution e Monitoring (Semana 3-8)
21. Lançar teste com monitoramento diário das métricas
22. Primeira análise em T+7: sinais iniciais e verificação de instrumentation
23. Check-in semanal: métricas vs guardrails, qualitative feedback
24. Monitorar efeitos secundários: support tickets, churn rate, NPS changes
25. Não interromper o teste prematuramente (a menos que guardrails sejam cruzados)
26. Coletar qualitative feedback de sales team e customers

### Fase 5: Analysis e Decision (Semana 8-9)
27. Compilar resultados finais com statistical significance test
28. Analisar por segment: o efeito é uniforme ou varia por cohort?
29. Calcular impacto anualizado de cada variação
30. Preparar recommendation com confidence level
31. Apresentar resultados para executive team
32. Decidir: rollout, iterate ou revert

## Frameworks a Aplicar
- **Van Westendorp Price Sensitivity** — Para descobrir range de preço aceitável
- **Conjoint Analysis** — Para testar tradeoffs entre features e preço
- **Price Elasticity Estimation** — Sensibilidade da demanda a mudanças de preço
- **Value-Based Pricing** — Precificar pelo valor entregue, não pelo custo
- **Good/Better/Best Framework** — 3-tier packaging structure
- **Penny Gap Analysis** — Testar a barreira free-to-paid

## Checklists de Qualidade
- [ ] Hypothesis de pricing documentada com rationale
- [ ] Variações definidas (max 3 + control)
- [ ] Sample size calculado para statistical significance
- [ ] Financial impact modelado para cada variação
- [ ] Guardrails definidos (auto-stop conditions)
- [ ] Technical implementation QA'd
- [ ] Sales team treinado nos novos prices
- [ ] Customer communication preparada
- [ ] Legal review completo (se necessário)
- [ ] Tracking e analytics configurados
- [ ] Test duration definida (min 4 semanas)
- [ ] Results analysis plan definido antes do launch

## Template de Entrega
```markdown
# Pricing Test — [Test Name]

## Hypothesis
[O que acreditamos e por que queremos testar]

## Test Design
- **Type:** [A/B / Phased / Segment-based]
- **Duration:** [X weeks]
- **Sample Size:** [N per variant]
- **Segments:** [Who is included]

## Variations
| Variant | Price/Packaging | Hypothesis | Expected Impact |
|---------|----------------|------------|-----------------|
| Control | [Current] | Baseline | — |
| Variant A | [Change] | [Why] | [Expected] |
| Variant B | [Change] | [Why] | [Expected] |

## Financial Model
| Scenario | Revenue Impact | Margin Impact | LTV Impact |
|----------|---------------|---------------|------------|
| Variant A wins | | | |
| Variant B wins | | | |
| Worst case | | | |

## Guardrails (Auto-Stop)
| Metric | Threshold | Action |
|--------|-----------|--------|
| Conversion Rate | <[X%] drop | Stop test |
| Churn Rate | >[X%] increase | Stop test |
| NPS | <[X] drop | Review |

## Results
| Metric | Control | Variant A | Variant B | Significance |
|--------|---------|-----------|-----------|-------------|
| Conversion | | | | p=[X] |
| ARPU | | | | p=[X] |
| Churn | | | | p=[X] |

## Recommendation
- **Winner:** [Variant X]
- **Confidence:** [High/Medium/Low]
- **Annualized Impact:** [R$ X]
- **Decision:** [Rollout / Iterate / Revert]

## Rollout Plan
[If rolling out, timeline and communication plan]
```

## Registries para Atualizar
- `registries/decisions-log.md` — Decisão de pricing e rationale
- `registries/metrics-log.md` — Test results e baselines
- `registries/experiments-log.md` — Teste documentado com learnings
- `registries/competitive-intelligence.md` — Positioning vs competitors updated

## Critérios de Aceitação
1. Teste desenhado com hypothesis clara e variações definidas
2. Financial modeling completo com worst-case scenario
3. Guardrails definidos e monitorados durante o teste
4. Teste executado pela duração mínima definida
5. Resultados analisados com statistical significance
6. Decisão tomada (rollout/iterate/revert) com rationale
7. Learnings documentados para futuros testes

## Dependências e Handoffs
- **Recebe de:** Market Research (CMO), Product Analytics (CPO), Financial Data (CFO)
- **Entrega para:** Sales Enablement, Billing System, Customer Communication
- **Cadência:** Ad-hoc (triggered por strategic need, max 2 testes simultâneos)
- **Timeline típico:** 8-10 semanas end-to-end
- **Escalation path:** Guardrails cruzados escalam imediatamente para CEO
