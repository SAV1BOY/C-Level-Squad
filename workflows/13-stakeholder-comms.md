# Workflow 13: Stakeholder Communications

## Objetivo

Orquestrar a comunicação estruturada com todos os stakeholders da organização — investidores, board, equipe interna, parceiros e público externo — garantindo consistência na narrativa, timing adequado, canal correto e feedback loop para ajuste contínuo. Este workflow garante que nenhuma audiência relevante fique sem informação e que a comunicação seja tratada como ativo estratégico, não como tarefa administrativa.

> **Princípio:** Comunicação não é o que você diz — é o que o stakeholder entende. Sem feedback loop, comunicação é monólogo disfarçado de diálogo.

---

## Agentes Envolvidos

| Agente | Papel no Workflow |
|--------|-------------------|
| **Vision Chief (CEO)** | Porta-voz principal, narrativa estratégica, comunicação com board/investidores |
| **COO Orchestrator** | Coordenação de cadências, tracking de compromissos, comunicação operacional |
| **CMO Architect** | Estratégia de comunicação, messaging framework, gestão de canais externos |
| **CFO Strategist** | Comunicação financeira, investor relations, reporting de métricas |
| **CTO Architect** | Comunicação técnica, updates de plataforma, comunicação com comunidade dev |
| **CIO Engineer** | Comunicação de compliance, updates de sistemas, comunicação regulatória |
| **CAIO Architect** | Comunicação sobre iniciativas de IA, updates de capability, governance |
| **Squad Coordinator** | Logística, calendário de comunicações, tracking de feedback |

---

## Trigger (quando iniciar)

### Cadência Regular
- **Semanal:** Update interno para equipe (all-hands digest)
- **Mensal:** Investor update, board digest, partner update
- **Trimestral:** Board meeting formal, investor call, all-hands completo
- **Anual:** Annual report, carta do CEO, strategic narrative update

### Triggers Ad-hoc
- Mudança estratégica significativa (pivot, nova bet, kill decision)
- Incidente que requer comunicação externa (`workflows/11-incident-response-exec.md`)
- Milestone relevante (funding round, partnership, product launch)
- Mudança regulatória que afeta stakeholders
- Mudança organizacional (contratação/saída de executivo, reestruturação)
- Resultado financeiro acima/abaixo das expectativas

---

## Pré-condições

- [ ] Mapa de stakeholders atualizado (última revisão < 90 dias)
- [ ] Messaging framework do CMO Architect disponível e calibrado
- [ ] Calendário de comunicações do trimestre publicado
- [ ] Templates de comunicação aprovados e atualizados
- [ ] Métricas e dados atualizados para suportar a narrativa
- [ ] Feedback da última rodada de comunicação analisado
- [ ] Acesso a canais de comunicação validado (email, plataforma, status page)

---

## Processo (step-by-step com decision points)

### FASE 1: Mapeamento de Audiências e Necessidades

**Step 1.1 — Stakeholder Map**

| Audiência | Interesse Principal | Frequência | Canal Primário | Owner |
|-----------|-------------------|-----------|---------------|-------|
| **Board of Directors** | Performance, estratégia, riscos, governança | Trimestral + ad-hoc | Reunião formal + board pack | Vision Chief |
| **Investidores (VC/PE)** | Métricas, growth, runway, milestones | Mensal + trimestral | Email update + call | Vision Chief + CFO |
| **All-hands (empresa)** | Direção, conquistas, desafios, cultura | Semanal digest + mensal completo | Slack + reunião | Vision Chief + COO |
| **Liderança (C-Level + VPs)** | Estratégia, operações, decisões, bloqueios | Semanal sync | Reunião + Slack | COO Orchestrator |
| **Parceiros estratégicos** | Roadmap, integração, oportunidades | Trimestral + ad-hoc | Email + reunião | CMO Architect |
| **Clientes enterprise** | Roadmap, SLAs, incidents, features | Mensal + ad-hoc | Email + portal | CMO + CTO |
| **Comunidade / Mercado** | Thought leadership, inovação, valores | Mensal | Blog + social media + PR | CMO Architect |
| **Reguladores** | Compliance, políticas, governança de dados | Conforme exigência | Comunicação formal | CIO Engineer |
| **Candidatos / Talent market** | Cultura, missão, oportunidades | Contínuo | Careers page + social | COO + CMO |

**Step 1.2 — Priorização de Audiências**

> **Decision Point 1:** Qual audiência tem prioridade neste ciclo?

Matriz de priorização:

| Critério | Peso |
|----------|------|
| Impacto na decisão do stakeholder | 40% |
| Urgência da informação | 30% |
| Risco de não comunicar | 20% |
| Esforço de preparação | 10% |

### FASE 2: Crafting da Mensagem

**Step 2.1 — Narrativa Central (Message House)**

Para cada ciclo de comunicação, definir a "message house":

```
┌─────────────────────────────────────┐
│         NARRATIVA CENTRAL           │
│  (1 frase que resume a mensagem)    │
├─────────────────┬───────────────────┤
│   PILAR 1       │   PILAR 2         │
│ (prova/dado)    │ (prova/dado)      │
├─────────────────┼───────────────────┤
│   PILAR 3       │   PILAR 4         │
│ (prova/dado)    │ (prova/dado)      │
└─────────────────┴───────────────────┘
     ↓ Suportado por dados, exemplos e métricas
```

**Step 2.2 — Adaptação por Audiência**

| Audiência | Tom | Profundidade | Foco | Anti-padrão |
|-----------|-----|-------------|------|-------------|
| Board | Formal, conciso | Alto nível + drill-down disponível | Decisões necessárias | Excesso de detalhe operacional |
| Investidores | Confiante, data-driven | Métricas + narrativa | Growth + milestones | Otimismo sem fundamento |
| All-hands | Transparente, motivador | Contexto + ação | Direção + conquistas + desafios | Sugar-coating |
| Liderança | Direto, operacional | Detalhado | Decisões + bloqueios | Falta de contexto |
| Parceiros | Profissional, colaborativo | Relevante para a parceria | Roadmap + oportunidades | Compartilhar demais |
| Clientes | Empático, solucionador | Impacto para o cliente | Valor + roadmap | Jargão interno |
| Mercado | Autoridade, inspirador | Insights + tendências | Thought leadership | Propaganda disfarçada |

**Step 2.3 — Revisão de Mensagem**

> **Decision Point 2:** A mensagem é consistente entre audiências? Há risco de mensagens conflitantes?

Checklist de consistência:
- [ ] A narrativa central é a mesma para todas as audiências (adaptada, não contraditória)
- [ ] Dados e métricas são consistentes entre reports
- [ ] Não há informação em um canal que contradiga outro
- [ ] Informações confidenciais estão restritas às audiências corretas
- [ ] O tom é adequado para cada audiência

### FASE 3: Seleção de Canal e Timing

**Step 3.1 — Matriz de Canal por Tipo de Comunicação**

| Tipo de Comunicação | Canal | Formato | Lead Time |
|---------------------|-------|---------|-----------|
| Board meeting | Reunião presencial/video + board pack | Deck + narrative memo | 2 semanas |
| Investor update | Email + call opcional | Structured email | 1 semana |
| All-hands | Reunião + recording + digest escrito | Apresentação + Q&A | 3 dias |
| Weekly digest | Slack + email | Bullet points + métricas | 1 dia |
| Incident comms | Status page + email + Slack | Template padronizado | Imediato |
| Product announcement | Blog + email + social | Blog post + press release | 2 semanas |
| Regulatory filing | Comunicação formal | Documento legal | Conforme prazo legal |
| Culture update | Slack + all-hands | Transparente, pessoal | 1-3 dias |

**Step 3.2 — Calendário de Comunicações**

```
SEMANA 1 do mês:
  - Seg: Investor monthly update enviado (CFO + Vision Chief)
  - Ter: Weekly digest interno (COO Orchestrator)
  - Qua: Partner quarterly update (se mês de QBR)

SEMANA 2:
  - Ter: Weekly digest interno
  - Qui: Thought leadership content publicado (CMO Architect)

SEMANA 3:
  - Ter: Weekly digest interno
  - Qua: All-hands mensal (Vision Chief + squad leads)

SEMANA 4:
  - Ter: Weekly digest interno
  - Sex: Board pack enviado (se mês de board meeting)
```

**Step 3.3 — Timing Strategy**

> **Decision Point 3:** Qual o melhor momento para cada comunicação?

Regras de timing:
- **Boas notícias:** Comunicar rapidamente, com dados de suporte
- **Más notícias:** Comunicar proativamente (antes que descubram), com plano de ação
- **Decisões estratégicas:** Comunicar internamente ANTES de externamente
- **Incidentes:** Comunicar imediatamente, mesmo com informação incompleta
- **Mudanças organizacionais:** Comunicar diretamente afetados ANTES do all-hands

### FASE 4: Execução da Comunicação

**Step 4.1 — Preparação de Conteúdo**

Para cada comunicação programada:
1. Owner prepara draft seguindo template da audiência
2. CMO Architect revisa messaging e tom
3. Vision Chief aprova comunicações para board, investidores e externas
4. CFO Strategist valida qualquer dado financeiro incluído
5. Squad Coordinator agenda envio/publicação

**Step 4.2 — Templates por Audiência**

**Template: Investor Monthly Update**
```
Assunto: [Nome da Empresa] — Update Mensal [Mês/Ano]

Olá [Nome],

TL;DR: [1-2 frases com o highlight do mês]

MÉTRICAS-CHAVE:
- MRR: R$ [valor] ([+/-X%] vs mês anterior)
- Clientes ativos: [N] ([+/-X%])
- CAC: R$ [valor] | LTV/CAC: [ratio]
- Burn rate: R$ [valor] | Runway: [N] meses
- NPS: [score]

DESTAQUES DO MÊS:
1. [Conquista/milestone principal]
2. [Segunda conquista]
3. [Terceira conquista]

DESAFIOS E APRENDIZADOS:
1. [Desafio honesto + o que estamos fazendo]
2. [Aprendizado + ajuste feito]

PRÓXIMO MÊS — FOCO:
1. [Prioridade 1]
2. [Prioridade 2]

ASK (se aplicável):
- [Pedido específico: intro, conselho, recurso]

[Assinatura Vision Chief]
```

**Template: All-Hands Mensal**
```
AGENDA:
1. Números do mês (5 min) — COO Orchestrator
2. Conquistas e celebrações (5 min) — Vision Chief
3. Desafios e o que estamos fazendo (10 min) — Vision Chief
4. Direção para o próximo mês (5 min) — Vision Chief
5. Spotlight de squad/time (5 min) — Squad convidado
6. Q&A aberto (15 min) — Todos
7. Encerramento (5 min) — Vision Chief

REGRAS:
- Transparência radical: não sugar-coat
- Perguntas anônimas permitidas
- Recording disponível em 24h
- Action items publicados em 48h
```

**Template: Weekly Digest Interno**
```
📊 WEEKLY DIGEST — Semana [N] de [Mês/Ano]

MÉTRICAS DA SEMANA:
- NSM: [valor] ([trend])
- Revenue: [valor] ([trend])
- [Métrica 3]: [valor]

WINS:
- ✅ [Conquista 1]
- ✅ [Conquista 2]

ATENÇÃO:
- ⚠️ [Item que precisa de atenção]

DECISÕES TOMADAS:
- [Decisão 1] — Owner: [DRI]
- [Decisão 2] — Owner: [DRI]

FOCO ESTA SEMANA:
- [Prioridade 1]
- [Prioridade 2]
```

**Step 4.3 — Envio e Distribuição**
- Squad Coordinator confirma que todos os canais estão operacionais
- Enviar comunicações conforme calendário
- Registrar envio com timestamp, canal e audiência

### FASE 5: Feedback Collection e Adjustment

**Step 5.1 — Coleta de Feedback**

| Audiência | Método de Feedback | Frequência |
|-----------|-------------------|-----------|
| Board | Feedback direto na reunião + 1:1 com Chair | Pós-reunião |
| Investidores | Reply ao update + NPS de investor relations | Trimestral |
| All-hands | Enquete pós-all-hands + perguntas anônimas | Mensal |
| Liderança | 1:1 com COO + survey de comunicação interna | Trimestral |
| Clientes | CSAT + NPS + feedback qualitativo | Contínuo |
| Mercado | Engagement metrics + sentiment analysis | Mensal |

**Step 5.2 — Análise de Efetividade**

Métricas de comunicação:

| Métrica | Target | Medição |
|---------|--------|---------|
| Investor reply rate | > 30% | % de investidores que respondem ao update |
| All-hands attendance | > 80% | % de participação |
| All-hands satisfaction | > 4.0/5 | Survey pós-evento |
| Weekly digest open rate | > 70% | Analytics de email/Slack |
| Board prep satisfaction | > 4.5/5 | Feedback do board chair |
| External content engagement | Crescente mês a mês | Views, shares, comments |

**Step 5.3 — Ajustes**

> **Decision Point 4:** O feedback indica necessidade de ajuste? Analisar:

- [ ] A frequência está adequada? (demais = fadiga, pouco = desinformação)
- [ ] O canal está correto? (stakeholders preferem outro formato?)
- [ ] A profundidade está adequada? (detalhado demais ou raso demais?)
- [ ] O tom está calibrado? (formal demais, informal demais?)
- [ ] Há gaps de informação? (stakeholders perguntam coisas que deveriam saber?)

Ajustes são implementados no próximo ciclo de comunicação.

---

## Quality Gates

### Gate 1: Preparação (antes de enviar qualquer comunicação)
- [ ] Audiência corretamente identificada e mapeada
- [ ] Mensagem adaptada para a audiência (não genérica)
- [ ] Dados e métricas validados e consistentes
- [ ] Revisão do CMO Architect concluída (messaging e tom)
- [ ] Aprovação do Vision Chief para comunicações externas e board
- [ ] Referência: `checklists/stakeholder-communication-quality.md`

### Gate 2: Consistência (entre comunicações do mesmo ciclo)
- [ ] Narrativa central consistente entre todas as audiências
- [ ] Sem contradições entre comunicações internas e externas
- [ ] Informações confidenciais restritas às audiências corretas
- [ ] Timeline de comunicação respeitada (interno antes de externo)

### Gate 3: Feedback Loop (após comunicação enviada)
- [ ] Feedback coletado de cada audiência-chave
- [ ] Métricas de efetividade medidas e comparadas com targets
- [ ] Ajustes identificados e documentados para o próximo ciclo
- [ ] Referência: `checklists/ralphloop-quality.md`

---

## Outputs / Artefatos

| Artefato | Formato | Responsável | Destino |
|----------|---------|-------------|---------|
| Stakeholder map atualizado | Markdown | CMO Architect | `data/stakeholders/stakeholder-map.md` |
| Calendário de comunicações | Markdown | Squad Coordinator | `data/calendars/comms-calendar.md` |
| Investor update mensal | Email | Vision Chief + CFO | Investidores |
| Board pack | Deck + memo | Vision Chief + COO | Board |
| All-hands recording + notes | Video + markdown | Squad Coordinator | Repositório interno |
| Weekly digest | Slack/email | COO Orchestrator | All-hands |
| Feedback analysis | Markdown | CMO Architect | `data/research/comms-feedback.md` |

---

## Registries Atualizados

- `data/registries/decision-registry.yaml` — Decisões comunicadas e feedback recebido
- `data/registries/metric-registry.yaml` — Métricas de efetividade de comunicação
- `data/registries/lessons-learned.yaml` — Aprendizados sobre comunicação com stakeholders
- `data/registries/culture-registry.yaml` — Insights de cultura derivados de feedback interno

---

## Próximos Passos

1. Feedback de cada ciclo alimenta melhorias no próximo ciclo (RalphLoop)
2. Investor updates alimentam preparação do board (`workflows/17-board-prep-and-delivery.md`)
3. Feedback interno alimenta o ciclo de cultura (`workflows/19-culture-health-cycle.md`)
4. Comunicação de incidentes segue o workflow dedicado (`workflows/11-incident-response-exec.md`)
5. Messaging framework é atualizado trimestralmente pelo CMO Architect
6. Calendário de comunicações é revisado no início de cada trimestre

---

## Cross-squad Handoffs

| Squad | Handoff | Direção | SLA |
|-------|---------|---------|-----|
| **Brand Squad** | Identidade visual, tom de marca, guidelines de comunicação | Brand → C-Level | 48h para guidelines |
| **Copy Squad** | Textos de comunicação, email copy, scripts de apresentação | C-Level → Copy | 48h para entregas |
| **Story Squad** | Narrativa da empresa, founder story, thought leadership | C-Level ↔ Story | 1 semana para conteúdo |
| **Movement Squad** | Comunicação com comunidade, engagement, cultura externa | C-Level → Movement | 48h para briefing |
| **Design Squad** | Decks de apresentação, visual de reports, infográficos | C-Level → Design | 1 semana para entregas |
| **Data Squad** | Dashboards para board, métricas de comunicação, analytics | Data → C-Level | 48h para análises |
| **Advisory Board** | Revisão de comunicação estratégica, feedback de board prep | C-Level ↔ Advisory | 1 semana para revisões |
| **Traffic Squad** | Distribuição de conteúdo externo, amplificação de mensagem | C-Level → Traffic | 48h para execução |
| **Cybersecurity Squad** | Revisão de compliance em comunicações públicas, LGPD | Cyber → C-Level | 24h para revisão |

---

## Referências

- `checklists/stakeholder-communication-quality.md` — Checklist de qualidade de comunicação
- `frameworks/vision-chief/vision-chief-narrative-cascade.md` — Cascata de narrativa
- `frameworks/cmo-architect/cmo-positioning-to-performance.md` — Posicionamento
- `templates/reports/stakeholder-update.md` — Template de update para stakeholders
- `templates/operating-system/board-prep-pack.md` — Template de board pack
