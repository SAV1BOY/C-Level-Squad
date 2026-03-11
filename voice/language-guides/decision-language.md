# Decision Language — Como Escrever Decisões

## Princípio Central

Decisões são o output mais importante de uma equipe executiva. A linguagem de decisão
deve ser precisa, rastreável e inequívoca. Cada decisão precisa de recommendation format,
linguagem de trade-off, calibração de incerteza e commitment language.

---

## Anatomia de uma Decisão Bem Escrita

### Estrutura Padrão

```
DECISÃO: [Afirmação clara e binária — fizemos X ou faremos X]
OWNER: [Nome da pessoa responsável pela execução]
DEADLINE: [Data específica]
CONTEXTO: [Por que essa decisão é necessária agora]
ALTERNATIVAS CONSIDERADAS: [O que mais avaliamos]
TRADE-OFFS: [O que ganhamos e o que perdemos]
NÍVEL DE CONFIANÇA: [Alto/Médio/Baixo com justificativa]
CRITÉRIO DE REVERSÃO: [Quando reconsideramos]
COMUNICAÇÃO: [Quem precisa saber e como]
```

---

## Recommendation Format

### Estrutura de Recomendação

Toda recomendação segue o padrão: **Recomendo [ação] porque [evidência], apesar de [trade-off].**

#### Exemplos

- "Recomendo aumentar o time de CS em 3 pessoas porque o churn correlaciona 0.85 com tempo de resposta, apesar de o custo adicional impactar margem em 2pp."
- "Recomendo adiar o launch para Q2 porque o NPS do beta é 32 (meta: 50), apesar de perdermos a janela do evento do setor."
- "Recomendo matar o produto B porque contribui 4% do revenue com 20% do custo de engenharia, apesar de 3 clientes enterprise dependerem dele."

### Graus de Recomendação

| Grau | Linguagem | Quando usar |
|------|-----------|-------------|
| Forte | "Recomendo fortemente" | Evidência clara, risco baixo de erro |
| Padrão | "Recomendo" | Evidência sólida, trade-offs aceitáveis |
| Condicional | "Recomendo, condicionado a [X]" | Depende de informação ou evento |
| Fraca | "Inclino para [X], mas preciso de mais dados" | Evidência insuficiente |
| Neutra | "Apresento as opções; a decisão é do [owner]" | Trade-offs equilibrados, decisão política |

---

## Trade-Off Language

### Como Articular Trade-offs

Todo trade-off tem três componentes: **o que ganhamos, o que perdemos, e por que vale a pena.**

#### Estrutura
```
GANHAMOS: [Benefício quantificado]
PERDEMOS: [Custo quantificado]
VALE PORQUE: [Razão estratégica]
```

#### Exemplos de Linguagem de Trade-off

- "Ao escolher velocidade sobre completude, entregamos em 4 semanas ao invés de 12, mas cobrimos 70% dos use cases ao invés de 95%. Vale porque os 70% representam 90% do revenue."

- "Ao priorizar enterprise sobre SMB, focamos em deals maiores ($50K+ ACV) mas reduzimos volume de novos logos. Vale porque LTV/CAC enterprise é 5x melhor."

- "Ao usar vendor solution ao invés de build, ganhamos 6 meses de velocidade mas perdemos 15% de margem e controle sobre roadmap. Vale porque time-to-market é o fator competitivo decisivo."

### Palavras de Trade-off

| Para ganhos | Para perdas | Para justificativa |
|-------------|-------------|---------------------|
| "Ganhamos" | "Ao custo de" | "Porque" |
| "Habilitamos" | "Abdicamos de" | "Dado que" |
| "Aceleramos" | "Desaceleramos" | "A evidência mostra que" |
| "Priorizamos" | "Despriorizamos" | "O ROI indica que" |
| "Investimos em" | "Desinvestimos de" | "O risco de não agir é" |

---

## Uncertainty Calibration — Linguagem de Incerteza

### Escala de Confiança

| Nível | Linguagem | Significado | Exemplo |
|-------|-----------|-------------|---------|
| 95%+ | "Sabemos" | Dados robustos, alta confiança | "Sabemos que enterprise churn caiu 30% com CS dedicado." |
| 80-95% | "Estamos confiantes" | Forte evidência, alguma incerteza | "Estamos confiantes que o novo pricing aumenta ACV em 15-25%." |
| 60-80% | "Acreditamos" | Evidência parcial, hipótese forte | "Acreditamos que o mercado LATAM está pronto para nosso produto." |
| 40-60% | "Nossa hipótese é" | Evidência limitada, teste necessário | "Nossa hipótese é que short-form video converte melhor para ICP SMB." |
| <40% | "Especulamos" | Pouca evidência, aposta | "Especulamos que AI agents substituem 50% do tier 1 support em 2 anos." |

### Regras de Calibração

1. **Nunca diga "sabemos" sem dados:** "Sabemos" implica que temos evidência verificável.
2. **Declare a fonte da confiança:** "Acreditamos, baseado em [3 meses de dados / pesquisa de mercado / feedback de 20 clientes]."
3. **Seja honesto sobre incerteza:** É melhor dizer "não sabemos" do que fingir certeza.
4. **Especifique ranges:** "Estimamos entre $2M e $3M" é melhor que "Estimamos $2.5M."

---

## Commitment Language — Linguagem de Compromisso

### Níveis de Compromisso

| Nível | Linguagem | Significado |
|-------|-----------|-------------|
| Hard commit | "Vamos fazer X até [data]" | Recurso alocado, plano definido |
| Soft commit | "Planejamos fazer X, condicionado a [Y]" | Intenção forte, dependência |
| Intent | "Nosso plano é X, revisamos em [data]" | Direção, sem commitment firme |
| Exploration | "Vamos investigar X até [data]" | Sem compromisso com ação, apenas análise |

### Compromisso Gradual

Para decisões grandes, use compromisso progressivo:

```
FASE 1 (commit): Investir $50K em piloto com 3 clientes. Deadline: 30 dias.
FASE 2 (conditional): Se piloto mostra > 20% improvement, expandir para 20 clientes.
FASE 3 (intent): Se escala funciona, rollout geral no Q3.
GATE: Review em cada transição. Kill criteria: <10% improvement.
```

---

## Decision Records — Como Documentar

### Template de Decision Record

```
ID: DEC-2026-042
DATA: 2026-03-11
TÍTULO: Migração para nova plataforma de billing
STATUS: Aprovada / Pendente / Rejeitada / Revisada

CONTEXTO:
O sistema atual de billing não suporta pricing multi-currency exigido
pela expansão para LATAM. Custo de workarounds: 40h/mês de engenharia.

DECISÃO:
Migrar para Stripe Billing até 30 de junho.

ALTERNATIVAS CONSIDERADAS:
A) Build in-house — 16 semanas, full control, alto custo de manutenção
B) Stripe Billing — 6 semanas, vendor dependency, escala automática
C) Manter atual + workarounds — $0 upfront, $200K/ano em custo indireto

TRADE-OFFS DA DECISÃO:
+ Velocity: 6 semanas vs 16 semanas
+ Escala: suporta multi-currency nativo
- Dependência de vendor (mitigação: abstraction layer)
- Custo: 2.9% + $0.30 por transação (aceitável até $10M ARR)

NÍVEL DE CONFIANÇA: Alto (85%)
BASEADO EM: Avaliação técnica de 3 semanas, referências de 5 empresas similares

OWNER: CTO (execução) + CFO (aprovação financeira)
DEADLINE: 30 de junho
REVIEW: 15 de abril (mid-point check)
CRITÉRIO DE REVERSÃO: Se integration issues excedem 2 semanas de atraso

COMUNICAÇÃO:
- Eng team: briefing na sprint planning de segunda
- Finance: reunião quinta com CTO para migration plan
- CS: aviso 2 semanas antes do switch para preparar clientes
```

---

## Anti-Padrões de Linguagem de Decisão

### Decisão Fantasma
- **Evitar:** "Decidimos focar em qualidade." (Não é decisão — não há trade-off explícito)
- **Preferir:** "Decidimos atrasar o launch 3 semanas para reduzir bugs críticos de 12 para 0."

### Falso Compromisso
- **Evitar:** "Vamos tentar fazer isso." ("Tentar" não é compromisso)
- **Preferir:** "Commitamos entregar MVP até dia 20. Se não for viável até dia 15, escalamos."

### Decisão sem Deadline
- **Evitar:** "Vamos migrar para o novo sistema." (Quando?)
- **Preferir:** "Migração começa dia 1 de abril. Fase 1 completa dia 30 de abril."

### Todos Decidem = Ninguém Decide
- **Evitar:** "O comitê decidiu." (Quem é accountable?)
- **Preferir:** "O CEO decidiu, após input do comitê executivo."

---

## Checklist de Decision Language

- [ ] A decisão está formulada como afirmação clara?
- [ ] O owner está nomeado (pessoa, não time)?
- [ ] O deadline é uma data específica?
- [ ] As alternativas consideradas estão listadas?
- [ ] Os trade-offs estão explícitos (ganho, perda, justificativa)?
- [ ] O nível de confiança está calibrado?
- [ ] O critério de reversão está definido?
- [ ] O plano de comunicação está feito?
- [ ] O commitment level é claro (hard/soft/intent/exploration)?
