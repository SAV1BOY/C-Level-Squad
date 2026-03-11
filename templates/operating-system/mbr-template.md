# Template de Monthly Business Review (MBR)

## Propósito
Consolidar a performance mensal do negócio com visão financeira, operacional e
estratégica, permitindo ajustes de curso, reforecast e decisões de alocação de
recursos com base em dados consolidados do mês.

## Quando Usar
- Na primeira semana de cada mês, revisando o mês anterior
- Como base para reforecast mensal e ajustes de plano
- Para alinhamento entre C-Level sobre prioridades do próximo mês
- Como input para a preparação do QBR

## Agente Responsável
- **Facilitador:** Chief of Staff Agent (CoS)
- **Contribuidor financeiro:** CFO Agent
- **Contribuidores operacionais:** Todos os agentes C-Level
- **Preparação:** Dados consolidados até D+3 do mês seguinte

## Template

---

### MONTHLY BUSINESS REVIEW — {{mes_ano}}

**Período:** {{data_inicio_mes}} a {{data_fim_mes}}
**Data da reunião:** {{data_reuniao}}
**Facilitador:** {{facilitador}}
**Duração:** 90 minutos

---

#### 1. Resumo Executivo do Mês

{{resumo_executivo_3_frases}}

**Nota geral do mês (1-5):** {{nota_mes}}
**Tema do mês:** {{tema_positivo_ou_negativo}}

---

#### 2. Métricas Financeiras

| Métrica | Plano Mensal | Realizado | Var. % | YTD Plan | YTD Real | YTD Var. |
|---------|-------------|-----------|--------|----------|----------|----------|
| Receita (MRR/ARR) | {{plan_receita}} | {{real_receita}} | {{var_receita}} | {{ytd_plan_rec}} | {{ytd_real_rec}} | {{ytd_var_rec}} |
| New MRR | {{plan_new}} | {{real_new}} | {{var_new}} | {{ytd_plan_new}} | {{ytd_real_new}} | {{ytd_var_new}} |
| Churn MRR | {{plan_churn}} | {{real_churn}} | {{var_churn}} | {{ytd_plan_churn}} | {{ytd_real_churn}} | {{ytd_var_churn}} |
| Expansion MRR | {{plan_exp}} | {{real_exp}} | {{var_exp}} | {{ytd_plan_exp}} | {{ytd_real_exp}} | {{ytd_var_exp}} |
| Margem Bruta | {{plan_mb}} | {{real_mb}} | {{var_mb}} | {{ytd_plan_mb}} | {{ytd_real_mb}} | {{ytd_var_mb}} |
| OPEX | {{plan_opex}} | {{real_opex}} | {{var_opex}} | {{ytd_plan_opex}} | {{ytd_real_opex}} | {{ytd_var_opex}} |
| EBITDA | {{plan_ebitda}} | {{real_ebitda}} | {{var_ebitda}} | {{ytd_plan_ebitda}} | {{ytd_real_ebitda}} | {{ytd_var_ebitda}} |
| Cash Burn | {{plan_burn}} | {{real_burn}} | {{var_burn}} | {{ytd_plan_burn}} | {{ytd_real_burn}} | {{ytd_var_burn}} |
| Cash Runway | {{plan_runway}} | {{real_runway}} | — | — | — | — |

---

#### 3. Métricas Operacionais

| Métrica | Meta | Realizado | Var. | Tendência (3M) |
|---------|------|-----------|------|---------------|
| {{metrica_ops_1}} | {{meta_ops_1}} | {{real_ops_1}} | {{var_ops_1}} | {{tend_ops_1}} |
| {{metrica_ops_2}} | {{meta_ops_2}} | {{real_ops_2}} | {{var_ops_2}} | {{tend_ops_2}} |
| {{metrica_ops_3}} | {{meta_ops_3}} | {{real_ops_3}} | {{var_ops_3}} | {{tend_ops_3}} |
| {{metrica_ops_4}} | {{meta_ops_4}} | {{real_ops_4}} | {{var_ops_4}} | {{tend_ops_4}} |
| {{metrica_ops_5}} | {{meta_ops_5}} | {{real_ops_5}} | {{var_ops_5}} | {{tend_ops_5}} |

---

#### 4. Progresso das Apostas (Bets)

| Aposta | Status | % Progresso | On Track? | Comentário |
|--------|--------|-------------|-----------|-----------|
| {{aposta_1}} | {{status_b1}} | {{progresso_b1}} | {{ontrack_b1}} | {{comentario_b1}} |
| {{aposta_2}} | {{status_b2}} | {{progresso_b2}} | {{ontrack_b2}} | {{comentario_b2}} |
| {{aposta_3}} | {{status_b3}} | {{progresso_b3}} | {{ontrack_b3}} | {{comentario_b3}} |

---

#### 5. Headcount e Pessoas

| Departamento | Headcount BOQ | Atual | Aberto | Saídas no Mês | Comentário |
|-------------|-------------|-------|--------|--------------|-----------|
| {{dept_1}} | {{boq_1}} | {{atual_1}} | {{aberto_1}} | {{saidas_1}} | {{coment_1}} |
| {{dept_2}} | {{boq_2}} | {{atual_2}} | {{aberto_2}} | {{saidas_2}} | {{coment_2}} |
| {{dept_3}} | {{boq_3}} | {{atual_3}} | {{aberto_3}} | {{saidas_3}} | {{coment_3}} |
| {{dept_4}} | {{boq_4}} | {{atual_4}} | {{aberto_4}} | {{saidas_4}} | {{coment_4}} |
| **Total** | **{{boq_total}}** | **{{atual_total}}** | **{{aberto_total}}** | **{{saidas_total}}** | — |

---

#### 6. Reforecast

**Forecast anterior (início do mês):** {{forecast_anterior}}
**Forecast atualizado:** {{forecast_atualizado}}
**Variação:** {{variacao_forecast}}

**Razão da mudança:**
{{razao_mudanca_forecast}}

---

#### 7. Top 3 Problemas do Mês

| # | Problema | Impacto | Causa Raiz | Ação | Owner | Prazo |
|---|---------|---------|-----------|------|-------|-------|
| 1 | {{problema_1}} | {{impacto_p1}} | {{causa_p1}} | {{acao_p1}} | {{owner_p1}} | {{prazo_p1}} |
| 2 | {{problema_2}} | {{impacto_p2}} | {{causa_p2}} | {{acao_p2}} | {{owner_p2}} | {{prazo_p2}} |
| 3 | {{problema_3}} | {{impacto_p3}} | {{causa_p3}} | {{acao_p3}} | {{owner_p3}} | {{prazo_p3}} |

---

#### 8. Decisões Tomadas no Mês

| # | Decisão | Data | DRI | Status de Implementação |
|---|---------|------|-----|------------------------|
| 1 | {{decisao_1}} | {{data_d1}} | {{dri_d1}} | {{status_d1}} |
| 2 | {{decisao_2}} | {{data_d2}} | {{dri_d2}} | {{status_d2}} |
| 3 | {{decisao_3}} | {{data_d3}} | {{dri_d3}} | {{status_d3}} |

---

#### 9. Prioridades do Próximo Mês

| # | Prioridade | Owner | Métrica de Sucesso | Dependências |
|---|-----------|-------|--------------------|--------------|
| 1 | {{prioridade_1}} | {{owner_pr1}} | {{metrica_pr1}} | {{dep_pr1}} |
| 2 | {{prioridade_2}} | {{owner_pr2}} | {{metrica_pr2}} | {{dep_pr2}} |
| 3 | {{prioridade_3}} | {{owner_pr3}} | {{metrica_pr3}} | {{dep_pr3}} |

---

## Instruções de Preenchimento

1. **Dados financeiros:** Devem ser fechados pelo CFO Agent. Não use estimativas para o MBR.
2. **YTD:** Sempre inclua a visão year-to-date para contexto de trajetória.
3. **Tendência 3M:** Mostra a direção dos últimos 3 meses, mais útil que o dado pontual.
4. **Reforecast:** Atualize o forecast do trimestre/ano com base nos dados reais.
5. **Problemas:** Limite a 3. Se há mais, priorize por impacto financeiro.
6. **Duração:** 90 minutos é o máximo. Se não cabe, os dados não estão suficientemente preparados.

## Exemplo Preenchido

---

### MONTHLY BUSINESS REVIEW — Fevereiro 2026

**Resumo:** Mês positivo em receita (+5% vs. plano) mas OPEX excedeu em 8% por contratações
antecipadas. Cash runway permanece saudável em 22 meses. Bet #1 (PLG) atrasada em 2 semanas.

**Nota geral do mês:** 3.5/5
**Tema do mês:** Crescimento sólido com disciplina de custos em risco

#### 2. Métricas Financeiras

| Métrica | Plano | Realizado | Var. % | YTD Plan | YTD Real | YTD Var. |
|---------|-------|-----------|--------|----------|----------|----------|
| MRR | R$ 4.0M | R$ 4.2M | +5% | R$ 7.8M | R$ 8.1M | +3.8% |
| New MRR | R$ 400K | R$ 450K | +12.5% | R$ 750K | R$ 820K | +9.3% |
| Churn MRR | R$ 60K | R$ 55K | +8.3% | R$ 125K | R$ 110K | +12% |

---

## Checklist de Qualidade

- [ ] Dados financeiros foram fechados e validados pelo CFO Agent
- [ ] Visão YTD está preenchida para contexto
- [ ] Tendência de 3 meses está indicada para métricas operacionais
- [ ] Progresso das apostas está atualizado com evidências
- [ ] Reforecast está baseado em dados reais (não em esperança)
- [ ] Top 3 problemas têm causa raiz identificada
- [ ] Prioridades do próximo mês estão definidas com owners
- [ ] Headcount tracker está atualizado
- [ ] A reunião respeitou o limite de 90 minutos
- [ ] Action items do MBR anterior foram revisados
