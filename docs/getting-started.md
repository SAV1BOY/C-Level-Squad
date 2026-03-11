# Getting Started — C-Level Squad OS

> Como começar a utilizar o C-Level Squad Operating System.

---

## Bem-vindo

O C-Level Squad OS é um sistema operacional organizacional desenhado para
coordenar a actuação de agentes de AI que desempenham funções executivas
(C-Level). Este guia ajuda-te a dar os primeiros passos.

---

## Pré-requisitos

Antes de começar, certifica-te de que tens:

1. **Acesso ao repositório**: clone ou acesso ao directório do C-Level Squad
2. **Compreensão básica de AI agents**: familiaridade com conceitos de agentes autónomos
3. **Contexto organizacional**: conhecimento da empresa ou organização onde será aplicado
4. **Permissões**: acesso de leitura e escrita aos ficheiros do squad
5. **Ferramentas**: editor de texto, terminal, e acesso aos sistemas integrados

---

## Primeiro Contacto — Percurso de 30 Minutos

### Minuto 0-5: Entender a Estrutura
Navega a estrutura de directórios:
```
C-Level-Squad/
├── agents/          → Definições dos 6 agentes
├── frameworks/      → Frameworks de decisão e operação
├── workflows/       → Processos operacionais
├── templates/       → Templates para outputs comuns
├── scripts/         → Scripts de automação
├── docs/            → Documentação (estás aqui)
├── config.yaml      → Configuração central
├── checklists/      → Listas de verificação
├── data/            → Dados operacionais
└── authority/       → Conteúdo de autoridade e referência
```

### Minuto 5-15: Conhecer os Agentes
Lê o ficheiro `docs/agent-roles-guide.md` para entender os 6 agentes:
1. **Vision Chief** (CEO) — Visão e estratégia
2. **COO Orchestrator** — Operações e execução
3. **CMO Architect** — Marketing e crescimento
4. **CTO Architect** — Tecnologia e produto
5. **CIO Engineer** — Informação e sistemas
6. **CAIO Architect** — AI e inovação

### Minuto 15-25: Entender o Operating System
Lê `docs/operating-system.md` para compreender:
- Como os agentes interagem
- Cadência operacional (daily, weekly, monthly, quarterly)
- Fluxos de decisão
- Mecanismos de coordenação

### Minuto 25-30: Explorar um Workflow
Escolhe um workflow em `workflows/` e lê-o do início ao fim.
Isto dá-te uma noção concreta de como o sistema funciona na prática.

---

## Configuração Inicial

### Passo 1 — Personalizar config.yaml
O ficheiro `config.yaml` na raiz contém configurações centrais. Revê e
ajusta para o teu contexto:
- Nome da organização
- Agentes activos
- Cadências operacionais
- Thresholds de alerta
- Integrações com sistemas externos

### Passo 2 — Definir Contexto Organizacional
Cria ou actualiza os ficheiros em `data/` com informação da tua organização:
- Missão e visão
- Objectivos estratégicos actuais
- Estrutura organizacional
- Métricas-chave (KPIs)
- Riscos conhecidos

### Passo 3 — Activar Agentes
Para cada agente que vais utilizar:
1. Lê a definição completa em `agents/[nome].md`
2. Lê o summary em `authority/agent-summaries/[nome]-summary.md`
3. Configura o agente com contexto específico da tua organização
4. Testa com um cenário simples

### Passo 4 — Estabelecer Cadência
Define a cadência operacional inicial:
- **Diária**: standup ou check-in rápido
- **Semanal**: WBR (Weekly Business Review)
- **Mensal**: MBR (Monthly Business Review)
- **Trimestral**: QBR (Quarterly Business Review)

---

## Primeiras Tarefas Recomendadas

Depois da configuração, experimenta estas tarefas por ordem:

1. **Gerar uma agenda de WBR** usando `scripts/generation/agenda-generator.md`
2. **Criar um metrics pack** usando `scripts/generation/metrics-pack-builder.md`
3. **Registar uma decisão** usando o formato de `scripts/tracking/decision-log-updater.md`
4. **Executar um risk scan** usando `scripts/tracking/risk-scan.md`
5. **Correr um workflow completo** escolhendo um de `workflows/`

---

## Modos de Utilização

### Modo Assistido (Recomendado para Início)
- Humano lidera, agentes assistem
- Cada output é revisto antes de ser usado
- Ideal para construir confiança e calibrar
- Duração recomendada: 2-4 semanas

### Modo Colaborativo
- Humano e agentes trabalham em parceria
- Agentes propõem, humano decide
- Outputs usados com revisão ligeira
- Após confiança estabelecida

### Modo Autónomo
- Agentes executam workflows dentro de guardrails
- Humano supervisiona e intervém quando necessário
- Apenas para processos bem testados e calibrados
- Requer governance sólida (ver `docs/ai-governance.md`)

---

## Erros Comuns a Evitar

1. **Tentar usar tudo ao mesmo tempo**: começa com 1-2 agentes e expande gradualmente
2. **Ignorar o contexto**: agentes sem contexto organizacional produzem outputs genéricos
3. **Saltar a calibração**: as primeiras semanas são para ajustar, não para produção
4. **Não registar decisões**: o decision log é fundamental para aprendizagem do sistema
5. **Copiar sem adaptar**: templates são pontos de partida, adapta ao teu contexto
6. **Automatizar demasiado cedo**: primeiro entende o processo manualmente

---

## Recursos Adicionais

| Recurso | Onde Encontrar | Para Quê |
|---------|---------------|----------|
| Overview completo | `docs/c-level-overview.md` | Visão geral do sistema |
| Guia de agentes | `docs/agent-roles-guide.md` | Detalhe de cada agente |
| Framework selection | `docs/framework-selection-guide.md` | Escolher o framework certo |
| Workflow guide | `docs/workflow-guide.md` | Como executar workflows |
| FAQ | `docs/faq.md` | Perguntas frequentes |
| Anti-patterns | `docs/anti-patterns-guide.md` | O que não fazer |
| Glossário | `docs/glossary.md` | Terminologia comum |

---

## Suporte

Se tiveres dúvidas:
1. Consulta o `docs/faq.md`
2. Lê o `docs/glossary.md` para terminologia
3. Revê o `docs/anti-patterns-guide.md` para evitar erros comuns
4. Consulta o `docs/contribution-guide.md` para contribuir com melhorias

---

## Próximos Passos

Depois de completar o getting started:
1. Lê o `docs/onboarding.md` para o processo de onboarding completo
2. Explora os `frameworks/` relevantes para a tua situação
3. Define os primeiros OKRs usando o sistema
4. Agenda a primeira WBR com o squad
5. Começa a construir o histórico de decisões e métricas
