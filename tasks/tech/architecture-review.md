# Architecture Review and ADR

## Objetivo
Executar uma revisão arquitetural completa do sistema, documentando decisões de arquitetura (Architecture Decision Records — ADRs) e avaliando se a arquitetura atual suporta os requisitos de negócio atuais e futuros. Arquitetura errada é o tipo de tech debt mais caro — quanto mais tarde se descobre, mais custa corrigir.

## Agente Responsável
- **CTO Agent** — Ownership de decisões arquiteturais

## Agentes de Suporte
- **CIO Agent** — Integration architecture e data platform alignment
- **CAI Agent** — AI/ML architecture requirements
- **CPO Agent** — Product requirements e scalability needs
- **CFO Agent** — Cost implications de decisões arquiteturais
- **COO Agent** — Operational requirements (reliability, performance SLAs)

## Pré-requisitos
1. Documentação da arquitetura atual (diagramas, tech stack, data flow)
2. Product roadmap para próximos 12-18 meses
3. Performance e reliability data (latency, throughput, error rates, uptime)
4. Incident post-mortems dos últimos 6 meses
5. Infrastructure cost data (cloud spend breakdown)
6. Scaling requirements projetados (users, transactions, data volume)
7. Security e compliance requirements atualizados
8. ADRs anteriores documentados

## Processo (step-by-step)

### Fase 1: Current State Assessment (3-5 dias)
1. Mapear a arquitetura atual: componentes, serviços, dependências, data flows
2. Documentar o tech stack completo: linguagens, frameworks, databases, infra
3. Identificar architectural patterns em uso: monolith, microservices, event-driven, etc.
4. Medir health metrics: latency percentiles (p50, p95, p99), error rates, throughput
5. Analisar scaling characteristics: horizontal vs vertical, bottlenecks identificados
6. Mapear single points of failure e blast radius de cada componente
7. Avaliar security posture: authentication, authorization, encryption, vulnerability scan

### Fase 2: Requirements Analysis (2-3 dias)
8. Compilar requisitos de negócio para próximos 12-18 meses (do product roadmap)
9. Projetar scaling needs: 2x, 5x, 10x do volume atual
10. Identificar novos capabilities necessários que a arquitetura atual não suporta
11. Documentar compliance e regulatory requirements (LGPD, SOC2, HIPAA, etc.)
12. Avaliar AI/ML infrastructure needs para AI strategy
13. Identificar integration requirements com novos sistemas ou parceiros
14. Definir reliability targets: SLOs para cada serviço crítico

### Fase 3: Gap Analysis e Architecture Evaluation (2-3 dias)
15. Comparar capabilities atuais vs. requirements futuros — identificar gaps
16. Classificar gaps por severity: blocker, significant, nice-to-have
17. Para cada gap blocker, propor solução arquitetural com trade-offs documentados
18. Avaliar "evolutionary architecture" viability: podemos evoluir incrementalmente?
19. Identificar onde refactoring vs. rewrite é necessário
20. Estimar esforço e custo para cada mudança arquitetural proposta
21. Avaliar build vs. buy para novos components

### Fase 4: ADR Creation (1-2 dias)
22. Para cada decisão arquitetural significativa, criar um ADR:
    - Context: situação e constraints
    - Decision: o que decidimos
    - Consequences: trade-offs aceitos
    - Alternatives considered: o que mais avaliamos
23. Classificar ADRs por impacto: Type 1 (irreversível) vs Type 2 (reversível)
24. Submeter ADRs Type 1 para review ampliado (CTO + senior engineers)
25. Publicar ADRs em repositório acessível a toda engenharia

### Fase 5: Roadmap e Communication (1-2 dias)
26. Criar architecture evolution roadmap com quarters definidos
27. Estimar investment necessário por fase
28. Apresentar para executive team com business justification
29. Comunicar para engineering team com context e rationale
30. Definir success metrics para cada mudança arquitetural

## Frameworks a Aplicar
- **C4 Model** — Context, Container, Component, Code diagrams
- **ADR (Architecture Decision Records)** — Documentação padronizada de decisões
- **Fitness Functions** — Métricas automatizadas que validam architectural characteristics
- **ATAM (Architecture Tradeoff Analysis)** — Avaliação sistemática de trade-offs
- **Evolutionary Architecture** — Guiar mudanças incrementais com fitness functions
- **Cell-Based Architecture** — Para avaliação de blast radius e fault isolation

## Checklists de Qualidade
- [ ] Arquitetura atual documentada com diagramas C4
- [ ] Tech stack completo catalogado
- [ ] Performance baselines documentadas (p50, p95, p99)
- [ ] Single points of failure identificados
- [ ] Requirements de 12-18 meses compilados
- [ ] Scaling analysis para 2x/5x/10x executada
- [ ] Gaps classificados por severity
- [ ] ADRs criados para cada decisão significativa
- [ ] Trade-offs documentados para cada alternativa
- [ ] Architecture roadmap com timeline e investment
- [ ] Security assessment incluído
- [ ] Compliance requirements validados

## Template de Entrega
```markdown
# Architecture Review — [Date]

## Current Architecture
[C4 Context Diagram]

### Tech Stack
| Layer | Technology | Version | Status |
|-------|-----------|---------|--------|
| Frontend | | | |
| Backend | | | |
| Database | | | |
| Cache | | | |
| Queue | | | |
| Infrastructure | | | |

### Health Metrics
| Service | Availability | p50 Latency | p99 Latency | Error Rate |
|---------|-------------|-------------|-------------|------------|

## Gap Analysis
| Gap | Severity | Current | Needed | Proposed Solution |
|-----|----------|---------|--------|-------------------|

## Architecture Decision Records
### ADR-[XXX]: [Title]
- **Status:** [Proposed/Accepted/Deprecated]
- **Context:** [Situation and constraints]
- **Decision:** [What we decided]
- **Consequences:** [Trade-offs accepted]
- **Alternatives:** [What else we considered]
- **Type:** [1-Irreversible / 2-Reversible]

## Evolution Roadmap
| Quarter | Change | Effort | Investment | Business Impact |
|---------|--------|--------|------------|-----------------|

## Investment Required
- **Total:** [R$ X over Y quarters]
- **Headcount:** [X engineers for Y months]
- **Infrastructure:** [Monthly cost change]
```

## Registries para Atualizar
- `registries/decisions-log.md` — ADRs registrados
- `registries/risk-register.md` — Architectural risks
- `registries/tech-debt.md` — Architecture-related tech debt
- `registries/resource-allocation.md` — Engineering investment needed

## Critérios de Aceitação
1. Arquitetura atual documentada com C4 diagrams
2. Gaps identificados e classificados por severity
3. ADRs criados para todas as decisões significativas
4. Architecture roadmap com timeline e investment estimado
5. Executive team briefed e aligned
6. Engineering team communicated
7. Success metrics definidos

## Dependências e Handoffs
- **Recebe de:** Product Roadmap (CPO), Business Requirements, Incident Data
- **Entrega para:** Engineering Teams, Platform Roadmap, Tech Debt Review, Budget Planning
- **Cadência:** Semestral (deep review) + Ad-hoc (para mudanças significativas)
- **Escalation path:** Gaps blockers sem solução escalam para CEO para prioritization
- **Integração:** Alimenta Platform Roadmap e Tech Debt Review
