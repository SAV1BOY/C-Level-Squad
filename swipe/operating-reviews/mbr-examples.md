# MBR — Monthly Business Review Examples

> Exemplos de MBRs bem executadas: deep-dives mensais, trend analysis, ajustes estratégicos.
> Complemento da WBR com foco em padrões de médio prazo.

---

## O Que é uma MBR

A Monthly Business Review é o mecanismo que preenche o gap entre a WBR (operacional,
semanal) e a QBR (estratégica, trimestral). Enquanto a WBR foca em anomalias semanais,
a MBR analisa tendências de 4-8 semanas, identifica padrões emergentes e faz ajustes
táticos antes que problemas se consolidem.

A MBR é onde micro-tendências da WBR se tornam insights actionáveis de médio prazo.

---

## Estrutura Recomendada da MBR

### Duração e Formato
- **Duração:** 90-120 minutos
- **Frequência:** Mensal, primeira semana do mês seguinte
- **Participantes:** C-Level + VPs + convidados por tópico
- **Formato:** Documento narrativo (4-6 páginas) + dashboard de métricas

### Agenda Padrão

**Bloco 1: Business Health (30 min)**
Revisão do estado geral do negócio com métricas consolidadas do mês.

**Bloco 2: Deep-Dive Temático (30-40 min)**
Um tópico por mês investigado em profundidade. Rotação entre áreas.

**Bloco 3: Cross-Functional Dependencies (15-20 min)**
Blockers, dependências entre áreas, escalations.

**Bloco 4: Forward Look (15-20 min)**
Riscos emergentes, oportunidades identificadas, ajustes necessários.

---

## Exemplo Completo: MBR de Empresa SaaS B2B

### Bloco 1: Business Health — Fevereiro 2026

#### Financial Summary

```
Métrica           | Fev Actual | Fev Target | Jan Actual | MoM Change | YTD
------------------|------------|------------|------------|------------|--------
ARR               | $28.4M     | $29.0M     | $27.8M     | +2.2%      | $28.4M
Net New ARR       | $620K      | $750K      | $580K      | +6.9%      | $1.2M
Gross Margin      | 72%        | 75%        | 73%        | -1pp       | 72.5%
Burn Rate         | $1.8M      | $1.5M      | $1.6M      | +12.5%     | $3.4M
Runway            | 18 months  | 20 months  | 19 months  | -1 month   | —
```

#### Customer Metrics

```
Métrica                  | Fev    | Jan    | MoM    | 3m Trend
-------------------------|--------|--------|--------|--------
Total Customers          | 342    | 335    | +2.1%  | ↗
Logo Churn               | 3.2%   | 2.8%   | +0.4pp | ↗ (ruim)
Revenue Churn             | 1.9%   | 1.5%   | +0.4pp | ↗ (ruim)
Net Revenue Retention    | 108%   | 112%   | -4pp   | ↘ (concern)
Expansion Revenue        | $180K  | $210K  | -14%   | ↘
NPS (monthly survey)     | 38     | 42     | -4pts  | ↘
```

#### Narrative Analysis (extracto do documento)

> "Fevereiro mostra sinais de desaceleração que merecem atenção. Enquanto ARR continua
> a crescer, o ritmo está abaixo do target por segundo mês consecutivo. A principal
> preocupação é a deterioração de Net Revenue Retention, que caiu de 115% em Novembro
> para 108% em Fevereiro. Esta tendência, se não revertida, projeta ARR growth de 15%
> em vez dos 25% planeados para o ano.
>
> A análise por cohort revela que o problema está concentrado nos clientes adquiridos
> no H2 2025 — o cohort com maior proporção de clientes SMB adquiridos via self-serve.
> Estes clientes têm NPS 15 pontos abaixo do cohort enterprise e churn 2x superior.
> Hipótese: o product-market fit para o segmento SMB é mais fraco do que assumimos
> no planning de 2026."

### Bloco 2: Deep-Dive — Análise de Cohort e Segmentação

#### Cohort Analysis

```
Cohort          | # Clientes | Avg ACV | 6m Retention | NPS  | Support Tickets/mo
----------------|------------|---------|--------------|------|-------------------
Enterprise 2024 | 45         | $120K   | 96%          | 52   | 0.8
Enterprise 2025 | 62         | $95K    | 93%          | 48   | 1.2
Mid-Market 2025 | 98         | $45K    | 88%          | 40   | 2.1
SMB H1 2025     | 67         | $18K    | 82%          | 35   | 3.4
SMB H2 2025     | 70         | $15K    | 71%          | 28   | 4.8
```

#### Insights do Deep-Dive

**Insight 1: Bimodalidade de produto**
O produto foi desenhado para enterprise. A adaptação para SMB foi superficial —
onboarding simplificado mas complexidade core mantida. SMBs não conseguem extrair
valor suficiente para justificar o investimento.

**Insight 2: Support cost erosion**
SMBs geram 4x mais tickets por dollar de revenue. O custo de servir este segmento
está a erodir gross margins.

**Insight 3: Acquisition vs. Retention mismatch**
Marketing optimizou para volume de leads (SMB é mais fácil de adquirir), mas o
negócio é optimizado para retenção (onde enterprise é superior).

#### Decisões do Deep-Dive
1. **Pausar investimento em aquisição SMB self-serve** até revisão de product-market fit
2. **Criar task force de 4 semanas** para avaliar: (a) adaptar produto para SMB, (b) criar
   tier específico, ou (c) abandonar segmento
3. **Realocar budget de marketing** de SMB para mid-market e enterprise

### Bloco 3: Cross-Functional Dependencies

| Blocker | Área Origem | Área Impactada | Status | Owner |
|---------|-------------|----------------|--------|-------|
| API v3 migration atrasada 3 semanas | Engineering | Product (integrações) | At Risk | CTO |
| Hiring de AEs parado por budget freeze | Finance | Sales | Blocked | CFO |
| Compliance SOC2 audit atrasada | Legal/Security | Sales (enterprise deals) | At Risk | CISO |
| Data warehouse migration | Data | Todos (reporting) | On Track | VP Data |

**Escalation:** Hiring de AEs precisa de resolução esta semana. Temos pipeline de
candidatos aprovados mas budget não liberado. CFO e CRO a alinhar na terça.

### Bloco 4: Forward Look — Março 2026

**Riscos emergentes:**
- Concorrente X anunciou feature que elimina nosso diferencial em integração
- Dois enterprise customers (combined ARR $450K) em renewal risk — sinais de evaluation de alternativas
- Engineering velocity em queda: tech debt acumulado está a impactar delivery

**Oportunidades identificadas:**
- Partnership com plataforma Y pode abrir canal de 500+ prospects enterprise
- AI feature prototype mostrando resultados promissores em beta interno
- Expansão para mercado LATAM tem demand signals fortes (12 inbound requests em Fev)

**Ajustes para Março:**
- Product: priorizar feature de integração competitiva (resposta ao concorrente X)
- CS: war room para os dois enterprise renewals em risco
- Engineering: agendar tech debt sprint (1 semana dedicada)

---

## MBR para Áreas Específicas

### MBR de Engineering

**Métricas mensais adicionais:**
- Technical debt ratio (tempo em debt vs. features)
- Architecture fitness functions scores
- Team satisfaction e engagement survey results
- Hiring pipeline health por role
- On-call burden distribution

**Deep-dive rotation:**
- Mês 1: System reliability e incident analysis
- Mês 2: Developer experience e tooling
- Mês 3: Architecture evolution e tech debt
- Mês 4: Team health e organizational design

### MBR de Product

**Métricas mensais adicionais:**
- Feature adoption rates (30-day post-launch)
- Discovery velocity (experiments per month)
- Outcome achievement rate (% of bets that worked)
- Customer interview cadence
- Competitive feature parity score

### MBR de People/HR

**Métricas mensais adicionais:**
- Regrettable attrition rate
- Offer acceptance rate
- Time to fill por nível e área
- Engagement survey trending (pulse)
- Diversity metrics por função e nível
- Internal mobility rate

---

## Diferenças entre WBR, MBR e QBR

| Dimensão | WBR | MBR | QBR |
|---|---|---|---|
| Frequência | Semanal | Mensal | Trimestral |
| Duração | 60 min | 90-120 min | Half-day |
| Foco | Anomalias operacionais | Tendências e ajustes | Estratégia e OKRs |
| Horizonte | Esta semana | Último mês, próximo mês | Último quarter, próximo quarter |
| Participantes | Team leads | C-Level + VPs | C-Level + Board |
| Output | Action items | Ajustes táticos | Decisões estratégicas |
| Formato | Dashboard | Narrativa + Dashboard | Memo + Dashboard |

---

## Erros Comuns em MBRs

### Erro 1: Repetir a WBR em Formato Mensal
A MBR não é a WBR com dados consolidados. É uma análise de padrões e tendências
que não são visíveis na granularidade semanal.

### Erro 2: Skip do Deep-Dive
Quando o tempo aperta, o deep-dive é cortado. É exatamente o oposto do que
deveria acontecer — o deep-dive é o componente mais valioso.

### Erro 3: Forward Look Genérico
"Vamos continuar a monitorar" não é um forward look. Deve haver ações concretas
com owners e deadlines.

### Erro 4: Ausência de Cross-Functional
Se cada área faz MBR separada sem momento cross-functional, silos consolidam-se.

### Erro 5: Dados Sem Narrativa
Dashboard sem análise narrativa é inútil. Os números precisam de interpretação
e contexto para gerar decisões.

---

## Template de Documento MBR

```
# MBR — [Mês/Ano]

## Executive Summary (1 parágrafo)
Estado geral, principais destaques e concerns.

## Business Health Dashboard
[Tabela de métricas com targets, actuals, trends]

## Narrative Analysis (1-2 páginas)
O que os números significam. Patterns emergentes. Causas.

## Deep-Dive: [Tópico do Mês] (1-2 páginas)
Análise profunda do tópico selecionado.

## Cross-Functional Dependencies
[Tabela de blockers e escalations]

## Forward Look (1 página)
Riscos, oportunidades, ajustes necessários.

## Action Items
[Tabela com ação, owner, deadline, status]
```

---

## Referências

- Colin Bryar & Bill Carr: "Working Backwards" — operating mechanisms
- Elad Gil: "High Growth Handbook" — scaling reviews
- Ben Horowitz: "The Hard Thing About Hard Things" — operational discipline
- Measure What Matters (John Doerr) — OKR integration com reviews

---

*Última atualização: Março 2026*
*Categoria: Operating Reviews | Nível: C-Level | Formato: Examples + Framework*
