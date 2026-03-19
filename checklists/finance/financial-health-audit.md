# Checklist de Auditoria de Saúde Financeira

> Checklist abrangente para avaliar a saúde financeira da empresa em quatro dimensões:
> liquidez, rentabilidade, eficiência e crescimento. Aplicar trimestralmente ou quando
> houver mudança material no contexto de negócio.

---

## Propósito

Garantir que a empresa mantém uma posição financeira saudável e sustentável, identificando
sinais de alerta antes que se tornem crises. Este checklist funciona como um "check-up médico"
financeiro — examina sinais vitais, diagnostica problemas e recomenda tratamentos.

## Quando Aplicar

- Trimestralmente como parte do QBR financeiro
- Antes de fundraising (investidores farão a mesma análise)
- Após eventos materiais (perda de cliente grande, mudança de mercado, contratação em massa)
- Quando runway cai abaixo de 12 meses
- Na preparação para board meetings
- Quando indicadores-chave mostram tendência negativa por 2+ meses

## Agente Responsável

**CFO Strategist** com input de COO Orchestrator (métricas operacionais) e CMO Architect (métricas de growth).

---

## Checklist

### 1. Liquidez e Caixa

- [ ] Posição de caixa atual documentada (todas as contas)
- [ ] Runway calculado com net burn atual (meses restantes)
- [ ] Runway calculado com gross burn (cenário worst case)
- [ ] 13-week cash forecast atualizado e revisado
- [ ] Minimum cash balance definido e respeitado (≥ 3 meses de gross burn)
- [ ] Cash conversion cycle (CCC) calculado e comparado com trimestre anterior
- [ ] DSO (Days Sales Outstanding) medido — prazo médio de recebimento
- [ ] DPO (Days Payable Outstanding) medido — prazo médio de pagamento
- [ ] Inadimplência medida como % da receita (aceitável: < 3%)
- [ ] Linhas de crédito disponíveis mapeadas (valor e condições)
- [ ] Concentração de receita avaliada (nenhum cliente > 20% da receita total)
- [ ] Sazonalidade de caixa mapeada para próximos 12 meses

### 2. Rentabilidade

- [ ] Margem bruta calculada e comparada com benchmark do setor
- [ ] Margem bruta por produto/serviço segmentada
- [ ] EBITDA margin calculada (ou projetada para path to profitability)
- [ ] Contribuition margin por segmento de cliente calculada
- [ ] Unit economics saudáveis: LTV:CAC > 3:1
- [ ] Payback period aceitável (< 12 meses SMB / < 18 meses Enterprise)
- [ ] Rule of 40 calculada (growth rate % + profit margin % ≥ 40)
- [ ] Custo fixo vs. variável como % da receita documentado
- [ ] Break-even analysis atualizada (quando a empresa se paga?)
- [ ] Path to profitability claro e documentado com timeline

### 3. Eficiência Operacional

- [ ] Burn rate (net e gross) monitorado com tendência de 6 meses
- [ ] Revenue per employee calculado e comparado com benchmarks
- [ ] CAC efficiency medida por canal (CAC vs. LTV por canal)
- [ ] Magic number calculado (eficiência de vendas): ≥ 0.75 é saudável
- [ ] Custo de infraestrutura como % da receita (SaaS: target < 15%)
- [ ] Custo de suporte como % da receita (target < 10%)
- [ ] Headcount growth vs. revenue growth alinhados (revenue deve crescer mais rápido)
- [ ] SaaS spend consolidado e racionalizado (sem ferramentas redundantes)
- [ ] Budget utilization por área (underspend pode ser tão ruim quanto overspend)
- [ ] Produtividade do time de vendas (quota attainment médio > 70%)

### 4. Crescimento e Sustentabilidade

- [ ] Revenue growth rate (MoM e YoY) calculado e com tendência
- [ ] Net Revenue Retention (NRR) medido (target: > 110%)
- [ ] Logo retention medida (target: > 85% anual para SMB, > 95% para Enterprise)
- [ ] Pipeline coverage ratio adequado (≥ 3x o target de vendas do trimestre)
- [ ] Diversificação de receita analisada (por cliente, produto, canal, mercado)
- [ ] Cohort analysis atualizada com últimos 6 cohorts
- [ ] Expansion revenue como % do new business documentada
- [ ] Tendência de CAC nos últimos 6 meses (estável ou decrescente = saudável)
- [ ] Market opportunity vs. penetration avaliada (TAM/SAM/SOM)
- [ ] Funding needs vs. disponibilidade mapeado para próximos 18 meses

### 5. Governança e Compliance

- [ ] Fechamento contábil mensal em dia (até D+10)
- [ ] Reconciliação bancária concluída e sem pendências
- [ ] Obrigações fiscais em dia (impostos, declarações)
- [ ] Budget vs. actual reportado mensalmente a todas as áreas
- [ ] Decision registry financeiro atualizado
- [ ] Contratos significativos com termos documentados e revisados
- [ ] Seguro adequado contratado (D&O, cyber, E&O se aplicável)
- [ ] Cap table atualizado e auditado (se aplicável)

---

## Critérios de Aprovação

Para considerar a saúde financeira **saudável**, todos os seguintes devem ser verdadeiros:

| Critério | Threshold |
|----------|-----------|
| Runway | ≥ 12 meses |
| LTV:CAC | ≥ 3:1 |
| Margem bruta | ≥ 60% (SaaS) ou benchmark do setor |
| NRR | ≥ 100% |
| Revenue growth | Positivo e acelerando ou estável |
| Budget variance | < 15% em todas as áreas |
| Fechamento contábil | Em dia |
| Concentração de receita | Nenhum cliente > 20% |

**Score:**
- ✅ 8/8 critérios atendidos: Saúde excelente
- 🟡 6-7/8: Saúde boa, com pontos de atenção
- 🟠 4-5/8: Saúde preocupante, ações corretivas necessárias
- 🔴 < 4/8: Saúde crítica, intervenção urgente

---

## O que Fazer se Falhar

1. **Runway < 12 meses:** Ativar protocolo de fundraising ou cost-cutting imediato. Ver `frameworks/cfo-strategist/cash-flow-management.md`.
2. **LTV:CAC < 3:1:** Investigar causa (CAC alto ou LTV baixo?). Aplicar `frameworks/cfo-strategist/unit-economics-engine.md`.
3. **Margem bruta abaixo do benchmark:** Auditar COGS por componente. Aplicar `frameworks/cfo-strategist/cost-optimization.md`.
4. **NRR < 100%:** Investigar churn e contraction. Conectar com Product e Customer Success.
5. **Revenue growth negativo:** Reunião emergencial de liderança. Revisar GTM strategy.
6. **Budget variance > 15%:** Implementar controles mais rígidos. Ver `frameworks/cfo-strategist/budget-governance.md`.
7. **Concentração de receita:** Plano de diversificação com CMO e Sales.

---

## Referências

- `frameworks/cfo-strategist/financial-modeling.md` — Modelo financeiro para projeções
- `frameworks/cfo-strategist/cash-flow-management.md` — Gestão detalhada de caixa
- `frameworks/cfo-strategist/unit-economics-engine.md` — Motor de unit economics
- `frameworks/cfo-strategist/budget-governance.md` — Governança orçamentária
- `checklists/finance/budget-review.md` — Revisão detalhada de budget
- `checklists/finance/cash-flow-quality.md` — Qualidade das projeções de caixa
- `templates/finance/monthly-financial-report.md` — Report mensal financeiro

---

*Última atualização: Março 2026*
*Responsável: CFO Strategist*
