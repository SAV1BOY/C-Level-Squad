# Risk Scoring — Metodologia Completa de Avaliação de Riscos

> Referência do C-Level Squad para identificação, quantificação e gestão de riscos.
> Uso: todos os agentes, especialmente COO (operacional), CTO (técnico), CIO (informação), CAIO (AI).

---

## 1. Fundamentos

### Fórmula base

```
Risk Score = Probabilidade × Impacto
```

Variações avançadas:
```
Risk Score Ajustado = Probabilidade × Impacto × Detectabilidade⁻¹
Risk Score Ponderado = (Probabilidade × Impacto) × Peso Estratégico
Residual Risk = Risk Score × (1 - Eficácia da Mitigação)
```

### Tipos de risco no contexto C-Level

| Categoria        | Descrição                                           | Agente primário |
|-----------------|-----------------------------------------------------|-----------------|
| Estratégico     | Riscos ao modelo de negócio, mercado, competição    | CEO             |
| Operacional     | Riscos a processos, execução, supply chain          | COO             |
| Tecnológico     | Riscos a sistemas, infraestrutura, segurança        | CTO             |
| Informacional   | Riscos a dados, privacidade, compliance             | CIO             |
| AI/ML           | Riscos de modelos, viés, alucinação, dependência    | CAIO            |
| Mercado/Growth  | Riscos de aquisição, retenção, brand                | CMO             |
| Financeiro      | Riscos de caixa, unit economics, funding            | CEO/COO         |
| Regulatório     | Riscos de compliance, mudanças legais               | CIO/CEO         |
| Pessoas         | Riscos de turnover, cultura, key-person dependency  | COO             |

---

## 2. Matriz de Probabilidade × Impacto (5×5)

### Escala de Probabilidade

| Score | Nível        | Descrição                                    | Frequência esperada        |
|-------|-------------|----------------------------------------------|---------------------------|
| 1     | Raro        | Pode acontecer apenas em circunstâncias excepcionais | <5% de chance em 12 meses |
| 2     | Improvável  | Pode acontecer mas não é esperado             | 5-20% de chance em 12 meses |
| 3     | Possível    | Pode acontecer em algum momento               | 20-50% de chance em 12 meses |
| 4     | Provável    | Vai provavelmente acontecer                    | 50-80% de chance em 12 meses |
| 5     | Quase certo | Esperado que aconteça, pode já estar acontecendo | >80% de chance em 12 meses |

### Escala de Impacto

| Score | Nível         | Financeiro              | Operacional                    | Reputacional                  |
|-------|--------------|-------------------------|-------------------------------|-------------------------------|
| 1     | Insignificante | <R$50K ou <1% da receita | Inconveniência menor, <1h downtime | Sem impacto externo           |
| 2     | Menor        | R$50K-500K ou 1-5% receita | Degradação de serviço, <4h    | Reclamações isoladas          |
| 3     | Moderado     | R$500K-2M ou 5-15% receita | Interrupção parcial, <24h     | Cobertura mídia negativa local |
| 4     | Significativo | R$2M-10M ou 15-30% receita | Interrupção total, <72h       | Cobertura mídia nacional       |
| 5     | Catastrófico | >R$10M ou >30% receita    | Interrupção prolongada, >72h  | Dano duradouro à marca         |

### Matriz visual (Heat Map)

```
               I M P A C T O
               1    2    3    4    5
          ┌────┬────┬────┬────┬────┐
     5    │ 5  │ 10 │ 15 │ 20 │ 25 │  ← Quase certo
P    4    │ 4  │ 8  │ 12 │ 16 │ 20 │  ← Provável
R    3    │ 3  │ 6  │ 9  │ 12 │ 15 │  ← Possível
O    2    │ 2  │ 4  │ 6  │ 8  │ 10 │  ← Improvável
B    1    │ 1  │ 2  │ 3  │ 4  │ 5  │  ← Raro
          └────┴────┴────┴────┴────┘

Legenda de cores:
🟢 Verde  (1-4):   Risco BAIXO    — Monitorar, revisar trimestralmente
🟡 Amarelo (5-9):  Risco MÉDIO    — Plano de mitigação necessário, revisar mensalmente
🟠 Laranja (10-15): Risco ALTO    — Ação imediata de mitigação, revisar semanalmente
🔴 Vermelho (16-25): Risco CRÍTICO — Escalação executiva, ação emergencial
```

---

## 3. Abordagem qualitativa

### Quando usar
- Riscos emergentes sem dados históricos
- Riscos reputacionais difíceis de quantificar
- Fase inicial de identificação de riscos (triagem rápida)
- Workshops de risco com stakeholders mistos

### Processo qualitativo

1. **Brainstorm de riscos:** Sessão estruturada com cada agente listando riscos da sua área
2. **Categorização:** Agrupar por tipo (ver tabela da Seção 1)
3. **Avaliação individual:** Cada participante avalia P×I independentemente
4. **Discussão de divergências:** Focar nos riscos onde as avaliações divergem >2 pontos
5. **Consenso:** Acordar score final para cada risco
6. **Documentação:** Registrar premissas e razões para cada avaliação

### Técnicas de elicitação
- **Pre-mortem:** "Imagine que falhamos completamente. O que aconteceu?" (Gary Klein)
- **Red team:** Designar alguém para argumentar contra a posição do grupo
- **Cenários:** "Se [evento extremo] acontecesse, qual seria o impacto?"
- **Analogias históricas:** "Quando algo similar aconteceu em [empresa/indústria], o resultado foi..."

---

## 4. Abordagem quantitativa

### Quando usar
- Riscos financeiros com dados históricos disponíveis
- Riscos operacionais com métricas de frequência
- Decisões de investimento significativo (>R$1M)
- Requisitos regulatórios de quantificação

### Métodos quantitativos

#### 4.1 Expected Monetary Value (EMV)

```
EMV = Σ (Probabilidade_i × Impacto_financeiro_i) para cada cenário i
```

**Exemplo:**
| Cenário         | Probabilidade | Impacto financeiro | EMV          |
|----------------|---------------|-------------------|--------------|
| Melhor caso    | 20%           | +R$5M             | +R$1.0M      |
| Caso base      | 50%           | +R$1M             | +R$0.5M      |
| Pior caso      | 25%           | -R$3M             | -R$0.75M     |
| Catastrófico   | 5%            | -R$10M            | -R$0.5M      |
| **EMV Total**  |               |                   | **+R$0.25M** |

#### 4.2 Monte Carlo simplificado

Para decisões complexas com múltiplas variáveis de risco:

```
1. Definir distribuição para cada variável (triangular: min, mais provável, max)
2. Simular N=1000 cenários aleatórios
3. Analisar distribuição dos resultados
4. Reportar: P10, P50, P90 (percentis 10, 50 e 90)

Exemplo de output:
- P10 (pessimista): Prejuízo de R$2M
- P50 (mediana): Lucro de R$500K
- P90 (otimista): Lucro de R$4M
- Probabilidade de resultado negativo: 35%
```

#### 4.3 Value at Risk (VaR) simplificado

```
VaR(95%) = Perda máxima esperada com 95% de confiança em [período]

Exemplo: VaR(95%, 1 quarter) = R$3M
Interpretação: "Com 95% de confiança, não perderemos mais que R$3M no próximo trimestre"
```

---

## 5. Risk Appetite — Definição de apetite a risco

### Framework de apetite

| Dimensão          | Avesso (Conservative) | Moderado            | Agressivo (Risk-seeking) |
|-------------------|----------------------|---------------------|--------------------------|
| Financeiro        | Max loss: 5% receita | Max loss: 15% receita | Max loss: 30% receita    |
| Operacional       | Zero downtime planejado | <4h downtime/quarter | <24h downtime/quarter    |
| Reputacional      | Zero controvérsia     | Controvérsia menor OK | Controvérsia estratégica OK |
| Regulatório       | 100% compliance       | 100% compliance       | 100% compliance (sempre) |
| Inovação/AI       | Apenas proven tech     | Early majority        | Bleeding edge OK          |

### Como definir o apetite do C-Level Squad

O CEO (Vision Chief) define o apetite geral, com input dos outros agentes:

```markdown
## Declaração de Risk Appetite — [Período]

O C-Level Squad opera com apetite de risco [MODERADO] para o período [Q1-2026].

Exceções:
- Risco regulatório: SEMPRE avesso (zero tolerance)
- Risco de inovação AI: AGRESSIVO (competir por vantagem)
- Risco financeiro: MODERADO (max 15% da receita em risco)
- Risco operacional: MODERADO (SLA de 99.5%)
- Risco reputacional: AVESSO (proteger marca)

Aprovado por: [CEO / Vision Chief]
Data: [YYYY-MM-DD]
Revisão: Trimestral
```

---

## 6. Risk Tolerance Thresholds — Limites de tolerância

### Definição de thresholds por score

| Risk Score | Nível    | Tolerância                                           | Ação requerida                         |
|-----------|----------|------------------------------------------------------|----------------------------------------|
| 1-4       | Baixo    | **Aceitar** — dentro do apetite                      | Monitorar, revisar em 90 dias          |
| 5-9       | Médio    | **Mitigar** — necessário plano de ação               | Plano de mitigação em 14 dias          |
| 10-15     | Alto     | **Escalar** — requer atenção executiva               | Revisão semanal, mitigação em 7 dias   |
| 16-25     | Crítico  | **Agir imediatamente** — potencialmente existencial  | War room em 24h, CEO informado         |

### Regras de escalação

```
Risco Baixo (1-4):
  → Owner: Agente da área
  → Report: Mensal no risk register
  → Aprovação: Nenhuma necessária

Risco Médio (5-9):
  → Owner: Agente da área + 1 agente de suporte
  → Report: Quinzenal com status de mitigação
  → Aprovação: Agente líder da área

Risco Alto (10-15):
  → Owner: 2 agentes designados
  → Report: Semanal com dashboard
  → Aprovação: CEO para plano de mitigação
  → Budget: Até 5% do orçamento trimestral sem aprovação adicional

Risco Crítico (16-25):
  → Owner: CEO + agente da área
  → Report: Diário até reduzir a Alto ou Médio
  → Aprovação: Todos os agentes informados
  → Budget: Sem limite pré-definido — prioridade máxima
```

---

## 7. Rubrica de Scoring — Guia detalhado

### Passo 1: Identificar o risco

```
Template de descrição:
"Existe o risco de que [EVENTO] ocorra devido a [CAUSA],
resultando em [CONSEQUÊNCIA] para [ÁREA AFETADA]."

Exemplo:
"Existe o risco de que uma violação de dados ocorra devido a
vulnerabilidade na API de parceiros, resultando em exposição de
dados de clientes para a área de Compliance e Reputação."
```

### Passo 2: Avaliar Probabilidade

Perguntas-guia:
- Isso já aconteceu antes na nossa organização? (Se sim, P ≥ 3)
- Isso já aconteceu em organizações similares? (Se sim, P ≥ 2)
- Existem controles preventivos em vigor? (Se não, P +1)
- O ambiente externo está mudando de forma relevante? (Se sim, P +1)
- Há dependência de terceiros? (Se sim, P +1)

### Passo 3: Avaliar Impacto

Perguntas-guia:
- Qual o impacto financeiro direto? (Usar escala da Seção 2)
- Quantos clientes seriam afetados? (<100: I=1-2, 100-1000: I=3, >1000: I=4-5)
- Há impacto regulatório? (Se sim, I ≥ 3)
- Há impacto em outros sistemas/processos (cascata)? (Se sim, I +1)
- É reversível em <24h? (Se não, I +1)

### Passo 4: Calcular e classificar

```
Risk Score = P × I
Classificar conforme Seção 6
Atribuir owner conforme regras de escalação
```

---

## 8. Método de agregação

### Risk Register — formato

```markdown
| ID    | Descrição                    | Cat.  | P | I | Score | Nível   | Owner | Mitigação          | Status    | Próx. Revisão |
|-------|------------------------------|-------|---|---|-------|---------|-------|--------------------|-----------|---------------|
| R-001 | Violação de dados via API    | Tech  | 3 | 5 | 15    | Alto    | CTO   | WAF + pen test     | Em andamento | 2026-03-25  |
| R-002 | Churn acima de 8% mensal     | Ops   | 4 | 4 | 16    | Crítico | COO   | Retention program  | Planejado | 2026-03-18    |
| R-003 | Modelo AI com viés detectado | AI    | 2 | 4 | 8     | Médio   | CAIO  | Audit framework    | Monitorando | 2026-04-01  |
```

### Métricas agregadas de risco

| Métrica                    | Fórmula                                      | Target          |
|---------------------------|----------------------------------------------|-----------------|
| Total Risk Exposure       | Σ (todos os Risk Scores)                     | < threshold por área |
| Average Risk Score        | Σ Scores / N riscos                          | < 8              |
| % Riscos Críticos         | N(Score ≥16) / N total                       | < 5%             |
| % Riscos com mitigação    | N(com plano ativo) / N(Score ≥5)             | > 90%            |
| Risk Velocity             | Δ Total Risk Exposure vs. período anterior    | Tendência de queda |
| Overdue mitigations       | N(mitigação atrasada)                         | 0                |

---

## 9. Visualização — Heat Map

### Formato para reporting executivo

```
HEAT MAP DE RISCOS — [Período]

               IMPACTO →
         1     2     3     4     5
    ┌─────┬─────┬─────┬─────┬─────┐
 5  │     │     │     │R-005│     │  P
    ├─────┼─────┼─────┼─────┼─────┤  R
 4  │     │     │R-004│     │R-002│  O
    ├─────┼─────┼─────┼─────┼─────┤  B
 3  │     │     │     │R-006│R-001│  A
    ├─────┼─────┼─────┼─────┼─────┤  B
 2  │     │R-007│     │R-003│     │  I
    ├─────┼─────┼─────┼─────┼─────┤  L
 1  │R-008│     │     │     │     │  I
    └─────┴─────┴─────┴─────┴─────┘  D
                                      A
                                      D
                                      E

Legenda: ■ Crítico (16-25)  ■ Alto (10-15)  ■ Médio (5-9)  ■ Baixo (1-4)

Total de riscos: 8
Críticos: 1 (R-002)
Altos: 2 (R-001, R-005)
Com mitigação ativa: 6/8 (75%)
```

---

## 10. Regras de owner assignment

| Categoria de risco | Owner primário | Owner backup | Escalação       |
|-------------------|---------------|--------------|-----------------|
| Estratégico       | CEO           | COO          | Board/Conselho  |
| Operacional       | COO           | CTO          | CEO             |
| Tecnológico       | CTO           | CIO          | CEO             |
| Informacional     | CIO           | CTO          | CEO             |
| AI/ML             | CAIO          | CTO          | CEO             |
| Mercado           | CMO           | CEO          | CEO             |
| Financeiro        | CEO           | COO          | Board/Conselho  |
| Regulatório       | CIO           | CEO          | Board/Conselho  |
| Pessoas           | COO           | CEO          | CEO             |

### Responsabilidades do Risk Owner

1. Manter a avaliação de P×I atualizada (mínimo mensal)
2. Desenvolver e executar plano de mitigação para riscos ≥ Médio
3. Reportar status no cadence definido pela classificação
4. Escalar imediatamente se o risco mudar de nível
5. Conduzir post-mortem se o risco se materializar
6. Propor remoção do registro quando o risco for eliminado ou aceito formalmente

---

## 11. Template de risk assessment completo

```markdown
## Risk Assessment — [Iniciativa/Decisão]

**Data:** [YYYY-MM-DD]
**Assessor:** [Agente]
**Contexto:** [Breve descrição da decisão ou iniciativa]

### Riscos identificados

#### R-XXX: [Nome do risco]
- **Descrição:** [Evento + causa + consequência]
- **Categoria:** [Estratégico/Operacional/Tech/etc.]
- **Probabilidade:** [1-5] — Justificativa: [razão]
- **Impacto:** [1-5] — Justificativa: [razão]
- **Risk Score:** [P×I]
- **Classificação:** [Baixo/Médio/Alto/Crítico]
- **Mitigação proposta:** [ação]
- **Risco residual após mitigação:** [novo P×I estimado]
- **Owner:** [Agente]
- **Timeline de mitigação:** [data]
- **Trigger de monitoramento:** [métrica ou evento que indica materialização]

### Sumário
- Total de riscos: [N]
- Riscos críticos: [N]
- Riscos sem mitigação: [N]
- Risk exposure total: [soma dos scores]
- Recomendação: [GO / GO com mitigação / NO-GO]
```
