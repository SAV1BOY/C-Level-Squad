# Checklist de Qualidade de Previsão de Receita (Revenue Forecast Quality)

## Propósito
Garantir que toda previsão de receita apresentada ao C-Level Squad tenha premissas
documentadas, ranges definidos, e que a acuracidade histórica seja monitorada e
melhorada continuamente. Este checklist evita surpresas negativas de receita e
melhora a credibilidade do planejamento financeiro perante investidores e board.

## Quando Aplicar
- Na elaboração do forecast anual de receita
- Em cada atualização mensal do forecast (rolling forecast)
- Antes de apresentações ao board ou investidores com projeções de receita
- Quando desvios significativos (>10%) entre forecast e actual são identificados
- Ao avaliar impacto de mudanças de pricing, produto ou mercado na receita

## Agente Responsável
- **Primário:** Chief Financial Officer (CFO) ou Head of FP&A
- **Secundário:** Chief Revenue Officer (CRO) para pipeline e dados de vendas
- **Revisor:** CEO para validação de premissas estratégicas

## Checklist

### Seção 1 — Premissas Documentadas (Documented Assumptions)
- [ ] Item 1: Todas as premissas do forecast estão listadas explicitamente (não implícitas)
- [ ] Item 2: Premissas de crescimento orgânico estão fundamentadas em dados históricos
- [ ] Item 3: Premissas de novos clientes estão baseadas em pipeline real e conversion rates históricos
- [ ] Item 4: Premissas de expansion revenue estão baseadas em NRR histórico e pipeline de upsell
- [ ] Item 5: Premissas de churn estão baseadas em dados reais de cohort, não em targets aspiracionais
- [ ] Item 6: Sazonalidade está modelada com base em pelo menos 2 anos de dados históricos
- [ ] Item 7: Impacto de lançamentos de produtos novos está estimado conservadoramente
- [ ] Item 8: Premissas macroeconômicas relevantes estão consideradas (FX, inflação, setor)
- [ ] Item 9: Cada premissa tem um owner que é responsável por monitorar sua validade
- [ ] Item 10: Premissas foram revisadas por pelo menos 2 stakeholders antes da finalização

### Seção 2 — Ranges e Cenários (Ranges & Scenarios)
- [ ] Item 11: Forecast inclui no mínimo 3 cenários (bear, base, bull)
- [ ] Item 12: Cada cenário tem premissas explicitamente diferentes do cenário base
- [ ] Item 13: O range entre bear e bull é realista (nem muito amplo nem muito estreito)
- [ ] Item 14: A probabilidade atribuída a cada cenário está documentada
- [ ] Item 15: O cenário bear é genuinamente pessimista (não apenas "base menos 5%")
- [ ] Item 16: O cenário bull é aspiracional mas atingível (não fantasioso)
- [ ] Item 17: Sensitivity analysis das variáveis mais impactantes está disponível
- [ ] Item 18: O impacto de variáveis fora do controle da empresa está modelado
- [ ] Item 19: Os cenários são atualizados quando novas informações significativas surgem
- [ ] Item 20: O cenário comunicado ao board é o base-case, com ranges explícitos

### Seção 3 — Metodologia de Forecast
- [ ] Item 21: A metodologia de forecast está documentada (bottom-up, top-down, ou hybrid)
- [ ] Item 22: Se bottom-up, os dados de pipeline e capacity de vendas estão validados
- [ ] Item 23: Se top-down, os market sizing e assumptions de share estão justificados
- [ ] Item 24: O forecast reconcilia abordagem bottom-up com top-down (sanity check)
- [ ] Item 25: Modelos de forecast são testados retroativamente (backtesting)
- [ ] Item 26: A granularidade do forecast é adequada (por produto, segmento, geografia)
- [ ] Item 27: Revenue recognition rules (ASC 606 ou equivalente) estão aplicadas corretamente
- [ ] Item 28: Distinção entre bookings, billings e revenue está clara no forecast
- [ ] Item 29: O tratamento de receita recorrente vs. não-recorrente está correto

### Seção 4 — Acuracidade e Tracking (Accuracy & Tracking)
- [ ] Item 30: A acuracidade histórica do forecast é medida (forecast vs. actual)
- [ ] Item 31: A acuracidade é monitorada por período (mensal, trimestral, anual)
- [ ] Item 32: A acuracidade é monitorada por segmento e produto
- [ ] Item 33: Tendência de bias é rastreada (sistematicamente otimista ou pessimista)
- [ ] Item 34: O target de acuracidade está definido (ex: dentro de 5% do actual)
- [ ] Item 35: Root cause analysis é conduzida quando desvios excedem o threshold
- [ ] Item 36: Melhorias no modelo são implementadas com base nos aprendizados
- [ ] Item 37: A acuracidade do forecast é reportada ao board como indicador de maturidade

### Seção 5 — Integração com Pipeline de Vendas
- [ ] Item 38: O pipeline de vendas é input direto para o forecast bottom-up
- [ ] Item 39: Stage conversion rates estão atualizados e calibrados por segmento
- [ ] Item 40: O average deal size por segmento está validado com dados recentes
- [ ] Item 41: O sales cycle length por segmento está refletido no timing do forecast
- [ ] Item 42: Pipeline coverage ratio está calculado e monitored (target: >3x para quarter)
- [ ] Item 43: Deals no pipeline estão corretamente classificados por probabilidade
- [ ] Item 44: O CRO e o CFO estão alinhados sobre as premissas de pipeline

### Seção 6 — Comunicação e Governança
- [ ] Item 45: O forecast é comunicado internamente com ranges, não como número único
- [ ] Item 46: Mudanças no forecast são comunicadas proativamente (não apenas no fechamento)
- [ ] Item 47: O board recebe update de forecast com frequência mínima trimestral
- [ ] Item 48: A narrativa que acompanha o forecast explica os drivers e riscos
- [ ] Item 49: O forecast é input para decisões de hiring, investimento e budget

## Critérios de Aprovação
O forecast de receita é considerado adequado quando:

1. **100% das premissas estão documentadas (Seção 1)**
2. **Pelo menos 3 cenários estão modelados com premissas diferenciadas (Seção 2)**
3. **A metodologia está documentada e é replicável (Seção 3)**
4. **Acuracidade histórica está dentro de 10% do actual (Seção 4)**
5. **Pipeline coverage ratio está acima de 3x (Seção 5)**
6. **O CFO e o CRO assinaram conjuntamente o forecast**
7. **O CEO validou que o forecast é consistente com a estratégia**

## O que Fazer se Falhar
Se o forecast de receita não atinge os critérios:

1. **Premissas review:** Revisitar cada premissa e validar com dados atualizados
2. **Pipeline scrub:** CRO conduz revisão rigorosa do pipeline com o time de vendas
3. **Model calibration:** Ajustar modelo de forecast com dados mais recentes
4. **External validation:** Consultar analistas ou advisors para outside-in perspective
5. **Conservatism injection:** Se tendência é otimismo, aplicar haircut conservador
6. **Frequency increase:** Se acuracidade está baixa, aumentar frequência de atualização
7. **Accountability:** Garantir que CRO e squad leads são accountable pelas suas premissas
8. **Board communication:** Se o forecast está materialmente diferente do guidance, comunicar ao board

## Referências
- SaaS Forecasting Best Practices — SaaStr, OpenView
- ASC 606 — Revenue Recognition Standard
- Bessemer Venture Partners — Efficiency benchmarks para SaaS
- Framework interno de Revenue Forecasting (documento em /finance-capital/)
- Template de Forecast Model (documento em /templates/revenue-forecast.md)
- Dashboard de Revenue (link interno: /dashboards/revenue)
- Histórico de Forecast vs. Actual (documento em /finance-capital/forecast-accuracy.md)
