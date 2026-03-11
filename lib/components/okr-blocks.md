# OKR Blocks — Blocos Reutilizáveis para OKRs (Objectives & Key Results)

> Referência do C-Level Squad para definir, acompanhar e avaliar OKRs.
> OKRs são a ponte entre estratégia (onde queremos ir) e execução (o que fazemos esta semana).

---

## 1. Objective Template

### Propósito
Definir um Objective que seja qualitativo, inspiracional e direcional. O Objective responde: "O que queremos alcançar?"

### Template

```markdown
## Objective: [Título inspiracional]

**Descrição:** [1-2 frases que expandem o título e dão contexto]

**Owner:** [Agente responsável]
**Período:** [Q1 2026 / H1 2026 / etc.]
**Alinhamento estratégico:** [Qual bet/tese estratégica este Objective suporta?]
**Tipo:** [Committed (vamos entregar) / Aspirational (stretch — 70% seria ótimo)]
```

### Regras para bons Objectives
1. **Qualitativo:** Sem números no Objective (números vão nos Key Results)
2. **Inspiracional:** Alguém deveria ficar motivado ao ler
3. **Acionável:** O time sabe o que fazer para perseguir este Objective
4. **Time-bound:** Tem um período definido (tipicamente 1 quarter)
5. **Alinhado:** Conecta-se à estratégia e aos OKRs do nível acima

### Teste de qualidade do Objective
- [ ] Cabe em uma frase curta? (Se não, é complexo demais)
- [ ] É inspirador? (Se é "meh", reescrever)
- [ ] Dá direção? (Ajuda a dizer "não" a coisas que não contribuem?)
- [ ] É diferente de um Key Result? (Se tem número, é KR, não Objective)
- [ ] É alcançável no período? (Se é multi-ano, é visão, não OKR)
- [ ] Alguém é claramente o owner?

### Anti-patterns de Objectives

| Anti-pattern | Exemplo ruim | Exemplo corrigido |
|---|---|---|
| **Métrica disfarçada** | "Atingir R$3M de MRR" | "Estabelecer motor de crescimento previsível e escalável" |
| **Business as usual** | "Manter a operação funcionando" | (Isso não é OKR — é work stream) |
| **Vago demais** | "Ser melhor" | "Tornar nosso onboarding o melhor da categoria" |
| **Escopo enorme** | "Transformar a empresa" | "Automatizar os 3 processos operacionais mais custosos" |
| **Sem owner** | "Alguém deveria melhorar o produto" | "Entregar experiência de produto que elimina o #1 motivo de churn" |

### Exemplos por agente

```markdown
CEO: "Validar que nosso modelo é escalável para 3 mercados LATAM"
COO: "Criar uma máquina operacional que escala sem adicionar headcount proporcional"
CMO: "Tornar nossa marca a primeira referência em AI para PMEs no Brasil"
CTO: "Estabelecer fundação tecnológica que suporte 10× de crescimento sem re-arquitetura"
CIO: "Transformar dados no ativo estratégico mais valioso da empresa"
CAIO: "Colocar AI em produção em 3 use cases com ROI demonstrado"
```

---

## 2. Key Result Template

### Propósito
Definir Key Results que sejam quantitativos, mensuráveis e ambiciosos. Key Results respondem: "Como saberemos que alcançamos o Objective?"

### Template

```markdown
### Key Result [#]: [Descrição com métrica e target]

- **Baseline (início do período):** [valor atual]
- **Target:** [valor alvo]
- **Stretch target:** [valor aspiracional — 120% do target]
- **Método de medição:** [Como e onde esta métrica é medida]
- **Frequência de medição:** [Semanal / Quinzenal / Mensal]
- **Owner:** [Pessoa — pode ser diferente do owner do Objective]
- **Confidence score inicial:** [1-10 — quão confiantes estamos de atingir]
```

### Regras para bons Key Results
1. **Quantitativo:** Deve ter um número. Sempre.
2. **Mensurável:** Deve existir uma forma confiável de medir
3. **Outcome, não output:** Medir resultado, não atividade
4. **Não mais que 3-5 KRs por Objective:** Se tem mais, o Objective é grande demais
5. **Ambicioso mas alcançável:** Committed KRs devem ser 100% atingíveis; Aspirational, 70%

### Teste de qualidade do Key Result
- [ ] Tem um número? (Se não, não é KR)
- [ ] É um outcome (resultado) ou output (entregável)?
  - Output: "Lançar feature X" ← preferir como Initiative, não KR
  - Outcome: "Aumentar adoption rate de 30% para 50%" ← bom KR
- [ ] O baseline é conhecido? (Se não, primeiro KR é medir o baseline)
- [ ] O método de medição existe e é confiável?
- [ ] O target é ambicioso? (Se é fácil, não motiva)
- [ ] O target é alcançável? (Se é impossível, desmotiva)

### Anti-patterns de Key Results

| Anti-pattern | Exemplo ruim | Exemplo corrigido |
|---|---|---|
| **Binary/milestone** | "Lançar produto v2" | "Atingir 500 usuários ativos no produto v2" |
| **Activity metric** | "Fazer 20 calls de vendas por semana" | "Converter 15% dos SQLs em clientes" |
| **Vanity metric** | "Atingir 100K pageviews" | "Atingir 2.000 signups qualificados" |
| **Uncontrollable** | "Atingir R$5M de revenue" (se depende de fatores externos) | "Gerar pipeline qualificado de R$15M" (mais controlável) |
| **No baseline** | "Melhorar NPS" | "Aumentar NPS de 38 para 50" |
| **Gaming-prone** | "Resolver 500 tickets por mês" | "Atingir CSAT >4.5 no suporte" |

### Exemplos completos (Objective + Key Results)

```markdown
## Objective: Tornar nosso onboarding o melhor da categoria

### KR1: Aumentar activation rate (feature core usada em <7 dias) de 35% para 55%
- Baseline: 35% (Q4-2025)
- Target: 55%
- Medição: Product analytics (Mixpanel), cohort semanal
- Confidence: 6/10

### KR2: Reduzir time-to-value (primeiro insight gerado) de 14 dias para 5 dias
- Baseline: 14 dias (mediana)
- Target: 5 dias
- Medição: Evento "first_insight" no analytics
- Confidence: 5/10

### KR3: Atingir NPS de onboarding de 55+ (atualmente 40)
- Baseline: NPS 40
- Target: 55
- Medição: Survey in-app ao final do onboarding (N>100)
- Confidence: 7/10
```

---

## 3. Initiative Linkage Block

### Propósito
Conectar OKRs às iniciativas/projetos que contribuirão para atingi-los. Initiatives são o "como fazemos" por trás dos KRs.

### Template

```markdown
## Initiatives vinculadas ao OKR

**Objective:** [referência ao Objective]

| KR    | Initiative                        | Contribuição esperada | Effort    | DRI     | Timeline      |
|-------|----------------------------------|----------------------|-----------|---------|---------------|
| KR1   | [Initiative 1]                   | [+X% no KR1]        | [S/M/L]   | [pessoa]| [start-end]   |
| KR1   | [Initiative 2]                   | [+Y% no KR1]        | [S/M/L]   | [pessoa]| [start-end]   |
| KR2   | [Initiative 3]                   | [reduzir KR2 em Z]  | [S/M/L]   | [pessoa]| [start-end]   |

### Priorização de initiatives
[Usar RICE ou ICE — ver prioritization-math.md]

| Initiative     | RICE Score | Prioridade | Status           |
|---------------|-----------|------------|------------------|
| [Initiative 1] | [score]   | P1         | [Not started/In progress/Done] |

### Nota sobre initiatives vs. Key Results
- Key Results = O que medimos (outcome)
- Initiatives = O que fazemos (output)
- Um KR pode ter 0 ou múltiplas initiatives
- Se uma initiative não contribui para nenhum KR, questione se vale fazer
- Se um KR não tem initiative vinculada, questione como será atingido
```

---

## 4. Progress Tracking Block

### Propósito
Acompanhar o progresso dos OKRs durante o período, permitindo ajustes de rota.

### Template

```markdown
## OKR Progress — [Período] — Semana [X/13]

### Objective: [título]
**Status geral:** [🟢 On track / 🟡 At risk / 🔴 Off track]

| KR  | Target | Atual | % do target | Trend | Status | Nota        |
|-----|--------|-------|-------------|-------|--------|-------------|
| KR1 | [val]  | [val] | [%]         | [↑↓→] | [🟢🟡🔴] | [1 frase]  |
| KR2 | [val]  | [val] | [%]         | [↑↓→] | [🟢🟡🔴] | [1 frase]  |
| KR3 | [val]  | [val] | [%]         | [↑↓→] | [🟢🟡🔴] | [1 frase]  |

### Expected vs. Actual trajectory
Estamos na semana [X] de 13 → esperado [X/13 = Y%] do target

| KR  | Esperado (linear) | Atual | On pace? |
|-----|-------------------|-------|----------|
| KR1 | [Y% do target]    | [%]   | [S/N]    |

### Confidence scores atualizados

| KR  | Confidence inicial | Confidence atual | Δ   | Razão da mudança         |
|-----|-------------------|-----------------|-----|--------------------------|
| KR1 | [X/10]            | [Y/10]          | [±Z]| [explicação em 1 frase]  |

### Initiatives status

| Initiative     | Status              | % done | Bloqueio?           |
|---------------|---------------------|--------|---------------------|
| [Initiative 1] | [On track/Blocked]  | [%]    | [descrição se bloqueado] |

### Ações para o próximo período
1. [Ação para KR que está off track]
2. [Ação para desbloquear initiative]
```

### Cadência de tracking

| Semana do quarter | Atividade                                    |
|-------------------|----------------------------------------------|
| Semana 1          | OKRs finalizados e comunicados               |
| Semana 2-4        | Check-in semanal: atualizar progresso        |
| Semana 5          | Mid-quarter review: confidence update formal  |
| Semana 6-9        | Check-in semanal + ajustes de rota se necessário |
| Semana 10         | Pre-mortem: "se não atingirmos, por que será?" |
| Semana 11-12      | Sprint final para KRs recuperáveis           |
| Semana 13         | Scoring final + retrospectiva               |

---

## 5. Confidence Score Block

### Propósito
Avaliar e comunicar o nível de confiança de atingir cada Key Result, permitindo priorização de esforço onde a confiança é mais baixa.

### Template

```markdown
## Confidence Assessment — [KR]

**Score atual:** [X/10]
**Score anterior:** [Y/10]
**Tendência:** [Subindo / Estável / Caindo]

### Escala de confidence

| Score | Significado                                                     |
|-------|-----------------------------------------------------------------|
| 10    | Já atingimos ou vamos atingir com certeza. Sem risco            |
| 8-9   | Alta confiança. Caminho claro, sem bloqueios significativos     |
| 6-7   | Confiança moderada. Caminho existe mas depende de execução perfeita |
| 4-5   | Incerto. Riscos significativos ou dependências não resolvidas   |
| 2-3   | Baixa confiança. Precisamos de mudança de abordagem ou ajuda   |
| 1     | Quase certo que não vamos atingir sem intervenção drástica      |

### Fatores que afetam a confiança

| Fator                              | Impacto na confiança | Controlável? |
|------------------------------------|---------------------|-------------|
| [Fator 1: ex. progresso técnico]  | [+/-]               | [Sim/Não]   |
| [Fator 2: ex. dependência externa]| [+/-]               | [Sim/Não]   |

### O que aumentaria a confiança
1. [Ação ou evento que aumentaria confidence em +2]
2. [Ação ou evento]

### O que diminuiria a confiança
1. [Risco ou evento que diminuiria confidence em -2]
2. [Risco]
```

### Regras de uso
- Confidence é atualizado no mínimo quinzenalmente
- Se confidence de um KR cai abaixo de 4/10: escalação obrigatória
- Se confidence de todos os KRs de um Objective está abaixo de 5: questionar o Objective
- Confidence é do INDIVÍDUO, não do grupo (evitar groupthink — média depois)

---

## 6. Retrospective Block

### Propósito
Avaliar o ciclo de OKR após sua conclusão para aprender e melhorar o próximo ciclo.

### Template

```markdown
## OKR Retrospective — [Período]

**Data:** [YYYY-MM-DD]
**Participantes:** [agentes envolvidos]

### Scoring final

| Objective / KR        | Target | Resultado | Score (0-1.0) | Avaliação    |
|-----------------------|--------|-----------|---------------|-------------|
| **Objective: [título]** |      |           | [média dos KRs]|            |
| KR1: [descrição]      | [val]  | [val]     | [0-1.0]       | [qualitativa]|
| KR2: [descrição]      | [val]  | [val]     | [0-1.0]       | [qualitativa]|
| KR3: [descrição]      | [val]  | [val]     | [0-1.0]       | [qualitativa]|

### Interpretação dos scores
- 0.0-0.3: Falha significativa — entender por que e se o target fazia sentido
- 0.4-0.6: Progresso parcial — normal para Aspirational OKRs
- 0.7-1.0: Sucesso — se >0.9 em Aspirational, o target era fácil demais?
- 1.0+ em Committed: Esperado e necessário

### O que funcionou
1. [Prática ou decisão que contribuiu positivamente para os OKRs]
2. [...]

### O que não funcionou
1. [O que tentamos e não deu resultado — e por quê]
2. [...]

### Surpresas (positivas e negativas)
1. [Algo que não esperávamos e que impactou os OKRs]

### Qualidade do OKR em si (meta-avaliação)
| Pergunta                                          | Score (1-5) | Nota           |
|--------------------------------------------------|-------------|----------------|
| O Objective era inspiracional e claro?            |             |                |
| Os KRs mediam o que importava (outcome)?          |             |                |
| Os targets eram ambiciosos mas alcançáveis?        |             |                |
| As initiatives estavam bem priorizadas?            |             |                |
| O tracking era suficiente para ajustes?            |             |                |
| O alinhamento cross-squad estava claro?            |             |                |

### Carry-overs (o que leva para o próximo ciclo)
- [ ] [KR não atingido que continua relevante → incluir no próximo OKR]
- [ ] [Initiative não concluída → priorizar ou matar]

### Lições para o próximo ciclo
1. [Lição 1 — ação concreta para o próximo OKR cycle]
2. [Lição 2]
3. [Lição 3]
```

### Regras de retrospectiva
1. **Blameless:** Focar no sistema, não nas pessoas
2. **Data-driven:** Resultados concretos, não narrativas
3. **Action-oriented:** Cada lição deve gerar ação para o próximo ciclo
4. **Honest:** Se o target era ridículo, dizer isso. Se a execução falhou, dizer isso
5. **Quick:** 45-60 minutos máximo. Retrospectiva não é therapy session

---

## 7. Alignment map — OKRs em cascata

### Propósito
Visualizar como os OKRs de cada agente se conectam e se reforçam mutuamente.

### Template

```markdown
## OKR Alignment Map — [Período]

### Company-level OKR (CEO)
**O:** [Objective da empresa]
  KR1: [KR empresa]
  KR2: [KR empresa]
  KR3: [KR empresa]

### Agent OKRs (contribuem para Company OKR)

COO — O: [Objective do COO]
  ↳ Contribui para Company KR[X]
  KR1: [...]
  KR2: [...]

CMO — O: [Objective do CMO]
  ↳ Contribui para Company KR[Y]
  KR1: [...]
  KR2: [...]

CTO — O: [Objective do CTO]
  ↳ Contribui para Company KR[Z]
  KR1: [...]
  KR2: [...]

CIO — O: [Objective do CIO]
  ↳ Contribui para Company KR[X] e KR[Z]
  KR1: [...]

CAIO — O: [Objective do CAIO]
  ↳ Contribui para Company KR[Y]
  KR1: [...]

### Dependências entre OKRs de agentes
| De (agente/KR) | Para (agente/KR) | Natureza da dependência      |
|----------------|------------------|------------------------------|
| CIO/KR1        | CAIO/KR2         | Dados necessários para modelo|
| CTO/KR3        | CMO/KR1          | Feature para campanha        |
```

---

## 8. Checklist de qualidade do ciclo de OKR

```markdown
### Antes do quarter
- [ ] OKRs da empresa definidos pelo CEO
- [ ] Cada agente tem 1-2 Objectives com 2-4 KRs cada
- [ ] Alinhamento mapeado (cada KR de agente conecta a um KR da empresa)
- [ ] Dependências identificadas e comunicadas
- [ ] Confidence scores iniciais registrados
- [ ] Initiatives vinculadas e priorizadas
- [ ] OKRs comunicados a todos

### Durante o quarter
- [ ] Check-in semanal de progresso (5 min por OKR)
- [ ] Confidence update quinzenal
- [ ] Mid-quarter review formal (semana 5-6)
- [ ] Ajustes de rota documentados (se houver)
- [ ] Escalação de KRs com confidence < 4

### Após o quarter
- [ ] Scoring final de todos os KRs
- [ ] Retrospectiva conduzida
- [ ] Lições documentadas
- [ ] Carry-overs definidos
- [ ] Input para OKRs do próximo quarter
```
