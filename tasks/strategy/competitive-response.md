# Competitive Response

## Objetivo
Avaliar movimentos competitivos relevantes e definir a resposta estratégica adequada. Nem todo movimento competitivo merece resposta — o objetivo é distinguir sinais de ruído, avaliar impacto real e executar uma resposta proporcional que proteja nossa posição sem desviar do foco estratégico.

## Agente Responsável
- **CEO Agent** — Decisão final sobre resposta competitiva

## Agentes de Suporte
- **CMO Agent** — Intelligence competitiva, market positioning e messaging response
- **CPO Agent** — Product response e feature gap analysis
- **CTO Agent** — Viabilidade técnica de respostas de produto
- **CFO Agent** — Impacto financeiro e pricing response analysis
- **COO Agent** — Capacidade operacional para executar resposta

## Pré-requisitos
1. Alerta de movimento competitivo com dados específicos
2. Market thesis atual (ver `tasks/strategy/market-thesis-update.md`)
3. Competitive intelligence baseline (positioning, pricing, features)
4. Win/loss data recente (últimos 90 dias)
5. Current strategic bets e prioridades
6. Customer feedback sobre o competidor em questão

## Processo (step-by-step)

### Fase 1: Triage e Assessment (24-48h)
1. Documentar o movimento competitivo com fatos verificáveis (não rumores)
2. Classificar o tipo de movimento: pricing, product launch, M&A, partnership, pivot, funding
3. Avaliar o impacto potencial em escala 1-5: revenue risk, customer risk, talent risk, market position
4. Determinar urgência: requer resposta imediata (dias), breve (semanas) ou pode esperar (meses)
5. Verificar se o movimento valida ou invalida alguma premissa da nossa market thesis
6. Coletar customer reaction data: estão mencionando o competidor? Pedindo features similares?

### Fase 2: Deep Analysis (2-3 dias se não urgente)
7. Analisar o "second order effect" do movimento: o que acontece se for bem-sucedido?
8. Mapear quais segmentos de clientes são mais afetados
9. Avaliar a sustentabilidade do movimento: é uma resposta pontual ou mudança estrutural?
10. Estimar o investimento necessário para diferentes tipos de resposta
11. Modelar cenários: não responder vs. resposta moderada vs. resposta agressiva
12. Consultar customers chave (informalmente) sobre percepção do movimento
13. Avaliar se o movimento abre oportunidades para nós (judo strategy)

### Fase 3: Response Design (1-2 dias)
14. Definir a strategic posture: attack, defend, absorb, ignore ou leapfrog
15. Desenhar o plano de resposta com ações específicas e timeline
16. Calcular custo e ROI esperado da resposta
17. Identificar trade-offs: o que deixamos de fazer para executar a resposta
18. Definir métricas de sucesso da resposta
19. Preparar comunicação: interna (equipe), externa (clientes, mercado) e sales enablement

### Fase 4: Execution e Monitoring (ongoing)
20. Executar o plano de resposta conforme timeline definido
21. Monitorar indicadores de eficácia da resposta
22. Coletar feedback de clientes e sales team sobre impacto
23. Ajustar resposta se necessário (iterate, não set-and-forget)
24. Documentar learnings para futuras respostas competitivas

## Frameworks a Aplicar
- **Competitive Response Matrix** — Classify: ignore / monitor / defend / attack / leapfrog
- **Impact-Urgency Matrix** — Priorizar resposta baseado em impacto real vs. urgência
- **OODA Loop (Boyd)** — Observe, Orient, Decide, Act — ciclo rápido de decisão
- **Judo Strategy** — Usar o movimento do competidor como alavanca a nosso favor
- **Asymmetric Response** — Responder onde somos fortes, não onde eles atacaram
- **Game Theory Basics** — Considerar reações secundárias antes de agir

## Checklists de Qualidade
- [ ] Movimento competitivo documentado com fatos verificáveis
- [ ] Impacto classificado em escala 1-5 com justificativa
- [ ] Urgência determinada com timeline de resposta
- [ ] Cenários modelados (não responder vs. responder)
- [ ] Trade-offs explícitos: o que deixamos de fazer
- [ ] Custo da resposta estimado e aprovado
- [ ] Comunicação preparada (interna, externa, sales)
- [ ] Métricas de sucesso definidas
- [ ] Owner da execução definido
- [ ] Plano de monitoramento estabelecido
- [ ] Não estamos reagindo a ruído (signal vs noise verified)
- [ ] Resposta não compromete strategic bets existentes

## Template de Entrega
```markdown
# Competitive Response — [Competitor] [Movement]

## Trigger
- **Date:** [When detected]
- **Competitor:** [Name]
- **Movement:** [Description factual]
- **Source:** [How we learned about it]

## Impact Assessment
- **Impact Score:** [1-5] — [Justificativa]
- **Urgency:** [Immediate/Short-term/Can wait]
- **Segments Affected:** [Customer segments at risk]
- **Revenue at Risk:** [R$ estimate]

## Analysis
- **Sustainability:** [One-time vs structural]
- **Second-order Effects:** [What happens if successful]
- **Opportunity Created:** [Any judo strategy angle]

## Response Decision
- **Posture:** [Ignore/Monitor/Defend/Attack/Leapfrog]
- **Rationale:** [Why this posture]

## Response Plan
| Action | Owner | Timeline | Cost | Expected Impact |
|--------|-------|----------|------|-----------------|

## Trade-offs
- **What we defer:** [Initiatives delayed]
- **Cost of response:** [R$ and opportunity cost]

## Success Metrics
| Metric | Baseline | Target | Timeline |
|--------|----------|--------|----------|

## Communication Plan
- **Internal:** [Key messages for team]
- **Sales Enablement:** [Battlecards, talk tracks]
- **Customer Communication:** [If needed]
- **Public/PR:** [If needed]

## Monitoring
- **Check-in cadence:** [Weekly/Bi-weekly]
- **Indicators to watch:** [List]
- **Escalation trigger:** [When to revisit]
```

## Registries para Atualizar
- `registries/competitive-intelligence.md` — Registrar o movimento e nossa resposta
- `registries/decisions-log.md` — Documentar a decisão de resposta e rationale
- `registries/risk-register.md` — Atualizar riscos competitivos
- `registries/strategic-bets.md` — Ajustar se a resposta impacta bets existentes

## Critérios de Aceitação
1. Movimento documentado com fatos verificáveis (não especulação)
2. Impact assessment completo com revenue at risk estimado
3. Decisão de resposta tomada com rationale claro
4. Trade-offs explicitamente documentados
5. Plano de execução com owners e timeline
6. Comunicação preparada para todos os públicos relevantes
7. Monitoramento configurado com check-in cadência definida

## Dependências e Handoffs
- **Recebe de:** Market Intelligence (CMO), Customer Feedback (CPO), Sales Data (CRO)
- **Entrega para:** Product Roadmap, Marketing Campaigns, Sales Enablement, Pricing
- **Cadência:** Ad-hoc, triggered por competitive alerts
- **SLA de resposta:** Triage em 24h, análise completa em 5 dias úteis
- **Escalation path:** Movimentos com impact score 4-5 escalam direto para CEO
