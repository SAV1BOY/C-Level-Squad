# Coleta Mensal de Métricas

> Processo estruturado para coleta, consolidação e análise de métricas-chave
> do negócio em cadência mensal.

## Objetivo

Garantir que a liderança tenha visibilidade completa e atualizada sobre a saúde
do negócio, identificando tendências, desvios e oportunidades antes que se tornem
crises ou oportunidades perdidas.

## Frequência e Timing

- **Cadência:** Mensal
- **Deadline de coleta:** Dia útil 5 de cada mês (dados do mês anterior)
- **Review com liderança:** Dia útil 7-8
- **Duração estimada:** 8-12 horas de trabalho distribuídas ao longo da primeira semana

## Responsáveis

| Papel | Responsabilidade |
|-------|-----------------|
| CFO/Head de FP&A | Métricas financeiras e consolidação final |
| VP Engineering | Métricas de produto e engenharia |
| VP Sales/Revenue | Métricas de receita e pipeline |
| VP Marketing | Métricas de aquisição e marca |
| VP People | Métricas de pessoas e cultura |
| Head de CS | Métricas de cliente e retenção |

## Métricas por Categoria

### Financeiras (CFO)
- [ ] Receita bruta e líquida (MRR/ARR se SaaS)
- [ ] Margem bruta e operacional
- [ ] Burn rate e runway (se startup)
- [ ] Cash position e cash flow
- [ ] Despesas por categoria vs budget
- [ ] CAC (Customer Acquisition Cost)
- [ ] LTV (Lifetime Value) e ratio LTV:CAC

### Produto e Engenharia (VP Eng)
- [ ] DAU/WAU/MAU e tendência
- [ ] Retenção de 7, 30, 90 dias
- [ ] Feature adoption rate
- [ ] Uptime e latência (p50, p95, p99)
- [ ] Velocity de entrega (story points ou throughput)
- [ ] Bug backlog e tempo médio de resolução
- [ ] Tech debt ratio

### Receita e Vendas (VP Sales)
- [ ] Pipeline total e por estágio
- [ ] Win rate e ciclo de vendas médio
- [ ] ACV (Average Contract Value)
- [ ] Churn e expansion revenue
- [ ] Net Revenue Retention (NRR)
- [ ] Quota attainment por rep

### Marketing e Aquisição (VP Marketing)
- [ ] Leads gerados por canal
- [ ] Conversion rate por estágio do funil
- [ ] CAC por canal
- [ ] Brand awareness metrics (se disponível)
- [ ] Content performance (tráfego, engagement)
- [ ] Share of voice vs competidores

### Pessoas (VP People)
- [ ] Headcount atual vs planejado
- [ ] Turnover voluntário e involuntário (rolling 12 meses)
- [ ] Time to hire por posição
- [ ] Employee NPS ou engagement score
- [ ] Diversidade do pipeline e do quadro
- [ ] Posições abertas e aging

### Cliente e Suporte (Head CS)
- [ ] NPS ou CSAT
- [ ] Tempo médio de resolução de tickets
- [ ] Volume de tickets e tendência
- [ ] Health score dos top 20 clientes
- [ ] Churn risk pipeline
- [ ] Expansão pipeline

## Processo de Coleta

### Dia 1-3: Coleta Individual
Cada responsável coleta suas métricas das fontes primárias:

- [ ] Extrair dados dos sistemas fonte (CRM, ERP, Analytics, HRIS)
- [ ] Validar dados contra período anterior (sanity check)
- [ ] Calcular métricas derivadas (ratios, tendências)
- [ ] Preparar comentários sobre desvios significativos (>10% vs meta ou vs mês anterior)
- [ ] Enviar para consolidação até dia útil 3

### Dia 3-5: Consolidação
Responsável pela consolidação (geralmente FP&A):

- [ ] Compilar todas as métricas em dashboard/deck padronizado
- [ ] Cross-check métricas que se relacionam (ex: CAC de marketing vs finanças)
- [ ] Identificar e destacar desvios significativos
- [ ] Preparar executive summary (1 página)
- [ ] Distribuir deck consolidado para review

### Dia 5-8: Review e Discussão
Reunião de liderança para revisar:

- [ ] Distribuir deck 24h antes da reunião
- [ ] Review de métricas vermelhas/amarelas primeiro
- [ ] Deep dive em 2-3 tópicos selecionados
- [ ] Definir action items com owner e deadline
- [ ] Documentar decisões tomadas

## Template de Executive Summary

```
MONTHLY METRICS SUMMARY - [MÊS/ANO]

SAÚDE GERAL: [VERDE/AMARELO/VERMELHO]

TOP 3 DESTAQUES POSITIVOS:
1. [Métrica] - [Resultado] vs [Meta] - [Comentário]
2.
3.

TOP 3 PREOCUPAÇÕES:
1. [Métrica] - [Resultado] vs [Meta] - [Ação planejada]
2.
3.

DECISÕES NECESSÁRIAS:
1. [Decisão] - [Contexto] - [Recomendação]
```

## Thresholds e Alertas

| Condição | Classificação | Ação |
|----------|--------------|------|
| Dentro de 5% da meta | Verde | Nenhuma ação especial |
| 5-15% abaixo da meta | Amarelo | Comentário obrigatório + plano |
| >15% abaixo da meta | Vermelho | Deep dive obrigatório + ação imediata |
| 3 meses consecutivos amarelo | Escalação | Requer revisão de meta ou estratégia |

## Ferramentas Recomendadas

### Coleta e Armazenamento
- Google Sheets/Excel para compilação manual
- Looker/Metabase/Power BI para dashboards automatizados
- Notion database para tracking histórico

### Distribuição
- Deck em PDF/Google Slides para a reunião
- Dashboard online para consulta ad-hoc
- Slack channel para highlights e alertas

## Melhoria Contínua

### Revisão Trimestral do Processo
- [ ] Todas as métricas ainda são relevantes?
- [ ] Alguma métrica nova precisa ser adicionada?
- [ ] Os thresholds estão calibrados corretamente?
- [ ] O processo de coleta pode ser mais automatizado?
- [ ] A reunião de review está sendo produtiva?

### Evolução de Maturidade
1. **Nível 1:** Coleta manual, deck estático, reunião reativa
2. **Nível 2:** Coleta semi-automatizada, dashboard, reunião com deep dives
3. **Nível 3:** Coleta automatizada, alertas proativos, decisões data-driven
4. **Nível 4:** AI-assisted análise, previsões, recomendações automatizadas
