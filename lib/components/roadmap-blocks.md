# Roadmap Blocks — Blocos Reutilizáveis para Roadmaps

> Referência do C-Level Squad para construir e gerenciar roadmaps executivos.
> Um roadmap não é uma lista de features — é a tradução da estratégia em planos de execução ao longo do tempo.

---

## 1. Theme / Pillar Block

### Propósito
Organizar o roadmap em temas estratégicos (pillars) que representam áreas de investimento, não tarefas individuais. Cada pilar conecta-se diretamente a um Bet ou OKR estratégico.

### Template

```markdown
## Pillar: [Nome do Pilar]

### Metadados
- **ID:** [PIL-NNN]
- **Owner:** [Agente responsável]
- **Período:** [Q1-Q2 2026 / H1 2026 / Full year 2026]
- **Alinhamento estratégico:** [Qual Bet/OKR/Tese suporta]
- **Peso no portfolio:** [% do budget/recursos total]

### Descrição
[1-2 parágrafos descrevendo o tema, por que investir, e o que esperamos alcançar]

### Thesis do pilar
"Acreditamos que investir em [ÁREA] nos próximos [PERÍODO] resultará em [OUTCOME],
porque [RAZÃO], e saberemos que estamos no caminho certo quando [LEADING INDICATOR]."

### Métricas de sucesso do pilar
| Métrica                  | Baseline | Target (fim do período) | Método de medição |
|--------------------------|----------|------------------------|-------------------|
| [Métrica primária]       | [atual]  | [target]               | [como]            |
| [Métrica secundária]     | [atual]  | [target]               | [como]            |

### Iniciativas neste pilar
| # | Iniciativa               | Status     | Milestone atual | Próximo milestone | DRI     |
|---|--------------------------|-----------|-----------------|-------------------|---------|
| 1 | [Iniciativa 1]           | [status]  | [milestone]     | [próximo]         | [DRI]   |
| 2 | [Iniciativa 2]           | [status]  | [milestone]     | [próximo]         | [DRI]   |

### Budget do pilar
- **Total alocado:** R$ [X]
- **Consumido até agora:** R$ [Y] ([Z%])
- **Projeção de conclusão:** R$ [W]
- **Status:** [🟢 dentro do budget / 🟡 at risk / 🔴 overrun]
```

### Exemplo

```markdown
## Pillar: AI-Powered Customer Intelligence

### Metadados
- **Owner:** CAIO
- **Período:** H1 2026
- **Alinhamento:** Bet #2 "Data Flywheel"
- **Peso:** 25% dos recursos de engenharia

### Thesis
"Acreditamos que investir em AI para entender comportamento do cliente resultará
em aumento de 40% em cross-sell e redução de 20% em churn, porque modelos preditivos
identificam padrões que humanos não conseguem ver em escala, e saberemos que estamos
no caminho certo quando nosso modelo atingir AUC >0.85 e gerar 50+ recommendations/dia."

### Iniciativas
| # | Iniciativa                    | Status      | DRI  |
|---|-------------------------------|------------|------|
| 1 | Churn prediction model        | Em produção | CAIO |
| 2 | Cross-sell recommendation     | POC         | CAIO |
| 3 | Customer health score         | Ideação     | CIO  |
```

---

## 2. Milestone Block

### Propósito
Definir marcos claros e verificáveis ao longo do roadmap que sinalizam progresso e habilitam decisões de go/no-go.

### Template

```markdown
## Milestone: [M-NNN] — [Nome do Milestone]

### Metadados
- **Pilar:** [PIL-NNN — Nome do pilar]
- **Iniciativa:** [INI-NNN — Nome da iniciativa]
- **Data target:** [YYYY-MM-DD]
- **DRI:** [Agente/pessoa responsável]
- **Tipo:** [Deliverable / Decision gate / Review point / External dependency]

### Definição de done
[Critério específico e binário (feito ou não feito) que define quando este milestone está completo]
- [ ] [Critério 1: ex. "POC funcional demonstrado para stakeholders"]
- [ ] [Critério 2: ex. "Performance > baseline por 15%"]
- [ ] [Critério 3: ex. "Documentação técnica completa"]

### Entregáveis
| Entregável                    | Formato        | Destinatário           |
|-------------------------------|---------------|------------------------|
| [Entregável 1]                | [Doc/Demo/Report] | [quem recebe]       |
| [Entregável 2]                | [formato]      | [destinatário]         |

### Dependências
| Depende de                   | Status    | Risco se atrasar              |
|------------------------------|-----------|-------------------------------|
| [Milestone/entregável anterior]| [🟢🟡🔴] | [Impacto no critical path?]  |

### Decisão associada (se Decision gate)
[Se este milestone é um gate, qual decisão será tomada?]
- **Decisão:** [GO / PIVOT / KILL]
- **Decisor:** [Agente]
- **Critérios de GO:** [O que precisa ser verdade para avançar]
- **Se NO-GO:** [O que acontece — kill, redesign, delay]

### Status tracking
| Data       | Status                  | Nota                          |
|-----------|-------------------------|-------------------------------|
| [data]    | [On track / At risk / Completed / Delayed] | [observação] |
```

### Tipos de milestone e guidance

| Tipo               | Propósito                                    | Exemplo                              |
|--------------------|----------------------------------------------|--------------------------------------|
| **Deliverable**    | Algo concreto é entregue                     | "MVP pronto para teste"              |
| **Decision gate**  | Momento de decidir continuar/parar/pivotar   | "Gate: validação de PMF"             |
| **Review point**   | Pausa para avaliar progresso e ajustar       | "Mid-quarter review"                 |
| **External dep**   | Dependência externa que precisa ser atingida | "Aprovação regulatória recebida"     |
| **Launch**         | Disponibilização para usuários finais        | "Feature disponível para 100%"       |

---

## 3. Dependency Block

### Propósito
Documentar e gerenciar dependências entre itens do roadmap, entre agentes e com stakeholders externos.

### Template

```markdown
## Dependencies — [Pilar/Iniciativa/Quarter]

### Dependency map visual

```
[Pilar A] ──depends on──→ [Pilar B]
    │                         │
    ▼                         ▼
[M-001: POC]              [M-010: Data pipeline]
    │                         │
    └──depends on──→──────────┘
    │
    ▼
[M-002: MVP]──depends on──→ [M-020: API (CTO)]
    │
    ▼
[M-003: Launch]──depends on──→ [M-030: Compliance (CIO)]
```

### Registry de dependências

| ID    | Milestone origem | Depende de (milestone) | Agente fornecedor | SLA    | Status | Risco | Plano B            |
|-------|-----------------|----------------------|-------------------|--------|--------|-------|--------------------|
| D-001 | M-001           | M-010                | CIO               | 03/25  | 🟢     | Baixo | —                  |
| D-002 | M-002           | M-020                | CTO               | 04/10  | 🟡     | Médio | API simplificada   |
| D-003 | M-003           | M-030                | CIO               | 04/30  | 🔴     | Alto  | Launch parcial sem feature regulada |

### Regras de gestão
1. **Identificação:** Toda dependência deve ser registrada no momento que o milestone é criado
2. **Comunicação:** Agente fornecedor deve ser notificado e confirmar capacidade + SLA
3. **Tracking:** Check semanal em dependências no critical path
4. **Escalação:** Se dependência muda para 🟡, notificar DRIs de ambos os lados. Se 🔴, escalar para sponsors
5. **Buffer:** Adicionar 20% de buffer em dependências de alto risco
6. **Plano B:** Toda dependência crítica deve ter alternativa documentada

### Análise de critical path
[Qual sequência de dependências determina a duração mínima do roadmap?]
```
Critical path: M-010 → M-001 → M-002 → M-020 → M-003
Duration: 12 semanas
Sem buffer: 10 semanas
Bottleneck: M-020 (API do CTO — 3 semanas de desenvolvimento)
```
```

---

## 4. Resource Allocation Block

### Propósito
Visualizar como os recursos (pessoas, budget, tempo) estão distribuídos entre os pilares e iniciativas do roadmap.

### Template

```markdown
## Resource Allocation — [Período]

### Distribuição por pilar

| Pilar                       | % Eng  | % Budget | # Pessoas | Período     | Owner |
|----------------------------|--------|----------|-----------|-------------|-------|
| [Pilar 1: Core product]    | [40%]  | [35%]    | [X]       | [Q1-Q4]     | [CTO] |
| [Pilar 2: Growth]          | [25%]  | [30%]    | [X]       | [Q1-Q4]     | [CMO] |
| [Pilar 3: AI]              | [20%]  | [20%]    | [X]       | [Q1-Q3]     | [CAIO]|
| [Pilar 4: Infra/Platform]  | [15%]  | [15%]    | [X]       | [Q1-Q4]     | [CTO] |
| **Total**                  | **100%**| **100%**| **[total]**|            |       |

### Distribuição no tempo (por quarter)

| Pilar          | Q1      | Q2      | Q3      | Q4      |
|---------------|---------|---------|---------|---------|
| Core product  | 5 FTEs  | 5 FTEs  | 4 FTEs  | 4 FTEs  |
| Growth        | 3 FTEs  | 4 FTEs  | 4 FTEs  | 3 FTEs  |
| AI            | 3 FTEs  | 3 FTEs  | 2 FTEs  | —       |
| Platform      | 2 FTEs  | 2 FTEs  | 2 FTEs  | 3 FTEs  |

### Framework de alocação recomendado (70/20/10)

| Categoria          | % Recursos | Descrição                              | Pilares          |
|-------------------|-----------|----------------------------------------|------------------|
| Core (70%)        | 70%       | Melhorar o produto/serviço existente   | Core, Platform   |
| Adjacent (20%)    | 20%       | Expandir para novos segmentos/features | Growth           |
| Transformational (10%) | 10%  | Apostas de longo prazo, alta incerteza | AI               |

### Conflitos de recurso identificados

| Conflito                                    | Agentes envolvidos | Resolução proposta          |
|--------------------------------------------|-------------------|----------------------------|
| [ML engineer compartilhado entre AI e Core]| CAIO + CTO        | [Priorizar AI em Q1-Q2, Core em Q3-Q4] |
| [Budget de marketing vs. produto]          | CMO + CTO         | [Alocar 60/40, revisar em Q2] |

### Utilização de recursos
| Recurso-chave    | Capacidade | Alocado   | Utilização | Status          |
|-----------------|-----------|-----------|-----------|-----------------|
| [Senior eng A]  | 100%      | 120%      | Over-allocated | 🔴 Rebalancear |
| [Data team]     | 400% (4p) | 350%      | 88%       | 🟢 OK          |
| [Cloud budget]  | R$50K/mês | R$42K/mês | 84%       | 🟢 OK          |
```

---

## 5. Risk Factor Block (roadmap-level)

### Template

```markdown
## Roadmap Risks — [Período]

### Riscos ao roadmap como um todo

| # | Risco                              | P | I | Score | Impacto no roadmap           | Mitigação                    | Owner |
|---|------------------------------------|---|---|-------|------------------------------|------------------------------|-------|
| 1 | [Perda de pessoa-chave]            |[P]|[I]| [S]   | [Atraso em pilar X]          | [Cross-training, backup]     | [COO] |
| 2 | [Budget cut mid-year]              |[P]|[I]| [S]   | [Cortar pilar Y]             | [Priorizar, proteger core]   | [CEO] |
| 3 | [Dependência externa atrasa]       |[P]|[I]| [S]   | [Pilar Z atrasado em Xm]    | [Plano B, alternativa]       | [DRI] |
| 4 | [Scope creep em múltiplos pilares] |[P]|[I]| [S]   | [Dilui foco e recursos]     | [Escopo fixo, change request]| [COO] |
| 5 | [Mudança estratégica (pivot)]      |[P]|[I]| [S]   | [Roadmap precisa ser refeito]| [Modularidade, decisão rápida]| [CEO]|

### Análise de sensibilidade
[Se um risco se materializar, quais milestones são mais afetados?]

| Risco          | Milestones afetados            | Impacto em semanas | Mitigável? |
|---------------|-------------------------------|-------------------|------------|
| [Risco 1]     | [M-002, M-003, M-005]        | [+3 semanas]      | [Sim/Parcial/Não] |
| [Risco 2]     | [M-010, M-011]               | [+6 semanas]      | [Parcial]  |

### Contingency budget
- **Buffer de tempo:** [X semanas] reservadas para imprevistos (recomendado: 15-20% da duração total)
- **Buffer de budget:** [R$ X] reservado (recomendado: 10-15% do budget total)
- **Buffer de pessoas:** [X% de slack] mantido para absorver urgências
```

---

## 6. Success Metric Block

### Template

```markdown
## Success Metrics — [Pilar/Iniciativa]

### North Star do roadmap
**Métrica:** [A métrica mais importante que o roadmap inteiro busca mover]
**Baseline:** [valor atual]
**Target (fim do período):** [valor target]

### Métricas por pilar

| Pilar          | Métrica primária     | Baseline | Target  | Métrica secundária  | Baseline | Target |
|---------------|---------------------|----------|---------|---------------------|----------|--------|
| [Pilar 1]     | [métrica]           | [val]    | [val]   | [métrica]           | [val]    | [val]  |
| [Pilar 2]     | [métrica]           | [val]    | [val]   | [métrica]           | [val]    | [val]  |

### Leading indicators (acompanhar semanalmente)
| Indicador              | Relacionado a     | Target semanal  | Atual  | Trend |
|-----------------------|-------------------|-----------------|--------|-------|
| [Leading indicator 1] | [Pilar/métrica]   | [valor]         | [valor]| [↑↓→] |
| [Leading indicator 2] | [Pilar/métrica]   | [valor]         | [valor]| [↑↓→] |

### Cadência de medição
| Métrica               | Frequência   | Responsável  | Onde reportado          |
|----------------------|-------------|-------------|------------------------|
| North Star           | Semanal     | CEO         | Weekly leadership sync  |
| Métricas de pilar    | Quinzenal   | Pilar owner | Pilar review            |
| Leading indicators   | Semanal     | DRI         | Dashboard / Slack       |
```

---

## 7. Review Checkpoint Block

### Propósito
Definir momentos formais de revisão do roadmap para garantir que o plano continua relevante e alinhado à estratégia.

### Template

```markdown
## Review Checkpoint: [Nome] — [Data]

### Metadados
- **Tipo:** [Monthly review / Quarterly planning / Mid-year strategic / Annual planning]
- **Duração:** [Xh]
- **Participantes:** [Agentes]
- **Facilitador:** [Agente]

### Agenda do checkpoint

1. **Performance review (30%):**
   - Métricas vs. targets
   - Milestones completed vs. planned
   - Budget consumed vs. planned

2. **Health assessment (20%):**
   - Status de cada pilar/iniciativa (traffic light)
   - Bloqueios ativos
   - Riscos materializados ou emergentes

3. **Strategy alignment check (20%):**
   - A estratégia mudou desde o último checkpoint?
   - O roadmap ainda está alinhado à estratégia?
   - Existem novas informações que mudam prioridades?

4. **Adjustment decisions (20%):**
   - O que adicionar ao roadmap?
   - O que remover/pausar?
   - O que re-priorizar?
   - Recursos precisam ser realocados?

5. **Next period preview (10%):**
   - Milestones do próximo período
   - Riscos antecipados
   - Dependências a resolver

### Template de output do checkpoint

```markdown
## Checkpoint Output — [Data]

### Decisões tomadas
| # | Decisão                            | Rationale         | DRI     |
|---|------------------------------------|-------------------|---------|
| 1 | [Adicionar initiative X]           | [por quê]         | [agente]|
| 2 | [Pausar initiative Y]              | [por quê]         | [agente]|
| 3 | [Realocar Z FTEs de A para B]      | [por quê]         | [agente]|

### Ajustes no roadmap
| Item                    | Antes              | Depois             | Razão            |
|------------------------|--------------------|--------------------|------------------|
| [Milestone X deadline] | [data antiga]      | [nova data]        | [razão]          |
| [Pilar Y budget]       | [R$ antigo]        | [R$ novo]          | [razão]          |

### Riscos para o próximo período
1. [Risco 1]
2. [Risco 2]

### Próximo checkpoint: [data]
```

### Cadência de checkpoints recomendada
| Tipo de checkpoint        | Frequência   | Duração | Foco principal                    |
|--------------------------|-------------|---------|-----------------------------------|
| Sprint/iteration review  | Quinzenal    | 1h      | Entregáveis e bloqueios           |
| Monthly roadmap review   | Mensal       | 2h      | Progresso, métricas, ajustes      |
| Quarterly planning       | Trimestral   | 4h      | Re-priorização, alocação, OKRs    |
| Mid-year strategic review| Semestral    | Full day| Validação estratégica, bets, visão |
| Annual planning          | Anual        | 2 dias  | Roadmap do próximo ano completo    |
```

---

## 8. Adjustment Trigger Block

### Propósito
Definir condições que automaticamente disparam revisão e possível ajuste do roadmap, sem esperar o próximo checkpoint agendado.

### Template

```markdown
## Adjustment Triggers — [Roadmap / Período]

### Triggers automáticos de review

| # | Trigger                                          | Threshold                    | Ação                              | Quem convoca |
|---|--------------------------------------------------|------------------------------|-----------------------------------|-------------|
| 1 | Milestone de critical path atrasado              | >2 semanas de atraso         | Review de impacto + replanning    | DRI          |
| 2 | Budget overrun                                   | >120% do planejado para período | Revisão de alocação             | COO          |
| 3 | Mudança estratégica (CEO/Board)                  | Qualquer mudança de bet/visão | Review completo do roadmap       | CEO          |
| 4 | Perda de recurso-chave                           | Saída de pessoa no critical path | Replanning de milestones       | COO          |
| 5 | Oportunidade de mercado inesperada               | Oportunidade com ROI >3× vs. roadmap atual | Avaliação de inclusão  | CMO/CEO      |
| 6 | Resultado de experimento que invalida premissa   | Kill criteria de uma bet atingido | Review do pilar afetado       | DRI da bet   |
| 7 | Dependência externa falha                        | Fornecedor/parceiro não entrega no SLA | Ativar Plano B         | DRI          |
| 8 | Métrica North Star em declínio sustentado        | 3+ períodos consecutivos de queda | Review estratégico completo  | CEO          |

### Processo de adjustment

```
1. Trigger detectado → DRI documenta impacto
2. DRI convoca mini-review com agentes afetados (24-48h)
3. Opções avaliadas:
   a. Absorver (resequenciar sem mudar escopo)
   b. Trade (trocar: adicionar X, remover Y)
   c. Expand (pedir mais recursos)
   d. Descope (reduzir escopo)
4. Decisão tomada e documentada
5. Roadmap atualizado
6. Comunicação ampla
```

### Princípios de ajuste
- **Escopo fixo, timeline flexível** OU **Timeline fixa, escopo flexível** — nunca ambos fixos
- Ao adicionar algo, tirar algo de igual esforço (trade, não acréscimo ilimitado)
- Mudanças no roadmap são normais e saudáveis — rigidez é mais perigosa que adaptação
- Documentar TODA mudança com razão (para aprender e para histórico)
```

---

## 9. Montagem de roadmap completo

### Template de roadmap executivo (Strategy on a Timeline)

```markdown
# Roadmap — [Período]

**Atualizado em:** [data]
**Owner:** [CEO / COO]
**Próximo checkpoint:** [data]

## North Star
[Métrica: valor atual → target]

## Pilares

### Pilar 1: [Nome] — Owner: [Agente] — [X%] dos recursos
[Thesis em 1 frase]
Milestones: M1 ([data]) → M2 ([data]) → M3 ([data])
KPI: [métrica] de [baseline] para [target]

### Pilar 2: [Nome] — Owner: [Agente] — [X%] dos recursos
[mesma estrutura]

### Pilar 3: [Nome] — Owner: [Agente] — [X%] dos recursos
[mesma estrutura]

## Dependências críticas
[Top 3 dependências no critical path]

## Riscos ao roadmap
[Top 3 riscos com mitigação]

## Resource allocation
[Tabela resumida]

## Adjustment triggers ativos
[Condições que disparam revisão]
```
