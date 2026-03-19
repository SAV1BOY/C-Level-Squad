# Workflow 08: Executive Hiring — Contratação Executiva End-to-End

## Objetivo

Executar o processo completo de contratação executiva: desde a identificação
da necessidade até o onboarding 30/60/90. Este workflow garante rigor na
definição do perfil, scorecarding objetivo, processo de entrevista calibrado,
referências verificadas e transição suave para o novo executivo.

> **Princípio**: Contratação executiva é decisão Type 1 (irreversível no
> curto prazo). Trate com o rigor proporcional ao impacto.

---

## Agentes Envolvidos

| Agente | Papel | Fase Principal |
|--------|-------|---------------|
| **Vision Chief (CEO)** | Sponsor, entrevistador final, decisor | Fases 1, 4, 5, 7 |
| **COO Orchestrator** | Coordenador do processo, calibração | Todas |
| **CMO Architect** | Entrevistador (para roles de growth) | Fase 4 |
| **CTO Architect** | Entrevistador (para roles de tech) | Fase 4 |
| **CIO Engineer** | Entrevistador (para roles de IT/data) | Fase 4 |
| **CAIO Architect** | Entrevistador (para roles de IA) | Fase 4 |
| **CFO Strategist** | Valida compensation, budget | Fases 1, 6 |
| **Squad Coordinator** | Logística, tracking, comunicação | Todas |

---

## Trigger (quando iniciar)

- **Evento**: Posição executiva aberta (nova ou replacement)
- **Evento**: Gap de liderança identificado no org design review
- **Evento**: Succession plan ativado (saída planejada)
- **Pré-requisito**: Budget aprovado para a posição
- **Quem dispara**: Vision Chief ou COO Orchestrator

---

## Pré-condições

- [ ] Necessidade de contratação validada pelo Vision Chief
- [ ] Budget para compensation aprovado pelo CFO
- [ ] Org chart atual documentado
- [ ] Gap analysis concluído (qual competência falta?)
- [ ] Timeline desejado definido (urgência)
- [ ] Hiring bar definida: `checklists/people-culture/hiring-bar-quality.md`

---

## Processo (step-by-step com decision points)

### FASE 1: Identificação da Necessidade (Semana 1)

**Step 1.1 — Business Case da Posição**

- DRI: Vision Chief + COO Orchestrator
- Framework: `frameworks/operating-system/decision-memo-framework.md`
- Processo:
  1. Documentar o business case:
     - Por que esta posição é necessária agora?
     - Qual o impacto de NÃO contratar?
     - O problema pode ser resolvido sem contratar (redistribuição)?
     - Qual o ROI esperado da contratação?
  2. Definir nível e reporte:
     - Reports to: quem?
     - Direct reports: quantos?
     - Scope: quais áreas/squads?
     - Authority: que decisões pode tomar?
  3. Aprovar formalmente a abertura da posição
- Registro: `data/registries/hiring-registry.yaml`
- Registro: `data/registries/decision-registry.yaml`

**Step 1.2 — Competency Mapping**

- DRI: COO Orchestrator
- Processo:
  1. Mapear competências necessárias:
     - Must-have (inegociáveis): 3-5 competências
     - Nice-to-have (diferenciais): 2-3 competências
     - Culture fit: valores e comportamentos esperados
  2. Definir anti-perfil: o que NÃO queremos
  3. Benchmarking: qual o perfil típico no mercado?
  4. Compensation benchmark: faixa salarial competitiva
- Output: Competency Map

### FASE 2: Design do Role (Semana 1-2)

**Step 2.1 — Scorecard da Posição**

- DRI: COO Orchestrator + Vision Chief
- Template: `templates/org-people/exec-hiring-scorecard.md`
- Checklist: `checklists/hiring-executive-quality.md`
- Estrutura do Scorecard:

```
POSIÇÃO: [Título]
REPORTS TO: [Nome/Cargo]
DATE: [Data de abertura]

MISSÃO DA POSIÇÃO (1 frase):
"[O que esta pessoa vai realizar em 12 meses]"

OUTCOMES ESPERADOS (3-5):
1. [Resultado mensurável em 6 meses]
2. [Resultado mensurável em 12 meses]
3. [Resultado mensurável em 12 meses]

COMPETÊNCIAS (scored 1-5 em entrevista):
Must-have:
1. [Competência] — [como avaliar]
2. [Competência] — [como avaliar]
3. [Competência] — [como avaliar]

Nice-to-have:
1. [Competência] — [como avaliar]
2. [Competência] — [como avaliar]

CULTURE FIT:
1. [Valor/Comportamento] — [como avaliar]
2. [Valor/Comportamento] — [como avaliar]

ANTI-PERFIL (red flags):
1. [Comportamento/Sinal de alerta]
2. [Comportamento/Sinal de alerta]

COMPENSATION RANGE: R$ [min] - R$ [max]
```

**Step 2.2 — Interview Design**

- DRI: COO Orchestrator
- Processo:
  1. Definir interview loop:

| Etapa | Entrevistador | Foco | Duração |
|-------|--------------|------|---------|
| Screen | Squad Coordinator | Fit básico, motivação | 30 min |
| Technical/Functional | C-Level da área | Competência técnica | 60 min |
| Case Study | COO + outro C-Level | Problem-solving | 60 min |
| Culture Fit | Vision Chief | Valores, visão | 45 min |
| Reverse Interview | Candidato pergunta | Alinhamento bilateral | 30 min |

  2. Para cada etapa, definir:
     - Perguntas obrigatórias (estruturadas)
     - Scoring criteria (1-5 em cada dimensão)
     - Red flags a observar
     - Decision: advance / hold / reject
  3. Definir quórum para decisão: quem tem veto?
- Referência: `workflows/hiring/03-interview-process.md`

### FASE 3: Sourcing (Semana 2-4)

**Step 3.1 — Definição da Estratégia de Sourcing**

- DRI: COO Orchestrator
- Referência: `workflows/hiring/02-sourcing-pipeline.md`
- Processo:
  1. Canais de sourcing:
     - Network pessoal do C-Level (prioridade #1)
     - Headhunter especializado (se posição senior)
     - LinkedIn outbound
     - Comunidades e eventos
     - Candidaturas inbound (job post)
  2. Definir target: quantos candidatos qualificados no pipeline?
     - Ideal: 5-8 candidatos qualificados para shortlist
  3. Preparar pitch da posição:
     - Por que esta empresa?
     - Por que agora?
     - O que a pessoa vai construir?
     - Compensation e equity (se aplicável)
  4. Definir timeline de sourcing: 2-4 semanas
- **Decision Point**: Usar headhunter?
  - **SIM** → Briefar headhunter com scorecard, pagar fee
  - **NÃO** → Sourcing interno (network + LinkedIn)

**Step 3.2 — Pipeline Management**

- DRI: Squad Coordinator
- Processo:
  1. Tracker de candidatos:
     - Nome, fonte, status, score parcial
  2. Weekly sync de pipeline (15 min):
     - Quantos no funil?
     - Quantos avançam?
     - Blockers?
  3. Quality over quantity: não avançar candidatos medianos
- Registro: `data/registries/hiring-registry.yaml`

### FASE 4: Interview Process (Semana 4-6)

**Step 4.1 — Screen (por candidato)**

- DRI: Squad Coordinator
- Duração: 30 min
- Avaliar:
  - Motivação: por que está interessado?
  - Fit básico: experiência, competências macro
  - Red flags iniciais: instabilidade, narrativa inconsistente
  - Availability: quando pode começar?
- **Decision Point**: Avançar para entrevista técnica?
  - Score >= 3/5 em todos os critérios → Avançar
  - Qualquer red flag → Rejeitar com feedback

**Step 4.2 — Technical/Functional Interview**

- DRI: C-Level da área relevante
- Duração: 60 min
- Avaliar (usando scorecard):
  - Profundidade técnica/funcional
  - Tomada de decisão sob ambiguidade
  - Exemplos concretos de resultados
  - Escala: já operou no nível que precisamos?
- Técnica: perguntas comportamentais STAR (Situation, Task, Action, Result)
- **Decision Point**: Score médio >= 3.5/5?
  - **SIM** → Avançar para case study
  - **NÃO** → Rejeitar com feedback

**Step 4.3 — Case Study**

- DRI: COO Orchestrator + outro C-Level
- Duração: 60 min
- Processo:
  1. Apresentar case relevante para a posição (baseado em desafio real)
  2. Candidato tem 10 min para ler e 20 min para apresentar abordagem
  3. 30 min de discussão e desafio
- Avaliar:
  - Structured thinking
  - Priorização
  - Comunicação
  - Capacidade de ser desafiado
  - Pragmatismo vs perfeccionismo
- **Decision Point**: Score médio >= 3.5/5?
  - **SIM** → Avançar para culture fit
  - **NÃO** → Rejeitar com feedback

**Step 4.4 — Culture Fit Interview**

- DRI: Vision Chief
- Duração: 45 min
- Avaliar:
  - Alinhamento com valores da empresa
  - Estilo de liderança
  - Como lida com conflito e ambiguidade
  - Visão de longo prazo pessoal vs empresa
  - "Eu gostaria de trabalhar com esta pessoa?"
- **Decision Point**: Culture fit aprovado?
  - **SIM** → Avançar para referências
  - **NÃO** → Rejeitar (culture fit é eliminatório)

### FASE 5: Calibração e Referências (Semana 6-7)

**Step 5.1 — Calibration Session**

- DRI: COO Orchestrator
- Participantes: Todos os entrevistadores
- Duração: 60 min
- Processo:
  1. Cada entrevistador apresenta seus scores e observações
  2. Consolidar scorecard final do candidato
  3. Discutir discrepâncias (scores muito diferentes)
  4. Identificar riscos e como mitigar
  5. Ranking de candidatos (se múltiplos)
  6. Decisão: top 1-2 candidatos para referências
- **Regra**: Nenhum candidato avança com red flag não resolvida
- Checklist: `checklists/people-culture/hiring-bar-quality.md`

**Step 5.2 — Reference Checks**

- DRI: Vision Chief ou COO Orchestrator
- Processo:
  1. Solicitar 3-5 referências do candidato:
     - 1-2 ex-chefes diretos
     - 1-2 ex-reports diretos
     - 1 par (colega de mesmo nível)
  2. Realizar back-channel references (não fornecidas):
     - Através da rede do C-Level
     - Mínimo 2 back-channels
  3. Perguntas obrigatórias para referências:
     - "Qual a maior força dessa pessoa?"
     - "Qual a maior área de desenvolvimento?"
     - "Você a contrataria de novo? Para qual posição?"
     - "Como ela lida com pressão e conflito?"
     - "O que eu deveria saber que ela não vai me contar?"
  4. Consolidar feedback de referências
- **Decision Point**: Referências confirmam o perfil?
  - **SIM** → Avançar para oferta
  - **NÃO** → Reavaliar candidato (risk assessment)
  - **RED FLAG** → Rejeitar

### FASE 6: Oferta (Semana 7-8)

**Step 6.1 — Package Design**

- DRI: CFO Strategist + Vision Chief
- Processo:
  1. Definir compensation package:
     - Base salary (dentro do range aprovado)
     - Variable/bonus (se aplicável)
     - Equity/options (se aplicável)
     - Benefits
     - Signing bonus (se necessário para fechar)
  2. Definir start date
  3. Definir probation period e critérios
  4. Preparar carta-oferta formal
- Referência: `workflows/hiring/04-offer-negotiation.md`

**Step 6.2 — Offer Delivery**

- DRI: Vision Chief
- Processo:
  1. Ligação pessoal do Vision Chief para comunicar a oferta
  2. Sell da oportunidade: visão, desafio, impacto
  3. Apresentar package por escrito
  4. Dar prazo de decisão (72h-1 semana)
- **Decision Point**: Candidato aceita?
  - **SIM** → Avançar para onboarding prep
  - **NEGOCIAÇÃO** → CFO + Vision Chief definem limites, contraproposta
  - **REJEIÇÃO** → Acionar próximo candidato ou reabrir sourcing

### FASE 7: Onboarding 30/60/90 (Pós-contratação)

**Step 7.1 — Pre-boarding (Antes do Day 1)**

- DRI: COO Orchestrator + Squad Coordinator
- Processo:
  1. Preparar 30/60/90 plan
  2. Configurar acessos e tooling
  3. Agendar reuniões de onboarding
  4. Preparar welcome kit (contexto do squad, docs chave)
  5. Designar buddy/mentor
- Template: `templates/org-people/30-60-90-plan.md`
- Referência: `workflows/hiring/05-onboarding-30-60-90.md`

**Step 7.2 — Kick-off com o Novo Executivo**

- DRI: Vision Chief
- Processo:
  1. Reunião 1:1 Vision Chief + novo executivo (Day 1)
  2. Compartilhar: missão, visão, tese, bets, OKRs
  3. Expectativas claras: o que sucesso significa em 30/60/90 dias
  4. Introdução ao C-Level Squad e cadência
  5. Apresentação formal para a organização

**Step 7.3 — Acompanhamento**

- DRI: COO Orchestrator
- Cadência:
  - Semana 1-2: Check-in diário (15 min)
  - Semana 3-4: Check-in 2x/semana
  - Mês 2: Check-in semanal
  - Mês 3: Check-in quinzenal
- Checkpoints formais:
  - 30 dias: avaliação de adaptação
  - 60 dias: avaliação de contribuição
  - 90 dias: avaliação de liderança
- Detalhamento: `workflows/10-30-60-90-onboarding.md`

---

## Quality Gates

### Gate 1: Qualidade do Scorecard

Aplicar `checklists/hiring-executive-quality.md`:
- [ ] Missão da posição clara e mensurável
- [ ] 3-5 outcomes esperados definidos
- [ ] Competências must-have com método de avaliação
- [ ] Anti-perfil documentado
- [ ] Compensation range aprovado pelo CFO

### Gate 2: Qualidade do Processo

Aplicar `checklists/people-culture/hiring-bar-quality.md`:
- [ ] Todos os entrevistadores calibrados no scorecard
- [ ] Perguntas estruturadas (não free-form)
- [ ] Scores registrados independentemente (sem group bias)
- [ ] Calibration session realizada antes da decisão
- [ ] Referências verificadas (incluindo back-channel)

### Gate 3: Qualidade da Decisão

- [ ] Scorecard final consolidado com scores numéricos
- [ ] Nenhum red flag não resolvido
- [ ] Vision Chief + COO alinhados na decisão
- [ ] Compensation dentro do range aprovado
- [ ] 30/60/90 plan preparado antes do Day 1

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| Business case da posição | Markdown | `data/memos/` | Vision Chief |
| Scorecard da posição | Markdown | `templates/org-people/exec-hiring-scorecard.md` | COO |
| Interview scorecards (por candidato) | Markdown | `data/memos/` | Cada entrevistador |
| Reference check report | Markdown | `data/memos/` | Vision Chief |
| Calibration session notes | Markdown | `data/meeting-minutes/` | COO |
| Offer letter | Documento | Confidencial | CFO |
| 30/60/90 plan | Markdown | `templates/org-people/30-60-90-plan.md` | COO |

---

## Registries Atualizados

- `data/registries/hiring-registry.yaml` — Posição, candidatos, decisão, timeline
- `data/registries/decision-registry.yaml` — Decisão de contratação com racional

---

## Próximos Passos

1. **Imediato pós-aceite**: Preparar onboarding → `workflows/10-30-60-90-onboarding.md`
2. **Day 1**: Kick-off com Vision Chief
3. **30 dias**: Primeiro checkpoint formal
4. **60 dias**: Segundo checkpoint
5. **90 dias**: Avaliação completa e confirmação

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| Vision Chief | Organização | Anúncio do novo executivo | Day 1 |
| COO | Squads do novo exec | Briefing de transição | Semana 1 |
| Squad Coordinator | Novo executivo | Welcome kit + contexto | Pre Day 1 |
| COO | Data Squad | Acessos e dashboards | Day 1 |
| CIO | IT | Setup de ferramentas e acessos | Pre Day 1 |
