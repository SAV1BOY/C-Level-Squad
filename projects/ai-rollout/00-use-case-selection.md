# AI Rollout — Fase 00: Seleção de Use Case

## Objetivo desta Fase

Identificar, avaliar e priorizar os use cases de inteligência artificial com maior
potencial de impacto e viabilidade para a organização. Esta fase evita o erro comum
de implementar AI por moda tecnológica, garantindo que cada investimento em AI está
ligado a um problema de negócio real com ROI mensurável. A seleção criteriosa do
primeiro use case é determinante para o sucesso de toda a estratégia de AI da empresa.

## Agentes Envolvidos

- **CTO Agent**: Lidera a avaliação técnica de viabilidade dos use cases
- **CEO Agent**: Define prioridades estratégicas e alinhamento com a visão
- **COO Agent**: Identifica use cases operacionais e avalia impacto nos processos
- **CFO Agent**: Avalia ROI potencial e define envelope de investimento
- **CMO Agent**: Identifica use cases de marketing, vendas e customer experience
- **CHRO Agent**: Avalia impacto nas pessoas e necessidades de upskilling
- **Chief of Staff Agent**: Facilita o processo de seleção e documenta decisões

## Inputs Necessários

1. Estratégia da empresa e prioridades atuais
2. Inventário de pain points operacionais por departamento
3. Mapa de processos com métricas de eficiência atuais
4. Inventário de dados disponíveis (qualidade, volume, acessibilidade)
5. Benchmark de AI no setor (concorrentes, tendências, casos de sucesso)
6. Budget disponível para investimento em AI
7. Capacidades técnicas internas (equipa de dados, infraestrutura ML)

## Processo (step-by-step)

1. **Pain point inventory**: Cada agente lista os top 5 pain points da sua área que
   poderiam beneficiar de soluções baseadas em AI, incluindo impacto estimado
2. **Use case brainstorming**: Chief of Staff Agent facilita sessão estruturada onde
   os pain points são transformados em use cases concretos com descrição, benefício
   esperado e complexidade estimada
3. **Technical feasibility assessment**: CTO Agent avalia cada use case quanto a
   viabilidade técnica, maturidade da tecnologia e dados necessários vs disponíveis
4. **Data readiness pre-check**: CTO Agent faz uma avaliação rápida da qualidade e
   disponibilidade dos dados necessários para cada use case
5. **Business impact scoring**: CFO Agent e CEO Agent pontuam cada use case quanto
   ao impacto financeiro e alinhamento estratégico
6. **Risk assessment**: Todos os agentes avaliam riscos de cada use case incluindo
   riscos éticos, regulatórios, técnicos e organizacionais
7. **Prioritization matrix**: Chief of Staff Agent consolida as avaliações numa matriz
   de impacto vs viabilidade, facilitando a priorização visual
8. **Selection decision**: CEO Agent lidera a decisão de selecionar 1-3 use cases
   para avançar, equilibrando quick wins com iniciativas transformacionais
9. **Use case charter**: Chief of Staff Agent documenta cada use case selecionado
   com escopo, objetivos, métricas de sucesso e owner designado

## Outputs / Entregáveis

- **Use Case Inventory**: Lista completa de use cases identificados e avaliados
- **Feasibility Assessment**: Avaliação técnica de viabilidade por use case
- **Impact-Feasibility Matrix**: Matriz visual de priorização
- **Selected Use Case Charters**: Documento detalhado de cada use case selecionado
- **Data Readiness Pre-Assessment**: Avaliação preliminar de dados necessários
- **AI Investment Budget**: Envelope de investimento aprovado para AI
- **Risk and Ethics Assessment**: Avaliação de riscos éticos e regulatórios

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-00.1 | Pelo menos 10 use cases avaliados antes da seleção | Chief of Staff |
| QG-00.2 | Viabilidade técnica validada para cada use case selecionado | CTO Agent |
| QG-00.3 | ROI estimado com pressupostos documentados | CFO Agent |
| QG-00.4 | Riscos éticos e de bias avaliados explicitamente | CEO Agent |
| QG-00.5 | Dados necessários identificados com assessment de disponibilidade | CTO Agent |
| QG-00.6 | Impacto nas pessoas avaliado com plano de change management | CHRO Agent |

## Critérios para Avançar

Para progredir para a Fase 01 (Data Readiness), todos os critérios devem ser satisfeitos:

- [ ] 1-3 use cases selecionados e priorizados
- [ ] Use case charters documentados com métricas de sucesso claras
- [ ] Viabilidade técnica confirmada preliminarmente pelo CTO Agent
- [ ] Budget aprovado pelo CFO Agent para a fase seguinte
- [ ] Riscos éticos e regulatórios avaliados sem bloqueadores
- [ ] Owner designado para cada use case selecionado

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Selecionar use case por hype em vez de impacto real | Alta | Alto | Exigir business case quantificado para cada use case |
| Use case tecnicamente inviável com dados atuais | Média | Alto | CTO Agent faz pre-check de dados antes da seleção |
| Expectativas irrealistas sobre o que AI pode fazer | Alta | Médio | Sessão educativa sobre capacidades e limitações de AI |
| Resistência organizacional à adoção de AI | Média | Alto | CHRO Agent lidera comunicação e change management |
| Riscos regulatórios não identificados (GDPR, AI Act) | Média | Crítico | Revisão legal obrigatória antes da seleção final |

## Templates a Usar

- `templates/ai-use-case-canvas.md` — Canvas de use case de AI
- `templates/feasibility-assessment.md` — Template de avaliação de viabilidade
- `templates/impact-feasibility-matrix.md` — Matriz de priorização
- `templates/ai-ethics-checklist.md` — Checklist de ética em AI

## Duração Estimada

- **Mínimo**: 3 dias úteis (organização pequena com poucos processos)
- **Típico**: 5-10 dias úteis
- **Máximo**: 15 dias úteis (organização grande com muitos processos candidatos)

> **Nota**: A seleção do primeiro use case de AI é a decisão mais consequencial de toda
> a estratégia de AI. Um primeiro sucesso cria momentum e buy-in organizacional. Um
> primeiro fracasso pode atrasar a adoção de AI em anos.
