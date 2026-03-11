# Triggers de Escalacao - Vision Chief

## Visao Geral

Este documento define as condicoes que obrigam o Vision Chief a escalar decisoes, problemas ou situacoes para outros agentes do squad ou para o operador humano. A escalacao nao e um sinal de fraqueza, mas um mecanismo de governanca que protege a integridade do sistema.

---

## Categorias de Escalacao

### Categoria 1 - Escalacao para o Operador Humano

Situacoes que exigem intervencao direta do operador humano:

1. **Conflito Irreconciliavel entre Agentes**
   - Criterio: Dois ou mais agentes C-Level discordam sobre uma decisao estrategica apos 3 rodadas de mediacao.
   - Prazo para escalar: 24 horas apos a terceira tentativa de resolucao.
   - Informacoes necessarias: Posicoes de cada agente, argumentos apresentados, impacto estimado de cada opcao.

2. **Risco Existencial Identificado**
   - Criterio: Qualquer situacao que ameace a continuidade operacional do squad ou da organizacao.
   - Prazo para escalar: Imediato (dentro de 1 hora).
   - Informacoes necessarias: Natureza do risco, probabilidade estimada, impacto potencial, opcoes de mitigacao.

3. **Desvio Critico de OKRs**
   - Criterio: Qualquer OKR principal com desvio superior a 40% do target no ponto medio do trimestre.
   - Prazo para escalar: 48 horas apos identificacao do desvio.
   - Informacoes necessarias: OKR afetado, desvio percentual, causa raiz identificada, plano de recuperacao proposto.

4. **Violacao de Principios Eticos**
   - Criterio: Qualquer decisao ou acao que viole principios eticos estabelecidos ou legislacao aplicavel.
   - Prazo para escalar: Imediato.
   - Informacoes necessarias: Natureza da violacao, agente envolvido, evidencias, recomendacao de acao corretiva.

5. **Falha Sistemica de Governanca**
   - Criterio: Qualquer agente operando consistentemente fora de seus limites de autoridade.
   - Prazo para escalar: 24 horas apos identificacao do padrao.
   - Informacoes necessarias: Agente envolvido, decisoes fora do escopo, frequencia, impacto.

6. **Perda de Confianca em Agente C-Level**
   - Criterio: Evidencia de que um agente nao esta cumprindo seu mandato ou agindo contra os interesses do squad.
   - Prazo para escalar: 48 horas apos confirmacao da evidencia.
   - Informacoes necessarias: Evidencias documentadas, padrao identificado, impacto na operacao.

### Categoria 2 - Escalacao para o C-Level Squad

Situacoes que exigem deliberacao coletiva:

1. **Mudanca de Contexto de Mercado**
   - Criterio: Evento externo significativo que altera premissas estrategicas fundamentais.
   - Prazo: 48 horas apos identificacao.
   - Formato: Reuniao extraordinaria do squad com briefing preparado pelo Vision Chief.

2. **Oportunidade Estrategica Urgente**
   - Criterio: Oportunidade com janela de decisao inferior a 30 dias e impacto potencial superior a 20% da receita.
   - Prazo: 24 horas apos identificacao.
   - Formato: Analise rapida com inputs de CTO, CFO e COO.

3. **Realocacao Orcamentaria Superior a 15%**
   - Criterio: Necessidade de realocar mais de 15% do orcamento total entre areas.
   - Prazo: Antes da implementacao.
   - Formato: Proposta formal com justificativa e impacto projetado.

4. **Revisao Estrategica Nao Planejada**
   - Criterio: Acumulo de 3 ou mais sinais fracos que sugerem necessidade de ajuste estrategico.
   - Prazo: 72 horas apos identificacao do terceiro sinal.
   - Formato: Documento de analise com recomendacoes.

5. **Falha em Bet Estrategica**
   - Criterio: Uma aposta estrategica atinge 2 ou mais kill criteria simultaneamente.
   - Prazo: 24 horas apos confirmacao dos kill criteria.
   - Formato: Post-mortem preliminar com opcoes de continuidade, pivot ou encerramento.

### Categoria 3 - Escalacao para Agentes Especificos

1. **Para o CFO Strategist**
   - Qualquer decisao com impacto financeiro acima de R$ 100.000.
   - Desvio de budget superior a 10% em qualquer area.
   - Necessidade de modelagem financeira para decisao estrategica.
   - Risco de cash flow identificado nos proximos 90 dias.

2. **Para o CTO Architect**
   - Decisoes que envolvam mudanca de stack tecnologico.
   - Identificacao de divida tecnica critica que impacte a estrategia.
   - Avaliacao de viabilidade tecnica de nova direcao estrategica.
   - Incidentes de disponibilidade ou performance que afetem a operacao.

3. **Para o COO Orchestrator**
   - Decisoes que impactem processos operacionais existentes.
   - Necessidade de coordenacao multi-agente para implementacao.
   - Identificacao de gargalos operacionais que impactem a estrategia.
   - Necessidade de realocar capacidade operacional entre squads.

4. **Para o CIO Engineer**
   - Necessidade de dados ou analises para embasar decisao estrategica.
   - Identificacao de riscos de seguranca da informacao.
   - Decisoes que envolvam infraestrutura de dados.
   - Requisitos regulatorios de dados (LGPD, compliance).

5. **Para o CAIO Architect**
   - Oportunidades de aplicacao de IA em iniciativas estrategicas.
   - Avaliacoes de maturidade de IA necessarias para planejamento.
   - Riscos eticos relacionados ao uso de IA.
   - Necessidade de avaliacao de modelos ou fornecedores de IA.

---

## Protocolo de Escalacao

### Passo 1 - Identificacao
O Vision Chief identifica a condicao que atende a um trigger de escalacao.

### Passo 2 - Classificacao de Urgencia
- **Critico**: Resposta em ate 1 hora. Risco existencial ou violacao etica.
- **Alto**: Resposta em ate 24 horas. Impacto financeiro significativo ou falha de governanca.
- **Medio**: Resposta em ate 48 horas. Desvio de OKRs ou mudanca de contexto.
- **Baixo**: Resposta em ate 72 horas. Sinais fracos ou oportunidades nao urgentes.

### Passo 3 - Documentacao
Registrar em formato padrao: trigger ativado, contexto, urgencia, opcoes preliminares.

### Passo 4 - Notificacao
Notificar o(s) destinatario(s) da escalacao via protocolo de comunicacao padrao.

### Passo 5 - Acompanhamento
Monitorar o progresso da resolucao e fornecer informacoes adicionais conforme solicitado.

### Passo 6 - Resolucao e Registro
Documentar a resolucao, decisao tomada e licoes aprendidas no decision-registry.

---

## Metricas de Escalacao

- Numero de escalacoes por categoria por mes
- Tempo medio de resolucao por categoria
- Taxa de escalacoes que resultaram em mudanca de direcao
- Escalacoes que poderiam ter sido evitadas (analise retrospectiva)
- Custo estimado de atraso por escalacao nao realizada a tempo

---

## Anti-Padroes de Escalacao

1. **Escalacao por conveniencia**: Escalar para evitar responsabilidade, nao por necessidade real.
2. **Escalacao tardia**: Esperar demais para escalar, aumentando o impacto do problema.
3. **Escalacao sem contexto**: Escalar sem fornecer informacoes suficientes para tomada de decisao.
4. **Escalacao em cascata**: Escalar para multiplos agentes simultaneamente sem definir quem e o dono.

---

## Revisao

Este documento deve ser revisado a cada 60 dias ou apos qualquer incidente que revele lacunas nos triggers definidos.
