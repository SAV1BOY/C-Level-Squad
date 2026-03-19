# Build vs Buy Framework — Decisão de Construir, Comprar ou Parceria

> **Domínio:** Engineering & Tech
> **Autor de referência:** Práticas de CTO/CIO, TCO analysis, Wardley Mapping
> **Uso primário:** Decidir se uma capacidade deve ser construída internamente, comprada (SaaS/licença) ou obtida via parceria.
> **Agente responsável:** cto-architect / cio-engineer

---

## Origem e Contexto

A decisão build vs buy é uma das mais frequentes e consequentes em tecnologia. Construir internamente oferece customização e controle, mas consome tempo e talento escasso. Comprar oferece velocidade e maturidade, mas gera dependência e custos recorrentes. Parceria oferece complementaridade, mas complexidade de coordenação.

O erro mais comum: **decidir com base em bias do time de engenharia** ("nós conseguimos fazer melhor") ou **bias de custo aparente** ("o SaaS custa R$ 5K/mês, fazer internamente é mais barato" — ignorando custo de manutenção, oportunidade e risco).

A decisão correta depende de uma análise que cruza 4 dimensões:
1. **Diferenciação estratégica:** Isso é core ou commodity?
2. **Total Cost of Ownership (TCO):** Quanto custa no total em 3-5 anos?
3. **Time-to-value:** Quanto tempo para entregar valor?
4. **Risco:** Vendor lock-in, dependência, continuidade.

Wardley Mapping (`frameworks/vision-strategy/wardley-mapping.md`) é a ferramenta complementar ideal: componentes em Genesis/Custom → build. Componentes em Product/Commodity → buy.

---

## Quando Usar

- Toda vez que surgir necessidade de nova capacidade técnica (ferramenta, plataforma, serviço).
- Na revisão de stack tecnológico — há soluções internas que poderiam ser substituídas por SaaS?
- Ao escalar — o que era OK fazer internamente com 10 devs pode não fazer sentido com 50.
- Em decisões de M&A (acqui-hire vs build vs partner).
- No planejamento de budget de tecnologia — build vs buy impacta CAPEX vs OPEX.

---

## Quando NÃO Usar

- Para decisões triviais (< R$ 5K/ano) — não vale o custo da análise.
- Quando a resposta é óbvia — ninguém deveria construir um email server em 2026.
- Como substituto de conversa — a análise informa, mas a decisão requer julgamento.
- Para justificar decisão já tomada — fazer a análise honestamente, não para confirmar bias.

---

## Estrutura / Modelo

### Decision Matrix

```
┌─────────────────────────────────────────────────────────────────────┐
│              BUILD vs BUY DECISION MATRIX                            │
├──────────────────┬──────────────┬──────────────┬───────────────────┤
│ Critério         │    BUILD     │     BUY      │    PARTNER        │
├──────────────────┼──────────────┼──────────────┼───────────────────┤
│ Core differentia-│ ✅ Forte     │ ❌ Fraco     │ ⚠️  Médio         │
│ tion (é core?)   │ (controle)   │ (commodity)  │ (complementar)    │
├──────────────────┼──────────────┼──────────────┼───────────────────┤
│ Time-to-value    │ ❌ Lento     │ ✅ Rápido    │ ⚠️  Médio         │
│                  │ (meses)      │ (dias/semanas│ (depende)         │
├──────────────────┼──────────────┼──────────────┼───────────────────┤
│ TCO 3 anos       │ ⚠️  Variável │ ⚠️  Variável │ ⚠️  Variável      │
│                  │ (dev + maint)│ (SaaS + integ│ (rev share + integ│
├──────────────────┼──────────────┼──────────────┼───────────────────┤
│ Customização     │ ✅ Total     │ ❌ Limitada  │ ⚠️  Negociável    │
├──────────────────┼──────────────┼──────────────┼───────────────────┤
│ Vendor lock-in   │ ✅ Zero      │ ❌ Alto      │ ⚠️  Médio         │
├──────────────────┼──────────────┼──────────────┼───────────────────┤
│ Manutenção       │ ❌ Interna   │ ✅ Fornecedor│ ⚠️  Compartilhada │
│                  │ (time dedic.)│ (incluída)   │                   │
├──────────────────┼──────────────┼──────────────┼───────────────────┤
│ Risco de         │ ❌ Time sai  │ ❌ Vendor    │ ❌ Parceiro       │
│ continuidade     │ (bus factor) │ fecha/pivota │ muda prioridades  │
└──────────────────┴──────────────┴──────────────┴───────────────────┘
```

### Scoring Model

| Critério | Peso | Build (1-10) | Buy (1-10) | Partner (1-10) |
|----------|------|-------------|-----------|---------------|
| Diferenciação estratégica | 30% | | | |
| TCO 3 anos | 25% | | | |
| Time-to-value | 20% | | | |
| Risco (lock-in, continuidade) | 15% | | | |
| Fit com capabilities existentes | 10% | | | |
| **Score ponderado** | 100% | | | |

---

## Processo de Aplicação (step-by-step)

### Step 1: Classificar — Core ou Commodity?
Usar Wardley Mapping para posicionar o componente:
- **Genesis/Custom-Built:** Provavelmente build. É novo, único, e diferencia.
- **Product:** Avaliar. Se o produto de mercado atende 80%+, buy. Se precisa de customização profunda, build.
- **Commodity:** Sempre buy. Não construa o que todo mundo já tem.

Perguntar: "Se nosso competidor usa a mesma ferramenta, perdemos vantagem?" Se sim → build. Se não → buy.

### Step 2: Calcular TCO (Total Cost of Ownership)
Para BUILD, incluir:
- Custo de desenvolvimento (headcount × meses).
- Custo de manutenção ongoing (20-30% do custo de desenvolvimento por ano).
- Custo de oportunidade (o que esses devs fariam se não estivessem neste projeto?).
- Custo de infra (hosting, monitoring, backups).

Para BUY, incluir:
- Licença/assinatura (SaaS) × 36 meses.
- Custo de integração e customização.
- Custo de migração (entrada E saída).
- Custo de training.
- Custo de lock-in (o que custa trocar se precisar?).

Usar `frameworks/it-information/total-cost-of-ownership.md` para análise detalhada.

### Step 3: Avaliar Time-to-Value
- BUILD: Quantos meses até a primeira versão usável? E até feature-parity com alternativa de mercado?
- BUY: Quanto tempo para integrar, configurar e treinar?
- PARTNER: Quanto tempo para assinar, integrar e ir ao mercado?

### Step 4: Avaliar Riscos
Para cada opção, listar e classificar riscos:
- **BUILD risks:** Bus factor (1 dev que sabe), scope creep, never-done syndrome.
- **BUY risks:** Vendor descontinua produto, preço sobe, API breaking changes.
- **PARTNER risks:** Parceiro muda estratégia, exclusividade limitada, conflito de prioridades.

### Step 5: Decidir e Documentar como ADR
Usando o scoring model, tomar a decisão e registrar como ADR (`frameworks/engineering-tech/adr-system.md`):
- Incluir contexto, alternativas avaliadas, score e rationale.
- Definir kill criteria: "Se em 6 meses o build não atingir [X], reavaliar para buy."

### Step 6: Revisão Periódica
O que era build 3 anos atrás pode ser commodity hoje. Revisar anualmente:
- O componente ainda diferencia? Ou virou commodity?
- O custo de manutenção justifica vs alternativa de mercado?
- Novas opções surgiram desde a decisão original?

---

## Exemplos Práticos

### Exemplo 1: Sistema de Autenticação
**Análise:** Autenticação é commodity. Auth0, Clerk, Firebase Auth são maduros.
**Decisão:** BUY (Auth0). TCO de build (6 meses de dev + manutenção de segurança) >> SaaS. Zero diferenciação.
**Exceção:** Se você É uma empresa de identidade/segurança, então build.

### Exemplo 2: Motor de Recomendação
**Análise:** Recomendação personalizada é core value prop do produto.
**Decisão:** BUILD. Diferenciação estratégica alta. Nenhum SaaS entende nosso domínio. TCO maior, mas valor estratégico justifica.
**ADR:** "Build motor de recomendação. Revisão em 12 meses se performance não atingir benchmark X."

### Exemplo 3: Plataforma de Analytics Interna
**Análise:** Analytics é Product (não mais commodity, não é core).
**Decisão:** BUY (Metabase self-hosted + Mixpanel para product analytics). Boa customização, custo razoável, time foca no core.

---

## Armadilhas Comuns

1. **NIH Syndrome (Not Invented Here):** Time de engenharia quer construir tudo. "Nosso ORM vai ser melhor." Provavelmente não.
2. **Ignorar custo de manutenção:** Build parece barato no mês 1. No mês 36, a manutenção consome 2 devs full-time.
3. **Ignorar custo de oportunidade:** Os devs construindo o componente poderiam estar construindo features de produto que geram receita.
4. **Subestimar integração do buy:** "É plug-and-play" raramente é verdade. Budget integração como 30-50% do custo da licença.
5. **Vendor lock-in como desculpa para build:** Algum lock-in é aceitável. O custo de evitar TODO lock-in é maior que o risco.
6. **Decisão emocional:** "Odeia vendor X" ou "ama technology Y" não são critérios. Dados e análise primeiro.
7. **Não revisar:** A decisão de build de 2023 pode ser obsoleta em 2026. O mercado evoluiu.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/vision-strategy/wardley-mapping.md` | Posição no mapa define se build (Genesis) ou buy (Commodity). |
| `frameworks/engineering-tech/adr-system.md` | Toda decisão build/buy/partner gera ADR. |
| `frameworks/it-information/total-cost-of-ownership.md` | TCO é o framework detalhado de análise de custo. |
| `frameworks/engineering-tech/architecture-patterns.md` | Arquitetura define como componentes comprados se integram. |
| `frameworks/operating-system/decision-memo-framework.md` | Decisões > R$ 200K usam Decision Memo completo. |
| `checklists/vendor-selection-quality.md` | Checklist para avaliar vendors na opção BUY. |
| `checklists/tech-architecture-decision-quality.md` | Checklist para validar a análise build vs buy. |

---

## Referências

- Wardley, S. "Build vs Buy: Using Wardley Maps." Medium.
- Fowler, M. "SacrificialArchitecture." martinfowler.com.
- Skelton, M. & Pais, M. (2019). *Team Topologies*. IT Revolution. (Cognitive load e decisões de build.)
- Gartner. "Total Cost of Ownership Analysis Framework."
