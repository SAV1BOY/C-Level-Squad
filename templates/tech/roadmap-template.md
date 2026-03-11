# Template de Roadmap Técnico

## Propósito
Comunicar o plano de desenvolvimento técnico com foco em outcomes (não features),
mapeando dependências, capacidade necessária e critérios de priorização para
alinhar engineering com objetivos de negócio.

## Quando Usar
- No planejamento trimestral de engineering/produto
- Para comunicar prioridades técnicas ao C-Level e ao Board
- Quando há necessidade de renegociar escopo ou timeline
- Como ferramenta de alinhamento entre squads e stakeholders

## Agente Responsável
- **Autor primário:** CTO Agent + CPO Agent
- **Contribuidores:** Tech Leads, Engineering Managers
- **Revisor:** CEO Agent, CFO Agent (investimento)
- **Aprovador:** CTO Agent + CEO Agent

## Template

---

### ROADMAP TÉCNICO — {{periodo}}

**Data de atualização:** {{data}}
**Autor:** {{autor}}
**Horizonte:** {{horizonte_temporal}}
**Versão:** {{versao}}

---

#### 1. Visão Técnica

> {{visao_tecnica_2_frases}}

**Princípios de priorização:**
1. {{principio_1}}
2. {{principio_2}}
3. {{principio_3}}

---

#### 2. Capacidade Disponível

| Squad/Time | Engenheiros | Sprints no Período | Capacidade (story points) | Alocação |
|-----------|-------------|-------------------|--------------------------|----------|
| {{squad_1}} | {{eng_1}} | {{sprints_1}} | {{capacidade_1}} | {{alocacao_1}} |
| {{squad_2}} | {{eng_2}} | {{sprints_2}} | {{capacidade_2}} | {{alocacao_2}} |
| {{squad_3}} | {{eng_3}} | {{sprints_3}} | {{capacidade_3}} | {{alocacao_3}} |
| {{squad_4}} | {{eng_4}} | {{sprints_4}} | {{capacidade_4}} | {{alocacao_4}} |
| **Total** | **{{eng_total}}** | — | **{{capacidade_total}}** | — |

**Alocação-alvo:**
| Tipo de Trabalho | % Alocação | Justificativa |
|-----------------|-----------|---------------|
| Novas features (product) | {{pct_features}} | {{just_features}} |
| Tech debt | {{pct_techdebt}} | {{just_techdebt}} |
| Reliability/Infrastructure | {{pct_reliability}} | {{just_reliability}} |
| Suporte/Bug fixes | {{pct_bugs}} | {{just_bugs}} |

---

#### 3. Outcomes Planejados

| # | Outcome | Métrica | Baseline | Meta | Squad | Quarter |
|---|---------|---------|----------|------|-------|---------|
| O1 | {{outcome_1}} | {{metrica_1}} | {{baseline_1}} | {{meta_1}} | {{squad_o1}} | {{quarter_1}} |
| O2 | {{outcome_2}} | {{metrica_2}} | {{baseline_2}} | {{meta_2}} | {{squad_o2}} | {{quarter_2}} |
| O3 | {{outcome_3}} | {{metrica_3}} | {{baseline_3}} | {{meta_3}} | {{squad_o3}} | {{quarter_3}} |
| O4 | {{outcome_4}} | {{metrica_4}} | {{baseline_4}} | {{meta_4}} | {{squad_o4}} | {{quarter_4}} |
| O5 | {{outcome_5}} | {{metrica_5}} | {{baseline_5}} | {{meta_5}} | {{squad_o5}} | {{quarter_5}} |

---

#### 4. Roadmap por Horizonte

**Now (Este Quarter):** Alta confiança, comprometido
| Item | Outcome | Squad | Estimativa | Status | Dependência |
|------|---------|-------|-----------|--------|-------------|
| {{item_now_1}} | {{outcome_now_1}} | {{squad_now_1}} | {{est_now_1}} | {{status_now_1}} | {{dep_now_1}} |
| {{item_now_2}} | {{outcome_now_2}} | {{squad_now_2}} | {{est_now_2}} | {{status_now_2}} | {{dep_now_2}} |
| {{item_now_3}} | {{outcome_now_3}} | {{squad_now_3}} | {{est_now_3}} | {{status_now_3}} | {{dep_now_3}} |

**Next (Próximo Quarter):** Média confiança, planejado
| Item | Outcome | Squad | Estimativa | Dependência |
|------|---------|-------|-----------|-------------|
| {{item_next_1}} | {{outcome_next_1}} | {{squad_next_1}} | {{est_next_1}} | {{dep_next_1}} |
| {{item_next_2}} | {{outcome_next_2}} | {{squad_next_2}} | {{est_next_2}} | {{dep_next_2}} |

**Later (2+ Quarters):** Baixa confiança, exploratório
| Item | Outcome | Conceito | Investigação Necessária |
|------|---------|---------|------------------------|
| {{item_later_1}} | {{outcome_later_1}} | {{conceito_1}} | {{investigacao_1}} |
| {{item_later_2}} | {{outcome_later_2}} | {{conceito_2}} | {{investigacao_2}} |

---

#### 5. Mapa de Dependências

| Item | Depende de | Tipo | Status | Risco se Atrasar |
|------|-----------|------|--------|-----------------|
| {{item_dep_1}} | {{dep_de_1}} | {{tipo_dep_1}} | {{status_dep_1}} | {{risco_dep_1}} |
| {{item_dep_2}} | {{dep_de_2}} | {{tipo_dep_2}} | {{status_dep_2}} | {{risco_dep_2}} |
| {{item_dep_3}} | {{dep_de_3}} | {{tipo_dep_3}} | {{status_dep_3}} | {{risco_dep_3}} |

**Tipos de dependência:** Técnica | Cross-squad | Externa (vendor) | Dados | Regulatória

---

#### 6. Riscos Técnicos

| Risco | Probabilidade | Impacto | Mitigação | Owner |
|-------|--------------|---------|-----------|-------|
| {{risco_tech_1}} | {{prob_1}} | {{imp_1}} | {{mit_1}} | {{owner_1}} |
| {{risco_tech_2}} | {{prob_2}} | {{imp_2}} | {{mit_2}} | {{owner_2}} |
| {{risco_tech_3}} | {{prob_3}} | {{imp_3}} | {{mit_3}} | {{owner_3}} |

---

#### 7. Investimento em Plataforma

| Investimento | Justificativa | Esforço | Benefício Esperado | Quarter |
|-------------|--------------|---------|-------------------|---------|
| {{invest_1}} | {{just_1}} | {{esforco_1}} | {{beneficio_1}} | {{quarter_i1}} |
| {{invest_2}} | {{just_2}} | {{esforco_2}} | {{beneficio_2}} | {{quarter_i2}} |

---

#### 8. Não Faremos (Backlog Consciente)

| Item | Por que não agora | Quando reconsiderar |
|------|------------------|---------------------|
| {{nao_faremos_1}} | {{razao_1}} | {{reconsiderar_1}} |
| {{nao_faremos_2}} | {{razao_2}} | {{reconsiderar_2}} |
| {{nao_faremos_3}} | {{razao_3}} | {{reconsiderar_3}} |

---

## Instruções de Preenchimento

1. **Outcomes, não features:** O roadmap comunica "o que queremos alcançar", não "o que vamos construir".
2. **Now/Next/Later:** Diminua o nível de detalhe conforme o horizonte aumenta.
3. **Capacidade:** Seja honesto. Não prometa 100% de alocação — reserve 20-30% para imprevistos.
4. **Dependências:** Mapeie cross-squad e externas. São a maior causa de atrasos.
5. **Não Faremos:** Tão importante quanto o roadmap. Comunica o que conscientemente não será feito.
6. **Atualização:** Roadmap é um documento vivo. Atualize pelo menos quinzenalmente.

## Exemplo Preenchido

---

### ROADMAP TÉCNICO — Q2 2026

**Visão:** Evoluir a plataforma para suportar 10x o volume atual mantendo p99 latency < 200ms
e atingir deploy diário em todos os squads.

**Now:**
| Item | Outcome | Squad | Estimativa |
|------|---------|-------|-----------|
| API Gateway v2 | Reduzir p99 latency de 450ms para 200ms | Platform | 6 semanas |
| Feature flags infra | Deploy diário sem risco | DevEx | 4 semanas |
| Payment service extraction | Deploy independente de payments | Payments | 8 semanas |

---

## Checklist de Qualidade

- [ ] Roadmap focado em outcomes (não lista de features)
- [ ] Capacidade realista e documentada
- [ ] Alocação entre features/tech-debt/reliability explícita
- [ ] Now/Next/Later com nível de confiança adequado
- [ ] Dependências mapeadas com riscos
- [ ] "Não faremos" documentado
- [ ] Investimentos em plataforma justificados
- [ ] Riscos técnicos com mitigações
- [ ] Alinhado com a estratégia de negócio
- [ ] Atualizado nos últimos 15 dias
