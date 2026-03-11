# Workflow: Production Readiness Review

## Objetivo

Garantir que novos serviços, funcionalidades críticas ou mudanças significativas de infraestrutura atendam a todos os requisitos de operabilidade, monitoramento, segurança e resiliência antes de serem expostos a tráfego de produção.

## Trigger

- Novo serviço pronto para deploy em produção pela primeira vez
- Migração de infraestrutura que afeta serviços existentes
- Feature com impacto em SLOs existentes
- Mudança de arquitetura aprovada no Architecture Council
- Pré-requisito para Gate 6 no workflow de implementation gates

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Tech Lead do Serviço | **Responsible** — Preenche checklist e apresenta review |
| SRE Lead | **Accountable** — Valida prontidão operacional |
| Security Engineer | **Consulted** — Valida aspectos de segurança |
| VP de Engenharia | **Informed** — Para serviços de alto impacto |
| On-call Engineer | **Informed** — Preparado para operar novo serviço |

## Checklist de Production Readiness

### Observabilidade
- [ ] Logging estruturado implementado (JSON, campos padronizados)
- [ ] Métricas de RED instrumentadas (Rate, Errors, Duration)
- [ ] Distributed tracing configurado (OpenTelemetry, Jaeger)
- [ ] Dashboards criados no Grafana/Datadog com métricas-chave
- [ ] Health check endpoint implementado e monitorado

### Alertas
- [ ] Alertas configurados para SLOs do serviço
- [ ] Alertas com severidade correta (P1-P4)
- [ ] Alertas testados (fire drill com alerta real)
- [ ] Routing de alertas para time correto no PagerDuty
- [ ] Runbook linkado a cada alerta

### Resiliência
- [ ] Circuit breakers configurados para dependências externas
- [ ] Retry com backoff exponencial implementado
- [ ] Timeouts definidos para todas as chamadas externas
- [ ] Graceful degradation para dependências não-críticas
- [ ] Rate limiting configurado para proteger o serviço

### Escalabilidade
- [ ] Auto-scaling configurado (HPA, ASG)
- [ ] Testes de carga executados simulando 2x volume esperado
- [ ] Connection pools dimensionados adequadamente
- [ ] Caching implementado para dados frequentemente acessados
- [ ] Queries de banco otimizadas e indexadas

### Segurança
- [ ] Autenticação e autorização implementadas
- [ ] Dados sensíveis encriptados em trânsito (TLS) e em repouso
- [ ] Secrets gerenciados via vault (não hardcoded)
- [ ] Scan de vulnerabilidades executado e limpo
- [ ] Princípio de menor privilégio aplicado

### Deploy e Rollback
- [ ] Pipeline de CI/CD configurado e testado
- [ ] Deploy automatizado (zero-downtime)
- [ ] Rollback testado e documentado
- [ ] Feature flags configuradas para controle gradual
- [ ] Canary deploy ou blue/green configurado

### Documentação
- [ ] Runbook operacional documentado
- [ ] Arquitetura documentada com diagramas atualizados
- [ ] API documentada (OpenAPI/Swagger)
- [ ] Dependências mapeadas (upstream e downstream)
- [ ] Procedimento de disaster recovery documentado

## Etapas do Workflow

### Etapa 1: Auto-Avaliação pelo Time
- Tech Lead preenche checklist completo com evidências
- Cada item: Atende / Não atende / N/A (com justificativa)
- Links para dashboards, alertas, runbooks como evidência
- Identificar itens que requerem waiver (exceção aprovada)
- **SLA: 3 dias úteis**

### Etapa 2: Review pelo SRE
- SRE Lead revisa checklist e evidências
- Valida que métricas e alertas estão funcionais
- Testa cenários de falha (chaos engineering se aplicável)
- Verifica runbooks com exercício prático
- **SLA: 3 dias úteis**

### Etapa 3: Sessão de Review (60 min)
- Tech Lead apresenta serviço e checklist preenchido
- SRE, Security e stakeholders questionam e validam
- Decisão: Approved / Approved with conditions / Not ready
- Conditions devem ter dono e prazo definidos
- **SLA: 1 sessão agendada em até 5 dias úteis**

### Etapa 4: Aprovação e Deploy
- Checklist aprovado registrado no repositório de production readiness
- Deploy para produção autorizado
- Monitoramento intensivo nas primeiras 48h
- SRE disponível para suporte durante estabilização
- **SLA: Deploy em até 3 dias úteis após aprovação**

## Outputs / Entregáveis

- Checklist de production readiness preenchido e aprovado
- Dashboards e alertas configurados e validados
- Runbook operacional publicado
- Registro de aprovação no repositório central
- Plano de rollback testado e documentado

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Serviços com production readiness completo | 100% | Contínua |
| Itens do checklist atendidos | ≥ 90% (waivers para o resto) | Por review |
| Incidentes em serviços recém-lançados (30 dias) | < 2 P2+ | Mensal |
| Tempo médio do review (submissão à aprovação) | ≤ 10 dias úteis | Mensal |
| Runbooks atualizados e válidos | 100% | Trimestral |

## Integração com Outros Workflows

- **04-implementation-gates.md**: Production readiness é Gate 6
- **03-architecture-council.md**: Council define padrões mínimos do checklist
- **Incident Response / 01-detection-triage.md**: Alertas do PRR alimentam triagem
- **Product Launch / 03-beta-rollout.md**: PRR obrigatório antes de beta em produção
