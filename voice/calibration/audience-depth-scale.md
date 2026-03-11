# Audience Depth Scale — Escala de Profundidade por Audiência

## Princípio Central

A mesma informação precisa ser comunicada em profundidades diferentes dependendo da audiência.
O erro mais comum é dar informação demais para quem precisa de pouco, e informação de menos
para quem precisa de muito.

**Escala: Team → Lead → VP → C-Level → Board**

---

## Os 5 Níveis de Profundidade

### Nível 1: Team (Detalhado)
**Audiência:** Membros do squad, contribuidores individuais
**Profundidade:** Máxima — implementação, código, processos, daily decisions
**Formato:** Documentação técnica, sprint tickets, daily standups, code reviews

**Exemplo — Incidente de Performance:**
> P99 latency no endpoint /api/checkout subiu de 180ms para 850ms após o deploy de
> ontem (commit abc123). Root cause: N+1 query no módulo de cálculo de frete que
> faz 1 query por item no carrinho. Fix: eager loading com preload(:shipping_rates).
> PR: #4521. Reviewer: @carlos. Deploy: hoje 15h. Monitoring: Datadog dashboard
> "Checkout Performance" por 48h.

### Nível 2: Lead (Resumo Tático)
**Audiência:** Tech leads, squad leads, gerentes de primeira linha
**Profundidade:** Alta — o que aconteceu, impacto, ação, timeline, owner
**Formato:** Status updates, sprint reviews, 1:1s com manager

**Exemplo — Mesmo incidente:**
> Performance issue no checkout identificado e corrigido. P99 latency estava em 850ms
> (SLO: 200ms). Root cause: query ineficiente no cálculo de frete. Fix deployado hoje.
> Owner: Ana. Monitoring intensificado por 48h. Impacto em clientes: mínimo — checkout
> ficou lento mas funcional por ~18h.

### Nível 3: VP (Highlights)
**Audiência:** VPs, Directors, senior leadership
**Profundidade:** Média — impacto no negócio, tendência, ação tomada, risco residual
**Formato:** Weekly reports, leadership meetings, dashboards executivos

**Exemplo — Mesmo incidente:**
> Incidente de performance no checkout: latência 4x acima do SLO por 18h. Corrigido.
> Impacto estimado: ~200 checkouts abandonados. Ação preventiva: adicionando performance
> testing obrigatório no CI pipeline. Implementação: próximas 2 semanas.

### Nível 4: C-Level (Decisões)
**Audiência:** CEO, COO, CTO, CFO, CMO, CAIO
**Profundidade:** Baixa-média — decisão necessária, impacto estratégico, resource implication
**Formato:** Executive briefings, decision memos, dashboard summaries

**Exemplo — Mesmo incidente:**
> Incidente de checkout resolvido. Impacto estimado: $15K em revenue perdido. Root cause
> corrigido. Investimento preventivo recomendado: performance testing automatizado —
> 2 sprints de eng time. Evita recorrência e protege reliability SLO de 99.9%.

### Nível 5: Board (Estratégico)
**Audiência:** Board of Directors, investidores
**Profundidade:** Mínima — só se for material. Foco em postura geral de reliability.
**Formato:** Board deck, quarterly report

**Exemplo — Mesmo incidente:**
> Platform reliability: 99.85% este quarter (target: 99.9%). Um incidente de performance
> impactou checkout por 18h. Corrigido com melhorias preventivas em andamento.
> Investimento em reliability: conforme plano. Risk assessment: baixo.

---

## Como Ajustar Profundidade

### Framework "ZOOM"

| Componente | Team | Lead | VP | C-Level | Board |
|-----------|------|------|-----|---------|-------|
| **Z**ero-in (detalhe técnico) | Completo | Resumido | Omitido | Omitido | Omitido |
| **O**utcome (resultado) | Detalhado | Detalhado | Destacado | Headline | Só se material |
| **O**wnership (quem/quando) | Individual | Por squad | Por área | Por executive | Omitido |
| **M**eaning (significado estratégico) | Contextual | Importante | Central | Central | Único foco |

### Regras de Ajuste

1. **Suba no nível = remova detalhe, adicione significado.**
   - Team: "Commit abc123 causou N+1 query"
   - Board: "Platform reliability está conforme o plano"

2. **Desça no nível = remova abstração, adicione ação.**
   - Board: "Investimos em reliability"
   - Team: "Adicionamos performance testing no CI com threshold de P99 < 200ms"

3. **Nunca dê mais detalhe do que o nível precisa.**
   - O CEO não precisa saber qual commit causou o bug.
   - O Board não precisa saber que contratamos 2 SREs.

4. **Sempre dê o suficiente para o nível agir.**
   - O VP precisa saber o impacto para priorizar recursos.
   - O C-Level precisa saber para aprovar investimento.

---

## Aplicação por Tipo de Informação

### Revenue Update

| Nível | Exemplo |
|-------|---------|
| Team | "Fechamos deal com Acme Corp: $120K ACV, 3-year contract, módulos X e Y, onboarding começa dia 15, CS owner: Marina" |
| Lead | "Novo deal enterprise: $120K ACV. Total mês: $450K (92% do target). Pipeline está healthy para bater meta." |
| VP | "Enterprise revenue on track: 92% do target com 3 weeks restantes. Pipeline coverage: 2.5x. Watch: mid-market abaixo por 15%." |
| C-Level | "Revenue: 92% on track. Enterprise forte. Mid-market at risk — recomendo realocar 2 AEs. Decisão necessária esta semana." |
| Board | "Revenue Q1: trending to $3.2M (target: $3.5M — 91%). Enterprise accelerating, mid-market adjusting. Forecast: $3.3M." |

### Product Launch

| Nível | Exemplo |
|-------|---------|
| Team | "Feature spec finalizada. PRD: [link]. Design: [link]. API contract: [link]. Sprint 1 começa segunda. Épicos: [lista]." |
| Lead | "Produto AI Analytics: development start segunda. 4 sprints estimados. Dependencies: data team (pipeline ready dia 20), design (UI specs dia 18)." |
| VP | "AI Analytics launch: Q2. Dev started. On track. Key risk: data pipeline dependency. Mitigation: daily sync com data team." |
| C-Level | "AI Analytics no roadmap de Q2. Investment: 8 eng-weeks. Expected impact: 15% increase em enterprise ACV. Launch: maio." |
| Board | "AI Analytics launching Q2. Strategic bet in AI-driven insights for enterprise. Expected revenue impact: +$500K ARR in first year." |

### Hiring Update

| Nível | Exemplo |
|-------|---------|
| Team | "Entrevistamos 5 candidatos para Senior Engineer. 2 passaram para final round: João (background em ML) e Clara (background em distributed systems). Decision: sexta." |
| Lead | "Hiring Senior Engineer: 2 finalistas, decisão sexta. Start date estimado: abril. Isso libera capacidade para o projeto de AI." |
| VP | "Eng hiring: 8/12 posições filled este quarter. 2 ofertas pendentes. Gap: 2 ML engineers — mercado competitivo. Ajustando compensation bands." |
| C-Level | "Hiring 67% complete. On track para 80% até Q-end. Blocker: ML talent — recomendo aumentar comp range em 15% para competir." |
| Board | "Team: 85 FTEs (plan: 92). Hiring on track. Key talent risk: ML engineers in competitive market. Adjusting comp strategy." |

---

## Erros Comuns de Calibração

### Over-Communication para Cima
- **Erro:** Dar ao C-Level o nível de detalhe do Team.
- **Sintoma:** Emails de 3 páginas para o CEO sobre um bug fix.
- **Correção:** "O CEO precisa saber isso? Muda alguma decisão? Se não, não escale."

### Under-Communication para Cima
- **Erro:** Dar ao C-Level menos informação do que precisa para decidir.
- **Sintoma:** "Está tudo bem" quando na verdade há risco crescente.
- **Correção:** "Se eu fosse o CEO, o que eu gostaria de saber para tomar boas decisões?"

### Wrong-Level para Baixo
- **Erro:** Dar ao Team informação estratégica sem contexto de ação.
- **Sintoma:** "O Board quer que cresçamos mais rápido." (Team: "E o que eu faço com isso?")
- **Correção:** Traduzir estratégia em ações concretas para o nível do Team.

### Same-Level para Todos
- **Erro:** Usar o mesmo formato de comunicação para todas as audiências.
- **Sintoma:** Board deck com 50 slides de detalhe operacional.
- **Correção:** Criar versões por audiência. É mais trabalho, mas gera mais impacto.

---

## Template: Multi-Level Communication

Quando um evento importante acontece, prepare comunicações em cascata:

```
EVENTO: [Descrição em uma frase]

BOARD (se material):
[2-3 frases: impacto, ação, postura]

C-LEVEL:
[5-7 frases: impacto quantificado, root cause, ação, owner, timeline]

VP:
[1 parágrafo: contexto, impacto, ação detalhada, recursos, timeline]

LEAD:
[2-3 parágrafos: detalhes operacionais, ações por squad, dependências]

TEAM:
[Documento completo: detalhes técnicos, PRs, configs, monitoring, runbooks]
```

---

## Checklist de Calibração de Profundidade

- [ ] A audiência está identificada corretamente?
- [ ] O nível de detalhe é adequado para essa audiência?
- [ ] A informação é suficiente para a audiência agir no seu nível?
- [ ] Detalhes desnecessários foram removidos (não escondidos — disponíveis se pedirem)?
- [ ] O significado estratégico aumenta conforme o nível sobe?
- [ ] O detalhe operacional aumenta conforme o nível desce?
- [ ] Se a audiência perguntar "e daí?", a comunicação já responde?
