# Padroes de Qualidade do C-Level Squad

## Objetivo

Este documento define os padroes minimos de qualidade para todos os outputs produzidos pelo C-Level Squad. Cada agente e responsavel por garantir que suas entregas atendam ou excedam esses padroes.

## Principios de Qualidade

### 1. Precisao e Confiabilidade
- Dados e metricas devem ser verificaveis e rastreavies a fontes confiaveis
- Nunca inventar numeros, estatisticas ou benchmarks
- Quando usar estimativas, declarar explicitamente que sao estimativas
- Citar fontes sempre que possivel (relatorios, pesquisas, bases de dados)
- Atualizar dados desatualizados antes de usar em analises

### 2. Relevancia Contextual
- Considerar o estagio da empresa (seed, series A, B, C+, scale)
- Adaptar recomendacoes a realidade brasileira quando aplicavel
- Considerar o setor de atuacao do cliente
- Levar em conta restricoes de recursos e capacidade de execucao
- Ponderar o momento macroeconomico

### 3. Acionabilidade
- Toda recomendacao deve ter proximo passo concreto
- Definir responsaveis sugeridos para cada acao
- Incluir timeline estimado para implementacao
- Priorizar acoes por impacto e esforco
- Evitar recomendacoes genericas que nao levam a acao

### 4. Clareza e Acessibilidade
- Linguagem acessivel ao publico-alvo da comunicacao
- Evitar jargao desnecessario; quando usar termos tecnicos, explicar
- Estruturar respostas com headers, bullets e formatacao clara
- Comecar sempre com resumo executivo de 2-3 linhas
- Usar tabelas e listas para comparacoes e dados quantitativos

## Padroes por Tipo de Entrega

### Analise Estrategica
- Minimo de 3 cenarios avaliados (conservador, base, otimista)
- Dados quantitativos de suporte para cada recomendacao
- Analise de riscos com probabilidade e impacto
- Benchmarks de mercado para contextualizar
- Proximo passo claro com timeline
- Tamanho minimo: 500 palavras

### Parecer Financeiro
- Numeros com precisao de duas casas decimais quando relevante
- Comparativo historico (minimo 2 periodos)
- Projecao de impacto no P&L e/ou caixa
- Premissas explicitamente declaradas
- Analise de sensibilidade para variaveis-chave
- Tamanho minimo: 400 palavras

### Parecer Tecnico
- Trade-offs documentados para cada opcao apresentada
- Impacto em performance, escalabilidade e seguranca
- Custo estimado de implementacao (tempo e recursos)
- Riscos tecnicos identificados com mitigacoes
- Alinhamento com arquitetura existente validado
- Tamanho minimo: 400 palavras

### Revisao de Processo
- Mapeamento do fluxo atual (as-is)
- Identificacao de gargalos e ineficiencias
- Proposta de fluxo otimizado (to-be)
- Metricas de melhoria esperada
- Plano de implementacao faseado
- Tamanho minimo: 500 palavras

### Resposta a Consulta Rapida
- Resumo executivo direto na primeira linha
- Fundamentacao concisa com dados
- Proximo passo acionavel
- Indicacao de onde aprofundar se necessario
- Tamanho minimo: 150 palavras

## Checklist de Qualidade Pre-Entrega

### Conteudo
- [ ] Resumo executivo presente e claro
- [ ] Dados e metricas verificados e com fontes
- [ ] Recomendacoes sao acionaveis e especificas
- [ ] Riscos e limitacoes declarados
- [ ] Cenarios multiplos considerados quando relevante
- [ ] Benchmarks de mercado incluidos para contexto

### Formato
- [ ] Estrutura com headers e subheaders logicos
- [ ] Bullet points para listas e passos
- [ ] Tabelas para comparacoes numericas
- [ ] Tamanho adequado ao tipo de entrega
- [ ] Tom de voz adequado ao contexto e audiencia

### Revisao
- [ ] Ortografia e gramatica verificadas
- [ ] Consistencia interna (numeros nao contraditorios)
- [ ] Premissas declaradas explicitamente
- [ ] Proximos passos com owners e prazos sugeridos
- [ ] Cross-reference com frameworks e documentos existentes

## Metricas de Qualidade

### Indicadores Quantitativos
- Percentual de entregas com resumo executivo: meta 100%
- Percentual de recomendacoes com proximo passo acionavel: meta 100%
- Percentual de analises com dados quantitativos de suporte: meta acima de 90%
- Tempo medio de entrega por tipo: monitorar tendencia

### Indicadores Qualitativos
- Satisfacao do stakeholder com a entrega (escala 1-5): meta acima de 4.0
- Utilidade percebida da recomendacao: meta acima de 4.0
- Clareza da comunicacao: meta acima de 4.0
- Adequacao do nivel de detalhe: meta acima de 3.5

## Processo de Melhoria Continua

### Revisao Mensal
- Analisar feedback recebido nas entregas do mes
- Identificar padroes de criticas ou elogios recorrentes
- Atualizar padroes de qualidade com base nos aprendizados
- Compartilhar best practices entre agentes do squad

### Revisao Trimestral
- Avaliar metricas de qualidade acumuladas
- Revisar e atualizar este documento
- Conduzir calibracao entre agentes sobre padroes
- Incorporar novos tipos de entrega se necessario

## Escalacao de Qualidade

Quando um output nao atende os padroes minimos:
1. O coordenador do squad identifica a deficiencia
2. Feedback especifico e enviado ao agente responsavel
3. Agente revisa e reentrega com correcoes
4. Se recorrente, revisao do processo e treinamento adicional
5. Documentar o caso para aprendizado coletivo
