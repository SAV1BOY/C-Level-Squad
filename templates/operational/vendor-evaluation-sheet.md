# Ficha de Avaliação de Vendor

## Propósito
Padronizar a avaliação de fornecedores para qualquer tipo de contratação significativa
(SaaS, serviços, infraestrutura, consultoria), garantindo comparação objetiva entre
candidatos com base em critérios pré-definidos e ponderados.

## Quando Usar
- Para qualquer contratação de vendor com valor > R$ 50K/ano
- Em processos de RFP/RFI
- Na renovação de contratos significativos
- Para avaliar substituição de vendors existentes

## Agente Responsável
- **Autor primário:** Agente funcional da área requisitante
- **Contribuidores:** CIO Agent (técnico), CFO Agent (financeiro), Legal (contratual)
- **Revisor:** Chief of Staff Agent (CoS)
- **Aprovador:** CEO Agent (>R$ 200K/ano) ou agente funcional (<R$ 200K/ano)

## Template

---

### FICHA DE AVALIAÇÃO DE VENDOR

**Data:** {{data}}
**Autor:** {{autor}}
**Categoria:** {{categoria_servico}}
**Necessidade de negócio:** {{necessidade_resumida}}
**Budget disponível:** {{budget}}
**Timeline de decisão:** {{deadline}}

---

#### 1. Requisitos

**Obrigatórios (eliminatórios):**
| # | Requisito | Descrição |
|---|----------|-----------|
| R1 | {{req_obrig_1}} | {{desc_obrig_1}} |
| R2 | {{req_obrig_2}} | {{desc_obrig_2}} |
| R3 | {{req_obrig_3}} | {{desc_obrig_3}} |
| R4 | {{req_obrig_4}} | {{desc_obrig_4}} |

**Desejáveis (diferenciais):**
| # | Requisito | Peso (1-5) |
|---|----------|-----------|
| D1 | {{req_desej_1}} | {{peso_d1}} |
| D2 | {{req_desej_2}} | {{peso_d2}} |
| D3 | {{req_desej_3}} | {{peso_d3}} |
| D4 | {{req_desej_4}} | {{peso_d4}} |

---

#### 2. Vendors Avaliados

| Vendor | Produto/Serviço | Tamanho | Clientes Similares | Contato |
|--------|----------------|---------|-------------------|---------|
| {{vendor_1}} | {{produto_1}} | {{tamanho_1}} | {{clientes_1}} | {{contato_1}} |
| {{vendor_2}} | {{produto_2}} | {{tamanho_2}} | {{clientes_2}} | {{contato_2}} |
| {{vendor_3}} | {{produto_3}} | {{tamanho_3}} | {{clientes_3}} | {{contato_3}} |

---

#### 3. Verificação de Requisitos Obrigatórios

| Requisito | Vendor A | Vendor B | Vendor C |
|----------|----------|----------|----------|
| {{req_obrig_1}} | {{atende_a1}} | {{atende_b1}} | {{atende_c1}} |
| {{req_obrig_2}} | {{atende_a2}} | {{atende_b2}} | {{atende_c2}} |
| {{req_obrig_3}} | {{atende_a3}} | {{atende_b3}} | {{atende_c3}} |
| {{req_obrig_4}} | {{atende_a4}} | {{atende_b4}} | {{atende_c4}} |
| **Passa?** | **{{passa_a}}** | **{{passa_b}}** | **{{passa_c}}** |

*Vendor que não atende TODOS os requisitos obrigatórios é eliminado.*

---

#### 4. Matriz de Pontuação (Requisitos Desejáveis)

| Critério | Peso | Vendor A | Vendor B | Vendor C |
|----------|------|----------|----------|----------|
| {{criterio_1}} | {{peso_1}} | {{nota_a1}} | {{nota_b1}} | {{nota_c1}} |
| {{criterio_2}} | {{peso_2}} | {{nota_a2}} | {{nota_b2}} | {{nota_c2}} |
| {{criterio_3}} | {{peso_3}} | {{nota_a3}} | {{nota_b3}} | {{nota_c3}} |
| {{criterio_4}} | {{peso_4}} | {{nota_a4}} | {{nota_b4}} | {{nota_c4}} |
| {{criterio_5}} | {{peso_5}} | {{nota_a5}} | {{nota_b5}} | {{nota_c5}} |
| {{criterio_6}} | {{peso_6}} | {{nota_a6}} | {{nota_b6}} | {{nota_c6}} |
| **Score Ponderado** | — | **{{total_a}}** | **{{total_b}}** | **{{total_c}}** |

---

#### 5. Análise de Custo (TCO)

| Componente | Vendor A | Vendor B | Vendor C |
|-----------|----------|----------|----------|
| Licença/Subscription (anual) | {{lic_a}} | {{lic_b}} | {{lic_c}} |
| Implementação (one-time) | {{impl_a}} | {{impl_b}} | {{impl_c}} |
| Treinamento | {{treino_a}} | {{treino_b}} | {{treino_c}} |
| Suporte/Manutenção (anual) | {{suporte_a}} | {{suporte_b}} | {{suporte_c}} |
| Recursos internos necessários | {{interno_a}} | {{interno_b}} | {{interno_c}} |
| Custo de migração/saída | {{migracao_a}} | {{migracao_b}} | {{migracao_c}} |
| **TCO 3 anos** | **{{tco_a}}** | **{{tco_b}}** | **{{tco_c}}** |

---

#### 6. Avaliação de Risco do Vendor

| Critério de Risco | Vendor A | Vendor B | Vendor C |
|------------------|----------|----------|----------|
| Saúde financeira do vendor | {{fin_a}} | {{fin_b}} | {{fin_c}} |
| Lock-in / Custo de saída | {{lock_a}} | {{lock_b}} | {{lock_c}} |
| Dependência de pessoas-chave | {{dep_a}} | {{dep_b}} | {{dep_c}} |
| Segurança e compliance | {{seg_a}} | {{seg_b}} | {{seg_c}} |
| Continuidade do produto/roadmap | {{cont_a}} | {{cont_b}} | {{cont_c}} |

---

#### 7. Referências

| Vendor | Referência | Caso de Uso | Satisfação (1-5) | Red Flag? |
|--------|-----------|-------------|------------------|-----------|
| {{vendor_ref_1}} | {{ref_nome_1}} | {{caso_1}} | {{sat_1}} | {{flag_1}} |
| {{vendor_ref_2}} | {{ref_nome_2}} | {{caso_2}} | {{sat_2}} | {{flag_2}} |
| {{vendor_ref_3}} | {{ref_nome_3}} | {{caso_3}} | {{sat_3}} | {{flag_3}} |

---

#### 8. Termos Contratuais

| Aspecto | Vendor A | Vendor B | Vendor C |
|---------|----------|----------|----------|
| Duração do contrato | {{duracao_a}} | {{duracao_b}} | {{duracao_c}} |
| Cláusula de saída | {{saida_a}} | {{saida_b}} | {{saida_c}} |
| SLA garantido | {{sla_a}} | {{sla_b}} | {{sla_c}} |
| Penalidades por SLA | {{penalidade_a}} | {{penalidade_b}} | {{penalidade_c}} |
| Reajuste anual | {{reajuste_a}} | {{reajuste_b}} | {{reajuste_c}} |
| Propriedade dos dados | {{dados_a}} | {{dados_b}} | {{dados_c}} |

---

#### 9. Recomendação

**Vendor recomendado:** {{vendor_recomendado}}
**Score ponderado:** {{score_recomendado}}
**TCO 3 anos:** {{tco_recomendado}}

**Justificativa:**
{{justificativa_recomendacao}}

**Riscos da escolha:**
- {{risco_escolha_1}}
- {{risco_escolha_2}}

**Plano de implementação resumido:**
| Fase | Timeline | Atividade |
|------|----------|-----------|
| 1 | {{timeline_1}} | {{atividade_1}} |
| 2 | {{timeline_2}} | {{atividade_2}} |
| 3 | {{timeline_3}} | {{atividade_3}} |

---

#### 10. Aprovações

| Aprovador | Voto | Comentário | Data |
|-----------|------|-----------|------|
| {{aprovador_1}} | {{voto_1}} | {{coment_1}} | {{data_1}} |
| {{aprovador_2}} | {{voto_2}} | {{coment_2}} | {{data_2}} |
| {{aprovador_3}} | {{voto_3}} | {{coment_3}} | {{data_3}} |

---

## Instruções de Preenchimento

1. **Requisitos:** Defina ANTES de falar com vendors. Não ajuste para favorecer candidatos.
2. **Eliminatórios:** Se não atende todos, está fora. Sem exceções.
3. **TCO:** Inclua custos de migração de entrada E de saída. Vendors escondem custo de saída.
4. **Referências:** Fale com pelo menos 2 clientes por vendor, incluindo 1 não indicado pelo vendor.
5. **Contrato:** Negocie cláusula de saída antes de assinar. Depois é tarde.
6. **Lock-in:** Avalie o que acontece se o vendor fechar ou mudar pricing. Tenha plano B.

## Exemplo Preenchido

---

### AVALIAÇÃO — Plataforma de Help Desk

**Budget:** R$ 120K/ano
**Vendors:** Zendesk, Freshdesk, Intercom

| Critério | Peso | Zendesk | Freshdesk | Intercom |
|----------|------|---------|-----------|----------|
| Funcionalidades | 5 | 5 | 4 | 4 |
| UX/Usabilidade | 4 | 4 | 4 | 5 |
| Integrações | 4 | 5 | 3 | 4 |
| Preço | 3 | 2 | 5 | 3 |
| Suporte | 3 | 4 | 3 | 4 |
| **Score** | — | **80** | **73** | **78** |

**Recomendação:** Zendesk — maior score técnico, melhor ecossistema de integrações.

---

## Checklist de Qualidade

- [ ] Requisitos definidos antes de iniciar avaliação
- [ ] Requisitos obrigatórios são eliminatórios (sem exceções)
- [ ] Mínimo de 3 vendors avaliados
- [ ] TCO calculado para 3 anos (não apenas licença anual)
- [ ] Riscos do vendor avaliados (financeiro, lock-in, continuidade)
- [ ] Referências de clientes contactadas
- [ ] Termos contratuais analisados (SLA, saída, reajuste, dados)
- [ ] Score ponderado calculado corretamente
- [ ] Recomendação é consistente com a avaliação
- [ ] Aprovações obtidas conforme política de procurement
