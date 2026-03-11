# Forecast de Fluxo de Caixa

> Processo estruturado para projetar entradas e saídas de caixa, garantindo
> que a empresa tenha liquidez suficiente para operar e investir.

## Objetivo

Antecipar necessidades de caixa, evitar surpresas de liquidez, otimizar
a gestão de capital de giro e informar decisões de investimento, captação
e distribuição de recursos.

## Frequência

- **Rolling forecast:** Semanal (13 semanas à frente)
- **Forecast mensal:** Mensal (12 meses à frente)
- **Forecast de longo prazo:** Trimestral (3-5 anos)
- **Atualização de cenários:** Quando premissas mudam significativamente

## Modelo de 13 Semanas (Rolling Weekly)

### Entradas de Caixa
- [ ] **Recebimentos de clientes:** Baseado em AR aging e termos de pagamento
- [ ] **Receita recorrente (MRR):** Previsível com base em base ativa
- [ ] **Receita não-recorrente:** Projetos, serviços profissionais
- [ ] **Outras entradas:** Juros sobre investimentos, tax refunds, incentivos

### Saídas de Caixa
- [ ] **Folha de pagamento:** Salários, bônus, encargos (previsível)
- [ ] **Fornecedores:** AP aging e compromissos futuros
- [ ] **Infraestrutura/Cloud:** Baseado em uso projetado
- [ ] **Aluguel e facilities:** Fixo e previsível
- [ ] **Impostos:** Baseado em cronograma fiscal
- [ ] **Capex:** Investimentos planejados
- [ ] **Debt service:** Juros e amortização de dívidas

### Template Semanal

```
CASH FLOW FORECAST - 13 SEMANAS
Preparado por: [Nome] | Data: [Data]

                    | Sem 1 | Sem 2 | ... | Sem 13 | Total
SALDO INICIAL       |       |       |     |        |
                    |       |       |     |        |
ENTRADAS            |       |       |     |        |
  Recebimentos      |       |       |     |        |
  MRR/ARR           |       |       |     |        |
  Outras            |       |       |     |        |
TOTAL ENTRADAS      |       |       |     |        |
                    |       |       |     |        |
SAÍDAS              |       |       |     |        |
  Folha             |       |       |     |        |
  Fornecedores      |       |       |     |        |
  Infra/Cloud       |       |       |     |        |
  Impostos          |       |       |     |        |
  Outros            |       |       |     |        |
TOTAL SAÍDAS        |       |       |     |        |
                    |       |       |     |        |
FLUXO LÍQUIDO       |       |       |     |        |
SALDO FINAL         |       |       |     |        |
                    |       |       |     |        |
RUNWAY (semanas)    |       |       |     |        |
```

## Modelo de 12 Meses (Monthly)

### Premissas-Chave
- [ ] Taxa de crescimento de receita (mensal/trimestral)
- [ ] Churn rate projetado
- [ ] Headcount plan (contratações por mês)
- [ ] Reajustes salariais planejados
- [ ] Investimentos de capital previstos
- [ ] Sazonalidade do negócio
- [ ] Condições de pagamento de clientes e fornecedores

### Cenários
Manter pelo menos 3 cenários:

**Base (probabilidade 60%):**
- Crescimento conforme forecast de vendas
- Custos conforme budget aprovado
- Sem eventos extraordinários

**Otimista (probabilidade 20%):**
- Crescimento 20% acima do base
- Fechamento de deals grandes no pipeline
- Eficiências operacionais realizadas

**Pessimista (probabilidade 20%):**
- Crescimento 30% abaixo do base
- Perda de clientes acima do esperado
- Atrasos em recebíveis
- Custos inesperados materializados

## Métricas de Cash Flow

### Operacionais
- **Cash Conversion Cycle:** DSO + DIO - DPO
- **DSO (Days Sales Outstanding):** Tempo para receber de clientes
- **DPO (Days Payable Outstanding):** Tempo para pagar fornecedores
- **Burn Rate:** Cash consumido por mês (se negativo)
- **Runway:** Meses de operação com caixa atual (cash / burn rate)

### Eficiência
- **Free Cash Flow:** Cash from operations - Capex
- **Cash Flow Margin:** Free Cash Flow / Receita
- **Working Capital Ratio:** Current Assets / Current Liabilities

### Alertas
| Métrica | Amarelo | Vermelho | Ação |
|---------|---------|----------|------|
| Runway | < 12 meses | < 6 meses | Iniciar captação ou cortes |
| DSO | > 60 dias | > 90 dias | Política de cobrança agressiva |
| Cash Flow negativo | 2 meses consecutivos | 3 meses consecutivos | Review de despesas |

## Processo Semanal

### Segunda-feira
- [ ] Atualizar posição de caixa real (saldos bancários)
- [ ] Comparar semana anterior: real vs forecast
- [ ] Atualizar forecast para próximas 13 semanas
- [ ] Identificar variações significativas

### Terça-feira
- [ ] Distribuir report para CFO e CEO
- [ ] Destacar riscos e oportunidades
- [ ] Propor ações se necessário

## Otimização de Capital de Giro

### Acelerar Recebimentos
- Faturamento imediato após entrega/ativação
- Incentivos para pagamento antecipado (desconto de 2% para 10 dias)
- Cobrança proativa de inadimplentes
- Pagamento via cartão de crédito (recebimento mais rápido)

### Otimizar Pagamentos
- Negociar prazos maiores com fornecedores
- Não pagar antes do vencimento (sem motivo)
- Consolidar pagamentos para reduzir custos bancários
- Avaliar financiamento de fornecedores quando custo é menor que capital

### Gestão de Estoque (se aplicável)
- Just-in-time onde possível
- Identificar itens de baixo giro
- Negociar consignação

## Comunicação

### Para o CEO (Semanal)
- Posição de caixa atual
- Runway atualizado
- Top 3 riscos de liquidez
- Ações recomendadas

### Para o Board (Mensal/Trimestral)
- Cash flow statement (realizado)
- Forecast de 12 meses (3 cenários)
- Runway e métricas de eficiência
- Necessidades de capital projetadas

### Para Investidores
- Cash position no início e fim do período
- Burn rate trend
- Runway e triggers para próxima captação
- Uso de capital vs plano apresentado

## Referências

- "Financial Intelligence" - Karen Berman & Joe Knight
- "The Essentials of Finance and Accounting" - Edward Fields
- "Venture Deals" - Brad Feld & Jason Mendelson (capítulo de cash management)
- SaaS CFO resources (saascfo.com)
