# Template: Dimensionamento de Mercado — TAM / SAM / SOM

## Propósito
Este template guia a análise de dimensionamento de mercado usando a metodologia TAM/SAM/SOM (Total Addressable Market, Serviceable Addressable Market, Serviceable Obtainable Market). Essencial para planejamento estratégico, pitch para investidores, e decisões de go-to-market.

## Instruções de Uso
1. Comece definindo o mercado de forma clara e delimitada
2. Use abordagem top-down E bottom-up para triangular estimativas
3. Documente todas as premissas e fontes de dados
4. Revise anualmente ou quando houver mudança significativa no mercado/produto

---

## 1. Definição do Mercado

**Produto/Serviço analisado:** [Nome e descrição breve]
**Mercado-alvo primário:** [Segmento principal]
**Geografia:** [Países/regiões analisados]
**Data da análise:** [DD/MM/AAAA]
**Responsável:** [Nome — Cargo]

---

## 2. TAM — Total Addressable Market

> "Se capturássemos 100% do mercado, qual seria a receita total?"

### 2.1 Abordagem Top-Down
- **Fonte de dados:** [Relatórios de mercado — citar fontes: Gartner, IDC, etc.]
- **Tamanho global do mercado:** [US$ / R$ X bilhões]
- **Crescimento anual (CAGR):** [X% — período de referência]
- **Projeção para [ANO+3]:** [US$ / R$ X bilhões]

### 2.2 Abordagem Bottom-Up
- **Número total de empresas/pessoas no mercado-alvo:** [N]
- **Ticket médio anual estimado:** [R$ X]
- **TAM calculado:** [N x Ticket = R$ X]

### 2.3 Reconciliação
| Método | Valor Estimado | Confiança |
|--------|---------------|-----------|
| Top-Down | [R$ X] | [Alta/Média/Baixa] |
| Bottom-Up | [R$ X] | [Alta/Média/Baixa] |
| **TAM Adotado** | **[R$ X]** | **[Justificativa]** |

---

## 3. SAM — Serviceable Addressable Market

> "Qual parcela do TAM nosso produto pode realmente atender?"

### 3.1 Filtros de Segmentação

| Filtro | Descrição | % do TAM Excluída |
|--------|-----------|-------------------|
| Geografia | [Apenas Brasil / LATAM / etc.] | [X%] |
| Porte de empresa | [PME / Mid-market / Enterprise] | [X%] |
| Setor/Indústria | [Setores que atendemos] | [X%] |
| Maturidade tecnológica | [Empresas com infra mínima] | [X%] |
| Regulatório | [Restrições de atuação] | [X%] |

### 3.2 Cálculo do SAM
- **TAM:** [R$ X]
- **Filtros aplicados:** [TAM x (1 - soma das exclusões)]
- **SAM estimado:** [R$ X]
- **Número de clientes potenciais:** [N empresas/pessoas]

---

## 4. SOM — Serviceable Obtainable Market

> "Quanto podemos realisticamente capturar nos próximos 1-3 anos?"

### 4.1 Fatores de Captura

| Fator | Estimativa | Justificativa |
|-------|-----------|---------------|
| Awareness / alcance de marketing | [X% do SAM] | [Base: canais atuais + planejados] |
| Taxa de conversão de pipeline | [X%] | [Base: dados históricos] |
| Capacidade de atendimento (sales + CS) | [N clientes/ano] | [Base: headcount atual/planejado] |
| Win rate competitivo | [X%] | [Base: dados de win/loss] |
| Churn esperado | [X% anual] | [Base: dados históricos] |

### 4.2 Cálculo do SOM
- **SAM:** [R$ X]
- **Market share realista em 12 meses:** [X%]
- **SOM ano 1:** [R$ X]
- **SOM ano 2:** [R$ X] (crescimento de [X%])
- **SOM ano 3:** [R$ X] (crescimento de [X%])

---

## 5. Resumo Visual

```
┌──────────────────────────────────────────────────┐
│                TAM: R$ [X] bilhões               │
│  ┌──────────────────────────────────────┐        │
│  │          SAM: R$ [X] milhões         │        │
│  │  ┌──────────────────────────┐        │        │
│  │  │    SOM: R$ [X] milhões   │        │        │
│  │  └──────────────────────────┘        │        │
│  └──────────────────────────────────────┘        │
└──────────────────────────────────────────────────┘
```

**Proporções:**
- SAM = [X%] do TAM
- SOM = [X%] do SAM
- SOM = [X%] do TAM

---

## 6. Análise de Sensibilidade

| Cenário | TAM | SAM | SOM (Ano 1) | Premissa-chave alterada |
|---------|-----|-----|-------------|------------------------|
| Otimista | [R$ X] | [R$ X] | [R$ X] | [Qual premissa muda] |
| Base | [R$ X] | [R$ X] | [R$ X] | [Premissas padrão] |
| Conservador | [R$ X] | [R$ X] | [R$ X] | [Qual premissa muda] |

---

## 7. Premissas e Fontes

### Premissas Críticas
1. [Premissa 1 — ex: "Mercado cresce a CAGR de 18% nos próximos 5 anos"]
2. [Premissa 2 — ex: "Ticket médio se mantém estável ajustado pela inflação"]
3. [Premissa 3 — ex: "Regulação não restringe atuação nos mercados-alvo"]

### Fontes de Dados
| Fonte | Tipo | Data | Confiabilidade |
|-------|------|------|---------------|
| [Gartner Report 2025] | Relatório de mercado | [MM/AAAA] | [Alta] |
| [IBGE / RAIS] | Dados governamentais | [MM/AAAA] | [Alta] |
| [Pesquisa interna] | Primary research | [MM/AAAA] | [Média] |
| [Crunchbase / Tracxn] | Dados de mercado | [MM/AAAA] | [Média] |

---

## 8. Implicações Estratégicas

### Com base no dimensionamento:
- **Go-to-market:** [Estratégia recomendada — ex: foco em mid-market antes de enterprise]
- **Pricing:** [Ajustes sugeridos — ex: tier intermediário para capturar mais SAM]
- **Produto:** [Features prioritárias para expandir SAM]
- **Expansão geográfica:** [Mercados que mais expandem o SAM]
- **Investimento necessário:** [Para capturar o SOM projetado]

---

## Exemplo Preenchido (Resumo)

> **Produto:** Plataforma SaaS de gestão de despesas corporativas
> **TAM Global:** US$ 12B (2025) — CAGR 15%
> **TAM Brasil:** R$ 4.5B
> **SAM:** R$ 1.2B (PMEs com 50-500 funcionários, setores serviços e tech)
> **SOM Ano 1:** R$ 18M (1.5% do SAM — 600 clientes x R$ 30K/ano)
> **SOM Ano 3:** R$ 72M (6% do SAM — 2.400 clientes)

---

## Dicas de Uso
- Sempre use duas metodologias (top-down + bottom-up) para triangular
- Investidores desconfiam de TAM inflado — seja conservador e justifique
- SAM é mais importante que TAM para decisões operacionais
- Revise SOM trimestralmente com base em dados reais de vendas
- Documente TODAS as premissas — elas são o ponto mais atacado em pitches
- Considere que novos produtos/features podem expandir o SAM ao longo do tempo
