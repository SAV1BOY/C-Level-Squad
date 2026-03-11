# Executive Summary Blocks — Blocos Reutilizáveis para Resumos Executivos

> Blocos padronizados para criar resumos executivos claros e impactantes.
> Um bom executive summary permite que o leitor tome uma decisão sem ler o documento inteiro.

---

## 1. Bloco: Abertura de Status (TL;DR)

### Propósito
Comunicar estado geral e principais destaques em formato ultra-compacto.

### Template

```markdown
## TL;DR

**Status geral:** [Verde / Amarelo / Vermelho]

1. **[Destaque positivo]:** [Métrica ou fato em uma frase]
2. **[Destaque de atenção]:** [Métrica ou fato que requer ação]
3. **[Próximo passo crítico]:** [Ação mais importante com prazo]
```

### Variantes

**Para board update:**
```markdown
**Estado do Negócio:** [Saudável / Atenção / Crítico]
- Receita: R$ [X]M ([+/- X%] vs plan) | Runway: [X] meses
- Destaque: [Principal conquista do período]
- Risco: [Principal preocupação]
- Pedido ao board: [O que precisa de aprovação]
```

**Para update de projeto:**
```markdown
**Projeto [Nome] — Status: [On Track / At Risk / Blocked]**
- Progresso: [X%] concluído | Prazo: [on time / X dias atrasado]
- Conquista: [Principal entrega do período]
- Bloqueio: [Principal impedimento — ação necessária de quem]
```

**Para comunicação de crise:**
```markdown
**Situação: [Título da crise]**
- Status: [Em andamento / Sob controle / Resolvida]
- Impacto: [N clientes / R$ X / X horas de indisponibilidade]
- Ação imediata: [O que estamos fazendo agora]
- Próxima atualização: [Data/hora]
```

---

## 2. Bloco: Contexto e Motivação

### Propósito
Fornecer contexto mínimo para que o leitor entenda por que este documento existe.

### Template

```markdown
## Contexto

[Empresa/Time] enfrenta [problema/oportunidade] que [impacto quantificado]. 
Este documento propõe [solução/decisão] com investimento de [R$ X] e 
retorno esperado de [R$ Y / X% de melhoria] em [prazo].
```

### Variantes

**Contexto orientado a problema:**
```markdown
**Problema:** [Descrição em 1-2 frases]
**Impacto atual:** [Métrica — custo, tempo, perda]
**Causa raiz:** [Por que o problema existe]
**Urgência:** [Por que precisa ser resolvido agora]
```

**Contexto orientado a oportunidade:**
```markdown
**Oportunidade:** [Descrição em 1-2 frases]
**Tamanho da oportunidade:** [R$ X / N clientes / X% do mercado]
**Janela de oportunidade:** [Por que agora — o que muda se demorarmos]
**Requisitos para capturar:** [O que precisamos investir/mudar]
```

---

## 3. Bloco: Recomendação e Decisão

### Propósito
Apresentar recomendação de forma clara para facilitar tomada de decisão.

### Template

```markdown
## Recomendação

**Decisão solicitada:** [O que precisa ser aprovado/decidido]

**Recomendamos:** [Opção X] porque [razão principal com dado].

| Critério | Opção A | Opção B | Status Quo |
|----------|:---:|:---:|:---:|
| Custo | [R$ X] | [R$ X] | [R$ X] |
| Benefício | [R$ X] | [R$ X] | [R$ X] |
| Risco | [A/M/B] | [A/M/B] | [A/M/B] |
| Prazo | [X meses] | [X meses] | [N/A] |

**Se aprovado, próximo passo:** [Ação imediata]
**Se não aprovado, consequência:** [O que acontece]
```

### Variantes

**Recomendação simples (go/no-go):**
```markdown
**Recomendação:** [Aprovação / Rejeição] do [investimento/projeto/contratação]
- **A favor:** [Argumento 1], [Argumento 2], [Argumento 3]
- **Contra:** [Trade-off 1], [Trade-off 2]
- **Risco residual:** [O que pode dar errado mesmo aprovando]
```

**Recomendação com urgência:**
```markdown
**DECISÃO URGENTE (prazo: [data])**
[Contexto em 2 frases]. Recomendamos [ação] com custo de [R$ X].
Delay de [N dias] resulta em [custo/perda de R$ X].
```

---

## 4. Bloco: Métricas-Chave

### Propósito
Apresentar números essenciais de forma scannable.

### Template

```markdown
## Métricas-Chave

| Métrica | Atual | Meta | Variação | Tendência |
|---------|-------|------|----------|-----------|
| [Métrica 1] | [Valor] | [Valor] | [+/- X%] | [Subindo/Estável/Caindo] |
| [Métrica 2] | [Valor] | [Valor] | [+/- X%] | [Tendência] |
| [Métrica 3] | [Valor] | [Valor] | [+/- X%] | [Tendência] |
```

### Variantes

**Métricas financeiras SaaS:**
```markdown
| ARR | MRR | NRR | Churn | LTV/CAC | Runway |
|-----|-----|-----|-------|---------|--------|
| R$ [X]M | R$ [X]K | [X%] | [X%] | [X.X] | [X] meses |
```

**Métricas de produto:**
```markdown
| DAU | MAU | DAU/MAU | NPS | Retention D7 | Retention D30 |
|-----|-----|---------|-----|-------------|---------------|
| [N]K | [N]K | [X%] | [Score] | [X%] | [X%] |
```

---

## 5. Bloco: Riscos e Mitigações (Compacto)

### Template

```markdown
## Riscos Principais

| # | Risco | Severidade | Status | Ação |
|---|-------|:---------:|--------|------|
| 1 | [Risco em 1 frase] | [Crítico/Alto/Médio] | [Novo/Monitorando/Mitigando] | [Ação em curso] |
| 2 | [Risco] | [Severidade] | [Status] | [Ação] |
| 3 | [Risco] | [Severidade] | [Status] | [Ação] |
```

---

## 6. Bloco: Próximos Passos

### Template

```markdown
## Próximos Passos

| Ação | Owner | Prazo | Dependência |
|------|-------|-------|------------|
| [Ação 1] | [Nome] | [Data] | [Nenhuma / Aprovação de X] |
| [Ação 2] | [Nome] | [Data] | [Dependência] |
| [Ação 3] | [Nome] | [Data] | [Dependência] |
```

---

## Exemplos de Uso Combinado

### Executive Summary de Board Deck
```markdown
## Resumo Executivo — Q2 2026

**Status:** Amarelo — receita on track, churn acima do esperado

1. **ARR atingiu R$ 42M** (+18% QoQ), acima do plan em 3%
2. **Churn MRR subiu para 3.2%** (meta: 2.5%) — plano de ação em execução
3. **Pedido ao board:** Aprovação de R$ 2M para programa de retenção

| ARR | NRR | Churn | Runway | HC |
|-----|-----|-------|--------|----|
| R$ 42M | 112% | 3.2% | 18m | 185 |
```

---

## Dicas de Uso
- Executive summary SEMPRE no topo — muitos leitores param aqui
- Máximo 1 página — se precisou de mais, não é resumo
- Números > narrativa — "crescemos 18%" é mais forte que "tivemos bom crescimento"
- Use status visual (verde/amarelo/vermelho) para scan rápido
- Inclua SEMPRE o "ask" — o que você precisa do leitor
- Teste: alguém que leu só o executive summary consegue tomar a decisão?
