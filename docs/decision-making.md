# Decision-Making — Regras e Processos de Decisão

> Como o C-Level Squad toma decisões: framework, regras, ownership e accountability.

---

## Filosofia de Decisão

O C-Level Squad segue princípios claros sobre como as decisões devem ser
tomadas. Decisões de qualidade requerem processo de qualidade, mas rapidez
é valorizada — indecisão é frequentemente pior que uma decisão imperfeita.

---

## Tipos de Decisão

### Type 1 — Irreversível (One-Way Door)
- **Impacto**: alto, difícil ou impossível de reverter
- **Exemplos**: mudança de estratégia, grande investimento, M&A, despedimento
- **Processo**: deliberação completa, múltiplos inputs, evidência robusta
- **Owner**: Vision Chief com consenso do squad
- **Tempo**: 1-2 semanas (pode ser acelerado se urgente)

### Type 2 — Reversível (Two-Way Door)
- **Impacto**: moderado, reversível com custo aceitável
- **Exemplos**: nova feature, mudança de processo, contratação, pricing test
- **Processo**: análise focada, consulta a stakeholders-chave
- **Owner**: agente do domínio relevante
- **Tempo**: 1-3 dias

### Type 3 — Operacional
- **Impacto**: baixo, facilmente reversível
- **Exemplos**: scheduling, priorização de backlog, formato de report
- **Processo**: decisão individual com bom julgamento
- **Owner**: qualquer agente dentro do seu domínio
- **Tempo**: imediato a horas

---

## Framework de Decisão — RAPID

### Roles
- **R**ecommend: quem analisa e propõe uma recomendação
- **A**gree: quem deve concordar (veto formal) — usar com parcimónia
- **P**erform: quem implementa após decisão
- **I**nput: quem fornece informação e perspectiva
- **D**ecide: quem toma a decisão final

### Regras do RAPID
1. Cada decisão tem exactamente 1 **D** (Decider)
2. O número de **A** (Agree) deve ser mínimo (0-2)
3. **I** (Input) é consultivo — pode ser ignorado com justificação
4. **R** (Recommend) prepara a proposta com opções e recomendação
5. **P** (Perform) é identificado antes da decisão, não depois

### Mapeamento por Default
| Tipo de Decisão | R | A | P | I | D |
|----------------|---|---|---|---|---|
| Estratégica | COO | Board | Squads | Todos | Vision Chief |
| Produto | CTO | — | Engineering | CMO, COO | CTO |
| Marketing | CMO | — | Marketing team | Vision, COO | CMO |
| Tecnologia | CTO/CIO | — | Engineering | CAIO | CTO |
| AI | CAIO | Vision | AI team | CTO, CIO | CAIO |
| Operacional | COO | — | Squads | Relevantes | COO |
| Pessoas | Vision | — | HR/Squads | COO | Vision Chief |
| Financeira | COO | Vision | Finance | Todos | Vision Chief |

---

## Processo de Decisão

### Passo 1 — Framing
Antes de decidir, enquadrar a decisão:
- **O que estamos a decidir?** (1 frase clara)
- **Porquê agora?** (trigger e urgência)
- **Que tipo de decisão é?** (Type 1, 2 ou 3)
- **Quem decide?** (aplicar RAPID)
- **Quando precisa de ser decidido?** (deadline)

### Passo 2 — Preparação
O **R** (Recommend) prepara:
- Contexto completo e dados relevantes
- Mínimo 2 alternativas viáveis (máximo 4)
- Análise de prós/contras de cada alternativa
- Recomendação com justificação
- Riscos identificados para cada opção
- Critérios de sucesso se a decisão for implementada

### Passo 3 — Consulta
- **I** (Input) fornece perspectiva e dados adicionais
- **A** (Agree) levanta concerns formais se existirem
- Consulta pode ser síncrona (reunião) ou assíncrona (documento)
- Prazo claro para input (default: 24h para Type 2, 72h para Type 1)

### Passo 4 — Deliberação
- **D** (Decide) revê toda a informação
- Pondera recomendação contra inputs e concerns
- Pode pedir clarificação ou dados adicionais
- Para Type 1: deliberação em reunião com debate aberto

### Passo 5 — Decisão
- **D** decide e comunica a decisão
- Decisão registada no decision log com todos os campos
- Se **A** não concorda: escalar ou aceitar dissent (registado)

### Passo 6 — Execução
- **P** (Perform) recebe a decisão com contexto
- Define plano de implementação
- Reports progresso conforme cadência

---

## Regras de Ouro

### 1. Disagree and Commit
Após decisão tomada, todos executam com energia total, mesmo quem discordou.
Dissent é registado mas não impede execução.

### 2. Bias for Action
Na dúvida entre decidir e esperar, decidir. Especialmente para Type 2 decisions.
Informação adicional raramente muda fundamentalmente a decisão.

### 3. Two-Pizza Rule for Input
Se precisas de mais de 6-8 pessoas para input, a decisão está mal enquadrada.
Simplifica ou divide.

### 4. Written Over Verbal
Decisões importantes são escritas. Isto força clareza de pensamento e cria
registo para o futuro.

### 5. Reversibility Determines Speed
Quanto mais reversível, mais rápido deve ser o processo. Type 2 decisions
não devem usar processo de Type 1.

### 6. No Decision is a Decision
Adiar uma decisão sem deadline é uma decisão de não decidir. Torna isso
explícito se for intencional.

---

## Resolução de Conflitos

### Quando Agentes Discordam
```
1. DEBATE: discussão aberta com dados e argumentos
2. COMPROMISE: procurar solução que acomoda as preocupações de ambos
3. ESCALATE: se não há consenso, o Vision Chief decide
4. COMMIT: todos executam a decisão final
```

### Quando Dados Conflituam
```
1. VERIFICAR: confirmar precisão de ambas as fontes
2. CONTEXTUALIZAR: entender o que cada dataset mede
3. TRIANGULAR: procurar terceira fonte independente
4. DECLARAR: explicitar limitações e decidir com incerteza conhecida
```

---

## Anti-Patterns de Decisão

| Anti-Pattern | Problema | Solução |
|-------------|---------|---------|
| Design by committee | Todos decidem, ninguém é accountable | Clarificar RAPID |
| Analysis paralysis | Sobre-análise impede acção | Definir deadline + boa o suficiente |
| HiPPO | Highest Paid Person's Opinion domina | Exigir dados antes de opinião |
| Decision amnesia | Decisões esquecidas ou revertidas | Decision log obrigatório |
| Scope creep decisório | Decisão expande para incluir tudo | Manter framing original |
| Veto abuse | Bloqueio sistemático sem alternativa | Veto exige contraproposta |

---

## Métricas de Decisão

| Métrica | Target | Como Medir |
|---------|--------|-----------|
| Decision velocity (Type 2) | <3 dias | Tempo entre trigger e decisão |
| Decision velocity (Type 1) | <2 semanas | Tempo entre trigger e decisão |
| Decision quality score | >70/100 | DQS framework |
| Decisões com registo completo | >90% | Decision log audit |
| Action completion pós-decisão | >85% | Action tracking |
