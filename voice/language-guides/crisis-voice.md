# Crisis Voice — Comunicação em Crise

## Princípio Central

Em crise, a comunicação é tão crítica quanto a ação. O tom deve ser calmo, factual,
acionável, transparente e empático. Pânico amplifica crise. Silêncio destrói confiança.
A comunicação de crise é um equilíbrio entre velocidade e precisão.

**Mantra: "Situação, contenção, comunicação, ações."**

---

## Os 5 Pilares da Comunicação de Crise

### 1. Calma
O líder é o termômetro emocional da organização. Se o líder demonstra pânico, a organização entra em pânico.

- **Bom:** "Temos uma situação séria. Estamos tratando com prioridade máxima. Aqui está o que sabemos e o que estamos fazendo."
- **Ruim:** "Isso é um desastre! Como isso aconteceu? Quem é o responsável?"

### 2. Factual
Apenas fatos confirmados são comunicados. Especulação em crise é perigoso.

- **Bom:** "Às 14:23, nosso sistema de pagamentos ficou indisponível. Impacto: aproximadamente 2.000 transações não processadas."
- **Ruim:** "Parece que tivemos um problema grave de segurança que pode ter afetado milhares de clientes."

### 3. Acionável
Toda comunicação de crise inclui o que está sendo feito e o que o receptor deve fazer.

- **Bom:** "Engenharia está fazendo rollback do deploy. CS: segurem outbound até resolução. Próximo update em 30 minutos."
- **Ruim:** "Estamos investigando. Atualizaremos quando tivermos mais informações."

### 4. Transparente
Esconder informação em crise destrói confiança de forma irreparável.

- **Bom:** "Dados de 500 clientes foram expostos. Identificamos a causa, corrigimos, e estamos notificando clientes afetados individualmente."
- **Ruim:** "Tivemos um pequeno incidente de segurança que já foi resolvido."

### 5. Empático
Reconhecer o impacto humano — em clientes, no time, em stakeholders.

- **Bom:** "Sabemos que isso afeta a confiança dos nossos clientes em nós. Levamos isso a sério e estamos tomando todas as medidas necessárias."
- **Ruim:** "Esses problemas acontecem em toda empresa de tecnologia."

---

## Fases da Comunicação de Crise

### Fase 1: Detecção e First Response (0-30 min)
**Tom:** Urgente, factual, controlado

```
SITUAÇÃO: [O que aconteceu — fatos confirmados apenas]
IMPACTO: [O que sabemos do impacto — ser honesto sobre o que não sabemos]
CONTENÇÃO: [O que estamos fazendo agora para conter]
PRÓXIMO UPDATE: [Quando — seja específico]
```

Exemplo:
> Situação: Sistema de checkout indisponível desde 14:23.
> Impacto: Estimativa inicial — 500 transações afetadas. Investigando amplitude total.
> Contenção: Time de engenharia acionado. Rollback em andamento.
> Próximo update: 15:00 ou antes se houver resolução.

### Fase 2: Gestão Ativa (30 min - resolução)
**Tom:** Informativo, progresso-oriented, cadenciado

```
STATUS: [Em andamento / Contido / Resolvido]
PROGRESSO: [O que já fizemos]
PENDENTE: [O que falta]
IMPACTO ATUALIZADO: [Revisão com dados mais precisos]
PRÓXIMO UPDATE: [Quando]
```

### Fase 3: Resolução (imediato pós-crise)
**Tom:** Aliviado mas sóbrio, accountable, forward-looking

```
RESOLUÇÃO: [O que foi feito para resolver]
IMPACTO FINAL: [Dados precisos de impacto]
ROOT CAUSE: [Causa raiz identificada ou timeline para identificação]
AÇÕES IMEDIATAS: [O que mudamos imediatamente]
FOLLOW-UP: [Plano de post-mortem com data]
```

### Fase 4: Post-Mortem (1-5 dias depois)
**Tom:** Analítico, sem blame, sistêmico, preventivo

```
TIMELINE: [Sequência detalhada de eventos]
ROOT CAUSE: [Análise profunda da causa raiz]
CONTRIBUTING FACTORS: [Fatores que agravaram]
IMPACT: [Quantificado — clientes, revenue, reputação]
CORRECTIVE ACTIONS: [Com owner e deadline para cada]
PREVENTIVE MEASURES: [O que muda no processo/sistema]
LESSONS LEARNED: [O que aprendemos]
```

---

## Comunicação por Audiência

### Para o Time Interno

- **Tom:** Direto, operacional, suportivo
- **Frequência:** A cada 30 minutos durante crise ativa
- **Canal:** Slack channel dedicado (#incident-[nome])
- Frase: "Aqui está o que sabemos. Aqui está o que estamos fazendo. Aqui está o que precisamos de vocês."

### Para Clientes

- **Tom:** Empático, transparente, acionável
- **Frequência:** No início, na resolução, e no follow-up
- **Canal:** Status page, email, in-app notification
- Frase: "Identificamos um problema que afeta [X]. Estamos trabalhando para resolver com máxima prioridade. Atualizaremos em [tempo]."

### Para o Board

- **Tom:** Conciso, impact-focused, com plano
- **Frequência:** Quando impacto é material
- **Canal:** Email direto do CEO
- Frase: "Incidente de [tipo] às [hora]. Impacto: [quantificado]. Status: [contido/resolvido]. Ações: [resumo]. Post-mortem: [data]."

### Para a Imprensa/Público

- **Tom:** Profissional, cuidadoso, factual
- **Frequência:** Apenas quando necessário
- **Canal:** Comunicado oficial, porta-voz designado
- Frase: "Estamos cientes do incidente e trabalhando para resolução. A proteção dos dados e a experiência dos nossos clientes são nossa prioridade máxima."

### Para Reguladores

- **Tom:** Formal, compliant, detalhado
- **Frequência:** Conforme exigência legal
- **Canal:** Canal oficial de notificação
- Frase: "Notificamos conforme [regulação]. Detalhes do incidente: [relatório completo]."

---

## Frases de Crise por Situação

### Início da Crise
- "Temos um incidente ativo. Classificação inicial: [severidade]. War room ativado."
- "Fatos confirmados: [lista]. Não confirmados: [lista]. Não especulem publicamente."
- "Commander do incidente: [nome]. Todas as comunicações passam por [nome]."

### Durante a Crise
- "Update: [progresso]. Ainda trabalhando em [pendências]. Próximo update: [hora]."
- "Impacto revisado para [cima/baixo]. Dados: [X]. Ações ajustadas: [Y]."
- "Precisamos de [recurso/decisão]. Quem pode liberar isso nos próximos 15 minutos?"

### Resolução
- "Incidente resolvido às [hora]. Sistemas operacionais. Monitoring intensificado por 24h."
- "Impacto total: [dados]. Todos os clientes afetados serão comunicados até [data]."
- "Post-mortem agendado para [data]. Participantes: [lista]."

### Post-Mortem
- "Timeline do incidente: [documento]. Root cause: [X]. Sem buscar culpados — foco em sistema."
- "3 ações corretivas definidas. Cada uma com owner e deadline. Review em 30 dias."
- "O que funcionou bem: [lista]. O que precisa melhorar: [lista]."

---

## Classificação de Severidade

| Nível | Nome | Critério | Comunicação |
|-------|------|----------|-------------|
| SEV-1 | Crítico | Sistema principal down, dados expostos | CEO + Board notificados em 15 min |
| SEV-2 | Alto | Funcionalidade major degradada | VP+ notificados em 30 min |
| SEV-3 | Médio | Funcionalidade minor afetada | Director notificado em 1h |
| SEV-4 | Baixo | Inconveniência, workaround disponível | Registrado, tratado em cadência normal |

---

## O Que NUNCA Fazer em Comunicação de Crise

1. **NUNCA especule.** Só comunique fatos confirmados.
2. **NUNCA blame publicamente.** Post-mortem é blameless.
3. **NUNCA minimize.** Clientes e stakeholders percebem e perdem confiança.
4. **NUNCA fique em silêncio.** Ausência de comunicação é comunicação — de descaso.
5. **NUNCA prometa o que não pode cumprir.** "Nunca mais vai acontecer" é promessa impossível.
6. **NUNCA use jargão com clientes.** "Nosso sistema de redundância falhou" → "Nosso serviço ficou fora do ar."
7. **NUNCA comunique sem plano de ação.** Toda bad news vem com next steps.
8. **NUNCA mude a narrativa.** Consistência entre comunicações é fundamental.

---

## Checklist de Comunicação de Crise

### Primeiros 15 Minutos
- [ ] Incidente classificado (SEV level)?
- [ ] Incident commander designado?
- [ ] Canal de comunicação interna ativado?
- [ ] Stakeholders iniciais notificados?
- [ ] Timer de próximo update definido?

### Durante a Crise
- [ ] Updates cadenciados a cada 30 minutos?
- [ ] Fatos separados de especulação?
- [ ] Impacto sendo quantificado continuamente?
- [ ] Comunicação com clientes iniciada (se aplicável)?
- [ ] Log de decisões sendo mantido?

### Pós-Resolução
- [ ] Comunicação de resolução enviada a todos os stakeholders?
- [ ] Post-mortem agendado (dentro de 5 dias)?
- [ ] Clientes afetados notificados individualmente?
- [ ] Ações corretivas documentadas com owners e deadlines?
- [ ] Lessons learned compartilhadas com a organização?
