# Audience Depth Scale — Escala de Profundidade por Audiência

## Princípio Central

A mesma informação precisa de profundidades diferentes dependendo da audiência.
Detalhes demais para o Board é ruído. Resumo demais para o time é insuficiente.
O líder eficaz ajusta a profundidade sem perder a precisão.

---

## A Escala de 5 Níveis

### Nível 1: Time (Detalhado)
**Audiência:** Engenheiros, analistas, operadores, ICs (Individual Contributors)
**Profundidade:** Máxima — todos os detalhes necessários para executar
**Formato:** Documentação técnica, specs, runbooks, tickets detalhados

```
Exemplo — Novo Feature:
"Implementar endpoint /api/v2/pricing com suporte a multi-currency.
Currencies suportadas: USD, BRL, EUR, MXN. Conversion rates via API do Banco Central.
Cache de 1h. Fallback: rate do dia anterior. Schema: [detalhado].
Tests: unit + integration + load (1000 req/s). Deadline: 22 de março.
PR review: João. Deploy: feature flag 'pricing-v2'. Monitoring: dashboard X."
```

### Nível 2: Lead / Manager (Sumário)
**Audiência:** Tech Leads, Team Leads, Engineering Managers
**Profundidade:** Sumário com contexto suficiente para tomar decisões de priorização
**Formato:** Status updates, sprint reviews, weekly summaries

```
Exemplo — Mesmo feature:
"Pricing v2 (multi-currency): em andamento, 60% completo. On track para 22 de março.
Blocker: API do Banco Central tem rate limit — investigando solução de cache.
Risco: se cache não funcionar, atraso de 3 dias. Plano B: usar provider alternativo.
Preciso de decisão sobre provider alternativo até quarta."
```

### Nível 3: VP / Director (Highlights)
**Audiência:** VPs, Directors, Senior Leadership
**Profundidade:** Highlights e exceções — o que está on track não precisa de detalhe
**Formato:** Weekly reports, operational reviews, dashboards

```
Exemplo — Mesmo feature:
"Pricing v2: on track para março. Habilitará expansão LATAM.
Um risco técnico em resolução — equipe está endereçando. Sem escalação necessária.
Impacto no roadmap: nenhum. Dependencies: nenhuma pendente."
```

### Nível 4: C-Level (Decisões)
**Audiência:** CEO, COO, CTO, CFO, CMO
**Profundidade:** Apenas o que requer decisão, investimento ou direção estratégica
**Formato:** Executive summaries, decision memos, board prep

```
Exemplo — Mesmo feature:
"Expansão LATAM: pricing multi-currency entrega em março. Sem blockers.
Próximo step: go-to-market plan para México no Q2. Decisão necessária: budget de $200K
para time local. Recomendação: aprovar — payback em 9 meses baseado em pipeline existente."
```

### Nível 5: Board (Estratégico)
**Audiência:** Board of Directors, investidores
**Profundidade:** Estratégia, resultados, riscos e asks — zero detalhes operacionais
**Formato:** Board deck, quarterly updates, investor letters

```
Exemplo — Mesmo feature:
"Expansão internacional em andamento. LATAM ready no Q2.
Pipeline identificado: $1.5M. Investment ask: $200K para team local.
Expected return: $800K revenue in 12 months. Risk: FX volatility (mitigated by USD pricing)."
```

---

## Como Ajustar a Profundidade

### Regra 1: "Zoom In/Zoom Out"
Pense na comunicação como uma câmera. Cada nível é um zoom level diferente.

| De | Para | Ação |
|----|------|------|
| Time → Lead | Remover detalhes de implementação, manter status e blockers |
| Lead → VP | Remover blockers em resolução, manter exceções e riscos |
| VP → C-Level | Remover operacional, manter decisões e investment asks |
| C-Level → Board | Remover tático, manter estratégico e financial impact |

### Regra 2: "So What?" Test
Para cada nível acima, pergunte: "E daí?" Se a informação não muda uma decisão no nível acima, ela não sobe.

| Informação | Time | Lead | VP | C-Level | Board |
|------------|------|------|----|---------| ------|
| "Cache invalidation usa TTL de 1h" | Sim | Não | Não | Não | Não |
| "API tem rate limit — workaround em andamento" | Sim | Sim | Não | Não | Não |
| "Feature at risk de atraso" | Sim | Sim | Sim | Depende | Não |
| "Expansão LATAM depende desta feature" | Sim | Sim | Sim | Sim | Sim |
| "LATAM representa $1.5M em pipeline" | Não | Não | Sim | Sim | Sim |

### Regra 3: Exceções Sobem, Norma Fica
O que está on track fica no nível onde é gerenciado. Exceções (riscos, blockers, oportunidades inesperadas) sobem.

- **On track:** Fica no nível do time/lead. Reporta-se como "on track" nos níveis acima.
- **At risk:** Sobe até o nível que pode resolver (geralmente VP ou C-Level).
- **Off track:** Sobe com plano de recovery até o nível de decisão.
- **Opportunity:** Sobe até o nível que pode alocar recurso.

---

## Formatos por Nível

### Nível 1 (Time): Documentação Completa
- Specs técnicas
- Tickets com acceptance criteria
- Runbooks e playbooks
- Code comments e ADRs (Architecture Decision Records)

### Nível 2 (Lead): Status Estruturado
```
PROJETO: [Nome]
STATUS: [Green/Yellow/Red]
PROGRESSO: [% ou milestone]
BLOCKERS: [Lista ou "nenhum"]
RISCOS: [Lista ou "nenhum"]
DECISÃO NECESSÁRIA: [Sim/Não — se sim, qual]
PRÓXIMO MILESTONE: [Data e descrição]
```

### Nível 3 (VP): Dashboard + Exceções
- Dashboard com métricas-chave (visual, não texto)
- Apenas itens Yellow/Red em detalhe
- Decisões necessárias highlighted

### Nível 4 (C-Level): Decision Brief
```
TÓPICO: [Uma frase]
STATUS: [On/At/Off track]
DECISÃO NECESSÁRIA: [Sim/Não]
SE SIM: [Opções com recomendação]
INVESTMENT: [Se aplicável]
TIMELINE: [Key dates]
```

### Nível 5 (Board): Strategic Narrative
- Narrativa de 2-3 parágrafos
- Métricas-chave (5-7 números)
- Asks explícitos
- Conexão com estratégia de longo prazo

---

## Erros Comuns de Calibração

### Over-Detailing para C-Level
- **Sintoma:** CEO recebe reports de 10 páginas sobre operações.
- **Solução:** Resumir em 1 página com opção de drill-down se quiser.
- **Frase:** "Aqui está o resumo. O detalhe está disponível se quiser mergulhar."

### Under-Detailing para Time
- **Sintoma:** Time recebe direção vaga sem contexto suficiente para executar.
- **Solução:** Incluir o "porquê" e os critérios de sucesso.
- **Frase:** "O contexto é [X]. O objetivo é [Y]. Os critérios de sucesso são [Z]. Perguntem se algo não está claro."

### Wrong Audience
- **Sintoma:** Board recebe detalhes técnicos. Time recebe estratégia sem ação.
- **Solução:** Antes de comunicar, pergunte: "Essa audiência precisa disso para tomar qual decisão?"

### Asymmetric Information
- **Sintoma:** Diferentes níveis têm informações conflitantes.
- **Solução:** A mesma fonte de verdade (dashboard/documento), filtrada por nível.

---

## Framework de Decisão: "Para Quem Estou Comunicando?"

Antes de escrever qualquer comunicação, responda:

1. **Quem é a audiência?** [Time / Lead / VP / C-Level / Board]
2. **Que decisão essa pessoa precisa tomar?** [Execução / Priorização / Investment / Estratégia]
3. **Qual é o mínimo de informação para essa decisão?** [Esse é o conteúdo]
4. **O que é "nice to know" vs "need to know"?** [Corte o "nice to know"]
5. **Há uma ação esperada?** [Se sim, está explícita?]

---

## Checklist de Calibração de Profundidade

- [ ] A audiência está identificada?
- [ ] O nível de profundidade é adequado ao nível da audiência?
- [ ] Detalhes operacionais foram removidos para audiências estratégicas?
- [ ] Contexto estratégico foi adicionado para audiências executivas?
- [ ] Exceções estão destacadas e normais estão resumidas?
- [ ] A ação esperada é clara para o nível da audiência?
- [ ] O formato é adequado (doc técnico vs summary vs narrative)?
- [ ] O "So What?" test foi aplicado para cada ponto?
