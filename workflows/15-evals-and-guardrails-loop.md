# Workflow 15 — Evals and Guardrails Loop

> **Loop contínuo de avaliação de modelos de IA e manutenção de guardrails para garantir qualidade, segurança e alinhamento.**
> Modelos em produção sem eval contínuo degradam silenciosamente. Este workflow previne isso.

---

## Objetivo

Estabelecer um loop contínuo e disciplinado de avaliação de modelos de IA em produção e manutenção dos guardrails que protegem a organização. O workflow garante que:

1. **Modelos são avaliados regularmente** — não apenas no deploy, mas continuamente
2. **Guardrails evoluem com ameaças** — novos riscos geram novos guardrails
3. **Degradação é detectada proativamente** — antes que afete usuários
4. **Red-teaming é recorrente** — adversarial testing como prática, não evento
5. **Aprendizados alimentam o pipeline** — integração com Workflow 14

> **Princípio:** Modelo sem eval é modelo desconhecido. Guardrail sem teste é falsa segurança.

---

## Agentes Envolvidos

| Agente | Papel no Workflow |
|--------|-------------------|
| **CAIO Architect** | Lead — define eval criteria, aprova guardrails, coordena red-teaming |
| **CTO Architect** | Support — performance engineering, infra de eval, reliability |
| **CIO Engineer** | Support — data quality para evals, compliance monitoring |
| **Vision Chief (CEO)** | Reviewer — riscos estratégicos de IA, reputação |
| **Squad Coordinator** | Logística — scheduling, consolidação de reports |

---

## Trigger (quando iniciar)

### Triggers Periódicos
- Cadência mensal: revisão de todos os modelos em produção
- Cadência trimestral: deep eval + red-teaming completo (alinhado ao QBR)
- Cadência anual: revisão completa de guardrails policy

### Triggers por Evento
- Novo modelo deployado em produção (Stage 7 do Workflow 14)
- Incidente com modelo (output incorreto, bias detectado, data leak)
- Alerta de monitoring (drift, degradação de performance, custo anômalo)
- Nova vulnerabilidade de IA publicada (prompt injection, jailbreak, etc.)
- Mudança regulatória que afeta IA (LGPD, AI Act, etc.)
- Update de modelo base (novo release do vendor)

---

## Pré-condições

- [ ] Modelos em produção registrados em `data/registries/ai-portfolio-registry.yaml`
- [ ] Eval framework definido (`frameworks/ai/evals-and-redteaming.md`)
- [ ] Guardrails baseline configurados para cada modelo
- [ ] Monitoring ativo com métricas de performance
- [ ] Red-teaming playbook documentado

---

## Processo (step-by-step)

### Stage 1: Define/Update Eval Criteria (1-2 dias)

**Owner**: CAIO Architect

1. **Revisar Critérios Existentes**
   - Para cada modelo em produção, verificar se eval criteria ainda são relevantes
   - Adicionar novos critérios baseados em incidentes ou mudanças de contexto
   - Verificar cobertura: funcionalidade, segurança, bias, performance, custo

2. **Categorias de Avaliação**
   ```
   ┌─────────────────────────────────────────────────────┐
   │              EVAL DIMENSIONS                         │
   ├──────────────┬──────────────┬──────────────┬────────┤
   │  FUNCTIONAL  │   SAFETY     │  FAIRNESS    │ PERF   │
   │              │              │              │        │
   │  Accuracy    │  Toxicity    │  Bias        │ Latency│
   │  Relevance   │  Jailbreak   │  Equity      │ Cost   │
   │  Coherence   │  Data leak   │  Representation│Throughput│
   │  Completeness│  Hallucinate │  Disparate   │ Uptime │
   └──────────────┴──────────────┴──────────────┴────────┘
   ```

3. **Definir Thresholds**
   - Para cada métrica: green / yellow / red thresholds
   - Yellow → alert + investigação
   - Red → circuit breaker + rollback + incident response

### Stage 2: Build/Update Eval Suite (2-3 dias)

**Owner**: CAIO Architect + equipe técnica

1. **Eval Datasets**
   - Manter golden dataset atualizado (ground truth)
   - Adicionar novos exemplos de edge cases
   - Incluir exemplos de incidentes passados
   - Garantir representatividade (demographics, use cases, languages)

2. **Automated Eval Pipeline**
   - Scripts de avaliação automatizados
   - CI/CD integration para eval on deploy
   - Scheduled runs para eval contínuo
   - Dashboard de resultados

3. **Red-Team Scenarios**
   - Prompt injection attempts
   - Jailbreak techniques (DAN, roleplay, encoding tricks)
   - Data extraction attempts
   - Bias elicitation prompts
   - Edge cases específicos do domínio

4. **Human Eval Protocol**
   - Quando automated eval não é suficiente
   - Quem avalia, quantas amostras, rubric de avaliação
   - Inter-annotator agreement target: > 0.8

### Stage 3: Run Evaluations (1-2 dias)

**Owner**: CAIO Architect

1. **Automated Eval Run**
   - Executar eval suite completa para cada modelo
   - Comparar com baseline (último eval) e thresholds
   - Gerar report automatizado com deltas

2. **Red-Team Session**
   - Frequência: trimestral para cada modelo
   - Equipe: CAIO + CIO + external (se disponível)
   - Duração: 2-4 horas por modelo
   - Documentar findings com severity scoring

3. **Production Monitoring Review**
   - Analisar logs de monitoring do último período
   - Identificar patterns de degradação
   - Verificar distribuição de inputs vs training data (drift)
   - Verificar custo per inference trends

### Stage 4: Analyze Results (1-2 dias)

**Owner**: CAIO Architect

1. **Compilar Report**
   - Consolidar automated eval + red-team + monitoring
   - Preencher `templates/caio/model-evaluation-report.md`
   - Comparar com eval anterior: melhorou, estável, degradou?

2. **Risk Assessment**
   - Aplicar `checklists/caio/caio-ai-risk-assessment.md`
   - Para cada finding: severity (critical / high / medium / low)
   - Para cada finding: likelihood × impact scoring
   - Priorizar por risk score

3. **Pattern Analysis**
   - Há padrões cross-model? (ex: todos degradaram em X)
   - Há correlação com eventos externos? (novo attack vector)
   - Há correlação com data changes? (drift)

### Stage 5: Update Guardrails (2-3 dias)

**Owner**: CAIO Architect + CTO Architect

1. **Guardrails Review**
   - Para cada finding de segurança: guardrail existente é suficiente?
   - Se não: definir novo guardrail ou fortalecer existente
   - Tipos de guardrails:
     - **Input guardrails**: content filtering, length limits, rate limiting
     - **Output guardrails**: toxicity detection, PII detection, hallucination detection
     - **System guardrails**: circuit breakers, fallbacks, human-in-the-loop
     - **Process guardrails**: approval workflows, audit logging

2. **Implementar Updates**
   - CTO implementa guardrails técnicos
   - CAIO define policies de guardrails
   - Testar guardrails antes de deploy

3. **Validar Guardrails**
   - Re-run red-team scenarios com novos guardrails
   - Verificar que guardrails não degradam performance aceitavelmente
   - Medir false positive rate dos guardrails

### Stage 6: Deploy Updates (1-2 dias)

**Owner**: CTO Architect

1. **Deploy Guardrail Updates**
   - Seguir padrão de gradual rollout (canary)
   - Monitorar impacto em metrics de negócio
   - Rollback plan definido

2. **Deploy Model Updates (se necessário)**
   - Re-training se drift significativo
   - Model swap se versão melhor disponível
   - Seguir pipeline completo do Workflow 14 Stage 7

3. **Update Documentation**
   - Atualizar guardrails documentation
   - Atualizar runbooks
   - Atualizar eval criteria se necessário

### Stage 7: Monitor (contínuo)

**Owner**: CIO Engineer + CAIO Architect

1. **Monitoring Dashboards**
   - Performance metrics em real-time
   - Guardrail trigger rates
   - Cost tracking
   - User feedback aggregation

2. **Alerting**
   - Degradação > threshold → alert para CAIO
   - Guardrail trigger spike → alert para CTO
   - Cost anomaly → alert para CFO
   - Security incident → trigger Workflow 11

3. **Feedback Collection**
   - User feedback (thumbs up/down, reports)
   - Internal feedback de operadores
   - Aggregate e categorize mensalmente

### Stage 8: Report (1 dia)

**Owner**: CAIO Architect

1. **Monthly Eval Summary**
   - Status de cada modelo: green / yellow / red
   - Actions taken no período
   - Guardrail effectiveness metrics
   - Cost trends

2. **Quarterly Deep Report**
   - Integrado ao QBR (Workflow 06)
   - Portfolio health assessment
   - Recommendations para próximo quarter
   - Budget projections

3. **Registrar Aprendizados**
   - Atualizar `data/registries/lessons-learned.yaml`
   - Atualizar `data/registries/ai-portfolio-registry.yaml`
   - Feed back to Workflow 14 para novos cases

---

## Quality Gates

### Gate 1: Eval Coverage
- [ ] Todos os modelos em produção foram avaliados
- [ ] Eval coverage mínima de 80% dos scenarios
- [ ] Red-teaming executado (trimestral)
- [ ] Results documentados no template padrão

### Gate 2: Guardrail Effectiveness
- [ ] Guardrails testados contra red-team scenarios
- [ ] False positive rate < 5%
- [ ] Zero bypass encontrado em red-teaming
- [ ] Guardrails documentados e versionados

### Gate 3: Report Quality
- [ ] Report preenche todos os campos do template
- [ ] Comparação com período anterior incluída
- [ ] Action items com DRI e deadline
- [ ] Aprovado pelo CAIO

---

## Outputs

| Output | Template | Destino |
|--------|----------|---------|
| Model Evaluation Report | `templates/caio/model-evaluation-report.md` | AI Portfolio Registry |
| Red-Team Findings | (inline no report) | Security review |
| Guardrails Update Log | (inline no report) | Ops documentation |
| Monthly Eval Summary | Dashboard | WBR/MBR |
| Quarterly Deep Report | (inline no QBR) | Board prep |

---

## Registries Atualizados

| Registry | Quando Atualizar |
|----------|-----------------|
| `data/registries/ai-portfolio-registry.yaml` | Cada eval cycle |
| `data/registries/risk-registry.yaml` | Novo risco de IA descoberto |
| `data/registries/lessons-learned.yaml` | Cada finding significativo |
| `data/registries/decision-registry.yaml` | Decisão de sunset/update modelo |

---

## Cross-Squad Handoffs

| Squad | Tipo | SLA | Owner |
|-------|------|-----|-------|
| Data | Eval data preparation, monitoring pipeline | 3 dias | CIO |
| Cyber | Adversarial testing, security review | 5 dias | CIO |

---

## Cadência Resumida

| Atividade | Frequência | Owner |
|-----------|-----------|-------|
| Monitoring review | Semanal | CIO |
| Automated eval run | Mensal | CAIO |
| Monthly summary report | Mensal | CAIO |
| Red-teaming session | Trimestral | CAIO |
| Deep eval + guardrails review | Trimestral | CAIO |
| Guardrails policy review | Anual | CAIO + Vision Chief |

---

## Referências Cruzadas

### Frameworks
- `frameworks/ai/evals-and-redteaming.md` — Metodologia de avaliação e red-teaming
- `frameworks/ai/ai-governance.md` — Governance de IA
- `frameworks/ai/mlops.md` — Operacionalização de modelos

### Checklists
- `checklists/caio/model-eval-and-guardrails.md` — Gate de avaliação
- `checklists/caio/caio-ai-risk-assessment.md` — Assessment de risco

### Templates
- `templates/caio/model-evaluation-report.md` — Relatório de avaliação

### Workflows Relacionados
- `workflows/14-ai-use-case-pipeline.md` — Pipeline de novos casos de uso
- `workflows/11-incident-response-exec.md` — Resposta a incidentes de IA
- `workflows/04-wbr-loop.md` — Review semanal inclui AI metrics
- `workflows/06-qbr-loop.md` — Quarterly inclui AI portfolio deep review
- `workflows/20-postmortem-and-learning.md` — Postmortem de falhas
