# Unblock and Escalate

## Objetivo
Resolver blockers operacionais rapidamente e escalar de forma eficiente quando necessário. Blockers não resolvidos são o maior destruidor silencioso de velocity organizacional. Este processo garante que nenhum blocker persiste mais que o tempo máximo aceitável e que escalações são tratadas com urgência proporcional ao impacto.

## Agente Responsável
- **COO Agent** — Ponto central de detecção e resolução de blockers

## Agentes de Suporte
- **CEO Agent** — Escalation final e decisões cross-functional
- **CTO Agent** — Blockers técnicos e de engenharia
- **CFO Agent** — Blockers financeiros e de budget
- **CPO Agent** — Blockers de produto e priorização
- **CHRO Agent** — Blockers de pessoas e org design
- **CIO Agent** — Blockers de sistemas e infraestrutura
- **CAI Agent** — Blockers de AI e data

## Pré-requisitos
1. Sistema de tracking de blockers ativo e atualizado
2. Critérios de escalação definidos e publicados
3. SLAs de resolução por tipo de blocker documentados
4. Canais de comunicação rápida estabelecidos
5. Mapa de ownership claro (quem resolve o quê)

## Processo (step-by-step)

### Fase 1: Detecção de Blockers
1. Monitorar signals de blocker nas seguintes fontes:
   - WBR: métricas que não se movem por 2+ semanas
   - Slack/comunicação: padrões de frustração ou espera
   - Sprint reviews: items carregados entre sprints
   - 1:1s: feedbacks de líderes sobre impedimentos
   - Initiative health reviews: initiatives stuck em "yellow" por 2+ semanas
2. Classificar cada blocker por tipo: técnico, organizacional, financeiro, decisão pendente, dependência externa, recurso insuficiente
3. Avaliar impacto do blocker: qual OKR ou strategic bet está sendo impedido
4. Calcular o custo de delay: quanto custa cada dia/semana que o blocker persiste

### Fase 2: Triage e Classificação
5. Aplicar severity levels ao blocker:
   - **P0 (Critical):** Impacta revenue ou clientes agora — resolução em horas
   - **P1 (High):** Bloqueia strategic bet ou OKR principal — resolução em 1-2 dias
   - **P2 (Medium):** Impacta velocity de iniciativa — resolução em 1 semana
   - **P3 (Low):** Incomodante mas não blocking — resolução no próximo ciclo
6. Atribuir owner para resolução (accountability individual, não comitê)
7. Definir deadline de resolução baseado na severity
8. Comunicar o blocker para todos os stakeholders afetados

### Fase 3: Resolução
9. Owner do blocker inicia resolução dentro do SLA definido
10. Para blockers de decisão: agendar decisão com decision maker em <24h
11. Para blockers de recurso: avaliar realocação temporária ou alternativas
12. Para blockers técnicos: avaliar workaround vs fix permanente
13. Para blockers de dependência externa: acionar vendor/partner e definir plano B
14. Documentar a resolução e root cause para prevenir recorrência
15. Comunicar resolução para todos os stakeholders

### Fase 4: Escalação (quando necessário)
16. Escalar quando o blocker não pode ser resolvido pelo owner no SLA
17. Path de escalação: owner → área lead → COO → CEO
18. Cada nível de escalação tem SLA: 4h para responder à escalação
19. Escalação deve incluir: contexto, tentativas de resolução, opções, recomendação
20. Decisor da escalação tem 24h para resolver ou escalar novamente
21. Post-mortem obrigatório para todo blocker P0 e P1

### Fase 5: Prevenção
22. Analisar patterns de blockers mensalmente: tipos recorrentes, áreas mais afetadas
23. Identificar root causes sistêmicos que geram blockers repetidamente
24. Propor mudanças estruturais para eliminar categorias de blockers
25. Atualizar processos e ownership maps baseado nos learnings

## Frameworks a Aplicar
- **Severity Classification (P0-P3)** — Triage rápido baseado em impacto
- **Cost of Delay** — Quantificar o impacto financeiro do blocker por unidade de tempo
- **5 Whys Root Cause** — Encontrar a causa raiz, não apenas o sintoma
- **Escalation Matrix** — Path claro de escalação com SLAs em cada nível
- **Dependency Management** — Mapear e mitigar dependências proativamente
- **Blameless Post-Mortem** — Aprender sem culpar para blockers P0/P1

## Checklists de Qualidade
- [ ] Blocker documentado com contexto e impacto claro
- [ ] Severity atribuída (P0-P3) com justificativa
- [ ] Owner individual atribuído (não equipe)
- [ ] Deadline de resolução definido conforme SLA
- [ ] Stakeholders afetados notificados
- [ ] Tentativas de resolução documentadas antes de escalar
- [ ] Escalação incluiu contexto, opções e recomendação
- [ ] Resolução documentada com root cause
- [ ] Post-mortem executado para P0/P1
- [ ] Learnings incorporados para prevenção

## Template de Entrega
```markdown
# Blocker Report — [ID]

## Blocker Description
- **Title:** [Short description]
- **Detected:** [Date/Time]
- **Reporter:** [Who flagged]
- **Severity:** [P0/P1/P2/P3]
- **Type:** [Technical/Org/Financial/Decision/Dependency/Resource]

## Impact
- **OKR/Bet Affected:** [Which]
- **Teams Blocked:** [List]
- **Cost of Delay:** [R$/day or qualitative]
- **Revenue Impact:** [If applicable]

## Resolution
- **Owner:** [Individual]
- **Deadline:** [Based on SLA]
- **Resolution Path:** [Steps taken]
- **Root Cause:** [Why this happened]
- **Resolution:** [What was done]
- **Resolved:** [Date/Time]

## Escalation Log (if escalated)
| Level | Escalated To | Date | Response | Resolution |
|-------|-------------|------|----------|------------|

## Prevention
- **Recurrence Risk:** [High/Med/Low]
- **Structural Fix:** [What to change to prevent]
- **Owner of Fix:** [Who]
```

## Registries para Atualizar
- `registries/blockers-log.md` — Registrar blocker com status e resolução
- `registries/decisions-log.md` — Se resolução exigiu decisão executiva
- `registries/escalations.md` — Registrar escalações e outcomes
- `registries/lessons-learned.md` — Learnings de post-mortems

## Critérios de Aceitação
1. Todo blocker tem owner individual e deadline definido
2. SLAs de resolução respeitados em >90% dos casos
3. Escalações respondem em <4h
4. Post-mortem executado para 100% dos blockers P0 e P1
5. Análise mensal de patterns de blockers realizada
6. Zero blockers P0 ou P1 sem resolução por >48h

## Dependências e Handoffs
- **Recebe de:** WBR (anomalias), Sprint Reviews, 1:1s, Initiative Health Reviews
- **Entrega para:** Resolved teams, Post-mortem learnings, Process improvements
- **Cadência:** Contínuo (real-time para P0, daily check para P1-P3)
- **Escalation path:** Owner → Lead → COO → CEO (com SLAs em cada nível)
- **Integração:** Blockers P0/P1 são reportados no próximo WBR
