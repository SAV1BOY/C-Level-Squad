# Workflow 03: Kill List & Sunsetting — Encerramento Sistemático de Iniciativas

## Objetivo

Identificar e encerrar sistematicamente iniciativas que não estão entregando
valor, liberando recursos (pessoas, budget, atenção) para bets com maior
potencial. Este workflow combate o viés de sunk cost e garante que "matar"
é uma decisão racional, documentada e comunicada — não um fracasso, mas
disciplina estratégica.

> **Princípio**: "Kill before it kills you." Se não define quando parar,
> não sabe o que está fazendo.

---

## Agentes Envolvidos

| Agente | Papel neste Workflow | Responsabilidade |
|--------|---------------------|-----------------|
| **Vision Chief (CEO)** | Decisor final | Aprova kill decisions, comunica narrativa |
| **COO Orchestrator** | Líder do processo | Coleta dados, coordena review, executa sunsetting |
| **CMO Architect** | Avaliador de growth | Analisa métricas de growth das iniciativas |
| **CTO Architect** | Avaliador técnico | Analisa custo técnico e dívida associada |
| **CIO Engineer** | Avaliador de sistemas | Analisa impacto em sistemas e integrações |
| **CAIO Architect** | Avaliador de IA | Analisa iniciativas de IA e automação |
| **CFO Strategist** | Avaliador financeiro | Analisa burn, ROI, custo de oportunidade |
| **Squad Coordinator** | Facilitador | Documentação, comunicação, tracking |

---

## Trigger (quando iniciar)

- **Cadência regular**: Trimestral (pré-QBR, 2 semanas antes)
- **Evento excepcional**: Iniciativa atinge kill criteria definidos
- **Evento excepcional**: Budget cut forçado
- **Evento excepcional**: Mudança de tese estratégica
- **Quem dispara**: COO Orchestrator (regular) ou Vision Chief (excepcional)

---

## Pré-condições

- [ ] Lista de iniciativas ativas disponível em `data/registries/initiative-registry.yaml`
- [ ] Kill criteria definidos para cada iniciativa (obrigatório desde o início)
- [ ] Dados de performance atualizados (métricas, financeiro, timeline)
- [ ] Budget atual e projeção disponíveis
- [ ] Capacidade de realocar recursos identificada
- [ ] Cultura de "kill sem culpa" reforçada (princípio operacional)

---

## Processo (step-by-step com decision points)

### FASE 1: Identificação de Candidatas (Semana 1)

**Step 1.1 — Scan de Kill Criteria**

- DRI: COO Orchestrator
- Framework: `frameworks/vision-chief/vision-chief-kill-list.md`
- Processo:
  1. Puxar todas as iniciativas ativas de `data/registries/initiative-registry.yaml`
  2. Para cada iniciativa, verificar kill criteria pré-definidos:
     - Métrica abaixo do threshold por X semanas consecutivas?
     - Budget consumido acima de Y% sem resultado proporcional?
     - Timeline estourado em mais de Z semanas?
     - Premissa invalidada por dados novos?
     - Dependência externa que não se materializou?
  3. Marcar como "Candidata a Kill" se qualquer criteria atingido
  4. Marcar como "Watch List" se próximo de atingir (dentro de 20%)
- Output: Lista de candidatas classificadas

**Step 1.2 — Análise de Sunk Cost Awareness**

- DRI: COO Orchestrator + CFO Strategist
- Processo (para cada candidata):
  1. Calcular investimento total até agora:
     - Headcount (horas/FTE)
     - Budget direto consumido
     - Custo de oportunidade estimado
  2. **IMPORTANTE**: Esses números são informativos, NÃO decisivos
  3. Aplicar o teste de sunk cost:
     > "Se estivéssemos começando do zero hoje, com o que sabemos agora,
     > investiríamos nisso? Se a resposta é NÃO, mate."
  4. Calcular custo de continuar vs custo de parar:
     - Continuar: R$ X/mês por Y meses + custo de oportunidade
     - Parar: R$ Z de wind-down + liberação de recursos
- **Decision Point**: O teste de sunk cost indica "não investiria"?
  - **SIM** → Forte candidata a kill (avançar para Fase 2)
  - **NÃO** → Revisar se kill criteria estão calibrados

**Step 1.3 — Coleta de Dados Qualitativos**

- DRI: Squad Coordinator
- Processo:
  1. Entrevistar DRI de cada iniciativa candidata:
     - "O que mudaria sua confiança de sucesso para 70%+?"
     - "Se tivesse que apostar R$ 100K do próprio bolso, apostaria?"
     - "Quanto tempo/budget mais precisa para provar valor?"
  2. Coletar input dos squads envolvidos:
     - Moral do time
     - Aprendizados gerados (mesmo se falhar)
     - Viabilidade técnica atualizada
  3. Documentar perspectivas (sem editoriar)
- Output: Ficha qualitativa por candidata

### FASE 2: Análise e Recomendação (Semana 2)

**Step 2.1 — Kill Review Board**

- DRI: COO Orchestrator
- Participantes: Vision Chief + C-Level owners das iniciativas
- Duração: 2-3 horas
- Processo:
  1. Para cada candidata, apresentar:
     - Dados quantitativos (métricas, financeiro, timeline)
     - Análise de sunk cost
     - Dados qualitativos (DRI, time, aprendizados)
     - Kill criteria atingidos
  2. Classificar em categorias:

| Categoria | Significado | Ação |
|-----------|------------|------|
| **KILL** | Sem perspectiva de recuperação | Encerrar em 2-4 semanas |
| **PIVOT** | A ideia tem valor, execução precisa mudar | Redesenhar em 2 semanas |
| **PROBATION** | Última chance com condições claras | 30 dias com novo kill criteria |
| **CONTINUE** | Dados não justificam encerrar | Manter com monitoramento |

  3. Para cada classificação, documentar:
     - Racional da decisão
     - Votos (quem concordou/discordou)
     - Condições (para PIVOT/PROBATION)
- **Decision Point**: Consenso ou Vision Chief decide?
  - **Consenso** → Documentar e avançar
  - **Sem consenso** → Vision Chief faz a call (Type 1 se irreversível)

**Step 2.2 — Impact Assessment de Kills Aprovados**

- DRI: COO Orchestrator
- Processo (para cada KILL aprovado):
  1. Mapear impacto:
     - Pessoas afetadas (realocação necessária)
     - Sistemas/código afetado (descomissionar?)
     - Clientes afetados (comunicação necessária?)
     - Contratos/vendors afetados (cancelamento?)
     - Outras iniciativas que dependiam desta
  2. Criar plano de wind-down com timeline
  3. Definir DRI do wind-down
  4. Calcular recursos liberados (budget + headcount + atenção)
- Output: Impact assessment por kill

**Step 2.3 — Plano de Realocação de Recursos**

- DRI: COO Orchestrator + CFO Strategist
- Processo:
  1. Consolidar recursos liberados de todos os kills
  2. Propor realocação para:
     - Bets ativos que precisam de reforço
     - Novas iniciativas em pipeline
     - Reserva estratégica (buffer)
  3. CFO valida viabilidade financeira
  4. Vision Chief aprova realocação
- Output: Plano de realocação aprovado

### FASE 3: Comunicação (Semana 3)

**Step 3.1 — Comunicação Interna**

- DRI: Vision Chief + COO Orchestrator
- Processo:
  1. Preparar narrativa de kill (OBRIGATÓRIO):
     - **NÃO é fracasso** → é disciplina estratégica
     - **Aprendizados** → o que aprendemos e como usaremos
     - **Para onde vão os recursos** → reinvestimento em bets melhores
     - **Reconhecimento** → agradecer quem trabalhou na iniciativa
  2. Comunicar para:
     - Time diretamente envolvido (primeiro, presencialmente se possível)
     - C-Level Squad (na próxima cadência)
     - Organização (comunicado geral)
  3. Tom da comunicação:
     - Transparente e honesto
     - Sem culpar indivíduos
     - Focado em aprendizado e futuro
- Template: `templates/decision/kill-decision-memo.md`

**Step 3.2 — Comunicação Externa (se aplicável)**

- DRI: CMO Architect + Vision Chief
- **Decision Point**: A iniciativa matada tem impacto externo?
  - **SIM (clientes, partners)** → Plano de comunicação específico:
    1. Definir mensagem para cada público
    2. Oferecer alternativas/migração
    3. Timeline de transição
    4. FAQ preparado
  - **NÃO** → Skip para Fase 4

### FASE 4: Execução do Sunsetting (Semana 3-4)

**Step 4.1 — Wind-down Técnico**

- DRI: CTO Architect + CIO Engineer
- Processo:
  1. Descomissionar sistemas/serviços (se aplicável)
  2. Migrar dados que serão preservados
  3. Documentar decisões arquiteturais (ADR de sunsetting)
  4. Remover custos recorrentes (infra, licenças, vendors)
  5. Atualizar `data/registries/system-registry.yaml`
- Timeline: 2-4 semanas dependendo da complexidade

**Step 4.2 — Wind-down de Pessoas**

- DRI: COO Orchestrator
- Processo:
  1. Realocar pessoas para novas iniciativas
  2. Garantir transição suave (1-2 semanas de overlap)
  3. Preservar conhecimento: handover documentation
  4. Ajustar OKRs dos profissionais realocados
- Output: Tabela de realocação executada

**Step 4.3 — Captura de Aprendizados**

- DRI: Squad Coordinator
- Processo:
  1. Sessão de retrospectiva com equipe da iniciativa (1-2 horas)
  2. Documentar:
     - O que aprendemos sobre o mercado/cliente?
     - O que aprendemos sobre nossa capacidade de execução?
     - O que faríamos diferente?
     - Que hipóteses foram validadas/invalidadas?
     - Que assets podem ser reaproveitados?
  3. Registrar em `data/registries/lessons-learned.yaml`
  4. Atualizar `data/registries/decision-registry.yaml` com outcome
- Checklist: `checklists/ralphloop-quality.md`

**Step 4.4 — Encerramento Formal**

- DRI: COO Orchestrator
- Processo:
  1. Atualizar status em `data/registries/initiative-registry.yaml` → "KILLED"
  2. Documentar data de encerramento e racional final
  3. Confirmar que todos os recursos foram realocados
  4. Confirmar que todos os custos recorrentes foram cancelados
  5. Marcar wind-down como completo
- Output: Iniciativa oficialmente encerrada

---

## Quality Gates

### Gate 1: Qualidade da Análise

- [ ] Kill criteria pré-definidos foram consultados (não inventados agora)
- [ ] Dados quantitativos são atuais (não mais de 2 semanas)
- [ ] Teste de sunk cost aplicado honestamente
- [ ] DRI da iniciativa foi ouvido antes da decisão
- [ ] Impact assessment completo (pessoas, tech, clientes, vendors)

### Gate 2: Qualidade da Decisão

Aplicar `checklists/execution/kill-criteria-quality.md`:
- [ ] Decisão baseada em dados, não em opinião
- [ ] Sunk cost não influenciou a decisão de continuar
- [ ] Alternativas foram consideradas (KILL / PIVOT / PROBATION)
- [ ] Vision Chief aprovou formalmente
- [ ] Racional documentado em `data/registries/decision-registry.yaml`

### Gate 3: Qualidade da Comunicação

- [ ] Narrativa de kill preparada (sem culpa, com aprendizado)
- [ ] Time envolvido comunicado ANTES do anúncio geral
- [ ] Plano de realocação comunicado a cada pessoa afetada
- [ ] Comunicação externa preparada (se aplicável)
- [ ] Tom: transparente, honesto, focado no futuro

### Gate 4: Qualidade do Sunsetting

- [ ] Wind-down técnico completo
- [ ] Custos recorrentes cancelados
- [ ] Pessoas realocadas
- [ ] Aprendizados capturados em `data/registries/lessons-learned.yaml`
- [ ] Registry atualizado com status KILLED
- [ ] Resources liberados e realocados conforme plano

---

## Outputs / Artefatos

| Artefato | Formato | Localização | Owner |
|----------|---------|------------|-------|
| Lista de candidatas a kill | Markdown | `data/memos/` | COO |
| Análise de sunk cost | Markdown | `data/memos/` | COO + CFO |
| Kill Review Board ata | Markdown | `data/meeting-minutes/` | Squad Coordinator |
| Kill Decision Memo | Markdown | `templates/decision/kill-decision-memo.md` | Vision Chief |
| Impact Assessment | Markdown | `data/memos/` | COO |
| Plano de realocação | Markdown | `data/memos/` | COO + CFO |
| Comunicação de kill | Markdown | `data/memos/` | Vision Chief |
| Retrospectiva de aprendizados | YAML | `data/registries/lessons-learned.yaml` | Squad Coordinator |

---

## Registries Atualizados

- `data/registries/initiative-registry.yaml` — Status alterado para KILLED + metadata
- `data/registries/decision-registry.yaml` — Kill decisions documentadas com racional
- `data/registries/lessons-learned.yaml` — Aprendizados da iniciativa encerrada
- `data/registries/risk-registry.yaml` — Riscos associados removidos/atualizados
- `data/registries/system-registry.yaml` — Sistemas descomissionados
- `data/registries/vendor-registry.yaml` — Contratos cancelados

---

## Próximos Passos

1. **Imediato**: Confirmar realocação de recursos nos roadmaps ativos
2. **Próximo WBR**: Reportar kills e realocações → `workflows/04-wbr-loop.md`
3. **Próximo MBR**: Revisão de impacto dos kills → `workflows/05-mbr-loop.md`
4. **Próximo QBR**: Avaliar se aprendizados foram incorporados → `workflows/06-qbr-loop.md`
5. **Contínuo**: Monitorar iniciativas em PROBATION (30 dias)

---

## Cross-squad Handoffs

| De | Para | O quê | SLA |
|----|------|-------|-----|
| COO | Squads afetados | Comunicação de kill + plano de transição | 24h após decisão |
| COO | Data Squad | Remoção de métricas descontinuadas | 1 semana |
| CTO | Design Squad | Comunicação de features descontinuadas | 48h |
| CMO | Traffic/Brand/Copy | Cancelamento de campanhas relacionadas | 24h |
| CIO | Cybersecurity | Atualização de risk register | 48h |
| Vision Chief | Advisory Board | Comunicação de kills estratégicos | 1 semana |
| Vision Chief | Storytelling | Narrativa de aprendizado | 1 semana |

### Anti-Padrões a Evitar

1. **"Vamos esperar mais um mês"** → Se os kill criteria foram atingidos, não esperar
2. **"Já investimos tanto"** → Sunk cost fallacy é o inimigo #1
3. **"O time vai ficar desmotivado"** → Motivação vem de trabalhar em coisas que importam
4. **"Mas e se der certo?"** → Se os dados dizem que não, os dados vencem
5. **"Ninguém quer ser o que matou"** → Matar com disciplina é coragem, não fraqueza
6. **"Vamos só reduzir o investimento"** → Zombie initiatives consomem atenção sem entregar
7. **"O fundador gosta dessa ideia"** → Até o fundador deve respeitar kill criteria
