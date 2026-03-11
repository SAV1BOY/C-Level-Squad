# Naming Conventions — Convenções de Nomenclatura

> Padrões de nomenclatura para todos os ficheiros, IDs e artefactos do C-Level Squad.

---

## Objetivo

Convenções de nomenclatura consistentes permitem encontrar qualquer coisa
rapidamente, evitam ambiguidade e facilitam automação. Este guia define os
padrões obrigatórios para todo o squad.

---

## Princípios Gerais

1. **Clareza sobre brevidade**: nome deve ser entendido sem contexto adicional
2. **Consistência**: mesmo padrão em todo o repositório
3. **Lowercase**: tudo em minúsculas excepto acrónimos em IDs
4. **Hífens como separadores**: usar `-` para separar palavras em nomes de ficheiros
5. **Sem espaços**: nunca usar espaços em nomes de ficheiros
6. **Sem caracteres especiais**: apenas letras, números, hífens e underscores
7. **Inglês para nomes técnicos**: nomes de ficheiros e IDs sempre em inglês
8. **Português para conteúdo**: texto operacional dentro dos ficheiros em português

---

## Ficheiros e Directórios

### Directórios
```
Padrão: lowercase-com-hifens/
Exemplos:
  agents/
  cross-squad/
  agent-summaries/
  iconic-operating-systems/
```

### Ficheiros Markdown
```
Padrão: nome-descritivo.md
Exemplos:
  getting-started.md
  risk-scan.md
  vision-chief-summary.md
  amazon-wbr-system.md
```

### Ficheiros de Dados (YAML)
```
Padrão: tipo-ou-id.yaml
Exemplos:
  config.yaml
  index.yaml
  DEC-2026-0001.yaml
```

### Ficheiros de Template
```
Padrão: template-nome.md
Exemplos:
  template-wbr-agenda.md
  template-decision-record.md
  template-stakeholder-update.md
```

---

## IDs e Referências

### Decision IDs
```
Padrão: DEC-YYYY-NNNN
Exemplo: DEC-2026-0042
- DEC: prefixo fixo para decisões
- YYYY: ano da decisão
- NNNN: número sequencial (0001-9999)
```

### Risk IDs
```
Padrão: RISK-YYYY-NNNN
Exemplo: RISK-2026-0015
- RISK: prefixo fixo para riscos
- YYYY: ano de identificação
- NNNN: número sequencial
```

### Initiative IDs
```
Padrão: INIT-YYYY-NNNN
Exemplo: INIT-2026-0003
- INIT: prefixo fixo para iniciativas
- YYYY: ano de criação
- NNNN: número sequencial
```

### Forecast IDs
```
Padrão: FC-YYYY-NNNN
Exemplo: FC-2026-0078
- FC: prefixo fixo para forecasts
- YYYY: ano da previsão
- NNNN: número sequencial
```

### Meeting IDs
```
Padrão: MTG-YYYY-MM-DD-tipo
Exemplo: MTG-2026-03-11-wbr
- MTG: prefixo fixo para reuniões
- YYYY-MM-DD: data da reunião
- tipo: wbr, mbr, qbr, adhoc, standup
```

### Eval IDs
```
Padrão: EVAL-YYYY-NNNN
Exemplo: EVAL-2026-0005
- EVAL: prefixo fixo para avaliações AI
- YYYY: ano da avaliação
- NNNN: número sequencial
```

### SLA IDs
```
Padrão: SLA-squad1-squad2-tipo
Exemplo: SLA-cto-cio-support
- SLA: prefixo fixo
- squad1: squad provider (abreviado)
- squad2: squad consumer (abreviado)
- tipo: tipo de serviço
```

### Roadmap Item IDs
```
Padrão: RM-NNN
Exemplo: RM-042
- RM: prefixo fixo para roadmap items
- NNN: número sequencial
```

---

## Versionamento de Ficheiros

### Documentos Versionados
```
Padrão: nome-YYYY-MM-DD-vN.md
Exemplo: board-pack-2026-03-15-v2.md
- nome: nome do documento
- YYYY-MM-DD: data da versão
- vN: número da versão (v1, v2, v3)
```

### Snapshots (Baselines)
```
Padrão: nome-YYYY-QN-baseline.yaml
Exemplo: roadmap-2026-Q1-baseline.yaml
- nome: tipo de snapshot
- YYYY-QN: trimestre de referência
- baseline: indicador de snapshot
```

---

## Tags e Labels

### Tags para Decisões e Riscos
```
Padrão: lowercase-sem-espacos
Categorias standard:
  Área: strategy, operations, technology, people, finance, marketing, ai
  Urgência: urgent, normal, low
  Status: open, in-progress, closed, blocked
```

### Status Labels
```
Padrão para estados de saúde:
  healthy | at-risk | troubled | critical

Padrão para estados de progresso:
  not-started | in-progress | completed | cancelled | on-hold

Padrão para estados de decisão:
  active | superseded | revoked
```

---

## Agentes e Squads

### Nomes dos Agentes (Official)
| ID Curto | Nome Completo | Uso em IDs |
|---------|--------------|-----------|
| vision | Vision Chief | vision |
| coo | COO Orchestrator | coo |
| cmo | CMO Architect | cmo |
| cto | CTO Architect | cto |
| cio | CIO Engineer | cio |
| caio | CAIO Architect | caio |

### Uso em Ficheiros
```
agents/vision-chief.md
agents/coo-orchestrator.md
authority/agent-summaries/vision-chief-summary.md
checklists/coo/checklist-nome.md
```

---

## Métricas e KPIs

### Nomes de Métricas
```
Padrão: dominio_metrica_unidade (snake_case para dados)
Exemplos:
  revenue_monthly_eur
  customer_churn_rate_pct
  sprint_velocity_points
  sla_compliance_rate_pct
  decision_quality_score
```

### Nomes em Dashboards (Display)
```
Padrão: Title Case com unidade
Exemplos:
  "Monthly Revenue (EUR)"
  "Customer Churn Rate (%)"
  "Sprint Velocity (Points)"
  "SLA Compliance Rate (%)"
```

---

## Comunicações

### Assuntos de Email / Updates
```
Padrão: [Tipo] — Resumo curto
Exemplos:
  [WBR] — Week 11 Review
  [MBR] — March 2026 Review
  [Decision] — New pricing approved
  [Alert] — SLA breach in Squad CTO
  [Update] — Q1 Progress Report
```

---

## Enforcement

### Como Garantir Cumprimento
1. **Linting automático**: script que verifica convenções (onde possível)
2. **PR review**: nomes verificados durante review de alterações
3. **Templates**: templates já incluem nomes correctos
4. **Onboarding**: convenções ensinadas durante onboarding
5. **Correcção activa**: ficheiros fora do padrão são renomeados quando detectados

### Excepções
Excepções ao padrão são permitidas quando:
- Integração com sistema externo que exige formato diferente
- Convenção do sector é diferente (ex: CHANGELOG.md em maiúsculas)
- Retrocompatibilidade requer manutenção de nome existente

Excepções devem ser documentadas neste ficheiro.

---

## Notas Técnicas

- Este ficheiro é a referência autoritativa para nomenclatura
- Alterações requerem aprovação do COO Orchestrator
- Automatização de verificação em `scripts/lint/naming-check.sh`
- Retrocompatibilidade: ficheiros existentes podem manter nomes antigos se renomear causa breaking changes
