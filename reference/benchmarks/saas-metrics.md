# Benchmarks: Métricas SaaS

## Visão Geral

Este documento compila benchmarks de métricas-chave para empresas SaaS (Software as a Service) em diferentes estágios de maturidade. Os ranges são baseados em dados de mercado de fontes como Bessemer Cloud Index, OpenView Partners, SaaS Capital, KeyBanc, e relatórios de bancos de investimento especializados. Use como referência para avaliar a saúde da empresa e identificar áreas de melhoria.

## Métricas de Crescimento

### ARR Growth Rate (Crescimento de Receita Recorrente Anual)
| Estágio | ARR | Growth Rate Bom | Growth Rate Excelente |
|---------|-----|-----------------|----------------------|
| Seed | <$1M | N/A (pré-PMF) | N/A |
| Series A | $1-5M | >100% YoY | >200% YoY |
| Series B | $5-20M | >80% YoY | >150% YoY |
| Series C | $20-50M | >50% YoY | >100% YoY |
| Growth | $50-100M | >40% YoY | >70% YoY |
| Scale | >$100M | >25% YoY | >40% YoY |

**Como medir:** ARR final do período / ARR inicial do período - 1

### T2D3 Framework (Triple, Triple, Double, Double, Double)
```
Benchmark para empresas de alto crescimento após $1M ARR:
Ano 1: $1M → $3M (3x)
Ano 2: $3M → $9M (3x)
Ano 3: $9M → $18M (2x)
Ano 4: $18M → $36M (2x)
Ano 5: $36M → $72M (2x)
```

### Net Dollar Retention (NDR / Net Revenue Retention)
| Segmento | Mediano | Bom | Excelente |
|----------|---------|-----|-----------|
| SMB | 90-95% | 95-105% | >105% |
| Mid-Market | 100-105% | 105-115% | >115% |
| Enterprise | 110-115% | 115-130% | >130% |

**Como medir:** (ARR início + expansão - contração - churn) / ARR início x 100
**Fonte:** KeyBanc SaaS Survey, Bessemer

### Gross Revenue Retention (GRR)
| Quartil | Range |
|---------|-------|
| Top quartile | >95% |
| Mediana | 90% |
| Bottom quartile | <85% |

**Como medir:** (ARR início - contração - churn) / ARR início x 100

## Métricas de Eficiência

### Rule of 40
```
Growth Rate (%) + Profit Margin (%) >= 40%

Interpretação:
- <20%: Preocupante
- 20-40%: Aceitável
- 40-60%: Bom
- >60%: Excepcional

Exemplos:
- 100% growth + -60% margin = 40% ✓
- 30% growth + 15% margin = 45% ✓
- 20% growth + 5% margin = 25% ✗
```

### Burn Multiple
```
Burn Multiple = Net Burn / Net New ARR

Interpretação:
- <1x: Excelente (eficiente)
- 1-1.5x: Bom
- 1.5-2x: Aceitável
- >2x: Preocupante (queimando muito para crescer pouco)

Fonte: David Sacks / Craft Ventures
```

### CAC Payback Period
| Segmento | Bom | Excelente |
|----------|-----|-----------|
| SMB | <12 meses | <6 meses |
| Mid-Market | <18 meses | <12 meses |
| Enterprise | <24 meses | <18 meses |

**Como medir:** CAC / (ARPU mensal x Gross Margin %)

### LTV/CAC Ratio
| Rating | Range |
|--------|-------|
| Excelente | >5x |
| Bom | 3-5x |
| Aceitável | 2-3x |
| Preocupante | <2x |

**Como medir:** (ARPU x Gross Margin x Vida média do cliente) / CAC

### Magic Number
```
Magic Number = Net New ARR do trimestre / S&M spend do trimestre anterior

Interpretação:
- >1.0: Investir mais em S&M (eficiente)
- 0.5-1.0: Bom, otimizar
- <0.5: Rever GTM e unit economics
```

## Métricas Operacionais

### Gross Margin
| Tipo de SaaS | Mediana | Top Quartile |
|--------------|---------|--------------|
| Pure Software | 75-80% | >80% |
| Infra/Usage-based | 55-65% | >70% |
| Services-heavy | 50-60% | >65% |

### Operating Margins por Estágio
| Estágio | Mediana | Top Quartile |
|---------|---------|--------------|
| Series A | -80% a -40% | >-40% |
| Series B | -50% a -20% | >-20% |
| Series C | -30% a 0% | >0% |
| Pre-IPO | -10% a +10% | >10% |
| Public | +5% a +20% | >20% |

### Revenue per Employee
| Estágio | Mediana | Top Quartile |
|---------|---------|--------------|
| <$10M ARR | $80-120K | >$150K |
| $10-50M ARR | $120-180K | >$200K |
| $50-100M ARR | $150-250K | >$300K |
| >$100M ARR | $200-350K | >$400K |

## Métricas de Produto

### Monthly Churn Rate
| Segmento | Bom | Excelente |
|----------|-----|-----------|
| SMB | <3% | <2% |
| Mid-Market | <1.5% | <1% |
| Enterprise | <0.5% | <0.3% |

### DAU/MAU Ratio (Stickiness)
| Tipo de Produto | Bom | Excelente |
|-----------------|-----|-----------|
| SaaS B2B Workflow | 30-40% | >50% |
| SaaS B2B Analytics | 15-25% | >30% |
| SaaS B2C | 20-30% | >40% |

### NPS (Net Promoter Score)
| Rating | Range |
|--------|-------|
| Excelente | >50 |
| Bom | 30-50 |
| Aceitável | 10-30 |
| Preocupante | <10 |

## Métricas de Go-to-Market

### Sales Efficiency por Modelo
```
Self-serve/PLG: ACV < $5K, CAC < $500, Payback < 3 meses
Inside Sales: ACV $5K-50K, CAC $5K-15K, Payback 6-12 meses
Mid-Market: ACV $50K-250K, CAC $20K-50K, Payback 12-18 meses
Enterprise: ACV >$250K, CAC $50K-150K, Payback 18-24 meses
```

### Quota Attainment
| Rating | Range |
|--------|-------|
| Excelente | >70% dos reps atingem quota |
| Bom | 50-70% dos reps atingem quota |
| Preocupante | <50% dos reps atingem quota |

## Fontes de Referência
- Bessemer Cloud Index e State of the Cloud
- OpenView SaaS Benchmarks
- KeyBanc Capital Markets SaaS Survey
- SaaS Capital Index
- Tomasz Tunguz blog e análises
- Jason Lemkin / SaaStr benchmarks
- Craft Ventures / David Sacks
- Meritech Capital Public SaaS Comps
