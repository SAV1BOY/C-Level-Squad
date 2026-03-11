# Initiative Blocks — Blocos Reutilizáveis para Gestão de Iniciativas

> Referência do C-Level Squad para documentar e gerenciar iniciativas estratégicas.
> Uma iniciativa sem charter é uma intenção. Uma intenção sem kill criteria é um projeto zumbi.

---

## 1. Initiative Charter Block

### Propósito
Documento fundacional de uma iniciativa. Define o "contrato social" entre o time que executa e a liderança que financia/aprova.

### Template

```markdown
## Initiative Charter: [Nome da Iniciativa]

### Metadados
- **ID:** [INI-YYYY-NNN]
- **Status:** [Proposed / Approved / In progress / Paused / Completed / Killed]
- **DRI:** [Agente responsável]
- **Sponsor:** [Agente que aprova e remove bloqueios]
- **Data de criação:** [YYYY-MM-DD]
- **Data de início previsto:** [YYYY-MM-DD]
- **Data de conclusão prevista:** [YYYY-MM-DD]
- **Alinhamento estratégico:** [Qual Bet ou OKR esta iniciativa suporta]

### Propósito (1 parágrafo)
[Por que esta iniciativa existe? Qual problema resolve ou oportunidade captura?]

### Escopo
**Inclui:**
- [Item 1 que está dentro do escopo]
- [Item 2]
- [Item 3]

**Não inclui (explicitamente):**
- [Item 1 que está FORA do escopo — para evitar scope creep]
- [Item 2]

### Entregáveis principais
| # | Entregável                    | Descrição                        | Milestone associado |
|---|-------------------------------|----------------------------------|---------------------|
| 1 | [Entregável 1]               | [O que será entregue]            | M[X]                |
| 2 | [Entregável 2]               | [descrição]                      | M[Y]                |

### Recursos necessários
| Recurso          | Quantidade     | Período        | Custo estimado |
|------------------|---------------|----------------|----------------|
| [Pessoas/Role]   | [X FTEs]      | [X meses]      | [R$]           |
| [Infraestrutura] | [descrição]   | [período]      | [R$]           |
| [Budget discreto]| [descrição]   | [one-time]     | [R$]           |
| **Total**        |               |                | **R$ [total]** |

### Governance
- **Cadência de report:** [Semanal / Quinzenal — conforme status]
- **Reporta para:** [Sponsor + CEO se relevante]
- **Gates de decisão:** [Quais checkpoints requerem aprovação para continuar]
- **Autonomia do DRI:** [O que o DRI pode decidir sozinho vs. o que precisa de aprovação]

### Aprovações
| Aprovador | Data       | Status    | Condições            |
|-----------|-----------|-----------|----------------------|
| [Sponsor] | [data]    | [Aprovado/Pendente] | [condições, se houver] |
| [CEO]     | [data]    | [Aprovado/Pendente] | [condições]          |
```

---

## 2. Hypothesis Block

### Propósito
Documentar a hipótese que a iniciativa pretende validar. Toda iniciativa é, em essência, um experimento.

### Template

```markdown
## Hipótese — [Nome da Iniciativa]

### Declaração da hipótese
**Formato:**
"Acreditamos que ao [AÇÃO/INTERVENÇÃO] para [PÚBLICO-ALVO],
conseguiremos [RESULTADO MENSURÁVEL], porque [RAZÃO/MECANISMO]."

### Componentes

| Componente      | Descrição                                                |
|-----------------|----------------------------------------------------------|
| Ação            | [O que faremos — específico e concreto]                  |
| Público-alvo    | [Para quem — segmento específico]                        |
| Resultado       | [O que esperamos ver — com métrica e target]             |
| Mecanismo       | [Por que acreditamos que vai funcionar — a lógica causal]|

### Evidências que suportam a hipótese
| # | Evidência                           | Tipo         | Força      |
|---|-------------------------------------|-------------|------------|
| 1 | [dado, pesquisa, feedback, analogia]| [quant/qual] | [forte/média/fraca] |
| 2 | [...]                               | [...]       | [...]      |

### Premissas implícitas
[O que precisa ser verdade, além da hipótese, para a iniciativa funcionar]
1. [Premissa 1: ex. "Clientes vão adotar o novo fluxo sem resistência significativa"]
2. [Premissa 2: ex. "O custo de aquisição não vai aumentar com a mudança"]
3. [Premissa 3]

### Anti-hipótese (o caso contra)
[Qual é o melhor argumento de que esta hipótese está ERRADA?]
"A hipótese pode falhar se [contra-argumento]. Evidências que suportam a anti-hipótese: [dados]."

### Como validar
| Fase    | Ação de validação               | Métrica de sucesso          | Timeline  |
|---------|----------------------------------|-----------------------------|-----------|
| Fase 1  | [ex: MVP com 50 early adopters] | [ex: >30% activation rate]  | [2 semanas]|
| Fase 2  | [ex: A/B test com 10% do tráfego]| [ex: +15% conversion]     | [4 semanas]|
| Fase 3  | [ex: Rollout para 100%]         | [ex: KR1 do OKR atingido]  | [8 semanas]|
```

---

## 3. Success Criteria Block

### Propósito
Definir antecipadamente o que "sucesso" significa, evitando julgamento retroativo e goal-post moving.

### Template

```markdown
## Success Criteria — [Nome da Iniciativa]

### Definição de sucesso
**Em uma frase:** [O que precisa ser verdade para dizermos que esta iniciativa foi um sucesso]

### Métricas de sucesso

| # | Métrica                  | Baseline | Target mínimo | Target ideal | Método de medição | Quando medir |
|---|--------------------------|----------|---------------|-------------|-------------------|-------------|
| 1 | [Métrica primária]       | [atual]  | [mínimo aceitável] | [ideal]| [como]           | [quando]    |
| 2 | [Métrica secundária]     | [atual]  | [mínimo]      | [ideal]     | [como]           | [quando]    |
| 3 | [Guardrail metric]       | [atual]  | [não piorar]  | [melhorar]  | [como]           | [quando]    |

### Guardrail metrics (o que NÃO pode piorar)
[Métricas que devem permanecer estáveis ou melhorar enquanto perseguimos o sucesso principal]
- [Guardrail 1: ex. "NPS não pode cair mais de 5 pontos"]
- [Guardrail 2: ex. "Custo operacional não pode aumentar mais de 10%"]
- [Guardrail 3: ex. "Velocidade do site não pode degradar mais de 200ms"]

### Níveis de resultado

| Nível        | Critério                                          | Decisão                    |
|-------------|---------------------------------------------------|----------------------------|
| Home run    | Target ideal atingido + guardrails mantidos       | Escalar agressivamente      |
| Sucesso     | Target mínimo atingido + guardrails mantidos      | Escalar com otimizações     |
| Parcial     | Algum progresso mas abaixo do target mínimo       | Iterar ou pivotar           |
| Falha       | Sem progresso significativo ou guardrails violados | Kill ou reset fundamental   |

### Timeline de avaliação
- **Early signal (2-4 semanas):** Avaliar leading indicators. Confidence check
- **Mid-point (50% do timeline):** Avaliação formal de progresso. Decisão continue/pivot
- **Final (conclusão do timeline):** Scoring definitivo contra success criteria
- **Post-mortem (+30 dias):** Avaliar impacto real vs. projetado (muitos efeitos demoram)
```

---

## 4. Kill Criteria Block

### Propósito
Definir antecipadamente as condições que justificam matar a iniciativa, removendo o viés emocional (sunk cost) do momento da decisão.

### Template

```markdown
## Kill Criteria — [Nome da Iniciativa]

### Filosofia
Kill criteria existem para proteger a organização de investir em caminhos sem retorno.
Matar uma iniciativa precocemente é uma vitória (recursos liberados), não uma derrota.

### Critérios automáticos de kill (se QUALQUER um for verdadeiro: matar)

| # | Critério                                          | Como detectar               | Checkpoint |
|---|---------------------------------------------------|-----------------------------|------------|
| 1 | [ex: Zero traction após 30 dias de lançamento]   | [métrica < threshold]       | M1         |
| 2 | [ex: Custo excede 150% do budget aprovado]        | [burn rate tracking]        | Contínuo   |
| 3 | [ex: Premissa-chave invalidada por dados]         | [resultado de experimento]  | M2         |
| 4 | [ex: Mercado mudou, tornando a iniciativa irrelevante] | [análise de mercado]   | Trimestral |

### Critérios de avaliação (se 2+ verdadeiros: considerar kill)

| # | Critério                                          | Checkpoint | Verdadeiro? |
|---|---------------------------------------------------|------------|-------------|
| 1 | [Progresso em <50% do esperado no mid-point]      | M2         | [ ]         |
| 2 | [Stakeholder principal retirou suporte]            | Contínuo   | [ ]         |
| 3 | [Existe alternativa com ROI significativamente melhor] | Contínuo | [ ]      |
| 4 | [Time está perdendo motivação/saindo]              | Contínuo   | [ ]         |
| 5 | [Custo de oportunidade de continuar > benefício]   | Trimestral | [ ]         |

### Processo de kill

1. **Detecção:** Kill criteria atingido → DRI identifica
2. **Análise:** DRI documenta: o que aconteceu, por que, opções (kill vs. pivot vs. continue com mudanças)
3. **Recomendação:** DRI recomenda kill + justificativa
4. **Decisão:** Sponsor + CEO decidem formalmente
5. **Comunicação:** Comunicar decisão e razões a todos os envolvidos
6. **Wrap-up:** Documentar lições aprendidas. Realocar recursos
7. **Celebração:** Reconhecer a coragem de matar cedo e as lições aprendidas

### O que NÃO é motivo para kill
- Dificuldade normal de execução (struggle ≠ failure)
- Atraso de 1-2 semanas em milestones (a menos que seja systematic)
- Opinião de uma pessoa sem dados
- "Intuição" de que não vai funcionar (sem evidência)
```

---

## 5. Resource Requirements Block

### Propósito
Documentar todos os recursos necessários para a iniciativa, incluindo pessoas, budget, ferramentas e tempo.

### Template

```markdown
## Resource Requirements — [Nome da Iniciativa]

### Pessoas

| Role            | FTE (0-1.0) | Skills necessárias             | Duração  | Fonte (existente/contratar) | Custo |
|-----------------|-------------|-------------------------------|----------|----------------------------|-------|
| [Role 1]        | [0.X]       | [skills]                      | [X meses]| [existente: Nome]          | [R$]  |
| [Role 2]        | [0.X]       | [skills]                      | [X meses]| [contratar]                | [R$]  |

### Budget

| Categoria       | Valor       | Recorrência  | Notas                    |
|-----------------|------------|-------------|--------------------------|
| Pessoas         | R$ [X]     | [período]    | [detalhes]               |
| Infraestrutura  | R$ [X]     | [mensal]     | [cloud, servers, etc.]   |
| Ferramentas     | R$ [X]     | [anual]      | [licenças, SaaS]         |
| Marketing       | R$ [X]     | [one-time]   | [se aplicável]           |
| Contingência 15%| R$ [X]     | [one-time]   | Buffer para imprevistos  |
| **Total**       | **R$ [X]** |              |                          |

### Dependências externas

| Dependência              | De quem/o quê           | Quando necessário | Risco se atrasar |
|--------------------------|-------------------------|-------------------|------------------|
| [Dependência 1]          | [agente/time/fornecedor]| [data]            | [impacto]        |
| [Dependência 2]          | [fonte]                 | [data]            | [impacto]        |

### Constraints
- **Budget máximo:** R$ [X] (aprovado por [agente])
- **Headcount máximo:** [X] FTEs
- **Timeline máximo:** [X] meses (hard deadline: [data] / soft deadline: [data])
- **Tecnologia:** [restrições técnicas, ex: "deve usar stack existente"]
```

---

## 6. Timeline / Milestones Block

### Propósito
Definir a timeline da iniciativa com milestones claros, gates de decisão e dependências.

### Template

```markdown
## Timeline — [Nome da Iniciativa]

### Visão geral
**Início:** [data] → **Fim previsto:** [data] → **Duração:** [X semanas]

### Fases e milestones

| Fase | Milestone                   | Data       | DRI     | Entregável                    | Tipo          |
|------|-----------------------------|------------|---------|-------------------------------|---------------|
| 1    | M1: [Kickoff + planning]    | [data]     | [DRI]   | [Charter aprovado, time formado] | Obrigatório |
| 1    | M2: [Discovery concluído]   | [data]     | [DRI]   | [Pesquisa, hipóteses validadas]  | Obrigatório |
| 2    | M3: [MVP / POC pronto]      | [data]     | [DRI]   | [Protótipo funcional]           | Obrigatório |
| 2    | G1: [Gate: GO/NO-GO]        | [data]     | [Sponsor]| [Decisão baseada em resultados de M3] | Gate   |
| 3    | M4: [Beta / Piloto]         | [data]     | [DRI]   | [Produto em teste com N usuários]| Obrigatório |
| 3    | M5: [Resultados de piloto]  | [data]     | [DRI]   | [Dados de validação]            | Obrigatório |
| 3    | G2: [Gate: Scale/Kill]      | [data]     | [Sponsor]| [Decisão baseada em M5]        | Gate         |
| 4    | M6: [Launch / Rollout]      | [data]     | [DRI]   | [Disponível para todos]        | Obrigatório  |
| 4    | M7: [Post-launch review]    | [data]     | [DRI]   | [Avaliação 30 dias]            | Obrigatório  |

### Gates de decisão detalhados

#### Gate 1: [Data]
**Decisor:** [Sponsor]
**Critérios de GO:**
- [Critério 1: ex. "POC demonstra viabilidade técnica"]
- [Critério 2: ex. "Feedback de early users é positivo (NPS >30)"]
- [Critério 3: ex. "Budget projetado dentro do aprovado"]

**Se NO-GO:** [O que acontece — kill, revisão de abordagem, delay]

### Critical path
[Quais milestones estão no critical path — atraso nestes = atraso total]
M1 → M2 → M3 → G1 → M4 → M5 → G2 → M6

### Buffer planejado
- [X dias] de buffer entre M3 e G1 (para ajustes)
- [Y dias] de buffer entre G2 e M6 (para preparação de launch)
```

---

## 7. Dependency Map Block

### Propósito
Visualizar todas as dependências da iniciativa — internas e externas — para gestão proativa de riscos de bloqueio.

### Template

```markdown
## Dependency Map — [Nome da Iniciativa]

### Dependências internas (dentro do Squad)

| De              | Para            | O que                          | Quando    | Status    | Risco   |
|-----------------|-----------------|--------------------------------|-----------|-----------|---------|
| [Esta iniciativa]| [Agente/Time]  | [O que precisamos deles]      | [data]    | [🟢🟡🔴]  | [B/M/A] |
| [Agente/Time]   | [Esta iniciativa]| [O que eles precisam de nós]  | [data]    | [🟢🟡🔴]  | [B/M/A] |

### Dependências externas (fora do Squad)

| De              | Para             | O que                         | Quando    | Status    | Risco   | Plano B  |
|-----------------|------------------|-------------------------------|-----------|-----------|---------|----------|
| [Fornecedor]    | [Esta iniciativa]| [entregável]                 | [data]    | [🟢🟡🔴]  | [B/M/A] | [alternativa] |
| [Regulador]     | [Esta iniciativa]| [aprovação]                  | [data]    | [🟢🟡🔴]  | [B/M/A] | [alternativa] |

### Visualização
```
[Esta Iniciativa]
  ├── depende de → CTO (API pronta até 04/01)
  ├── depende de → CIO (dados limpos até 03/25)
  ├── depende de → Fornecedor X (integração até 04/15)
  ├── fornece para → CMO (produto pronto para campanha até 05/01)
  └── fornece para → COO (processo operacional até 05/15)
```

### Gestão de dependências
- **Review semanal:** Checar status de cada dependência
- **Antecipação:** Se uma dependência está 🟡, contatar o fornecedor proativamente
- **Plano B:** Para cada dependência crítica, ter alternativa mapeada
- **Buffer:** Adicionar 20-30% de buffer em dependências de alto risco
```

---

## 8. Stakeholder Map Block

### Propósito
Identificar todos os stakeholders da iniciativa e definir a estratégia de engajamento com cada um.

### Template

```markdown
## Stakeholder Map — [Nome da Iniciativa]

### Mapa de stakeholders

| Stakeholder      | Papel/Interesse        | Influência (A/M/B) | Posição (apoiador/neutro/resistente) | Estratégia de engajamento |
|-----------------|----------------------|---------------------|--------------------------------------|---------------------------|
| [CEO]           | [Sponsor / funding]  | Alta                | Apoiador                             | Update mensal, decision gates |
| [COO]           | [Operações afetadas] | Alta                | Neutro                               | Envolver em design operacional |
| [CTO]           | [Dependência técnica]| Média               | Apoiador                             | Sync técnico semanal      |
| [Clientes beta] | [Early adopters]     | Média               | Variável                             | Feedback loop quinzenal   |
| [Time de vendas]| [Impactados pela mudança]| Baixa            | Resistente                           | Comunicação + treinamento |

### Matriz de engajamento (Poder × Interesse)

```
              Alto Interesse
                   │
    ┌──────────────┼──────────────┐
    │  MANTER      │  GERENCIAR   │
    │  SATISFEITO  │  DE PERTO    │
    │              │  (CEO, COO)  │
Alto├──────────────┼──────────────┤
Poder│  MONITORAR  │  MANTER      │
    │  (mínimo)   │  INFORMADO   │
    │              │  (Clientes,  │
    │              │   Time vendas)│
    └──────────────┼──────────────┘
                   │
              Baixo Interesse
```

### Plano de comunicação por stakeholder

| Stakeholder      | Formato        | Frequência    | Conteúdo principal            | Responsável |
|-----------------|----------------|---------------|-------------------------------|-------------|
| CEO             | Memo + reunião | Mensal        | Status, riscos, decisões      | DRI         |
| COO             | Sync           | Quinzenal     | Impacto operacional, recursos | DRI         |
| CTO             | Standup        | Semanal       | Dependências técnicas         | Tech lead   |
| Clientes beta   | Email + call   | Quinzenal     | Feedback, próximos passos     | Product     |
| Time de vendas  | All-hands      | Ao lançar     | O que muda, treinamento       | CMO         |

### Riscos de stakeholder
| Risco                               | Probabilidade | Mitigação                       |
|-------------------------------------|---------------|---------------------------------|
| [CEO retira sponsorship]            | Baixa         | Demonstrar progresso contínuo   |
| [Time de vendas sabota adoção]      | Média         | Envolver cedo, treinar, incentivos |
| [Clientes beta não engajam]         | Média         | Incentivos + seleção cuidadosa  |
```
