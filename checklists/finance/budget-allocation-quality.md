# Checklist de Qualidade de Alocação de Budget

> Checklist para validar que a alocação de budget é estrategicamente alinhada,
> financeiramente justificada e operacionalmente exequível. Aplicar na aprovação
> do budget anual, em reallocation decisions e em pedidos de budget incremental.

---

## Propósito

Garantir que cada real alocado no budget tem propósito claro, retorno esperado mensurável
e alinhamento com a estratégia da empresa. Este checklist previne os erros mais comuns de
alocação: peanut butter spreading (distribuir igualmente), sunk cost bias (continuar gastando
no que não funciona) e disconnected budgets (budget desconectado de OKRs).

## Quando Aplicar

- Na aprovação do budget anual (Annual Planning)
- Em cada pedido de budget incremental (acima do planejado)
- Nas revisões trimestrais com proposta de reallocation
- Quando uma área solicita aumento > 10% do budget original
- Ao avaliar investimentos em novos projetos ou iniciativas
- Antes de aprovar contratações em massa (> 5 FTEs)

## Agente Responsável

**CFO Strategist** como DRI de aprovação. Cada líder de área como DRI do budget request.
CEO como approver final para alocações > R$ 100K ou mudanças estratégicas.

---

## Checklist

### 1. Alinhamento Estratégico

- [ ] Alocação conectada a OKRs ou iniciativas estratégicas aprovadas
- [ ] Prioridades de alocação refletem as bets estratégicas do período
- [ ] Proporção Run/Grow/Transform definida e justificada
- [ ] Cada área com budget linkado a pelo menos 1 OKR mensurável
- [ ] Kill list respeitada (budget não alocado para iniciativas descartadas)
- [ ] Alinhamento com thesis de investimento aprovada pelo board
- [ ] Trade-offs explícitos documentados (o que NÃO estamos financiando e por quê)

### 2. Justificativa Financeira

- [ ] ROI estimado para cada investimento > 5% do budget total
- [ ] Payback period calculado para investimentos de Grow e Transform
- [ ] IRR comparado com hurdle rate para investimentos materiais
- [ ] Opportunity cost avaliado (melhor uso alternativo do capital)
- [ ] Business case completo para investimentos > R$ 100K
- [ ] Alternativas analisadas (build vs. buy vs. partner)
- [ ] Custo de NÃO fazer avaliado e documentado
- [ ] Impacto no burn rate e runway calculado

### 3. Exequibilidade Operacional

- [ ] Headcount necessário disponível ou com plano de contratação viável
- [ ] Timeline de execução realista (não assume contratação instantânea)
- [ ] Dependências mapeadas (um projeto bloqueia outro?)
- [ ] Capacidade técnica confirmada com CTO/Engineering
- [ ] Capacidade de go-to-market confirmada com CMO/Sales
- [ ] Riscos de execução identificados com mitigação
- [ ] Seasonality considerada (contratação em dezembro é mais difícil)

### 4. Governança e Accountability

- [ ] DRI definido para cada linha de budget significativa
- [ ] Métricas de sucesso definidas para cada alocação
- [ ] Cadência de review definida (mensal para Grow, milestone-based para Transform)
- [ ] Kill criteria definidos para investimentos de Transform
- [ ] Authority matrix respeitada (aprovações conforme nível de valor)
- [ ] Variações de threshold definidas (quando escalar vs. quando resolver)
- [ ] Plano de contingência definido (3-5% do budget reservado)

### 5. Qualidade do Processo

- [ ] Budget construído bottom-up (não apenas top-down arbitrário)
- [ ] Inputs de todas as áreas coletados e considerados
- [ ] CFO revisou consolidação e identificou inconsistências
- [ ] CEO/Vision Chief validou alinhamento com visão estratégica
- [ ] Board aprovou (se aplicável para budget anual)
- [ ] Comunicação clara para toda a empresa sobre prioridades e trade-offs
- [ ] Template de `templates/finance/budget-allocation-matrix.md` preenchido

---

## Critérios de Aprovação

A alocação de budget está **aprovada** quando:

| Critério | Requisito |
|----------|-----------|
| Alinhamento estratégico | 100% das alocações linkadas a OKRs/iniciativas |
| Justificativa financeira | ROI/payback documentado para investimentos > 5% do budget |
| Exequibilidade | Headcount e capacidade confirmados |
| Accountability | DRI + métricas + kill criteria definidos |
| Envelope respeitado | Total alocado ≤ budget disponível + contingência |
| Diversificação | Nenhuma categoria (Run/Grow/Transform) com 0% |
| Aprovações | Cadeia de aprovação completa conforme authority matrix |

**Se qualquer critério não for atendido, a alocação volta para revisão antes de aprovação.**

---

## O que Fazer se Falhar

1. **Sem alinhamento estratégico:** Reunião com CEO/Vision Chief para validar prioridades. Resubmeter budget com linkage explícito a OKRs.

2. **Sem justificativa financeira:** Solicitar business case ao requestor. Usar template de `templates/finance/budget-request.md`. Prazo: 5 dias úteis.

3. **Sem exequibilidade:** Ajustar timeline ou scope. Não aprovar budget sem capacidade de execução — capital parado é desperdício.

4. **Sem accountability:** Não aprovar sem DRI nomeado. Se o dono não está definido, o investimento não está maduro para aprovação.

5. **Acima do envelope:** Priorizar usando capital allocation framework. Cortar investimentos de menor ROI ou postergar para próximo trimestre.

6. **Aprovações incompletas:** Escalar para próximo nível de authority. Não executar gasto sem aprovação documentada.

---

## Referências

- `frameworks/cfo-strategist/cfo-capital-allocation.md` — Framework de alocação de capital
- `frameworks/cfo-strategist/budget-governance.md` — Governança orçamentária
- `frameworks/cfo-strategist/financial-modeling.md` — Modelo financeiro
- `templates/finance/budget-allocation-matrix.md` — Matriz de alocação
- `templates/finance/budget-request.md` — Template de pedido de budget
- `checklists/finance/budget-review.md` — Checklist de revisão de budget
- `checklists/finance/financial-health-audit.md` — Auditoria de saúde financeira

---

*Última atualização: Março 2026*
*Responsável: CFO Strategist*
