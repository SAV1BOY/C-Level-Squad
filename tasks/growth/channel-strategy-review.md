# Channel Strategy Review

## Objetivo
Revisar a estratégia de canais de distribuição e aquisição, avaliando performance de cada canal, identificando oportunidades de otimização e decidindo onde investir, manter ou descontinuar. A channel strategy determina como o produto chega ao cliente — canais errados significam CAC insustentável e growth limitado.

## Agente Responsável
- **CMO Agent** — Ownership da channel strategy e performance

## Agentes de Suporte
- **CFO Agent** — Unit economics por canal e ROI analysis
- **CPO Agent** — Product-channel fit e self-serve optimization
- **CEO Agent** — Strategic partnerships e channel bets
- **COO Agent** — Operational capacity por canal
- **CTO Agent** — Technical infrastructure de cada canal

## Pré-requisitos
1. Dados de performance por canal (últimos 6-12 meses)
2. CAC, LTV e payback period por canal
3. Attribution model implementado e confiável
4. Competitive channel analysis
5. Customer research sobre descoberta e decisão de compra
6. Budget allocation atual por canal

## Processo (step-by-step)

### Fase 1: Channel Performance Audit (2-3 dias)
1. Mapear todos os canais ativos: paid, organic, partnerships, referral, sales, events, etc.
2. Para cada canal, compilar: volume (leads/users), conversion rate, CAC, LTV, payback period
3. Calcular channel efficiency score: (LTV - CAC) / CAC para cada canal
4. Analisar trends de 6-12 meses: canais melhorando vs. deteriorando
5. Identificar channel saturation signals: diminishing returns em spend increase
6. Avaliar attribution confidence: quão confiáveis são os dados de cada canal
7. Mapear customer journey por canal: como diferentes canais se complementam

### Fase 2: Strategic Assessment (1-2 dias)
8. Classificar canais por stage: awareness, acquisition, activation, expansion
9. Avaliar channel-market fit: o canal alcança o ICP eficientemente?
10. Analisar competitive channel strategy: onde competidores investem
11. Identificar canais underinvested com potencial de crescimento
12. Avaliar riscos de concentração: dependência excessiva de um canal
13. Identificar emerging channels relevantes para o mercado
14. Avaliar channel mix por segment: SMB vs Mid-Market vs Enterprise

### Fase 3: Optimization Planning (1-2 dias)
15. Para cada canal, recomendar: invest more, maintain, optimize, or sunset
16. Calcular reallocation de budget proposta com expected impact
17. Identificar quick wins de otimização em canais existentes
18. Propor novos canais para teste (com hypothesis e test design)
19. Definir targets por canal para o próximo trimestre
20. Calcular headcount needs para suportar a channel strategy atualizada

### Fase 4: Review e Decisão (1 dia)
21. Apresentar channel performance data para executive team
22. Propor reallocation de budget e justify com data
23. Decidir canais para sunset e transition plan
24. Aprovar novos canais para teste
25. Definir cadência de review going forward

## Frameworks a Aplicar
- **Channel Efficiency Matrix** — Plot canais por volume vs. efficiency (LTV/CAC)
- **Bullseye Framework** — Priorizar canais com testes rápidos
- **Channel-Market Fit** — Cada segmento tem canais naturais, não forçar fit
- **Attribution Modeling** — Multi-touch attribution para entender channel interplay
- **Diminishing Returns Analysis** — Identificar ponto de saturação por canal
- **Portfolio Theory** — Diversificar canais como portfolio de investimento

## Checklists de Qualidade
- [ ] Todos os canais ativos catalogados com métricas
- [ ] CAC e LTV calculados por canal com confidence level
- [ ] Trends de 6-12 meses analisados
- [ ] Channel concentration risk avaliado
- [ ] Competitive channel strategy mapeada
- [ ] Quick wins identificados
- [ ] Budget reallocation proposta com expected ROI
- [ ] Canais para sunset identificados com transition plan
- [ ] Novos canais para teste propostos com hypothesis
- [ ] Targets por canal definidos para próximo período

## Template de Entrega
```markdown
# Channel Strategy Review — [Period]

## Channel Portfolio Overview
| Channel | Stage | Volume | CAC | LTV | LTV/CAC | Payback | Trend | Recommendation |
|---------|-------|--------|-----|-----|---------|---------|-------|---------------|
| Organic Search | Awareness | | | | | | | |
| Paid Search | Acquisition | | | | | | | |
| Content/Blog | Awareness | | | | | | | |
| Social Media | Awareness | | | | | | | |
| Email | Activation | | | | | | | |
| Referral | Acquisition | | | | | | | |
| Partnerships | Acquisition | | | | | | | |
| Direct Sales | Acquisition | | | | | | | |
| Events | Awareness | | | | | | | |

## Channel Mix by Segment
| Segment | Primary Channel | Secondary | Tertiary |
|---------|----------------|-----------|----------|
| SMB | | | |
| Mid-Market | | | |
| Enterprise | | | |

## Concentration Risk
- **Top Channel Share:** [X% of pipeline from Channel Y]
- **Risk Assessment:** [High/Medium/Low]
- **Mitigation:** [Diversification plan]

## Budget Reallocation Proposal
| Channel | Current Budget | Proposed Budget | Change | Expected Impact |
|---------|---------------|----------------|--------|-----------------|

## New Channels to Test
| Channel | Hypothesis | Test Budget | Duration | Success Criteria |
|---------|-----------|-------------|----------|-----------------|

## Channels to Sunset
| Channel | Reason | Transition Plan | Timeline | Savings |
|---------|--------|----------------|----------|---------|

## Targets (Next Quarter)
| Channel | Volume Target | CAC Target | Pipeline Target |
|---------|-------------|------------|-----------------|
```

## Registries para Atualizar
- `registries/metrics-log.md` — Channel metrics atualizados
- `registries/resource-allocation.md` — Budget allocation por canal
- `registries/decisions-log.md` — Decisões de invest/sunset
- `registries/experiments-log.md` — Novos canais a testar

## Critérios de Aceitação
1. Todos os canais auditados com métricas completas
2. LTV/CAC calculado por canal com confiança
3. Reallocation proposta com modeling de impacto
4. Canais para sunset com transition plan
5. Novos canais com test hypothesis
6. Targets por canal definidos para próximo período
7. Budget aprovado pelo CFO

## Dependências e Handoffs
- **Recebe de:** Marketing Analytics, CRM Data, Financial Data (CFO)
- **Entrega para:** Marketing Execution, Budget Allocation, Sales Enablement
- **Cadência:** Trimestral (deep review) + Mensal (light check)
- **Escalation path:** Channel com LTV/CAC <1x escala para CEO
- **Integração:** Alimenta GTM Plan e Quarterly Planning
