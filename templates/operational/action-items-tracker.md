# Template de Rastreamento de Action Items

## Propósito
Centralizar o tracking de todos os action items gerados em reuniões, revisões e
decisões do C-Level Squad, garantindo accountability, visibilidade de progresso
e resolução tempestiva de pendências.

## Quando Usar
- Como registro contínuo atualizado após cada WBR, MBR e QBR
- Para acompanhar ações derivadas de decisões executivas
- Como ferramenta de accountability semanal
- Para identificar padrões de atraso e bloqueios recorrentes

## Agente Responsável
- **Mantenedor:** Chief of Staff Agent (CoS)
- **Contribuidores:** Todos os agentes C-Level
- **Revisão:** Semanal no WBR
- **Escalação:** CEO Agent (para itens atrasados > 2 semanas)

## Template

---

### TRACKER DE ACTION ITEMS — {{data_atualizacao}}

**Última atualização:** {{data_atualizacao}}
**Mantenedor:** {{mantenedor}}
**Total de itens ativos:** {{total_ativos}}
**Itens concluídos no período:** {{total_concluidos}}
**Itens atrasados:** {{total_atrasados}}

---

#### 1. Resumo de Saúde

| Status | Quantidade | % do Total |
|--------|-----------|-----------|
| No prazo (verde) | {{qtd_verde}} | {{pct_verde}} |
| Em risco (amarelo) | {{qtd_amarelo}} | {{pct_amarelo}} |
| Atrasado (vermelho) | {{qtd_vermelho}} | {{pct_vermelho}} |
| Concluído | {{qtd_concluido}} | {{pct_concluido}} |
| Cancelado | {{qtd_cancelado}} | {{pct_cancelado}} |

**Taxa de conclusão no prazo:** {{taxa_conclusao}}
**Tempo médio de resolução:** {{tempo_medio_resolucao}}

---

#### 2. Action Items Ativos

| ID | Ação | Owner | Origem | Data Criação | Prazo | Prioridade | Status | Notas |
|----|------|-------|--------|-------------|-------|-----------|--------|-------|
| AI-{{id_1}} | {{acao_1}} | {{owner_1}} | {{origem_1}} | {{criacao_1}} | {{prazo_1}} | {{prior_1}} | {{status_1}} | {{notas_1}} |
| AI-{{id_2}} | {{acao_2}} | {{owner_2}} | {{origem_2}} | {{criacao_2}} | {{prazo_2}} | {{prior_2}} | {{status_2}} | {{notas_2}} |
| AI-{{id_3}} | {{acao_3}} | {{owner_3}} | {{origem_3}} | {{criacao_3}} | {{prazo_3}} | {{prior_3}} | {{status_3}} | {{notas_3}} |
| AI-{{id_4}} | {{acao_4}} | {{owner_4}} | {{origem_4}} | {{criacao_4}} | {{prazo_4}} | {{prior_4}} | {{status_4}} | {{notas_4}} |
| AI-{{id_5}} | {{acao_5}} | {{owner_5}} | {{origem_5}} | {{criacao_5}} | {{prazo_5}} | {{prior_5}} | {{status_5}} | {{notas_5}} |
| AI-{{id_6}} | {{acao_6}} | {{owner_6}} | {{origem_6}} | {{criacao_6}} | {{prazo_6}} | {{prior_6}} | {{status_6}} | {{notas_6}} |
| AI-{{id_7}} | {{acao_7}} | {{owner_7}} | {{origem_7}} | {{criacao_7}} | {{prazo_7}} | {{prior_7}} | {{status_7}} | {{notas_7}} |
| AI-{{id_8}} | {{acao_8}} | {{owner_8}} | {{origem_8}} | {{criacao_8}} | {{prazo_8}} | {{prior_8}} | {{status_8}} | {{notas_8}} |

**Origens:** WBR | MBR | QBR | Decision Memo | Postmortem | Ad-hoc
**Prioridades:** P1 (Urgente) | P2 (Alta) | P3 (Normal) | P4 (Baixa)
**Status:** No Prazo | Em Risco | Atrasado | Concluído | Cancelado | Bloqueado

---

#### 3. Itens Atrasados (Escalação)

| ID | Ação | Owner | Prazo Original | Dias de Atraso | Bloqueio | Ação de Escalação |
|----|------|-------|---------------|---------------|---------|-------------------|
| AI-{{id_atr_1}} | {{acao_atr_1}} | {{owner_atr_1}} | {{prazo_atr_1}} | {{dias_1}} | {{bloqueio_1}} | {{escalacao_1}} |
| AI-{{id_atr_2}} | {{acao_atr_2}} | {{owner_atr_2}} | {{prazo_atr_2}} | {{dias_2}} | {{bloqueio_2}} | {{escalacao_2}} |

**Política de escalação:**
- 1-7 dias atrasado: Owner reporta motivo no WBR
- 8-14 dias atrasado: CoS Agent intervém para desbloqueio
- 15+ dias atrasado: CEO Agent intervém ou item é reavaliado/cancelado

---

#### 4. Itens Concluídos (Período Atual)

| ID | Ação | Owner | Prazo | Concluído Em | No Prazo? |
|----|------|-------|-------|-------------|-----------|
| AI-{{id_conc_1}} | {{acao_conc_1}} | {{owner_conc_1}} | {{prazo_conc_1}} | {{concl_1}} | {{np_1}} |
| AI-{{id_conc_2}} | {{acao_conc_2}} | {{owner_conc_2}} | {{prazo_conc_2}} | {{concl_2}} | {{np_2}} |
| AI-{{id_conc_3}} | {{acao_conc_3}} | {{owner_conc_3}} | {{prazo_conc_3}} | {{concl_3}} | {{np_3}} |

---

#### 5. Métricas de Accountability

| Owner | Ativos | Concluídos no Prazo | Atrasados | Taxa de Conclusão |
|-------|--------|--------------------|-----------|--------------------|
| {{owner_metrica_1}} | {{ativos_1}} | {{concl_prazo_1}} | {{atrasados_1}} | {{taxa_1}} |
| {{owner_metrica_2}} | {{ativos_2}} | {{concl_prazo_2}} | {{atrasados_2}} | {{taxa_2}} |
| {{owner_metrica_3}} | {{ativos_3}} | {{concl_prazo_3}} | {{atrasados_3}} | {{taxa_3}} |
| {{owner_metrica_4}} | {{ativos_4}} | {{concl_prazo_4}} | {{atrasados_4}} | {{taxa_4}} |

---

#### 6. Tendências

| Período | Criados | Concluídos | Saldo | Taxa no Prazo |
|---------|---------|-----------|-------|---------------|
| {{periodo_1}} | {{criados_1}} | {{concluidos_1}} | {{saldo_1}} | {{taxa_prazo_1}} |
| {{periodo_2}} | {{criados_2}} | {{concluidos_2}} | {{saldo_2}} | {{taxa_prazo_2}} |
| {{periodo_3}} | {{criados_3}} | {{concluidos_3}} | {{saldo_3}} | {{taxa_prazo_3}} |
| {{periodo_4}} | {{criados_4}} | {{concluidos_4}} | {{saldo_4}} | {{taxa_prazo_4}} |

---

## Instruções de Preenchimento

1. **ID:** Use sequencial (AI-001, AI-002). Nunca reutilize IDs.
2. **Owner:** Sempre uma pessoa, nunca uma equipe. Se delegado, o owner original mantém accountability.
3. **Prazo:** Data específica, não "em breve" ou "próxima semana".
4. **Origem:** Rastreie de onde veio o action item para avaliar produtividade dos rituais.
5. **Atualização:** O tracker deve ser atualizado antes de cada WBR (no mínimo semanalmente).
6. **Escalação:** Siga a política de escalação rigorosamente. Itens eternamente atrasados
   corroem a credibilidade do sistema.
7. **Cancelamento:** Melhor cancelar formalmente do que deixar atrasado indefinidamente.

## Exemplo Preenchido

---

### TRACKER — Semana 11/2026

**Total ativos:** 18 | **Concluídos esta semana:** 5 | **Atrasados:** 3
**Taxa de conclusão no prazo:** 78%

| ID | Ação | Owner | Prazo | Status |
|----|------|-------|-------|--------|
| AI-042 | Enviar proposta de pricing para CFO | CMO Agent | 2026-03-14 | No Prazo |
| AI-043 | Implementar alerta de latency > 500ms | CTO Agent | 2026-03-12 | Concluído |
| AI-044 | Contratar 2 SDRs para pipeline enterprise | CRO Agent | 2026-03-20 | Em Risco |

---

## Checklist de Qualidade

- [ ] Todos os action items têm ID único
- [ ] Cada item tem owner individual e prazo específico
- [ ] Origem de cada item está registrada
- [ ] Itens atrasados estão na seção de escalação
- [ ] Política de escalação está sendo seguida
- [ ] Métricas de accountability por owner estão calculadas
- [ ] Tendências mostram se o saldo está crescendo ou diminuindo
- [ ] Itens cancelados estão formalmente registrados com razão
- [ ] O tracker foi atualizado antes do WBR
- [ ] Taxa de conclusão no prazo é monitorada como meta (target: >80%)
