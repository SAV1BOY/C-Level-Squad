# AI Readiness Assessment — Avaliação de Prontidão Organizacional para AI

## Origem e Contexto

AI Readiness Assessment é a avaliação estruturada do quão preparada uma organização está para
adotar e escalar inteligência artificial. Antes de investir em AI, é fundamental entender se
a fundação necessária existe: dados organizados, talento disponível, infraestrutura adequada,
cultura receptiva e liderança comprometida.

O maior desperdício em AI é investir em tecnologia sofisticada sobre uma fundação fraca. Segundo
pesquisa da MIT Sloan (2023), organizações que investem em readiness antes de AI têm 3x mais
chance de gerar valor com suas iniciativas. O assessment não é burocracia — é o diagnóstico
que evita gastar R$2M em projeto que vai falhar por falta de dados limpos.

O princípio fundamental: AI readiness não é binário (pronto/não pronto). É um espectro com
múltiplas dimensões, onde a organização pode estar avançada em uma e atrasada em outra. O
assessment identifica os gaps específicos que precisam ser resolvidos antes ou em paralelo
com as iniciativas de AI.

Referências: Google Cloud AI Adoption Framework, McKinsey AI Readiness Assessment, MIT Sloan
AI Maturity Model, Gartner AI Maturity Model.

## Quando Usar

- Antes de definir estratégia de AI (diagnóstico inicial)
- Na justificação de investimento em fundação de dados/AI
- Em revisões anuais de maturidade de AI
- Quando iniciativas de AI estão falhando sem explicação técnica clara
- Na preparação para contratação de liderança de AI (CAIO, Head of AI)
- Em due diligence de empresas para M&A (avaliar capabilities de AI)

## Quando NÃO Usar

- Como substitute para começar (não espere estar 100% pronto; comece pelo que é possível)
- Para bloqueiar iniciativas legítimas (assessment informa, não bloqueia)
- Em organizações que já são maduras em AI (use portfolio strategy)
- Como exercício anual que ninguém usa para decidir (assessment sem ação é desperdício)

## Estrutura / Modelo

### As 6 Dimensões de AI Readiness

```
AI READINESS
│
├── DIMENSÃO 1: DADOS (peso 25%)
│   ├── Disponibilidade: dados necessários existem?
│   ├── Qualidade: limpos, completos, consistentes?
│   ├── Acessibilidade: fáceis de acessar e combinar?
│   ├── Governance: ownership, políticas, compliance?
│   └── Volume: quantidade suficiente para ML?
│
├── DIMENSÃO 2: TECNOLOGIA (peso 20%)
│   ├── Infraestrutura: compute e storage adequados?
│   ├── Plataforma: ferramentas de ML disponíveis?
│   ├── Integração: sistemas podem consumir AI outputs?
│   ├── MLOps: pipelines de ML operacionalizados?
│   └── Segurança: infraestrutura segura para AI?
│
├── DIMENSÃO 3: TALENTO (peso 20%)
│   ├── AI/ML specialists: cientistas de dados, ML engineers?
│   ├── Data Engineering: profissionais de dados?
│   ├── AI Literacy: equipe geral entende AI?
│   ├── Liderança: líder de AI identificado/contratado?
│   └── Pipeline: capacidade de recrutar e reter talento?
│
├── DIMENSÃO 4: ESTRATÉGIA (peso 15%)
│   ├── Visão: liderança articulou visão de AI?
│   ├── Use Cases: casos de uso priorizados?
│   ├── Roadmap: plano de implementação definido?
│   ├── Budget: investimento alocado?
│   └── Métricas: como sucesso será medido?
│
├── DIMENSÃO 5: CULTURA (peso 10%)
│   ├── Data-driven: decisões baseadas em dados?
│   ├── Experimentação: falhar é aceitável?
│   ├── Colaboração: silos entre áreas são baixos?
│   ├── Mudança: receptividade a novas formas de trabalho?
│   └── Ética: sensibilidade a uso responsável de AI?
│
└── DIMENSÃO 6: GOVERNANÇA (peso 10%)
    ├── Políticas: AI use policy existe?
    ├── Compliance: regulação é monitorada?
    ├── Ética: princípios de AI responsável definidos?
    ├── Risco: framework de risco inclui AI?
    └── Auditoria: mecanismos de audit em AI?
```

### AI Readiness Scorecard

```
DIMENSÃO       │ SCORE (1-5) │ NÍVEL          │ GAP CRÍTICO?
───────────────┼─────────────┼────────────────┼─────────────
Dados          │ ___         │ ___            │ [ ] Sim/Não
Tecnologia     │ ___         │ ___            │ [ ] Sim/Não
Talento        │ ___         │ ___            │ [ ] Sim/Não
Estratégia     │ ___         │ ___            │ [ ] Sim/Não
Cultura        │ ___         │ ___            │ [ ] Sim/Não
Governança     │ ___         │ ___            │ [ ] Sim/Não
───────────────┼─────────────┼────────────────┼─────────────
OVERALL        │ ___         │ ___            │

NÍVEIS:
1 = Inexistente (nenhuma capability)
2 = Inicial (esforços ad hoc, sem consistência)
3 = Definido (processos estabelecidos, parcialmente adotados)
4 = Gerenciado (processos maduros, métricas de acompanhamento)
5 = Otimizado (referência de mercado, melhoria contínua)
```

### Mapa de Readiness vs Ambição

```
        ALTA AMBIÇÃO DE AI
              │
   "PREPARE   │   "EXECUTE"
    FIRST"    │
   Fundação   │   Prontos para
   fraca para │   escalar AI
   a ambição  │
              │
──────────────┼──────────────
              │
   "RETHINK"  │   "START SMALL"
   Ambição    │   Fundação
   baixa e    │   existe, falta
   fundação   │   ambição/foco
   fraca      │
              │
        BAIXA AMBIÇÃO DE AI

   BAIXO READINESS ←────→ ALTO READINESS
```

## Processo de Aplicação (step-by-step)

### Passo 1: Preparar o Assessment (1 semana)

- Definir scope: toda a organização ou unidade específica?
- Identificar respondentes: mix de liderança, técnicos, negócio
- Preparar instrumentos: questionário, roteiro de entrevista, checklist de dados
- Alinhar com sponsor executivo sobre objetivo e uso dos resultados

### Passo 2: Coletar Dados (2-3 semanas)

- Questionário quantitativo para 20-50 stakeholders (escala 1-5 por sub-dimensão)
- Entrevistas qualitativas com 8-12 líderes chave
- Audit técnico: inventário de dados, avaliação de infraestrutura, review de ferramentas
- Benchmark: comparar com dados de mercado (Gartner, McKinsey surveys)

### Passo 3: Analisar e Pontuar (1-2 semanas)

- Consolidar dados quantitativos e qualitativos
- Pontuar cada dimensão no Readiness Scorecard
- Identificar gaps críticos (bloqueadores para AI)
- Mapear na matriz Readiness vs Ambição
- Identificar quick wins (melhorias de alto impacto e baixo esforço)

### Passo 4: Construir Roadmap de Readiness (1-2 semanas)

- Para cada gap crítico: ação, owner, timeline, investimento
- Priorizar: o que precisa ser resolvido ANTES de iniciar AI vs em PARALELO
- Quick wins (0-3 meses): ex: data catalog, AI literacy training
- Fundação (3-12 meses): ex: data platform, ML infrastructure
- Maturidade (12-24 meses): ex: MLOps, governance completa

### Passo 5: Apresentar e Alinhar (1 semana)

- Relatório executivo com scorecard e roadmap
- Apresentar para C-suite/board com recomendações claras
- Alinhar investimento necessário em fundação vs AI
- Definir cadência de re-assessment (anual ou semestral)

### Passo 6: Re-Assessment (anual)

- Repetir assessment com mesma metodologia
- Comparar com baseline (progresso real vs esperado)
- Ajustar roadmap baseado em resultados e mudanças de contexto
- Celebrar avanços e recalibrar ambição

## Exemplos Práticos

### Exemplo 1: Assessment de Scale-up (300 funcionários)

| Dimensão | Score | Diagnóstico | Ação Prioritária |
|----------|-------|-------------|------------------|
| Dados | 2.5 | Dados em silos, sem catálogo, qualidade inconsistente | Data platform + catalog |
| Tecnologia | 3.0 | Cloud ok, sem ML tools, sem GPU | ML platform (managed) |
| Talento | 1.5 | 1 data analyst, nenhum ML engineer | Contratar ML lead + 2 engineers |
| Estratégia | 2.0 | CEO quer AI, sem plano concreto | AI Strategy workshop |
| Cultura | 3.5 | Data-driven, aberta a experimentação | Manter, fortalecer |
| Governança | 1.0 | Nada definido para AI | AI Use Policy v1.0 |
| **Overall** | **2.3** | **"Prepare First"** | **Investir em fundação 6 meses antes de AI** |

### Exemplo 2: Progresso de Readiness (12 meses)

| Dimensão | Mês 0 | Mês 6 | Mês 12 | Δ |
|----------|-------|-------|--------|---|
| Dados | 2.5 | 3.5 | 4.0 | +1.5 |
| Tecnologia | 3.0 | 3.5 | 4.0 | +1.0 |
| Talento | 1.5 | 3.0 | 3.5 | +2.0 |
| Estratégia | 2.0 | 3.5 | 4.0 | +2.0 |
| Cultura | 3.5 | 4.0 | 4.0 | +0.5 |
| Governança | 1.0 | 2.5 | 3.5 | +2.5 |
| **Overall** | **2.3** | **3.3** | **3.8** | **+1.5** |

Investimento em readiness: R$ 1.5M (contratação + infra + consultoria)
Resultado: 3 modelos em produção ao final do ano, gerando R$ 2M em valor.

## Armadilhas Comuns

1. **Analysis paralysis**: Assessment eterno sem iniciar nada. Assessment é meio, não fim.
2. **Over-stating readiness**: Pontuar alto por otimismo ou política; seja brutalmente honesto.
3. **Ignorar cultura**: Dados e tech OK mas cultura resiste a AI = falha na adoção.
4. **Assessment sem ação**: Relatório bonito que ninguém usa para decidir investimento.
5. **Esperar 100% pronto**: Nenhuma organização está 100% pronta; comece com o que é possível.
6. **Foco só em dados e tech**: Talento, estratégia e cultura são igualmente importantes.
7. **One-time assessment**: O mundo muda; reassess regularmente.
8. **Benchmark errado**: Comparar com Google/Amazon é irrelevante; compare com peers realistas.
9. **Não envolver negócio**: Assessment só com TI perde a perspectiva de valor.
10. **Confundir readiness com maturidade**: Readiness é "podemos começar?"; maturidade é "quão avançados estamos?".

## Integração com Outros Frameworks

- **`frameworks/ai/ai-strategy.md`**: Assessment como input para definir estratégia
- **`frameworks/ai/adoption-playbook.md`**: Readiness determina em qual fase começar
- **`frameworks/caio-architect/ai-maturity-model.md`**: Maturidade como evolução de readiness
- **`frameworks/caio-architect/caio-ai-portfolio-strategy.md`**: Readiness informa viabilidade do portfólio
- **`frameworks/cio-engineer/data-platform.md`**: Data platform como pilar de readiness
- **`frameworks/cio-engineer/cio-data-as-product.md`**: Data products como indicador de maturidade de dados
- **`frameworks/shared/change-leadership.md`**: Readiness cultural como desafio de change

## Referências

- Google Cloud — "AI Adoption Framework" (readiness assessment component)
- McKinsey — "AI Readiness Assessment" (survey global)
- MIT Sloan — "Artificial Intelligence: The Insights You Need from Harvard Business Review"
- Gartner — "AI Maturity Model"
- Microsoft — "AI Business School" (readiness modules)
- Andrew Ng — "AI Transformation Playbook" (readiness steps)
- PwC — "AI Predictions" (readiness benchmarks por indústria)
