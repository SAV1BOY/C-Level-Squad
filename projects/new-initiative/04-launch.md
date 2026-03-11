# Nova Iniciativa — Fase 04: Lançamento e Execução

## Objetivo desta Fase

Executar o plano aprovado, coordenando todas as workstreams em paralelo, monitorizando
progresso contra o baseline e tomando decisões rápidas quando surgem desvios ou bloqueios.
Esta é a fase onde o valor é efetivamente criado, e onde a disciplina de execução e a
capacidade de adaptação são mais críticas. O foco é entregar os milestones definidos
mantendo qualidade, custo e timeline dentro dos parâmetros acordados.

## Agentes Envolvidos

- **COO Agent**: Lidera a execução operacional diária e resolve bloqueios
- **CTO Agent**: Gere as sprints técnicas e garante qualidade do código e infraestrutura
- **CMO Agent**: Executa atividades de go-to-market sincronizadas com milestones técnicos
- **CFO Agent**: Monitoriza burn rate e forecast financeiro atualizado
- **CHRO Agent**: Garante onboarding de novos recursos e gestão de performance da equipa
- **CEO Agent**: Participa em decisões estratégicas e removes bloqueadores escalados
- **Chief of Staff Agent**: Produz reporting de progresso e facilita cerimónias de governance

## Inputs Necessários

1. Plano de execução aprovado e baseline estabelecido (output da Fase 03)
2. Equipa completa onboarded e operacional
3. Ferramentas e infraestrutura de desenvolvimento configuradas
4. Acessos e permissões necessários concedidos
5. Budget released e processos de procurement ativados
6. Contratos com fornecedores externos assinados
7. Canais de comunicação da equipa configurados

## Processo (step-by-step)

1. **Kickoff meeting**: CEO Agent abre o projeto formalmente, reforça a visão e
   importância da iniciativa para a organização. Todos os agentes apresentam os seus
   planos de execução respetivos
2. **Sprint execution (técnico)**: CTO Agent gere ciclos de 2 semanas com sprint planning,
   daily standups, sprint review e retrospetiva. Cada sprint entrega funcionalidade
   incremental testada e documentada
3. **Operational ramp-up**: COO Agent ativa processos operacionais progressivamente,
   começando com operação manual que será automatizada ao longo do tempo
4. **GTM execution**: CMO Agent executa campanhas de awareness, prepara materiais de
   venda e ativa canais de distribuição conforme o plano
5. **Financial monitoring**: CFO Agent produz relatório semanal de burn rate vs budget,
   forecast atualizado e alertas de desvio significativo (>10%)
6. **Weekly status review**: Chief of Staff Agent facilita reunião semanal com todos os
   agentes para revisão de progresso, identificação de bloqueios e decisões necessárias
7. **Monthly steering committee**: CEO Agent lidera revisão mensal de alto nível com
   avaliação de riscos, decisões estratégicas e ajustes ao plano se necessário
8. **Continuous quality assurance**: Cada agente é responsável por garantir a qualidade
   na sua área, com métricas de qualidade reportadas semanalmente
9. **Issue and risk management**: COO Agent gere o issue log e risk register, escalando
   para CEO Agent quando necessário conforme a governance charter

## Outputs / Entregáveis

- **Sprint Deliverables**: Funcionalidade incremental entregue a cada 2 semanas
- **Weekly Status Reports**: Relatório semanal de progresso por workstream
- **Monthly Steering Report**: Relatório mensal consolidado para steering committee
- **Financial Tracking Report**: Burn rate, forecast e variância vs budget
- **Updated Risk Register**: Risk register atualizado com novos riscos e status
- **Issue Log**: Registo de problemas com status de resolução
- **Change Log**: Registo de alterações ao plano baseline aprovadas

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-04.1 | Sprint deliverables passam acceptance criteria definidos | CTO Agent |
| QG-04.2 | Burn rate dentro de 110% do planeado | CFO Agent |
| QG-04.3 | Milestone review positiva a cada 30 dias | COO Agent |
| QG-04.4 | Issues críticos resolvidos em menos de 48 horas | COO Agent |
| QG-04.5 | Equipa mantém engagement score acima de 7/10 | CHRO Agent |
| QG-04.6 | GTM activities executadas conforme o plano (>85%) | CMO Agent |

## Critérios para Avançar

Para progredir para a Fase 05 (Measure), todos os critérios devem ser satisfeitos:

- [ ] Todos os milestones de lançamento alcançados (ou replaneados e aprovados)
- [ ] Produto/serviço em produção e acessível aos utilizadores finais
- [ ] Processos operacionais ativos e equipa de suporte operacional
- [ ] Métricas de monitorização configuradas e a reportar dados
- [ ] Burn rate acumulado dentro de 115% do orçamento baseline
- [ ] Handover formal da equipa de projeto para equipa de operação (se aplicável)

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Atrasos técnicos acumulados | Alta | Alto | Sprint buffer e scope negotiation contínua |
| Burnout da equipa | Média | Crítico | CHRO Agent monitoriza sinais; enforce work-life balance |
| Mudança de prioridades organizacionais | Média | Crítico | CEO Agent protege o projeto de distrações |
| Problemas de integração entre sistemas | Média | Alto | Integration testing contínuo desde sprint 1 |
| Stakeholder fatigue e perda de interesse | Média | Médio | Comunicação regular de quick wins e progresso |

## Templates a Usar

- `templates/sprint-report.md` — Template de relatório de sprint
- `templates/weekly-status.md` — Template de status semanal
- `templates/steering-report.md` — Template de relatório para steering committee
- `templates/change-request.md` — Template de pedido de alteração ao baseline

## Duração Estimada

- **Mínimo**: 4 semanas (para MVPs simples)
- **Típico**: 8-16 semanas
- **Máximo**: 24 semanas (para iniciativas complexas multi-fase)

> **Nota**: A execução deve ser gerida em ciclos curtos (sprints) para permitir
> adaptação rápida. Evitar "big bang" deployments sempre que possível.
