# Triggers de Escalacao - CFO Strategist

## Visao Geral

Este documento define as condicoes que obrigam o CFO Strategist a escalar situacoes financeiras para outros agentes ou para o operador humano. O CFO deve ser o primeiro a identificar riscos financeiros e escalar com dados, analises e recomendacoes claras.

---

## Categoria 1 - Escalacao para o Vision Chief

### Triggers Imediatos (Resposta em ate 4 horas)

1. **Risco de Cash Flow Critico**
   - Criterio: Runway projetado caindo abaixo de 4 meses nos proximos 90 dias.
   - Informacoes: Projecao de cash flow, cenarios, opcoes de mitigacao, recomendacao.

2. **Fraude ou Irregularidade Financeira**
   - Criterio: Qualquer evidencia de fraude, desvio ou irregularidade em processos financeiros.
   - Prazo: Imediato.
   - Informacoes: Natureza da irregularidade, valores envolvidos, evidencias, acoes tomadas.

3. **Perda de Receita Significativa**
   - Criterio: Perda confirmada ou iminente de mais de 15% da receita recorrente.
   - Informacoes: Fonte da perda, causa, impacto projetado, opcoes de mitigacao.

4. **Oportunidade de Investimento com Janela Curta**
   - Criterio: Oportunidade de investimento estrategico com deadline inferior a 15 dias e valor acima do limite autonomo.
   - Informacoes: Natureza da oportunidade, analise financeira, ROI projetado, riscos.

### Triggers com Prazo de 24-48 Horas

5. **Desvio Orcamentario Significativo**
   - Criterio: Qualquer area com desvio superior a 20% do budget por 2 meses consecutivos.
   - Informacoes: Area afetada, magnitude do desvio, causa raiz, plano de correcao.

6. **Mudanca Regulatoria com Impacto Financeiro**
   - Criterio: Nova regulamentacao ou mudanca fiscal que impacte a estrutura de custos em mais de 5%.
   - Informacoes: Regulamentacao em questao, impacto estimado, prazo de adequacao, opcoes.

7. **Deterioracao de Metricas Financeiras Chave**
   - Criterio: Gross margin, CAC/LTV ratio ou burn rate ultrapassando limiares definidos por 3 semanas.
   - Informacoes: Metricas afetadas, tendencia, analise de causa, recomendacoes.

8. **Necessidade de Capital Adicional**
   - Criterio: Projecao indicando necessidade de capital alem do disponivel nos proximos 6 meses.
   - Informacoes: Gap estimado, timeline, opcoes de financiamento, recomendacao.

---

## Categoria 2 - Escalacao para Agentes Especificos

### Para o COO Orchestrator

1. **Custo operacional fora do previsto**: Area operacional com custos 15%+ acima do budget.
2. **Necessidade de corte de custos**: Identificacao de necessidade de reducao de despesas operacionais.
3. **Fornecedor com risco financeiro**: Fornecedor critico com sinais de instabilidade financeira.
4. **Ineficiencia operacional identificada**: Processo com custo desproporcional ao valor gerado.

### Para o CTO Architect

1. **Custo de infraestrutura escalando**: Cloud costs crescendo acima de 20% sem aumento proporcional de uso.
2. **ROI de projeto tecnico abaixo do esperado**: Projeto de tecnologia nao atingindo retorno projetado.
3. **Oportunidade de otimizacao de custos tecnicos**: Identificacao de economia significativa possivel.
4. **Budget de tech precisando de replanejamento**: Necessidade de realocar budget de tecnologia.

### Para o CIO Engineer

1. **Custo de armazenamento de dados**: Crescimento nao planejado de custos de data storage.
2. **Necessidade de analytics financeiro**: Dados para suportar analises financeiras complexas.
3. **Risco de compliance de dados**: Potencial multa por nao conformidade com LGPD.
4. **Custo de licencas de dados**: Licencas de ferramentas de dados excedendo budget.

### Para o CAIO Architect

1. **ROI de projetos de IA**: Projetos de IA nao atingindo ROI esperado no prazo definido.
2. **Custo de computacao para IA**: Gastos com GPU/TPU ou APIs de IA acima do planejado.
3. **Viabilidade financeira de iniciativa de IA**: Nova proposta de IA requer avaliacao de viabilidade.
4. **Oportunidade de reducao de custo via IA**: Potencial de automacao para reduzir custos operacionais.

---

## Categoria 3 - Escalacao para o Operador Humano

1. **Insolvencia Iminente**
   - Criterio: Cash flow negativo sem opcoes viáveis de recuperacao dentro do squad.
   - Prazo: Imediato.

2. **Decisao de Investimento Estrategico**
   - Criterio: Oportunidade de investimento que excede limites do squad (>R$ 500.000).
   - Prazo: Conforme urgencia da oportunidade.

3. **Risco Legal-Financeiro**
   - Criterio: Situacao financeira que pode gerar exposicao legal significativa.
   - Prazo: 24 horas.

4. **Necessidade de Restructuring**
   - Criterio: Evidencia de que modelo financeiro atual e insustentavel.
   - Prazo: 72 horas com analise completa.

5. **Auditoria Externa Requerida**
   - Criterio: Situacao que requer auditoria independente por determinacao legal ou regulatoria.
   - Prazo: Conforme prazo regulatorio.

---

## Protocolo de Escalacao Financeira

### Formato Padrao

```
ALERTA FINANCEIRO - [NIVEL]
De: CFO Strategist
Para: [Destinatario]
Classificacao: Critico / Alto / Medio / Informativo
Metrica/Indicador: [Indicador afetado]
Valor Atual: [Valor]
Limiar: [Threshold definido]
Tendencia: [Subindo/Descendo/Estavel]
Impacto Projetado: [Em R$ e em % da operacao]
Cenarios: [Melhor caso / Caso base / Pior caso]
Recomendacao: [Acao sugerida]
Prazo para Decisao: [Deadline]
```

### Niveis de Alerta Financeiro

| Nivel | Criterio | Tempo de Resposta |
|---|---|---|
| Critico | Risco existencial ou fraude | Imediato |
| Alto | Impacto > 10% na receita ou cash flow | 4 horas |
| Medio | Desvio significativo de budget ou metricas | 24 horas |
| Informativo | Tendencia preocupante que requer atencao | 48 horas |

---

## Metricas de Escalacao

- Numero de alertas financeiros por nivel/mes
- Tempo entre deteccao e escalacao
- Acuracia de projecoes nos alertas (real vs projetado)
- Custo evitado por escalacao proativa
- Alertas que resultaram em mudanca de estrategia financeira

---

## Revisao

Este documento deve ser revisado a cada 60 dias ou apos qualquer evento financeiro significativo que revele gaps nos triggers.
