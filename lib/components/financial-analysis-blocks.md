# Financial Analysis Blocks — Blocos Reutilizáveis para Análise Financeira

> Blocos padronizados para análises financeiras em documentos executivos.
> Use como componentes modulares em business cases, reports e apresentações.

---

## 1. Bloco: P&L Resumido

```markdown
### Demonstração de Resultados — [Período]

| Linha | Real | Budget | Var | YoY |
|-------|------|--------|-----|-----|
| **Receita Bruta** | R$ [X] | R$ [X] | [+/-X%] | [+/-X%] |
| (-) Deduções | (R$ [X]) | (R$ [X]) | | |
| **Receita Líquida** | R$ [X] | R$ [X] | [+/-X%] | [+/-X%] |
| (-) COGS | (R$ [X]) | (R$ [X]) | | |
| **Margem Bruta** | R$ [X] ([X%]) | R$ [X] ([X%]) | [+/-X pp] | |
| (-) OPEX | (R$ [X]) | (R$ [X]) | | |
| **EBITDA** | R$ [X] ([X%]) | R$ [X] ([X%]) | [+/-X pp] | |
| (-) D&A / Juros / IR | (R$ [X]) | (R$ [X]) | | |
| **Resultado Líquido** | R$ [X] | R$ [X] | [+/-X%] | |
```

---

## 2. Bloco: Unit Economics SaaS

```markdown
### Unit Economics — [Período]

| Métrica | Valor | Benchmark | Status |
|---------|-------|-----------|--------|
| **CAC** (Custo de Aquisição) | R$ [X] | [Referência do setor] | [Bom/Atenção/Ruim] |
| **LTV** (Lifetime Value) | R$ [X] | — | |
| **LTV/CAC** | [X.X]x | >3x ideal | [Status] |
| **Payback de CAC** | [X meses] | <12 meses ideal | [Status] |
| **ARPU** (Receita por usuário/mês) | R$ [X] | — | |
| **Gross Margin** | [X%] | >70% para SaaS | [Status] |
| **Net Revenue Retention** | [X%] | >110% ideal | [Status] |
| **Logo Churn** | [X%/mês] | <2% ideal | [Status] |
| **MRR Churn** | [X%/mês] | <1.5% ideal | [Status] |

**Narrativa:** [O que os unit economics dizem sobre a saúde do negócio]
```

---

## 3. Bloco: Cash Flow Simplificado

```markdown
### Fluxo de Caixa — [Período]

| Categoria | [Mês 1] | [Mês 2] | [Mês 3] | Total Q |
|-----------|---------|---------|---------|---------|
| **Saldo Inicial** | R$ [X] | R$ [X] | R$ [X] | R$ [X] |
| (+) Receitas recebidas | R$ [X] | R$ [X] | R$ [X] | R$ [X] |
| (+) Outros recebimentos | R$ [X] | R$ [X] | R$ [X] | R$ [X] |
| (-) Folha + encargos | (R$ [X]) | (R$ [X]) | (R$ [X]) | (R$ [X]) |
| (-) Fornecedores | (R$ [X]) | (R$ [X]) | (R$ [X]) | (R$ [X]) |
| (-) Infra/Cloud | (R$ [X]) | (R$ [X]) | (R$ [X]) | (R$ [X]) |
| (-) Marketing | (R$ [X]) | (R$ [X]) | (R$ [X]) | (R$ [X]) |
| (-) Outros | (R$ [X]) | (R$ [X]) | (R$ [X]) | (R$ [X]) |
| **Fluxo Líquido** | R$ [X] | R$ [X] | R$ [X] | R$ [X] |
| **Saldo Final** | R$ [X] | R$ [X] | R$ [X] | R$ [X] |

**Burn Rate Mensal:** R$ [X] | **Runway:** [N meses]
```

---

## 4. Bloco: Análise de Variação (Bridge)

```markdown
### Bridge de Receita — Budget vs Real [Período]

Budget: R$ [X]
(+) Clientes novos acima do plan: +R$ [X]
(+) Upsell acima do plan: +R$ [X]
(-) Churn acima do plan: -R$ [X]
(-) Delay em enterprise deals: -R$ [X]
(-) Desconto não planejado: -R$ [X]
= **Realizado: R$ [X]** (Variação: [+/-X%])

**Conclusão:** [O que explica a maior parte da variação]
```

---

## 5. Bloco: Análise de Cohort de Receita

```markdown
### Cohort de Receita Mensal (MRR por mês de aquisição)

| Cohort | Mês 0 | Mês 3 | Mês 6 | Mês 12 | Retenção 12m |
|--------|-------|-------|-------|--------|:------------:|
| [Jan/24] | R$ [X] | R$ [X] | R$ [X] | R$ [X] | [X%] |
| [Abr/24] | R$ [X] | R$ [X] | R$ [X] | R$ [X] | [X%] |
| [Jul/24] | R$ [X] | R$ [X] | R$ [X] | — | [Projeção] |
| [Out/24] | R$ [X] | R$ [X] | — | — | [Projeção] |

**Tendência:** [Cohorts melhorando/piorando — o que explica]
```

---

## 6. Bloco: Comparação de Cenários Financeiros

```markdown
### Cenários Financeiros — [Decisão/Contexto]

| Métrica | Conservador | Base | Otimista |
|---------|:----------:|:----:|:--------:|
| Premissa principal | [Premissa] | [Premissa] | [Premissa] |
| Receita (12m) | R$ [X] | R$ [X] | R$ [X] |
| Custo total | R$ [X] | R$ [X] | R$ [X] |
| EBITDA | R$ [X] | R$ [X] | R$ [X] |
| Runway | [N meses] | [N meses] | [N meses] |
| Headcount final | [N] | [N] | [N] |
| Probabilidade | [X%] | [X%] | [X%] |

**Recomendação:** Planejar para cenário [base] com contingência para [conservador].
```

---

## 7. Bloco: Métricas de Eficiência

```markdown
### Eficiência Operacional — [Período]

| Métrica | Valor | QoQ | Benchmark |
|---------|-------|-----|-----------|
| Receita por funcionário | R$ [X]/mês | [+/-X%] | [Referência] |
| ARR por funcionário | R$ [X] | [+/-X%] | [>R$ 200K para SaaS B2B] |
| Burn multiple | [X.X]x | [+/-X] | [<2x ideal] |
| Magic number | [X.X] | [+/-X] | [>0.75 ideal] |
| Rule of 40 | [X] | [+/-X] | [>40 ideal] |
| OPEX como % da receita | [X%] | [+/-X pp] | [Referência] |
```

---

## 8. Bloco: ROI Simplificado

```markdown
### ROI — [Nome do Investimento]

| | Valor |
|---|-------|
| **Investimento total** | R$ [X] |
| **Benefício anual** | R$ [X] |
| **ROI** | **[X%]** |
| **Payback** | **[X meses]** |
| **NPV (taxa X%)** | R$ [X] |

**Racional:** [1-2 frases explicando de onde vem o retorno]
```

---

## Exemplos de Uso

**Para Business Case:** Blocos 1 (P&L) + 6 (Cenários) + 8 (ROI)
**Para Board Deck:** Blocos 1 (P&L) + 2 (Unit Economics) + 3 (Cash Flow) + 4 (Bridge)
**Para Forecast:** Blocos 1 (P&L) + 3 (Cash Flow) + 5 (Cohort) + 6 (Cenários)
**Para Budget Request:** Blocos 8 (ROI) + 6 (Cenários)

---

## Dicas de Uso
- Sempre inclua variação (vs budget, QoQ, YoY) — números absolutos sem contexto não informam
- Use formatação consistente: negativos entre parênteses, percentuais com 1 casa decimal
- Narrative é obrigatória — tabela sem explicação gera mais perguntas que respostas
- Benchmarks dão contexto — "CAC de R$ 500" sozinho não diz nada, "vs benchmark de R$ 800" sim
- Arredonde para facilitar leitura — R$ 1.2M é melhor que R$ 1.234.567 em apresentações
