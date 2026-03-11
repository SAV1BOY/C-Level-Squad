# Workflow: Beta e Rollout Gradual

## Objetivo

Validar funcionalidades em ambiente de produção com um grupo controlado de usuários antes do lançamento geral, coletando feedback real, identificando problemas e ajustando o produto para garantir uma experiência de alta qualidade no GA (General Availability).

## Trigger

- Feature complete confirmada pela equipe de engenharia
- Testes em staging concluídos com zero bugs P1/P2
- Plano de rollback documentado e testado
- Feature flags configuradas e prontas para ativação gradual

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Product Manager | **Accountable** — Define critérios de sucesso e decide go/no-go |
| Tech Lead | **Responsible** — Gerencia rollout técnico e monitoramento |
| Customer Success | **Responsible** — Recruta beta testers e coleta feedback |
| SRE / DevOps | **Consulted** — Monitora estabilidade e performance |
| Product Designer | **Consulted** — Analisa feedback de usabilidade |
| VP de Produto | **Informed** — Visibilidade sobre progresso do beta |

## Fases do Rollout Gradual

| Fase | Audiência | Percentual | Duração |
|------|-----------|-----------|---------|
| Alpha interno | Colaboradores, dogfooding | 100% interno | 1 semana |
| Beta fechado | Clientes selecionados, early adopters | 5-10% | 2 semanas |
| Beta aberto | Opt-in para qualquer cliente | 10-25% | 1-2 semanas |
| Rollout gradual | Expansão controlada | 25% → 50% → 100% | 1-2 semanas |

## Etapas do Workflow

### Etapa 1: Preparação do Beta
- Definir critérios de entrada no beta (stability gates)
- Selecionar cohort de beta testers (diversidade de perfis e use cases)
- Preparar canal de feedback (formulário, Slack, in-app)
- Configurar dashboards de monitoramento específicos do beta
- Preparar FAQ e documentação de suporte para beta testers
- Comunicar internamente o início do beta (CS, Suporte, Vendas)
- **SLA: 3 dias úteis**

### Etapa 2: Alpha Interno (Dogfooding)
- Ativar feature para todos os colaboradores via feature flag
- Time interno usa a funcionalidade no dia a dia
- Bugs e feedback reportados no canal dedicado
- Correções rápidas aplicadas antes de abrir para clientes
- **SLA: 1 semana**

### Etapa 3: Beta Fechado
- Ativar feature para cohort selecionada de clientes
- CS notifica beta testers com guia de uso e expectativas
- Monitorar métricas de adoção, erros e performance em tempo real
- Coletar feedback estruturado via survey e entrevistas
- Cadência de syncs: diários (primeira semana), depois a cada 2 dias
- **Critério de saída: ≥ 70% dos testers ativos, NPS ≥ 30, zero P1**

### Etapa 4: Beta Aberto
- Expandir acesso via opt-in no produto
- Monitorar métricas de escala (performance sob carga maior)
- Iterar em ajustes de UX baseado em feedback agregado
- Preparar documentação final e release notes
- **Critério de saída: métricas estáveis por 5 dias, CSAT ≥ 4.0**

### Etapa 5: Rollout Gradual (25% → 50% → 100%)
- Expandir progressivamente via feature flag
- Cada incremento mantido por mínimo 48h antes de avançar
- Monitorar: error rate, latência, métricas de negócio, tickets de suporte
- Rollback automático se error rate exceder threshold definido
- **Critério para avançar: métricas dentro do baseline em cada incremento**

### Etapa 6: Go/No-Go para GA
- PM consolida dados do beta: métricas, feedback, bugs restantes
- Reunião de Go/No-Go com stakeholders (PM, Tech Lead, CS, SRE)
- Decisão documentada com base em critérios objetivos
- Se Go: transição para workflow de GA Launch
- Se No-Go: plano de correção com novo timeline

## Outputs / Entregáveis

- Relatório de beta com métricas consolidadas
- Lista de bugs encontrados e status de correção
- Feedback qualitativo sintetizado de beta testers
- Decisão de Go/No-Go documentada
- Release notes finalizadas para GA
- Documentação de suporte atualizada

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Taxa de adoção no beta | ≥ 70% dos testers | Semanal |
| NPS de beta testers | ≥ 30 | Ao final do beta |
| Bugs P1/P2 encontrados em beta | Todos corrigidos antes de GA | Diária |
| Error rate em produção durante rollout | < 0.1% | Diária |
| Latência p95 | ≤ baseline + 10% | Diária |
| Rollbacks executados | 0 | Por rollout |

## Integração com Outros Workflows

- **02-build-phase.md**: Recebe feature pronta para beta
- **04-ga-launch.md**: Beta aprovado alimenta lançamento GA
- **Incident Response / 01-detection-triage.md**: Alertas configurados para beta
- **Tech Review / 05-production-readiness.md**: Checklist de produção validado antes do beta
