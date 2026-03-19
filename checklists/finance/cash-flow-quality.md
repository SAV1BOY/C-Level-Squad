# Checklist de Qualidade de Projeção de Cash Flow

> Checklist para validar que projeções de cash flow são confiáveis, com premissas
> fundamentadas, cenários modelados e riscos identificados. Aplicar antes de publicar
> qualquer projeção de caixa para stakeholders internos ou externos.

---

## Propósito

Garantir que projeções de cash flow não sejam exercícios de ficção otimista, mas sim
ferramentas confiáveis de decisão. Uma projeção ruim é pior que nenhuma projeção — ela
dá falsa confiança e leva a decisões que destroem caixa. Este checklist valida a qualidade
do processo, das premissas e dos outputs antes que a projeção seja usada.

## Quando Aplicar

- Antes de publicar o cash forecast semanal (13-week)
- Antes de apresentar projeção de caixa ao board
- Na preparação para fundraising (investidores avaliarão estas projeções)
- Quando premissas materiais mudam (perda de cliente, mudança de pricing, etc.)
- Após cada reforecast trimestral
- Quando variação entre projetado e realizado > 15% por 2 meses consecutivos

## Agente Responsável

**CFO Strategist** como DRI. Controller ou FP&A como executor. CEO como reviewer para projeções
apresentadas ao board ou investidores.

---

## Checklist

### 1. Qualidade dos Dados de Input

- [ ] Dados de receita recorrente reconciliados com billing system
- [ ] Dados de receita não-recorrente documentados com evidência (contratos, pipeline)
- [ ] Contas a receber aging atualizado e classificado por probabilidade de recebimento
- [ ] Folha de pagamento projetada com headcount plan aprovado
- [ ] Contratos de fornecedores com valores e datas de vencimento mapeados
- [ ] Compromissos futuros (leases, SaaS anuais, empréstimos) listados
- [ ] Dados históricos de pelo menos 6 meses utilizados como base
- [ ] Sazonalidade identificada e incorporada na projeção
- [ ] Inadimplência histórica considerada nos recebimentos projetados
- [ ] Impostos e obrigações fiscais calendariados corretamente

### 2. Qualidade das Premissas

- [ ] Toda premissa documentada explicitamente (nada hardcoded em fórmulas)
- [ ] Premissas de receita baseadas em drivers bottom-up (não "crescer 10% ao mês")
- [ ] Premissa de churn baseada em dados reais de cohort (não em estimativa otimista)
- [ ] Premissa de novos clientes alinhada com pipeline real e conversion rates históricas
- [ ] Premissas de custo baseadas em contratos reais e plano de contratação aprovado
- [ ] Premissas de timing de recebimento baseadas em DSO real (não em termos contratuais)
- [ ] Premissas de timing de pagamento baseadas em DPO real
- [ ] Premissas validadas com owners de cada área (não apenas estimativa do finance)
- [ ] Premissas comparadas com benchmarks de mercado (são realistas?)
- [ ] Delta entre premissas e realizado dos últimos 3 meses documentado e explicado

### 3. Cenários Modelados

- [ ] Cenário base construído com premissas realistas (não otimistas)
- [ ] Cenário bear (pessimista) modelado: o que acontece se receita cai 20-30%?
- [ ] Cenário bull (otimista) modelado: o que acontece se crescimento acelera?
- [ ] Probabilidades atribuídas a cada cenário (e somam 100%)
- [ ] Runway calculado para cada cenário
- [ ] Ponto de break-even de caixa identificado em cada cenário
- [ ] Trigger points definidos: "Se X acontecer, ativamos plano Y"
- [ ] Stress test extremo realizado: "Se receita para 100%, quanto tempo temos?"

### 4. Riscos Identificados

- [ ] Top 5 riscos de downside ao cash flow listados com probabilidade e impacto
- [ ] Concentração de receita avaliada (risco de perda de cliente-chave)
- [ ] Risco cambial avaliado (se receita/custo em moeda estrangeira)
- [ ] Risco de inadimplência quantificado por segmento de cliente
- [ ] Risco de aumento de custos mapeado (reajustes, inflação, câmbio)
- [ ] Risco regulatório/fiscal avaliado (mudanças tributárias)
- [ ] Mitigação documentada para cada risco material
- [ ] Buffer de contingência incluído na projeção (5-10% das saídas)

### 5. Qualidade do Output

- [ ] Projeção em formato padronizado e legível por não-financeiros
- [ ] Saldo de caixa projetado semana a semana (13-week) e mês a mês (12 meses)
- [ ] Minimum cash balance destacado com alerta visual
- [ ] Gráfico de evolução de caixa com banda de cenários (bear/base/bull)
- [ ] Runway atual e projetado destacado
- [ ] Principais drivers de variação vs. mês anterior explicados
- [ ] Ações recomendadas baseadas na projeção documentadas
- [ ] Versão e data da projeção claramente identificadas
- [ ] Comparação com projeção anterior (o que mudou e por quê)

---

## Critérios de Aprovação

A projeção está **aprovada para uso** quando:

| Critério | Requisito |
|----------|-----------|
| Dados reconciliados | 100% dos inputs verificados contra fonte |
| Premissas documentadas | Todas explícitas e validadas com owners |
| Cenários modelados | Mínimo 3 (bear, base, bull) |
| Riscos identificados | Top 5 com probabilidade, impacto e mitigação |
| Accuracy histórica | Variação dos últimos 3 meses < 15% |
| Peer review | Revisado por pelo menos 1 pessoa além do autor |
| Formato padrão | Segue template de `templates/finance/cash-flow-projection.md` |

**Se a accuracy histórica for > 15%, a projeção pode ser publicada mas com disclaimer
explícito sobre a margem de erro e as causas da imprecisão.**

---

## O que Fazer se Falhar

1. **Dados não reconciliados:** Pausar projeção. Reconciliar dados antes de prosseguir. Projeção com dados ruins é pior que nenhuma projeção.

2. **Premissas não validadas:** Agendar reunião rápida (30 min) com owners das premissas críticas. Atualizar e re-rodar o modelo.

3. **Cenários não modelados:** No mínimo, criar cenário bear com 70% da receita base e 110% dos custos base. Documenta, mesmo que simples.

4. **Riscos não identificados:** Workshop de 1 hora com CFO + COO + CEO para brainstorm de riscos. Usar pre-mortem: "Imagine que ficamos sem caixa em 6 meses. O que causou?"

5. **Accuracy ruim (> 15%):** Investigar causa raiz da imprecisão. Recalibrar premissas. Considerar granularidade maior (semana ao invés de mês) para melhorar precisão.

6. **Sem peer review:** Não publicar para board sem revisão. Internamente, publicar com flag "draft — pending review."

---

## Referências

- `frameworks/cfo-strategist/cash-flow-management.md` — Framework de gestão de caixa
- `frameworks/cfo-strategist/financial-modeling.md` — Modelagem financeira
- `frameworks/cfo-strategist/scenario-planning.md` — Planejamento de cenários
- `templates/finance/cash-flow-projection.md` — Template de projeção de caixa
- `checklists/finance/financial-health-audit.md` — Auditoria de saúde financeira
- `checklists/finance/monthly-close-quality.md` — Qualidade do fechamento mensal

---

*Última atualização: Março 2026*
*Responsável: CFO Strategist*
