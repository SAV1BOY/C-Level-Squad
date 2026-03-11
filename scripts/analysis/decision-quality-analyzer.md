# Decision Quality Analyzer

> Script para análise da qualidade das decisões tomadas pelo C-Level Squad.

---

## Objetivo

Avaliar retrospectivamente a qualidade das decisões tomadas, analisando o
processo decisório, a evidência utilizada e os resultados obtidos. O objectivo
não é julgar decisões individuais, mas melhorar o sistema decisório como um todo.

---

## Framework de Análise

### Dimensão 1 — Process Quality (Qualidade do Processo)

Avalia se o processo decisório seguiu boas práticas:

| Critério | Peso | Escala |
|----------|------|--------|
| Problema claramente definido | 15% | 1-5 |
| Alternativas suficientes consideradas | 15% | 1-5 |
| Stakeholders relevantes consultados | 10% | 1-5 |
| Timeframe adequado para deliberação | 10% | 1-5 |
| Vieses cognitivos mitigados | 15% | 1-5 |
| Critérios de decisão explícitos | 10% | 1-5 |
| Riscos identificados e aceites | 15% | 1-5 |
| Reversibilidade avaliada | 10% | 1-5 |

#### Checklist de Vieses Cognitivos
- [ ] Confirmation bias: procurou-se evidência contrária?
- [ ] Anchoring: a primeira opção dominou indevidamente?
- [ ] Sunk cost: custos passados influenciaram a decisão?
- [ ] Groupthink: houve espaço para dissent?
- [ ] Availability bias: dados recentes dominaram sobre dados completos?
- [ ] Overconfidence: intervalo de confiança foi testado?

### Dimensão 2 — Evidence Quality (Qualidade da Evidência)

Avalia a base informacional da decisão:

| Critério | Peso | Escala |
|----------|------|--------|
| Dados quantitativos utilizados | 20% | 1-5 |
| Dados qualitativos considerados | 15% | 1-5 |
| Fontes diversificadas | 15% | 1-5 |
| Dados actualizados (freshness) | 15% | 1-5 |
| Análise de cenários realizada | 20% | 1-5 |
| Pressupostos explicitados | 15% | 1-5 |

#### Hierarquia de Evidência
```
Nível 5: Dados experimentais (A/B test, piloto)
Nível 4: Dados históricos internos + benchmarks externos
Nível 3: Análise quantitativa de dados disponíveis
Nível 2: Expert opinion + case studies
Nível 1: Intuição / experiência sem dados de suporte
```

### Dimensão 3 — Outcome Tracking (Acompanhamento de Resultados)

Avalia os resultados da decisão após implementação:

| Critério | Peso | Escala |
|----------|------|--------|
| Resultado vs expectativa | 25% | 1-5 |
| Timeline de implementação | 15% | 1-5 |
| Efeitos secundários (positivos) | 15% | 1-5 |
| Efeitos secundários (negativos) | 15% | 1-5 |
| Custo real vs estimado | 15% | 1-5 |
| Satisfação dos stakeholders | 15% | 1-5 |

---

## Scoring

### Cálculo do Decision Quality Score (DQS)
```
Process Score = soma_ponderada(critérios_processo)  → 0-100
Evidence Score = soma_ponderada(critérios_evidência) → 0-100
Outcome Score = soma_ponderada(critérios_resultado)  → 0-100

DQS = Process(40%) + Evidence(30%) + Outcome(30%)
```

### Nota Importante sobre Process vs Outcome
Uma decisão pode ter:
- **Bom processo + bom resultado** = Decisão de qualidade confirmada
- **Bom processo + mau resultado** = Azar / circunstâncias — processo OK
- **Mau processo + bom resultado** = Sorte — processo precisa melhoria
- **Mau processo + mau resultado** = Falha sistémica — acção urgente

O foco é sempre melhorar o PROCESSO, não apenas celebrar resultados.

---

## Classificação
| DQS | Classificação | Implicação |
|-----|--------------|------------|
| 85-100 | Exemplar | Usar como referência |
| 70-84 | Sólida | Boas práticas seguidas |
| 55-69 | Adequada | Espaço para melhoria |
| 40-54 | Fraca | Revisão de processo necessária |
| 0-39 | Deficiente | Intervenção urgente |

---

## Processo de Análise

### Passo 1 — Selecção de Decisões
- Todas as decisões com impacto alto (severity ≥ 12) são analisadas
- Sample aleatório de 20% das decisões médias
- Qualquer decisão pode ser nominada para análise
- Análise obrigatória para decisões com outcome negativo

### Passo 2 — Recolha de Dados
- Extrair registo do decision log
- Entrevistar decision maker e stakeholders-chave (5-10min)
- Recolher dados de outcome dos sistemas relevantes
- Compilar timeline da decisão

### Passo 3 — Avaliação
- Aplicar scoring framework a cada dimensão
- Identificar pontos fortes e fracos específicos
- Documentar vieses detectados
- Registar lições aprendidas

### Passo 4 — Aggregação
- Calcular scores médios por período, squad e tipo
- Identificar padrões e tendências
- Comparar com períodos anteriores
- Gerar recomendações sistémicas

---

## Reporting

### Decision Quality Dashboard
- DQS médio por período (trend line)
- Distribuição de scores (histogram)
- Breakdown por dimensão (radar chart)
- Padrões de vieses mais frequentes
- Correlação entre process quality e outcomes

### Quarterly Decision Quality Report
```markdown
# Decision Quality Report — [Trimestre]

## Resumo
- Decisões analisadas: [N]
- DQS médio: [score]
- Tendência vs trimestre anterior: [melhoria/declínio]

## Padrões Identificados
- [Padrão 1 com evidência]
- [Padrão 2 com evidência]

## Top Decisions (exemplares)
- [DEC-ID]: [título] — DQS [score] — [porquê exemplar]

## Áreas de Melhoria
- [Área 1]: [recomendação específica]
- [Área 2]: [recomendação específica]

## Acções Propostas
- [Acção 1 com owner e prazo]
- [Acção 2 com owner e prazo]
```

---

## Integração

- **Decision Log**: fonte primária de dados para análise
- **Meeting Effectiveness**: decisões são output de reuniões
- **Forecast Accuracy**: previsões são tipo de decisão
- **Quarterly Review**: DQS é input para review trimestral
- **Training**: resultados informam necessidades de formação

---

## Notas Técnicas

- Análises armazenadas em `data/decision-quality/`
- Scoring pode ser parcialmente automatizado para dimensões quantitativas
- Análise de vieses requer avaliação humana
- Confidencialidade: análises individuais são partilhadas apenas com decision maker e squad lead
- Dados agregados são públicos dentro do C-Level Squad
