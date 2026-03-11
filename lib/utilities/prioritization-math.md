# Prioritization Math — Guia Completo de Frameworks de Priorização

> Referência operacional do C-Level Squad para tomada de decisão baseada em dados.
> Uso: qualquer agente (CEO, COO, CMO, CTO, CIO, CAIO) ao priorizar iniciativas, features, investimentos ou projetos.

---

## 1. RICE — Reach, Impact, Confidence, Effort

### Fórmula

```
RICE Score = (Reach × Impact × Confidence) / Effort
```

### Definição de cada variável

| Variável     | Descrição                                                        | Unidade sugerida          |
|-------------|------------------------------------------------------------------|---------------------------|
| **Reach**   | Quantas pessoas/transações/eventos serão afetados por trimestre  | Número absoluto (ex: 5.000 usuários/quarter) |
| **Impact**  | Quanto cada pessoa afetada será impactada                        | Escala: 3 = massivo, 2 = alto, 1 = médio, 0.5 = baixo, 0.25 = mínimo |
| **Confidence** | Nível de certeza nas estimativas de Reach e Impact            | Percentual: 100% = alta, 80% = média, 50% = baixa |
| **Effort**  | Trabalho necessário em pessoa-mês                                | Pessoa-mês (ex: 2 = dois meses de uma pessoa full-time) |

### Rubrica de Scoring detalhada

**Reach — Como estimar:**
- Usar dados reais de analytics (MAU, DAU, transações)
- Se não houver dados, usar proxy: tamanho do segmento × taxa de exposição esperada
- Sempre definir o período: por trimestre é o padrão recomendado
- Exemplo: "Feature de onboarding alcança 100% dos novos usuários = 3.000/quarter"

**Impact — Calibração:**
- 3 (Massivo): Muda fundamentalmente a experiência. Ex: resolver o #1 motivo de churn
- 2 (Alto): Melhoria significativa e mensurável. Ex: reduzir tempo de setup em 50%
- 1 (Médio): Melhoria notável. Ex: adicionar filtro de busca frequentemente pedido
- 0.5 (Baixo): Melhoria marginal. Ex: ajuste de UI em fluxo secundário
- 0.25 (Mínimo): Quase imperceptível. Ex: correção de typo em tela pouco acessada

**Confidence — Regras:**
- 100%: Dados quantitativos sólidos (A/B test prévio, benchmark validado)
- 80%: Dados qualitativos fortes (pesquisa com N>30, padrão claro de tickets)
- 50%: Intuição informada, sem dados diretos
- Abaixo de 50%: Não use RICE — primeiro invista em descoberta

**Effort — Como calcular:**
- Incluir: design, engenharia, QA, data, marketing (se aplicável)
- Arredondar para cima: 0.5 mês é o mínimo
- Se effort > 6 pessoa-mês, considere quebrar a iniciativa

### Exemplo prático completo

| Iniciativa               | Reach  | Impact | Confidence | Effort | RICE Score |
|--------------------------|--------|--------|------------|--------|------------|
| Novo onboarding guiado   | 3.000  | 2      | 80%        | 3      | 1.600      |
| Dashboard de métricas    | 1.500  | 1      | 50%        | 2      | 375        |
| Integração com Slack     | 800    | 2      | 80%        | 1      | 1.280      |
| Redesign da pricing page | 10.000 | 0.5    | 50%        | 0.5    | 5.000      |

**Decisão:** Redesign da pricing page tem o maior RICE apesar de baixo impacto individual — o reach massivo compensa.

### Template de Spreadsheet

```
| Coluna A: Iniciativa (texto livre)
| Coluna B: Reach (número inteiro, por quarter)
| Coluna C: Impact (3 / 2 / 1 / 0.5 / 0.25)
| Coluna D: Confidence (1.0 / 0.8 / 0.5)
| Coluna E: Effort (pessoa-mês, mínimo 0.5)
| Coluna F: =B*C*D/E (RICE Score)
| Ordenar por Coluna F descendente
```

### Armadilhas comuns
- **Inflação de Reach:** Contar o mesmo usuário múltiplas vezes. Usar unique users
- **Impact sem critério:** Times diferentes calibram diferente. Fazer sessão de calibração conjunta
- **Confidence alta demais:** Viés de otimismo. Regra: se não tem dados, máximo 50%
- **Effort subestimado:** Adicionar buffer de 30% para integrações e dependências externas
- **Comparar categorias diferentes:** RICE de bug fix vs. RICE de nova feature não é comparável diretamente

### Quando usar RICE
- Product backlog com >20 itens
- Decisão entre features para o próximo trimestre
- Quando há debate subjetivo sobre prioridade e precisa de ancoragem numérica

### Quando NÃO usar RICE
- Decisões estratégicas de longo prazo (usar WSJF ou Strategy Blocks)
- Itens de compliance/regulatório (esses são obrigatórios, não priorizáveis)
- Quando confidence geral é <50% para todas as opções (investir em discovery primeiro)

---

## 2. ICE — Impact, Confidence, Ease

### Fórmula

```
ICE Score = Impact × Confidence × Ease
```

Todas as variáveis numa escala de 1-10.

### Rubrica de Scoring

**Impact (1-10):**
- 10: Move a métrica-chave (North Star) em >20%
- 7-9: Move a métrica-chave em 5-20%
- 4-6: Move uma métrica secundária de forma mensurável
- 1-3: Impacto marginal ou indireto

**Confidence (1-10):**
- 10: Validado com A/B test ou dados históricos
- 7-9: Forte evidência qualitativa + dados parciais
- 4-6: Hipótese razoável baseada em benchmarks
- 1-3: Pura intuição

**Ease (1-10):**
- 10: Menos de 1 dia de trabalho, sem dependências
- 7-9: Menos de 1 semana, equipe autônoma
- 4-6: 1-4 semanas, alguma coordenação necessária
- 1-3: Mais de 1 mês, múltiplas dependências

### Exemplo prático

| Iniciativa                | Impact | Confidence | Ease | ICE Score |
|---------------------------|--------|------------|------|-----------|
| CTA mais visível na home  | 6      | 8          | 9    | 432       |
| Novo sistema de referral  | 9      | 5          | 3    | 135       |
| Email drip para trial     | 7      | 7          | 7    | 343       |
| Chatbot de suporte        | 5      | 4          | 4    | 80        |

### Quando usar ICE
- Priorização rápida de experimentos de growth
- Backlog de marketing/growth com muitos itens pequenos
- Quando velocidade de decisão importa mais que precisão

### Diferença fundamental entre ICE e RICE
- ICE não separa "alcance" — isso pode mascarar features que afetam poucos usuários mas com alto impacto
- ICE é mais rápido mas menos granular
- RICE é melhor para product, ICE é melhor para growth experiments

---

## 3. WSJF — Weighted Shortest Job First

### Fórmula (SAFe)

```
WSJF = Cost of Delay / Job Duration

Cost of Delay = User-Business Value + Time Criticality + Risk Reduction/Opportunity Enablement
```

### Rubrica de Scoring (escala Fibonacci: 1, 2, 3, 5, 8, 13, 21)

**User-Business Value:**
- 21: Diretamente gera receita significativa ou evita perda catastrófica
- 13: Forte impacto em retenção ou expansão
- 8: Impacto mensurável em satisfação ou eficiência
- 5: Melhoria moderada em métricas operacionais
- 3: Nice-to-have com algum valor demonstrável
- 1-2: Valor marginal

**Time Criticality:**
- 21: Deadline regulatório ou contratual iminente
- 13: Janela de mercado que fecha em <1 quarter
- 8: Vantagem competitiva se feito antes do concorrente
- 5: Valor diminui com o tempo mas sem deadline hard
- 1-3: Timing não é fator relevante

**Risk Reduction / Opportunity Enablement:**
- 21: Desbloqueia múltiplas iniciativas de alto valor
- 13: Reduz risco existencial ou desbloqueia um stream de receita
- 8: Reduz risco operacional significativo
- 5: Habilita melhorias futuras
- 1-3: Impacto isolado

### Exemplo prático

| Iniciativa         | User Value | Time Crit | Risk/Opp | CoD  | Duration | WSJF |
|--------------------|-----------|-----------|----------|------|----------|------|
| Compliance LGPD    | 8         | 21        | 13       | 42   | 5        | 8.4  |
| Plataforma de API  | 13        | 5         | 21       | 39   | 13       | 3.0  |
| Novo pricing model | 21        | 8         | 5        | 34   | 3        | 11.3 |
| Mobile app v2      | 13        | 3         | 8        | 24   | 21       | 1.1  |

**Decisão:** Novo pricing model primeiro (maior WSJF), depois Compliance LGPD.

### Quando usar WSJF
- Priorização de épicos/features grandes no nível de portfolio
- Quando "custo de atraso" é um fator relevante (janelas de mercado, deadlines)
- Em ambientes SAFe ou que usam lean flow

### Armadilhas
- Estimativas de duration muito imprecisas distorcem todo o cálculo
- Times tendem a inflar Time Criticality para "furar a fila"
- Calibração em grupo é essencial — uma pessoa sozinha enviesará

---

## 4. MoSCoW — Must, Should, Could, Won't

### Definição de cada categoria

| Categoria  | Critério                                                        | % típico do backlog |
|-----------|----------------------------------------------------------------|---------------------|
| **Must**  | Sem isso, a entrega não tem valor / é ilegal / sistema quebra  | 40-60%              |
| **Should**| Importante mas contornável. Dói não ter, mas sobrevive         | 20-30%              |
| **Could** | Desejável. Melhora a experiência mas não é crítico             | 10-20%              |
| **Won't** | Explicitamente fora de escopo para este ciclo                  | Listado para clareza |

### Regras de aplicação
1. **Must** deve ter consequência concreta se não for feito: "Se não fizermos X, Y acontece"
2. **Should** deve ter impacto quantificável: "Sem isso, perdemos Z% de eficiência"
3. **Could** é o buffer — se sobrar tempo/recurso, entra
4. **Won't** é tão importante quanto as outras categorias — explicitar o que NÃO faremos evita scope creep

### Teste de calibração para "Must"
Pergunte: "Se entregarmos tudo EXCETO este item, a entrega ainda tem valor?"
- Se SIM → não é Must
- Se NÃO → é Must

### Quando usar MoSCoW
- Definição de MVP ou escopo de release
- Negociação de escopo com stakeholders
- Quando o time tem mais ideias do que capacidade (sempre)

### Quando NÃO usar
- Quando precisa de ranking ordinal (MoSCoW agrupa, não ordena)
- Quando tudo é "Must" — sinal de que a calibração falhou

---

## 5. Kano Model

### Categorias

| Categoria        | Descrição                                                              | Efeito se presente    | Efeito se ausente      |
|-----------------|------------------------------------------------------------------------|-----------------------|------------------------|
| **Must-Be**     | Expectativa básica. Cliente não nota quando tem, mas detesta sem       | Neutro                | Muito insatisfeito     |
| **Performance** | Mais é melhor. Satisfação proporcional à entrega                       | Mais satisfeito       | Menos satisfeito       |
| **Attractive**  | Delighter. Cliente não esperava, fica encantado                        | Muito satisfeito      | Neutro                 |
| **Indifferent** | Cliente não se importa                                                 | Neutro                | Neutro                 |
| **Reverse**     | Alguns clientes ativamente não querem isso                             | Insatisfeito          | Satisfeito             |

### Como classificar (Kano Questionnaire)

Para cada feature, fazer duas perguntas:
1. "Como você se sentiria SE tivéssemos [feature]?" → Funcional
2. "Como você se sentiria SE NÃO tivéssemos [feature]?" → Disfuncional

Respostas possíveis: Gostaria muito / Espero que tenha / Neutro / Tolero / Não gostaria

### Tabela de classificação (Functional × Dysfunctional)

```
                    Disfuncional →
                    Gosta  Espera  Neutro  Tolera  Não gosta
Funcional ↓
Gosta muito         Q      A       A       A       P
Espera que tenha    R      I       I       I       M
Neutro              R      I       I       I       M
Tolera              R      I       I       I       M
Não gostaria        R      R       R       R       Q

A = Attractive, M = Must-Be, P = Performance, I = Indifferent, R = Reverse, Q = Questionable
```

### Estratégia de priorização com Kano
1. **Primeiro:** Garantir todos os Must-Be (table stakes)
2. **Segundo:** Maximizar Performance features (competitividade)
3. **Terceiro:** Incluir 1-2 Attractive features por release (diferenciação)
4. **Ignorar:** Indifferent
5. **Evitar:** Reverse

### Quando usar Kano
- Planejamento de produto com foco em satisfação do cliente
- Quando precisa diferenciar "higiênico" de "diferencial"
- Para argumentar investimento em features que não geram receita direta (Must-Be)

---

## 6. Comparação entre frameworks

| Critério              | RICE    | ICE     | WSJF    | MoSCoW  | Kano     |
|----------------------|---------|---------|---------|---------|----------|
| Velocidade de uso    | Média   | Alta    | Baixa   | Alta    | Baixa    |
| Precisão             | Alta    | Média   | Alta    | Baixa   | Alta     |
| Melhor para          | Product | Growth  | Portfolio| Escopo  | UX/Produto|
| Requer dados         | Sim     | Parcial | Sim     | Não     | Sim (pesquisa)|
| Output               | Ranking | Ranking | Ranking | Grupos  | Categorias|
| Agente recomendado   | COO/CTO | CMO     | CEO/COO | Todos   | CMO/CTO  |

---

## 7. Dicas de calibração cross-framework

1. **Sessão de calibração trimestral:** Reunir os agentes para alinhar escalas
2. **Anchor examples:** Definir 3 exemplos-âncora (baixo, médio, alto) para cada escala
3. **Blind scoring:** Cada agente pontua independentemente, depois compara
4. **Recalibrar após resultados:** Quando uma iniciativa terminar, comparar score previsto vs. resultado real
5. **Nunca usar um framework sozinho:** Combinar RICE para ranking + MoSCoW para escopo + Kano para validação de categoria

---

## 8. Template de decisão combinada

```markdown
## Decisão de Priorização — [Nome do Ciclo]

**Data:** [YYYY-MM-DD]
**Agente responsável:** [CEO/COO/CMO/CTO/CIO/CAIO]
**Framework primário:** [RICE/ICE/WSJF]
**Framework de validação:** [MoSCoW/Kano]

### Ranking final
| # | Iniciativa | Score primário | Categoria MoSCoW | Kano | Decisão |
|---|-----------|---------------|-------------------|------|---------|
| 1 |           |               |                   |      | GO/NO-GO|

### Premissas e riscos
- [Premissa 1]
- [Risco 1]

### Próxima revisão: [data]
```
