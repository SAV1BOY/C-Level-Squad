# Amazon Weekly Business Review (WBR) - Deep Dive

## Contexto

O Weekly Business Review (WBR) é o principal mecanismo operacional da Amazon.
Toda semana, líderes de cada negócio revisam métricas detalhadas em uma reunião
estruturada que força accountability, identifica problemas cedo e mantém
alinhamento entre execução e estratégia. É considerado o "sistema operacional"
da gestão Amazon.

## Estrutura do WBR

### Formato
- **Duração:** 60-90 minutos
- **Frequência:** Semanal (sem exceção)
- **Participantes:** Líder do negócio + reports diretos + convidados relevantes
- **Documento:** Deck de métricas padronizado (não narrativo - exceção ao 6-pager)
- **Preparação:** Dados atualizados até 24h antes da reunião

### O Deck de Métricas
O deck segue um formato rígido com seções padronizadas:

1. **Métricas de Output** (o que o cliente vê)
   - Exemplos: tempo de entrega, disponibilidade de produto, NPS

2. **Métricas de Input** (o que controlamos para afetar output)
   - Exemplos: inventory levels, seller onboarding, page load time

3. **Tendências** (WoW, MoM, YoY)
   - Cada métrica comparada com períodos anteriores e metas

4. **Andon Cord Items** (métricas fora do esperado)
   - Destaque visual para métricas que cruzaram thresholds
   - Requer explicação e plano de ação

5. **Deep Dives** (análise aprofundada de 1-2 tópicos)
   - Rodízio semanal de tópicos para deep dive
   - Análise de causa raiz, não apenas descrição do problema

## O Conceito de Métricas de Input vs Output

### Por Que Input Metrics São Centrais

A Amazon acredita que:
- **Output metrics** (receita, lucro, NPS) são consequências
- **Input metrics** (ações que a equipe controla) são causas
- Gerenciar inputs leva a melhores outputs
- Outputs são lagging indicators; inputs são leading indicators

### Exemplo Prático: Marketplace

| Output Metric | Input Metrics que Influenciam |
|---------------|-------------------------------|
| GMV (receita bruta) | # de sellers ativos, # de SKUs listados, % de buy box |
| Customer satisfaction | Tempo de entrega, taxa de defeito, resolução de disputas |
| Seller retention | Tempo para primeira venda, suporte ao seller, fees competitivos |

### Como Identificar Boas Input Metrics
1. **Controlável:** O time pode influenciar diretamente
2. **Preditiva:** Mudança na input leva a mudança na output (com lag conhecido)
3. **Acionável:** Se a métrica está ruim, sabemos o que fazer
4. **Mensurável:** Dados disponíveis semanalmente (no mínimo)

## O Sistema Andon Cord

### Origem
Inspirado no sistema Toyota de produção onde qualquer operário pode parar
a linha de produção ao puxar uma corda (andon cord) quando identifica um problema.

### No WBR
- Métricas com thresholds pré-definidos (verde/amarelo/vermelho)
- Qualquer métrica "vermelha" requer explicação imediata no WBR
- Não importa se o líder sabe a causa: o fato de estar vermelho requer atenção
- O objetivo não é punir, é resolver rapidamente

### Thresholds Típicos
- **Verde:** Dentro de 5% da meta
- **Amarelo:** 5-15% abaixo da meta
- **Vermelho:** >15% abaixo da meta ou deterioração por 3+ semanas consecutivas

## Deep Dives

### Formato
Cada WBR inclui 1-2 deep dives em tópicos rotativos:
- Preparado por um membro do time (não pelo líder)
- Formato narrativo (parágrafo, não bullets) de 2-4 páginas
- Inclui: contexto, dados, análise de causa raiz, plano de ação, timeline
- 15-20 minutos de leitura silenciosa + 20-30 minutos de discussão

### Critérios para Selecionar Deep Dives
1. Métrica persistentemente amarela/vermelha
2. Oportunidade significativa identificada nos dados
3. Decisão estratégica que requer dados para informar
4. Post-mortem de incidente ou falha

### O Que Torna um Deep Dive Bom
- Vai além da descrição do problema (5 Whys)
- Quantifica o impacto financeiro e/ou de cliente
- Propõe ações específicas com owners e deadlines
- Antecipa objeções e riscos do plano proposto

## Rituais e Comportamentos Esperados

### Preparação
- Dados devem estar no deck 24h antes
- Líder revisa o deck na véspera e anota perguntas
- Deep dives enviados 24h antes para leitura prévia

### Durante a Reunião
- Sem celulares ou laptops abertos (exceto para referência de dados)
- Leitura silenciosa dos deep dives antes de discutir
- Perguntas focadas em "por que" e "o que faremos", não "o que aconteceu"
- Decisões documentadas em tempo real com owner e deadline

### Após a Reunião
- Action items distribuídos em até 2 horas
- Follow-ups trackados no próximo WBR
- Deep dive summaries arquivados para referência

## Implementação Prática

### Semana 1-2: Definição de Métricas
- Identificar 15-25 métricas para o WBR
- Mix de input e output metrics
- Definir thresholds para cada métrica
- Garantir que dados são coletáveis semanalmente

### Semana 3-4: Construção do Deck Template
- Criar template padronizado (sempre o mesmo formato)
- Automatizar coleta de dados quando possível
- Definir quem atualiza cada seção
- Testar com dados de 2-3 semanas anteriores

### Semana 5-8: Primeiros WBRs
- Começar com foco em familiarização com o formato
- Ajustar métricas que não se provarem úteis
- Estabelecer cadência de deep dives
- Coletar feedback e iterar

### Semana 9+: Maturidade
- WBR se torna o ritual principal de gestão
- Decisões operacionais são tomadas ou escaladas no WBR
- Métricas evoluem com o negócio
- Novos membros aprendem o negócio pelo WBR

## Erros Comuns

### 1. Métricas Demais
- WBR com 100 métricas = nenhuma recebe atenção
- Recomendação: 15-25 métricas no deck principal
- Métricas adicionais disponíveis para drill-down, mas não no deck principal

### 2. Foco em Output Sem Input
- "Receita caiu 10%" sem entender quais inputs mudaram
- Sem input metrics, o WBR vira uma sessão de relato, não de gestão

### 3. Deep Dives Superficiais
- "Fizemos um deep dive e concluímos que precisamos melhorar" não é deep dive
- Exigir 5 Whys e plano de ação concreto com owner e deadline

### 4. WBR Como Tribunal
- Se o WBR vira "quem é culpado", as pessoas escondem problemas
- Cultura deve ser de curiosidade ("por que?"), não de culpa

### 5. Cancelar o WBR
- "Essa semana não tem nada importante" = não entendeu o propósito
- O WBR existe para pegar problemas cedo, não para discutir crises

## Adaptação por Tamanho de Empresa

### Startup (10-50 pessoas)
- WBR com CEO + todos os leads (30 min)
- 8-12 métricas essenciais
- Deep dive rotativo a cada 2 semanas
- Foco em velocidade de iteração

### Scale-up (50-500 pessoas)
- WBR por área funcional + WBR executivo
- 15-20 métricas por área
- Deep dive semanal
- Foco em consistência e previsibilidade

### Enterprise (500+ pessoas)
- WBR hierárquico (time → departamento → divisão → empresa)
- Métricas cascateiam de cima para baixo
- Deep dives especializados por nível
- Foco em accountability e cross-functional alignment

## Referências

- "Working Backwards" - Colin Bryar & Bill Carr (2021)
- "The Amazon Way" - John Rossman (2014)
- Amazon Shareholder Letters (Jeff Bezos, 1997-2020)
- "Measure What Matters" - John Doerr (complementar para OKRs)
- Internal Amazon docs (via ex-Amazonians em blogs e podcasts)
