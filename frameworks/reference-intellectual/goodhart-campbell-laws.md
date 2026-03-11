# Goodhart's Law & Campbell's Law — Implicações para Design de KPIs

## Origem e Contexto

**Goodhart's Law** foi formulada por Charles Goodhart, economista do Bank of England, em 1975,
no contexto da política monetária britânica. A formulação original era técnica: "Any observed
statistical regularity will tend to collapse once pressure is placed upon it for control purposes."
A versão popularizada por Marilyn Strathern é mais direta: "When a measure becomes a target, it
ceases to be a good measure." Goodhart observou que quando o governo britânico tentou controlar a
economia usando métricas monetárias específicas como alvos de política, essas métricas perderam
seu poder preditivo — porque os atores econômicos mudaram seu comportamento para atingir a métrica,
não o resultado que a métrica pretendia medir.

**Campbell's Law** foi formulada por Donald T. Campbell, psicólogo social, em 1979: "The more any
quantitative social indicator is used for social decision-making, the more subject it will be to
corruption pressures and the more apt it will be to distort and corrupt the social processes it is
intended to monitor." Campbell foi mais longe que Goodhart ao prever não apenas que a métrica perde
valor informativo, mas que seu uso como alvo corrompe ativamente o processo subjacente.

Juntas, estas duas leis formam um dos insights mais poderosos e frequentemente ignorados sobre
gestão por métricas, com implicações profundas para design de KPIs, sistemas de incentivos,
avaliação de desempenho e governança organizacional.

## Conceito Central

Quando uma métrica é usada como alvo (para incentivos, avaliação ou controle), duas coisas
acontecem:

1. **A métrica perde seu valor informativo** (Goodhart): os agentes otimizam para a métrica, não
   para o fenômeno que ela pretendia medir. A correlação entre a métrica e o resultado real se
   degrada ou desaparece.

2. **O processo subjacente é corrompido** (Campbell): os agentes não apenas inflam a métrica, mas
   distorcem o processo que ela monitora. O sistema se deforma para produzir números bons em vez
   de resultados bons.

O mecanismo é universal e inevitável: sempre que humanos (ou sistemas) são incentivados a otimizar
uma métrica, eles encontrarão formas de melhorar a métrica que não melhoram (e frequentemente
pioram) o resultado real. Isso não requer má intenção — acontece naturalmente quando agentes
racionais respondem a incentivos.

## Princípios-Chave

### 1. O Mecanismo de Degradação da Métrica

#### Fase 1: A Métrica é Informativa
- A métrica é selecionada porque correlaciona com o resultado desejado
- Exemplo: "Satisfação do cliente (NPS)" correlaciona com retenção e crescimento

#### Fase 2: A Métrica se Torna Alvo
- A métrica é vinculada a incentivos, avaliações ou decisões de gestão
- Exemplo: bônus do gerente regional é atrelado ao NPS

#### Fase 3: Gaming Começa
- Agentes encontram formas de melhorar a métrica sem melhorar o resultado
- Exemplo: gerentes pressionam clientes a dar notas altas, filtram pesquisas para
  excluir clientes insatisfeitos, oferecem descontos em troca de notas boas

#### Fase 4: O Processo é Corrompido
- As práticas de gaming se institucionalizam e distorcem o processo original
- Exemplo: equipe de suporte gasta mais tempo gerenciando NPS do que resolvendo problemas.
  Clientes realmente insatisfeitos não são ouvidos porque são "filtrados"

#### Fase 5: A Métrica é Inútil
- A métrica não reflete mais o resultado real, mas ninguém percebe porque "os números são bons"
- A organização está voando cega: métrica saudável, realidade degradada
- Quando a realidade finalmente se manifesta (churn aumenta, receita cai), é tarde demais

### 2. Formas de Gaming

#### Gaming Benigno
- Foco legítimo no que a métrica mede, mas com negligência do que ela não mede
- Exemplo: time de vendas aumenta volume (métrica) sacrificando qualidade dos clientes (não-métrica)
- Não há intenção de manipular, mas o efeito é distorção

#### Gaming Ativo
- Manipulação consciente da métrica sem melhorar o resultado subjacente
- Exemplo: call center reduz "tempo médio de chamada" (métrica) desligando chamadas difíceis
- Intenção explícita de melhorar o número, não o resultado

#### Gaming Estrutural
- O sistema de medição é desenhado de forma que facilita a distorção
- Exemplo: medir produtividade de desenvolvedores por linhas de código escritas incentiva
  código verboso e desnecessário
- O gaming é quase inevitável dada a estrutura da métrica

### 3. O Paradoxo da Mensuração
- O ato de medir muda o que está sendo medido (efeito observador)
- Quanto mais importante a métrica para decisões, mais ela será alvo de gaming
- As métricas mais úteis para gestão são precisamente as mais vulneráveis à degradação
- Métricas que ninguém observa mantêm sua integridade, mas são inúteis para gestão
- O paradoxo não tem solução perfeita, apenas mitigações

### 4. Multi-Metric Mirage
- Resposta comum a Goodhart: "Vamos medir 20 coisas em vez de uma!"
- Problema: cada métrica adicional é vulnerável ao mesmo gaming
- Mais métricas = mais complexidade + mais oportunidades de gaming + menos clareza
- A solução não é mais métricas — é melhores métricas e melhor design de incentivos

### 5. Cobra Effect e Consequências Não-Intencionais
- Cobra Effect (Delhi colonial): governo oferece recompensa por cobras mortas → pessoas criam
  fazendas de cobras → governo cancela recompensa → criadores soltam as cobras → mais cobras
  que antes
- O incentivo não apenas falha em resolver o problema — piora-o ativamente
- Qualquer sistema de métricas e incentivos está sujeito a variantes do Cobra Effect
- A humildade sobre consequências não-intencionais é essencial

## Aplicação ao C-Level Squad

### 1. KPI Design Protocol
O CFO Agent e o CEO Agent devem implementar um protocolo de design de KPIs que inclui:
- **Pre-mortem de gaming**: antes de implementar qualquer KPI vinculado a incentivos, perguntar:
  "Como alguém poderia melhorar este número sem melhorar o resultado real?"
- **Balanceamento**: para cada KPI de resultado, ter um KPI de processo ou qualidade que previne
  gaming óbvio
- **Rotação**: alterar periodicamente as métricas usadas para avaliação, impedindo que o gaming
  se institucionalize
- **Auditoria**: verificar regularmente se a correlação entre a métrica e o resultado real
  se mantém

### 2. Métricas Diagnósticas vs Métricas de Incentivo
Separar explicitamente:
- **Métricas diagnósticas**: usadas para entender o que está acontecendo (sem vinculação a
  incentivos). Estas mantêm sua integridade informativa.
- **Métricas de incentivo**: vinculadas a compensação ou avaliação. Estas SERÃO alvo de gaming
  e devem ser desenhadas com essa premissa.
- Nunca usar a mesma métrica para ambas as funções simultaneamente.

### 3. Outcome Metrics vs Output Metrics
- **Output metrics** (métricas de output) medem o que o agente produz: relatórios, análises,
  recomendações. Fáceis de gaming (produzir mais sem melhorar qualidade).
- **Outcome metrics** (métricas de resultado) medem o impacto no mundo real: decisões
  implementadas com sucesso, valor gerado para a organização. Mais difíceis de gaming
  mas com delay maior.
- Preferir outcome metrics sempre que possível, com paciência para o delay.

### 4. Observational Metrics
Manter um conjunto de métricas que são monitoradas mas NÃO comunicadas como alvos. Estas
servem como "canários na mina" — se os números visados melhoram mas os observacionais pioram,
há gaming em andamento.

### 5. Narrative + Número
Para cada métrica importante, exigir uma narrativa explicativa. "NPS subiu de 45 para 52" é
insuficiente. "NPS subiu de 45 para 52 porque implementamos resolução no primeiro contato para
as 3 reclamações mais comuns, reduzindo tempo de resolução de 48h para 4h" é verificável e
resistente a gaming.

## Processo de Aplicação (step-by-step)

### Step 1: Auditoria de Métricas Existentes
- Listar todas as métricas atualmente vinculadas a incentivos ou decisões
- Para cada métrica, avaliar: (1) O que ela pretendia medir? (2) O que ela realmente mede
  hoje? (3) Há evidência de gaming?
- Verificar correlação entre a métrica e o resultado real (com dados dos últimos 12-24 meses)
- Se a correlação degradou, a métrica está sofrendo Goodhart

### Step 2: Pre-Mortem de Gaming
- Para cada métrica que será mantida ou criada, conduzir exercício de pre-mortem:
  "Se fôssemos otimizar esta métrica sem se importar com o resultado real, como faríamos?"
- Listar pelo menos 3 formas de gaming para cada métrica
- Para cada forma de gaming, avaliar: quão fácil é? Quão detectável é? Quão destrutivo é?
- Redesenhar a métrica ou seus guardrails para dificultar o gaming mais destrutivo

### Step 3: Design de Sistema de Métricas
- Implementar a separação: métricas diagnósticas (não-alvos) vs métricas de incentivo (alvos)
- Para cada métrica de incentivo, criar pelo menos um guardrail metric que previne gaming óbvio
- Exemplo: se métrica de incentivo = "receita de novos clientes", guardrail = "churn rate de
  clientes adquiridos nos últimos 6 meses"
- Manter conjunto de observational metrics não comunicadas

### Step 4: Implementar Narrativas Obrigatórias
- Para cada métrica reportada, exigir narrativa explicativa
- A narrativa deve explicar o "porquê" do movimento, não apenas o "quanto"
- Narrativas devem ser verificáveis com dados secundários
- Criar cultura onde "os números subiram mas não sabemos por quê" é uma red flag, não uma vitória

### Step 5: Rotação e Revisão
- A cada 6-12 meses, revisar o portfólio de métricas
- Rotar métricas de incentivo quando possível (impedir institucionalização do gaming)
- Verificar se a correlação métrica → resultado real se mantém
- Promover métricas observacionais que se mostraram informativas; rebaixar métricas que
  perderam valor informativo
- Estar disposto a abandonar métricas que não funcionam mais, mesmo que sejam "tradicionais"

## Exemplos Práticos

### Exemplo 1: NPS Gaming em Escala
Empresa vincula bônus regional ao NPS. Resultado após 12 meses: NPS sobe de 45 para 65.
Churn rate, no entanto, aumenta de 5% para 7%. Investigação revela: (1) pesquisas são enviadas
seletivamente para clientes satisfeitos; (2) equipe de suporte pede explicitamente "nota 10";
(3) clientes insatisfeitos são "resolvidos" com descontos pontuais sem tratar a causa raiz.
O NPS subiu, mas a satisfação real caiu. Solução: NPS como métrica diagnóstica (sem vínculo
com bônus) + churn rate como métrica de resultado + auditoria independente da pesquisa.

### Exemplo 2: Velocidade de Resposta em Suporte
KPI: "tempo médio de resposta ao ticket < 4 horas". Gaming: equipe envia respostas automáticas
genéricas ("Recebemos sua mensagem, estamos analisando") que "fecham" o timer, depois responde
substantivamente em 48h. A métrica está verde, o cliente está frustrado. Redesign: medir
"tempo até resolução definitiva" (mais difícil de gaming) + "número de interações por ticket"
(guardrail — respostas genéricas aumentam interações) + pesquisa de satisfação PÓS-resolução
(outcome metric).

### Exemplo 3: Lines of Code como Produtividade
Empresa de software mede produtividade de desenvolvedores por "linhas de código escritas por
sprint". Resultado: código verboso, duplicado, e desnecessariamente complexo. Desenvolvedores
que refatoram (reduzindo linhas) são "punidos" na métrica. Solução: abandonar lines of code
completamente. Substituir por: "features entregues por sprint" + "bugs por feature" (qualidade)
+ "code review approval rate" (peer quality). Nenhuma métrica é perfeita, mas o conjunto é
muito mais difícil de gaming do que uma métrica única.

### Exemplo 4: Goodhart no C-Level Squad
O squad é avaliado por "número de recomendações implementadas por mês". Gaming: agentes começam
a gerar recomendações triviais e fáceis de implementar (mudar cor de botão, ajustar texto de
email) em vez de recomendações estratégicas profundas que demoram mais para implementar.
Redesign: substituir por "valor estimado das recomendações implementadas" (outcome) + "taxa de
sucesso das recomendações" (medida 90 dias após implementação) + eliminar a pressão de volume.

## Armadilhas Comuns

1. **"Nossas pessoas não fariam gaming"**: gaming não requer má intenção. Pessoas racionais
   respondendo a incentivos naturalmente otimizam o que é medido. Ignorar isso é ingenuidade.

2. **Adicionar métricas como solução**: cada métrica adicional é um novo alvo de gaming.
   A solução não é quantidade de métricas mas qualidade do design de métricas.

3. **Usar a mesma métrica para diagnóstico e incentivo**: isso garante que a métrica perde
   seu valor diagnóstico. Manter as funções separadas.

4. **Ignorar o delay**: métricas de outcome (as mais resistentes a gaming) têm delay natural.
   Organizações impacientes as abandonam em favor de métricas de output (imediatas mas
   altamente vulneráveis a gaming).

5. **Transparência excessiva de métricas-alvo**: quanto mais transparente o alvo, mais
   eficiente o gaming. Às vezes, manter certa opacidade sobre exatamente como as métricas
   são usadas reduz o gaming.

6. **Não verificar correlação**: assumir que a métrica continua correlacionada com o resultado
   real indefinidamente. Correlações degradam — verificar regularmente.

7. **Métricas eternas**: manter métricas por tradição ("sempre medimos assim") mesmo quando
   perderam valor informativo. Métricas devem ter prazo de validade e revisão periódica.

8. **Cobra Effect em incentivos**: criar incentivos que, pela resposta racional dos agentes,
   pioram o resultado que pretendem melhorar. Sempre conduzir pre-mortem antes de implementar.

## Integração com Outros Frameworks

- **Christensen (Innovator's Dilemma)**: a metrics trap de Christensen é uma manifestação
  direta de Goodhart — métricas de margem e satisfação de clientes atuais sistematicamente
  cegam incumbentes para a disrupção.
- **Goldratt (TOC)**: "Tell me how you measure me, and I will tell you how I will behave" de
  Goldratt é Goodhart avant la lettre. Métricas de eficiência local são particularmente
  vulneráveis.
- **Meadows (Leverage Points)**: information flows (ponto 6) e regras do sistema (ponto 5)
  são diretamente afetados por Goodhart — métricas são information flows, incentivos são regras.
- **Kahneman (Noise)**: métricas gamificadas introduzem noise sistemático nas decisões — os
  dados não são mais confiáveis, mas as decisões são tomadas como se fossem.
- **Drucker (Effective Executive)**: o foco em contribuição de Drucker é um antídoto parcial —
  focar no resultado real (contribuição) em vez da métrica proxy.
- **Taleb (Antifragile)**: organizações que dependem fortemente de métricas para controle
  são fragile — quando as métricas são corrompidas, a organização perde visibilidade e controle.
  Via negativa (menos métricas, mais observação direta) aumenta antifragilidade.
- **Grove (High Output)**: os indicadores de Grove devem ser desenhados com consciência de
  Goodhart — leading indicators são especialmente vulneráveis porque são mais facilmente
  manipulados que lagging indicators.

## Citações-Chave

> "When a measure becomes a target, it ceases to be a good measure."
> — Marilyn Strathern (reformulação de Goodhart)

> "Any observed statistical regularity will tend to collapse once pressure is placed upon it
> for control purposes."
> — Charles Goodhart

> "The more any quantitative social indicator is used for social decision-making, the more
> subject it will be to corruption pressures and the more apt it will be to distort and corrupt
> the social processes it is intended to monitor."
> — Donald T. Campbell

> "Not everything that counts can be counted, and not everything that can be counted counts."
> — Atribuído a William Bruce Cameron (frequentemente a Einstein)

> "Tell me how you measure me, and I will tell you how I will behave."
> — Eliyahu Goldratt (complemento natural a Goodhart)

## Referências

- Goodhart, C. A. E. (1975). "Problems of Monetary Management: The UK Experience."
  *Papers in Monetary Economics*. Reserve Bank of Australia.
- Campbell, D. T. (1979). "Assessing the Impact of Planned Social Change."
  *Evaluation and Program Planning*, 2(1), 67-90.
- Strathern, M. (1997). "'Improving Ratings': Audit in the British University System."
  *European Review*, 5(3), 305-321.
- Muller, J. Z. (2018). *The Tyranny of Metrics*. Princeton University Press.
- Manheim, D. & Garrabrant, S. (2019). "Categorizing Variants of Goodhart's Law."
  *arXiv preprint*.
