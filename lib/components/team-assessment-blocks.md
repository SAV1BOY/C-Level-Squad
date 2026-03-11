# Team Assessment Blocks — Blocos Reutilizáveis para Avaliação de Time

> Blocos padronizados para avaliar saúde, performance e desenvolvimento de times.
> Use em reviews trimestrais, board decks, planejamento de pessoas e 1:1s com liderança.

---

## 1. Bloco: Health Check do Time

### Template
```markdown
## Health Check — Time [Nome]

| Dimensão | Score (1-5) | Tendência | Comentário |
|----------|:-----------:|:---------:|------------|
| Entrega / Velocidade | [1-5] | [Melhorando/Estável/Piorando] | [Contexto] |
| Qualidade | [1-5] | [Tendência] | [Contexto] |
| Colaboração interna | [1-5] | [Tendência] | [Contexto] |
| Moral / Engajamento | [1-5] | [Tendência] | [Contexto] |
| Aprendizado / Crescimento | [1-5] | [Tendência] | [Contexto] |
| Alinhamento com estratégia | [1-5] | [Tendência] | [Contexto] |
| Clareza de papéis | [1-5] | [Tendência] | [Contexto] |
| Processos e ferramentas | [1-5] | [Tendência] | [Contexto] |

**Score geral:** [X.X / 5.0]
**Áreas de atenção:** [Top 2 dimensões com score mais baixo]
```

---

## 2. Bloco: Métricas de People

### Template
```markdown
## Métricas de People — [Período]

| Métrica | Valor | Meta | Var | Benchmark |
|---------|-------|------|-----|-----------|
| Headcount total | [N] | [N] | [+/- N] | — |
| Turnover voluntário (anualizado) | [X%] | [<X%] | [+/- X pp] | [Mercado: X%] |
| Turnover involuntário | [X%] | — | [+/- X pp] | — |
| eNPS | [Score] | [>X] | [+/- N] | [Benchmark] |
| Tempo médio para contratar | [X dias] | [<X dias] | [+/- X] | — |
| Taxa de aceitação de ofertas | [X%] | [>X%] | [+/- X pp] | — |
| Vagas abertas (aging > 60 dias) | [N] | [<N] | [+/- N] | — |
| Diversidade (gênero liderança) | [X%] | [>X%] | [+/- X pp] | — |
```

---

## 3. Bloco: Mapa de Competências

### Template
```markdown
## Mapa de Competências — Time [Nome]

| Competência | Nível Atual | Nível Necessário | Gap | Plano |
|------------|:-----------:|:----------------:|:---:|-------|
| [Comp. 1 — ex: Go/Python] | [Intermediário] | [Avançado] | [Sim] | [Treinamento + mentoria] |
| [Comp. 2 — ex: System Design] | [Avançado] | [Avançado] | [Não] | [Manter] |
| [Comp. 3 — ex: ML/AI] | [Básico] | [Intermediário] | [Sim] | [Contratação + curso] |
| [Comp. 4 — ex: Leadership] | [Intermediário] | [Avançado] | [Sim] | [Coaching externo] |

**Competências críticas sem cobertura:** [Listar]
**Bus factor (competência em 1 pessoa):** [Listar áreas de risco]
```

---

## 4. Bloco: Performance Distribution (9-Box)

### Template
```markdown
## Distribuição de Performance — Time [Nome]

| | Baixo Potencial | Médio Potencial | Alto Potencial |
|---|:---:|:---:|:---:|
| **Alta Performance** | Especialista Consistente: [N] | Core Player: [N] | Estrela / HiPo: [N] |
| **Média Performance** | Risco / Atenção: [N] | Sólido / Confiável: [N] | Promessa / Investir: [N] |
| **Baixa Performance** | Desligamento / PIP: [N] | Coaching Urgente: [N] | Potencial Bloqueado: [N] |

**Distribuição saudável esperada:** ~20% Estrelas, ~60% Core/Sólido, ~10% Promessas, ~10% Atenção
**Distribuição atual:** [Análise se está saudável ou distorcida]
```

---

## 5. Bloco: Organograma com Insights

### Template
```markdown
## Estrutura e Insights — Time [Nome]

| Papel | Nome | Nível | Tempo de Casa | Performance | Flight Risk | Notas |
|-------|------|-------|:---:|:---:|:---:|-------|
| [Tech Lead] | [Nome] | [Sênior+] | [X anos] | [Excepcional] | [Baixo] | [Key person] |
| [Engineer] | [Nome] | [Pleno] | [X anos] | [Atende] | [Alto] | [Insatisfeito com salário] |
| [Engineer] | [Nome] | [Júnior] | [X meses] | [Acima] | [Baixo] | [Crescendo rápido] |

**Span of control (ratio gestor:IC):** [1:X]
**Tempo médio de casa:** [X anos]
**% do time com < 6 meses:** [X%] (alto = risco de produtividade)
```

---

## 6. Bloco: Succession Planning

### Template
```markdown
## Planejamento de Sucessão

| Posição Crítica | Ocupante Atual | Successor #1 | Readiness | Successor #2 | Readiness |
|----------------|---------------|-------------|:---------:|-------------|:---------:|
| [CTO] | [Nome] | [Nome] | [Pronto / 6m / 12m+] | [Nome] | [Readiness] |
| [VP Eng] | [Nome] | [Nome] | [Readiness] | [Externo necessário] | [N/A] |
| [Tech Lead Core] | [Nome] | [Nome] | [Readiness] | [Nome] | [Readiness] |

**Posições sem sucessor identificado:** [Listar — risco crítico]
**Ações de desenvolvimento para sucessores:** [Listar top 3]
```

---

## 7. Bloco: Engajamento e Satisfação

### Template
```markdown
## Resultados de Engajamento — [Período da Pesquisa]

| Dimensão | Score | Var vs Anterior | Benchmark | Ação |
|----------|:-----:|:--------------:|:---------:|------|
| Engajamento geral | [X/10] | [+/- X] | [X/10] | [Ação se necessário] |
| Confiança na liderança | [X/10] | [+/- X] | [X/10] | [Ação] |
| Crescimento profissional | [X/10] | [+/- X] | [X/10] | [Ação] |
| Compensação e benefícios | [X/10] | [+/- X] | [X/10] | [Ação] |
| Work-life balance | [X/10] | [+/- X] | [X/10] | [Ação] |
| Ferramentas e ambiente | [X/10] | [+/- X] | [X/10] | [Ação] |

**eNPS:** [Score] ([Promotores X% / Neutros Y% / Detratores Z%])
**Taxa de resposta:** [X%] (aceitável: >75%)
**Top verbatim positivo:** "[Citação representativa]"
**Top verbatim negativo:** "[Citação representativa]"
```

---

## 8. Bloco: Plano de Contratação

### Template
```markdown
## Plano de Contratação — [Período]

| Vaga | Nível | Prioridade | Status | Pipeline | ETA | Justificativa |
|------|-------|:---------:|--------|:--------:|:---:|--------------|
| [Vaga 1] | [Sênior] | [P0] | [Entrevistando] | [N candidatos] | [Data] | [Por que é necessário] |
| [Vaga 2] | [Pleno] | [P1] | [Sourcing] | [N] | [Data] | [Justificativa] |
| [Vaga 3] | [Lead] | [P0] | [Oferta enviada] | [1] | [Data] | [Justificativa] |

**Budget de contratação:** R$ [X] (restante do período)
**Custo por contratação médio:** R$ [X]
**Bottleneck atual:** [O que está travando — ex: "poucos candidatos seniores no mercado"]
```

---

## Exemplos de Uso

### Para Board Deck (resumo de People)
```markdown
## People & Org

| Métrica | Q Anterior | Q Atual | Meta |
|---------|-----------|---------|------|
| Headcount | 163 | 185 | 190 |
| Turnover vol. | 12% | 14% | <15% |
| eNPS | 42 | 38 | >40 |
| Vagas abertas | 15 | 22 | — |

**Contratações-chave:** VP Sales (iniciou), 3 Senior Engineers
**Risco:** eNPS em queda — investigar com pulse survey focado
```

---

## Dicas de Uso
- Métricas de people são leading indicators — turnover alto hoje é receita menor amanhã
- Bus factor = 1 é risco inaceitável para qualquer competência crítica
- eNPS em queda é sinal de alerta antes do turnover subir — aja proativamente
- Flight risk deve ser avaliado para todos os high performers — não espere a surpresa
- Succession planning não é só para C-Level — faça para cada posição crítica
- Dados de people são sensíveis — controle acesso e anonimize quando possível
