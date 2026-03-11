# OKR Blocks — Blocos Reutilizáveis para OKRs

> Referência do C-Level Squad para definir, acompanhar e avaliar OKRs.
> OKRs são a ponte entre estratégia (onde queremos ir) e execução (o que fazemos esta semana).

---

## 1. Bloco: Objective Template

### Template
```markdown
## Objective: [Título inspiracional e qualitativo]

**Descrição:** [1-2 frases expandindo o título com contexto]
**Owner:** [Nome — Cargo]
**Período:** [Q1 2026 / H1 2026 / Anual]
**Alinhamento:** [Pilar estratégico ou bet que este Objective suporta]
**Tipo:** [Committed (vamos entregar) / Aspirational (stretch — 70% seria ótimo)]
```

### Regras para Bons Objectives
1. **Qualitativo:** Sem números (números vão nos Key Results)
2. **Inspiracional:** Alguém deveria ficar motivado ao ler
3. **Acionável:** O time sabe para onde caminhar
4. **Time-bound:** Período definido (tipicamente 1 quarter)
5. **3-5 por nível:** Não mais que 5 objectives por empresa/time/pessoa

### Exemplos por Área
- **Negócio:** "Tornar-nos a escolha padrão para PMEs de serviços"
- **Produto:** "Entregar uma experiência de onboarding que encanta"
- **Eng:** "Construir uma plataforma que escala sem dor"
- **Vendas:** "Dominar o segmento mid-market no Sudeste"
- **People:** "Criar uma cultura onde os melhores querem trabalhar"

---

## 2. Bloco: Key Result Template

### Template
```markdown
### KR[N]: [Descrição mensurável]

- **Métrica:** [Nome da métrica]
- **Baseline:** [Valor atual / ponto de partida]
- **Target:** [Valor alvo]
- **Fonte de dados:** [Onde a métrica é medida]
- **Frequência de medição:** [Diária / Semanal / Mensal]
- **Progresso atual:** [X%] — [Valor atual vs target]
- **Confiança:** [Alta / Média / Baixa] de atingir o target
```

### Tipos de Key Results
| Tipo | Exemplo | Quando Usar |
|------|---------|-------------|
| **Valor / Métrica** | "Aumentar NPS de 32 para 50" | Quando há métrica clara e mensurável |
| **Milestone** | "Lançar módulo X em produção até DD/MM" | Quando o resultado é binário |
| **Threshold** | "Manter churn abaixo de 2% por 3 meses" | Quando é sobre manter um padrão |

### Regras para Bons Key Results
1. **Mensurável:** Número claro — sem ambiguidade sobre "atingiu ou não"
2. **Outcome, não output:** "Aumentar retenção D30 para 60%" (bom) vs "Enviar 10 emails" (ruim)
3. **Desafiador mas possível:** 70% de confiança de atingir = stretch certo
4. **2-5 por Objective:** Menos que 2 é vago, mais que 5 é disperso
5. **Independente:** Cada KR pode ser atingido sem depender dos outros

---

## 3. Bloco: OKR Tracking (Status)

### Template Semanal
```markdown
## OKR Status — Semana [N] / [Quarter]

| Objective | KR | Target | Atual | % | Confiança | Nota |
|-----------|-----|--------|-------|:---:|:---------:|------|
| O1: [Título] | KR1: [Desc.] | [Target] | [Atual] | [X%] | [Alta/Média/Baixa] | [Contexto] |
| | KR2: [Desc.] | [Target] | [Atual] | [X%] | [Confiança] | [Nota] |
| O2: [Título] | KR1: [Desc.] | [Target] | [Atual] | [X%] | [Confiança] | [Nota] |
| | KR2: [Desc.] | [Target] | [Atual] | [X%] | [Confiança] | [Nota] |

**Legenda de confiança:**
- Alta: Vamos atingir no ritmo atual
- Média: Possível, mas precisa de atenção/ação
- Baixa: Improvável sem mudança significativa de plano
```

### Template de Mid-Quarter Review
```markdown
## Mid-Quarter OKR Review — [Quarter]

### O que Está Funcionando
- [OKR/KR que está on track e por quê]
- [Prática ou decisão que está gerando resultado]

### O que Precisa de Atenção
- [OKR/KR at risk — causa e ação necessária]
- [Bloqueio que precisa ser removido]

### Ajustes Propostos
| OKR | Ajuste | Justificativa | Impacto |
|-----|--------|-------------|---------|
| [KR X] | [Alterar target de Y para Z] | [Por que mudou o contexto] | [Baixo — reflete realidade] |
| [O2] | [Adicionar KR sobre W] | [Novo insight do mercado] | [Médio — foca esforço] |
```

---

## 4. Bloco: OKR Scoring (End of Quarter)

### Template
```markdown
## OKR Scoring — [Quarter]

| Objective | KR | Target | Resultado | Score | Análise |
|-----------|-----|--------|-----------|:-----:|---------|
| O1: [Título] | KR1 | [Target] | [Resultado real] | [0.0-1.0] | [O que aprendemos] |
| | KR2 | [Target] | [Resultado] | [Score] | [Análise] |
| | **O1 Score** | | | **[Média]** | |
| O2: [Título] | KR1 | [Target] | [Resultado] | [Score] | [Análise] |
| | KR2 | [Target] | [Resultado] | [Score] | [Análise] |
| | **O2 Score** | | | **[Média]** | |

**Score geral do período:** [X.X]

### Interpretação de Score
| Score | Significado |
|:-----:|-----------|
| 0.0-0.3 | Falha significativa — investigar causa |
| 0.4-0.6 | Progresso, mas abaixo do esperado |
| 0.7-0.8 | Sweet spot para OKRs aspiracionais |
| 0.9-1.0 | Atingido — o target era ambicioso o suficiente? |

### Reflexão
- **O que deu certo e queremos repetir:** [Insights]
- **O que não funcionou e como ajustar:** [Aprendizados]
- **OKRs que devem continuar no próximo quarter:** [Quais e por quê]
```

---

## 5. Bloco: Alinhamento de OKRs (Cascata)

### Template
```markdown
## Alinhamento de OKRs — [Quarter]

### Empresa
- **O1:** [Objective da empresa]
  - KR1: [Key Result]

### ↓ Times que contribuem

| Time | Seu Objective | KR que Contribui | Conexão |
|------|-------------|------------------|---------|
| Eng | [Objective do time] | [KR: Métrica → Target] | [Contribui para KR1 da empresa] |
| Sales | [Objective] | [KR] | [Contribui para KR1] |
| Product | [Objective] | [KR] | [Contribui para KR1] |
```

---

## 6. Bloco: OKR para Board

### Template
```markdown
## Progresso dos OKRs — [Quarter]

| # | Objective | Score Parcial | Status | Comentário Executivo |
|---|-----------|:---:|:---:|---------------------|
| O1 | [Título curto] | [X.X] | [On Track / At Risk / Off Track] | [1 frase de contexto] |
| O2 | [Título curto] | [X.X] | [Status] | [Contexto] |
| O3 | [Título curto] | [X.X] | [Status] | [Contexto] |
```

---

## 7. Anti-Padrões de OKR

```markdown
## O que NÃO Fazer com OKRs

| Anti-padrão | Exemplo | Correção |
|-------------|---------|----------|
| KR como tarefa | "Enviar 50 emails" | "Gerar 20 SQLs via outbound" |
| Objective com número | "Crescer 30%" | "Dominar o segmento enterprise" |
| Muitos OKRs | 8 objectives com 25 KRs | Máximo 4 objectives com 12-15 KRs |
| OKR sandbag (fácil demais) | Score de 1.0 todo quarter | Se sempre atinge, está fácil demais |
| OKR como meta de performance | Bônus atrelado a OKR score | OKRs são para aprendizado e direção |
| KR sem baseline | "Melhorar NPS" | "Aumentar NPS de 32 para 50" |
| KR não medível | "Melhorar qualidade do código" | "Reduzir bugs em prod de 10/mês para 3/mês" |
```

---

## Exemplos Completos

### OKR de Produto
```markdown
## Objective: Entregar uma experiência de onboarding que encanta novos usuários

- KR1: Aumentar taxa de ativação em 7 dias de 45% para 65%
- KR2: Reduzir tempo médio de onboarding de 3 dias para 4 horas
- KR3: Atingir NPS de onboarding > 50 (atual: 28)

Owner: VP Product | Período: Q1 2026 | Tipo: Committed
```

---

## Dicas de Uso
- OKRs são DIREÇÃO, não contrato — é ok ajustar se o contexto mudar
- Score de 0.7 em OKR aspiracional é excelente — não punam
- Check-in semanal de 5 min por OKR — mais que isso é overhead
- Se ninguém olha os OKRs entre check-ins, eles estão errados
- Comece com poucos e simples — sofisticação vem com prática
- OKRs sem alinhamento vertical são silos disfarçados
