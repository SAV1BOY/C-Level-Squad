# Migração de Sistema — Fase 00: Brief de Migração

## Objetivo desta Fase

Definir o escopo, motivação e contexto da migração de sistema, identificando claramente
o sistema atual (as-is), o sistema alvo (to-be), os drivers da migração e os critérios
de sucesso. O brief de migração serve como documento fundacional que previne migrações
desnecessárias, mal dimensionadas ou sem business case claro. Migrar sistemas é uma das
atividades mais arriscadas em tecnologia — começar com clareza é fundamental.

## Agentes Envolvidos

- **CTO Agent**: Lidera a definição técnica da migração e avalia complexidade
- **CEO Agent**: Valida o alinhamento estratégico e aprova o investimento
- **CFO Agent**: Avalia o business case financeiro e custos de migração
- **COO Agent**: Identifica impacto operacional e requisitos de continuidade
- **CMO Agent**: Avalia impacto na experiência do cliente durante a migração
- **CHRO Agent**: Avalia necessidades de formação e impacto na equipa
- **Chief of Staff Agent**: Coordena o processo de briefing e documenta decisões

## Inputs Necessários

1. Inventário do sistema atual (funcionalidades, integrações, dados, utilizadores)
2. Pain points documentados do sistema atual
3. Requisitos para o novo sistema (funcionais e não-funcionais)
4. Análise de risco do sistema atual (end-of-life, security, performance)
5. Budget disponível para a migração
6. Restrições de timeline (contratos, compliance deadlines, market pressure)
7. Stakeholder map (quem usa o sistema e como)

## Processo (step-by-step)

1. **Migration driver articulation**: CEO Agent e CTO Agent articulam claramente porque
   a migração é necessária agora — razões técnicas, financeiras ou estratégicas
2. **Current system inventory**: CTO Agent documenta o sistema atual incluindo todas as
   funcionalidades, integrações, volumes de dados e número de utilizadores
3. **Pain point collection**: COO Agent recolhe pain points de todos os utilizadores
   do sistema, categorizando por severidade e frequência
4. **Target state vision**: CTO Agent define a visão do estado alvo, incluindo
   capacidades desejadas, performance targets e arquitetura de referência
5. **Business case development**: CFO Agent desenvolve o business case incluindo custos
   de migração, custos de operação do novo sistema e benefícios quantificados
6. **Impact assessment**: Cada agente avalia o impacto da migração na sua área:
   operações, clientes, equipa, finanças e tecnologia
7. **Risk preliminary assessment**: CTO Agent e COO Agent fazem uma avaliação
   preliminar de riscos, focando em data loss, downtime e integrations
8. **Timeline and scope definition**: Chief of Staff Agent consolida uma timeline
   macro com scope definido (big bang vs phased migration)
9. **Brief approval**: Todos os agentes revisam e aprovam o brief de migração

## Outputs / Entregáveis

- **Migration Brief Document**: Documento principal do brief de migração
- **Current System Inventory**: Inventário completo do sistema atual
- **Business Case**: Business case com custos, benefícios e ROI projetado
- **Target State Vision**: Visão do estado alvo da migração
- **Stakeholder Impact Map**: Mapa de impacto por stakeholder group
- **Preliminary Risk Assessment**: Avaliação preliminar de riscos
- **Migration Scope Statement**: Definição do escopo da migração (in/out)

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-00.1 | Drivers de migração articulados e validados com dados | CEO Agent |
| QG-00.2 | Sistema atual inventariado com todas as integrações mapeadas | CTO Agent |
| QG-00.3 | Business case positivo com payback period definido | CFO Agent |
| QG-00.4 | Impacto operacional avaliado com plano de continuidade | COO Agent |
| QG-00.5 | Riscos preliminares identificados sem bloqueadores absolutos | CTO Agent |
| QG-00.6 | Brief aprovado por todos os agentes | Chief of Staff |

## Critérios para Avançar

Para progredir para a Fase 01 (Audit Current), todos os critérios devem ser satisfeitos:

- [ ] Brief de migração aprovado por todos os agentes
- [ ] Business case positivo aprovado pelo CFO Agent
- [ ] Escopo da migração definido e acordado
- [ ] Timeline macro realista confirmada pelo CTO Agent
- [ ] Riscos preliminares sem bloqueadores absolutos
- [ ] Budget alocado para a fase de audit

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Migração motivada por moda tecnológica sem business case | Média | Alto | Exigir ROI quantificado antes de aprovar |
| Subestimar a complexidade do sistema atual | Alta | Crítico | Inventário detalhado antes de qualquer decisão |
| Scope creep incluindo "melhorias" além da migração | Alta | Alto | Separar claramente migração de melhorias |
| Stakeholders não compreendem o impacto da migração | Média | Médio | Comunicação proativa com exemplos concretos |
| Timeline irrealista imposta por deadlines externos | Média | Alto | Negociar scope se timeline é fixa |

## Templates a Usar

- `templates/migration-brief.md` — Template do brief de migração
- `templates/system-inventory.md` — Inventário de sistema
- `templates/migration-business-case.md` — Business case de migração
- `templates/stakeholder-impact-map.md` — Mapa de impacto em stakeholders

## Duração Estimada

- **Mínimo**: 3 dias úteis (para migrações simples e bem compreendidas)
- **Típico**: 5-10 dias úteis
- **Máximo**: 15 dias úteis (para sistemas complexos com muitas integrações)

> **Nota**: A melhor migração é aquela que não precisa de acontecer. Antes de iniciar,
> confirmar que a migração é realmente necessária e que não há alternativas mais simples.
