# Nova Iniciativa — Fase 01: Formulação de Hipótese

## Objetivo desta Fase

Transformar o brief estratégico numa hipótese testável e estruturada.
A hipótese deve ser suficientemente específica para ser validada ou refutada com dados.
Esta fase força rigor analítico antes de comprometer recursos significativos.
O output principal é um documento que articula claramente o que acreditamos, porquê, e como vamos testar.

## Agentes Envolvidos

- **CEO Agent**: Validação da hipótese contra a visão estratégica de longo prazo
- **Strategy Advisor Agent**: Estruturação da hipótese e definição de métricas de validação
- **CFO Agent**: Modelação financeira da hipótese (cenários bull/base/bear)
- **CMO Agent**: Validação de mercado e análise de demand signals
- **CTO Agent**: Avaliação de feasibility técnica detalhada
- **Chief of Staff Agent**: Coordenação e documentação do processo

## Inputs Necessários

1. Brief aprovado da Fase 00 (documento fundacional)
2. Dados de mercado detalhados (competitor analysis, market trends, customer insights)
3. Dados internos relevantes (performance atual, capacidades existentes, recursos disponíveis)
4. Feedback de clientes ou potenciais clientes (qualitativo e quantitativo)
5. Benchmarks de iniciativas similares (internas ou de mercado)
6. Restrições técnicas identificadas na fase anterior
7. Framework de hipótese a utilizar (Lean Canvas, Business Model Canvas, ou similar)

## Processo (step-by-step)

### Step 1: Decomposição do Brief em Assunções
O Strategy Advisor identifica todas as assunções implícitas no brief.
Categoriza cada assunção como: validada, parcialmente validada, ou não validada.
Prioriza assunções por impacto no sucesso da iniciativa.

### Step 2: Formulação da Hipótese Central
Estrutura: "Acreditamos que [acção] resultará em [outcome] para [público-alvo]"
A hipótese deve ser específica, mensurável e time-bound.
O CEO Agent valida que a hipótese está alinhada com a direcção estratégica.

### Step 3: Definição de Métricas de Sucesso
O Strategy Advisor define KPIs primários e secundários para validação.
O CFO Agent traduz métricas em impacto financeiro quantificável.
Estabelecem-se thresholds claros: o que constitui sucesso, resultado ambíguo e fracasso.

### Step 4: Modelação Financeira
O CFO Agent cria modelo com três cenários (bull, base, bear).
Inclui análise de sensitivity para variáveis-chave.
Calcula break-even point e payback period para cada cenário.

### Step 5: Análise de Mercado Detalhada
O CMO Agent valida demand signals com dados concretos.
Analisa competitive landscape e identifica white spaces.
Documenta riscos de mercado e barreiras à adopção.

### Step 6: Technical Feasibility Deep-Dive
O CTO Agent detalha a arquitectura técnica necessária.
Identifica build vs buy decisions e dependências externas.
Estima effort técnico em story points ou person-months.

### Step 7: Síntese e Validação
O Chief of Staff consolida todos os inputs no Hypothesis Document.
Sessão de challenge com todos os agentes para stress-test da hipótese.
Documentação de riscos identificados e plano de mitigação inicial.

## Outputs / Entregáveis

1. **Hypothesis Document** — Documento estruturado com hipótese central e sub-hipóteses
2. **Financial Model (v1)** — Modelo com cenários bull/base/bear e sensitivity analysis
3. **Market Validation Report** — Análise de mercado com demand signals e competitive insights
4. **Technical Feasibility Report** — Avaliação técnica detalhada com estimativas de effort
5. **Assumptions Register** — Lista de todas as assunções categorizadas por status de validação
6. **Success Metrics Framework** — KPIs definidos com thresholds de sucesso/fracasso
7. **Risk Register (v1)** — Actualização do risk register com novos riscos identificados

## Quality Gates

- [ ] A hipótese central é específica, mensurável e time-bound
- [ ] Existem pelo menos 3 métricas de sucesso quantificáveis definidas
- [ ] O modelo financeiro cobre cenários bull, base e bear
- [ ] A análise de mercado está suportada por dados (não apenas opinião)
- [ ] A feasibility técnica foi avaliada com estimativa de effort
- [ ] Todas as assunções críticas estão identificadas e categorizadas
- [ ] O risk register foi actualizado com mitigações propostas

## Critérios para Avançar

Para avançar para a Fase 02 (Design), é necessário:
1. Hipótese central aprovada por CEO Agent e Strategy Advisor
2. Modelo financeiro valida viabilidade no cenário base (mínimo)
3. Não existem showstoppers técnicos identificados pelo CTO Agent
4. Market validation mostra sinais positivos de demand
5. Pelo menos 70% das assunções críticas estão validadas ou com plano de validação
6. Budget para a fase de design está aprovado pelo CFO Agent

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Confirmation bias na validação de hipótese | Alta | Alto | Designar um agente como "devil's advocate" |
| Dados de mercado insuficientes ou desactualizados | Média | Alto | Triangular múltiplas fontes, usar proxies quando necessário |
| Modelo financeiro baseado em assunções frágeis | Média | Alto | Sensitivity analysis rigorosa, stress-test de variáveis |
| Hipótese demasiado broad para ser testável | Média | Médio | Decompor em sub-hipóteses específicas e testáveis |
| Desacordo entre agentes sobre viabilidade | Baixa | Alto | Processo de decisão estruturado com critérios claros |

## Templates a Usar

- `templates/hypothesis-canvas.md` — Canvas para estruturação de hipóteses
- `templates/financial-model.md` — Template de modelação financeira com cenários
- `templates/market-analysis.md` — Template de análise de mercado
- `templates/technical-feasibility.md` — Template de avaliação técnica
- `templates/assumptions-register.md` — Template de registo de assunções

## Duração Estimada

- **Mínimo**: 5 dias úteis (dados disponíveis, hipótese simples)
- **Típico**: 10 dias úteis (requer alguma recolha de dados)
- **Máximo**: 15 dias úteis (hipótese complexa, múltiplos mercados)
- **Deadline recomendado**: Não exceder 3 semanas para manter momentum
