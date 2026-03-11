# North Star Alignment — Framework de Alinhamento de Métricas

## Origem e Contexto

A North Star Metric (NSM) é a métrica única que melhor captura o valor central que sua
organização entrega aos clientes. Não é uma métrica de vaidade, não é receita (que é
output, não value), e não é uma métrica composta. É a métrica que, se crescer de forma
sustentável, significa que o negócio está saudável e os clientes estão sendo bem servidos.

O problema que este framework resolve: a maioria das organizações tem dezenas de métricas
e nenhum acordo sobre qual importa mais. Marketing otimiza leads, Vendas otimiza pipeline,
Produto otimiza engagement, Finanças otimiza margem — e frequentemente essas otimizações
conflitam. A NSM cria um ponto de convergência que alinha decisões em toda a organização.

A inspiração vem de empresas como Spotify (tempo de escuta), Airbnb (noites reservadas),
Facebook (daily active users), e Slack (mensagens enviadas por equipes ativas). Em cada
caso, uma métrica simples captura a essência do valor entregue.

O framework vai além de escolher a NSM. Ele conecta a métrica de visão ao dia-a-dia de
cada equipe através de uma árvore de métricas que desdobra a NSM em driver metrics e
team metrics acionáveis.

## Quando Usar

- Quando a organização não tem clareza sobre "a métrica que mais importa"
- Na definição de OKRs para garantir alinhamento vertical
- Quando equipes otimizam métricas locais que prejudicam o todo
- Após mudança de estratégia ou modelo de negócio
- Para resolver debates recorrentes sobre prioridade
- Na avaliação de novas features ou iniciativas ("isso move a NSM?")

## Quando NÃO Usar

- Em empresas pré-product-market fit (a NSM muda rápido demais; foque em PMF signals)
- Como métrica única para bônus (distorce comportamento e causa gaming)
- Para substituir entendimento profundo do negócio ("a NSM subiu, está tudo bem!")
- Quando o negócio tem múltiplas linhas independentes com clientes diferentes

## Estrutura / Modelo

### Árvore de Alinhamento

```
VISÃO (horizonte 5-10 anos)
  "Democratizar acesso a educação de qualidade na América Latina"
    │
NORTH STAR METRIC (NSM)
  "Alunos ativos completando módulos por mês"
    │
┌───┴────────────────────────────────────────────────────┐
│                  DRIVER METRICS                         │
│  (alavancas que movem a NSM — ownership do C-Level)    │
├─────────────────┬──────────────┬───────────────────────┤
│ Aquisição       │ Ativação     │ Retenção              │
│ Novos alunos/   │ % completam  │ % voltam no           │
│ mês             │ 1o módulo    │ mês seguinte          │
│ (CMO)           │ (CPO)        │ (CPO/CS)              │
├─────────────────┼──────────────┼───────────────────────┤
│                 TEAM METRICS                            │
│  (métricas que cada equipe controla diretamente)       │
├─────────────────┼──────────────┼───────────────────────┤
│ CAC por canal   │ Time-to-     │ Churn 30/60/90 dias   │
│ Lead quality    │ first-value  │ NPS por cohort        │
│ Conversion rate │ Onboarding   │ Feature adoption      │
│ (Mkt/Growth)    │ completion   │ Support tickets       │
│                 │ (Product)    │ (CS/Product)          │
└─────────────────┴──────────────┴───────────────────────┘
```

### Critérios para Escolha da NSM

A boa North Star Metric atende TODOS estes critérios:

```
CRITÉRIO          │ TESTE                                    │ EXEMPLO PASS │ EXEMPLO FAIL
──────────────────┼──────────────────────────────────────────┼──────────────┼─────────────
Valor ao cliente  │ Se cresce, o cliente está melhor?         │ Horas de     │ Revenue
                  │                                          │ aprendizado  │ (beneficia
                  │                                          │              │ empresa)
──────────────────┼──────────────────────────────────────────┼──────────────┼─────────────
Leading indicator │ Prevê crescimento futuro de receita?     │ Weekly       │ MRR (é
                  │                                          │ active users │ lagging)
──────────────────┼──────────────────────────────────────────┼──────────────┼─────────────
Acionável         │ Equipes podem influenciar diretamente?   │ Tasks        │ Market
                  │                                          │ completed    │ share
──────────────────┼──────────────────────────────────────────┼──────────────┼─────────────
Compreensível     │ Qualquer pessoa entende em 5 segundos?   │ Noites       │ Adjusted
                  │                                          │ reservadas   │ LTV/CAC ratio
──────────────────┼──────────────────────────────────────────┼──────────────┼─────────────
Não-manipulável   │ Difícil de gaming sem entregar valor?    │ Successful   │ Page views
                  │                                          │ transactions │ (inflável)
```

### Templates de NSM por Tipo de Negócio

| Modelo de Negócio | NSM Sugerida | Lógica |
|-------------------|-------------|--------|
| SaaS B2B | Equipes ativas usando feature core semanalmente | Uso real = valor = retenção |
| Marketplace | Transações completadas com sucesso por mês | Ambos os lados satisfeitos |
| E-commerce | Clientes com 2+ compras nos últimos 90 dias | Repeat = PMF real |
| Mídia/Conteúdo | Tempo de consumo qualificado por usuário ativo | Atenção = valor |
| Fintech | Volume transacionado por clientes ativos | Confiança operacional |
| EdTech | Alunos completando milestones de aprendizado | Progresso real do aluno |

## Processo de Aplicação (step-by-step)

### Passo 1: Mapear o Value Moment (1-2 dias)

Identifique o momento exato em que o cliente recebe valor do seu produto:
- Para Uber: completar uma corrida com segurança e satisfação
- Para Slack: equipe se comunicando e resolvendo problemas
- Para Netflix: assistindo conteúdo que gosta

**Exercício**: entreviste 10 clientes satisfeitos e pergunte: "Qual é o momento em
que nosso produto realmente faz diferença para você?" O padrão revela o value moment.

**Cuidado**: o value moment NÃO é o sign-up, não é o pagamento, não é o login.
É o momento de valor real entregue.

### Passo 2: Traduzir Value Moment em Métrica (1-2 dias)

Converta o value moment em algo mensurável:
- Value moment: "equipe resolve problemas mais rápido"
- Métrica candidata: "tickets resolvidos por equipe por semana"
- Teste contra os 5 critérios acima

Gere 3-5 métricas candidatas e avalie cada uma:

| Candidata | Valor | Leading | Acionável | Compreensível | Não-gaming | Total |
|-----------|-------|---------|-----------|---------------|------------|-------|
| Métrica A | 4     | 5       | 3         | 5             | 4          | 21    |
| Métrica B | 5     | 4       | 4         | 4             | 3          | 20    |
| Métrica C | 3     | 3       | 5         | 5             | 5          | 21    |

### Passo 3: Validar com Dados Históricos (1 semana)

Antes de adotar a NSM, valide:
- **Correlação com receita**: a métrica correlaciona com crescimento de receita? (R² > 0.7)
- **Correlação com retenção**: clientes com NSM alta retêm mais? (diferença >20pp)
- **Sensibilidade**: a métrica se move quando fazemos mudanças no produto?
- **Não-sazonalidade excessiva**: variações são por valor real ou por calendário?

Se não tem dados históricos, rode a métrica como leading indicator paralelo por 2-3 meses
antes de oficializar.

### Passo 4: Construir a Árvore de Métricas (2-3 dias)

Decomponha a NSM em driver metrics:

**Método de decomposição matemática**:
```
NSM = Novos usuários ativos × Taxa de ativação × Frequência de uso × Retenção

Cada componente se torna um driver metric:
- Aquisição: novos usuários → ownership CMO
- Ativação: taxa de conversão do onboarding → ownership CPO
- Frequência: sessões por semana → ownership Product/Growth
- Retenção: % que volta no mês seguinte → ownership CS/Product
```

**Método de input/output**:
```
Para cada driver metric, identifique as team metrics que são inputs:
- Driver: Taxa de ativação
  - Team metric 1: Tempo até primeiro value moment
  - Team metric 2: % que completa onboarding
  - Team metric 3: # de friction points no fluxo
```

### Passo 5: Atribuir Ownership (1 dia)

Cada métrica na árvore precisa de um dono claro:
- **NSM**: CEO/Vision Chief (accountability final)
- **Driver metrics**: membros do C-Level (accountability funcional)
- **Team metrics**: gerentes e tech leads (accountability operacional)

**Regra**: uma métrica, um dono. Co-ownership é non-ownership. Se duas áreas
influenciam a mesma métrica, uma delas é accountable e a outra é contributora.

### Passo 6: Instrumentar e Visualizar (1-2 semanas)

- Configure tracking confiável para NSM e todos os drivers
- Crie dashboard acessível a toda a organização
- NSM no topo, driver metrics abaixo, team metrics por área
- Alertas automáticos quando NSM ou drivers desviam > 10% da tendência
- Review semanal na liderança, mensal com toda a organização

### Passo 7: Integrar com Processos de Decisão (ongoing)

A NSM deve permear decisões cotidianas:
- **Roadmap de produto**: "esta feature move a NSM? Quanto?"
- **Priorização de backlog**: score de impacto na NSM como fator
- **Contratação**: "esta vaga move qual driver metric?"
- **Budget**: alocação proporcional ao impacto no driver metric
- **Review de performance**: métricas de equipe derivadas da árvore

## Exemplos Práticos

### Exemplo 1: SaaS de Gestão de Projetos

**NSM**: Equipes com 3+ membros ativos completando tarefas semanalmente

**Árvore**:
- Driver 1 — Aquisição: novos workspaces criados por semana
  - Team: sign-ups → trials → paid conversion
- Driver 2 — Ativação: % de workspaces que adicionam 3+ membros na primeira semana
  - Team: invite rate, onboarding completion, time-to-first-task
- Driver 3 — Engagement: tarefas completadas por membro ativo por semana
  - Team: feature adoption, mobile usage, integration adoption
- Driver 4 — Retenção: % de workspaces ativos mês-a-mês
  - Team: churn por cohort, NPS, support resolution time

### Exemplo 2: Marketplace de Serviços

**NSM**: Serviços concluídos com avaliação >= 4 estrelas por mês

Nota: inclui qualidade (>= 4 estrelas) para evitar otimização de volume
sem qualidade. A métrica força tanto supply quality quanto demand satisfaction.

### Exemplo 3: A Armadilha da NSM de Revenue

Uma empresa escolheu MRR como NSM. Resultado: time de vendas começou a fechar
contratos com clientes mal-fit que churnavam em 3 meses. MRR subia no curto prazo
e desabava no médio. Substituíram por "clientes ativos com NRR > 100%" — alinha
valor ao cliente com crescimento sustentável.

## Armadilhas Comuns

1. **NSM como receita**: receita é consequência de valor, não o valor em si. Use
   receita como constraint (precisa ser saudável), não como NSM.

2. **NSM composta demais**: "Score ponderado de engagement, satisfação e retenção".
   Ninguém entende, ninguém age. Mantenha simples.

3. **Gaming**: qualquer métrica pode ser manipulada. A defesa é ter métricas de
   counter-balance. Se NSM é "mensagens enviadas", monitore "conversas com resposta"
   para detectar spam.

4. **NSM estática**: a NSM pode mudar conforme o negócio evolui. Pre-PMF pode ser
   "engagement de early adopters". Post-PMF pode ser "transações recorrentes".
   Revise anualmente.

5. **Desalinhamento da árvore**: driver metrics que matematicamente não decompõem a
   NSM. Se aquisição × ativação × retenção ≠ NSM, a árvore está errada.

6. **Vanity metrics disfarçadas**: "usuários registrados" parece bom mas não mede valor.
   Teste: se a métrica dobrar mas ninguém usar o produto, ela subiria? Se sim, é vanity.

7. **Tirania da NSM**: usar a NSM para bloquear toda iniciativa que não a move
   diretamente. Algumas coisas importantes (segurança, compliance, debt) não movem
   a NSM mas são necessárias. Trate como investimento em infraestrutura.

## Integração com Outros Frameworks

- **Tese Estratégica** (`vision-chief-strategic-thesis.md`): a NSM deve derivar da tese.
  Se a tese muda, a NSM pode precisar mudar.
- **Kill List** (`vision-chief-kill-list.md`): iniciativas que não movem nenhum driver
  metric são candidatas naturais ao kill list.
- **Bet Sizing** (`vision-chief-bet-sizing.md`): apostas Core devem mover a NSM diretamente.
  O impacto estimado na NSM informa o sizing.
- **Operating Rhythm** (`coo-operating-rhythm.md`): a NSM e drivers são o conteúdo
  principal dos rituais de review operacional.
- **Full Funnel Architecture** (`cmo-full-funnel-architecture.md`): as métricas de funil
  do CMO devem conectar com a árvore da NSM.
- **Engineering Excellence** (`cto-engineering-excellence.md`): DORA metrics conectam com
  velocity de entrega que impacta drivers do produto.
- **Data as Product** (`cio-data-as-product.md`): a instrumentação da NSM é um data product
  core da organização.

## Referências

- Sean Ellis, *Hacking Growth* — conceito original de North Star Metric
- John Cutler — artigos sobre metric trees e product thinking
- Spotify — modelo de Squad Metrics alinhadas com missão
- Amplitude, *North Star Playbook* — guia prático de implementação
- Frank Slootman, *Amp It Up* — foco implacável em driving metrics
- Andy Grove, *High Output Management* — output vs activity metrics
- Marty Cagan, *Empowered* — outcome-based teams e metric ownership
