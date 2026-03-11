# WBR — Weekly Business Review Examples

> Exemplos de WBRs bem executadas no modelo Amazon e adaptações.
> Metrics-driven reviews com decision tracking integrado.

---

## O Que é uma WBR

A Weekly Business Review é o mecanismo operacional mais poderoso para manter uma
organização alinhada, informada e accountable. Originada na Amazon, a WBR é uma
reunião semanal onde métricas-chave são revisadas, anomalias são investigadas e
decisões operacionais são tomadas.

Não é uma reunião de status update. É uma sessão de análise de dados que força a
organização a confrontar a realidade semanalmente, antes que problemas se tornem crises.

---

## Modelo Amazon — A WBR Canónica

### Estrutura e Formato

**Duração:** 60 minutos (estritamente respeitado)
**Frequência:** Semanal, mesmo dia e horário (inegociável)
**Participantes:** Leadership team da área (6-10 pessoas)
**Formato:** Deck de métricas pré-preparado, sem apresentação — leitura silenciosa

### O Deck de Métricas

O deck segue um formato padronizado que não muda semana a semana:

**Página 1: Executive Summary Dashboard**
- 8-12 métricas-chave com actuals vs. targets
- Sinalização visual: verde (on track), amarelo (at risk), vermelho (off track)
- Tendência de 8 semanas para cada métrica
- Week-over-week delta

**Página 2-3: Input Metrics**
Input metrics são as métricas que a equipa controla diretamente:
- Número de features deployed por semana
- Tempo médio de resposta ao cliente
- Número de experimentos lançados
- Pipeline de candidatos em processo
- Número de bugs críticos resolvidos

**Página 4-5: Output Metrics**
Output metrics são os resultados que emergem dos inputs:
- Revenue (MRR, ARR, growth rate)
- Customer satisfaction (NPS, CSAT)
- Retention e churn rates
- Conversion rates por funil
- Cost per acquisition

**Página 6: Anomalias e Investigações**
- Desvios significativos (>2 standard deviations) identificados
- Root cause analysis preliminar para cada anomalia
- Ações tomadas ou propostas
- Owner e deadline para cada ação

**Página 7: Action Items Tracker**
- Ações da semana anterior com status
- Novas ações desta semana
- Ações bloqueadas com escalation path
- Tendência: número de ações abertas por semana

### O Processo de Leitura

1. **Pré-leitura (5 min):** Participantes lêem o deck em silêncio
2. **Perguntas de clarificação (5 min):** "O que significa este número?"
3. **Análise de anomalias (30 min):** Foco nos desvios — o que está fora do esperado?
4. **Decisões e ações (15 min):** O que fazemos com base no que vimos?
5. **Wrap-up (5 min):** Confirmar owners e deadlines

### Regras Inegociáveis

- **Dados, não opiniões:** "Eu acho que..." é substituído por "os dados mostram que..."
- **Sem surpresas:** Se há bad news, deve estar no deck antes da reunião
- **Owner accountability:** Cada métrica tem um owner individual, não um comitê
- **Andon cord:** Qualquer pessoa pode parar a reunião para investigar uma anomalia
- **No PowerPoint narrative:** O deck é dados, não slides narrativos

---

## Exemplo Prático: WBR de Produto SaaS

### Dashboard Semanal

```
Métrica                  | Actual | Target | Delta | Trend (8w)
-------------------------|--------|--------|-------|----------
MRR                      | $2.3M  | $2.4M  | -4%   | ↗ (lento)
New Customers            | 47     | 55     | -15%  | ↘
Churn Rate               | 2.1%   | 1.8%   | +0.3% | ↗ (ruim)
NPS                      | 42     | 50     | -8pts | ↘
Avg Response Time        | 4.2h   | 2h     | +110% | ↗ (ruim)
Features Shipped         | 3      | 5      | -40%  | ↘
Uptime                   | 99.91% | 99.95% | -0.04%| → (estável)
Pipeline Value           | $890K  | $1.1M  | -19%  | ↘
Trial-to-Paid Conv.      | 12%    | 18%    | -6pts | ↘
Support Tickets/Customer | 1.8    | 1.2    | +50%  | ↗ (ruim)
```

### Análise de Anomalias (exemplo)

**Anomalia 1: Churn rate a subir há 4 semanas consecutivas**
- Root cause investigation: 60% do churn concentrado em clientes do plano Basic
- Correlação identificada: update de pricing em Fevereiro aumentou Basic em 20%
- Clientes saindo citam "valor não justifica preço novo" em exit surveys
- Ação proposta: grandfathering de preço para clientes existentes + revisão de
  value proposition do plano Basic
- Owner: VP Product | Deadline: próxima sexta-feira

**Anomalia 2: Avg Response Time duplicou**
- Root cause: 2 agentes de suporte saíram, não foram substituídos
- Impacto cascata: NPS em queda, support tickets por cliente a subir
- Ação imediata: redistribuir load + contratar 2 agentes (pipeline existe)
- Owner: Head of Support | Deadline: contratação em 2 semanas

### Decisões Tomadas na WBR
1. Aprovar grandfathering de preço — impacto estimado de -$30K MRR, compensado
   por redução de churn estimada em $80K MRR preservado
2. Fast-track hiring de suporte — orçamento aprovado na reunião
3. Product team vai investigar correlação entre features shipped e trial conversion

---

## Variação: WBR para Engineering

### Métricas Específicas

```
Métrica                    | Actual | Target | Trend
---------------------------|--------|--------|------
Deployment Frequency       | 12/sem | 15/sem | ↗
Lead Time for Changes      | 3.2d   | 2d     | ↘ (melhorando)
Change Failure Rate        | 8%     | 5%     | → (estável)
Mean Time to Recovery      | 45min  | 30min  | ↗ (piorando)
Code Coverage              | 72%    | 80%    | ↗ (melhorando)
Tech Debt Score            | 34     | 25     | ↘ (piorando)
Sprint Velocity            | 42pts  | 45pts  | → (estável)
On-call Incidents          | 7      | 3      | ↗ (piorando)
Developer Satisfaction     | 7.2/10 | 8/10   | ↘ (piorando)
```

### Foco de Análise
- DORA metrics como leading indicators de saúde da engineering
- Correlação entre tech debt score e change failure rate
- Developer satisfaction como proxy para retention risk

---

## Variação: WBR para Go-to-Market

### Métricas Específicas

```
Métrica                    | Actual | Target | Trend
---------------------------|--------|--------|------
SQLs Generated             | 120    | 150    | ↘
SQL-to-Opp Conversion      | 35%    | 40%    | ↘
Pipeline Created           | $1.2M  | $1.5M  | ↘
Win Rate                   | 28%    | 32%    | → (estável)
Average Deal Size          | $45K   | $50K   | ↗
Sales Cycle Length          | 42d    | 35d    | ↗ (piorando)
CAC                        | $12K   | $10K   | ↗ (piorando)
LTV/CAC Ratio              | 3.2x   | 4x     | ↘
Expansion Revenue %        | 18%    | 25%    | ↗ (melhorando)
```

---

## Erros Comuns em WBRs

### Erro 1: Transformar em Status Update
Cada pessoa apresenta "o que fiz esta semana". Não é o propósito.
Fix: Focar em métricas e anomalias, não em atividades.

### Erro 2: Excesso de Métricas
40 métricas no dashboard. Ninguém consegue processar.
Fix: 8-12 métricas-chave. Detalhes em appendix.

### Erro 3: Métricas Sem Owner
"A métrica de churn está vermelha." "De quem é?" Silêncio.
Fix: Cada métrica tem um owner nomeado antes de entrar no dashboard.

### Erro 4: Sem Follow-Through
Ações definidas na WBR mas nunca rastreadas.
Fix: Tracker de ações é a primeira coisa revisada na WBR seguinte.

### Erro 5: Cancelar Quando Está "Tudo Bem"
"Não há anomalias esta semana, vamos cancelar."
Fix: WBR acontece sempre. Semanas sem anomalias são para deep-dives.

### Erro 6: Dados Atrasados
Métricas de terça revisadas na sexta — já são velhas.
Fix: Automação de data pipeline. Dados de D-1 no máximo.

---

## Implementação de WBR — Guia Prático

### Semana 1-2: Setup
- Definir as 8-12 métricas-chave com owners
- Criar template padronizado de dashboard
- Configurar data pipeline automatizado
- Agendar slot fixo semanal (nunca mover)

### Semana 3-4: Calibração
- Primeiras WBRs serão desconfortáveis — é normal
- Calibrar targets com base em dados reais
- Ajustar formato do deck com base em feedback
- Estabelecer normas de conduta (dados, não opiniões)

### Mês 2-3: Maturação
- Introduzir anomaly detection automatizada
- Conectar action tracker a sistema de gestão
- Começar trend analysis de 8+ semanas
- Adicionar correlações entre métricas

### Mês 4+: Excelência
- WBR roda no piloto automático
- Decisões são tomadas na reunião, não depois
- Dados driving decisions é a norma cultural
- Escalar modelo para sub-teams

---

## Referências

- Colin Bryar & Bill Carr: "Working Backwards" — WBR chapter detalhado
- John Rossman: "The Amazon Way" — operational mechanisms
- DORA: "Accelerate" — métricas de engineering performance
- Marty Cagan: "Empowered" — product metrics frameworks

---

*Última atualização: Março 2026*
*Categoria: Operating Reviews | Nível: C-Level | Formato: Examples + Framework*
