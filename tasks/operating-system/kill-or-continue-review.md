# Kill or Continue Review

## Objetivo
Executar uma avaliação rigorosa para decidir se uma iniciativa em risco deve ser continuada (com ajustes) ou encerrada (kill). Esta é a contraparte operacional do pivot-or-persevere estratégico, focada em iniciativas específicas que estão consumindo recursos sem entregar resultados esperados.

## Agente Responsável
- **COO Agent** — Facilitação do review e enforcement da decisão

## Agentes de Suporte
- **CEO Agent** — Decisão final em casos de alto impacto estratégico
- **CFO Agent** — Análise financeira: sunk cost, continuation cost, opportunity cost
- **CTO Agent** — Avaliação técnica e engineering capacity freed
- **CPO Agent** — Product impact e customer implications
- **CHRO Agent** — People implications (reallocation, morale)

## Pré-requisitos
1. Iniciativa flagged como Red no Initiative Health Review por 2+ ciclos
2. OU kill criteria definidos no launch da iniciativa foram atingidos
3. OU request explícito de C-Level para review
4. Dados de performance da iniciativa compilados
5. Original business case e métricas de sucesso
6. Resource allocation atual (quem e quanto está alocado)
7. Dependency map (quem depende desta iniciativa)

## Processo (step-by-step)

### Fase 1: Evidence Assembly (2-3 dias)
1. Compilar performance completa da iniciativa desde o launch
2. Comparar actual vs. original projections para cada métrica chave
3. Calcular total investment: budget consumido + opportunity cost de headcount
4. Documentar o trajectory: métricas melhorando, estáveis ou piorando?
5. Entrevistar initiative owner para perspectiva interna (sem sugar-coating)
6. Mapear dependências: quem será impactado se a iniciativa for killed
7. Estimar recursos liberados se killed (budget, headcount, management attention)

### Fase 2: Structured Assessment (1-2 dias)
8. Aplicar o "Four Tests":
   - **Market Test:** O mercado ainda quer o que estamos construindo?
   - **Execution Test:** O problema é de execução (fixável) ou de thesis (fundamental)?
   - **Economics Test:** Os unit economics podem funcionar mesmo se tudo der certo?
   - **Opportunity Test:** Esses recursos gerariam mais valor em outro lugar?
9. Calcular o continuation cost: quanto mais precisamos investir para ter chance de sucesso
10. Calcular o kill cost: custo de encerrar (wind-down, customer migration, team impact)
11. Modelar 3 cenários se continuar: optimistic, base, pessimistic
12. Documentar o "best alternative use" dos recursos se liberados

### Fase 3: Decision Session (60 minutos)
13. Apresentar o evidence package para o decision-making group
14. Cada participante vota independentemente antes da discussão: kill, continue, or modify
15. Facilitar discussão estruturada: argumentos para continuar vs argumentos para kill
16. Aplicar o "clean slate test": se começássemos do zero, faríamos isso?
17. Aplicar o "sunk cost check": estamos continuando pelas razões certas?
18. Tomar decisão: kill, continue (with changes), ou extend (more time to prove)
19. Se extend: definir hard deadline e metrics que devem ser atingidas

### Fase 4: Execution da Decisão (1-2 semanas)
20. Se KILL: executar wind-down plan
    - Comunicar decisão para o time com respeito e transparência
    - Definir plano de realocação para cada membro do time
    - Comunicar para clientes afetados (se aplicável)
    - Documentar learnings em formato de post-mortem
    - Liberar budget e realocar conforme planejado
21. Se CONTINUE (with changes): documentar mudanças e novo timeline
    - Definir novas métricas e targets revisados
    - Ajustar resource allocation se necessário
    - Definir próximo review checkpoint
22. Se EXTEND: definir prova de vida
    - Timeline máximo para próximo checkpoint (geralmente 30-60 dias)
    - Métricas específicas que devem melhorar
    - Consequência automática se métricas não melhorarem (auto-kill)

## Frameworks a Aplicar
- **Four Tests Framework** — Market, Execution, Economics, Opportunity
- **Clean Slate Test** — Remover sunk cost bias da decisão
- **Sunk Cost Fallacy Check** — Verificar se continuação é racional
- **Opportunity Cost Analysis** — Comparar com melhor uso alternativo dos recursos
- **Graceful Wind-down Protocol** — Encerrar com dignidade e respeito pelo time
- **Post-Mortem (Blameless)** — Aprender sem culpar

## Checklists de Qualidade
- [ ] Performance data compilada com comparação vs projections
- [ ] Total investment calculado (budget + opportunity cost)
- [ ] Four Tests aplicados com scores e evidência
- [ ] Continuation cost e kill cost calculados
- [ ] Clean slate test e sunk cost check executados
- [ ] Votos independentes coletados antes da discussão
- [ ] Decisão documentada com rationale claro
- [ ] Wind-down plan ou recovery plan definido
- [ ] Comunicação preparada para team e stakeholders
- [ ] Learnings documentados (post-mortem)
- [ ] Resource reallocation plan definido
- [ ] Dependencies impact assessed e mitigated

## Template de Entrega
```markdown
# Kill or Continue Review — [Initiative Name]

## Initiative Summary
- **Launch Date:** [When]
- **Original Thesis:** [Why we started]
- **Owner:** [Who]
- **Team Size:** [X people]
- **Total Investment:** [R$ spent + opportunity cost]

## Performance vs Projections
| Metric | Projected | Actual | Gap |
|--------|-----------|--------|-----|
| [Key metric 1] | | | |

## Four Tests
| Test | Score (1-5) | Evidence |
|------|-------------|----------|
| Market | | |
| Execution | | |
| Economics | | |
| Opportunity | | |

## Cost Analysis
- **Continuation Cost (next quarter):** [R$]
- **Kill Cost (wind-down):** [R$]
- **Resources Freed if Killed:** [Budget + X people]
- **Best Alternative Use:** [What else we'd do with resources]

## Voting Results
| Voter | Vote | Key Argument |
|-------|------|-------------|

## Decision
- **Decision:** [Kill / Continue with Changes / Extend]
- **Rationale:** [Why]
- **Dissent:** [Who disagreed and why]

## Execution Plan
### If Kill:
- Wind-down timeline: [X weeks]
- Team reallocation: [Plan]
- Customer communication: [Plan]
- Learnings: [Key takeaways]

### If Continue:
- Changes: [What's different]
- New targets: [Metrics]
- Next review: [Date]

### If Extend:
- Proof of life deadline: [Date]
- Must-hit metrics: [List]
- Auto-kill trigger: [Condition]
```

## Registries para Atualizar
- `registries/initiatives.md` — Atualizar status (active/killed/modified)
- `registries/decisions-log.md` — Registrar decisão com rationale
- `registries/resource-allocation.md` — Refletir realocação de recursos
- `registries/lessons-learned.md` — Post-mortem learnings

## Critérios de Aceitação
1. Análise completa com dados de performance e financial impact
2. Four Tests aplicados com scores documentados
3. Decisão tomada em sessão com votos independentes
4. Plano de execução definido (wind-down ou recovery)
5. Comunicação realizada para team e stakeholders
6. Recursos realocados conforme plano
7. Post-mortem documentado com learnings

## Dependências e Handoffs
- **Recebe de:** Initiative Health Review (Red flags), Strategic Bets Review, WBR Escalations
- **Entrega para:** Resource Allocation, Team Reallocation (CHRO), Quarterly Planning
- **Cadência:** Triggered (quando critérios de review são atingidos)
- **SLA:** Decisão em no máximo 10 dias úteis após trigger
- **Escalation path:** Se decisão não converge, CEO decide em 24h
