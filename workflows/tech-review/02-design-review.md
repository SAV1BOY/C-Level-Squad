# Workflow: Design Review

## Objetivo

Avaliar soluções técnicas detalhadas antes da implementação, garantindo que o design atenda requisitos funcionais e não-funcionais, siga padrões da organização e seja viável dentro das restrições de prazo, custo e complexidade.

## Trigger

- RFC aprovada que requer design detalhado antes de implementação
- Novo serviço ou componente sendo projetado do zero
- Refatoração significativa de sistema existente
- Integração com sistema externo de alto impacto
- Solicitação do Tech Lead ou Architecture Council

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Engenheiro/Tech Lead autor | **Responsible** — Cria design doc e apresenta |
| Reviewers técnicos (2-3) | **Consulted** — Revisam e desafiam o design |
| Tech Lead da área | **Accountable** — Garante que design atende requisitos |
| SRE representante | **Consulted** — Valida aspectos de operabilidade |
| Product Manager | **Informed** — Visibilidade sobre trade-offs técnicos |

## Aspectos Avaliados no Design Review

### Funcionalidade
- O design atende todos os requisitos funcionais?
- Casos de borda e cenários de erro estão cobertos?
- Comportamento esperado está claramente definido?

### Escalabilidade e Performance
- O design suporta a carga esperada (10x do volume atual)?
- Pontos de contenção (bottlenecks) identificados e mitigados?
- Estratégia de caching definida quando aplicável?

### Confiabilidade e Resiliência
- Pontos únicos de falha (SPOF) eliminados?
- Estratégia de retry, circuit breaker e fallback definida?
- Plano de disaster recovery documentado?

### Segurança
- Autenticação e autorização adequadas?
- Dados sensíveis protegidos em trânsito e em repouso?
- Superfície de ataque minimizada?

### Operabilidade
- Logging, métricas e tracing instrumentados?
- Alertas definidos para cenários de falha?
- Runbooks de operação documentados?
- Deploy e rollback automatizados?

### Manutenibilidade
- Código testável e modular?
- Interfaces bem definidas entre componentes?
- Documentação suficiente para onboarding de novos engenheiros?

## Etapas do Workflow

### Etapa 1: Elaboração do Design Document
- Autor cria documento detalhado seguindo template
- Incluir diagramas: arquitetura, sequência, dados, deploy
- Documentar decisões e trade-offs explicitamente
- Estimar impacto em custo de infraestrutura
- **SLA: 5-10 dias úteis dependendo da complexidade**

### Etapa 2: Pre-Review Assíncrono
- Design doc compartilhado com reviewers para leitura prévia
- Reviewers adicionam comentários e perguntas no documento
- Autor endereça comentários simples antes da reunião
- Identificar temas para discussão síncrona
- **SLA: 3 dias úteis**

### Etapa 3: Sessão de Design Review
- Reunião presencial ou virtual (60-90 min)
- Autor walkthrough do design (30 min)
- Discussão focada nos pontos levantados (30-60 min)
- Resultado: Aprovado / Aprovado com condições / Necessita revisão
- **SLA: Agendada dentro de 1 semana após submissão**

### Etapa 4: Incorporação de Feedback
- Autor atualiza design doc com decisões da sessão
- Resolve todos os action items abertos
- Publica versão final para confirmação dos reviewers
- **SLA: 3 dias úteis**

### Etapa 5: Aprovação e Handoff para Implementação
- Reviewers confirmam que feedback foi endereçado
- Status atualizado para "Approved"
- Design doc vinculado aos tickets de implementação
- Comunicado para o time de engenharia
- **SLA: 2 dias úteis**

## Outputs / Entregáveis

- Design document aprovado e publicado
- Diagramas de arquitetura atualizados no repositório
- Action items resolvidos e documentados
- Tickets de implementação criados com referência ao design
- Estimativa de esforço refinada

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Design reviews concluídos no prazo | ≥ 85% | Mensal |
| Problemas encontrados em review (vs em produção) | ≥ 70% dos issues | Trimestral |
| Tempo médio de review (submissão à aprovação) | ≤ 10 dias úteis | Mensal |
| Designs que precisaram revisão após implementação | < 10% | Trimestral |
| Participação dos reviewers | ≥ 2 reviewers por doc | Por review |

## Integração com Outros Workflows

- **01-rfc-submission.md**: RFCs aprovadas geram design reviews quando necessário
- **03-architecture-council.md**: Designs cross-funcionais escalados para council
- **04-implementation-gates.md**: Design aprovado é gate para início de implementação
- **Product Launch / 02-build-phase.md**: Design precede Sprint 0 da build phase
