# Forecast de Fluxo de Caixa

## Objetivo

Projetar entradas e saidas de caixa de forma sistematica, garantindo que a empresa
mantenha liquidez suficiente para operar, investir e crescer, antecipando necessidades
de capital e evitando surpresas financeiras.

## Frequencia e Cadencia

- **Rolling forecast semanal**: 13 semanas a frente (visao operacional)
- **Forecast mensal**: 12 meses a frente (visao tatica)
- **Forecast de longo prazo**: Trimestral, 3-5 anos (visao estrategica)
- **Atualizacao de cenarios**: Quando premissas mudam significativamente

## Modelo de 13 Semanas (Rolling Weekly)

### Componentes de Entrada de Caixa

- [ ] **Recebimentos de clientes**: Baseado em AR aging e termos de pagamento
- [ ] **Receita recorrente (MRR/ARR)**: Previsivel com base em base ativa e churn
- [ ] **Receita nao-recorrente**: Projetos, servicos profissionais, implementacao
- [ ] **Outras entradas**: Juros sobre aplicacoes, restituicoes fiscais, incentivos
- [ ] **Aportes de capital**: Rodadas de investimento, emprestimos programados

### Componentes de Saida de Caixa

- [ ] **Folha de pagamento**: Salarios, bonus, encargos (INSS, FGTS, IRRF)
- [ ] **Fornecedores**: AP aging e compromissos futuros confirmados
- [ ] **Infraestrutura/Cloud**: Baseado em uso projetado (AWS, GCP, Azure)
- [ ] **Aluguel e facilities**: Custos fixos previsiveis
- [ ] **Impostos**: Cronograma fiscal (ISS, PIS, COFINS, IR, CSLL)
- [ ] **CAPEX**: Investimentos planejados em equipamentos e tecnologia
- [ ] **Dividas**: Juros e amortizacao de emprestimos e debentures

### Template Semanal

```
FORECAST DE FLUXO DE CAIXA - 13 SEMANAS
Preparado por: [Nome] | Data: [Data] | Versao: [N]

                    | Sem 1 | Sem 2 | Sem 3 | ... | Sem 13 | Total
SALDO INICIAL       |       |       |       |     |        |
                    |       |       |       |     |        |
ENTRADAS            |       |       |       |     |        |
  Recebimentos      |       |       |       |     |        |
  MRR/ARR           |       |       |       |     |        |
  Servicos          |       |       |       |     |        |
  Outras            |       |       |       |     |        |
TOTAL ENTRADAS      |       |       |       |     |        |
                    |       |       |       |     |        |
SAIDAS              |       |       |       |     |        |
  Folha             |       |       |       |     |        |
  Fornecedores      |       |       |       |     |        |
  Infra/Cloud       |       |       |       |     |        |
  Impostos          |       |       |       |     |        |
  CAPEX             |       |       |       |     |        |
  Dividas           |       |       |       |     |        |
  Outros            |       |       |       |     |        |
TOTAL SAIDAS        |       |       |       |     |        |
                    |       |       |       |     |        |
FLUXO LIQUIDO       |       |       |       |     |        |
SALDO FINAL         |       |       |       |     |        |
RUNWAY (semanas)    |       |       |       |     |        |
```

## Modelo de 12 Meses (Monthly)

### Premissas-Chave

- [ ] Taxa de crescimento de receita (mensal e trimestral)
- [ ] Churn rate projetado por segmento de cliente
- [ ] Headcount plan (contratacoes e desligamentos por mes)
- [ ] Reajustes salariais planejados e dissidio coletivo
- [ ] Investimentos de capital previstos (CAPEX plan)
- [ ] Sazonalidade do negocio (meses de pico e vale)
- [ ] Condicoes de pagamento de clientes e fornecedores
- [ ] Projecao de inadimplencia baseada em historico

### Cenarios Obrigatorios

**Cenario Base (probabilidade 60%)**
- Crescimento conforme forecast de vendas aprovado
- Custos conforme budget aprovado pelo board
- Sem eventos extraordinarios

**Cenario Otimista (probabilidade 20%)**
- Crescimento 20% acima do cenario base
- Fechamento de deals grandes no pipeline com >70% probabilidade
- Eficiencias operacionais realizadas conforme plano

**Cenario Pessimista (probabilidade 20%)**
- Crescimento 30% abaixo do cenario base
- Perda de clientes top 10 acima do esperado
- Atrasos em recebiveis (DSO +15 dias)
- Custos inesperados materializados

## Metricas de Cash Flow

### Metricas Operacionais

| Metrica | Formula | Meta | Alerta |
|---------|---------|------|--------|
| Cash Conversion Cycle | DSO + DIO - DPO | <60 dias | >90 dias |
| DSO | AR / Receita Diaria | <45 dias | >60 dias |
| DPO | AP / Compras Diarias | >30 dias | <15 dias |
| Burn Rate | Cash consumido/mes | Decrescente | Crescente 3 meses |
| Runway | Cash / Burn Rate | >12 meses | <6 meses |
| Free Cash Flow | Cash Operations - CAPEX | Positivo | Negativo 3 meses |
| Working Capital Ratio | Ativo Circ / Passivo Circ | >1.5 | <1.0 |

### Sistema de Alertas

| Metrica | Amarelo | Vermelho | Acao Imediata |
|---------|---------|----------|--------------|
| Runway | <12 meses | <6 meses | Iniciar captacao ou cortes |
| DSO | >60 dias | >90 dias | Politica de cobranca agressiva |
| Cash Flow negativo | 2 meses consecutivos | 3 meses | Review de despesas urgente |
| Concentracao AR | Top 3 >40% | Top 1 >25% | Diversificar base |
| Inadimplencia | >5% | >10% | Revisao de credito |

## Processo Operacional Semanal

### Segunda-feira

- [ ] Atualizar posicao de caixa real (saldos bancarios de todas as contas)
- [ ] Comparar semana anterior: real vs forecast (analise de variancia)
- [ ] Atualizar forecast para proximas 13 semanas com dados reais
- [ ] Identificar variacoes significativas (>10%) e investigar causas

### Terca-feira

- [ ] Distribuir report atualizado para CFO e CEO
- [ ] Destacar riscos e oportunidades de liquidez identificados
- [ ] Propor acoes corretivas se necessario (acelerar cobranca, renegociar prazos)
- [ ] Atualizar dashboard de cash flow no BI

## Otimizacao de Capital de Giro

### Acelerar Recebimentos

- Faturamento imediato apos entrega/ativacao do servico
- Incentivos para pagamento antecipado (desconto de 2% para pagamento em 10 dias)
- Cobranca proativa de inadimplentes (regua de cobranca automatizada)
- Oferecer pagamento via cartao de credito (recebimento mais rapido)
- Antecipar recebiveis quando custo e menor que custo de capital
- Implementar cobranca recorrente automatica (debito automatico, Pix agendado)

### Otimizar Pagamentos

- Negociar prazos maiores com fornecedores (30 para 45-60 dias)
- Nao pagar antes do vencimento sem motivo estrategico
- Consolidar pagamentos para reduzir custos bancarios
- Avaliar financiamento de fornecedores quando custo e menor que capital proprio
- Aproveitar descontos de pagamento antecipado apenas se TIR > custo de capital

### Gestao de Investimentos de Curto Prazo

- Aplicar excedentes em CDB/LCI/LCA com liquidez diaria
- Escalonar aplicacoes para coincidir com necessidades de caixa previstas
- Manter reserva minima de 3 meses de operacao em alta liquidez
- Diversificar entre pelo menos 3 instituicoes financeiras

## Comunicacao de Resultados

### Para o CEO (Semanal)
- Posicao de caixa atual e variacao vs semana anterior
- Runway atualizado nos 3 cenarios
- Top 3 riscos de liquidez com plano de acao
- Acoes recomendadas que requerem decisao executiva

### Para o Board (Mensal/Trimestral)
- Cash flow statement realizado vs budget
- Forecast de 12 meses nos 3 cenarios
- Runway e metricas de eficiencia de capital
- Necessidades de capital projetadas e timeline de captacao

### Para Investidores (Trimestral)
- Cash position no inicio e fim do periodo
- Burn rate trend e comparacao com plano apresentado na captacao
- Runway e triggers para proxima rodada
- Uso de capital vs plano apresentado no memorando de investimento
