# Risk Assessment Blocks — Blocos Reutilizáveis para Avaliação de Risco

> Blocos padronizados para identificar, avaliar e comunicar riscos em documentos executivos.

---

## 1. Bloco: Matriz de Risco (Padrão)

```markdown
### Matriz de Riscos — [Contexto]

| # | Risco | Prob. | Impacto | Score | Mitigação | Owner | Status |
|---|-------|:-----:|:-------:|:-----:|-----------|-------|--------|
| R1 | [Descrição] | [A/M/B] | [A/M/B] | [1-9] | [Ação] | [Nome] | [Aberto/Em mitigação/Mitigado] |
| R2 | [Descrição] | [A/M/B] | [A/M/B] | [1-9] | [Ação] | [Nome] | [Status] |
| R3 | [Descrição] | [A/M/B] | [A/M/B] | [1-9] | [Ação] | [Nome] | [Status] |

**Score:** Alto(3) x Alto(3) = 9, Alto x Médio = 6, Médio x Médio = 4, etc.
**Threshold de ação imediata:** Score >= 6
```

---

## 2. Bloco: Heat Map de Riscos

```markdown
### Mapa de Calor de Riscos

|              | Baixo Impacto | Médio Impacto | Alto Impacto |
|:------------:|:---:|:---:|:---:|
| **Alta Prob** | [R5] Amarelo | [R2] Vermelho | [R1] Vermelho |
| **Média Prob** | [R6] Verde | [R4] Amarelo | [R3] Vermelho |
| **Baixa Prob** | Verde | [R7] Verde | [R8] Amarelo |

**Vermelho (Score 6-9):** Ação imediata obrigatória
**Amarelo (Score 3-4):** Monitorar com plano de mitigação
**Verde (Score 1-2):** Aceitar e monitorar periodicamente
```

---

## 3. Bloco: Risco com Impacto Financeiro

```markdown
### Riscos com Quantificação Financeira

| Risco | Probabilidade | Impacto (R$) | Valor Esperado | Custo de Mitigação | Decisão |
|-------|:---:|---:|---:|---:|---------|
| [Risco 1] | [X%] | R$ [X] | R$ [prob x impacto] | R$ [X] | [Mitigar/Aceitar/Transferir] |
| [Risco 2] | [X%] | R$ [X] | R$ [X] | R$ [X] | [Decisão] |
| [Risco 3] | [X%] | R$ [X] | R$ [X] | R$ [X] | [Decisão] |

**Regra:** Mitigar se custo de mitigação < valor esperado do risco
**Exposição total:** R$ [soma dos valores esperados]
```

---

## 4. Bloco: Riscos por Categoria

```markdown
### Riscos Estratégicos
- [Risco de mercado] — [Mitigação]
- [Risco competitivo] — [Mitigação]
- [Risco regulatório] — [Mitigação]

### Riscos Operacionais
- [Risco de execução] — [Mitigação]
- [Risco de dependência] — [Mitigação]
- [Risco de capacidade] — [Mitigação]

### Riscos Financeiros
- [Risco de caixa] — [Mitigação]
- [Risco cambial] — [Mitigação]
- [Risco de concentração de receita] — [Mitigação]

### Riscos de Pessoas
- [Risco de turnover key person] — [Mitigação]
- [Risco de hiring] — [Mitigação]
- [Risco de burnout] — [Mitigação]

### Riscos Tecnológicos
- [Risco de segurança] — [Mitigação]
- [Risco de scalability] — [Mitigação]
- [Risco de vendor lock-in] — [Mitigação]
```

---

## 5. Bloco: Evolução de Riscos (Trending)

```markdown
### Evolução de Riscos — [Período]

| Risco | Score Q Anterior | Score Q Atual | Tendência | Comentário |
|-------|:---:|:---:|:---:|-----------|
| [Risco 1] | [6] | [4] | Melhorando | [Mitigação X surtiu efeito] |
| [Risco 2] | [3] | [6] | Piorando | [Novo contexto aumentou probabilidade] |
| [Risco 3] | [4] | [4] | Estável | [Monitorando] |

**Novos riscos identificados:** [Lista]
**Riscos removidos:** [Lista — por que não são mais relevantes]
```

---

## 6. Bloco: Análise de Risco para Decisão

```markdown
### Análise de Risco — [Nome da Decisão]

**Se fizermos:**
| Risco | Prob | Impacto | Mitigação |
|-------|:---:|:---:|-----------|
| [Risco 1] | [A/M/B] | [A/M/B] | [Plano] |
| [Risco 2] | [A/M/B] | [A/M/B] | [Plano] |

**Se NÃO fizermos:**
| Risco | Prob | Impacto | Consequência |
|-------|:---:|:---:|-------------|
| [Risco de inação 1] | [A/M/B] | [A/M/B] | [O que acontece] |
| [Risco de inação 2] | [A/M/B] | [A/M/B] | [O que acontece] |

**Conclusão:** [Fazer / Não fazer — baseado na análise comparativa de riscos]
```

---

## 7. Bloco: RAID Log (Riscos, Ações, Issues, Dependências)

```markdown
### RAID Log — [Projeto]

| Tipo | Descrição | Status | Owner | Data |
|:----:|-----------|--------|-------|------|
| R | [Risco identificado] | [Aberto] | [Nome] | [Data] |
| A | [Ação pendente] | [Em andamento] | [Nome] | [Data] |
| I | [Issue/Problema ativo] | [Bloqueando] | [Nome] | [Data] |
| D | [Dependência externa] | [Aguardando] | [Nome] | [Data] |
```

---

## 8. Bloco: Triggers e Early Warning

```markdown
### Early Warning Indicators

| Risco | Trigger / Sinal de Alerta | Threshold | Monitoramento | Ação se Triggered |
|-------|--------------------------|-----------|--------------|-------------------|
| [Risco 1] | [Indicador observável] | [Valor limite] | [Como monitorar] | [Ação imediata] |
| [Risco 2] | [Indicador] | [Threshold] | [Monitoramento] | [Ação] |
| [Risco 3] | [Indicador] | [Threshold] | [Monitoramento] | [Ação] |
```

---

## Exemplos de Uso

**Para Strategy Doc:** Blocos 1 (Matriz) + 4 (Por categoria) + 8 (Triggers)
**Para Board Deck:** Blocos 2 (Heat map) + 5 (Evolução) + 3 (Financeiro)
**Para Projeto:** Blocos 7 (RAID) + 1 (Matriz) + 8 (Triggers)
**Para Decisão:** Bloco 6 (Análise comparativa) + 3 (Financeiro)

---

## Dicas de Uso
- Risco sem owner é risco ignorado — sempre atribua
- Revise riscos a cada ciclo (sprint, mês, trimestre) — novos riscos surgem continuamente
- Quantifique quando possível — "risco alto" é subjetivo, "R$ 500K de impacto" é concreto
- Inclua riscos de INAÇÃO — frequentemente maiores que riscos de ação
- Triggers são mais úteis que probabilidades — defina sinais observáveis
