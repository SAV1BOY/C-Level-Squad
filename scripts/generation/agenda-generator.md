# Agenda Generator — WBR/MBR

> Script/prompt para geração automática de agendas de Weekly Business Review (WBR) e Monthly Business Review (MBR).

---

## Objetivo

Este script automatiza a criação de agendas estruturadas para revisões de negócio,
garantindo que todas as métricas relevantes, pontos de decisão e responsáveis estejam
claramente definidos antes de cada reunião.

---

## Inputs Necessários

### Dados Obrigatórios
1. **Tipo de revisão**: WBR ou MBR
2. **Data da reunião**: formato ISO 8601 (YYYY-MM-DD)
3. **Participantes confirmados**: lista com nome e role de cada participante
4. **Período de referência**: semana ou mês sendo analisado
5. **Squad responsável**: qual squad lidera a revisão

### Dados Opcionais
6. **Itens carryover**: decisões pendentes da reunião anterior
7. **Alertas ativos**: riscos ou incidentes em aberto
8. **Temas especiais**: itens fora da cadência normal que precisam de espaço

---

## Formato de Saída

A agenda gerada deve seguir esta estrutura:

### Bloco 1 — Abertura (5 minutos)
- Confirmação de quórum
- Revisão de action items da reunião anterior
- Status de decisões pendentes (carryover)

### Bloco 2 — Métricas Core (15–25 minutos)
- Apresentação do metrics pack atualizado
- Destaque para métricas fora do threshold definido
- Análise de tendências (week-over-week ou month-over-month)
- Comparação contra forecast e targets

### Bloco 3 — Deep Dives (15–20 minutos)
- Máximo de 2 temas por sessão
- Cada deep dive deve ter owner, contexto e pergunta central
- Formato recomendado: narrativa escrita (não slides)

### Bloco 4 — Decisões (10–15 minutos)
- Lista de decisões a serem tomadas na reunião
- Para cada decisão: contexto, opções, recomendação, owner
- Classificação por urgência e impacto

### Bloco 5 — Action Items e Encerramento (5 minutos)
- Registro de todas as decisões tomadas
- Atribuição de action items com deadline e owner
- Confirmação de próxima reunião

---

## Métricas a Incluir por Tipo

### WBR — Métricas Semanais
| Categoria | Métricas | Fonte |
|-----------|----------|-------|
| Revenue | ARR pipeline, deals closed, churn semanal | CRM / Finance |
| Product | Uptime, deploy frequency, incident count | Engineering dashboard |
| Growth | WAU, activation rate, NPS semanal | Product analytics |
| Operations | SLA compliance, ticket resolution time | Operations dashboard |
| People | Headcount, open positions, offer acceptance | HR system |

### MBR — Métricas Mensais
| Categoria | Métricas | Fonte |
|-----------|----------|-------|
| Financial | P&L, cash flow, burn rate, runway | Finance system |
| Strategic | OKR progress, initiative health scores | Strategy tracker |
| Market | Market share, competitive moves, CAC/LTV | Marketing analytics |
| Talent | Retention rate, engagement score, DEI metrics | People analytics |
| AI/Tech | AI adoption rate, model accuracy, tech debt ratio | Engineering metrics |

---

## Pontos de Decisão — Framework

Cada ponto de decisão na agenda deve conter:

1. **Título da decisão**: descrição clara em uma frase
2. **Contexto**: por que esta decisão é necessária agora
3. **Dados de suporte**: métricas e evidências relevantes
4. **Opções identificadas**: mínimo de 2, máximo de 4 opções
5. **Recomendação**: opção recomendada com justificativa
6. **Impacto estimado**: o que muda se aprovado vs. não aprovado
7. **Owner da execução**: quem implementa a decisão
8. **Deadline**: quando deve estar implementado
9. **Critério de sucesso**: como saberemos que funcionou

---

## Regras de Validação

Antes de finalizar a agenda, o script deve verificar:

- [ ] Duração total não excede 60 minutos (WBR) ou 90 minutos (MBR)
- [ ] Todas as métricas core têm dados atualizados (máximo 24h de atraso)
- [ ] Cada deep dive tem owner confirmado
- [ ] Decisões pendentes da reunião anterior estão listadas
- [ ] Participantes obrigatórios estão confirmados
- [ ] Narrativas de deep dive foram submetidas com 24h de antecedência
- [ ] Metrics pack foi revisado pelo COO Orchestrator antes da reunião

---

## Prompt Template

```
Gere uma agenda de {tipo_revisao} para a data {data_reuniao}.
Participantes: {lista_participantes}
Período de referência: {periodo}
Itens carryover: {carryover_items}
Alertas ativos: {alertas}

A agenda deve seguir o formato padrão do C-Level Squad OS,
incluindo blocos de abertura, métricas, deep dives, decisões
e encerramento. Priorize itens por impacto no negócio.
```

---

## Notas de Implementação

- O agenda generator deve ser executado automaticamente 48h antes de cada WBR/MBR
- Notificações devem ser enviadas aos owners de deep dive para submissão de narrativas
- O metrics pack deve ser puxado automaticamente das fontes de dados configuradas
- Agendas anteriores devem ser consultadas para identificar padrões e carryover items
- O output final deve ser armazenado em `data/agendas/` com naming convention padrão
