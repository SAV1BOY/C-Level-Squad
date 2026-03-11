# Certainty Scale — Escala de Linguagem de Certeza

## Princípio Central

A precisão da linguagem de certeza é fundamental para decisões corretas. Usar "sabemos"
quando na verdade "acreditamos" leva a overconfidence. Usar "talvez" quando na verdade
"sabemos" leva a paralisia. Calibrar a linguagem de certeza é disciplina executiva essencial.

---

## A Escala de 5 Níveis

### Nível 5: SABEMOS (Confiança 95%+)

**Definição:** Temos dados robustos, verificáveis e replicáveis que suportam a afirmação.

**Quando usar:**
- Dados históricos consistentes por 3+ períodos
- Resultados de experimentos controlados
- Fatos verificáveis e auditáveis
- Métricas com tracking confiável

**Linguagem:**
- "Sabemos que..."
- "Os dados confirmam que..."
- "É fato que..."
- "Verificamos que..."
- "O resultado é..."

**Exemplo:**
> "Sabemos que enterprise churn caiu de 8% para 5% nos últimos 3 quarters, correlacionado
> com a implementação de CS dedicado. Dados de 150 contas enterprise confirmam."

**Regra:** Nunca use "sabemos" sem poder apontar para dados específicos.

---

### Nível 4: ESTAMOS CONFIANTES (Confiança 80-95%)

**Definição:** Temos forte evidência, mas há alguma incerteza residual — amostra menor,
variáveis não controladas, ou período de observação curto.

**Quando usar:**
- Dados de 1-2 períodos consistentes
- Análises com variáveis de confusão controladas parcialmente
- Forte sinal qualitativo confirmado por dados quantitativos iniciais
- Benchmarks de mercado corroborados por dados internos

**Linguagem:**
- "Estamos confiantes que..."
- "A evidência indica fortemente que..."
- "Com alta probabilidade..."
- "Baseado em [dados], é muito provável que..."
- "Temos forte indicação de que..."

**Exemplo:**
> "Estamos confiantes que o novo pricing aumenta ACV em 15-25%, baseado em teste com
> 50 deals no último quarter. A amostra é sólida mas o período é curto."

**Regra:** Sempre mencione a base da confiança e o que falta para subir para "sabemos."

---

### Nível 3: ACREDITAMOS (Confiança 60-80%)

**Definição:** Temos evidência parcial que suporta a afirmação. Hipótese forte, mas
precisa de mais dados para confirmar.

**Quando usar:**
- Dados iniciais de piloto ou experimento early-stage
- Feedback qualitativo consistente sem validação quantitativa robusta
- Analogias com outros mercados/empresas
- Análise lógica com premissas razoáveis

**Linguagem:**
- "Acreditamos que..."
- "Nossa avaliação é que..."
- "A evidência parcial sugere que..."
- "Baseado no que sabemos até agora..."
- "Nosso melhor entendimento é que..."

**Exemplo:**
> "Acreditamos que o mercado LATAM está pronto para nosso produto, baseado em
> 20 entrevistas com prospects e 5 deals em pipeline. Precisamos de 2 quarters
> de dados de vendas para confirmar."

**Regra:** Sempre declare o que precisa acontecer para mover para "confiantes" ou "sabemos."

---

### Nível 2: HIPÓTESE (Confiança 40-60%)

**Definição:** Temos uma teoria informada, mas a evidência é limitada. O próximo passo
é testar, não agir em escala.

**Quando usar:**
- Insights de poucos data points (< 10)
- Analogias fracas com outros contextos
- Intuição informada por experiência
- Análise de mercado sem validação local

**Linguagem:**
- "Nossa hipótese é que..."
- "Suspeitamos que..."
- "É possível que..."
- "A teoria é que..."
- "Precisamos testar se..."

**Exemplo:**
> "Nossa hipótese é que short-form video converte melhor que blog para ICP SMB.
> Baseado em: tendência de mercado e 3 data points de conteúdo nosso.
> Teste planejado: 30 dias, $10K, com control group."

**Regra:** Nunca aja em escala com base em hipótese. Desenhe o experimento primeiro.

---

### Nível 1: ESPECULAÇÃO (Confiança < 40%)

**Definição:** Temos pouca ou nenhuma evidência. É opinião informada, gut feeling, ou
extrapolação de cenários distantes.

**Quando usar:**
- Previsões de longo prazo (3+ anos)
- Mercados que não conhecemos
- Tecnologias emergentes sem track record
- Cenários "what if"

**Linguagem:**
- "Especulamos que..."
- "É possível, mas sem evidência, que..."
- "Um cenário é que..."
- "Se [premissa não validada], então..."
- "Pura intuição: ..."

**Exemplo:**
> "Especulamos que AI agents vão substituir 50% do customer support tier 1 em 3 anos.
> Base: tendência de mercado e capability atual de LLMs. Evidência direta: zero.
> Não recomendo apostar estratégia nisso — mas recomendo monitorar e experimentar."

**Regra:** Especulação é legítima, mas deve ser rotulada como tal. Nunca passe especulação como crença ou fato.

---

## Tabela de Referência Rápida

| Nível | Palavra-Chave | Confiança | Base | Ação Apropriada |
|-------|---------------|-----------|------|-----------------|
| 5 | Sabemos | 95%+ | Dados robustos | Agir com escala |
| 4 | Confiantes | 80-95% | Forte evidência | Agir com monitoramento |
| 3 | Acreditamos | 60-80% | Evidência parcial | Agir com cautela, expandir dados |
| 2 | Hipótese | 40-60% | Evidência limitada | Testar antes de agir |
| 1 | Especulação | <40% | Pouca/nenhuma evidência | Monitorar, não agir |

---

## Regras de Calibração

### Regra 1: Declare o Nível Explicitamente
- **Ruim:** "O mercado vai crescer 40%."
- **Bom:** "Acreditamos que o mercado vai crescer 30-50%, baseado em reports de [fonte] e nossos dados de pipeline."

### Regra 2: Mostre a Base
- **Ruim:** "Estamos confiantes no novo produto."
- **Bom:** "Estamos confiantes no novo produto: NPS de beta users é 72, 8 de 10 converteram para paid, ACV 20% acima do target."

### Regra 3: Declare o que Muda o Nível
- **Ruim:** "Acreditamos que isso vai funcionar."
- **Bom:** "Acreditamos que isso vai funcionar. Para ter confiança, precisamos de 90 dias de dados de produção com n > 500."

### Regra 4: Não Inflacione Certeza
- **Ruim:** "Sabemos que AI vai transformar nossa indústria." (Isso é especulação, não fato.)
- **Bom:** "Acreditamos que AI vai impactar significativamente nossa indústria nos próximos 3 anos, baseado em adoption rates e capability improvements."

### Regra 5: Não Deflacione Certeza
- **Ruim:** "Talvez devêssemos considerar que churn está subindo." (Os dados mostram claramente.)
- **Bom:** "Sabemos que churn subiu de 3% para 5% nos últimos 2 quarters. Os dados são inequívocos."

---

## Aplicação em Decisões

### Decisão com "Sabemos"
> "Sabemos que enterprise conversion cai 30% quando sales cycle > 90 dias.
> Decisão: implementar fast-track process para deals > $100K. Owner: VP Sales. Start: imediato."

### Decisão com "Acreditamos"
> "Acreditamos que self-serve onboarding reduz time-to-value em 50%.
> Decisão: investir 4 sprints em self-serve. Mas: checkpoint em 6 semanas com dados
> de 100 users antes de expandir."

### Decisão com "Hipótese"
> "Nossa hipótese é que vertical SaaS tem melhor product-market fit que horizontal.
> Decisão: NÃO pivotar. Em vez disso: pilot com 10 clientes vertical por 90 dias.
> Se resultados confirmam, revisamos estratégia."

---

## Calibração em Grupo

### Exercício: Calibration Check
Em reuniões de decisão, o facilitador pede a cada pessoa:

1. "Qual é seu nível de confiança nesta afirmação? (1-5)"
2. "O que precisaríamos ver para aumentar em 1 nível?"
3. "O que nos faria diminuir em 1 nível?"

Isso previne groupthink e garante que a incerteza real da equipe é capturada.

### Sinais de Má Calibração
- Todo mundo diz "sabemos" o tempo todo → overconfidence
- Todo mundo diz "hipótese" o tempo todo → paralisia
- Ninguém discorda do nível proposto → groupthink
- A mesma afirmação muda de nível dependendo da audiência → manipulação

---

## Checklist de Calibração de Certeza

- [ ] O nível de certeza está declarado explicitamente?
- [ ] A base de evidência está citada?
- [ ] O que muda o nível está identificado?
- [ ] A ação é proporcional ao nível de certeza?
- [ ] Há plano para reduzir incerteza quando possível?
- [ ] A linguagem é consistente (não "sabemos" em um lugar e "acreditamos" em outro para a mesma afirmação)?
- [ ] A equipe foi consultada sobre a calibração?
