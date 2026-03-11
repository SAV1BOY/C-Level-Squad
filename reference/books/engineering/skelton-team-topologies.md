# Team Topologies — Matthew Skelton & Manuel Pais (2019)

## Resumo Executivo

Skelton e Pais apresentam um modelo para organizar times de tecnologia de forma que otimize
o fluxo de entrega de software. Baseado em Conway's Law (a arquitetura do sistema reflete
a estrutura da organização), o livro define quatro tipos fundamentais de times e três modos
de interação, criando uma linguagem comum para design organizacional de engineering.

A tese: a estrutura de times é decisão arquitetural. Se os times não estão organizados
para suportar o fluxo de valor, nenhuma prática técnica compensa.

## Conceitos-Chave

### Conway's Law (e Inverse Conway Maneuver)
- "Organizations design systems that mirror their own communication structure"
- Se quer architecture X, organize times para que a comunicação reflita X
- **Inverse Conway Maneuver**: Estruture times para produzir a arquitetura desejada
- Não lute contra Conway's Law — use-a a seu favor

### Four Fundamental Team Types
1. **Stream-Aligned Team**: Alinhado a um fluxo de valor/domínio de negócio
   - É o tipo principal — a maioria dos times deve ser stream-aligned
   - Responsável end-to-end por uma fatia do negócio
   - Minimiza handoffs e dependências
   - Objetivo: fast flow of change (da ideia à produção)

2. **Enabling Team**: Ajuda stream-aligned teams a superar obstacles
   - Especialistas que treinam e capacitam outros times
   - Temporários na interação — o objetivo é que o stream-aligned team absorva a capability
   - Exemplos: DevOps enablement, security champions, data literacy

3. **Complicated-Subsystem Team**: Especialistas em subsistemas complexos
   - Necessário quando a complexidade técnica excede o que um stream-aligned team pode dominar
   - Exemplos: ML/AI engine, motor de regras complexas, codec de vídeo
   - Reduz cognitive load do stream-aligned team

4. **Platform Team**: Fornece serviços internos para acelerar stream-aligned teams
   - Self-service: os stream-aligned teams usam a plataforma sem pedir permissão
   - Reduz cognitive load de infra e operações
   - Trata times internos como clientes — UX de plataforma importa
   - Exemplos: CI/CD platform, cloud infrastructure, observability

### Three Interaction Modes
1. **Collaboration**: Times trabalham juntos em objetivo comum (alto bandwidth, temporário)
2. **X-as-a-Service**: Um time consome serviço de outro (baixo coupling, self-service)
3. **Facilitating**: Um time ajuda outro a aprender/crescer (enabling → stream-aligned)

### Cognitive Load
- Cada time tem capacidade cognitiva limitada
- Três tipos:
  - **Intrinsic**: Complexidade fundamental do domínio
  - **Extraneous**: Complexidade desnecessária (ferramentas ruins, processos burocráticos)
  - **Germane**: Complexidade de criar valor (design, problem-solving)
- Objetivo: minimizar extraneous load para maximizar germane load
- Se o time tem muitas responsabilidades, cognitive load impede fast flow

### Team-First Approach
- O time é a unidade fundamental de delivery (não o indivíduo)
- Tamanho ideal: 5-9 pessoas (Dunbar's number scaling)
- Time deve ter ownership claro e estável (não realocar constantemente)
- "Team API": Como o time se comunica com o exterior (interfaces, canais, docs)

### Fracture Planes (Onde Dividir)
- Business domain bounded context
- Regulatory compliance
- Change cadence (partes que mudam em velocidades diferentes)
- Team location (colocação física ou timezone)
- Technology (quando tech requer especialização distinta)
- User personas (quando personas diferentes têm necessidades muito distintas)
- Risk (separar componentes de alto risco)

## Frameworks e Modelos

### Team Topology Assessment
1. O time é stream-aligned, enabling, complicated-subsystem ou platform?
2. O tipo de time está correto para seu propósito?
3. As interações são collaboration, X-as-a-Service ou facilitating?
4. O cognitive load é gerenciável? (sintoma: time sobrecarregado, slow delivery)
5. A topology atual produz a arquitetura desejada? (Conway's Law check)

### Team API Template
```
Team: [Nome]
Type: [Stream-Aligned | Enabling | Complicated-Subsystem | Platform]
Mission: [1 frase]
Owns: [Serviços/domínios sob ownership]
Interfaces: [APIs, canais de comunicação, docs]
Interaction Mode with [Team X]: [Collaboration | X-as-a-Service | Facilitating]
```

## Aplicação ao C-Level Squad

### Para o CEO Agent
- Reconhecer que estrutura de times É decisão de arquitetura e velocidade
- Usar Team Topologies como linguagem comum para discussões de org design
- Inverse Conway: se a arquitetura desejada não combina com os times, mude os times

### Para o CTO Agent
- Estruturar engineering como stream-aligned teams com platform e enabling support
- Usar cognitive load como critério para definir scope de cada time
- Platform team como investimento em developer experience e velocidade
- Fracture planes para decidir onde dividir monólito em serviços

### Para o CFO Agent
- Stream-aligned teams reduzem handoffs = menor custo de coordenação
- Platform team como investimento compartilhado que reduz custo marginal de novos times
- Cognitive load excessivo = menor produtividade = maior custo efetivo por feature

### Para o CMO Agent
- Stream-aligned teams focados em valor para o cliente = faster time-to-market
- Marketing pode ter seu próprio stream-aligned team para marketing tech/experimentation
- Menos dependências = go-to-market mais ágil

### Para o COO Agent
- Operational responsibilities dentro dos stream-aligned teams (you build it, you run it)
- Platform team como centralizador de operational capabilities (monitoring, deploy)
- Interação X-as-a-Service minimiza coordinação operacional

## Takeaways Acionáveis (top 5)

1. **Organize por stream de valor** — A maioria dos times deve ser stream-aligned. Se os
   times estão organizados por camada técnica (frontend team, backend team), reorganize.

2. **Manage cognitive load** — Se um time reclama de sobrecarga, não é fraqueza — é sinal
   de que o scope está errado. Reduza responsabilidades ou crie platform/enabling teams.

3. **Use Inverse Conway** — Se quer loosely coupled architecture, organize times loosely
   coupled. A estrutura de comunicação determinará a arquitetura do sistema.

4. **Platform as a product** — Platform team deve tratar devs internos como clientes.
   Self-service, boa documentação, developer experience como prioridade.

5. **Define interaction modes** — Para cada par de times, defina: collaboration (temporário),
   X-as-a-Service (ongoing, low-touch) ou facilitating (transfer de conhecimento).

## Citações-Chave

> "Organizations should be designed as a system of interacting teams, not a hierarchy
> of individuals."

> "The goal is to minimize the cognitive load on each team and maximize their
> ability to deliver value quickly."

> "If you want to achieve a specific software architecture, you need to design
> your team interactions to match."

> "A platform exists to accelerate and simplify software delivery for
> stream-aligned teams."

> "Team-first thinking is the key to modern software delivery."

## Quando Consultar

- Ao (re)organizar equipes de engineering
- Quando delivery está lento por dependências entre times
- Na definição de platform team scope e roadmap
- Ao decidir como dividir monólito (fracture planes)
- Quando cognitive load é alto e times estão sobrecarregados
- Para alinhar org design com architecture decisions (Conway)

## Referências Cruzadas

- **Newman — Building Microservices**: Service boundaries alinhadas com team boundaries
- **Forsgren — Accelerate**: Loosely coupled teams como capability de performance
- **Martin — Clean Architecture**: Boundaries dentro do código alinhadas com team boundaries
- **Spotify Engineering Culture**: Squads, tribes e chapters como implementação prática
- **Goldratt — The Goal**: Otimizar flow do sistema, não das partes
- **Grove — High Output Management**: Dual reporting como precursor de team interactions
