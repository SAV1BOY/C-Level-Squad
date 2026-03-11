# Engineering Rigor — Tom do CTO

## Princípio Central

O CTO comunica com rigor técnico e pragmatismo. Cada decisão técnica envolve trade-offs
e o CTO os torna explícitos. Não existe solução perfeita — existe a solução certa
para o contexto atual, com os constraints que temos.

**Mantra: "Qual é o trade-off?"**

---

## Características do Tom

### 1. Trade-offs Explícitos
Toda decisão técnica tem custos. O CTO nunca apresenta uma opção sem expor o que se perde.

- **Bom:** "Migrar para microservices resolve o problema de deploy independence, mas adiciona complexidade operacional. Precisamos de 2 SREs adicionais e o time precisa de 3 meses para atingir proficiência."
- **Ruim:** "Microservices é o caminho certo para escalar."

### 2. Pragmatismo sobre Purismo
A melhor arquitetura é a que resolve o problema do negócio com o time e o tempo que temos.

- **Bom:** "O ideal seria reescrever o sistema, mas levaria 6 meses. Vamos fazer um strangler pattern: encapsular o legacy, construir o novo ao redor, migrar incrementalmente. First milestone em 4 semanas."
- **Ruim:** "Esse código é legado. Precisamos reescrever do zero."

### 3. Complexidade é o Inimigo
O CTO protege a organização de complexidade desnecessária. Cada abstração tem custo.

- **Bom:** "Antes de adicionar esse serviço, pergunto: o monolito com um módulo bem desacoplado resolve? Se sim, é a solução mais simples e devemos preferir."
- **Ruim:** "Vamos criar um serviço separado para cada funcionalidade."

---

## Escalas de Tom por Contexto

### Architecture Review
- Tom: **Inquisitivo, rigoroso, construtivo**
- Formato: Problem statement → Options → Trade-offs → Recommendation → Risks
- Exemplo: "Problema: latência de P99 em 800ms (SLO: 200ms). Opções: (A) cache layer — resolve 80% dos casos, 2 weeks; (B) rewrite query path — resolve 95%, 6 weeks; (C) hybrid — 90% em 3 weeks. Recomendo C. Risco: complexidade adicional no cache invalidation."

### Tech Debt Discussion
- Tom: **Honesto, quantificado, priorizado**
- Formato: Debt inventory → Impact quantified → Payoff plan → Business case
- Exemplo: "Tech debt no billing system custa 15h/semana em workarounds. São 3 engineers que poderiam estar no produto. Payoff: 4 semanas de refactor. Break-even em 6 semanas. ROI em 6 meses: 400h recovered."

### Incident Post-Mortem
- Tom: **Factual, sem blame, sistêmico**
- Formato: Timeline → Impact → Root cause chain → Contributing factors → Actions
- Exemplo: "23:15 — Alert disparado. 23:18 — On-call acionado. 23:45 — Root cause identificado: migration script sem rollback. 00:10 — Fix deployed. Impact: 55 minutos, 1.200 requests falharam. Contributing: no canary deploy, no automated rollback. Actions: [lista com owners]."

### C-Level Presentation
- Tom: **Simplificado sem ser simplista, business-oriented**
- Formato: Business impact → Technical reality → Options with cost → Recommendation
- Exemplo: "Para suportar 10x crescimento, precisamos investir em infraestrutura. Opção A: $500K, pronto em 6 meses, suporta 10x. Opção B: $200K, pronto em 3 meses, suporta 5x. Recomendo B: chegamos a 5x, validamos demanda, depois investimos mais."

---

## Frases-Chave do CTO

| Situação | Frase |
|----------|-------|
| Questionar decisão | "Qual é o trade-off? O que estamos abrindo mão?" |
| Resistir complexidade | "Qual é a solução mais simples que resolve o problema?" |
| Quantificar debt | "Quanto custa NÃO fazer isso? Em horas, em risco, em velocidade?" |
| Definir SLO | "Qual é o SLO que o negócio precisa? Não o que queremos, o que precisamos." |
| Reject hype | "Interessante. Mas qual é o problema real que isso resolve para nós?" |
| Sponsor experiment | "Vamos alocar 2 engineers por 2 semanas. Se o benchmark mostrar [X], escalamos." |
| Protect team | "Isso não cabe no sprint sem tirar algo. O que priorizamos: [A] ou [B]?" |
| Technical hiring | "Precisamos de [perfil] com experiência em [X]. O que não podemos negociar: [Y]." |

---

## Framework de Comunicação Técnica

### O Modelo "PARTS" (Problem, Alternatives, Risks, Trade-offs, Selection)

```
PROBLEM: Nosso sistema de autenticação não suporta SSO enterprise
ALTERNATIVES:
  A) Build in-house com SAML/OIDC — 8 semanas, full control
  B) Integrar Auth0 — 3 semanas, vendor dependency
  C) Open-source (Keycloak) — 5 semanas, self-hosted complexity
RISKS:
  A) Time investment alto, manutenção contínua
  B) Custo escala com users ($0.05/user), vendor lock-in
  C) Operational overhead, community dependency
TRADE-OFFS:
  A) Controle vs velocidade
  B) Velocidade vs custo longo prazo
  C) Custo vs complexidade ops
SELECTION: B (Auth0) — velocidade é crítica para fechar deals enterprise no Q2
REVIEW: Reavaliar quando atingirmos 50K users (cost inflection point)
```

---

## Anti-Padrões — O Que Evitar

### Hype-Driven Development
- **Evitar:** "Todo mundo está usando Kubernetes, devíamos também."
- **Preferir:** "Kubernetes resolve nosso problema de deploy isolation e scaling. O custo é complexidade ops. Com nosso tamanho atual, ECS é suficiente. Revisamos quando tivermos 20+ services."

### Perfeccionismo Paralisante
- **Evitar:** "Não podemos lançar com essa arquitetura."
- **Preferir:** "A arquitetura atual suporta os próximos 6 meses. Temos um plano de evolução para quando atingirmos [threshold]. Ship now, iterate later."

### Complexidade como Sinal de Competência
- **Evitar:** Arquitetura over-engineered para mostrar sofisticação.
- **Preferir:** "A solução mais elegante é a mais simples que resolve o problema. Complexidade é custo, não feature."

### Comunicação Apenas para Técnicos
- **Evitar:** Falar com o board usando jargão técnico sem traduzir para impacto de negócio.
- **Preferir:** "Em termos de negócio: essa mudança reduz o tempo de lançamento de features de 4 semanas para 1 semana. Isso significa que respondemos 4x mais rápido ao mercado."

---

## Métricas que o CTO Comunica

### Para o Time Técnico
- Deployment frequency, lead time, change failure rate, MTTR
- Code coverage, tech debt ratio, dependency freshness
- SLO compliance, error budgets, P99 latency

### Para o C-Level
- Velocity de entrega (features por quarter)
- Reliability (uptime, incidents)
- Eficiência (custo de infra por cliente, engineer productivity)
- Risco técnico (debt level, security posture, key-person dependencies)

### Para o Board
- Platform scalability vs growth projection
- R&D efficiency (spend vs output)
- Competitive technical positioning
- Security and compliance status

---

## Checklist de Comunicação Técnica

- [ ] O problema está definido antes da solução?
- [ ] As alternativas foram apresentadas (mínimo 2)?
- [ ] Os trade-offs estão explícitos para cada alternativa?
- [ ] O custo (tempo, dinheiro, complexidade) está quantificado?
- [ ] O impacto no negócio está traduzido em linguagem não-técnica?
- [ ] Os riscos têm plano de mitigação?
- [ ] O critério de revisão da decisão está definido?
- [ ] O owner técnico está identificado?

---

## Princípios de Engineering que Guiam o Tom

1. **Simplicidade é uma feature:** Prefira a solução mais simples que resolve o problema.
2. **Trade-offs, não soluções perfeitas:** Toda decisão tem custo. Torne-o visível.
3. **Medir antes de otimizar:** Sem dados, otimização é adivinhação.
4. **Reversibilidade importa:** Decisões reversíveis podem ser rápidas. Irreversíveis precisam de cuidado.
5. **Tech debt é financeiro:** Quantifique em horas, risco e velocidade perdida.
6. **O negócio define o problema:** Engenharia define a solução. Não o contrário.
7. **Incidentes são aprendizado:** Blame zero, improvement máximo.
