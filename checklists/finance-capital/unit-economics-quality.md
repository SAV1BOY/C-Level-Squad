# Checklist de Qualidade de Unit Economics (Unit Economics Quality)

## Propósito
Garantir que as métricas de unit economics — CAC, LTV, payback period, margem e
cohort analysis — estejam corretamente calculadas, validadas e utilizadas para
tomada de decisão. Este checklist evita que decisões de investimento em growth
sejam baseadas em métricas distorcidas ou desatualizadas.

## Quando Aplicar
- Na revisão mensal de métricas de negócio (business review)
- Antes de decisões de escalar investimento em canais de aquisição
- Na preparação de materiais para investidores ou board
- Quando métricas de crescimento mostram tendência de deterioração
- Ao avaliar novas linhas de negócio ou segmentos de clientes

## Agente Responsável
- **Primário:** Chief Financial Officer (CFO) ou Head of FP&A
- **Secundário:** Head of Growth ou Marketing para dados de aquisição
- **Revisor:** CEO para validação de decisões baseadas em unit economics

## Checklist

### Seção 1 — CAC (Customer Acquisition Cost)
- [ ] Item 1: A definição de CAC está padronizada e documentada (quais custos estão incluídos)
- [ ] Item 2: CAC blended (todos os canais) está calculado e atualizado mensalmente
- [ ] Item 3: CAC por canal de aquisição está calculado separadamente
- [ ] Item 4: CAC por segmento de cliente está disponível (SMB, mid-market, enterprise)
- [ ] Item 5: Custos de vendas (sales salaries, commissions) estão incluídos no CAC
- [ ] Item 6: Custos de marketing (paid, organic, content) estão atribuídos corretamente
- [ ] Item 7: A tendência do CAC nos últimos 6 meses está mapeada (crescendo, estável, diminuindo)
- [ ] Item 8: CAC payback period está calculado por segmento
- [ ] Item 9: O custo de reativação de clientes inativos está separado do CAC de novos
- [ ] Item 10: CAC está benchmarked contra competidores e indústria

### Seção 2 — LTV (Lifetime Value)
- [ ] Item 11: A metodologia de cálculo de LTV está documentada (histórico vs. preditivo)
- [ ] Item 12: LTV está calculado por segmento de cliente
- [ ] Item 13: Churn rate utilizado no cálculo está atualizado e validado
- [ ] Item 14: Gross margin utilizada no LTV é a margem real, não a margem alvo
- [ ] Item 15: Expansion revenue (upsell, cross-sell) está incluído no LTV
- [ ] Item 16: A tendência do LTV nos últimos 6 meses está mapeada
- [ ] Item 17: O ratio LTV/CAC está acima de 3:1 (ou threshold definido pela empresa)
- [ ] Item 18: LTV é calculado com desconto (discounted) para refletir valor presente
- [ ] Item 19: O período usado para estimativa de lifetime está justificado com dados
- [ ] Item 20: Variações de LTV por cohort estão analisadas

### Seção 3 — Payback Period
- [ ] Item 21: Payback period blended está calculado e monitorado mensalmente
- [ ] Item 22: Payback por canal de aquisição está disponível
- [ ] Item 23: Payback por segmento de cliente está calculado
- [ ] Item 24: O payback está dentro do threshold aceitável (ex: <18 meses para SaaS B2B)
- [ ] Item 25: A tendência do payback nos últimos 6 meses está rastreada
- [ ] Item 26: O impacto de mudanças de pricing no payback foi modelado

### Seção 4 — Margem e Contribuição (Margin & Contribution)
- [ ] Item 27: Gross margin está calculada corretamente com COGS bem definido
- [ ] Item 28: Contribution margin por produto ou linha de negócio está disponível
- [ ] Item 29: Contribution margin por segmento de cliente está calculada
- [ ] Item 30: Custos variáveis vs. fixos estão corretamente classificados
- [ ] Item 31: A evolução de margem nos últimos 12 meses está documentada
- [ ] Item 32: O impacto de economias de escala está projetado para próximos 12 meses
- [ ] Item 33: Margem negativa em algum segmento está identificada e tem plano de correção
- [ ] Item 34: Operating leverage está calculado e tendência é positiva

### Seção 5 — Cohort Analysis
- [ ] Item 35: Cohort analysis de retenção é atualizada mensalmente
- [ ] Item 36: Cohorts estão segmentados por canal de aquisição
- [ ] Item 37: Cohorts estão segmentados por segmento de cliente
- [ ] Item 38: Cohorts estão segmentados por período de entrada (mês de aquisição)
- [ ] Item 39: Revenue retention por cohort está calculada (net dollar retention)
- [ ] Item 40: Logo retention por cohort está calculada separadamente
- [ ] Item 41: Comportamento de cohorts mais recentes vs. mais antigos é comparado
- [ ] Item 42: Cohorts com performance deteriorante estão sinalizados para investigação
- [ ] Item 43: O impacto de product changes em cohorts recentes está sendo rastreado
- [ ] Item 44: Cohort analysis é apresentada no business review mensal

### Seção 6 — Validação e Integridade dos Dados
- [ ] Item 45: As fontes de dados para cada métrica estão documentadas e são confiáveis
- [ ] Item 46: Reconciliação entre dados de marketing, vendas e finance é feita mensalmente
- [ ] Item 47: Definições de métricas são consistentes entre squads (single source of truth)
- [ ] Item 48: Anomalias nos dados são investigadas e explicadas (não ignoradas)
- [ ] Item 49: Um data owner é responsável pela integridade de cada métrica-chave

## Critérios de Aprovação
Unit economics são considerados saudáveis quando:

1. **LTV/CAC ratio está acima de 3:1 (ou threshold aprovado pelo board)**
2. **CAC payback period está dentro do threshold aceitável por segmento**
3. **Gross margin está acima do threshold mínimo definido pela empresa**
4. **Net dollar retention está acima de 100% (expansão supera churn)**
5. **Cohort analysis mostra melhora ou estabilidade nos últimos 3 cohorts**
6. **100% das métricas da Seção 6 (validação) estão atendidas**
7. **O CFO assinou a validação das métricas apresentadas**

## O que Fazer se Falhar
Se unit economics não atingem os critérios:

1. **Deep dive por segmento:** Identificar quais segmentos estão puxando métricas para baixo
2. **CAC optimization:** Se CAC está alto, revisar mix de canais e eficiência de funil
3. **Churn investigation:** Se LTV está baixo, priorizar análise de churn por cohort
4. **Pricing review:** Se margem está comprimida, reavaliar pricing e packaging
5. **Channel kill:** Desligar canais de aquisição com payback inaceitável
6. **Product intervention:** Se cohorts recentes deterioram, avaliar product-market fit
7. **Board transparency:** Comunicar ao board métricas reais sem sugar-coating
8. **Recovery plan:** Criar plano com milestones de melhoria e timeline

## Referências
- David Skok — "SaaS Metrics 2.0" (unit economics para SaaS)
- a16z — "16 Startup Metrics" (framework de métricas de startups)
- Bessemer Venture Partners — Cloud Index (benchmarks de SaaS)
- Framework interno de Business Metrics (documento em /finance-capital/)
- Template de Unit Economics Dashboard (documento em /templates/)
- Definições de métricas (documento em /finance-capital/metric-definitions.md)
