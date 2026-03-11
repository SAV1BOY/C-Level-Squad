# Framework de Planejamento Financeiro — FP&A Estratégico

## Propósito e Contexto

Planejamento financeiro em empresas de tecnologia vai muito além da contabilidade tradicional.
É a tradução da estratégia em números, a criação de cenários para decisões sob incerteza e o
sistema de alerta antecipado que permite à empresa reagir antes que problemas se tornem crises.
O CFO moderno não é apenas o guardião do caixa — é o arquiteto financeiro da estratégia.

Este framework estrutura o processo de FP&A (Financial Planning & Analysis) para empresas em
crescimento, desde startups com primeiro funding até scale-ups preparando para IPO. O foco é
em planejamento acionável — não em planilhas bonitas que ninguém usa.

## Quando Usar

- No ciclo anual de planejamento (budget anual)
- Em revisões trimestrais de forecast (re-forecast)
- Na preparação para fundraising (projeções para investidores)
- Ao avaliar novos investimentos (hiring, expansão, M&A)
- Quando runway está abaixo de 18 meses
- Em momentos de mudança macroeconômica significativa

## Componentes do Framework

### 1. Modelo Financeiro de 3 Camadas

**Camada 1: Operating Model (mensal, 12-18 meses)**
- Granularidade: linha por linha, mês a mês
- Inputs: pipeline de vendas, hiring plan, contratos existentes
- Outputs: P&L mensal, cash flow, headcount plan
- Responsável: FP&A com inputs de cada área

**Camada 2: Strategic Model (anual, 3-5 anos)**
- Granularidade: por unidade de negócio, anual
- Inputs: market sizing, penetration assumptions, unit economics targets
- Outputs: revenue trajectories, investment requirements, path to profitability
- Responsável: CFO com CEO e board

**Camada 3: Scenario Model (event-driven)**
- Cenários: base, upside, downside, catastrophe
- Trigger-based: "Se X acontecer, o plano muda para Y"
- Outputs: contingency plans, decision triggers
- Referência cruzada: `frameworks/cfo-strategist/scenario-planning.md`

### 2. Estrutura de Revenue Forecasting

**Para SaaS/Recorrência:**
```
MRR Início do Mês
+ New MRR (novos clientes)
+ Expansion MRR (upsell, cross-sell)
- Contraction MRR (downgrade)
- Churn MRR (cancelamentos)
= MRR Fim do Mês

ARR = MRR × 12
```

**Para Transacional:**
```
Receita = Transações × Ticket Médio
Transações = Usuários Ativos × Frequência × Conversão
```

### 3. Estrutura de Cost Planning

**Custos por Natureza:**
- Pessoas: salários, benefícios, impostos, contratações planejadas
- Infraestrutura: cloud, SaaS, licenças, escritório
- Marketing: paid acquisition, eventos, branding
- Serviços: jurídico, contabilidade, consultoria
- Outros: viagens, equipamentos, contingência

**Custos por Função:**
- COGS (Custo do Serviço): infra, suporte, customer success
- R&D: engenharia, produto, design
- S&M: vendas, marketing, partnerships
- G&A: finance, legal, people, administração

### 4. Cash Management

**Runway Calculation:**
```
Runway (meses) = Caixa Atual / Burn Rate Mensal
Burn Rate = Despesas Totais - Receita
Net Burn Rate (com receita) vs. Gross Burn (sem receita)
```

**Regras de Ouro:**
- Runway mínimo confortável: 18 meses
- Iniciar fundraising com ≥ 12 meses de runway
- Buffer de contingência: 15-20% do budget anual não alocado

## Processo Passo-a-Passo

### Ciclo Anual de Planejamento (T-2 meses antes do ano fiscal)

**Semana 1-2: Diretrizes Estratégicas**
1. CEO e board definem metas de crescimento e limites de investimento
2. CFO traduz em guidelines financeiros (budget envelope por área)
3. Cada C-level recebe guidelines para planejamento da sua área

**Semana 3-4: Bottom-Up Planning**
1. Cada área constrói seu plano detalhado dentro do envelope
2. Revenue team projeta pipeline e conversão
3. Engineering planeja hiring e infra
4. Marketing projeta investimento e ROI esperado

**Semana 5-6: Consolidação e Trade-offs**
1. CFO consolida planos em modelo integrado
2. Identificação de gaps entre aspiração e realidade
3. Sessões de trade-off com C-level (o que cortar para investir)
4. Cenários: base, upside, downside

**Semana 7-8: Aprovação e Comunicação**
1. Apresentação para o board
2. Aprovação formal do budget
3. Comunicação para toda a empresa (versão simplificada)
4. Setup de dashboards e cadência de revisão

### Ciclo Mensal de Acompanhamento
1. Fechamento financeiro (D+5 do mês)
2. Análise de variância: actual vs. budget vs. forecast
3. Atualização de forecast rolling (próximos 3-6 meses)
4. Report para C-level e board

## Template de Report Mensal

```markdown
# Financial Report — [Mês/Ano]

## TL;DR
- Revenue: R$ [X] ([+/-Y%] vs budget)
- Burn: R$ [X] ([+/-Y%] vs budget)
- Runway: [X] meses
- Headcount: [X] ([+/-Y] vs plan)

## Revenue Analysis
[Tabela com breakdown por produto/segmento]
[Análise de variância]

## Cost Analysis
[Tabela com breakdown por área]
[Itens above/below budget com explicação]

## Cash Position
[Saldo, projeção de runway, upcoming large payments]

## Key Risks & Opportunities
[2-3 bullets com impacto financeiro estimado]

## Forecast Update
[Mudanças no forecast para o restante do ano]
```

## Checklist de Planejamento

- [ ] Revenue forecast é baseado em pipeline real (bottom-up), não apenas growth rate?
- [ ] Hiring plan está alinhado com budget de pessoas?
- [ ] Custos de infra incluem projeção de crescimento de uso?
- [ ] Existe buffer de contingência (15-20%)?
- [ ] Cenários downside foram modelados com ações de contingência?
- [ ] Runway projetado é ≥ 18 meses no cenário base?
- [ ] O modelo é auditável (inputs claros, fórmulas transparentes)?
- [ ] Cada área validou e concordou com seu budget?

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Forecast accuracy (revenue) | Variação < 10% | Mensal |
| Forecast accuracy (costs) | Variação < 5% | Mensal |
| Fechamento financeiro | ≤ D+5 do mês | Mensal |
| Budget utilization | 90-105% (nem sub nem super) | Trimestral |
| Runway | ≥ 18 meses | Mensal |
| Report delivery | 100% no prazo | Mensal |

## Referências Cruzadas

- `frameworks/cfo-strategist/unit-economics.md` — Métricas unitárias que alimentam o modelo
- `frameworks/cfo-strategist/scenario-planning.md` — Cenários detalhados
- `frameworks/cfo-strategist/fundraising-readiness.md` — Projeções para investidores
- `frameworks/cfo-strategist/cost-optimization.md` — Otimização quando custos excedem budget
- `frameworks/vision-chief/vision-strategy-cascade.md` — Estratégia que o plano financia
- `frameworks/vision-chief/board-communication.md` — Financials para o board
- `frameworks/shared/risk-management.md` — Riscos financeiros no framework de risco
