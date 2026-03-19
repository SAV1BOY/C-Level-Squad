# Pricing & Value Metric — Precificação Baseada em Valor

> **Domínio:** Growth & GTM
> **Autor de referência:** Patrick Campbell (ProfitWell/Paddle), Madhavan Ramanujam — "Monetizing Innovation"
> **Uso primário:** Definir preço e modelo de cobrança alinhados ao valor percebido pelo cliente.
> **Agente responsável:** cmo-architect / cfo-strategist

---

## Origem e Contexto

A maioria das empresas precifica errado: cost-plus (custo + margem) ou competitor-based (copia o concorrente). Ambas ignoram o elemento mais importante: **quanto valor o cliente percebe e está disposto a pagar.**

Value-based pricing, popularizado por Patrick Campbell (ProfitWell) e Madhavan Ramanujam ("Monetizing Innovation"), parte da premissa que o preço deve refletir o valor entregue ao cliente, não o custo de produção.

O conceito central é a **Value Metric** — a unidade pela qual o cliente paga e que escala com o valor recebido. A value metric ideal tem 3 propriedades:
1. **Alinha com o valor percebido:** Quanto mais o cliente usa/recebe, mais paga.
2. **É previsível:** O cliente consegue estimar quanto vai pagar.
3. **Escala naturalmente:** Conforme o cliente cresce, o preço cresce proporcionalmente.

Exemplos de value metrics:
- Slack: por usuário ativo
- AWS: por compute/storage consumido
- HubSpot: por contatos no CRM
- Stripe: % por transação processada

---

## Quando Usar

- Ao lançar ou re-precificar produto — pricing é a alavanca de crescimento mais subutilizada.
- Quando o churn está alto e clientes dizem "caro demais" — pode ser desalinhamento de value metric.
- Ao escalar para novos segmentos — cada segmento pode ter willingness-to-pay diferente.
- Quando unit economics não fecham — pricing wrong pode ser a causa.
- Trimestralmente, como parte da revisão de GTM — pricing não é "set and forget."

---

## Quando NÃO Usar

- Para fixar preço sem dados — value-based pricing requer pesquisa com clientes reais.
- Em mercados commodity onde preço é definido pelo mercado (ex.: hosting básico).
- Como exercício puramente financeiro sem input de produto e marketing.
- Para justificar preço abusivo — value-based não é "cobrar o máximo possível", é "cobrar proporcional ao valor."

---

## Estrutura / Modelo

### Componentes de Pricing Strategy

```
┌─────────────────────────────────────────────────────────────────────┐
│                    PRICING STRATEGY FRAMEWORK                        │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  1. VALUE METRIC                                                     │
│     └── Por que unidade o cliente paga?                             │
│         (users, transactions, API calls, contacts, revenue %)       │
│                                                                      │
│  2. PRICING MODEL                                                    │
│     └── Como o preço é calculado?                                   │
│         (flat-rate, per-unit, tiered, usage-based, hybrid)          │
│                                                                      │
│  3. TIER STRUCTURE                                                   │
│     └── Good / Better / Best                                        │
│         (Free → Starter → Pro → Enterprise)                         │
│                                                                      │
│  4. PACKAGING                                                        │
│     └── O que está incluído em cada tier?                           │
│         (Features, support level, SLA, limits)                      │
│                                                                      │
│  5. PRICE POINT                                                      │
│     └── Valor específico por tier/unidade                           │
│         (Baseado em WTP research + competitive positioning)         │
│                                                                      │
│  6. DISCOUNTING POLICY                                               │
│     └── Regras para descontos                                       │
│         (Annual vs monthly, volume, strategic)                      │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

### Value Metric Selection Matrix

| Critério | Peso | Candidata A (por usuário) | Candidata B (por transação) |
|----------|------|--------------------------|---------------------------|
| Alinhamento com valor | 30% | 7/10 | 9/10 |
| Previsibilidade | 25% | 9/10 | 6/10 |
| Escalabilidade | 25% | 7/10 | 9/10 |
| Facilidade de comunicar | 20% | 9/10 | 7/10 |
| **Score ponderado** | | **7.9** | **7.8** |

---

## Processo de Aplicação (step-by-step)

### Step 1: Pesquisa de Willingness-to-Pay (WTP)
Conduzir pesquisa com clientes atuais e potenciais usando o método Van Westendorp:
4 perguntas por respondente:
1. "A que preço você consideraria [produto] tão barato que questionaria a qualidade?"
2. "A que preço [produto] começa a parecer caro, mas você ainda consideraria?"
3. "A que preço [produto] é caro demais, mesmo se quisesse não compraria?"
4. "A que preço [produto] é uma barganha?"

Plotar as curvas e encontrar a faixa de preço aceitável.

### Step 2: Identificar a Value Metric
Listar candidatas a value metric e avaliar cada uma:
- **Alinhamento:** O cliente percebe que paga mais quando recebe mais?
- **Previsibilidade:** O cliente consegue estimar o custo mensal antes de comprar?
- **Escalabilidade:** O preço cresce naturalmente conforme o cliente cresce?

Exemplos por tipo de produto:
- CRM: por contatos ou por seats
- Analytics: por eventos/mês ou por data sources
- API: por chamadas/mês
- Marketplace: % por transação

### Step 3: Definir Tier Structure (Good/Better/Best)
Regra dos 3 tiers:
- **Good (Starter):** Entrada acessível. Cobre o job básico. Objetivo: conversão.
- **Better (Pro):** Valor incremental significativo. É o tier que mais clientes devem estar. Objetivo: revenue.
- **Best (Enterprise):** Features avançadas, SLA, suporte dedicado. Objetivo: capturar valor de grandes clientes.

**Princípio:** O tier do meio deve parecer o melhor custo-benefício (anchoring effect).

### Step 4: Definir Packaging (Feature Gating)
Para cada tier, definir:
- **Features incluídas:** Quais funcionalidades estão disponíveis?
- **Limits:** Quantos users/events/storage?
- **Support level:** Self-service, email, chat, telefone, dedicated CSM?
- **SLA:** Uptime commitment, response time?

**Regra:** Features que são core para o job básico não devem ser gated. Gate features que adicionam valor incremental.

### Step 5: Definir Price Points
Usando WTP research + análise competitiva + unit economics:
- **Floor:** Custo de servir + margem mínima aceitável.
- **Ceiling:** Máximo que WTP research indica.
- **Sweet spot:** Onde conversão × preço maximiza revenue.

### Step 6: Testar e Iterar
- **Grandfather existing customers** ao mudar preço — não surpreenda quem já paga.
- **A/B test** com novos clientes quando possível.
- **Revisão trimestral** de métricas: conversion rate por tier, upgrade rate, churn por tier, ARPU trend.

---

## Exemplos Práticos

### Exemplo: SaaS de Project Management

| | Starter | Pro | Enterprise |
|---|---------|-----|------------|
| **Preço** | R$ 29/user/mês | R$ 69/user/mês | Custom |
| **Value metric** | Por usuário ativo | Por usuário ativo | Por usuário ativo |
| **Projetos** | 5 | Ilimitados | Ilimitados |
| **Storage** | 5GB | 100GB | Ilimitado |
| **Integrações** | 3 | Todas | Todas + custom |
| **Suporte** | Email | Chat + email | Dedicated CSM |
| **SLA** | — | 99.9% | 99.99% |
| **Analytics** | Básico | Avançado | Custom + BI export |

**Distribuição esperada:** 20% Starter, 60% Pro, 20% Enterprise.
**ARPU target:** R$ 55/user/mês (weighted average).

---

## Armadilhas Comuns

1. **Precificar pelo custo:** "Custa R$ 10 para servir, vou cobrar R$ 30." Ignora o valor que o cliente recebe. Se resolve problema de R$ 10K/mês, cobrar R$ 500 é leaving money on the table.
2. **Copiar o concorrente:** Se o concorrente precifica errado, você precificará errado também. Começar pelo valor, não pela competição.
3. **Value metric errada:** "Por usuário" quando o valor está na transação. Ou "por transação" quando o valor está na informação gerada.
4. **Muitos tiers:** Mais de 4 tiers confunde o cliente (paradoxo da escolha). 3 tiers é ideal.
5. **Free tier sem limites:** Freemium sem limite claro não converte para pago. O free deve dar gostinho, não substituir o pago.
6. **Nunca mudar preço:** Empresas ficam anos com o mesmo preço por medo de churn. Pricing deve ser revisado trimestralmente.
7. **Desconto como padrão:** Se todo mundo pede desconto e ganha, o preço de lista é ficção. Ter política clara.
8. **Não segmentar preço:** Um preço para todos ignora que diferentes segmentos têm WTP diferentes.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/growth-gtm/stp.md` | O segmento define a WTP. Pricing varia por target segment. |
| `frameworks/growth-gtm/jtbd.md` | O valor do job define o teto de pricing. Jobs mais valiosos permitem preço mais alto. |
| `frameworks/growth-gtm/offer-mechanism.md` | Pricing é componente da oferta. Value stack contextualiza o preço. |
| `frameworks/growth-gtm/growth-loops.md` | Freemium pricing habilita product-led growth loops. |
| `frameworks/vision-strategy/strategy-choice-cascade.md` | "How to Win" pode ser via pricing strategy (low-cost ou premium). |
| `frameworks/operating-system/okrs.md` | OKRs de monetização incluem ARPU, conversion rate, upgrade rate. |

---

## Referências

- Ramanujam, M. & Tacke, G. (2016). *Monetizing Innovation*. Wiley.
- Campbell, P. "Pricing Strategy Guide." ProfitWell/Paddle Blog.
- Simon, H. & Fassnacht, M. (2019). *Price Management*. Springer.
- Nagle, T. & Muller, G. (2018). *The Strategy and Tactics of Pricing*. 6th Ed. Routledge.
- Van Westendorp, P. "Price Sensitivity Meter." NSS Research Methodology.
