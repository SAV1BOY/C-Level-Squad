# Slack Executive Guidelines — Comunicação Assíncrona C-Level

## Princípio Central

Slack é a comunicação em tempo real da empresa. Para o C-Level, é ferramenta de
alinhamento rápido, decisão assíncrona e visibilidade. Sem disciplina, vira ruído.
Com disciplina, é o sistema nervoso da organização.

---

## Estrutura de Canais Executivos

### Canais Recomendados

| Canal | Propósito | Quem | Frequência |
|-------|-----------|------|-----------|
| #c-level | Decisões e alinhamento executivo | C-Level only | Diário |
| #leadership | Comunicação com VPs e Directors | C-Level + VPs | Diário |
| #company-updates | Anúncios para toda a empresa | C-Level → All | Semanal |
| #metrics-dashboard | Métricas automáticas e commentary | C-Level + leads | Diário (auto) |
| #incidents | Incidentes ativos | Relevant stakeholders | Quando necessário |
| #decisions-log | Registro de decisões tomadas | C-Level + VPs | Conforme decisões |
| #parking-lot | Temas que precisam de follow-up | C-Level | Semanal cleanup |

### Regras de Canal

1. **#c-level é para decisões, não para chat.** Conversa casual vai para DM.
2. **#leadership é para cascata de informação.** O que o C-Level decide, VPs precisam saber.
3. **#company-updates é curado.** Cada post é revisado antes de publicar.
4. **#incidents tem protocolo.** Formato padronizado, updates regulares.
5. **#decisions-log é append-only.** Não editar decisões passadas — adicionar updates.

---

## Formato de Mensagem Executiva no Slack

### Mensagem de Decisão
```
📌 DECISÃO: [O que foi decidido]
Owner: [Nome]
Deadline: [Data]
Contexto: [1 frase]
Thread para detalhes →
```

### Mensagem de Status
```
📊 [PROJETO/ÁREA] Status: [Green/Yellow/Red]
Headline: [1 frase]
Metric: [Atual vs Target]
Action: [Se necessário]
```

### Mensagem de Ask
```
🙋 PRECISO DE: [O que]
De quem: [Nome ou role]
Até quando: [Data/hora]
Contexto: [1 frase — detalhes na thread]
```

### Mensagem de FYI
```
ℹ️ FYI: [Tópico]
[2-3 frases de contexto]
Ação: Nenhuma necessária.
```

### Mensagem de Alerta
```
🟡 ALERT: [Tópico]
Situação: [O que está acontecendo]
Impacto: [Quantificado]
Ação: [O que estamos fazendo / precisamos]
Próximo update: [Quando]
```

### Mensagem Crítica
```
🔴 CRITICAL: [Tópico]
[Situação em 2 frases]
War room: #incident-[nome]
@here — resposta necessária
```

---

## Decisões Assíncronas via Slack

### Framework de Async Decision

Para decisões que não precisam de reunião:

```
📌 DECISÃO ASSÍNCRONA — Deadline: [data/hora]

Proposta: [O que proponho — 2-3 frases]
Contexto: [Por que agora — 1-2 frases]
Trade-offs: [O que ganhamos vs perdemos]
Alternativas: [O que mais consideramos]

VOTEM:
✅ Aprovo
⚠️ Aprovo com ressalvas (explique na thread)
❌ Não aprovo (explique na thread)
🤔 Preciso de mais informação (pergunte na thread)

Se não votar até [data/hora], assumo aprovação.
Decision owner: [Nome]
```

### Regras de Async Decision

1. **Deadline claro.** Sem deadline, não é decisão — é discussão.
2. **Silêncio = aprovação.** Declarado explicitamente no post.
3. **Objeções na thread.** Não em DM, não em outro canal.
4. **Decision owner resolve impasses.** Se não há consenso, o owner decide.
5. **Resultado postado em #decisions-log.** Após deadline, decisão é documentada.

---

## Comunicação Urgente vs Não-Urgente

### Não-Urgente (maioria das mensagens)
- Canal público relevante
- Sem @here ou @channel
- Resposta esperada em horário de trabalho
- Use thread para detalhes
- Sem expectativa de resposta imediata

### Urgente (use com moderação)
- @[nome] diretamente + DM se sem resposta em 30 min
- Canal #incidents para incidentes técnicos
- Claramente marcado como urgente no formato
- Phone/WhatsApp se fora de horário

### Regras de @here e @channel
- **@here:** Apenas para ALERT ou CRITICAL. Nunca para FYI.
- **@channel:** Apenas para CRITICAL que afeta todos no canal.
- **@[nome]:** Para requests específicos — preferido sobre @here.
- **Abuso de @here** = cry wolf. Use com extrema moderação.

---

## Thread Discipline

### Regras de Thread

1. **Sempre responda na thread**, não no canal principal.
2. **O post original no canal é o headline.** Detalhes vão na thread.
3. **Thread longa = precisa de reunião.** Se a thread tem mais de 15 mensagens, agende conversa.
4. **Resuma conclusão de thread no canal.** "Thread resolvida: decisão é [X]. Owner: [nome]."
5. **Não inicie novos tópicos dentro de threads.** Crie novo post no canal.

---

## Etiqueta de Slack Executivo

### Timing
- **Responda em horário de trabalho.** Se ler fora do horário, use scheduled send.
- **Não envie mensagens de madrugada.** Cria pressão de disponibilidade.
- **Use o status do Slack.** "Em reunião", "Focado", "Offline" — ajuda a calibrar expectativas.

### Tom
- **Profissional mas humano.** Slack é mais informal que email — ok.
- **Emojis com moderação.** Reações são eficientes (confirma, aprova, agradece sem gerar notificação).
- **Sem sarcasmo por escrito.** Não funciona em texto — cria ambiguidade.

### Produtividade
- **Mute canais que não são relevantes para você.** Cuide do seu feed.
- **Use remind.** `/remind me about this in 2 hours` — para follow-up.
- **Não use Slack para documentação permanente.** Decisões vão para o decision log. Docs vão para o wiki.
- **Batch check.** Não cheque Slack a cada 5 minutos. Defina cadências (ex: a cada hora).

---

## Templates de Reação com Emoji

| Emoji | Significado | Quando usar |
|-------|------------|-------------|
| ✅ | Aprovado / Concordo / Feito | Decisões, confirmações |
| 👀 | Estou olhando / Vou ler | Acknowledge receipt |
| 🙏 | Obrigado / Reconhecimento | Gratidão por contribuição |
| ⏰ | Precisa de atenção / Tempo | Lembretes de deadline |
| 🔥 | Urgente / Prioridade alta | Alertas |
| 🎯 | On target / Exatamente isso | Validação de ideia/direção |
| 📌 | Pinado / Importante | Marcar para referência |
| ➡️ | Next step / Ação necessária | Transição para ação |

---

## Anti-Padrões de Slack Executivo

### Canal como Chat Room
- **Evitar:** 50 mensagens por dia no #c-level com observações casuais.
- **Preferir:** Posts estruturados com detalhes na thread.

### DM para Decisões
- **Evitar:** Tomar decisões em DM que afetam outros.
- **Preferir:** Decisão no canal relevante para visibilidade e registro.

### Slack Substitui Reunião
- **Evitar:** Debates complexos de 30 mensagens no Slack.
- **Preferir:** "Isso precisa de 15 min ao vivo. Agendo para [hora]."

### Notificação Anxiety
- **Evitar:** Esperar resposta imediata para tudo.
- **Preferir:** Deadline claro. Se urgente, escale canal. Se não, espere.

---

## Checklist de Slack Executivo

- [ ] A mensagem está no canal correto?
- [ ] O formato segue o template adequado (Decision/Status/Ask/FYI/Alert)?
- [ ] Detalhes estão na thread, não no canal principal?
- [ ] @here/@channel são usados apenas quando justificado?
- [ ] O tom é profissional e claro?
- [ ] Se é decisão assíncrona, deadline e regra de silêncio estão claros?
- [ ] A mensagem é necessária? (ou poderia esperar para a próxima cadência?)
