# Glossário — Linguagem Comum do C-Level Squad

> Definições de 50+ termos utilizados no C-Level Squad OS. Português para descrições, inglês para termos técnicos.

---

## Objetivo

Garantir que todos os membros do squad utilizam os mesmos termos com os mesmos
significados. Ambiguidade terminológica é fonte frequente de desalinhamento.

---

## A

### Action Item
Tarefa específica atribuída a um owner com prazo definido, resultante de uma
reunião ou decisão. Deve ser concreta, mensurável e ter deadline.

### Agent
No contexto do C-Level Squad, um agente de AI que desempenha uma função
executiva específica. Existem 6 agentes no squad.

### Alignment
Estado em que todos os agentes e squads trabalham na mesma direcção com
entendimento comum dos objectivos e prioridades.

### Anti-Pattern
Prática ou comportamento que parece útil mas que prejudica a eficácia.
O oposto de best practice. Documentados em `docs/anti-patterns-guide.md`.

---

## B

### Baseline
Ponto de referência estabelecido num momento específico contra o qual se medem
mudanças futuras. Exemplo: roadmap baseline para diff trimestral.

### Bias (Viés)
Tendência sistemática que distorce julgamento ou decisão. Pode ser cognitivo
(humano) ou estatístico (dados/modelos).

### Blocker (Bloqueio)
Impedimento que impede o progresso de uma tarefa ou iniciativa. Requer
resolução para avançar. Pode ser interno ou dependência externa.

### Board Pack
Pacote de documentos preparado para reunião de conselho de administração.
Construído via `scripts/generation/board-prep-builder.md`.

### BLUF (Bottom Line Up Front)
Técnica de comunicação que coloca a conclusão ou pedido principal no início
da mensagem, seguido pelo contexto e detalhes.

### Burn Rate
Taxa a que uma organização gasta dinheiro. Usado para calcular runway
(tempo até ficar sem capital).

---

## C

### Cadência
Ritmo operacional regular do squad: diário, semanal, mensal, trimestral.
Cada cadência tem rituais e outputs definidos.

### Calibration
Processo de ajustar estimativas e previsões baseado em resultados reais.
Melhora precisão ao longo do tempo.

### CAC (Customer Acquisition Cost)
Custo total para adquirir um novo cliente. Inclui marketing, vendas e
outros custos de aquisição.

### CAIO (Chief AI Officer)
Agente responsável pela estratégia e governance de AI no squad.

### Churn Rate
Percentagem de clientes que deixam de usar o produto/serviço num período.
Oposto de retention rate.

### Cross-Squad
Actividade, dependência ou interacção que envolve mais de um squad ou agente.

---

## D

### Dashboard
Visualização consolidada de métricas e KPIs. Pode ser estático (report) ou
dinâmico (tempo real).

### Decision Log
Registo centralizado de todas as decisões significativas tomadas pelo squad.
Inclui contexto, alternativas, rationale e outcome.

### Decision Gate
Ponto num workflow onde se avalia se os critérios para avançar estão cumpridos.
Se sim, avança; se não, volta ou pára.

### Diff
Comparação entre dois estados (planeado vs real, versão A vs versão B).
Destaca adições, remoções e alterações.

### DoD (Definition of Done)
Conjunto de critérios que devem ser cumpridos para considerar uma entrega
como completa. Parte dos contratos cross-squad.

### DoR (Definition of Ready)
Conjunto de critérios que devem ser cumpridos antes de aceitar um pedido
para execução. Porta de entrada do trabalho.

---

## E

### Escalation (Escalação)
Processo de passar um problema ou decisão a um nível superior quando o
nível actual não consegue resolver dentro do prazo.

### Eval (Evaluation)
Avaliação estruturada de uma ferramenta, processo ou sistema. No contexto de
AI, avaliação de modelos e ferramentas.

---

## F

### Forecast
Previsão quantitativa ou qualitativa sobre um valor ou evento futuro.
Precisão de forecasts é monitorizada pelo forecast accuracy tracker.

### Framework
Estrutura conceptual que orienta análise, decisão ou execução. O squad
disponibiliza múltiplos frameworks para diferentes contextos.

---

## G

### Gold Standard
Nível de qualidade que o squad exige em todos os outputs. Definido em
`docs/gold-standard-and-sota.md`.

### Governance
Conjunto de regras, processos e práticas que asseguram que a organização
opera de forma responsável, transparente e accountable.

---

## H

### Handoff
Transferência formal de responsabilidade e informação entre squads ou
agentes. Segue protocolo definido nos contratos cross-squad.

### Health Score
Pontuação composta que indica o estado de saúde de uma iniciativa.
Calculado a partir de múltiplas dimensões (schedule, scope, resource, quality).

### HiPPO
Highest Paid Person's Opinion. Anti-pattern onde a opinião do mais sénior
domina independentemente dos dados.

---

## I

### Initiative
Projecto ou programa estratégico com objectivos, timeline e recursos definidos.
Monitorizado pelo initiative health tracker.

### Input
Dado ou informação necessária para iniciar um processo ou tomar uma decisão.

---

## K

### KPI (Key Performance Indicator)
Métrica-chave que indica performance em relação a um objectivo. Cada agente
tem KPIs específicos do seu domínio.

---

## L

### LTV (Lifetime Value)
Valor total que um cliente gera ao longo da relação com a organização.
Rácio LTV/CAC indica sustentabilidade do modelo de aquisição.

---

## M

### MBR (Monthly Business Review)
Revisão mensal de performance com análise de tendências e ajustes de plano.
Mais profunda que WBR, menos que QBR.

### Metrics Pack
Pacote consolidado de métricas formatado para consumo executivo. Construído
via `scripts/generation/metrics-pack-builder.md`.

### MTTR (Mean Time To Recovery)
Tempo médio para recuperar de um incidente. Métrica-chave de resiliência
operacional.

---

## N

### NPS (Net Promoter Score)
Métrica de satisfação e lealdade do cliente. Calculada como % promoters
menos % detractors. Escala de -100 a +100.

---

## O

### OKR (Objectives and Key Results)
Framework de definição de objectivos. Objective = direcção qualitativa.
Key Results = métricas quantitativas que indicam progresso.

### Operating System (OS)
No contexto deste squad, o conjunto de processos, cadências, frameworks e
ferramentas que coordenam a operação executiva.

### Output
Resultado produzido por um processo, workflow ou agente. Pode ser documento,
decisão, comunicação ou acção.

### Owner
Pessoa ou agente responsável por algo (decisão, tarefa, processo, risco).
Accountability é individual, mesmo quando execução é colaborativa.

---

## P

### Post-Mortem
Análise retrospectiva de um incidente ou falha. Sempre blameless — foca em
sistema e processo, não em culpa individual.

### Pre-Read
Material de preparação enviado antes de uma reunião. Leitura obrigatória
para participação informada.

### Pre-Mortem
Exercício de antecipar o que pode correr mal antes de implementar uma
decisão. Identifica riscos proactivamente.

---

## Q

### QBR (Quarterly Business Review)
Revisão trimestral abrangente de performance, estratégia e planeamento.
A cadência mais profunda e consequente.

### Quality Gate
Ponto de verificação de qualidade antes de avançar num workflow ou entregar
um output. Previne que trabalho insuficiente prossiga.

---

## R

### RAPID
Framework de decisão: Recommend, Agree, Perform, Input, Decide.
Define papéis claros no processo decisório.

### Risk Register
Registo centralizado de riscos identificados com classificação, owner
e planos de mitigação.

### Roadmap
Plano de alto nível que mostra iniciativas, milestones e timeline.
Comparado com execução real via roadmap diff.

### Runway
Tempo que a organização pode operar com os recursos actuais antes de
ficar sem capital. Calculado a partir de cash e burn rate.

---

## S

### SLA (Service Level Agreement)
Acordo formal que define expectativas de performance entre provider e
consumer de um serviço. Parte dos contratos cross-squad.

### SOTA (State of the Art)
O melhor que existe actualmente numa área. Benchmark externo que informa
o gold standard interno.

### Squad
Equipa ou unidade funcional dentro da organização. No C-Level Squad, cada
agente pode ser visto como um squad individual ou como parte do squad C-Level.

### Stakeholder
Qualquer pessoa ou grupo com interesse nos resultados da organização.
Segmentados por tier para comunicação.

---

## T

### Threshold
Limite ou limiar que, quando ultrapassado, dispara uma acção (alerta,
escalação, mudança de status).

### Type 1/Type 2 Decision
Classificação de decisões: Type 1 = irreversível (one-way door), Type 2 =
reversível (two-way door). O tipo determina o nível de deliberação.

---

## V

### Velocity
Medida de ritmo de trabalho de uma equipa. Usada para planeamento e
previsão de capacidade.

---

## W

### WBR (Weekly Business Review)
Revisão semanal de performance operacional. Principal cadência de gestão
corrente do squad. Inspirada no modelo Amazon.

### Workflow
Processo estruturado com passos, inputs, outputs e quality gates. A forma
como o squad executa trabalho de forma consistente.

---

## Notas Técnicas

- Este glossário é mantido actualizado pelo COO Orchestrator
- Novos termos adicionados quando surgem em documentação
- Termos obsoletos são marcados como deprecated antes de remoção
- Mínimo de 50 termos mantidos no glossário
- Contribuições de termos seguem `docs/contribution-guide.md`
