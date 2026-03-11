# Executive Clarity Style Guide

## Princípio Central

Comunicação executiva é sobre clareza, não complexidade. Cada palavra deve ganhar seu lugar.
Bottom-line up front. Voz ativa. Específico sobre genérico. Sem jargão desnecessário.

---

## Regra #1: Bottom-Line Up Front (BLUF)

A conclusão vem primeiro. O contexto vem depois, para quem precisar.

### Estrutura BLUF

```
CONCLUSÃO: [O que queremos/recomendamos/decidimos]
CONTEXTO: [Por que isso importa agora]
DADOS: [Evidências que suportam]
AÇÃO: [O que precisa acontecer]
```

### Exemplo Bom
> Revenue Q2 ficou 15% abaixo do target. Root cause: conversion rate caiu em enterprise.
> Recomendação: realocar 3 AEs para enterprise e ajustar pricing tier.
> Decisão necessária até sexta.

### Exemplo Ruim
> Queria compartilhar uma atualização sobre como as coisas estão indo no Q2. Tivemos
> alguns desafios interessantes e o time tem trabalhado muito para superar obstáculos...

---

## Regra #2: Voz Ativa Sempre

Voz passiva esconde responsabilidade. Voz ativa cria ownership.

| Passiva (evitar) | Ativa (preferir) |
|-------------------|-------------------|
| "Foi decidido que..." | "O CEO decidiu que..." |
| "O projeto será entregue..." | "Maria entrega o projeto dia 15." |
| "Erros foram cometidos..." | "Erramos na estimativa de demand." |
| "O budget foi aprovado..." | "O CFO aprovou o budget." |
| "As metas serão revisadas..." | "Revisamos as metas na segunda." |

---

## Regra #3: Específico sobre Genérico

Generalidades não movem organizações. Especificidade sim.

| Genérico (evitar) | Específico (preferir) |
|---------------------|------------------------|
| "Melhorar a experiência" | "Reduzir time-to-value de 45 para 21 dias" |
| "Aumentar vendas" | "Crescer ARR de $5M para $7M até dezembro" |
| "Em breve" | "Até 15 de março" |
| "Alguns clientes" | "23 clientes enterprise (12% da base)" |
| "Investir mais" | "Aumentar budget de marketing em $200K" |
| "Melhorar performance" | "Reduzir P99 latency de 800ms para 200ms" |

---

## Regra #4: Eliminar Jargão Desnecessário

Jargão cria barreira. Use linguagem que qualquer executivo entende.

| Jargão | Alternativa clara |
|--------|-------------------|
| "Synergize cross-functional capabilities" | "Times de vendas e produto trabalham juntos" |
| "Leverage our core competencies" | "Usar o que fazemos de melhor" |
| "Move the needle" | "Impactar [métrica específica]" |
| "Low-hanging fruit" | "Quick wins com impacto imediato" |
| "Circle back" | "Retomo na quinta com a resposta" |
| "Take it offline" | "Discutimos isso separadamente — eu e João, amanhã às 10h" |
| "Deep dive" | "Análise detalhada" |
| "Boil the ocean" | "Escopo muito amplo — precisamos focar" |

### Exceção: Technical Terms
Termos técnicos com significado preciso são aceitáveis quando a audiência é técnica:
SLO, API, LTV, CAC, ARR, MRR, NPS, P99 — esses são vocabulário compartilhado que acelera comunicação.

---

## Regra #5: Uma Ideia por Frase

Frases longas com múltiplas ideias diluem o impacto.

### Ruim
> Dado que o mercado está em consolidação e nossos competidores estão investindo
> pesadamente em AI, e considerando que nosso runway é de 18 meses, precisamos
> decidir se vamos buscar funding agora ou cortar custos, sendo que cada opção
> tem implicações diferentes para o time e para o produto.

### Bom
> O mercado está consolidando. Competidores investem pesado em AI. Nosso runway: 18 meses.
> Duas opções: buscar funding ou cortar custos. Cada uma tem implicações distintas para
> time e produto. Recomendação: buscar funding agora, enquanto temos leverage.

---

## Regra #6: Números Falam

Quantifique sempre que possível. Números criam objetividade e credibilidade.

### Sem números (fraco)
> O produto está crescendo bem e os clientes estão satisfeitos.

### Com números (forte)
> Produto: +35% em users ativos MoM. NPS: 72 (meta: 60). Churn: 2.1% (meta: 3%).

---

## Regra #7: Estrutura Visual

Paredes de texto são inimigas da compreensão executiva. Use estrutura visual.

### Ferramentas de Estrutura
- **Bullet points** para listas de itens paralelos
- **Numeração** para sequências ou prioridades
- **Tabelas** para comparações
- **Negrito** para conceitos-chave (com moderação)
- **Headers** para separar seções

### Comprimento Ideal por Formato
| Formato | Comprimento | Estrutura |
|---------|------------|-----------|
| Slack message | 3-5 linhas | BLUF + ação |
| Email executivo | 5-10 linhas | BLUF + contexto + ação |
| Status update | 10-15 linhas | Métricas + blockers + ações |
| Decision memo | 1-2 páginas | Contexto + opções + recomendação |
| Board report | 3-5 páginas | Narrative + data + asks |

---

## Regra #8: Call-to-Action Explícito

Toda comunicação executiva termina com clareza sobre o que o receptor deve fazer.

| Sem CTA (fraco) | Com CTA (forte) |
|-----------------|-----------------|
| "Queria compartilhar essa atualização." | "Preciso de aprovação do budget até sexta." |
| "O que acham?" | "Recomendo opção B. Objeções até quinta 18h. Sem objeção, seguimos." |
| "Segue o relatório." | "Key finding: churn subiu 20%. Ação recomendada: reunião de emergência amanhã. Confirme presença." |

---

## Framework de Revisão: O Teste "CLEAR"

Antes de enviar qualquer comunicação executiva, aplique:

- **C** — Concisa? Cada palavra ganha seu lugar?
- **L** — Lógica? A estrutura faz sentido? BLUF está no topo?
- **E** — Específica? Há números, nomes, datas?
- **A** — Acionável? O receptor sabe o que fazer?
- **R** — Relevante? Tudo que está ali precisa estar?

---

## Exemplos Completos

### Email Executivo — Exemplo
```
Subject: Revenue Q2 at risk — decisão necessária até sexta

Revenue Q2: $1.2M (target: $1.5M — 80% on track).
Root cause: enterprise conversion caiu de 25% para 15%.

Recomendação: realocar 3 AEs de mid-market para enterprise.
Impacto esperado: recover $200K em pipeline este mês.
Trade-off: mid-market pipeline perde 15% de velocity.

Preciso de aprovação do VP Sales e CFO até sexta 17h.
Sem resposta, assumo aprovação e implemento segunda.
```

### Slack Update — Exemplo
```
🔴 Incident: Payment system down desde 14:23
Impact: ~500 transactions queued
Status: Eng investigating. ETA fix: 30 min.
Action: CS team — hold outbound calls until resolved.
Next update: 15:00 ou quando resolvido.
```

### Decision Memo — Estrutura
```
DECISÃO NECESSÁRIA: [Uma frase]
DEADLINE: [Data]
CONTEXTO: [2-3 frases]
OPÇÕES:
  A) [Descrição] — Prós: [X]. Contras: [Y]. Custo: [Z].
  B) [Descrição] — Prós: [X]. Contras: [Y]. Custo: [Z].
  C) [Descrição] — Prós: [X]. Contras: [Y]. Custo: [Z].
RECOMENDAÇÃO: [Opção] — porque [razão em uma frase].
RISCOS: [Principais riscos da opção recomendada com mitigação].
NEXT STEPS: [Se aprovado, quem faz o quê até quando].
```

---

## Checklist de Estilo Executivo

- [ ] BLUF no topo?
- [ ] Voz ativa?
- [ ] Específico com números e datas?
- [ ] Sem jargão desnecessário?
- [ ] Uma ideia por frase?
- [ ] CTA explícito?
- [ ] Estrutura visual (bullets, headers)?
- [ ] Comprimento adequado ao formato?
- [ ] Passou no teste CLEAR?
