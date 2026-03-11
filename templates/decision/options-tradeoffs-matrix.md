# Matriz de Opções e Trade-offs

## Propósito
Estruturar a análise comparativa de 3 a 5 opções para uma decisão, apresentando de forma
visual e objetiva os trade-offs entre cada alternativa com base em critérios ponderados.

## Quando Usar
- Quando existem múltiplas opções viáveis para uma decisão
- Para facilitar discussões de alinhamento entre executivos
- Antes de elaborar o Memo Executivo de Decisão
- Quando stakeholders divergem sobre a melhor abordagem

## Agente Responsável
- **Autor primário:** Chief of Staff Agent (CoS)
- **Contribuidores:** Agentes funcionais relevantes à decisão
- **Revisor:** CEO Agent

## Template

---

### MATRIZ DE OPÇÕES E TRADE-OFFS

**Decisão em análise:** {{titulo_decisao}}
**Data da análise:** {{data_analise}}
**Autor:** {{nome_autor}}
**Deadline para decisão:** {{data_limite_decisao}}

---

#### 1. Definição do Problema

**Problema central:**
{{descricao_problema}}

**Resultado desejado:**
{{resultado_esperado}}

**Restrições conhecidas:**
- {{restricao_1}}
- {{restricao_2}}
- {{restricao_3}}

---

#### 2. Critérios de Avaliação

| # | Critério | Peso (1-5) | Definição |
|---|----------|------------|-----------|
| C1 | {{criterio_1}} | {{peso_1}} | {{definicao_criterio_1}} |
| C2 | {{criterio_2}} | {{peso_2}} | {{definicao_criterio_2}} |
| C3 | {{criterio_3}} | {{peso_3}} | {{definicao_criterio_3}} |
| C4 | {{criterio_4}} | {{peso_4}} | {{definicao_criterio_4}} |
| C5 | {{criterio_5}} | {{peso_5}} | {{definicao_criterio_5}} |

**Escala de pontuação:** 1 (Muito Fraco) | 2 (Fraco) | 3 (Neutro) | 4 (Forte) | 5 (Muito Forte)

---

#### 3. Descrição das Opções

**Opção A: {{nome_opcao_a}}**
{{descricao_opcao_a}}

**Opção B: {{nome_opcao_b}}**
{{descricao_opcao_b}}

**Opção C: {{nome_opcao_c}}**
{{descricao_opcao_c}}

**Opção D: {{nome_opcao_d}}** *(opcional)*
{{descricao_opcao_d}}

**Opção E: {{nome_opcao_e}}** *(opcional)*
{{descricao_opcao_e}}

---

#### 4. Matriz de Pontuação

| Critério | Peso | Opção A | Opção B | Opção C | Opção D | Opção E |
|----------|------|---------|---------|---------|---------|---------|
| {{criterio_1}} | {{peso_1}} | {{nota_a1}} | {{nota_b1}} | {{nota_c1}} | {{nota_d1}} | {{nota_e1}} |
| {{criterio_2}} | {{peso_2}} | {{nota_a2}} | {{nota_b2}} | {{nota_c2}} | {{nota_d2}} | {{nota_e2}} |
| {{criterio_3}} | {{peso_3}} | {{nota_a3}} | {{nota_b3}} | {{nota_c3}} | {{nota_d3}} | {{nota_e3}} |
| {{criterio_4}} | {{peso_4}} | {{nota_a4}} | {{nota_b4}} | {{nota_c4}} | {{nota_d4}} | {{nota_e4}} |
| {{criterio_5}} | {{peso_5}} | {{nota_a5}} | {{nota_b5}} | {{nota_c5}} | {{nota_d5}} | {{nota_e5}} |
| **Score Ponderado** | — | **{{total_a}}** | **{{total_b}}** | **{{total_c}}** | **{{total_d}}** | **{{total_e}}** |

*Score ponderado = Soma de (nota x peso) para cada critério*

---

#### 5. Análise de Trade-offs

**Trade-off 1: {{tradeoff_1_titulo}}**
{{tradeoff_1_descricao}}

**Trade-off 2: {{tradeoff_2_titulo}}**
{{tradeoff_2_descricao}}

**Trade-off 3: {{tradeoff_3_titulo}}**
{{tradeoff_3_descricao}}

---

#### 6. Riscos por Opção

| Opção | Risco Principal | Probabilidade | Impacto | Mitigação |
|-------|----------------|---------------|---------|-----------|
| A | {{risco_a}} | {{prob_a}} | {{impacto_a}} | {{mitigacao_a}} |
| B | {{risco_b}} | {{prob_b}} | {{impacto_b}} | {{mitigacao_b}} |
| C | {{risco_c}} | {{prob_c}} | {{impacto_c}} | {{mitigacao_c}} |
| D | {{risco_d}} | {{prob_d}} | {{impacto_d}} | {{mitigacao_d}} |
| E | {{risco_e}} | {{prob_e}} | {{impacto_e}} | {{mitigacao_e}} |

---

#### 7. Análise de Sensibilidade

**Se mudarmos os pesos, a recomendação muda?**

| Cenário de Pesos | Opção Vencedora | Score |
|-------------------|----------------|-------|
| Pesos originais | {{vencedor_original}} | {{score_original}} |
| Peso máximo em custo | {{vencedor_custo}} | {{score_custo}} |
| Peso máximo em velocidade | {{vencedor_velocidade}} | {{score_velocidade}} |
| Peso máximo em risco | {{vencedor_risco}} | {{score_risco}} |

**Conclusão da sensibilidade:** {{conclusao_sensibilidade}}

---

#### 8. Recomendação Preliminar

**Opção recomendada:** {{opcao_recomendada}}
**Score ponderado:** {{score_recomendada}}
**Justificativa resumida:** {{justificativa_breve}}

**Próximo passo:** {{proximo_passo}}

---

## Instruções de Preenchimento

1. **Critérios:** Defina de 3 a 7 critérios relevantes. Os mais comuns são: custo, velocidade
   de implementação, risco, alinhamento estratégico, impacto no cliente, escalabilidade.
2. **Pesos:** Atribua pesos de 1 a 5. O peso reflete a importância relativa do critério para
   esta decisão específica. Nem todos os critérios têm a mesma importância.
3. **Pontuação:** Use a escala de 1 a 5. Seja consistente na aplicação dos critérios entre opções.
4. **Trade-offs:** Descreva as tensões reais entre critérios. Ex.: "Velocidade vs. Custo" —
   a opção mais rápida custa 3x mais.
5. **Riscos:** Foque nos riscos materiais, não em todos os riscos possíveis.
6. **Opções:** Inclua sempre a opção de "não fazer nada" ou "manter status quo" como baseline.
7. **Fórmula do score:** Multiplique nota x peso para cada critério e some os resultados.
8. **Sensibilidade:** Teste se a recomendação muda com pesos diferentes. Se a mesma opção vence
   em todos os cenários, a recomendação é robusta.

## Exemplo Preenchido

---

### MATRIZ DE OPÇÕES E TRADE-OFFS

**Decisão em análise:** Escolha de plataforma de CRM para expansão comercial
**Data da análise:** 2026-03-11
**Autor:** CoS Agent
**Deadline para decisão:** 2026-03-25

---

#### 1. Definição do Problema

**Problema central:**
A equipe comercial opera com planilhas e o CRM atual não suporta automações necessárias
para escalar de 50 para 200 clientes enterprise no próximo ano.

**Resultado desejado:**
CRM implementado com automações de pipeline, scoring de leads e integração com marketing.

**Restrições conhecidas:**
- Orçamento máximo de R$ 300K/ano em licenciamento
- Migração deve ocorrer em no máximo 90 dias
- Integração obrigatória com ERP SAP existente

---

#### 4. Matriz de Pontuação

| Critério | Peso | Salesforce | HubSpot | Pipedrive |
|----------|------|------------|---------|-----------|
| Custo total (TCO 3 anos) | 4 | 2 | 4 | 5 |
| Velocidade de implementação | 3 | 2 | 4 | 5 |
| Funcionalidades nativas | 5 | 5 | 4 | 3 |
| Integração com SAP | 5 | 5 | 3 | 2 |
| Escalabilidade | 3 | 5 | 4 | 3 |
| **Score Ponderado** | — | **78** | **75** | **70** |

---

#### 8. Recomendação Preliminar

**Opção recomendada:** Salesforce
**Score ponderado:** 78
**Justificativa resumida:** Apesar do custo mais alto, a superioridade em funcionalidades
nativas e integração com SAP (ambos critérios de peso 5) compensa o investimento adicional
dado o objetivo de escalar para 200 clientes enterprise.

---

## Checklist de Qualidade

- [ ] Mínimo de 3 opções avaliadas
- [ ] Critérios possuem definição clara (não ambígua)
- [ ] Pesos foram discutidos e validados com stakeholders
- [ ] Pontuações são justificáveis com dados ou evidências
- [ ] Trade-offs estão explícitos e não omitidos
- [ ] A opção "não fazer nada" foi considerada
- [ ] Score ponderado foi calculado corretamente
- [ ] Análise de sensibilidade foi realizada
- [ ] Riscos materiais estão mapeados para cada opção
- [ ] Recomendação é consistente com a análise (não contradiz os scores)
- [ ] A matriz foi revisada por pelo menos dois agentes diferentes
