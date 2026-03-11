# Bet Sizing — Framework de Dimensionamento de Apostas Estratégicas

## Origem e Contexto

Todo negócio é um portfólio de apostas. A questão não é se você está apostando — é se está
dimensionando suas apostas conscientemente ou por acidente. A maioria das organizações aloca
recursos por inércia (o mesmo que ano passado + 10%), por política (quem grita mais alto), ou
por otimismo (tudo vai dar certo, então investe em tudo igualmente).

O framework de Bet Sizing adapta conceitos de gestão de portfólio e do Kelly Criterion para
o contexto de decisões estratégicas de negócio. A ideia central: o tamanho da aposta deve ser
proporcional à sua vantagem informacional (edge) e inversamente proporcional à incerteza.
Apostas grandes quando temos alta convicção e vantagem clara. Apostas pequenas (ou zero)
quando estamos explorando ou não temos edge.

Diferente de venture capital (onde 1 em 10 investimentos carrega o fundo), uma empresa
operacional não pode ter 9 apostas falhando. O framework equilibra a necessidade de ousadia
com a realidade de que cada aposta consome recursos que poderiam estar em outro lugar.

## Quando Usar

- Na alocação anual ou semestral de recursos (budget, headcount, atenção)
- Ao avaliar uma nova oportunidade significativa de investimento
- Quando precisar decidir entre dobrar uma aposta ou diversificar
- Para calibrar o portfólio de iniciativas estratégicas
- Ao negociar recursos com board ou investidores
- Quando uma aposta inicial mostra sinais positivos e a tentação é escalar rápido

## Quando NÃO Usar

- Para decisões operacionais rotineiras (compra de material, contratação de reposição)
- Quando a decisão é facilmente reversível e de baixo custo
- Para justificar apostas emocionais com racionalização matemática
- Em contextos de sobrevivência onde não há portfólio — apenas uma opção

## Estrutura / Modelo

### Taxonomia de Apostas

```
TIPO DE APOSTA      | ALOCAÇÃO SUGERIDA | HORIZONTE | EXPECTATIVA
─────────────────────────────────────────────────────────────────
Core (70%)          | 60-80% recursos   | 0-12 meses| ROI previsível
  Melhorias no core business, crescimento orgânico, eficiência

Adjacent (20%)      | 15-25% recursos   | 6-24 meses| ROI provável
  Novos segmentos, novos canais, extensões de produto

Transformational(10%)| 5-15% recursos   | 12-36 meses| ROI incerto
  Novos modelos de negócio, tecnologia disruptiva, moonshots
```

### Kelly Criterion Adaptado para Negócios

O Kelly Criterion original determina a fração ótima do bankroll para apostar:

```
f* = (bp - q) / b

Onde:
  f* = fração do capital a apostar
  b  = odds (retorno por unidade apostada)
  p  = probabilidade de sucesso
  q  = probabilidade de fracasso (1 - p)
```

**Adaptação para negócios** (Half-Kelly recomendado por segurança):

```
Alocação = [(Retorno Esperado × Probabilidade de Sucesso) - Probabilidade de Fracasso]
           ÷ Retorno Esperado
           × 0.5 (fator de segurança Half-Kelly)

Exemplo:
  Retorno esperado: 5x o investimento
  Probabilidade de sucesso: 40%
  Probabilidade de fracasso: 60%

  f* = (5 × 0.40 - 0.60) / 5 = (2.0 - 0.6) / 5 = 0.28
  Half-Kelly: 0.28 × 0.5 = 14% dos recursos disponíveis
```

### Matriz de Sizing

```
                    CONVICÇÃO (baseada em evidências)
                    Baixa         Média         Alta
                ┌────────────┬────────────┬────────────┐
    Alto        │ 5-10%      │ 15-25%     │ 30-50%     │
RETORNO         │ Explore    │ Invest     │ Go Big     │
POTENCIAL       ├────────────┼────────────┼────────────┤
    Médio       │ 2-5%       │ 10-15%     │ 20-30%     │
                │ Test       │ Grow       │ Scale      │
                ├────────────┼────────────┼────────────┤
    Baixo       │ 0%         │ 2-5%       │ 10-15%     │
                │ Kill       │ Maintain   │ Optimize   │
                └────────────┴────────────┴────────────┘
```

### Scorecard de Aposta

```
APOSTA: [Nome]
Data de avaliação: [YYYY-MM-DD]
Sponsor: [quem defende]

DIMENSÃO                          SCORE (1-5)  PESO    PONDERADO
────────────────────────────────────────────────────────────────
Alinhamento com tese estratégica    [  ]        25%     [  ]
Tamanho da oportunidade (TAM)       [  ]        20%     [  ]
Vantagem competitiva (edge)         [  ]        20%     [  ]
Evidência/validação existente       [  ]        15%     [  ]
Reversibilidade da decisão          [  ]        10%     [  ]
Capacidade de execução              [  ]        10%     [  ]
────────────────────────────────────────────────────────────────
SCORE TOTAL                                             [  ]

SIZING RECOMENDADO:
  Score 4.0-5.0: Go Big (25-40% dos recursos disponíveis)
  Score 3.0-3.9: Invest (10-25%)
  Score 2.0-2.9: Explore (5-10%)
  Score < 2.0:   Kill ou Defer
```

## Processo de Aplicação (step-by-step)

### Passo 1: Inventariar as Apostas Atuais (1-2 dias)

Mapeie onde os recursos estão alocados HOJE:
- Liste todas as iniciativas com recursos dedicados
- Quantifique: headcount, budget direto, % de atenção da liderança
- Classifique cada uma como Core, Adjacent, ou Transformational
- Calcule a proporção atual (geralmente descobre-se algo como 90/8/2)

Este inventário frequentemente revela que a organização não tem nenhuma aposta
transformacional real, ou que tem recursos espalhados em 15 apostas adjacentes
sem massa crítica em nenhuma.

### Passo 2: Avaliar Cada Aposta (2-3 dias)

Para cada aposta ativa e proposta:
- Preencha o Scorecard de Aposta com o sponsor + 2 avaliadores independentes
- Estime o retorno potencial em cenários (pessimista, base, otimista)
- Estime a probabilidade de sucesso baseada em evidências, não otimismo
- Calcule o Kelly adaptado para cada aposta
- Identifique correlações entre apostas (se A falha, B também falha?)

**Regra anti-otimismo**: multiplique a probabilidade de sucesso estimada pelo
sponsor por 0.6. Pesquisas mostram que sponsors superestimam probabilidades
consistentemente em ~40%.

### Passo 3: Construir o Portfólio (1-2 dias)

Monte o portfólio balanceado:
- Total de recursos disponíveis = 100%
- Aloque Core primeiro (floor de 60% para empresas em estágio de crescimento)
- Aloque Transformational depois (cap de 15% para preservar o core)
- Adjacent recebe o restante
- Verifique que nenhuma aposta individual excede 40% dos recursos totais
- Verifique diversificação: as apostas são independentes ou correlacionadas?

**Teste de stress do portfólio**:
- "Se a maior aposta falhar completamente, sobrevivemos?" → Se não, reduza
- "Se duas apostas adjacentes falharem, o core sustenta?" → Se não, rebalanceie
- "Temos pelo menos uma aposta que pode mudar o jogo em 3 anos?" → Se não, ouse mais

### Passo 4: Definir Gates de Progressão (1 dia)

Cada aposta precisa de checkpoints claros:

```
GATE 1 (3 meses):  Validação de premissa principal
  → Continua / Pivota / Kill
  → Se continua: libera próxima tranche de recursos

GATE 2 (6 meses):  Evidência de tração
  → Escala / Mantém / Reduz / Kill
  → Se escala: aumenta alocação em X%

GATE 3 (12 meses): ROI mensurável ou path to ROI claro
  → Dobra / Mantém / Harvests / Kill
```

### Passo 5: Comunicar e Executar (ongoing)

- Comunique o portfólio para toda a liderança (transparência de alocação)
- Cada sponsor recebe budget e headcount conforme sizing
- Dashboard de acompanhamento com métricas por aposta
- Reviews mensais de health check (leading indicators)
- Reviews trimestrais de portfólio (rebalanceamento se necessário)

### Passo 6: Rebalancear Disciplinadamente (trimestral)

O portfólio muda conforme apostas evoluem:
- **Winners**: considere dobrar (mas cuidado com winner's curse)
- **Losers**: corte rápido (sunk cost fallacy é o inimigo)
- **Indefinidos**: defina prazo final para clareza
- **Novas oportunidades**: só entram se algo sai (regra one-in-one-out)

## Exemplos Práticos

### Exemplo 1: SaaS B2B com R$10M de Budget Anual

**Portfólio anterior** (por inércia):
- 12 projetos recebendo R$500K-R$1.5M cada
- Nenhum com recursos suficientes para impacto real
- 4 projetos zombie consumindo recursos sem progresso

**Portfólio recalibrado**:
- Core (65%): R$6.5M — produto principal + vendas enterprise
- Adjacent (25%): R$2.5M — dois projetos com R$1.25M cada
  - Expansão para novo segmento (score 3.8)
  - Canal de parcerias (score 3.5)
- Transformational (10%): R$1M — um moonshot
  - Produto AI-native (score 2.8 mas upside transformacional)
- Kill: 7 projetos eliminados, recursos realocados

### Exemplo 2: Quando Ir All-In

**Critérios para concentração extrema (>50% em uma aposta)**:
- Product-market fit confirmado com dados inequívocos
- Janela competitiva que fecha em 12-18 meses
- Capacidade de execução comprovada (não primeira vez)
- Downside limitado (o core sobrevive se falhar)
- Consenso da liderança baseado em evidências, não emoção

**Exemplo real**: empresa com PMF confirmado em novo segmento. Churn < 2%,
NPS > 70, pipeline 4x target. Concorrente levantou série B para entrar no
mesmo espaço. Decisão: 55% dos recursos para escalar rápido no novo segmento
por 6 meses com gate de revisão no mês 3.

### Exemplo 3: O Erro de Diversificação Excessiva

Uma startup com 30 engenheiros trabalhando em 8 produtos simultaneamente.
Média de 3.75 engenheiros por produto — abaixo do mínimo viável para qualquer um.

Após bet sizing: 3 produtos (18 eng + 8 eng + 4 eng), 5 produtos eliminados.
Resultado em 6 meses: o produto principal cresceu 3x o ritmo anterior.

## Armadilhas Comuns

1. **Peanut buttering**: espalhar recursos igualmente ("todo mundo recebe um pouquinho").
   É politicamente fácil e estrategicamente fatal. Ninguém tem recursos suficientes.

2. **Sunk cost escalation**: dobrar apostas que estão falhando porque "já investimos tanto".
   O passado é irrelevante. Avalie apenas o retorno marginal futuro.

3. **Winner's curse**: escalar apostas vencedoras sem considerar que o retorno marginal
   diminui. O primeiro R$1M pode dar 10x; o décimo R$1M pode dar 1.2x.

4. **Correlation blindness**: três apostas que parecem independentes mas todas dependem
   da mesma premissa macro. Se essa premissa falha, tudo falha junto.

5. **Confundir tamanho da aposta com coragem**: às vezes a aposta corajosa é NÃO investir
   e preservar capital para quando surgir a oportunidade certa.

6. **Political sizing**: alocar recursos baseado em senioridade política do sponsor, não
   na qualidade da oportunidade. Solução: scorecard objetivo com múltiplos avaliadores.

7. **Recency bias**: superponderar a última informação. "O trimestre passado foi ótimo,
   vamos dobrar" sem verificar se o crescimento é sustentável.

## Integração com Outros Frameworks

- **Tese Estratégica** (`vision-chief-strategic-thesis.md`): a tese define quais apostas são
  válidas; bet sizing define quanto colocar em cada uma.
- **Kill List** (`vision-chief-kill-list.md`): apostas com score baixo alimentam o kill list.
  Recursos liberados alimentam apostas maiores.
- **North Star Alignment** (`vision-chief-north-star-alignment.md`): apostas Core devem mover
  a North Star diretamente. Adjacent e Transformational podem mover métricas secundárias.
- **Execution Engine** (`coo-execution-engine.md`): o COO precisa saber o sizing para alocar
  capacidade de execução proporcionalmente.
- **AI Portfolio Strategy** (`caio-ai-portfolio-strategy.md`): apostas de AI seguem a mesma
  lógica de portfólio — quick wins, foundations, moonshots.
- **Growth Experimentation** (`cmo-growth-experimentation.md`): experimentos de growth são
  apostas pequenas que informam sizing de apostas maiores.

## Referências

- John Larry Kelly Jr., *Kelly Criterion* — dimensionamento ótimo de apostas
- Nassim Taleb, *Antifragile* — barbell strategy e convexidade
- Annie Duke, *Thinking in Bets* — calibração de probabilidades
- Howard Marks, *The Most Important Thing* — second-level thinking em investimentos
- Nagraj Kashyap, *Corporate Portfolio Management* — portfólio de iniciativas
- Amazon, *Working Backwards* — apostas irreversíveis vs reversíveis
- Geoffrey Moore, *Zone to Win* — framework de quatro zonas de investimento
- McKinsey, *Three Horizons of Growth* — base para taxonomia Core/Adjacent/Transformational
