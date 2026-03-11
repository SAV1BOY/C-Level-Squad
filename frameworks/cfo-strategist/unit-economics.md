# Unit Economics Framework — Economia Unitária para Decisões de Crescimento

## Propósito e Contexto

Unit economics é a análise de receita e custo por unidade fundamental do negócio (geralmente
um cliente ou uma transação). É o teste de realidade mais importante para qualquer empresa em
crescimento: "Se eu escalar 10x o que faço hoje, o modelo funciona?" Crescimento sem unit
economics saudáveis é como encher um balde furado — mais rápido você enche, mais rápido vaza.

Este framework vai além do LTV/CAC simplificado. Ele estrutura a análise por cohort, incorpora
payback period, e conecta unit economics com decisões operacionais de go-to-market, produto e
engenharia. É a linguagem comum entre CFO, CEO, CMO e CTO quando discutem investimento em
crescimento.

## Quando Usar

- Na avaliação de viabilidade de novos canais de aquisição
- Na decisão de investir em growth vs. rentabilidade
- Em board meetings e investor updates (métrica obrigatória)
- Ao avaliar viabilidade de novo segmento de mercado
- Quando CAC está subindo ou retention está caindo
- Na definição de pricing e packaging de produtos

## Componentes do Framework

### 1. Métricas Fundamentais

**CAC — Customer Acquisition Cost**
```
CAC = (Gastos com S&M no período) / (Clientes adquiridos no período)

CAC Blended = Total S&M / Total novos clientes
CAC Paid = Gastos pagos / Clientes via canais pagos
CAC por Canal = Gasto do canal / Clientes adquiridos pelo canal
```

**Observações críticas:**
- Incluir salários do time de vendas e marketing (fully loaded)
- Separar CAC de new logos vs. expansion (são dinâmicas diferentes)
- Medir lagged CAC: gasto do mês M gera clientes no mês M+1 ou M+2

**LTV — Lifetime Value**
```
LTV Simples = ARPA × Gross Margin % × (1 / Churn Rate)

LTV por Cohort = Σ (Receita mensal da cohort × Gross Margin %)
                  para cada mês de vida da cohort

LTV Ponderado = Σ (LTV do segmento × % clientes no segmento)
```

**Payback Period**
```
Payback (meses) = CAC / (ARPA × Gross Margin %)
```
- Benchmark SaaS: < 12 meses para SMB, < 18 meses para enterprise
- Payback < 6 meses: possível investir agressivamente em growth
- Payback > 24 meses: modelo precisa de ajuste antes de escalar

### 2. Análise por Cohort

A análise por cohort é essencial para entender se unit economics estão melhorando ou
deteriorando. Cada cohort é um grupo de clientes adquiridos no mesmo período.

**Revenue Retention Curve:**
```
Mês 0: 100% (por definição)
Mês 1: [X]% (retenção do primeiro mês)
Mês 3: [X]% (sinal de product-market fit)
Mês 6: [X]% (retenção de médio prazo)
Mês 12: [X]% (retenção de longo prazo)
Mês 12+: [estabilização? crescimento? queda contínua?]
```

**Net Revenue Retention (NRR):**
```
NRR = (MRR início + Expansion - Contraction - Churn) / MRR início × 100

Benchmarks:
- < 90%: Problema sério (leaky bucket)
- 90-100%: OK para SMB
- 100-120%: Bom (expansion compensa churn)
- > 120%: Excelente (land-and-expand funcionando)
```

### 3. LTV:CAC Ratio

| Ratio | Interpretação | Ação |
|-------|--------------|------|
| < 1:1 | Destruindo valor a cada cliente | Parar de escalar. Corrigir modelo. |
| 1-2:1 | Marginalmente viável | Otimizar CAC ou melhorar retention |
| 3:1 | Benchmark saudável | Manter e considerar investir mais |
| > 5:1 | Possivelmente sub-investindo em growth | Testar aumento de CAC para crescer mais rápido |

### 4. Economia da Transação (para modelos transacionais)

```
Receita por Transação
- COGS direto (processamento, hosting, suporte)
= Contribution Margin por Transação

Contribution Margin × Volume Mensal = Contribution Profit
Contribution Profit - Custos Fixos Alocados = Unit Profit
```

## Processo Passo-a-Passo

### Fase 1: Definição da Unidade (1 semana)
1. Definir qual é a "unidade" do negócio (cliente? transação? assento?)
2. Mapear todas as fontes de receita por unidade
3. Mapear todos os custos atribuíveis por unidade
4. Validar com dados de pelo menos 6 meses

### Fase 2: Cálculo Baseline (1-2 semanas)
1. Calcular CAC por canal e blended
2. Construir curva de retenção por cohort (pelo menos 6 cohorts)
3. Calcular LTV usando método de cohort (não fórmula simplificada)
4. Determinar payback period atual
5. Calcular LTV:CAC ratio por segmento

### Fase 3: Diagnóstico (1 semana)
1. Identificar segmentos com melhores e piores unit economics
2. Mapear tendências: estão melhorando ou deteriorando?
3. Identificar alavancas: onde mover a agulha tem mais impacto?
4. Benchmark contra comparáveis do setor

### Fase 4: Plano de Ação
1. Para CAC alto: otimizar canais, melhorar conversão, investir em PLG
2. Para LTV baixo: melhorar onboarding, expandir valor entregue, reduzir churn
3. Para payback longo: ajustar pricing, cobrar upfront, reduzir COGS
4. Definir targets para próximos 2-4 trimestres

## Template de Dashboard de Unit Economics

```markdown
# Unit Economics Dashboard — [Período]

## Métricas-Chave
| Métrica | Atual | Meta | Trend |
|---------|-------|------|-------|
| CAC Blended | R$ [X] | R$ [Y] | [↑↓→] |
| CAC Paid | R$ [X] | R$ [Y] | [↑↓→] |
| ARPA | R$ [X] | R$ [Y] | [↑↓→] |
| Gross Margin | [X]% | [Y]% | [↑↓→] |
| LTV | R$ [X] | R$ [Y] | [↑↓→] |
| LTV:CAC | [X]:1 | [Y]:1 | [↑↓→] |
| Payback | [X] meses | [Y] meses | [↑↓→] |
| NRR | [X]% | [Y]% | [↑↓→] |

## Cohort Analysis
[Heatmap de retenção por cohort]

## Segmentação
[Breakdown por segmento/canal/produto]
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| LTV:CAC Ratio | ≥ 3:1 | Mensal |
| Payback Period | < 12 meses (SMB) / < 18 (Enterprise) | Mensal |
| Net Revenue Retention | > 110% | Mensal |
| Gross Margin | > 70% (SaaS) / > 40% (marketplace) | Mensal |
| Cohort retention M12 | > 80% | Por cohort |
| CAC trend | Estável ou decrescente | Trimestral |

## Armadilhas

1. **LTV:CAC sem cohort** — Média esconde realidade; cohorts recentes podem ser piores
2. **CAC sem fully-loaded costs** — Excluir salários distorce a métrica
3. **LTV com churn rate de steady state** — Usar churn atual se empresa é jovem
4. **Ignorar payback** — LTV:CAC bom mas payback de 3 anos = problema de capital
5. **Blended metrics only** — Segmentar por canal, produto e geography é essencial

## Referências Cruzadas

- `frameworks/cfo-strategist/financial-planning.md` — Unit economics alimentam o modelo financeiro
- `frameworks/cfo-strategist/fundraising-readiness.md` — Investidores olham estas métricas
- `frameworks/cfo-strategist/cost-optimization.md` — COGS optimization impacta unit economics
- `frameworks/vision-chief/market-thesis-framework.md` — Sizing baseado em unit economics
- `frameworks/vision-chief/competitive-moat-analysis.md` — Moats que melhoram unit economics
- `frameworks/shared/decision-framework.md` — Unit economics como critério de decisão
