# Card de Saúde de Iniciativa (Traffic Light)

## Propósito
Fornecer uma visão rápida e visual do estado de saúde de cada iniciativa estratégica
em andamento, usando o sistema de semáforo (verde/amarelo/vermelho) para comunicar
status, riscos e necessidade de intervenção ao C-Level.

## Quando Usar
- Semanalmente como parte do WBR (visão de portfólio)
- Quinzenalmente para revisão detalhada de cada iniciativa
- Quando uma iniciativa muda de status (especialmente para amarelo ou vermelho)
- Como ferramenta de comunicação visual para o Board

## Agente Responsável
- **Mantenedor:** Chief of Staff Agent (CoS)
- **Atualização:** Owner de cada iniciativa
- **Revisão:** CEO Agent
- **Frequência:** Semanal

## Template

---

### HEALTH CARD — {{nome_iniciativa}}

**ID:** {{id_iniciativa}}
**Owner:** {{owner}}
**Sponsor:** {{sponsor}}
**Data de início:** {{data_inicio}}
**Data prevista de conclusão:** {{data_conclusao}}
**Budget aprovado:** {{budget_aprovado}}
**Última atualização:** {{data_atualizacao}}

---

#### Status Geral: {{verde_amarelo_vermelho}}

| Dimensão | Status | Comentário |
|----------|--------|-----------|
| Escopo | {{status_escopo}} | {{coment_escopo}} |
| Timeline | {{status_timeline}} | {{coment_timeline}} |
| Budget | {{status_budget}} | {{coment_budget}} |
| Qualidade | {{status_qualidade}} | {{coment_qualidade}} |
| Riscos | {{status_riscos}} | {{coment_riscos}} |
| Equipe | {{status_equipe}} | {{coment_equipe}} |

**Legenda:** Verde = no plano | Amarelo = em risco (ação necessária) | Vermelho = fora do plano (escalação)

---

#### Progresso

**% Completo:** {{percentual_completo}}
**Milestone atual:** {{milestone_atual}}
**Próximo milestone:** {{proximo_milestone}} ({{data_proximo_milestone}})

| Milestone | Planejado | Realizado | Status |
|-----------|----------|-----------|--------|
| {{milestone_1}} | {{plan_1}} | {{real_1}} | {{status_m1}} |
| {{milestone_2}} | {{plan_2}} | {{real_2}} | {{status_m2}} |
| {{milestone_3}} | {{plan_3}} | {{real_3}} | {{status_m3}} |
| {{milestone_4}} | {{plan_4}} | {{real_4}} | {{status_m4}} |
| {{milestone_5}} | {{plan_5}} | {{real_5}} | {{status_m5}} |

---

#### Métricas-Chave

| Métrica | Target | Atual | Tendência | Status |
|---------|--------|-------|-----------|--------|
| {{metrica_1}} | {{target_1}} | {{atual_1}} | {{tend_1}} | {{status_met_1}} |
| {{metrica_2}} | {{target_2}} | {{atual_2}} | {{tend_2}} | {{status_met_2}} |
| {{metrica_3}} | {{target_3}} | {{atual_3}} | {{tend_3}} | {{status_met_3}} |

---

#### Budget Tracking

| Item | Budget | Realizado | Comprometido | Disponível |
|------|--------|-----------|-------------|-----------|
| {{item_budget_1}} | {{budget_1}} | {{real_b1}} | {{comprom_1}} | {{disp_1}} |
| {{item_budget_2}} | {{budget_2}} | {{real_b2}} | {{comprom_2}} | {{disp_2}} |
| {{item_budget_3}} | {{budget_3}} | {{real_b3}} | {{comprom_3}} | {{disp_3}} |
| **Total** | **{{budget_total}}** | **{{real_total}}** | **{{comprom_total}}** | **{{disp_total}}** |

**Burn rate:** {{burn_rate_atual}} vs. {{burn_rate_planejado}} planejado

---

#### Riscos e Bloqueios

| # | Risco/Bloqueio | Tipo | Impacto | Mitigação | Owner | Status |
|---|---------------|------|---------|-----------|-------|--------|
| 1 | {{risco_1}} | {{tipo_1}} | {{impacto_1}} | {{mit_1}} | {{owner_r1}} | {{status_r1}} |
| 2 | {{risco_2}} | {{tipo_2}} | {{impacto_2}} | {{mit_2}} | {{owner_r2}} | {{status_r2}} |
| 3 | {{risco_3}} | {{tipo_3}} | {{impacto_3}} | {{mit_3}} | {{owner_r3}} | {{status_r3}} |

---

#### Decisões Necessárias

| # | Decisão | Contexto | Deadline | Decisor |
|---|---------|----------|---------|---------|
| 1 | {{decisao_1}} | {{contexto_1}} | {{deadline_1}} | {{decisor_1}} |
| 2 | {{decisao_2}} | {{contexto_2}} | {{deadline_2}} | {{decisor_2}} |

---

#### Dependências

| Dependência | De Quem | Status | Impacto se Atrasar |
|-------------|---------|--------|-------------------|
| {{dep_1}} | {{de_quem_1}} | {{status_dep_1}} | {{impacto_dep_1}} |
| {{dep_2}} | {{de_quem_2}} | {{status_dep_2}} | {{impacto_dep_2}} |

---

#### Resumo da Semana

**O que avançou:**
- {{avanco_1}}
- {{avanco_2}}

**O que está travado:**
- {{travado_1}}

**Plano para a próxima semana:**
- {{plano_prox_1}}
- {{plano_prox_2}}

---

#### Histórico de Status

| Data | Status | Mudança | Razão |
|------|--------|---------|-------|
| {{data_hist_1}} | {{status_hist_1}} | — | Início |
| {{data_hist_2}} | {{status_hist_2}} | {{mudanca_2}} | {{razao_2}} |
| {{data_hist_3}} | {{status_hist_3}} | {{mudanca_3}} | {{razao_3}} |

---

## Instruções de Preenchimento

1. **Status geral:** É o PIOR status entre as 6 dimensões. Se uma dimensão é vermelha, o status geral é vermelho.
2. **Cores:** Verde = dentro de 10% do plano. Amarelo = 10-25% de desvio. Vermelho = >25% de desvio.
3. **Escalação:** Vermelho requer ação do CEO/Sponsor na mesma semana.
4. **Honestidade:** Nunca pinte de verde algo que é amarelo. Otimismo falso custa mais caro depois.
5. **Frequência:** Atualize semanalmente, mesmo que nada tenha mudado (confirma que está monitorando).
6. **Histórico:** Registre todas as mudanças de status com razão.

## Exemplo Preenchido

---

### HEALTH CARD — PLG Self-Service Launch

**Status Geral:** AMARELO
**Owner:** CMO Agent | **Budget:** R$ 2M | **% Completo:** 65%

| Dimensão | Status | Comentário |
|----------|--------|-----------|
| Escopo | Verde | Sem mudanças |
| Timeline | Amarelo | 2 semanas de atraso no módulo de onboarding |
| Budget | Verde | 62% do budget consumido para 65% de progresso |
| Qualidade | Verde | NPS beta = 78 (target: 70) |
| Riscos | Amarelo | Dependência de redesign do checkout não resolvida |
| Equipe | Verde | Equipe completa e engajada |

---

## Checklist de Qualidade

- [ ] Status geral reflete o pior status entre as dimensões
- [ ] Todas as 6 dimensões estão avaliadas
- [ ] Milestones estão com datas planejadas e realizadas
- [ ] Budget tracking inclui comprometido e disponível
- [ ] Riscos e bloqueios estão atualizados
- [ ] Decisões necessárias têm deadline e decisor
- [ ] Dependências externas estão mapeadas
- [ ] Resumo da semana é honesto e conciso
- [ ] Histórico de status está registrado
- [ ] Atualizado nos últimos 7 dias
