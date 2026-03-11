# QBR — Quarterly Business Review Examples

> Exemplos de QBRs bem executadas: revisão trimestral, OKR scoring, forward planning.
> O mecanismo que conecta operação a estratégia.

---

## O Que é uma QBR

A Quarterly Business Review é o momento onde a organização levanta a cabeça da
execução diária e avalia: estamos no caminho certo para os objetivos anuais?
Os pressupostos que definimos há 3 meses ainda são válidos? Precisamos ajustar
o curso estratégico?

A QBR é o mecanismo de feedback loop mais importante entre estratégia e execução.
Sem ela, planos anuais tornam-se ficção em 90 dias.

---

## Estrutura Recomendada da QBR

### Formato
- **Duração:** Half-day (4-5 horas) ou full-day para QBRs anuais
- **Frequência:** Trimestral, nas primeiras 2 semanas após fecho do quarter
- **Participantes:** C-Level completo, VPs, convidados estratégicos
- **Formato:** Pre-read distribuído 48h antes + apresentação + workshop

### Agenda de Half-Day

```
09:00-09:30  Abertura: State of Business (CEO)
09:30-10:30  Quarter em Revista: Métricas e OKR Scoring
10:30-10:45  Break
10:45-11:45  Deep-Dives por Área (3x20 min)
11:45-12:30  Forward Planning: Prioridades do Próximo Quarter
12:30-13:00  Decisões e Commitments
```

---

## Exemplo Completo: QBR Q4 2025

### State of Business — Abertura pelo CEO

**Contexto macro:**
"Fechamos 2025 com $32M ARR, 8% abaixo do target de $35M. O gap concentra-se em
dois fatores: atraso no lançamento do produto enterprise (que impactou $2M em pipeline)
e churn acima do esperado no segmento mid-market ($1M). Apesar do miss no target
absoluto, a qualidade do revenue melhorou — gross margins subiram de 68% para 74%
e net revenue retention estabilizou em 112%."

**Highlights do quarter:**
- Lançamento do produto enterprise (2 meses atrasado, mas com excelente reception)
- 3 enterprise logos fechados com ACV > $200K (validação de product-market fit)
- Engineering velocity melhorou 25% após tech debt sprint do Q3
- NPS subiu de 35 para 44 (maior ganho trimestral desde fundação)

**Lowlights do quarter:**
- Revenue target missed por 8%
- 2 senior hires recusaram oferta (compensation gap vs. mercado)
- Concorrente Z fechou Series C de $80M — war chest significativa
- Data warehouse migration atrasada (impacta reporting quality)

### OKR Scoring — Q4 2025

#### Objective 1: Estabelecer Product-Market Fit no Enterprise
**Score: 0.7 (Achieved with caveats)**

| Key Result | Target | Actual | Score |
|---|---|---|---|
| Fechar 5 enterprise deals > $100K ACV | 5 | 3 | 0.6 |
| Enterprise NPS > 50 | 50 | 52 | 1.0 |
| Enterprise logo churn = 0% | 0% | 0% | 1.0 |
| Win rate enterprise > 30% | 30% | 24% | 0.4 |

**Análise:** Product-market fit confirmado qualitativamente (NPS forte, zero churn),
mas go-to-market motion ainda não está calibrado (win rate baixo, fewer deals que
target). O problema não é o produto — é o processo de venda.

#### Objective 2: Escalar Engineering para Suportar Roadmap 2026
**Score: 0.8 (Strong)**

| Key Result | Target | Actual | Score |
|---|---|---|---|
| Contratar 8 engineers seniores | 8 | 7 | 0.9 |
| Reduzir tech debt score de 40 para 25 | 25 | 28 | 0.8 |
| Deployment frequency > 20/semana | 20 | 22 | 1.0 |
| Change failure rate < 5% | 5% | 4.8% | 1.0 |

**Análise:** Engineering team está a executar bem. Tech debt precisa de mais um
sprint dedicado no Q1 para atingir target. Hiring quase completo — o 8o engineer
tem offer aceite, começa em Janeiro.

#### Objective 3: Construir Motor de Growth Previsível
**Score: 0.5 (Below expectations)**

| Key Result | Target | Actual | Score |
|---|---|---|---|
| Pipeline gerado > $5M | $5M | $3.8M | 0.6 |
| CAC payback < 12 meses | 12m | 16m | 0.4 |
| Marketing qualified leads > 500/mês | 500 | 380 | 0.5 |
| Implement attribution model | Done | Partial | 0.5 |

**Análise:** Growth engine ainda não é previsível. Pipeline abaixo do target por
conta de delays no enterprise marketing program. CAC payback alto reflete investimento
em segmento enterprise (deals maiores = ciclo mais longo). Attribution model parcial
— precisa de completion da data warehouse migration.

### Deep-Dives por Área

#### Deep-Dive 1: Product & Engineering (20 min)

**Roadmap execution vs. plan:**
- 70% do roadmap Q4 entregue (target: 80%)
- Principais atrasos: enterprise admin console (complexidade subestimada)
- Bet that worked: AI-powered search (adoption 3x acima da projeção)
- Bet that didn't: integration marketplace (adoção quase zero)

**Decisões necessárias para Q1:**
- Kill or pivot o integration marketplace?
- Investir mais no AI feature (double down on winner)?
- Priorizar admin console (enterprise blocker) ou novo produto?

#### Deep-Dive 2: Go-to-Market (20 min)

**Sales performance:**
- Enterprise: 3 deals fechados, pipeline growing, win rate a melhorar
- Mid-market: estável, 12 deals fechados, mas ASP a cair
- SMB: decisão de pause foi correcta — churn caiu 40% nos remanescentes

**Marketing performance:**
- Content marketing gerando 60% dos MQLs (eficiente)
- Paid acquisition com CAC 2x acima do target (ineficiente)
- Events: ROI positivo mas volume limitado

#### Deep-Dive 3: People & Finance (20 min)

**People:**
- Headcount: 87 (target: 92) — 5 positions open
- Regrettable attrition Q4: 2 people (aceitável)
- Engagement score: 7.4/10 (up from 6.8 em Q3)
- Compensation review necessária: 3 ofertas recusadas por compensation gap

**Finance:**
- Burn rate: $1.7M/mês (target: $1.5M)
- Runway: 19 meses
- Revenue efficiency: 0.7x (target: 1.0x)
- Next fundraise: provavelmente Q3 2026

### Forward Planning: Q1 2026 Prioridades

#### Company-Level OKRs Propostos para Q1

**Objective 1: Converter Enterprise PMF em Revenue Engine**
- KR1: Fechar 8 enterprise deals (pipeline: $4.2M qualified)
- KR2: Improve enterprise win rate de 24% para 35%
- KR3: Reduzir enterprise sales cycle de 90 para 60 dias
- KR4: Hire VP Sales com enterprise experience

**Objective 2: Dobrar Aposta em AI Features**
- KR1: Lançar AI assistant v2 com 3 novos use cases
- KR2: AI feature adoption > 60% da base active
- KR3: AI features citadas em 5+ enterprise deal wins
- KR4: File 2 patents de AI aplicada ao nosso domínio

**Objective 3: Resolver Foundation Issues**
- KR1: Complete data warehouse migration
- KR2: Compensation review + ajustes para roles em risco
- KR3: Tech debt score de 28 para 20
- KR4: Implement full attribution model

### Decisões e Commitments

| Decisão | Rationale | Owner | Deadline |
|---|---|---|---|
| Kill integration marketplace | Zero adoption em 6 meses, reallocar resources | VP Product | Imediato |
| Double-down AI features | Maior adoption metric do quarter | CTO + VP Product | Q1 roadmap |
| Hire VP Sales (enterprise) | Win rate gap requer specialized leadership | CEO | 60 dias |
| Compensation adjustment fund $200K | Retention risk em roles-chave | CFO + VP People | Janeiro |
| Pause paid acquisition | CAC 2x target, realocar para content + events | CMO | Imediato |

---

## Melhores Práticas para QBRs

### Pre-Read é Obrigatório
Distribuir o documento 48h antes. Participantes que não leram desperdiçam tempo
de todos. Considere começar com 15 min de leitura silenciosa (modelo Amazon).

### OKR Scoring Deve Ser Honesto
Score inflado destrói o propósito do sistema. Um score de 0.5 não é falha —
é informação. A cultura deve premiar honestidade, não green-washing.

### Forward Planning Deve Ser Constrained
Não tente fazer tudo. 3 objectives por quarter é o máximo para execução real.
Priorizar é decidir o que NÃO fazer.

### Decisões Devem Ser Tomadas na Sala
Se a QBR termina com "vamos pensar mais" em tudo, falhou. Pelo menos 2-3
decisões concretas devem sair da reunião.

### Action Items Com Owners e Deadlines
Toda decisão precisa de um owner individual (não um comitê) e um deadline
específico (não "em breve").

---

## Anti-Patterns de QBR

| Anti-Pattern | Descrição | Fix |
|---|---|---|
| Victory parade | Só highlights, sem lowlights | Exigir formato balanced |
| Data dump | 100 slides de dados sem insight | Narrativa > dados raw |
| Blame game | QBR como tribunal | Focar em sistema, não em indivíduos |
| Fantasy planning | OKRs impossíveis para Q+1 | Constrain a 3 objectives |
| Skip the hard conversations | Evitar tópicos desconfortáveis | CEO deve modelar o comportamento |

---

## QBR vs. Board Meeting

| Dimensão | QBR | Board Meeting |
|---|---|---|
| Audiência | Internal leadership | Board + Investors |
| Tom | Operacional, direto | Governança, formal |
| Profundidade | Deep-dives táticos | Strategic overview |
| Decisões | Operacionais e táticas | Governança e estratégia |
| Vulnerabilidade | Alta (lowlights esperados) | Calibrada (honesta mas controlada) |

---

## Referências

- John Doerr: "Measure What Matters" — OKR system
- Christina Wodtke: "Radical Focus" — OKR execution
- Colin Bryar & Bill Carr: "Working Backwards" — quarterly mechanisms
- Elad Gil: "High Growth Handbook" — scaling operating cadence

---

*Última atualização: Março 2026*
*Categoria: Operating Reviews | Nível: C-Level | Formato: Examples + Framework*
