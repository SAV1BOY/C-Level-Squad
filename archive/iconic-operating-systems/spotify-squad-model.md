# Spotify Squad Model — Squads, Tribes e Chapters

> Análise do modelo organizacional do Spotify e lições para o C-Level Squad.

---

## Contexto Histórico

O Spotify popularizou um modelo organizacional baseado em "squads" autónomos,
agrupados em "tribes", com "chapters" e "guilds" como mecanismos transversais.
Apresentado por Henrik Kniberg e Anders Ivarsson em 2012 no whitepaper
"Scaling Agile @ Spotify", rapidamente tornou-se uma das referências mais
citadas em design organizacional.

---

## Estrutura do Modelo

### Squads
- Unidade básica de organização (equivalente a uma equipa pequena)
- 6-12 pessoas com competências multidisciplinares
- Autónomos: decidem o que construir, como construir e como trabalhar
- Cada squad tem uma missão clara de longo prazo
- Owner do produto ou área que lhes é atribuída
- Mini-startups dentro da organização

### Tribes
- Agrupamento de squads que trabalham em áreas relacionadas
- Máximo ~100 pessoas (Dunbar's number)
- Tribe lead coordena sem microgerir
- Squads dentro da mesma tribe partilham contexto e recursos
- Permite escala mantendo sensação de pequena equipa

### Chapters
- Grupo de pessoas com a mesma competência técnica (ex: backend developers)
- Transversal a squads dentro da mesma tribe
- Chapter lead é o people manager
- Garante desenvolvimento profissional e standards técnicos
- Resolve o problema "como crescer tecnicamente num squad pequeno"

### Guilds
- Comunidades de interesse transversais a toda a organização
- Voluntárias e orgânicas
- Partilha de conhecimento e boas práticas
- Qualquer pessoa pode juntar-se ou sair
- Exemplos: Web Guild, Testing Guild, Leadership Guild

---

## Princípios Operacionais

### Autonomia
Squads têm autonomia para:
- Decidir processos internos (scrum, kanban, whatever)
- Escolher ferramentas e tecnologias (dentro de guidelines)
- Definir prioridades (alinhadas com missão)
- Organizar o seu trabalho diário
- Experimentar e falhar (dentro de limites razoáveis)

### Alinhamento
Alinhamento é garantido por:
- **Product owner**: define o quê e porquê
- **Tribe lead**: alinha direcção entre squads
- **Company goals**: objectivos que todos conhecem
- **Dependency tracking**: sistema para gerir dependências inter-squad
- **Release trains**: coordenação para releases que envolvem múltiplos squads

### Confiança
O modelo assenta na confiança:
- Confiar que squads tomam boas decisões
- Confiar que pessoas são competentes e motivadas
- Erros são oportunidades de aprendizagem
- Microgestão é anti-pattern explícito
- Transparency como mecanismo de confiança

---

## Cerimónias e Cadências

### Dentro do Squad
- **Daily standup**: 15 min, sincronização diária
- **Sprint planning**: definição de trabalho (se usam sprints)
- **Retrospective**: melhoria contínua do processo
- **Demo/showcase**: mostrar trabalho concluído

### Ao Nível da Tribe
- **Town hall**: reunião trimestral de toda a tribe
- **Dependency meeting**: coordenação semanal entre squads
- **Tribe retrospective**: melhoria ao nível da tribe
- **Hackathons**: 10% do tempo para inovação e experimentação

### Transversal
- **Guild meetings**: encontros regulares das guilds
- **Chapter meetings**: desenvolvimento profissional
- **All-hands**: comunicação company-wide

---

## Lições para o C-Level Squad

### O Que Adoptar
1. **Squad como unidade**: cada agente opera como um squad autónomo
2. **Autonomia com alinhamento**: agentes decidem no seu domínio, alinhados
   pela visão e cadências comuns
3. **Chapters como mecanismo**: competências técnicas partilhadas entre agentes
   (ex: todos usam os mesmos frameworks de decisão)
4. **Guilds como conhecimento**: áreas de interesse transversal mantidas como
   knowledge bases partilhadas
5. **Cadências multi-nível**: daily, weekly, quarterly em diferentes níveis

### O Que Adaptar
1. **Tamanho**: C-Level Squad é um squad de 6, não uma organização de centenas
2. **Tribes**: não aplicável directamente, mas o conceito de agrupamento por
   área é útil (ex: strategy cluster, operations cluster)
3. **People management**: chapters como gestão de pessoas não se aplica a AI
4. **Voluntariedade**: guilds voluntárias não fazem sentido num squad de 6;
   todo o conhecimento é partilhado
5. **Ferramentas**: squads Spotify escolhem ferramentas; no C-Level Squad,
   há mais standardização por necessidade de coerência

### O Que Evitar
1. **Spotify model cargo cult**: copiar terminologia sem substância
2. **Autonomia sem alinhamento**: agentes autónomos sem coordenação é caos
3. **Dependency hell**: dependências não geridas são o ponto fraco do modelo
4. **Scaling prematuro**: modelo foi desenhado para escala; usar apenas o que
   é relevante para o tamanho actual
5. **Process anarchy**: autonomia não significa ausência de standards

---

## Evolução e Críticas

### O Que Mudou Desde 2012
- Spotify ajustou significativamente o modelo ao longo dos anos
- Chapters evoluíram para ter papel de people management mais forte
- Guilds tornaram-se menos orgânicas e mais estruturadas
- Dependency management tornou-se mais formal
- O próprio Spotify não usa o "Spotify Model" como descrito em 2012

### Críticas Comuns
- Modelo foi apresentado como aspiração, não como realidade
- Dependency management é o calcanhar de Aquiles
- Autonomia pode levar a duplicação e inconsistência
- Funciona melhor em tech companies product-led
- Chapter leads com dual role (people + technical) é difícil

---

## Referências

- "Scaling Agile @ Spotify" — Henrik Kniberg & Anders Ivarsson (2012)
- "Spotify's Failed Squad Goals" — Jeremiah Lee (2020)
- "Spotify Engineering Culture" — videos por Henrik Kniberg
- "Team Topologies" — Matthew Skelton & Manuel Pais (evolução do conceito)

---

## Notas Técnicas

- A designação "squad" no C-Level Squad é inspirada neste modelo
- Contratos cross-squad em `docs/cross-squad-contracts.md` abordam dependencies
- Autonomia dos agentes é definida em `agents/` e governance em `docs/`
- Cadências multi-nível definidas em `docs/operating-system.md`
