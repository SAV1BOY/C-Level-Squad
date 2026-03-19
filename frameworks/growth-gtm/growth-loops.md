# Growth Loops — Loops de Crescimento Composto

> **Domínio:** Growth & GTM
> **Autor de referência:** Reforge (Brian Balfour, Casey Winters, Andrew Chen)
> **Uso primário:** Identificar e otimizar mecanismos de crescimento que se auto-alimentam e compõem.
> **Agente responsável:** cmo-architect

---

## Origem e Contexto

Growth Loops é um modelo mental desenvolvido pela Reforge (Brian Balfour, Casey Winters) que substitui o funil linear (AARRR/Pirate Metrics) por loops que se retroalimentam. A premissa: **o crescimento sustentável não vem de funis — vem de loops onde o output de um ciclo é o input do próximo.**

A diferença fundamental entre crescimento linear e composto:
- **Linear (funil):** Cada novo cliente requer investimento incremental. Se parar de investir, o crescimento para.
- **Composto (loop):** Cada novo cliente gera ações que atraem mais clientes. O crescimento se auto-alimenta.

Exemplos clássicos:
- **Pinterest:** Novo usuário cria pin → pin indexado no Google → novo visitante encontra via SEO → cria conta → cria mais pins → loop.
- **Slack:** Time adota → convida outro time → outro time adota → convida parceiros → loop.
- **HubSpot:** Cria conteúdo → atrai visitantes → visitantes usam free tool → compartilham resultado → mais visitantes → loop.

O modelo identifica 4 tipos principais de loops, e toda empresa deveria ter pelo menos 1 loop dominante funcionando.

---

## Quando Usar

- Ao definir estratégia de crescimento — entender qual loop é o motor principal do negócio.
- Quando o CAC está subindo e a empresa precisa de canais de crescimento mais eficientes.
- No planejamento de produto — features que alimentam o loop devem ser priorizadas.
- Para avaliar sustentabilidade do crescimento — crescimento dependente 100% de paid ads é frágil.
- Ao analisar competidores — qual loop eles dominam? Podemos competir nesse loop?

---

## Quando NÃO Usar

- Pré-product-market fit — antes de PMF, o foco é validar o job e a solução, não escalar loops.
- Como substituto de execução básica — se o produto tem bugs e o suporte é ruim, nenhum loop salva.
- Para justificar "crescimento orgânico" sem investimento — loops precisam de investimento para iniciar e otimizar.
- Quando o mercado é muito pequeno para loop — em nichos com 500 clientes potenciais, outbound direto é mais eficiente.

---

## Estrutura / Modelo

### Os 4 Tipos de Growth Loops

```
┌─────────────────────────────────────────────────────────────────────┐
│                    GROWTH LOOPS FRAMEWORK                            │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  1. VIRAL LOOP                    2. CONTENT LOOP                   │
│  ┌──────────────────┐            ┌──────────────────┐              │
│  │ User → Invites → │            │ Create content → │              │
│  │ New user → Uses →│            │ SEO/Social → New │              │
│  │ Invites more     │            │ visitor → Signs  │              │
│  │                  │            │ up → Creates     │              │
│  └──────────────────┘            │ more content     │              │
│  Ex: Slack, Dropbox              └──────────────────┘              │
│                                  Ex: Pinterest, HubSpot            │
│                                                                      │
│  3. PAID LOOP                     4. PRODUCT-LED LOOP              │
│  ┌──────────────────┐            ┌──────────────────┐              │
│  │ Revenue → Invest │            │ Use product →    │              │
│  │ in ads → New     │            │ Create artifact →│              │
│  │ customer →       │            │ Artifact shared →│              │
│  │ Revenue → ...    │            │ New user sees →  │              │
│  └──────────────────┘            │ Signs up         │              │
│  Ex: Performance mkt             └──────────────────┘              │
│  quando LTV > CAC                Ex: Figma, Notion, Loom          │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

### Anatomia de um Loop

Cada loop tem 3 componentes:
1. **Input:** O que entra no loop (novo usuário, conteúdo, investimento).
2. **Action:** O que o participante faz dentro do loop (cria, compartilha, compra).
3. **Output → New Input:** Como o output retroalimenta o input (referral, SEO, revenue reinvestido).

**Métrica-chave: Loop efficiency**
- Para viral: K-factor (quantos novos usuários cada usuário gera)
- Para content: organic growth rate (crescimento de tráfego orgânico)
- Para paid: payback period (tempo para recuperar CAC)
- Para product-led: activation rate × share rate

---

## Processo de Aplicação (step-by-step)

### Step 1: Mapear Loops Existentes
Antes de criar novos loops, mapear os que já existem (mesmo que não intencionalmente):
- Analisar de onde vêm os clientes (attribution data).
- Identificar se algum canal se auto-alimenta.
- Perguntar: "Se parássemos todo investimento em aquisição, o que continuaria crescendo?"

### Step 2: Identificar o Loop Dominante
Toda empresa de sucesso tem um loop dominante. Qual é o seu?
- **B2B SaaS com produto simples:** Product-led (free tier → uso → compartilhamento → novo usuário)
- **B2B SaaS enterprise:** Content loop (thought leadership → SEO → MQLs → clientes → case studies → mais autoridade)
- **Marketplace:** Network effect loop (mais sellers → mais buyers → mais sellers)
- **E-commerce:** Paid loop (revenue → reinvestir em ads → mais revenue) ou content loop (SEO)

### Step 3: Desenhar o Loop em Detalhe
Para o loop dominante, mapear cada step:
```
[Input: Novo visitante via SEO]
    ↓
[Action: Usa free tool / lê conteúdo]
    ↓
[Conversion: Cria conta free]
    ↓
[Activation: Usa o produto e resolve job]
    ↓
[Output: Cria artefato (report, dashboard) e compartilha]
    ↓
[New Input: Colega vê artefato → visita o site → novo visitante]
```

### Step 4: Medir Cada Step do Loop
Para cada transição, medir a taxa de conversão:
- Visitante → Sign-up: X%
- Sign-up → Activated: Y%
- Activated → Shares: Z%
- Shares → New visitor: W%
- **Loop efficiency = X × Y × Z × W**

### Step 5: Otimizar o Bottleneck
O ponto mais fraco do loop é o bottleneck. Focar 80% do esforço no bottleneck:
- Se Activated → Shares é 2%, este é o bottleneck. Como incentivar compartilhamento?
- Se Sign-up → Activated é 10%, o onboarding é o problema.
- Não otimizar tudo ao mesmo tempo. Um bottleneck por vez.

### Step 6: Adicionar Loops Secundários
Depois que o loop dominante funciona, adicionar loops secundários:
- Se o dominante é content, adicionar viral loop (referral program).
- Se o dominante é paid, adicionar content loop (SEO) para reduzir dependência.
- Diversificar gradualmente, sem perder foco no dominante.

---

## Exemplos Práticos

### Exemplo 1: SaaS B2B de Analytics (Product-Led)
```
[User cria account free]
    → [Conecta dados e cria dashboard]
    → [Compartilha dashboard com stakeholder]
    → [Stakeholder vê dashboard e cria próprio account]
    → [Novo user cria dashboard...]
```
**Loop efficiency:** 1000 sign-ups → 300 activated → 60 shared → 18 new sign-ups = 1.8% efficiency.
**Bottleneck:** Activated → Shared (20%). Ação: tornar compartilhamento 1-click, adicionar branding no shared dashboard.

### Exemplo 2: E-commerce D2C (Content + Paid)
**Content loop:** Blog posts → SEO → visitantes → compra → review → mais SEO signals → mais visitantes.
**Paid loop:** Revenue → 30% reinvestido em Meta Ads → novos clientes → revenue.
**Meta:** Content loop assume 40% da aquisição em 18 meses, reduzindo dependência de paid de 90% para 60%.

---

## Armadilhas Comuns

1. **Funil, não loop:** Pensar em funil linear (topo → meio → fundo) em vez de loop (output → novo input). O funil não se auto-alimenta.
2. **Loop sem medição:** "Temos viralidade" sem medir K-factor é wishful thinking.
3. **Otimizar o errado:** Melhorar o step que já funciona em vez de focar no bottleneck. 80/20.
4. **Dependência de um único loop:** Paid-only é frágil (CPM sobe, margem cai). Diversificar loops gradualmente.
5. **Loop sem product-market fit:** Crescer via loop com produto ruim = churn amplificado. PMF primeiro, loop depois.
6. **Forçar viralidade:** Nem todo produto é naturalmente viral. Forçar "invite 5 friends" em produto B2B enterprise é ridículo.
7. **Ignorar cohort analysis:** O loop parece funcionar no agregado, mas cohorts mais recentes têm eficiência menor. Medir por cohort.
8. **Confundir growth hack com growth loop:** Growth hack é tática pontual. Growth loop é sistema sustentável.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/growth-gtm/stp.md` | O segmento define qual loop é mais natural (B2B enterprise = content, PLG = product-led). |
| `frameworks/growth-gtm/jtbd.md` | O job do cliente informa qual ação dentro do loop é natural (share se o job é social). |
| `frameworks/growth-gtm/offer-mechanism.md` | A oferta pode ser desenhada para alimentar loops (referral bonus, freemium). |
| `frameworks/growth-gtm/pricing-value-metric.md` | Pricing freemium habilita product-led loop. |
| `frameworks/growth-gtm/brand-to-demand.md` | Brand building alimenta content loops de longo prazo. |
| `frameworks/operating-system/okrs.md` | OKRs de growth devem incluir métricas de loop efficiency. |
| `frameworks/engineering-tech/dora-metrics.md` | Deploy frequency afeta velocidade de iteração nos loops. |

---

## Referências

- Balfour, B. "Growth Loops are the New Funnels." Reforge Blog.
- Chen, A. (2021). *The Cold Start Problem*. Harper Business.
- Winters, C. "Why Growth Loops are the Future." Reforge.
- Cagan, M. (2018). *Inspired: How to Create Tech Products Customers Love*. Wiley.
- Ellis, S. & Brown, M. (2017). *Hacking Growth*. Currency.
