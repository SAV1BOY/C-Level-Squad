# Risk Assessment Blocks — Blocos Reutilizáveis para Avaliação de Risco

> Blocos padronizados para identificar, avaliar e comunicar riscos em documentos executivos.
> Riscos bem documentados permitem decisões informadas e preparação adequada.

---

## 1. Bloco: Matriz de Riscos

### Template Padrão
```markdown
## Matriz de Riscos

| # | Risco | Categoria | Probabilidade | Impacto | Severidade | Owner | Status |
|---|-------|-----------|:---:|:---:|:---:|-------|--------|
| R1 | [Descrição] | [Cat.] | [A/M/B] | [A/M/B] | [Crítico/Alto/Médio/Baixo] | [Nome] | [Novo/Monitorando/Mitigando/Mitigado] |
| R2 | [Descrição] | [Cat.] | [A/M/B] | [A/M/B] | [Severidade] | [Nome] | [Status] |
```

### Variante: Matriz Visual (Heat Map em Texto)
```markdown
              │ Baixo Impacto │ Médio Impacto │ Alto Impacto │
──────────────┼───────────────┼───────────────┼──────────────┤
Alta Prob.    │   MÉDIO       │   ALTO        │  CRÍTICO     │
              │               │               │  [R1, R3]    │
──────────────┼───────────────┼───────────────┼──────────────┤
Média Prob.   │   BAIXO       │   MÉDIO       │  ALTO        │
              │               │   [R4]        │  [R2]        │
──────────────┼───────────────┼───────────────┼──────────────┤
Baixa Prob.   │   BAIXO       │   BAIXO       │  MÉDIO       │
              │   [R5]        │               │  [R6]        │
──────────────┴───────────────┴───────────────┴──────────────┘
```

---

## 2. Bloco: Risco Detalhado

### Template
```markdown
### Risco: [Título]

| Campo | Detalhes |
|-------|---------|
| **ID** | [R-NNN] |
| **Categoria** | [Estratégico / Operacional / Financeiro / Técnico / Legal / Reputacional / People] |
| **Descrição** | [O que pode acontecer — ser específico] |
| **Causa raiz** | [Por que pode acontecer] |
| **Probabilidade** | [Alta (>60%) / Média (30-60%) / Baixa (<30%)] |
| **Impacto** | [Alto / Médio / Baixo — quantificar quando possível: R$ X, N dias] |
| **Severidade** | [Probabilidade x Impacto] |
| **Trigger/Indicador** | [Sinal que indica que o risco está se materializando] |
| **Mitigação** | [Ação para reduzir probabilidade ou impacto] |
| **Contingência** | [Plano B se o risco se materializar] |
| **Owner** | [Nome — responsável pela mitigação] |
| **Prazo de revisão** | [Quando reavaliar] |
```

---

## 3. Bloco: Análise FMEA (Failure Mode and Effects Analysis)

### Template
```markdown
## FMEA — Análise de Modos de Falha

| Modo de Falha | Efeito | Severidade (1-10) | Probabilidade (1-10) | Detecção (1-10) | RPN | Ação |
|--------------|--------|:-:|:-:|:-:|:-:|------|
| [Como pode falhar] | [Impacto da falha] | [1-10] | [1-10] | [1-10] | [SxPxD] | [Mitigação] |
| [Modo 2] | [Efeito] | [S] | [P] | [D] | [RPN] | [Ação] |

**RPN (Risk Priority Number)** = Severidade x Probabilidade x (in)Detecção
- RPN > 200: Ação imediata obrigatória
- RPN 100-200: Plano de mitigação necessário
- RPN < 100: Monitorar
```

---

## 4. Bloco: Riscos por Categoria

### Template
```markdown
## Panorama de Riscos por Categoria

### Riscos Estratégicos
- [Mudança de mercado / Concorrência / Regulação]

### Riscos Operacionais
- [Processos / Sistemas / Capacidade / Dependências]

### Riscos Financeiros
- [Liquidez / Câmbio / Inadimplência / Custos]

### Riscos de Pessoas
- [Turnover / Key-person dependency / Cultura]

### Riscos Tecnológicos
- [Segurança / Escalabilidade / Dívida técnica / Vendor lock-in]

### Riscos Legais/Regulatórios
- [LGPD / Trabalhista / Tributário / Contratos]

### Riscos Reputacionais
- [Marca / Confiança de clientes / ESG]
```

---

## 5. Bloco: Evolução de Riscos

### Template
```markdown
## Evolução de Riscos (período a período)

| Risco | Q Anterior | Q Atual | Tendência | Comentário |
|-------|:---:|:---:|:---:|------------|
| [Risco 1] | [Médio] | [Alto] | Piorando | [O que mudou] |
| [Risco 2] | [Alto] | [Médio] | Melhorando | [Mitigação funcionou] |
| [Risco 3] | [N/A] | [Alto] | Novo | [Identificado esta semana] |
| [Risco 4] | [Baixo] | [Encerrado] | Resolvido | [O que foi feito] |
```

---

## 6. Bloco: Risk Appetite Statement

### Template
```markdown
## Apetite de Risco

| Categoria | Apetite | Descrição | Limite |
|-----------|---------|-----------|--------|
| Financeiro | [Baixo/Médio/Alto] | [Quanto estamos dispostos a perder] | [R$ X máximo] |
| Técnico | [Baixo/Médio/Alto] | [Quanto downtime aceitamos] | [X horas/trimestre] |
| Reputacional | [Baixo] | [Zero tolerância para incidentes públicos graves] | [N/A] |
| Regulatório | [Muito Baixo] | [Compliance total é obrigatório] | [Zero violações] |
| Inovação | [Alto] | [Aceitamos falhas em projetos experimentais] | [X% do budget para bets] |
```

---

## 7. Bloco: Análise de Impacto

### Template
```markdown
## Análise de Impacto — Cenário: [Descrição]

| Dimensão | Impacto Imediato (0-30 dias) | Impacto Médio Prazo (1-6 meses) | Impacto Longo Prazo (6-12 meses) |
|----------|----------------------------|-------------------------------|-------------------------------|
| Receita | [R$ X / X%] | [R$ X / X%] | [R$ X / X%] |
| Operações | [Descrição] | [Descrição] | [Descrição] |
| Clientes | [N afetados] | [Churn estimado] | [Recuperação] |
| Pessoas | [Descrição] | [Descrição] | [Descrição] |
| Reputação | [Descrição] | [Descrição] | [Descrição] |
```

---

## 8. Bloco: Plano de Contingência

### Template
```markdown
## Plano de Contingência — Risco: [Nome]

**Trigger:** [O que ativa o plano de contingência]

| Passo | Ação | Responsável | Prazo | Recursos |
|-------|------|-------------|-------|----------|
| 1 | [Ação imediata] | [Nome] | [Imediato] | [O que precisa] |
| 2 | [Ação de curto prazo] | [Nome] | [24-48h] | [Recursos] |
| 3 | [Ação de estabilização] | [Nome] | [1 semana] | [Recursos] |
| 4 | [Ação de normalização] | [Nome] | [1 mês] | [Recursos] |

**Custo estimado da contingência:** [R$ X]
**Impacto residual após contingência:** [Descrição do impacto que ainda resta]
```

---

## Exemplos de Uso

### Para Board Deck (compacto)
```markdown
## Top 3 Riscos

| Risco | Severidade | Mitigação | Status |
|-------|:---------:|-----------|--------|
| Churn acima do plan (3.2% vs 2.5%) | Alto | Programa de retenção + CS proativo | Em execução |
| Key engineer saiu (arquiteto do core) | Alto | Documentação + contratação urgente | Contratação em andamento |
| Regulação LGPD para AI features | Médio | Consultoria jurídica + DPO envolvido | Monitorando |
```

---

## Dicas de Uso
- Risco sem owner é risco ignorado — sempre atribua responsável
- Quantifique impacto sempre que possível — "alto impacto" é vago, "R$ 500K de perda" é claro
- Triggers são essenciais — defina indicadores que alertam sobre materialização
- Revise riscos mensalmente no mínimo — cenário muda rápido
- Novos riscos não são falha — é sinal de que você está atento
- Risco mitigado não é risco eliminado — continue monitorando
