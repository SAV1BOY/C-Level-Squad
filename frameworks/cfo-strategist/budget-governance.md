# Budget Governance Framework — Governança Orçamentária para Accountability e Performance

## Origem e Contexto

Budget governance é o sistema que garante que o capital alocado é **gasto conforme o planejado,
monitorado rigorosamente e ajustado quando necessário**. Sem governança, budget é um exercício
de ficção — planeja-se em janeiro e a realidade diverge em março sem que ninguém perceba, reaja
ou seja responsabilizado.

Este framework trata budget não como um documento estático, mas como um **contrato operacional**
entre o CFO e cada líder de área. O contrato tem três componentes: **allocation rules** (como
distribuir), **variance tracking** (como monitorar desvios), e **reforecasting** (como ajustar
quando a realidade muda). A accountability é o elo que conecta tudo — cada real tem um dono, um
propósito e uma métrica de sucesso.

A inspiração vem de práticas de **Amazon (OP1/OP2)**, **Google (OKR-linked budgets)** e
**venture-backed startups** onde capital é escasso e cada decisão de gasto é uma aposta com
retorno mensurável. O objetivo é criar um sistema onde gastar bem é tão valorizado quanto gastar
menos.

---

## Quando Usar

- Na construção do budget anual (Annual Planning / OP1)
- Nas revisões mensais de budget (MBR financeiro)
- Nas revisões trimestrais com reforecast (QBR financeiro)
- Ao aprovar pedidos de budget incremental (acima do planejado)
- Quando variações significativas (> 10%) são detectadas
- Na comunicação com board sobre performance financeira
- Ao avaliar performance de líderes de área (accountability)
- Na definição de regras de autoridade para gastos

---

## Quando NÃO Usar

- Para micro-gestão de gastos operacionais de baixo valor
- Quando a empresa está em modo de sobrevivência (< 3 meses de runway) — governança cede lugar a triage
- Para substituir bom senso — governança é framework, não burocracia
- Quando a empresa ainda não tem estrutura de áreas/squads definida (pre-seed)
- Para bloquear inovação — budget de Transform deve ter regras mais flexíveis que Run

---

## Estrutura / Modelo

### 1. Hierarquia de Budget

```
┌──────────────────────────────────────────────┐
│           BUDGET TOTAL DA EMPRESA             │
│              (Aprovado pelo Board)            │
├──────────────────────────────────────────────┤
│                                               │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐   │
│  │ Run      │  │ Grow     │  │Transform │   │
│  │ Budget   │  │ Budget   │  │ Budget   │   │
│  │ (fixo)   │  │(flexível)│  │(milestone│   │
│  │          │  │          │  │ based)   │   │
│  └────┬─────┘  └────┬─────┘  └────┬─────┘   │
│       │              │              │         │
│  ┌────┴─────────────┴──────────────┴────┐    │
│  │     BUDGET POR ÁREA / SQUAD           │    │
│  │  Engineering | Marketing | Sales |    │    │
│  │  Product | G&A | Data | People        │    │
│  └────┬─────────────┬──────────────┬────┘    │
│       │              │              │         │
│  ┌────┴─────────────┴──────────────┴────┐    │
│  │     BUDGET POR INICIATIVA / PROJETO   │    │
│  │  OKR-linked | DRI-owned | Time-bound  │    │
│  └──────────────────────────────────────┘    │
└──────────────────────────────────────────────┘
```

### 2. Allocation Rules

**Regra 1: Proporção por Categoria**
```
Run the Business:       [X]% do budget total
Grow the Business:      [Y]% do budget total
Transform the Business: [Z]% do budget total

Exemplo scale-up: 35% Run / 50% Grow / 15% Transform
```

**Regra 2: Budget por Tipo de Custo**
```
Headcount (fully-loaded):    60-70% do budget total (típico em tech)
Ferramentas e Infra:         10-15%
Marketing e Vendas:          10-20%
G&A (admin, legal, office):  5-10%
Contingência:                3-5%
```

**Regra 3: Authority Matrix**

| Valor | Quem Aprova | Processo |
|-------|------------|----------|
| < R$ 5K | Gestor direto | Aprovação simples |
| R$ 5K - R$ 25K | Diretor da área | Budget request simplificado |
| R$ 25K - R$ 100K | CFO + Diretor | Budget request completo |
| R$ 100K - R$ 500K | CFO + CEO | Business case + apresentação |
| > R$ 500K | Board | Business case + board approval |

**Regra 4: Uso do Contingency Budget**
```
Contingência = 3-5% do budget total
Uso permitido:
  - Oportunidades não previstas com ROI comprovável
  - Custos emergenciais genuínos (não má gestão)
  - Projetos aprovados acima do orçado (com justificativa)
Uso não permitido:
  - Cobrir overspend de área que não geriu bem o budget
  - Projetos que não passaram pelo gate de aprovação
  - "Buffer" para não ter que priorizar
```

### 3. Variance Tracking

**Framework de Classificação de Variações:**

| Tipo de Variação | Descrição | Ação |
|-----------------|-----------|------|
| **Timing** | Gasto previsto para Mês X ocorreu no Mês Y | Monitorar, ajustar forecast mensal |
| **Volume** | Mais/menos unidades que o planejado | Analisar causa, ajustar projeção |
| **Preço** | Custo unitário diferente do planejado | Renegociar ou ajustar budget |
| **Mix** | Composição diferente do planejado | Avaliar impacto em margem |
| **Escopo** | Novo gasto não previsto no budget original | Aprovação incremental necessária |
| **Eficiência** | Mesmo output com mais/menos custo | Documentar e aplicar learning |

**Thresholds de Ação:**
```
Variação < 5%:     Monitorar. Sem ação obrigatória.
Variação 5-10%:    Documentar causa raiz. Owner explica.
Variação 10-20%:   Plano de ação obrigatório. Reforecast.
Variação > 20%:    Escalação para CFO/CEO. Ação corretiva imediata.
```

### 4. Reforecasting

```
Cadência de Reforecast:
  - Mensal: Atualizar actuals, ajustar forecast dos meses restantes
  - Trimestral (QBR): Reforecast completo com revisão de premissas
  - Ad-hoc: Quando evento material muda premissas fundamentais

Regras:
  1. Reforecast é baseado em dados reais + premissas atualizadas
  2. Nunca ajustar budget original (preserve para comparação)
  3. Manter versionamento: Forecast v1 (original), v2 (Q1 update), etc.
  4. Comunicar mudanças materiais ao board proativamente
```

### 5. Accountability Framework

```
┌─────────────────────────────────────────────────┐
│  CADA LINHA DE BUDGET TEM:                       │
│                                                  │
│  → DRI (Dono): Quem é responsável pelo gasto    │
│  → Propósito: Para que serve este gasto         │
│  → Métrica: Como medimos sucesso deste gasto    │
│  → Gate: Qual checklist valida a qualidade      │
│  → Review: Quando será revisado                 │
│  → Kill Criteria: Quando parar de gastar        │
└─────────────────────────────────────────────────┘
```

---

## Processo de Aplicação

### Fase 1: Construção do Budget (Annual Planning — 4-6 semanas)

1. **Semana 1-2: Top-Down Envelope**
   - Board/CEO define revenue target e investment thesis
   - CFO calcula envelope total disponível (receita projetada - margem target = OPEX budget)
   - Definir split Run/Grow/Transform

2. **Semana 2-4: Bottom-Up Requests**
   - Cada líder de área submete budget request detalhado
   - Requests devem ser linkados a OKRs e iniciativas aprovadas
   - CFO consolida: total pedido vs. envelope disponível (gap típico: 1.5-2x)

3. **Semana 4-5: Negociação e Priorização**
   - CFO + CEO revisam cada request contra critérios de priorização
   - Aplicar capital allocation framework para decisões de trade-off
   - Comunicar decisões com justificativa para cada área

4. **Semana 5-6: Aprovação e Comunicação**
   - Budget final aprovado pelo board
   - Comunicar para toda a empresa: prioridades, investimentos, trade-offs
   - Cada DRI assina seu budget commitment

### Fase 2: Acompanhamento Mensal (MBR Financeiro)

1. Fechar o mês contábil (até D+5 do mês seguinte)
2. Consolidar actuals vs. budget por área e por categoria
3. Identificar variações > threshold
4. Cada DRI com variação > 10% prepara explicação e plano
5. CFO apresenta consolidado no MBR
6. Decisões de reallocation documentadas no decision registry

### Fase 3: Reforecast Trimestral (QBR Financeiro)

1. Avaliar performance acumulada do ano vs. budget
2. Revisar premissas: o que mudou? (mercado, produto, equipe)
3. Construir novo forecast para meses restantes
4. Identificar riscos e oportunidades de budget
5. Propor reallocations baseadas em performance
6. Apresentar ao board com cenários (base/bear/bull)

### Fase 4: Fechamento Anual

1. Consolidar actuals do ano completo vs. budget
2. Análise de variação profunda por área
3. Identificar top learnings: onde acertamos? onde erramos?
4. Alimentar RalphLoop com insights para melhorar o processo
5. Aplicar learnings na construção do budget do próximo ano

---

## Exemplos Práticos

### Exemplo 1: Variance Report Mensal

```
VARIANCE REPORT — MARÇO 2026

| Área        | Budget  | Actual  | Var (R$)  | Var (%) | Status | Ação        |
|-------------|---------|---------|-----------|---------|--------|-------------|
| Engineering | R$ 420K | R$ 415K | -R$ 5K    | -1.2%   | ✅     | OK          |
| Marketing   | R$ 180K | R$ 210K | +R$ 30K   | +16.7%  | 🔴     | Plano req.  |
| Sales       | R$ 150K | R$ 155K | +R$ 5K    | +3.3%   | ✅     | OK          |
| Product     | R$ 100K | R$ 95K  | -R$ 5K    | -5.0%   | 🟡     | Monitorar   |
| G&A         | R$ 80K  | R$ 75K  | -R$ 5K    | -6.3%   | 🟡     | Monitorar   |
| TOTAL       | R$ 930K | R$ 950K | +R$ 20K   | +2.2%   | 🟡     | Investigar  |

DETALHE — Marketing (+16.7%):
  Causa: Campanha de lançamento de produto acelerada (prevista para abril)
  Tipo: Timing (gasto antecipado) + Volume (30% mais leads que projetado)
  Impacto anual: Neutro se abril vier abaixo do budget proporcionalmente
  Ação: Monitorar abril. Se persistir, reforecast + reallocation.
  DRI: CMO | Deadline: 10/Abr/2026
```

### Exemplo 2: Reallocation Decision

```
QBR Q1/2026 — Proposta de Reallocation

De: Marketing Brand (R$ 120K no Q2)
  Motivo: Campanha de brand awareness não gerou impacto mensurável em pipeline
  Evidência: Zero correlação entre gasto em brand e MQLs nos últimos 3 meses
  Kill criteria atingido: < 5% de contribuição para pipeline após 2 trimestres

Para: Marketing Performance (R$ 80K) + Product-Led Growth (R$ 40K)
  Motivo: CAC paid caiu 15% no Q1 → ROI comprovado
  PLG: Onboarding self-serve pode reduzir CAC orgânico em 20%
  Expected ROI: 45 leads adicionais/mês → R$ 270K pipeline incremental

Aprovação: CFO + CMO + CEO
Status: Aprovado em 08/Abr/2026
Registro: decision-registry.yaml #DEC-2026-042
```

---

## Armadilhas Comuns

1. **Budget como teto, não como investimento** — Mentalidade de "gastar o mínimo possível" ao invés de "investir para maximizar retorno." Budget é ferramenta de crescimento, não só de controle.

2. **Use it or lose it** — Áreas que gastam o budget todo para não perder no próximo ano. Criar incentivo para devolver budget não utilizado (realocar para pool de oportunidades).

3. **Governança como burocracia** — Processo de aprovação tão lento que oportunidades são perdidas. Fast-track para gastos urgentes com ROI claro.

4. **Budget desconectado de OKRs** — Dinheiro alocado para atividades que não conectam com resultados mensuráveis. Todo budget deve ter OKR ou iniciativa associada.

5. **Reforecast como desculpa** — Usar reforecast para "mover a trave" e esconder performance ruim. Preservar budget original para comparação honest.

6. **Falta de accountability** — Variações identificadas mas ninguém é responsabilizado ou age. Cada variação > 10% precisa de DRI, ação e deadline.

7. **Over-indexing em cost cutting** — Cortar custos que geram retorno (vendedores, infra crítica) porque "precisamos cortar 10% linear." Cortar baseado em ROI, não em percentual.

8. **Governança one-size-fits-all** — Aplicar as mesmas regras para Run (previsível), Grow (variável) e Transform (experimental). Flexibilidade deve aumentar com o risco.

---

## Integração com Outros Frameworks

- `frameworks/cfo-strategist/cfo-capital-allocation.md` — Capital allocation define as prioridades; governance executa
- `frameworks/cfo-strategist/financial-modeling.md` — O modelo financeiro gera o budget base
- `frameworks/cfo-strategist/cash-flow-management.md` — Budget governance controla as saídas de caixa
- `frameworks/cfo-strategist/unit-economics-engine.md` — Unit economics validam ROI das alocações
- `frameworks/cfo-strategist/cost-optimization.md` — Otimização de custos alimenta decisões de reallocation
- `frameworks/shared/decision-framework.md` — Budget decisions seguem o framework de decisão
- `checklists/finance/budget-allocation-quality.md` — Quality gate para alocações de budget
- `checklists/finance/budget-review.md` — Checklist de revisão periódica de budget
- `templates/finance/budget-allocation-matrix.md` — Template para documentar alocações
- `templates/finance/budget-request.md` — Template para pedidos de budget incremental

---

## Referências

- **Amazon** — OP1/OP2 annual planning process — Disciplina de budget linkado a narrativa
- **Google** — OKR-linked budgeting — Conectar budget com resultados mensuráveis
- **Lencioni, P.** — "The Advantage" — Accountability como vantagem competitiva
- **Horowitz, B.** — "The Hard Thing About Hard Things" — Budget em tempos difíceis
- **CFO.com** — "Zero-Based Budgeting in Practice" — Técnicas de ZBB para startups
- **McKinsey** — "Beyond Budgeting" — Evolução de governança orçamentária em empresas ágeis
