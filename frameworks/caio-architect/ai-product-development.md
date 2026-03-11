# Desenvolvimento de Produto AI — Framework de Product Development para AI/ML

## Propósito e Contexto

Desenvolver produtos baseados em AI é fundamentalmente diferente de desenvolvimento de software
tradicional. Em software clássico, você escreve regras e o sistema as segue. Em AI, você fornece
dados e o sistema aprende padrões — o que significa que o comportamento é probabilístico, não
determinístico. Isso muda tudo: como você planeja, como testa, como promete aos usuários e como
monitora em produção.

Este framework adapta práticas de product development para a realidade de produtos de AI,
cobrindo desde ideação até operação em produção. É para PMs, ML engineers e líderes técnicos
que precisam navegar as incertezas inerentes ao desenvolvimento com AI.

## Quando Usar

- Ao iniciar um novo produto ou feature baseada em AI/ML
- Na avaliação de viabilidade de um caso de uso de AI
- Quando um produto de AI não está performando como esperado
- No planejamento de roadmap de produtos com componentes de AI
- Ao decidir entre abordagem baseada em regras vs. ML
- Na integração de LLMs e AI generativa em produtos existentes

## Componentes do Framework

### 1. AI Product Viability Assessment

Antes de investir em AI, valide viabilidade em 4 dimensões:

**Viabilidade de Dados:**
- Os dados necessários existem e são acessíveis?
- Volume suficiente para treinamento? (mínimos variam por problema)
- Qualidade adequada (rotulagem, completude, representatividade)?
- Custo de aquisição/rotulagem de dados é viável?

**Viabilidade Técnica:**
- O problema é adequado para ML? (patterns vs. regras)
- Existem benchmarks ou papers que demonstrem viabilidade?
- A performance necessária (accuracy, latência) é alcançável?
- A equipe tem expertise técnica necessária?

**Viabilidade de Negócio:**
- O problema vale a pena resolver com AI? (ROI positivo)
- Qual a alternativa non-AI e quanto custa?
- O impacto é mensurável e significativo?
- Existe willingness-to-pay por uma solução AI-powered?

**Viabilidade Ética:**
- O caso de uso é aceitável eticamente?
- Riscos de bias são gerenciáveis?
- Compliance regulatório é possível?
- Referência: `frameworks/caio-architect/responsible-ai.md`

### 2. AI Product Development Lifecycle

Diferente do ciclo tradicional de software, AI tem loops adicionais:

```
IDEAÇÃO → VIABILIDADE → DATA → EXPERIMENTAÇÃO → PRODUÇÃO → MONITORING
   ↑                      ↑        ↑                           |
   |                      |        └─── Retrain ←──────────────┤
   |                      └──── Mais dados ←───────────────────┤
   └──────── Pivot/Kill ←─────────────────────────────────────┘
```

**Fase de Data (não existe em software tradicional):**
- Coleta e curadoria de dados de treinamento
- Rotulagem (manual, semi-automática ou active learning)
- Feature engineering e feature selection
- Data split (train/validation/test) com cuidado temporal

**Fase de Experimentação:**
- Baseline com abordagem simples (heurística ou modelo simples)
- Iteração de modelos com tracking de experimentos (MLflow, W&B)
- Avaliação offline: métricas técnicas (accuracy, F1, AUC)
- Avaliação online: A/B testing com métricas de negócio
- Go/no-go baseado em critérios pré-definidos

### 3. Especificidades de Produtos com LLMs/GenAI

**Desafios Únicos:**
- Output não-determinístico (mesma entrada, respostas diferentes)
- Hallucinations (modelo gera informação falsa com confiança)
- Cost per inference significativo (vs. ML tradicional)
- Latência maior que software tradicional
- Dificuldade de avaliar qualidade automaticamente

**Práticas Recomendadas:**
- Eval suites: conjuntos de testes com respostas esperadas
- Guardrails: filtros de output (toxicidade, factualidade)
- Human-in-the-loop para decisões de alto risco
- RAG (Retrieval Augmented Generation) para grounding em dados reais
- Prompt engineering como disciplina (versionamento, A/B testing de prompts)
- Caching e batching para otimização de custo
- Fallback gracioso quando modelo não tem confiança

### 4. Métricas de Produto AI

| Tipo | Métrica | Descrição |
|------|---------|-----------|
| Técnica | Accuracy / F1 / AUC | Performance do modelo offline |
| Produto | Task completion rate | % de usuários que completam a tarefa com AI |
| Produto | AI acceptance rate | % de sugestões aceitas pelo usuário |
| Negócio | Time saved | Tempo economizado por interação |
| Negócio | Revenue impact | Impacto em conversão, ticket, retention |
| Confiança | User trust score | Pesquisa de confiança na AI |
| Custo | Cost per inference | Custo por chamada ao modelo |

## Processo Passo-a-Passo

### Sprint 0: Viabilidade (1-2 semanas)
1. Completar AI Product Viability Assessment
2. Identificar datasets existentes e gaps
3. Definir baseline (abordagem mais simples que funciona)
4. Estimar timeline e recursos necessários
5. Go/no-go com PM + ML lead + stakeholder de negócio

### Sprint 1-N: Experimentação (2-6 semanas)
1. Construir pipeline de dados e feature engineering
2. Treinar e avaliar modelos iterativamente
3. Comparar com baseline — melhoria significativa?
4. Se performance insuficiente: mais dados? melhor features? problema diferente?
5. Definir critérios de go-to-production

### Sprint N+1: Produção (2-4 semanas)
1. Deploy com feature flag (soft launch)
2. A/B test AI vs. non-AI (ou vs. versão anterior)
3. Monitor performance técnica e métricas de negócio
4. Ramp up gradual baseado em resultados

### Ongoing: Operação
1. Monitoring de drift e degradação
2. Feedback loop: usar interações de produção para melhorar modelo
3. Retraining schedule baseado em triggers (não apenas calendário)
4. Evolução do modelo com novos dados e técnicas

## Template de AI Product Brief

```markdown
# AI Product Brief: [Nome]

## Problema
[Qual problema estamos resolvendo e para quem]

## Hipótese de AI
[Por que AI é a melhor abordagem para este problema]

## Viabilidade Assessment
- Dados: [score 1-5 e justificativa]
- Técnica: [score 1-5 e justificativa]
- Negócio: [score 1-5 e justificativa]
- Ética: [score 1-5 e justificativa]

## Approach
- Tipo de modelo: [classificação, generativo, recomendação, etc.]
- Baseline: [abordagem simples para comparação]
- Success criteria: [métrica ≥ threshold]
- Kill criteria: [quando desistir]

## Recursos
- Dados: [datasets necessários e disponibilidade]
- Equipe: [ML engineer, PM, domain expert]
- Timeline: [estimativa com fases]
- Infra: [GPU, serving, etc.]
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Viability assessment completion | 100% antes de iniciar | Por projeto |
| Model performance vs. baseline | > 20% improvement | Por modelo |
| Time-to-production | < 3 meses para v1 | Por projeto |
| AI feature adoption | > 50% dos usuários elegíveis | Mensal |
| Cost per inference | Decrescente | Mensal |
| Model retraining frequency | Conforme SLA definido | Contínuo |

## Referências Cruzadas

- `frameworks/caio-architect/mlops-framework.md` — Infraestrutura para levar AI a produção
- `frameworks/caio-architect/responsible-ai.md` — Ética no desenvolvimento de produto AI
- `frameworks/caio-architect/ai-maturity-model.md` — Maturidade necessária para cada tipo de produto
- `frameworks/caio-architect/ai-governance.md` — Governança de produtos de AI
- `frameworks/cto-architect/build-vs-buy.md` — Build vs buy para capabilities de AI
- `frameworks/vision-chief/market-thesis-framework.md` — Tese de mercado para produtos AI
- `frameworks/cfo-strategist/unit-economics.md` — Unit economics de produtos AI
