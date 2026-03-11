# Nova Iniciativa — Fase 05: Medição e Avaliação

## Objetivo desta Fase

Medir sistematicamente os resultados da iniciativa contra a hipótese original e as
métricas de sucesso definidas. Esta fase transforma dados brutos em insights acionáveis
que informam a decisão de escalar, pivotar ou descontinuar a iniciativa. O foco está
em validar ou invalidar os pressupostos da hipótese com dados reais de mercado e
operação, removendo a subjetividade do processo de avaliação.

## Agentes Envolvidos

- **CFO Agent**: Lidera a análise financeira e avalia o ROI efetivo vs projetado
- **CMO Agent**: Analisa métricas de mercado, aquisição e satisfação do cliente
- **CTO Agent**: Avalia métricas técnicas de performance, reliability e scalability
- **COO Agent**: Mede eficiência operacional e compara com SLAs definidos
- **CEO Agent**: Interpreta resultados no contexto estratégico amplo
- **CHRO Agent**: Avalia impacto organizacional e métricas de equipa
- **Chief of Staff Agent**: Consolida dashboards e prepara narrativa integrada

## Inputs Necessários

1. Hypothesis Document com métricas de validação (output da Fase 01)
2. Dados de produção acumulados desde o lançamento
3. Dados financeiros reais (revenue, custos, margin)
4. Métricas de produto/serviço (usage, engagement, retention, NPS)
5. Métricas técnicas (uptime, latency, error rates, scalability metrics)
6. Métricas operacionais (throughput, cycle time, quality metrics)
7. Feedback qualitativo de clientes e equipa interna

## Processo (step-by-step)

1. **Data collection setup**: Chief of Staff Agent garante que todas as fontes de dados
   estão a reportar corretamente e que o período de medição é suficiente para conclusões
   estatisticamente significativas
2. **Financial analysis**: CFO Agent calcula o ROI real, compara revenue e custos com
   as projeções do modelo financeiro e analisa unit economics
3. **Market metrics analysis**: CMO Agent analisa métricas de aquisição (CAC, conversion
   rates), retenção (churn, LTV) e satisfação (NPS, CSAT)
4. **Technical performance review**: CTO Agent avalia métricas de reliability (uptime,
   SLA compliance), performance (latency, throughput) e qualidade (bug rate, tech debt)
5. **Operational efficiency review**: COO Agent compara métricas operacionais reais com
   os SLAs e benchmarks definidos no design
6. **Hypothesis validation**: CEO Agent e Chief of Staff Agent comparam cada pressuposto
   da hipótese original com os dados reais, classificando como validado, parcialmente
   validado ou invalidado
7. **Root cause analysis**: Para métricas abaixo do esperado, os agentes relevantes
   conduzem análise de causa raiz para entender os desvios
8. **Insight synthesis**: Chief of Staff Agent consolida todas as análises num relatório
   integrado com insights chave e recomendações claras
9. **Decision preparation**: CEO Agent prepara a recomendação de próximos passos
   (escalar, pivotar, iterar ou descontinuar) com base nos dados

## Outputs / Entregáveis

- **Performance Dashboard**: Dashboard consolidado com todas as métricas chave
- **Financial Analysis Report**: Relatório financeiro detalhado com ROI e unit economics
- **Hypothesis Validation Report**: Status de cada pressuposto (validado/invalidado)
- **Root Cause Analysis**: Análise de causa raiz para desvios significativos
- **Customer Insights Report**: Compilação de feedback e insights de clientes
- **Recommendation Document**: Recomendação fundamentada de próximos passos
- **Lessons Learned (Draft)**: Rascunho de lições aprendidas para a fase de review

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-05.1 | Dados de pelo menos 30 dias de operação analisados | Chief of Staff |
| QG-05.2 | ROI calculado com metodologia consistente e auditável | CFO Agent |
| QG-05.3 | NPS ou CSAT medido com amostra estatisticamente significativa | CMO Agent |
| QG-05.4 | Technical metrics baseados em dados de monitoring, não estimativas | CTO Agent |
| QG-05.5 | Cada pressuposto da hipótese tem status de validação documentado | CEO Agent |
| QG-05.6 | Root cause analysis completa para todos os desvios >20% | COO Agent |

## Critérios para Avançar

Para progredir para a Fase 06 (Review), todos os critérios devem ser satisfeitos:

- [ ] Dashboard de métricas completo e validado por todos os agentes
- [ ] Relatório de validação da hipótese finalizado
- [ ] Root cause analysis concluída para todos os desvios significativos
- [ ] Recomendação de próximos passos documentada e fundamentada
- [ ] Dados financeiros reconciliados com a contabilidade oficial
- [ ] Draft de lições aprendidas preparado

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Dados insuficientes para conclusões robustas | Média | Alto | Definir período mínimo de medição antes de iniciar |
| Viés de confirmação na interpretação dos dados | Alta | Crítico | Análise independente por agente não envolvido na execução |
| Métricas vanity mascarando problemas reais | Média | Alto | Focar em métricas de outcome, não de output |
| Atribuição incorreta de causalidade | Média | Alto | Usar controles e comparações A/B quando possível |
| Pressão para declarar sucesso prematuramente | Alta | Crítico | Critérios de sucesso definidos previamente na Fase 01 |

## Templates a Usar

- `templates/performance-dashboard.md` — Template de dashboard de métricas
- `templates/hypothesis-validation.md` — Relatório de validação de hipótese
- `templates/root-cause-analysis.md` — Template de análise de causa raiz
- `templates/recommendation-memo.md` — Memorando de recomendação

## Duração Estimada

- **Mínimo**: 5 dias úteis (após período mínimo de coleta de dados)
- **Típico**: 10-15 dias úteis
- **Máximo**: 20 dias úteis (para iniciativas com métricas complexas)

> **Nota**: A medição honesta é o ato mais importante de uma organização que aprende.
> Nunca manipular ou cherry-pick dados para suportar uma narrativa pré-definida.
