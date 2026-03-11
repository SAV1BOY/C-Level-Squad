# Workflow: General Availability Launch

## Objetivo

Coordenar o lançamento público de produto ou funcionalidade para todos os usuários, orquestrando comunicação, habilitação de vendas, suporte e monitoramento para maximizar impacto e minimizar riscos no dia do lançamento.

## Trigger

- Decisão de Go confirmada no beta review
- Rollout gradual concluído com sucesso (100% sem incidentes)
- Materiais de lançamento prontos e aprovados
- Data de lançamento definida e comunicada internamente

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Product Manager | **Accountable** — Coordena lançamento cross-funcional |
| Product Marketing | **Responsible** — Comunicação externa e posicionamento |
| Sales Enablement | **Responsible** — Treinamento e materiais para vendas |
| Customer Support | **Responsible** — Preparação para volume de tickets |
| Engineering | **Consulted** — Suporte técnico e monitoramento |
| VP de Produto | **Informed** — Aprovação final de mensagem e timing |

## Etapas do Workflow

### Etapa 1: Planejamento do Lançamento (L-30 dias)
- Definir tier do lançamento: Tier 1 (grande), Tier 2 (médio), Tier 3 (incremental)
- Montar GTM (Go-to-Market) brief: posicionamento, mensagens-chave, público-alvo
- Definir canais de comunicação por tier
- Alinhar com PR se houver interesse de imprensa
- Criar timeline reverso com todas as dependências e donos
- **SLA: Plan aprovado 30 dias antes do lançamento**

### Etapa 2: Preparação de Materiais (L-15 dias)
- Blog post anunciando a funcionalidade
- Atualização de página de produto no site
- Email de anúncio para base de clientes
- In-app notification ou banner
- Materiais de sales enablement (deck, one-pager, FAQ)
- Atualização de help center e documentação
- Vídeo demo ou tutorial (se Tier 1)
- **SLA: Materiais prontos e aprovados 7 dias antes**

### Etapa 3: Habilitação Interna (L-7 dias)
- Training session para time de vendas
- Briefing para Customer Success sobre impacto em clientes
- Treinamento de suporte com cenários e respostas
- Comunicação interna all-hands sobre o lançamento
- Dry run do plano de lançamento com todos os envolvidos
- **SLA: Todos os times habilitados 5 dias antes**

### Etapa 4: Dia do Lançamento (L-Day)
- War room de lançamento ativo com representantes de cada área
- Publicação coordenada: blog, email, in-app, redes sociais
- Monitoramento intensivo de métricas técnicas e de produto
- Suporte com equipe reforçada para as primeiras 24-48h
- Relatório de primeira hora: adoção, erros, feedback inicial
- **SLA: Todas as comunicações publicadas conforme timeline**

### Etapa 5: Primeira Semana Pós-Lançamento
- Monitorar adoção diariamente e comparar com projeção
- Responder a feedback de clientes rapidamente
- Corrigir bugs encontrados com prioridade máxima
- Atualizar FAQ com perguntas recorrentes
- Relatório diário para stakeholders (primeiros 5 dias)
- **SLA: Bug fixes em ≤ 24h para P1, ≤ 48h para P2**

### Etapa 6: Encerramento do Lançamento (L+14 dias)
- Consolidar métricas de lançamento vs targets
- Coletar feedback de vendas, CS e suporte
- Documentar lições aprendidas
- Transição de monitoramento intensivo para regular
- Handoff para time de sustentação

## Outputs / Entregáveis

- Materiais de comunicação publicados (blog, email, site)
- Materiais de sales enablement distribuídos
- Help center e documentação atualizados
- Relatório de lançamento com métricas consolidadas
- Lições aprendidas documentadas
- Handoff formal para sustentação

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Adoção na primeira semana | Conforme target por tier | Diária |
| Tickets de suporte relacionados | < 5% da base impactada | Diária |
| Bugs P1 no dia do lançamento | 0 | Diária |
| Cobertura de sales enablement | 100% do time treinado | Pré-launch |
| NPS da nova funcionalidade | ≥ 40 | L+30 dias |
| Impacto em receita (se aplicável) | Conforme business case | L+90 dias |

## Integração com Outros Workflows

- **03-beta-rollout.md**: Recebe funcionalidade validada no beta
- **05-post-launch-review.md**: Alimenta review pós-lançamento
- **Change Management / 03-communication-plan.md**: Plano de comunicação alinhado
- **OKR Cycle / 03-weekly-check-in.md**: Métricas de lançamento no check-in semanal
