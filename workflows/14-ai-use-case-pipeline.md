# Workflow 14 — AI Use Case Pipeline

> **Pipeline completo para identificar, avaliar, priorizar, implementar e escalar casos de uso de IA na organização.**
> Da ideação ao deploy em produção, com gates de qualidade em cada transição.

---

## Objetivo

Estabelecer um pipeline estruturado e repetível para levar casos de uso de IA desde a identificação inicial até a operação em produção com monitoramento contínuo. O pipeline garante que:

1. **Casos de uso são avaliados objetivamente** — não por hype, mas por impacto e viabilidade
2. **POCs têm critérios claros de sucesso** — antes de começar, não depois
3. **A transição POC → Produção tem gates rigorosos** — modelo, dados, infra, ética
4. **Modelos em produção são monitorados** — drift, bias, performance, custo
5. **Aprendizados alimentam o próximo ciclo** — RalphLoop integrado

> **Princípio:** IA sem pipeline é experimentação sem aprendizado. O pipeline transforma experimentos em capacidades organizacionais.

---

## Agentes Envolvidos

| Agente | Papel no Workflow |
|--------|-------------------|
| **CAIO Architect** | Lead — owner do pipeline, define critérios de avaliação, aprova transições |
| **CTO Architect** | Support — infraestrutura de ML, integração com plataforma, reliability |
| **CIO Engineer** | Support — data availability, data quality, compliance (LGPD) |
| **Vision Chief (CEO)** | Reviewer — alinhamento estratégico, priorização de investimento |
| **CFO Strategist** | Support — ROI analysis, budget allocation para AI initiatives |
| **COO Orchestrator** | Support — integração com processos operacionais, change management |
| **Squad Coordinator** | Logística — tracking de pipeline, consolidação de status, meeting prep |

---

## Trigger (quando iniciar)

### Triggers Primários
- Novo caso de uso de IA identificado por qualquer agente ou squad
- Revisão trimestral do portfolio de IA (cadência QBR)
- Oportunidade de mercado que requer capability de IA
- Problema operacional onde IA pode ser solução
- Request do board/investidores para AI strategy update

### Triggers Secundários
- Novo modelo/API disponível no mercado (ex: novo LLM release)
- Competidor lançou feature AI-powered
- Mudança regulatória que afeta uso de IA
- Incidente com modelo em produção que requer reavaliação

---

## Pré-condições

- [ ] AI Strategy definida (`frameworks/ai/ai-strategy.md`)
- [ ] AI Governance framework ativo (`frameworks/ai/ai-governance.md`)
- [ ] Data governance mínimo em operação (`frameworks/it-information/data-governance-lite.md`)
- [ ] Infra de ML básica disponível (compute, storage, experiment tracking)
- [ ] AI Portfolio Registry inicializado (`data/registries/ai-portfolio-registry.yaml`)
- [ ] Budget para AI experiments aprovado

---

## Processo (step-by-step)

### Stage 1: Identificação e Registro (1-2 dias)

**Owner**: Qualquer agente pode submeter. CAIO faz triagem.

1. **Submeter Caso de Uso**
   - Preencher template: `templates/ai/ai-use-case-proposal.md`
   - Campos obrigatórios: problema, hipótese, dados necessários, impacto esperado, riscos
   - Classificar tipo: generative AI, predictive, optimization, automation, analytics

2. **Triagem Inicial pelo CAIO**
   - Verificar duplicidade com portfolio existente
   - Classificar prioridade inicial: high / medium / low / reject
   - Verificar alinhamento com AI Strategy
   - Atribuir ID único no portfolio

3. **Registro no Portfolio**
   - Atualizar `data/registries/ai-portfolio-registry.yaml`
   - Status: `identified`
   - Notificar agentes relevantes

### Stage 2: Avaliação de Viabilidade (3-5 dias)

**Owner**: CAIO Architect com CIO Engineer e CTO Architect

1. **Assessment de Dados**
   - CIO avalia: dados disponíveis? qualidade? volume? freshness?
   - Identifica gaps de dados e custo de preenchê-los
   - Verifica compliance (LGPD, consentimento, anonimização)

2. **Assessment Técnico**
   - CTO avalia: infra necessária? integração com stack? latência aceitável?
   - Identifica dependências técnicas
   - Estima custo de infra (compute, storage, APIs)

3. **Assessment de Impacto**
   - CAIO quantifica: impacto em métricas, economia de tempo, receita potencial
   - CFO valida ROI projetado
   - Vision Chief confirma alinhamento estratégico

4. **Scoring Consolidado**
   - Matriz: Impacto × Viabilidade × Alinhamento Estratégico × Risco
   - Score final: 1-10
   - Decisão: proceed to POC / backlog / reject

5. **Atualizar Portfolio**
   - Status: `evaluated` com score
   - Registrar decisão no `data/registries/decision-registry.yaml`

### Stage 3: POC Design (3-5 dias)

**Owner**: CAIO Architect

1. **Definir Escopo do POC**
   - Hipótese clara e testável
   - Métricas de sucesso quantificadas (accuracy, latency, cost, user satisfaction)
   - Critérios de go/no-go explícitos
   - Timeline: máximo 4 semanas para POC

2. **Definir Arquitetura do POC**
   - Stack técnico (modelo, framework, infra)
   - Dados de treino/teste/validação
   - Guardrails iniciais (content filtering, rate limiting, fallbacks)
   - Estratégia de avaliação (eval suite)

3. **Alocar Recursos**
   - Equipe: quem executa o POC?
   - Budget: compute costs, API costs, data costs
   - Timeline com milestones semanais

4. **Approval Gate**
   - CAIO + Vision Chief aprovam POC design
   - CFO valida budget allocation
   - CTO confirma viabilidade técnica

### Stage 4: POC Execution (2-4 semanas)

**Owner**: CAIO Architect + equipe técnica

1. **Sprint 1: Baseline**
   - Implementar pipeline de dados
   - Treinar/configurar modelo baseline
   - Implementar métricas de avaliação
   - Checkpoint semanal: on track?

2. **Sprint 2: Iteration**
   - Otimizar modelo (fine-tuning, prompt engineering, RAG)
   - Testar edge cases
   - Implementar guardrails
   - Checkpoint semanal: métricas melhorando?

3. **Sprint 3: Evaluation**
   - Rodar eval suite completa
   - Red-teaming (adversarial testing)
   - User testing (se aplicável)
   - Documentar resultados

4. **Checkpoints Semanais**
   - CAIO revisa progresso
   - Go/pivot/stop decision a cada semana
   - Se 2 semanas sem progresso → stop

### Stage 5: Evaluation (3-5 dias)

**Owner**: CAIO Architect

1. **Compilar Resultados**
   - Preencher `templates/caio/model-evaluation-report.md`
   - Comparar métricas vs critérios de sucesso definidos no Stage 3
   - Documentar limitações descobertas

2. **Eval de Segurança e Ética**
   - Aplicar `checklists/caio/model-eval-and-guardrails.md`
   - Aplicar `checklists/caio/caio-ai-risk-assessment.md`
   - Verificar bias, fairness, toxicidade, data leakage
   - Cross-squad: Cyber squad review (se dados sensíveis)

3. **Análise de Custo-Benefício**
   - CFO valida unit economics do modelo em produção
   - Custo por inference, custo total mensal projetado
   - Comparar com alternativas (regra simples, vendor, etc.)

4. **Recommendation**
   - Go to production / iterate more / pivot / kill
   - Se "go": definir requirements de produção
   - Se "kill": documentar aprendizados no RalphLoop

### Stage 6: Production Decision (1-2 dias)

**Owner**: Vision Chief + CAIO Architect

1. **Decision Review**
   - CAIO apresenta resultados e recomendação
   - Vision Chief avalia alinhamento estratégico
   - CTO confirma readiness de infra
   - CFO aprova investment case

2. **Go/No-Go Gate**
   - Todos os checklists passam? ✅
   - Budget aprovado para operação contínua? ✅
   - SLA de produção definido? ✅
   - Rollback plan definido? ✅
   - Monitoring configurado? ✅

3. **Registrar Decisão**
   - `data/registries/decision-registry.yaml`
   - Tipo: Type 1 (se infra commitment significativo) ou Type 2
   - Status no portfolio: `approved-for-production`

### Stage 7: Rollout (1-4 semanas)

**Owner**: CTO Architect + CAIO Architect

1. **Production Setup**
   - Deploy infra de produção (seguindo `frameworks/engineering-tech/platform-engineering.md`)
   - Implementar monitoring (latência, erros, custos, drift)
   - Configurar alertas e on-call
   - Implementar guardrails de produção

2. **Gradual Rollout**
   - Canary deployment: 5% → 25% → 50% → 100%
   - Monitorar métricas a cada expansão
   - Gate de cada expansão: métricas dentro do SLA? ✅
   - Rollback automático se threshold ultrapassado

3. **Integration**
   - Integrar com sistemas existentes (APIs, UIs, workflows)
   - Documentar endpoints e contratos
   - Atualizar architecture diagrams

4. **Handoff para Operações**
   - Cross-squad: Data squad (monitoring contínuo)
   - Runbook para operações
   - On-call rotation definida
   - Status no portfolio: `in-production`

### Stage 8: Monitoring e Continuous Improvement (contínuo)

**Owner**: CAIO Architect + CIO Engineer

1. **Monitoring Contínuo**
   - Model performance (accuracy, latency, throughput)
   - Data drift detection
   - Cost tracking
   - User feedback collection

2. **Revisão Mensal**
   - CAIO revisa portfolio completo
   - Modelos com degradação → trigger re-training ou re-evaluation
   - Modelos com alto custo → trigger optimization

3. **Revisão Trimestral**
   - Integrada ao QBR (`workflows/06-qbr-loop.md`)
   - Portfolio scoring: invest / maintain / sunset
   - Novos casos de uso identificados → volta ao Stage 1

---

## Quality Gates

### Gate 1: Avaliação → POC (Stage 2 → 3)
- [ ] Score de viabilidade ≥ 6/10
- [ ] Dados necessários identificados e acessíveis (ou plano de coleta)
- [ ] Alinhamento estratégico confirmado pelo Vision Chief
- [ ] Budget para POC aprovado pelo CFO

### Gate 2: POC → Avaliação (Stage 4 → 5)
- [ ] Métricas de sucesso mensuradas
- [ ] Eval suite executada completamente
- [ ] Resultados documentados no template padrão
- [ ] Red-teaming executado

### Gate 3: Avaliação → Produção (Stage 5 → 6)
- [ ] `checklists/caio/model-eval-and-guardrails.md` — PASS ✅
- [ ] `checklists/caio/caio-ai-risk-assessment.md` — PASS ✅
- [ ] ROI positivo confirmado pelo CFO
- [ ] Infra de produção viável confirmada pelo CTO
- [ ] Compliance verificado pelo CIO

### Gate 4: Produção → Rollout Completo (Stage 7 canary gates)
- [ ] Canary metrics dentro do SLA
- [ ] Zero incidentes críticos
- [ ] User feedback positivo (se aplicável)
- [ ] Custos de produção dentro do budget

---

## Outputs

| Output | Template | Destino |
|--------|----------|---------|
| Use Case Proposal | `templates/ai/ai-use-case-proposal.md` | Portfolio registry |
| Evaluation Report | `templates/caio/model-evaluation-report.md` | Decision registry |
| Production Runbook | (inline no workflow) | Ops team |
| Portfolio Status | Dashboard consolidado | QBR, Board |

---

## Registries Atualizados

| Registry | Quando Atualizar |
|----------|-----------------|
| `data/registries/ai-portfolio-registry.yaml` | Cada stage transition |
| `data/registries/decision-registry.yaml` | Go/no-go decisions |
| `data/registries/lessons-learned.yaml` | POC kill ou production incident |
| `data/registries/risk-registry.yaml` | Novo risco de IA identificado |

---

## Cross-Squad Handoffs

| Squad | Tipo | SLA | Owner |
|-------|------|-----|-------|
| Data | Dados para treino/avaliação, monitoring contínuo | 3 dias | CIO |
| Cyber | Security review de modelos e dados | 5 dias | CIO |
| Design | UX de AI-powered features | 5 dias | CTO |

---

## Métricas do Pipeline

| Métrica | Target |
|---------|--------|
| Time-to-POC (identificação → POC completo) | < 6 semanas |
| POC success rate | > 40% |
| Time-to-production (POC aprovado → produção) | < 4 semanas |
| Models in production with monitoring | 100% |
| Portfolio review cadence | Mensal |

---

## Referências Cruzadas

### Frameworks
- `frameworks/ai/ai-strategy.md` — Estratégia de IA organizacional
- `frameworks/ai/ai-governance.md` — Governance e compliance
- `frameworks/ai/evals-and-redteaming.md` — Metodologia de avaliação
- `frameworks/ai/mlops.md` — Operacionalização de ML
- `frameworks/ai/adoption-playbook.md` — Change management para IA
- `frameworks/ai/ai-vendor-evaluation.md` — Avaliação de vendors

### Checklists
- `checklists/caio/model-eval-and-guardrails.md` — Gate de avaliação de modelo
- `checklists/caio/caio-ai-risk-assessment.md` — Gate de risco de IA

### Templates
- `templates/ai/ai-use-case-proposal.md` — Proposta de caso de uso
- `templates/caio/model-evaluation-report.md` — Relatório de avaliação

### Workflows Relacionados
- `workflows/06-qbr-loop.md` — Revisão trimestral inclui AI portfolio
- `workflows/11-incident-response-exec.md` — Incidentes de IA
- `workflows/15-evals-and-guardrails-loop.md` — Loop contínuo de avaliação
- `workflows/20-postmortem-and-learning.md` — Postmortem de falhas de IA
