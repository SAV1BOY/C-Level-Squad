# Workflow 02: Bets-to-Roadmaps — De Apostas Estratégicas a Roadmaps Concretos

## Objetivo

Traduzir as bets estratégicas aprovadas em roadmaps concretos e executáveis,
com decomposição em iniciativas, alocação de recursos, timeline, dependências
mapeadas e riscos avaliados. Este workflow garante que cada aposta ganha um
plano de execução com milestones mensuráveis e kill criteria embutidos.

> **Princípio**: Bet sem roadmap é esperança. Roadmap sem bet é desperdício.

---

## Agentes Envolvidos

| Agente | Papel neste Workflow | Responsabilidade |
|--------|---------------------|-----------------|
| **Vision Chief (CEO)** | Sponsor dos bets | Aprova roadmaps, valida alinhamento com tese |
| **COO Orchestrator** | Líder de decomposição | Coordena timeline, recursos, dependências |
| **CMO Architect** | Owner de bets de growth | Roadmap GTM, canais, aquisição, receita |
| **CTO Architect** | Owner de bets de tech | Roadmap plataforma, arquitetura, engenharia |
| **CIO Engineer** | Suporte de sistemas | Roadmap IT, integrações, dados |
| **CAIO Architect** | Suporte de IA | Roadmap IA, automação, evals |
| **CFO Strategist** | Validador financeiro | Budget allocation, unit economics, ROI projetado |
| **Squad Coordinator** | Facilitador | Documentação, tracking, follow-up |

---

## Trigger (quando iniciar)

- **Cadência regular**: Após conclusão do Workflow 01 (Vision-to-OKRs)
- **Evento excepcional**: Nova bet aprovada mid-quarter
- **Frequência**: Trimestral (com atualizações mensais no MBR)
- **Quem dispara**: COO Orchestrator após OKRs aprovados

---

## Pré-condições

- [ ] Bets estratégicas aprovadas (1-3 bets ativos)
- [ ] OKRs de empresa e área definidos (Workflow 01 concluído)
- [ ] Budget do período confirmado pelo CFO
- [ ] Capacidade de time mapeada (headcount disponível)
- [ ] Stack tecnológico atual documentado
- [ ] Dados de performance de iniciativas anteriores disponíveis
- [ ] Kill criteria definidos para cada bet

---

## Processo (step-by-step com decision points)

### FASE 1: Decomposição de Bets (Semana 1)

**Step 1.1 — Bet Deep Dive**

- DRI: Owner do bet (C-Level responsável)
- Framework: `frameworks/vision-chief/vision-chief-strategic-thesis.md`
- Processo (para cada bet):
  1. Revisitar a tese por trás do bet
  2. Definir o "Win Condition": como sabemos que ganhamos?
  3. Mapear premissas: o que precisa ser verdade para funcionar?
  4. Identificar incógnitas: o que não sabemos ainda?
  5. Listar experimentos necessários para validar premissas
- Output: Bet Deep Dive Document (1-2 páginas por bet)

**Step 1.2 — Decomposição em Iniciativas**

- DRI: COO Orchestrator + Owner do bet
- Framework: `frameworks/coo-orchestrator/coo-execution-engine.md`
- Processo:
  1. Para cada bet, identificar 3-7 iniciativas necessárias
  2. Cada iniciativa deve ter:
     - Nome claro e descritivo
     - Descrição em 1-2 frases
     - Owner (DRI)
     - Tipo: Build / Buy / Partner / Optimize
     - Horizonte: H1 (0-3 meses) / H2 (3-6 meses) / H3 (6-12 meses)
  3. Classificar iniciativas por dependência sequencial
  4. Identificar "Must Win Battles": as 2-3 iniciativas sem as quais o bet falha
- **Decision Point**: Há mais de 7 iniciativas por bet?
  - **SIM** → Cortar ou agrupar. Se não cabe em 7, está mal definido.
  - **NÃO** → Avançar para Step 1.3

**Step 1.3 — RICE Scoring**

- DRI: COO Orchestrator
- Framework: Scoring RICE adaptado
- Para cada iniciativa, pontuar:

| Dimensão | Descrição | Escala |
|----------|-----------|--------|
| **Reach** | Quantos clientes/users impacta? | 1-10 |
| **Impact** | Qual o tamanho do impacto por pessoa? | 0.25 / 0.5 / 1 / 2 / 3 |
| **Confidence** | Quão confiantes estamos na estimativa? | 10% / 50% / 80% / 100% |
| **Effort** | Quantas pessoas-mês necessárias? | 0.5 / 1 / 2 / 3 / 5+ |

- Fórmula: `RICE = (Reach × Impact × Confidence) / Effort`
- Processo:
  1. Cada owner pontua suas iniciativas
  2. COO consolida e rank
  3. Top 3-5 por bet avançam para roadmap detalhado
  4. Restantes vão para backlog priorizado
- Output: Tabela RICE com ranking

**Step 1.4 — Mapeamento nos Three Horizons**

- DRI: Vision Chief
- Framework: `frameworks/vision-strategy/three-horizons.md`
- Processo:
  1. Plotar todas as iniciativas nos 3 horizontes:
     - **H1 — Core (70% dos recursos)**: Melhorar o que já funciona
     - **H2 — Adjacente (20% dos recursos)**: Expandir para novo segmento/produto
     - **H3 — Transformacional (10% dos recursos)**: Apostar no futuro
  2. Verificar distribuição de recursos
  3. Ajustar se necessário
- **Decision Point**: A distribuição está equilibrada (70/20/10 ± 10%)?
  - **SIM** → Avançar
  - **NÃO** → Rebalancear com Vision Chief

### FASE 2: Construção dos Roadmaps (Semana 2)

**Step 2.1 — Roadmap por Bet**

- DRI: Owner do bet
- Template: `templates/tech/roadmap-template.md`
- Checklist: `checklists/roadmap-quality.md`
- Estrutura do roadmap:

```
BET: [Nome do Bet]
Owner: [DRI]
Horizonte: [H1/H2/H3]
Budget: R$ [valor]
Kill Criteria: [condição de parada]

MÊS 1:
  - Iniciativa A: [descrição] | Owner: [nome] | KR: [métrica]
  - Iniciativa B: [descrição] | Owner: [nome] | KR: [métrica]

MÊS 2:
  - Iniciativa C: [descrição] | Owner: [nome] | KR: [métrica]
  - Milestone: [decisão go/no-go baseada em dados do mês 1]

MÊS 3:
  - Iniciativa D: [descrição] | Owner: [nome] | KR: [métrica]
  - Milestone: [kill criteria review]

DEPENDÊNCIAS:
  - [lista de dependências cross-area]

RISCOS:
  - [top 3 riscos com mitigação]
```

**Step 2.2 — Mapeamento de Dependências**

- DRI: COO Orchestrator
- Processo:
  1. Para cada iniciativa de cada roadmap:
     - Depende de qual outra iniciativa? (precedência)
     - Depende de qual time/squad? (cross-funcional)
     - Depende de qual recurso externo? (vendor, partner)
  2. Criar grafo de dependências
  3. Identificar caminho crítico
  4. Identificar single points of failure
- **Decision Point**: Há dependências externas não controladas?
  - **SIM** → Criar plano B ou negociar SLA com vendor/partner
  - **NÃO** → Avançar para Step 2.3

**Step 2.3 — Resource Allocation**

- DRI: COO Orchestrator + CFO Strategist
- Processo:
  1. Para cada iniciativa, definir:
     - Headcount necessário (FTEs)
     - Budget direto (R$)
     - Tooling/infraestrutura (R$)
     - Timeline (semanas)
  2. Confrontar com capacidade disponível
  3. Identificar gaps:
     - Gap de headcount → acionar hiring ou realocar
     - Gap de budget → negociar com CFO ou cortar escopo
     - Gap de skills → acionar training ou contractor
  4. Aprovação do CFO para alocação final
- **Decision Point**: Resources disponíveis cobrem o roadmap?
  - **SIM** → Avançar para Fase 3
  - **NÃO** → Cortar escopo (eliminar iniciativas de menor RICE) até caber

**Step 2.4 — Risk Assessment por Roadmap**

- DRI: Owner do bet + COO Orchestrator
- Processo (para cada roadmap):
  1. Identificar top 5 riscos
  2. Para cada risco:
     - Probabilidade: Alta / Média / Baixa
     - Impacto: Alto / Médio / Baixo
     - Mitigação: ação preventiva
     - Contingência: ação se o risco se materializar
     - Owner: DRI da mitigação
  3. Riscos com probabilidade Alta + impacto Alto → escalar para Vision Chief
- Registro: `data/registries/risk-registry.yaml`

### FASE 3: Validação e Aprovação (Semana 3)

**Step 3.1 — Peer Review de Roadmaps**

- DRI: COO Orchestrator
- Participantes: Todos os C-Level
- Duração: 2-3 horas
- Processo:
  1. Cada owner apresenta seu roadmap (15 min por bet)
  2. Grupo faz perguntas e desafia:
     - "O que precisa ser verdade para isso funcionar?"
     - "Se só pudesse fazer 1 coisa, qual seria?"
     - "Qual é o risco que te tira o sono?"
  3. Identificar conflitos de recursos entre roadmaps
  4. Resolver trade-offs (Vision Chief decide se necessário)
- Checklist: `checklists/roadmap-quality.md`

**Step 3.2 — Aprovação do Vision Chief**

- DRI: Vision Chief
- Processo:
  1. Revisar pacote completo: bets → iniciativas → roadmaps → resources → risks
  2. Validar alinhamento com tese e OKRs
  3. Aprovar ou solicitar ajustes
  4. Assinar decisão em `data/registries/decision-registry.yaml`
- **Decision Point**: Roadmaps aprovados?
  - **SIM** → Ativar execução
  - **NÃO** → Iterar (máximo 2 rounds de revisão)

**Step 3.3 — CFO Sign-off Financeiro**

- DRI: CFO Strategist
- Processo:
  1. Validar que alocação total não excede budget aprovado
  2. Verificar unit economics das iniciativas (ROI projetado)
  3. Confirmar que burn rate está dentro do planejado
  4. Aprovar formalmente o budget por roadmap
- Checklist: `checklists/capital-allocation-quality.md`

### FASE 4: Ativação e Comunicação (Semana 4)

**Step 4.1 — Registro e Publicação**

- DRI: Squad Coordinator
- Processo:
  1. Registrar roadmaps em `data/registries/initiative-registry.yaml`
  2. Atualizar `data/registries/okr-registry.yaml` com mapeamento OKR → iniciativa
  3. Publicar roadmaps para squads envolvidos
  4. Configurar tracking de milestones no WBR
- Template: `templates/tech/roadmap-template.md`

**Step 4.2 — Kick-off por Bet**

- DRI: Owner do bet
- Processo (para cada bet):
  1. Reunião de kick-off com todos os envolvidos
  2. Compartilhar: contexto, roadmap, dependências, kill criteria
  3. Confirmar owners e deadlines
  4. Alinhar cadência de check-in (semanal ou quinzenal)
  5. Identificar first milestone (próximos 2-3 semanas)
- Output: Ata de kick-off com action items

**Step 4.3 — Integração com Cadência Operacional**

- DRI: COO Orchestrator
- Processo:
  1. Adicionar milestones do roadmap ao WBR dashboard
  2. Configurar alertas de milestone missed
  3. Definir check-points mensais de roadmap no MBR
  4. Agendar revisão completa de roadmap no próximo QBR
- Referência: `frameworks/operating-system/wbr-mbr-qbr.md`

---

## Quality Gates

### Gate 1: Qualidade da Decomposição

- [ ] Cada bet tem 3-7 iniciativas (não mais, não menos)
- [ ] Cada iniciativa tem owner, timeline e KR mensurável
- [ ] RICE scoring aplicado a todas as iniciativas
- [ ] Must Win Battles identificadas (2-3 por bet)
- [ ] Distribuição Three Horizons equilibrada (70/20/10 ± 10%)

### Gate 2: Qualidade do Roadmap

Aplicar `checklists/roadmap-quality.md`:
- [ ] Timeline realista (baseada em velocidade histórica)
- [ ] Dependências mapeadas com caminho crítico identificado
- [ ] Resources alocados e confirmados
- [ ] Kill criteria embutidos em milestones
- [ ] Go/no-go decision points a cada mês
- [ ] Budget aprovado pelo CFO
- [ ] Riscos top 5 documentados com mitigação

### Gate 3: Alinhamento Estratégico

- [ ] Cada roadmap contribui para pelo menos 1 OKR de empresa
- [ ] Nenhuma iniciativa contradiz a kill list
- [ ] Roadmaps são complementares (não competem por recursos)
- [ ] Vision Chief aprovou todos os roadmaps
- [ ] Cross-squad handoffs definidos

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| Bet Deep Dive (por bet) | Markdown | `data/memos/` | Owner do bet |
| Tabela RICE consolidada | Markdown | `data/memos/` | COO |
| Roadmap por bet (1-3) | Markdown | `data/memos/` | Owner do bet |
| Mapa de dependências | Markdown | `data/memos/` | COO |
| Resource allocation | YAML | `data/registries/initiative-registry.yaml` | COO + CFO |
| Risk register atualizado | YAML | `data/registries/risk-registry.yaml` | COO |
| Ata de kick-off | Markdown | `data/meeting-minutes/` | Squad Coordinator |

---

## Registries Atualizados

- `data/registries/initiative-registry.yaml` — Iniciativas com roadmap, owner, timeline, RICE
- `data/registries/okr-registry.yaml` — Mapeamento OKR → iniciativa
- `data/registries/risk-registry.yaml` — Riscos por roadmap
- `data/registries/decision-registry.yaml` — Decisões de priorização e trade-offs
- `data/registries/metric-registry.yaml` — Métricas de milestone tracking

---

## Próximos Passos

1. **Imediato**: Tracking semanal via WBR → `workflows/04-wbr-loop.md`
2. **Mensal**: Revisão de saúde das iniciativas no MBR → `workflows/05-mbr-loop.md`
3. **Trimestral**: Revisão completa de roadmap no QBR → `workflows/06-qbr-loop.md`
4. **Se iniciativa falha**: Acionar kill review → `workflows/03-kill-list-and-sunsetting.md`
5. **Se novo bet surge**: Re-executar este workflow para o novo bet

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| Owner do bet | Squads executores | Roadmap + briefing + KRs | 48h após kick-off |
| COO | Data Squad | Milestones para tracking | 24h |
| CMO | Traffic Squad | Growth roadmap + budget | 48h |
| CMO | Brand Squad | Positioning roadmap | 48h |
| CMO | Copy Squad | Messaging roadmap | 48h |
| CTO | Design Squad | Product roadmap | 48h |
| CIO | Cybersecurity | Compliance checkpoints | 1 semana |
| CAIO | Data Squad | AI data requirements | 48h |
| CFO | Todos owners | Budget allocation confirmada | 24h após aprovação |

### Formato de Handoff para Squads

```yaml
roadmap_handoff:
  from: "[C-Level owner]"
  to: "[squad]"
  bet: "[nome do bet]"
  iniciativas_relevantes: ["lista de iniciativas que o squad toca"]
  krs_esperados: ["métricas de contribuição"]
  timeline: "[mês/semana]"
  budget_alocado: "R$ [valor]"
  dependencias: ["o que o squad precisa de outros"]
  kill_criteria: "[condição de parada]"
  check_in: "[cadência: semanal/quinzenal]"
  escalation: "COO Orchestrator"
```
