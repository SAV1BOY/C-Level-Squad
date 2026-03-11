# Base Rate Checks — Guia de Análise de Taxas Base para Decisões Executivas

> Referência do C-Level Squad para ancorar decisões em dados históricos e estatísticos.
> "A negligência da taxa base é a fonte mais significativa de erro em previsões." — Daniel Kahneman, Thinking, Fast and Slow

---

## 1. O que são Base Rates?

Base rates (taxas base) são as frequências históricas de um resultado em uma população de referência relevante. Antes de avaliar qualquer caso específico, o decisor deve primeiro perguntar: **"Qual é a taxa base para este tipo de evento?"**

### Por que importam (Referência Kahneman)

Daniel Kahneman e Amos Tversky demonstraram que humanos sistematicamente ignoram base rates ao fazer previsões, preferindo confiar em informações narrativas específicas do caso (o "inside view"). Este viés é chamado de **base rate neglect** ou **base rate fallacy**.

**Exemplo clássico:** Se alguém diz "nossa startup vai dar certo porque temos ótimo produto e equipe forte", está usando o inside view. O outside view pergunta: "Qual percentual de startups com características semelhantes realmente deu certo?" (Resposta: ~10% sobrevivem 5 anos, ~1-2% têm exit significativo).

### Inside View vs. Outside View

| Perspectiva    | Descrição                                              | Risco                          |
|---------------|--------------------------------------------------------|-------------------------------|
| **Inside View** | Foca nas especificidades do caso: equipe, produto, plano | Viés de otimismo, planning fallacy |
| **Outside View** | Foca na classe de referência: "projetos como este"      | Pode ignorar fatores únicos genuínos |
| **Recomendação** | Começar SEMPRE pelo outside view, depois ajustar com inside view | Ajuste máximo de ±30% da base rate |

---

## 2. Como encontrar Base Rates

### Passo a passo

1. **Definir a classe de referência:** Qual é a categoria mais específica e relevante?
   - Ruim: "startups" (muito genérico)
   - Melhor: "SaaS B2B Series A no Brasil com ARR entre R$5-20M"
   - Ideal: "SaaS B2B vertical saúde, Series A, LATAM, 2020-2025"

2. **Buscar dados:**
   - Relatórios de mercado (CB Insights, Crunchbase, Distrito)
   - Benchmarks de indústria (OpenView, Bessemer, a16z)
   - Dados internos históricos (CRM, analytics)
   - Papers acadêmicos (Google Scholar)
   - Associações setoriais

3. **Validar qualidade do dado:**
   - Tamanho da amostra (N > 30 para confiabilidade mínima)
   - Período relevante (dados de 5+ anos atrás podem estar defasados)
   - Viés de sobrevivência (os dados incluem os que falharam?)
   - Geografia e contexto comparáveis

4. **Aplicar com ajuste:**
   - Iniciar com a base rate encontrada
   - Ajustar para cima ou para baixo com evidência específica
   - Documentar os ajustes e as razões
   - Nunca ajustar mais que 2-3× a base rate sem evidência extraordinária

---

## 3. Base Rates por vertical

### 3.1 SaaS (Software as a Service)

| Métrica                        | Base Rate típica          | Fonte / Contexto                     |
|-------------------------------|--------------------------|--------------------------------------|
| Monthly churn rate (SMB)      | 3-7%                     | Média de SaaS SMB                    |
| Monthly churn rate (Enterprise)| 0.5-1.5%                | SaaS Enterprise com contratos anuais |
| Annual net revenue retention  | 100-130% (bom: >110%)   | Melhor indicador de saúde SaaS       |
| Trial → Paid conversion       | 2-5% (free trial sem CC) | Com cartão de crédito: 15-25%        |
| Freemium → Paid conversion    | 1-4%                     | Depende muito do produto             |
| CAC Payback period            | 12-18 meses (saudável)   | >24 meses = problema                 |
| LTV:CAC ratio                 | 3:1 (bom), >5:1 (ótimo) | <3:1 = unit economics ruins          |
| Month-over-month growth (early)| 15-20% (excepcional)    | 5-10% (bom), <5% (preocupante)      |
| Sales cycle (Enterprise)      | 3-9 meses                | Varia por ticket e complexidade      |
| Win rate de pipeline          | 15-25%                   | Top performers: 30%+                 |
| Feature adoption rate         | 5-25% dos usuários       | Feature usada por >40% = core feature|
| NPS                           | 30-50 (bom), >50 (ótimo) | Mediana SaaS: ~30                    |

### 3.2 E-commerce

| Métrica                        | Base Rate típica          | Contexto                             |
|-------------------------------|--------------------------|--------------------------------------|
| Conversion rate (site)        | 1-3%                     | Top performers: 5%+                  |
| Cart abandonment rate         | 65-80%                   | Mobile é pior (~85%)                 |
| Return rate                   | 15-30%                   | Moda: 30-40%, eletrônicos: 10-15%   |
| Email open rate               | 15-25%                   | E-commerce tende a ~18%              |
| Repeat purchase rate          | 20-40%                   | >40% = excelente                     |
| Average order value growth    | 5-10% ao ano             | Via cross-sell e upsell              |
| Customer acquisition cost     | R$30-150 (varia muito)   | Depende do ticket e canal            |
| ROAS (Return on Ad Spend)     | 3-5× (saudável)          | <2× = problema, >8× = excelente     |
| Delivery on-time rate         | 85-95%                   | >95% = world-class                   |

### 3.3 Marketplace

| Métrica                        | Base Rate típica          | Contexto                             |
|-------------------------------|--------------------------|--------------------------------------|
| Take rate                     | 10-25%                   | Varia por vertical e valor agregado  |
| Supply-side churn (mensal)    | 5-15%                    | Lado da oferta é mais volátil        |
| Demand-side churn (mensal)    | 3-8%                     | Depende da frequência de uso         |
| Liquidity rate                | 30-60%                   | % de listagens que geram transação   |
| Time to first transaction     | Idealmente <7 dias       | >30 dias = problema de ativação      |
| Buyer-to-seller ratio         | 5:1 a 20:1               | Varia dramaticamente por tipo        |
| GMV growth (early stage)      | 15-30% MoM               | Após product-market fit              |
| Disintermediação rate         | 10-30%                   | Risco existencial de marketplaces    |

### 3.4 Fintech

| Métrica                        | Base Rate típica          | Contexto                             |
|-------------------------------|--------------------------|--------------------------------------|
| App download → account creation| 30-50%                  | Depende da fricção do KYC            |
| Account → first transaction   | 40-70%                   | Depende do incentivo de ativação     |
| Monthly active rate           | 40-60%                   | Fintech com billing: 80%+            |
| Default rate (crédito PF)     | 3-8%                     | Varia por score e produto            |
| Default rate (crédito PJ PME) | 5-15%                    | PME tem mais risco                   |
| NPS (neobanks)                | 50-80                    | Muito acima do banking tradicional   |
| Cost to serve                 | R$5-20/cliente/mês       | Bancos tradicionais: R$50-200        |
| Regulatory approval time      | 6-24 meses               | BACEN/CVM                            |

---

## 4. Base Rates para decisões organizacionais

### 4.1 Contratação e Pessoas

| Métrica                                | Base Rate                | Contexto                             |
|---------------------------------------|--------------------------|--------------------------------------|
| Contratação bem-sucedida (18 meses)   | 50-60%                   | ~40-50% saem ou são demitidos em 18m |
| Sucesso de promoção interna           | 60-70%                   | Melhor que contratação externa        |
| Referral hire success rate            | 65-75%                   | Melhor canal de contratação           |
| Time to productivity (IC)             | 3-6 meses                | Senior: 3m, Junior: 6m               |
| Time to productivity (VP+)           | 6-12 meses               | Executivo demora mais                 |
| Voluntary turnover (tech, anual)      | 15-25%                   | No Brasil, pode ser maior             |
| Engagement → Retention correlation    | 0.6-0.7                  | eNPS > 50 correlaciona com <10% churn|

### 4.2 Iniciativas e Projetos

| Métrica                                | Base Rate                | Contexto                             |
|---------------------------------------|--------------------------|--------------------------------------|
| Projetos entregues no prazo           | 30-40%                   | PMI data                             |
| Projetos entregues no orçamento       | 40-50%                   | PMI data                             |
| Iniciativas que atingem KPI target    | 25-35%                   | Muitas falham silenciosamente         |
| Transformações digitais bem-sucedidas | 20-30%                   | McKinsey data                        |
| M&A que cria valor                    | 30-40%                   | Maioria destrói valor                 |
| Pivots bem-sucedidos                  | 10-20%                   | Depende da definição de sucesso       |
| OKRs atingidos (70%+ do target)       | 60-70%                   | Se >90%, targets muito fáceis         |

### 4.3 Growth e GTM

| Métrica                                | Base Rate                | Contexto                             |
|---------------------------------------|--------------------------|--------------------------------------|
| Cold email response rate              | 1-5%                     | Personalizado: 5-15%                 |
| Cold call connection rate             | 5-15%                    | Meeting booking: 1-3%                |
| Webinar attendance rate               | 30-50% dos registrados   | Replay adiciona 10-20%               |
| Blog post → lead conversion          | 0.5-2%                   | Content com alto intent: 3-5%        |
| Landing page conversion              | 2-5% (mediana)           | Otimizada: 8-15%                     |
| Product-led growth activation rate    | 20-40%                   | Definição varia por produto          |

---

## 5. Exercícios de calibração

### Exercício 1: Estimativa pessoal vs. base rate

Para cada cenário, primeiro estime SUA resposta, depois confira a base rate:

1. "Qual a probabilidade de nossa nova feature aumentar retenção em >5%?"
   - Sua estimativa: ____%
   - Base rate: ~15-25% das features têm impacto mensurável em retenção
   - Lição: a maioria das features não move métricas-chave

2. "Qual a chance de entregarmos o projeto no prazo prometido?"
   - Sua estimativa: ____%
   - Base rate: 30-40%
   - Lição: planning fallacy é universal

3. "Qual a chance de nosso novo canal de aquisição ter ROAS >3×?"
   - Sua estimativa: ____%
   - Base rate: ~30-40% dos canais testados performam acima do threshold
   - Lição: testar múltiplos canais é estratégia, não desperdício

### Exercício 2: Classe de referência

Para cada situação, defina a melhor classe de referência:

| Situação                               | Classe ruim                | Classe boa                                    |
|----------------------------------------|---------------------------|-----------------------------------------------|
| Lançar produto em novo mercado         | "Empresas que expandem"   | "SaaS B2B que expandiram para LATAM com <$10M ARR" |
| Contratar VP de Engenharia             | "Contratações de VP"      | "VP Eng contratado externamente em startup Series B-C" |
| Implementar OKRs                       | "Empresas que usam OKRs"  | "Empresas de 50-200 pessoas implementando OKRs pela 1a vez" |

### Exercício 3: Atualização Bayesiana simplificada

```
P(sucesso | evidência) = P(sucesso base) × fator de ajuste

Fator de ajuste por tipo de evidência:
- Dados quantitativos fortes (A/B test, cohort analysis): ×1.5 a ×2.0
- Dados qualitativos fortes (N>30, padrão claro): ×1.2 a ×1.5
- Opinião de especialista: ×1.1 a ×1.3
- Analogia com caso anterior: ×1.0 a ×1.2
- Intuição sem dados: ×1.0 (não ajustar)
```

**Exemplo:** Base rate de sucesso de nova feature = 25%
- Temos A/B test positivo em MVP (fator ×1.8) → 25% × 1.8 = 45%
- Temos feedback qualitativo de 5 clientes (fator ×1.1) → 25% × 1.1 = 27.5%

---

## 6. Protocolo de uso no C-Level Squad

### Quando aplicar base rate checks

| Situação                                    | Agente responsável | Ação                                        |
|---------------------------------------------|--------------------|---------------------------------------------|
| Forecast de crescimento                     | CEO / CMO          | Comparar com base rates de vertical          |
| Estimativa de prazo de projeto              | CTO / COO          | Aplicar multiplicador da base rate           |
| Projeção de ROI de iniciativa               | CIO / CAIO         | Ancorar em taxa de sucesso de iniciativas    |
| Decisão de invest/kill de produto           | CEO                | Comparar com base rates de pivots/launches   |
| Previsão de contratação                     | COO                | Usar base rate de hiring success             |

### Template de base rate check

```markdown
## Base Rate Check — [Decisão]

**Data:** [YYYY-MM-DD]
**Agente:** [CEO/COO/CMO/CTO/CIO/CAIO]

### Classe de referência
[Descrição da classe de referência escolhida]

### Base rate encontrada
[X%] — Fonte: [referência]

### Ajustes com inside view
| Fator                    | Direção | Magnitude | Justificativa |
|--------------------------|---------|-----------|---------------|
| [fator 1]               | +/-     | [×1.X]    | [razão]       |

### Estimativa final ajustada
[Y%] (base rate X% × fatores de ajuste)

### Decisão
[Go / No-go / Mais informação necessária]
```

---

## 7. Armadilhas comuns

1. **Classe de referência muito ampla:** "Startups" não é útil. Ser específico
2. **Viés de sobrevivência nos dados:** Relatórios de "melhores práticas" só mostram quem deu certo
3. **Dados desatualizados:** Base rates de 2019 podem não refletir 2025 (especialmente pós-AI)
4. **Ajuste excessivo:** Não ajustar a base rate em mais de 3× sem evidência extraordinária
5. **Ignorar a base rate quando o resultado é desejado:** O viés mais perigoso e mais comum
6. **Confundir correlação com base rate:** "80% das empresas que fizeram X tiveram sucesso" — mas quantas fizeram X?
7. **Não atualizar:** Base rates devem ser revisitadas trimestralmente com dados internos
