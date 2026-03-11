# Evaluate Models and Set Guardrails

## Objetivo
Avaliar modelos de AI para use cases selecionados e estabelecer guardrails de segurança, ética e qualidade. A escolha do modelo correto determina custo, performance e risco. Guardrails mal definidos podem resultar em outputs prejudiciais, violações de privacidade ou decisões enviesadas.

## Agente Responsável
- **CAI Agent** — Ownership da avaliação de modelos e definição de guardrails

## Agentes de Suporte
- **CTO Agent** — Technical infrastructure e engineering constraints
- **CIO Agent** — Data security e compliance alignment
- **CPO Agent** — Product quality standards e UX requirements
- **CFO Agent** — Cost analysis de diferentes modelos
- **CEO Agent** — Risk appetite e brand protection

## Pré-requisitos
1. AI use cases selecionados (ver `tasks/ai/select-ai-use-cases.md`)
2. Requirements por use case: accuracy, latency, throughput, cost targets
3. Evaluation dataset preparado para cada use case
4. Baseline performance metrics (current process)
5. Regulatory requirements (LGPD, AI Act, industry-specific)
6. Ethical guidelines da organização
7. Budget para model evaluation e testing

## Processo (step-by-step)

### Fase 1: Model Selection (3-5 dias)
1. Para cada use case, definir requirements: task type, accuracy needs, latency SLA, cost budget
2. Identify candidate models: commercial APIs (OpenAI, Anthropic, Google), open source (Llama, Mistral), specialized
3. Create evaluation criteria matrix: accuracy, latency, cost, scalability, privacy, customizability
4. Run benchmark evaluations usando evaluation dataset padronizado
5. Compare cost per query/token/transaction para cada modelo
6. Evaluate vendor lock-in risk para commercial APIs
7. Assess fine-tuning needs e feasibility por modelo
8. Document trade-offs: accuracy vs. cost, latency vs. quality, privacy vs. capability

### Fase 2: Guardrails Design (2-3 dias)
9. Define input guardrails: content filtering, prompt injection protection, PII detection
10. Define output guardrails: toxicity detection, hallucination checks, factual accuracy
11. Define behavioral guardrails: what the model should and should NOT do
12. Design human-in-the-loop checkpoints para decisões de alto risco
13. Define monitoring guardrails: performance degradation alerts, drift detection
14. Establish data guardrails: what data can be sent to external APIs, anonymization requirements
15. Define rate limiting e cost guardrails: maximum spend per day/month
16. Create escalation procedures: what happens when guardrails are triggered

### Fase 3: Testing e Validation (2-3 dias)
17. Execute red team testing: try to break the model, find edge cases
18. Run bias testing: evaluate outputs across different demographics e scenarios
19. Test guardrails effectiveness: verify they catch what they should catch
20. Measure false positive rate of guardrails (blocking legitimate use)
21. Load test: verify performance under expected production load
22. Test failure modes: what happens when model API is down
23. Validate cost projections at scale

### Fase 4: Documentation e Approval (1-2 dias)
24. Document model selection rationale (ADR format)
25. Publish guardrails specification accessible to all teams
26. Create monitoring dashboard with guardrail metrics
27. Define guardrail review cadence (monthly)
28. Get approval from CEO/CTO on risk profile
29. Communicate guardrails to all teams building with AI

## Frameworks a Aplicar
- **Model Evaluation Framework** — Accuracy, latency, cost, privacy, scalability scoring
- **AI Ethics Framework** — Fairness, accountability, transparency, safety
- **NIST AI Risk Management Framework** — Risk identification e mitigation
- **Red Team Methodology** — Adversarial testing para AI systems
- **Guardrail Taxonomy** — Input, output, behavioral, monitoring, data, cost guardrails
- **Responsible AI Principles** — Human oversight, technical robustness, fairness

## Checklists de Qualidade
- [ ] Candidate models benchmarked on evaluation dataset
- [ ] Cost per unit calculated for each model
- [ ] Vendor lock-in risk assessed
- [ ] Input guardrails defined and tested
- [ ] Output guardrails defined and tested
- [ ] Behavioral boundaries documented
- [ ] Human-in-the-loop checkpoints designed
- [ ] Red team testing executed
- [ ] Bias testing completed
- [ ] Data privacy guardrails defined
- [ ] Cost guardrails (max spend) set
- [ ] Monitoring dashboard configured
- [ ] Documentation published
- [ ] Executive approval obtained

## Template de Entrega
```markdown
# AI Model Evaluation & Guardrails — [Use Case]

## Model Evaluation
| Criteria | Weight | Model A | Model B | Model C |
|----------|--------|---------|---------|---------|
| Accuracy | [X%] | | | |
| Latency (p95) | [X%] | | | |
| Cost per 1K queries | [X%] | | | |
| Privacy | [X%] | | | |
| Customizability | [X%] | | | |
| Scalability | [X%] | | | |
| **Weighted Score** | 100% | | | |

### Selected Model: [Name]
- **Rationale:** [Why this model]
- **Trade-offs Accepted:** [What we're giving up]
- **Lock-in Risk:** [Assessment]
- **Cost Projection (monthly):** [R$ at expected volume]

## Guardrails Specification

### Input Guardrails
| Guardrail | Description | Action When Triggered |
|-----------|-------------|---------------------|
| PII Detection | Strip/mask PII before sending to model | Block and sanitize |
| Prompt Injection | Detect manipulation attempts | Block and log |
| Content Filter | Block prohibited content categories | Block and alert |

### Output Guardrails
| Guardrail | Description | Action When Triggered |
|-----------|-------------|---------------------|
| Toxicity Check | Detect harmful content | Block and escalate |
| Hallucination Check | Verify factual claims | Flag for review |
| Format Validation | Ensure output matches schema | Retry or fallback |

### Behavioral Guardrails
- **Must Do:** [List of required behaviors]
- **Must Not Do:** [List of prohibited behaviors]
- **Escalate When:** [Conditions for human review]

### Data Guardrails
- **Can Send to External API:** [Data types allowed]
- **Must Anonymize:** [Data types requiring anonymization]
- **Never Send:** [Prohibited data types]

### Cost Guardrails
- **Daily Max Spend:** [R$ X]
- **Monthly Max Spend:** [R$ X]
- **Alert Threshold:** [X% of budget]

## Testing Results
| Test | Result | Issues Found | Resolution |
|------|--------|-------------|------------|
| Red Team | | | |
| Bias Testing | | | |
| Load Testing | | | |
| Guardrail Effectiveness | | | |

## Monitoring
| Metric | Target | Alert Threshold |
|--------|--------|----------------|
| Accuracy | | |
| Latency p95 | | |
| Guardrail Trigger Rate | | |
| Cost per Day | | |
| Error Rate | | |
```

## Registries para Atualizar
- `registries/decisions-log.md` — Model selection ADR
- `registries/risk-register.md` — AI-specific risks and guardrails
- `registries/vendor-registry.md` — AI vendor details
- `registries/compliance-tracker.md` — AI compliance status

## Critérios de Aceitação
1. Models benchmarked with evaluation dataset
2. Selected model documented with rationale
3. All guardrail categories defined (input, output, behavioral, data, cost)
4. Red team testing completed
5. Bias testing completed with results documented
6. Monitoring dashboard live
7. Executive approval on risk profile

## Dependências e Handoffs
- **Recebe de:** AI Use Case Selection, Data Governance Review, Technical Requirements
- **Entrega para:** AI Deployment, Engineering Teams, Product Teams
- **Cadência:** Per use case (initial) + Monthly guardrail review + Quarterly model re-evaluation
- **Escalation path:** Guardrail breaches escalam imediatamente para CAI + CTO
- **Integração:** Feeds AI Deployment and AI Risk Assessment
