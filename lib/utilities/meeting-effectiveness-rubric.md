# Meeting Effectiveness Rubric — Rubrica de Efetividade de Reuniões

> Referência do C-Level Squad para garantir que cada reunião gere valor proporcional ao custo.
> Custo de reunião = (salário/hora × participantes × duração) + custo de oportunidade.

---

## 1. Premissa fundamental

Uma reunião só deve existir se **não houver alternativa assíncrona** que produza o mesmo resultado. Antes de agendar, perguntar:

- Isso poderia ser um memo? → Não agendar
- Isso poderia ser um comentário no documento? → Não agendar
- Precisa de debate ao vivo para desbloquear? → Agendar
- Precisa de alinhamento emocional/relacional? → Agendar
- É uma decisão Type 1 que requer deliberação? → Agendar

### Cálculo de custo de reunião

```
Custo por hora de reunião = Σ (custo/hora de cada participante)

Exemplo: Reunião de 6 agentes C-Level por 1 hora
- Custo estimado: 6 × R$500/hora = R$3.000
- Custo com oportunidade (×2): R$6.000
- Reunião semanal de 1h × 48 semanas = R$288.000/ano

Pergunta: essa reunião gera R$288K/ano de valor?
```

---

## 2. Dimensões de avaliação (7 dimensões, score 1-5 cada)

### Dimensão 1: Clareza da Agenda (Agenda Clarity)

| Score | Descrição |
|-------|-----------|
| 1 | Sem agenda. Reunião marcada sem propósito definido. "Vamos nos alinhar" sem especificar sobre o quê |
| 2 | Agenda genérica: lista de tópicos sem tempo alocado, sem outcome esperado. Ex: "Discutir produto" |
| 3 | Agenda com tópicos e tempo alocado. Alguns outcomes definidos mas não todos. Falta priorização |
| 4 | Agenda clara: cada tópico com (a) tempo alocado, (b) tipo (informação, discussão, decisão), (c) outcome esperado, (d) responsável pela condução |
| 5 | Agenda exemplar: tudo do nível 4 + priorizada (itens mais importantes primeiro), com buffer de 10% para imprevistos, enviada >24h antes, com campo para participantes adicionarem tópicos antes da reunião |

**Template de agenda efetiva:**
```
## Agenda — [Nome da reunião]
**Data:** [YYYY-MM-DD HH:MM]  **Duração:** [XX min]
**Facilitador:** [agente]

| # | Tópico                  | Tipo       | Tempo | Owner | Outcome esperado       |
|---|-------------------------|-----------|-------|-------|------------------------|
| 1 | [tópico prioritário]    | Decisão   | 15min | [DRI] | Decisão GO/NO-GO sobre X |
| 2 | [tópico 2]              | Discussão | 10min | [DRI] | Alinhar opções para Y  |
| 3 | [tópico 3]              | Informação| 5min  | [DRI] | Ciência sobre Z        |
|   | Buffer                  |           | 5min  |       |                        |
```

### Dimensão 2: Qualidade do Pre-read (Pre-read Quality)

| Score | Descrição |
|-------|-----------|
| 1 | Sem pre-read. Toda informação apresentada ao vivo pela primeira vez. Tempo gasto "educando" em vez de decidindo |
| 2 | Pre-read enviado mas tarde demais (<2h antes) ou muito longo (>10 páginas sem sumário) |
| 3 | Pre-read enviado >24h antes, com tamanho razoável. Mas sem perguntas-chave ou pontos de decisão destacados |
| 4 | Pre-read enviado >24h antes, conciso (<5 páginas), com Executive Summary, dados relevantes, perguntas-chave numeradas, e opções para decisão |
| 5 | Pre-read exemplar: tudo do nível 4 + evidência de que participantes leram (comentários prévios, perguntas enviadas antes). Facilitador monitora quem leu e ajusta dinâmica |

**Regra de ouro:** Tempo de leitura do pre-read deve ser ≤ 50% da duração da reunião. Se o pre-read leva 30min para ler, a reunião deve ter ≥ 60min.

**Template de pre-read:**
```markdown
## Pre-read — [Nome da reunião] — [Data]

### TL;DR (3 bullets máximo)
- [ponto 1]
- [ponto 2]
- [ponto 3]

### Contexto (1 parágrafo)
[Contexto essencial para quem não está no dia-a-dia]

### Dados relevantes
[Tabela, gráfico ou métricas-chave]

### Perguntas para decisão
1. [Pergunta 1] — Opções: A, B, C
2. [Pergunta 2] — Opções: X, Y

### Recomendação do autor
[O que o autor recomenda e por quê]
```

### Dimensão 3: Decisões Tomadas (Decisions Made)

| Score | Descrição |
|-------|-----------|
| 1 | Nenhuma decisão tomada. Reunião termina com "vamos pensar mais". Mesmos tópicos retornam na próxima reunião |
| 2 | Decisão implícita ("parece que concordamos") mas não formalizada. Ambiguidade sobre o que foi decidido |
| 3 | Decisões tomadas e verbalizadas, mas não registradas formalmente. Sem rationale documentado |
| 4 | Decisões claramente tomadas, registradas em ata/notes, com rationale. Dissidências registradas. Decisões comunicadas aos ausentes |
| 5 | Decisões tomadas com processo claro: opções apresentadas → trade-offs discutidos → decisão formalizada → DRI atribuído → rationale e dissidências registrados → comunicação ampla planejada |

**Framework para decisões em reunião:**
```
1. Apresentar contexto (pre-read — não repetir ao vivo)
2. Verificar entendimento compartilhado
3. Apresentar opções (mínimo 3)
4. Discutir trade-offs de cada opção
5. Poll de posicionamento (rápido — 1 minuto)
6. Discussão de divergências (focar onde discordamos)
7. Decisão do DRI (com input recebido)
8. Registrar: decisão + rationale + dissidências
```

### Dimensão 4: Action Items com DRI (Action Items with DRI)

| Score | Descrição |
|-------|-----------|
| 1 | Sem action items. Reunião termina sem próximos passos definidos |
| 2 | Action items vagos: "vamos investigar", "alguém precisa olhar isso" |
| 3 | Action items definidos com responsável, mas sem deadline ou sem critério de completude |
| 4 | Action items SMART: Específico, com DRI nomeado, deadline, critério de done, e onde será reportado o status |
| 5 | Action items SMART + tracking system definido (qual ferramenta), follow-up agendado, dependências entre items mapeadas, bloqueios identificados proativamente |

**Template de action item:**
```
- [ ] [AÇÃO específica e verificável]
      DRI: [nome/agente]
      Deadline: [YYYY-MM-DD]
      Done when: [critério objetivo]
      Report in: [próxima reunião / Slack / doc]
      Depends on: [outro item, se houver]
```

### Dimensão 5: Eficiência de Tempo (Time Efficiency)

| Score | Descrição |
|-------|-----------|
| 1 | Reunião excedeu o tempo em >50%. Tangentes constantes. Tópicos da agenda não cobertos. Repetição de informação do pre-read |
| 2 | Reunião excedeu o tempo em 20-50%. Algumas tangentes. Metade dos tópicos cobertos com qualidade |
| 3 | Reunião dentro do tempo (±10%). Maioria dos tópicos cobertos. Algumas tangentes mas controladas |
| 4 | Reunião dentro do tempo. Todos os tópicos cobertos. Facilitador gerenciou tangentes. Sobrou tempo para perguntas |
| 5 | Reunião terminou cedo ou exatamente no tempo. Todos os tópicos cobertos com qualidade. Tangentes redirecionadas para parking lot. Energia alta do início ao fim |

**Técnicas para manter eficiência:**
- **Timeboxing visível:** Timer na tela para cada tópico
- **Facilitador ativo:** Uma pessoa responsável por gerenciar tempo e tangentes
- **Parking lot:** Espaço para tópicos importantes mas fora de escopo — endereçar depois
- **Standup format:** Para updates, limitar a 2 minutos por pessoa
- **Decisão-first:** Começar com a decisão mais importante (quando energia é maior)
- **Regra dos 2 minutos:** Se pode ser respondido em 2 min, responder agora; senão, offline

### Dimensão 6: Participantes Corretos (Right Attendees)

| Score | Descrição |
|-------|-----------|
| 1 | Participantes errados: decisores ausentes, muitos espectadores passivos, pessoas que não contribuíram nada |
| 2 | Alguns decisores-chave presentes, mas também muitos "turistas". Pessoas faltando para tomar certas decisões |
| 3 | Maioria dos participantes corretos. 1-2 pessoas poderiam ter sido substituídas por pre-read. Nenhum decisor ausente |
| 4 | Participantes bem selecionados: decisores presentes, contribuidores relevantes, sem turistas. Lista revisada antes de enviar convite |
| 5 | Participantes otimizados: mínimo viável de pessoas para as decisões necessárias. Roles definidos (decisor, advisor, informado). Pessoas adicionais recebem notes depois |

**Framework de participantes (RACI para reuniões):**
```
D = Decisor      — DEVE estar na reunião
A = Advisor      — Contribui com input, DEVE estar
I = Informado    — Recebe notes DEPOIS, NÃO precisa estar
O = Opcional     — Pode contribuir mas não é essencial
```

**Regra de ouro (Jeff Bezos):** Máximo de pessoas que 2 pizzas alimentam (~6-8).

### Dimensão 7: Follow-up e Tracking (Follow-up)

| Score | Descrição |
|-------|-----------|
| 1 | Nenhum follow-up. Notas não registradas. Decisões e action items perdidos. Mesma discussão se repete na próxima reunião |
| 2 | Notes enviados mas tarde (>48h). Sem tracking de action items. Sem verificação de completude |
| 3 | Notes enviados em <24h com decisões e action items. Mas sem tracking sistemático — items "caem no esquecimento" |
| 4 | Notes enviados em <4h. Action items em sistema de tracking. Review de items pendentes na próxima reunião. Bloqueios escalados |
| 5 | Notes enviados em <2h. Action items em sistema compartilhado com status visível. Próxima reunião começa com review de items. Métricas de completion rate rastreadas. Loop de feedback sobre efetividade da reunião |

---

## 3. Scoring e interpretação

### Cálculo

```
Meeting Effectiveness Score = Σ (scores das 7 dimensões)
Máximo: 35 pontos
```

### Faixas de efetividade

| Score  | Nível       | Interpretação                                                    |
|--------|-------------|------------------------------------------------------------------|
| 30-35  | World-class | Reunião exemplar. Cada minuto gera valor. Modelo para outras     |
| 23-29  | Bom         | Reunião produtiva com melhorias pontuais possíveis               |
| 16-22  | Adequado    | Reunião funcional mas com desperdício significativo de tempo      |
| 9-15   | Fraco       | Reunião mais atrapalha que ajuda. Reformular ou eliminar          |
| 1-8    | Cancelar    | Esta reunião não deveria existir. Substituir por async            |

### Benchmarks por tipo de reunião

| Tipo de reunião            | Score mínimo | Frequência de avaliação |
|---------------------------|-------------|------------------------|
| Board / Strategy review   | ≥ 28        | Toda ocorrência         |
| Weekly leadership sync    | ≥ 23        | Mensal (amostral)       |
| Sprint planning           | ≥ 20        | Trimestral              |
| 1:1                       | ≥ 18        | Trimestral              |
| All-hands                 | ≥ 23        | Toda ocorrência         |
| Ad-hoc decision meeting   | ≥ 25        | Toda ocorrência         |

---

## 4. Tipos de reunião e expectativas

### 4.1 Reunião de decisão

```
Propósito: Tomar uma decisão específica
Duração ideal: 30-45 min
Participantes: Decisor + advisors (máx 6)
Score mínimo: 25/35

Expectativas:
- Pre-read obrigatório com opções e trade-offs
- Saída obrigatória: decisão documentada + DRI + timeline
- Se não houver decisão, registrar: o que falta para decidir + quem + quando
```

### 4.2 Reunião de alinhamento/sync

```
Propósito: Compartilhar status, identificar bloqueios, alinhar prioridades
Duração ideal: 15-25 min
Participantes: Time direto (máx 8)
Score mínimo: 20/35

Expectativas:
- Updates assíncronos antes (cada pessoa preenche status)
- Tempo ao vivo usado para: bloqueios, riscos, perguntas
- Saída: bloqueios com DRI para desbloquear
```

### 4.3 Reunião de brainstorm/creative

```
Propósito: Gerar ideias, explorar possibilidades
Duração ideal: 45-60 min
Participantes: Diversidade de perspectivas (máx 8)
Score mínimo: 18/35 (flexibilidade maior)

Expectativas:
- Contexto e constraints compartilhados antes
- Fase divergente (gerar) separada de fase convergente (avaliar)
- Saída: lista priorizada de ideias + próximos passos para top 3
```

### 4.4 Reunião de review/retrospectiva

```
Propósito: Avaliar resultados, aprender, ajustar
Duração ideal: 45-60 min
Participantes: Time envolvido na execução
Score mínimo: 22/35

Expectativas:
- Dados/métricas compartilhados antes
- Framework: O que funcionou? O que não funcionou? O que mudar?
- Saída: 3-5 ações de melhoria com DRI e deadline
```

---

## 5. Processo de melhoria contínua

### Feedback loop de 2 minutos

No final de cada reunião importante, 2 minutos para:
1. "Esta reunião foi produtiva? (1-5)" — votação rápida
2. "Uma coisa que melhoraria a próxima:" — cada pessoa diz uma frase
3. Facilitador registra e implementa na próxima ocorrência

### Métricas de saúde de reuniões (organizacional)

| Métrica                         | Target               | Como medir                         |
|--------------------------------|----------------------|-----------------------------------|
| Horas em reunião / semana      | <15h para ICs, <20h para liderança | Calendar audit              |
| % reuniões com agenda          | >90%                 | Audit mensal de convites           |
| % reuniões com notes/follow-up | >80%                 | Verificação semanal                |
| Action item completion rate    | >85%                 | Tracking system                    |
| Meeting NPS (avg)              | >3.5/5               | Survey mensal amostral             |
| % reuniões que poderiam ser email | <10%              | Retrospectiva trimestral           |
| Reuniões canceladas por desnecessárias | >5% (saudável!) | Calendar audit                |

### Audit trimestral de reuniões

```markdown
## Meeting Audit — [Quarter]

Para cada reunião recorrente:

| Reunião              | Freq.    | Dur. | Part. | Score médio | Decisão          |
|----------------------|----------|------|-------|-------------|------------------|
| Weekly leadership    | Semanal  | 60m  | 6     | 24/35       | Manter, melhorar pre-read |
| Sprint planning      | Quinzenal| 90m  | 12    | 18/35       | Reduzir para 60m |
| Monthly business rev | Mensal   | 120m | 15    | 26/35       | Manter            |
| Team standup         | Diária   | 15m  | 8     | 22/35       | Manter            |
| "Sync" sem agenda    | Semanal  | 30m  | 4     | 12/35       | ELIMINAR          |

### Ações:
1. Eliminar [reunião] — economia de [X horas/mês]
2. Reduzir [reunião] de [X]min para [Y]min
3. Tornar [reunião] quinzenal em vez de semanal
4. Investir em pre-read para [reunião]

### Economia projetada: [X] horas/mês × [Y] pessoas = [Z] horas-pessoa/mês
```

---

## 6. Template de avaliação rápida

```markdown
## Meeting Effectiveness — Quick Score

**Reunião:** [nome]
**Data:** [YYYY-MM-DD]
**Avaliador:** [agente]

| # | Dimensão          | Score (1-5) | Nota rápida        |
|---|-------------------|-------------|---------------------|
| 1 | Agenda Clarity    |             |                     |
| 2 | Pre-read Quality  |             |                     |
| 3 | Decisions Made    |             |                     |
| 4 | Action Items+DRI  |             |                     |
| 5 | Time Efficiency   |             |                     |
| 6 | Right Attendees   |             |                     |
| 7 | Follow-up         |             |                     |
|   | **TOTAL**         | **/35**     |                     |

**Maior strength:** [dimensão]
**Maior oportunidade:** [dimensão] — Sugestão: [ação]
```
