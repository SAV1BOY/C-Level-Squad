# AI Vendor Evaluation — Framework de Avaliação de Fornecedores de IA

## Origem e Contexto

A decisão de comprar capacidades de IA de um vendor é uma das mais consequentes que uma organização
faz no domínio de tecnologia. Diferente de SaaS tradicional, vendors de IA têm riscos específicos:
lock-in de dados e modelos, dependência de APIs proprietárias, custos que escalam de forma
imprevisível, e risco de obsolescência rápida em um mercado que muda a cada trimestre.

Este framework estrutura a avaliação de vendors de IA com critérios objetivos, processo de POC
rigoroso, e análise de riscos específicos do domínio. Não é um checklist genérico de procurement —
é uma ferramenta de decisão estratégica para CTO, CAIO e líderes técnicos.

Inspirado em frameworks de vendor evaluation de Gartner e Forrester, adaptado com critérios
específicos para IA: qualidade de modelos, data handling, explicabilidade, vendor viability,
e estratégia de saída.

## Quando Usar

- Na seleção entre vendors de IA para um use case específico
- Ao decidir build vs buy e o "buy" está na mesa
- Na renovação de contrato com vendor de IA existente
- Quando múltiplos times querem comprar soluções de IA diferentes
- Na consolidação de vendors de IA (reduzir fragmentação)
- Na avaliação de plataformas de ML / AI as a Service

## Quando NÃO Usar

- Quando a decisão já é claramente build (diferencial competitivo core)
- Para ferramentas genéricas que não envolvem IA proprietária
- Como substituto para avaliação técnica profunda (este framework complementa)
- Quando o budget não comporta nenhum vendor (resolve funding primeiro)

## Estrutura / Modelo

### Scorecard de Avaliação de Vendor de IA

```
┌─────────────────────────────────────────────────────┐
│        AI VENDOR EVALUATION SCORECARD                │
│                                                      │
│  ┌────────────────┐  Peso  Score  Weighted          │
│  │ CAPABILITY     │  25%   ___    ___               │
│  │ (funcional)    │                                  │
│  ├────────────────┤                                  │
│  │ DATA & PRIVACY │  20%   ___    ___               │
│  │ (dados)        │                                  │
│  ├────────────────┤                                  │
│  │ INTEGRATION    │  15%   ___    ___               │
│  │ (técnico)      │                                  │
│  ├────────────────┤                                  │
│  │ COMMERCIAL     │  15%   ___    ___               │
│  │ (financeiro)   │                                  │
│  ├────────────────┤                                  │
│  │ VENDOR HEALTH  │  10%   ___    ___               │
│  │ (viabilidade)  │                                  │
│  ├────────────────┤                                  │
│  │ LOCK-IN RISK   │  10%   ___    ___               │
│  │ (saída)        │                                  │
│  ├────────────────┤                                  │
│  │ SUPPORT & SLA  │  5%    ___    ___               │
│  │ (suporte)      │                                  │
│  └────────────────┘                                  │
│                    TOTAL:   ___                       │
└─────────────────────────────────────────────────────┘
```

### Critérios Detalhados por Dimensão

| Dimensão | Critério | Peso no Grupo | Escala |
|----------|---------|---------------|--------|
| **Capability** | Accuracy/Quality no nosso use case | 40% | 1-10 |
| | Latência e throughput | 20% | 1-10 |
| | Customização/fine-tuning disponível | 20% | 1-10 |
| | Roadmap e velocidade de evolução | 20% | 1-10 |
| **Data & Privacy** | Localização dos dados (residency) | 25% | 1-10 |
| | Tratamento de dados de treinamento | 25% | 1-10 |
| | Conformidade LGPD/GDPR | 25% | 1-10 |
| | Encriptação e segurança | 25% | 1-10 |
| **Integration** | APIs e SDKs disponíveis | 30% | 1-10 |
| | Compatibilidade com nosso stack | 30% | 1-10 |
| | Documentação e developer experience | 20% | 1-10 |
| | Webhooks, eventos, extensibilidade | 20% | 1-10 |
| **Commercial** | Modelo de pricing (previsibilidade) | 35% | 1-10 |
| | TCO em 3 anos vs alternativas | 35% | 1-10 |
| | Flexibilidade contratual | 30% | 1-10 |
| **Vendor Health** | Funding/revenue e sustentabilidade | 40% | 1-10 |
| | Base de clientes e referências | 30% | 1-10 |
| | Time técnico e liderança | 30% | 1-10 |
| **Lock-in Risk** | Portabilidade de dados | 35% | 1-10 |
| | Portabilidade de modelos/configs | 35% | 1-10 |
| | Alternativas de mercado viáveis | 30% | 1-10 |
| **Support & SLA** | SLA de uptime garantido | 40% | 1-10 |
| | Qualidade do suporte técnico | 30% | 1-10 |
| | Acesso a account manager/CSM | 30% | 1-10 |

## Processo de Aplicação (step-by-step)

### Step 1: Definir Requisitos e Critérios (Requirements Doc)

Antes de avaliar qualquer vendor, documentar:

```
AI VENDOR REQUIREMENTS
━━━━━━━━━━━━━━━━━━━━━━━
Use Case:
Business Owner:
Technical Owner:
Budget Approved:
Timeline:

MUST HAVE (eliminatório):
- [ ] ...

SHOULD HAVE (diferenciador):
- [ ] ...

NICE TO HAVE:
- [ ] ...

DEAL BREAKERS:
- [ ] Dados saem do Brasil
- [ ] Sem SLA de uptime
```

### Step 2: Long List para Short List

1. **Long List**: identificar todos os vendors relevantes (5-10)
2. **Filtrar por deal breakers**: eliminar quem não atende must-haves
3. **Short List**: 2-4 vendors para avaliação detalhada
4. **Documentar razões de eliminação**: transparência na decisão

### Step 3: Avaliação Técnica Profunda

Para cada vendor na short list:

- **Demo técnica**: não marketing, demo com engenheiro do vendor
- **Sandbox/trial**: acesso a ambiente de teste com nossos dados
- **API testing**: testar integração real, não apenas documentação
- **Security review**: questionário de segurança + análise de políticas

### Step 4: POC (Proof of Concept) Estruturado

Design do POC:

```
POC DESIGN
━━━━━━━━━━━
Duração: 2-4 semanas
Escopo: use case real, dados reais (sample representativo)
Critérios de sucesso (definidos ANTES):
- Métrica 1: accuracy > X%
- Métrica 2: latência p95 < Yms
- Métrica 3: integração funcional em < Z dias
- Métrica 4: custo estimado < R$ W/mês

Avaliadores: tech lead + product owner + end user
Documentação: relatório comparativo entre vendors
```

**Regra**: POC sem critérios de sucesso pré-definidos é perda de tempo.

### Step 5: Análise Comercial e TCO

Calcular TCO (Total Cost of Ownership) para 3 anos:

| Custo | Ano 1 | Ano 2 | Ano 3 | Total |
|-------|-------|-------|-------|-------|
| Licenças/API | | | | |
| Implementação | | | | |
| Integração | | | | |
| Treinamento | | | | |
| Suporte premium | | | | |
| Overhead interno | | | | |
| **TOTAL** | | | | |

**Referência**: `frameworks/it-information/total-cost-of-ownership.md`

### Step 6: Negociação e Contrato

Pontos críticos para contrato de vendor de IA:

- **Data ownership**: nossos dados continuam nossos, sempre
- **Training data**: vendor pode usar nossos dados para treinar modelo?
- **Export**: direito de exportar dados e configurações a qualquer momento
- **SLA**: uptime, latência, e penalidades por descumprimento
- **Pricing lock**: proteção contra aumento de preço unilateral
- **Exit clause**: condições e prazo para encerramento
- **IP**: propriedade intelectual de customizações e fine-tuning
- **Audit rights**: direito de auditar práticas de segurança e privacidade

### Step 7: Exit Strategy

Definir estratégia de saída ANTES de assinar:

- **Data portability**: como extrair todos os dados? Formato? Prazo?
- **Model portability**: customizações/fine-tuning são exportáveis?
- **Transition plan**: tempo estimado para migrar para alternativa
- **Alternativas mapeadas**: 2-3 vendors alternativos identificados
- **Internal fallback**: capacidade mínima interna para período de transição

## Exemplos Práticos

### Exemplo 1: Seleção de LLM Provider

**Use case**: chatbot de atendimento ao cliente
**Short list**: OpenAI, Anthropic, Google Vertex AI, AWS Bedrock

**Scorecard resumido**:
| Critério | OpenAI | Anthropic | Google | AWS |
|----------|--------|-----------|--------|-----|
| Capability | 9 | 9 | 8 | 7 |
| Data & Privacy | 7 | 8 | 8 | 9 |
| Integration | 9 | 8 | 8 | 9 |
| Commercial | 7 | 7 | 8 | 8 |
| Vendor Health | 8 | 8 | 10 | 10 |
| Lock-in Risk | 6 | 7 | 7 | 6 |
| **Weighted Total** | **7.8** | **7.9** | **8.1** | **8.0** |

**Decisão**: Google Vertex AI por combinação de capability + vendor stability + pricing.

### Exemplo 2: Avaliação de Plataforma de ML

**Use case**: platform para time de data science (5 pessoas)
**Short list**: Databricks, Vertex AI, SageMaker

**POC results**:
- Databricks: melhor para data engineering + ML integration, pricing complexo
- Vertex AI: melhor managed experience, limitado em customização
- SageMaker: mais flexível, curva de aprendizado maior

**Decisão**: Databricks por fit com stack existente (Spark/Delta Lake).

## Armadilhas Comuns

1. **Demo-driven decision**: escolher baseado na melhor demo, não na melhor avaliação
2. **Ignorar TCO**: escolher o mais barato no Ano 1 sem calcular Ano 2-3
3. **POC sem critérios**: rodar POC e depois decidir com base em "feeling"
4. **Vendor lock-in invisível**: não perceber dependências até tentar migrar
5. **Avaliar features atuais, não roadmap**: vendor pode não evoluir na direção necessária
6. **Ignorar data handling**: não verificar como vendor trata nossos dados
7. **Single point of failure**: depender de um único vendor sem fallback
8. **Comprar por FOMO**: "todos estão usando X" não é critério de avaliação

## Integração com Outros Frameworks

| Framework | Relação |
|-----------|---------|
| `frameworks/ai/ai-strategy.md` | Vendor selection como parte da estratégia de IA |
| `frameworks/ai/ai-governance.md` | Requisitos de governança para vendors |
| `frameworks/cto-architect/build-vs-buy.md` | Decisão build vs buy que precede vendor eval |
| `frameworks/it-information/total-cost-of-ownership.md` | TCO analysis detalhada |
| `checklists/ai/ai-vendor-evaluation.md` | Checklist operacional de avaliação |
| `checklists/caio/caio-ai-vendor-eval.md` | Checklist CAIO para vendor evaluation |

## Referências

- Gartner, "Magic Quadrant for Data Science and Machine Learning Platforms"
- Forrester, "The Forrester Wave: AI/ML Platforms"
- a16z, "Emerging Architectures for LLM Applications" (2023)
- Matt Turck, "MAD (Machine Learning, AI & Data) Landscape" (anual)
- Stanford HAI, "AI Index Report" (comparativos de modelos e plataformas)
- NIST, "AI Risk Management Framework" — seção de third-party risk
- C-Level Squad: `checklists/ai/ai-vendor-evaluation.md`, `checklists/caio/caio-ai-vendor-eval.md`
