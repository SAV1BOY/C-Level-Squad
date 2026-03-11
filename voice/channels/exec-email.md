# Executive Email — Templates e Guidelines

## Princípio Central

Email executivo é uma ferramenta de decisão, não de conversação. Cada email tem
subject line preciso, estrutura BLUF, call-to-action claro e comprimento adequado.
Se não cabe em uma tela, está longo demais.

---

## Anatomia do Email Executivo

### Estrutura Padrão

```
SUBJECT: [Tipo] [Tópico] — [Ação necessária ou status]
BODY:
  Linha 1-2: Bottom line (conclusão/pedido/decisão)
  Linha 3-5: Contexto essencial (dados, evidência)
  Linha 6-8: Opções ou recomendação (se aplicável)
  Última linha: CTA (o que preciso de você, até quando)
```

---

## Subject Lines — A Porta de Entrada

### Regras de Subject Line

1. **Inclua o tipo.** [Decision], [FYI], [Action Needed], [Update], [Alert]
2. **Seja específico.** Não "Update", sim "Q2 Revenue Update — 15% below target"
3. **Inclua deadline se houver.** "[Action by 14/03] Budget approval for ML hire"
4. **Máximo 60 caracteres** para funcionar em mobile

### Exemplos de Subject Line

| Ruim | Bom |
|------|-----|
| "Thoughts?" | "[Decision by Friday] Series B terms — need Board input" |
| "Quick question" | "[Action needed] Approve hiring plan — 3 positions" |
| "Update" | "[FYI] Competitor Y launched AI analytics" |
| "Important" | "[Alert] Top enterprise client signaling churn risk" |
| "Re: Re: Re: Meeting" | "[Decision] New meeting cadence proposal" |

---

## Templates por Tipo de Email

### 1. Decision Request

```
Subject: [Decision by DD/MM] [Tópico]

Decisão necessária: [O que precisa ser decidido, em uma frase]
Deadline: [Data]

Contexto: [2-3 frases — por que agora, o que está em jogo]

Opções:
A) [Descrição] — Custo: [X]. Benefício: [Y]. Risco: [Z].
B) [Descrição] — Custo: [X]. Benefício: [Y]. Risco: [Z].

Recomendação: [Opção] — porque [razão em uma frase].

Para aprovar, responda "approve" ou "approve with conditions."
Se não responder até [data], seguimos com a recomendação.
```

**Exemplo:**
```
Subject: [Decision by 14/03] Increase ML engineer comp band by 15%

Decisão necessária: Aumentar banda salarial para ML engineers em 15%.
Deadline: Quinta 17h — temos oferta pendente para candidato top.

Contexto: Perdemos 3 candidatos ML nos últimos 2 meses por compensation.
Mercado se moveu 15-20% para cima neste role. Sem ajuste, não contratamos.

Opções:
A) Aumentar 15% — Custo: ~$90K/ano. Benefício: competitivos no mercado.
B) Manter atual + equity kicker — Custo: ~$50K. Risco: ainda abaixo de mercado.
C) Manter atual — Custo: $0. Risco: não contratamos ML talent.

Recomendação: A — o custo de não ter ML engineers é maior que $90K/ano.

CFO: approve / reject / approve with conditions? Até quinta 17h.
```

### 2. Status Update

```
Subject: [Update] [Projeto/Área] — [Status em 3 palavras]

Headline: [Uma frase que resume o status]

Métricas:
- [KPI 1]: [Atual] vs [Target] — [On/At/Off track]
- [KPI 2]: [Atual] vs [Target] — [On/At/Off track]
- [KPI 3]: [Atual] vs [Target] — [On/At/Off track]

Highlights: [Top 1-2 wins]
Risks: [Top 1-2 riscos com mitigação]
Decisions needed: [Se houver — senão, omitir]
Next update: [Data]
```

### 3. FYI / Informational

```
Subject: [FYI] [Tópico]

Headline: [Uma frase — o que e por que importa]
Detalhes: [2-3 frases de contexto]
Implicação: [O que isso significa para nós]
Ação: Nenhuma necessária. Disponível para perguntas.
```

### 4. Alert

```
Subject: [Alert] [Tópico] — [Ação ou awareness]

Situação: [O que está acontecendo — fatos confirmados]
Impacto: [Quantificado se possível]
Ação em andamento: [O que já estamos fazendo]
Preciso de: [Se aplicável]
Próximo update: [Quando]
```

### 5. Ask / Request

```
Subject: [Request] [O que preciso] — [De quem] — [Até quando]

O que preciso: [Específico]
Por que: [Contexto — 1-2 frases]
Deadline: [Data]
Formato: [Como quero receber — doc, verbal, email]
Se não for possível: [Alternativa ou impacto]
```

---

## Regras de Ouro do Email Executivo

### 1. Comprimento
- **Executive summary:** 5-7 linhas
- **Decision request:** 10-15 linhas
- **Status update:** 10-20 linhas
- **Regra de ouro:** Se não cabe em uma tela de celular, está longo demais.

### 2. Formatação
- **Bullet points** sobre parágrafos longos
- **Bold** para conceitos-chave (com moderação — máximo 3-4 por email)
- **Números** alinhados para fácil scanning
- **Whitespace** entre seções para respiração visual

### 3. Destinatários
- **To:** Quem precisa agir
- **CC:** Quem precisa saber (sem ação esperada)
- **BCC:** Quase nunca. Se precisa esconder destinatários, repense.
- **Regra:** Menos é mais. Se tem mais de 5 pessoas no To:, provavelmente ninguém vai agir.

### 4. Reply vs New Thread
- **Reply:** Quando é continuação direta da conversa.
- **New thread:** Quando o tópico mudou, a decisão mudou, ou a audiência mudou.
- **Regra:** Se o subject line original não faz mais sentido, new thread.

### 5. Timing
- **Envie em horário de trabalho.** Email fora de horário cria expectativa de disponibilidade.
- **Se é urgente, não é email.** Use Slack, phone, ou SMS.
- **Programe para manhã.** Emails enviados pela manhã têm 30% mais engagement.

---

## Erros Comuns a Evitar

### Email sem CTA
- **Ruim:** "Queria compartilhar essa atualização com vocês." (E daí?)
- **Bom:** "FYI — nenhuma ação necessária. Relevante para planejamento de Q3."

### Reply All Desnecessário
- **Regra:** Antes de reply all, pergunte: "Todos na lista precisam ver minha resposta?"

### Email como Chat
- **Ruim:** 15 replies de uma linha debatendo.
- **Bom:** "Isso precisa de conversa. Agendem 15 min — [nome] facilita."

### Passive-Aggressive por Email
- **Ruim:** "Conforme mencionado anteriormente..." ou "Por favor, veja abaixo..."
- **Bom:** Releia o email antes de enviar. Se parece passivo-agressivo, provavelmente é.

### Forward sem Contexto
- **Ruim:** "FYI" com forward de 20 emails.
- **Bom:** "Resumo do thread abaixo: [2 frases]. Relevante porque [motivo]. Ação: [se houver]."

---

## Templates de Resposta Rápida

### Aprovar
```
Aprovado. Pode seguir. Qualquer mudança de scope, me avise.
```

### Aprovar com Condições
```
Aprovado, com uma condição: [condição]. Se isso mudar o timeline, me informe.
```

### Rejeitar
```
Não aprovo neste momento. Motivo: [razão]. Alternativa: [sugestão].
Disponível para discutir se precisar.
```

### Delegar
```
[Nome] é a melhor pessoa para isso. Copiando. [Nome], contexto: [1 frase].
```

### Pedir Mais Info
```
Preciso de mais info para decidir: [lista do que falta].
Pode trazer até [data]?
```

### Acknowledge
```
Recebido. Obrigado pelo update. Nenhuma ação necessária da minha parte.
```

---

## Checklist de Email Executivo

- [ ] Subject line tem tipo, tópico e ação?
- [ ] BLUF está na primeira linha?
- [ ] Comprimento é adequado ao tipo?
- [ ] CTA é claro (ou explicitamente "nenhuma ação")?
- [ ] Destinatários são só os necessários?
- [ ] Formatação facilita scanning (bullets, bold, whitespace)?
- [ ] Tom é profissional e claro (sem passivo-agressividade)?
- [ ] Timing é adequado (horário de trabalho, não urgente)?
- [ ] Se urgente: deveria ser email ou outro canal?
