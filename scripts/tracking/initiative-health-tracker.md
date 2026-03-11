# Initiative Health Tracker

> Script para monitorização contínua da saúde de iniciativas estratégicas.

---

## Objetivo

Acompanhar o estado de saúde de todas as iniciativas activas, recolhendo dados
de múltiplas fontes, calculando scores compostos e gerando alertas quando
uma iniciativa mostra sinais de degradação.

---

## Data Collection — Recolha de Dados

### Dimensões Monitorizadas

#### 1. Schedule Health
- **Milestone completion**: % de milestones concluídos no prazo
- **Timeline variance**: desvio actual vs plano original
- **Velocity trend**: aceleração ou desaceleração do progresso
- **Critical path status**: estado dos itens no caminho crítico
- **Buffer consumption**: % do buffer temporal consumido

#### 2. Scope Health
- **Scope changes**: número e magnitude de alterações de scope
- **Requirements stability**: frequência de mudanças em requirements
- **Feature completion**: % de features entregues vs planeadas
- **Scope creep index**: ratio de scope adicionado vs removido
- **MVP alignment**: aderência ao minimum viable scope

#### 3. Resource Health
- **Budget utilization**: gastos actuais vs orçamento
- **Team allocation**: FTEs alocados vs planeados
- **Key person risk**: dependência de indivíduos específicos
- **Skill gaps**: competências em falta identificadas
- **External dependencies**: estado de dependências externas

#### 4. Quality Health
- **Defect rate**: defeitos encontrados por unidade de trabalho
- **Rework rate**: % de trabalho que requer refazer
- **Technical debt**: acumulação de dívida técnica
- **Test coverage**: cobertura de testes (se aplicável)
- **Stakeholder satisfaction**: feedback qualitativo dos stakeholders

#### 5. Alignment Health
- **Strategic fit**: alinhamento com objectivos estratégicos actuais
- **Stakeholder engagement**: nível de envolvimento dos sponsors
- **Cross-squad coordination**: qualidade da coordenação inter-squads
- **Communication effectiveness**: fluxo de informação adequado
- **Decision velocity**: rapidez na tomada de decisões necessárias

---

## Scoring — Sistema de Pontuação

### Cálculo do Health Score

Cada dimensão recebe um score de 0 a 100:

```
Score por dimensão = média ponderada dos indicadores

Pesos por indicador:
- Schedule: milestone_completion(30%) + timeline_variance(25%) +
            velocity_trend(20%) + critical_path(15%) + buffer(10%)
- Scope:    scope_changes(25%) + requirements_stability(25%) +
            feature_completion(20%) + scope_creep(20%) + mvp(10%)
- Resource: budget(30%) + team(25%) + key_person(20%) +
            skills(15%) + dependencies(10%)
- Quality:  defects(25%) + rework(25%) + tech_debt(20%) +
            test_coverage(15%) + satisfaction(15%)
- Alignment: strategic_fit(30%) + stakeholder(25%) +
             cross_squad(20%) + communication(15%) + decisions(10%)
```

### Health Score Composto
```
Overall Health = Schedule(25%) + Scope(20%) + Resource(20%) +
                 Quality(20%) + Alignment(15%)
```

### Classificação
| Score | Classificação | Cor | Significado |
|-------|--------------|-----|-------------|
| 80-100 | Healthy | Verde | A iniciativa está on track |
| 60-79 | At Risk | Amarelo | Existem sinais de alerta |
| 40-59 | Troubled | Laranja | Intervenção necessária |
| 0-39 | Critical | Vermelho | Acção imediata requerida |

---

## Alerting — Sistema de Alertas

### Alertas por Nível
| Nível | Trigger | Destinatário | Acção Esperada |
|-------|---------|-------------|----------------|
| Info | Score desce >5 pontos numa semana | Initiative owner | Monitorar |
| Warning | Score entra em At Risk | Initiative owner + squad lead | Investigar e plano |
| Alert | Score entra em Troubled | C-Level Squad | Review e intervenção |
| Critical | Score entra em Critical | C-Level Squad + sponsors | War room imediato |

### Alertas Específicos
- **Schedule alert**: milestone atrasado >1 semana sem recovery plan
- **Budget alert**: burn rate >110% do planeado por 2 semanas consecutivas
- **Scope alert**: >3 scope changes num período de 2 semanas
- **Quality alert**: defect rate duplica vs período anterior
- **Alignment alert**: sponsor não responde em >5 dias úteis

### Escalation Path
```
1. Initiative Owner (resposta em 24h)
   ↓ (se não resolvido em 48h)
2. Squad Lead (resposta em 24h)
   ↓ (se não resolvido em 48h)
3. C-Level Sponsor (resposta em 24h)
   ↓ (se não resolvido em 48h)
4. Full C-Level Squad Review
```

---

## Processo de Tracking

### Frequência de Actualização
- **Dados automáticos**: recolhidos diariamente
- **Input manual**: actualizado semanalmente pelo initiative owner
- **Health score**: recalculado diariamente
- **Deep review**: quinzenalmente pelo initiative owner
- **Portfolio review**: mensalmente pelo C-Level Squad

### Workflow Semanal
```
Segunda: Recolha automática de dados da semana anterior
Terça:   Initiative owners completam inputs manuais
Quarta:  Scores recalculados, alertas gerados
Quinta:  Follow-up de alertas, actualizações de status
Sexta:   Report semanal consolidado distribuído
```

### Dados de Input Manual
O initiative owner actualiza semanalmente:
1. Progresso qualitativo (2-3 frases)
2. Riscos novos ou alterados
3. Bloqueios actuais
4. Necessidades de apoio
5. Confiança subjectiva (1-10)

---

## Reporting e Visualização

### Dashboard Individual por Iniciativa
- Health score trend (últimas 12 semanas)
- Breakdown por dimensão (radar chart)
- Milestones timeline (gantt simplificado)
- Budget burn-down chart
- Top 3 risks com status
- Action items pendentes

### Dashboard Portfolio
- Heatmap de todas as iniciativas por health score
- Distribuição de scores (histogram)
- Trend de portfolio health ao longo do tempo
- Resource allocation cross-iniciativas
- Dependency map entre iniciativas
- Alertas activos consolidados

---

## Integração com Outros Processos

- **Decision Log**: decisões que afectam health são ligadas
- **Risk Scan**: riscos de iniciativas alimentam o risk register global
- **Metrics Pack**: health scores incluídos nos metrics packs
- **Quarterly Review**: histórico de health é input para análise trimestral
- **Resource Planning**: health informa realocação de recursos

---

## Notas Técnicas

- Dados armazenados em `data/initiatives/[initiative-id]/health/`
- Histórico mantido indefinidamente para análise de padrões
- Scores calculados via script automatizado (idempotente)
- Alertas distribuídos via canais configurados por squad
- API disponível para integração com dashboards externos
