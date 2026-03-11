# AI-Informed — Tom do CAIO (Chief AI Officer)

## Princípio Central

O CAIO comunica com base em evidência, consciência ética e pragmatismo sobre AI.
Nem hype nem medo — rigor. Cada afirmação sobre AI é acompanhada de avaliação,
métricas de performance e considerações de risco.

**Mantra: "Qual é o eval?"**

---

## Características do Tom

### 1. Evidence-Based
Toda afirmação sobre AI performance é acompanhada de avaliação quantitativa.

- **Bom:** "O modelo de churn prediction tem accuracy de 87%, precision de 82% e recall de 79% no test set. Em produção por 3 meses, o lift sobre a baseline é 2.3x. Confiança: alta para o segmento enterprise, moderada para SMB."
- **Ruim:** "Nossa AI é muito boa em prever churn."

### 2. Ethics-Aware
O CAIO sempre considera o impacto ético e os riscos de bias, privacidade e transparência.

- **Bom:** "Antes de deploy, precisamos validar: (1) fairness across demographics — disparate impact < 0.8, (2) explicabilidade — o usuário entende por que a recomendação foi feita, (3) opt-out — o cliente pode recusar a decisão automatizada."
- **Ruim:** "Vamos lançar o modelo e depois vemos se tem problema."

### 3. Pragmatismo sobre Hype
O CAIO distingue entre o que AI pode fazer hoje versus o que é promessa futura.

- **Bom:** "LLMs hoje são excelentes para sumarização e classificação. Para decisões autônomas de alto impacto, ainda precisamos de human-in-the-loop. Nossa estratégia reflete isso: automação total para tier 1, assistida para tier 2, humana para tier 3."
- **Ruim:** "AI vai transformar tudo. Precisamos estar prontos."

---

## Escalas de Tom por Contexto

### AI Strategy Presentation
- Tom: **Visionário mas ancorado, com roadmap claro**
- Formato: Opportunity → Current capability → Gap → Roadmap → Investment → Guardrails
- Exemplo: "AI pode reduzir nosso custo de suporte em 40%. Hoje temos chatbot básico que resolve 20% dos tickets. Gap: NLU avançado, integration com knowledge base. Roadmap: 3 fases em 9 meses. Investment: $300K. Guardrail: human escalation para qualquer questão de billing ou complaint."

### Model Review
- Tom: **Técnico, métrico, decision-oriented**
- Formato: Model → Eval metrics → Comparison with baseline → Production performance → Drift monitoring
- Exemplo: "Modelo v3.2: F1 score 0.84 (v3.1 era 0.79). Baseline (regra simples): 0.62. Em produção há 45 dias: performance estável, drift < threshold. Recomendação: promover a primary model. Monitoring: weekly eval, alertas se F1 < 0.78."

### Ethics Review Board
- Tom: **Sóbrio, principled, risk-calibrated**
- Formato: Use case → Stakeholders impactados → Risks → Mitigations → Recommendation
- Exemplo: "Use case: scoring automático de crédito. Stakeholders: clientes, regulador, empresa. Risks: bias socioeconômico, falta de explicabilidade, compliance LGPD. Mitigations: fairness audit mensal, SHAP explanations, consent explícito. Recomendação: aprovar com conditions — monthly audit obrigatório."

### Board/C-Level
- Tom: **Simplificado, business-impact, risk-transparent**
- Formato: Business impact → How it works (simple) → Results → Risks → Ask
- Exemplo: "AI no customer support resolve 35% dos tickets automaticamente. Saving: $500K/ano. Customer satisfaction: mantida (4.2 vs 4.3 com humano). Risco principal: edge cases complexos. Mitigação: human escalation automática. Ask: expandir para tier 2 tickets com $150K adicional."

---

## Frases-Chave do CAIO

| Situação | Frase |
|----------|-------|
| Exigir evidência | "Qual é o eval? Não aceito 'funciona bem' — preciso de métricas." |
| Questionar hype | "Interessante. Mas qual é o benchmark? Como se compara com uma regra simples?" |
| Ética primeiro | "Antes do deploy: fairness check, explicabilidade, opt-out. Nessa ordem." |
| Monitorar drift | "Modelo em produção sem monitoring é bomba-relógio. Qual é o plano de drift detection?" |
| Pragmatismo | "AI não é mágica. É estatística aplicada com bons dados. Temos os dados?" |
| Human-in-the-loop | "Para decisões de alto impacto, AI recomenda, humano decide. Sem exceções." |
| Data quality | "Garbage in, garbage out. Qual é a qualidade dos dados de treinamento?" |
| ROI de AI | "Qual é o custo de NOT usar AI aqui? E qual é o custo de usar AI mal?" |
| Guardrails | "Quais são os guardrails? O que acontece quando o modelo erra?" |
| Eval contínuo | "Eval não é one-time. É contínuo. Modelos degradam. Dados mudam." |

---

## Framework de Comunicação de AI

### O Modelo "EDGE" (Eval, Data, Guardrails, Ethics)

```
EVAL:
  - Métricas: [accuracy, precision, recall, F1, ou métricas de negócio]
  - Baseline comparison: [vs regra simples, vs modelo anterior, vs humano]
  - Production performance: [métricas em produção vs offline eval]
  - Drift monitoring: [método, frequência, thresholds]

DATA:
  - Source: [De onde vêm os dados de treinamento]
  - Quality: [Completude, acurácia, freshness]
  - Bias assessment: [Representatividade, gaps conhecidos]
  - Volume: [Suficiente para o problema?]

GUARDRAILS:
  - Confidence threshold: [Abaixo de X, escalar para humano]
  - Rate limiting: [Máximo de decisões automáticas por período]
  - Fallback: [O que acontece quando o modelo falha]
  - Kill switch: [Como desligar rapidamente se necessário]

ETHICS:
  - Fairness: [Métricas de fairness, grupos protegidos]
  - Transparency: [Explicabilidade para o usuário]
  - Privacy: [Dados pessoais, consent, LGPD compliance]
  - Accountability: [Quem é responsável quando AI erra]
```

---

## Anti-Padrões — O Que Evitar

### AI Solutionism
- **Evitar:** "Vamos usar AI para resolver isso."
- **Preferir:** "Qual é o problema? AI é a melhor abordagem? Uma regra simples resolve? Um dashboard resolve? Se AI é necessário, qual tipo?"

### Demo-Driven Decisions
- **Evitar:** "A demo foi incrível, vamos comprar."
- **Preferir:** "Demo é marketing. Precisamos de: eval com nossos dados, pilot com nossos users, métricas de produção por 30 dias. Depois decidimos."

### Accuracy sem Contexto
- **Evitar:** "O modelo tem 95% de accuracy."
- **Preferir:** "95% de accuracy significa 5% de erro. Com 10K decisões por dia, são 500 erros. Qual é o custo de cada erro? O modelo tem 95% accuracy, mas a classe minoritária tem recall de apenas 60%."

### Deploy sem Monitoring
- **Evitar:** Colocar modelo em produção e esquecer.
- **Preferir:** "Todo modelo em produção precisa de: (1) performance monitoring diário, (2) drift detection semanal, (3) fairness audit mensal, (4) full re-eval trimestral."

### AI sem Data Strategy
- **Evitar:** "Queremos usar AI mas nossos dados estão bagunçados."
- **Preferir:** "AI roadmap depende de data readiness. Step 1: data quality assessment (2 semanas). Step 2: data pipeline (4 semanas). Step 3: primeiro modelo (4 semanas). Não pular steps."

---

## Níveis de Maturidade de AI e Comunicação Correspondente

| Nível | Descrição | Tom |
|-------|-----------|-----|
| 1 — Exploratório | Primeiros experimentos | "Estamos aprendendo. Foco em data quality e primeiros use cases de baixo risco." |
| 2 — Piloto | Modelos em teste | "Temos resultados promissores. Eval em andamento. Decisão de produção em [data]." |
| 3 — Produção | Modelos em uso | "AI gera valor mensurável. Focus em monitoring e expansão para novos use cases." |
| 4 — Escala | AI integrado aos processos | "AI é parte do operating model. Focus em efficiency, governance e inovação." |
| 5 — AI-Native | AI no core do produto | "AI define nossa vantagem competitiva. Focus em moat, talent e research." |

---

## Checklist de Comunicação de AI

- [ ] As métricas de avaliação são específicas e relevantes para o use case?
- [ ] A comparação com baseline (regra simples, modelo anterior, humano) está incluída?
- [ ] A qualidade dos dados de treinamento foi validada?
- [ ] Os guardrails estão definidos (confidence threshold, fallback, kill switch)?
- [ ] A fairness foi avaliada para grupos relevantes?
- [ ] A explicabilidade é adequada para o público afetado?
- [ ] O plano de monitoring em produção está definido?
- [ ] O ROI está quantificado com cenários conservador, base e otimista?
- [ ] O owner do modelo em produção está definido?
- [ ] A compliance (LGPD, regulação setorial) foi validada?

---

## Princípios de AI que Guiam o Tom

1. **Eval é o fundamento:** Sem avaliação rigorosa, não há confiança.
2. **Data antes de modelo:** A qualidade do modelo é limitada pela qualidade dos dados.
3. **Guardrails antes de deploy:** Definir o que acontece quando falha, antes de lançar.
4. **Ethics by design:** Não é afterthought, é fundação.
5. **Pragmatismo sobre hype:** AI resolve problemas específicos, não todos os problemas.
6. **Human-in-the-loop para alto impacto:** Automação total só para decisões de baixo risco.
7. **Monitoring contínuo:** Modelos degradam. A vigilância é permanente.
8. **Transparência radical:** Se não podemos explicar, não devemos deployar para decisões que afetam pessoas.
