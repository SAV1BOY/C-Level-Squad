# Workflow: Fase de Construção (Build Phase)

## Objetivo

Estruturar a fase de desenvolvimento de produto desde o planejamento de sprint até a entrega de código pronto para beta, garantindo qualidade técnica, alinhamento com requisitos validados no discovery e cadência previsível de entregas.

## Trigger

- Discovery aprovado com decisão de Go documentada
- Épicos e user stories priorizados no backlog
- Time de engenharia alocado e capacidade confirmada
- RFC aprovada (se aplicável para mudanças arquiteturais)

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Product Manager | **Accountable** — Define prioridades e aceita entregas |
| Tech Lead | **Responsible** — Lidera implementação técnica |
| Engenheiros | **Responsible** — Desenvolvem, testam e entregam código |
| Product Designer | **Consulted** — Suporte em UX durante desenvolvimento |
| QA Engineer | **Consulted** — Estratégia de testes e validação |
| Engineering Manager | **Informed** — Monitora capacidade e blockers |

## Etapas do Workflow

### Etapa 1: Planejamento da Build (Sprint 0)
- Refinamento técnico dos épicos aprovados no discovery
- Quebra de épicos em user stories com critérios de aceite
- Estimativa de esforço (story points ou t-shirt sizing)
- Identificação de dependências técnicas e riscos
- Definição de arquitetura e design técnico (se necessário, gera RFC)
- Acordo sobre Definition of Done (DoD)
- **SLA: 1 sprint (2 semanas)**

### Etapa 2: Desenvolvimento Iterativo (Sprints 1-N)
- Sprint planning: seleção de stories conforme capacidade e prioridade
- Daily standups: sincronização diária do time (15 min)
- Desenvolvimento com pair programming para funcionalidades complexas
- Code review obrigatório (mínimo 1 aprovação) antes de merge
- Testes unitários e de integração escritos junto com código
- Deploy contínuo para ambiente de staging
- **Cadência: sprints de 2 semanas**

### Etapa 3: Quality Assurance Contínuo
- QA testa stories concluídas no ambiente de staging
- Testes exploratórios para cenários não cobertos por automação
- Testes de regressão automatizados rodando no CI/CD
- Bugs classificados por severidade e corrigidos antes do release
- Critério: zero bugs P1/P2 abertos para avançar para beta
- **SLA: QA completo em até 2 dias após dev done**

### Etapa 4: Sprint Review e Demo
- PM e stakeholders assistem demo das entregas do sprint
- Feedback coletado e priorizado para sprints seguintes
- Ajustes de escopo documentados e comunicados
- Métricas de velocidade e burndown revisadas
- **Cadência: ao final de cada sprint**

### Etapa 5: Sprint Retrospectiva
- Time reflete sobre o que funcionou e o que melhorar
- Ações de melhoria definidas com dono e prazo
- Máximo 3 ações por retro para garantir execução
- Acompanhamento de ações da retro anterior
- **Cadência: ao final de cada sprint**

### Etapa 6: Feature Complete e Preparação para Beta
- Todas as stories do escopo mínimo entregues e testadas
- Feature flags configuradas para controle de rollout
- Documentação técnica atualizada (API docs, runbooks)
- Métricas de produto instrumentadas (analytics, logs)
- Plano de rollback documentado
- Aprovação do PM: funcionalidade pronta para beta
- **SLA: conforme roadmap acordado**

## Outputs / Entregáveis

- Código deployado e testado em staging
- Feature flags configuradas para controle gradual
- Documentação técnica completa (arquitetura, APIs, runbooks)
- Métricas e dashboards de monitoramento configurados
- Plano de rollback documentado e testado
- Release notes rascunhadas para comunicação

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Velocidade do time (story points) | Estável (±15%) | Por sprint |
| Taxa de bugs encontrados em staging | < 10% das stories | Por sprint |
| Cobertura de testes automatizados | ≥ 80% | Por sprint |
| Escopo entregue vs planejado | ≥ 85% | Por sprint |
| Lead time (story start → done) | ≤ 5 dias | Por sprint |
| Cycle time de code review | ≤ 24h | Semanal |

## Integração com Outros Workflows

- **01-discovery-validation.md**: Recebe requisitos validados e priorizados
- **03-beta-rollout.md**: Entrega funcionalidade pronta para beta
- **Tech Review / 01-rfc-submission.md**: Mudanças arquiteturais geram RFC
- **Tech Review / 04-implementation-gates.md**: Gates de qualidade durante build
