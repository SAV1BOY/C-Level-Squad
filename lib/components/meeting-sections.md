# Meeting Sections — Blocos Reutilizáveis para Reuniões

> Referência do C-Level Squad para estruturar reuniões que geram decisões e ações.
> Cada bloco pode ser usado independentemente ou combinado para diferentes tipos de reunião.

---

## 1. Pre-read Block

### Propósito
Garantir que todos os participantes cheguem à reunião com contexto suficiente para contribuir produtivamente, eliminando tempo gasto "educando" durante a reunião.

### Template

```markdown
## Pre-read — [Nome da Reunião] — [Data]

**Tempo estimado de leitura:** [X minutos]
**Deadline para leitura:** [data/hora — mínimo 24h antes da reunião]
**Ação esperada após leitura:** [Ler e anotar perguntas | Comentar no doc | Votar nas opções]

---

### TL;DR
[3 bullets máximo com o essencial]

### Contexto necessário
[1-2 parágrafos com o contexto que o participante precisa para contribuir]

### Dados-chave
[Tabela ou lista com as métricas/informações mais relevantes]

| Métrica          | Atual  | Target | Trend |
|------------------|--------|--------|-------|
| [métrica 1]      | [valor] | [valor] | [↑↓→] |

### Pontos de decisão previstos
Para cada ponto, o participante deve formar uma opinião ANTES da reunião:

1. **[Decisão 1]:** [Contexto em 1 frase]
   - Opção A: [descrição breve]
   - Opção B: [descrição breve]
   - Opção C: [descrição breve]
   → Qual sua posição inicial? [anotar antes da reunião]

2. **[Decisão 2]:** [Contexto]
   → [mesma estrutura]

### Perguntas para reflexão prévia
- [Pergunta 1 que ajuda a chegar preparado]
- [Pergunta 2]

### Documentos de referência (opcionais)
- [Link 1]: [descrição — leia se quiser aprofundar em X]
- [Link 2]: [descrição]
```

### Instruções para o facilitador
- Enviar pre-read no mínimo 24h antes (idealmente 48h para reuniões de decisão)
- Tempo de leitura máximo: metade da duração da reunião
- Verificar quem leu antes da reunião (poll rápido ou checkin tool)
- Se <50% leu, considerar reagendar (reunião sem pre-read = tempo desperdiçado)
- Para decisões importantes: pedir comentários no documento antes da reunião

### Guidance de timing
| Tipo de reunião        | Pre-read enviado | Tempo de leitura max |
|-----------------------|------------------|---------------------|
| Weekly sync (30min)   | 24h antes        | 10min               |
| Decision meeting (45min)| 48h antes      | 20min               |
| Strategy review (2h)  | 72h antes        | 45min               |
| Board meeting (3h)    | 1 semana antes   | 60min               |

---

## 2. Agenda Block

### Propósito
Estruturar o tempo da reunião para maximizar decisões e ações, minimizando discussões improdutivas.

### Template

```markdown
## Agenda — [Nome da Reunião]

**Data:** [YYYY-MM-DD HH:MM-HH:MM]
**Duração total:** [XX min]
**Facilitador:** [agente]
**Notetaker:** [agente]

### Regras da reunião
- Pre-read lido antes de entrar (sem recap ao vivo)
- Laptops fechados (exceto notetaker)
- Tangentes → Parking lot
- Decisões serão registradas em tempo real

| #  | Tempo    | Tópico                     | Tipo        | Owner  | Outcome esperado              |
|----|----------|---------------------------|-------------|--------|-------------------------------|
| 0  | 0-2min   | Check-in + regras         | Setup       | Facil. | Todos presentes e focados     |
| 1  | 2-17min  | [Tópico prioritário]      | Decisão     | [DRI]  | GO/NO-GO decidido             |
| 2  | 17-27min | [Tópico 2]                | Discussão   | [DRI]  | Opções alinhadas              |
| 3  | 27-35min | [Tópico 3]                | Informação  | [DRI]  | Ciência compartilhada         |
| 4  | 35-40min | Action items + Parking lot| Wrap-up     | Facil. | Items registrados com DRI     |
|    | Buffer   | 5 min reservados          |             |        |                               |

### Tipos de tópico e condução

| Tipo        | Objetivo                    | Como conduzir                                |
|-----------|----------------------------|----------------------------------------------|
| Decisão   | Tomar uma decisão          | Apresentar opções → Debate → Poll → Decidir  |
| Discussão | Alinhar perspectivas       | Apresentar contexto → Rodada de input → Síntese |
| Informação| Comunicar algo             | Apresentar em 3-5min → Perguntas breves      |
| Brainstorm| Gerar ideias               | Divergir (silêncio) → Convergir (debate)      |
```

### Instruções para o facilitador
- Colocar o tópico mais importante PRIMEIRO (energia e atenção são maiores no início)
- Alocar tempo proporcional à importância, não à complexidade
- Buffer de 10-15% da duração total para imprevistos
- Se um tópico exceder o tempo: (a) pedir 5 min extras com acordo do grupo, ou (b) mover para follow-up
- No final, sempre perguntar: "Faltou algo que não cobrimos?"

---

## 3. Metrics Review Block

### Propósito
Revisão estruturada de métricas-chave para identificar tendências, anomalias e necessidade de ação.

### Template

```markdown
## Metrics Review — [Período]

**Apresentado por:** [agente]
**Tempo alocado:** [X min]

### Scorecard resumido

| Métrica          | Target   | Atual    | Anterior | Trend | Status |
|------------------|----------|----------|----------|-------|--------|
| [North Star]     | [target] | [valor]  | [valor]  | [↑↓→] | [🟢🟡🔴] |
| [Métrica 2]      | [target] | [valor]  | [valor]  | [↑↓→] | [🟢🟡🔴] |
| [Métrica 3]      | [target] | [valor]  | [valor]  | [↑↓→] | [🟢🟡🔴] |

### Destaques (máximo 3)
1. **[Positivo]:** [Métrica X subiu Y% porque Z]
2. **[Preocupante]:** [Métrica X caiu Y% — hipótese: Z]
3. **[Ação necessária]:** [Métrica X cruzou threshold — proposta: Z]

### Deep dive (apenas métricas fora do target)

#### [Métrica em 🔴]
- **O que aconteceu:** [descrição factual]
- **Por que aconteceu:** [análise de causa raiz]
- **O que estamos fazendo:** [ação em andamento]
- **Quando esperamos melhora:** [projeção com base]
- **Precisamos de ajuda com:** [pedido específico, se houver]
```

### Instruções
- Não perder tempo em métricas verdes — menção de 5 segundos cada é suficiente
- Focar 80% do tempo em métricas amarelas e vermelhas
- Para cada métrica vermelha: causa raiz + ação + timeline
- Evitar "watermelon metrics" (verde por fora, vermelho por dentro): cavar nos leading indicators
- Comparar com base rates quando relevante (ver `base-rate-checks.md`)

### Timing guidance
- 5-8 métricas: 10 minutos para overview + 5 min por deep dive
- 8-15 métricas: 15 minutos para overview + 5 min por deep dive
- >15 métricas: considerar reduzir o scorecard ou dividir em múltiplas reuniões

---

## 4. Decision Point Block

### Propósito
Estruturar o momento da decisão dentro da reunião para garantir processo claro e registro.

### Template

```markdown
## Decision Point — [Título da Decisão]

**Decisor final:** [agente — quem tem a última palavra]
**Tipo:** [Type 1 (irreversível) / Type 2 (reversível)]
**Contexto:** [1 frase — referência ao pre-read para detalhes]

### Opções na mesa

| Opção | Descrição breve              | Prós (top 2)        | Contras (top 2)      |
|-------|------------------------------|---------------------|----------------------|
| A     | [descrição]                  | [pro 1], [pro 2]    | [con 1], [con 2]     |
| B     | [descrição]                  | [pro 1], [pro 2]    | [con 1], [con 2]     |
| C     | [descrição]                  | [pro 1], [pro 2]    | [con 1], [con 2]     |

### Posicionamento (rodada rápida — 1 min por pessoa)
| Agente | Posição | Comentário breve (1 frase) |
|--------|---------|---------------------------|
| CEO    |         |                           |
| COO    |         |                           |
| CMO    |         |                           |
| CTO    |         |                           |
| CIO    |         |                           |
| CAIO   |         |                           |

### Discussão de divergências
[Focar apenas onde há discordância — onde todos concordam, não precisa de debate]
Tempo máximo: [X min]

### Decisão
**Opção escolhida:** [X]
**Decidido por:** [agente]
**Rationale em 1 frase:** [por quê]
**Dissidências registradas:** [agente(s) que discordaram e razão breve]
**Comprometimento:** Todos os agentes se comprometem a executar (disagree and commit)

### Próximos passos imediatos
- [ ] [Ação] — DRI: [agente] — Até: [data]
```

### Instruções para o facilitador
- Votação/posicionamento ANTES do debate (evitar anchoring)
- Se houver consenso imediato, confirmar e seguir (não debater por debater)
- Se houver divisão forte: debate focado em 10-15 min, depois decisão do DRI
- Registrar dissidências — é saudável e importante para revisão futura
- "Disagree and commit" é a regra: após a decisão, todos executam independente de posição pessoal

---

## 5. Action Items Block

### Propósito
Capturar ações concretas com ownership claro para garantir que a reunião gere resultados.

### Template

```markdown
## Action Items — [Reunião] — [Data]

| # | Ação                                    | DRI     | Deadline   | Done when                    | Dep. |
|---|----------------------------------------|---------|------------|------------------------------|------|
| 1 | [Ação específica e verificável]        | [agente]| [data]     | [critério objetivo de done]  | —    |
| 2 | [Ação 2]                               | [agente]| [data]     | [critério]                   | #1   |
| 3 | [Ação 3]                               | [agente]| [data]     | [critério]                   | —    |

### Ações carregadas de reuniões anteriores (pendentes)

| # | Ação original               | DRI     | Deadline original | Status         | Novo deadline |
|---|-----------------------------|---------|-------------------|----------------|---------------|
| P1| [Ação de reunião anterior]  | [agente]| [data]            | [em andamento/bloqueado] | [data] |
```

### Regras de action items
1. **Específico:** "Enviar proposta de budget para AI para CEO com 3 cenários" (não "pensar sobre budget")
2. **Verificável:** Critério de done deve ser binário (feito ou não feito)
3. **Com DRI:** Uma pessoa, não um time ("Maria", não "time de dados")
4. **Com deadline:** Data específica, não "em breve"
5. **Tracking:** Cada reunião começa revisando action items da reunião anterior
6. **Limite:** Máximo 5-7 action items por reunião (se há mais, priorizar)

---

## 6. Parking Lot Block

### Propósito
Capturar tópicos importantes que surgiram durante a reunião mas estão fora do escopo atual, garantindo que não se percam nem desviem a reunião.

### Template

```markdown
## Parking Lot — [Reunião] — [Data]

| # | Tópico                           | Levantado por | Relevante para | Disposição                          |
|---|----------------------------------|---------------|---------------|-------------------------------------|
| 1 | [Tópico que surgiu mas é off-topic]| [agente]     | [agente(s)]   | [Agendar reunião separada / Memo / Slack thread / Próxima reunião] |
| 2 | [Tópico 2]                       | [agente]      | [agente(s)]   | [disposição]                        |
```

### Instruções para o facilitador
- Quando alguém levanta tópico fora da agenda: "Ótimo ponto. Vou colocar no parking lot para não perdermos. Voltamos ao tópico atual?"
- No final da reunião: revisar parking lot e definir disposição para cada item
- Cada item deve ter próximo passo claro (não ficar no limbo)
- Se o mesmo tópico vai para parking lot 3× seguidas → é importante o suficiente para entrar na agenda

---

## 7. Follow-up Block

### Propósito
Documentar tudo que aconteceu na reunião e garantir que informação chegue a quem precisa.

### Template

```markdown
## Follow-up — [Reunião] — [Data]

**Enviado em:** [data/hora — idealmente <2h após a reunião]
**Enviado por:** [notetaker]
**Distribuição:** [Participantes + pessoas que precisam saber mas não estavam]

---

### Presentes
[Lista de participantes]

### Ausentes (recebem este follow-up)
[Lista]

### Decisões tomadas

| # | Decisão                         | Rationale breve           | Decidido por | Dissidências |
|---|---------------------------------|---------------------------|-------------|--------------|
| 1 | [Decisão 1]                     | [por quê em 1 frase]     | [agente]    | [se houver]  |

### Action items

| # | Ação                    | DRI     | Deadline   |
|---|------------------------|---------|------------|
| 1 | [Ação 1]               | [agente]| [data]     |

### Discussões-chave (resumo)
[Para cada tópico discutido: 2-3 frases capturando os pontos principais e conclusão]

1. **[Tópico 1]:** [resumo da discussão e conclusão]
2. **[Tópico 2]:** [resumo]

### Parking lot (para endereçar depois)
[Lista de itens com disposição]

### Próxima reunião
**Data:** [data]
**Pré-agenda:** [tópicos já previstos para a próxima]
```

### Instruções para o notetaker
- Enviar em até 2 horas após a reunião (enquanto a memória está fresca)
- Focar em: decisões, action items, insights-chave
- NÃO transcrever a reunião inteira — ninguém lê
- Destacar mudanças de plano ou surpresas
- Marcar ausentes que precisam de contexto específico
- Usar formato consistente toda vez (as pessoas aprendem a escanear rapidamente)

---

## 8. Combinações para tipos de reunião

### Weekly Leadership Sync (30 min)

```
| Bloco              | Tempo  | Notas                           |
|--------------------|--------|---------------------------------|
| Action item review | 5 min  | Items da semana anterior         |
| Metrics Review     | 10 min | Foco em anomalias apenas         |
| Decision Points    | 10 min | Máximo 2 decisões                |
| Action Items       | 5 min  | Novos items desta reunião        |
```

### Monthly Business Review (90 min)

```
| Bloco              | Tempo  | Notas                           |
|--------------------|--------|---------------------------------|
| Pre-read (leitura) | 15 min | Silent reading no início         |
| Metrics Review     | 20 min | Scorecard completo               |
| Decision Points    | 30 min | 2-3 decisões importantes         |
| Strategy discussion| 15 min | 1 tópico estratégico             |
| Action Items       | 10 min | Consolidar todos os items        |
```

### Quarterly Strategy Review (180 min)

```
| Bloco              | Tempo  | Notas                           |
|--------------------|--------|---------------------------------|
| Pre-read (leitura) | 20 min | Silent reading                   |
| Metrics Review     | 30 min | Quarter completo + trends        |
| Strategy blocks    | 60 min | Revisão de teses e bets          |
| Decision Points    | 40 min | Decisões de portfolio/prioridade |
| OKR setting        | 20 min | Próximo quarter                  |
| Action Items       | 10 min | Consolidar                       |
```

---

## 9. Checklist do facilitador

```markdown
### Antes da reunião
- [ ] Agenda enviada com >24h de antecedência
- [ ] Pre-read enviado no prazo
- [ ] Participantes confirmados (decisores presentes)
- [ ] Notetaker designado
- [ ] Timer/clock preparado

### Durante a reunião
- [ ] Confirmar que todos leram pre-read
- [ ] Seguir a agenda e tempos
- [ ] Redirecionar tangentes para parking lot
- [ ] Garantir que todos contribuam (puxar os silenciosos)
- [ ] Registrar decisões em tempo real
- [ ] Capturar action items com DRI e deadline

### Após a reunião
- [ ] Follow-up enviado em <2h
- [ ] Action items em sistema de tracking
- [ ] Parking lot items com disposição definida
- [ ] Feedback rápido pedido (se aplicável)
```
