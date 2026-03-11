# Template: Architecture Decision Record (ADR)

## Propósito
Este template documenta decisões arquiteturais significativas de forma estruturada. ADRs criam um registro histórico do "por quê" por trás de decisões técnicas, facilitando onboarding, auditorias e reavaliações futuras.

## Instruções de Uso
1. Crie um novo ADR para cada decisão arquitetural significativa
2. Numere sequencialmente (ADR-001, ADR-002, etc.)
3. Uma vez aceito, o status muda para "Aceito" — nunca delete ADRs, apenas superseda
4. Revise ADRs antigos quando o contexto mudar significativamente

---

## ADR-[NNN]: [Título da Decisão]

### Metadados

| Campo | Valor |
|-------|-------|
| **Status** | [Proposto / Aceito / Depreciado / Supersedido por ADR-XXX] |
| **Data da Decisão** | [DD/MM/AAAA] |
| **Decisores** | [Nomes e cargos] |
| **Revisores** | [Nomes e cargos] |
| **Área Afetada** | [Backend / Frontend / Infra / Data / etc.] |
| **Impacto** | [Alto / Médio / Baixo] |
| **Esforço de Implementação** | [Alto / Médio / Baixo] |

---

### Contexto

[Descrever a situação atual, problema ou necessidade que motivou esta decisão. Incluir:]

- **Problema:** [Qual problema estamos resolvendo]
- **Contexto de negócio:** [Por que isso é importante agora]
- **Restrições técnicas:** [Limitações existentes que influenciam a decisão]
- **Restrições de tempo/budget:** [Prazos ou limites financeiros relevantes]
- **Stakeholders impactados:** [Quem é afetado por esta decisão]

---

### Decisão

**Decidimos:** [Declaração clara e concisa da decisão tomada]

[Parágrafo expandindo a decisão com detalhes de implementação]

---

### Alternativas Consideradas

#### Alternativa A: [Nome/Descrição]
- **Descrição:** [Como funcionaria]
- **Prós:** [Listar vantagens]
- **Contras:** [Listar desvantagens]
- **Custo estimado:** [R$ X / N sprints]
- **Por que foi descartada:** [Razão principal]

#### Alternativa B: [Nome/Descrição]
- **Descrição:** [Como funcionaria]
- **Prós:** [Listar vantagens]
- **Contras:** [Listar desvantagens]
- **Custo estimado:** [R$ X / N sprints]
- **Por que foi descartada:** [Razão principal]

#### Alternativa C: Não fazer nada
- **Impacto:** [O que acontece se mantivermos o status quo]
- **Riscos:** [Riscos de não agir]

---

### Matriz de Decisão

| Critério | Peso | Opção Escolhida | Alt. A | Alt. B | Não Fazer |
|----------|------|:---:|:---:|:---:|:---:|
| Performance | [1-5] | [1-5] | [1-5] | [1-5] | [1-5] |
| Manutenibilidade | [1-5] | [1-5] | [1-5] | [1-5] | [1-5] |
| Custo | [1-5] | [1-5] | [1-5] | [1-5] | [1-5] |
| Time-to-market | [1-5] | [1-5] | [1-5] | [1-5] | [1-5] |
| Escalabilidade | [1-5] | [1-5] | [1-5] | [1-5] | [1-5] |
| Risco | [1-5] | [1-5] | [1-5] | [1-5] | [1-5] |
| **Score Ponderado** | — | **[X.X]** | **[X.X]** | **[X.X]** | **[X.X]** |

---

### Consequências

#### Positivas
- [Benefício 1 esperado com a decisão]
- [Benefício 2 esperado com a decisão]
- [Benefício 3 esperado com a decisão]

#### Negativas (Trade-offs aceitos)
- [Trade-off 1 que estamos aceitando conscientemente]
- [Trade-off 2 que estamos aceitando conscientemente]

#### Riscos da Decisão
| Risco | Probabilidade | Impacto | Mitigação |
|-------|-------------|---------|-----------|
| [Risco 1] | [A/M/B] | [A/M/B] | [Plano] |
| [Risco 2] | [A/M/B] | [A/M/B] | [Plano] |

---

### Plano de Implementação

| Fase | Atividade | Prazo | Responsável |
|------|----------|-------|-------------|
| 1 | [Etapa inicial] | [Semana X] | [Nome] |
| 2 | [Etapa intermediária] | [Semana Y] | [Nome] |
| 3 | [Etapa final e validação] | [Semana Z] | [Nome] |

---

### Métricas de Sucesso

- [Métrica 1 — como saberemos que a decisão foi boa]
- [Métrica 2 — indicador de que precisamos reavaliar]
- **Data de reavaliação:** [DD/MM/AAAA — quando revisitaremos esta decisão]

---

### Referências

- [Link para RFC relacionada]
- [Link para doc técnico]
- [Link para benchmark/POC]
- [ADRs relacionados: ADR-XXX, ADR-YYY]

---

## Exemplo Preenchido (Resumo)

> **ADR-042:** Migração de PostgreSQL para CockroachDB para multi-região
> **Status:** Aceito | **Data:** 15/01/2026 | **Impacto:** Alto
> **Contexto:** Latência de 200ms+ para usuários LATAM acessando DB em us-east-1
> **Decisão:** Migrar para CockroachDB com clusters em 3 regiões (us-east, sa-east, eu-west)
> **Trade-off:** +40% no custo de infra, complexidade de operação
> **Alternativa descartada:** Read replicas do PostgreSQL (não resolve writes)
> **Métrica de sucesso:** p99 latência < 50ms em todas as regiões

---

## Dicas de Uso
- ADR é para decisões SIGNIFICATIVAS — não documente cada escolha técnica
- Foque no "por quê" mais do que no "como" — o código mostra o como
- Inclua o contexto temporal — decisões que parecem ruins hoje fizeram sentido no contexto original
- Nunca delete um ADR — marque como "Supersedido" e referencie o novo
- Revise ADRs em tech reviews trimestrais — contexto muda
- Mantenha ADRs próximos ao código (no repo) — não em wiki separada
