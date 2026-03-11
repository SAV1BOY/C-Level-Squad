# Memo Sections — Blocos Reutilizáveis para Memos Executivos

> Referência do C-Level Squad para construção de memos estruturados e persuasivos.
> Cada bloco pode ser usado independentemente ou combinado para formar memos completos.
> Inspirado em: Amazon 6-pager, Stripe operating memos, Basecamp pitches.

---

## 1. Executive Summary Block

### Propósito
Permitir que o leitor entenda a essência do memo em 60 segundos. Se o leitor só lê este bloco, deve sair com entendimento suficiente para agir.

### Template

```markdown
## Executive Summary

**Pedido:** [Uma frase: o que está sendo pedido/proposto/comunicado]

**Contexto em 1 linha:** [Por que agora? O que motivou este memo?]

**Recomendação:** [O que o autor recomenda, em termos concretos]

**Impacto esperado:** [Resultado quantificado: "Esperamos X, gerando Y em Z meses"]

**Investimento necessário:** [Recursos: R$, pessoas, tempo]

**Decisão necessária:** [GO/NO-GO | Aprovação de budget | Mudança de prioridade | etc.]

**Deadline para decisão:** [Data]
```

### Instruções
- Máximo de 150 palavras — se não cabe em 150 palavras, o memo não está claro o suficiente
- BLUF (Bottom Line Up Front): a primeira frase é a mais importante
- Use números, não adjetivos ("reduzir churn em 15%" em vez de "melhorar significativamente a retenção")
- Não use jargão que o leitor mais júnior da audiência não entenderia

### Exemplo

```markdown
## Executive Summary

**Pedido:** Aprovação para investir R$400K na construção de um motor de recomendação baseado em AI.

**Contexto:** Nossa taxa de cross-sell está em 8%, abaixo da média de mercado (15-20%). Análise de cohort mostra que clientes que descobrem o 2o produto nos primeiros 30 dias têm LTV 3.2× maior.

**Recomendação:** Desenvolver e lançar motor de recomendação em 4 meses, focando nos 3 produtos com maior propensão de cross-sell.

**Impacto esperado:** Aumento de cross-sell rate de 8% para 14%, gerando R$2.1M em receita incremental anualizada.

**Investimento:** R$400K (2 ML engineers + infra por 4 meses) + R$50K/ano de manutenção.

**Decisão:** GO/NO-GO do CEO + aprovação de budget do COO.

**Deadline:** 2026-03-25 (para iniciar no próximo sprint cycle).
```

---

## 2. Context Block

### Propósito
Fornecer o contexto necessário para que qualquer leitor, mesmo sem background no assunto, entenda a situação e por que ela importa.

### Template

```markdown
## Contexto

### Situação atual
[Descreva o estado atual com dados. O que está acontecendo? Quais métricas definem a situação?]

### Como chegamos aqui
[Breve histórico relevante. Decisões anteriores que moldaram a situação atual. Não mais que 3-5 frases.]

### Por que agora
[O que mudou que torna esta decisão necessária neste momento? Trigger específico: deadline, mudança de mercado, resultado de experimento, feedback de cliente, etc.]

### O que acontece se não fizermos nada
[Status quo bias check: descreva concretamente o cenário de inação. Inclua custo de oportunidade.]
```

### Instruções
- Fatos antes de interpretações
- Dados antes de opiniões
- Citar fontes quando possível
- Incluir a data dos dados (dados de 6 meses atrás podem estar obsoletos)
- "Por que agora" é a parte mais importante — se não há urgência clara, questione se o memo é necessário

### Exemplo

```markdown
## Contexto

### Situação atual
Nosso NPS caiu de 52 para 38 nos últimos 2 quarters (Q3-2025: 52, Q4-2025: 45, Q1-2026: 38). A principal categoria de detratores é "suporte lento" (42% dos detratores). Tempo médio de primeira resposta: 14h (benchmark: <4h). Volume de tickets cresceu 80% no período enquanto time de suporte cresceu 20%.

### Como chegamos aqui
Em Q2-2025 decidimos priorizar growth sobre operações (decisão do CEO, memo ref: CEO-2025-Q2-004). Crescemos 40% em clientes mas mantivemos a estrutura de suporte. A dívida operacional acumulou.

### Por que agora
(1) Churn rate subiu de 3.2% para 4.8% mensal, correlacionado com NPS (r=0.72). (2) Dois clientes enterprise sinalizaram risco de cancelamento citando suporte. (3) Board review em 30 dias — precisamos de plano de ação.

### Se não fizermos nada
Projeção: NPS chegará a ~30 em Q2-2026. Churn poderá atingir 6%+. Perda estimada: R$1.2M em ARR nos próximos 6 meses. Dano reputacional em review sites (G2, Capterra) difícil de reverter.
```

---

## 3. Options + Trade-offs Block

### Propósito
Apresentar alternativas genuínas com análise honesta de prós e contras. Evitar o anti-pattern de "3 opções onde 2 são absurdas para forçar a terceira".

### Template

```markdown
## Opções e Trade-offs

### Critérios de avaliação
[Listar os 3-5 critérios mais relevantes para esta decisão, em ordem de importância]

| Critério          | Peso | Descrição                                    |
|-------------------|------|----------------------------------------------|
| [Critério 1]      | [%]  | [Por que este critério importa]              |
| [Critério 2]      | [%]  | [...]                                        |

### Opção A: [Nome descritivo]
- **Descrição:** [O que exatamente faríamos]
- **Investimento:** [R$, pessoas, tempo]
- **Prós:** [bullets]
- **Contras:** [bullets]
- **Riscos:** [bullets]
- **Score:** [pontuação nos critérios]

### Opção B: [Nome descritivo]
[Mesmo formato]

### Opção C: [Nome descritivo]
[Mesmo formato]

### Opção D: Não fazer nada (status quo)
[Sempre incluir esta opção como baseline]

### Comparação resumida

| Critério      | Opção A | Opção B | Opção C | Status quo |
|---------------|---------|---------|---------|------------|
| [Critério 1]  |         |         |         |            |
| **Score total**|         |         |         |            |
```

### Instruções
- Mínimo 3 opções genuínas + "não fazer nada"
- Cada opção deve ser defensável — se não é, não inclua
- Prós E contras para TODAS as opções, inclusive a recomendada
- Quantificar sempre que possível (R$, %, tempo)
- Explicitar quem é negativamente afetado por cada opção

---

## 4. Recommendation Block

### Propósito
Apresentar a recomendação do autor com rationale claro. Separar claramente fato de opinião.

### Template

```markdown
## Recomendação

**Opção recomendada:** [Opção X: Nome]

### Rationale
[Por que esta opção é a melhor escolha, referenciando os critérios de avaliação]

1. [Argumento 1 — preferencialmente com dado]
2. [Argumento 2]
3. [Argumento 3]

### O que me faria mudar de opinião
[Quais evidências ou mudanças de cenário fariam o autor recomendar outra opção. Importante para demonstrar pensamento honesto.]

### Riscos aceitos com esta recomendação
[Listar os riscos da opção recomendada que estamos consciente e conscientemente aceitando]

### Condições de sucesso
[O que precisa ser verdade para esta recomendação funcionar]
```

### Instruções
- A recomendação deve fluir logicamente da análise de opções
- "O que me faria mudar de opinião" é o teste de integridade intelectual
- Se o autor não consegue articular o que o faria mudar de opinião, a análise pode estar enviesada
- Diferenciar "recomendo porque os dados mostram" de "recomendo porque acredito"

---

## 5. Risk Assessment Block

### Propósito
Análise de riscos específica para a decisão em questão. Versão compacta do framework de `risk-scoring.md`.

### Template

```markdown
## Análise de Riscos

| # | Risco                    | P (1-5) | I (1-5) | Score | Mitigação proposta          | Owner |
|---|--------------------------|---------|---------|-------|-----------------------------|-------|
| 1 | [Descrição do risco]     |         |         |       | [Ação de mitigação]         | [DRI] |
| 2 | [...]                    |         |         |       | [...]                       | [DRI] |

### Risco residual após mitigação
[Breve avaliação: com as mitigações, o risco total é aceitável?]

### Cenário de pior caso
[Se tudo der errado, qual é o impacto máximo? É sobrevivível?]
```

---

## 6. Timeline Block

### Template

```markdown
## Timeline

### Visão geral
**Início:** [data]  →  **Fim estimado:** [data]  →  **Duração:** [X semanas/meses]

### Milestones

| # | Milestone                      | Data       | DRI  | Dependências     | Critério de done          |
|---|-------------------------------|------------|------|------------------|---------------------------|
| 1 | [Milestone 1]                 | [data]     | [DRI]| [dep]            | [critério]                |
| 2 | [Milestone 2]                 | [data]     | [DRI]| [dep]            | [critério]                |

### Gates de decisão
| Gate | Data   | Decisão                        | Decisor | Input necessário |
|------|--------|--------------------------------|---------|------------------|
| G1   | [data] | Continue/Pivot/Kill            | [DRI]   | [dados]          |

### Premissas de timeline
- [Premissa 1: ex. "Contratação de ML engineer concluída até [data]"]
- [Premissa 2]

### Riscos de timeline
- [Risco 1: o que pode atrasar + impacto + mitigação]
```

---

## 7. Budget Block

### Template

```markdown
## Budget

### Investimento total: R$ [total]

### Breakdown

| Categoria         | Valor (R$) | Recorrência    | Notas                     |
|-------------------|-----------|----------------|---------------------------|
| Pessoas           | [R$]      | [one-time/mensal]| [detalhes]               |
| Infraestrutura    | [R$]      | [mensal]        | [detalhes]               |
| Licenças/Tools    | [R$]      | [anual]         | [detalhes]               |
| Consultoria       | [R$]      | [one-time]      | [detalhes]               |
| Contingência (15%)| [R$]      | [one-time]      | Buffer para imprevistos  |
| **Total**         | **[R$]**  |                 |                          |

### Fonte de funding
[De onde vem o dinheiro? Budget existente? Novo budget? Realocação?]

### ROI esperado
- Investimento: R$ [X]
- Retorno esperado: R$ [Y] em [Z] meses
- ROI: [Y/X]×
- Payback period: [N] meses
- Break-even: [data]

### Cenários de ROI
| Cenário    | Probabilidade | Retorno | ROI  |
|-----------|---------------|---------|------|
| Otimista  | 20%           | R$ [X]  | [X]× |
| Base      | 60%           | R$ [X]  | [X]× |
| Pessimista| 20%           | R$ [X]  | [X]× |
| **EMV**   |               | **R$ [X]** | **[X]×** |
```

---

## 8. DRI Assignment Block

### Template

```markdown
## Responsabilidades (RACI)

**DRI (Directly Responsible Individual):** [Nome/Agente]

| Atividade                     | R (Responsible) | A (Accountable) | C (Consulted) | I (Informed) |
|------------------------------|-----------------|-----------------|---------------|--------------|
| [Atividade 1]                | [agente]        | [agente]        | [agentes]     | [agentes]    |
| [Atividade 2]                | [agente]        | [agente]        | [agentes]     | [agentes]    |

### Mandato do DRI
- **Pode decidir sem aprovação:** [escopo de autonomia]
- **Precisa de aprovação para:** [decisões que requerem escalação]
- **Budget autorizado:** R$ [X]
- **Timeline de autoridade:** [data início] a [data fim]
- **Reporta progresso para:** [agente] via [canal] com frequência [X]
```

---

## 9. Next Steps Block

### Template

```markdown
## Próximos Passos

### Imediatos (esta semana)
- [ ] [Ação 1] — DRI: [agente] — Até: [data]
- [ ] [Ação 2] — DRI: [agente] — Até: [data]

### Curto prazo (próximas 2-4 semanas)
- [ ] [Ação 3] — DRI: [agente] — Até: [data]
- [ ] [Ação 4] — DRI: [agente] — Até: [data]

### Dependências para avançar
- [Dependência 1] — De quem: [agente] — Até quando: [data]

### Checkpoints de revisão
- [Data 1]: Review de progresso — Participantes: [agentes]
- [Data 2]: Gate de decisão continue/kill — Decisor: [agente]
```

---

## 10. Appendix Block

### Template

```markdown
## Apêndice

### A. Dados complementares
[Tabelas, gráficos, análises detalhadas que suportam o memo mas não são essenciais para o entendimento principal]

### B. Referências
- [Fonte 1]: [descrição e link]
- [Fonte 2]: [descrição e link]

### C. Glossário
| Termo | Definição |
|-------|-----------|
| [termo]| [definição simples] |

### D. Histórico de decisões relacionadas
| Data | Decisão | Memo ref | Resultado |
|------|---------|----------|-----------|
| [data]| [decisão] | [ref] | [resultado] |

### E. Feedback recebido (pré-publicação)
| Reviewer | Feedback principal | Incorporado? |
|----------|-------------------|-------------|
| [agente] | [feedback]        | Sim/Não — [razão] |
```

---

## 11. Guia de montagem de memos completos

### Memo de proposta (6-pager style)

```
1. Executive Summary ← Obrigatório
2. Context ← Obrigatório
3. Options + Trade-offs ← Obrigatório
4. Recommendation ← Obrigatório
5. Risk Assessment ← Obrigatório
6. Timeline ← Obrigatório
7. Budget ← Se aplicável
8. DRI Assignment ← Obrigatório
9. Next Steps ← Obrigatório
10. Appendix ← Se necessário
```

### Memo de status/update

```
1. Executive Summary (foco em status e bloqueios)
2. Context (o que mudou desde o último update)
3. Risk Assessment (novos riscos ou mudanças)
4. Next Steps
```

### Memo de decisão (decision doc)

```
1. Executive Summary (com a decisão recomendada)
2. Context (por que esta decisão é necessária)
3. Options + Trade-offs
4. Recommendation
5. DRI Assignment
6. Next Steps
```

### Memo de post-mortem

```
1. Executive Summary (o que aconteceu e impacto)
2. Context (timeline detalhada do incidente)
3. Risk Assessment (o que deu errado e por quê — 5 Whys)
4. Recommendation (ações corretivas)
5. DRI Assignment
6. Next Steps
```

---

## 12. Regras gerais para memos no C-Level Squad

1. **Máximo 6 páginas** de conteúdo (excluindo apêndice)
2. **Narrativa, não bullets** para argumentos principais (Amazon style)
3. **Dados, não opiniões** como fundamento
4. **Leitura silenciosa** nos primeiros 15 minutos da reunião de review
5. **Versionamento:** nomear como `[AGENTE]-[ANO]-[QUARTER]-[SEQ]` (ex: CTO-2026-Q1-003)
6. **Review cycle:** autor → 1 reviewer → revisão → distribuição → leitura → discussão
7. **Não apresentar slides:** o memo é o documento. Se precisa de slides, o memo não está bom
