---
source: "Compilação — Netflix, Uber, Stripe tech blogs"
date_captured: 2026-03-11
category: tech-architecture
agents: [cto-architect, cio-engineer]
tags: [architecture, system-design, scalability, patterns]
quality: gold
---

# System Design References — Patterns de Escala

## Patterns Recorrentes em Sistemas de Escala

### 1. Event-Driven Architecture (Netflix)

**Problema:** Acoplamento síncrono entre serviços causa cascading failures.

**Solução Netflix:**
- Event sourcing para todas as mudanças de estado
- Apache Kafka como backbone de eventos
- Consumers idempotentes por design
- Dead letter queues para eventos não processados

**Resultado:** 99.99% uptime com 200+ microservices.

### 2. Cell-Based Architecture (Uber)

**Problema:** Falha em uma região afeta usuários globalmente.

**Solução Uber:**
- Cada "cell" é uma unidade isolada de deployment
- Cells são geograficamente distribuídas
- Routing layer direciona para cell saudável
- Blast radius limitado a uma cell

**Resultado:** Falha regional não afeta outras regiões.

### 3. Idempotency Keys (Stripe)

**Problema:** Retries em sistemas distribuídos causam duplicação.

**Solução Stripe:**
- Toda request mutadora requer idempotency key
- Key é hash de (user_id + intent + params)
- Servidor mantém cache de results por key
- Retry com mesma key retorna resultado original

**Resultado:** Zero pagamentos duplicados em bilhões de transações.

### 4. Circuit Breaker Pattern

**Estado Normal:** requests passam normalmente.
**Estado Aberto:** requests falham imediatamente (fast-fail).
**Estado Half-Open:** permite requests limitados para testar recuperação.

```
Normal → [falhas > threshold] → Aberto
Aberto → [timeout expira] → Half-Open
Half-Open → [sucesso] → Normal
Half-Open → [falha] → Aberto
```

## O que Aprendemos

1. **Design for failure** — assuma que tudo vai falhar e planeje recovery
2. **Idempotência não é opcional** — é requisito em sistemas distribuídos
3. **Blast radius é a métrica principal** — minimize o impacto de falhas
4. **Observabilidade > Prevenção** — você não pode prevenir todas as falhas

## Como Aplicar no C-Level Squad

- Referência para decisões de arquitetura via `cto-architect`
- Vocabulary de patterns em `reference/books/engineering/`
- Checklists de revisão em `checklists/engineering/`
