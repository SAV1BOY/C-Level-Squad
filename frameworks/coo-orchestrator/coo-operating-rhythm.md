# Ritmo Operacional — Framework de Cadência Organizacional

## Origem e Contexto

O Ritmo Operacional é o sistema nervoso da organização. Define o que acontece quando, quem é
responsável por quê, e quais outputs são esperados em cada ciclo. Sem um ritmo claro, a
organização oscila entre dois extremos: caos (ninguém sabe o que está acontecendo) e burocracia
(reuniões infinitas sem decisão).

A inspiração vem de múltiplas fontes: o Operating System de empresas como Bridgewater (radical
transparency), o EOS (Entrepreneurial Operating System) de Gino Wickman, o modelo de cadência
da Intel sob Andy Grove, e práticas de empresas como Amazon (six-pager reviews) e Google (OKR
cadence).

O princípio fundamental: previsibilidade gera produtividade. Quando todos sabem exatamente
quando serão cobrados, quando poderão levantar problemas, e quando decisões serão tomadas,
a ansiedade organizacional diminui e a velocidade de execução aumenta. O paradoxo é que
estrutura rígida de timing libera flexibilidade de conteúdo.

## Quando Usar

- Quando a organização cresce além de 20-30 pessoas e coordenação informal não escala
- Quando decisões importantes ficam paradas esperando "a próxima reunião"
- Quando há excesso de reuniões ad hoc e sensação de "viver em reuniões"
- Quando equipes não sabem o status de outras equipes
- Na transição de startup para scale-up
- Quando um novo COO ou líder operacional assume

## Quando NÃO Usar

- Em equipes muito pequenas (< 10 pessoas) onde conversa direta resolve
- Como imposição burocrática sem adaptar à cultura existente
- Para microgerenciar equipes autônomas que estão performando bem
- Como substituto para decisões difíceis (ritmo não substitui coragem)

## Estrutura / Modelo

### Cadência Completa

```
CADÊNCIA DIÁRIA (Daily Pulse)
├── O quê: Stand-up ou async update
├── Quem: Cada equipe internamente
├── Duração: 15 min sync OU 5 min async
├── Output: Bloqueios identificados, ajuda solicitada
│
CADÊNCIA SEMANAL (Weekly Rhythm)
├── O quê: Review de métricas + decisões pendentes
├── Quem: Liderança funcional (C-Level ou Diretores)
├── Duração: 60-90 min
├── Output: Decisões tomadas, bloqueios escalados, próximos passos
│
CADÊNCIA MENSAL (Monthly Business Review)
├── O quê: Deep-dive em performance financeira e operacional
├── Quem: C-Level + Diretores relevantes
├── Duração: 2-3 horas
├── Output: Health check do negócio, ajustes táticos, forecast update
│
CADÊNCIA TRIMESTRAL (Quarterly Planning)
├── O quê: Review de OKRs, replanejamento, alocação de recursos
├── Quem: C-Level + Líderes seniores (20-40 pessoas)
├── Duração: 1-2 dias (offsite ideal)
├── Output: OKRs do próximo trimestre, prioridades atualizadas, kills
│
CADÊNCIA ANUAL (Annual Strategy)
├── O quê: Revisão da tese estratégica, planejamento de longo prazo
├── Quem: C-Level + Board (se aplicável)
├── Duração: 2-3 dias
├── Output: Tese atualizada, orçamento anual, portfólio de apostas
```

### Template — Reunião Semanal de Liderança

```
WEEKLY LEADERSHIP SYNC — [data]
Duração: 75 minutos
Facilitador: COO (rotaciona apresentação, não facilitação)

BLOCO 1: NÚMEROS (15 min)
  → Dashboard de NSM + driver metrics
  → Destaque: o que está verde, amarelo, vermelho
  → Regra: sem discussão aqui, apenas visibilidade

BLOCO 2: ROCKS/PRIORIDADES (20 min)
  → Status das 3-5 prioridades do trimestre
  → On track / At risk / Off track com ações corretivas
  → Owner de cada prioridade reporta em 3-4 minutos

BLOCO 3: DECISÕES (20 min)
  → Itens que precisam de decisão coletiva
  → Formato: contexto (2 min) → opções (2 min) → debate (5 min) → decisão
  → Máximo 2-3 decisões por semana (resto via async ou 1:1)

BLOCO 4: ISSUES (15 min)
  → Problemas cross-functional que requerem coordenação
  → IDS: Identify → Discuss → Solve
  → Se não resolve em 15 min, designa owner + deadline

BLOCO 5: WRAP-UP (5 min)
  → Recap de decisões e action items
  → Cascata: o que comunicar para equipes esta semana
  → Rating da reunião (1-5) para melhoria contínua
```

### Template — Monthly Business Review

```
MONTHLY BUSINESS REVIEW — [Mês/Ano]
Duração: 2.5 horas
Owner: CFO (números) + COO (operações) + cada líder funcional

PARTE 1: FINANCEIRO (30 min)
  → P&L real vs budget vs forecast
  → Cash position e runway
  → Unit economics atualizado (CAC, LTV, payback)
  → Alerta: qualquer item > 10% off budget

PARTE 2: PRODUTO & ENGENHARIA (30 min)
  → Releases do mês e impacto
  → DORA metrics e velocidade de entrega
  → Tech debt status e decisões de investimento
  → Roadmap: próximo mês + ajustes

PARTE 3: GO-TO-MARKET (30 min)
  → Pipeline e conversão por estágio
  → CAC e ROI por canal
  → Retenção e expansão (NRR)
  → Experimentos: resultados e aprendizados

PARTE 4: PEOPLE (20 min)
  → Headcount vs plan
  → Attrition e engajamento
  → Contratações críticas: status
  → Culture pulse: o que estamos ouvindo

PARTE 5: STRATEGIC ITEMS (30 min)
  → 1-2 deep dives em temas estratégicos
  → Formato: pre-read de 2 páginas + discussão
  → Output: decisão ou próximos passos claros

PARTE 6: FORECAST UPDATE (10 min)
  → Ajuste do forecast para o trimestre
  → Riscos e oportunidades identificados
```

## Processo de Aplicação (step-by-step)

### Passo 1: Auditar o Estado Atual (1 semana)

Antes de implementar, entenda o que já existe:
- Liste TODAS as reuniões recorrentes na organização
- Classifique: informativa, decisória, criativa, social, desconhecida
- Calcule o "custo" em horas-pessoa por semana
- Identifique: reuniões sem dono, sem agenda, sem output claro
- Pergunte: que reunião, se cancelada, ninguém sentiria falta?

**Dado típico**: organizações de 100+ pessoas gastam 30-50% do tempo em reuniões,
das quais 40-60% são consideradas "pouco produtivas" pelos participantes.

### Passo 2: Desenhar a Cadência Alvo (2-3 dias)

Com o C-Level, defina:
- Quais decisões precisam de qual fórum?
- Qual é a latência aceitável para cada tipo de decisão?
- Quem PRECISA estar em cada ritual? (não quem QUER estar)
- Qual é o output obrigatório de cada ritual?

**Princípio de design**: reuniões devem ser o menor grupo possível pelo menor tempo
possível para produzir o output necessário. Cada pessoa adicional aumenta o custo
geometricamente (mais coordenação, mais opiniões, mais lentidão).

### Passo 3: Implementar Gradualmente (2-4 semanas)

Não mude tudo de uma vez:
- **Semana 1**: implemente o weekly leadership sync
- **Semana 2**: ajuste baseado no feedback; adicione daily pulse por equipe
- **Semana 3**: primeiro monthly business review
- **Semana 4**: estabilize; elimine reuniões substituídas

**Kill rule para reuniões antigas**: se a nova cadência cobre o propósito, cancele a
reunião antiga explicitamente. Não deixe ambas coexistindo.

### Passo 4: Criar Disciplina de Execução (ongoing)

O ritmo só funciona com disciplina:
- **Pontualidade**: começa e termina no horário — sem exceção
- **Preparação**: pre-reads enviados 24h antes; quem não leu, não opina
- **Facilitação**: um facilitador (geralmente COO) controla tempo e agenda
- **Documentação**: decisões e action items registrados em tempo real
- **Follow-up**: action items revisados na próxima sessão

### Passo 5: Otimizar Continuamente (mensal)

Métricas de saúde do ritmo operacional:
- % de rituais realizados conforme planejado (target: >90%)
- NPS dos participantes por ritual (survey mensal rápido)
- % de decisões tomadas no fórum correto (vs escaladas incorretamente)
- Tempo médio de resolução de bloqueios (deve diminuir com o tempo)
- % de action items completados no prazo (target: >80%)

## Exemplos Práticos

### Exemplo 1: Scale-up de 80 Pessoas

**Antes**: 47 reuniões recorrentes por semana, C-Level em reunião 70% do tempo,
decisões demorando 2-3 semanas para serem tomadas.

**Depois** (cadência implementada):
- Diário: cada squad faz async stand-up via Slack
- Semanal: leadership sync (C-Level, 75 min), squad syncs (30 min cada)
- Mensal: business review (C-Level + diretores, 2.5h)
- Trimestral: planning offsite (liderança expandida, 1.5 dias)

**Resultado**: 31 reuniões eliminadas, tempo em reuniões do C-Level caiu para 40%,
latência de decisão caiu de 2.5 semanas para 3 dias.

### Exemplo 2: Startup de 15 Pessoas

Cadência simplificada:
- Diário: stand-up de 10 min (toda empresa)
- Semanal: all-hands de 45 min (números + demo + discussão)
- Mensal: founder + leads review de 2h
- Trimestral: half-day de planejamento
- Sem monthly business review formal (incorporado no semanal)

### Exemplo 3: O Anti-Pattern da Reunião-Que-Gera-Reunião

Uma empresa implementou weekly sync mas sem disciplina de decisão. Resultado: cada weekly
gerava 3-4 reuniões de follow-up que geravam mais follow-ups. Em 2 meses, tinham mais
reuniões que antes. Solução: regra IDS (Identify, Discuss, Solve) — se não resolve em
15 minutos, owner + deadline + async resolution.

## Armadilhas Comuns

1. **Ritual sem conteúdo**: reunião acontece no horário mas sem substância. Solução:
   output obrigatório por sessão. Se não tem output, cancele.

2. **Excesso de rituais**: cadência vira burocracia quando há ritual para tudo. Regra:
   se pode resolver com uma mensagem async, não precisa de reunião.

3. **Ritmo sem autonomia**: a cadência centraliza todas as decisões na liderança. Solução:
   defina claramente o que PRECISA subir e o que equipes decidem sozinhas.

4. **Skip de rituais em crise**: quando há crise, o primeiro instinto é cancelar o
   weekly "para ter tempo de resolver". É exatamente quando o ritual é mais necessário.

5. **Dashboard theater**: números lindos no dashboard que ninguém questiona. Solução:
   sempre pergunte "por que?" quando um número muda significativamente.

6. **Facilitação passiva**: facilitador que não corta discussões longas, não controla
   tempo, não força decisões. O COO como facilitador precisa ser assertivo.

7. **Pre-read como ficção**: ninguém lê os materiais antes. Solução: os primeiros 5 min
   são para leitura silenciosa (modelo Amazon) ou não distribua pre-reads.

## Integração com Outros Frameworks

- **Narrative Cascade** (`vision-chief-narrative-cascade.md`): os rituais da cadência são
  os veículos naturais para cascata de comunicação estratégica.
- **Execution Engine** (`coo-execution-engine.md`): o ritmo operacional é o heartbeat do
  execution engine — cadência sem execução é teatro.
- **Bottleneck Theory** (`coo-bottleneck-theory.md`): o weekly sync é onde bottlenecks
  são identificados e escalados.
- **Cross-Functional Orchestration** (`coo-cross-functional-orchestration.md`): a cadência
  define os pontos formais de sincronização entre áreas.
- **North Star Alignment** (`vision-chief-north-star-alignment.md`): NSM e drivers são o
  conteúdo principal dos rituais de review.
- **Engineering Excellence** (`cto-engineering-excellence.md`): DORA metrics e sprint reviews
  alimentam o monthly business review.

## Referências

- Andy Grove, *High Output Management* — meetings como meio de produção do gestor
- Gino Wickman, *Traction (EOS)* — Level 10 meetings e cadência empresarial
- Patrick Lencioni, *Death by Meeting* — diferenciação de tipos de reunião
- Amazon, *Working Backwards* — six-pager reviews e narrativa em reuniões
- Ray Dalio, *Principles* — radical transparency em cadências de gestão
- Keith Rabois — operating cadence para scale-ups
- Basecamp, *It Doesn't Have to Be Crazy at Work* — anti-meeting culture
