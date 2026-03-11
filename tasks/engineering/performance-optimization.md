# Otimização de Performance

> Processo estruturado para identificar, medir e resolver gargalos de
> performance em sistemas de software, garantindo experiência adequada
> para usuários e eficiência de custos de infraestrutura.

## Objetivo

Manter a performance dos sistemas dentro de targets definidos, reduzir custos
de infraestrutura onde possível e garantir que a experiência do usuário não
degrada com o crescimento do negócio.

## Frequência

- **Review de métricas:** Semanal (automatizado)
- **Deep dive de performance:** Mensal
- **Otimização sprint:** Trimestral ou quando targets são violados
- **Load testing:** Antes de eventos de pico conhecidos

## Métricas de Performance

### User-Facing (Core Web Vitals + Custom)
- [ ] **LCP (Largest Contentful Paint):** Target < 2.5s
- [ ] **FID (First Input Delay) / INP:** Target < 100ms
- [ ] **CLS (Cumulative Layout Shift):** Target < 0.1
- [ ] **TTFB (Time to First Byte):** Target < 200ms
- [ ] **Page Load Time (p50, p95, p99):** Targets por página
- [ ] **API Response Time (p50, p95, p99):** Target por endpoint

### Backend
- [ ] **Throughput:** Requests/second por serviço
- [ ] **Error Rate:** Target < 0.1%
- [ ] **Database Query Time (p50, p95):** Target < 100ms
- [ ] **Queue Depth:** Mensagens pendentes por fila
- [ ] **Cache Hit Rate:** Target > 90%

### Infraestrutura
- [ ] **CPU Utilization:** Target 40-70% (headroom para picos)
- [ ] **Memory Utilization:** Target < 80%
- [ ] **Disk I/O:** Latência e throughput
- [ ] **Network Latency:** Entre serviços e para o usuário
- [ ] **Cost per Request:** Target decrescente com escala

## Processo de Otimização

### Fase 1: Measure (Não Otimize Sem Dados)
Regra de ouro: "Se você não mediu, você não sabe."

- [ ] Instrumentar serviços com métricas (Prometheus, Datadog, New Relic)
- [ ] Distributed tracing ativo (Jaeger, Zipkin, OpenTelemetry)
- [ ] Real User Monitoring (RUM) para métricas de frontend
- [ ] Profiling em produção para hotspots (continuous profiling)
- [ ] Baseline documentado para cada métrica-chave

### Fase 2: Identify (Encontrar o Gargalo Real)
A maioria dos problemas de performance está em poucos hotspots:

- [ ] Analisar traces dos requests mais lentos (p99)
- [ ] Identificar os top 5 endpoints mais lentos
- [ ] Profiling de CPU e memória dos serviços críticos
- [ ] Análise de queries de banco (slow query log)
- [ ] Review de cache effectiveness

### Fase 3: Optimize (Resolver na Ordem Certa)
Priorizar otimizações pelo maior impacto com menor esforço:

**Quick Wins (horas)**
- [ ] Adicionar/melhorar caching (CDN, application cache, query cache)
- [ ] Otimizar queries de banco (índices, query rewriting)
- [ ] Comprimir respostas (gzip/brotli)
- [ ] Lazy loading de recursos não-críticos
- [ ] Connection pooling para databases

**Melhorias Médias (dias)**
- [ ] Redesign de queries N+1
- [ ] Implementar pagination e infinite scroll
- [ ] Async processing para operações não-críticas
- [ ] CDN e edge caching para assets e API
- [ ] Right-sizing de instâncias

**Melhorias Estruturais (semanas)**
- [ ] Denormalização de dados para leituras frequentes
- [ ] Introdução de cache layer (Redis/Memcached)
- [ ] Event-driven architecture para desacoplamento
- [ ] Database sharding ou read replicas
- [ ] Migração para serviços mais adequados

### Fase 4: Validate (Confirmar a Melhoria)
- [ ] Comparar métricas antes e depois
- [ ] Load test com perfil de tráfego realista
- [ ] Monitorar por 1-2 semanas após mudança
- [ ] Documentar resultado e decisão

## Load Testing

### Tipos de Teste
1. **Baseline Test:** Performance com carga normal
2. **Stress Test:** Performance com 2-5x a carga normal
3. **Spike Test:** Performance com pico súbito de carga
4. **Soak Test:** Performance sob carga constante por horas/dias
5. **Breakpoint Test:** Encontrar o ponto de falha

### Checklist de Load Test
- [ ] Ambiente de teste similar a produção
- [ ] Dados de teste representativos
- [ ] Cenários de teste cobrindo fluxos críticos
- [ ] Métricas de monitoramento ativas durante teste
- [ ] Critérios de pass/fail definidos antes do teste
- [ ] Resultados documentados e comparados com baseline

### Ferramentas Recomendadas
- k6 (para testes scriptados)
- Locust (Python-based)
- Gatling (Scala-based)
- Artillery (Node.js-based)
- JMeter (Java-based, complexo mas completo)

## Cost Optimization

### Estratégias de Redução de Custo
1. **Right-sizing:** Ajustar tamanho de instâncias ao uso real
2. **Reserved instances:** Comprometer para desconto (40-60%)
3. **Spot instances:** Para workloads tolerantes a interrupção
4. **Auto-scaling:** Escalar para baixo fora de pico
5. **Serverless:** Para workloads intermitentes
6. **Data lifecycle:** Mover dados antigos para storage barato

### Monitoramento de Custos
- [ ] Dashboard de custo por serviço/time
- [ ] Alertas para anomalias de custo (>20% vs média)
- [ ] Monthly cost review com engineering leads
- [ ] Tagging de recursos por time/projeto

## Comunicação de Resultados

### Para Engenharia
- Métricas detalhadas (p50, p95, p99)
- Trace analysis de problemas encontrados
- PRs de otimização com dados before/after
- Playbooks para problemas recorrentes

### Para C-Level
- Performance vs SLAs definidos
- Custo de infraestrutura vs receita (trend)
- Impacto de performance em métricas de negócio (conversão, churn)
- Investimento necessário para melhorias

## Referências

- "High Performance Browser Networking" - Ilya Grigorik
- "Systems Performance" - Brendan Gregg
- Google Web Vitals (web.dev/vitals)
- "Designing Data-Intensive Applications" - Martin Kleppmann
- Brendan Gregg's USE Method (utilization, saturation, errors)
