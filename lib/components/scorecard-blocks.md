# Scorecard Blocks — Blocos Reutilizáveis para Scorecards Executivos

> Referência do C-Level Squad para construção de scorecards que informam decisões.
> Um bom scorecard não é uma tabela de números — é uma ferramenta de decisão que destaca o que precisa de atenção.

---

## 1. KPI Row Template

### Propósito
Linha padronizada para cada KPI no scorecard, garantindo informação completa e acionável em uma visualização rápida.

### Template

```markdown
| KPI Name | Owner | Target | Actual | Prev. Period | Trend | Var. | Status | Action trigger |
|----------|-------|--------|--------|-------------|-------|------|--------|----------------|
| [nome]   | [DRI] | [valor]| [valor]| [valor]     | [↑↓→] | [%]  | [🟢🟡🔴]| [se 🔴: ação]  |
```

### Definição de cada campo

| Campo           | Descrição                                                    | Formato                    |
|-----------------|--------------------------------------------------------------|----------------------------|
| **KPI Name**    | Nome claro e não ambíguo da métrica                          | Texto curto (máx 30 chars) |
| **Owner**       | Agente responsável por esta métrica                          | CEO/COO/CMO/CTO/CIO/CAIO  |
| **Target**      | Meta para o período                                          | Número com unidade          |
| **Actual**      | Valor real medido no período                                 | Número com unidade          |
| **Prev. Period**| Valor do período anterior (para comparação)                  | Número com unidade          |
| **Trend**       | Direção de movimento nos últimos 3+ períodos                 | ↑ ↓ → (ou arrow emoji)     |
| **Variance**    | Diferença entre actual e target, em percentual               | +X% ou -X%                  |
| **Status**      | Classificação do traffic light                               | 🟢 🟡 🔴                    |
| **Action trigger**| Ação automática quando status é amarelo ou vermelho        | Texto descritivo             |

### Exemplo completo

```markdown
| KPI                    | Owner | Target | Actual | Prev.  | Trend | Var.  | Status | Action trigger                  |
|------------------------|-------|--------|--------|--------|-------|-------|--------|---------------------------------|
| MRR                    | CEO   | R$2.5M | R$2.3M | R$2.2M | ↑     | -8%   | 🟡     | Review pipeline com CMO         |
| Monthly churn           | COO   | 3.0%   | 4.2%   | 3.8%   | ↑     | +40%  | 🔴     | War room de retenção em 48h     |
| NPS                    | COO   | 50     | 42     | 45     | ↓     | -16%  | 🟡     | Root cause analysis esta semana |
| CAC                    | CMO   | R$150  | R$135  | R$142  | ↓     | -10%  | 🟢     | —                               |
| Platform uptime        | CTO   | 99.9%  | 99.95% | 99.8%  | ↑     | +0.05%| 🟢     | —                               |
| Data quality score     | CIO   | 85%    | 78%    | 80%    | ↓     | -8%   | 🟡     | Audit de top 5 datasets         |
| AI adoption rate       | CAIO  | 40%    | 32%    | 28%    | ↑     | -20%  | 🟡     | Training session para laggards  |
```

---

## 2. Traffic Light Indicator

### Propósito
Sistema visual consistente para classificar o status de cada KPI, eliminando ambiguidade sobre "como estamos".

### Regras de classificação

```markdown
🟢 VERDE — On Target
  Condição: Actual está dentro de [target - threshold verde]
  Threshold padrão: ≤ 5% de desvio do target
  Ação: Nenhuma. Manter o curso.
  Report: Menção breve no scorecard.

🟡 AMARELO — At Risk
  Condição: Actual está entre [threshold verde] e [threshold vermelho]
  Threshold padrão: 5-15% de desvio do target
  Ação: Root cause analysis em 7 dias. Plano de correção em 14 dias.
  Report: Explicação de 2-3 linhas no scorecard + ação proposta.

🔴 VERMELHO — Off Target
  Condição: Actual está além do [threshold vermelho]
  Threshold padrão: >15% de desvio do target
  Ação: Escalação imediata. Plano de ação em 48h. Review semanal até voltar a amarelo.
  Report: Deep dive obrigatório com causa raiz + plano + timeline.
```

### Thresholds customizados por tipo de KPI

| Tipo de KPI        | Verde (≤)   | Amarelo       | Vermelho (>)  | Razão                              |
|--------------------|-------------|---------------|---------------|------------------------------------|
| Revenue (MRR, ARR) | 5% off      | 5-15% off     | 15% off       | Impacto financeiro direto          |
| Churn rate         | 10% acima   | 10-30% acima  | 30% acima     | Mais tolerância pois é volátil     |
| NPS                | 5 pontos    | 5-15 pontos   | 15 pontos     | Escala diferente                   |
| Uptime (SLA)       | 0.05% off   | 0.05-0.2% off | 0.2% off      | High sensitivity para infra        |
| Conversion rate    | 10% off     | 10-25% off    | 25% off       | Mais tolerância pois depende de volume |
| Cost/efficiency    | 5% acima    | 5-20% acima   | 20% acima     | Impacto em unit economics          |

### Regra de override
- KPI com trend ↓ por 3 períodos consecutivos: elevar um nível (verde→amarelo, amarelo→vermelho), independente do threshold
- KPI com risco de cruzar threshold no próximo período (projeção): elevar um nível proativamente

---

## 3. Trend Arrow

### Propósito
Indicar a direção de movimento da métrica ao longo de múltiplos períodos, complementando o status pontual.

### Definição

```markdown
↑ (UP): Métrica melhorou nos últimos 3 períodos consecutivos
  Para métricas "higher is better" (revenue, NPS): valor subiu
  Para métricas "lower is better" (churn, CAC): valor desceu

↓ (DOWN): Métrica piorou nos últimos 3 períodos consecutivos
  Inverso do acima

→ (FLAT): Métrica estável (variação <3% entre períodos)

↗ (UP SLIGHT): Melhoria em 2 de 3 períodos, sem consistência clara

↘ (DOWN SLIGHT): Piora em 2 de 3 períodos, sem consistência clara
```

### Combinação Trend × Status para priorização

| Trend | Status 🟢 | Status 🟡 | Status 🔴 |
|-------|-----------|-----------|-----------|
| ↑     | Celebrar  | Monitorar (melhorando) | Monitorar de perto (recuperando?) |
| →     | OK        | Atenção (estagnado) | Ação urgente (não está melhorando) |
| ↓     | Atenção precoce | Ação necessária | Crise — escalação imediata |

---

## 4. Target vs. Actual Comparison

### Propósito
Visualizar de forma clara onde estamos vs. onde deveríamos estar, incluindo trajectory para fim do período.

### Template

```markdown
## Target vs. Actual — [KPI] — [Período]

### Snapshot atual
- **Target (fim do período):** [valor]
- **Actual (hoje):** [valor]
- **Run rate projetado:** [valor] — baseado em [últimos N períodos]
- **Gap:** [valor absoluto] ([%])
- **On track para target?** [Sim / Não — falta X por período para alcançar]

### Trajectory visual

| Período  | Target acumulado | Actual acumulado | Gap   |
|----------|-----------------|-----------------|-------|
| Mês 1    | [valor]         | [valor]         | [+/-] |
| Mês 2    | [valor]         | [valor]         | [+/-] |
| Mês 3    | [valor]         | [valor]         | [+/-] |
| Projeção | [target final]  | [projeção]      | [+/-] |

### Análise
[Se gap > 10%: O que causou o gap? O que precisa mudar para fechar?]
[Se on track: O que está funcionando? É sustentável?]
```

### Cálculo de run rate

```
Run Rate = (Actual acumulado / Períodos transcorridos) × Total de períodos

Exemplo:
- Target anual: R$30M
- Actual em Março (3 meses): R$6.5M
- Run rate: (R$6.5M / 3) × 12 = R$26M
- Gap: R$30M - R$26M = R$4M (13.3% abaixo do target)
- Para atingir target: precisa de R$2.6M/mês nos 9 meses restantes (vs. R$2.17M/mês atual)
```

---

## 5. Variance Analysis

### Propósito
Explicar POR QUE a métrica está diferente do esperado, decompondo a variância em fatores.

### Template

```markdown
## Variance Analysis — [KPI] — [Período]

### Variância total
- **Target:** [valor]
- **Actual:** [valor]
- **Variância:** [valor absoluto] ([%])

### Decomposição da variância

| Fator                        | Impacto   | Direção | Explicação                          |
|------------------------------|-----------|---------|-------------------------------------|
| [Fator 1: ex. volume]       | [R$X/X%] | [+/-]   | [Mais/menos clientes que esperado]  |
| [Fator 2: ex. preço]        | [R$X/X%] | [+/-]   | [Mudança de mix ou pricing]         |
| [Fator 3: ex. sazonalidade] | [R$X/X%] | [+/-]   | [Efeito sazonal não previsto]       |
| [Fator 4: ex. one-off]      | [R$X/X%] | [+/-]   | [Evento não recorrente]             |
| **Variância total**          | **[R$X/X%]** |     |                                     |

### Variância recorrente vs. one-off
- **Recorrente (vai continuar):** [R$X] — Requer ajuste de forecast
- **One-off (não se repete):** [R$X] — Não requer ajuste

### Ação
[Baseado na decomposição, qual ação é necessária?]
```

### Exemplo

```markdown
### Variância total: MRR R$200K abaixo do target

| Fator                 | Impacto    | Direção | Explicação                              |
|-----------------------|------------|---------|----------------------------------------|
| Churn acima do esperado| -R$120K   | -       | 15 clientes enterprise churned (vs. 8 esperados) |
| New business abaixo   | -R$150K   | -       | Pipeline menor que projetado             |
| Expansion revenue     | +R$70K    | +       | Upsell em 3 contas grandes superou target |
| **Variância total**   | **-R$200K**|        |                                          |

Recorrente: Churn trend (R$120K) — necessita programa de retenção
One-off: Pipeline fraco em fevereiro (carnaval) — deve normalizar
```

---

## 6. Commentary Section

### Propósito
Narrativa qualitativa que complementa os números, fornecendo contexto que métricas sozinhas não capturam.

### Template

```markdown
## Commentary — [Período]

### Narrativa geral (3-5 frases)
[Resumo do período em linguagem simples. O que definiu este período? Como nos sentimos sobre a performance?]

### O que funcionou
- [Item 1: ação específica que gerou resultado positivo]
- [Item 2]

### O que não funcionou
- [Item 1: o que tentamos e não deu certo + lição aprendida]
- [Item 2]

### Mudanças de contexto
[Algo mudou no mercado, na equipe, na estratégia que afeta a leitura dos números?]

### Outlook para próximo período
[Expectativa informada para o próximo período. Otimista/neutro/cauteloso e por quê]
```

### Instruções
- Commentary não repete números (os números estão no scorecard)
- Commentary explica o "por quê" e o "e daí?"
- Ser honesto: se não sabemos por que algo aconteceu, dizer isso
- Evitar spin positivo em resultados negativos — o scorecard é para aprender, não para impressionar

---

## 7. Action Trigger

### Propósito
Definir antecipadamente quais ações são disparadas quando uma métrica atinge determinado threshold, eliminando delay entre detecção e ação.

### Template

```markdown
## Action Triggers — [Scorecard]

| KPI              | Trigger condition             | Ação automática                      | Owner | SLA      |
|------------------|-------------------------------|--------------------------------------|-------|----------|
| Churn rate       | >4% por 2 meses consecutivos | Convocar war room de retenção        | COO   | 48h      |
| NPS              | <35 em qualquer medição       | Root cause analysis + plano de ação  | COO   | 7 dias   |
| Uptime           | <99.5% no mês                | Post-mortem obrigatório              | CTO   | 5 dias   |
| CAC              | >R$200 por 2 meses            | Review de canais com CMO             | CMO   | 7 dias   |
| Burn rate        | >120% do planejado            | Revisão de budget com CEO            | COO   | 48h      |
| Pipeline coverage| <3× do target de quarter      | Pipeline generation sprint           | CMO   | 7 dias   |
| Data quality     | <70% em qualquer dataset crítico| Data quality sprint                | CIO   | 14 dias  |
| Model accuracy   | Degradação >5% vs. baseline  | Model retraining + investigation     | CAIO  | 7 dias   |
```

### Regras de action triggers
1. Trigger deve ser objetivo (baseado em número, não julgamento)
2. Ação deve ser específica (não "investigar", mas "convocar reunião com X, Y, Z")
3. SLA deve ser curto o suficiente para ser útil (não "quando possível")
4. Owner deve ser uma pessoa, não um comitê
5. Triggers são revisados trimestralmente (thresholds podem mudar com crescimento)

---

## 8. Owner Assignment

### Propósito
Definir claramente quem é responsável por cada KPI e qual o nível de accountability.

### Template

```markdown
## KPI Ownership Map

| KPI              | Primary owner | Secondary owner | Accountability level            |
|------------------|--------------|-----------------|----------------------------------|
| MRR              | CEO          | CMO             | Reporta em toda board meeting     |
| Churn rate       | COO          | CTO             | Reporta semanalmente se amarelo+  |
| NPS              | COO          | CMO             | Reporta mensalmente               |
| CAC              | CMO          | COO             | Reporta mensalmente               |
| LTV:CAC          | CEO          | CMO             | Reporta trimestralmente           |
| Uptime           | CTO          | CIO             | Reporta se incidente              |
| Release velocity | CTO          | COO             | Reporta mensalmente               |
| Data quality     | CIO          | CTO             | Reporta mensalmente               |
| Compliance score | CIO          | CEO             | Reporta trimestralmente           |
| AI ROI           | CAIO         | CTO             | Reporta trimestralmente           |
```

### Responsabilidades do KPI owner
1. Definir target no início do período
2. Monitorar com frequência adequada (no mínimo semanal)
3. Reportar status conforme cadência definida
4. Investigar desvios proativamente (não esperar alguém perguntar)
5. Propor ações corretivas quando fora do target
6. Escalar quando ação corretiva requer recursos ou decisão além do seu mandato

---

## 9. Formatting Guidance — Padrões visuais

### Cores e símbolos padrão do C-Level Squad

```
Status:
  🟢 Verde  = On target / Saudável / Aprovado
  🟡 Amarelo = At risk / Atenção necessária / Pendente
  🔴 Vermelho = Off target / Crítico / Rejeitado
  ⚪ Cinza   = Sem dados / Não aplicável / Futuro

Trend:
  ↑  = Melhorando (3+ períodos)
  ↗  = Levemente melhorando
  →  = Estável
  ↘  = Levemente piorando
  ↓  = Piorando (3+ períodos)

Prioridade:
  🔥 = Urgente (ação em <48h)
  ⚡ = Alta prioridade (ação em <7 dias)
  📌 = Normal (ação no ciclo regular)
```

### Layout do scorecard completo

```markdown
# Scorecard Executivo — [Período]

**Atualizado em:** [data]
**Próxima revisão:** [data]

## North Star Metric
[Uma linha dedicada à métrica mais importante]

## Financial KPIs
[3-5 métricas financeiras]

## Growth KPIs
[3-5 métricas de crescimento]

## Product/Technology KPIs
[3-5 métricas de produto e tech]

## Operational KPIs
[3-5 métricas operacionais]

## AI/Data KPIs
[2-3 métricas de AI e dados]

## Action items gerados por este scorecard
[Lista de ações disparadas pelos action triggers]
```
