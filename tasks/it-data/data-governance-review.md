# Data Governance Review

## Objetivo
Revisar as práticas de governança de dados da organização, garantindo que dados são confiáveis, acessíveis, seguros e compliant. Dados são o ativo mais valioso — mas sem governance, viram um passivo: decisões erradas, multas regulatórias e perda de confiança do cliente.

## Agente Responsável
- **CIO Agent** — Ownership de data governance e data quality

## Agentes de Suporte
- **CTO Agent** — Data architecture e infrastructure
- **CFO Agent** — Financial data accuracy e regulatory compliance
- **CAI Agent** — Data readiness para AI/ML use cases
- **CEO Agent** — Data strategy alignment
- **COO Agent** — Operational data quality requirements

## Pré-requisitos
1. Data catalog existente (ou inventário de data sources)
2. Current data governance policies e procedures
3. Data quality metrics (se existentes)
4. Regulatory requirements (LGPD, GDPR, SOC2, etc.)
5. Data access control documentation
6. Incident history relacionada a dados (breaches, quality issues)
7. Data architecture documentation

## Processo (step-by-step)

### Fase 1: Data Landscape Assessment (3-5 dias)
1. Catalogar todas as fontes de dados: databases, APIs, files, SaaS systems, spreadsheets
2. Classificar dados por tipo: customer data, financial data, operational data, analytics data
3. Mapear data flows: como dados se movem entre sistemas (ETL/ELT pipelines)
4. Identificar data owners para cada dataset (quem é accountable)
5. Avaliar data quality current state: completeness, accuracy, timeliness, consistency
6. Mapear sensitive data locations: PII, financial data, health data
7. Documentar current data access controls: who can access what

### Fase 2: Compliance Assessment (2-3 dias)
8. Mapear regulatory requirements aplicáveis: LGPD, GDPR, SOC2, HIPAA, etc.
9. Avaliar current compliance state para cada regulation
10. Identificar gaps de compliance com risk scoring
11. Revisar data retention policies: estão aderentes às regulações?
12. Avaliar data processing agreements com vendors (DPAs)
13. Verificar consent management: como consentimento é coletado e rastreado
14. Revisar incident response plan para data breaches

### Fase 3: Quality e Accessibility Review (2-3 dias)
15. Medir data quality metrics por dataset: accuracy, completeness, freshness, consistency
16. Identificar "data swamps": datasets abandonados ou sem ownership
17. Avaliar self-serve data access: analistas e teams conseguem acessar dados sem bottleneck?
18. Revisar data documentation: metadata, data dictionaries, lineage documentation
19. Avaliar data pipeline health: freshness SLAs, failure rates, monitoring
20. Identificar single sources of truth vs. conflicting data sources
21. Avaliar data literacy: teams entendem e usam dados adequadamente?

### Fase 4: Recommendations e Roadmap (1-2 dias)
22. Propor governance framework improvements
23. Definir data ownership model se não existir
24. Propor data quality improvement initiatives
25. Recomendar compliance gap remediation com timeline
26. Definir data governance KPIs para tracking contínuo
27. Criar data governance roadmap por quarter

## Frameworks a Aplicar
- **DAMA-DMBOK** — Data Management Body of Knowledge framework
- **Data Quality Dimensions** — Accuracy, completeness, consistency, timeliness, validity, uniqueness
- **RACI for Data** — Responsible, Accountable, Consulted, Informed para data ownership
- **Data Maturity Model** — Reactive → Managed → Proactive → Optimized
- **LGPD/GDPR Compliance Framework** — Data protection assessment
- **Data Mesh Principles** — Domain ownership, data as product, self-serve platform

## Checklists de Qualidade
- [ ] Data catalog completo com todas as sources
- [ ] Data owners atribuídos para cada dataset
- [ ] Data quality measured por dataset
- [ ] Compliance gaps identificados e scored
- [ ] Data access controls reviewed
- [ ] Sensitive data locations mapped
- [ ] Data retention policies reviewed
- [ ] Data pipeline health assessed
- [ ] Self-serve access capability evaluated
- [ ] Governance KPIs defined
- [ ] Remediation roadmap created

## Template de Entrega
```markdown
# Data Governance Review — [Date]

## Data Landscape
- **Total Data Sources:** [X]
- **Total Datasets:** [X]
- **Data Volume:** [X TB]
- **Sensitive Data Sources:** [X]

| Source | Type | Owner | Quality Score | Compliance | Status |
|--------|------|-------|--------------|-----------|--------|

## Data Quality Scorecard
| Dataset | Accuracy | Completeness | Freshness | Consistency | Overall |
|---------|----------|-------------|-----------|------------|---------|

## Compliance Status
| Regulation | Requirement | Current State | Gap | Risk | Remediation |
|-----------|------------|--------------|-----|------|-------------|

## Data Access Review
| Data Type | Who Has Access | Appropriate? | Action Needed |
|-----------|---------------|-------------|---------------|

## Issues Found
| Issue | Severity | Impact | Remediation | Owner | Timeline |
|-------|----------|--------|------------|-------|----------|

## Data Governance Maturity
- **Current Level:** [Reactive / Managed / Proactive / Optimized]
- **Target Level:** [X]
- **Key Gaps:** [List]

## KPIs
| Metric | Current | Target | Measurement Frequency |
|--------|---------|--------|---------------------|

## Roadmap
| Quarter | Focus | Initiatives | Investment |
|---------|-------|------------|------------|
```

## Registries para Atualizar
- `registries/risk-register.md` — Data risks e compliance gaps
- `registries/decisions-log.md` — Data governance decisions
- `registries/systems-inventory.md` — Data sources updated
- `registries/compliance-tracker.md` — Compliance status updated

## Critérios de Aceitação
1. Data catalog complete with ownership assigned
2. Data quality scored for all critical datasets
3. Compliance gaps identified with severity e remediation plan
4. Data access controls reviewed and documented
5. Governance KPIs defined and baselined
6. Roadmap created with quarterly milestones
7. Executive team briefed on findings and risks

## Dependências e Handoffs
- **Recebe de:** Systems Audit, Security Assessment, Compliance Requirements
- **Entrega para:** AI Use Cases (data readiness), Compliance Remediation, Data Platform
- **Cadência:** Semestral (full review) + Contínuo (KPI monitoring)
- **Escalation path:** Compliance gaps with regulatory risk escalam para CEO e Legal
- **Integração:** Alimenta AI readiness e Systems Audit
