# Checklist de Auditoria de Unit Economics

> Checklist para validar que as métricas de unit economics são precisas, atualizadas
> e refletem a realidade operacional do negócio. Aplicar mensalmente como parte do
> Unit Economics Engine e antes de apresentar métricas a investidores ou board.

---

## Propósito

Unit economics são as métricas mais citadas em board meetings e investor decks — e também
as mais frequentemente calculadas de forma errada. Este checklist garante que CAC, LTV, payback
e métricas relacionadas são **precisas, segmentadas, atualizadas e acionáveis**. Uma métrica
errada leva a decisões erradas: investir em canal que destrói valor, ou parar de investir em
canal que gera retorno.

## Quando Aplicar

- Mensalmente como parte do review de Unit Economics Engine
- Antes de qualquer apresentação a investidores ou board
- Quando métricas mostram mudança significativa (> 15%) sem causa óbvia
- Ao entrar em novo segmento de mercado ou lançar novo produto
- Após mudanças de pricing ou packaging
- Quando churn rate muda significativamente (> 2pp)

## Agente Responsável

**CFO Strategist** como DRI de accuracy. **CMO Architect** como co-owner de métricas de aquisição.
**CTO Architect** como co-owner de métricas de produto/retenção.

---

## Checklist

### 1. Precisão do CAC

- [ ] CAC calculado como fully-loaded (inclui salários, ferramentas, overhead de S&M)
- [ ] CAC segmentado por canal (paid, organic, referral, outbound, partner)
- [ ] CAC segmentado por segmento de cliente (SMB, Mid-Market, Enterprise)
- [ ] Período de atribuição definido e consistente (lag entre gasto e conversão)
- [ ] Modelo de atribuição documentado (first-touch, last-touch, multi-touch)
- [ ] Custos de vendas incluídos (salários, comissões, ferramentas de sales)
- [ ] Custos de marketing incluídos (ads, content, events, tools)
- [ ] Overhead alocado proporcionalmente (escritório, management, etc.)
- [ ] CAC trend dos últimos 6 meses documentado com explicação de variações
- [ ] CAC comparado com benchmarks do setor (está na faixa razoável?)

### 2. Precisão do LTV

- [ ] LTV calculado por método de cohort (não apenas fórmula simplificada)
- [ ] Dados de cohort de pelo menos 6-12 cohorts utilizados
- [ ] Churn rate utilizado é o real medido (não estimado ou "target")
- [ ] Gross margin aplicada corretamente no cálculo de LTV
- [ ] LTV segmentado por plano/produto e por segmento de cliente
- [ ] Expansion revenue incluída (upsell, cross-sell)
- [ ] Contraction revenue considerada (downgrades)
- [ ] Período de projeção de LTV limitado (não projetar além de dados observados)
- [ ] Discount rate aplicado para LTV de longo prazo (valor presente)
- [ ] LTV trend dos últimos 6 meses documentado

### 3. Qualidade da Cohort Analysis

- [ ] Cohorts definidas por mês de aquisição (padrão)
- [ ] Pelo menos 12 cohorts ativas com dados suficientes
- [ ] Revenue retention curve plotada para cada cohort
- [ ] Logo retention curve plotada para cada cohort
- [ ] Tendência de qualidade de cohorts documentada (melhorando ou piorando?)
- [ ] Cohorts segmentadas por canal de aquisição
- [ ] Cohorts segmentadas por segmento de cliente (SMB vs. Enterprise)
- [ ] Outliers identificados e explicados (cohort atípica = por quê?)
- [ ] Seasonality effects documentados (Q4 vs. Q1, por exemplo)
- [ ] Time-to-value por cohort medido (quanto tempo até ativação)

### 4. Métricas Compostas

- [ ] LTV:CAC ratio calculado corretamente (por segmento, não apenas blended)
- [ ] LTV:CAC trend documentado (melhorando ou piorando?)
- [ ] Payback period calculado e realista (CAC / ARPA × GM%)
- [ ] Net Revenue Retention (NRR) calculado mensalmente
- [ ] Gross Revenue Retention (GRR) calculado mensalmente
- [ ] Contribution margin por cliente/segmento atualizada
- [ ] ARPA (Average Revenue Per Account) trend documentado
- [ ] Comparação com benchmarks do setor para todas as métricas compostas

### 5. Integridade e Consistência dos Dados

- [ ] Fonte de dados de receita reconciliada com contabilidade
- [ ] Fonte de dados de clientes reconciliada com CRM
- [ ] Fonte de dados de custos reconciliada com financeiro
- [ ] Definição de "cliente ativo" consistente em todas as métricas
- [ ] Definição de "churn" consistente (logo churn vs. revenue churn documentado)
- [ ] Período de cálculo consistente (mensal para todas as métricas)
- [ ] Não há double-counting de receita ou custos
- [ ] Free trials e freemium excluídos ou tratados separadamente
- [ ] Refunds e chargebacks tratados corretamente na receita

---

## Critérios de Aprovação

As métricas de unit economics estão **aprovadas para uso** quando:

| Critério | Requisito |
|----------|-----------|
| Dados reconciliados | Receita, custo e clientes batendo com contabilidade |
| Segmentação mínima | CAC e LTV por canal + por segmento de cliente |
| Cohort analysis | ≥ 6 cohorts com dados de pelo menos 6 meses |
| Definições documentadas | Glossário de cada métrica com fórmula e fonte |
| Trend analysis | 6+ meses de histórico para cada métrica |
| Benchmarks | Comparação com pelo menos 3 benchmarks do setor |
| Peer review | Validado por pelo menos 1 pessoa além do autor |

---

## O que Fazer se Falhar

1. **CAC não fully-loaded:** Listar todos os custos de S&M e incluir no cálculo. Usar CAC fully-loaded internamente e destacar para investidores.

2. **LTV com fórmula simplificada apenas:** Construir análise de cohort real. Se não há dados suficientes (< 6 meses), declarar explicitamente que LTV é estimativa.

3. **Dados não reconciliados:** Pausar report de unit economics. Reconciliar com contabilidade antes de publicar.

4. **Sem segmentação:** Priorizar segmentação por canal (impacta decisões de marketing) e por tamanho de cliente (impacta decisões de go-to-market).

5. **Cohorts insuficientes:** Iniciar tracking imediatamente. Enquanto não há dados suficientes, usar fórmula simplificada com disclaimers explícitos.

6. **Métricas piorando:** Acionar investigação com CMO (se CAC) ou CPO (se retenção). Documentar causa raiz e plano de ação com DRI e deadline.

---

## Referências

- `frameworks/cfo-strategist/unit-economics-engine.md` — Motor de unit economics
- `frameworks/cfo-strategist/unit-economics.md` — Framework base de unit economics
- `frameworks/cfo-strategist/financial-modeling.md` — Conexão com modelo financeiro
- `templates/finance/unit-economics-dashboard.md` — Template de dashboard
- `checklists/finance/financial-health-audit.md` — Auditoria de saúde financeira

---

*Última atualização: Março 2026*
*Responsável: CFO Strategist*
