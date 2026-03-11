# Tarefa: Setup de Observabilidade

## Objetivo
Implementar uma stack completa de observabilidade que permita entender o comportamento dos sistemas em produção, detectar problemas rapidamente e fazer troubleshooting eficaz.

---

## 1. Os Três Pilares da Observabilidade

### Pilares
```
                 Observabilidade
                /       |       \
           Logs      Métricas    Traces
           |            |            |
    O que aconteceu  Como está    Onde passou
    (eventos)        (saúde)      (fluxo)
```

### Definições
- **Logs**: Registros de eventos discretos com contexto (quem, quando, o que)
- **Métricas**: Medidas numéricas agregadas ao longo do tempo (counters, gauges, histograms)
- **Traces**: Representação do caminho de uma requisição através do sistema distribuído

### Objetivo Final
- Detectar problemas antes que clientes percebam
- Diagnosticar causa raiz em minutos, não horas
- Entender comportamento do sistema sob diferentes condições
- Tomar decisões baseadas em dados sobre performance e capacidade
- Reduzir MTTR (Mean Time to Resolve) para incidentes

---

## 2. Assessment Atual

### Checklist de Estado Atual
- [ ] Qual ferramenta de logs está em uso? Cobertura é completa?
- [ ] Métricas de infraestrutura estão sendo coletadas? (CPU, memória, disco, rede)
- [ ] Métricas de aplicação estão sendo coletadas? (latência, errors, throughput)
- [ ] Distributed tracing está implementado? Para quais serviços?
- [ ] Alertas estão configurados? Quantos são acionáveis vs ruído?
- [ ] Dashboards existem? São usados no dia a dia?
- [ ] Runbooks estão linkados aos alertas?
- [ ] Qual é o custo atual de observabilidade?
- [ ] Qual é a retenção de dados atual?

### Gaps Comuns
| Gap | Impacto | Prioridade |
|-----|---------|-----------|
| Logs não estruturados | Debug lento, busca difícil | Alta |
| Sem tracing distribuído | Impossível seguir requisição | Alta |
| Alertas demais (alert fatigue) | Alertas ignorados | Alta |
| Sem métricas de negócio | Não sabe impacto em clientes | Média |
| Dashboards desatualizados | Informação irrelevante | Média |
| Sem correlação entre pilares | Análise fragmentada | Média |

---

## 3. Stack de Observabilidade

### Opção A: Stack Open Source
| Componente | Ferramenta | Uso |
|-----------|-----------|-----|
| Métricas | Prometheus + Grafana | Coleta e visualização |
| Logs | Loki + Grafana | Agregação e busca |
| Traces | Jaeger ou Tempo | Distributed tracing |
| Alerting | Alertmanager + Grafana | Alertas e notificações |
| Collection | OpenTelemetry | Instrumentação unificada |

### Opção B: Stack SaaS
| Componente | Ferramenta | Uso |
|-----------|-----------|-----|
| All-in-one | Datadog ou New Relic | Métricas, logs, traces, APM |
| Alerting | PagerDuty ou OpsGenie | Gestão de incidentes |
| Status Page | Statuspage.io | Comunicação com clientes |
| Error Tracking | Sentry | Erros de aplicação |

### Opção C: Stack Híbrida (Recomendada para Médio Porte)
| Componente | Ferramenta | Custo |
|-----------|-----------|-------|
| Instrumentação | OpenTelemetry (open source) | Gratuito |
| APM + Métricas | Datadog ou Grafana Cloud | SaaS pago |
| Error Tracking | Sentry | SaaS pago |
| On-Call | PagerDuty ou OpsGenie | SaaS pago |
| Dashboards | Grafana | Gratuito/Pago |

---

## 4. Implementação

### Fase 1: Fundação (Semanas 1-3)

**Instrumentação com OpenTelemetry**
- [ ] Adicionar SDK do OpenTelemetry aos serviços principais
- [ ] Configurar auto-instrumentação onde possível (HTTP, gRPC, DB)
- [ ] Definir padrões de span naming e atributos
- [ ] Configurar propagação de contexto (trace context) entre serviços
- [ ] Implementar sampling strategy (nem toda requisição precisa de trace)

**Logging Estruturado**
- [ ] Migrar logs para formato estruturado (JSON)
- [ ] Padronizar campos obrigatórios: timestamp, level, service, trace_id, message
- [ ] Implementar correlation_id para rastrear fluxos de negócio
- [ ] Configurar níveis de log adequados por ambiente (DEBUG dev, INFO prod)
- [ ] Centralizar logs em plataforma de agregação

**Métricas Básicas**
- [ ] Configurar métricas de infraestrutura (CPU, memória, disco, rede)
- [ ] Implementar RED metrics para cada serviço:
  - **R**ate: Requisições por segundo
  - **E**rrors: Taxa de erros
  - **D**uration: Latência (P50, P95, P99)
- [ ] Implementar USE metrics para infraestrutura:
  - **U**tilization: % de capacidade em uso
  - **S**aturation: Fila de trabalho pendente
  - **E**rrors: Erros de hardware/sistema

### Fase 2: Dashboards e Alertas (Semanas 4-6)

**Dashboards Essenciais**
- [ ] Dashboard de Overview do Sistema (golden signals de todos os serviços)
- [ ] Dashboard por Serviço (RED metrics, dependências, erros)
- [ ] Dashboard de Infraestrutura (nodes, pods, databases)
- [ ] Dashboard de Business Metrics (transações, conversão, receita em tempo real)
- [ ] Dashboard de SLA (uptime, latência vs SLA contratual)

**Alertas Eficazes**
- [ ] Definir SLOs (Service Level Objectives) para cada serviço
- [ ] Configurar alertas baseados em SLO burn rate (não em threshold fixo)
- [ ] Implementar multi-window alerting para reduzir falsos positivos
- [ ] Cada alerta deve ter: severidade, runbook link, owner
- [ ] Revisar e calibrar alertas semanalmente nas primeiras 4 semanas
- [ ] Meta: zero alertas que não são acionáveis

**Princípios de Alertas**
| Severidade | Ação | Tempo de Resposta | Exemplo |
|-----------|------|-------------------|---------|
| Critical | Wake someone up | < 5 min | Sistema principal down |
| Warning | Ação em horário comercial | < 4 horas | Latência acima do SLO |
| Info | Review na próxima oportunidade | < 1 dia | Disco 80% cheio |

### Fase 3: Tracing e Correlação (Semanas 7-10)

**Distributed Tracing**
- [ ] Implementar tracing em todos os serviços do caminho crítico
- [ ] Configurar trace sampling (100% para erros, 1-10% para normal)
- [ ] Adicionar atributos de negócio nos spans (user_id, order_id)
- [ ] Criar trace-based dashboards (latência por operação)
- [ ] Implementar exemplar linking (métrica -> trace específico)

**Correlação entre Pilares**
- [ ] Garantir trace_id presente em logs, métricas e traces
- [ ] Configurar drill-down: dashboard -> trace -> logs
- [ ] Implementar service map visual (dependências entre serviços)
- [ ] Correlacionar deploys com mudanças em métricas

### Fase 4: Maturidade (Semanas 11-16)

**SLOs e Error Budget**
- [ ] Definir SLOs formais para serviços críticos (ex: 99.9% uptime)
- [ ] Implementar error budget tracking (quanto "margem" temos)
- [ ] Usar error budget para decisão: investir em reliability vs features
- [ ] Dashboard de SLO visível para engenharia e produto

**Automação**
- [ ] Auto-remediation para problemas conhecidos (restart, scale-up)
- [ ] Anomaly detection com ML para métricas-chave
- [ ] Automatizar criação de incidente quando alerta critical dispara
- [ ] Runbooks automatizados para diagnóstico inicial

---

## 5. Métricas de Sucesso

| Métrica | Baseline | Meta 3 Meses | Meta 6 Meses |
|---------|----------|-------------|-------------|
| MTTD (tempo para detectar) | [X min] | <5 min | <2 min |
| MTTR (tempo para resolver) | [X min] | -50% | -70% |
| Alertas falso-positivo | [X%] | <20% | <5% |
| Cobertura de serviços | [X%] | >80% | 100% |
| Dashboards em uso diário | [X] | 5+ | 10+ |
| Incidentes detectados por monitoring | [X%] | >70% | >90% |

---

## 6. Custos e Otimização

### Estimativa de Custos
| Componente | Custo Mensal | Otimização |
|-----------|-------------|-----------|
| Logs storage | [R$ X] | Definir retenção adequada, filtrar ruído |
| Métricas | [R$ X] | Cardinalidade controlada, aggregation |
| Traces | [R$ X] | Sampling strategy adequada |
| SaaS licenses | [R$ X] | Avaliar vs open source |
| Infra (runners) | [R$ X] | Rightsizing, spot instances |

### Boas Práticas de Custo
- Log levels: não logar DEBUG em produção
- Métrica cardinality: evitar labels com alta cardinalidade (ex: user_id)
- Trace sampling: 1-10% para tráfego normal, 100% para erros
- Data retention: logs 30 dias, métricas 13 meses, traces 7 dias
- Compression: habilitar compressão em todos os dados
