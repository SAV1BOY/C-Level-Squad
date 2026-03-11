# Review de Unit Economics

> Processo estruturado para calcular, analisar e otimizar os unit economics
> do negócio, garantindo que cada unidade de venda gera valor sustentável.

## Objetivo

Entender profundamente quanto custa adquirir e servir cada cliente, quanto
cada cliente gera de valor ao longo do tempo, e se o modelo de negócio é
fundamentalmente saudável e escalável.

## Frequência

- **Cálculo completo:** Mensal
- **Deep dive por segmento:** Trimestral
- **Revisão estratégica:** Semestral (com board/investidores)

## Métricas Fundamentais

### Customer Acquisition Cost (CAC)
```
CAC = (Gastos com Marketing + Gastos com Vendas) / Novos Clientes Adquiridos
```

Detalhamento:
- [ ] CAC total (blended)
- [ ] CAC por canal (organic, paid, referral, outbound)
- [ ] CAC por segmento de cliente (SMB, mid-market, enterprise)
- [ ] CAC payback period: meses para recuperar o CAC

### Lifetime Value (LTV)
```
LTV = ARPU × Gross Margin % × Customer Lifetime (em meses)
```

Onde:
- ARPU = Average Revenue Per User (mensal)
- Customer Lifetime = 1 / Churn Rate mensal

Detalhamento:
- [ ] LTV total (blended)
- [ ] LTV por segmento
- [ ] LTV por cohort (clientes de jan, fev, mar, etc.)
- [ ] LTV por canal de aquisição

### Ratio LTV:CAC
```
LTV:CAC = LTV / CAC
```

| Ratio | Interpretação |
|-------|--------------|
| < 1:1 | Destruindo valor a cada cliente (insustentável) |
| 1:1 - 2:1 | Margem muito apertada, risco alto |
| 3:1 | Benchmark saudável para SaaS |
| > 5:1 | Pode estar subinvestindo em crescimento |

### CAC Payback Period
```
CAC Payback = CAC / (ARPU × Gross Margin %)
```

| Payback | Interpretação |
|---------|--------------|
| < 6 meses | Excelente - dinheiro para reinvestir rápido |
| 6-12 meses | Bom - padrão saudável para SaaS |
| 12-18 meses | Aceitável se LTV é alto |
| > 18 meses | Preocupante - capital intensivo demais |

## Métricas Complementares

### Receita
- [ ] MRR (Monthly Recurring Revenue)
- [ ] ARR (Annual Recurring Revenue)
- [ ] ARPU (Average Revenue Per User)
- [ ] ACV (Average Contract Value)
- [ ] Expansion Revenue (upsell/cross-sell)

### Retenção
- [ ] Gross Revenue Retention (sem expansion)
- [ ] Net Revenue Retention (com expansion)
- [ ] Logo Churn (% de clientes perdidos)
- [ ] Revenue Churn (% de receita perdida)
- [ ] Cohort retention curves (30, 90, 180, 365 dias)

### Eficiência
- [ ] Gross Margin (receita - COGS)
- [ ] Contribution Margin (receita - COGS - custos variáveis diretos)
- [ ] Magic Number: Net New ARR / S&M spend do trimestre anterior
- [ ] Burn Multiple: Net Burn / Net New ARR

## Processo de Cálculo

### Passo 1: Coleta de Dados (Dia 1-3)
- [ ] Receita por cliente (do CRM/billing system)
- [ ] Gastos com marketing por canal (do marketing/finance)
- [ ] Gastos com vendas por canal (do sales/finance)
- [ ] COGS por cliente (hosting, suporte, serviços)
- [ ] Clientes adquiridos, churned, expandidos (do CRM)

### Passo 2: Cálculo Base (Dia 3-4)
- [ ] Calcular CAC blended e por canal
- [ ] Calcular LTV blended e por segmento
- [ ] Calcular ratio LTV:CAC
- [ ] Calcular payback period
- [ ] Calcular cohort retention curves

### Passo 3: Análise por Segmento (Dia 4-5)
- [ ] Segmentar por tamanho de cliente (SMB/Mid/Enterprise)
- [ ] Segmentar por canal de aquisição
- [ ] Segmentar por produto/plano
- [ ] Segmentar por geografia (se relevante)
- [ ] Identificar segmentos mais e menos rentáveis

### Passo 4: Tendências e Insights (Dia 5-6)
- [ ] Comparar com mês anterior e mesmo mês do ano anterior
- [ ] Identificar tendências (CAC subindo? LTV caindo?)
- [ ] Analisar drivers de mudança
- [ ] Projetar impacto se tendência continuar

### Passo 5: Recomendações (Dia 6-7)
- [ ] Onde investir mais (segmentos de alto LTV:CAC)
- [ ] Onde cortar investimento (segmentos de baixo LTV:CAC)
- [ ] Iniciativas para melhorar retenção
- [ ] Oportunidades de expansion revenue

## Template de Report

```
UNIT ECONOMICS REPORT - [MÊS/ANO]

RESUMO EXECUTIVO
LTV:CAC = X:1 (meta: 3:1) [trend: ↑↓→]
CAC Payback = X meses (meta: <12) [trend: ↑↓→]
NRR = X% (meta: >110%) [trend: ↑↓→]

DETALHAMENTO
| Métrica | Mês Atual | Mês Anterior | YoY | Meta |
|---------|-----------|-------------|-----|------|
| MRR | | | | |
| ARPU | | | | |
| CAC (blended) | | | | |
| LTV | | | | |
| LTV:CAC | | | | |
| Payback (meses) | | | | |
| Gross Margin | | | | |
| NRR | | | | |
| Logo Churn | | | | |

POR SEGMENTO
| Segmento | CAC | LTV | LTV:CAC | Payback | NRR |
|----------|-----|-----|---------|---------|-----|
| SMB | | | | | |
| Mid-Market | | | | | |
| Enterprise | | | | | |

TOP 3 INSIGHTS
1.
2.
3.

RECOMENDAÇÕES
1.
2.
3.
```

## Alavancas de Melhoria

### Para Melhorar CAC
1. Investir em canais orgânicos (content, SEO, community)
2. Otimizar funil de conversão (menos friction)
3. Programa de referral (CAC mais baixo que paid)
4. Melhorar qualifying para não gastar em leads ruins
5. Automação de marketing para nurturing

### Para Melhorar LTV
1. Reduzir churn (onboarding, CS proativo, product-market fit)
2. Aumentar ARPU (upsell, cross-sell, pricing optimization)
3. Expandir use cases (mais valor = mais stickiness)
4. Programa de customer success para enterprise
5. Produto com efeitos de rede (mais valor com mais uso)

### Para Melhorar Gross Margin
1. Otimizar infraestrutura (right-sizing, reserved instances)
2. Automatizar suporte (chatbot, self-service, knowledge base)
3. Reduzir customização por cliente
4. Economias de escala em COGS

## Referências

- "Lean Analytics" - Alistair Croll & Benjamin Yoskovitz
- SaaStr: "The Ultimate Guide to SaaS Metrics"
- "Scaling Lean" - Ash Maurya
- David Skok Blog (forEntrepreneurs.com)
- Bessemer Cloud Index (benchmarks de SaaS)
