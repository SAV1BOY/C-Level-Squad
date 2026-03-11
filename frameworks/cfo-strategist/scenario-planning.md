# Planejamento por Cenários — Framework de Decisão sob Incerteza

## Propósito e Contexto

Cenários não são previsões — são narrativas estruturadas sobre futuros plausíveis que ajudam a
organização a se preparar para múltiplas realidades. A diferença entre planejamento tradicional
(um plano + esperança) e scenario planning (múltiplos planos + triggers de ativação) é a
diferença entre ser surpreendido e estar preparado.

Este framework adapta o método de cenários originado na Shell nos anos 1970 para o contexto de
empresas de tecnologia, onde a incerteza é ainda maior e os ciclos de mudança são mais rápidos.
Não se trata de acertar o futuro — se trata de estar pronto para reagir rápido qualquer que
seja o futuro que se materialize.

## Quando Usar

- No planejamento anual (complementar ao budget determinístico)
- Quando o ambiente externo tem alta incerteza (economia, regulação, competição)
- Na preparação para board meetings (boards amam cenários)
- Em decisões irreversíveis de alto impacto (expansão, pivot, M&A)
- Quando a equipe executiva tem visões divergentes sobre o futuro
- Em crises para mapear possíveis desdobramentos

## Componentes do Framework

### 1. Estrutura de Cenários

**Modelo 4 Cenários (recomendado):**

| Cenário | Definição | Probabilidade |
|---------|-----------|---------------|
| **Base** | Continuidade do momento atual com ajustes incrementais | 40-50% |
| **Upside** | Coisas dão mais certo que o esperado | 15-25% |
| **Downside** | Deterioração significativa mas gerenciável | 15-25% |
| **Stress/Catástrofe** | Cenário extremo mas plausível | 5-10% |

**Importante:** Probabilidades devem somar 100%. Cada cenário deve ser internamente
consistente (as variáveis se reforçam mutuamente).

### 2. Variáveis-Chave (Uncertainty Drivers)

Identifique as 3-5 variáveis com maior incerteza e maior impacto:

**Variáveis Externas:**
- Crescimento econômico / recessão
- Taxa de juros e disponibilidade de capital
- Regulação do setor
- Comportamento do consumidor
- Movimentos de grandes concorrentes

**Variáveis de Mercado:**
- Velocidade de adoção do produto/categoria
- Consolidação do mercado (M&A)
- Entrada de grandes players
- Mudança tecnológica disruptiva

**Variáveis Internas:**
- Capacidade de execução (hiring, delivery)
- Retenção de talentos-chave
- Sucesso de novos produtos
- Eficiência de go-to-market

### 3. Matriz de Cenário

Combine as 2 variáveis mais impactantes em uma matriz 2×2:

```
                    [Variável 1: Positivo]
                           |
    Cenário C              |           Cenário A
    (Var1+, Var2-)         |           (Var1+, Var2+) = Upside
                           |
[Var 2: Negativo] ---------|---------- [Var 2: Positivo]
                           |
    Cenário D              |           Cenário B
    (Var1-, Var2-)         |           (Var1-, Var2+) = Downside
    = Stress               |
                           |
                    [Variável 1: Negativo]
```

### 4. Plano de Resposta por Cenário

Para cada cenário, definir:
- **Financial implications:** Impacto em receita, custos, runway
- **Strategic response:** O que fazer se esse cenário se materializar
- **Trigger indicators:** Sinais antecipados de que estamos entrando nesse cenário
- **Activation threshold:** Quando exatamente executar o plano de resposta
- **Pre-positioned actions:** O que fazer agora para estar pronto

## Processo Passo-a-Passo

### Fase 1: Identificação de Incertezas (2-3 dias)
1. Workshop com C-level: listar todas as incertezas relevantes
2. Classificar por impacto (alto/médio/baixo) e incerteza (alta/média/baixa)
3. Selecionar 3-5 variáveis de alto impacto e alta incerteza
4. Definir range de cada variável (pior caso → melhor caso)

### Fase 2: Construção de Cenários (2-3 dias)
1. Construir a matriz 2×2 com as 2 variáveis principais
2. Dar nome e narrativa para cada cenário
3. Projetar impacto financeiro de cada cenário (P&L, cash flow)
4. Validar consistência interna de cada cenário

### Fase 3: Planos de Resposta (1 semana)
1. Para cada cenário, definir strategic response
2. Identificar trigger indicators e activation thresholds
3. Calcular custos e benefícios de cada plano de resposta
4. Identificar pre-positioned actions (hedge bets que fazem sentido em múltiplos cenários)

### Fase 4: Monitoramento (contínuo)
1. Dashboard de trigger indicators atualizado mensalmente
2. Revisão de cenários a cada trimestre (cenários mudam com informação nova)
3. Ativação automática quando thresholds são atingidos
4. Post-mortem: qual cenário se materializou e por quê

## Template de Cenário

```markdown
# Cenário: [Nome] — [Probabilidade]%

## Narrativa
[Parágrafo descrevendo o mundo neste cenário — o que aconteceu e por quê]

## Variáveis-Chave
| Variável | Valor neste cenário |
|----------|-------------------|
| [Var 1] | [valor] |
| [Var 2] | [valor] |
| [Var 3] | [valor] |

## Impacto Financeiro
- Receita: R$ [X] ([+/-Y%] vs. base)
- Burn rate: R$ [X]/mês
- Runway: [X] meses
- Headcount necessário: [X]

## Plano de Resposta
1. [Ação imediata]
2. [Ação em 30 dias]
3. [Ação em 90 dias]

## Trigger Indicators
- [ ] [Indicador 1]: quando [threshold específico]
- [ ] [Indicador 2]: quando [threshold específico]

## Pre-positioned Actions (fazer AGORA)
- [Ação que nos prepara para este cenário sem custo significativo]
```

## Checklist de Qualidade

- [ ] Pelo menos 4 cenários definidos (base, up, down, stress)?
- [ ] Cenários são internamente consistentes?
- [ ] Probabilidades somam ~100%?
- [ ] Cada cenário tem impacto financeiro quantificado?
- [ ] Trigger indicators são mensuráveis e monitoráveis?
- [ ] Planos de resposta foram stress-tested (são executáveis)?
- [ ] Pre-positioned actions foram implementadas?
- [ ] Dashboard de monitoramento está ativo?

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Cenários atualizados | Revisão trimestral mínima | Trimestral |
| Trigger indicators monitorados | 100% com dashboard ativo | Mensal |
| Tempo de reação a cenário ativado | < 2 semanas para executar plano | Por evento |
| Accuracy de cenários | Cenário real dentro dos ranges modelados | Anual |
| Pre-positioned actions implementadas | 100% | Contínuo |

## Referências Cruzadas

- `frameworks/cfo-strategist/financial-planning.md` — Modelo financeiro que gera os números
- `frameworks/cfo-strategist/cost-optimization.md` — Playbook para cenário downside
- `frameworks/cfo-strategist/fundraising-readiness.md` — Cenários impactam timing de fundraising
- `frameworks/vision-chief/vision-strategy-cascade.md` — Cenários podem alterar o cascade
- `frameworks/shared/risk-management.md` — Cenários como ferramenta de gestão de risco
- `frameworks/shared/crisis-management.md` — Cenário stress como trigger de crise
- `frameworks/shared/decision-framework.md` — Cenários informam decisões estratégicas
