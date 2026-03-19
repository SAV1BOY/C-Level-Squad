# Checklist de Qualidade do Fechamento Mensal

> Checklist para garantir que o fechamento contábil mensal é completo, preciso
> e gera insights acionáveis. Aplicar até D+10 de cada mês para o mês anterior.

---

## Propósito

O fechamento mensal é o alicerce de toda decisão financeira. Se os números não estão corretos,
reconciliados e analisados, toda decisão baseada neles é potencialmente errada. Este checklist
garante que o processo de close produz números confiáveis, variações explicadas e forecasts
atualizados — transformando dados contábeis em inteligência de negócio.

## Quando Aplicar

- Todo mês, até D+10 do mês subsequente (ex: close de fevereiro até 10 de março)
- Close trimestral segue o mesmo checklist com itens adicionais de reporting para board
- Close anual segue este checklist + preparação para auditoria externa (se aplicável)
- Qualquer close extraordinário solicitado (due diligence, fundraising)

## Agente Responsável

**CFO Strategist** como DRI do close. Controller/FP&A como executor. Cada líder de área como
responsável por validar dados da sua área.

---

## Checklist

### 1. Reconciliação e Fechamento Contábil

- [ ] Todas as contas bancárias reconciliadas (saldo contábil = saldo bancário)
- [ ] Contas a receber atualizadas e aging classificado (current, 30, 60, 90+ dias)
- [ ] Contas a pagar atualizadas e vencimentos mapeados
- [ ] Provisões atualizadas (férias, 13o, impostos diferidos)
- [ ] Receita diferida (deferred revenue) reconciliada com billing
- [ ] Revenue recognition aplicado conforme política contábil
- [ ] Depreciação e amortização calculadas e contabilizadas
- [ ] Folha de pagamento reconciliada (valor contábil = valor pago)
- [ ] Impostos apurados e provisões atualizadas
- [ ] Cartões corporativos reconciliados e categorizados
- [ ] Estoque (se aplicável) inventariado e ajustado
- [ ] Intercompany transactions reconciliadas (se aplicável)

### 2. Demonstração de Resultados (DRE/P&L)

- [ ] Receita total fechada e reconciliada com faturamento
- [ ] Receita segmentada por produto/serviço, cliente, canal
- [ ] COGS apurado por componente (infra, suporte, pagamentos)
- [ ] Margem bruta calculada (total e por segmento)
- [ ] OPEX consolidado por área (Engineering, S&M, G&A, Product)
- [ ] EBITDA calculado
- [ ] Resultado antes e depois de impostos fechado
- [ ] Comparação com mês anterior e mesmo mês do ano anterior
- [ ] Comparação com budget do mês (actuals vs. budget)

### 3. Análise de Variações

- [ ] Top 5 variações positivas vs. budget documentadas com causa raiz
- [ ] Top 5 variações negativas vs. budget documentadas com causa raiz
- [ ] Variações classificadas por tipo (timing, volume, preço, escopo, eficiência)
- [ ] Variações > 10% com plano de ação e DRI designado
- [ ] Variações > 20% escaladas para CFO/CEO com ação corretiva
- [ ] Variações one-time identificadas e separadas de recorrentes
- [ ] Impacto acumulado no ano das variações documentado
- [ ] Tendência de variações analisada (variação crescente = problema sistêmico)

### 4. KPIs e Métricas Operacionais

- [ ] MRR/ARR atualizado e reconciliado
- [ ] Net Revenue Retention (NRR) calculado
- [ ] Logo churn e revenue churn do mês medidos
- [ ] CAC do mês calculado (blended e por canal)
- [ ] Burn rate (net e gross) atualizado
- [ ] Runway recalculado com dados atuais
- [ ] Revenue per employee atualizado
- [ ] Rule of 40 atualizada
- [ ] Cash conversion cycle recalculado
- [ ] Headcount vs. plan atualizado

### 5. Forecast Update

- [ ] Forecast do ano atualizado com actuals até o mês corrente
- [ ] Premissas revisadas com base em performance real
- [ ] Revenue forecast ajustado (pipeline real + conversion rate atual)
- [ ] Cost forecast ajustado (headcount plan + compromissos conhecidos)
- [ ] Cash forecast (13-week) atualizado com dados reais
- [ ] Cash forecast (12-month) atualizado
- [ ] Cenários (bull/base/bear) recalibrados
- [ ] Runway reprojetado com novo forecast
- [ ] Gaps vs. targets anuais identificados e quantificados
- [ ] Ações de recovery documentadas se performance < plan

### 6. Reporting e Comunicação

- [ ] Report executivo para C-level preparado (1-2 páginas)
- [ ] Dashboard financeiro atualizado e acessível
- [ ] Highlights e lowlights resumidos em formato claro
- [ ] Ações do mês anterior revisadas (concluídas/pendentes/atrasadas)
- [ ] Novas ações documentadas com DRI e deadline
- [ ] Report para board preparado (se mês de board meeting)
- [ ] Comunicação para gestores de área com performance de seus budgets
- [ ] Agenda da reunião de MBR financeiro preparada

---

## Critérios de Aprovação

O fechamento mensal está **aprovado** quando:

| Critério | Requisito |
|----------|-----------|
| Reconciliação | 100% das contas reconciliadas, diferença < R$ 1K |
| Timing | Close completo até D+10 |
| Variações | 100% das variações > 10% explicadas com causa raiz |
| KPIs | Todas as métricas-chave atualizadas |
| Forecast | Forecast do ano atualizado com actuals |
| Report | Report executivo preparado e revisado |
| Ações | Ações do mês anterior com status atualizado |

**Score de Close:**
- ✅ 7/7: Close perfeito
- 🟡 5-6/7: Close aceitável, melhorar itens pendentes
- 🔴 < 5/7: Close incompleto — não publicar até completar

---

## O que Fazer se Falhar

1. **Reconciliação incompleta:** Não publicar números. Diferença inexplicada pode esconder erro material. Resolver antes de D+12 no máximo.

2. **Close atrasado (> D+10):** Identificar gargalo (dados de área? sistema? processo?). Implementar SLA com áreas para entrega de dados até D+3.

3. **Variações não explicadas:** Owner da área tem 48h para explicar. Se não explicar, escalar para COO. Variação inexplicada = falta de controle.

4. **KPIs desatualizados:** Priorizar MRR, burn rate e runway (métricas de sobrevivência). Demais KPIs podem ser atualizados até D+15.

5. **Forecast não atualizado:** Publicar close com disclaimer "forecast em atualização." Completar forecast até D+15. Nunca apresentar ao board com forecast desatualizado.

6. **Report incompleto:** Report mínimo viável: P&L vs. budget + top 3 variações + runway. Versão completa até D+15.

---

## Referências

- `frameworks/cfo-strategist/financial-modeling.md` — Modelo financeiro para forecast update
- `frameworks/cfo-strategist/budget-governance.md` — Governance de variações
- `frameworks/cfo-strategist/cash-flow-management.md` — Gestão de caixa
- `templates/finance/monthly-financial-report.md` — Template do report mensal
- `checklists/finance/financial-health-audit.md` — Auditoria de saúde financeira
- `checklists/finance/cash-flow-quality.md` — Qualidade de projeções de caixa
- `checklists/finance/budget-review.md` — Revisão de budget

---

*Última atualização: Março 2026*
*Responsável: CFO Strategist*
