# Cross-Squad Effectiveness Rubric — Rubrica de Efetividade de Colaboração Cross-Squad

> Referência do C-Level Squad para avaliar e melhorar a colaboração entre os 6 agentes.
> A efetividade de um squad executivo não é a soma das partes individuais — é a qualidade das interações entre elas.

---

## 1. Contexto: Por que colaboração cross-squad importa

O C-Level Squad opera com 6 agentes interdependentes:

```
CEO (Vision Chief) ← Define direção, arbitra conflitos
     ↕
COO ←→ CTO ←→ CIO
 ↕      ↕      ↕
CMO ←→ CAIO ←→ COO
```

**Falhas de colaboração cross-squad tipicamente se manifestam como:**
- Decisões tomadas em silo que impactam outros agentes
- Dependências não comunicadas que atrasam entregas
- Conflitos de prioridade que escalam desnecessariamente
- Duplicação de esforço (dois agentes fazendo a mesma coisa sem saber)
- Handoffs perdidos (informação que não chega ao próximo agente)

---

## 2. Dimensões de avaliação (7 dimensões, score 1-5 cada)

### Dimensão 1: Handoff Quality (Qualidade dos Handoffs)

Quando um agente entrega trabalho, informação ou responsabilidade para outro, a qualidade do handoff é adequada?

| Score | Descrição |
|-------|-----------|
| 1 | Handoffs inexistentes ou caóticos. Informação perdida na transição. Receptor precisa "redescobrir" contexto. Trabalho refeito frequentemente |
| 2 | Handoffs informais. Alguma informação passada mas incompleta. Receptor precisa fazer muitas perguntas para entender contexto e expectativas |
| 3 | Handoffs estruturados na maioria dos casos. Template básico seguido (o quê, por quê, quando). Mas sem verificação de que o receptor entendeu |
| 4 | Handoffs consistentes e completos: contexto, expectativas, timeline, critérios de sucesso, constraints. Receptor confirma entendimento. Handoff documentado |
| 5 | Handoffs exemplares: tudo do nível 4 + histórico de decisões anteriores, lições aprendidas, stakeholders relevantes, riscos conhecidos. Feedback loop sobre qualidade do handoff. Zero retrabalho por informação faltante |

**Template de handoff entre agentes:**

```markdown
## Handoff — De: [Agente origem] → Para: [Agente destino]

**Data:** [YYYY-MM-DD]
**Assunto:** [descrição em uma frase]

### Contexto
- O que foi feito até agora: [resumo]
- Por que está sendo passado: [razão]
- Decisões já tomadas: [lista]
- Decisões pendentes: [lista]

### O que é esperado
- Entregável: [descrição clara]
- Critérios de sucesso: [métricas ou condições]
- Deadline: [data]
- Constraints: [limitações conhecidas]

### Recursos
- Documentos relevantes: [links]
- Pessoas para consultar: [nomes e contexto]
- Riscos conhecidos: [lista]

### Confirmação
- [ ] Receptor revisou este handoff
- [ ] Receptor confirma entendimento
- [ ] Receptor confirma capacidade de entrega no prazo
```

### Dimensão 2: SLA Compliance (Cumprimento de SLAs)

Os agentes cumprem os prazos e padrões acordados para entregas inter-squad?

| Score | Descrição |
|-------|-----------|
| 1 | Sem SLAs definidos entre agentes. Cada um entrega "quando dá". Sem previsibilidade. Frustrações constantes |
| 2 | SLAs informais ("geralmente em 1 semana"). Cumpridos esporadicamente (<50%). Sem tracking |
| 3 | SLAs definidos para os fluxos principais. Cumpridos em 60-80% dos casos. Tracking manual. Atrasos comunicados mas tarde |
| 4 | SLAs definidos para todos os fluxos inter-agente. Cumpridos em >85% dos casos. Tracking sistemático. Atrasos comunicados proativamente com novo ETA |
| 5 | SLAs otimizados: definidos, medidos, revisados trimestralmente. Cumpridos em >95%. Atrasos raros e sempre com plano B. Melhoria contínua de SLAs baseada em dados |

**SLAs recomendados entre agentes:**

| Fluxo                               | SLA recomendado          | Consequência de descumprimento     |
|--------------------------------------|--------------------------|-------------------------------------|
| Request de análise de dados (CIO)    | 3 dias úteis (standard), 24h (urgente) | Escalação para CEO se >2× SLA |
| Review técnico de proposta (CTO)     | 2 dias úteis             | Aprovação tácita se >3× SLA        |
| Avaliação de risco (qualquer agente) | 5 dias úteis             | Escalação se bloqueia decisão       |
| Feedback em documento/memo           | 48h para revisão         | Segue sem o feedback se >72h        |
| Input para decisão (qualquer)        | Conforme deadline do memo | Decisão tomada sem o input           |
| Deploy/release review (CTO)          | 24h para standard, 4h para hotfix | Processo de exceção ativado   |
| AI model review (CAIO)              | 5 dias úteis             | Não deploy sem review                |
| Compliance check (CIO)              | 5 dias úteis             | Não launch sem sign-off              |

### Dimensão 3: Communication Clarity (Clareza de Comunicação)

A comunicação entre agentes é clara, consistente e sem ambiguidade?

| Score | Descrição |
|-------|-----------|
| 1 | Comunicação caótica. Mensagens ambíguas. Cada agente usa terminologia diferente para os mesmos conceitos. Informação importante perdida em threads longas |
| 2 | Comunicação funcional mas inconsistente. Alguns agentes comunicam bem, outros não. Sem padrão. Mal-entendidos frequentes |
| 3 | Comunicação razoavelmente clara. Glossário compartilhado para termos-chave. Canais definidos (quando usar memo vs. mensagem vs. reunião). Mal-entendidos ocasionais |
| 4 | Comunicação consistente. Formato padrão para diferentes tipos de comunicação. Contexto sempre incluído. Receptor pode agir sem precisar pedir esclarecimento na maioria dos casos |
| 5 | Comunicação exemplar: clara, concisa, com contexto, acionável. Glossário vivo mantido. Comunicação assíncrona preferida para eficiência. Sincrona reservada para debate e decisão. Feedback loop sobre qualidade da comunicação |

**Princípios de comunicação cross-squad:**

```
1. BLUF (Bottom Line Up Front): Comece com a conclusão/pedido
2. Contexto suficiente: Receptor não precisa adivinhar "por quê"
3. Ação clara: O que exatamente é esperado do receptor?
4. Deadline explícito: Quando precisa de resposta/entrega?
5. Canal adequado:
   - Informação: Documento/memo (assíncrono)
   - Decisão simples: Mensagem com opções
   - Decisão complexa: Reunião com pre-read
   - Urgência: Mensagem direta + tag de urgência
```

### Dimensão 4: Dependency Management (Gestão de Dependências)

As dependências entre agentes são mapeadas, comunicadas e gerenciadas proativamente?

| Score | Descrição |
|-------|-----------|
| 1 | Dependências não mapeadas. Descobertas apenas quando algo quebra. "Eu não sabia que precisava disso de você" é frase comum |
| 2 | Dependências conhecidas informalmente. Não documentadas. Gerenciadas reativamente (quando bloqueiam) |
| 3 | Dependências mapeadas para iniciativas principais. Comunicadas em planning. Mas sem tracking ativo — bloqueios ainda surpreem |
| 4 | Mapa de dependências mantido ativamente. Cada iniciativa identifica dependências inter-agente no charter. Check-in regular sobre status. Bloqueios identificados proativamente |
| 5 | Gestão de dependências excelente: mapa visual atualizado, check-in semanal sobre dependências críticas, bloqueios antecipados e resolvidos antes de impactar critical path. Buffer planejado para dependências de alto risco |

**Template de mapa de dependências:**

```markdown
## Dependency Map — [Iniciativa/Quarter]

| Iniciativa    | Agente owner | Depende de | Entregável esperado              | SLA    | Status      |
|--------------|-------------|------------|----------------------------------|--------|-------------|
| Plataforma v2| CTO         | CIO        | Data pipeline para novo módulo   | 2026-04-01 | 🟢 On track |
| Plataforma v2| CTO         | CAIO       | Modelo de recomendação treinado  | 2026-04-15 | 🟡 At risk  |
| Expansão LATAM| CMO        | CTO        | Localização da plataforma        | 2026-03-30 | 🟢 On track |
| Expansão LATAM| CMO        | CIO        | Compliance por país              | 2026-04-01 | 🔴 Atrasado |

### Dependências críticas (critical path):
1. [CIO → Compliance por país] — Bloqueio: aguardando parecer jurídico externo
   Ação: CEO escalar com escritório de advocacia. Deadline: 2026-03-15

### Dependências de risco:
1. [CAIO → Modelo de recomendação] — Risco: dados de treinamento insuficientes
   Ação: CAIO + CIO alinhar data pipeline até 2026-03-18
```

### Dimensão 5: Conflict Resolution Speed (Velocidade de Resolução de Conflitos)

Quando há conflito entre agentes (prioridades, recursos, abordagem), quão rápido é resolvido?

| Score | Descrição |
|-------|-----------|
| 1 | Conflitos não resolvidos. Acumulam-se. Passivo-agressividade. Agentes "trabalham ao redor" do conflito em vez de resolvê-lo. Decisões travadas |
| 2 | Conflitos eventualmente resolvidos mas lentamente (>2 semanas). Escalação para CEO é a única forma de resolver. Ressentimento residual |
| 3 | Conflitos resolvidos em 1-2 semanas. Processo de escalação definido mas não sempre seguido. Alguns conflitos recorrentes (mesmos temas) |
| 4 | Conflitos resolvidos em 3-5 dias úteis. Processo claro: 1) Diálogo direto entre agentes, 2) Se não resolver em 48h, mediação do COO, 3) Se não resolver, decisão do CEO. Conflitos documentados para evitar recorrência |
| 5 | Conflitos resolvidos em <48h. Cultura de discordância respeitosa. Conflitos vistos como saudáveis e necessários. Framework de "disagree and commit". Padrões de conflito identificados e endereçados sistemicamente |

**Framework de resolução de conflitos:**

```
Nível 1 — Diálogo direto (0-48h):
  Os dois agentes conversam diretamente.
  Regras: Foco em interesses (não posições), dados antes de opiniões,
  buscar opção que atenda ambos os interesses.

Nível 2 — Mediação (48h-5 dias):
  COO media a conversa.
  Framework: Cada lado apresenta (a) o que quer, (b) por que quer,
  (c) o que está disposto a ceder. COO facilita acordo.

Nível 3 — Arbitragem (5-7 dias):
  CEO decide com input de ambos os lados.
  Regra: CEO documenta a decisão e o rationale.
  Ambos os lados se comprometem a executar ("disagree and commit").

Nível 4 — Revisão sistêmica (pós-resolução):
  Se o mesmo tipo de conflito ocorre 3× → problema é sistêmico.
  Requer mudança de processo, não apenas resolução caso a caso.
```

### Dimensão 6: Shared KPI Alignment (Alinhamento de KPIs compartilhados)

Os agentes têm KPIs compartilhados que incentivam colaboração, ou apenas KPIs individuais que incentivam silos?

| Score | Descrição |
|-------|-----------|
| 1 | Apenas KPIs individuais por agente. Nenhum KPI compartilhado. Incentivos potencialmente conflitantes. "Meu OKR" importa mais que "nosso resultado" |
| 2 | KPIs individuais dominantes. 1-2 KPIs compartilhados existem mas não são priorizados. Ninguém é accountable pelo KPI compartilhado |
| 3 | Mix de KPIs individuais e compartilhados. KPIs compartilhados revisados mensalmente. Mas ainda não influenciam decisões de prioridade quando conflitam com KPIs individuais |
| 4 | KPIs compartilhados são prioridade #1 para todos os agentes. KPIs individuais existem mas são secundários. Conflitos de prioridade resolvidos em favor do KPI compartilhado. Scorecard unificado |
| 5 | KPI system otimizado: North Star Metric compartilhada por todos + KPIs de contribuição por agente que alimentam a NSM. Alinhamento perfeito entre individual e coletivo. Celebração de wins coletivos |

**Exemplo de estrutura de KPIs alinhados:**

```
North Star Metric (todos os agentes): Monthly Recurring Revenue (MRR)

KPIs de contribuição:
- CEO: Strategic clarity score, decision quality score
- COO: Operational efficiency (cost/revenue ratio), initiative completion rate
- CMO: Customer acquisition cost, pipeline value, brand NPS
- CTO: Platform uptime, release velocity, tech debt ratio
- CIO: Data quality score, compliance score, security incidents
- CAIO: AI use case ROI, model accuracy in production, AI adoption rate

Cada KPI de contribuição tem impacto demonstrável no North Star.
Quando KPIs conflitam, North Star prevalece.
```

### Dimensão 7: Feedback Loops (Loops de Feedback)

Existe mecanismo estruturado para agentes darem e receberem feedback sobre a colaboração?

| Score | Descrição |
|-------|-----------|
| 1 | Nenhum feedback entre agentes. Problemas acumulam-se silenciosamente. Frustrações explodem em momentos de crise |
| 2 | Feedback informal e esporádico. Geralmente apenas negativo (quando algo deu errado). Sem estrutura para feedback positivo ou construtivo |
| 3 | Feedback em retrospectivas trimestrais. Útil mas infrequente. Ações de melhoria nem sempre implementadas |
| 4 | Feedback regular: retrospectiva mensal + feedback pontual quando necessário. Framework estruturado (SBI: Situation-Behavior-Impact). Ações de melhoria rastreadas |
| 5 | Cultura de feedback contínuo: feedback em tempo real é normal e bem-vindo. Retrospectivas mensais com métricas de colaboração. 360-degree review semestral entre agentes. Melhoria demonstrável ao longo do tempo |

**Framework SBI para feedback entre agentes:**

```
S (Situation): "Na reunião de planning de ontem..."
B (Behavior): "...você compartilhou a análise de riscos com 3 dias de antecedência..."
I (Impact): "...o que permitiu que todos chegassem preparados e a decisão foi tomada em 20 min em vez de 1h."

Ou para feedback construtivo:
S: "No handoff da iniciativa de compliance semana passada..."
B: "...o documento de handoff não incluía as decisões já tomadas..."
I: "...o que me fez gastar 2 dias redescobrir contexto que já existia."
```

---

## 3. Scoring e interpretação

### Cálculo

```
Cross-Squad Effectiveness Score = Σ (scores das 7 dimensões)
Máximo: 35 pontos
```

### Faixas

| Score  | Nível         | Interpretação                                                |
|--------|--------------|-------------------------------------------------------------|
| 30-35  | World-class  | Squad opera como unidade coesa. Colaboração é diferencial    |
| 23-29  | Efetivo      | Colaboração boa com pontos de melhoria. Squad funcional      |
| 16-22  | Funcional    | Colaboração básica. Silos emergindo. Oportunidade grande     |
| 9-15   | Disfuncional | Mais atrito que valor. Intervenção necessária                |
| 1-8    | Tóxico       | Squad não funciona como time. Redesign necessário            |

---

## 4. Padrões comuns de disfunção cross-squad

| Padrão | Descrição | Sintomas | Tratamento |
|--------|-----------|----------|------------|
| **Silos** | Cada agente opera isoladamente | Surpresas frequentes, duplicação de esforço | KPIs compartilhados, sync regular |
| **Bottleneck** | Um agente é gargalo para todos | Filas de espera, frustração com SLAs | Redistribuir responsabilidades, automatizar |
| **Avoidance** | Agentes evitam conflito necessário | Decisões adiadas, passivo-agressividade | Framework de resolução, CEO modela o comportamento |
| **Blame game** | Quando algo falha, culpar outro agente | Post-mortems tóxicos, defensividade | Blameless post-mortems, foco em sistema não indivíduo |
| **CEO bypass** | Agentes escalam tudo para CEO em vez de resolver entre si | CEO sobrecarregado, agentes desempoderados | Processo de escalação com tentativa obrigatória de resolução direta |
| **Information hoarding** | Agente retém informação como "poder" | Decisões ruins por falta de contexto | Cultura de transparência, informação como default público |

---

## 5. Cadência de avaliação

### Mensal: Quick pulse (10 minutos)
Cada agente responde 3 perguntas:
1. "Minha colaboração com os outros agentes este mês foi [1-5]"
2. "O maior atrito foi com [agente] sobre [tema]"
3. "Uma coisa que melhoraria a colaboração: [sugestão]"

### Trimestral: Full assessment (60 minutos)
1. Cada agente preenche a rubrica completa (7 dimensões)
2. Resultados agregados e comparados com quarter anterior
3. Top 3 ações de melhoria definidas com DRI e deadline
4. Celebrar dimensões que melhoraram

### Semestral: 360-degree review
Cada agente recebe feedback de todos os outros sobre:
- Qualidade dos handoffs recebidos deste agente
- Responsividade e cumprimento de SLAs
- Clareza de comunicação
- Gestão de dependências
- Abertura a feedback

---

## 6. Template de avaliação

```markdown
## Cross-Squad Effectiveness — [Período]

**Data:** [YYYY-MM-DD]
**Avaliador:** [agente ou todos]

### Scores

| # | Dimensão              | Score (1-5) | Evidência                    |
|---|----------------------|-------------|------------------------------|
| 1 | Handoff Quality      |             |                              |
| 2 | SLA Compliance       |             |                              |
| 3 | Communication Clarity|             |                              |
| 4 | Dependency Management|             |                              |
| 5 | Conflict Resolution  |             |                              |
| 6 | Shared KPI Alignment |             |                              |
| 7 | Feedback Loops       |             |                              |
|   | **TOTAL**            | **/35**     |                              |

### Trend vs. período anterior: [↑/→/↓]

### Pares de agentes com maior atrito:
1. [Agente A] ↔ [Agente B] — Tema: [tema] — Ação: [ação]

### Pares de agentes com melhor colaboração:
1. [Agente A] ↔ [Agente B] — O que funciona: [descrição]

### Top 3 ações de melhoria:
1. [Ação] — DRI: [agente] — Deadline: [data]
2. [Ação] — DRI: [agente] — Deadline: [data]
3. [Ação] — DRI: [agente] — Deadline: [data]
```

---

## 7. Métricas operacionais de colaboração

| Métrica                            | Como medir                              | Target           |
|------------------------------------|-----------------------------------------|------------------|
| Handoff rework rate                | % handoffs que requerem esclarecimento  | <10%             |
| SLA compliance rate                | % entregas inter-agente dentro do SLA   | >90%             |
| Dependency block time              | Tempo médio de bloqueio por dependência | <3 dias úteis    |
| Conflict resolution time           | Tempo médio do conflito até resolução   | <5 dias úteis    |
| Cross-squad NPS                    | "Recomendaria trabalhar com [agente]?"  | >40              |
| Shared KPI achievement             | % KPIs compartilhados atingidos         | >70%             |
| Feedback action completion rate    | % ações de feedback implementadas       | >80%             |
