# Lançamento de Produto — Fase 04: Launch Day

## Objetivo desta Fase

Executar o lançamento do produto no dia definido com coordenação precisa entre todas
as equipas, monitorização em tempo real e capacidade de resposta rápida a qualquer
incidente. O launch day é o culminar de semanas de preparação e o momento em que o
produto encontra o mercado pela primeira vez. A excelência na execução deste dia
define a primeira impressão dos clientes e o momentum inicial do produto.

## Agentes Envolvidos

- **CEO Agent**: Disponível para comunicações de alto nível e decisões críticas
- **CMO Agent**: Lidera a ativação de campanhas e monitoriza resposta do mercado
- **CTO Agent**: Lidera o war room técnico e monitoriza estabilidade dos sistemas
- **COO Agent**: Coordena operações de suporte e monitoriza experiência do cliente
- **CFO Agent**: Monitoriza métricas financeiras em tempo real (signups, conversões)
- **Chief of Staff Agent**: Coordena o war room central e comunicação entre equipas

## Inputs Necessários

1. Tech Readiness Report com go confirmado (output da Fase 02)
2. Ops Readiness Report com go confirmado (output da Fase 03)
3. GTM Plan com campanhas prontas para ativação (output da Fase 01)
4. War room configurado e canais de comunicação testados
5. Runbook do launch day com timeline hora-a-hora
6. Equipa completa em standby nos seus postos
7. Rollback plan testado e pronto para execução se necessário

## Processo (step-by-step)

1. **Pre-launch check (T-2h)**: Chief of Staff Agent convoca reunião rápida de 15 min
   com todos os agentes para confirmar go/no-go final. Cada agente confirma readiness
   na sua área com um simples "go" ou "no-go com razão"
2. **Technical deployment (T-1h)**: CTO Agent executa o deployment em produção seguindo
   o runbook, incluindo feature flags, database migrations e cache warmup
3. **Smoke testing (T-30min)**: CTO Agent e COO Agent executam smoke tests em produção
   para confirmar que o produto está funcional e acessível
4. **Campaign activation (T-0)**: CMO Agent ativa todas as campanhas de marketing
   simultaneamente: email blasts, social media posts, PR releases, paid ads
5. **Real-time monitoring (T+0 to T+4h)**: Todos os agentes monitorizam as suas
   métricas em tempo real no war room, reportando anomalias imediatamente
6. **First hour assessment (T+1h)**: Chief of Staff Agent facilita checkpoint rápido
   para avaliar primeiras métricas: traffic, signups, error rates, support tickets
7. **Support surge management**: COO Agent gere a equipa de suporte, escala recursos
   se necessário e garante tempos de resposta dentro dos SLAs
8. **Issue triage and resolution**: CTO Agent classifica e resolve issues técnicos
   conforme prioridade, comunicando status no war room central
9. **Stakeholder updates**: Chief of Staff Agent envia updates regulares (a cada 2h)
   para stakeholders que não estão no war room
10. **End-of-day assessment (T+8h)**: Todos os agentes participam num debrief do dia,
    avaliando métricas, issues e plano para os dias seguintes
11. **Post-launch monitoring (D+1 to D+7)**: Cadência reduzida de monitorização nos
    7 dias seguintes ao lançamento com daily standups de 15 minutos

## Outputs / Entregáveis

- **Launch Day Log**: Registo cronológico de todos os eventos do dia de lançamento
- **Real-time Metrics Report**: Métricas em tempo real capturadas durante o dia
- **Incident Log**: Registo de todos os incidentes com status de resolução
- **First Day Summary**: Resumo executivo do primeiro dia com métricas chave
- **First Week Report**: Relatório completo da primeira semana pós-lançamento
- **Customer Feedback Compilation**: Compilação de feedback inicial dos clientes
- **Lessons for Next Launch**: Notas rápidas sobre o que melhorar no próximo launch

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-04.1 | Deployment em produção sem rollback necessário | CTO Agent |
| QG-04.2 | Uptime >99.9% nas primeiras 24 horas | CTO Agent |
| QG-04.3 | Support response time dentro do SLA definido | COO Agent |
| QG-04.4 | Signups/conversões dentro de 50% do target do dia 1 | CMO Agent |
| QG-04.5 | Zero incidentes P0 não resolvidos nas primeiras 4 horas | CTO Agent |
| QG-04.6 | Todas as campanhas de marketing ativadas conforme plano | CMO Agent |

## Critérios para Avançar

Para progredir para a Fase 05 (Post-Launch Review), os seguintes critérios aplicam-se:

- [ ] Produto em produção e estável há pelo menos 7 dias
- [ ] Todos os incidentes P0 e P1 do lançamento resolvidos
- [ ] Métricas da primeira semana compiladas e disponíveis
- [ ] Feedback inicial de clientes recolhido e categorizado
- [ ] War room desativado e transição para operação normal concluída
- [ ] Equipa de suporte operando em cadência normal

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Sistema cai sob carga real de produção | Média | Crítico | Auto-scaling configurado; rollback plan pronto |
| Bug crítico descoberto por utilizadores reais | Alta | Alto | Equipa de engenharia em standby para hotfix |
| Campanhas de marketing não geram tráfego esperado | Média | Médio | Plano B de amplificação com budget adicional |
| Volume de support tickets excede capacidade | Média | Alto | Equipa de backup pré-identificada e em standby |
| Feedback negativo viral nas redes sociais | Baixa | Alto | Social media monitoring e response plan preparado |

## Templates a Usar

- `templates/launch-day-runbook.md` — Runbook hora-a-hora do launch day
- `templates/incident-report.md` — Template de relatório de incidente
- `templates/launch-day-summary.md` — Resumo executivo do dia de lançamento
- `templates/first-week-report.md` — Relatório da primeira semana

## Duração Estimada

- **Launch Day**: 1 dia (com extensão para 12-16 horas de monitorização ativa)
- **Post-launch monitoring intensivo**: 3-7 dias adicionais
- **Transição para operação normal**: 7-14 dias após o lançamento

> **Nota**: O launch day é um evento de equipa. Todos os agentes devem estar acessíveis
> e focados. Nenhuma outra prioridade deve competir com a atenção ao lançamento.
