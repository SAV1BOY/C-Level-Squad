# Financial Analysis Blocks — Blocos Reutilizáveis para Análise Financeira

> Blocos padronizados para análises financeiras em documentos executivos.
> Use como componentes modulares em business cases, board decks, forecasts e reports.

---

## 1. Bloco: P&L Resumido

### Template
```markdown
## Demonstração de Resultado (P&L)

| Linha | Período Anterior | Período Atual | Variação | % Receita |
|-------|-----------------|--------------|----------|-----------|
| Receita Bruta | [R$ X] | [R$ X] | [+/- X%] | 100% |
| (-) Deduções | [(R$ X)] | [(R$ X)] | [+/- X%] | [X%] |
| = Receita Líquida | [R$ X] | [R$ X] | [+/- X%] | [X%] |
| (-) COGS | [(R$ X)] | [(R$ X)] | [+/- X%] | [X%] |
| = Margem Bruta | [R$ X] | [R$ X] | [+/- X pp] | [X%] |
| (-) OPEX | [(R$ X)] | [(R$ X)] | [+/- X%] | [X%] |
| = EBITDA | [R$ X] | [R$ X] | [+/- X%] | [X%] |
| (-) D&A | [(R$ X)] | [(R$ X)] | [+/- X%] | [X%] |
| = EBIT | [R$ X] | [R$ X] | [+/- X%] | [X%] |
| (-) Juros e Impostos | [(R$ X)] | [(R$ X)] | [+/- X%] | [X%] |
| = Resultado Líquido | [R$ X] | [R$ X] | [+/- X%] | [X%] |
```

### Variante: P&L Simplificado para Board
```markdown
| Linha | Budget | Realizado | Var | Forecast FY |
|-------|--------|-----------|-----|------------|
| Receita | [R$ X] | [R$ X] | [X%] | [R$ X] |
| Margem Bruta | [X%] | [X%] | [X pp] | [X%] |
| OPEX | [(R$ X)] | [(R$ X)] | [X%] | [(R$ X)] |
| EBITDA | [R$ X] | [R$ X] | [X%] | [R$ X] |
```

---

## 2. Bloco: Unit Economics SaaS

### Template
```markdown
## Unit Economics

| Métrica | Valor | Benchmark | Status |
|---------|-------|-----------|--------|
| **CAC (Custo de Aquisição)** | R$ [X] | R$ [X] | [Saudável/Atenção] |
| **LTV (Lifetime Value)** | R$ [X] | R$ [X] | [Status] |
| **LTV/CAC** | [X.X]x | >3x | [Status] |
| **Payback CAC** | [X] meses | <12 meses | [Status] |
| **ARPU** | R$ [X]/mês | R$ [X] | [Status] |
| **Gross Margin** | [X%] | >70% | [Status] |
| **Net Revenue Retention** | [X%] | >110% | [Status] |
| **Logo Churn** | [X%]/mês | <2%/mês | [Status] |
| **Revenue Churn** | [X%]/mês | <1%/mês | [Status] |

### Cálculos
- CAC = (Sales + Marketing spend) / Novos clientes = R$ [X] / [N] = R$ [X]
- LTV = ARPU x Gross Margin / Churn Rate = R$ [X] x [X%] / [X%] = R$ [X]
- Payback = CAC / (ARPU x Gross Margin) = [X] meses
```

---

## 3. Bloco: Análise de Cash Flow

### Template
```markdown
## Fluxo de Caixa

| Mês | Entradas | Saídas | Fluxo Líquido | Saldo Acumulado |
|-----|---------|--------|-------------|----------------|
| [M1] | R$ [X] | (R$ [X]) | R$ [+/- X] | R$ [X] |
| [M2] | R$ [X] | (R$ [X]) | R$ [+/- X] | R$ [X] |
| [M3] | R$ [X] | (R$ [X]) | R$ [+/- X] | R$ [X] |

**Burn rate médio:** R$ [X]/mês
**Runway:** [X] meses (caixa atual / burn rate)
**Meses até breakeven:** [X] meses
```

### Variante: Cash Flow por Categoria
```markdown
| Categoria | M1 | M2 | M3 | Total Q |
|-----------|-----|-----|-----|---------|
| **Entradas** | | | | |
| Receita recorrente | R$ [X] | R$ [X] | R$ [X] | R$ [X] |
| Receita não-recorrente | R$ [X] | R$ [X] | R$ [X] | R$ [X] |
| **Saídas** | | | | |
| Folha de pagamento | (R$ [X]) | (R$ [X]) | (R$ [X]) | (R$ [X]) |
| Infraestrutura | (R$ [X]) | (R$ [X]) | (R$ [X]) | (R$ [X]) |
| Marketing | (R$ [X]) | (R$ [X]) | (R$ [X]) | (R$ [X]) |
| G&A | (R$ [X]) | (R$ [X]) | (R$ [X]) | (R$ [X]) |
| **Fluxo Líquido** | **R$ [X]** | **R$ [X]** | **R$ [X]** | **R$ [X]** |
```

---

## 4. Bloco: ROI Simplificado

### Template
```markdown
## Análise de ROI

**Investimento:** R$ [X]
**Benefício anual:** R$ [X]
**ROI:** [((Benefício - Investimento) / Investimento) x 100]%
**Payback:** [Investimento / Benefício mensal] meses

| Cenário | Investimento | Benefício (12m) | ROI | Payback |
|---------|-------------|----------------|-----|---------|
| Otimista | R$ [X] | R$ [X] | [X%] | [X]m |
| Base | R$ [X] | R$ [X] | [X%] | [X]m |
| Pessimista | R$ [X] | R$ [X] | [X%] | [X]m |
```

---

## 5. Bloco: Budget vs Realizado

### Template
```markdown
## Budget vs Realizado

| Área | Budget | Realizado | Variação | Comentário |
|------|--------|-----------|----------|------------|
| [Área 1] | R$ [X] | R$ [X] | [+/- X%] | [Motivo da variação] |
| [Área 2] | R$ [X] | R$ [X] | [+/- X%] | [Motivo] |
| [Área 3] | R$ [X] | R$ [X] | [+/- X%] | [Motivo] |
| **Total** | **R$ [X]** | **R$ [X]** | **[+/- X%]** | |

**Variações > 10% requerem explicação detalhada.**
```

---

## 6. Bloco: Análise de Cenários

### Template
```markdown
## Cenários Financeiros

| Variável | Pessimista | Base | Otimista |
|----------|-----------|------|----------|
| Crescimento de receita | [X%] | [X%] | [X%] |
| Churn rate | [X%] | [X%] | [X%] |
| CAC | R$ [X] | R$ [X] | R$ [X] |
| **Resultado** | | | |
| Receita FY | R$ [X] | R$ [X] | R$ [X] |
| EBITDA | R$ [X] | R$ [X] | R$ [X] |
| Caixa final | R$ [X] | R$ [X] | R$ [X] |
| Runway | [X] meses | [X] meses | [X] meses |
```

---

## 7. Bloco: Waterfall de Receita

### Template
```markdown
## Waterfall de Receita MRR

| Componente | Valor | % do MRR Inicial |
|-----------|-------|-----------------|
| MRR Início do Período | R$ [X] | 100% |
| (+) New MRR | +R$ [X] | +[X%] |
| (+) Expansion MRR | +R$ [X] | +[X%] |
| (-) Churn MRR | -R$ [X] | -[X%] |
| (-) Contraction MRR | -R$ [X] | -[X%] |
| = **MRR Final do Período** | **R$ [X]** | **[X%]** |
| = **Net New MRR** | **R$ [X]** | **[X%]** |
```

---

## 8. Bloco: Headcount e Custo por Área

### Template
```markdown
## Custo de Headcount

| Área | HC | Salário Médio | Encargos | Custo Total Mensal | % do OPEX |
|------|:--:|-------------|---------|-------------------|-----------|
| Engineering | [N] | R$ [X] | R$ [X] | R$ [X] | [X%] |
| Sales | [N] | R$ [X] | R$ [X] | R$ [X] | [X%] |
| Marketing | [N] | R$ [X] | R$ [X] | R$ [X] | [X%] |
| CS | [N] | R$ [X] | R$ [X] | R$ [X] | [X%] |
| G&A | [N] | R$ [X] | R$ [X] | R$ [X] | [X%] |
| **Total** | **[N]** | | | **R$ [X]** | **100%** |

**Custo per capita médio:** R$ [X]/mês
**Receita per capita:** R$ [X]/mês
**Eficiência (receita/headcount):** [Valor comparado com benchmark]
```

---

## Exemplos de Uso Combinado

### Análise Financeira para Business Case
```markdown
## Análise Financeira

**Investimento:** R$ 450K (3 engenheiros x 6 meses + R$ 50K infra)
**Benefício:** R$ 1.2M/ano em redução de churn (de 3% para 2% MRR churn)
**ROI:** 167% | **Payback:** 5 meses

| Cenário | Redução de Churn | Receita Retida | ROI |
|---------|-----------------|---------------|-----|
| Pessimista | 0.5 pp | R$ 600K | 33% |
| Base | 1.0 pp | R$ 1.2M | 167% |
| Otimista | 1.5 pp | R$ 1.8M | 300% |
```

---

## Dicas de Uso
- Sempre compare com benchmark ou período anterior — números absolutos sem referência são inúteis
- Use % da receita para OPEX — facilita comparação entre períodos de tamanhos diferentes
- Destaque variações > 10% — são as que importam para decisão
- Inclua cenários — ninguém acredita em previsão de número único
- Mostre tendência (subindo/estável/caindo) além do snapshot — dá contexto direcional
- Para board, simplifique — para finance, detalhe
