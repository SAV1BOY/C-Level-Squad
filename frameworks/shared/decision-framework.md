# Framework de Decisão Compartilhado — Como Tomamos Decisões na Organização

## Propósito e Contexto

Decisões são o output mais importante de qualquer organização. A qualidade das decisões
determina a trajetória da empresa mais do que qualquer estratégia brilhante. Porém, a maioria
das empresas não tem um processo explícito de decisão — decisões acontecem em reuniões
aleatórias, por quem grita mais alto, ou por inércia (não decidir é decidir).

Este framework, inspirado em Bezos (Type 1 vs Type 2), Grove (decisão pelo mais informado),
e Kahneman (redução de noise), estabelece um vocabulário comum e um processo claro para como
a organização toma decisões. Não burocratiza — acelera, porque todos sabem quem decide, como
decide, e quando decide.

## Quando Usar

- Em qualquer decisão que afete mais de um time ou tenha impacto > 1 mês
- Quando há paralisia por análise (excesso de deliberação, falta de decisão)
- Quando decisões são revertidas frequentemente (sinal de processo ruim)
- No onboarding de novos líderes (como funcionamos)
- Quando há conflito sobre quem tem autoridade para decidir
- Em retrospectivas de decisões que deram errado

## Componentes do Framework

### 1. Classificação de Decisões (Bezos Adaptado)

**Type 1 — Irreversíveis e de Alto Impacto**
- Características: difícil ou impossível de reverter, consequências de longo prazo
- Exemplos: pivot de modelo de negócio, demissão em massa, escolha de stack core
- Processo: deliberação cuidadosa, múltiplos inputs, decisão pelo CEO/C-level
- Timeline: dias a semanas
- Documentação: obrigatória (Decision Record)

**Type 2 — Reversíveis ou de Baixo Impacto**
- Características: reversível, consequências limitadas, pode ser testado
- Exemplos: design de feature, ferramenta de produtividade, processo de sprint
- Processo: decisão rápida pela pessoa mais informada
- Timeline: horas a dias
- Documentação: opcional (pode ser Slack message ou meeting notes)

**Regra de ouro:** A maioria das decisões é Type 2. Trate-as como Type 2 a menos que haja
evidência clara de que é Type 1. O erro mais comum é tratar Type 2 como Type 1 (paralisia).

### 2. Modelo RAPID de Ownership

Para decisões Type 1, defina claramente os papéis:

| Papel | Descrição | Quem |
|-------|-----------|------|
| **R**ecommend | Propõe a decisão com análise e recomendação | Líder do tema |
| **A**gree | Deve concordar (tem poder de veto — usar com parcimônia) | Stakeholders críticos |
| **P**erform | Executa a decisão após tomada | Time responsável |
| **I**nput | Fornece informação e perspectiva (não tem veto) | Especialistas, afetados |
| **D**ecide | Toma a decisão final | Uma pessoa (não comitê) |

**Princípio fundamental:** O D (Decide) é sempre UMA pessoa. Decisões por comitê diluem
responsabilidade e geram compromissos medíocres.

### 3. Processo de Decisão Estruturado

**Para Type 1:**

```
1. FRAME: Definir a decisão a ser tomada (não a solução)
   "Devemos [X]?" é melhor que "Vamos fazer X!"

2. GATHER: Coletar informação e perspectivas
   - Dados quantitativos disponíveis
   - Input de stakeholders (I no RAPID)
   - Premissas explícitas
   - Riscos identificados

3. EVALUATE: Analisar opções
   - Mínimo 2 opções reais (se só há uma, você não está decidindo)
   - Prós e contras de cada opção
   - Reversibilidade de cada opção
   - Análise de cenários (o que acontece se der errado?)

4. DECIDE: Tomar a decisão
   - O Decider decide (não é votação)
   - Prazo: deadline definido antes de começar
   - "Disagree and commit" é válido e esperado

5. COMMUNICATE: Comunicar a decisão
   - Para quem precisa saber
   - Incluir o rationale (o "porquê", não só o "o quê")
   - Especificar next steps e owners

6. REVIEW: Avaliar a decisão depois
   - Data de review pré-definida
   - Critérios de sucesso/falha definidos antecipadamente
   - Ajustar ou reverter se necessário
```

### 4. Heurísticas de Decisão Rápida

Para decisões Type 2, use heurísticas ao invés de processo completo:

- **Regra 70%:** Se você tem 70% da informação e 70% de confiança, decida
- **Regra do arrependimento:** Qual decisão você se arrependeria mais de NÃO tomar?
- **Two-way door test:** Posso voltar atrás facilmente? Se sim, decide e testa
- **10/10/10:** Como me sentirei sobre essa decisão em 10 minutos? 10 meses? 10 anos?
- **Default to action:** Na dúvida, faça. Inação é sempre uma decisão (geralmente ruim)

## Template de Decision Record

```markdown
# Decision Record: [Título]

**Data:** [YYYY-MM-DD]
**Type:** [1 ou 2]
**Status:** [Proposta | Decidida | Implementada | Revertida]
**Decider:** [Nome]

## Contexto
[Por que essa decisão precisa ser tomada agora?]

## Opções
### Opção A: [Nome]
- Descrição: [resumo]
- Prós: [lista]
- Contras: [lista]
- Custo/Esforço: [estimativa]

### Opção B: [Nome]
(mesma estrutura)

## Decisão
[Qual opção foi escolhida]

## Rationale
[Por que esta opção e não as outras]

## Consequências Esperadas
- Positivas: [lista]
- Negativas/Riscos: [lista com mitigação]

## Review
- Data de review: [YYYY-MM-DD]
- Critérios de sucesso: [como saberemos se acertamos]
```

## Checklist de Qualidade de Decisão

- [ ] A decisão está classificada (Type 1 ou Type 2)?
- [ ] O Decider está claramente definido (uma pessoa)?
- [ ] Pelo menos 2 opções reais foram consideradas?
- [ ] Premissas estão explícitas?
- [ ] Existe deadline para a decisão?
- [ ] Stakeholders foram consultados (Input) sem ter poder de veto excessivo?
- [ ] O rationale está documentado (para Type 1)?
- [ ] Data de review está agendada?
- [ ] A decisão foi comunicada para os afetados?

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Decisões Type 1 documentadas | 100% | Contínuo |
| Tempo médio de decisão Type 2 | < 48 horas | Mensal |
| Decision reversal rate | < 20% | Trimestral |
| Decisões com review pós-decisão | > 80% das Type 1 | Trimestral |
| Decision velocity (decisões/semana) | Estável ou crescente | Mensal |
| Stakeholder satisfaction com processo | > 4/5 | Semestral |

## Anti-Padrões

1. **HiPPO** — Highest Paid Person's Opinion decide tudo
2. **Analysis paralysis** — Type 2 tratada como Type 1
3. **Consensus trap** — Buscar unanimidade em vez de decisão clara
4. **Undocumented reversal** — Reverter decisão sem explicar por quê
5. **Decision by meeting** — Agendar reunião = decidir (não é verdade)
6. **Decide and forget** — Decidir sem follow-up ou review

## Referências Cruzadas

- `frameworks/vision-chief/vision-strategy-cascade.md` — Decisões estratégicas no cascade
- `frameworks/cto-architect/build-vs-buy.md` — Framework de decisão build vs buy
- `frameworks/cto-architect/tech-radar.md` — Decisões de tecnologia
- `frameworks/cfo-strategist/scenario-planning.md` — Cenários que informam decisões
- `frameworks/shared/risk-management.md` — Risco como input para decisões
- `frameworks/shared/stakeholder-management.md` — Stakeholders no processo de decisão
- `frameworks/shared/communication-framework.md` — Comunicação de decisões
