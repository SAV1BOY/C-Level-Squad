# Decision Quality Rubric — Rubrica de Qualidade de Decisão

> Referência do C-Level Squad para avaliar e melhorar a qualidade das decisões executivas.
> Princípio: uma boa decisão pode ter resultado ruim (variância), mas decisões de alta qualidade geram melhores resultados ao longo do tempo.

---

## 1. Filosofia: Qualidade do processo vs. Qualidade do resultado

É fundamental separar a qualidade da **decisão** da qualidade do **resultado**:

| | Resultado bom | Resultado ruim |
|---|---|---|
| **Processo bom** | Merecido sucesso ✓ | Má sorte (variância) — não punir |
| **Processo ruim** | Boa sorte — não recompensar | Falha previsível — aprender |

O C-Level Squad avalia e recompensa **qualidade do processo**, não apenas resultados.

---

## 2. Dimensões de avaliação

A rubrica avalia 10 dimensões, cada uma de 1 a 5. Score máximo: 50 pontos.

### Dimensão 1: Enquadramento do Problema (Problem Framing)

O problema foi definido corretamente antes de buscar soluções?

| Score | Descrição |
|-------|-----------|
| 1 | Problema não definido. Solução buscada antes de entender o problema. Confusão entre sintoma e causa raiz |
| 2 | Problema vagamente definido. Sem distinção clara entre causa e sintoma. Escopo indefinido |
| 3 | Problema definido com clareza razoável. Causa raiz parcialmente investigada. Escopo definido mas pode estar incorreto |
| 4 | Problema bem definido com análise de causa raiz. Escopo claro. Stakeholders concordam com o enquadramento |
| 5 | Problema rigorosamente enquadrado. Múltiplas perspectivas consideradas (5 Whys, Ishikawa). Validado com dados. Escopo preciso e acordado |

**Perguntas-guia:**
- Qual exatamente é o problema que estamos resolvendo?
- Para quem é um problema? Por que agora?
- Estamos tratando o sintoma ou a causa raiz?
- Se resolvêssemos este problema, o que mudaria concretamente?

### Dimensão 2: Qualidade da Evidência (Evidence Quality)

As informações usadas para decidir eram suficientes e confiáveis?

| Score | Descrição |
|-------|-----------|
| 1 | Nenhuma evidência. Decisão baseada puramente em opinião ou hierarquia (HiPPO — Highest Paid Person's Opinion) |
| 2 | Evidência anedótica. Dados de uma única fonte não validada. Viés de confirmação provável |
| 3 | Evidência moderada. Múltiplas fontes mas com gaps. Dados qualitativos sem triangulação quantitativa |
| 4 | Boa evidência. Dados quantitativos de fontes confiáveis + qualitativos complementares. Gaps identificados e documentados |
| 5 | Evidência excelente. Base rate check realizado. Dados quantitativos robustos + qualitativos triangulados. Fontes diversas. Limitações explícitas |

**Perguntas-guia:**
- Quais dados embasaram esta decisão?
- De onde vieram os dados? São confiáveis?
- Qual a base rate para este tipo de decisão?
- Que informação nos falta e quanto isso importa?

### Dimensão 3: Alternativas Consideradas (Alternatives)

Foram exploradas opções suficientes antes de decidir?

| Score | Descrição |
|-------|-----------|
| 1 | Apenas uma opção considerada (a "óbvia"). Nenhum esforço de explorar alternativas |
| 2 | Duas opções: "fazer" ou "não fazer". Falsa dicotomia. Sem criatividade |
| 3 | 3+ opções identificadas, mas análise superficial das alternativas. Uma opção claramente favorecida desde o início |
| 4 | 3-5 opções genuinamente viáveis analisadas com critérios consistentes. Pelo menos uma opção "de fora da caixa" |
| 5 | Ampla geração de alternativas (brainstorm estruturado). Cada opção analisada com os mesmos critérios. Opções híbridas exploradas. Opção "não fazer nada" incluída |

**Perguntas-guia:**
- Quantas opções foram consideradas seriamente?
- Existe uma opção que não consideramos?
- E se fizéssemos o oposto do que planejamos?
- Qual seria a abordagem de alguém de fora da indústria?

### Dimensão 4: Trade-offs Explícitos (Trade-off Clarity)

Os trade-offs de cada opção foram articulados claramente?

| Score | Descrição |
|-------|-----------|
| 1 | Trade-offs não mencionados. Decisão apresentada como "óbvia" e sem custos |
| 2 | Trade-offs vagamente reconhecidos ("tem riscos") mas não articulados |
| 3 | Principais trade-offs identificados mas não quantificados. Falta análise de "quem perde" |
| 4 | Trade-offs claros, documentados e quantificados onde possível. Impacto em diferentes stakeholders explícito |
| 5 | Trade-offs rigorosamente documentados com quantificação. Análise de segunda ordem (trade-offs dos trade-offs). Stakeholders afetados informados e consultados |

**Perguntas-guia:**
- O que estamos abrindo mão com esta escolha?
- Quem é negativamente afetado?
- Qual o custo de oportunidade?
- Se isso der errado, quanto custa reverter?

### Dimensão 5: Reversibilidade Avaliada (Reversibility Assessment)

A decisão foi classificada corretamente quanto à sua reversibilidade?

| Score | Descrição |
|-------|-----------|
| 1 | Reversibilidade não considerada. Decisão irreversível tratada como reversível (ou vice-versa) |
| 2 | Reversibilidade mencionada mas não analisada. Sem plano de contingência |
| 3 | Classificada como Type 1 (irreversível) ou Type 2 (reversível) corretamente. Plano básico de rollback |
| 4 | Reversibilidade bem avaliada. Para Type 1: processo deliberado com mais tempo e evidência. Para Type 2: bias para ação com kill criteria |
| 5 | Análise completa de reversibilidade. Type 1 com múltiplos gate reviews. Type 2 com experimento rápido planejado. Custos de reversão estimados. Triggers de reversão definidos |

**Framework de referência (Jeff Bezos):**
- **Type 1 (porta de mão única):** Irreversível ou muito custoso para reverter → Decidir devagar, com muita evidência
- **Type 2 (porta de mão dupla):** Reversível com custo razoável → Decidir rápido, aprender, ajustar

**Perguntas-guia:**
- Se esta decisão der errado, podemos voltar atrás? Quanto custaria?
- Isso é uma porta de mão única ou de mão dupla?
- Estamos aplicando o processo certo para o tipo de decisão?

### Dimensão 6: Vieses Mitigados (Bias Mitigation)

Houve esforço deliberado para identificar e mitigar vieses cognitivos?

| Score | Descrição |
|-------|-----------|
| 1 | Nenhuma consideração de vieses. Processo susceptível a groupthink, anchoring, confirmation bias |
| 2 | Vieses mencionados genericamente mas sem ação concreta para mitigá-los |
| 3 | Algumas técnicas de debiasing usadas (ex: devil's advocate, pre-mortem) mas de forma ad hoc |
| 4 | Processo estruturado de debiasing: base rate check, pre-mortem, red team, votação independente antes de discussão |
| 5 | Arsenal completo de debiasing: outside view, pre-mortem, red team, blind scoring, cenários, consulta externa. Vieses específicos identificados e endereçados |

**Vieses mais comuns em decisões executivas:**
- **Anchoring:** Primeira informação domina o julgamento
- **Confirmation bias:** Buscar apenas evidências que confirmam a hipótese
- **Sunk cost fallacy:** Continuar investindo por já ter investido
- **Overconfidence:** Superestimar precisão das próprias previsões
- **Groupthink:** Conformidade do grupo suprimindo dissidência
- **Availability bias:** Dar peso excessivo a eventos recentes ou memoráveis
- **Planning fallacy:** Subestimar tempo e custo sistematicamente

### Dimensão 7: Owner Designado (DRI — Directly Responsible Individual)

Foi atribuído um responsável claro pela execução e pelo resultado?

| Score | Descrição |
|-------|-----------|
| 1 | Nenhum owner definido. "Todo mundo" é responsável (ninguém é responsável) |
| 2 | Owner vaguamente mencionado ("time de produto vai cuidar") sem indivíduo específico |
| 3 | DRI nomeado mas sem mandato claro, sem recursos garantidos, sem timeline |
| 4 | DRI nomeado com mandato, recursos e timeline. Accountability claras. Checkpoints definidos |
| 5 | DRI nomeado com RACI completo. Mandato, recursos, timeline, checkpoints, critérios de sucesso e de kill. DRI aceitou publicamente a responsabilidade |

### Dimensão 8: Timeline Definida (Timeline)

A decisão tem prazos claros para execução e avaliação?

| Score | Descrição |
|-------|-----------|
| 1 | Sem timeline. "Vamos fazer eventualmente" |
| 2 | Timeline vaga: "próximo quarter" sem datas específicas |
| 3 | Datas definidas para início e conclusão, mas sem milestones intermediários |
| 4 | Timeline detalhada com milestones, checkpoints e deadlines intermediários. Dependências mapeadas |
| 5 | Timeline robusta com milestones, checkpoints, buffer para riscos, critérios de go/no-go em cada gate, e data de revisão da decisão pós-implementação |

### Dimensão 9: Critérios de Sucesso e Kill (Success & Kill Criteria)

Foram definidos antecipadamente os critérios para avaliar se a decisão foi boa?

| Score | Descrição |
|-------|-----------|
| 1 | Nenhum critério definido. Sucesso será julgado retroativamente e subjetivamente |
| 2 | Critérios vagos: "melhorar a experiência", "crescer receita" |
| 3 | Métricas de sucesso definidas mas sem targets numéricos. Sem kill criteria |
| 4 | Métricas de sucesso com targets numéricos. Kill criteria básicos definidos (ex: "se não atingir X em Y meses, revisamos") |
| 5 | Métricas de sucesso com targets, baseline, e método de medição. Kill criteria específicos com triggers automáticos. Leading indicators definidos para detecção precoce |

### Dimensão 10: Comunicação e Alinhamento (Communication)

A decisão foi comunicada adequadamente a todos os afetados?

| Score | Descrição |
|-------|-----------|
| 1 | Decisão não comunicada. Pessoas afetadas descobrem por acidente |
| 2 | Comunicação informal, inconsistente. Diferentes pessoas têm entendimentos diferentes |
| 3 | Comunicação formal feita, mas sem contexto (razões) ou sem canal para perguntas |
| 4 | Comunicação clara com: decisão, razões, trade-offs, timeline, DRI. Canal para perguntas estabelecido |
| 5 | Comunicação excelente: memo estruturado (ver memo-sections.md), Q&A realizada, dissidentes ouvidos e respondidos, follow-up planejado. Registro acessível para referência futura |

---

## 3. Scoring e interpretação

### Cálculo

```
Decision Quality Score = Σ (scores das 10 dimensões)
Máximo: 50 pontos
```

### Faixas de qualidade

| Score    | Nível        | Interpretação                                           |
|----------|-------------|--------------------------------------------------------|
| 41-50    | World-class | Processo de decisão exemplar. Documentar como referência |
| 31-40    | Bom         | Processo sólido com áreas pontuais de melhoria          |
| 21-30    | Adequado    | Funcional mas com gaps significativos. Melhorar          |
| 11-20    | Fraco       | Processo com falhas sérias. Alto risco de decisão ruim   |
| 1-10     | Crítico     | Processo essencialmente inexistente. Refazer              |

### Benchmarks por tipo de decisão

| Tipo de decisão              | Score mínimo recomendado | Justificativa                    |
|------------------------------|--------------------------|----------------------------------|
| Type 1 (irreversível, >R$1M) | ≥ 40                     | Alto impacto, baixa reversibilidade |
| Type 1 (irreversível, <R$1M) | ≥ 35                     | Irreversível mas impacto contido |
| Type 2 (reversível, estratégica) | ≥ 30                 | Reversível mas sinaliza direção  |
| Type 2 (reversível, tática)  | ≥ 20                     | Rápida e reversível — bias para ação |

---

## 4. Processo de aplicação

### Pré-decisão (proativo)
Usar a rubrica como checklist ANTES de decidir:
1. Revisar cada dimensão
2. Identificar gaps (scores < 3)
3. Investir tempo nas dimensões fracas antes de decidir

### Pós-decisão (retrospectivo)
Usar a rubrica para avaliar decisões passadas e aprender:
1. 30 dias após a decisão: avaliar processo (todas as 10 dimensões)
2. 90 dias após: avaliar resultados iniciais
3. Comparar qualidade do processo com qualidade do resultado
4. Identificar padrões: quais dimensões são consistentemente fracas?

### Cadência de review

```
Semanal:   Top 3 decisões da semana — quick score (5 minutos cada)
Mensal:    Decisões Type 1 do mês — full rubric (30 minutos cada)
Trimestral: Análise de padrões — quais dimensões precisam de investimento sistêmico?
```

---

## 5. Template de avaliação

```markdown
## Decision Quality Assessment

**Decisão:** [descrição em uma frase]
**Data da decisão:** [YYYY-MM-DD]
**Avaliador:** [agente]
**Data da avaliação:** [YYYY-MM-DD]
**Tipo:** [Type 1 / Type 2] — [Valor em jogo]

### Scores

| # | Dimensão               | Score (1-5) | Evidência / Justificativa |
|---|------------------------|-------------|---------------------------|
| 1 | Problem Framing        |             |                           |
| 2 | Evidence Quality       |             |                           |
| 3 | Alternatives           |             |                           |
| 4 | Trade-off Clarity      |             |                           |
| 5 | Reversibility          |             |                           |
| 6 | Bias Mitigation        |             |                           |
| 7 | DRI Assignment         |             |                           |
| 8 | Timeline               |             |                           |
| 9 | Success/Kill Criteria  |             |                           |
| 10| Communication          |             |                           |
|   | **TOTAL**              | **/50**     |                           |

### Dimensões mais fortes (top 3):
1. [dimensão] — [por quê]

### Dimensões mais fracas (bottom 3):
1. [dimensão] — [ação de melhoria]

### Resultado (preencher em 90 dias):
- [ ] Resultado positivo / negativo / neutro
- [ ] Processo previu o resultado? Sim / Não
- [ ] Lição aprendida: [texto]
```

---

## 6. Anti-patterns — Sinais de decisão de baixa qualidade

| Anti-pattern | Descrição | Dimensão afetada |
|---|---|---|
| **HiPPO** | A pessoa mais sênior decide e ninguém questiona | Evidence, Bias |
| **Analysis paralysis** | Dados infinitos, decisão nunca tomada | Timeline, Reversibility |
| **Solucionismo** | Pular direto para a solução sem entender o problema | Problem Framing |
| **Falsa unanimidade** | Todos "concordam" mas ninguém realmente se comprometeu | Communication, Alternatives |
| **Decisão fantasma** | "Decidimos" mas ninguém sabe quem faz o quê | DRI, Timeline |
| **Goalpost moving** | Critérios de sucesso mudam retroativamente | Success/Kill Criteria |
| **Sunk cost trap** | "Já investimos tanto, não podemos parar agora" | Bias, Trade-offs |
| **Decision amnesia** | Ninguém lembra por que decidimos isso | Communication |

---

## 7. Integração com outros frameworks do C-Level Squad

- **Evidência:** Usar `base-rate-checks.md` para Dimensão 2
- **Alternativas:** Usar `prioritization-math.md` para Dimensão 3
- **Riscos:** Usar `risk-scoring.md` para Dimensão 4 e 5
- **Comunicação:** Usar `memo-sections.md` para Dimensão 10
- **Timeline:** Usar `initiative-blocks.md` para Dimensão 8
- **Critérios:** Usar `okr-blocks.md` para Dimensão 9
