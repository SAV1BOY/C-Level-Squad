# Relatório de Reliability

## Propósito
Consolidar o estado de confiabilidade dos sistemas, reportando SLOs, incidentes,
postmortems, disponibilidade e tendências, fornecendo visibilidade para decisões
de investimento em infraestrutura e processos.

## Quando Usar
- Mensalmente como parte do MBR (seção técnica)
- Trimestralmente para revisão detalhada com C-Level
- Após incidentes significativos (P0/P1)
- Para justificar investimento em reliability/infrastructure

## Agente Responsável
- **Autor primário:** CTO Agent
- **Contribuidores:** SRE Lead, Engineering Managers
- **Revisor:** CEO Agent, CISO Agent
- **Destinatários:** Todos os agentes C-Level

## Template

---

### RELATÓRIO DE RELIABILITY — {{periodo}}

**Data:** {{data_relatorio}}
**Autor:** {{autor}}
**Período coberto:** {{data_inicio}} a {{data_fim}}

---

#### 1. Resumo Executivo

**Status geral de reliability:** {{saudavel_atencao_critico}}
**Uptime do período:** {{uptime_percentual}}
**Incidentes P0/P1:** {{quantidade_incidentes_graves}}
**Error budget restante:** {{error_budget_restante}}

---

#### 2. SLOs (Service Level Objectives)

| Serviço | SLO | Target | Realizado | Error Budget | Status |
|---------|-----|--------|-----------|-------------|--------|
| {{servico_1}} | {{slo_1}} | {{target_1}} | {{real_1}} | {{eb_1}} | {{status_1}} |
| {{servico_2}} | {{slo_2}} | {{target_2}} | {{real_2}} | {{eb_2}} | {{status_2}} |
| {{servico_3}} | {{slo_3}} | {{target_3}} | {{real_3}} | {{eb_3}} | {{status_3}} |
| {{servico_4}} | {{slo_4}} | {{target_4}} | {{real_4}} | {{eb_4}} | {{status_4}} |
| {{servico_5}} | {{slo_5}} | {{target_5}} | {{real_5}} | {{eb_5}} | {{status_5}} |

**Serviços com error budget esgotado:** {{lista_esgotados}}
**Ação:** {{acao_error_budget}}

---

#### 3. Métricas de Performance

| Métrica | Target | P50 | P95 | P99 | Tendência |
|---------|--------|-----|-----|-----|-----------|
| Latência — API principal | {{target_lat}} | {{p50_lat}} | {{p95_lat}} | {{p99_lat}} | {{tend_lat}} |
| Latência — Dashboard | {{target_dash}} | {{p50_dash}} | {{p95_dash}} | {{p99_dash}} | {{tend_dash}} |
| Throughput (req/s) | {{target_thr}} | — | — | {{peak_thr}} | {{tend_thr}} |
| Error rate | {{target_err}} | — | — | {{actual_err}} | {{tend_err}} |

---

#### 4. Incidentes do Período

| ID | Data | Severidade | Duração | Serviço | Impacto | Causa Raiz | Postmortem? |
|----|------|-----------|---------|---------|---------|-----------|------------|
| {{inc_1}} | {{data_inc_1}} | {{sev_1}} | {{dur_1}} | {{serv_1}} | {{imp_1}} | {{causa_1}} | {{pm_1}} |
| {{inc_2}} | {{data_inc_2}} | {{sev_2}} | {{dur_2}} | {{serv_2}} | {{imp_2}} | {{causa_2}} | {{pm_2}} |
| {{inc_3}} | {{data_inc_3}} | {{sev_3}} | {{dur_3}} | {{serv_3}} | {{imp_3}} | {{causa_3}} | {{pm_3}} |

**Total de incidentes:** {{total_incidentes}}
**MTTD (Mean Time to Detect):** {{mttd}}
**MTTR (Mean Time to Recover):** {{mttr}}

---

#### 5. Análise de Incidentes por Categoria

| Categoria | Quantidade | % do Total | Tendência |
|----------|-----------|-----------|-----------|
| Infraestrutura | {{qtd_infra}} | {{pct_infra}} | {{tend_infra}} |
| Código/Deploy | {{qtd_codigo}} | {{pct_codigo}} | {{tend_codigo}} |
| Dependência externa | {{qtd_dep}} | {{pct_dep}} | {{tend_dep}} |
| Configuração | {{qtd_config}} | {{pct_config}} | {{tend_config}} |
| Capacidade | {{qtd_cap}} | {{pct_cap}} | {{tend_cap}} |
| Segurança | {{qtd_seg}} | {{pct_seg}} | {{tend_seg}} |

---

#### 6. Status dos Action Items de Postmortems

| Postmortem | Action Item | Owner | Prazo | Status |
|-----------|-------------|-------|-------|--------|
| {{pm_ref_1}} | {{ai_1}} | {{owner_1}} | {{prazo_1}} | {{status_ai_1}} |
| {{pm_ref_2}} | {{ai_2}} | {{owner_2}} | {{prazo_2}} | {{status_ai_2}} |
| {{pm_ref_3}} | {{ai_3}} | {{owner_3}} | {{prazo_3}} | {{status_ai_3}} |

**Action items concluídos:** {{qtd_concluidos}} / {{qtd_total_ai}}
**Action items atrasados:** {{qtd_atrasados}}

---

#### 7. Infraestrutura e Capacidade

| Recurso | Uso Atual | Capacidade | % Utilização | Threshold | Ação |
|---------|----------|-----------|-------------|-----------|------|
| {{recurso_1}} | {{uso_1}} | {{cap_1}} | {{util_1}} | {{thresh_1}} | {{acao_1}} |
| {{recurso_2}} | {{uso_2}} | {{cap_2}} | {{util_2}} | {{thresh_2}} | {{acao_2}} |
| {{recurso_3}} | {{uso_3}} | {{cap_3}} | {{util_3}} | {{thresh_3}} | {{acao_3}} |

---

#### 8. DORA Metrics

| Métrica | Período Anterior | Período Atual | Target | Status |
|---------|-----------------|---------------|--------|--------|
| Deploy Frequency | {{df_ant}} | {{df_atual}} | {{df_target}} | {{df_status}} |
| Lead Time for Changes | {{lt_ant}} | {{lt_atual}} | {{lt_target}} | {{lt_status}} |
| Change Failure Rate | {{cfr_ant}} | {{cfr_atual}} | {{cfr_target}} | {{cfr_status}} |
| MTTR | {{mttr_ant}} | {{mttr_atual}} | {{mttr_target}} | {{mttr_status}} |

---

#### 9. Investimentos Recomendados

| Investimento | Justificativa | Impacto Esperado | Esforço | Prioridade |
|-------------|--------------|-----------------|---------|-----------|
| {{invest_1}} | {{just_1}} | {{impacto_1}} | {{esforco_1}} | {{prior_1}} |
| {{invest_2}} | {{just_2}} | {{impacto_2}} | {{esforco_2}} | {{prior_2}} |
| {{invest_3}} | {{just_3}} | {{impacto_3}} | {{esforco_3}} | {{prior_3}} |

---

## Instruções de Preenchimento

1. **SLOs:** Defina SLOs baseados na experiência do usuário, não em métricas internas.
2. **Error Budget:** Quando esgotado, a política deve ser congelar deploys até recuperar.
3. **Incidentes:** Classifique por severidade consistentemente (P0=downtime total, P1=degradação major).
4. **Postmortems:** Todo P0/P1 deve ter postmortem blameless em até 5 dias úteis.
5. **DORA Metrics:** Compare com benchmarks da indústria (Elite/High/Medium/Low performers).
6. **Tendências:** Mais importante que números absolutos. Indique direção de 3+ períodos.

## Exemplo Preenchido

---

### RELATÓRIO DE RELIABILITY — Fevereiro 2026

**Uptime:** 99.92% (target: 99.95%)
**Incidentes P0/P1:** 2 (1 P0, 1 P1)
**Error budget restante:** 38% (consumido 62% do budget mensal)

#### 4. Incidentes
| ID | Sev | Duração | Serviço | Causa |
|----|-----|---------|---------|-------|
| INC-347 | P0 | 47 min | Payment API | Deploy com breaking change em schema |
| INC-351 | P1 | 23 min | Dashboard | Memory leak após update de dependência |

**MTTD:** 4 min (target: <5 min)
**MTTR:** 35 min (target: <30 min)

---

## Checklist de Qualidade

- [ ] SLOs definidos e medidos para todos os serviços críticos
- [ ] Error budget calculado e monitorado
- [ ] Todos os incidentes P0/P1 possuem postmortem
- [ ] Action items de postmortems têm tracking de progresso
- [ ] DORA metrics calculadas e comparadas com benchmarks
- [ ] Capacidade de infraestrutura monitorada
- [ ] Tendências de 3+ períodos documentadas
- [ ] Investimentos recomendados com justificativa de ROI
- [ ] Relatório distribuído a todos os stakeholders relevantes
- [ ] MTTD e MTTR calculados com dados reais
