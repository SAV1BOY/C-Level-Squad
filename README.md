# C-Level Squad — MMOS

> **O C-Level Squad mais completo e pragmático possível.**
> 8 agentes executivos | Sistema operacional de negócios | Gold Standard / SOTA

---

## O que é o C-Level Squad?

O C-Level Squad é um **sistema operacional executivo** que transforma visão em execução através de 8 agentes de IA especializados (6 C-Level + CFO + Squad Coordinator), operando com frameworks, checklists, templates e workflows integrados.

**Não é um conjunto de opiniões.** É um sistema onde:
- Toda decisão vira **registro + métrica + dono**
- Toda cadência tem **agenda + dados + decisões + follow-ups**
- Todo handoff tem **contrato: inputs/outputs, DoD/DoR, SLAs**
- Toda iniciativa tem **kill criteria definidos antes de iniciar**

---

## Os 8 Agentes

| Agente | Papel | Responsabilidade Principal |
|--------|-------|---------------------------|
| **Vision Chief** | CEO / Diretor Executivo | Direção, tese estratégica, prioridades, kill list, bets |
| **COO Orchestrator** | Diretor de Operações | Sistema operacional, cadência, accountability, execução |
| **CMO Architect** | Diretor de Marketing | GTM, positioning-to-performance, crescimento, receita |
| **CTO Architect** | Diretor de Tecnologia | Arquitetura, DORA, segurança, plataforma, DX |
| **CIO Engineer** | Diretor de Informação | Processos, sistemas, dados, governança, LGPD |
| **CAIO Architect** | Diretor de IA | Estratégia de IA, evals, MLOps, governança, ROI |
| **CFO Strategist** | Diretor Financeiro | Capital allocation, unit economics, cash flow, orçamento |
| **Squad Coordinator** | Coordenador Operacional | Facilitação, alinhamento, tracking, cadência operacional |

---

## Metodologia

### HRM (Hierarchical Reasoning Model)

Cada agente opera em 6 layers:

1. **Constitutional** — Regras imutáveis, limites, autoridade
2. **Identity** — Papel, modelo mental, heurísticas
3. **Operational** — Triggers, handoffs, escalonamento
4. **Competence** — Domínio técnico, ferramentas
5. **Voice** — Tom, formalidade, canal
6. **Meta-Cognitive** — Auto-reflexão, vieses, quality checks

### Prompt Engineering Avançado

- **Chain-of-Thought (CoT)** para raciocínio estruturado
- **Role Prompting** para identidade e expertise
- **Few-Shot Examples** para calibração de output
- **Constitutional AI** para guardrails invioláveis
- **Self-Reflection** para qualidade contínua

---

## Estrutura do Repositório

```
squads/c-level/
├── agents/          # 6 agentes C-Level (HRM)
├── archive/         # Referências históricas
├── authority/       # Construção de autoridade
├── checklists/      # ~110+ quality gates
├── data/            # Memória operacional (registries, metrics)
├── docs/            # Documentação
├── frameworks/      # ~80+ frameworks (tema + proprietários + intelectuais)
├── lib/             # Componentes reutilizáveis
├── phrases/         # Bibliotecas de frases
├── projects/        # Templates de projeto (8 tipos)
├── reference/       # Base de conhecimento (~85+ referências)
├── scripts/         # Automação
├── swipe/           # Exemplos curados
├── swipe-sources/   # Fontes de swipe
├── tasks/           # ~65+ tarefas executáveis
├── templates/       # ~55+ entregáveis padronizados
├── voice/           # Tom e linguagem
├── workflows/       # ~20 playbooks ponta-a-ponta
├── ARCHITECTURE.md  # Constituição do sistema
├── config.yaml      # Cérebro de roteamento
├── README.md        # Este arquivo
└── swipe.config     # Configuração de swipe files
```

**Total: ~780+ arquivos**

---

## Como Funciona

### O Cérebro de Roteamento (`config.yaml`)

Para cada task, o config.yaml define:

```yaml
task-name:
  agents: [quem participa]
  frameworks: [como pensar]
  checklists: [quality gates]
  templates: [formato do output]
  registries: [onde registrar]
```

### Fluxo de Execução

```
Task → Agents → Frameworks → Checklists → Templates → Registries → Metrics → RalphLoop
```

### Cadência Operacional

| Cadência | Frequência | Owner | Template |
|----------|-----------|-------|----------|
| WBR | Semanal | COO | `templates/operating-system/wbr-template.md` |
| MBR | Mensal | COO + Vision Chief | `templates/operating-system/mbr-template.md` |
| QBR | Trimestral | Todos os 6 agentes | `templates/operating-system/qbr-template.md` |
| Annual Planning | Anual | Todos os 6 agentes | `templates/strategy/annual-operating-plan.md` |

---

## Cross-Squad Integration

O C-Level Squad é o **hub central** que conecta 9 squads:

| Squad | C-Level Owner | Relação |
|-------|--------------|---------|
| Brand | CMO | Marca e posicionamento |
| Copy | CMO | Mensagem e conversão |
| Storytelling | CMO + Vision Chief | Narrativa e autoridade |
| Movement | CMO | Comunidade e cultura |
| Traffic | CMO | Aquisição e performance |
| Design | CTO | Experiência e entrega |
| Data | CIO + COO | Métrica e evidência |
| Cybersecurity | CIO + CTO | Risco e compliance |
| Advisory | Vision Chief | Orientação estratégica |

---

## Quick Start

1. **Leia** `ARCHITECTURE.md` para entender as regras do sistema
2. **Consulte** `config.yaml` para ver o roteamento de qualquer task
3. **Escolha uma task** em `tasks/` que corresponda ao que precisa fazer
4. **Siga o workflow** correspondente em `workflows/`
5. **Use os frameworks** indicados no config.yaml
6. **Passe pelos checklists** (quality gates) antes de finalizar
7. **Preencha o template** do output esperado
8. **Registre** no registry correspondente em `data/registries/`

---

## Princípios Operacionais

1. **Artifacts over opinions** — Se não está escrito, não é decisão
2. **Cadence is the OS** — WBR/MBR/QBR é o sistema operacional
3. **Accountability by default** — Dono, prazo, métrica — sempre
4. **Kill before it kills you** — Kill criteria obrigatório
5. **Cross-squad contracts** — SLAs e handoffs explícitos
6. **AI as leverage** — IA como alavanca real, não buzzword
7. **Compounding decisions** — Decisões que compõem no longo prazo
8. **Evidence over intuition** — Base-rates e dados primeiro
9. **Simplicity by design** — Complexidade é o inimigo

---

## KPIs Principais

| Categoria | KPIs |
|-----------|------|
| **Strategic** | North Star Metric, Bet Success Rate, Moat Strength |
| **Growth** | Revenue Growth, CAC, LTV/CAC, Activation, NRR/GRR |
| **Operational** | Initiative Completion, Decision Lead Time, Action Items |
| **Engineering** | DORA (Deploy Freq, Lead Time, MTTR, Change Fail Rate) |
| **AI** | Use Case ROI, Adoption Rate, Quality Score, Incident Rate |
| **Org Health** | Trust Index, Culture Alignment, Leadership Pipeline, eNPS |

---

## Custo

**R$ 540K/mês** para o squad completo de 6 agentes com profundidade Gold Standard.

---

## Contribuindo

Veja `docs/contribution-guide.md` para convenções e processos.

---

*C-Level Squad — MMOS | Versão 2.0.0*
