# ARCHITECTURE.md — Constituição do C-Level Squad

> **Este documento é a "constituição" do C-Level Squad.**
> Toda decisão de design, convenção, padrão e regra operacional está aqui.
> Se não está neste documento, não é padrão — é opinião.

---

## 1. VISÃO DO SISTEMA

O C-Level Squad é um **sistema operacional executivo** — não um conjunto de opiniões.
Ele transforma visão em execução através de uma cadeia rigorosa:

```
Visão → Tese → Bets → OKRs → Roadmaps → Tasks → Execution → Metrics → Learning
```

### 1.1 O que torna este C-Level SOTA (State of the Art)

| Dimensão | Abordagem Comum | Abordagem C-Level Squad |
|----------|----------------|------------------------|
| Decisão | Reunião + conversa | Memo + trade-offs + owner + registry |
| Cadência | Ad-hoc | WBR/MBR/QBR com agenda, dados e decisões |
| Accountability | "A gente combinou" | DRI + deadline + métrica + checklist |
| Aprendizado | Pós-mortem quando dá | RalphLoop: registrar → medir → retroalimentar |
| Cross-squad | "Manda no Slack" | Contratos: inputs/outputs, DoD/DoR, SLAs |
| IA | "Usamos ChatGPT" | Portfólio de IA: evals, guardrails, ROI medido |
| Kill | "Vamos esperar mais" | Kill criteria definidos antes de iniciar |

### 1.2 Princípio Fundacional

> **Se não vira registro + métrica + dono, não é decisão — é conversa.**

---

## 2. METODOLOGIA HRM (Hierarchical Reasoning Model)

### 2.1 O que é HRM

O HRM (Hierarchical Reasoning Model) é uma arquitetura inspirada no cérebro humano que processa problemas através de raciocínio hierárquico em múltiplas escalas de tempo:

- **Módulo de alto nível**: Planejamento estratégico lento e abstrato
- **Módulo de baixo nível**: Computação detalhada e rápida com feedback
- **Loop de retroalimentação**: Interação dinâmica entre planejamento e execução

### 2.2 Aplicação ao C-Level Squad

Cada agente do C-Level Squad opera em duas camadas simultâneas:

```
┌─────────────────────────────────────────────┐
│  HIGH-LEVEL (Estratégico)                   │
│  → Visão, tese, bets, prioridades           │
│  → Decisões Type 1 (irreversíveis)          │
│  → Planejamento trimestral/anual            │
│  → Cadência: QBR, Annual Planning           │
├─────────────────────────────────────────────┤
│  LOW-LEVEL (Operacional)                    │
│  → Execução, tasks, checklists              │
│  → Decisões Type 2 (reversíveis)            │
│  → Monitoramento semanal/diário             │
│  → Cadência: WBR, Daily Standups            │
└─────────────────────────────────────────────┘
         ↕ FEEDBACK LOOP (RalphLoop)
```

### 2.3 Estrutura de 6 Layers para Agentes

Todo agente segue exatamente 6 layers:

| Layer | Nome | Propósito | Técnica de PE |
|-------|------|-----------|--------------|
| 1 | **Constitutional** | Regras imutáveis, limites éticos, autoridade | Constitutional AI |
| 2 | **Identity** | Papel, modelo mental, heurísticas de decisão | Role Prompting |
| 3 | **Operational** | Triggers, cadeia de comando, handoffs | Chain-of-Thought |
| 4 | **Competence** | Domínio técnico, ferramentas, cross-squad | Few-Shot Examples |
| 5 | **Voice** | Tom, formalidade, padrões linguísticos | Style Transfer |
| 6 | **Meta-Cognitive** | Auto-reflexão, vieses, quality checks | Self-Reflection |

### 2.4 Técnicas de Prompt Engineering Embarcadas

| Técnica | Aplicação no C-Level Squad |
|---------|---------------------------|
| **Chain-of-Thought (CoT)** | "Antes de responder: 1) contexto, 2) stakeholders, 3) riscos, 4) alternativas, 5) recomendação" |
| **Role Prompting** | Cada agente tem identidade, expertise e voz únicos |
| **Few-Shot Examples** | 2-3 exemplos por cenário-chave em cada agente |
| **Constitutional AI** | Regras que NUNCA podem ser violadas (Layer 1) |
| **Tree-of-Thought** | Para decisões Type 1: explorar múltiplos caminhos antes de decidir |
| **Self-Reflection** | "Revise sua resposta contra: [checklist-reference]" |
| **Tool-Use Instructions** | "Para [cenário], use [framework] + [checklist] + [template]" |
| **Structured Output** | Todos os outputs seguem templates padronizados |

---

## 3. HIERARQUIA DE AGENTES

```
                    ┌──────────────────┐
                    │   VISION CHIEF   │
                    │  (CEO/Fundador)  │
                    └───────┬──────────┘
            ┌───────────────┼───────────────┐
            │               │               │
     ┌──────┴─────┐  ┌─────┴──────┐  ┌─────┴──────┐
     │    COO     │  │    CMO     │  │    CTO     │
     │Orchestrator│  │  Architect │  │  Architect │
     └──────┬─────┘  └────────────┘  └─────┬──────┘
            │                               │
     ┌──────┴─────┐                  ┌──────┴─────┐
     │    CIO     │                  │    CAIO    │
     │  Engineer  │                  │  Architect │
     └────────────┘                  └────────────┘
```

### 3.1 Regras de Autoridade

| Nível | Quem Decide | Exemplos |
|-------|------------|----------|
| **Type 1 (irreversível)** | Vision Chief (com input dos outros) | Pivotar, fechar produto, contratação C-Level |
| **Type 2 (reversível, estratégico)** | Agente responsável + Vision Chief | Pricing, nova feature, novo canal |
| **Type 2 (reversível, operacional)** | Agente responsável | Sprint planning, vendor selection, SLA |
| **Escalação** | COO Orchestrator → Vision Chief | Bloqueios, conflitos cross-squad, deadlines em risco |

### 3.2 Anti-caos: Quem manda em quê

- **Vision Chief** → direção, "win condition", fronteiras, trade-offs, 1–3 bets
- **COO** → sistema: cadência, donos, prazos, operações, risco operacional
- **CMO** → tese em demanda + receita: GTM, canais, oferta, posicionamento
- **CTO** → tecnologia sustenta o plano: arquitetura, DORA, confiabilidade
- **CIO** → infraestrutura de informação: processos, tooling, dados, LGPD
- **CAIO** → IA cria vantagem: onde, como medir, como implantar, como governar

---

## 4. FLUXO DE DADOS

```
┌──────────┐    ┌────────────┐    ┌────────────┐    ┌───────────┐
│  TASKS   │───→│ FRAMEWORKS │───→│ CHECKLISTS │───→│ TEMPLATES │
│ (o quê)  │    │ (como)     │    │ (gates)    │    │ (output)  │
└──────────┘    └────────────┘    └────────────┘    └─────┬─────┘
                                                          │
                                                          ▼
                                                   ┌────────────┐
                                                   │ REGISTRIES │
                                                   │ (memória)  │
                                                   └──────┬─────┘
                                                          │
                                                          ▼
                                                   ┌────────────┐
                                                   │  METRICS   │
                                                   │ (feedback) │
                                                   └──────┬─────┘
                                                          │
                                                          ▼
                                                   ┌────────────┐
                                                   │ RALPHLOOP  │
                                                   │(aprendizado)│
                                                   └────────────┘
```

### 4.1 Roteamento via config.yaml

O `config.yaml` é o **cérebro de roteamento**. Para cada task:

```yaml
task-name:
  agents: [quem participa]
  frameworks: [como pensar]
  checklists: [quality gates]
  templates: [formato do output]
  registries: [onde registrar]
```

---

## 5. CONVENÇÕES DE NAMING

### 5.1 Diretórios

| Tipo | Padrão | Exemplo |
|------|--------|---------|
| Diretório raiz | `lowercase-hyphenated/` | `frameworks/` |
| Subdiretório temático | `lowercase-hyphenated/` | `frameworks/vision-strategy/` |
| Subdiretório de agente | `agent-name/` | `frameworks/vision-chief/` |

### 5.2 Arquivos

| Tipo | Padrão | Exemplo |
|------|--------|---------|
| Agente | `role-name.md` | `vision-chief.md` |
| Framework | `descriptive-name.md` | `strategy-choice-cascade.md` |
| Checklist | `descriptive-name-quality.md` ou `-audit.md` | `okr-quality.md` |
| Template | `descriptive-name.md` | `quarterly-plan.md` |
| Task | `verb-noun.md` | `run-quarterly-planning.md` |
| Workflow | `NN-descriptive-name.md` | `04-wbr-loop.md` |
| Registry | `descriptive-name.yaml` | `decision-registry.yaml` |
| Voice | `descriptive-name.md` | `strategic-clarity.md` |
| Phrase | `domain-phrases.md` | `strategy-phrases.md` |

### 5.3 Idioma

| Contexto | Idioma | Exemplo |
|----------|--------|---------|
| Texto operacional | PT-BR | "Definir visão e bets estratégicas" |
| Termos técnicos | EN | "OKR", "DORA", "SLO", "CoT", "GTM" |
| Nomes de arquivo | EN | `strategy-choice-cascade.md` |
| Headers em arquivos | PT-BR | "## Processo de Decisão" |
| Métricas e KPIs | EN | `north_star_metric_trend` |

---

## 6. PADRÕES DE CONTEÚDO

### 6.1 Estrutura Obrigatória por Tipo de Arquivo

#### Agentes (`agents/*.md`)
```markdown
# [Nome do Agente]

## Layer 1: Constitutional (Regras Imutáveis)
## Layer 2: Identity (Identidade e Modelo Mental)
## Layer 3: Operational (Protocolos Operacionais)
## Layer 4: Competence (Competências Técnicas)
## Layer 5: Voice (Tom e Linguagem)
## Layer 6: Meta-Cognitive (Auto-reflexão)
## Prompt de Ativação
## Few-Shot Examples
```

#### Frameworks (`frameworks/**/*.md`)
```markdown
# [Nome do Framework]

## Origem e Contexto
## Quando Usar
## Quando NÃO Usar
## Estrutura / Modelo
## Processo de Aplicação (step-by-step)
## Exemplos Práticos
## Armadilhas Comuns
## Integração com Outros Frameworks
## Referências
```

#### Checklists (`checklists/**/*.md`)
```markdown
# [Nome do Checklist]

## Propósito
## Quando Aplicar
## Agente Responsável
## Checklist
- [ ] Item 1: [descrição clara]
- [ ] Item 2: [descrição clara]
...
## Critérios de Aprovação
## O que Fazer se Falhar
## Referências
```

#### Templates (`templates/**/*.md`)
```markdown
# [Nome do Template]

## Propósito
## Quando Usar
## Agente Responsável
## Template
[Estrutura completa com placeholders]
## Instruções de Preenchimento
## Exemplo Preenchido
## Checklist de Qualidade
```

#### Tasks (`tasks/**/*.md`)
```markdown
# [Nome da Task]

## Objetivo
## Agente Responsável
## Agentes de Suporte
## Pré-requisitos
## Processo (step-by-step)
## Frameworks a Aplicar
## Checklists de Qualidade
## Template de Entrega
## Registries para Atualizar
## Critérios de Aceitação
## Dependências e Handoffs
```

#### Workflows (`workflows/*.md`)
```markdown
# Workflow NN: [Nome]

## Objetivo
## Agentes Envolvidos
## Trigger (quando iniciar)
## Pré-condições
## Processo (step-by-step com decision points)
## Quality Gates
## Outputs / Artefatos
## Registries Atualizados
## Próximos Passos
## Cross-squad Handoffs
```

### 6.2 Profundidade Mínima

| Tipo | Mínimo de Linhas | Observação |
|------|-----------------|------------|
| Agente | 400 | 6 layers + prompt + few-shot |
| Framework | 150 | Teoria + processo + exemplos |
| Checklist | 80 | Items + critérios + instruções |
| Template | 100 | Estrutura + instruções + exemplo |
| Task | 120 | Processo + referências + critérios |
| Workflow | 250 | Orquestração completa com gates |
| Voice | 80 | Tom + exemplos + calibração |
| Reference | 100 | Resumo + takeaways + aplicação |

---

## 7. RESOLUÇÃO DE CONFLITOS

### 7.1 Cadeia de Escalonamento

```
Nível 1: Agentes resolvem entre si (decisão Type 2)
  ↓ (se não resolve em 48h)
Nível 2: COO Orchestrator medeia
  ↓ (se não resolve em 24h)
Nível 3: Vision Chief decide (decisão final)
  ↓ (se impacta board/investidores)
Nível 4: Advisory Board consulta
```

### 7.2 Regras de Desempate

1. **Dados vencem opiniões** — quem tem evidência, tem a palavra
2. **Reversibilidade decide velocidade** — Type 2 (reversível) = decide rápido, Type 1 = delibere
3. **Owner decide** — o DRI tem a última palavra no seu domínio
4. **Kill criteria são inegociáveis** — se não passou no gate, não passa

---

## 8. CROSS-SQUAD PROTOCOL

### 8.1 Contrato de Handoff

Todo handoff entre squads deve seguir:

```yaml
handoff:
  from: [squad de origem]
  to: [squad de destino]
  input: [o que está sendo entregue]
  format: [template/formato esperado]
  dod: [Definition of Done — quando o input está "pronto"]
  dor: [Definition of Ready — quando o destino está "pronto para receber"]
  sla: [prazo máximo]
  owner: [DRI do handoff]
  escalation: [o que fazer se SLA estourar]
```

### 8.2 Squads Integrados

| Squad | C-Level Owner | Relação |
|-------|--------------|---------|
| Brand | CMO | Braço de marca e posicionamento |
| Copy | CMO | Braço de mensagem e conversão |
| Story | CMO + Vision Chief | Braço de narrativa e autoridade |
| Movement | CMO | Braço de comunidade e cultura |
| Traffic | CMO | Braço de aquisição e performance |
| Design | CTO | Ponte de experiência e entrega |
| Data | CIO + COO | Braço de métrica e evidência |
| Cyber | CIO + CTO | Gate de risco e compliance |
| Advisory | Vision Chief | Conselho de orientação estratégica |

---

## 9. RALPHLOOP — SISTEMA DE APRENDIZADO

O RalphLoop é o mecanismo que garante que o C-Level Squad **aprende e melhora**:

```
┌─────────┐    ┌─────────┐    ┌──────────┐    ┌──────────┐
│ REGISTRAR│───→│  MEDIR  │───→│ ANALISAR │───→│ AJUSTAR  │
│ decisão  │    │ resultado│    │ gap vs   │    │ processo │
│ no       │    │ real vs  │    │ esperado │    │ framework│
│ registry │    │ previsto │    │          │    │ checklist│
└─────────┘    └─────────┘    └──────────┘    └──────┬───┘
      ↑                                              │
      └──────────────────────────────────────────────┘
                    LOOP CONTÍNUO
```

### 9.1 Onde o RalphLoop se materializa

- `data/registries/lessons-learned.yaml` — repositório central de aprendizados
- `data/registries/decision-registry.yaml` — decisões com outcome tracking
- `checklists/ralphloop-quality.md` — gate para garantir que o loop foi executado
- `workflows/18-decision-quality-review.md` — revisão trimestral de qualidade de decisões
- `workflows/20-postmortem-and-learning.md` — pós-mortem e incorporação de aprendizado

---

## 10. VERSIONAMENTO E EVOLUÇÃO

### 10.1 Semantic Versioning

- **Major** (X.0.0): Mudança na estrutura de agentes ou arquitetura fundamental
- **Minor** (0.X.0): Novo framework, checklist, workflow ou template
- **Patch** (0.0.X): Correção de conteúdo, atualização de referência

### 10.2 Changelog

Toda alteração é registrada em `docs/changelog.md` com:
- Data
- Tipo (added/changed/removed/fixed)
- Descrição
- Impacto (quais agentes/workflows afetados)

---

## 11. GLOSSÁRIO RÁPIDO

| Termo | Definição |
|-------|----------|
| **Bet** | Aposta estratégica com prazo, owner e kill criteria |
| **DRI** | Directly Responsible Individual — o dono |
| **DoD** | Definition of Done — quando algo está "pronto" |
| **DoR** | Definition of Ready — quando algo está "pronto para começar" |
| **Gate** | Checklist obrigatório antes de avançar |
| **HRM** | Hierarchical Reasoning Model — arquitetura dos agentes |
| **Kill List** | Lista de coisas que decidimos NÃO fazer |
| **NSM** | North Star Metric — métrica principal do negócio |
| **RalphLoop** | Sistema de aprendizado: registrar → medir → retroalimentar |
| **Type 1** | Decisão irreversível — delibere com cuidado |
| **Type 2** | Decisão reversível — decida rápido |
| **WBR/MBR/QBR** | Weekly/Monthly/Quarterly Business Review |
