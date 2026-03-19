# Unit Economics Engine — Motor de Economia Unitária para Escala Sustentável

## Origem e Contexto

Enquanto o framework de Unit Economics básico responde "nossas métricas estão saudáveis?", o
Unit Economics Engine responde a pergunta mais profunda: **"como construímos um sistema que
monitora, diagnostica e otimiza unit economics continuamente?"**

Este framework transforma unit economics de uma análise pontual em um **motor operacional** —
um sistema vivo que conecta CAC, LTV, payback, contribution margin e cohort analysis com
decisões diárias de go-to-market, produto e engenharia. O engine não apenas mede; ele **alerta,
diagnostica causas raiz e recomenda ações**.

A diferença entre empresas que escalam com sucesso e empresas que crescem para morrer está na
capacidade de operar este engine em tempo real. Quando CAC sobe 15% no meio do trimestre, a
empresa que tem o engine detecta em dias, diagnostica a causa e corrige. A empresa sem o engine
descobre no board meeting — três meses depois, quando o caixa já evaporou.

O conceito de "engine" vem da disciplina de growth engineering: tratar métricas financeiras não
como outputs passivos, mas como sinais de controle em um sistema de feedback loop.

---

## Quando Usar

- Como sistema operacional contínuo (não é análise one-off)
- Na construção de dashboards financeiros automatizados
- Quando a empresa atinge scale (> 100 clientes ou > R$ 1M ARR)
- Para diagnosticar deterioração de métricas antes que vire crise
- Na preparação para fundraising (investidores querem ver o engine, não só os números)
- Ao avaliar entrada em novos segmentos ou canais
- Para conectar decisões de produto com impacto financeiro
- Quando CFO e CMO precisam de linguagem comum sobre eficiência

---

## Quando NÃO Usar

- Pre-product-market fit (< 50 clientes) — foco deve ser em validação, não em otimização
- Quando dados não são confiáveis — engine com dados ruins gera decisões piores que intuição
- Para substituir experimentação — engine otimiza o que existe, não descobre o que não existe
- Quando a empresa tem um único cliente dominante (> 50% da receita) — a "unidade" não é representativa
- Para justificar cortar investimento em inovação — engine mede eficiência, não potencial

---

## Estrutura / Modelo

### 1. Componentes do Engine

```
┌──────────────────────────────────────────────────────────────┐
│                    UNIT ECONOMICS ENGINE                       │
│                                                               │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐    │
│  │ COLETA   │→ │ CÁLCULO  │→ │ ANÁLISE  │→ │ AÇÃO     │    │
│  │ de Dados │  │ de       │  │ e        │  │ e        │    │
│  │          │  │ Métricas │  │ Alertas  │  │ Feedback │    │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘    │
│       ↑                                          │           │
│       └──────────────────────────────────────────┘           │
│                     FEEDBACK LOOP                             │
└──────────────────────────────────────────────────────────────┘
```

### 2. Métricas do Engine — Camada por Camada

**Camada 1: Métricas de Aquisição**
```
CAC Blended = Total S&M spend / Total new customers
CAC Paid = Paid channel spend / Paid channel customers
CAC Organic = Organic costs (content, SEO team) / Organic customers
CAC por Canal = Channel spend / Channel customers
CAC Efficiency = 1 / CAC (quanto menor CAC, maior eficiência)

Fully-Loaded CAC inclui:
  + Salários do time de marketing e vendas
  + Ferramentas de sales/marketing (CRM, ads platforms)
  + Comissões e bonificações
  + Agências e freelancers
  + Overhead alocado proporcionalmente
```

**Camada 2: Métricas de Monetização**
```
ARPA (Average Revenue Per Account) = MRR total / Contas ativas
ARPU (Average Revenue Per User) = MRR total / Usuários ativos
ACV (Annual Contract Value) = Valor médio anual por contrato

Contribution Margin por Cliente:
  Receita do cliente
  - COGS direto (hosting, suporte, processamento)
  = Contribution Margin

  CM% = Contribution Margin / Receita × 100
```

**Camada 3: Métricas de Retenção**
```
Logo Retention = 1 - (Clientes churned / Clientes início do período)
Revenue Retention (GRR) = (MRR início - Contraction - Churn) / MRR início
Net Revenue Retention (NRR) = (MRR início + Expansion - Contraction - Churn) / MRR início

Cohort Retention Rate por mês:
  M0: 100% (por definição)
  M1: [X]% — indica quality of onboarding
  M3: [X]% — indica product-market fit
  M6: [X]% — indica core value delivery
  M12: [X]% — indica long-term stickiness
```

**Camada 4: Métricas Compostas**
```
LTV = ARPA × Gross Margin% × (1 / Monthly Churn Rate)
LTV por Cohort = Σ receita acumulada da cohort × GM%

LTV:CAC Ratio = LTV / CAC
  < 1:1 → Destruindo valor
  1-3:1 → Zona de otimização
  3:1   → Benchmark saudável
  > 5:1 → Possível sub-investimento em growth

Payback Period = CAC / (ARPA × Gross Margin%)
  < 6 meses → Excelente, investir agressivamente
  6-12 meses → Saudável para SMB
  12-18 meses → Aceitável para enterprise
  > 18 meses → Modelo precisa de ajuste

CAC Payback-Adjusted LTV:CAC = (LTV discounted) / CAC
  Desconta LTV pelo custo de capital para refletir o valor temporal do dinheiro
```

### 3. Dashboard do Engine

```
┌─────────────────────────────────────────────────────────┐
│             UNIT ECONOMICS ENGINE DASHBOARD               │
├─────────────────────────────────────────────────────────┤
│                                                          │
│  CAC Blended: R$ 850    [↓5% MoM]  ✅ Meta: < R$ 1.000 │
│  CAC Paid:    R$ 1.200  [↑8% MoM]  ⚠️ Meta: < R$ 1.100 │
│  ARPA:        R$ 2.100  [↑2% MoM]  ✅ Meta: > R$ 2.000 │
│  CM%:         72%       [→ estável] ✅ Meta: > 70%       │
│  LTV:         R$ 50.4K  [↑3% MoM]  ✅ Meta: > R$ 40K   │
│  LTV:CAC:     3.5:1     [↑ trend]  ✅ Meta: > 3:1       │
│  Payback:     9.2 meses [↓ trend]  ✅ Meta: < 12 meses  │
│  NRR:         112%      [→ estável] ✅ Meta: > 110%      │
│                                                          │
│  ALERTAS:                                                │
│  ⚠️ CAC Paid subiu 8% — investigar: Meta Ads CPL +12%   │
│  ⚠️ Cohort Jan/26 com retenção M3 abaixo da média       │
│                                                          │
├─────────────────────────────────────────────────────────┤
│  COHORT HEATMAP (Logo Retention %)                       │
│                                                          │
│         M0   M1   M3   M6   M9   M12                    │
│  Jul/25 100  88   76   68   64   61                     │
│  Ago/25 100  89   78   70   66    -                     │
│  Set/25 100  90   79   71    -    -                     │
│  Out/25 100  87   74    -    -    -                     │
│  Nov/25 100  91   80    -    -    -                     │
│  Dez/25 100  85    -    -    -    -   ← Investigar      │
│  Jan/26 100  82    -    -    -    -   ← ALERTA          │
└─────────────────────────────────────────────────────────┘
```

---

## Processo de Aplicação

### Fase 1: Instrumentação (Semanas 1-4)

1. **Mapear fontes de dados:**
   - CRM (HubSpot, Salesforce) → leads, conversões, deals
   - Billing (Stripe, sistema interno) → MRR, churn, expansion
   - Analytics (Mixpanel, Amplitude) → usage, activation, engagement
   - Ads platforms → spend por canal
   - HR/Finance → headcount costs, fully-loaded CAC
2. **Definir a "unidade"** — cliente, conta, ou transação
3. **Construir pipeline de dados** — automatizar coleta diária/semanal
4. **Validar dados históricos** — reconciliar com financeiro contábil

### Fase 2: Cálculo e Baseline (Semanas 4-6)

1. Calcular todas as métricas das 4 camadas com dados históricos
2. Construir cohort analysis com pelo menos 6-12 cohorts
3. Segmentar métricas por: canal, plano, tamanho de cliente, vertical
4. Estabelecer baselines e targets por métrica
5. Definir thresholds de alerta (amarelo e vermelho)

### Fase 3: Dashboard e Alertas (Semanas 6-8)

1. Construir dashboard automatizado (Metabase, Looker, Sheets)
2. Configurar alertas automáticos para desvios > threshold
3. Criar cadência de review:
   - Semanal: CAC, conversão, churn (sinais rápidos)
   - Mensal: LTV, NRR, cohort analysis (sinais de tendência)
   - Trimestral: deep dive por segmento, recalibrar targets

### Fase 4: Operacionalização (Contínuo)

1. **Reunião semanal de Unit Economics** (30 min):
   - Revisar alertas da semana
   - Identificar causas raiz
   - Definir ações corretivas com DRI e deadline
2. **Review mensal com CFO + CMO + CPO:**
   - Tendências de cohort
   - Impacto de mudanças de produto/pricing/canal
   - Ajustes de target para próximo mês
3. **Deep dive trimestral:**
   - Recalcular LTV com dados atualizados
   - Reclassificar segmentos
   - Atualizar modelo financeiro com inputs reais

---

## Exemplos Práticos

### Exemplo 1: Diagnóstico de CAC Rising

**Sinal:** CAC Paid subiu de R$ 900 para R$ 1.200 em 3 meses

**Diagnóstico pelo Engine:**
```
Decomposição do CAC Paid:
  CPL (Cost Per Lead):     R$ 45 → R$ 62   (+38%) ← CAUSA RAIZ
  Lead-to-MQL rate:        30% → 28%        (-7%)
  MQL-to-SQL rate:         25% → 24%        (-4%)
  SQL-to-Close rate:       20% → 19%        (-5%)

  CAC = CPL / (L→MQL × MQL→SQL × SQL→Close)
  CAC = R$ 62 / (0.28 × 0.24 × 0.19) = R$ 62 / 0.0128 = R$ 4.844 por lead ÷ ...

  Principal driver: CPL subiu 38% (competição em Meta Ads)
  Secundário: Funil degradou levemente em todas as etapas
```

**Ações recomendadas pelo Engine:**
1. Diversificar canais (testar Google Ads, LinkedIn, content/SEO)
2. Otimizar criativo de ads (A/B test com novas abordagens)
3. Melhorar lead scoring para focar em leads de maior qualidade
4. Revisar ICP — estamos atraindo o público certo?

### Exemplo 2: Cohort Analysis Revelando Problema

**Sinal:** Cohorts dos últimos 3 meses com retenção M3 caindo

```
Cohort M3 Retention (histórico):
  Jul/25: 76%  |  Ago/25: 78%  |  Set/25: 79%  ← Tendência positiva
  Out/25: 74%  |  Nov/25: 71%  |  Dez/25: 68%  ← TENDÊNCIA NEGATIVA

Investigação:
  - Deploy do novo onboarding em Set/25 → impacto negativo?
  - Mudança de ICP? Novas cohorts vêm de canal diferente?
  - Seasonal effect? (Dez/25 = empresas com budget congelado)

Correlação encontrada: cohorts pós-Out/25 têm 40% mais clientes
de segmento SMB (que tem churn naturalmente maior) vs. 25% antes.

Causa raiz: Nova campanha de Meta Ads está atraindo SMB em excesso.
```

---

## Armadilhas Comuns

1. **Vanity metrics** — Medir MAU sem conectar com monetização. O engine deve ligar usage → revenue → unit economics.

2. **LTV com churn de steady state em empresa jovem** — Se você tem 18 meses de história, não use churn rate "estabilizado" para projetar LTV de 5 anos.

3. **Blended metrics escondem problemas** — CAC blended de R$ 800 pode esconder CAC paid de R$ 2.000 e CAC orgânico de R$ 200. Segmentar sempre.

4. **Cohort analysis sem segmentação** — Cohorts totais escondem que Enterprise retém 95% e SMB retém 50%. Decisões diferentes para segmentos diferentes.

5. **Otimizar CAC sem considerar LTV** — Reduzir CAC cortando quality de leads gera churn maior e LTV menor. Olhar o sistema, não a métrica isolada.

6. **Não atualizar LTV** — LTV calculado há 6 meses com premissas que já mudaram. Recalcular mensalmente com dados reais de cohort.

7. **Confundir correlação com causação** — "Churn subiu quando mudamos o pricing" não significa que pricing causou o churn. Investigar com rigor.

8. **Engine sem ação** — Dashboard bonito que ninguém usa para tomar decisão. Cada alerta deve ter DRI e deadline de investigação.

---

## Integração com Outros Frameworks

- `frameworks/cfo-strategist/unit-economics.md` — Framework base de conceitos; o Engine operacionaliza
- `frameworks/cfo-strategist/financial-modeling.md` — Unit economics são os drivers do modelo financeiro
- `frameworks/cfo-strategist/cfo-capital-allocation.md` — Unit economics validam premissas de investimento
- `frameworks/cfo-strategist/cash-flow-management.md` — Payback period impacta diretamente a gestão de caixa
- `frameworks/cmo-architect/growth-loop-framework.md` — Growth loops devem ser avaliados pelo engine
- `checklists/finance/unit-economics-audit.md` — Audit periódico da qualidade das métricas do engine
- `templates/finance/unit-economics-dashboard.md` — Template de dashboard padronizado

---

## Referências

- **David Skok** — "SaaS Metrics 2.0" — Framework canônico de unit economics para SaaS
- **Bill Gurley** — "The Dangerous Seduction of the LTV Formula" — Armadilhas de LTV
- **Lenny Rachitsky** — Benchmarks de retenção e growth por vertical
- **ChartMogul** — "SaaS Benchmarks Report" — Dados de benchmark para calibrar o engine
- **Reforge** — Growth Loops e Unit Economics integration
- **Andrew Chen** — "The Law of Shitty Clickthroughs" — Por que CAC sobe com o tempo
