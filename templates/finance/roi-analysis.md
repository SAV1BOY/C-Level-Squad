# Template: Análise de ROI (Return on Investment)

## Propósito
Este template estrutura a análise de retorno sobre investimento para projetos, ferramentas, contratações ou qualquer decisão que envolva alocação de capital. Fornece framework padronizado para comparar alternativas e justificar investimentos.

## Instruções de Uso
1. Defina claramente o investimento e o horizonte de análise
2. Quantifique TODOS os custos (diretos e indiretos)
3. Seja conservador nos benefícios — melhor surpreender positivamente
4. Apresente cenários para dar conforto ao tomador de decisão

---

## Informações da Análise

| Campo | Valor |
|-------|-------|
| **Projeto / Investimento** | [Nome] |
| **Analista** | [Nome — Cargo] |
| **Data** | [DD/MM/AAAA] |
| **Horizonte de Análise** | [12 / 24 / 36 meses] |
| **Taxa de Desconto** | [X% — WACC ou hurdle rate da empresa] |
| **Moeda** | [BRL / USD] |

---

## 1. Definição do Investimento

### 1.1 O que Estamos Avaliando
[Descrição clara do investimento — ex: "Migração do sistema de billing de solução proprietária para Stripe"]

### 1.2 Situação Atual (Baseline)
[Descrever custos e performance atuais que servem de base para comparação]
- **Custo atual mensal/anual:** [R$ X]
- **Performance atual:** [Métricas relevantes]
- **Dores atuais:** [Problemas quantificados]

---

## 2. Custos do Investimento

### 2.1 Custos Diretos

| Item | Tipo | Valor | Recorrência | Total (horizonte) |
|------|------|-------|------------|-------------------|
| [Licença/Software] | OPEX | [R$ X/mês] | Mensal | [R$ X] |
| [Desenvolvimento/Implementação] | CAPEX | [R$ X] | Único | [R$ X] |
| [Consultoria externa] | OPEX | [R$ X] | Único | [R$ X] |
| [Infraestrutura adicional] | OPEX | [R$ X/mês] | Mensal | [R$ X] |
| [Treinamento] | OPEX | [R$ X] | Único | [R$ X] |

### 2.2 Custos Indiretos

| Item | Estimativa | Cálculo |
|------|-----------|---------|
| Custo de oportunidade (time alocado) | [R$ X] | [N pessoas x X meses x salário médio] |
| Produtividade perdida durante transição | [R$ X] | [Estimativa de slow-down] |
| Risco de falha (custo esperado) | [R$ X] | [Probabilidade x Impacto] |

### 2.3 Custo Total do Investimento

| Categoria | Ano 1 | Ano 2 | Ano 3 | Total |
|-----------|-------|-------|-------|-------|
| Custos diretos | [R$ X] | [R$ X] | [R$ X] | [R$ X] |
| Custos indiretos | [R$ X] | [R$ X] | [R$ X] | [R$ X] |
| **Total** | **[R$ X]** | **[R$ X]** | **[R$ X]** | **[R$ X]** |

---

## 3. Benefícios Esperados

### 3.1 Benefícios Financeiros Diretos

| Benefício | Métrica | Valor Mensal | Valor Anual | Início |
|-----------|--------|-------------|-------------|--------|
| Aumento de receita | [Descrição] | [R$ X] | [R$ X] | [Mês X] |
| Redução de custo operacional | [Descrição] | [R$ X] | [R$ X] | [Mês X] |
| Redução de churn/perda | [Descrição] | [R$ X] | [R$ X] | [Mês X] |
| Aumento de eficiência | [Descrição] | [R$ X] | [R$ X] | [Mês X] |

### 3.2 Benefícios Financeiros Indiretos

| Benefício | Estimativa | Base de Cálculo |
|-----------|-----------|----------------|
| Redução de risco operacional | [R$ X/ano] | [Custo de incidentes evitados] |
| Aumento de produtividade | [R$ X/ano] | [Horas economizadas x custo/hora] |
| Aceleração de time-to-market | [R$ X] | [Receita capturada mais cedo] |

### 3.3 Benefícios Não-Financeiros
- [Benefício 1 — ex: "Melhoria na experiência do desenvolvedor"]
- [Benefício 2 — ex: "Conformidade regulatória"]
- [Benefício 3 — ex: "Redução de risco de segurança"]

### 3.4 Total de Benefícios

| Categoria | Ano 1 | Ano 2 | Ano 3 | Total |
|-----------|-------|-------|-------|-------|
| Benefícios diretos | [R$ X] | [R$ X] | [R$ X] | [R$ X] |
| Benefícios indiretos | [R$ X] | [R$ X] | [R$ X] | [R$ X] |
| **Total** | **[R$ X]** | **[R$ X]** | **[R$ X]** | **[R$ X]** |

---

## 4. Cálculos de ROI

### 4.1 ROI Simples
```
ROI = (Benefício Total - Custo Total) / Custo Total x 100

ROI = (R$ [benefício] - R$ [custo]) / R$ [custo] x 100 = [X%]
```

### 4.2 Payback Period
```
Payback = Investimento Inicial / Benefício Líquido Mensal

Payback = R$ [investimento] / R$ [benefício mensal] = [X meses]
```

### 4.3 Fluxo de Caixa e NPV

| Mês/Trimestre | Investimento | Benefício | Fluxo Líquido | Fluxo Acumulado |
|--------------|-------------|-----------|-------------|----------------|
| [Mês 0] | [(R$ X)] | [R$ 0] | [(R$ X)] | [(R$ X)] |
| [Mês 3] | [(R$ X)] | [R$ X] | [+/- R$ X] | [R$ X] |
| [Mês 6] | [(R$ X)] | [R$ X] | [+/- R$ X] | [R$ X] |
| [Mês 12] | [(R$ X)] | [R$ X] | [R$ X] | [R$ X] |
| [Mês 24] | [(R$ X)] | [R$ X] | [R$ X] | [R$ X] |
| [Mês 36] | [(R$ X)] | [R$ X] | [R$ X] | [R$ X] |

**NPV (taxa de [X%]):** R$ [valor]
**IRR:** [X%]

### 4.4 Resumo de Métricas

| Métrica | Valor | Benchmark da Empresa |
|---------|-------|---------------------|
| **ROI** | [X%] | [Mínimo aceitável: X%] |
| **Payback** | [X meses] | [Máximo aceitável: X meses] |
| **NPV** | [R$ X] | [Mínimo: > R$ 0] |
| **IRR** | [X%] | [Mínimo: > WACC de X%] |

---

## 5. Análise de Sensibilidade

### 5.1 Variáveis-Chave

| Variável | Cenário Base | Range Testado | Impacto no ROI |
|----------|-------------|--------------|---------------|
| [Variável 1 — ex: taxa de adoção] | [X%] | [Y% — Z%] | [ROI varia de A% a B%] |
| [Variável 2 — ex: custo de implementação] | [R$ X] | [R$ Y — R$ Z] | [ROI varia de A% a B%] |
| [Variável 3 — ex: timeline] | [X meses] | [Y — Z meses] | [ROI varia de A% a B%] |

### 5.2 Cenários

| Cenário | Premissa | Investimento | Benefício (3a) | ROI | Payback |
|---------|---------|-------------|---------------|-----|---------|
| Otimista | [O que muda] | [R$ X] | [R$ X] | [X%] | [X m] |
| Base | [Premissas padrão] | [R$ X] | [R$ X] | [X%] | [X m] |
| Pessimista | [O que muda] | [R$ X] | [R$ X] | [X%] | [X m] |
| Worst case | [Tudo dá errado] | [R$ X] | [R$ X] | [X%] | [X m] |

---

## 6. Premissas e Fontes

| Premissa | Valor | Fonte | Confiança |
|----------|-------|-------|-----------|
| [Premissa 1] | [Valor] | [Fonte] | [Alta/Média/Baixa] |
| [Premissa 2] | [Valor] | [Fonte] | [Alta/Média/Baixa] |
| [Premissa 3] | [Valor] | [Fonte] | [Alta/Média/Baixa] |

---

## 7. Recomendação

**Decisão recomendada:** [Investir / Não investir / Investir com gate review]

**Justificativa:**
[2-3 parágrafos sumarizando por que o investimento vale a pena (ou não)]

---

## Exemplo Preenchido (Resumo)

> **Investimento:** Migração para Stripe — R$ 420K (implementação) + R$ 15K/mês (licença)
> **Benefícios:** R$ 180K/ano em redução de falhas de cobrança + R$ 120K/ano em economia de DevOps
> **ROI (3 anos):** 185% | **Payback:** 16 meses | **NPV:** R$ 380K
> **Cenário pessimista:** ROI 68% — ainda positivo mesmo com metade dos benefícios

---

## Dicas de Uso
- ROI negativo não é necessariamente "não investir" — considere benefícios não-financeiros
- Sempre inclua cenário pessimista — se o ROI for positivo mesmo no worst case, decisão é fácil
- Custo de oportunidade do time é frequentemente o maior custo — não esqueça de incluir
- Compare com o retorno de investir o mesmo capital em alternativas
- Revise o ROI realizado 12 meses após implementação — aprenda com a precisão
- NPV > 0 é condição necessária mas não suficiente — considere risco e liquidez
