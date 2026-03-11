# Execution Engine — Framework de Conversão de Planos em Resultados

## Origem e Contexto

O Execution Engine é a máquina organizacional que converte intenção estratégica em resultados
mensuráveis de forma confiável e repetível. Não é um projeto ou uma iniciativa — é um sistema
permanente composto por três engrenagens: Cadência (ritmo), Accountability (responsabilização),
e Resultado (métricas).

A maioria das organizações tem boas estratégias e péssima execução. A razão não é falta de
talento ou esforço — é ausência de um sistema que conecte o "o que queremos fazer" ao "o que
fizemos de fato". O gap entre estratégia e resultado é preenchido por um engine de execução,
não por motivação individual.

Este framework se inspira no conceito de "execution as discipline" de Larry Bossidy e Ram Charan,
no modelo de OKR da Intel/Google, no sistema Andon da Toyota, e na cadência de accountability
do 4DX (Four Disciplines of Execution) de Chris McChesney.

## Quando Usar

- Quando a organização tem planos claros mas resultados inconsistentes
- Na implementação de OKRs ou qualquer sistema de metas
- Quando equipes "estão ocupadas" mas métricas não se movem
- Após definir a tese estratégica e portfólio de apostas
- Quando novos líderes precisam de um sistema de gestão padrão
- Em turnarounds onde execução precisa melhorar rapidamente

## Quando NÃO Usar

- Como microgerenciamento disfarçado (o engine é sobre outcomes, não atividades)
- Em fase de exploração radical onde o objetivo é aprender, não executar
- Como substituto para decisões estratégicas (executar bem a coisa errada é pior)
- Quando o problema é de pessoas, não de sistema (engine não compensa incompetência)

## Estrutura / Modelo

### As Três Engrenagens

```
┌─────────────────────────────────────────────────────┐
│                 EXECUTION ENGINE                     │
│                                                      │
│   ┌──────────┐    ┌──────────────┐    ┌──────────┐ │
│   │          │    │              │    │          │  │
│   │ CADÊNCIA │───→│ACCOUNTABILITY│───→│RESULTADO │  │
│   │          │    │              │    │          │  │
│   └────┬─────┘    └──────┬───────┘    └────┬─────┘ │
│        │                 │                  │       │
│        └─────────────────┴──────────────────┘       │
│                    FEEDBACK LOOP                     │
└─────────────────────────────────────────────────────┘

CADÊNCIA: quando revisamos, decidimos, ajustamos
ACCOUNTABILITY: quem é responsável, como cobramos, como apoiamos
RESULTADO: o que medimos, como medimos, como celebramos/corrigimos
```

### Framework C.A.R. Detalhado

```
C — CADÊNCIA
├── Ritmo de planejamento (trimestral)
├── Ritmo de review (semanal)
├── Ritmo de ajuste (contínuo com gates mensais)
├── Ritmo de retrospectiva (mensal)
└── Ritmo de celebração (quando milestone é atingido)

A — ACCOUNTABILITY
├── Ownership claro: 1 pessoa = 1 métrica
├── Compromisso público: declarado na frente dos pares
├── Check-in regular: progresso reportado semanalmente
├── Support system: bloqueios escalados e resolvidos
└── Consequências: reconhecimento ou correção de rota

R — RESULTADO
├── Métricas leading: indicadores de esforço e direção
├── Métricas lagging: indicadores de resultado final
├── Targets específicos: número + prazo
├── Tracking visível: dashboard acessível a todos
└── Aprendizado: o que funcionou, o que não, por quê
```

### Template de OKR Operacional

```
OBJECTIVE: [Verbo + resultado qualitativo inspirador]
  Owner: [Nome] | Prazo: [Trimestre] | Status: [🔴🟡🟢]

  KR1: [Métrica específica] de [baseline] para [target]
    Owner: [Nome]
    Leading indicators: [métricas semanais que predizem o KR]
    Confidence: [Low/Med/High]
    Último update: [data] — [progresso e comentário]

  KR2: [Métrica específica] de [baseline] para [target]
    Owner: [Nome]
    Leading indicators: [métricas semanais]
    Confidence: [Low/Med/High]
    Último update: [data] — [progresso e comentário]

  KR3: [Métrica específica] de [baseline] para [target]
    Owner: [Nome]
    Leading indicators: [métricas semanais]
    Confidence: [Low/Med/High]
    Último update: [data] — [progresso e comentário]
```

## Processo de Aplicação (step-by-step)

### Passo 1: Traduzir Estratégia em OKRs (1 semana)

A ponte entre estratégia e execução são OKRs bem escritos:

**Da tese para objectives**: cada aposta da tese gera 1-2 objectives
**Dos objectives para key results**: cada objective tem 2-4 KRs mensuráveis

**Regras de ouro para KRs**:
- Tem número (meta quantitativa)
- Tem prazo (deadline explícito)
- Tem baseline (de onde partimos)
- É influenciável (a equipe pode mover)
- É verificável (qualquer pessoa pode checar se foi atingido)

**Anti-patterns de KR**:
- "Melhorar a experiência do cliente" → vago, sem número
- "Lançar feature X" → é output, não outcome
- "Reduzir churn em 50%" → se churn é 0.5%, isso é impossível; se é 40%, é fácil
  → sempre inclua baseline e target absolutos

### Passo 2: Atribuir Ownership Inequívoco (2-3 dias)

Para cada OKR e cada KR:
- **Um owner, uma métrica**: nunca co-ownership
- **Owner ≠ executor solitário**: owner é accountable pelo resultado, coordena outros
- **Owner tem autoridade**: se não pode tomar decisões sobre a métrica, não é owner real
- **Owner declarado publicamente**: na reunião de planning, cada owner diz "eu sou
  responsável por [KR], e vou atingir [target] até [data]"

**Teste de ownership**: se o KR não for atingido, quem é cobrado? Se a resposta é
"todo mundo" ou "ninguém", o ownership está errado.

### Passo 3: Construir o Sistema de Tracking (1-2 semanas)

O que não é visível não é gerenciado:

**Dashboard requirements**:
- Atualizado automaticamente (não depende de alguém "preencher")
- Acessível a todos (transparência radical)
- Mostra tendência, não apenas snapshot (estamos melhorando ou piorando?)
- Alertas para desvios significativos (> 10% off-track)

**Estrutura do dashboard**:
```
NÍVEL 1: Executive view
  → NSM + 5-7 driver metrics + semáforo (verde/amarelo/vermelho)

NÍVEL 2: Functional view
  → OKRs por área com KRs e progresso
  → Leading indicators por KR

NÍVEL 3: Team view
  → Team metrics com drill-down
  → Sprint/cycle deliverables
```

### Passo 4: Implementar o Weekly Check-in (ongoing)

O heartbeat do execution engine é o check-in semanal:

**Para cada KR, o owner reporta semanalmente**:
1. **Progresso**: confidence level (on-track / at-risk / off-track)
2. **Número**: atualização da métrica
3. **Aprendizado**: o que aprendemos esta semana
4. **Bloqueio**: preciso de ajuda com [específico]
5. **Próxima ação**: o que farei na próxima semana para mover o número

**Formato**: pode ser async (Slack, email, tool) na maioria das semanas,
com sync mensal para deep-dive nos at-risk.

### Passo 5: Criar o Loop de Correção (ongoing)

Quando algo está off-track:

```
DETECÇÃO (semana N)
  → KR classificado como at-risk ou off-track no weekly check-in
  │
ROOT CAUSE (semana N, mesma reunião)
  → Owner apresenta análise: por que está off-track?
  → É problema de execução, premissa errada, ou recurso insuficiente?
  │
DECISÃO (semana N ou N+1)
  → OPÇÃO A: Correção de rota — nova tática, mesmo target
  → OPÇÃO B: Apoio adicional — recursos ou remoção de bloqueio
  → OPÇÃO C: Ajuste de target — se premissa original estava errada
  → OPÇÃO D: Kill — se KR não é mais relevante
  │
IMPLEMENTAÇÃO (semana N+1 em diante)
  → Ação corretiva executada
  → Monitoramento intensificado (daily check até estabilizar)
  │
VERIFICAÇÃO (semana N+2 ou N+3)
  → Correção funcionou? Se sim, volta ao ritmo normal
  → Não funcionou? Escalate para próximo nível
```

### Passo 6: Retrospectiva de Ciclo (final do trimestre)

Ao final de cada ciclo de OKR:
- **Scoring**: cada KR recebe score de 0 a 1.0 (0.7 = bom no modelo Google)
- **Padrões**: quais equipes/áreas consistentemente atingem? Quais não?
- **Aprendizados**: o que aprendemos sobre nossa capacidade de execução?
- **Calibração**: estamos colocando targets ambiciosos demais ou fáceis demais?
- **Melhoria do engine**: o que mudar no processo para o próximo ciclo?

## Exemplos Práticos

### Exemplo 1: De "Ocupados" para "Produtivos"

**Antes**: equipe de 12 engenheiros "trabalhando muito" mas velocity de entrega caindo.
Ninguém sabe por que. Weekly é lista de tarefas, não outcomes.

**Engine implementado**:
- Objective: "Entregar valor mensurável aos clientes toda sprint"
- KR1: Features entregues com adoption > 30% em 30 dias (de 1 para 3 por sprint)
- KR2: Cycle time de idea-to-production < 5 dias (baseline: 14 dias)
- KR3: Zero sprints com zero features shipped (baseline: 2 por trimestre)

**Resultado em 2 trimestres**: velocity real (medida por adoption, não story points)
aumentou 2.4x. O problema era excesso de WIP — muitas coisas em paralelo, nada terminava.

### Exemplo 2: Accountability sem Microgerenciamento

**Framework de 1:1 orientado a outcomes**:
```
1:1 SEMANAL (30 min)
  5 min: Como você está? (pessoal, energia, motivação)
  10 min: Status dos seus KRs (números, não atividades)
  10 min: Bloqueios — o que posso fazer para ajudar?
  5 min: Uma coisa que aprendi esta semana
```

O gestor pergunta "como posso ajudar?" não "o que você fez?". A diferença
é entre accountability de suporte e accountability de controle.

### Exemplo 3: O Perigo do Teatro de Execução

Empresa implementou OKRs mas sem mudar comportamentos:
- KRs definidos no início do trimestre e esquecidos
- Scoring no final sem ação intermediária
- Meetings de review viraram apresentações de PowerPoint
- Zero kills ou ajustes durante o trimestre

**Correção**: implementação do weekly check-in async com bot que cobra atualização
toda sexta. Se não atualiza, aparece como "unknown" no dashboard — visibilidade
como incentivo.

## Armadilhas Comuns

1. **Output vs Outcome**: medir atividades (features lançadas) em vez de resultados
   (clientes ativos). O engine deve medir outcomes.

2. **Accountability punitiva**: cobrar culpados em vez de resolver problemas. A accountability
   saudável é "como ajudamos a atingir?" não "por que você falhou?"

3. **OKR como to-do list**: OKRs com 15 KRs que são tarefas disfarçadas. Máximo 4 KRs
   por objective, e cada KR é um resultado mensurável.

4. **Cadência sem disciplina**: reuniões acontecem mas sem preparação, sem decisão,
   sem follow-up. O ritual vira teatro.

5. **Tracking manual**: se alguém precisa preencher uma planilha manualmente toda semana,
   eventualmente para de preencher. Automatize o máximo possível.

6. **Ignorar leading indicators**: só olhar lagging metrics (receita, churn) que mudam
   devagar. Quando percebe o problema, já é tarde. Monitore leading indicators semanalmente.

7. **Engine sem poder**: o sistema identifica problemas mas ninguém tem autoridade para
   realocar recursos ou mudar prioridades. O engine precisa estar conectado a decisões reais.

## Integração com Outros Frameworks

- **Operating Rhythm** (`coo-operating-rhythm.md`): o ritmo operacional é a cadência do engine;
  o engine adiciona accountability e resultado ao ritmo.
- **Bottleneck Theory** (`coo-bottleneck-theory.md`): o engine identifica onde a execução
  trava; a teoria de constraints direciona a correção.
- **Process Antifragility** (`coo-process-antifragility.md`): o engine funciona em condições
  normais; antifragility garante que funciona em crise.
- **North Star Alignment** (`vision-chief-north-star-alignment.md`): a árvore de métricas da
  NSM define O QUE medir; o engine define COMO cobrar e corrigir.
- **Bet Sizing** (`vision-chief-bet-sizing.md`): recursos alocados pelo bet sizing são
  executados pelo engine com accountability proporcional.
- **Engineering Excellence** (`cto-engineering-excellence.md`): DORA metrics alimentam o
  engine como leading indicators de capacidade de entrega.

## Referências

- Larry Bossidy & Ram Charan, *Execution: The Discipline of Getting Things Done*
- Chris McChesney et al, *The 4 Disciplines of Execution (4DX)*
- John Doerr, *Measure What Matters* — OKRs
- Andy Grove, *High Output Management* — output-oriented management
- Toyota Production System — Andon, visual management, cadência
- Christina Wodtke, *Radical Focus* — OKRs para startups
- Eliyahu Goldratt, *The Goal* — throughput como métrica de sistema
