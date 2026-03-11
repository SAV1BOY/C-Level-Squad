# Workflow: Aprovação de Requisição de Vaga

## Objetivo

Garantir que toda nova posição aberta na organização passe por um processo estruturado de justificativa, análise de impacto orçamentário e aprovação hierárquica antes de iniciar o processo de recrutamento. Este workflow visa alinhar as contratações com a estratégia organizacional e assegurar o uso responsável dos recursos financeiros.

## Trigger (Gatilho)

- Gestor identifica necessidade de nova contratação (posição nova ou reposição).
- Aprovação automática de reposição em até 30 dias após desligamento (conforme política vigente).
- Solicitação originada a partir do planejamento de headcount aprovado no ciclo orçamentário.

## Participantes (RACI)

| Papel | Responsabilidade |
|---|---|
| Gestor Solicitante | **Responsible** — Preenche a requisição com justificativa detalhada |
| Business Partner de RH | **Accountable** — Valida aderência à estrutura organizacional |
| Controller / FP&A | **Consulted** — Analisa impacto orçamentário e disponibilidade de budget |
| VP / Diretor da Área | **Accountable** — Aprovação de primeiro nível |
| CFO | **Accountable** — Aprovação final para posições acima do nível gerencial ou fora do budget |
| CHRO | **Informed** — Visibilidade sobre pipeline de contratações |
| CEO | **Accountable** — Aprovação para posições de diretoria ou C-Level |

## Etapas do Workflow

### Etapa 1: Elaboração da Requisição
- Gestor preenche formulário de requisição no sistema de ATS ou HRIS.
- Campos obrigatórios: título da posição, área, nível hierárquico, justificativa de negócio, tipo (nova ou reposição), faixa salarial pretendida, modelo de trabalho (presencial/híbrido/remoto), data desejada de início.
- Gestor deve incluir descrição do cargo e competências essenciais.
- Prazo: até 2 dias úteis para preenchimento completo.

### Etapa 2: Validação pelo Business Partner de RH
- BP de RH revisa a requisição quanto à aderência à estrutura organizacional.
- Verifica se a posição está prevista no headcount plan aprovado.
- Analisa se a descrição de cargo está atualizada e alinhada com a arquitetura de cargos.
- Pode solicitar ajustes ao gestor antes de avançar.
- Prazo: até 2 dias úteis após submissão.

### Etapa 3: Análise de Impacto Orçamentário
- FP&A recebe a requisição e calcula o custo total da posição (salário + encargos + benefícios + equipamentos).
- Verifica disponibilidade orçamentária no centro de custo do solicitante.
- Classifica a requisição: dentro do budget aprovado, requer remanejamento ou requer aprovação extra.
- Emite parecer financeiro anexado à requisição.
- Prazo: até 3 dias úteis.

### Etapa 4: Aprovação de Primeiro Nível
- VP ou Diretor da área revisa a requisição com o parecer financeiro.
- Pode aprovar, reprovar ou solicitar mais informações.
- Para posições dentro do budget e abaixo de nível gerencial, esta aprovação é suficiente para prosseguir.
- Prazo: até 2 dias úteis.

### Etapa 5: Aprovação de Segundo Nível (quando aplicável)
- CFO aprova posições acima do nível gerencial ou que excedam o budget da área.
- CEO aprova posições de diretoria ou C-Level.
- Em caso de urgência comprovada, existe um fast-track com SLA de 24 horas.
- Prazo padrão: até 3 dias úteis.

### Etapa 6: Abertura Formal da Vaga
- Após todas as aprovações, o sistema libera a vaga para o time de Talent Acquisition.
- Requisição recebe número de controle único.
- SLA global do processo de aprovação: máximo de 10 dias úteis do início ao fim.

## Outputs / Entregáveis

- Requisição de vaga aprovada e numerada no sistema ATS.
- Parecer financeiro de impacto orçamentário documentado.
- Job description validada e publicável.
- Registro de aprovações com timestamps e responsáveis.
- Notificação automática para o time de Talent Acquisition iniciar o sourcing.

## Métricas de Sucesso

| Métrica | Meta |
|---|---|
| Tempo médio de aprovação (end-to-end) | ≤ 7 dias úteis |
| % de requisições aprovadas na primeira submissão (sem devolução) | ≥ 80% |
| % de requisições dentro do budget aprovado | ≥ 90% |
| % de requisições com job description completa na primeira submissão | ≥ 85% |
| Tempo de resposta por aprovador | ≤ 2 dias úteis |

## Integração com Outros Workflows

- **02-sourcing-pipeline.md** — Após aprovação, a requisição alimenta diretamente o pipeline de sourcing.
- **budget-cycle/01-planning-kickoff.md** — O headcount plan aprovado no ciclo orçamentário determina quais posições são pré-aprovadas.
- **okr-cycle/02-quarterly-planning.md** — Necessidades de contratação podem surgir do planejamento trimestral de OKRs.
- **change-management/01-impact-assessment.md** — Reestruturações organizacionais podem gerar requisições em lote.

## Exceções e Casos Especiais

- **Reposição emergencial**: Posições críticas (ex.: segurança, compliance) podem seguir fast-track com aprovação verbal seguida de formalização em 48h.
- **Posições temporárias ou PJ**: Seguem workflow simplificado com aprovação apenas do VP e FP&A.
- **Vagas confidenciais**: Tramitam com acesso restrito no sistema, visíveis apenas para os aprovadores e o CHRO.

## Ferramentas e Sistemas

- ATS (Applicant Tracking System) para registro e tramitação.
- HRIS para validação de estrutura organizacional.
- ERP Financeiro para consulta orçamentária.
- Slack/Teams para notificações e follow-ups de aprovação.
