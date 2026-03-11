# Workflow: Review Pós-Lançamento

## Objetivo

Conduzir uma análise abrangente dos resultados do lançamento de produto, comparando outcomes reais com projeções do business case, identificando lições aprendidas e definindo próximos passos para otimização e iteração.

## Trigger

- 30 dias após o lançamento GA de produto ou funcionalidade
- Métricas de adoção e impacto estabilizadas
- Feedback inicial de clientes, vendas e suporte consolidado

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Product Manager | **Responsible** — Consolida dados e conduz review |
| Data Analyst | **Responsible** — Análise quantitativa de métricas |
| Head de Produto | **Accountable** — Aprova conclusões e próximos passos |
| Product Marketing | **Consulted** — Resultados de comunicação e GTM |
| Customer Success | **Consulted** — Feedback de clientes e churn |
| Engineering | **Consulted** — Estabilidade técnica e débito |
| Vendas | **Informed** — Impacto em pipeline e conversão |

## Etapas do Workflow

### Etapa 1: Coleta de Dados (L+25 a L+30)
- Extrair métricas de produto: adoção, engajamento, retenção, conversão
- Coletar dados financeiros: impacto em receita, custo de aquisição
- Compilar feedback qualitativo: NPS, reviews, tickets de suporte
- Levantar métricas técnicas: uptime, performance, incidentes
- Solicitar input de vendas, CS e suporte
- **SLA: 5 dias para coleta completa**

### Etapa 2: Análise Comparativa
- Comparar resultados reais vs projeções do business case
- Analisar métricas por segmento: plano, tamanho de empresa, região
- Identificar cohorts com melhor e pior performance
- Análise de funil: onde estão os maiores drop-offs
- Mapear correlação entre feature e métricas de negócio (receita, churn)
- **SLA: 1 semana**

### Etapa 3: Síntese de Insights
- Consolidar top 5 insights quantitativos e qualitativos
- Categorizar: o que superou expectativas, o que ficou abaixo, surpresas
- Identificar oportunidades de otimização de curto prazo
- Mapear gaps para features complementares
- **SLA: 3 dias**

### Etapa 4: Sessão de Review (90 min)
- Apresentação de resultados para stakeholders cross-funcionais
- Discussão aberta sobre learnings e próximos passos
- Definição de ações priorizadas: otimizações, iterações, pivots
- Alinhamento sobre investimento contínuo vs redirecionamento
- **SLA: Agendar até L+35 dias**

### Etapa 5: Documentação e Comunicação
- Publicar documento de post-launch review no repositório de produto
- Comunicar resultados para toda a empresa (resumo executivo)
- Atualizar roadmap com iterações aprovadas
- Arquivar learnings no knowledge base para referência futura
- **SLA: 3 dias após sessão de review**

### Etapa 6: Plano de Iteração
- Priorizar melhorias com base nos dados do review
- Incluir itens no backlog com contexto e métricas de sucesso
- Definir timeline para próxima rodada de discovery (se necessário)
- Agendar follow-up review em L+90 dias para métricas de longo prazo
- **SLA: 1 semana após review**

## Outputs / Entregáveis

- Documento de post-launch review publicado
- Comparativo de métricas reais vs projetadas
- Lista priorizada de otimizações e iterações
- Backlog atualizado com próximos passos
- Comunicação de resultados para a empresa
- Follow-up review agendado para L+90

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Reviews realizados no prazo (L+35) | 100% | Por lançamento |
| Métricas de adoção vs target | ≥ 70% do target | L+30 |
| Impacto em receita vs business case | ≥ 60% do projetado | L+90 |
| Ações de iteração executadas | ≥ 80% no quarter seguinte | Trimestral |
| NPS da funcionalidade | ≥ 40 | L+30 e L+90 |

## Integração com Outros Workflows

- **04-ga-launch.md**: Recebe dados e contexto do lançamento
- **01-discovery-validation.md**: Learnings alimentam novos ciclos de discovery
- **OKR Cycle / 04-mid-quarter-review.md**: Resultados de lançamento no mid-quarter review
- **Budget Cycle / 05-quarterly-reforecast.md**: Impacto financeiro atualiza reforecast
