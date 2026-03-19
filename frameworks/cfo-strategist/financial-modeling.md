# Financial Modeling Framework — Modelagem Financeira para Decisões Estratégicas

## Origem e Contexto

Financial modeling é a arte e ciência de construir representações matemáticas do desempenho
financeiro de uma empresa. Um bom modelo financeiro não é uma previsão — é uma **ferramenta de
pensamento** que permite testar hipóteses, quantificar cenários e tomar decisões com base em
dados ao invés de intuição.

O modelo de 3 demonstrações (3-statement model) é o padrão-ouro: integra **DRE (Income Statement)**,
**Balanço Patrimonial (Balance Sheet)** e **Fluxo de Caixa (Cash Flow Statement)** em um sistema
que se auto-balanceia. Quando bem construído, permite simular o impacto de qualquer decisão em
receita, custo, caixa e valuation — simultaneamente.

Este framework vai além da mecânica de modelagem. Ele estrutura **como pensar sobre drivers**,
como construir cenários úteis (não infinitos), e como usar o modelo para tomar decisões melhores.
O objetivo não é prever o futuro com precisão, mas entender a sensibilidade do negócio às variáveis
que importam e preparar a empresa para múltiplos futuros possíveis.

---

## Quando Usar

- Na construção do plano financeiro anual (budget + forecast)
- Em preparação para fundraising (investidores exigem modelo)
- Ao avaliar viabilidade de novos produtos, mercados ou modelos de negócio
- Para decisões de pricing (impacto em receita, margem e caixa)
- Em cenários de M&A (valuation e sinergias)
- Quando o board pede projeções de runway e path to profitability
- Na avaliação de impacto financeiro de decisões estratégicas (pivotar, expandir, contrair)
- Em stress tests: "O que acontece se receita cair 30%?"

---

## Quando NÃO Usar

- Para decisões operacionais do dia-a-dia (análise simples basta)
- Quando não há dados históricos mínimos (< 3 meses) — o modelo será pura especulação
- Para impressionar investidores com projeções hockey-stick sem fundamento
- Quando a precisão importa menos que a velocidade — use back-of-envelope calculation
- Para substituir julgamento de negócio — o modelo é input, não a decisão

---

## Estrutura / Modelo

### 1. Arquitetura do 3-Statement Model

```
┌─────────────────────────────────────────────────────────┐
│                    ASSUMPTIONS / DRIVERS                  │
│  (Revenue drivers, cost drivers, capital drivers)        │
└───────────┬──────────────────┬──────────────────┬───────┘
            │                  │                  │
            ▼                  ▼                  ▼
┌───────────────┐  ┌───────────────┐  ┌───────────────────┐
│     DRE       │  │    BALANÇO    │  │   FLUXO DE CAIXA  │
│  (P&L)        │  │ PATRIMONIAL   │  │   (Cash Flow)     │
│               │  │               │  │                   │
│ Receita       │  │ Ativos        │  │ Operacional       │
│ - COGS        │  │   Circulante  │  │   Lucro líquido   │
│ = Margem Bruta│  │   Não-circ.   │  │   + D&A           │
│ - OPEX        │  │ Passivos      │  │   ± Working Cap   │
│ = EBITDA      │  │   Circulante  │  │ Investimento      │
│ - D&A         │  │   Não-circ.   │  │   CAPEX           │
│ = EBIT        │  │ Patrimônio    │  │ Financiamento     │
│ - Impostos    │  │   Líquido     │  │   Dívida/Equity   │
│ = Lucro Líq.  │  │               │  │ = Δ Caixa         │
└───────┬───────┘  └───────┬───────┘  └─────────┬─────────┘
        │                  │                     │
        └──────────────────┴─────────────────────┘
                    INTERCONECTADOS
```

### 2. Drivers Fundamentais

**Revenue Drivers (Motor de Receita):**
```
Receita = f(Volume, Preço, Mix, Retenção, Expansão)

SaaS:
  MRR = Clientes_ativos × ARPA
  Clientes_ativos = Clientes_início + Novos - Churned
  Novos = Leads × Conversion_rate
  ARR = MRR × 12

Marketplace:
  GMV = Transações × Ticket_médio
  Receita = GMV × Take_rate

E-commerce:
  Receita = Visitantes × Conversion × AOV
```

**Cost Drivers (Motor de Custo):**
```
COGS:
  Hosting = f(Usuários ativos, usage per user)
  Suporte = f(Tickets, custo por ticket)
  Payment processing = f(GMV, taxa)

OPEX:
  Headcount = FTEs × Custo_médio_loaded
  Marketing = f(CAC_target × Novos_clientes_target)
  G&A = f(Revenue, compliance requirements)
```

**Capital Drivers:**
```
Working Capital:
  Contas a Receber = Receita × DSO / 365
  Contas a Pagar = COGS × DPO / 365
  Necessidade WC = Δ(Receber - Pagar)

CAPEX:
  Maintenance CAPEX = % do ativo imobilizado
  Growth CAPEX = Investimentos em expansão
```

### 3. Cenários Estruturados

Três cenários obrigatórios, com probabilidades explícitas:

| Cenário | Probabilidade | Descrição | Premissas-Chave |
|---------|-------------|-----------|-----------------|
| **Bull (Otimista)** | 20-25% | Tudo dá certo, mercado favorável | Growth > plan, churn < plan, margem expande |
| **Base (Realista)** | 50-60% | Execução competente, mercado neutro | Growth = plan, churn = atual, margem estável |
| **Bear (Pessimista)** | 20-25% | Execução com falhas, mercado adverso | Growth < plan, churn sobe, margem comprime |

**Expected Value:**
```
EV = P(Bull) × Resultado_Bull + P(Base) × Resultado_Base + P(Bear) × Resultado_Bear
```

---

## Processo de Aplicação

### Fase 1: Estruturação (Semana 1)

1. Definir o objetivo do modelo (budget? fundraising? decisão específica?)
2. Mapear os drivers do negócio (revenue, cost, capital)
3. Coletar dados históricos (mínimo 6 meses, ideal 12-24)
4. Definir granularidade temporal (mensal para 12-18 meses, trimestral/anual para anos 2-5)
5. Escolher ferramenta (Google Sheets para colaboração, Excel para complexidade)

### Fase 2: Construção do Modelo (Semana 2-3)

1. **Tab de Assumptions:**
   - Listar todos os drivers com valores históricos e projetados
   - Separar inputs (editáveis, em azul) de cálculos (fórmulas, em preto)
   - Documentar fontes e lógica de cada premissa

2. **Tab de DRE (P&L):**
   - Construir receita bottom-up a partir dos drivers
   - Modelar COGS por componente
   - Modelar OPEX por categoria (P&D, S&M, G&A)
   - Calcular EBITDA, EBIT e lucro líquido

3. **Tab de Balanço:**
   - Modelar working capital a partir de DSO/DPO
   - Projetar ativos fixos com CAPEX e depreciação
   - Modelar dívida (se aplicável)
   - Garantir que balanço fecha (Assets = Liabilities + Equity)

4. **Tab de Cash Flow:**
   - Derivar cash from operations (lucro líquido + ajustes)
   - Incluir investing activities (CAPEX)
   - Incluir financing activities (dívida, equity)
   - Validar: Δ caixa = saldo final - saldo inicial do balanço

5. **Tab de Cenários:**
   - Criar toggle para Bull / Base / Bear
   - Testar cada cenário e validar resultados

### Fase 3: Sensitivity Analysis (Semana 3)

1. Identificar as 5-8 variáveis mais impactantes
2. Criar tabela de sensibilidade 2D para as 2 variáveis mais críticas
3. Testar: "Se churn sobe 2pp E growth cai 20%, quando acaba o caixa?"
4. Documentar breakeven points e danger zones

```
Exemplo — Sensitivity de Runway (meses):

               Churn Rate
               3%    5%    7%    10%
Growth   30%  | 24  | 20  | 16  | 11  |
Rate     20%  | 20  | 17  | 13  |  9  |
         10%  | 16  | 13  | 10  |  7  |
          0%  | 12  | 10  |  8  |  5  |
```

### Fase 4: Validação e Uso (Semana 4)

1. Revisar modelo com outro membro do time financeiro (peer review)
2. Stress test: inserir valores extremos e verificar se modelo se comporta logicamente
3. Comparar projeções com benchmarks de mercado (são realistas?)
4. Apresentar ao CFO/CEO para alinhamento de premissas
5. Estabelecer cadência de atualização (mensal: actuals vs. forecast)

---

## Exemplos Práticos

### Exemplo 1: SaaS B2B — Revenue Build

```
Premissas Base:
- Clientes início do ano: 500
- New logos/mês: 25 (crescendo 5%/mês)
- Monthly churn: 3%
- ARPA: R$ 2.000/mês
- Expansion rate: 2%/mês sobre base existente

Projeção Q1:
                    Jan        Fev        Mar
Clientes início     500        510        520
+ Novos              25         26         27
- Churned            15         15         16
+ Expansion (net)     0          0          0
Clientes fim        510        521        531

MRR            R$ 1.020K  R$ 1.042K  R$ 1.062K
Growth MoM         2.0%       2.2%       1.9%
ARR run-rate   R$ 12.2M   R$ 12.5M   R$ 12.7M
```

### Exemplo 2: Tornado Chart — Top Sensitivities

```
Impacto no EBITDA anual (variação de ±20% no driver):

Churn rate:        ████████████████████  R$ -1.2M a +R$ 1.5M
Preço médio:       ███████████████████   R$ -1.1M a +R$ 1.1M
New logos/mês:     ██████████████        R$ -0.8M a +R$ 0.8M
Headcount growth:  ████████████          R$ -0.7M a +R$ 0.7M
CAC:               ██████████            R$ -0.6M a +R$ 0.6M
Hosting cost/user: ████████              R$ -0.5M a +R$ 0.5M
```

---

## Armadilhas Comuns

1. **Modelo sem dono** — Modelo criado para fundraising e nunca mais atualizado. Designar DRI que atualiza mensalmente com actuals.

2. **Revenue top-down sem bottom-up** — "Queremos R$ 50M" não é modelagem. Construa receita a partir de drivers reais (leads × conversão × preço).

3. **Hockey stick sem justificativa** — Growth acelerando mês a mês sem explicar por que. Investidores experientes rejeitam na hora.

4. **Custo fixo que não escala** — Modelar headcount como fixo quando receita triplica. Pessoas são necessárias para suportar crescimento.

5. **Ignorar working capital** — Empresa lucrativa mas sem caixa porque não modelou tempo de recebimento vs. pagamento.

6. **Cenário único** — Só ter cenário base é fingir que sabe o futuro. Cenários bull/bear revelam onde estão os riscos reais.

7. **Excesso de complexidade** — Modelo com 50 tabs que ninguém entende ou mantém. Melhor simples e atualizado do que complexo e abandonado.

8. **Premissas enterradas em fórmulas** — Toda premissa deve estar na tab de assumptions, visível e editável. Hardcoded numbers em fórmulas são bugs.

---

## Integração com Outros Frameworks

- `frameworks/cfo-strategist/cfo-capital-allocation.md` — O modelo financeiro gera os inputs de IRR e payback para decisões de alocação
- `frameworks/cfo-strategist/unit-economics.md` — Unit economics são os drivers fundamentais do modelo de receita
- `frameworks/cfo-strategist/cash-flow-management.md` — O modelo projeta cash flow; cash management operacionaliza
- `frameworks/cfo-strategist/scenario-planning.md` — Cenários estratégicos alimentam os cenários financeiros
- `frameworks/cfo-strategist/budget-governance.md` — Budget é o output do modelo; governance garante execução
- `frameworks/cfo-strategist/fundraising-readiness.md` — Investidores exigem modelo financeiro robusto
- `checklists/finance/financial-health-audit.md` — Audita a saúde financeira que o modelo projeta
- `templates/finance/monthly-financial-report.md` — Report mensal compara actuals vs. modelo

---

## Referências

- **Rosenbaum, J. & Pearl, J.** — "Investment Banking: Valuation, LBOs, M&A" — Referência em modelagem financeira
- **Pignataro, P.** — "Financial Modeling and Valuation" — Guia prático de 3-statement model
- **SaaS Capital** — Benchmarks de métricas SaaS para calibrar premissas
- **Damodaran, A.** — NYU Stern datasets e frameworks de valuation
- **Christoph Janz** — "Five Ways to Build a $100M Business" — Framework de revenue modeling para SaaS
- **a16z** — "16 Startup Metrics" — Métricas que importam para modelar startups
