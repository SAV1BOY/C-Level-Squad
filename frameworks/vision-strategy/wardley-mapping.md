# Wardley Mapping — Mapeamento Estratégico de Value Chain

> **Domínio:** Vision & Strategy
> **Autor de referência:** Simon Wardley — "Wardley Maps"
> **Uso primário:** Visualizar a cadeia de valor, entender evolução de componentes e tomar decisões estratégicas contextuais.
> **Agente responsável:** vision-chief / cto-architect

---

## Origem e Contexto

Wardley Mapping foi criado por Simon Wardley, ex-CEO da Fotango (subsidiária do grupo Canon), nos anos 2000. Wardley percebeu que a maioria das decisões estratégicas era tomada sem um "mapa" — o equivalente a um general tentando vencer uma batalha sem mapear o terreno.

O insight central: **todos os componentes de uma cadeia de valor evoluem por estágios previsíveis** — de Genesis (novo, incerto) até Commodity (padronizado, utility). Entender onde cada componente está nessa evolução muda radicalmente a estratégia correta.

Um Wardley Map tem dois eixos:
- **Eixo Y (Visibilidade):** Quão visível o componente é para o usuário final. Topo = visível, base = infraestrutura invisível.
- **Eixo X (Evolução):** Estágio evolutivo do componente — Genesis → Custom-Built → Product (+Rental) → Commodity (+Utility).

O mapa resultante mostra a cadeia de valor completa e permite identificar oportunidades estratégicas: o que construir internamente, o que comprar, onde investir, onde desinvestir, e como se posicionar competitivamente.

---

## Quando Usar

- Decisões de build vs buy vs partner (`frameworks/engineering-tech/build-vs-buy-framework.md`).
- Definição de estratégia de plataforma e ecossistema.
- Análise competitiva — entender onde competir e onde cooperar.
- Planejamento de arquitetura de sistemas — quais componentes são differentiators vs commodity.
- Discussões de M&A — visualizar o que a aquisição adiciona à cadeia de valor.
- Strategy offsites — mapas são ferramentas visuais poderosas de comunicação.
- Avaliação de riscos de vendor lock-in e dependências tecnológicas.

---

## Quando NÃO Usar

- Para decisões táticas de curto prazo que não envolvem a cadeia de valor.
- Quando falta conhecimento básico sobre a cadeia de valor — é preciso entender o negócio antes de mapear.
- Como ferramenta isolada — Wardley Maps são mais poderosos quando combinados com outros frameworks.
- Em contextos onde a precisão absoluta é necessária — mapas são aproximações úteis, não modelos exatos.
- Se não há tempo para o exercício completo — um mapa superficial pode enganar mais do que ajudar.

---

## Estrutura / Modelo

```
Visibilidade (Usuário)
    │
    │  [Necessidade do Usuário]
    │        │
    │   [Componente A]──────[Componente B]
    │        │                     │
    │   [Componente C]        [Componente D]
    │        │                     │
    │   [Componente E]────────────┘
    │        │
    │   [Componente F]
    │
    └──────────────────────────────────────────────
         Genesis    Custom-Built    Product    Commodity
```

### Estágios de Evolução

| Estágio | Características | Gestão Adequada | Exemplo |
|---------|----------------|-----------------|---------|
| **Genesis** | Novo, incerto, alto risco, alto potencial | Ágil, exploratório, tolerar falhas | Blockchain em 2015 |
| **Custom-Built** | Funciona, mas feito sob medida. Diferencial competitivo | Lean, iterativo, foco em aprendizado | CRM interno em 2005 |
| **Product (+Rental)** | Produtos de mercado disponíveis. Competição por features | Best practices, eficiência, comparação | Salesforce, AWS EC2 |
| **Commodity (+Utility)** | Padronizado, volume, preço. Essencial mas não diferencia | Outsource, SLA, custo mínimo | Eletricidade, email hosting |

---

## Processo de Aplicação (step-by-step)

### Step 1: Identificar o Usuário e Suas Necessidades
Quem é o usuário do sistema? Quais são suas necessidades fundamentais? Posicionar no topo do mapa.

### Step 2: Mapear a Cadeia de Valor
De cima para baixo, listar todos os componentes necessários para atender cada necessidade:
- O que o usuário vê/interage diretamente? (topo)
- O que é necessário para entregar isso? (meio)
- O que sustenta a infraestrutura? (base)

Desenhar as dependências (setas de cima para baixo).

### Step 3: Posicionar na Evolução
Para cada componente, avaliar seu estágio evolutivo:
- **Ubiquidade:** Quão disponível é no mercado?
- **Certeza:** Quão bem entendido é?
- **Maturidade:** Há práticas estabelecidas?

### Step 4: Identificar Movimentos Estratégicos
Com o mapa pronto, identificar oportunidades:
- **Componentes em Genesis/Custom que poderiam ser substituídos por Product/Commodity:** Economia de custo e foco.
- **Componentes em Product que estão virando Commodity:** Trocar build por buy. Renegociar contratos.
- **Componentes em Genesis que são differentiators:** Investir, proteger, construir competência.
- **Inércia:** Onde a organização resiste à evolução?

### Step 5: Aplicar Gameplays
Simon Wardley documentou dezenas de gameplays (padrões estratégicos):
- **Ecosystem play:** Construir plataforma em cima de commodities para capturar valor acima.
- **ILC (Innovate-Leverage-Commoditize):** Modelo da Amazon — inovar, escalar, comoditizar, repetir.
- **Tower and moat:** Posicionar-se em componentes de alto valor e difícil substituição.
- **Open approach:** Abrir componentes que estão comoditizando para acelerar evolução e capturar valor em camadas adjacentes.
- **Signal distortion:** Competidores podem sinalizar evolução falsa para confundir o mercado.

### Step 6: Tomar Decisões e Documentar
Usar o mapa para informar decisões em:
- `frameworks/engineering-tech/build-vs-buy-framework.md` — build para Genesis/Custom, buy para Product/Commodity.
- `frameworks/engineering-tech/architecture-patterns.md` — arquitetura reflete a evolução dos componentes.
- `frameworks/operating-system/decision-memo-framework.md` — incluir o mapa no memo de decisão.

### Step 7: Revisar e Atualizar
Mapas são vivos. Componentes evoluem. Revisar trimestralmente ou quando há mudança significativa no mercado/tecnologia.

---

## Exemplos Práticos

### Exemplo: Plataforma de E-commerce

```
[Cliente quer comprar online]
        │
   [Storefront/UX]         ← Custom-Built (diferenciador)
        │
   [Payment Processing]    ← Commodity (usar Stripe/PagSeguro)
   [Search/Recommendations]← Product (Algolia) ou Custom (se é core)
   [Inventory Management]  ← Product (ERP) ou Custom (se escala exige)
        │
   [Cloud Infrastructure]  ← Commodity (AWS/GCP)
   [CDN]                   ← Commodity (CloudFront/Cloudflare)
   [Monitoring]            ← Product (Datadog/New Relic)
```

**Decisões derivadas:**
- Storefront/UX é differentiator → build interno, investir em time de design.
- Payment → commodity → usar API de terceiro. Não construir gateway próprio.
- Search → depende: se recomendação personalizada é core value prop, custom-build. Se não, Algolia.
- Cloud → commodity → avaliar multi-cloud para evitar lock-in excessivo.

### Exemplo: Decisão de Build vs Buy para CRM
Mapeando CRM no eixo de evolução: CRM é Product/Commodity. Existem dezenas de opções maduras (Salesforce, HubSpot, Pipedrive). Construir CRM interno só faz sentido se:
- O CRM é parte CORE da proposta de valor (ex.: empresa de CRM).
- Requisitos são tão únicos que nenhum produto de mercado atende.

Na vasta maioria dos casos: buy, não build.

---

## Armadilhas Comuns

1. **Mapa sem decisão:** Mapear é meio, não fim. Se o mapa não gera ação estratégica, foi exercício acadêmico.
2. **Precisão excessiva:** A posição exata de um componente no eixo X é subjetiva. O valor está na posição relativa e na discussão.
3. **Mapa estático:** Componentes evoluem. Um mapa antigo pode estar desatualizado. Revisar periodicamente.
4. **Ignorar inércia organizacional:** O mapa mostra onde os componentes DEVERIAM estar, mas a organização pode resistir.
5. **Confundir evolução com qualidade:** Um componente em Genesis não é "pior" que um em Commodity — é diferente.
6. **Mapear sozinho:** Mapas são ferramentas de conversa. Fazer em grupo gera insights superiores e alinhamento.
7. **Não considerar o mapa do competidor:** Seu mapa é mais útil quando comparado com o mapa (estimado) dos competidores.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/engineering-tech/build-vs-buy-framework.md` | O mapa informa diretamente: Genesis → build, Commodity → buy. |
| `frameworks/engineering-tech/architecture-patterns.md` | Componentes em diferentes estágios requerem arquiteturas diferentes. |
| `frameworks/vision-strategy/three-horizons.md` | Genesis = H3, Custom-Built = H2, Product/Commodity = H1. |
| `frameworks/vision-strategy/strategy-choice-cascade.md` | O mapa torna visíveis as capabilities necessárias (pergunta 4 do cascade). |
| `frameworks/vision-strategy/scenario-planning.md` | Cenários diferentes podem mover componentes em velocidades diferentes. |
| `frameworks/engineering-tech/platform-engineering.md` | Wardley Maps mostram quais componentes comoditizar via plataforma interna. |
| `checklists/tech-architecture-decision-quality.md` | Decisões de arquitetura devem referenciar posição no mapa. |

---

## Referências

- Wardley, S. (2020). *Wardley Maps: The Use of Topographical Intelligence in Business Strategy*. (Disponível gratuitamente em medium.com/wardleymaps.)
- Wardley, S. *On Being Lost* — série de posts no Medium que documenta toda a teoria.
- LearnWardleyMapping.com — recursos interativos e exemplos.
- MapCamp — conferência anual sobre Wardley Mapping.
- Wardley, S. "Doctrine" — 40 princípios universais de boa estratégia derivados de mapping.
