# Release Notes - C-Level Squad

> Histórico de releases do repositório C-Level Squad com detalhamento de
> novos conteúdos, melhorias e correções em cada versão.

---

## v2.4.0 - 2026-03-11

### Novos Conteúdos

**Swipe Files**
- `swipe/strategy-decks/` - Análises de decks estratégicos (Airbnb, Buffer)
- `swipe/decision-memos/` - Memos de decisão (Stripe API, Netflix Culture)
- `swipe/org-design/` - Design organizacional (Amazon Two Pizza, Valve Flat)
- `swipe/hiring/` - Processos de contratação (Netflix Keeper, Google HC)
- `swipe/ai-use-cases/` - Casos de uso AI (GitHub Copilot, Duolingo)
- `swipe/tech-architecture/` - Arquitetura técnica (Netflix Chaos, Stripe Versioning)
- `swipe/crisis-comms/` - Comunicação de crise (CrowdStrike 2024)
- `swipe/operating-reviews/` - Reviews operacionais (Amazon WBR, Google OKR)

**Tarefas Operacionais**
- `tasks/operations/` - 5 tarefas operacionais (métricas, strategy review, budget, vendors, compliance)
- `tasks/engineering/` - 5 tarefas de engenharia (tech debt, architecture, security, performance, DR)
- `tasks/ai/` - 5 tarefas de AI (model eval, bias audit, data quality, ethics, ROI)
- `tasks/finance/` - 5 tarefas financeiras (cash flow, unit economics, investor update, variance, close)

**Projetos**
- `projects/digital-transformation/` - 4 fases de transformação digital
- `projects/ai-adoption/` - 4 fases de adoção de AI
- `projects/platform-migration/` - 2 fases de migração de plataforma

**Documentação**
- `docs/architecture-decisions-log.md` - Log de decisões arquiteturais (ADR)
- `docs/release-notes.md` - Este arquivo
- `docs/integration-guide.md` - Guia de integração com ferramentas

### Melhorias
- Estrutura de diretórios expandida para acomodar novos tipos de conteúdo
- Cross-references entre swipe files e frameworks existentes
- Padronização de formato em todos os novos arquivos

---

## v2.3.0 - 2026-02-15

### Novos Conteúdos
- Frameworks decisórios expandidos
- Templates para board presentations
- Checklists de due diligence

### Melhorias
- Reorganização de `/frameworks` por área funcional
- Atualização de referências bibliográficas
- Correções de formatação em templates existentes

---

## v2.2.0 - 2026-01-20

### Novos Conteúdos
- Guias de agentes AI para cada role C-level
- Framework de governança de AI
- Anti-patterns guide para decisões executivas

### Melhorias
- Integração com config.yaml para metadata
- Padronização de headers e estrutura de arquivos
- Glossário expandido com termos de AI

---

## v2.1.0 - 2025-11-01

### Novos Conteúdos
- Workflow guides para processos executivos
- Cross-squad contracts framework
- Gold standard e SOTA reference

### Melhorias
- Onboarding guide revisado e expandido
- FAQ atualizado com perguntas mais frequentes
- Naming conventions documentadas

---

## v2.0.0 - 2025-09-01

### Breaking Changes
- Reestruturação completa de diretórios
- Novo sistema de naming conventions
- Config.yaml como source of truth

### Novos Conteúdos
- Operating system guide
- Decision-making frameworks
- Governance and policies

### Migração
- Conteúdos antigos movidos para `/archive`
- Paths antigos redirecionados via README em cada diretório
- Guia de migração em `/docs/migration-v2.md`

---

## v1.0.0 - 2025-06-01

### Release Inicial
- Estrutura base do repositório
- Frameworks fundamentais (estratégia, operações, finanças)
- Templates iniciais para reuniões e reports
- Documentação de getting started
- Contribution guide

---

## Convenções de Versionamento

O C-Level Squad segue versionamento semântico adaptado:

- **Major (X.0.0):** Mudanças estruturais que afetam navegação ou organização
- **Minor (0.X.0):** Novos conteúdos significativos (frameworks, swipe files, projetos)
- **Patch (0.0.X):** Correções, atualizações menores, typos

## Como Contribuir para Release Notes

Ao contribuir com conteúdo significativo:
1. Adicione uma entrada na seção do release atual (draft)
2. Categorize: Novos Conteúdos, Melhorias, ou Correções
3. Inclua path relativo do arquivo para navegação fácil
4. Mantenha descrições concisas (1 linha por item)
