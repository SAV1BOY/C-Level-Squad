# Template: Runbook Operacional

## Propósito
Este template documenta procedimentos operacionais para sistemas em produção. Runbooks garantem que qualquer engenheiro de plantão possa diagnosticar e resolver incidentes seguindo passos claros, mesmo sem conhecimento profundo do sistema.

## Instruções de Uso
1. Crie um runbook para cada serviço/sistema crítico
2. Escreva para alguém que NUNCA viu o sistema — seja explícito
3. Teste o runbook com um engenheiro que não é do time
4. Revise a cada quarter ou após cada incidente que expõe gaps
5. Mantenha links e comandos atualizados — runbook desatualizado é pior que nenhum

---

## [Nome do Serviço/Sistema]

### Informações Gerais

| Campo | Valor |
|-------|-------|
| **Serviço** | [Nome do serviço] |
| **Time Responsável** | [Nome do time — canal Slack] |
| **Criticidade** | [P0 / P1 / P2 / P3] |
| **SLA** | [99.9% / 99.99% — tempo de resposta: Xms p99] |
| **Última Atualização** | [DD/MM/AAAA] |
| **Autor** | [Nome] |
| **Revisores** | [Nomes] |

### Arquitetura de Alto Nível

```
[Diagrama simplificado do serviço e dependências]

                    ┌─────────┐
  Clientes ────────▶│   LB    │
                    └────┬────┘
                         │
              ┌──────────┼──────────┐
              ▼          ▼          ▼
         ┌────────┐ ┌────────┐ ┌────────┐
         │ App 1  │ │ App 2  │ │ App 3  │
         └───┬────┘ └───┬────┘ └───┬────┘
             │          │          │
             ▼          ▼          ▼
         ┌──────────────────────────────┐
         │        PostgreSQL (RDS)       │
         └──────────────────────────────┘
```

### Links Importantes

| Recurso | URL |
|---------|-----|
| Dashboard principal | [URL do Grafana/Datadog] |
| Logs | [URL do Kibana/CloudWatch] |
| Alertas | [URL do PagerDuty/OpsGenie] |
| Repositório | [URL do GitHub/GitLab] |
| CI/CD Pipeline | [URL] |
| Configurações (feature flags) | [URL do LaunchDarkly/etc] |
| Status page | [URL] |

---

### Procedimentos de Diagnóstico

#### Passo 1: Verificar Status Geral
```bash
# Verificar health check do serviço
curl -s https://[servico].internal/health | jq .

# Verificar pods/instâncias rodando
kubectl get pods -n [namespace] -l app=[servico]

# Verificar métricas de erro recentes (últimos 30 min)
# [Comando ou link para query no Grafana/Datadog]
```

#### Passo 2: Identificar o Tipo de Problema
| Sintoma | Provável Causa | Ir Para |
|---------|---------------|---------|
| HTTP 5xx alto | Erro na aplicação | Seção: Erros de Aplicação |
| Latência alta | DB lento ou dependência | Seção: Problemas de Performance |
| Pods reiniciando | OOM ou crash loop | Seção: Problemas de Infraestrutura |
| Sem tráfego | DNS ou LB | Seção: Problemas de Rede |
| Dados inconsistentes | Falha em job/pipeline | Seção: Problemas de Dados |

---

### Cenários de Incidente

#### Cenário 1: Erros de Aplicação (5xx)

**Sintomas:** Taxa de erro > [X%], alertas de erro rate

**Diagnóstico:**
```bash
# 1. Verificar logs de erro recentes
kubectl logs -n [namespace] -l app=[servico] --tail=100 | grep ERROR

# 2. Verificar se houve deploy recente
kubectl rollout history deployment/[servico] -n [namespace]

# 3. Verificar dependências
curl -s https://[servico].internal/health/dependencies | jq .
```

**Resolução:**
- Se causado por deploy recente: executar rollback (ver Seção Rollback)
- Se causado por dependência: verificar status da dependência e acionar time responsável
- Se causado por dados: verificar logs para payload problemático

#### Cenário 2: Problemas de Performance

**Sintomas:** Latência p99 > [X ms], timeouts frequentes

**Diagnóstico:**
```bash
# 1. Verificar queries lentas no DB
# [Query para identificar slow queries — RDS/PostgreSQL]

# 2. Verificar uso de CPU/memória dos pods
kubectl top pods -n [namespace] -l app=[servico]

# 3. Verificar connection pool
# [Comando ou métrica para verificar conexões ao DB]
```

**Resolução:**
- Se DB lento: verificar se há lock contention, running queries, ou necessidade de índice
- Se CPU/memória alta: escalar horizontalmente (ver Seção Scaling)
- Se connection pool esgotado: reiniciar pods gradualmente

#### Cenário 3: Problemas de Infraestrutura

**Sintomas:** Pods em CrashLoopBackOff, OOMKilled

**Diagnóstico:**
```bash
# 1. Verificar status dos pods
kubectl describe pod [pod-name] -n [namespace]

# 2. Verificar eventos do cluster
kubectl get events -n [namespace] --sort-by='.lastTimestamp' | tail -20

# 3. Verificar uso de recursos do node
kubectl top nodes
```

**Resolução:**
- Se OOM: aumentar memory limits no deployment
- Se CrashLoop: verificar logs do container que está falhando
- Se node com problemas: drenar e substituir

---

### Procedimentos Operacionais

#### Rollback de Deploy
```bash
# 1. Identificar revisão anterior estável
kubectl rollout history deployment/[servico] -n [namespace]

# 2. Executar rollback
kubectl rollout undo deployment/[servico] -n [namespace]

# 3. Verificar que rollback completou
kubectl rollout status deployment/[servico] -n [namespace]

# 4. Confirmar que métricas normalizaram
# [Link para dashboard]
```

#### Scaling Manual
```bash
# Escalar horizontalmente
kubectl scale deployment/[servico] -n [namespace] --replicas=[N]

# Verificar que novos pods estão healthy
kubectl get pods -n [namespace] -l app=[servico] -w
```

#### Restart Graceful
```bash
# Restart rolling (sem downtime)
kubectl rollout restart deployment/[servico] -n [namespace]

# Monitorar o rollout
kubectl rollout status deployment/[servico] -n [namespace]
```

---

### Contatos de Escalonamento

| Nível | Quem | Quando Acionar | Canal |
|-------|------|---------------|-------|
| L1 | Engenheiro de plantão | Qualquer alerta | PagerDuty — [policy] |
| L2 | Tech Lead do time | L1 não resolveu em 30min | Slack #[canal] |
| L3 | Engineering Manager | Incidente P0/P1 > 1h | Telefone: [número] |
| Exec | VP/CTO | Incidente P0 com impacto em clientes | Telefone: [número] |

---

### Manutenção Programada

| Tarefa | Frequência | Procedimento | Responsável |
|--------|-----------|-------------|-------------|
| Rotação de certificados | [Trimestral] | [Link para proc.] | [Time] |
| Limpeza de logs/dados | [Mensal] | [Link para proc.] | [Time] |
| Atualização de dependências | [Quinzenal] | [Link para proc.] | [Time] |
| Teste de disaster recovery | [Semestral] | [Link para proc.] | [Time] |

---

## Exemplo Preenchido (Resumo)

> **Serviço:** payment-gateway | **Criticidade:** P0 | **SLA:** 99.99%
> **Stack:** Go + PostgreSQL + Redis + Kafka
> **Cenário mais comum:** Timeout no gateway bancário externo
> **Resolução típica:** Circuit breaker já ativado — verificar se banco parceiro está com instabilidade, acionar contato no parceiro

---

## Dicas de Uso
- Escreva como se o leitor estivesse às 3h da manhã, cansado e sob pressão
- Cada comando deve ser copy-paste ready — sem ambiguidade
- Inclua screenshots de dashboards quando possível
- Teste o runbook com engenheiro de outro time a cada trimestre
- Após cada incidente, atualize o runbook com o que faltou
- Mantenha uma seção de "gotchas" — coisas contra-intuitivas do sistema
