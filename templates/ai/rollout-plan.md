# Plano de Rollout de AI (Piloto → Produção)

## Propósito
Definir o plano faseado de implantação de soluções de AI, desde o piloto controlado
até a produção completa, com critérios de progressão, monitoramento e rollback,
minimizando risco e maximizando aprendizado em cada fase.

## Quando Usar
- Após aprovação do AI Use Case Card e conclusão do Eval Plan
- Para qualquer implantação de modelo de AI/ML em produção
- Quando atualizando versão de modelo existente em produção
- Para expansão de solução de AI para novos segmentos/mercados

## Agente Responsável
- **Autor primário:** AI/ML Agent ou CTO Agent
- **Contribuidores:** ML Engineers, Product Owner, Operations
- **Revisor:** CISO Agent, CEO Agent
- **Aprovador:** CTO Agent + CEO Agent

## Template

---

### PLANO DE ROLLOUT DE AI

**Solução:** {{nome_solucao}}
**Versão:** {{versao}}
**Data:** {{data}}
**Autor:** {{autor}}
**Status:** {{planejado_em_piloto_em_expansao_produção_completa}}

---

#### 1. Visão Geral do Rollout

**Solução em uma frase:**
{{descricao_uma_frase}}

**Referências:**
- AI Use Case Card: {{link_use_case_card}}
- Eval Plan: {{link_eval_plan}}
- ADR: {{link_adr}}

**Estratégia de rollout:** {{canary_blue_green_progressive_feature_flag}}

---

#### 2. Fases do Rollout

**Fase 0: Shadow Mode ({{duracao_fase_0}})**
| Aspecto | Detalhes |
|---------|---------|
| Descrição | Modelo roda em paralelo sem afetar produção |
| Cobertura | {{cobertura_fase_0}} |
| Critério de entrada | Eval Plan aprovado (Go) |
| Critério de saída | {{criterio_saida_0}} |
| Métricas monitoradas | {{metricas_fase_0}} |
| Rollback trigger | N/A (não afeta produção) |
| Owner | {{owner_fase_0}} |

**Fase 1: Piloto Controlado ({{duracao_fase_1}})**
| Aspecto | Detalhes |
|---------|---------|
| Descrição | {{descricao_fase_1}} |
| Cobertura | {{cobertura_fase_1}} |
| Usuários/Segmento | {{usuarios_fase_1}} |
| Critério de entrada | Fase 0 aprovada |
| Critério de saída | {{criterio_saida_1}} |
| Métricas monitoradas | {{metricas_fase_1}} |
| Rollback trigger | {{rollback_trigger_1}} |
| Human-in-the-loop | {{hitl_fase_1}} |
| Owner | {{owner_fase_1}} |

**Fase 2: Expansão Gradual ({{duracao_fase_2}})**
| Aspecto | Detalhes |
|---------|---------|
| Descrição | {{descricao_fase_2}} |
| Cobertura | {{cobertura_fase_2}} |
| Ramp-up schedule | {{rampup_schedule}} |
| Critério de entrada | Fase 1 aprovada |
| Critério de saída | {{criterio_saida_2}} |
| Métricas monitoradas | {{metricas_fase_2}} |
| Rollback trigger | {{rollback_trigger_2}} |
| Owner | {{owner_fase_2}} |

**Fase 3: Produção Completa ({{duracao_fase_3}})**
| Aspecto | Detalhes |
|---------|---------|
| Descrição | {{descricao_fase_3}} |
| Cobertura | 100% |
| Critério de entrada | Fase 2 aprovada |
| Monitoramento contínuo | {{monitoramento_fase_3}} |
| Cadência de review | {{cadencia_review}} |
| Owner | {{owner_fase_3}} |

---

#### 3. Critérios de Progressão entre Fases

| Da Fase | Para Fase | Critério | Threshold | Quem Decide |
|---------|----------|----------|-----------|-------------|
| 0 → 1 | Shadow → Piloto | {{criterio_0_1}} | {{threshold_0_1}} | {{decisor_0_1}} |
| 1 → 2 | Piloto → Expansão | {{criterio_1_2}} | {{threshold_1_2}} | {{decisor_1_2}} |
| 2 → 3 | Expansão → Full | {{criterio_2_3}} | {{threshold_2_3}} | {{decisor_2_3}} |

**Critérios de STOP (qualquer fase):**
- {{stop_criterio_1}}
- {{stop_criterio_2}}
- {{stop_criterio_3}}

---

#### 4. Infraestrutura e Dependências

| Componente | Status | Owner | Fase Necessária |
|-----------|--------|-------|----------------|
| {{componente_1}} | {{status_1}} | {{owner_1}} | {{fase_necessaria_1}} |
| {{componente_2}} | {{status_2}} | {{owner_2}} | {{fase_necessaria_2}} |
| {{componente_3}} | {{status_3}} | {{owner_3}} | {{fase_necessaria_3}} |
| {{componente_4}} | {{status_4}} | {{owner_4}} | {{fase_necessaria_4}} |

---

#### 5. Plano de Rollback

| Cenário | Trigger | Ação de Rollback | Tempo Estimado | Responsável |
|---------|---------|-----------------|---------------|-------------|
| {{cenario_rb_1}} | {{trigger_rb_1}} | {{acao_rb_1}} | {{tempo_rb_1}} | {{resp_rb_1}} |
| {{cenario_rb_2}} | {{trigger_rb_2}} | {{acao_rb_2}} | {{tempo_rb_2}} | {{resp_rb_2}} |
| {{cenario_rb_3}} | {{trigger_rb_3}} | {{acao_rb_3}} | {{tempo_rb_3}} | {{resp_rb_3}} |

**Fallback durante rollback:** {{descricao_fallback}}

---

#### 6. Comunicação e Change Management

| Fase | Audiência | Mensagem | Canal | Quando |
|------|-----------|---------|-------|--------|
| Pré-piloto | {{aud_pre}} | {{msg_pre}} | {{canal_pre}} | {{quando_pre}} |
| Piloto | {{aud_piloto}} | {{msg_piloto}} | {{canal_piloto}} | {{quando_piloto}} |
| Expansão | {{aud_expansao}} | {{msg_expansao}} | {{canal_expansao}} | {{quando_expansao}} |
| Full production | {{aud_full}} | {{msg_full}} | {{canal_full}} | {{quando_full}} |

**Treinamento necessário:**
| Audiência | Conteúdo | Formato | Duração | Quando |
|-----------|---------|---------|---------|--------|
| {{aud_treino_1}} | {{conteudo_1}} | {{formato_1}} | {{duracao_1}} | {{quando_treino_1}} |
| {{aud_treino_2}} | {{conteudo_2}} | {{formato_2}} | {{duracao_2}} | {{quando_treino_2}} |

---

#### 7. Monitoramento e Alertas

| Métrica | Threshold Normal | Threshold de Alerta | Threshold Crítico | Ação |
|---------|-----------------|--------------------|--------------------|------|
| {{metric_mon_1}} | {{normal_1}} | {{alerta_1}} | {{critico_1}} | {{acao_mon_1}} |
| {{metric_mon_2}} | {{normal_2}} | {{alerta_2}} | {{critico_2}} | {{acao_mon_2}} |
| {{metric_mon_3}} | {{normal_3}} | {{alerta_3}} | {{critico_3}} | {{acao_mon_3}} |

**Dashboard de monitoramento:** {{link_dashboard}}
**On-call responsável:** {{oncall}}

---

#### 8. Timeline Consolidado

| Marco | Data | Owner | Dependência |
|-------|------|-------|-------------|
| Fase 0 início | {{data_f0_inicio}} | {{owner_f0}} | Eval Plan aprovado |
| Fase 0 → Fase 1 gate | {{data_gate_1}} | {{decisor_gate_1}} | Critérios Fase 0 |
| Fase 1 início | {{data_f1_inicio}} | {{owner_f1}} | Gate 1 aprovado |
| Fase 1 → Fase 2 gate | {{data_gate_2}} | {{decisor_gate_2}} | Critérios Fase 1 |
| Fase 2 início | {{data_f2_inicio}} | {{owner_f2}} | Gate 2 aprovado |
| Fase 2 → Fase 3 gate | {{data_gate_3}} | {{decisor_gate_3}} | Critérios Fase 2 |
| Full production | {{data_full}} | {{owner_full}} | Gate 3 aprovado |

---

## Instruções de Preenchimento

1. **Fases:** Nunca pule fases. Shadow mode é obrigatório para validar sem risco.
2. **Critérios de progressão:** Devem ser quantitativos e não negociáveis.
3. **Rollback:** Teste o rollback ANTES do piloto. Rollback não testado = não existe.
4. **Ramp-up:** Na expansão, use incrementos graduais (10% → 25% → 50% → 100%).
5. **Monitoramento:** Configure alertas ANTES do início de cada fase.
6. **Change management:** Não subestime. Pessoas resistem a mudanças, especialmente AI.

## Exemplo Preenchido

---

### ROLLOUT — Classificador Automático de Tickets

| Fase | Cobertura | Duração | Critério de Saída |
|------|-----------|---------|-------------------|
| 0 — Shadow | 100% (sem ação) | 2 semanas | Accuracy > 85% vs. humanos |
| 1 — Piloto | 10% (1 equipe) | 4 semanas | F1 > 0.83, CSAT sem degradação |
| 2 — Expansão | 10→25→50% | 6 semanas | Métricas mantidas em cada step |
| 3 — Full | 100% | Contínuo | Review mensal |

**Rollback trigger:** CSAT cai > 5 pontos OU F1 < 0.78 por 3 dias consecutivos.

---

## Checklist de Qualidade

- [ ] Shadow mode planejado antes do piloto
- [ ] Critérios de progressão são quantitativos e acordados
- [ ] Rollback plan testado antes do início
- [ ] Infraestrutura pronta para cada fase
- [ ] Monitoramento e alertas configurados
- [ ] Comunicação planejada para cada fase e audiência
- [ ] Treinamento definido para usuários afetados
- [ ] Feature flags configuradas para controle granular
- [ ] On-call definido durante rollout
- [ ] Timeline realista com buffers entre fases
