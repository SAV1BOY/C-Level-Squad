# Card de Caso de Uso de AI

## Propósito
Documentar e avaliar casos de uso de inteligência artificial de forma estruturada,
cobrindo definição do problema, dados necessários, riscos, viabilidade técnica e
ROI esperado, garantindo que investimentos em AI sejam orientados por valor de negócio.

## Quando Usar
- Ao propor um novo caso de uso de AI/ML para avaliação
- Para priorizar entre múltiplos casos de uso de AI
- Como registro de casos aprovados, rejeitados ou em avaliação
- Para comunicar oportunidades de AI ao C-Level de forma padronizada

## Agente Responsável
- **Autor primário:** AI/ML Agent ou CTO Agent
- **Contribuidores:** Owner do processo de negócio, Data Team
- **Revisor:** CEO Agent (estratégia), CFO Agent (ROI), CISO Agent (risco)
- **Aprovador:** CEO Agent

## Template

---

### AI USE CASE CARD

**ID:** {{id_caso}}
**Nome do caso de uso:** {{nome_caso}}
**Data:** {{data}}
**Autor:** {{autor}}
**Status:** {{proposto_em_avaliacao_aprovado_em_piloto_produção_rejeitado}}
**Prioridade:** {{alta_media_baixa}}

---

#### 1. Definição do Problema

**Problema de negócio:**
{{descricao_problema_negocio}}

**Como é resolvido hoje (sem AI):**
{{solucao_atual}}

**Custo/ineficiência atual:**
{{custo_atual_quantificado}}

**Quem se beneficia:**
{{beneficiarios}}

---

#### 2. Solução Proposta com AI

**Descrição da solução:**
{{descricao_solucao_ai}}

**Tipo de AI/ML:**
| Aspecto | Detalhes |
|---------|---------|
| Categoria | {{classificacao_regressao_nlp_cv_genai_recsys}} |
| Abordagem | {{supervised_unsupervised_rl_llm_fine_tuning}} |
| Modelo(s) base | {{modelos_considerados}} |
| Build vs. Buy | {{build_buy_hybrid}} |

**Input(s):** {{inputs_do_modelo}}
**Output(s):** {{outputs_do_modelo}}
**Human-in-the-loop?** {{sim_nao_quando}}

---

#### 3. Dados Necessários

| Dataset | Fonte | Volume | Disponível? | Qualidade | Sensibilidade |
|---------|-------|--------|-------------|-----------|--------------|
| {{dataset_1}} | {{fonte_1}} | {{volume_1}} | {{disp_1}} | {{qual_1}} | {{sens_1}} |
| {{dataset_2}} | {{fonte_2}} | {{volume_2}} | {{disp_2}} | {{qual_2}} | {{sens_2}} |
| {{dataset_3}} | {{fonte_3}} | {{volume_3}} | {{disp_3}} | {{qual_3}} | {{sens_3}} |

**Gaps de dados identificados:**
- {{gap_dados_1}}
- {{gap_dados_2}}

**Necessidade de labeling/anotação:** {{sim_nao_detalhes}}

---

#### 4. Avaliação de Risco

| Categoria de Risco | Nível (1-5) | Descrição | Mitigação |
|-------------------|------------|-----------|-----------|
| Viés/Fairness | {{risco_vies}} | {{desc_vies}} | {{mit_vies}} |
| Privacidade (PII/LGPD) | {{risco_priv}} | {{desc_priv}} | {{mit_priv}} |
| Explicabilidade | {{risco_expl}} | {{desc_expl}} | {{mit_expl}} |
| Segurança | {{risco_seg}} | {{desc_seg}} | {{mit_seg}} |
| Dependência de vendor | {{risco_vendor}} | {{desc_vendor}} | {{mit_vendor}} |
| Reputacional | {{risco_rep}} | {{desc_rep}} | {{mit_rep}} |

**Risco geral:** {{baixo_medio_alto_critico}}

---

#### 5. Viabilidade Técnica

| Critério | Avaliação | Comentário |
|----------|----------|-----------|
| Dados suficientes e de qualidade? | {{sim_nao_dados}} | {{coment_dados}} |
| Infraestrutura disponível? | {{sim_nao_infra}} | {{coment_infra}} |
| Skills internos disponíveis? | {{sim_nao_skills}} | {{coment_skills}} |
| Problema é bem definido para ML? | {{sim_nao_ml}} | {{coment_ml}} |
| Baseline não-AI disponível? | {{sim_nao_baseline}} | {{coment_baseline}} |
| Latência aceitável? | {{sim_nao_latencia}} | {{coment_latencia}} |

**Viabilidade geral:** {{alta_media_baixa}}

---

#### 6. ROI Estimado

| Item | Valor |
|------|-------|
| Investimento total (build + run, 12 meses) | {{investimento_total}} |
| Economia/receita esperada (12 meses) | {{retorno_esperado}} |
| ROI | {{roi_percentual}} |
| Payback period | {{payback_meses}} |
| Break-even volume | {{breakeven}} |

**Premissas do ROI:**
- {{premissa_roi_1}}
- {{premissa_roi_2}}
- {{premissa_roi_3}}

---

#### 7. Métricas de Sucesso

| Métrica | Tipo | Baseline | Meta (Piloto) | Meta (Produção) |
|---------|------|----------|---------------|-----------------|
| {{metrica_neg_1}} | Negócio | {{base_neg_1}} | {{meta_piloto_1}} | {{meta_prod_1}} |
| {{metrica_neg_2}} | Negócio | {{base_neg_2}} | {{meta_piloto_2}} | {{meta_prod_2}} |
| {{metrica_ml_1}} | ML (técnica) | {{base_ml_1}} | {{meta_piloto_ml_1}} | {{meta_prod_ml_1}} |
| {{metrica_ml_2}} | ML (técnica) | {{base_ml_2}} | {{meta_piloto_ml_2}} | {{meta_prod_ml_2}} |

---

#### 8. Timeline Estimado

| Fase | Duração | Entregas |
|------|---------|---------|
| Discovery & Data | {{duracao_discovery}} | {{entregas_discovery}} |
| PoC/Protótipo | {{duracao_poc}} | {{entregas_poc}} |
| Piloto | {{duracao_piloto}} | {{entregas_piloto}} |
| Produção | {{duracao_producao}} | {{entregas_producao}} |
| Monitoramento & Melhoria | Contínuo | {{entregas_monit}} |

---

#### 9. Decisão

| Avaliador | Voto | Comentário |
|-----------|------|-----------|
| {{avaliador_1}} | {{voto_1}} | {{coment_1}} |
| {{avaliador_2}} | {{voto_2}} | {{coment_2}} |
| {{avaliador_3}} | {{voto_3}} | {{coment_3}} |

**Decisão:** {{aprovado_rejeitado_mais_analise}}
**Condições (se aprovado):** {{condicoes}}

---

## Instruções de Preenchimento

1. **Problema de negócio:** Comece pelo problema, não pela solução. AI é o meio, não o fim.
2. **Baseline:** Sempre defina como o problema é resolvido hoje. AI precisa ser melhor que o baseline.
3. **Dados:** Avalie honestamente. Sem dados de qualidade, não há AI que funcione.
4. **Risco:** Seja especialmente rigoroso com viés e privacidade. Reguladores e clientes observam.
5. **ROI:** Seja conservador. Multiplique custos por 2x e divida benefícios por 2x para teste de realidade.
6. **Human-in-the-loop:** Para casos de alto risco, sempre mantenha revisão humana.

## Exemplo Preenchido

---

### AI USE CASE CARD — Classificação Automática de Tickets de Suporte

**Problema:** 60% do tempo de L1 é gasto classificando e roteando tickets manualmente.
Tempo médio de classificação: 8 min/ticket. Volume: 3000 tickets/mês.

**Solução:** Modelo NLP para classificação automática em 12 categorias com confidence threshold.
Tickets com confidence > 85% são roteados automaticamente; abaixo disso, revisão humana.

**ROI:** Investimento R$ 120K (12 meses). Economia: R$ 280K/ano (4 FTEs parciais). ROI: 133%.

---

## Checklist de Qualidade

- [ ] Problema de negócio claramente definido (não "usar AI porque sim")
- [ ] Baseline (solução sem AI) documentada
- [ ] Dados necessários avaliados em volume, qualidade e disponibilidade
- [ ] Riscos de viés e privacidade especificamente avaliados
- [ ] ROI calculado com premissas documentadas e conservadoras
- [ ] Métricas de sucesso incluem tanto negócio quanto ML técnico
- [ ] Human-in-the-loop definido para cenários de alto risco
- [ ] Viabilidade técnica avaliada honestamente
- [ ] Timeline inclui fase de discovery/dados antes de construir modelo
- [ ] CISO Agent revisou aspectos de segurança e privacidade
