# Scorecard de Avaliação de Vendor de AI

## Propósito
Avaliar e comparar vendors de soluções de AI/ML de forma estruturada, considerando
capacidades técnicas, segurança, custo, suporte, roadmap e fit estratégico,
garantindo decisões de compra informadas e comparáveis.

## Quando Usar
- Ao avaliar plataformas de AI/ML (MLOps, LLM APIs, AI SaaS)
- Para comparar vendors em processo de RFP
- Na decisão build vs. buy para capacidades de AI
- Para revisão periódica de vendors existentes

## Agente Responsável
- **Autor primário:** CTO Agent ou AI/ML Agent
- **Contribuidores:** CISO Agent (segurança), CFO Agent (custo), Legal (contrato)
- **Revisor:** CEO Agent
- **Aprovador:** CTO Agent + CFO Agent

## Template

---

### SCORECARD DE VENDOR DE AI

**Data:** {{data}}
**Autor:** {{autor}}
**Categoria de solução:** {{categoria_solucao}}
**Budget disponível:** {{budget_disponivel}}
**Timeline de decisão:** {{deadline_decisao}}

---

#### 1. Requisitos (definidos antes da avaliação)

**Requisitos obrigatórios (must-have):**
- [ ] {{req_obrigatorio_1}}
- [ ] {{req_obrigatorio_2}}
- [ ] {{req_obrigatorio_3}}
- [ ] {{req_obrigatorio_4}}
- [ ] {{req_obrigatorio_5}}

**Requisitos desejáveis (nice-to-have):**
- [ ] {{req_desejavel_1}}
- [ ] {{req_desejavel_2}}
- [ ] {{req_desejavel_3}}

---

#### 2. Vendors Avaliados

| Vendor | Produto | Versão | Website | Contato |
|--------|---------|--------|---------|---------|
| {{vendor_1}} | {{produto_1}} | {{versao_1}} | {{site_1}} | {{contato_1}} |
| {{vendor_2}} | {{produto_2}} | {{versao_2}} | {{site_2}} | {{contato_2}} |
| {{vendor_3}} | {{produto_3}} | {{versao_3}} | {{site_3}} | {{contato_3}} |

---

#### 3. Matriz de Avaliação

| Critério | Peso (1-5) | Vendor A | Vendor B | Vendor C |
|----------|-----------|----------|----------|----------|
| **Capacidades Técnicas** | | | | |
| Performance/Accuracy | {{peso_perf}} | {{nota_perf_a}} | {{nota_perf_b}} | {{nota_perf_c}} |
| Escalabilidade | {{peso_escala}} | {{nota_escala_a}} | {{nota_escala_b}} | {{nota_escala_c}} |
| Integração (APIs, SDKs) | {{peso_integ}} | {{nota_integ_a}} | {{nota_integ_b}} | {{nota_integ_c}} |
| Customização/Fine-tuning | {{peso_custom}} | {{nota_custom_a}} | {{nota_custom_b}} | {{nota_custom_c}} |
| Latência | {{peso_lat}} | {{nota_lat_a}} | {{nota_lat_b}} | {{nota_lat_c}} |
| **Segurança e Compliance** | | | | |
| Data privacy (LGPD/GDPR) | {{peso_priv}} | {{nota_priv_a}} | {{nota_priv_b}} | {{nota_priv_c}} |
| SOC 2 / ISO 27001 | {{peso_cert}} | {{nota_cert_a}} | {{nota_cert_b}} | {{nota_cert_c}} |
| Data residency | {{peso_resid}} | {{nota_resid_a}} | {{nota_resid_b}} | {{nota_resid_c}} |
| Encryption (transit/rest) | {{peso_enc}} | {{nota_enc_a}} | {{nota_enc_b}} | {{nota_enc_c}} |
| **Custo** | | | | |
| Pricing model clarity | {{peso_pricing}} | {{nota_pricing_a}} | {{nota_pricing_b}} | {{nota_pricing_c}} |
| TCO (3 anos) | {{peso_tco}} | {{nota_tco_a}} | {{nota_tco_b}} | {{nota_tco_c}} |
| Previsibilidade de custos | {{peso_prev}} | {{nota_prev_a}} | {{nota_prev_b}} | {{nota_prev_c}} |
| **Suporte e Ecossistema** | | | | |
| Qualidade do suporte | {{peso_sup}} | {{nota_sup_a}} | {{nota_sup_b}} | {{nota_sup_c}} |
| Documentação | {{peso_doc}} | {{nota_doc_a}} | {{nota_doc_b}} | {{nota_doc_c}} |
| Comunidade/Ecossistema | {{peso_eco}} | {{nota_eco_a}} | {{nota_eco_b}} | {{nota_eco_c}} |
| **Estratégico** | | | | |
| Roadmap alignment | {{peso_road}} | {{nota_road_a}} | {{nota_road_b}} | {{nota_road_c}} |
| Viabilidade do vendor | {{peso_viab}} | {{nota_viab_a}} | {{nota_viab_b}} | {{nota_viab_c}} |
| Lock-in risk | {{peso_lock}} | {{nota_lock_a}} | {{nota_lock_b}} | {{nota_lock_c}} |
| **Score Ponderado Total** | — | **{{total_a}}** | **{{total_b}}** | **{{total_c}}** |

---

#### 4. Análise de Custo (TCO 3 anos)

| Componente | Vendor A | Vendor B | Vendor C |
|-----------|----------|----------|----------|
| Licenciamento/Subscription | {{lic_a}} | {{lic_b}} | {{lic_c}} |
| Implementação | {{impl_a}} | {{impl_b}} | {{impl_c}} |
| Treinamento | {{treino_a}} | {{treino_b}} | {{treino_c}} |
| Consumo/Usage | {{consumo_a}} | {{consumo_b}} | {{consumo_c}} |
| Suporte premium | {{suporte_a}} | {{suporte_b}} | {{suporte_c}} |
| Equipe interna necessária | {{equipe_a}} | {{equipe_b}} | {{equipe_c}} |
| **TCO Total (3 anos)** | **{{tco_a}}** | **{{tco_b}}** | **{{tco_c}}** |

---

#### 5. Resultados de PoC/Demo

| Teste | Critério | Vendor A | Vendor B | Vendor C |
|-------|----------|----------|----------|----------|
| {{teste_1}} | {{criterio_1}} | {{result_a1}} | {{result_b1}} | {{result_c1}} |
| {{teste_2}} | {{criterio_2}} | {{result_a2}} | {{result_b2}} | {{result_c2}} |
| {{teste_3}} | {{criterio_3}} | {{result_a3}} | {{result_b3}} | {{result_c3}} |

---

#### 6. Referências de Clientes

| Vendor | Cliente Ref. | Caso de Uso Similar? | Satisfação | Comentário |
|--------|-------------|---------------------|-----------|-----------|
| {{vendor_ref_1}} | {{cliente_1}} | {{similar_1}} | {{sat_1}} | {{coment_ref_1}} |
| {{vendor_ref_2}} | {{cliente_2}} | {{similar_2}} | {{sat_2}} | {{coment_ref_2}} |
| {{vendor_ref_3}} | {{cliente_3}} | {{similar_3}} | {{sat_3}} | {{coment_ref_3}} |

---

#### 7. Riscos por Vendor

| Vendor | Risco Principal | Mitigação |
|--------|----------------|-----------|
| {{vendor_a}} | {{risco_a}} | {{mit_a}} |
| {{vendor_b}} | {{risco_b}} | {{mit_b}} |
| {{vendor_c}} | {{risco_c}} | {{mit_c}} |

---

#### 8. Recomendação

**Vendor recomendado:** {{vendor_recomendado}}
**Score ponderado:** {{score_vencedor}}
**Justificativa:** {{justificativa_recomendacao}}
**Condições de contrato:** {{condicoes_contrato}}
**Próximos passos:** {{proximos_passos}}

---

## Instruções de Preenchimento

1. **Requisitos:** Defina ANTES de falar com vendors. Não ajuste requisitos para favorecer um vendor.
2. **PoC:** Sempre faça PoC com dados reais (ou representativos). Demo do vendor não é suficiente.
3. **TCO:** Inclua custos ocultos (equipe interna, treinamento, migração). Vendors só mostram licença.
4. **Lock-in:** Avalie custo de saída. Se for proibitivo, adicione penalidade no score.
5. **Referências:** Fale com clientes similares em tamanho e caso de uso. Peça referências que o vendor NÃO indicou.
6. **Segurança:** CISO Agent deve avaliar todos os vendors antes da shortlist.

## Exemplo Preenchido

---

### SCORECARD — Plataforma de LLM API

**Vendors:** OpenAI (GPT-4), Anthropic (Claude), Google (Gemini)
**Budget:** R$ 50K/mês

| Critério | Peso | OpenAI | Anthropic | Google |
|----------|------|--------|-----------|--------|
| Performance | 5 | 4 | 5 | 4 |
| Safety/Alignment | 5 | 4 | 5 | 3 |
| Pricing clarity | 4 | 3 | 4 | 3 |
| Data privacy | 5 | 3 | 4 | 3 |
| **Score Total** | — | **72** | **82** | **64** |

**Recomendação:** Anthropic (Claude) — maior score em safety e privacy, alinhado com nossos requisitos de compliance.

---

## Checklist de Qualidade

- [ ] Requisitos definidos antes de iniciar avaliação
- [ ] Mínimo 3 vendors avaliados
- [ ] PoC realizada com dados reais/representativos
- [ ] TCO calculado para 3 anos (não apenas licença)
- [ ] CISO Agent revisou aspectos de segurança e compliance
- [ ] Referências de clientes contactadas
- [ ] Lock-in risk avaliado com custo de saída
- [ ] Score ponderado calculado corretamente
- [ ] Recomendação é consistente com a avaliação
- [ ] CFO Agent validou os custos e TCO
