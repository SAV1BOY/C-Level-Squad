# Cash Flow Management Framework — Gestão de Caixa para Sobrevivência e Crescimento

## Origem e Contexto

"Revenue is vanity, profit is sanity, cash is reality." Esta frase resume por que cash flow
management é o framework mais urgente do CFO. Empresas lucrativas no papel podem quebrar por
falta de caixa. Empresas com prejuízo contábil podem prosperar com gestão de caixa disciplinada.
A diferença entre as duas está neste framework.

Cash flow management vai muito além de "olhar o saldo bancário." É um sistema integrado de
**forecasting** (prever), **monitoring** (acompanhar), **optimizing** (otimizar) e **protecting**
(proteger) o recurso mais precioso da empresa: dinheiro disponível. Em startups, runway é
literalmente a medida de quanto tempo você tem para acertar. Em empresas maduras, working capital
optimization é uma das alavancas mais poderosas de geração de valor.

Este framework combina técnicas de **treasury management**, **working capital optimization** e
**startup finance** em um sistema prático que funciona desde a seed stage até o scale-up.

---

## Quando Usar

- Como prática operacional contínua (weekly cash review)
- Na construção e atualização do cash forecast (rolling 13 semanas + 12 meses)
- Ao identificar necessidade de funding (antes que vire emergência)
- Em períodos de crise ou incerteza econômica (gestão defensiva)
- Quando burn rate está acelerando e runway diminuindo
- Na negociação de termos de pagamento com fornecedores e clientes
- Ao avaliar impacto de cash de decisões estratégicas (contratação, expansão, M&A)
- Na preparação para fundraising (investidores avaliam gestão de caixa)

---

## Quando NÃO Usar

- Para análise de rentabilidade (use DRE e unit economics)
- Para avaliação de investimentos de longo prazo (use NPV/IRR no capital allocation framework)
- Para contabilidade fiscal — cash flow management é gerencial, não contábil
- Quando a empresa tem caixa abundante (> 36 meses de runway) — foque em alocação, não em sobrevivência

---

## Estrutura / Modelo

### 1. Cash Flow Dashboard

```
┌──────────────────────────────────────────────────────────┐
│              CASH FLOW COMMAND CENTER                      │
├──────────────────────────────────────────────────────────┤
│                                                           │
│  POSIÇÃO ATUAL                                           │
│  Caixa disponível:     R$ 3.200K                         │
│  Investimentos líquidos: R$ 800K                         │
│  Posição total:        R$ 4.000K                         │
│                                                           │
│  BURN & RUNWAY                                           │
│  Net burn mensal:      R$ 320K    [↑5% vs mês anterior]  │
│  Gross burn mensal:    R$ 580K    [→ estável]            │
│  Runway (net burn):    12.5 meses                        │
│  Runway (gross burn):  6.9 meses  [worst case]           │
│                                                           │
│  FORECAST 13 SEMANAS                                     │
│  Saldo projetado S+4:  R$ 2.900K                         │
│  Saldo projetado S+8:  R$ 2.500K                         │
│  Saldo projetado S+13: R$ 2.050K                         │
│  Mínimo projetado:     R$ 2.050K  (S13)                  │
│                                                           │
│  ALERTAS                                                 │
│  ⚠️ Runway < 12 meses — iniciar processo de fundraising   │
│  ✅ Working capital cycle estável (45 dias)                │
│  ✅ Nenhum pagamento grande nos próximos 30 dias           │
└──────────────────────────────────────────────────────────┘
```

### 2. Métricas Fundamentais

**Burn Rate:**
```
Gross Burn = Total de saídas de caixa no período
Net Burn = Saídas - Entradas de caixa no período

Se Net Burn é negativo → empresa é cash-flow positive (gera caixa)

Exemplo:
  Receita recebida:   R$ 260K
  Despesas pagas:     R$ 580K
  Net Burn:           R$ 320K/mês
  Gross Burn:         R$ 580K/mês
```

**Runway:**
```
Runway (meses) = Caixa Disponível / Net Burn Mensal

Zona de conforto:
  > 18 meses: Seguro — foco em growth
  12-18 meses: Atenção — planejar próximo funding
  6-12 meses: Alerta — iniciar fundraising ou cortar custos
  < 6 meses: Emergência — modo sobrevivência
```

**Working Capital Cycle:**
```
Cash Conversion Cycle (CCC) = DSO + DIO - DPO

DSO (Days Sales Outstanding) = (Contas a Receber / Receita) × 365
DIO (Days Inventory Outstanding) = (Estoque / COGS) × 365
DPO (Days Payable Outstanding) = (Contas a Pagar / COGS) × 365

Exemplo SaaS (sem estoque):
  DSO = 35 dias (clientes pagam em média em 35 dias)
  DIO = 0 (sem estoque)
  DPO = 30 dias (pagamos fornecedores em 30 dias)
  CCC = 35 + 0 - 30 = 5 dias

Quanto menor o CCC, melhor a eficiência de caixa.
CCC negativo = fornecedores financiam a operação (modelo marketplace ideal).
```

### 3. Modelo de Forecasting — 3 Horizontes

```
┌──────────────────────────────────────────────────────┐
│  HORIZONTE 1: 13-Week Cash Forecast (Operacional)    │
│  Granularidade: Semanal                               │
│  Precisão esperada: ±5%                               │
│  Atualização: Semanal (toda segunda-feira)            │
│  Método: Bottom-up (recebimentos + pagamentos reais) │
├──────────────────────────────────────────────────────┤
│  HORIZONTE 2: 12-Month Cash Projection (Tático)      │
│  Granularidade: Mensal                                │
│  Precisão esperada: ±15%                              │
│  Atualização: Mensal (após fechamento)               │
│  Método: Driver-based (receita × conversion, etc.)   │
├──────────────────────────────────────────────────────┤
│  HORIZONTE 3: 3-Year Cash Outlook (Estratégico)      │
│  Granularidade: Trimestral/Anual                     │
│  Precisão esperada: ±30%                              │
│  Atualização: Trimestral (QBR)                       │
│  Método: Scenario-based (bull/base/bear)             │
└──────────────────────────────────────────────────────┘
```

### 4. Alavancas de Otimização de Caixa

**Lado da Receita (Acelerar Entradas):**
```
1. Cobrar upfront (anual ao invés de mensal) — desconto de 10-20%
2. Reduzir DSO: cobranças automatizadas, penalidade por atraso
3. Milestone billing em contratos de serviço
4. Antecipação de recebíveis (factoring) como último recurso
5. Deposits e adiantamentos para projetos grandes
```

**Lado do Custo (Desacelerar/Reduzir Saídas):**
```
1. Negociar termos de pagamento maiores (30→45→60 dias)
2. Renegociar contratos anuais de SaaS (pagar mensal em crise)
3. Postergar CAPEX não essencial
4. Reduzir headcount growth rate (não necessariamente demitir)
5. Consolidar ferramentas e fornecedores
6. Revisar assinaturas e serviços não utilizados
```

**Working Capital Optimization:**
```
1. Implementar sistema de cobrança automatizada
2. Oferecer incentivos para pagamento antecipado
3. Segmentar clientes por risco de inadimplência
4. Centralizar tesouraria (conta única para visibilidade)
5. Alocar excedente em investimentos de alta liquidez
```

---

## Processo de Aplicação

### Fase 1: Setup do Sistema (Semanas 1-2)

1. Centralizar visão de caixa (todas as contas bancárias em um dashboard)
2. Mapear todos os recebimentos recorrentes e suas datas
3. Mapear todos os pagamentos recorrentes e suas datas
4. Identificar pagamentos variáveis e sazonais
5. Construir template do 13-week forecast
6. Definir responsável (DRI) pela atualização semanal

### Fase 2: Diagnóstico (Semanas 2-3)

1. Calcular burn rate (gross e net) dos últimos 6 meses
2. Calcular runway atual
3. Analisar working capital cycle (DSO, DPO)
4. Identificar os top 10 pagamentos por valor
5. Identificar clientes com pagamento atrasado
6. Mapear obrigações futuras (contratos, hiring commitments)
7. Avaliar sazonalidade de receita e custo

### Fase 3: Forecasting (Semana 3-4)

1. Construir 13-week forecast bottom-up:
   - Semana por semana: quais recebimentos são esperados?
   - Semana por semana: quais pagamentos estão programados?
   - Incluir buffers para imprevistos (5-10% de variância)
2. Construir 12-month projection:
   - Derivar do modelo financeiro (P&L → Cash Flow)
   - Incorporar 3 cenários (bull, base, bear)
   - Identificar meses de maior pressão de caixa
3. Definir "minimum cash balance" — saldo mínimo que nunca deve ser violado
   - Regra: 3 meses de gross burn como piso absoluto

### Fase 4: Operação Contínua

1. **Segunda-feira:** Atualizar 13-week forecast com dados reais da semana anterior
2. **Mensal:** Reconciliar forecast vs. actual, ajustar projeções
3. **Trimestral:** Deep dive em working capital, renegociar termos se necessário
4. **Trigger-based:** Se runway < 12 meses, ativar protocolo de fundraising/cost-cutting

---

## Exemplos Práticos

### Exemplo 1: 13-Week Cash Forecast

```
| Semana        | Saldo Inicial | Entradas  | Saídas    | Saldo Final |
|---------------|--------------|-----------|-----------|-------------|
| S1 (17/Mar)   | R$ 3.200K    | R$ 180K   | R$ 145K   | R$ 3.235K   |
| S2 (24/Mar)   | R$ 3.235K    | R$ 95K    | R$ 130K   | R$ 3.200K   |
| S3 (31/Mar)   | R$ 3.200K    | R$ 120K   | R$ 290K*  | R$ 3.030K   |
| S4 (07/Abr)   | R$ 3.030K    | R$ 200K   | R$ 140K   | R$ 3.090K   |
| ...           | ...          | ...       | ...       | ...         |
| S13 (16/Jun)  | R$ 2.150K    | R$ 160K   | R$ 260K   | R$ 2.050K   |

* S3: Folha de pagamento + aluguel trimestral
Mínimo projetado: R$ 2.050K (S13) — acima do piso de R$ 1.740K (3× gross burn) ✅
```

### Exemplo 2: Decisão de Fundraising Timing

```
Situação:
  Caixa atual: R$ 4.0M
  Net burn: R$ 320K/mês (crescendo 3%/mês)
  Runway: ~11.5 meses

Regra: Iniciar fundraising com 9-12 meses de runway
        (fundraising leva 3-6 meses)

Análise de cenários:
  Base: Fecha round em 6 meses → runway mínimo de 5.5 meses ✅
  Bear: Fundraising leva 9 meses → runway mínimo de 2.5 meses ⚠️

Decisão: Iniciar fundraising AGORA + ativar plano de contenção de burn
  - Congelar contratações não-essenciais (economia de R$ 80K/mês)
  - Renegociar contratos de SaaS (economia de R$ 20K/mês)
  - Novo net burn projetado: R$ 220K/mês → runway estende para 16 meses
```

### Exemplo 3: Working Capital Optimization

```
Antes:
  DSO = 45 dias | DPO = 30 dias | CCC = 15 dias
  Capital imobilizado: R$ 450K

Ações:
  1. Implementar cobrança automática D+3 (Asaas/Vindi)
  2. Desconto de 5% para pagamento antecipado
  3. Migrar 40% dos clientes para billing anual upfront
  4. Renegociar DPO com fornecedores-chave (30→45 dias)

Depois:
  DSO = 28 dias | DPO = 45 dias | CCC = -17 dias
  Capital liberado: R$ 450K + R$ 170K adicional = R$ 620K

  CCC negativo = fornecedores financiam a operação
```

---

## Armadilhas Comuns

1. **Confundir lucro com caixa** — Empresa lucrativa pode ter caixa negativo se DSO é alto e DPO é baixo. Cash flow e P&L são análises diferentes.

2. **Forecast anual sem rolling update** — Budget de caixa feito em janeiro e nunca mais atualizado. Cash forecast deve ser rolling e atualizado semanalmente.

3. **Ignorar sazonalidade** — Empresa com 60% da receita no Q4 precisa de reserva de caixa para os 3 primeiros trimestres.

4. **Runway calculado com net burn decrescente** — "Burn vai cair porque vamos crescer receita." Calcular runway com burn atual ou crescente para ser conservador.

5. **Não ter minimum cash balance** — Operar com caixa zero como meta. Sempre manter piso de 3-6 meses de gross burn.

6. **Late fundraising** — Iniciar fundraising com 3 meses de runway é modo pânico. Investidores percebem desespero e negociam termos piores.

7. **Cortar na proteína** — Em crise de caixa, cortar investimento em produto/engenharia (a fonte de valor futuro) ao invés de otimizar custos administrativos primeiro.

8. **Não monitorar concentração de receita** — 40% da receita vem de 1 cliente que paga a 60 dias. Se atrasar, crise imediata.

---

## Integração com Outros Frameworks

- `frameworks/cfo-strategist/financial-modeling.md` — O modelo financeiro gera a projeção de cash flow
- `frameworks/cfo-strategist/cfo-capital-allocation.md` — Cash disponível define o envelope de capital alocável
- `frameworks/cfo-strategist/unit-economics-engine.md` — Payback period impacta diretamente cash consumption
- `frameworks/cfo-strategist/budget-governance.md` — Budget governance controla as saídas de caixa
- `frameworks/cfo-strategist/fundraising-readiness.md` — Cash management informa timing de fundraising
- `frameworks/cfo-strategist/scenario-planning.md` — Cenários stress-testam o cash position
- `checklists/finance/cash-flow-quality.md` — Quality gate para validar projeções de caixa
- `templates/finance/cash-flow-projection.md` — Template para projeção 12 meses com cenários

---

## Referências

- **Mulford, C. & Comiskey, E.** — "Creative Cash Flow Reporting" — Detecção de manipulação de cash flow
- **Sagner, J.** — "Essentials of Working Capital Management" — Otimização de working capital
- **Wilson, F.** — "Burn Rate" (AVC blog) — Framework prático de burn rate para startups
- **Horowitz, B.** — "The Hard Thing About Hard Things" — Gestão de caixa em tempos de crise
- **Graham, P.** — "Default Alive or Default Dead?" — Diagnóstico binário de saúde de caixa
- **Stripe Atlas** — "Guide to Startup Finance" — Fundamentos de cash management para startups
