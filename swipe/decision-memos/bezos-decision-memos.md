# Bezos Decision-Making — Day 1, Type 1/2, Disagree and Commit

> Os frameworks de decisão de Jeff Bezos que moldaram a Amazon.
> Análise profunda com exemplos e aplicação para C-Level.

---

## Contexto

Jeff Bezos construiu um dos sistemas de decisão mais estudados da história empresarial.
Não se trata de um único framework, mas de um sistema interligado de princípios que,
juntos, permitem escala de decisão sem perda de qualidade. Este documento analisa cada
componente, com exemplos reais e orientação para aplicação no contexto C-Level.

---

## Framework 1: Day 1 vs. Day 2

### O Conceito

Na carta aos acionistas de 2016, Bezos definiu:

> "Day 2 is stasis. Followed by irrelevance. Followed by excruciating, painful decline.
> Followed by death. And that is why it is always Day 1."

Day 1 não é uma fase temporal — é um mindset operacional. Uma empresa pode ter 30 anos
e estar no Day 1 se mantiver certas disciplinas. Uma startup pode estar no Day 2 se
perder velocidade de decisão.

### Características de Day 1

**Obsessão pelo cliente (não pelo concorrente):**
- Decisões começam com "o que o cliente precisa?" não "o que o concorrente fez?"
- Customer feedback loops são medidos em horas/dias, não semanas/meses
- Métricas de satisfação são input metrics, não vanity metrics

**Resistência a proxies:**
Proxies são quando o processo substitui o resultado. Exemplos perigosos:
- "Seguimos o processo" como justificativa para resultado ruim
- Survey scores como substituto para real customer understanding
- Compliance com framework como substituto para pensamento crítico

**Adoção agressiva de tendências externas:**
Day 1 significa abraçar tendências antes que sejam óbvias. Bezos investiu em:
- Cloud computing (AWS, 2006) quando ninguém entendia
- Voice interfaces (Alexa, 2014) antes do mercado estar pronto
- AI/ML em escala (2015+) antes de ser mainstream

**Alta velocidade de decisão:**
"Most decisions should probably be made with somewhere around 70% of the information
you wish you had. If you wait for 90%, in most cases, you're probably being slow."

### Sinais de Day 2

Indicadores de que uma organização entrou em Day 2:
- Decisões levam semanas onde antes levavam dias
- Processos são adicionados mas nunca removidos
- "Sempre fizemos assim" é aceite como argumento
- Reports sobre reports — layers de aprovação sem valor
- Customer complaints são geridos, não eliminados
- Inovação vem de aquisições, não de desenvolvimento interno

### Aplicação para C-Level
- Audite regularmente a velocidade de decisão da organização
- Identifique proxies que substituíram resultados reais
- Mantenha um "Day 2 radar" — sinais precoces de burocratização
- Pergunte em cada review: "estamos no Day 1 nesta área?"

---

## Framework 2: Type 1 vs. Type 2 Decisions

### O Conceito

Bezos classificou decisões em dois tipos fundamentais:

**Type 1 — Decisões irreversíveis (one-way doors):**
- Consequências difíceis ou impossíveis de reverter
- Exemplos: vender uma divisão, entrar num mercado regulado, fazer um M&A
- Devem ser tomadas com cuidado, deliberação e consulta ampla
- É adequado investir tempo significativo na análise

**Type 2 — Decisões reversíveis (two-way doors):**
- Podem ser revertidas com custo aceitável
- Exemplos: testar um feature, mudar pricing num segmento, experimentar um processo
- Devem ser tomadas rapidamente, por indivíduos ou pequenos grupos
- O custo de decidir devagar supera o custo de decidir errado

### O Problema Organizacional

À medida que empresas crescem, tendem a tratar TODAS as decisões como Type 1:
- Múltiplas camadas de aprovação para decisões triviais
- Análises de 30 páginas para experimentos de 2 semanas
- Comitês de 10 pessoas para decisões que uma pessoa poderia tomar
- Resultado: paralisia decisória que mata velocidade e inovação

### Como Classificar Decisões

Perguntas para determinar o tipo:

| Pergunta | Type 1 | Type 2 |
|---|---|---|
| Se der errado, podemos reverter? | Difícil/Impossível | Sim, com custo aceitável |
| Quanto tempo temos para decidir? | Meses (mas com urgência) | Dias a semanas |
| Quem precisa estar envolvido? | C-Level + Board | Team lead + 1-2 pessoas |
| Que nível de dados precisamos? | 80-90% | 60-70% |
| Qual o custo de atrasar? | Baixo (se dentro do window) | Alto (oportunidade perdida) |

### Exemplos Reais da Amazon

**Type 1 — Decisão de criar AWS:**
- Investimento massivo em infraestrutura
- Mudança fundamental no modelo de negócio
- Risco reputacional se falhasse
- Processo: meses de análise, memos detalhados, aprovação de Bezos

**Type 2 — Amazon Prime free shipping threshold:**
- Testar se $25 ou $35 era o threshold ideal
- Reversível em dias se não funcionasse
- Processo: team decision, implementação rápida, medição de resultados

**Type 2 que foi tratada como Type 1 (anti-pattern):**
- Mudar a cor de um botão no site levou 3 semanas de aprovações
- Resultado: frustração do time, oportunidade perdida
- Fix: delegation de decisões de UI/UX para product teams autónomos

### Aplicação para C-Level

**Crie uma "decision classification" explícita:**
- Publique critérios claros para Type 1 vs. Type 2
- Defina quem decide o quê — decision rights matrix
- Audite mensalmente: estamos tratando Type 2 como Type 1?

**Meça a velocidade de decisão:**
- Tempo médio de decisão por tipo
- Número de decisões por mês por nível
- Backlog de decisões pendentes

---

## Framework 3: Disagree and Commit

### O Conceito

"I disagree and commit all the time. We recently greenlit a particular Amazon Studios
original. I told the team my view: debatable whether it would be interesting enough,
complicated to produce, the business terms aren't that good, and we have lots of other
opportunities. They had a completely different opinion and wanted to go ahead. I wrote
back right away with 'I disagree and commit and hope it becomes the most watched thing
we've ever made.'"

### Por Que Este Framework é Revolucionário

**Resolve o paradoxo hierarquia vs. velocidade:**
Em organizações tradicionais, quando o líder discorda, ou:
a) O líder veta (mata ownership do time), ou
b) O time recua (perde-se a ideia), ou
c) Debate interminável (perde-se velocidade)

"Disagree and commit" oferece uma 4ª opção: o líder expressa desacordo, registra-o,
e depois compromete-se genuinamente com a decisão do time. Não é compliance passiva —
é commitment ativo apesar do desacordo.

### Condições para Funcionar

**Confiança mútua é pré-requisito:**
O líder confia que o time tem informação e julgamento válidos.
O time confia que o líder vai realmente apoiar a decisão.

**O desacordo deve ser articulado:**
Não basta dizer "concordo". É preciso dizer "discordo porque X, Y, Z — mas confio
no vosso julgamento e vou apoiar esta decisão com tudo o que tenho."

**Reversibilidade deve estar acordada:**
"Vamos em frente, mas se até [data] não virmos [métrica], reavaliamos."

**Não funciona para decisões éticas ou de valores:**
Se a discordância envolve princípios éticos ou valores fundamentais, "disagree and
commit" não é apropriado. Nesses casos, a discordância deve ser escalada.

### Anti-Patterns

**"Disagree and sabotage":**
Concordar na reunião e depois minar a execução. Destrutivo e comum.

**"Disagree and comply":**
Fazer o mínimo sem entusiasmo. Diferente de commit, que é apoio ativo.

**"Agree and resent":**
Não expressar discordância e guardar ressentimento. Corrói confiança.

**Usar como ferramenta de poder:**
"Eu discordo mas commit" dito pelo CEO cria pressão — o time interpreta como veto
velado. O tom e o follow-up precisam ser genuínos.

### Aplicação para C-Level
- Modele o comportamento: use explicitamente "disagree and commit"
- Crie safety para que outros também possam usá-lo
- Documente as decisões onde houve disagree and commit
- Faça retrospectivas: quem tinha razão? O que aprendemos?

---

## Framework 4: Working Backwards (PR/FAQ)

### O Conceito

Antes de construir qualquer produto, escreva o press release de lançamento e o FAQ.
Se o press release não é excitante, o produto não vale a pena.

### Estrutura do PR/FAQ

**Press Release (1 página):**
- Headline: o que o cliente vai ver
- Subheadline: quem é o cliente e que benefício recebe
- Problema: que dor estamos a resolver
- Solução: como resolvemos de forma simples
- Quote do líder: por que isto importa
- Call to action: como o cliente começa

**FAQ Interno (2-5 páginas):**
- Perguntas que stakeholders internos farão
- Respostas com dados e lógica
- Riscos e mitigações
- Timeline e recursos necessários

**FAQ Externo (1-2 páginas):**
- Perguntas que clientes farão
- Respostas focadas em benefício, não em feature

### Aplicação para C-Level
- Use PR/FAQ para avaliar iniciativas estratégicas
- Se o press release não anima, repense a iniciativa
- Force product teams a começar por aqui antes de roadmaps

---

## Sistema Integrado de Decisão

Os 4 frameworks funcionam juntos:

```
1. Day 1 mindset → mantém urgência e foco no cliente
2. Type 1/2 classification → calibra profundidade de análise
3. Disagree and commit → desbloqueia decisões sem unanimidade
4. Working Backwards → garante que o resultado importa para o cliente
```

### Fluxo Decisório Recomendado

```
Nova decisão surge
    ↓
É Day 1 ou Day 2 thinking? (Verificar mindset)
    ↓
Type 1 ou Type 2? (Classificar reversibilidade)
    ↓
Se Type 2: decide rápido, team-level
Se Type 1: análise profunda (memo/PR-FAQ)
    ↓
Há consenso? → Executa
Não há consenso? → Disagree and commit com critérios de revisão
    ↓
Retrospectiva em [data definida]
```

---

## Referências

- Jeff Bezos: Shareholder Letters 1997-2023 (todas disponíveis publicamente)
- Colin Bryar & Bill Carr: "Working Backwards" (2021)
- Brad Stone: "The Everything Store" (2013) e "Amazon Unbound" (2021)
- Jeff Bezos: "Invent and Wander" — collected writings (2020)
- John Rossman: "The Amazon Way" (2016)

---

*Última atualização: Março 2026*
*Categoria: Decision Memos | Nível: C-Level | Formato: Framework Analysis*
