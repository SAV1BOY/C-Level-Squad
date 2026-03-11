# Changelog — Registo de Alterações

> Registo cronológico de todas as alterações significativas ao C-Level Squad OS.

---

## Formato

Cada entrada segue o formato:
```
## [Versão] — YYYY-MM-DD

### Adicionado
- [Descrição do que foi adicionado]

### Alterado
- [Descrição do que foi modificado]

### Corrigido
- [Descrição do que foi corrigido]

### Removido
- [Descrição do que foi removido]

### Notas
- [Contexto adicional relevante]
```

---

## Princípios do Changelog

1. **Para humanos**: escrito para pessoas, não para máquinas
2. **Cada versão tem data**: sempre com data ISO (YYYY-MM-DD)
3. **Mais recente primeiro**: entradas em ordem cronológica reversa
4. **Agrupado por tipo**: adicionado, alterado, corrigido, removido
5. **Referência ao contribuidor**: quando relevante, indicar quem contribuiu

---

## Categorias de Mudança

### Adicionado
Para funcionalidades, ficheiros ou capacidades completamente novas.

### Alterado
Para mudanças em funcionalidades existentes, reformulações ou actualizações.

### Corrigido
Para correcções de bugs, erros de documentação ou problemas.

### Removido
Para funcionalidades ou ficheiros que foram eliminados.

### Deprecated
Para funcionalidades que serão removidas numa versão futura.

### Segurança
Para alterações relacionadas com vulnerabilidades ou compliance.

---

## Registo de Versões

## [1.0.0] — 2026-03-11

### Adicionado

#### Estrutura Base
- Repositório C-Level Squad inicializado com estrutura completa
- Ficheiro `config.yaml` com configuração central do sistema
- Ficheiro `ARCHITECTURE.md` com visão da arquitectura
- Ficheiro `README.md` com introdução ao projecto

#### Agentes
- Definições completas dos 6 agentes em `agents/`
- Vision Chief, COO Orchestrator, CMO Architect
- CTO Architect, CIO Engineer, CAIO Architect

#### Documentação
- `docs/getting-started.md` — guia de início rápido
- `docs/c-level-overview.md` — visão geral do sistema
- `docs/agent-roles-guide.md` — guia detalhado dos agentes
- `docs/operating-system.md` — como o OS opera
- `docs/decision-making.md` — regras de decisão
- `docs/cross-squad-contracts.md` — SLAs e contratos
- `docs/governance-and-policies.md` — políticas e governance
- `docs/ai-governance.md` — governance de AI
- `docs/framework-selection-guide.md` — como escolher frameworks
- `docs/workflow-guide.md` — como executar workflows
- `docs/onboarding.md` — processo de onboarding
- `docs/naming-conventions.md` — convenções de nomenclatura
- `docs/contribution-guide.md` — como contribuir
- `docs/changelog.md` — este ficheiro
- `docs/gold-standard-and-sota.md` — definição de gold standard
- `docs/glossary.md` — glossário com 50+ termos
- `docs/faq.md` — perguntas frequentes
- `docs/anti-patterns-guide.md` — anti-patterns comuns

#### Scripts de Geração
- `scripts/generation/agenda-generator.md` — geração de agendas
- `scripts/generation/metrics-pack-builder.md` — construção de metrics packs
- `scripts/generation/board-prep-builder.md` — preparação de board packs
- `scripts/generation/stakeholder-update-builder.md` — updates a stakeholders

#### Scripts de Tracking
- `scripts/tracking/decision-log-updater.md` — actualização de decision log
- `scripts/tracking/initiative-health-tracker.md` — tracking de saúde de iniciativas
- `scripts/tracking/risk-scan.md` — scan de riscos
- `scripts/tracking/roadmap-diff.md` — diff de roadmaps
- `scripts/tracking/forecast-accuracy-tracker.md` — tracking de precisão de forecasts

#### Scripts de Análise
- `scripts/analysis/decision-quality-analyzer.md` — análise de qualidade de decisões
- `scripts/analysis/meeting-effectiveness-analyzer.md` — análise de eficácia de reuniões
- `scripts/analysis/ai-eval-runner.md` — avaliação de ferramentas AI
- `scripts/analysis/cross-squad-effectiveness.md` — eficácia cross-squad
- `scripts/analysis/quarterly-review-builder.md` — construção de quarterly review

#### Archive
- 6 sistemas operacionais icónicos em `archive/iconic-operating-systems/`
- 4 ficheiros de evolução em `archive/evolution/`
- 4 ficheiros de falhas e lições em `archive/failures-and-lessons/`

#### Authority
- 6 agent summaries em `authority/agent-summaries/`
- 3 essays em `authority/essays/`
- 2 talk scripts em `authority/talks/`
- 3 case studies em `authority/case-studies/`
- 3 workshop kits em `authority/workshop-kits/`

#### Frameworks, Workflows, Templates, Checklists
- Frameworks de decisão e operação em `frameworks/`
- Workflows operacionais em `workflows/`
- Templates para outputs em `templates/`
- Checklists por domínio em `checklists/`

### Notas
- Versão inicial completa do C-Level Squad OS
- Sistema desenhado para ser adaptado ao contexto de cada organização
- Contribuições bem-vindas conforme `docs/contribution-guide.md`
- Próximas versões focarão em automação e integração com ferramentas externas

---

## Como Manter o Changelog

### Quando Actualizar
- A cada contribuição que é aceite e integrada
- Antes de cada release ou milestone significativo
- Quando políticas ou processos mudam

### Quem Actualiza
- O contribuidor adiciona a entrada
- O reviewer valida antes de merge
- O COO Orchestrator mantém a coerência geral

### Template para Nova Entrada
```markdown
## [X.Y.Z] — YYYY-MM-DD

### Adicionado
- [Novo ficheiro/funcionalidade]

### Alterado
- [Mudança em ficheiro/processo existente]

### Corrigido
- [Bug ou erro corrigido]

### Removido
- [Ficheiro/funcionalidade eliminada]
```

---

## Notas Técnicas

- Formato baseado em Keep a Changelog (keepachangelog.com)
- Versionamento semântico: MAJOR.MINOR.PATCH
- MAJOR: mudanças incompatíveis ou reorganização significativa
- MINOR: novas funcionalidades compatíveis
- PATCH: correcções e pequenas melhorias
