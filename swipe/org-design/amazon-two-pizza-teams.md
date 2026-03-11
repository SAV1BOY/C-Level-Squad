# Análise Two Pizza Teams - Amazon

## Conceito Original

Jeff Bezos introduziu o conceito "Two Pizza Teams" nos primeiros anos da Amazon:
nenhum time deveria ser grande o bastante que duas pizzas não consigam alimentá-lo.
Na prática, isso significa times de 6-10 pessoas.

Mas o conceito vai muito além do tamanho. É um modelo organizacional completo que
combina autonomia, ownership e alinhamento com métricas.

## Princípios Fundamentais

### 1. Tamanho Limitado (6-10 pessoas)
- Comunicação cresce exponencialmente com tamanho do time (n*(n-1)/2 canais)
- 6 pessoas = 15 canais de comunicação
- 12 pessoas = 66 canais de comunicação
- Times pequenos tomam decisões mais rápido e com menos burocracia

### 2. Single-Threaded Leadership
- Cada time tem um líder focado 100% naquela missão
- O líder não divide atenção entre múltiplos projetos
- "Single-threaded" significa que o sucesso do líder = sucesso do time

**Por que funciona:** Líderes multi-threaded otimizam para o portfólio,
não para o resultado. Um líder single-threaded otimiza para o cliente daquele time.

### 3. Fitness Function (Métrica de Sucesso)
- Cada time tem UMA métrica principal que define sucesso
- A métrica deve ser controlável pelo time (não dependente de outros)
- Exemplos: latência da página, conversão do checkout, custo por transação

**Por que funciona:** Sem métrica clara, times otimizam para o que o líder pede,
não para o que o cliente precisa.

### 4. Ownership de Ponta a Ponta
- O time é dono do serviço: build, deploy, operate, on-call
- "You build it, you run it" - Werner Vogels
- Sem handoffs para "time de operações" ou "time de QA" separados

**Por que funciona:** Quando quem constrói também opera, a qualidade sobe
naturalmente. Ninguém escreve código ruim sabendo que vai ser acordado às 3AM.

### 5. APIs como Contratos
- Times se comunicam via APIs bem definidas, não reuniões
- O famoso "Bezos API Mandate" (2002): toda comunicação entre times
  deve ser via interfaces de serviço, sem exceção
- Quem violar será demitido (literal, do memo original)

**Por que funciona:** APIs forçam clareza de contrato. Reuniões permitem
ambiguidade. Contratos explícitos escalam; dependências implícitas não.

## Estrutura Operacional

### Rituais de um Two Pizza Team

**Diário:**
- Standup de 15 minutos (status, bloqueios)
- Monitoramento de fitness function

**Semanal:**
- Review de métricas (comparação com semana anterior)
- Priorização de backlog

**Mensal:**
- Narrativa de 6 páginas sobre o estado do serviço
- Review com liderança (se necessário)

**Trimestral:**
- OP1/OP2 planning (planejamento operacional)
- Revisão de fitness function e OKRs

### Documento Narrativo (6-Pager)
Em vez de PowerPoint, a Amazon usa documentos narrativos de 6 páginas:
- Primeiros 20 minutos de cada reunião são leitura silenciosa
- Documento deve ter frases completas, não bullets
- Força pensamento rigoroso (bullets escondem lógica fraca)
- Inclui FAQ antecipando perguntas

## Vantagens Comprovadas

### Velocidade
- Times da Amazon deployam em média 136.000 vezes por dia
- Cada time deploya independentemente (sem release trains)
- Decisões tomadas em horas, não semanas

### Inovação
- AWS nasceu de um two-pizza team
- Alexa nasceu de um two-pizza team
- Amazon Go nasceu de um two-pizza team
- Autonomia permite experimentação sem permissão central

### Escalabilidade Organizacional
- Amazon cresceu de 5.000 para 1.5M+ funcionários mantendo o modelo
- Adicionar capacidade = adicionar times, não aumentar times existentes
- Cada time opera como uma mini-startup

### Accountability
- Sucesso e fracasso são claros (fitness function não mente)
- Sem "difusão de responsabilidade" de times grandes
- Promoções baseadas em resultados do time, não política

## Desafios e Soluções

### Desafio 1: Coordenação Entre Times
**Problema:** Times autônomos podem divergir em direções conflitantes.
**Solução Amazon:** Mechanisms, não reuniões.
- APIs bem definidas como contratos
- Tenets (princípios) escritos que guiam decisões
- Revisões de arquitetura periódicas (não aprovações prévias)

### Desafio 2: Duplicação de Esforço
**Problema:** Times independentes podem construir a mesma coisa.
**Solução Amazon:** Platform teams que oferecem serviços compartilhados.
- Mas clientes internos não são obrigados a usar (competição interna)
- Se o serviço interno é pior que a alternativa externa, o time pode sair

### Desafio 3: Crescimento de Carreira
**Problema:** Times pequenos limitam hierarquia (poucas posições de liderança).
**Solução Amazon:** Dual track (IC e management) com promoções baseadas em scope/impact.
- Um IC sênior pode ganhar mais que um gerente
- Scope aumenta horizontalmente (mais serviços) não verticalmente

### Desafio 4: Isolamento e Silos
**Problema:** Times muito autônomos perdem visão do todo.
**Solução Amazon:**
- Bar raisers em contratação (cross-team)
- Operational reviews semanais (visibilidade cross-team)
- Tenets compartilhados no nível de organização

## Como Implementar na Sua Empresa

### Fase 1: Identificar Domínios (Mês 1-2)
- Mapear serviços e responsabilidades atuais
- Identificar acoplamentos desnecessários entre times
- Definir boundaries de domínio (DDD ajuda aqui)

### Fase 2: Definir Fitness Functions (Mês 2-3)
- Para cada domínio, definir UMA métrica de output
- Garantir que a métrica é controlável pelo time
- Criar dashboard acessível a todos

### Fase 3: Reorganizar Times (Mês 3-4)
- Cada time com 6-10 pessoas
- Single-threaded leader para cada time
- Ownership de ponta a ponta (dev, ops, on-call)

### Fase 4: Estabelecer Contratos (Mês 4-6)
- Definir APIs entre times
- Documentar contratos e SLAs internos
- Eliminar dependências implícitas

### Fase 5: Rituais e Cadência (Mês 6+)
- Implementar 6-pagers em vez de decks
- Weekly metrics review por time
- Quarterly planning com narrativas

## Anti-Padrões Comuns

1. **Criar times pequenos sem dar autonomia** - Tamanho sem ownership é apenas um org chart menor
2. **Fitness function controlada por outro time** - Gera frustração e gaming de métricas
3. **Single-threaded leader que reporta a múltiplos stakeholders** - Dilui o foco
4. **APIs sem versionamento ou SLA** - Acoplamento escondido
5. **Copiar o modelo sem investir em plataforma** - Cada time reinventando a roda

## Referências

- "Working Backwards" - Colin Bryar & Bill Carr (2021)
- "The Everything Store" - Brad Stone (2013)
- Werner Vogels Blog - "The Bezos API Mandate"
- Amazon Shareholder Letters (1997-2024)
- "Team Topologies" - Matthew Skelton & Manuel Pais (2019)
