# Padroes de Interacao entre Agentes do C-Level Squad

## Objetivo

Este documento define os padroes de comunicacao e colaboracao entre os agentes do C-Level Squad. Estabelece protocolos para consultas, decisoes conjuntas, resolucao de conflitos e fluxos de trabalho multi-agente.

## Tipos de Interacao

### 1. Consulta Direta (1:1)
Um agente consulta outro sobre tema especifico de sua especialidade.

**Quando usar:**
- Duvida tecnica sobre area de outro agente
- Validacao de recomendacao que toca outra area
- Busca de dados ou benchmarks de outra disciplina

**Protocolo:**
1. Agente solicitante formula a pergunta com contexto
2. Especifica o nivel de detalhe necessario
3. Agente consultado responde com fundamentacao
4. Se relevante, solicita que a resposta seja documentada

**Exemplo:**
```
CFO para CIO: "Estou avaliando o investimento em migrar para multi-cloud.
Preciso de uma estimativa de custo de infraestrutura e timeline de
implementacao para incluir no business case que vou apresentar ao board."
```

### 2. Analise Conjunta (Multi-agente)
Dois ou mais agentes colaboram em uma analise que requer multiplas perspectivas.

**Quando usar:**
- Decisao estrategica que impacta multiplas areas
- Avaliacao de projeto ou investimento significativo
- Preparacao de material para board ou investidores

**Protocolo:**
1. Coordenador identifica a necessidade e convoca agentes relevantes
2. Define o escopo e o output esperado
3. Cada agente contribui com sua perspectiva
4. Coordenador sintetiza as contribuicoes
5. Agentes validam a sintese antes da entrega final

**Exemplo:**
```
Coordenador: "Precisamos avaliar a oportunidade de expansao internacional.
Convoco CFO (viabilidade financeira), CIO (infraestrutura tecnica) e
CHRO (desafios de pessoas). Cada um prepara sua analise ate quinta.
Sintese na sexta."
```

### 3. Revisao entre Pares (Peer Review)
Um agente revisa o output de outro para garantir qualidade e completude.

**Quando usar:**
- Entregas de alta visibilidade (board, investidores)
- Recomendacoes que envolvem risco significativo
- Novos frameworks ou politicas

**Protocolo:**
1. Autor solicita revisao ao agente mais relevante
2. Revisor avalia em ate 48 horas
3. Feedback e estruturado: pontos fortes, ajustes necessarios, sugestoes
4. Autor incorpora feedback e finaliza
5. Ambos assinam a versao final

### 4. Escalacao e Resolucao de Conflito
Quando agentes tem recomendacoes divergentes sobre um mesmo tema.

**Quando usar:**
- CFO recomenda cortar investimento que CIO considera essencial
- CAIO propoe projeto de IA que CHRO avalia como risco para cultura
- Duas prioridades competem pelos mesmos recursos

**Protocolo:**
1. Agentes documentam suas posicoes com fundamentacao
2. Coordenador facilita a discussao
3. Busca-se consenso baseado em criterios objetivos
4. Se nao ha consenso, coordenador toma a decisao com base em prioridades estrategicas
5. Decisao e documentada com racional
6. Agente dissidente pode registrar ressalva

## Fluxos de Trabalho Padrao

### Fluxo: Resposta a Consulta Simples
```
Cliente -> Coordenador -> Agente Especialista -> Coordenador -> Cliente

Tempo esperado: 2-4 horas
Agentes envolvidos: 1-2
```

### Fluxo: Analise Estrategica Completa
```
Cliente -> Coordenador -> [Multiplos Agentes em paralelo] ->
Coordenador (sintese) -> Revisao cruzada -> Coordenador -> Cliente

Tempo esperado: 2-5 dias
Agentes envolvidos: 3-5
```

### Fluxo: Resposta a Crise
```
Deteccao -> Coordenador ativa protocolo -> Agentes relevantes mobilizados ->
War room virtual -> Updates regulares -> Resolucao -> Retrospectiva

Tempo esperado: variavel (horas a dias)
Prioridade: maxima - suspende outros trabalhos
```

### Fluxo: Projeto Multi-fase
```
Kick-off (Coordenador) -> Fase 1 (Agentes designados) ->
Checkpoint -> Fase 2 -> ... -> Entrega final -> Retrospectiva

Cada fase tem: owner, prazo, criterios de conclusao, checkpoint
```

## Regras de Comunicacao entre Agentes

### Principios
1. **Respeito a especialidade**: Cada agente e a autoridade em sua area
2. **Fundamentacao**: Discordar e saudavel, mas deve ser fundamentado
3. **Transparencia**: Compartilhar informacoes relevantes proativamente
4. **Concisao**: Respeitar o tempo dos outros agentes
5. **Documentacao**: Decisoes importantes sao registradas

### Formato de Solicitacao entre Agentes
```
De: [agente solicitante]
Para: [agente consultado]
Assunto: [tema em uma linha]
Contexto: [2-3 frases sobre o motivo]
Pergunta/Pedido: [especifico e claro]
Urgencia: [alta/media/baixa]
Prazo: [quando precisa da resposta]
Output esperado: [tipo e tamanho da resposta]
```

### Formato de Resposta entre Agentes
```
De: [agente consultado]
Re: [assunto original]
Resumo: [resposta em 1-2 frases]
Detalhamento: [analise completa]
Ressalvas: [limitacoes ou incertezas]
Sugestao: [proximos passos recomendados]
```

## Matriz de Responsabilidade (RACI)

### Para Consultas de Clientes
| Atividade | Coordenador | Agente Principal | Agentes Apoio |
|-----------|------------|-----------------|---------------|
| Triagem e roteamento | R/A | I | - |
| Analise e recomendacao | I | R/A | C |
| Revisao de qualidade | A | R | C |
| Entrega ao cliente | R | I | I |

R=Responsavel, A=Aprovador, C=Consultado, I=Informado

### Para Decisoes Estrategicas
| Atividade | Coordenador | Agentes | CEO |
|-----------|------------|---------|-----|
| Identificar necessidade | R | I | I |
| Reunir perspectivas | R | R | I |
| Sintetizar opcoes | R/A | C | I |
| Tomar decisao | I | C | R/A |
| Implementar | R | R | I |

## Anti-Padroes de Interacao

### Evitar
- **Silo**: Agente trabalha isolado sem consultar areas impactadas
- **Ping-pong**: Solicitacao fica indo e voltando sem resolucao
- **Hierarquia implicita**: Tratar um agente como superior a outro
- **Overload**: Consultar todos os agentes para toda questao
- **Bypass**: Ignorar o coordenador para questoes que requerem orquestracao
- **Paralise por analise**: Buscar consenso perfeito em vez de decidir
- **Falta de follow-up**: Nao fechar o loop apos consulta

### Boas Praticas
- Identificar o agente certo antes de consultar
- Fornecer contexto suficiente na primeira mensagem
- Definir prazo e urgencia desde o inicio
- Documentar decisoes e racional
- Agradecer contribuicoes e dar visibilidade ao impacto
- Fazer retrospectivas em colaboracoes complexas
