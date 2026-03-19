# AI Governance — Framework de Governança de Inteligência Artificial

## Origem e Contexto

Governança de IA é o conjunto de políticas, processos e estruturas organizacionais que garantem
o uso responsável, ético e eficaz de inteligência artificial. Sem governança, IA se torna um risco
regulatório, reputacional e operacional — modelos enviesados, decisões inexplicáveis, dados
sensíveis expostos, e compliance violado.

A governança de IA não é burocracia — é infraestrutura de confiança. Assim como governança
corporativa permite escalar decisões financeiras com controle, governança de IA permite escalar
o uso de modelos com responsabilidade.

Este framework se baseia nos princípios de Responsible AI da OECD, no AI Act da União Europeia,
nas diretrizes do NIST AI Risk Management Framework, e nas práticas de empresas líderes em
AI governance (Microsoft, Google, Anthropic). Adaptado para conformidade com LGPD e regulamentações
brasileiras.

## Quando Usar

- Ao implementar qualquer modelo de IA em produção
- Na criação de políticas corporativas de uso de IA
- Quando regulação exige explicabilidade ou auditoria de modelos
- Ao avaliar riscos de bias em sistemas de decisão automatizada
- Na preparação para auditorias regulatórias ou de compliance
- Ao definir quem pode aprovar deploy de modelos em produção

## Quando NÃO Usar

- Como barreira para experimentação em sandbox/dev (governança é para produção)
- Para projetos puramente internos sem impacto em decisões sobre pessoas
- Como substituto para qualidade técnica (governança não compensa modelo ruim)
- Quando o processo de governança é mais caro que o risco que mitiga

## Estrutura / Modelo

### Modelo GREAT (Governance, Risk, Ethics, Accountability, Transparency)

```
┌─────────────────────────────────────────────────────┐
│              AI GOVERNANCE FRAMEWORK                 │
│                                                      │
│  ┌───────────────────────────────────────────┐      │
│  │         AI REVIEW BOARD                    │      │
│  │  (Ethics + Legal + Tech + Business)        │      │
│  └─────────────────┬─────────────────────────┘      │
│                    │                                 │
│  ┌─────┬───────────┼───────────┬─────────┐          │
│  │     │           │           │         │          │
│  ▼     ▼           ▼           ▼         ▼          │
│ RISK  ETHICS    ACCOUNT-   TRANS-    COMPLIANCE     │
│ MGMT  REVIEW   ABILITY    PARENCY   & AUDIT        │
│  │     │           │           │         │          │
│  └─────┴───────────┴───────────┴─────────┘          │
│                    │                                 │
│           ┌────────▼────────┐                        │
│           │  CONTINUOUS     │                        │
│           │  MONITORING     │                        │
│           └─────────────────┘                        │
└─────────────────────────────────────────────────────┘
```

### Classificação de Risco de Modelos de IA

| Nível | Descrição | Exemplos | Governança Requerida |
|-------|-----------|----------|---------------------|
| **Crítico** | Decisões sobre pessoas, saúde, segurança | Crédito, diagnóstico, contratação | AI Review Board + Auditoria externa |
| **Alto** | Impacto financeiro significativo ou dados sensíveis | Pricing, fraud detection, PII | AI Review Board + Documentação completa |
| **Médio** | Automação operacional com supervisão | Chatbots, recomendação, previsão | Revisão técnica + Monitoramento |
| **Baixo** | Ferramentas internas, sem impacto em pessoas | Autocompletar, classificação interna | Registro + boas práticas |

### Pilares da Governança

| Pilar | Objetivo | Mecanismo |
|-------|----------|-----------|
| **Fairness** | Evitar bias discriminatório | Testes de fairness por subgrupo, auditorias |
| **Accountability** | Responsável claro por cada modelo | Model owner, DRI, cadeia de aprovação |
| **Transparency** | Explicar como e por que decisões são tomadas | Model cards, explicabilidade, logs |
| **Privacy** | Proteger dados pessoais e sensíveis | PIA, anonimização, LGPD compliance |
| **Safety** | Prevenir danos e comportamentos inesperados | Red-teaming, guardrails, kill switches |
| **Robustness** | Garantir performance confiável | Monitoramento, drift detection, fallbacks |

## Processo de Aplicação (step-by-step)

### Step 1: Estabelecer AI Review Board

**Composição mínima**:
- Líder técnico de IA/ML (CAIO ou delegado)
- Representante de Legal/Compliance
- Representante de Ética/Privacidade
- Representante do negócio (stakeholder do use case)
- Representante de Engenharia/Infraestrutura

**Cadência**: reunião quinzenal para revisão de novos modelos; mensal para portfólio existente.

### Step 2: Criar Política de Uso Aceitável de IA

Documentar explicitamente:

- Usos permitidos de IA na organização
- Usos proibidos (ex: decisões automatizadas sobre pessoas sem supervisão humana)
- Processo de solicitação para novos use cases
- Requisitos mínimos para deploy em produção
- Política de dados para treinamento de modelos
- Uso de IA generativa por colaboradores (dados corporativos, propriedade intelectual)

### Step 3: Implementar Model Cards

Para cada modelo em produção, documentar:

```
MODEL CARD — [Nome do Modelo]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Versão:
Owner (DRI):
Data de deploy:
Classificação de risco:
Dados de treinamento (resumo):
Métricas de performance:
Limitações conhecidas:
Testes de bias realizados:
Próxima revisão agendada:
Processo de rollback:
```

### Step 4: Definir Processo de Aprovação por Nível de Risco

- **Baixo**: Auto-aprovação pelo time técnico com registro
- **Médio**: Aprovação do tech lead + revisão de Model Card
- **Alto**: Aprovação do AI Review Board + documentação completa
- **Crítico**: AI Review Board + auditoria independente + aprovação executiva

### Step 5: Implementar Monitoramento Contínuo

Monitorar em produção:
- **Data drift**: distribuição dos inputs mudou?
- **Model drift**: performance do modelo degradou?
- **Bias drift**: métricas de fairness por subgrupo mudaram?
- **Usage patterns**: modelo sendo usado como esperado?
- **Incidents**: comportamentos inesperados ou reclamações?

**Alertas**: definir thresholds para cada métrica e processo de resposta.

### Step 6: Auditoria e Compliance

- Auditoria interna trimestral do portfólio de modelos
- Auditoria externa anual para modelos de risco Crítico/Alto
- Relatório de conformidade LGPD para modelos que processam dados pessoais
- Documentação de decisões automatizadas para atender direito de explicação

**Checklist**: `checklists/caio/caio-ai-risk-assessment.md`

### Step 7: Incident Response para IA

Processo específico para incidentes envolvendo IA:

1. **Detecção**: monitoramento identifica anomalia ou reclamação chega
2. **Contenção**: kill switch ou fallback para lógica não-ML
3. **Investigação**: root cause analysis do comportamento do modelo
4. **Remediação**: fix no modelo, dados, ou pipeline
5. **Comunicação**: stakeholders internos e, se necessário, externos
6. **Post-mortem**: documentação e aprendizados registrados

## Exemplos Práticos

### Exemplo 1: Modelo de Scoring de Crédito

**Classificação**: Risco Crítico
**Governança aplicada**:
- Model Card completo com documentação de dados de treinamento
- Testes de fairness por gênero, raça, idade, região geográfica
- Auditoria externa anual por empresa especializada
- Monitoramento contínuo de drift e fairness metrics
- Processo de explicação para clientes negados (LGPD Art. 20)
- Kill switch: fallback para regras manuais em caso de falha

### Exemplo 2: Chatbot de Atendimento com LLM

**Classificação**: Risco Médio-Alto
**Governança aplicada**:
- Guardrails para tópicos proibidos (financeiro, jurídico, médico)
- Monitoramento de outputs por sampling (5% revisados por humanos)
- Política de dados: conversas não usadas para treinamento sem consentimento
- Fallback para atendente humano em edge cases
- Red-teaming mensal para testar jailbreaks e manipulação
- Template de Model Card preenchido e revisado trimestralmente

## Armadilhas Comuns

1. **Governance theater**: criar políticas bonitas que ninguém segue
2. **Over-governance**: processo tão pesado que mata inovação e velocidade
3. **Under-governance**: liberdade total até o primeiro incidente grave
4. **Bias como afterthought**: testar bias só depois do deploy
5. **Documentação desatualizada**: Model Cards que não refletem o modelo atual
6. **Compliance checkbox**: tratar governança como checklist burocrático, não como prática viva
7. **Falta de enforcement**: regras sem consequências para descumprimento
8. **Ignorar IA generativa**: não ter política para uso de ChatGPT/Claude pelos colaboradores

## Integração com Outros Frameworks

| Framework | Relação |
|-----------|---------|
| `frameworks/ai/ai-strategy.md` | Governança como pilar da estratégia de IA |
| `frameworks/ai/evals-and-redteaming.md` | Avaliação técnica e testes adversariais |
| `frameworks/ai/mlops.md` | Monitoramento e operacionalização |
| `frameworks/caio-architect/caio-responsible-ai.md` | Implementação de IA responsável |
| `frameworks/caio-architect/caio-ai-portfolio-strategy.md` | Gestão do portfólio com governança |
| `checklists/caio/caio-ai-risk-assessment.md` | Assessment de risco por modelo |
| `checklists/caio/model-eval-and-guardrails.md` | Guardrails e avaliação de modelos |
| `checklists/ai/bias-evaluation-checklist.md` | Avaliação específica de bias |

## Referências

- OECD, "AI Principles" (2019)
- EU AI Act — Regulamento (UE) 2024/1689
- NIST, "AI Risk Management Framework" (AI RMF 1.0, 2023)
- Brasil — LGPD (Lei 13.709/2018), especialmente Art. 20 (decisões automatizadas)
- Microsoft, "Responsible AI Standard" (v2, 2022)
- Google, "AI Principles" e "Model Cards for Model Reporting"
- Anthropic, "Core Views on AI Safety"
- Margaret Mitchell et al., "Model Cards for Model Reporting" (2019)
- C-Level Squad: `checklists/caio/caio-ai-risk-assessment.md`, `checklists/ai/bias-evaluation-checklist.md`
