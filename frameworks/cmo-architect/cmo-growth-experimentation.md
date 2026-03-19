# CMO Growth Experimentation — Sistema de Experimentação para Crescimento

## Origem e Contexto

Crescimento sustentável não vem de intuição — vem de experimentação disciplinada. O Growth
Experimentation System é a máquina que gera aprendizados rápidos, valida hipóteses com dados
e escala o que funciona. Sem esse sistema, marketing opera por palpite e repete erros.

O princípio central é: toda ação de marketing é uma hipótese até ser validada por dados. A
diferença entre um time de marketing medíocre e um excelente não é a qualidade das ideias
iniciais — é a velocidade com que testam, aprendem e iteram.

Este framework se baseia nas práticas de growth engineering da Airbnb, no sistema ICE de Sean
Ellis (GrowthHackers), no conceito de "experiment velocity" de Brian Balfour (Reforge), e nos
princípios de experimentação estatística rigorosa. Adaptado para times de marketing de diferentes
tamanhos e maturidades.

## Quando Usar

- Na otimização contínua de campanhas e funil
- Ao testar novas mensagens, canais ou ofertas
- Quando métricas estão estagnadas e precisa de novos insights
- Na validação de hipóteses antes de investir budget significativo
- Na construção de cultura de experimentação no time de marketing
- Ao priorizar entre múltiplas ideias de growth

## Quando NÃO Usar

- Como substituto para estratégia (experimentar sem direção é desperdício)
- Quando o volume de dados é insuficiente para significância estatística
- Para decisões irreversíveis que requerem análise profunda (não A/B test)
- Quando o time não tem disciplina para seguir o processo

## Estrutura / Modelo

### Ciclo de Experimentação

```
┌─────────────────────────────────────────────────────┐
│           GROWTH EXPERIMENT CYCLE                    │
│                                                      │
│     ┌──────────┐                                    │
│     │ IDEATE   │ ← Gerar hipóteses                  │
│     └────┬─────┘                                    │
│          │                                           │
│     ┌────▼─────┐                                    │
│     │PRIORITIZE│ ← Scoring ICE                      │
│     └────┬─────┘                                    │
│          │                                           │
│     ┌────▼─────┐                                    │
│     │ DESIGN   │ ← Design do experimento            │
│     └────┬─────┘                                    │
│          │                                           │
│     ┌────▼─────┐                                    │
│     │ EXECUTE  │ ← Rodar o teste                    │
│     └────┬─────┘                                    │
│          │                                           │
│     ┌────▼─────┐                                    │
│     │ ANALYZE  │ ← Medir resultados                 │
│     └────┬─────┘                                    │
│          │                                           │
│     ┌────▼─────┐                                    │
│     │ LEARN    │ ← Registrar aprendizados           │
│     └────┬─────┘                                    │
│          │                                           │
│          └──────→ REPEAT                             │
└─────────────────────────────────────────────────────┘
```

### Framework ICE de Priorização

| Critério | Definição | Escala |
|----------|-----------|--------|
| **I**mpact | Quanto impacto terá na métrica-alvo? | 1-10 |
| **C**onfidence | Quão confiantes estamos que vai funcionar? | 1-10 |
| **E**ase | Quão fácil é implementar e medir? | 1-10 |

**Score ICE** = (Impact + Confidence + Ease) / 3

### Classificação de Experimentos

| Tipo | Escopo | Duração | Risco | Exemplo |
|------|--------|---------|-------|---------|
| **Micro** | 1 variável, 1 canal | 1-2 semanas | Baixo | CTA color test |
| **Standard** | Hipótese completa | 2-4 semanas | Médio | Nova landing page |
| **Strategic** | Novo canal/oferta | 4-8 semanas | Alto | Novo pricing model |

## Processo de Aplicação (step-by-step)

### Step 1: Gerar Hipóteses (Ideation)

Fontes de hipóteses:

- **Dados**: analytics, heatmaps, user recordings, funnel drop-off
- **Clientes**: entrevistas, surveys, NPS comments, support tickets
- **Time**: brainstorms estruturados com SDRs, vendas, CS
- **Mercado**: o que concorrentes testam, tendências do setor
- **Benchmarks**: onde nossas métricas estão abaixo do benchmark?

**Formato da hipótese**:
```
Se [mudança que faremos],
então [resultado esperado],
porque [razão/insight que suporta].

Métrica primária: [qual métrica medimos]
Métrica guardrail: [métrica que não pode piorar]
```

### Step 2: Priorizar com ICE (ou variantes)

Manter backlog de experimentos priorizado:

```
EXPERIMENT BACKLOG
━━━━━━━━━━━━━━━━━━
ID  | Hipótese              | Impact | Conf. | Ease | ICE  | Status
────|───────────────────────|────────|───────|──────|──────|────────
E01 | Nova headline na LP   | 8      | 7     | 9    | 8.0  | Ready
E02 | Email sequence A/B    | 7      | 6     | 8    | 7.0  | Ready
E03 | Pricing page redesign | 9      | 5     | 4    | 6.0  | Backlog
E04 | TikTok awareness      | 6      | 4     | 6    | 5.3  | Backlog
```

**Regra**: rodar o experimento com maior ICE score primeiro.

### Step 3: Design do Experimento

Para cada experimento aprovado, documentar:

```
EXPERIMENT DESIGN CARD
━━━━━━━━━━━━━━━━━━━━━━
ID: E-[número]
Hipótese: [formato se/então/porque]
Tipo: Micro / Standard / Strategic
Owner (DRI): [nome]
Métrica primária: [ex: conversion rate]
Métrica guardrail: [ex: bounce rate não pode subir >5%]
Controle: [o que existe hoje]
Variante: [o que vamos testar]
Tráfego: [% para teste vs controle]
Duração estimada: [semanas]
Sample size necessário: [calculado para 95% confidence]
Start date:
End date:
```

### Step 4: Execução com Rigor

Regras de execução:

1. **Não espiar resultados antes do prazo** (peeking bias)
2. **Não parar o teste cedo** mesmo que pareça óbvio
3. **Controlar variáveis externas**: sazonalidade, campanhas paralelas
4. **Documentar qualquer mudança** durante o período do teste
5. **Garantir sample size adequado** antes de concluir

### Step 5: Análise Estatística

Para cada experimento concluído:

- **Significância estatística**: p-value < 0.05 (95% confidence)?
- **Tamanho do efeito**: a diferença é relevante para o negócio?
- **Segmentos**: resultado é consistente ou varia por segmento?
- **Guardrails**: alguma métrica guardrail foi violada?
- **Conclusão**: Winner / Loser / Inconclusive

**Cuidados estatísticos**:
- Calcular sample size ANTES (power analysis)
- Usar teste adequado (t-test, chi-square, bayesian)
- Considerar multiple testing correction se muitas variantes
- Verificar se dados seguem premissas do teste

### Step 6: Registrar Aprendizados

Manter Learning Registry acessível a todo o time:

```
LEARNING REGISTRY
━━━━━━━━━━━━━━━━━
ID: E-[número]
Data: [data de conclusão]
Hipótese: [original]
Resultado: Winner (+12% conv.) / Loser (-3% conv.) / Inconclusive
Insight: [o que aprendemos que não sabíamos]
Ação: [o que vamos fazer com esse aprendizado]
Applicable to: [onde mais esse insight se aplica]
```

### Step 7: Escalar Winners e Manter Cadência

- **Winners**: implementar permanentemente + explorar variantes
- **Losers**: documentar aprendizado, não repetir o erro
- **Inconclusive**: reformular hipótese ou aumentar sample size

**Meta de cadência**: 2-4 experimentos por semana (ajustar por tamanho do time).

## Exemplos Práticos

### Exemplo 1: Otimização de Landing Page (Micro)

**Hipótese**: "Se mudarmos headline de feature-focused para outcome-focused, conv. sobe 10%"
**Controle**: "Plataforma de gestão de projetos com IA"
**Variante**: "Entregue projetos 30% mais rápido — sem planilhas"
**Resultado**: +18% conversion rate (p < 0.01)
**Insight**: Clientes respondem melhor a outcomes tangíveis que a features
**Ação**: Revisar todas as headlines de campaigns e ad copies

### Exemplo 2: Teste de Novo Canal (Strategic)

**Hipótese**: "LinkedIn Thought Leadership Ads podem gerar awareness qualificado a CAC <R$200"
**Design**: 8 semanas, R$15K budget, 3 creative variations
**Resultado**: CAC R$180, mas quality score 40% abaixo de Google Search
**Insight**: Canal funciona para awareness mas não para direct response
**Ação**: Incluir no portfólio como canal de TOFU, não como driver de pipeline

## Armadilhas Comuns

1. **HiPPO** (Highest Paid Person's Opinion): opinião do chefe sobrepõe dados
2. **Peeking**: olhar resultados parciais e tomar decisão prematura
3. **Underpowered tests**: sample size insuficiente gera falsos negativos
4. **Testing everything**: testar sem hipótese é desperdício
5. **Winner and done**: não explorar por que a variante ganhou
6. **Ignoring losers**: aprendizados de falhas são tão valiosos quanto sucessos
7. **No registry**: testar e esquecer, repetindo erros do passado
8. **Local optima**: micro-otimizações que não movem a métrica macro

## Integração com Outros Frameworks

| Framework | Relação |
|-----------|---------|
| `frameworks/cmo-architect/cmo-positioning-to-performance.md` | Testar elementos da cadeia P2P |
| `frameworks/cmo-architect/cmo-full-funnel-architecture.md` | Experimentar em cada estágio |
| `frameworks/cmo-architect/cmo-channel-portfolio.md` | Testar novos canais |
| `frameworks/cmo-architect/cmo-brand-equity-engine.md` | Testar mensagens de brand |
| `checklists/cmo/cmo-marketing-roi-quality.md` | Qualidade do ROI dos experimentos |
| `checklists/cmo/go-to-market-quality.md` | Validação de GTM via experimentação |

## Referências

- Sean Ellis, "Hacking Growth" (ICE framework, experiment velocity)
- Brian Balfour, Reforge — "Growth Process" e "Experiment Velocity"
- Stefan Thomke, "Experimentation Works" (HBS, 2020)
- Ronny Kohavi, "Trustworthy Online Controlled Experiments" (2020)
- Andrew Chen, "The Cold Start Problem" — growth experimentation
- Airbnb Engineering, "Experiment Platform" papers
- C-Level Squad: `checklists/cmo/cmo-marketing-roi-quality.md`
