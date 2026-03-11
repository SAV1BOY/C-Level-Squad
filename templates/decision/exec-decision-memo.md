# Memo Executivo de Decisão

## Propósito
Fornecer um formato estruturado de uma página para documentar decisões executivas críticas,
garantindo clareza sobre contexto, opções avaliadas, trade-offs, recomendação final,
responsável direto (DRI) e data de efetivação.

## Quando Usar
- Antes de qualquer decisão estratégica com impacto significativo no negócio
- Quando múltiplos stakeholders precisam alinhar sobre uma escolha
- Para decisões que requerem registro formal e rastreabilidade
- Quando o CEO ou C-Level precisa aprovar uma mudança relevante

## Agente Responsável
- **Autor primário:** Chief of Staff Agent (CoS)
- **Revisores:** CEO Agent, agente funcional relevante (CFO, CTO, CMO, etc.)
- **Aprovador final:** CEO Agent

## Template

---

### MEMO DE DECISÃO EXECUTIVA

**Título da Decisão:** {{titulo_decisao}}
**Data:** {{data_decisao}}
**Autor:** {{nome_autor}}
**DRI (Directly Responsible Individual):** {{nome_dri}}
**Classificação:** {{confidencial_interno_publico}}
**Status:** {{rascunho_em_revisao_aprovado}}

---

#### 1. Contexto e Problema

{{descricao_contexto}}

**Pergunta-chave que esta decisão responde:**
> {{pergunta_chave}}

**Urgência:** {{alta_media_baixa}}
**Impacto estimado:** {{descricao_impacto}}

---

#### 2. Opções Consideradas

| # | Opção | Descrição Resumida |
|---|-------|--------------------|
| 1 | {{opcao_1_nome}} | {{opcao_1_descricao}} |
| 2 | {{opcao_2_nome}} | {{opcao_2_descricao}} |
| 3 | {{opcao_3_nome}} | {{opcao_3_descricao}} |

---

#### 3. Trade-offs Principais

| Critério | Opção 1 | Opção 2 | Opção 3 |
|----------|---------|---------|---------|
| Custo | {{custo_1}} | {{custo_2}} | {{custo_3}} |
| Velocidade | {{velocidade_1}} | {{velocidade_2}} | {{velocidade_3}} |
| Risco | {{risco_1}} | {{risco_2}} | {{risco_3}} |
| Alinhamento estratégico | {{alinhamento_1}} | {{alinhamento_2}} | {{alinhamento_3}} |

---

#### 4. Recomendação

**Opção recomendada:** {{opcao_recomendada}}

**Justificativa:**
{{justificativa_recomendacao}}

**Riscos residuais e mitigações:**
- {{risco_residual_1}}: {{mitigacao_1}}
- {{risco_residual_2}}: {{mitigacao_2}}

---

#### 5. Próximos Passos

| Ação | Responsável | Prazo |
|------|-------------|-------|
| {{acao_1}} | {{responsavel_1}} | {{prazo_1}} |
| {{acao_2}} | {{responsavel_2}} | {{prazo_2}} |
| {{acao_3}} | {{responsavel_3}} | {{prazo_3}} |

---

#### 6. Assinaturas / Aprovações

- [ ] {{aprovador_1}} — Data: {{data_aprovacao_1}}
- [ ] {{aprovador_2}} — Data: {{data_aprovacao_2}}

---

## Instruções de Preenchimento

1. **Título da Decisão:** Seja específico e objetivo. Evite títulos genéricos como "Decisão sobre estratégia".
2. **Contexto:** Limite a 3-5 frases. O leitor deve entender o problema em 30 segundos.
3. **Opções:** Liste no mínimo 2 e no máximo 5 opções. Inclua sempre a opção "não fazer nada".
4. **Trade-offs:** Use classificações simples (Alto/Médio/Baixo) ou valores numéricos quando disponíveis.
5. **Recomendação:** Seja direto. Indique claramente qual opção escolher e por quê.
6. **DRI:** Deve ser uma única pessoa, nunca um comitê ou equipe.
7. **Próximos Passos:** Cada ação deve ser concreta, com responsável individual e prazo definido.
8. **Mantenha o memo em uma página.** Se precisar de mais detalhes, use anexos.

## Exemplo Preenchido

---

### MEMO DE DECISÃO EXECUTIVA

**Título da Decisão:** Migração do sistema de pagamentos para Stripe
**Data:** 2026-03-11
**Autor:** CoS Agent
**DRI (Directly Responsible Individual):** CTO Agent
**Classificação:** Confidencial
**Status:** Em Revisão

---

#### 1. Contexto e Problema

O sistema atual de pagamentos (gateway legado) apresenta taxa de falha de 4,2% nas transações,
gerando perda estimada de R$ 180K/mês em receita. O contrato atual vence em 60 dias e a
renovação exige compromisso de 24 meses. Precisamos decidir se migramos ou renovamos.

**Pergunta-chave que esta decisão responde:**
> Devemos migrar o processamento de pagamentos para Stripe ou renovar com o gateway atual?

**Urgência:** Alta
**Impacto estimado:** R$ 2,1M/ano em receita recuperada + redução de churn

---

#### 2. Opções Consideradas

| # | Opção | Descrição Resumida |
|---|-------|--------------------|
| 1 | Migrar para Stripe | Migração completa em 45 dias com equipe dedicada |
| 2 | Renovar contrato atual | Renovação por 24 meses com desconto de 15% |
| 3 | Não fazer nada | Operar mês-a-mês no contrato atual sem compromisso |

---

#### 3. Trade-offs Principais

| Critério | Opção 1 | Opção 2 | Opção 3 |
|----------|---------|---------|---------|
| Custo | Alto (R$ 200K migração) | Médio (R$ 50K/mês) | Baixo (R$ 65K/mês) |
| Velocidade | 45 dias | Imediato | Imediato |
| Risco | Médio (migração) | Baixo | Alto (sem contrato) |
| Alinhamento estratégico | Alto | Baixo | Baixo |

---

#### 4. Recomendação

**Opção recomendada:** Opção 1 — Migrar para Stripe

**Justificativa:**
A redução da taxa de falha de 4,2% para <1% representa R$ 2,1M/ano em receita recuperada,
pagando o investimento da migração em menos de 5 semanas. A API do Stripe permite maior
velocidade de desenvolvimento de funcionalidades futuras.

**Riscos residuais e mitigações:**
- Downtime durante migração: Migração paralela com rollback automático
- Curva de aprendizado da equipe: Training de 2 semanas antes do go-live

---

#### 5. Próximos Passos

| Ação | Responsável | Prazo |
|------|-------------|-------|
| Assinar contrato Stripe | CFO Agent | 2026-03-15 |
| Montar squad de migração | CTO Agent | 2026-03-18 |
| Comunicar timeline aos stakeholders | CoS Agent | 2026-03-19 |

---

#### 6. Assinaturas / Aprovações

- [x] CEO Agent — Data: 2026-03-12
- [x] CFO Agent — Data: 2026-03-12

---

## Checklist de Qualidade

- [ ] O memo cabe em uma página impressa
- [ ] O contexto é compreensível em menos de 30 segundos
- [ ] Pelo menos 2 opções foram consideradas (incluindo "não fazer nada")
- [ ] Os trade-offs usam critérios mensuráveis sempre que possível
- [ ] A recomendação é clara e direta
- [ ] O DRI é uma pessoa específica, não uma equipe
- [ ] Todos os próximos passos têm responsável e prazo
- [ ] O memo foi revisado por pelo menos um stakeholder antes da aprovação
- [ ] Dados financeiros foram validados pelo CFO Agent
- [ ] Riscos residuais possuem mitigações definidas
