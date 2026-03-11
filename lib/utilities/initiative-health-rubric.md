# Initiative Health Rubric — Rubrica de Saúde de Iniciativas

> Referência do C-Level Squad para monitoramento contínuo de iniciativas estratégicas.
> Uma iniciativa sem monitoramento de saúde é um projeto esperança — funciona até não funcionar.

---

## 1. Sistema de Traffic Light (Semáforo)

### Definição dos estados

| Status         | Símbolo | Significado                                                  | Ação requerida                    |
|---------------|---------|--------------------------------------------------------------|-----------------------------------|
| **On Track**  | 🟢 Verde | Progresso conforme planejado. Riscos sob controle. Métricas dentro ou acima do esperado | Manter cadência de monitoramento |
| **At Risk**   | 🟡 Amarelo | Desvios detectados mas recuperáveis. Riscos emergentes. 1-2 indicadores fora do threshold | Plano de correção em 7 dias     |
| **Off Track** | 🔴 Vermelho | Desvios significativos. Riscos materializados. Múltiplos indicadores fora do threshold. Prazo/escopo/qualidade comprometidos | Escalação imediata. War room se necessário. Decisão de continue/pivot/kill |

### Regras de transição

```
Verde → Amarelo:
- Qualquer leading indicator cruza threshold por 2+ períodos consecutivos
- Novo risco identificado com score ≥ 10 (ver risk-scoring.md)
- Milestone atrasado em >1 semana
- Resource burn rate >110% do planejado

Amarelo → Vermelho:
- Indicador crítico fora do threshold por 3+ períodos
- Milestone crítico (critical path) atrasado
- Resource burn rate >130% do planejado
- Risco materializado sem mitigação efetiva
- Stakeholder principal expressa perda de confiança

Vermelho → Amarelo (recuperação):
- Plano de correção implementado com resultados visíveis
- Indicadores voltando para dentro dos thresholds
- Riscos materializados com mitigação efetiva ativa

Amarelo → Verde (recuperação):
- Todos os indicadores dentro dos thresholds por 2+ períodos
- Riscos anteriores mitigados ou eliminados
- Milestones re-planejados e atingidos
```

---

## 2. Dimensões de avaliação (8 dimensões)

### Dimensão 1: Milestone Completion (Completude de Marcos)

| Score | Status  | Critério                                                           |
|-------|---------|-------------------------------------------------------------------|
| 5     | 🟢      | Todos os milestones no prazo ou adiantados. Critical path limpo    |
| 4     | 🟢      | Milestones menores com atraso < 1 semana. Critical path no prazo   |
| 3     | 🟡      | 1-2 milestones atrasados em 1-2 semanas. Critical path sob pressão |
| 2     | 🔴      | Múltiplos milestones atrasados. Critical path comprometido          |
| 1     | 🔴      | Milestones principais falhados. Replanning necessário               |

**Como monitorar:**
- Manter Gantt ou timeline atualizado semanalmente
- Distinguir milestones de critical path vs. milestones secundários
- Atraso em critical path = escalação automática para Amarelo
- Calcular: % milestones concluídos / % milestones planejados até a data

**Thresholds:**
```
Verde:  Completion ratio ≥ 0.90
Amarelo: Completion ratio 0.70 - 0.89
Vermelho: Completion ratio < 0.70
```

### Dimensão 2: Resource Burn Rate (Taxa de consumo de recursos)

| Score | Status  | Critério                                                           |
|-------|---------|-------------------------------------------------------------------|
| 5     | 🟢      | Burn rate ≤ 95% do planejado. Budget on track                      |
| 4     | 🟢      | Burn rate 95-105% do planejado. Variação dentro da margem          |
| 3     | 🟡      | Burn rate 105-120% do planejado. Requer atenção e possível ajuste  |
| 2     | 🔴      | Burn rate 120-140% do planejado. Overrun provável. Requer ação     |
| 1     | 🔴      | Burn rate >140% do planejado. Budget estourado ou estourará em breve|

**Como calcular:**
```
Burn Rate Ratio = (Recursos consumidos até hoje / Recursos planejados até hoje)

Projeção de conclusão:
EAC (Estimate at Completion) = Budget total × (1 / CPI)
CPI (Cost Performance Index) = Valor entregue / Custo real

Exemplo:
- Budget total: R$500K
- Gasto até hoje: R$200K (40% do budget)
- Valor entregue até hoje: R$150K equivalente (30% do escopo)
- CPI = 0.75 (gastando mais do que entregando)
- EAC = R$500K / 0.75 = R$667K (projeção de overrun de R$167K)
```

**Recursos incluem:** Pessoas (horas/custo), infraestrutura, licenças, consultoria, outros custos diretos.

### Dimensão 3: Leading Indicators (Indicadores antecedentes)

| Score | Status  | Critério                                                           |
|-------|---------|-------------------------------------------------------------------|
| 5     | 🟢      | Todos os leading indicators dentro ou acima do target               |
| 4     | 🟢      | 1 leading indicator levemente abaixo do target (<10% off)          |
| 3     | 🟡      | 1-2 leading indicators significativamente abaixo (10-25% off)     |
| 2     | 🔴      | 3+ leading indicators abaixo ou 1 leading indicator >25% off      |
| 1     | 🔴      | Leading indicators indicam que a iniciativa não atingirá o objetivo|

**O que são leading indicators:**
Leading indicators são métricas que **predizem** o resultado futuro, em contraste com lagging indicators que **medem** o resultado passado.

| Tipo de iniciativa    | Leading indicators típicos                              | Lagging indicators     |
|----------------------|--------------------------------------------------------|------------------------|
| Produto/Feature      | Uso em beta, NPS de early adopters, bugs críticos       | Adoção geral, revenue  |
| Growth/Marketing     | CTR, signup rate, activation rate                       | Revenue, LTV           |
| Infraestrutura       | Cobertura de testes, tech debt resolvido, latência      | Uptime, incidents      |
| Hiring               | Pipeline de candidatos, offer accept rate               | Time to productivity   |
| AI/ML                | Acurácia em dev, data quality score                     | Impacto em produção    |
| Processo/Ops         | Compliance com novo processo, feedback do time          | Eficiência operacional |

### Dimensão 4: Risk Register Status (Status do registro de riscos)

| Score | Status  | Critério                                                           |
|-------|---------|-------------------------------------------------------------------|
| 5     | 🟢      | Risk register atualizado. Nenhum risco ≥ Alto sem mitigação ativa  |
| 4     | 🟢      | Risk register atualizado. 1 risco Alto com mitigação em andamento  |
| 3     | 🟡      | Risk register parcialmente atualizado. Riscos Altos sem mitigação clara |
| 2     | 🔴      | Risk register desatualizado. Novos riscos não registrados. Mitigações atrasadas |
| 1     | 🔴      | Sem risk register ou completamente abandonado. Riscos materializados sem plano |

**Regras de manutenção:**
- Atualizar risk register a cada checkpoint (semanal para amarelo/vermelho, quinzenal para verde)
- Adicionar novos riscos dentro de 48h da identificação
- Rever scores de P×I mensalmente (condições mudam)
- Fechar riscos que não são mais relevantes (com justificativa)

### Dimensão 5: Stakeholder Satisfaction (Satisfação de stakeholders)

| Score | Status  | Critério                                                           |
|-------|---------|-------------------------------------------------------------------|
| 5     | 🟢      | Stakeholders ativamente elogiam progresso. Confiança alta. Sem surpresas |
| 4     | 🟢      | Stakeholders satisfeitos. Comunicação regular e bem recebida        |
| 3     | 🟡      | Stakeholders neutros ou com preocupações pontuais. Alguma incerteza |
| 2     | 🔴      | Stakeholders insatisfeitos. Perguntas difíceis sem boas respostas. Confiança caindo |
| 1     | 🔴      | Stakeholders perderam confiança. Ameaça de cancelamento ou takeover |

**Como medir:**
- Pulse check informal a cada 2 semanas
- Survey formal mensal (3 perguntas: satisfação, confiança, comunicação)
- Observar: stakeholder está pedindo mais reports? (sinal de perda de confiança)
- Observar: stakeholder está "micromanageando"? (sinal vermelho)

### Dimensão 6: Quality of Deliverables (Qualidade das entregas)

| Score | Status  | Critério                                                           |
|-------|---------|-------------------------------------------------------------------|
| 5     | 🟢      | Entregas excedem expectativas de qualidade. Feedback positivo consistente |
| 4     | 🟢      | Entregas atendem expectativas. Problemas de qualidade menores e raros |
| 3     | 🟡      | Entregas aceitáveis mas com retrabalho frequente (>15% de rework)  |
| 2     | 🔴      | Entregas abaixo do esperado. Rework significativo (>30%). Bugs ou erros recorrentes |
| 1     | 🔴      | Entregas inaceitáveis. Rejeição por stakeholders. Impacto em credibilidade |

**Métricas de qualidade por tipo:**
```
Software: Bugs críticos por release, test coverage, latência P95
Processo: Taxa de erro, tempo de ciclo, compliance rate
Conteúdo: Revisões necessárias, accuracy rate
Data/AI: Acurácia do modelo, false positive rate, data freshness
```

### Dimensão 7: Team Health (Saúde do time)

| Score | Status  | Critério                                                           |
|-------|---------|-------------------------------------------------------------------|
| 5     | 🟢      | Time motivado, engajado, sustentável. Sem overtime crônico. Colaboração forte |
| 4     | 🟢      | Time funcional com energia boa. Overtime ocasional e gerenciado     |
| 3     | 🟡      | Sinais de fadiga. Overtime frequente. Motivação caindo. 1 pessoa-chave em risco de sair |
| 2     | 🔴      | Time sobrecarregado. Burnout visível. Conflitos não resolvidos. Turnover ativo |
| 1     | 🔴      | Time em crise. Saídas recentes de pessoas-chave. Capacidade comprometida |

**Sinais de alerta precoce:**
- Aumento de horas extras sem aumento proporcional de output
- Diminuição de participação em discussões/reuniões
- Aumento de sick days
- Qualidade das entregas caindo
- Feedback negativo em 1:1s
- Pessoas atualizando LinkedIn (sinal clássico)

### Dimensão 8: Dependency Management (Gestão de dependências)

| Score | Status  | Critério                                                           |
|-------|---------|-------------------------------------------------------------------|
| 5     | 🟢      | Dependências mapeadas, comunicadas e no prazo. Nenhum bloqueio ativo |
| 4     | 🟢      | Dependências mapeadas. 1 bloqueio menor resolvido dentro do SLA    |
| 3     | 🟡      | Dependências parcialmente mapeadas. 1-2 bloqueios ativos com plano de resolução |
| 2     | 🔴      | Dependências não bem mapeadas. Bloqueios ativos sem plano claro. Critical path afetado |
| 1     | 🔴      | Dependências desconhecidas surgindo constantemente. Múltiplos bloqueios sem resolução |

---

## 3. Scoring agregado e classificação

### Cálculo

```
Initiative Health Score = Σ (scores das 8 dimensões)
Máximo: 40 pontos
```

### Classificação final

| Score  | Status geral | Ação                                                    |
|--------|-------------|--------------------------------------------------------|
| 33-40  | 🟢 On Track  | Manter cadência. Report quinzenal                       |
| 25-32  | 🟢/🟡 Mostly On Track | Atenção em dimensões < 3. Report semanal       |
| 17-24  | 🟡 At Risk   | Plano de correção obrigatório. Report semanal. CEO informado |
| 9-16   | 🔴 Off Track | Escalação imediata. War room. Decisão continue/pivot/kill |
| 1-8    | 🔴 Critical  | Decisão de kill ou reset completo. Não continuar como está |

### Regra de override

**Qualquer dimensão individual com score 1 = Status geral automático de 🔴 Off Track**, independente do score agregado. Uma dimensão em 1 indica risco existencial para a iniciativa.

---

## 4. Cadência de monitoramento

### Por status

| Status      | Frequência de review | Participantes                  | Duração     | Output                       |
|-------------|---------------------|-------------------------------|-------------|------------------------------|
| 🟢 On Track | Quinzenal           | DRI + 1 agente sponsor         | 15 min      | Status update breve           |
| 🟡 At Risk  | Semanal             | DRI + agente sponsor + COO     | 30 min      | Status + plano de correção    |
| 🔴 Off Track | 2× por semana       | DRI + CEO + agentes relevantes | 45 min      | Status + decisão de caminho   |
| 🔴 Critical | Diária              | Todos os agentes envolvidos     | 30 min      | Status + ação imediata        |

### Dashboard de iniciativas

```markdown
## Initiative Health Dashboard — [Data]

| # | Iniciativa              | DRI  | Status | Score | Trend | Alerta principal              | Próx. review |
|---|-------------------------|------|--------|-------|-------|-------------------------------|--------------|
| 1 | Plataforma v2           | CTO  | 🟢     | 35/40 | →     | —                             | 2026-03-25   |
| 2 | Expansão LATAM          | CMO  | 🟡     | 23/40 | ↓     | Burn rate 125%                | 2026-03-18   |
| 3 | AI Recommendation Engine| CAIO | 🟡     | 26/40 | →     | Dependência de dados bloqueada| 2026-03-18   |
| 4 | Compliance LGPD         | CIO  | 🔴     | 14/40 | ↓     | Milestone crítico atrasado 3sem| 2026-03-14   |
| 5 | Novo pricing model      | CEO  | 🟢     | 32/40 | ↑     | —                             | 2026-03-25   |

### Sumário
- Total de iniciativas: 5
- 🟢 On Track: 2 (40%)
- 🟡 At Risk: 2 (40%)
- 🔴 Off Track: 1 (20%)
- Trend geral: Estável com 1 deteriorando

### Ações prioritárias:
1. [Compliance LGPD] War room agendada para 2026-03-14
2. [Expansão LATAM] Revisão de budget com COO
3. [AI Engine] Desbloquear dependência de dados com CIO
```

---

## 5. Protocolo de escalação

### Quando escalar

```
Escalar para COO:
- Qualquer iniciativa que mude de Verde para Amarelo
- Bloqueio de dependência não resolvido em 5 dias úteis
- Burn rate >115%

Escalar para CEO:
- Qualquer iniciativa que mude para Vermelho
- Iniciativa estratégica (top 3) em Amarelo por >2 semanas
- Decisão de kill necessária
- Conflito entre agentes sobre prioridade de recursos

Escalar para todo o Squad:
- Iniciativa em estado Crítico (score <9)
- Risco materializado com impacto cross-funcional
- Decisão de pivot que afeta estratégia geral
```

### Framework de decisão para Off Track

Quando uma iniciativa está 🔴 Off Track, o Squad deve decidir entre:

| Opção      | Quando usar                                          | Requisitos                         |
|-----------|------------------------------------------------------|------------------------------------|
| **Continue** | Problemas são temporários e solúveis. Tese original ainda válida | Plano de correção concreto com milestones de 2 semanas |
| **Pivot**  | Tese original parcialmente validada mas direção precisa mudar | Nova hipótese documentada. Kill criteria atualizados |
| **Kill**   | Tese invalidada, ou custo de oportunidade muito alto | Documentação de lições aprendidas. Realocação de recursos |

### Critérios para KILL

A decisão de matar uma iniciativa deve ser tomada quando:
1. Kill criteria originais (definidos no charter) foram atingidos
2. Custo para completar > valor esperado (com base rates atualizadas)
3. O cenário de mercado mudou e a iniciativa perdeu relevância
4. O time não tem capacidade e existem iniciativas de maior impacto
5. O sponsor/stakeholder principal retirou o suporte

**Importante:** Matar uma iniciativa NÃO é fracasso — é boa gestão de portfolio. Premiar a coragem de matar cedo.

---

## 6. Template de health check completo

```markdown
## Initiative Health Check — [Nome da Iniciativa]

**Data:** [YYYY-MM-DD]
**DRI:** [agente]
**Sponsor:** [agente]
**Início:** [data]  **Fim previsto:** [data]  **% concluído:** [X%]

### Status geral: [🟢/🟡/🔴] — Score: [XX/40]

### Scores por dimensão

| # | Dimensão              | Score | Status | Comentário                    |
|---|----------------------|-------|--------|-------------------------------|
| 1 | Milestone Completion | /5    |        |                               |
| 2 | Resource Burn Rate   | /5    |        |                               |
| 3 | Leading Indicators   | /5    |        |                               |
| 4 | Risk Register        | /5    |        |                               |
| 5 | Stakeholder Satisf.  | /5    |        |                               |
| 6 | Quality of Delivers  | /5    |        |                               |
| 7 | Team Health          | /5    |        |                               |
| 8 | Dependency Mgmt      | /5    |        |                               |
|   | **TOTAL**            | **/40**|       |                               |

### Trend (últimos 3 períodos)
[Score atual] vs [Score anterior] vs [Score antes] — Trend: [↑/→/↓]

### Top riscos ativos
1. [Risco] — P:[X] I:[X] Score:[XX] — Mitigação: [ação]

### Bloqueios ativos
1. [Bloqueio] — Owner para desbloquear: [agente] — ETA: [data]

### Decisões necessárias
1. [Decisão] — De quem: [agente] — Até quando: [data]

### Próximos milestones
| Milestone                  | Data prevista | Status    |
|---------------------------|--------------|-----------|
| [milestone 1]             | [data]       | [on track/atrasado] |

### Ação requerida
[Nenhuma / Plano de correção / Escalação / Decisão continue-pivot-kill]
```

---

## 7. Anti-patterns de gestão de iniciativas

| Anti-pattern | Descrição | Como detectar | Como corrigir |
|---|---|---|---|
| **Watermelon project** | Verde por fora, vermelho por dentro. Reports otimistas mascaram problemas | Leading indicators vs. lagging indicators divergem. Perguntar "o que pode dar errado?" | Exigir métricas objetivas, não narrativas |
| **Zombie initiative** | Não morre, não progride. Consome recursos sem entregar valor | Meses sem milestone significativo completado. Team "ocupado" mas sem output | Aplicar kill criteria rigorosamente |
| **Scope creep silencioso** | Escopo cresce sem reconhecimento formal | Original plan vs. current scope diverge sem change request | Revisão de escopo formal a cada milestone |
| **Hero dependency** | Uma pessoa carrega a iniciativa. Se sair, colapsa | Bus factor = 1. Verificar: "se [pessoa] sair amanhã, o que acontece?" | Cross-training, documentação, backup |
| **Vanity metrics** | Métricas que parecem boas mas não indicam saúde real | Métricas sobem mas outcome não melhora | Vincular métricas a outcomes de negócio |
