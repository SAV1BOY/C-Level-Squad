# Nova Iniciativa — Fase 03: Plano de Execução

## Objetivo desta Fase

Converter o design aprovado num plano de execução detalhado, com milestones, owners,
dependências, orçamento detalhado e cronograma realista. O plano deve ser suficientemente
granular para permitir tracking semanal de progresso, mas deve preservar flexibilidade
para adaptação durante a execução. Esta fase cria o "contrato de execução" entre todos
os agentes envolvidos.

## Agentes Envolvidos

- **COO Agent**: Lidera o planeamento operacional e define a estrutura de governance
- **CEO Agent**: Aprova milestones estratégicos e critérios de sucesso finais
- **CFO Agent**: Detalha o orçamento por fase e define controles financeiros
- **CTO Agent**: Planeia sprints técnicos e define dependências tecnológicas
- **CMO Agent**: Planeia atividades de go-to-market alinhadas com milestones técnicos
- **CHRO Agent**: Finaliza plano de staffing e onboarding de novos recursos
- **Chief of Staff Agent**: Consolida o plano integrado e configura ferramentas de tracking

## Inputs Necessários

1. Design completo aprovado (outputs da Fase 02)
2. Modelo financeiro refinado com custos detalhados
3. Inventário de recursos disponíveis e comprometidos
4. Calendário corporativo (feriados, outros projetos em curso, blackout periods)
5. SLAs de fornecedores e parceiros externos
6. Lições aprendidas de projetos anteriores similares
7. Risk register atualizado com riscos do design

## Processo (step-by-step)

1. **Work Breakdown Structure (WBS)**: COO Agent decompõe o design em work packages
   gerenciáveis, cada um com escopo, owner e critério de conclusão claros
2. **Dependency mapping**: CTO Agent e COO Agent mapeiam todas as dependências entre
   work packages, identificando o critical path do projeto
3. **Resource allocation**: CHRO Agent e COO Agent alocam recursos a cada work package,
   garantindo que não há conflitos de alocação com outros projetos
4. **Budget breakdown**: CFO Agent distribui o orçamento por work package e por mês,
   criando o baseline financeiro para controle de custos
5. **Sprint planning**: CTO Agent organiza os work packages técnicos em sprints de
   2 semanas, definindo deliverables por sprint
6. **GTM timeline**: CMO Agent alinha atividades de marketing e comunicação com os
   milestones técnicos, garantindo sincronização
7. **Risk response planning**: Todos os agentes definem planos de resposta para os
   riscos prioritários, incluindo triggers e ações específicas
8. **Governance setup**: COO Agent define a cadência de reuniões, reporting structure,
   escalation paths e mecanismos de decisão
9. **Baseline e aprovação**: Chief of Staff Agent consolida o plano final, estabelece
   o baseline e obtém aprovação formal de todos os agentes

## Outputs / Entregáveis

- **Execution Plan Document**: Plano integrado com WBS, timeline e milestones
- **Gantt Chart / Roadmap**: Visualização temporal do projeto com dependências
- **Budget Baseline**: Orçamento detalhado por work package e por período
- **RACI Matrix**: Matriz de responsabilidades para cada deliverable
- **Risk Response Plan**: Plano de resposta para os top 10 riscos
- **Governance Charter**: Documento com cadência de reuniões e processos de decisão
- **Communication Plan**: Plano de comunicação para stakeholders internos e externos

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-03.1 | WBS completa com todos os work packages estimados | COO Agent |
| QG-03.2 | Critical path identificado e validado | CTO Agent |
| QG-03.3 | Orçamento detalhado dentro de 5% do envelope aprovado | CFO Agent |
| QG-03.4 | Todos os recursos alocados e confirmados | CHRO Agent |
| QG-03.5 | Riscos top 10 com planos de resposta definidos | COO Agent |
| QG-03.6 | RACI matrix completa sem gaps ou conflitos | Chief of Staff |

## Critérios para Avançar

Para progredir para a Fase 04 (Launch), todos os critérios devem ser satisfeitos:

- [ ] Plano de execução aprovado por todos os agentes
- [ ] Orçamento baseline estabelecido e aprovado pelo CFO Agent
- [ ] Todos os recursos confirmados e disponíveis na data de início
- [ ] Governance charter assinado por todos os participantes
- [ ] Ferramentas de tracking configuradas e acessíveis
- [ ] Kickoff meeting agendado com toda a equipa

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Estimativas demasiado otimistas | Alta | Alto | Aplicar buffer de 20% em todas as estimativas |
| Conflitos de alocação de recursos | Alta | Crítico | Validar disponibilidade com CHRO antes de alocar |
| Dependências externas com timelines incertas | Média | Alto | Incluir contingência no critical path |
| Plano demasiado rígido sem margem para adaptação | Média | Médio | Reservar 15% do tempo para adaptação |
| Falta de buy-in da equipa de execução | Baixa | Alto | Envolver equipa no planeamento desde o início |

## Templates a Usar

- `templates/execution-plan.md` — Template do plano de execução integrado
- `templates/raci-matrix.md` — Matriz RACI para atribuição de responsabilidades
- `templates/governance-charter.md` — Modelo de governance charter
- `templates/communication-plan.md` — Plano de comunicação estruturado

## Duração Estimada

- **Mínimo**: 3 dias úteis (para projetos pequenos com equipa experiente)
- **Típico**: 5-10 dias úteis
- **Máximo**: 15 dias úteis (para projetos complexos multi-equipa)

> **Nota**: Um bom plano de execução é aquele que a equipa consegue seguir e adaptar.
> Se o plano for demasiado complexo para ser compreendido por todos, deve ser simplificado.
