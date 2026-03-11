# Log de Decisões Arquiteturais (ADR Log)

> Registro centralizado de todas as decisões arquiteturais do C-Level Squad,
> seguindo o formato ADR (Architecture Decision Record) para garantir rastreabilidade.

## Como Usar Este Log

Cada decisão arquitetural segue o formato:
- **ID:** Identificador sequencial
- **Data:** Data da decisão
- **Status:** Proposta | Aceita | Deprecated | Substituída
- **Contexto:** Por que a decisão foi necessária
- **Decisão:** O que decidimos
- **Consequências:** O que muda com essa decisão
- **Responsável:** Quem tomou a decisão final

---

## ADR-001: Estrutura de Diretórios do Repositório

- **Data:** 2024-01-15
- **Status:** Aceita
- **Contexto:** O repositório precisava de uma estrutura que acomodasse frameworks,
  templates, swipe files, tarefas e projetos de forma organizada e navegável.
  A estrutura precisava ser intuitiva para novos usuários e escalável para
  centenas de arquivos.
- **Decisão:** Adotar estrutura hierárquica por tipo de conteúdo:
  - `/frameworks` - Frameworks decisórios e analíticos
  - `/templates` - Templates reutilizáveis
  - `/swipe` - Exemplos e análises de referência
  - `/tasks` - Tarefas operacionais recorrentes
  - `/projects` - Projetos multi-fase
  - `/docs` - Documentação do repositório
  - `/scripts` - Automações e ferramentas
  - `/data` - Dados de referência
- **Consequências:**
  - Novos conteúdos devem ser categorizados no diretório correto
  - Conteúdos que cruzam categorias devem usar cross-references
  - README de cada diretório deve explicar o propósito e conteúdo
- **Responsável:** Equipe fundadora

---

## ADR-002: Idioma Principal - Português Brasileiro

- **Data:** 2024-01-15
- **Status:** Aceita
- **Contexto:** O público-alvo principal são executivos C-level no Brasil.
  Conteúdo em inglês criaria barreira de adoção. Termos técnicos em inglês
  são aceitáveis quando não há tradução natural estabelecida.
- **Decisão:** Todo conteúdo em português brasileiro. Termos técnicos sem
  tradução natural mantidos em inglês (ex: "stakeholder", "framework", "sprint").
- **Consequências:**
  - Contribuições em outros idiomas precisam ser traduzidas
  - Glossário de termos técnicos mantido em `/docs/glossary.md`
  - Referências podem ser em inglês com contexto em português
- **Responsável:** Equipe fundadora

---

## ADR-003: Formato de Conteúdo - Markdown

- **Data:** 2024-01-20
- **Status:** Aceita
- **Contexto:** Precisávamos de um formato que fosse legível como texto puro,
  versionável com Git, renderizável em GitHub e acessível sem ferramentas especiais.
- **Decisão:** Todo conteúdo em Markdown (`.md`). Diagramas em Mermaid quando
  necessário. Dados tabulares em Markdown tables ou CSV em `/data`.
- **Consequências:**
  - Formatação limitada ao que Markdown suporta
  - Sem conteúdo em Word, PowerPoint ou PDF no repositório
  - Ferramentas de edição: qualquer editor de texto funciona
- **Responsável:** Equipe fundadora

---

## ADR-004: Filosofia de Conteúdo - Acionável sobre Teórico

- **Data:** 2024-02-01
- **Status:** Aceita
- **Contexto:** A maioria dos recursos para executivos é teórica demais.
  O C-Level Squad deve ser prático e imediatamente utilizável.
- **Decisão:** Todo conteúdo deve incluir pelo menos um de:
  - Checklist acionável
  - Template preenchível
  - Framework aplicável
  - Exemplo real analisado
  Conteúdo puramente teórico sem componente prático não é aceito.
- **Consequências:**
  - Cada arquivo deve ter seção de "como aplicar" ou equivalente
  - Contribuições teóricas devem incluir componente prático
  - Review de PRs deve verificar acionabilidade
- **Responsável:** Equipe fundadora

---

## ADR-005: Swipe Files como Referência, Não Como Cópia

- **Data:** 2024-02-15
- **Status:** Aceita
- **Contexto:** Swipe files são referências de empresas reais. Precisávamos
  definir o propósito: inspiração e análise, não cópia literal.
- **Decisão:** Cada swipe file deve incluir:
  1. Contexto da empresa e situação
  2. Análise do que foi feito e por quê
  3. Resultados mensuráveis quando disponíveis
  4. Lições aplicáveis para outros contextos
  5. Referências para aprofundamento
- **Consequências:**
  - Swipe files não são transcrições de documentos originais
  - Análise crítica é obrigatória (prós e contras)
  - Fontes devem ser citadas
- **Responsável:** Equipe fundadora

---

## ADR-006: Sistema de Tarefas - Cadência Operacional

- **Data:** 2024-03-01
- **Status:** Aceita
- **Contexto:** Executivos precisam de templates para tarefas recorrentes
  organizados por cadência (diária, semanal, mensal, trimestral, anual).
- **Decisão:** Tarefas organizadas por área funcional em `/tasks`:
  - `/tasks/operations` - Operações gerais
  - `/tasks/engineering` - Engenharia e tecnologia
  - `/tasks/ai` - AI e machine learning
  - `/tasks/finance` - Finanças e controle
  Cada tarefa inclui: objetivo, frequência, responsáveis, checklist, métricas.
- **Consequências:**
  - Novas tarefas devem seguir o template estabelecido
  - Tarefas devem especificar cadência e duração estimada
  - Cross-references entre tarefas relacionadas são encorajadas
- **Responsável:** Equipe fundadora

---

## ADR-007: Projetos Multi-Fase

- **Data:** 2024-03-15
- **Status:** Aceita
- **Contexto:** Alguns conteúdos representam projetos complexos com múltiplas fases.
  Precisavam de estrutura diferente de tarefas recorrentes.
- **Decisão:** Projetos em `/projects/{nome-do-projeto}/` com arquivos numerados:
  - `01-fase.md`, `02-fase.md`, etc.
  - Cada fase é auto-contida mas referencia as demais
  - Fase inclui: objetivos, atividades, deliverables, critérios de saída
- **Consequências:**
  - Projetos devem ter pelo menos 3 fases
  - Cada fase deve ter critérios claros de conclusão
  - Gate reviews entre fases são recomendados
- **Responsável:** Equipe fundadora

---

## ADR-008: Versionamento e Changelog

- **Data:** 2024-04-01
- **Status:** Aceita
- **Contexto:** Com múltiplos contribuidores, precisávamos de rastreabilidade
  de mudanças significativas.
- **Decisão:** Manter changelog em `/docs/changelog.md` com entradas para:
  - Novos frameworks ou templates
  - Mudanças significativas em conteúdo existente
  - Novos swipe files ou projetos
  - Não logar correções menores (typos, formatação)
- **Consequências:**
  - Contribuidores devem atualizar changelog para adições significativas
  - Formato: data + tipo de mudança + descrição breve
  - Git log complementa mas não substitui o changelog
- **Responsável:** Equipe fundadora

---

## ADR-009: Integração com Agentes AI

- **Data:** 2024-06-01
- **Status:** Aceita
- **Contexto:** O repositório pode ser consumido tanto por humanos quanto por
  agentes AI (como assistentes de C-level). A estrutura precisa ser AI-friendly.
- **Decisão:**
  - Arquivos devem ter headers claros e hierárquicos (H1, H2, H3)
  - Checklists em formato parseable (- [ ] item)
  - Metadata quando relevante (tags, categorias)
  - Conteúdo auto-explicativo (sem dependência de contexto externo)
- **Consequências:**
  - Conteúdo deve ser compreensível sem ler outros arquivos
  - Cross-references devem incluir contexto suficiente
  - Formatação consistente facilita parsing automático
- **Responsável:** Equipe fundadora

---

## ADR-010: Configuração Central

- **Data:** 2024-07-01
- **Status:** Aceita
- **Contexto:** Configurações do repositório (estrutura, regras, metadata)
  precisavam de um local central.
- **Decisão:** Configuração em `/config.yaml` com:
  - Estrutura de diretórios e propósitos
  - Regras de contribuição
  - Metadata do repositório
- **Consequências:**
  - Mudanças estruturais devem ser refletidas no config
  - Ferramentas de automação podem consumir o config
  - Config é a source of truth para estrutura do repo
- **Responsável:** Equipe fundadora

---

## Template para Novas ADRs

```markdown
## ADR-XXX: [Título da Decisão]

- **Data:** YYYY-MM-DD
- **Status:** Proposta | Aceita | Deprecated | Substituída por ADR-YYY
- **Contexto:** [Por que essa decisão é necessária]
- **Decisão:** [O que decidimos]
- **Consequências:** [O que muda, prós e contras]
- **Responsável:** [Quem tomou a decisão]
```

## Índice de ADRs

| ID | Título | Status | Data |
|----|--------|--------|------|
| 001 | Estrutura de Diretórios | Aceita | 2024-01-15 |
| 002 | Idioma Principal | Aceita | 2024-01-15 |
| 003 | Formato Markdown | Aceita | 2024-01-20 |
| 004 | Acionável sobre Teórico | Aceita | 2024-02-01 |
| 005 | Swipe Files como Referência | Aceita | 2024-02-15 |
| 006 | Sistema de Tarefas | Aceita | 2024-03-01 |
| 007 | Projetos Multi-Fase | Aceita | 2024-03-15 |
| 008 | Versionamento e Changelog | Aceita | 2024-04-01 |
| 009 | Integração com Agentes AI | Aceita | 2024-06-01 |
| 010 | Configuração Central | Aceita | 2024-07-01 |
