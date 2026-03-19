# CFO Capital Allocation Framework — Alocação de Capital para Decisões de Portfólio

## Origem e Contexto

Capital allocation é a disciplina mais importante do CFO: decidir **onde investir recursos finitos**
para maximizar retorno ajustado ao risco. A cada real alocado, existe um custo de oportunidade —
o retorno do melhor uso alternativo que foi sacrificado. Empresas que dominam capital allocation
consistentemente superam concorrentes em geração de valor de longo prazo.

Este framework combina princípios de **portfolio theory** (Markowitz), **corporate finance** (Damodaran),
e **venture capital discipline** para criar um sistema estruturado de decisão. Ele trata o budget não
como uma planilha estática, mas como um **portfólio de investimentos** que precisa ser otimizado
continuamente contra retorno esperado, risco e alinhamento estratégico.

A premissa central: toda alocação de capital é uma aposta — e apostas devem ter tese, métricas de
sucesso, kill criteria e revisão periódica. Se o capital não tem dono, tese e deadline, é desperdício.

---

## Quando Usar

- Na construção e revisão do budget anual (Annual Planning)
- Em decisões de investimento em novos produtos, mercados ou canais
- Ao avaliar trade-offs entre growth e profitability
- Na priorização de iniciativas que competem por recursos limitados
- Em board meetings quando investidores questionam alocação de recursos
- Ao decidir entre build, buy ou partner
- Na avaliação de M&A opportunities
- Quando runway é limitado e priorização é questão de sobrevivência

---

## Quando NÃO Usar

- Para decisões operacionais de baixo valor (< 1% do budget) — use bom senso
- Quando o investimento já está contratualmente comprometido e irreversível
- Para alocação de tempo de indivíduos (use frameworks de priorização operacional)
- Quando a empresa está em modo de sobrevivência extremo — nesse caso, o framework é "cortar tudo que não gera caixa em 30 dias"
- Para decisões puramente técnicas sem impacto financeiro material

---

## Estrutura / Modelo

### 1. Categorias de Alocação

Todo capital alocado deve ser classificado em uma das seguintes categorias:

| Categoria | Descrição | Risk Profile | Expected Return | Horizonte |
|-----------|-----------|-------------|----------------|-----------|
| **Run the Business** | Manter operações atuais (infra, headcount core, compliance) | Baixo | Preservação | Contínuo |
| **Grow the Business** | Expandir o que já funciona (mais vendas, mais features, mais mercados) | Médio | 2-5x | 6-18 meses |
| **Transform the Business** | Apostar em novos modelos, produtos ou mercados | Alto | 5-10x+ | 12-36 meses |

**Regra de ouro:** A proporção entre estas categorias define o DNA financeiro da empresa.

```
Startup early-stage:    20% Run / 30% Grow / 50% Transform
Startup growth-stage:   30% Run / 50% Grow / 20% Transform
Scale-up:               40% Run / 45% Grow / 15% Transform
Empresa madura:         60% Run / 30% Grow / 10% Transform
```

### 2. Métricas de Avaliação por Investimento

**IRR — Internal Rate of Return**
```
IRR = Taxa que faz NPV = 0

NPV = Σ [Cash Flow_t / (1 + IRR)^t] = 0
      t=0 até n

Critério: IRR > Hurdle Rate (custo de capital + prêmio de risco)
```

**Payback Period**
```
Payback Simples = Investimento Inicial / Cash Flow Anual Esperado

Payback Descontado = Tempo até NPV acumulado ≥ 0

Critério:
- Run: Payback < 6 meses
- Grow: Payback < 18 meses
- Transform: Payback < 36 meses
```

**ROIC — Return on Invested Capital**
```
ROIC = NOPAT / Capital Investido

NOPAT = EBIT × (1 - Tax Rate)
Capital Investido = Equity + Debt - Cash

Critério: ROIC > WACC (criando valor) ou ROIC < WACC (destruindo valor)
```

**Opportunity Cost Score**
```
Para cada R$1 alocado no Projeto A, qual o retorno perdido
do melhor Projeto B que não foi financiado?

OC Score = IRR do projeto escolhido / IRR da melhor alternativa recusada
Ideal: OC Score > 1.0
```

### 3. Matriz de Priorização de Capital

```
                    ALTO RETORNO ESPERADO
                           │
              ┌────────────┼────────────┐
              │  INVEST    │  INVEST    │
              │  (com      │  FIRST     │
              │  hedge)    │  (máxima   │
              │            │  prioridade│
    ALTO      │            │            │
    RISCO ────┼────────────┼────────────┤ BAIXO
              │  EVALUATE  │  INVEST    │ RISCO
              │  (kill     │  (base     │
              │  criteria  │  sólida)   │
              │  rigoroso) │            │
              └────────────┼────────────┘
                           │
                    BAIXO RETORNO ESPERADO
```

---

## Processo de Aplicação

### Fase 1: Inventário de Demandas (Semana 1)

1. Coletar todas as demandas de capital de todos os squads/áreas
2. Classificar cada demanda em Run / Grow / Transform
3. Exigir business case padronizado para cada demanda > 1% do budget
4. Consolidar em uma lista única ordenada por valor solicitado

### Fase 2: Análise Individual (Semana 2-3)

1. Para cada investimento significativo (> 5% do budget):
   - Calcular IRR com cenários (base, otimista, pessimista)
   - Determinar payback period (simples e descontado)
   - Estimar ROIC esperado
   - Identificar riscos e mitigações
   - Definir kill criteria (quando desistir)
2. Para investimentos menores (1-5% do budget):
   - Análise simplificada: payback + alinhamento estratégico
3. Para Run the Business:
   - Validar necessidade (é realmente essencial?)
   - Buscar oportunidades de otimização (fazer mais com menos)

### Fase 3: Otimização de Portfólio (Semana 3-4)

1. Plotar todos os investimentos na Matriz de Priorização
2. Aplicar constraints:
   - Budget total disponível
   - Capacidade de execução (headcount, bandwidth)
   - Dependências entre projetos
   - Diversificação mínima (não apostar tudo em uma tese)
3. Montar portfólio ótimo:
   - Maximizar retorno esperado do portfólio total
   - Respeitar limites de risco por categoria
   - Garantir que Run the Business está coberto primeiro
4. Definir "wait list" — projetos aprovados condicionalmente se capital liberar

### Fase 4: Governança e Acompanhamento (Contínuo)

1. Revisão mensal: investimentos on track?
2. Revisão trimestral: rebalancear portfólio se necessário
3. Kill reviews: projetos Transform que não atingiram gates
4. Reallocation: capital liberado de projetos cancelados volta ao pool

---

## Exemplos Práticos

### Exemplo 1: Startup SaaS com R$ 5M de Budget Anual

**Demandas recebidas: R$ 9M (quase 2x o disponível)**

| Projeto | Categoria | Valor | IRR Est. | Payback | Decisão |
|---------|-----------|-------|----------|---------|---------|
| Infra e salários core | Run | R$ 2.0M | N/A | N/A | Aprovado (essencial) |
| Expansão time comercial | Grow | R$ 1.5M | 85% | 8 meses | Aprovado |
| Novo produto B2C | Transform | R$ 1.8M | 120% | 24 meses | Aprovado parcial (R$ 1.0M, MVP) |
| Marketing performance | Grow | R$ 1.2M | 60% | 10 meses | Aprovado (R$ 0.8M, otimizar primeiro) |
| Escritório novo | Run | R$ 0.8M | N/A | N/A | Recusado (remote-first) |
| Plataforma de dados | Grow | R$ 0.7M | 40% | 14 meses | Wait list |
| Programa de eventos | Grow | R$ 0.5M | 25% | 18 meses | Recusado |
| R&D exploratório IA | Transform | R$ 1.5M | ? | ? | Aprovado (R$ 0.2M, discovery) |

**Alocação final:** R$ 2.0M Run (40%) / R$ 2.3M Grow (46%) / R$ 1.2M Transform (24%) = R$ 5.0M ✓ (ajustado de 9M para 5M com priorização rigorosa)

### Exemplo 2: Kill Decision

Projeto "Novo produto B2C" após 6 meses:
- Investido: R$ 600K de R$ 1.0M alocados
- Resultados: 200 usuários beta vs. meta de 2.000
- NPS: 35 vs. meta de 50
- **Kill criteria atingido:** < 30% da meta de usuários em 6 meses
- **Decisão:** Kill. R$ 400K remanescentes realocados para expansão comercial (IRR comprovado)

---

## Armadilhas Comuns

1. **Sunk cost fallacy** — Continuar investindo em projeto fracassado porque "já gastamos muito." O dinheiro gasto não volta. Avalie apenas o retorno marginal do próximo real investido.

2. **Peanut butter spreading** — Distribuir budget igualmente entre todas as áreas para "ser justo." Capital allocation não é democracia — é meritocracia de retorno.

3. **Ignorar custo de oportunidade** — Aprovar projeto com IRR de 15% quando existem projetos com IRR de 50% esperando na fila. Cada aprovação é uma recusa implícita.

4. **Run the Business creep** — Custos de manutenção crescem silenciosamente e consomem budget de Growth/Transform. Auditar Run the Business trimestralmente.

5. **Overconfidence em projeções** — IRR calculado com premissas otimistas é ficção. Sempre usar cenário pessimista como base de decisão.

6. **Falta de kill criteria** — Investimentos Transform sem gates claros viram "projetos zumbis" que nunca morrem e nunca entregam.

7. **Viés de recência** — Alocar desproporcionalmente para o último sucesso ou fugir do último fracasso, ao invés de analisar o portfólio de forma objetiva.

8. **Ignorar capacidade de execução** — Budget aprovado sem time para executar é capital parado. Alinhar alocação financeira com alocação de pessoas.

---

## Integração com Outros Frameworks

- `frameworks/cfo-strategist/financial-modeling.md` — Modelos financeiros alimentam as projeções de IRR e payback
- `frameworks/cfo-strategist/unit-economics.md` — Unit economics validam premissas de investimento em growth
- `frameworks/cfo-strategist/scenario-planning.md` — Cenários informam o range de retornos esperados
- `frameworks/cfo-strategist/cash-flow-management.md` — Cash disponível define o envelope de capital alocável
- `frameworks/cfo-strategist/budget-governance.md` — Governança garante que alocações são respeitadas e monitoradas
- `frameworks/shared/decision-framework.md` — Capital allocation é decisão Type 1 (parcialmente irreversível)
- `frameworks/vision-strategy/strategy-choice-cascade.md` — Estratégia define as prioridades que guiam a alocação
- `checklists/finance/budget-allocation-quality.md` — Quality gate para validar a alocação proposta
- `templates/finance/budget-allocation-matrix.md` — Template para documentar a alocação final

---

## Referências

- **Damodaran, A.** — "Corporate Finance: Theory and Practice" — Framework de ROIC, WACC e criação de valor
- **Markowitz, H.** — "Portfolio Selection" (1952) — Teoria de portfólio aplicada a decisões corporativas
- **Mauboussin, M.** — "Capital Allocation: Evidence, Analytical Methods, and Assessment Guidance" — Pesquisa sobre capital allocation e value creation
- **Buffett, W.** — Cartas anuais da Berkshire Hathaway — Princípios práticos de alocação de capital
- **Horowitz, B.** — "The Hard Thing About Hard Things" — Capital allocation em startups com runway limitado
- **Graham, P.** — "Default Alive or Default Dead?" — Framework para decisões de capital em early-stage
