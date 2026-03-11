# Reliability Review (SLOs, Incidents)

## Objetivo
Avaliar a confiabilidade dos sistemas em produção, revisar SLOs e seu cumprimento, analisar incidentes do período e garantir que a organização está investindo adequadamente em reliability. Um sistema não confiável é um sistema que destrói confiança do cliente e gera churn silencioso.

## Agente Responsável
- **CTO Agent** — Ownership de reliability e engineering standards

## Agentes de Suporte
- **CIO Agent** — Infrastructure reliability e monitoring
- **COO Agent** — Business impact de outages e customer SLAs
- **CPO Agent** — Product impact e feature reliability
- **CFO Agent** — Cost of downtime e reliability investment ROI

## Pré-requisitos
1. SLOs definidos para cada serviço crítico
2. Error budget tracking data
3. Incident log dos últimos 90 dias com post-mortems
4. Monitoring e alerting coverage data
5. On-call rotation data (response times, escalations)
6. Customer-reported issues data
7. Infrastructure cost data

## Processo (step-by-step)

### Fase 1: SLO Review (2-3 dias)
1. Compilar SLO compliance para cada serviço: availability, latency, throughput
2. Calcular error budget remaining para cada SLO
3. Identificar serviços que queimaram >50% do error budget no período
4. Avaliar se os SLOs atuais refletem as expectativas reais dos clientes
5. Propor ajustes de SLO onde necessário (mais strict ou mais lenient)
6. Validar que SLOs estão sendo medidos corretamente (instrumentation audit)

### Fase 2: Incident Analysis (2-3 dias)
7. Compilar todos os incidentes do período: severity, duration, blast radius, root cause
8. Classificar incidentes por: severity (P0-P3), type (infra, code, config, dependency)
9. Calcular MTTR (Mean Time to Recovery) e MTTD (Mean Time to Detect) por severity
10. Identificar patterns: mesma root cause aparece múltiplas vezes?
11. Avaliar eficácia de post-mortem action items: quantos foram implementados?
12. Calcular custo estimado de downtime (revenue lost, customer impact, team cost)
13. Analisar on-call health: response times, escalation rates, toil burden

### Fase 3: Reliability Investment Assessment (1-2 dias)
14. Mapear reliability investments do período: o que fizemos para melhorar
15. Avaliar eficácia: investimentos reduziram incidentes e melhoraram SLOs?
16. Identificar reliability gaps: áreas que precisam de mais investimento
17. Calcular o "reliability debt": trabalho de reliability acumulado e não feito
18. Propor reliability roadmap para próximo período
19. Estimar investment needed (headcount, tools, infrastructure)

### Fase 4: Review Meeting (60-90 minutos)
20. Apresentar SLO compliance dashboard com trends
21. Review de incidentes significativos e patterns
22. Discutir error budget policy: o que acontece quando error budget é excedido
23. Aprovar reliability investments para próximo período
24. Definir reliability targets e improvement goals
25. Avaliar se current team structure suporta reliability needs

## Frameworks a Aplicar
- **SLO/SLI/SLA Framework (Google SRE)** — Structured reliability targets
- **Error Budget Policy** — Ações automáticas quando error budget é consumido
- **DORA Metrics** — Deploy frequency, lead time, change failure rate, MTTR
- **Blameless Post-Mortem** — Focar em sistema, não em pessoas
- **Reliability Pyramid** — Monitoring → Incident Response → Post-Mortem → Testing → Design
- **Chaos Engineering** — Proactive reliability testing

## Checklists de Qualidade
- [ ] SLOs compilados para todos os serviços críticos
- [ ] Error budget calculated e tracked
- [ ] Incidentes do período catalogados com severity e root cause
- [ ] MTTR e MTTD calculados e trended
- [ ] Incident patterns identificados
- [ ] Post-mortem action items tracked (completion rate)
- [ ] Downtime cost estimado
- [ ] On-call health assessed
- [ ] Reliability investment ROI calculado
- [ ] Reliability roadmap proposto
- [ ] Error budget policy defined e enforced

## Template de Entrega
```markdown
# Reliability Review — [Period]

## SLO Compliance
| Service | SLO Target | Actual | Error Budget Remaining | Status |
|---------|-----------|--------|----------------------|--------|
| [Service A] | 99.9% | | | |
| [Service B] | p99 <200ms | | | |

## Incident Summary
- **Total Incidents:** [X]
- **P0:** [X] | **P1:** [X] | **P2:** [X] | **P3:** [X]
- **Total Downtime:** [X hours]
- **Estimated Cost:** [R$ X]

### Incident Trends
| Metric | Previous Period | Current | Trend |
|--------|----------------|---------|-------|
| Total Incidents | | | |
| MTTD | | | |
| MTTR | | | |
| Post-Mortem Completion | | | |

### Top Incident Patterns
| Pattern | Occurrences | Impact | Fix Status |
|---------|-------------|--------|------------|

## DORA Metrics
| Metric | Value | Target | Industry Benchmark |
|--------|-------|--------|-------------------|
| Deploy Frequency | | | |
| Lead Time for Changes | | | |
| Change Failure Rate | | | |
| MTTR | | | |

## On-Call Health
| Metric | Value | Target |
|--------|-------|--------|
| Avg Response Time | | |
| Pages per Week | | |
| Escalation Rate | | |
| Toil % | | |

## Reliability Investments
| Investment | Status | Impact |
|-----------|--------|--------|

## Reliability Roadmap (Next Period)
| Initiative | Effort | Expected Impact | Owner |
|-----------|--------|-----------------|-------|

## Error Budget Policy Actions
| Condition | Action |
|-----------|--------|
| Budget >50% consumed | Feature freeze on affected service |
| Budget >80% consumed | Dedicated reliability sprint |
| Budget exhausted | Full feature freeze until restored |
```

## Registries para Atualizar
- `registries/metrics-log.md` — SLO compliance e DORA metrics
- `registries/incidents-log.md` — Incidents catalogados
- `registries/tech-debt.md` — Reliability debt items
- `registries/risk-register.md` — Reliability risks

## Critérios de Aceitação
1. SLO compliance reportado para todos os serviços críticos
2. Incidentes analisados com patterns identificados
3. DORA metrics calculados e benchmarked
4. Reliability roadmap com investment estimate
5. Error budget policy defined e communicated
6. On-call health assessed e improvements planned
7. Post-mortem action item completion rate >80%

## Dependências e Handoffs
- **Recebe de:** Monitoring Systems, Incident Management, Post-Mortems, Infrastructure Data
- **Entrega para:** Architecture Review, Platform Roadmap, Budget Planning, Engineering Health
- **Cadência:** Mensal (light) + Trimestral (deep)
- **Escalation path:** SLO breach >24h escala para CEO; repeat incidents escala para CTO
- **Integração:** Alimenta Engineering Health Check e Tech Debt Review
