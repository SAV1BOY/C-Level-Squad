# Plano de Avaliação de AI (Eval Plan)

## Propósito
Definir a metodologia de avaliação de modelos e sistemas de AI, incluindo métricas,
datasets de avaliação, critérios de aceitação e processos de validação, garantindo
que modelos em produção atendam padrões de qualidade e segurança.

## Quando Usar
- Antes de colocar qualquer modelo de AI/ML em produção
- Para avaliações periódicas de modelos já em produção
- Ao comparar modelos candidatos (model selection)
- Para auditorias de fairness e performance
- Quando há degradação suspeita de modelo (model drift)

## Agente Responsável
- **Autor primário:** AI/ML Agent ou CTO Agent
- **Contribuidores:** Data Scientists, ML Engineers
- **Revisor:** CISO Agent (segurança e fairness)
- **Aprovador:** CTO Agent

## Template

---

### PLANO DE AVALIAÇÃO DE AI

**Modelo/Sistema:** {{nome_modelo}}
**Versão:** {{versao_modelo}}
**Data:** {{data}}
**Autor:** {{autor}}
**Tipo de avaliação:** {{pre_producao_periodica_auditoria_comparativa}}

---

#### 1. Escopo da Avaliação

**O que está sendo avaliado:**
{{descricao_modelo_sistema}}

**Objetivo do modelo:**
{{objetivo_modelo}}

**Usuários do modelo:**
{{usuarios_modelo}}

**Decisões influenciadas pelo modelo:**
{{decisoes_influenciadas}}

---

#### 2. Métricas de Avaliação

**Métricas de performance:**
| Métrica | Definição | Threshold Mínimo | Target | Peso |
|---------|-----------|-----------------|--------|------|
| {{metrica_perf_1}} | {{def_1}} | {{threshold_1}} | {{target_1}} | {{peso_1}} |
| {{metrica_perf_2}} | {{def_2}} | {{threshold_2}} | {{target_2}} | {{peso_2}} |
| {{metrica_perf_3}} | {{def_3}} | {{threshold_3}} | {{target_3}} | {{peso_3}} |

**Métricas de fairness:**
| Métrica | Definição | Threshold | Grupos Avaliados |
|---------|-----------|-----------|-----------------|
| {{metrica_fair_1}} | {{def_fair_1}} | {{threshold_fair_1}} | {{grupos_1}} |
| {{metrica_fair_2}} | {{def_fair_2}} | {{threshold_fair_2}} | {{grupos_2}} |

**Métricas operacionais:**
| Métrica | Definição | Threshold |
|---------|-----------|-----------|
| Latência (p50/p95/p99) | {{def_latencia}} | {{threshold_latencia}} |
| Throughput | {{def_throughput}} | {{threshold_throughput}} |
| Custo por inferência | {{def_custo}} | {{threshold_custo}} |
| Taxa de erro/timeout | {{def_erro}} | {{threshold_erro}} |

---

#### 3. Datasets de Avaliação

| Dataset | Propósito | Tamanho | Fonte | Representatividade | Atualização |
|---------|----------|---------|-------|--------------------|------------|
| {{dataset_1}} | {{prop_1}} | {{tam_1}} | {{fonte_1}} | {{repr_1}} | {{atual_1}} |
| {{dataset_2}} | {{prop_2}} | {{tam_2}} | {{fonte_2}} | {{repr_2}} | {{atual_2}} |
| {{dataset_3}} | {{prop_3}} | {{tam_3}} | {{fonte_3}} | {{repr_3}} | {{atual_3}} |

**Golden dataset (benchmark imutável):**
- Nome: {{nome_golden}}
- Tamanho: {{tamanho_golden}}
- Curadoria: {{processo_curadoria}}
- Última validação: {{data_validacao_golden}}

---

#### 4. Metodologia de Avaliação

**Abordagem:**
{{abordagem_avaliacao}}

**Técnicas utilizadas:**
- [ ] Hold-out test set
- [ ] Cross-validation (k={{k_folds}})
- [ ] A/B testing
- [ ] Shadow deployment
- [ ] Human evaluation
- [ ] Red teaming
- [ ] Backtesting
- [ ] {{tecnica_adicional}}

**Comparação com baseline:**
| Modelo | Descrição | Métrica Principal | Score |
|--------|-----------|-------------------|-------|
| Baseline (regras) | {{desc_baseline}} | {{metrica_base}} | {{score_baseline}} |
| Modelo anterior | {{desc_anterior}} | {{metrica_base}} | {{score_anterior}} |
| Modelo candidato | {{desc_candidato}} | {{metrica_base}} | {{score_candidato}} |

---

#### 5. Avaliação de Segurança e Robustez

| Teste | Descrição | Resultado Esperado | Status |
|-------|----------|-------------------|--------|
| Adversarial inputs | {{desc_adversarial}} | {{resultado_adversarial}} | {{status_adversarial}} |
| Edge cases | {{desc_edge}} | {{resultado_edge}} | {{status_edge}} |
| Out-of-distribution | {{desc_ood}} | {{resultado_ood}} | {{status_ood}} |
| Data poisoning | {{desc_poison}} | {{resultado_poison}} | {{status_poison}} |
| Prompt injection (se LLM) | {{desc_prompt}} | {{resultado_prompt}} | {{status_prompt}} |

---

#### 6. Avaliação Humana (se aplicável)

**Avaliadores:** {{quantidade_avaliadores}}
**Perfil:** {{perfil_avaliadores}}
**Amostra avaliada:** {{tamanho_amostra_humana}}

| Critério | Escala | Score Médio | Inter-rater Agreement |
|----------|--------|------------|----------------------|
| {{criterio_humano_1}} | {{escala_1}} | {{score_h1}} | {{agreement_1}} |
| {{criterio_humano_2}} | {{escala_2}} | {{score_h2}} | {{agreement_2}} |
| {{criterio_humano_3}} | {{escala_3}} | {{score_h3}} | {{agreement_3}} |

---

#### 7. Critérios de Go/No-Go

| Critério | Threshold | Resultado | Pass/Fail |
|----------|-----------|-----------|-----------|
| {{criterio_go_1}} | {{threshold_go_1}} | {{resultado_go_1}} | {{pass_fail_1}} |
| {{criterio_go_2}} | {{threshold_go_2}} | {{resultado_go_2}} | {{pass_fail_2}} |
| {{criterio_go_3}} | {{threshold_go_3}} | {{resultado_go_3}} | {{pass_fail_3}} |
| {{criterio_go_4}} | {{threshold_go_4}} | {{resultado_go_4}} | {{pass_fail_4}} |
| {{criterio_go_5}} | {{threshold_go_5}} | {{resultado_go_5}} | {{pass_fail_5}} |

**Resultado geral:** {{go_nogo}}
**Condições (se Go condicional):** {{condicoes_go}}

---

#### 8. Monitoramento Pós-Deploy

| Métrica | Frequência | Threshold de Alerta | Ação se Threshold Violado |
|---------|-----------|--------------------|--------------------------|
| {{monitor_1}} | {{freq_1}} | {{alert_1}} | {{acao_alert_1}} |
| {{monitor_2}} | {{freq_2}} | {{alert_2}} | {{acao_alert_2}} |
| {{monitor_3}} | {{freq_3}} | {{alert_3}} | {{acao_alert_3}} |

**Política de re-treinamento:** {{politica_retrain}}
**Rollback automático:** {{condicao_rollback}}

---

## Instruções de Preenchimento

1. **Métricas:** Defina métricas de negócio E técnicas. Accuracy sozinha não é suficiente.
2. **Fairness:** Obrigatório para modelos que afetam pessoas. Avalie por grupos protegidos.
3. **Golden dataset:** Mantenha um dataset imutável de benchmark. Não o use para treinamento.
4. **Baseline:** Sempre compare com a solução atual (regras, heurísticas, modelo anterior).
5. **Segurança:** Para LLMs, teste prompt injection e jailbreaking obrigatoriamente.
6. **Go/No-Go:** Todos os critérios devem passar. Um "Fail" bloqueia o deploy.
7. **Monitoramento:** Defina antes do deploy. Model drift é inevitável.

## Exemplo Preenchido

---

### EVAL PLAN — Modelo de Classificação de Tickets v3

**Métricas de performance:**
| Métrica | Threshold | Target | Score |
|---------|-----------|--------|-------|
| Macro F1 | > 0.80 | 0.88 | 0.86 |
| Precision (auto-route) | > 0.90 | 0.95 | 0.93 |
| Recall | > 0.75 | 0.85 | 0.82 |

**Go/No-Go:** GO (todos os thresholds atingidos)

---

## Checklist de Qualidade

- [ ] Métricas de performance, fairness e operacionais definidas
- [ ] Datasets de avaliação representativos e documentados
- [ ] Golden dataset mantido separadamente do treinamento
- [ ] Baseline de comparação definida
- [ ] Testes de segurança e robustez planejados
- [ ] Avaliação humana incluída (quando aplicável)
- [ ] Critérios de Go/No-Go são binários e não negociáveis
- [ ] Monitoramento pós-deploy configurado
- [ ] Política de rollback definida
- [ ] CISO Agent revisou aspectos de fairness e segurança
