# OGSM — Objectives, Goals, Strategies, Measures

> **Domínio:** Vision & Strategy
> **Autor de referência:** Procter & Gamble (popularização), Marc van Eck & Ellen van Zanten
> **Uso primário:** Plano estratégico em uma página — da visão à métrica.
> **Agente responsável:** vision-chief / coo-orchestrator

---

## Origem e Contexto

O OGSM (Objectives, Goals, Strategies, Measures) é um framework de planejamento estratégico que cabe em uma única página. Popularizado pela Procter & Gamble nas décadas de 1950-60, tornou-se o padrão interno de planejamento da empresa por décadas. A premissa é brutal na sua simplicidade: se sua estratégia não cabe em uma página, você não a entendeu.

O modelo conecta quatro camadas de forma linear e rastreável:

1. **Objective (Objetivo):** O quê queremos alcançar? Declaração qualitativa e inspiradora.
2. **Goals (Metas):** Quanto e quando? Metas quantificáveis que comprovam o atingimento do objetivo.
3. **Strategies (Estratégias):** Como? As escolhas que faremos para atingir as metas.
4. **Measures (Medidas):** Como sabemos que a estratégia está funcionando? KPIs e dashboards.

A grande força do OGSM é a **rastreabilidade vertical**: cada medida liga-se a uma estratégia, que liga-se a uma meta, que liga-se ao objetivo. Se algo não conecta, está sobrando.

O OGSM complementa o OKR — enquanto OKR foca em ciclos trimestrais de execução, o OGSM é o plano anual/plurianual que dá contexto estratégico aos OKRs.

---

## Quando Usar

- Planejamento anual ou trienal — consolidar toda a estratégia em uma página por unidade de negócio.
- Comunicação para board, investidores ou all-hands — visão clara e objetiva do plano.
- Quando OKRs existem mas falta contexto estratégico — o OGSM é a "camada acima" dos OKRs.
- Para alinhar múltiplas áreas em torno de um plano coerente — cada área pode ter seu OGSM derivado do OGSM corporativo.
- Em processos de budget — o OGSM justifica alocação de recursos por estratégia.

---

## Quando NÃO Usar

- Para planejamento tático semanal — OGSM é estratégico, não operacional. Use OKRs + WBR para isso.
- Em contextos de altíssima incerteza onde a estratégia muda mensalmente — o OGSM pressupõe estabilidade mínima de 6-12 meses.
- Como substituto de análise competitiva profunda — OGSM é output de estratégia, não input.
- Para equipes pequenas (< 5 pessoas) que não precisam de formalização — nesse caso, OKRs são suficientes.
- Quando o objetivo real é parecer estratégico sem ser — OGSM não sobrevive a review sério se as estratégias forem vazias.

---

## Estrutura / Modelo

```
┌─────────────────────────────────────────────────────────────────────┐
│                        OGSM — One-Page Plan                         │
├─────────────────────────────────────────────────────────────────────┤
│ OBJECTIVE (Qualitativo — o quê queremos ser/alcançar)               │
│ "Ser a plataforma de referência em gestão financeira para PMEs      │
│  no Brasil, reconhecida por simplicidade e resultado."              │
├─────────────────────────────────────────────────────────────────────┤
│ GOALS (Quantitativo — quanto e quando)                              │
│ G1: Atingir R$ 50M ARR até Dez/2027                                │
│ G2: NPS ≥ 70 mantido por 4 trimestres consecutivos                 │
│ G3: Market share de 15% no segmento PME (faturamento 1-10M)        │
├─────────────────────────────────────────────────────────────────────┤
│ STRATEGIES (Como — escolhas estratégicas)                           │
│ S1: Product-led growth com free tier agressivo                      │
│ S2: Partnerships com contadores como canal de distribuição          │
│ S3: Expansão de módulos (crédito, folha) via build + integração     │
├─────────────────────────────────────────────────────────────────────┤
│ MEASURES (KPIs por estratégia)                                      │
│ S1 → Activation rate, PQL→SQL conversion, time-to-value            │
│ S2 → # Partners ativos, revenue via canal, partner NPS             │
│ S3 → Adoption rate por módulo, revenue incremental, integration %  │
└─────────────────────────────────────────────────────────────────────┘
```

---

## Processo de Aplicação (step-by-step)

### Step 1: Definir o Objective
Escrever uma frase qualitativa que descreva o estado futuro desejado. Deve ser:
- Inspiradora, mas realista.
- Entendível por qualquer pessoa na organização.
- Estável por pelo menos 12 meses.
- Alinhada com a tese estratégica do vision-chief (ver `frameworks/vision-chief/vision-chief-strategic-thesis.md`).

### Step 2: Quantificar os Goals
Para cada dimensão relevante (financeira, cliente, produto, mercado), definir metas SMART:
- **Specific:** O que exatamente?
- **Measurable:** Qual número?
- **Achievable:** É possível com os recursos disponíveis?
- **Relevant:** Conecta ao Objective?
- **Time-bound:** Até quando?

Regra prática: 3-5 goals. Menos de 3 = falta de ambição. Mais de 5 = falta de foco.

### Step 3: Escolher as Strategies
Estratégias são ESCOLHAS, não desejos. Para cada strategy, perguntar:
- O que estamos DECIDINDO fazer (e, portanto, decidindo NÃO fazer)?
- Se esta estratégia funcionar, quais Goals ela endereça?
- Temos capacidade (ou podemos construí-la) para executar esta estratégia?

Usar o Strategy Choice Cascade (`frameworks/vision-strategy/strategy-choice-cascade.md`) como input para essa etapa.

### Step 4: Definir Measures por Estratégia
Cada estratégia precisa de 2-4 KPIs que permitam saber se a estratégia está funcionando:
- **Leading indicators:** Métricas de input/atividade (ex.: # demos realizadas).
- **Lagging indicators:** Métricas de output/resultado (ex.: revenue de novos clientes).

### Step 5: Validar Coerência Vertical
Ler o OGSM de baixo para cima: se as Measures melhoram → as Strategies estão funcionando → os Goals serão atingidos → o Objective será alcançado. Se qualquer link quebra, revisar.

### Step 6: Cascatear para Áreas
O OGSM corporativo gera OGSMs por área. A Strategy "S2: Partnerships com contadores" vira o Objective do OGSM da área de parcerias. Os Goals da área derivam das Measures da estratégia corporativa.

### Step 7: Revisar na Cadência de QBR
O OGSM é revisado trimestralmente na QBR (`frameworks/operating-system/wbr-mbr-qbr.md`). Perguntas-chave:
- Os Goals estão on-track? Se não, por quê?
- Alguma Strategy precisa ser ajustada?
- O Objective ainda faz sentido dado o contexto de mercado?

---

## Exemplos Práticos

### Exemplo 1: Startup B2B SaaS (Série A)
| Camada | Conteúdo |
|--------|----------|
| **O** | Ser a solução #1 de automação de procurement para mid-market no Brasil. |
| **G** | G1: R$ 8M ARR até Dez/2027. G2: 120 clientes pagantes. G3: Net Revenue Retention ≥ 110%. |
| **S** | S1: Outbound focado em diretores de compras (ICP definido). S2: Produto self-service para tail. S3: Integração nativa com ERPs top-5. |
| **M** | S1: # SQLs/mês, win rate, ACV. S2: Sign-up → activated %, MRR self-service. S3: # integrações live, adoption rate. |

### Exemplo 2: Área de Marketing (derivado do OGSM corporativo)
| Camada | Conteúdo |
|--------|----------|
| **O** | Posicionar a marca como autoridade em procurement inteligente, gerando demanda qualificada. |
| **G** | G1: 500 MQLs/mês. G2: Brand awareness de 25% no ICP. G3: CAC ≤ R$ 2.500. |
| **S** | S1: Content engine com SEO + LinkedIn. S2: Eventos setoriais como patrocinador. S3: Customer stories como proof-of-concept. |
| **M** | S1: Organic traffic, keyword rankings, MQL via content. S2: Leads por evento, brand recall survey. S3: # cases publicados, influence on pipeline. |

---

## Armadilhas Comuns

1. **Objective vago demais:** "Ser a melhor empresa do Brasil" não é objetivo — é slogan. O Objective deve ter escopo claro (mercado, segmento, diferencial).
2. **Goals sem baseline:** Definir "NPS ≥ 70" sem saber o NPS atual é chute, não meta.
3. **Strategies como atividades:** "Fazer 10 webinars" é tática, não estratégia. Estratégia é a ESCOLHA ("content-led demand gen"), a tática é o desdobramento.
4. **Measures desconectadas:** KPIs que não ligam à estratégia. Se a measure melhora mas a strategy não avança, a measure está errada.
5. **OGSM como documento morto:** Escrever no Q1 e nunca mais olhar. OGSM só funciona com revisão trimestral rigorosa.
6. **Cascateamento mecânico:** Copiar o OGSM corporativo para as áreas sem adaptação. Cada área traduz para seu contexto.
7. **Confundir OGSM com OKR:** OGSM é anual/plurianual e estratégico. OKR é trimestral e de execução. São complementares.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/operating-system/okrs.md` | OKRs são o desdobramento trimestral das Strategies e Measures do OGSM. O OGSM dá contexto; o OKR dá ritmo. |
| `frameworks/vision-strategy/strategy-choice-cascade.md` | O cascade alimenta as escolhas de Strategy no OGSM. Where to Play → Objective. How to Win → Strategies. |
| `frameworks/vision-strategy/three-horizons.md` | O OGSM pode ter versões por horizonte — H1 com OGSM de otimização, H2 com OGSM de escala. |
| `frameworks/operating-system/wbr-mbr-qbr.md` | O OGSM é revisado na QBR. As Measures alimentam o dashboard da WBR/MBR. |
| `checklists/okr-quality.md` | Checklist para garantir que os OKRs derivados do OGSM são de qualidade. |
| `checklists/annual-planning-quality.md` | Checklist para validar a qualidade do OGSM durante o planejamento anual. |

---

## Referências

- Van Eck, M. & Van Zanten, E. (2014). *OGSM: The One Page Plan*. S2N Publishing.
- Procter & Gamble Internal Strategy Methodology (referência histórica).
- Lafley, A.G. & Martin, R. (2013). *Playing to Win*. Harvard Business Review Press.
- Doerr, J. (2018). *Measure What Matters*. Portfolio.
