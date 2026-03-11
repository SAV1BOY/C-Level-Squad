# Certainty Scale — Escala de Certeza na Comunicação

## Princípio Central

Calibrar a linguagem de certeza é uma habilidade executiva crítica. Dizer "sabemos"
quando na verdade "acreditamos" cria falsa confiança. Dizer "talvez" quando temos
dados sólidos enfraquece decisões. A precisão na linguagem de certeza é a base da
confiança organizacional.

---

## A Escala de 5 Níveis

### Nível 1: SABEMOS (95%+ de confiança)
**Definição:** Fato verificável com dados robustos e múltiplas fontes.
**Base:** Dados históricos, métricas em produção, resultados medidos.

**Quando usar:**
- Dados de sistemas em produção
- Resultados financeiros auditados
- Métricas com 6+ meses de histórico
- Fatos legais ou regulatórios

**Exemplos:**
- "Sabemos que nosso churn é 5% ao mês — dados dos últimos 12 meses, verificados por finance."
- "Sabemos que o deployment leva 23 minutos — medido em 500+ deploys."
- "Sabemos que o NPS é 72 — pesquisa com 2.000 respondentes, margem de erro 2%."

**Linguagem permitida:**
- "Os dados confirmam que..."
- "É fato que..."
- "Temos certeza de que..."
- "Os resultados mostram que..."

---

### Nível 2: ESTAMOS CONFIANTES (80-95% de confiança)
**Definição:** Forte evidência, mas com alguma incerteza ou variáveis não controladas.
**Base:** Dados sólidos mas com range, tendências consistentes, múltiplos indicadores alinhados.

**Quando usar:**
- Tendências com 3-6 meses de dados
- Resultados de pilotos com amostra razoável
- Análises com múltiplas variáveis convergindo
- Feedback consistente de múltiplas fontes

**Exemplos:**
- "Estamos confiantes que o novo onboarding reduz churn — piloto com 200 clientes mostra 30% de melhoria."
- "Forte indicação que o mercado LATAM é viável — 50 entrevistas com prospects, 70% com intenção de compra."
- "Os indicadores apontam consistentemente para crescimento de 25-35% no próximo quarter."

**Linguagem permitida:**
- "Estamos confiantes que..."
- "A evidência é forte de que..."
- "Com alta probabilidade..."
- "Os indicadores convergem para..."

---

### Nível 3: ACREDITAMOS (60-80% de confiança)
**Definição:** Evidência parcial suporta a afirmação, mas existem gaps significativos.
**Base:** Dados iniciais, analogias de mercado, expert opinions alinhadas.

**Quando usar:**
- Resultados de testes com amostra pequena
- Análise de mercado com dados limitados
- Correlações ainda não validadas como causais
- Estimativas baseadas em analogias

**Exemplos:**
- "Acreditamos que AI chatbot pode resolver 40% dos tickets — baseado em benchmark de empresas similares e teste interno de 2 semanas."
- "Nossa visão é que o pricing precisa subir 20% — baseado em análise de willingness-to-pay com 30 clientes."
- "Acreditamos que a contratação de 5 AEs gera $500K em pipeline adicional — baseado na produtividade dos AEs atuais."

**Linguagem permitida:**
- "Acreditamos que..."
- "Nossa avaliação é que..."
- "Com base na evidência disponível..."
- "A análise preliminar sugere..."

---

### Nível 4: HIPÓTESE (40-60% de confiança)
**Definição:** Ideia fundamentada que precisa de validação. Pode estar certa ou errada.
**Base:** Lógica de primeiro princípio, dados anecdóticos, intuição informada.

**Quando usar:**
- Novos mercados sem dados diretos
- Mudanças de modelo de negócio
- Inovações de produto sem precedente direto
- Early signals que podem ou não confirmar

**Exemplos:**
- "Nossa hipótese é que vertical SaaS para saúde tem TAM de $500M — baseado em projeção top-down. Precisamos de validação bottom-up."
- "Testamos a hipótese de que pricing por uso converte melhor que subscription — experimento de 30 dias começa segunda."
- "A hipótese é que self-serve reduz CAC em 50% — vamos validar com 1.000 leads no funnel novo."

**Linguagem permitida:**
- "Nossa hipótese é..."
- "Estamos testando se..."
- "O racional sugere que... mas precisamos validar."
- "Se nossa hipótese estiver correta..."

---

### Nível 5: ESPECULAÇÃO (<40% de confiança)
**Definição:** Opinião informada sem dados que a suportem. Pode ser útil para exploração.
**Base:** Visão de futuro, analogias distantes, gut feeling de experts.

**Quando usar:**
- Previsões de longo prazo (3+ anos)
- Impacto de tecnologias emergentes
- Mudanças regulatórias potenciais
- Movimentos competitivos desconhecidos

**Exemplos:**
- "Especulamos que em 3 anos, AI agents substituirão 50% do customer support tier 1 — mas é uma projeção sem dados diretos."
- "É possível que o regulador mude as regras de dados em 2027 — não temos indicação formal, mas o ambiente político sugere isso."
- "Existe a possibilidade de que nosso maior competidor lance produto concorrente — sem intel confirmado."

**Linguagem permitida:**
- "Especulamos que..."
- "É possível que..."
- "Sem dados confirmatórios, nossa intuição é..."
- "No cenário especulativo..."
- "Se [premissa não validada], então..."

---

## Regras de Calibração

### Regra 1: Declare o Nível Explicitamente
Não deixe o receptor adivinhar seu nível de certeza. Seja explícito.

- **Errado:** "O mercado vai crescer 30%." (Sabemos? Acreditamos? Especulamos?)
- **Certo:** "Acreditamos que o mercado cresce 30%, baseado em dados do Gartner e tendência dos últimos 3 anos."

### Regra 2: Cite a Fonte da Certeza
O nível de certeza é tão forte quanto a fonte que o suporta.

| Fonte | Nível típico |
|-------|-------------|
| Dados em produção (6+ meses) | Sabemos |
| Piloto controlado (30+ dias) | Confiantes |
| Pesquisa com amostra razoável | Acreditamos |
| Benchmarks de mercado | Acreditamos → Hipótese |
| Analogia com outra empresa | Hipótese |
| Expert opinion individual | Hipótese → Especulação |
| Gut feeling | Especulação |

### Regra 3: Não Upgrade Certeza sem Dados
É tentador falar com mais convicção para parecer seguro. Resista.

- **Errado:** Apresentar hipótese como certeza para convencer o Board.
- **Certo:** "É uma hipótese. Propomos investir $50K para validar em 30 dias."

### Regra 4: Downgrade é OK
Se novos dados enfraquecem uma certeza anterior, comunique abertamente.

- "Quarter passado dissemos que estávamos confiantes sobre [X]. Novos dados sugerem que é mais uma hipótese. Estamos validando."

### Regra 5: Use Ranges para Incerteza
Quanto menos certeza, mais amplo o range.

| Nível | Range aceitável |
|-------|----------------|
| Sabemos | ±5% — "Revenue: $1.2M ± $60K" |
| Confiantes | ±15% — "Crescimento entre 25% e 35%" |
| Acreditamos | ±30% — "TAM entre $300M e $500M" |
| Hipótese | ±50%+ — "CAC pode ser entre $100 e $200" |
| Especulação | Cenários — "Cenário otimista: X. Pessimista: Y." |

---

## Mapeamento para Decisões

| Nível de Certeza | Tipo de Decisão Apropriada |
|-------------------|---------------------------|
| Sabemos | Investimento significativo, commitment firme, comunicação externa |
| Confiantes | Escalar pilotos, alocar recursos, planejar quarters |
| Acreditamos | Iniciar pilotos, testar com budget limitado, propor ao Board |
| Hipótese | Experimentos pequenos, discovery, pesquisa |
| Especulação | Brainstorms, scenario planning, contingências |

---

## Frases por Nível para Diferentes Contextos

### Em Reunião de Liderança

| Nível | Frase |
|-------|-------|
| Sabemos | "Os dados são claros: [X]. Recomendo ação imediata." |
| Confiantes | "A evidência é forte. Recomendo avançar com [X], monitorando [Y]." |
| Acreditamos | "A análise preliminar suporta [X]. Recomendo piloto antes de escalar." |
| Hipótese | "Temos uma hipótese sobre [X]. Proponho teste de [Y] semanas antes de decidir." |
| Especulação | "Não temos dados, mas vale considerar [X]. Vamos incluir no scenario planning." |

### Em Board Meeting

| Nível | Frase |
|-------|-------|
| Sabemos | "Resultado confirmado: [X]. Base: [dados]." |
| Confiantes | "Forte indicação de [X]. Confidence level: alto." |
| Acreditamos | "Nossa avaliação é [X], baseada em [dados limitados]. Validando com [plano]." |
| Hipótese | "Estamos testando a hipótese de [X]. Resultados em [prazo]." |
| Especulação | "Para efeito de planejamento, consideramos o cenário de [X]." |

---

## Checklist de Calibração de Certeza

- [ ] O nível de certeza está explícito na comunicação?
- [ ] A fonte da certeza está citada?
- [ ] O nível é honesto (não inflado para persuadir)?
- [ ] Ranges foram usados quando há incerteza?
- [ ] A decisão proposta é proporcional ao nível de certeza?
- [ ] O plano para aumentar certeza está definido (se necessário)?
- [ ] A audiência entende a diferença entre os níveis?
- [ ] Mudanças de nível em relação a comunicações anteriores estão explicadas?
