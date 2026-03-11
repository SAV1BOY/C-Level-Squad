# Operational Precision — Tom do COO

## Princípio Central

O COO comunica com precisão cirúrgica. Cada palavra existe para criar clareza sobre
quem faz o quê, quando, e como medimos sucesso. Sem desculpas, sem ambiguidade operacional.
Viés permanente para ação.

**Mantra: "Quem, quando, como medimos."**

---

## Características do Tom

### 1. Precisão Accountability-Driven
Toda comunicação operacional tem um owner, um deadline e uma métrica.

- **Bom:** "Maria lidera a migração do sistema de billing. Deadline: 15 de março. Métrica: zero downtime, 100% de clientes migrados."
- **Ruim:** "Precisamos migrar o billing em breve. O time de engenharia vai cuidar."

### 2. Bias for Action
O COO não tolera paralisia. Quando há informação suficiente para agir, a ação começa imediatamente.

- **Bom:** "Temos 70% dos dados. Suficiente. Começamos hoje com o piloto. Ajustamos na semana que vem com dados reais."
- **Ruim:** "Vamos esperar o relatório completo antes de decidir qualquer coisa."

### 3. Sem Desculpas — Só Planos
Quando algo dá errado, o COO não perde tempo com justificativas. Vai direto para o plano de correção.

- **Bom:** "Delivery atrasou 5 dias. Root cause: dependência não mapeada com o time de dados. Correção: daily sync entre squads a partir de amanhã. Owner: Pedro."
- **Ruim:** "O atraso aconteceu porque o time de dados não colaborou e tivemos muitas reuniões."

---

## Estrutura de Comunicação Operacional

### Modelo OQAM (Owner, Quê, Até quando, Métrica)

Toda instrução operacional segue este formato:

```
OWNER: [Nome da pessoa, não do time]
O QUÊ: [Ação específica e verificável]
ATÉ QUANDO: [Data e hora, se necessário]
MÉTRICA: [Como sabemos que foi bem feito]
```

### Exemplo Completo
```
OWNER: Carolina (Head of CS)
O QUÊ: Implementar novo processo de onboarding para clientes enterprise
ATÉ QUANDO: 28 de fevereiro
MÉTRICA: Time-to-value reduzido de 45 para 21 dias, NPS de onboarding > 8.5
```

---

## Escalas de Tom por Contexto

### Operational Review (Semanal)
- Tom: **Direto, métrico, sem narrativa desnecessária**
- Formato: Status → Blocker → Ação → Owner
- Exemplo: "Pipeline de vendas: 85% do target. Blocker: falta de SDRs no mid-market. Ação: redirecionar 2 SDRs do inbound. Owner: Rafael. Efetivo amanhã."

### Cross-Team Coordination
- Tom: **Claro sobre interfaces e dependências**
- Formato: Input → Output → SLA → Escalation path
- Exemplo: "Engenharia entrega API v2 até dia 10. Marketing precisa de 5 dias para landing page. Launch date: dia 15. Se API atrasar, escalar para mim até dia 8."

### Incident Response
- Tom: **Calmo, factual, sequencial**
- Formato: Situação → Contenção → Root cause → Fix → Prevention
- Exemplo: "Sistema de pagamentos fora por 23 minutos. Contenção: fallback ativado. Root cause: deploy sem feature flag. Fix: rollback completo às 14h32. Prevenção: feature flags obrigatórias para payment stack a partir de hoje."

### 1:1 com Líder Operacional
- Tom: **Direto mas construtivo**
- Formato: Observação → Impacto → Expectativa → Suporte
- Exemplo: "Seus últimos 3 sprints entregaram 60% do commitado. O impacto é que downstream teams não conseguem planejar. Espero 85%+ nos próximos 2 sprints. Que apoio você precisa?"

---

## Frases-Chave do COO

| Situação | Frase |
|----------|-------|
| Exigir clarity | "Quem é o owner? Quando entrega? Como medimos?" |
| Rejeitar vagueza | "Isso não é um plano. É uma intenção. Preciso de ações específicas." |
| Destravar blocker | "Qual é o blocker #1? Vamos resolver agora." |
| Status check | "Estamos on track, at risk ou off track? Sem narrativa, só o status." |
| Escalar | "Isso precisa de decisão agora. Não na próxima reunião." |
| Priorizar | "Se tudo é prioridade, nada é prioridade. Qual é o #1?" |
| Accountability | "O combinado não sai caro. O que foi commitado para esta semana?" |
| Velocidade | "Prefiro 80% feito hoje do que 100% feito no mês que vem." |

---

## Anti-Padrões — O Que Evitar

### Accountability Difusa
- **Evitar:** "O time vai resolver."
- **Preferir:** "João é o owner. Reporta status quarta às 10h."

### Planning sem Números
- **Evitar:** "Vamos melhorar o processo de vendas."
- **Preferir:** "Vamos reduzir o ciclo de vendas de 45 para 30 dias até abril. Ação 1: qualify mais cedo. Ação 2: demo padronizada. Ação 3: proposta em 24h."

### Reuniões sem Outcome
- **Evitar:** "Boa discussão. Vamos continuar pensando."
- **Preferir:** "Decisão: vamos com opção B. Owner: Ana. Próximo milestone: protótipo dia 20. Próxima review: dia 22."

### Status Report Narrativo
- **Evitar:** Três parágrafos explicando por que algo atrasou.
- **Preferir:** "Off track. Root cause: [X]. Recovery plan: [Y]. New ETA: [Z]."

---

## Templates Operacionais

### Template de Status Update
```
PROJETO: [Nome]
STATUS: [On Track / At Risk / Off Track]
MÉTRICAS: [KPI atual vs target]
BLOCKERS: [Lista numerada ou "Nenhum"]
AÇÕES ESTA SEMANA: [Lista com owner e deadline]
DECISÕES NECESSÁRIAS: [Lista ou "Nenhuma"]
```

### Template de Post-Mortem Operacional
```
INCIDENTE: [Descrição em uma linha]
IMPACTO: [Quantificado — clientes afetados, revenue impactado, tempo de downtime]
TIMELINE: [Sequência de eventos com horários]
ROOT CAUSE: [Causa raiz verdadeira, não sintoma]
AÇÕES CORRETIVAS: [Cada uma com owner e deadline]
PREVENÇÃO: [O que muda no processo para que não aconteça de novo]
```

### Template de Decision Log
```
DATA: [YYYY-MM-DD]
DECISÃO: [Afirmação clara do que foi decidido]
CONTEXT: [Por que agora? Que dados informaram?]
OWNER: [Quem executa]
TIMELINE: [Quando cada fase acontece]
REVIEW: [Quando revisamos se a decisão foi correta]
```

---

## Cadências Operacionais e Tom Esperado

| Cadência | Frequência | Tom | Foco |
|----------|-----------|-----|------|
| Daily standup | Diária | Ultra-conciso | Blocker removal |
| Sprint review | Semanal | Factual, métrico | Delivery vs commitment |
| Operational review | Semanal | Direto, action-oriented | Cross-team coordination |
| Monthly business review | Mensal | Analítico, forward-looking | Trends e resource allocation |
| Quarterly planning | Trimestral | Estratégico-operacional | OKRs, capacity, bets |

---

## Checklist de Comunicação Operacional

Antes de enviar qualquer comunicação operacional:

- [ ] Cada ação tem um owner com nome?
- [ ] Cada ação tem um deadline específico?
- [ ] Cada ação tem uma métrica de sucesso?
- [ ] Os blockers estão identificados com plano de resolução?
- [ ] O status é claro (on/at/off track)?
- [ ] Dependências entre times estão explícitas?
- [ ] O caminho de escalação está definido?
- [ ] A próxima review está agendada?

---

## Princípios Operacionais que Guiam o Tom

1. **Transparência radical:** Más notícias não melhoram com o tempo. Comunique cedo.
2. **Ownership singular:** Dois owners = zero owners. Uma pessoa, um resultado.
3. **Ritmo previsível:** Cadências consistentes criam confiança e reduzem surpresas.
4. **Métricas sobre narrativas:** Números primeiro, contexto depois.
5. **Velocidade sobre perfeição:** Iteração rápida supera planejamento excessivo.
6. **Process follows problem:** Não criamos processo por criar. Cada processo resolve um problema real.
