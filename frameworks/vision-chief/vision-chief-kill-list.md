# Kill List — Framework de Disciplina de Foco

## Origem e Contexto

O Kill List é o complemento essencial de qualquer estratégia. Se a estratégia diz o que fazer,
o Kill List declara explicitamente o que NÃO fazer. A maioria das organizações falha não por
falta de boas ideias, mas por excesso delas — perseguindo muitas iniciativas simultaneamente
e diluindo recursos, atenção e energia.

Peter Drucker argumentou que "não há nada tão inútil quanto fazer com grande eficiência algo
que não deveria ser feito". O Kill List institucionaliza essa sabedoria. É um documento vivo
que lista explicitamente: projetos cancelados, mercados que não vamos entrar, features que
não vamos construir, clientes que não vamos perseguir, e oportunidades que vamos ignorar
deliberadamente.

A disciplina de manter um Kill List é contra-intuitiva. Dizer "não" dói. Cada item na lista
representa uma oportunidade real que alguém defende. Mas o custo de não dizer "não" é pior:
fragmentação, mediocridade, burnout organizacional, e a incapacidade de vencer em qualquer
frente porque está tentando vencer em todas.

## Quando Usar

- Após definir a tese estratégica — para derivar os "nãos" dos "sins"
- Quando a organização tem mais de 5 iniciativas estratégicas simultâneas
- Quando equipes reclamam de context switching excessivo e falta de foco
- Antes de cada ciclo de planejamento (trimestral ou semestral)
- Quando um novo líder assume e herda uma carteira de projetos inflada
- Quando recursos (capital, pessoas, tempo) estão sob pressão
- Para resolver conflitos de prioridade entre áreas

## Quando NÃO Usar

- Como desculpa para não inovar ou explorar — o kill list é sobre foco, não sobre paralisia
- Para eliminar trabalho de manutenção necessário (debt, compliance, segurança)
- De forma autoritária sem explicar o racional — kills sem contexto geram ressentimento
- Como arma política para eliminar projetos de rivais internos
- Para decisões que são facilmente reversíveis (use o modelo two-way door da Amazon)

## Estrutura / Modelo

### Formato do Kill List

```
KILL LIST — [Organização] — [Período]

STATUS: ATIVO | Última revisão: [data] | Próxima revisão: [data]

═══════════════════════════════════════════════════════
ITEM #1: [Nome da iniciativa/oportunidade]
───────────────────────────────────────────────────────
Categoria:    [ ] Projeto  [ ] Mercado  [ ] Feature  [ ] Cliente  [ ] Processo
Data do Kill: [YYYY-MM-DD]
Sponsor Original: [quem defendia]
Racional:     [por que estamos matando — em 2-3 frases]
Custo de Oportunidade Evitado: [estimativa de recursos liberados]
Condição de Ressurreição: [o que precisaria mudar para reconsiderarmos]
Comunicação:  [ ] Equipe  [ ] Stakeholders  [ ] Clientes  [ ] Público
═══════════════════════════════════════════════════════
```

### Categorias de Kill

| Categoria | Descrição | Exemplo |
|-----------|-----------|---------|
| **Hard Kill** | Cancelamento definitivo, sem retorno | Sair de um mercado geográfico |
| **Soft Kill** | Pausado indefinidamente, pode ressuscitar | Feature deprioritizada |
| **Slow Kill** | Morte gradual, sem novos investimentos | Produto legacy em end-of-life |
| **Preemptive Kill** | Nunca começou, decisão de não perseguir | Oportunidade avaliada e rejeitada |

### Matriz de Decisão para Kill

```
                    IMPACTO ESTRATÉGICO
                    Baixo           Alto
                ┌───────────┬───────────┐
    Alto        │  KILL     │  KEEP     │
CUSTO DE        │  RÁPIDO   │  (core)   │
MANUTENÇÃO      ├───────────┼───────────┤
    Baixo       │  AVALIAR  │  KEEP     │
                │  (noise?) │  (grow)   │
                └───────────┴───────────┘
```

## Processo de Aplicação (step-by-step)

### Passo 1: Inventário Completo (1 semana)

Liste TUDO que a organização está fazendo ou considerando fazer:
- Projetos ativos com recursos alocados
- Projetos "em pausa" que consomem atenção mental
- Oportunidades em pipeline de avaliação
- Features solicitadas por clientes ou mercado
- Mercados ou segmentos em consideração
- Parcerias ou integrações em discussão

Regra: se consome tempo de pelo menos uma pessoa por semana, está na lista.

### Passo 2: Classificação contra a Tese (2-3 dias)

Para cada item, pergunte:
1. Este item conecta diretamente a uma aposta da tese estratégica?
2. Se não, ele protege algo existente de valor comprovado?
3. Se não, qual é o argumento para mantê-lo?

Itens sem conexão clara com a tese ou com proteção de valor existente são candidatos a kill.

### Passo 3: Análise de Custo de Oportunidade (2-3 dias)

Para cada candidato a kill, calcule:
- **Custo direto**: horas de engenharia, marketing spend, licenças
- **Custo indireto**: context switching, reuniões, comunicação
- **Custo de oportunidade**: o que essas pessoas/recursos fariam se liberadas
- **Custo de abandono**: compromissos com clientes, contratos, reputação

A decisão é: custo de oportunidade de manter > custo de abandono?

### Passo 4: Decisão e Documentação (1-2 dias)

Para cada item decidido como kill:
- Documente no formato do Kill List com racional claro
- Defina a condição de ressurreição (evita rediscussão infinita)
- Identifique dependências e impactos downstream
- Planeje a transição (clientes afetados, equipe realocada)

### Passo 5: Comunicação dos Kills (1 semana)

A comunicação é tão importante quanto a decisão:

**Para a equipe que trabalhava no item:**
- Explique o racional estratégico (não "corte de custos")
- Reconheça o trabalho feito ("não foi em vão, aprendemos X")
- Apresente o que vão fazer em seguida (realocação positiva)

**Para stakeholders e clientes afetados:**
- Comunique com antecedência quando possível
- Ofereça alternativas ou plano de transição
- Seja honesto sobre o motivo sem ser desnecessariamente detalhado

**Para a organização:**
- Contextualize dentro da estratégia ("estamos focando em X, por isso paramos Y")
- Celebre a disciplina de foco, não lamente a perda

### Passo 6: Ritual de Manutenção (ongoing)

O Kill List é vivo:
- **Mensal**: revise se novos candidatos surgiram
- **Trimestral**: avalie condições de ressurreição
- **Semestral**: revisão completa alinhada com a tese estratégica
- **Ad hoc**: quando nova oportunidade significativa aparece, force a pergunta
  "o que vamos parar de fazer para fazer isso?"

## Exemplos Práticos

### Exemplo 1: Startup SaaS com 50 pessoas

**Contexto**: produto B2B com 3 features principais. Equipe recebendo pedidos de
clientes enterprise para customizações, pedidos de SMB para simplificação, e
ideias internas para novo produto adjacente.

**Kill List resultante**:
- KILL: Customizações enterprise one-off (custo: 40% do tempo de eng)
- KILL: Novo produto adjacente (custo: 2 engenheiros + 1 PM por 6 meses)
- KEEP: Simplificação para SMB (alinhado com tese de escala via self-service)
- KILL: Integração com ERP X (apenas 3 clientes pedem, custo alto)

**Recursos liberados**: 5 engenheiros + 1 PM → realocados para core product.

### Exemplo 2: Scale-up com Múltiplos Produtos

**Contexto**: empresa com 3 produtos, sendo 2 lucrativos e 1 em estágio inicial.
Tese estratégica aponta para consolidação no mercado principal.

**Kill List resultante**:
- SLOW KILL: Produto 3 (estágio inicial, sem product-market fit após 18 meses)
- KILL: Expansão internacional para mercado C (distração do mercado principal)
- PREEMPTIVE KILL: Aquisição da empresa Y (boa empresa, direção errada)
- KEEP: Produtos 1 e 2 com investimento aumentado

### Exemplo 3: O Kill Mais Difícil — Matar o Projeto do Fundador

O kill mais politicamente difícil é quando o item é o "baby" de alguém poderoso.
Framework para essa conversa:
1. Apresente os dados sem julgamento
2. Reconheça o valor da visão original
3. Mostre o custo de oportunidade com números
4. Ofereça a condição de ressurreição (dá dignidade ao kill)
5. Deixe a pessoa processar antes de pedir acordo

## Armadilhas Comuns

1. **Kill list vazio**: se sua kill list está vazia, você não está sendo honesto sobre
   suas restrições de recursos. Toda organização tem mais oportunidades que capacidade.

2. **Kills sem comunicação**: matar um projeto silenciosamente cria confusão, rumores e
   ressentimento. Cada kill merece comunicação explícita.

3. **Zombie projects**: projetos "mortos" que continuam consumindo recursos porque ninguém
   formalizou o kill. Faça auditorias mensais.

4. **Kill e recriação**: matar um projeto e 3 meses depois aprovar algo muito parecido
   com outro nome. Mantenha o histórico de kills visível.

5. **Confundir kill com falha**: o kill é uma decisão estratégica, não um julgamento de
   qualidade. Muitos kills são de coisas boas que simplesmente não são as melhores.

6. **Paralisia por kill**: medo de matar qualquer coisa por medo de estar errado.
   Solução: a condição de ressurreição permite reverter se necessário.

7. **Kill list como punição**: usar o kill list para eliminar projetos de pessoas que
   caíram em desgraça. O critério é estratégico, não político.

## Integração com Outros Frameworks

- **Tese Estratégica** (`vision-chief-strategic-thesis.md`): a tese é o filtro primário
  para decisões de kill. Sem tese clara, kills são arbitrários.
- **Bet Sizing** (`vision-chief-bet-sizing.md`): recursos liberados por kills alimentam
  apostas maiores nas prioridades sobreviventes.
- **North Star Alignment** (`vision-chief-north-star-alignment.md`): itens que não movem
  a North Star Metric são candidatos naturais a kill.
- **Execution Engine** (`coo-execution-engine.md`): o COO precisa do kill list para
  alocar capacidade de execução nas prioridades certas.
- **Bottleneck Theory** (`coo-bottleneck-theory.md`): kills liberam o bottleneck
  organizacional — atenção da liderança.
- **Channel Portfolio** (`cmo-channel-portfolio.md`): canais com ROI abaixo do threshold
  são candidatos a kill no portfólio de marketing.

## Referências

- Michael Porter, *What is Strategy?* — "a essência da estratégia é escolher o que não fazer"
- Greg McKeown, *Essentialism* — disciplina de menos mas melhor
- Jim Collins, *Good to Great* — conceito de stop doing list
- Steve Jobs — "I'm as proud of what we don't do as I am of what we do"
- Warren Buffett — "The difference between successful people and really successful people
  is that really successful people say no to almost everything"
- Tim Ferriss — "What you don't do determines what you can do"
- Amazon, *Two-Way Door* framework — distinguir decisões reversíveis de irreversíveis
