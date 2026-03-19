# Evals e Red-Teaming — Framework de Avaliação e Testes Adversariais de Modelos de IA

## Origem e Contexto

Evals (avaliações) e red-teaming são os dois pilares que garantem que modelos de IA funcionem
como esperado e não causem danos quando expostos ao mundo real. Evals medem performance
quantitativa; red-teaming testa robustez contra uso malicioso, edge cases e comportamentos
inesperados.

A indústria aprendeu da pior forma que modelos podem ser brilhantes em benchmarks e desastrosos
em produção. O gap entre "funciona no teste" e "funciona no mundo real" é preenchido por um
sistema rigoroso de avaliação contínua e testes adversariais.

Este framework se baseia nas práticas de Anthropic (Constitutional AI, red-teaming), OpenAI
(evals framework), Google DeepMind (safety evaluations), e no NIST AI RMF. Adaptado para
organizações que deployam modelos proprietários e utilizam LLMs via API.

## Quando Usar

- Antes de qualquer deploy de modelo em produção
- Em ciclos regulares de avaliação de modelos já em produção
- Ao fine-tunar ou customizar modelos de terceiros
- Quando novos riscos ou vulnerabilidades são descobertos na comunidade
- Na seleção entre modelos concorrentes para um use case
- Quando stakeholders pedem evidência de que o modelo é seguro e eficaz

## Quando NÃO Usar

- Como único critério de decisão (evals medem o que medem, não tudo)
- Em substituição a testes de software tradicionais (unit tests, integration tests)
- Quando o modelo ainda está em fase exploratória e não vai a produção
- Como burocracia para protótipos internos de baixo risco

## Estrutura / Modelo

### Modelo de Avaliação em 4 Camadas

```
┌─────────────────────────────────────────────────────┐
│           EVALUATION PYRAMID                         │
│                                                      │
│                  ┌───────┐                           │
│                  │ RED   │  ← Testes adversariais    │
│                  │ TEAM  │    (segurança, abuso)     │
│                ┌─┴───────┴─┐                         │
│                │  HUMAN    │  ← Avaliação humana      │
│                │  EVAL     │    (qualidade, utilidade) │
│              ┌─┴───────────┴─┐                       │
│              │  DOMAIN       │  ← Benchmarks          │
│              │  BENCHMARKS   │    específicos          │
│            ┌─┴───────────────┴─┐                     │
│            │  AUTOMATED EVALS   │ ← Métricas          │
│            │  (baseline)        │   automáticas        │
│            └────────────────────┘                     │
└─────────────────────────────────────────────────────┘
```

### Tipos de Avaliação

| Tipo | O que Mede | Quando | Quem |
|------|-----------|--------|------|
| **Automated Evals** | Accuracy, latency, throughput, regression | Contínuo (CI/CD) | Pipeline automatizado |
| **Domain Benchmarks** | Performance em tarefas específicas do domínio | Pré-deploy + mensal | Time de ML |
| **Human Eval** | Qualidade percebida, utilidade, naturalidade | Pré-deploy + trimestral | Avaliadores treinados |
| **Red-Teaming** | Segurança, robustez, manipulabilidade | Pré-deploy + mensal | Red team dedicado |

### Categorias de Red-Teaming

| Categoria | Objetivo | Exemplos de Testes |
|-----------|----------|-------------------|
| **Jailbreaking** | Contornar guardrails | Prompt injection, role-play attacks |
| **Elicitação de conteúdo nocivo** | Gerar outputs perigosos | Violência, desinformação, CSAM |
| **Data extraction** | Extrair dados de treinamento | Membership inference, data leakage |
| **Bias probing** | Identificar vieses discriminatórios | Testes por subgrupo demográfico |
| **Adversarial inputs** | Inputs malformados ou adversariais | Typos intencionais, unicode tricks |
| **Social engineering** | Manipular o modelo via contexto | Multi-turn manipulation, authority claims |

## Processo de Aplicação (step-by-step)

### Step 1: Definir Eval Suite Baseline

Para cada modelo, criar suite de avaliação automática:

```
EVAL SUITE — [Nome do Modelo]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. FUNCTIONAL EVALS
   - Accuracy no task principal (benchmark interno)
   - Accuracy em edge cases documentados
   - Latência p50/p95/p99
   - Throughput sob carga esperada

2. REGRESSION EVALS
   - Golden dataset (inputs/outputs esperados)
   - Comparação com versão anterior do modelo
   - A/B test metrics (se aplicável)

3. SAFETY EVALS (automatizados)
   - Toxicity classifier nos outputs
   - PII detection nos outputs
   - Refusal rate em prompts proibidos
   - Format compliance (JSON schema, etc.)
```

### Step 2: Construir Domain Benchmarks

Criar benchmarks específicos para o domínio de atuação:

- **Curar dataset de avaliação**: 200-1000 exemplos representativos
- **Definir métricas**: precisão, recall, F1, BLEU, ROUGE, ou métricas custom
- **Estabelecer baseline**: performance mínima aceitável
- **Versionar**: tratar benchmarks como código (versionado, reprodutível)

**Importante**: benchmarks devem incluir exemplos difíceis e edge cases, não apenas o "happy path".

### Step 3: Implementar Human Evaluation

Protocolo de avaliação humana:

1. **Recrutar avaliadores**: mínimo 3 avaliadores por task; treinar em guidelines
2. **Definir rubric**: escala clara (ex: 1-5) com exemplos para cada nível
3. **Blind evaluation**: avaliadores não sabem qual modelo gerou o output
4. **Inter-rater agreement**: calcular Cohen's Kappa ou Krippendorff's Alpha
5. **Sample size**: mínimo 100 exemplos para significância estatística
6. **Documentar**: registrar guidelines, rubric, resultados e decisões

### Step 4: Executar Red-Teaming Estruturado

**Fase de Preparação**:
- Montar red team (interno + externo se possível)
- Definir escopo: quais categorias de ataque testar
- Criar threat model: quem atacaria, por quê, como
- Documentar guardrails existentes

**Fase de Execução**:
- Cada red teamer recebe budget de tempo (ex: 4h por categoria)
- Documentar cada tentativa: input, output, sucesso/falha
- Priorizar achados por severidade (Critical/High/Medium/Low)
- Testar em diferentes condições (temperatura, system prompt, etc.)

**Fase de Remediação**:
- Classificar achados: fix imediato vs aceitar risco vs mitigar
- Implementar fixes e retestar
- Adicionar casos ao regression test suite
- Atualizar guardrails e system prompts

### Step 5: Estabelecer Cadência de Avaliação

| Frequência | Atividade |
|------------|-----------|
| **Contínuo** | Automated evals no CI/CD pipeline |
| **Semanal** | Review de métricas de produção e alertas |
| **Mensal** | Red-teaming focado + domain benchmark refresh |
| **Trimestral** | Human eval completa + benchmark suite update |
| **Ad-hoc** | Quando nova vulnerabilidade é publicada na comunidade |

### Step 6: Monitoramento em Produção

Após deploy, monitorar continuamente:

- **Output quality**: sampling de outputs para review humano
- **Safety incidents**: logs de guardrail triggers e refusals
- **User feedback**: thumbs up/down, complaints, escalations
- **Drift detection**: mudança na distribuição de inputs ou outputs
- **Latency/errors**: SLOs de performance técnica

**Referência**: `checklists/caio/model-eval-and-guardrails.md`

## Exemplos Práticos

### Exemplo 1: Eval de Chatbot de Atendimento

**Automated Evals**:
- Intent classification accuracy: >92% no test set
- Response latency: p95 < 2s
- PII detection: 0 vazamentos em 10K testes
- Refusal rate em tópicos proibidos: >99%

**Human Eval** (rubric 1-5):
- Relevância da resposta: média >4.0
- Naturalidade: média >3.8
- Completude: média >3.5

**Red-Teaming** (achados):
- Jailbreak via role-play: 2 bypasses encontrados (Critical) — corrigidos
- Data extraction: modelo revelou formato de dados internos (High) — mitigado
- Bias: respostas diferentes por idioma do input (Medium) — em investigação

### Exemplo 2: Modelo de Classificação de Documentos

**Domain Benchmarks**:
- F1-score por categoria: mínimo 0.85 em cada
- Confusion matrix: sem confusão entre categorias críticas
- Performance em documentos multilíngue: >0.80 F1

**Red-Teaming** (focado):
- Adversarial inputs: documentos com formatação corrompida
- Boundary cases: documentos que pertencem a múltiplas categorias
- Data poisoning simulation: performance com 5% de labels incorretos

## Armadilhas Comuns

1. **Goodhart's Law**: otimizar para o benchmark em vez do problema real
2. **Benchmark overfitting**: modelo "decora" o benchmark mas não generaliza
3. **Red-teaming insuficiente**: testar só o óbvio e ignorar ataques sofisticados
4. **Human eval sem rigor**: avaliadores sem treinamento, rubric vaga, amostra pequena
5. **Eval uma vez e pronto**: não reavaliar após mudanças no modelo ou dados
6. **Ignorar produção**: evals em sandbox não refletem comportamento real
7. **Segurança como feature, não processo**: tratar segurança como algo que se "adiciona" no final
8. **Métricas sem contexto**: accuracy de 95% pode ser péssimo se baseline é 94%

## Integração com Outros Frameworks

| Framework | Relação |
|-----------|---------|
| `frameworks/ai/ai-governance.md` | Evals como mecanismo de governança |
| `frameworks/ai/mlops.md` | Pipeline de evals integrado ao MLOps |
| `frameworks/ai/ai-strategy.md` | Critérios de qualidade para go/no-go |
| `frameworks/caio-architect/caio-responsible-ai.md` | Fairness evals como parte de IA responsável |
| `checklists/caio/model-eval-and-guardrails.md` | Checklist de avaliação e guardrails |
| `checklists/ai/bias-evaluation-checklist.md` | Avaliação específica de bias |
| `checklists/ai/model-deployment-checklist.md` | Pré-deploy checklist incluindo evals |

## Referências

- OpenAI, "Evals" (framework open-source de avaliação)
- Anthropic, "Red Teaming Language Models to Reduce Harms" (2022)
- Google DeepMind, "Scalable Oversight" e safety evaluations
- NIST AI RMF, "AI Risk Management Framework" (2023)
- Hugging Face, "Evaluate" library e model benchmarking
- Stanford HELM, "Holistic Evaluation of Language Models" (2022)
- Ethan Perez et al., "Red Teaming Language Models with Language Models" (2022)
- C-Level Squad: `checklists/caio/model-eval-and-guardrails.md`, `checklists/ai/bias-evaluation-checklist.md`
