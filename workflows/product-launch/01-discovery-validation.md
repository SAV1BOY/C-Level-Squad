# Workflow: Discovery e Validação

## Objetivo

Conduzir um processo estruturado de descoberta e validação de oportunidades de produto, garantindo que ideias sejam testadas com usuários reais antes de comprometer recursos de engenharia, reduzindo o risco de construir funcionalidades que não geram valor.

## Trigger

- Hipótese de produto identificada no planejamento estratégico
- Feedback recorrente de clientes (NPS, suporte, CS)
- Oportunidade de mercado identificada pelo time de Product
- Análise de dados revelando gap ou oportunidade
- Request de stakeholder executivo com justificativa de negócio

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Product Manager | **Responsible** — Conduz discovery, sintetiza insights |
| Product Designer | **Responsible** — Pesquisa com usuários, prototipagem |
| Tech Lead | **Consulted** — Viabilidade técnica e estimativas |
| Head de Produto | **Accountable** — Aprova investimento na oportunidade |
| Data Analyst | **Consulted** — Análise quantitativa de dados |
| Stakeholders de Negócio | **Informed** — Visibilidade sobre oportunidades em análise |

## Etapas do Workflow

### Etapa 1: Enquadramento do Problema (Problem Framing)
- Documentar a oportunidade no formato: "Como podemos [objetivo] para [persona] que [contexto/dor]?"
- Levantar evidências existentes: dados de produto, feedback, benchmarks
- Definir hipóteses a serem validadas (máximo 3 hipóteses por ciclo)
- Mapear riscos: valor (os usuários querem?), usabilidade (conseguem usar?), viabilidade (conseguimos construir?), negócio (faz sentido financeiramente?)
- **SLA: 3 dias úteis**

### Etapa 2: Pesquisa Qualitativa
- Recrutar 5-8 usuários representativos do segmento-alvo
- Conduzir entrevistas de descoberta (45-60 min cada)
- Roteiro semi-estruturado focado em jobs-to-be-done
- Técnicas: entrevistas em profundidade, contextual inquiry, diary studies
- Sintetizar achados em mapa de afinidade ou jobs map
- **SLA: 2 semanas**

### Etapa 3: Análise Quantitativa
- Data Analyst puxa métricas relevantes do produto atual
- Análise de funil, retenção, uso de features correlatas
- Sizing da oportunidade: TAM, SAM, SOM quando aplicável
- Benchmarking competitivo: como concorrentes endereçam o problema
- **SLA: 1 semana (paralelo à pesquisa qualitativa)**

### Etapa 4: Ideação e Prototipagem
- Workshop de ideação com PM, Designer e Tech Lead
- Gerar múltiplas soluções (divergir antes de convergir)
- Selecionar 2-3 conceitos mais promissores
- Designer cria protótipos de baixa/média fidelidade
- Tech Lead avalia viabilidade técnica de cada conceito
- **SLA: 1 semana**

### Etapa 5: Teste de Usabilidade
- Testar protótipos com 5-8 usuários (podem ser os mesmos da pesquisa)
- Tarefas estruturadas para validar fluxos principais
- Métricas: taxa de sucesso, tempo na tarefa, satisfação (SUS/CSAT)
- Iterar no protótipo conforme feedback
- Documentar decisões de design e trade-offs
- **SLA: 1-2 semanas**

### Etapa 6: Business Case e Go/No-Go
- PM consolida findings em documento de discovery
- Incluir: problema validado, solução proposta, estimativa de impacto, riscos, esforço estimado
- Apresentar para Head de Produto e stakeholders
- Decisão: Go (seguir para build) / Pivot (reframear) / Kill (não prosseguir)
- Se Go: priorizar no roadmap e iniciar planejamento de build
- **SLA: 1 semana**

## Outputs / Entregáveis

- Documento de discovery com síntese de pesquisa e validação
- Protótipo validado com usuários (link no Figma/InVision)
- Business case com métricas de impacto esperado
- Decisão de Go/No-Go documentada com justificativa
- Backlog inicial de épicos e user stories (se Go)
- Riscos identificados e mitigações propostas

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Ciclos de discovery concluídos no prazo | ≥ 80% | Trimestral |
| Taxa de Go vs Kill | 40-60% Go (sinal de rigor) | Trimestral |
| Usuários entrevistados por discovery | ≥ 5 | Por ciclo |
| Hipóteses validadas com dados | 100% | Por ciclo |
| Features lançadas com discovery prévio | ≥ 80% | Trimestral |
| Impacto realizado vs projetado no business case | ≥ 70% | Semestral |

## Anti-Padrões a Evitar

- Pular discovery e ir direto para build ("já sabemos o que o cliente quer")
- Discovery sem acesso a usuários reais (apenas stakeholders internos)
- Prototipar solução antes de entender o problema
- Business case sem métricas de sucesso definidas
- Discovery que dura mais de 6 semanas (analysis paralysis)

## Integração com Outros Workflows

- **02-build-phase.md**: Discoveries aprovadas (Go) alimentam a fase de build
- **OKR Cycle / 02-quarterly-planning.md**: Discoveries priorizadas alinhadas a OKRs
- **Tech Review / 01-rfc-submission.md**: Soluções com impacto arquitetural geram RFC
- **Budget Cycle / 02-department-submissions.md**: Discoveries de grande porte requerem alocação orçamentária
