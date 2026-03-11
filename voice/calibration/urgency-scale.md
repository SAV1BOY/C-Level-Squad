# Urgency Scale — Escala de Urgência de Comunicação

## Princípio Central

Nem tudo é urgente. Quando tudo é urgente, nada é urgente. A escala de urgência
define 5 níveis claros para que a organização saiba como reagir a cada tipo de
comunicação. Cada nível tem tom, canal, tempo de resposta e template específicos.

---

## Os 5 Níveis de Urgência

### Nível 1: FYI (Informacional)

**Definição:** Informação útil que não requer ação. O receptor decide se e quando consome.

**Tom:** Casual, informativo, sem pressão.
**Canal:** Email, Slack (canal geral), newsletter interna, wiki.
**Tempo de resposta:** Nenhum esperado. Leia quando puder.
**Frequência de uso:** 60% das comunicações deveriam ser FYI.

**Indicadores:**
- Não muda decisão nenhuma esta semana
- Não tem deadline associado
- É contexto útil, não ação necessária

**Template:**
```
[FYI] [Tópico]

Contexto: [O que aconteceu ou o que é relevante]
Relevância: [Por que isso importa no médio/longo prazo]
Ação: Nenhuma necessária. Disponível para perguntas.
```

**Exemplo:**
> [FYI] Competidor Y lançou feature de AI analytics
> Contexto: Competidor Y anunciou AI-powered analytics para enterprise.
> Relevância: Confirma a tendência do mercado. Nosso lançamento em Q2 está alinhado.
> Ação: Nenhuma. Product team está monitorando.

---

### Nível 2: NEEDS ATTENTION (Requer Atenção)

**Definição:** Algo que merece ser visto e considerado nos próximos dias, mas não é urgente.

**Tom:** Profissional, claro, com contexto suficiente.
**Canal:** Email, Slack (canal relevante), tagged message.
**Tempo de resposta:** 24-48 horas.
**Frequência de uso:** 25% das comunicações.

**Indicadores:**
- Pode impactar planejamento da semana seguinte
- Há uma tendência emergente que precisa ser considerada
- Alguém precisa pensar sobre isso, mas não agir imediatamente

**Template:**
```
[NEEDS ATTENTION] [Tópico]

Situação: [O que está acontecendo]
Impacto potencial: [O que pode acontecer se não dermos atenção]
Sugestão: [O que proponho]
Timeline: [Quando precisamos decidir/agir — não é esta semana]
```

**Exemplo:**
> [NEEDS ATTENTION] Churn em SMB subindo gradualmente
> Situação: Churn mensal em SMB subiu de 3.2% para 3.8% nos últimos 2 meses.
> Impacto potencial: Se tendência continuar, perda de $200K ARR no quarter.
> Sugestão: Análise de cohort para identificar driver. CS team pode liderar.
> Timeline: Proposta de ação até próxima semana. Não é emergência ainda.

---

### Nível 3: NEEDS ACTION THIS WEEK (Ação Necessária esta Semana)

**Definição:** Algo que precisa de decisão ou ação nos próximos 5 dias úteis.

**Tom:** Direto, orientado a ação, deadline claro.
**Canal:** Slack (canal relevante + tag do owner), email com subject claro.
**Tempo de resposta:** Mesmo dia.
**Frequência de uso:** 10% das comunicações.

**Indicadores:**
- Há um deadline real esta semana
- Bloqueia trabalho de outra pessoa/time
- Impacto material se não for tratado nos próximos 5 dias

**Template:**
```
[ACTION NEEDED BY dd/mm] [Tópico]

Situação: [O que precisa acontecer]
Por quê agora: [O que acontece se não agirmos esta semana]
Ação necessária: [Especificamente o que preciso de você]
Deadline: [Data e hora]
Owner: [Quem deve agir]
```

**Exemplo:**
> [ACTION NEEDED BY 14/03] Aprovação de budget para contratação de ML engineer
> Situação: Candidato top aceita oferta se confirmarmos até sexta.
> Por quê agora: Perdemos o candidato se não confirmarmos. Próximo candidato qualificado: 6+ semanas.
> Ação necessária: CFO aprovar compensation package de $180K base + equity.
> Deadline: Quinta 17h.
> Owner: CFO.

---

### Nível 4: ALERT (Alerta)

**Definição:** Algo significativo que requer atenção e possivelmente ação nas próximas 24 horas.

**Tom:** Sério, factual, com plano de ação.
**Canal:** Slack (DM ou canal de leadership), phone/WhatsApp se fora de horário.
**Tempo de resposta:** 2-4 horas.
**Frequência de uso:** 4% das comunicações.

**Indicadores:**
- Impacto financeiro ou reputacional significativo potencial
- Cliente estratégico em risco
- Problema que pode escalar para critical se não tratado
- Regulatory ou legal deadline iminente

**Template:**
```
🟡 [ALERT] [Tópico]

Situação: [O que aconteceu — fatos]
Impacto: [Quantificado se possível]
Ação em andamento: [O que já estamos fazendo]
Decisão necessária: [O que preciso de você — se aplicável]
Deadline: [Quando precisamos agir]
Próximo update: [Quando informo novamente]
```

**Exemplo:**
> 🟡 [ALERT] Cliente enterprise #3 (Acme Corp — $400K ARR) sinalizou churn risk
> Situação: VP of Eng da Acme expressou insatisfação com reliability. Mencionou avaliação de competidores.
> Impacto: $400K ARR em risco (8% do enterprise revenue).
> Ação em andamento: CS Director agendou call com VP amanhã. CTO preparando SLA review.
> Decisão necessária: Autorizar discount de 20% para renewal se necessário? Ou investir em SLA customizado?
> Deadline: Decisão antes da call de amanhã 14h.
> Próximo update: Amanhã 16h pós-call.

---

### Nível 5: CRITICAL (Crítico)

**Definição:** Emergência. Ação imediata necessária. Impacto grave em andamento ou iminente.

**Tom:** Urgente, calmo, factual, protocolo de crise ativado.
**Canal:** Phone call, WhatsApp/SMS, Slack @here/@channel, war room.
**Tempo de resposta:** Imediato (< 30 minutos).
**Frequência de uso:** 1% das comunicações (ou menos).

**Indicadores:**
- Sistema principal down afetando clientes
- Breach de segurança confirmado
- Regulatory violation descoberta
- Incidente que pode gerar cobertura de mídia negativa
- Perda financeira ativa e crescente

**Template:**
```
🔴 [CRITICAL] [Tópico] — Resposta imediata necessária

SITUAÇÃO: [O que está acontecendo — agora]
IMPACTO: [Quantificado — clientes, revenue, risco]
CONTENÇÃO: [O que já estamos fazendo]
PRECISO DE: [O que preciso agora — de quem]
WAR ROOM: [Link/local para coordenação]
PRÓXIMO UPDATE: [Em XX minutos]
```

**Exemplo:**
> 🔴 [CRITICAL] Sistema de pagamentos DOWN — Resposta imediata necessária
> SITUAÇÃO: Stripe integration falhando desde 14:23. Zero transações processadas.
> IMPACTO: ~$50K/hora em transações bloqueadas. Todos os clientes afetados.
> CONTENÇÃO: Eng ativou fallback para processamento manual. On-call investigando.
> PRECISO DE: CTO — decisão sobre rollback vs hotfix. COO — ativar comunicação com clientes.
> WAR ROOM: #incident-payments-20260311
> PRÓXIMO UPDATE: 14:45 (em 15 min).

---

## Matriz de Decisão: Qual Nível Usar?

| Pergunta | Se Sim → |
|----------|----------|
| Há dano ativo acontecendo agora? | CRITICAL |
| Sem ação em 24h, haverá dano significativo? | ALERT |
| Há deadline real esta semana? | ACTION THIS WEEK |
| Alguém precisa considerar isso nos próximos dias? | NEEDS ATTENTION |
| É informação útil sem ação necessária? | FYI |

---

## Regras de Uso

### 1. Não Inflacione Urgência
Marcar tudo como ALERT ou CRITICAL destrói a credibilidade do sistema.
Se você marca algo como CRITICAL e não era, da próxima vez vão ignorar.

### 2. Não Deflacione Urgência
Marcar algo como FYI quando é ALERT por medo de "incomodar" é irresponsável.
Bad news não melhora com o tempo.

### 3. Atualize o Nível
Se um FYI vira NEEDS ATTENTION, comunique a mudança: "Escalando de FYI para NEEDS ATTENTION porque [dados novos]."

### 4. Deescale Também
Quando um CRITICAL é resolvido: "Deescalando de CRITICAL para FYI. Situação resolvida. Post-mortem em [data]."

### 5. Respeite os Canais
Não mande CRITICAL por email. Não mande FYI por phone call. O canal reforça a urgência.

---

## Acordo de Resposta por Nível

| Nível | Resposta esperada | Canal | Horário |
|-------|-------------------|-------|---------|
| FYI | Nenhuma | Email/Slack | Business hours |
| NEEDS ATTENTION | 24-48h | Email/Slack | Business hours |
| ACTION THIS WEEK | Mesmo dia | Slack tagged + email | Business hours |
| ALERT | 2-4h | DM/Slack + phone backup | Extended hours |
| CRITICAL | < 30 min | Phone + Slack + SMS | 24/7 |

---

## Exemplos Adicionais por Área

### Engenharia
- FYI: "Novo framework de testing disponível para experimentar."
- NEEDS ATTENTION: "Tech debt no módulo X está crescendo — sprint de cleanup recomendado."
- ACTION THIS WEEK: "Security patch disponível — precisa deploy até sexta."
- ALERT: "Performance degradation detectada — P99 2x acima do SLO."
- CRITICAL: "Produção down. Zero requests processados."

### Vendas
- FYI: "Competidor mudou pricing — análise disponível no wiki."
- NEEDS ATTENTION: "Win rate caiu 5pp no último mês — vale investigar."
- ACTION THIS WEEK: "Deal de $200K precisa de aprovação de discount até quinta."
- ALERT: "Top-3 cliente sinalizou risco de churn."
- CRITICAL: "Vazamento de pricing confidencial para competidor."

### Financeiro
- FYI: "Taxa de câmbio favorável para operações LATAM."
- NEEDS ATTENTION: "Burn rate acelerou 10% — investigar."
- ACTION THIS WEEK: "Payroll precisa de aprovação até quarta."
- ALERT: "Runway caiu para < 12 meses."
- CRITICAL: "Fraude detectada em sistema de pagamentos."

---

## Checklist de Urgência

- [ ] O nível está correto (nem inflacionado, nem deflacionado)?
- [ ] O canal é adequado ao nível?
- [ ] O template do nível está sendo seguido?
- [ ] O impacto está quantificado?
- [ ] A ação necessária está clara?
- [ ] O deadline está explícito?
- [ ] O owner está identificado?
- [ ] O próximo update está agendado (para ALERT e CRITICAL)?
