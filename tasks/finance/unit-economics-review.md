# Review de Unit Economics

## Objetivo

Calcular, analisar e otimizar os unit economics do negocio de forma sistematica,
garantindo que cada unidade de venda gera valor sustentavel e que o modelo de
negocio e fundamentalmente saudavel e escalavel.

## Frequencia

- **Calculo completo**: Mensal (ate D+7 do mes seguinte)
- **Deep dive por segmento**: Trimestral (alinhado com QBR)
- **Revisao estrategica**: Semestral (com board e investidores)
- **Ad-hoc**: Quando houver mudanca significativa em pricing ou modelo

## Metricas Fundamentais

### Customer Acquisition Cost (CAC)

```
CAC = (Gastos com Marketing + Gastos com Vendas) / Novos Clientes Adquiridos
```

Desdobramentos obrigatorios:
- [ ] CAC total (blended) - media ponderada de todos os canais
- [ ] CAC por canal (organico, pago, referral, outbound, parceiros)
- [ ] CAC por segmento de cliente (SMB, mid-market, enterprise)
- [ ] CAC payback period: meses para recuperar o investimento de aquisicao
- [ ] Fully loaded CAC: incluindo overhead de equipe e ferramentas

### Lifetime Value (LTV)

```
LTV = ARPU mensal x Margem Bruta % x Tempo de Vida do Cliente (meses)
Onde: Tempo de Vida = 1 / Churn Rate mensal
```

Desdobramentos obrigatorios:
- [ ] LTV total (blended) - media ponderada
- [ ] LTV por segmento de cliente
- [ ] LTV por cohort (clientes adquiridos em cada mes/trimestre)
- [ ] LTV por canal de aquisicao (para avaliar qualidade do canal)
- [ ] LTV projetado vs realizado (validar premissas do modelo)

### Ratio LTV:CAC

| Ratio | Interpretacao | Acao |
|-------|-------------|------|
| < 1:1 | Destruindo valor a cada cliente | Parar aquisicao, corrigir modelo |
| 1:1 - 2:1 | Margem muito apertada, risco alto | Otimizar urgente |
| 3:1 | Benchmark saudavel para SaaS | Manter e escalar |
| > 5:1 | Pode estar subinvestindo em crescimento | Aumentar investimento |

### CAC Payback Period

```
CAC Payback = CAC / (ARPU mensal x Margem Bruta %)
```

| Payback | Interpretacao | Contexto |
|---------|-------------|---------|
| < 6 meses | Excelente - capital recicla rapido | Ideal para self-service/PLG |
| 6-12 meses | Bom - padrao saudavel para SaaS | Maioria das empresas B2B |
| 12-18 meses | Aceitavel se LTV alto | Enterprise com contratos longos |
| > 18 meses | Preocupante - capital intensivo | Necessita captacao constante |

## Metricas Complementares

### Receita
- [ ] MRR (Monthly Recurring Revenue) e componentes (new, expansion, contraction, churn)
- [ ] ARR (Annual Recurring Revenue) e crescimento YoY
- [ ] ARPU (Average Revenue Per User) por segmento
- [ ] ACV (Average Contract Value) e tendencia
- [ ] Expansion Revenue como % do MRR total

### Retencao
- [ ] Gross Revenue Retention (sem considerar expansion)
- [ ] Net Revenue Retention (com expansion - meta >110%)
- [ ] Logo Churn (% de clientes perdidos por mes)
- [ ] Revenue Churn (% de receita perdida por mes)
- [ ] Curvas de retencao por cohort (30, 90, 180, 365 dias)

### Eficiencia
- [ ] Gross Margin (receita - COGS direto)
- [ ] Contribution Margin (receita - COGS - custos variaveis diretos)
- [ ] Magic Number: Net New ARR / S&M spend do trimestre anterior
- [ ] Burn Multiple: Net Burn / Net New ARR (meta <2x)
- [ ] Revenue per Employee (produtividade organizacional)

## Processo de Calculo

### Passo 1: Coleta de Dados (Dia 1-3)

- [ ] Receita por cliente e por plano (sistema de billing/CRM)
- [ ] Gastos com marketing por canal e campanha
- [ ] Gastos com vendas por canal (salarios, comissoes, ferramentas)
- [ ] COGS por cliente (hosting, suporte, servicos profissionais)
- [ ] Movimentacao de clientes: novos, churned, expandidos, contraidos

### Passo 2: Calculo Base (Dia 3-4)

- [ ] Calcular CAC blended e por canal
- [ ] Calcular LTV blended e por segmento
- [ ] Calcular ratio LTV:CAC e payback period
- [ ] Calcular NRR e GRR
- [ ] Gerar curvas de retencao por cohort

### Passo 3: Analise por Segmento (Dia 4-5)

- [ ] Segmentar por tamanho de cliente (SMB / Mid-Market / Enterprise)
- [ ] Segmentar por canal de aquisicao (organico, pago, outbound, parceiro)
- [ ] Segmentar por produto/plano (basico, profissional, enterprise)
- [ ] Segmentar por geografia (se relevante)
- [ ] Identificar segmentos mais e menos rentaveis

### Passo 4: Tendencias e Insights (Dia 5-6)

- [ ] Comparar com mes anterior e mesmo mes do ano anterior
- [ ] Identificar tendencias (CAC subindo? LTV caindo? NRR estavel?)
- [ ] Analisar drivers de mudanca (o que causou a variacao?)
- [ ] Projetar impacto se tendencia continuar por 6-12 meses

### Passo 5: Recomendacoes (Dia 6-7)

- [ ] Onde investir mais (segmentos com alto LTV:CAC e capacidade de escala)
- [ ] Onde cortar investimento (segmentos com baixo LTV:CAC)
- [ ] Iniciativas para melhorar retencao (onboarding, CS, produto)
- [ ] Oportunidades de expansion revenue (upsell, cross-sell)
- [ ] Ajustes de pricing recomendados

## Template de Report

```
UNIT ECONOMICS REPORT - [MES/ANO]
Preparado por: [Nome] | Aprovado por: [CFO]

RESUMO EXECUTIVO
LTV:CAC = X:1 (meta: 3:1) [tendencia: subindo/caindo/estavel]
CAC Payback = X meses (meta: <12) [tendencia]
NRR = X% (meta: >110%) [tendencia]
Magic Number = X (meta: >0.75) [tendencia]

DETALHAMENTO
| Metrica        | Mes Atual | Mes Anterior | YoY    | Meta  | Status |
|---------------|-----------|-------------|--------|-------|--------|
| MRR           |           |             |        |       |        |
| ARPU          |           |             |        |       |        |
| CAC (blended) |           |             |        |       |        |
| LTV           |           |             |        |       |        |
| LTV:CAC       |           |             |        |       |        |
| Payback       |           |             |        |       |        |
| Gross Margin  |           |             |        |       |        |
| NRR           |           |             |        |       |        |
| Logo Churn    |           |             |        |       |        |
| Burn Multiple |           |             |        |       |        |

POR SEGMENTO
| Segmento    | CAC  | LTV  | LTV:CAC | Payback | NRR   |
|------------|------|------|---------|---------|-------|
| SMB        |      |      |         |         |       |
| Mid-Market |      |      |         |         |       |
| Enterprise |      |      |         |         |       |

TOP 3 INSIGHTS
1. [Insight com dados e impacto]
2. [Insight com dados e impacto]
3. [Insight com dados e impacto]

RECOMENDACOES
1. [Acao com responsavel e prazo]
2. [Acao com responsavel e prazo]
3. [Acao com responsavel e prazo]
```

## Alavancas de Melhoria

### Para Melhorar CAC
1. Investir em canais organicos (conteudo, SEO, comunidade, eventos)
2. Otimizar funil de conversao (reduzir friccao em cada etapa)
3. Programa de referral estruturado (CAC 60-70% menor que pago)
4. Melhorar qualificacao de leads (nao gastar em leads ruins)
5. Automacao de marketing para nurturing de longo prazo

### Para Melhorar LTV
1. Reduzir churn (onboarding, CS proativo, product-market fit)
2. Aumentar ARPU (upsell, cross-sell, pricing optimization)
3. Expandir use cases dentro do cliente (mais valor = mais stickiness)
4. Programa de customer success estruturado para enterprise
5. Produto com efeitos de rede (mais valor com mais uso)

### Para Melhorar Gross Margin
1. Otimizar infraestrutura (right-sizing, reserved instances, spot)
2. Automatizar suporte (chatbot, self-service, knowledge base)
3. Reduzir customizacao por cliente (produto padronizado)
4. Economias de escala conforme base de clientes cresce
5. Renegociar contratos com fornecedores de infraestrutura
