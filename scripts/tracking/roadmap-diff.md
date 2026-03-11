# Roadmap Diff

> Script para comparação entre roadmap planeado e execução real.

---

## Objetivo

Comparar sistematicamente o roadmap planeado com a execução real, identificar
desvios, quantificar a sua magnitude e gerar insights sobre padrões de
divergência para melhorar a precisão do planeamento futuro.

---

## Conceito de Diff

O roadmap diff funciona como um "git diff" para o planeamento organizacional:
mostra o que mudou entre o que foi planeado e o que realmente aconteceu,
destacando adições, remoções, alterações e atrasos.

---

## Inputs Necessários

### Roadmap Planeado (Baseline)
```yaml
baseline:
  version: "YYYY-QN-baseline"     # Ex: "2026-Q1-baseline"
  snapshot_date: "YYYY-MM-DD"      # Data em que o plano foi aprovado
  items:
    - id: "RM-001"
      title: "Nome do item"
      type: "feature | initiative | milestone | dependency"
      planned_start: "YYYY-MM-DD"
      planned_end: "YYYY-MM-DD"
      owner: "squad / pessoa"
      priority: "P0 | P1 | P2 | P3"
      dependencies: ["RM-002", "RM-003"]
      expected_outcome: "Resultado esperado"
      resources_planned: "FTEs ou budget"
```

### Execução Real (Actual)
```yaml
actual:
  snapshot_date: "YYYY-MM-DD"       # Data da comparação
  items:
    - id: "RM-001"
      status: "completed | in_progress | delayed | cancelled | added"
      actual_start: "YYYY-MM-DD"
      actual_end: "YYYY-MM-DD"      # ou estimated_end se in_progress
      completion_percentage: 75
      actual_outcome: "Resultado obtido"
      resources_used: "FTEs ou budget real"
      notes: "Contexto relevante"
```

---

## Tipos de Desvio

### 1. Timeline Deviation
- **Adiantamento**: item concluído antes do planeado
- **Atraso**: item concluído ou estimado depois do planeado
- **Fórmula**: `deviation_days = actual_end - planned_end`
- **Classificação**:
  - On time: desvio ≤ 5 dias
  - Minor delay: 6-15 dias
  - Significant delay: 16-30 dias
  - Major delay: >30 dias

### 2. Scope Deviation
- **Scope added**: itens que não estavam no baseline
- **Scope removed**: itens do baseline que foram cancelados
- **Scope changed**: itens cujo scope foi significativamente alterado
- **Fórmula**: `scope_change_rate = (added + removed + changed) / baseline_total`

### 3. Priority Deviation
- **Escalated**: prioridade aumentou (ex: P2 → P0)
- **De-prioritized**: prioridade diminuiu (ex: P1 → P3)
- **Fórmula**: `priority_shift = new_priority - original_priority`

### 4. Resource Deviation
- **Over-resourced**: mais recursos usados que planeado
- **Under-resourced**: menos recursos disponíveis que planeado
- **Fórmula**: `resource_variance = (actual - planned) / planned × 100`

### 5. Outcome Deviation
- **Met expectations**: resultado alinhado com o esperado
- **Exceeded**: resultado superou expectativas
- **Below expectations**: resultado abaixo do esperado
- **Different outcome**: resultado diferente do planeado

---

## Highlight Deviations — Formato de Output

### Diff Summary
```markdown
# Roadmap Diff: [Baseline Version] → [Actual Date]

## Summary
- Total items no baseline: [N]
- Completed on time: [N] ([%])
- Delayed: [N] ([%])
- Cancelled: [N] ([%])
- Added (não planeados): [N]
- Overall schedule accuracy: [%]
- Overall scope stability: [%]

## Critical Deviations (Major delays + Cancelled P0/P1)
| ID | Item | Desvio | Impacto | Causa Raiz |
|----|------|--------|---------|------------|
| RM-001 | [nome] | +45 dias | [descrição] | [causa] |
| RM-005 | [nome] | Cancelado | [descrição] | [causa] |

## Timeline Heatmap
| Item | Jan | Fev | Mar | Abr | Mai | Jun |
|------|-----|-----|-----|-----|-----|-----|
| RM-001 | ██░░ | ████ | ████ | ░░░░ | ░░░░ | ░░░░ |
(██ = planeado, ░░ = actual, ▓▓ = overlap)

## Scope Changes
### Added
- [NEW-001] [título] — razão da adição
### Removed
- [RM-003] [título] — razão do cancelamento
### Changed
- [RM-007] [título] — natureza da alteração

## Dependency Impact
- [RM-002] atrasou [RM-004] em 15 dias (cascading delay)
- [RM-006] bloqueado por dependência externa não prevista
```

---

## Análise de Padrões

### Padrões a Identificar
1. **Optimism bias**: tendência sistemática de subestimar duração
2. **Scope creep pattern**: crescimento consistente de scope ao longo do tempo
3. **Dependency blindness**: subestimação do impacto de dependências
4. **Resource contention**: conflitos recorrentes de alocação
5. **Priority inflation**: tendência de marcar tudo como P0
6. **Planning horizon effect**: precisão degrada com distância temporal

### Métricas de Precisão do Planeamento
- **Schedule Accuracy**: % de itens entregues dentro de ±10% do prazo
- **Scope Stability**: % de itens que mantêm scope original
- **Estimation Accuracy**: ratio actual/planned para tempo e recursos
- **Dependency Prediction**: % de dependências correctamente identificadas
- **Priority Stability**: % de itens que mantêm prioridade original

---

## Processo de Execução

### Passo 1 — Snapshot Collection
- Exportar baseline do roadmap tool
- Exportar estado actual de todos os itens
- Normalizar formatos para comparação

### Passo 2 — Automated Diff
- Matching de itens por ID
- Cálculo de desvios por dimensão
- Identificação de itens added/removed
- Análise de impacto em cascata de dependências

### Passo 3 — Analysis
- Classificar desvios por severidade
- Identificar padrões recorrentes
- Calcular métricas de precisão
- Gerar root cause hypotheses

### Passo 4 — Report Generation
- Produzir diff summary
- Criar visualizações (heatmap, timeline)
- Adicionar comentário analítico
- Distribuir aos stakeholders relevantes

### Passo 5 — Learning Loop
- Registar learnings no knowledge base
- Ajustar estimation guidelines
- Actualizar risk factors para planeamento
- Calibrar buffers baseado em dados históricos

---

## Frequência de Execução

| Tipo de Diff | Frequência | Audiência |
|-------------|-----------|-----------|
| Sprint diff | Bi-semanal | Squad leads |
| Monthly diff | Mensal | C-Level Squad |
| Quarterly diff | Trimestral | C-Level + Board |
| Annual diff | Anual | Full organization |

---

## Notas Técnicas

- Baselines guardados em `data/roadmap/baselines/`
- Diffs guardados em `data/roadmap/diffs/`
- Automação via script que compara ficheiros YAML
- Visualizações geradas automaticamente para inclusão em reports
- Histórico de diffs mantido para análise de tendências multi-período
