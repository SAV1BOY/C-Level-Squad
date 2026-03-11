# Avaliação de Decisão Reversível vs. Irreversível

## Propósito
Classificar decisões como Type 1 (irreversível, "porta de mão única") ou Type 2
(reversível, "porta de mão dupla"), determinando o nível apropriado de análise,
aprovação e velocidade de execução para cada caso.

## Quando Usar
- Antes de iniciar a análise profunda de qualquer decisão significativa
- Para calibrar o nível de rigor necessário na tomada de decisão
- Quando há debate sobre a velocidade vs. profundidade da análise
- Para evitar over-engineering em decisões reversíveis ou under-analysis em irreversíveis

## Agente Responsável
- **Autor primário:** Chief of Staff Agent (CoS)
- **Validador:** CEO Agent
- **Consultor:** Agente funcional da área impactada

## Template

---

### AVALIAÇÃO TYPE 1 vs. TYPE 2

**Decisão em análise:** {{titulo_decisao}}
**Data:** {{data_avaliacao}}
**Autor:** {{nome_autor}}
**Área impactada:** {{area_impactada}}

---

#### 1. Descrição da Decisão

**O que está sendo decidido:**
{{descricao_decisao}}

**Contexto que motivou a decisão:**
{{contexto_motivador}}

**Alternativa ao status quo:**
{{descricao_alternativa}}

---

#### 2. Teste de Reversibilidade

Responda cada pergunta com Sim ou Não e justifique brevemente:

| # | Pergunta de Reversibilidade | Resposta | Justificativa |
|---|---------------------------|----------|---------------|
| 1 | Se esta decisão der errado, podemos voltar atrás em menos de 90 dias? | {{sim_nao_1}} | {{justificativa_1}} |
| 2 | O custo de reverter é menor que 20% do custo de implementar? | {{sim_nao_2}} | {{justificativa_2}} |
| 3 | A reputação/marca pode ser restaurada se revertermos? | {{sim_nao_3}} | {{justificativa_3}} |
| 4 | Não há compromissos contratuais de longo prazo envolvidos? | {{sim_nao_4}} | {{justificativa_4}} |
| 5 | Os dados/informações expostos podem ser "des-expostos"? | {{sim_nao_5}} | {{justificativa_5}} |
| 6 | Pessoas-chave não serão perdidas como consequência? | {{sim_nao_6}} | {{justificativa_6}} |
| 7 | Não envolve mudança regulatória ou legal irreversível? | {{sim_nao_7}} | {{justificativa_7}} |
| 8 | Clientes não serão permanentemente impactados? | {{sim_nao_8}} | {{justificativa_8}} |

**Contagem:** {{quantidade_sim}} Sim / {{quantidade_nao}} Não

---

#### 3. Classificação

**Resultado do teste:**

| Faixa | Classificação | Descrição |
|-------|--------------|-----------|
| 7-8 Sim | **Type 2 — Totalmente Reversível** | Decidir rápido, ajustar depois |
| 5-6 Sim | **Type 2 — Majoritariamente Reversível** | Análise leve, decidir com velocidade |
| 3-4 Sim | **Zona Cinzenta** | Análise moderada, buscar mais dados |
| 1-2 Sim | **Type 1 — Majoritariamente Irreversível** | Análise profunda obrigatória |
| 0 Sim | **Type 1 — Totalmente Irreversível** | Máximo rigor, múltiplas aprovações |

**Classificação desta decisão:** {{classificacao_final}}

---

#### 4. Implicações da Classificação

**Se Type 2 (Reversível):**

| Aspecto | Recomendação |
|---------|-------------|
| Nível de análise | Leve (1-2 dias) |
| Aprovação necessária | DRI da área + 1 executivo |
| Documentação | Memo simples ou registro em ata |
| Velocidade esperada | Decidir em até 1 semana |
| Monitoramento | Check-in em 30 dias para avaliar ajustes |
| Plano de rollback | Documentar rollback básico antes de executar |

**Se Type 1 (Irreversível):**

| Aspecto | Recomendação |
|---------|-------------|
| Nível de análise | Profundo (1-4 semanas) |
| Aprovação necessária | CEO + C-Level relevante + Board (se aplicável) |
| Documentação | Memo executivo completo + matriz de trade-offs |
| Velocidade esperada | Decidir com dados, não com pressa |
| Monitoramento | Milestones de acompanhamento definidos |
| Plano de rollback | Plano detalhado de contingência obrigatório |

---

#### 5. Fatores Agravantes

Marque os fatores que se aplicam (cada um "empurra" a decisão para Type 1):

- [ ] Envolve mais de 30% do orçamento anual
- [ ] Impacta mais de 50% da base de clientes
- [ ] Requer demissões ou reestruturação significativa
- [ ] Envolve fusão, aquisição ou venda de ativos
- [ ] Tem implicações regulatórias ou legais
- [ ] Compromete a empresa por mais de 12 meses
- [ ] Envolve dados sensíveis de clientes ou funcionários
- [ ] Pode gerar cobertura de mídia negativa

**Quantidade de fatores agravantes:** {{qtd_fatores_agravantes}}

---

#### 6. Decisão sobre o Processo

**Classificação final ajustada:** {{classificacao_ajustada}}
**Processo recomendado:** {{processo_recomendado}}
**Timeline de decisão:** {{timeline_decisao}}
**Aprovadores necessários:** {{lista_aprovadores}}

---

#### 7. Plano de Rollback (obrigatório para ambos os tipos)

**Trigger para rollback:** {{condicao_rollback}}
**Ações de rollback:**
1. {{acao_rollback_1}}
2. {{acao_rollback_2}}
3. {{acao_rollback_3}}

**Custo estimado do rollback:** {{custo_rollback}}
**Tempo estimado do rollback:** {{tempo_rollback}}

---

## Instruções de Preenchimento

1. **Teste de Reversibilidade:** Responda honestamente. Na dúvida, responda "Não" — é mais
   seguro tratar uma decisão reversível como irreversível do que o contrário.
2. **Fatores Agravantes:** Um único fator agravante pode elevar uma decisão Type 2 para Type 1.
   Use o bom senso.
3. **Classificação Ajustada:** Após considerar fatores agravantes, a classificação pode mudar.
   Documente a razão do ajuste.
4. **Plano de Rollback:** Mesmo decisões Type 2 devem ter um rollback básico documentado.
   Para Type 1, o plano deve ser detalhado e testado.
5. **Velocidade:** Decisões Type 2 devem ser tomadas rapidamente. Não aplique rigor excessivo.
   O custo da lentidão em decisões reversíveis é maior que o custo de eventual correção.

## Exemplo Preenchido

---

### AVALIAÇÃO TYPE 1 vs. TYPE 2

**Decisão em análise:** Lançamento de plano freemium para produto SaaS
**Data:** 2026-03-11
**Autor:** CoS Agent
**Área impactada:** Produto, Comercial, Financeiro

---

#### 2. Teste de Reversibilidade

| # | Pergunta de Reversibilidade | Resposta | Justificativa |
|---|---------------------------|----------|---------------|
| 1 | Podemos voltar atrás em menos de 90 dias? | Sim | Podemos descontinuar o plano free com aviso de 60 dias |
| 2 | Custo de reverter < 20% do custo de implementar? | Sim | Reverter é basicamente desligar a feature flag |
| 3 | A reputação pode ser restaurada? | Não | Remover um plano gratuito gera percepção negativa |
| 4 | Não há compromissos contratuais de longo prazo? | Sim | Sem contratos, é self-service |
| 5 | Dados podem ser "des-expostos"? | Sim | Não há exposição adicional de dados |
| 6 | Pessoas-chave não serão perdidas? | Sim | Não requer contratação específica |
| 7 | Não envolve mudança regulatória? | Sim | Sem implicações regulatórias |
| 8 | Clientes não serão permanentemente impactados? | Não | Usuários free perderiam acesso |

**Contagem:** 6 Sim / 2 Não

**Classificação:** Type 2 — Majoritariamente Reversível

**Fatores agravantes:** 1 (impacta percepção de marca)

**Classificação final ajustada:** Type 2 — com monitoramento reforçado
**Processo recomendado:** Análise de 1 semana, aprovação CEO + CMO, piloto de 90 dias
**Timeline de decisão:** Decidir até 2026-03-18

---

## Checklist de Qualidade

- [ ] Todas as 8 perguntas de reversibilidade foram respondidas com justificativa
- [ ] Fatores agravantes foram avaliados honestamente
- [ ] A classificação é consistente com as respostas do teste
- [ ] O processo recomendado é proporcional à classificação
- [ ] Plano de rollback está documentado independentemente do tipo
- [ ] Não há "teatro de análise" — decisões Type 2 não foram over-analyzed
- [ ] Decisões Type 1 têm rigor suficiente e múltiplos aprovadores
- [ ] O template foi preenchido ANTES de iniciar a análise profunda
- [ ] Stakeholders concordam com a classificação
- [ ] Timeline de decisão está definido e é realista
