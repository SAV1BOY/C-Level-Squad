# Market Thesis Update

## Objetivo
Atualizar a tese de mercado da empresa com base em evidências recentes, validando ou invalidando as premissas estratégicas fundamentais. A market thesis é o foundation sobre o qual todas as decisões estratégicas são construídas — se a thesis estiver errada, a estratégia inteira está em risco.

## Agente Responsável
- **CEO Agent** — Ownership da market thesis e premissas estratégicas

## Agentes de Suporte
- **CFO Agent** — Dados financeiros de mercado e unit economics benchmarks
- **CTO Agent** — Technology trends e viabilidade técnica de mudanças
- **CPO Agent** — Customer insights e product-market fit signals
- **CMO Agent** — Market intelligence, competitive data e demand signals
- **CAI Agent** — AI-driven market analysis e trend detection

## Pré-requisitos
1. Market thesis anterior documentada com premissas explícitas
2. Dados de mercado atualizados (TAM, SAM, SOM)
3. Competitive intelligence recente (últimos 30-60 dias)
4. Customer data: win/loss analysis, churn reasons, expansion drivers
5. Macroeconomic data relevante para o setor
6. Technology trend reports de fontes confiáveis
7. Regulatory updates que impactam o mercado

## Processo (step-by-step)

### Fase 1: Evidence Collection (2-3 dias)
1. Revisar a market thesis atual e listar todas as premissas explícitas
2. Para cada premissa, definir: que evidência confirmaria ou invalidaria
3. Coletar dados quantitativos de mercado: tamanho, growth rate, segmentation
4. Analisar movimentos competitivos dos últimos 90 dias: funding, launches, pivots, M&A
5. Compilar customer signals: win rates, deal sizes, sales cycle, churn patterns
6. Mapear technology shifts relevantes: novos enablers, disruptions, standards
7. Identificar regulatory changes que afetam dinâmica do mercado

### Fase 2: Premise Validation (2-3 dias)
8. Para cada premissa da thesis, classificar como: confirmada, questionada ou invalidada
9. Documentar evidência específica que suporta cada classificação
10. Identificar novas premissas que emergiram dos dados e não estavam na thesis anterior
11. Calcular o "confidence score" (0-100%) para cada premissa
12. Executar red team exercise: tentar invalidar as premissas mais críticas
13. Consultar fontes externas (analysts, advisors, customers) para triangular evidências

### Fase 3: Thesis Refinement (1-2 dias)
14. Reescrever a market thesis incorporando novos dados e premissas atualizadas
15. Atualizar TAM/SAM/SOM com dados mais recentes
16. Refinar a segmentação de mercado se necessário
17. Atualizar o competitive positioning map
18. Documentar "what would have to be true" para a thesis estar certa
19. Identificar leading indicators que sinalizariam mudança na thesis

### Fase 4: Implications e Recommendations (1 dia)
20. Documentar implicações estratégicas das mudanças na thesis
21. Recomendar ajustes nas strategic bets se necessário
22. Identificar novas oportunidades reveladas pela análise
23. Sinalizar ameaças emergentes que requerem ação
24. Definir triggers que demandariam revisão antecipada da thesis

## Frameworks a Aplicar
- **Premise Mapping** — Tornar explícitas todas as premissas implícitas na estratégia
- **Evidence-Based Strategy** — Classificar cada premissa por nível de evidência
- **Jobs-to-be-Done (JTBD)** — Revalidar o job principal que o mercado está contratando
- **Five Forces (Porter)** — Analisar mudanças nas forças competitivas do mercado
- **Value Chain Analysis** — Mapear onde o valor está sendo criado e capturado
- **Technology S-Curve** — Identificar onde estamos na curva de adoção tecnológica
- **TAM/SAM/SOM Analysis** — Quantificar oportunidade de mercado atualizada

## Checklists de Qualidade
- [ ] Todas as premissas da thesis anterior revisadas e classificadas
- [ ] Evidência específica documentada para cada premissa
- [ ] Confidence score atribuído a cada premissa (0-100%)
- [ ] Red team exercise executado nas premissas críticas
- [ ] TAM/SAM/SOM atualizados com fontes citadas
- [ ] Competitive positioning map atualizado
- [ ] Implicações estratégicas documentadas
- [ ] Leading indicators definidos para monitoramento contínuo
- [ ] Triggers de revisão antecipada estabelecidos
- [ ] Novas oportunidades e ameaças catalogadas

## Template de Entrega
```markdown
# Market Thesis — [Date]

## Thesis Statement
[Declaração de 2-3 parágrafos sobre nossa visão do mercado]

## Key Premises
| # | Premise | Status | Confidence | Evidence |
|---|---------|--------|------------|----------|
| 1 | [Premissa] | Confirmed/Questioned/Invalidated | [X%] | [Resumo da evidência] |

## Market Sizing
- **TAM:** [Value] — [Source, Date]
- **SAM:** [Value] — [Methodology]
- **SOM:** [Value] — [Assumptions]
- **Growth Rate:** [X% CAGR] — [Source]

## Competitive Landscape
| Competitor | Positioning | Recent Moves | Threat Level |
|-----------|-------------|--------------|--------------|

## Customer Signals
- **Win Rate Trend:** [Improving/Stable/Declining]
- **Avg Deal Size Trend:** [Direction]
- **Churn Rate Trend:** [Direction]
- **NPS Trend:** [Direction]

## Technology Trends
| Trend | Impact on Us | Timeline | Action Required |
|-------|-------------|----------|-----------------|

## What Would Have to Be True
1. [Premissa crítica 1]
2. [Premissa crítica 2]
3. [Premissa crítica 3]

## Strategic Implications
- [Implicação 1: ação recomendada]
- [Implicação 2: ação recomendada]

## Leading Indicators to Monitor
| Indicator | Current | Threshold | Action if Crossed |
|-----------|---------|-----------|-------------------|

## Revision Triggers
- [Trigger 1: condição que forçaria revisão antecipada]
- [Trigger 2: condição que forçaria revisão antecipada]
```

## Registries para Atualizar
- `registries/strategic-bets.md` — Ajustar bets se thesis mudou significativamente
- `registries/decisions-log.md` — Registrar insights e mudanças de premissas
- `registries/risk-register.md` — Adicionar riscos emergentes identificados
- `registries/competitive-intelligence.md` — Atualizar dados competitivos

## Critérios de Aceitação
1. Todas as premissas classificadas com evidência documentada
2. TAM/SAM/SOM atualizados com fontes verificáveis
3. Competitive landscape analysis completa e atual
4. Implicações estratégicas documentadas com ações recomendadas
5. Leading indicators definidos e monitoráveis
6. Apresentação para C-Level team realizada
7. Thesis document publicado e acessível

## Dependências e Handoffs
- **Recebe de:** Customer Data (CPO), Financial Data (CFO), Competitive Intel (CMO)
- **Entrega para:** Strategic Bets Review, Quarterly Planning, Board Prep
- **Cadência:** Atualização trimestral, com revisão ad-hoc se triggers forem acionados
- **Escalation path:** Invalidação de premissa crítica escala imediatamente para CEO + Board
