# Workflow: Submissão de RFC (Request for Comments)

## Objetivo

Formalizar o processo de proposição de mudanças técnicas significativas através de documentos de RFC, garantindo que decisões arquiteturais e de engenharia sejam documentadas, revisadas por pares e aprovadas antes da implementação.

## Trigger

- Nova funcionalidade que impacta arquitetura existente
- Adoção de nova tecnologia, framework ou linguagem
- Mudança em padrões de integração entre serviços
- Migração de infraestrutura ou banco de dados
- Tech Lead ou engenheiro identifica necessidade de decisão técnica documentada

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Autor da RFC | **Responsible** — Redige, apresenta e itera no documento |
| Tech Lead da Área | **Accountable** — Garante qualidade técnica e completude |
| Reviewers (pares) | **Consulted** — Revisam e fornecem feedback técnico |
| Architecture Council | **Consulted** — Para RFCs de impacto cross-funcional |
| VP de Engenharia | **Informed** — Visibilidade sobre decisões técnicas relevantes |

## Classificação de RFCs

| Tipo | Escopo | Aprovação Necessária |
|------|--------|---------------------|
| **Small** | Impacto em 1 serviço, sem breaking changes | Tech Lead da área |
| **Medium** | Impacto em 2-3 serviços, mudança de interface | Tech Lead + 2 reviewers |
| **Large** | Cross-funcional, nova tecnologia, migração | Architecture Council |

## Etapas do Workflow

### Etapa 1: Elaboração da RFC
- Autor preenche template padrão de RFC
- Seções obrigatórias: contexto, problema, solução proposta, alternativas consideradas, riscos, plano de migração
- Incluir diagramas de arquitetura quando aplicável
- Estimar esforço de implementação em alto nível
- Publicar como draft para feedback informal
- **SLA: 3-5 dias úteis para primeira versão**

### Etapa 2: Período de Comentários
- RFC publicada em repositório central (GitHub, Confluence, Notion)
- Notificação enviada para stakeholders técnicos relevantes
- Período aberto para comentários e perguntas
- Autor responde a todos os comentários e atualiza RFC conforme necessário
- **SLA: 5 dias úteis para RFCs Small/Medium, 10 dias para Large**

### Etapa 3: Review Meeting (para Medium e Large)
- Reunião de 60 min com autor, reviewers e stakeholders
- Autor apresenta RFC (20 min) seguido de discussão (40 min)
- Identificar pontos de consenso e divergência
- Definir ações para resolver pontos em aberto
- **SLA: Agendada dentro do período de comentários**

### Etapa 4: Iteração e Finalização
- Autor incorpora feedback e resolve pontos em aberto
- Versão final publicada com changelog das alterações
- Reviewers confirmam que suas preocupações foram endereçadas
- **SLA: 3 dias úteis após review meeting**

### Etapa 5: Aprovação
- Aprovadores assinam conforme nível de classificação
- Status atualizado: Draft → In Review → Approved / Rejected / Deferred
- RFCs rejeitadas: documentar razões para referência futura
- RFCs deferidas: agendar re-review com timeline
- **SLA: 2 dias úteis após finalização**

### Etapa 6: Comunicação e Arquivamento
- RFC aprovada comunicada em canal de engenharia (#engineering-rfcs)
- Indexada no catálogo de decisões técnicas (ADR - Architecture Decision Records)
- Vinculada aos tickets de implementação no backlog
- Disponível para consulta futura como registro histórico
- **SLA: 1 dia útil após aprovação**

## Template da RFC

```
# RFC-[NÚMERO]: [Título]
## Metadata
- Autor:
- Status: Draft | In Review | Approved | Rejected | Deferred
- Classificação: Small | Medium | Large
- Data de criação:
- Data de decisão:

## Contexto
(Qual é o cenário atual e por que uma mudança é necessária?)

## Problema
(Qual problema específico estamos resolvendo?)

## Solução Proposta
(Descrição detalhada da solução técnica)

## Alternativas Consideradas
(Quais outras opções foram avaliadas e por que foram descartadas?)

## Riscos e Mitigações
(Quais riscos esta mudança introduz?)

## Plano de Implementação
(Como será a implementação? Fases? Rollback?)

## Métricas de Sucesso
(Como saberemos que deu certo?)
```

## Outputs / Entregáveis

- RFC documentada, aprovada e publicada
- Registro no catálogo de decisões arquiteturais (ADR)
- Tickets de implementação criados e vinculados à RFC
- Comunicação para engenharia sobre decisão tomada

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| RFCs resolvidas no prazo do período de comentários | ≥ 85% | Mensal |
| Decisões técnicas documentadas via RFC | ≥ 90% | Trimestral |
| Participação de reviewers (comentários por RFC) | ≥ 3 reviewers | Por RFC |
| RFCs que necessitaram revisão pós-implementação | < 15% | Trimestral |

## Integração com Outros Workflows

- **02-design-review.md**: RFCs complexas podem exigir design review separado
- **03-architecture-council.md**: RFCs Large são revisadas pelo council
- **Product Launch / 02-build-phase.md**: RFCs aprovadas habilitam implementação
- **Incident Response / 04-postmortem-process.md**: Postmortems podem gerar RFCs para mudanças estruturais
