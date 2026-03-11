# Loop de Feedback entre Agentes

## Visao Geral

Este documento define o sistema de feedback continuo entre agentes do C-Level Squad. Feedback efetivo e o mecanismo que permite ao squad se auto-corrigir, aprender e melhorar continuamente. Sem feedback, erros se repetem e oportunidades de melhoria sao desperdicadas.

---

## Principios de Feedback

1. **Frequente e rapido**: Feedback dado proximo ao evento e mais acionavel que feedback acumulado.
2. **Especifico e factual**: Baseado em comportamentos observaveis e resultados mensuráveis, nao em opinioes vagas.
3. **Bidirecional**: Todo agente da e recebe feedback, independente de posicao hierarquica.
4. **Construtivo**: O objetivo e melhorar, nao criticar. Foco em "o que fazer diferente" ao inves de "o que fez errado".
5. **Documentado**: Feedback significativo deve ser registrado para tracking de evolucao.
6. **Seguro**: Nenhum agente deve ser penalizado por dar feedback honesto e respeitoso.

---

## Tipos de Feedback

### 1. Feedback Operacional (Continuo)

**O que e**: Feedback sobre a qualidade de entregas, processos e interacoes do dia a dia.
**Quando dar**: Imediatamente apos observar algo relevante.
**Formato**: Informal, direto, especifico.

**Exemplos**:
- "A analise financeira que voce entregou nao incluia o cenario pessimista. Para a proxima, inclua os 3 cenarios conforme nosso padrao."
- "O deploy de ontem teve zero downtime. Excelente planejamento de rollout."
- "O dashboard de metricas esta com latencia de 30 min. O SLA e de 5 min. Pode verificar?"

**Formato SBI (Situacao-Comportamento-Impacto)**:
```
FEEDBACK OPERACIONAL
De: [Agente]
Para: [Agente]
Situacao: [Quando e onde aconteceu]
Comportamento: [O que foi observado - factual]
Impacto: [Qual foi o impacto positivo ou negativo]
Sugestao: [O que manter ou mudar - se aplicavel]
```

### 2. Feedback de Performance (Periodico)

**O que e**: Avaliacao estruturada da performance do agente contra metricas definidas.
**Quando dar**: Mensalmente (resumo) e trimestralmente (completo).
**Formato**: Estruturado, baseado em metricas.

**Formato de Performance Review**:
```
FEEDBACK DE PERFORMANCE - [Periodo]
Agente avaliado: [Nome]
Avaliado por: [Nome(s)]

METRICAS QUANTITATIVAS
| Metrica | Target | Realizado | Status |
|---|---|---|---|
| [Metrica 1] | [Target] | [Real] | [Verde/Amarelo/Vermelho] |

PONTOS FORTES
1. [Evidencia especifica de excelencia]
2. [Evidencia especifica de excelencia]

AREAS DE MELHORIA
1. [Evidencia especifica + sugestao de melhoria]
2. [Evidencia especifica + sugestao de melhoria]

ALINHAMENTO ESTRATEGICO
[Avaliacao de contribuicao para OKRs do squad]

RECOMENDACOES
[Acoes especificas para o proximo periodo]
```

### 3. Feedback de Processo (Retrospectiva)

**O que e**: Avaliacao de como o squad trabalha junto, identificando melhorias em processos.
**Quando dar**: Quinzenalmente (retrospectiva) e trimestralmente (revisao profunda).
**Formato**: Facilitado pelo Squad Coordinator.

**Formato de Retrospectiva**:
```
RETROSPECTIVA - [Data]
Facilitador: Squad Coordinator
Participantes: [Lista]

O QUE FUNCIONOU BEM
1. [Processo/pratica que deve continuar]
2. [Processo/pratica que deve continuar]

O QUE PODE MELHORAR
1. [Processo/pratica com sugestao de melhoria]
2. [Processo/pratica com sugestao de melhoria]

O QUE DEVEMOS PARAR
1. [Processo/pratica que esta gerando desperdicio]

ACTION ITEMS
| Acao | Dono | Prazo | Status |
|---|---|---|---|
| [Acao 1] | [Agente] | [Data] | [Pendente] |
```

### 4. Feedback de Decisao (Post-mortem)

**O que e**: Avaliacao da qualidade de decisoes tomadas, revisando resultados vs expectativas.
**Quando dar**: 30-90 dias apos decisao significativa.
**Formato**: Analise estruturada.

**Formato de Review de Decisao**:
```
REVIEW DE DECISAO
Decisao: [Titulo]
Data da decisao: [Data]
Data da review: [Data]
Decidido por: [Agente(s)]

RESULTADO ESPERADO vs REAL
| Metrica | Esperado | Real | Delta |
|---|---|---|---|
| [Metrica] | [Valor] | [Valor] | [Diferenca] |

ANALISE
- O que deu certo na decisao: [...]
- O que nao deu certo: [...]
- O que fariamos diferente: [...]
- Informacao que tinhamos e nao usamos: [...]
- Informacao que nao tinhamos e precisavamos: [...]

LICOES APRENDIDAS
1. [Licao aplicavel a futuras decisoes]
2. [Licao aplicavel a futuras decisoes]
```

---

## Cadencia de Feedback

### Feedback Continuo (Diario/Semanal)

| Tipo | Cadencia | Responsavel | Formato |
|---|---|---|---|
| Feedback operacional | Continuo | Qualquer agente | SBI informal |
| Reconhecimento de boas praticas | Semanal (WBR) | Qualquer agente | Publico no squad |
| Alertas de melhoria | Imediato | Qualquer agente | Direto ao agente |

### Feedback Periodico (Mensal/Trimestral)

| Tipo | Cadencia | Responsavel | Formato |
|---|---|---|---|
| Performance review resumido | Mensal | COO + Vision Chief | Metricas + highlights |
| Retrospectiva de processos | Quinzenal | Squad Coordinator | Facilitacao estruturada |
| Performance review completo | Trimestral | Vision Chief | Review formal |
| Review de decisoes | 30-90 dias apos | Agente que decidiu | Post-mortem |
| Calibracao de squad | Trimestral | Vision Chief | Sessao com todo squad |

---

## Mecanismos de Seguranca Psicologica

### Regras para Dar Feedback

1. Focar em comportamentos observaveis, nao em intencoes presumidas.
2. Usar linguagem descritiva, nao julgadora.
3. Dar feedback negativo em privado, reconhecimento positivo em publico.
4. Oferecer sugestao concreta, nao apenas apontar o problema.
5. Ser oportuno — feedback tardio perde relevancia.

### Regras para Receber Feedback

1. Ouvir sem interromper ou justificar imediatamente.
2. Agradecer pelo feedback, mesmo quando desconfortavel.
3. Pedir exemplos especificos se o feedback for vago.
4. Refletir antes de responder — cooling period de 24h para feedback dificil.
5. Criar plano de acao para feedback acionavel.

### Protecoes do Sistema

1. Nenhum agente pode ser penalizado por dar feedback honesto e respeitoso.
2. Feedback anonimo e permitido em situacoes sensiveis, mas preferencia por feedback direto.
3. Padrao de retaliacao apos feedback e tratado como violacao de governance.
4. Vision Chief e responsavel por garantir seguranca psicologica do squad.

---

## Metricas do Sistema de Feedback

- Numero de feedbacks dados por agente/mes (target: minimo 2 por agente)
- Taxa de action items de retrospectiva completados (target: > 80%)
- Evolucao de metricas de performance entre trimestres
- Satisfacao dos agentes com o sistema de feedback (pesquisa trimestral)
- Decisoes revisadas que geraram aprendizado aplicado
- Tempo medio entre feedback e acao corretiva

---

## Integracao com Outros Protocolos

- **Escalacao**: Feedback negativo recorrente sem melhoria pode ser trigger de escalacao.
- **Handoff**: Feedback sobre qualidade de handoffs melhora o processo.
- **Comunicacao**: Feedback sobre clareza de comunicacao ajusta o protocolo.
- **Decisao conjunta**: Review de decisoes alimenta melhores decisoes futuras.

---

## Revisao

Este protocolo deve ser revisado a cada 90 dias ou quando a pesquisa de satisfacao indicar problemas no sistema de feedback.
