# Relatório de ROI de Marketing

## Propósito
Medir e reportar o retorno sobre investimento das atividades de marketing, conectando
gastos a resultados de negócio (pipeline, receita, retenção), fornecendo visibilidade
para decisões de alocação de budget.

## Quando Usar
- Mensalmente como parte do MBR
- Trimestralmente para revisão de alocação de budget
- Ao final de campanhas significativas
- Para justificar aumento ou realocação de investimento em marketing

## Agente Responsável
- **Autor primário:** CMO Agent
- **Validação financeira:** CFO Agent
- **Revisor:** Chief of Staff Agent (CoS)

## Template

---

### RELATÓRIO DE ROI DE MARKETING

**Período:** {{periodo_analise}}
**Data do relatório:** {{data_relatorio}}
**Autor:** {{autor}}
**Budget total do período:** {{budget_total}}

---

#### 1. Resumo Executivo

**ROI geral de marketing:** {{roi_percentual}}
**Para cada R$ 1 investido, geramos:** R$ {{retorno_por_real}}
**Comparação com período anterior:** {{comparacao_anterior}}

---

#### 2. Funil Completo

| Estágio | Volume | Conversão | Custo Total | Custo Unitário | vs. Período Anterior |
|---------|--------|-----------|-------------|----------------|---------------------|
| Impressões | {{impressoes}} | — | {{custo_impressoes}} | {{cpm}} | {{vs_impressoes}} |
| Visitantes | {{visitantes}} | {{conv_visit}} | — | — | {{vs_visitantes}} |
| Leads (MQL) | {{mqls}} | {{conv_mql}} | {{custo_mql}} | {{cpl}} | {{vs_mqls}} |
| Oportunidades (SQL) | {{sqls}} | {{conv_sql}} | {{custo_sql}} | {{cpo}} | {{vs_sqls}} |
| Clientes fechados | {{clientes}} | {{conv_cliente}} | {{custo_total}} | {{cac}} | {{vs_clientes}} |
| Receita gerada | {{receita}} | — | — | — | {{vs_receita}} |

---

#### 3. ROI por Canal

| Canal | Investimento | Leads | Clientes | Receita | ROI | ROAS | Tendência |
|-------|-------------|-------|----------|---------|-----|------|-----------|
| {{canal_1}} | {{invest_1}} | {{leads_1}} | {{clientes_1}} | {{receita_1}} | {{roi_1}} | {{roas_1}} | {{tend_1}} |
| {{canal_2}} | {{invest_2}} | {{leads_2}} | {{clientes_2}} | {{receita_2}} | {{roi_2}} | {{roas_2}} | {{tend_2}} |
| {{canal_3}} | {{invest_3}} | {{leads_3}} | {{clientes_3}} | {{receita_3}} | {{roi_3}} | {{roas_3}} | {{tend_3}} |
| {{canal_4}} | {{invest_4}} | {{leads_4}} | {{clientes_4}} | {{receita_4}} | {{roi_4}} | {{roas_4}} | {{tend_4}} |
| {{canal_5}} | {{invest_5}} | {{leads_5}} | {{clientes_5}} | {{receita_5}} | {{roi_5}} | {{roas_5}} | {{tend_5}} |
| **Total** | **{{invest_total}}** | **{{leads_total}}** | **{{clientes_total}}** | **{{receita_total}}** | **{{roi_total}}** | **{{roas_total}}** | — |

---

#### 4. ROI por Campanha

| Campanha | Budget | Leads | SQLs | Revenue | ROI | Status |
|----------|--------|-------|------|---------|-----|--------|
| {{campanha_1}} | {{budget_c1}} | {{leads_c1}} | {{sqls_c1}} | {{rev_c1}} | {{roi_c1}} | {{status_c1}} |
| {{campanha_2}} | {{budget_c2}} | {{leads_c2}} | {{sqls_c2}} | {{rev_c2}} | {{roi_c2}} | {{status_c2}} |
| {{campanha_3}} | {{budget_c3}} | {{leads_c3}} | {{sqls_c3}} | {{rev_c3}} | {{roi_c3}} | {{status_c3}} |

---

#### 5. Análise de CAC e Payback

| Segmento | CAC | LTV | LTV/CAC | Payback (meses) | Tendência |
|---------|-----|-----|---------|-----------------|-----------|
| {{segmento_1}} | {{cac_1}} | {{ltv_1}} | {{ratio_1}} | {{payback_1}} | {{tend_1}} |
| {{segmento_2}} | {{cac_2}} | {{ltv_2}} | {{ratio_2}} | {{payback_2}} | {{tend_2}} |
| {{segmento_3}} | {{cac_3}} | {{ltv_3}} | {{ratio_3}} | {{payback_3}} | {{tend_3}} |
| **Blended** | **{{cac_blended}}** | **{{ltv_blended}}** | **{{ratio_blended}}** | **{{payback_blended}}** | — |

---

#### 6. Content e SEO Performance

| Métrica | Período Atual | Anterior | Var. % |
|---------|-------------|----------|--------|
| Organic traffic | {{organic_atual}} | {{organic_ant}} | {{var_organic}} |
| Organic leads | {{org_leads_atual}} | {{org_leads_ant}} | {{var_org_leads}} |
| Domain authority | {{da_atual}} | {{da_ant}} | {{var_da}} |
| Ranking keywords (top 10) | {{kw_atual}} | {{kw_ant}} | {{var_kw}} |
| Content pieces published | {{content_atual}} | {{content_ant}} | {{var_content}} |

---

#### 7. Recomendações de Alocação

| Canal | Budget Atual | Budget Recomendado | Var. | Justificativa |
|-------|-------------|-------------------|------|---------------|
| {{canal_1}} | {{atual_1}} | {{recom_1}} | {{var_1}} | {{just_1}} |
| {{canal_2}} | {{atual_2}} | {{recom_2}} | {{var_2}} | {{just_2}} |
| {{canal_3}} | {{atual_3}} | {{recom_3}} | {{var_3}} | {{just_3}} |
| {{canal_4}} | {{atual_4}} | {{recom_4}} | {{var_4}} | {{just_4}} |

---

#### 8. Insights e Aprendizados

**O que funcionou:**
- {{insight_positivo_1}}
- {{insight_positivo_2}}

**O que não funcionou:**
- {{insight_negativo_1}}
- {{insight_negativo_2}}

**Hipóteses para o próximo período:**
- {{hipotese_1}}
- {{hipotese_2}}

---

## Instruções de Preenchimento

1. **Atribuição:** Defina o modelo de atribuição usado (first-touch, last-touch, multi-touch).
   Documente e mantenha consistente entre períodos.
2. **ROI vs ROAS:** ROI inclui todos os custos (equipe, ferramentas). ROAS considera apenas media spend.
3. **Cohorts:** Receita de marketing tem lag. Considere a janela de atribuição adequada (30, 60, 90 dias).
4. **Tendências:** Mais importante que o número absoluto é a direção. Indique tendências de 3+ períodos.
5. **Recomendações:** Baseie realocações em dados, não em preferências. Aumente o que funciona, corte o que não.

## Exemplo Preenchido

---

### RELATÓRIO DE ROI — Fevereiro 2026

**Budget total:** R$ 380K
**ROI geral:** 340%
**Para cada R$ 1 investido:** R$ 3,40 em receita

#### 3. ROI por Canal
| Canal | Investimento | Leads | Revenue | ROI |
|-------|-------------|-------|---------|-----|
| Google Ads | R$ 120K | 450 | R$ 520K | 333% |
| LinkedIn Ads | R$ 80K | 180 | R$ 380K | 375% |
| Content/SEO | R$ 60K | 320 | R$ 280K | 367% |
| Events | R$ 90K | 85 | R$ 150K | 67% |
| Referral | R$ 30K | 120 | R$ 290K | 867% |

**Recomendação:** Realocar R$ 40K de Events para Referral (maior ROI, sub-investido).

---

## Checklist de Qualidade

- [ ] Modelo de atribuição documentado e consistente
- [ ] Funil completo rastreado (impressão → receita)
- [ ] ROI calculado por canal e por campanha
- [ ] Unit economics (CAC, LTV, Payback) atualizados
- [ ] Dados de organic/SEO incluídos
- [ ] Recomendações de realocação baseadas em dados
- [ ] Tendências de 3+ períodos indicadas
- [ ] CFO Agent validou os números de receita atribuída
- [ ] Insights e aprendizados documentados
- [ ] Janela de atribuição e lag de receita considerados
