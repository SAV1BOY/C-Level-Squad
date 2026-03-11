# SaaS — Software as a Service

## Visão Geral

SaaS é o modelo de distribuição de software onde o produto é acessado via internet,
com pagamento recorrente (subscription). É um dos modelos de negócio mais bem
compreendidos em termos de métricas e benchmarks, o que facilita comparação e
planejamento — mas também cria armadilhas de "seguir a fórmula" sem contexto.

---

## 1. Métricas Fundamentais

### Revenue Metrics

**ARR (Annual Recurring Revenue)**
Receita recorrente anualizada. É a métrica norte do SaaS.
- Cálculo: MRR × 12
- Inclui apenas receita recorrente (excluir one-time fees, serviços, setup)
- Variações: novo ARR, expansion ARR, churned ARR, contraction ARR

**MRR (Monthly Recurring Revenue)**
Receita recorrente mensal. Mais granular que ARR para acompanhamento operacional.
- MRR Novo: de novos clientes
- MRR Expansion: upsell e cross-sell de clientes existentes
- MRR Contraction: downgrades de clientes existentes
- MRR Churn: cancelamentos

**NRR (Net Revenue Retention)**
Quanto da receita de uma coorte é retida após 12 meses, incluindo expansion e churn.
- Fórmula: (ARR início + expansion - contraction - churn) / ARR início
- Benchmark excelente: >120% (receita cresce mesmo sem novos clientes)
- Benchmark bom: 100-120%
- Benchmark preocupante: <100% (base encolhendo)

**GRR (Gross Revenue Retention)**
Quanto da receita é retida sem considerar expansion. Mede apenas a capacidade de
reter o que já tem.
- Fórmula: (ARR início - contraction - churn) / ARR início
- Benchmark excelente: >95%
- Benchmark bom: 85-95%
- Benchmark preocupante: <85%

### Customer Metrics

**CAC (Customer Acquisition Cost)**
Custo total para adquirir um novo cliente.
- Fórmula: (gastos S&M totais) / (novos clientes no período)
- Incluir: salários de vendas e marketing, ferramentas, ads, eventos
- Variações: blended CAC vs organic vs paid; por segmento e canal

**LTV (Lifetime Value)**
Valor total que um cliente gera durante seu ciclo de vida.
- Fórmula simplificada: ARPA × Gross Margin / Churn Rate
- LTV/CAC ratio: >3x é o benchmark clássico; >5x sugere underinvestment em growth
- CAC Payback: tempo para recuperar o CAC; benchmark <18 meses

**Logo Churn vs Revenue Churn**
- Logo churn: % de clientes que cancelam (todas as logos iguais)
- Revenue churn: % de receita que churn (pondera pelo tamanho do cliente)
- Revenue churn é mais importante porque 1 enterprise = 100 SMBs em receita

### Efficiency Metrics

**Rule of 40**
Growth Rate + Profit Margin ≥ 40%. Benchmark de eficiência para SaaS maduro.
- Empresa crescendo 60% com margem de -20% = 40 ✓
- Empresa crescendo 20% com margem de 20% = 40 ✓
- Trade-off entre crescimento e lucratividade

**Burn Multiple**
Net Burn / Net New ARR. Quanto queimamos para cada real novo de ARR.
- <1x: excelente (eficiente)
- 1-2x: bom
- >2x: ineficiente — ajustar antes que o caixa acabe

**Magic Number**
Net New ARR / S&M Spend do quarter anterior.
- >1.0: investir mais em vendas (eficiência alta)
- 0.5-1.0: otimizar antes de escalar
- <0.5: problema de eficiência de go-to-market

---

## 2. Benchmarks por Estágio

### Early Stage (Pre-Product Market Fit)

| Métrica           | Referência                    |
|-------------------|-------------------------------|
| ARR               | <$1M                         |
| Growth Rate       | Não relevante (base pequena) |
| NRR               | Acompanhar, não otimizar     |
| CAC Payback       | Pode ser alto (experimentando)|
| Burn Multiple     | <2x ideal, aceitável >2x     |
| Foco              | Product-market fit, não escala|

### Growth Stage ($1M-$10M ARR)

| Métrica           | Referência                    |
|-------------------|-------------------------------|
| Growth Rate       | >100% YoY (T2D3: triple, triple, double, double, double) |
| NRR               | >110%                         |
| GRR               | >85%                          |
| CAC Payback       | <18 meses                     |
| LTV/CAC           | >3x                           |
| Burn Multiple     | <1.5x                         |
| Foco              | Encontrar modelo repetível de aquisição |

### Scale Stage ($10M-$100M ARR)

| Métrica           | Referência                    |
|-------------------|-------------------------------|
| Growth Rate       | >50% YoY                      |
| NRR               | >120%                         |
| GRR               | >90%                          |
| Rule of 40        | ≥40                           |
| CAC Payback       | <12 meses                     |
| Gross Margin      | >70%                          |
| Foco              | Eficiência + crescimento sustentável |

---

## 3. Modelos Operacionais

### Sales-Led Growth (SLG)

Modelo tradicional com equipe de vendas como motor de aquisição.
- **Adequado para**: ACV alto (>$10K), venda complexa, enterprise
- **Estrutura**: SDR → AE → CSM → AM
- **Métricas-chave**: pipeline coverage, win rate, sales cycle, quota attainment
- **Desafio**: escalar time de vendas é caro e lento

### Product-Led Growth (PLG)

Produto como motor de aquisição — free trial ou freemium como entrada.
- **Adequado para**: ACV baixo-médio, produto self-serve, SMB/mid-market
- **Estrutura**: growth team, product, customer success light-touch
- **Métricas-chave**: signup → activation → conversion → expansion
- **Desafio**: construir produto bom o suficiente para vender sozinho

### Hybrid (PLG + SLG)

Combinação dos dois modelos. PLG para aquisição e qualificação, SLG para
upsell e enterprise.
- **Adequado para**: multi-segmento (SMB via PLG, enterprise via SLG)
- **Estrutura**: ambas, com handoff definido
- **Tendência**: maioria das empresas SaaS bem-sucedidas está indo para hybrid

---

## 4. Padrões de Crescimento

### T2D3 Framework

Framework de crescimento para SaaS VC-backed:
- Ano 1-2: Triple (3x)
- Ano 3-4: Double (2x)
- Ano 5: Double (2x)
- Resultado: ~$100M ARR em ~7 anos partindo de ~$2M

### Endure Framework (SaaStr)

Para SaaS que não segue o caminho VC tradicional:
- Crescimento sustentável de 50-80% por vários anos
- Foco em eficiência desde cedo
- Pode demorar mais para escalar, mas com unit economics saudáveis

### Efficient Growth

Tendência pós-2022 (era de capital eficiente):
- Rule of 40 ganhou importância sobre growth-at-all-costs
- Burn multiple como métrica primária de eficiência
- FCF positivo como milestone valorizado
- "Grow efficiently or die" substituiu "grow fast or die"

---

## 5. Desafios Comuns

### Churn e Retention

- **Churn invisível**: degradação gradual do uso antes do cancelamento
- **Involuntary churn**: falhas de pagamento (3-5% do churn total é recuperável)
- **Expansion vs churn**: NRR alta pode mascarar GRR ruim
- **Cohort analysis**: é essencial — métricas agregadas escondem deterioração

### Pricing

- **Underpricing**: problema mais comum que overpricing em SaaS
- **Value metric**: alinhar preço ao valor entregue (por usuário, por uso, por resultado)
- **Packaging**: tiers que criam natural expansion path
- **Pricing como growth lever**: aumentos de preço impactam NRR diretamente

### Go-to-Market Efficiency

- **CAC cresce com escala**: canais mais fáceis saturam primeiro
- **Channel concentration**: dependência de um canal é risco
- **Marketing attribution**: cada vez mais difícil em mundo privacy-first
- **Sales productivity**: ramp time de novos vendedores pode ser 6-9 meses

### Tecnologia e Produto

- **Tech debt**: velocidade de desenvolvimento cai se não gerenciar
- **Platform vs feature**: quando construir plataforma vs features pontuais
- **AI disruption**: LLMs estão redefinindo expectativas de produto SaaS
- **Integration ecosystem**: APIs e marketplace como moat competitivo

---

## 6. Contexto Brasil

### Oportunidades

- Mercado sub-penetrado em muitas verticais
- Custo de desenvolvimento relativamente baixo (engenheiros competentes, custo menor que US)
- Oportunidade de adaptar playbooks internacionais ao contexto local
- PIX e infraestrutura de pagamento facilitam cobrança recorrente

### Desafios

- **Ticket médio menor**: poder aquisitivo menor que mercados desenvolvidos
- **Complexidade fiscal**: emissão de NF, regimes tributários, ISS por município
- **Câmbio**: custos de infra em USD, receita em BRL
- **Cultura de compra**: resistência a contratos longos, preferência por mensal
- **Pagamento**: inadimplência mais alta que mercados maduros
- **Talent competition**: disputa com empresas US que pagam em dólar

---

## Referências

- SaaStr Annual Benchmarks Report
- OpenView Partners — Product Benchmarks
- Bessemer Cloud Index
- "From Impossible to Inevitable" — Aaron Ross & Jason Lemkin
- "Obviously Awesome" — April Dunford (positioning)
