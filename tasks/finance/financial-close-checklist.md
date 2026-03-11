# Checklist de Fechamento Financeiro Mensal

## Objetivo

Garantir um fechamento contabil mensal preciso, completo e tempestivo, produzindo
demonstracoes financeiras confiaveis que suportem decisoes de gestao, compliance
regulatorio e comunicacao com investidores e stakeholders.

## Timeline de Fechamento

### Target: Fechamento em 5 Dias Uteis (D+5)

| Dia | Atividade Principal | Responsavel |
|-----|-------------------|-------------|
| D+1 | Corte de periodo e reconciliacoes bancarias | Tesouraria |
| D+2 | Reconciliacao de receitas e contas a receber | Revenue Accounting |
| D+3 | Reconciliacao de despesas e contas a pagar | AP + Controladoria |
| D+4 | Accruals, provisoes e ajustes de competencia | Controladoria |
| D+5 | Revisao final, geracao de reports, aprovacao | Controller + CFO |

## Dia 1: Corte de Periodo e Bancos

### Corte de Periodo
- [ ] Confirmar que todas as transacoes do mes estao registradas no ERP
- [ ] Verificar que nenhuma transacao do mes seguinte foi antecipada
- [ ] Confirmar corte de notas fiscais emitidas e recebidas
- [ ] Verificar recebimentos de ultimo dia processados corretamente
- [ ] Bloquear lancamentos no periodo anterior no sistema

### Reconciliacao Bancaria
- [ ] Baixar extratos de todas as contas bancarias (corrente, investimento)
- [ ] Reconciliar cada conta: saldo do banco vs saldo contabil
- [ ] Identificar e investigar itens pendentes de reconciliacao
- [ ] Documentar itens em aberto com justificativa e prazo de resolucao
- [ ] Confirmar posicoes em aplicacoes financeiras e rendimentos
- [ ] Atualizar posicao consolidada de caixa para report de tesouraria

## Dia 2: Receitas e Contas a Receber

### Reconhecimento de Receita
- [ ] Confirmar receita recorrente (MRR) do periodo com sistema de billing
- [ ] Reconhecer receita de novos contratos conforme CPC 47/IFRS 15
- [ ] Tratar upgrades, downgrades e cancelamentos do mes
- [ ] Reconhecer receita de servicos profissionais e implementacao
- [ ] Confirmar receita diferida (deferred revenue) correta no balanco
- [ ] Reconciliar receita contabil com sistema de billing (zero gap)

### Contas a Receber
- [ ] Atualizar aging de contas a receber (current, 30, 60, 90+ dias)
- [ ] Provisionar perdas esperadas com credito de liquidacao duvidosa (PECLD)
- [ ] Baixar inadimplentes irrecuperaveis (com aprovacao do controller)
- [ ] Reconciliar AR total com sistema de billing e CRM
- [ ] Verificar recebimentos pos-fechamento referentes ao mes

### Impostos sobre Receita
- [ ] Calcular ISS sobre receita de servicos
- [ ] Calcular PIS e COFINS sobre faturamento
- [ ] Verificar retencoes na fonte realizadas por clientes
- [ ] Reconciliar impostos calculados com notas fiscais emitidas

## Dia 3: Despesas e Contas a Pagar

### Contas a Pagar
- [ ] Confirmar que todas as notas de fornecedores foram registradas
- [ ] Verificar notas recebidas apos o corte que se referem ao mes
- [ ] Reconciliar AP com sistema de compras e contratos vigentes
- [ ] Aprovar lancamentos acima do threshold definido (ex: R$ 10K)

### Folha de Pagamento
- [ ] Confirmar calculo da folha (salarios, beneficios, encargos completos)
- [ ] Provisionar 13o salario e ferias proporcionais (1/12 avos)
- [ ] Registrar comissoes e bonus do periodo conforme politica
- [ ] Reconciliar com guias de FGTS, INSS e IRRF
- [ ] Verificar stock compensation expense se houver plano de opcoes

### Despesas por Categoria
- [ ] Infraestrutura/Cloud: reconciliar com faturas AWS, GCP, Azure
- [ ] SaaS/Ferramentas: confirmar assinaturas ativas vs registradas
- [ ] Marketing: reconciliar gastos com plataformas (Google, Meta, LinkedIn)
- [ ] Viagens: confirmar reembolsos pendentes e cartao corporativo
- [ ] Servicos profissionais: confirmar faturas de consultorias e advogados

### Classificacao Contabil
- [ ] Despesas classificadas na conta correta (COGS vs Opex)
- [ ] CAPEX separado de Opex adequadamente (criterio de capitalizacao)
- [ ] Centros de custo atribuidos corretamente por departamento
- [ ] Reclassificar itens incorretos identificados na revisao

## Dia 4: Accruals, Provisoes e Ajustes

### Accruals (Regime de Competencia)
- [ ] Apropriar despesas incorridas mas ainda nao faturadas
- [ ] Apropriar receitas reconhecidas mas ainda nao faturadas
- [ ] Reverter accruals do mes anterior que se realizaram
- [ ] Documentar base de calculo e justificativa de cada accrual

### Provisoes
- [ ] Atualizar provisao para contingencias trabalhistas (com juridico)
- [ ] Atualizar provisao para contingencias fiscais e tributarias
- [ ] Atualizar provisao para perdas com clientes (PECLD)
- [ ] Revisar adequacao de cada provisao com departamento juridico

### Depreciacao e Amortizacao
- [ ] Calcular depreciacao de ativos fixos (imobilizado)
- [ ] Calcular amortizacao de intangiveis (software, patentes)
- [ ] Calcular amortizacao de custos de aquisicao diferidos (se aplicavel)
- [ ] Verificar se algum ativo deve sofrer impairment

### Ajustes de Cambio (se houver operacao internacional)
- [ ] Atualizar saldos em moeda estrangeira pela taxa de fechamento PTAX
- [ ] Registrar variacao cambial realizada e nao-realizada
- [ ] Reconciliar contas intercompany se houver subsidiarias

### Impostos sobre Resultado
- [ ] Calcular IRPJ e CSLL (corrente e diferido)
- [ ] Verificar creditos tributarios a apropriar (prejuizo fiscal, incentivos)
- [ ] Reconciliar posicao fiscal acumulada no ano

## Dia 5: Revisao Final e Aprovacao

### Revisao de Qualidade
- [ ] Analytical review: comparar P&L com mes anterior e mesmo mes YoY
- [ ] Investigar anomalias (variacoes >20% sem explicacao documentada)
- [ ] Verificar integridade do balancete (Ativo = Passivo + PL)
- [ ] Confirmar eliminacao intercompany se houver consolidacao
- [ ] Validar consistencia entre DRE, Balanco e DFC

### Geracao de Demonstracoes
- [ ] DRE (Demonstracao de Resultado do Exercicio) - mensal e acumulado
- [ ] Balanco Patrimonial completo
- [ ] DFC (Demonstracao de Fluxo de Caixa) pelo metodo indireto
- [ ] Report gerencial por departamento e centro de custo
- [ ] Dashboard de metricas-chave para C-Level

### Aprovacao e Distribuicao
- [ ] Controller revisa e assina o fechamento
- [ ] CFO revisa highlights, anomalias e riscos
- [ ] Documentar itens em aberto para resolucao no proximo mes
- [ ] Comunicar que o fechamento esta completo para todas as areas
- [ ] Enviar P&L e dashboard para C-Level e board
- [ ] Alimentar processo de budget variance analysis
- [ ] Arquivar documentacao de suporte (digital, organizado)

## Melhoria Continua

### Metricas do Processo de Fechamento

| Metrica | Meta D+5 | Meta D+3 | Classe Mundial |
|---------|----------|----------|---------------|
| Dias para fechar | 5 | 3 | 1 (continuous close) |
| Ajustes pos-fechamento | <3 | <1 | 0 |
| Itens reconciliacao abertos | <10 | <5 | 0 |
| Horas totais gastas | <80h | <40h | <20h |
| Erros identificados em auditoria | <5 | <2 | 0 |

### Automacao Progressiva
- [ ] Reconciliacao bancaria automatizada (integracao Open Banking)
- [ ] Importacao de faturas de cloud/SaaS via API automatizada
- [ ] Calculos de depreciacao/amortizacao automatizados no ERP
- [ ] Geracao de reports e dashboards automatizada
- [ ] Alertas automaticos para itens pendentes e prazos
- [ ] Validacoes automaticas de consistencia pre-fechamento
