# Benchmarks: Métricas SaaS

## Visão Geral

Este documento compila benchmarks de métricas SaaS por estágio de empresa, baseado em dados de fontes como Bessemer Venture Partners, OpenView, SaaS Capital, KeyBanc e Stripe. Os ranges representam medianas e quartis superiores — empresas de alto desempenho frequentemente superam significativamente esses benchmarks.

## Métricas de Crescimento

### ARR Growth Rate (Crescimento Anual)
| Estágio | ARR | Mediana | Top Quartile |
|---------|-----|---------|-------------|
| Seed | <$1M | N/A (pré-receita ou muito cedo) | N/A |
| Series A | $1M-$5M | 100-200% | >300% |
| Series B | $5M-$15M | 80-120% | >150% |
| Series C | $15M-$50M | 50-80% | >100% |
| Growth | $50M-$100M | 30-50% | >60% |
| Scale | >$100M | 20-35% | >40% |

### T2D3 Framework (Triple, Triple, Double, Double, Double)
```
Ano 1: $1M ARR
Ano 2: $3M (3x)
Ano 3: $9M (3x)
Ano 4: $18M (2x)
Ano 5: $36M (2x)
Ano 6: $72M (2x)

Empresas que seguem T2D3 são top-decile performers
Poucas empresas mantêm essa trajetória completa
```

### Net Dollar Retention (NDR)
| Estágio | Mediana | Bom | Excelente |
|---------|---------|-----|-----------|
| SMB-focused | 90-100% | 100-110% | >110% |
| Mid-market | 100-110% | 110-120% | >120% |
| Enterprise | 110-120% | 120-130% | >130% |

Composição do NDR:
- Gross Retention: 85-95% (% de receita mantida sem expansão)
- Expansion Rate: 10-30% (upsell + cross-sell)
- NDR = Gross Retention + Expansion - Downgrades

### Gross Churn Rate (Mensal)
| Segmento | Aceitável | Bom | Excelente |
|----------|-----------|-----|-----------|
| SMB | <3% | <2% | <1.5% |
| Mid-market | <1.5% | <1% | <0.5% |
| Enterprise | <1% | <0.5% | <0.3% |

## Métricas de Eficiência

### CAC Payback Period (Meses)
| Estágio | Aceitável | Bom | Excelente |
|---------|-----------|-----|-----------|
| Early-stage | <24 meses | <18 meses | <12 meses |
| Growth | <18 meses | <12 meses | <9 meses |
| Scale | <15 meses | <12 meses | <6 meses |

### LTV/CAC Ratio
| Rating | Ratio | Interpretação |
|--------|-------|---------------|
| Abaixo do esperado | <3x | Não sustentável, rever unit economics |
| Bom | 3-5x | Saudável, negócio viável |
| Excelente | 5-8x | Eficiente, possível sub-investimento em growth |
| Muito alto | >8x | Provavelmente sub-investindo em aquisição |

### Magic Number (Eficiência de Vendas)
```
Magic Number = (ARR novo net do trimestre) / (S&M spend do trimestre anterior)

< 0.5: Ineficiente — reavaliar go-to-market
0.5 - 0.75: Aceitável — otimizar
0.75 - 1.0: Bom — continuar investindo
> 1.0: Excelente — acelerar investimento em S&M
```

### Burn Multiple
```
Burn Multiple = Net Burn / Net New ARR

< 1.0x: Excelente eficiência
1.0-1.5x: Bom
1.5-2.0x: Aceitável para early-stage
2.0-3.0x: Preocupante
> 3.0x: Insustentável
```

### Rule of 40
```
Rule of 40 = Revenue Growth Rate (%) + EBITDA Margin (%)

> 40%: Excelente — empresa saudável
30-40%: Bom
20-30%: Aceitável
< 20%: Abaixo do esperado

Exemplos:
- 100% growth + (-60%) margin = 40% ✓ (early-stage ok)
- 30% growth + 15% margin = 45% ✓ (growth balanced)
- 10% growth + 5% margin = 15% ✗ (problema)
```

## Métricas de Produto

### Engagement
| Métrica | SMB SaaS | Enterprise SaaS |
|---------|----------|-----------------|
| DAU/MAU | 20-30% | 30-50% |
| WAU/MAU | 50-60% | 60-75% |
| Feature Adoption (top features) | 30-50% | 40-60% |
| Sessions/user/week | 3-5 | 5-10 |

### Ativação e Onboarding
| Métrica | Benchmark |
|---------|-----------|
| Free-to-Paid Conversion | 2-5% (self-serve), 15-25% (sales-assisted) |
| Trial-to-Paid | 15-25% (14-day trial), 10-15% (30-day trial) |
| Time-to-Value | <24h é excelente, <7 dias é bom |
| Onboarding Completion | >80% é bom |

## Métricas Financeiras

### Gross Margin
| Tipo | Mediana | Top Quartile |
|------|---------|-------------|
| SaaS puro (cloud) | 70-75% | >80% |
| SaaS + serviços | 55-65% | >70% |
| SaaS + hardware | 40-55% | >60% |

### Operating Expenses (% da Receita)
| Categoria | Early-stage | Growth | Scale |
|-----------|-------------|--------|-------|
| S&M | 50-80% | 30-50% | 20-35% |
| R&D | 30-50% | 20-35% | 15-25% |
| G&A | 15-25% | 10-20% | 8-15% |
| Total OpEx | 100-150% | 70-100% | 50-75% |

### Revenue per Employee
| Estágio | Mediana | Top Quartile |
|---------|---------|-------------|
| <$10M ARR | $80K-$120K | >$150K |
| $10M-$50M | $120K-$180K | >$200K |
| $50M-$100M | $150K-$250K | >$300K |
| >$100M | $200K-$350K | >$400K |

## Fontes de Referência
- Bessemer Cloud Index (BVP)
- OpenView SaaS Benchmarks Report
- KeyBanc SaaS Survey (anual)
- SaaS Capital Index
- Stripe Atlas / Patrick McKenzie
- Baremetrics Open Benchmarks
- ChartMogul SaaS Benchmarks

## Como Medir
```
Ferramentas recomendadas:
- ChartMogul, Baremetrics, ProfitWell (métricas de subscription)
- Amplitude, Mixpanel (métricas de produto)
- Salesforce, HubSpot (métricas de vendas)
- Stripe, Chargebee (métricas de billing)
- Looker, Metabase (dashboards customizados)

Cadência de revisão:
- Semanal: pipeline, MRR, churn signals
- Mensal: unit economics, cohort analysis, burn rate
- Trimestral: NDR, Rule of 40, benchmarking vs. peers
- Anual: LTV/CAC, TAM penetration, efficiency trends
```
