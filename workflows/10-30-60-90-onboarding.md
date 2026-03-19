# Workflow 10: 30-60-90 Onboarding — Integração Executiva Estruturada

## Objetivo

Garantir que novos executivos atinjam produtividade máxima em 90 dias
através de um plano estruturado em 3 fases: 30 dias de aprendizado
(absorver contexto), 60 dias de contribuição (entregar early wins) e
90 dias de liderança (assumir ownership plena). Cada fase tem milestones,
checkpoints e mentoring definidos.

> **Princípio**: Os primeiros 90 dias definem os próximos 900.
> Onboarding ruim é a causa #1 de turnover executivo prematuro.

---

## Agentes Envolvidos

| Agente | Papel | Fase |
|--------|-------|------|
| **Vision Chief (CEO)** | Sponsor, mentor estratégico | Todas (checkpoints) |
| **COO Orchestrator** | Coordenador do onboarding, mentor operacional | Todas |
| **C-Level da área** | Mentor funcional (se aplicável) | Todas |
| **Squad Coordinator** | Facilitador, logística | Todas |
| **Buddy designado** | Suporte informal | Dias 1-30 |

---

## Trigger (quando iniciar)

- **Evento**: Novo executivo aceitou a oferta
- **Timing**: Pre-boarding inicia 1-2 semanas antes do Day 1
- **Duração total**: 90 dias com checkpoints em 30, 60 e 90
- **Quem dispara**: COO Orchestrator (automático pós-aceite)

---

## Pré-condições

- [ ] Oferta aceita e start date confirmado
- [ ] 30/60/90 plan customizado para a posição
- [ ] Buddy designado e briefado
- [ ] Acessos e tooling solicitados ao CIO/IT
- [ ] Agenda de onboarding preparada (primeiras 2 semanas)
- [ ] Welcome kit preparado (documentação-chave)
- [ ] Stakeholder map: com quem o novo exec precisa falar
- [ ] Scorecard da posição revisado (outcomes esperados)

---

## Processo (step-by-step com decision points)

### PRE-BOARDING (1-2 semanas antes do Day 1)

**Step 0.1 — Preparação do Welcome Kit**

- DRI: Squad Coordinator
- Conteúdo do welcome kit:
  1. **Contexto do negócio**:
     - Missão, visão e tese estratégica
     - Bets ativos e status
     - OKRs do trimestre atual
     - Org chart e quem é quem
  2. **Contexto operacional**:
     - ARCHITECTURE.md (constituição do squad)
     - config.yaml (como o squad funciona)
     - Cadência: WBR/MBR/QBR (horários, formato)
     - Glossário de termos internos
  3. **Contexto da posição**:
     - Scorecard da posição (outcomes esperados)
     - OKRs herdados ou a definir
     - Stakeholder map
     - Iniciativas em andamento na área
  4. **Contexto da equipe**:
     - Quem são os reports diretos
     - Team health recent (survey results)
     - Desafios conhecidos
- Output: Welcome kit digital (pasta organizada)

**Step 0.2 — Setup de Tooling e Acessos**

- DRI: CIO Engineer + Squad Coordinator
- Checklist:
  - [ ] Email e comunicação (Slack/Teams)
  - [ ] Repositório C-Level Squad (acesso completo)
  - [ ] Dashboards de métricas
  - [ ] Calendar com cadências já agendadas
  - [ ] Sistemas da área específica
  - [ ] VPN e segurança (se aplicável)
- SLA: Tudo pronto até Day 1

**Step 0.3 — Agenda das Primeiras 2 Semanas**

- DRI: COO Orchestrator
- Estrutura de agenda:

| Dia | Atividade | Com quem | Duração |
|-----|-----------|----------|---------|
| 1 | Welcome + Vision/Tese | Vision Chief | 90 min |
| 1 | Sistema operacional (cadências, processos) | COO Orchestrator | 60 min |
| 1 | Setup de tools + tour | Squad Coordinator | 60 min |
| 2 | Deep dive na área | C-Level mentor | 120 min |
| 2 | Meet the team | Reports diretos | 60 min |
| 3 | 1:1 com CMO | CMO Architect | 45 min |
| 3 | 1:1 com CTO | CTO Architect | 45 min |
| 4 | 1:1 com CIO | CIO Engineer | 45 min |
| 4 | 1:1 com CAIO | CAIO Architect | 45 min |
| 5 | 1:1 com CFO | CFO Strategist | 45 min |
| 5 | Retrospectiva Semana 1 | COO Orchestrator | 30 min |
| 6-10 | 1:1 com squad leads | Squads relevantes | 30 min cada |
| 6-10 | Deep dive em iniciativas ativas | DRIs das iniciativas | 45 min cada |
| 10 | Retrospectiva Semana 2 | COO + Vision Chief | 45 min |

---

### FASE 1: APRENDIZADO — Dias 1-30

**Mantra dos 30 dias: "Escute mais, fale menos. Absorva o contexto."**

**Step 1.1 — Imersão Estratégica (Semana 1)**

- DRI: Vision Chief
- Atividades:
  1. 1:1 profundo com Vision Chief:
     - História da empresa: de onde viemos, por que existimos
     - Tese estratégica: o que acreditamos, por que estamos certos
     - Bets ativos: no que estamos apostando
     - Kill list: o que decidimos não fazer
     - Expectations: o que o CEO espera em 30/60/90 dias
  2. Ler e absorver documentos-chave:
     - ARCHITECTURE.md
     - Tese estratégica atual
     - Últimos 3 MBR/QBR atas
     - OKR scorecard do trimestre anterior
  3. Formular primeiras perguntas (não respostas)
- Output: Lista de perguntas do novo exec (documentar)

**Step 1.2 — Imersão Operacional (Semana 1-2)**

- DRI: COO Orchestrator
- Atividades:
  1. Participar como observador no próximo WBR
  2. Revisar metrics pack: entender cada métrica
  3. Mapear processos-chave da área:
     - Como decisões são tomadas?
     - Onde estão os bottlenecks?
     - Quais são os handoffs críticos?
  4. Entender cadência e ritmo do squad
- Output: Notas de observação do novo exec

**Step 1.3 — Relationship Building (Semana 2-3)**

- DRI: Novo executivo (com suporte do buddy)
- Atividades:
  1. 1:1 com cada C-Level (já agendado):
     - Entender suas prioridades e desafios
     - Identificar pontos de conexão e dependência
     - Perguntar: "O que eu deveria saber que ninguém vai me contar?"
  2. 1:1 com squad leads relevantes:
     - Entender dinâmica dos times
     - Identificar talentos-chave
     - Entender frustrações e ambições
  3. 1:1 com stakeholders externos (clientes, partners) se aplicável
  4. Almoços/cafés informais com pares
- Output: Stakeholder relationship map pessoal

**Step 1.4 — Diagnóstico da Área (Semana 3-4)**

- DRI: Novo executivo
- Atividades:
  1. Com base nas primeiras semanas, documentar:
     - **O que está funcionando** (preservar)
     - **O que precisa melhorar** (oportunidades)
     - **Quick wins** (mudanças de baixo risco, alto impacto)
     - **Big bets** (mudanças de longo prazo)
     - **Riscos** identificados
  2. Preparar "30-Day Observations" document
  3. Compartilhar draft com COO para feedback
  4. NÃO fazer mudanças grandes ainda — apenas diagnosticar
- Output: 30-Day Observations Document

**Step 1.5 — Checkpoint de 30 Dias**

- DRI: Vision Chief + COO Orchestrator
- Participantes: Novo executivo
- Duração: 60 min
- Agenda:
  1. Novo exec apresenta suas observações (20 min)
  2. Vision Chief e COO dão feedback (15 min)
  3. Alinhamento de prioridades para dias 31-60 (15 min)
  4. Check de satisfação mútua (10 min):
     - "A posição é o que esperava?"
     - "O suporte está adequado?"
     - "Há algo que precisa mudar?"
- Avaliação (30 dias):

| Dimensão | Critério | Score (1-5) |
|----------|---------|-------------|
| Contexto | Entende a tese, bets e OKRs | |
| Relacionamentos | Conhece todos os stakeholders-chave | |
| Área | Entende estado atual da área | |
| Cultura | Se adaptou ao estilo de trabalho | |
| Diagnóstico | Apresentou observações relevantes | |

- **Decision Point**: Checkpoint satisfatório?
  - **SIM** → Avançar para Fase 2
  - **PARCIAL** → Ajustar plano, intensificar suporte
  - **NÃO** → Conversa séria: gap de fit ou suporte insuficiente?
- Registro: `data/registries/hiring-registry.yaml`

---

### FASE 2: CONTRIBUIÇÃO — Dias 31-60

**Mantra dos 60 dias: "Entregue early wins. Prove capacidade."**

**Step 2.1 — Definição de Quick Wins (Semana 5)**

- DRI: Novo executivo + COO Orchestrator
- Processo:
  1. Com base no diagnóstico de 30 dias:
     - Selecionar 2-3 quick wins para entregar em 30 dias
     - Critérios de seleção:
       - Baixo risco
       - Alto impacto visível
       - Demonstra competência
       - Não depende de aprovação longa
  2. Definir para cada quick win:
     - O que será entregue
     - Métrica de sucesso
     - Timeline
     - Recursos necessários
  3. Validar com Vision Chief e COO
- Output: Quick Wins Plan

**Step 2.2 — Execução dos Quick Wins (Semana 5-8)**

- DRI: Novo executivo
- Processo:
  1. Executar quick wins com transparência:
     - Comunicar o que está fazendo e por quê
     - Envolver o time (não fazer sozinho)
     - Medir resultado
  2. Report de progresso no WBR semanal
  3. Pedir feedback contínuo
- **Regra**: Quick wins devem ser genuínos, não teatro

**Step 2.3 — OKR Ownership (Semana 5-6)**

- DRI: Novo executivo + COO Orchestrator
- Processo:
  1. Assumir ownership dos OKRs da área:
     - Revisar OKRs herdados: ainda fazem sentido?
     - Propor ajustes se necessário (via COO para validação)
     - Definir como vai medir e reportar
  2. Começar a contribuir ativamente no WBR
  3. Assumir responsabilidade por initiative health da área
- Framework: `frameworks/operating-system/okrs.md`

**Step 2.4 — Team Assessment (Semana 6-8)**

- DRI: Novo executivo
- Processo:
  1. Avaliar cada report direto:
     - Performance atual (dados + observação)
     - Potencial de crescimento
     - Fit com a nova direção
     - Gaps de competência
  2. Identificar:
     - Stars: top performers para investir
     - Solid: bons profissionais para manter
     - Develop: potencial mas precisa de suporte
     - Address: performance insuficiente
  3. NÃO fazer mudanças de pessoal nos primeiros 60 dias
     (exceto urgências óbvias)
  4. Documentar assessment para discussão no checkpoint
- Output: Team Assessment (confidencial)

**Step 2.5 — Checkpoint de 60 Dias**

- DRI: Vision Chief + COO Orchestrator
- Participantes: Novo executivo
- Duração: 60 min
- Agenda:
  1. Review dos quick wins: entregou? Impacto? (15 min)
  2. OKR ownership: progresso? Ajustes? (15 min)
  3. Team assessment: observações? Preocupações? (15 min)
  4. Plano para dias 61-90 (15 min)
- Avaliação (60 dias):

| Dimensão | Critério | Score (1-5) |
|----------|---------|-------------|
| Quick wins | Entregou 2-3 resultados visíveis | |
| OKRs | Assumiu ownership e está contribuindo | |
| Team | Avaliou o time com lucidez | |
| Decisões | Está tomando decisões Type 2 com confiança | |
| Cultura | É visto como membro do C-Level Squad | |
| Comunicação | Comunica com clareza no WBR/MBR | |

- **Decision Point**: Checkpoint satisfatório?
  - **SIM** → Avançar para Fase 3
  - **PARCIAL** → Feedback direto, plano de aceleração
  - **NÃO** → Performance improvement conversation (considerar off-ramp)
- Registro: `data/registries/hiring-registry.yaml`

---

### FASE 3: LIDERANÇA — Dias 61-90

**Mantra dos 90 dias: "Lidere com visão. Assuma plena responsabilidade."**

**Step 3.1 — Strategic Initiative Ownership (Semana 9-10)**

- DRI: Novo executivo
- Processo:
  1. Propor 1 iniciativa estratégica para os próximos 6 meses:
     - Baseada no diagnóstico e aprendizados
     - Alinhada com bets e OKRs
     - Com roadmap, resources e kill criteria
  2. Apresentar para Vision Chief e C-Level para aprovação
  3. Se aprovada, iniciar execução
- Framework: `frameworks/coo-orchestrator/coo-execution-engine.md`

**Step 3.2 — Full Cadence Participation (Semana 9-12)**

- DRI: Novo executivo
- Processo:
  1. Participar ativamente em todas as cadências:
     - WBR: apresentar métricas da área, discutir exceções
     - MBR: apresentar bloco completo da área
     - C-Level sync: contribuir com perspectiva
  2. Contribuir para decisões cross-area
  3. Gerenciar handoffs com squads
- Expectativa: Comportamento indistinguível de C-Level veterano

**Step 3.3 — Team Decisions (Semana 10-12)**

- DRI: Novo executivo (com coaching do COO)
- Processo:
  1. Com base no team assessment:
     - Implementar planos de desenvolvimento para "Develop"
     - Iniciar performance conversations para "Address"
     - Promover/reconhecer "Stars"
  2. Propor ajustes de estrutura na área (se necessário)
  3. Definir hiring needs (se gaps identificados)
- **Regra**: Mudanças de pessoal requerem alinhamento com Vision Chief

**Step 3.4 — Cross-squad Integration (Semana 10-12)**

- DRI: Novo executivo
- Processo:
  1. Assumir ownership plena dos cross-squad handoffs da área
  2. Negociar SLAs com squads dependentes
  3. Resolver bottlenecks cross-squad pendentes
  4. Representar a área em decisões cross-funcionais

**Step 3.5 — 90-Day Plan Forward (Semana 12)**

- DRI: Novo executivo
- Processo:
  1. Preparar documento "90-Day Assessment & Forward Plan":
     - O que aprendi (insights-chave)
     - O que entreguei (quick wins + resultados)
     - Estado da área (honesto, com dados)
     - Plano para os próximos 6 meses
     - Resources que precisa
     - Riscos que vejo
  2. Apresentar para Vision Chief e COO

**Step 3.6 — Checkpoint de 90 Dias (FINAL)**

- DRI: Vision Chief + COO Orchestrator
- Participantes: Novo executivo
- Duração: 90 min
- Agenda:
  1. Apresentação do 90-Day Assessment (30 min)
  2. Feedback do Vision Chief e COO (20 min)
  3. Discussão de forward plan (20 min)
  4. Decisão formal de confirmação (20 min)
- Avaliação (90 dias):

| Dimensão | Critério | Score (1-5) |
|----------|---------|-------------|
| Resultados | Entregou quick wins + early impact | |
| Liderança | Lidera a área com confiança e clareza | |
| Estratégia | Propôs iniciativa estratégica relevante | |
| Time | Gerencia e desenvolve o time | |
| Cross-squad | Gerencia handoffs e dependências | |
| Cultura | É referência nos valores da empresa | |
| Cadência | Participa ativamente e contribui em WBR/MBR | |
| Autonomia | Toma decisões Type 2 sem pedir permissão | |

- **Decision Point**: Confirmação formal?
  - **CONFIRMADO** → Celebrar, registrar, plano de 6 meses ativado
  - **EXTENSÃO** → Mais 30 dias com metas específicas
  - **OFF-RAMP** → Conversa honesta, transição planejada
- Registro: `data/registries/hiring-registry.yaml`
- Registro: `data/registries/decision-registry.yaml`

---

## Quality Gates

### Gate 1: Qualidade do Pre-boarding

- [ ] Welcome kit completo e entregue
- [ ] Acessos e tooling prontos no Day 1
- [ ] Agenda de 2 semanas montada
- [ ] Buddy designado e briefado
- [ ] Stakeholder map preparado

### Gate 2: Qualidade do Checkpoint 30

- [ ] Novo exec participou de pelo menos 3 WBRs como observador
- [ ] 1:1 com todos os C-Level realizados
- [ ] 30-Day Observations document entregue
- [ ] Relacionamentos-chave construídos
- [ ] Score médio >= 3/5 em todas as dimensões

### Gate 3: Qualidade do Checkpoint 60

- [ ] 2-3 quick wins entregues com resultado mensurável
- [ ] OKR ownership assumida
- [ ] Team assessment realizado
- [ ] Participação ativa no WBR
- [ ] Score médio >= 3.5/5 em todas as dimensões

### Gate 4: Qualidade do Checkpoint 90

Aplicar `checklists/people-culture/hiring-bar-quality.md`:
- [ ] Iniciativa estratégica proposta e aprovada
- [ ] Participação plena em todas as cadências
- [ ] Team management ativo (1:1s, coaching, decisions)
- [ ] Cross-squad handoffs funcionando
- [ ] 90-Day Assessment document entregue
- [ ] Score médio >= 4/5 em todas as dimensões

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| Welcome Kit | Folder digital | Compartilhado com exec | Squad Coordinator |
| Agenda de onboarding | Markdown | `data/memos/` | COO |
| 30-Day Observations | Markdown | `data/memos/` | Novo executivo |
| Quick Wins Plan | Markdown | `data/memos/` | Novo executivo |
| Team Assessment | Markdown | Confidencial | Novo executivo |
| 90-Day Assessment & Forward Plan | Markdown | `data/memos/` | Novo executivo |
| Checkpoint reports (30/60/90) | Markdown | `data/memos/` | COO |
| 30/60/90 Plan | Markdown | `templates/org-people/30-60-90-plan.md` | COO |

---

## Registries Atualizados

- `data/registries/hiring-registry.yaml` — Status onboarding, checkpoints, decisão final
- `data/registries/decision-registry.yaml` — Decisão de confirmação (90 dias)
- `data/registries/initiative-registry.yaml` — Iniciativa proposta pelo novo exec
- `data/registries/culture-registry.yaml` — Observações de culture fit

---

## Próximos Passos

1. **Pós-confirmação**: Novo exec entra no ritmo normal do C-Level Squad
2. **6 meses**: First performance review formal
3. **12 meses**: Full year review (vs scorecard da posição)
4. **Contínuo**: Mentoring do Vision Chief (quarterly 1:1 estratégico)
5. **Contínuo**: Development plan baseado no team assessment

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| COO | Todos C-Level | Briefing sobre novo executivo | Pre-Day 1 |
| Squad Coordinator | CIO/IT | Request de acessos e tooling | 1 semana antes Day 1 |
| Vision Chief | Organização | Anúncio formal do novo exec | Day 1 |
| COO | Squads da área | Introdução + transição | Semana 1 |
| Buddy | Novo exec | Suporte informal diário | Dias 1-30 |
| Novo exec | Squads da área | Assumir ownership de handoffs | Dia 60+ |

### Sinais de Alerta durante Onboarding

Monitorar e agir se observar:

1. **Isolamento**: Novo exec não está construindo relacionamentos → Buddy intervém
2. **Over-promise**: Prometendo mudanças grandes antes de entender contexto → COO coaching
3. **Análise-paralisia**: Só diagnostica, não age → Empurrar para quick wins
4. **Criticismo excessivo**: Critica tudo sem propor soluções → Feedback direto
5. **Ignonrando cadência**: Não participa ou contribui em WBR/MBR → Conversa séria
6. **Team conflict**: Conflitos com reports diretos → COO media
7. **Desalinhamento cultural**: Comportamento inconsistente com valores → Vision Chief intervém
8. **Burnout precoce**: Trabalhando demais, sem equilíbrio → Buddy + COO intervêm

### Métricas de Sucesso do Onboarding

| Métrica | Target 30 dias | Target 60 dias | Target 90 dias |
|---------|---------------|----------------|----------------|
| Stakeholder meetings | 100% realizados | N/A | N/A |
| Quick wins entregues | N/A | >= 2 | >= 3 |
| WBR contribution | Observer | Active contributor | Full owner |
| Team 1:1s | Iniciados | Regular cadence | Coaching mode |
| OKR ownership | Understanding | Contributing | Leading |
| Decision autonomy | Consulting | Co-deciding | Deciding (Type 2) |
| Checkpoint score avg | >= 3.0 | >= 3.5 | >= 4.0 |
