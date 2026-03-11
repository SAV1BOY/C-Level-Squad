# Decision Blocks — Blocos Reutilizáveis para Tomada de Decisão

> Blocos padronizados para estruturar, documentar e comunicar decisões.
> Decisões bem documentadas são mais fáceis de implementar, comunicar e revisar.

---

## 1. Bloco: Decision Log (Registro de Decisão)

### Template
```markdown
## Registro de Decisão

| Campo | Detalhes |
|-------|---------|
| **ID** | [DEC-AAAA-NNN] |
| **Título** | [Descrição curta da decisão] |
| **Data** | [DD/MM/AAAA] |
| **Decisor(es)** | [Quem tomou a decisão] |
| **Contexto** | [Por que a decisão foi necessária — 2-3 frases] |
| **Decisão** | [O que foi decidido — declaração clara] |
| **Alternativas descartadas** | [O que foi considerado e descartado] |
| **Racional** | [Por que esta opção — argumento principal] |
| **Consequências esperadas** | [O que esperamos que aconteça] |
| **Reversibilidade** | [Fácil de reverter / Difícil / Irreversível] |
| **Data de revisão** | [Quando revisitar a decisão] |
```

---

## 2. Bloco: Framework de Decisão (RAPID)

### Template
```markdown
## RAPID — [Título da Decisão]

| Papel | Pessoa | Responsabilidade |
|-------|--------|-----------------|
| **R** — Recommend | [Nome] | Analisa opções e recomenda uma |
| **A** — Agree | [Nome(s)] | Precisa concordar (pode vetar) |
| **P** — Perform | [Nome(s)] | Implementa a decisão |
| **I** — Input | [Nome(s)] | Fornece dados/perspectiva (consultado) |
| **D** — Decide | [Nome] | Tomador final da decisão |

**Regra:** D decide após ouvir R e I. A pode vetar, mas raramente deve.
```

### Variante: DACI
```markdown
| Papel | Pessoa | Descrição |
|-------|--------|-----------|
| **D** — Driver | [Nome] | Conduz o processo de decisão |
| **A** — Approver | [Nome] | Toma a decisão final (1 pessoa) |
| **C** — Contributors | [Nomes] | Contribuem com input e perspectiva |
| **I** — Informed | [Nomes] | São informados após a decisão |
```

---

## 3. Bloco: Matriz de Decisão Ponderada

### Template
```markdown
## Matriz de Decisão — [Título]

| Critério | Peso | Opção A | Opção B | Opção C |
|----------|:----:|:------:|:------:|:------:|
| [Critério 1] | [1-5] | [1-5] | [1-5] | [1-5] |
| [Critério 2] | [1-5] | [1-5] | [1-5] | [1-5] |
| [Critério 3] | [1-5] | [1-5] | [1-5] | [1-5] |
| [Critério 4] | [1-5] | [1-5] | [1-5] | [1-5] |
| [Critério 5] | [1-5] | [1-5] | [1-5] | [1-5] |
| **Score Ponderado** | — | **[X.X]** | **[X.X]** | **[X.X]** |

**Cálculo:** Para cada opção, soma de (peso x score) / soma dos pesos
**Vencedor:** Opção [X] com score [X.X]
**Nota:** A matriz informa, mas não substitui julgamento — considere fatores qualitativos.
```

---

## 4. Bloco: Decisão Tipo 1 vs Tipo 2 (Amazon)

### Template
```markdown
## Classificação da Decisão

### Tipo 1 (Porta de mão única — irreversível)
- Consequências são significativas e difíceis de reverter
- Requer análise profunda e aprovação sênior
- Exemplos: aquisição, demissões em massa, escolha de stack core
- **Processo:** Análise detalhada → Revisão multi-stakeholder → Decisão executiva

### Tipo 2 (Porta de mão dupla — reversível)
- Consequências são limitadas e facilmente reversíveis
- Pode ser tomada rapidamente por quem está mais próximo do problema
- Exemplos: escolha de ferramenta, naming, formato de reunião, A/B test
- **Processo:** Decida e execute → Ajuste se necessário

**Esta decisão é:** [Tipo 1 / Tipo 2]
**Portanto:** [Processo adequado ao tipo]
```

---

## 5. Bloco: Pre-Mortem

### Template
```markdown
## Pre-Mortem — [Decisão/Projeto]

> "É 6 meses no futuro. A decisão falhou completamente. O que deu errado?"

| # | Cenário de Falha | Probabilidade | Impacto | Prevenção |
|---|------------------|:---:|:---:|-----------|
| 1 | [O que poderia dar errado] | [A/M/B] | [A/M/B] | [Como prevenir] |
| 2 | [Cenário] | [Prob.] | [Impacto] | [Prevenção] |
| 3 | [Cenário] | [Prob.] | [Impacto] | [Prevenção] |
| 4 | [Cenário] | [Prob.] | [Impacto] | [Prevenção] |
| 5 | [Cenário] | [Prob.] | [Impacto] | [Prevenção] |

**Decisão ajustada com base no pre-mortem:**
[Como o exercício mudou ou reforçou a decisão]
```

---

## 6. Bloco: Trade-off Analysis

### Template
```markdown
## Análise de Trade-offs — [Decisão]

### O que Ganhamos
- [Benefício 1 — quantificado quando possível]
- [Benefício 2]
- [Benefício 3]

### O que Perdemos / Abrimos Mão
- [Trade-off 1 — custo ou perda aceita conscientemente]
- [Trade-off 2]
- [Trade-off 3]

### Por que os Benefícios Superam os Trade-offs
[Argumento em 2-3 frases justificando por que aceitamos os trade-offs]

### Condições para Reavaliação
[Em que circunstâncias os trade-offs se tornam inaceitáveis]
```

---

## 7. Bloco: Comunicação de Decisão

### Template
```markdown
## Decisão: [Título]

**O que decidimos:** [Declaração clara em 1-2 frases]

**Por que decidimos isso:** [Razão principal — 2-3 frases]

**O que consideramos e descartamos:**
- [Alternativa A — por que não]
- [Alternativa B — por que não]

**O que muda para você:**
- [Impacto concreto 1]
- [Impacto concreto 2]

**Próximos passos:**
- [Ação 1 — owner — prazo]
- [Ação 2 — owner — prazo]

**Perguntas?** [Canal]
```

---

## 8. Bloco: Decision Review (Revisão Retrospectiva)

### Template
```markdown
## Revisão de Decisão — [ID/Título]

| Campo | Original | Atualização |
|-------|---------|------------|
| **Data da decisão** | [DD/MM/AAAA] | — |
| **Data da revisão** | — | [DD/MM/AAAA] |
| **Resultado esperado** | [O que esperávamos] | [O que aconteceu de fato] |
| **A decisão foi boa?** | — | [Sim / Parcialmente / Não] |
| **O que aprendemos** | — | [Insight para decisões futuras] |
| **Ação** | — | [Manter / Ajustar / Reverter] |
```

---

## 9. Bloco: Speed vs Quality Framework

### Template
```markdown
## Quando Decidir Rápido vs Quando Ir Devagar

| Fator | Decidir Rápido | Ir Devagar |
|-------|:---:|:---:|
| Reversibilidade | Fácil de reverter | Difícil/impossível |
| Custo do atraso | Alto (mercado, oportunidade) | Baixo |
| Informação disponível | 70%+ do necessário | < 50% do necessário |
| Impacto em pessoas | Baixo | Alto (demissões, reorg) |
| Consequência de errar | Limitada | Significativa |
| Complexidade | Baixa | Alta (muitas variáveis) |

**Para esta decisão:** [Rápido / Devagar — justificativa]
```

---

## Exemplos de Uso

### Decision Log para Reunião Executiva
```markdown
## Decisões da Semana — C-Level

| # | Decisão | Decisor | Tipo | Próximo Passo |
|---|---------|---------|:---:|--------------|
| 1 | Aprovar budget de R$ 200K para rebrand | CEO | Tipo 1 | Kick-off com agência em 15/03 |
| 2 | Adotar Notion como wiki interna | CTO | Tipo 2 | Migração inicia semana que vem |
| 3 | Pausar hiring de SDRs até Q2 | CRO+CFO | Tipo 2 | Redirecionar budget para marketing |
```

---

## Dicas de Uso
- Documente decisões importantes — "por que fizemos isso?" é a pergunta mais frequente 6 meses depois
- Use frameworks como apoio, não como substituto para julgamento
- A maioria das decisões deveria ser Tipo 2 — decidida rápido e ajustada depois
- Pre-mortem é o exercício mais subutilizado e mais valioso
- Defina quem decide ANTES de discutir opções — evita política
- Revise decisões importantes em 90 dias — aprenda com resultados
- "Disagree and commit" é válido — nem todos precisam concordar, mas todos devem executar
