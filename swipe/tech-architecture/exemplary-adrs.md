---
source: "Multiple — ADR best practices compilação"
date_captured: 2026-03-11
category: tech-architecture
agents: [cto-architect, cio-engineer]
tags: [architecture, adr, decision-record, engineering]
quality: gold
---

# Architecture Decision Records (ADRs) — Exemplos de Excelência

## O que é um ADR

Um Architecture Decision Record documenta uma decisão arquitetural
significativa, seu contexto, alternativas consideradas e consequências.
ADRs são imutáveis — nunca editados, apenas substituídos por novos ADRs.

## Template MADR (Markdown ADR)

```markdown
# ADR-NNNN: [Título da Decisão]

## Status
[Proposed | Accepted | Deprecated | Superseded by ADR-XXXX]

## Context
[Qual é o problema? Por que precisamos decidir agora?]

## Decision
[O que decidimos fazer?]

## Consequences
### Positivas
- [Consequência positiva 1]

### Negativas
- [Trade-off aceito 1]

### Neutras
- [Mudança que não é boa nem ruim]

## Alternatives Considered
### Alternativa A
- Prós: ...
- Contras: ...

### Alternativa B
- Prós: ...
- Contras: ...

## References
- [Links relevantes]
```

## Exemplo: ADR de Migração para Microservices

### ADR-0042: Decomposição do Monolito em Serviços de Domínio

**Status:** Accepted

**Context:**
O monolito Ruby on Rails atingiu 500K LOC. Deploys levam 45min.
Uma falha em qualquer módulo derruba todo o sistema. Time de 80 devs
tem conflitos de merge constantes. CI leva 2h para rodar.

**Decision:**
Adotar decomposição gradual usando Strangler Fig Pattern. Começar pelos
domínios de Pagamentos e Notificações (boundaries mais claros). Usar
eventos assíncronos via Kafka para comunicação entre serviços. Manter
monolito como fallback durante transição.

**Consequences:**
- (+) Deploys independentes por domínio (target: < 5min)
- (+) Fault isolation — falha em Notificações não afeta Pagamentos
- (+) Times autônomos por domínio
- (-) Complexidade operacional aumenta (observabilidade, tracing)
- (-) Consistência eventual requer mudança de mindset
- (-) Custo de infra aumenta ~30% durante transição

**Alternatives Considered:**
1. **Modular Monolith** — Prós: simples; Contras: não resolve deploy coupling
2. **Full Rewrite** — Prós: clean slate; Contras: risco altíssimo, 12+ meses
3. **Micro-frontends only** — Prós: menos risco; Contras: não resolve backend

## O que Aprendemos

1. **ADRs eliminam "por que fizemos isso?"** — contexto preservado para
   futuros engenheiros
2. **Alternativas documentadas mostram rigor** — provam que a decisão
   foi deliberada, não acidental
3. **Consequências negativas são obrigatórias** — toda decisão tem trade-offs
4. **ADRs são imutáveis** — crie novos, nunca edite existentes
5. **Numere sequencialmente** — permite rastrear evolução arquitetural

## Como Aplicar no C-Level Squad

- Usar como referência para o agente `cto-architect` ao documentar decisões
- Template ADR disponível em `templates/engineering/`
- Integrar com processo de Tech Review em `workflows/tech-review/`
