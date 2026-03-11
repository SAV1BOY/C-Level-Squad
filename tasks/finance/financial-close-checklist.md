# Checklist de Fechamento Financeiro

> Processo estruturado para o fechamento contábil mensal, garantindo que os
> números estão corretos, completos e disponíveis para tomada de decisão
> no prazo adequado.

## Objetivo

Fechar os livros contábeis de forma precisa e tempestiva, produzindo
demonstrações financeiras confiáveis que suportem decisões de gestão,
compliance regulatório e comunicação com investidores.

## Timeline de Fechamento

### Target: Fechamento em 5 Dias Úteis (D+5)

| Dia | Atividade Principal |
|-----|-------------------|
| D+1 | Corte de período e reconciliações bancárias |
| D+2 | Reconciliação de receitas e contas a receber |
| D+3 | Reconciliação de despesas e contas a pagar |
| D+4 | Accruals, provisões e ajustes |
| D+5 | Revisão final, geração de reports, aprovação |

## Dia 1: Corte e Bancos

### Corte de Período
- [ ] Confirmar que todas as transações do mês estão registradas
- [ ] Verificar que nenhuma transação do mês seguinte foi antecipada
- [ ] Confirmar corte de notas fiscais emitidas e recebidas
- [ ] Verificar recebimentos de last-minute processados corretamente

### Reconciliação Bancária
- [ ] Baixar extratos de todas as contas bancárias
- [ ] Reconciliar cada conta: saldo do banco vs saldo contábil
- [ ] Identificar e investigar itens pendentes
- [ ] Documentar itens de reconciliação em aberto com justificativa
- [ ] Confirmar que investimentos e aplicações estão corretos

### Caixa e Equivalentes
- [ ] Confirmar posições em contas correntes
- [ ] Confirmar posições em aplicações financeiras
- [ ] Calcular rendimentos a apropriar
- [ ] Atualizar posição consolidada de caixa

## Dia 2: Receitas e Contas a Receber

### Reconhecimento de Receita
- [ ] Confirmar receita recorrente (MRR) do período
- [ ] Reconhecer receita de novos contratos conforme critério (CPC 47/IFRS 15)
- [ ] Tratar upgrades, downgrades e cancelamentos do mês
- [ ] Reconhecer receita de serviços profissionais (se houver)
- [ ] Confirmar receita diferida (deferred revenue) está correta
- [ ] Reconciliar receita com sistema de billing

### Contas a Receber
- [ ] Atualizar aging de contas a receber
- [ ] Provisionar perdas esperadas (PECLD)
- [ ] Baixar inadimplentes irrecuperáveis
- [ ] Reconciliar AR com sistema de billing
- [ ] Verificar recebimentos pós-fechamento mas referentes ao mês

### Impostos sobre Receita
- [ ] Calcular ISS, ICMS, PIS, COFINS (conforme aplicável)
- [ ] Verificar retenções na fonte
- [ ] Reconciliar impostos com notas fiscais

## Dia 3: Despesas e Contas a Pagar

### Contas a Pagar
- [ ] Confirmar que todas as notas de fornecedores foram registradas
- [ ] Verificar notas recebidas após o corte que se referem ao mês
- [ ] Reconciliar AP com sistema de compras
- [ ] Aprovar lançamentos acima de threshold

### Folha de Pagamento
- [ ] Confirmar cálculo da folha (salários, benefícios, encargos)
- [ ] Provisionar 13° salário e férias proporcionais
- [ ] Registrar comissões e bônus do período
- [ ] Reconciliar com FGTS, INSS, IRRF
- [ ] Verificar stock compensation expense (se houver)

### Despesas por Categoria
- [ ] Infraestrutura/Cloud: reconciliar com faturas (AWS, GCP, etc.)
- [ ] SaaS/Ferramentas: confirmar assinaturas ativas vs registradas
- [ ] Marketing: reconciliar gastos com plataformas (Google Ads, etc.)
- [ ] Viagens: confirmar reembolsos e cartão corporativo
- [ ] Serviços profissionais: confirmar faturas de consultorias

### Classificação Contábil
- [ ] Despesas classificadas na conta correta (COGS vs Opex)
- [ ] Capex separado de Opex adequadamente
- [ ] Centros de custo atribuídos corretamente
- [ ] Reclassificar itens incorretos

## Dia 4: Accruals, Provisões e Ajustes

### Accruals (Competência)
- [ ] Apropriar despesas incorridas mas não faturadas
- [ ] Apropriar receitas reconhecidas mas não faturadas
- [ ] Reverter accruals do mês anterior que se realizaram
- [ ] Documentar base de cálculo de cada accrual

### Provisões
- [ ] Atualizar provisão para contingências trabalhistas
- [ ] Atualizar provisão para contingências fiscais
- [ ] Atualizar provisão para perdas com clientes
- [ ] Revisar adequação de cada provisão com jurídico

### Depreciação e Amortização
- [ ] Calcular depreciação de ativos fixos
- [ ] Calcular amortização de intangíveis
- [ ] Calcular amortização de SaaS capitalizado (se houver)
- [ ] Verificar se algum ativo deve ser impaired

### Ajustes de Câmbio (se houver operação internacional)
- [ ] Atualizar saldos em moeda estrangeira pela taxa de fechamento
- [ ] Registrar variação cambial
- [ ] Reconciliar contas intercompany

### Impostos
- [ ] Calcular imposto de renda e CSLL (corrente e diferido)
- [ ] Verificar créditos tributários a apropriar
- [ ] Reconciliar posição fiscal acumulada

## Dia 5: Revisão e Finalização

### Revisão de Qualidade
- [ ] Analytical review: comparar P&L com mês anterior e mesmo mês YoY
- [ ] Identificar anomalias (variações > 20% sem explicação)
- [ ] Verificar integridade do balancete (ativo = passivo + PL)
- [ ] Confirmar que intercompany está eliminado (se consolidação)

### Geração de Demonstrações
- [ ] P&L (Demonstração de Resultado)
- [ ] Balanço Patrimonial
- [ ] Fluxo de Caixa (DFC)
- [ ] Report gerencial por departamento
- [ ] Dashboard de métricas-chave

### Aprovação
- [ ] Controller/Contador revisa e aprova
- [ ] CFO revisa highlights e anomalias
- [ ] Documentar qualquer item em aberto para o próximo mês
- [ ] Comunicar que o fechamento está completo

### Distribuição
- [ ] Enviar P&L e dashboard para C-level
- [ ] Atualizar dashboard de métricas
- [ ] Alimentar processo de budget variance analysis
- [ ] Arquivar documentação de suporte

## Melhoria Contínua

### Métricas do Processo de Fechamento
- Dias para fechar (target: D+5)
- Número de ajustes pós-fechamento
- Número de itens de reconciliação em aberto
- Horas totais gastas no fechamento

### Automação
- [ ] Reconciliação bancária automatizada
- [ ] Importação de faturas de cloud/SaaS automatizada
- [ ] Cálculos de depreciação/amortização automatizados
- [ ] Geração de reports automatizada
- [ ] Alertas para itens pendentes automatizados

### Evolução de Maturidade
| Nível | Fechamento | Automação | Qualidade |
|-------|-----------|-----------|-----------|
| 1 | D+15 | Manual | Erros frequentes |
| 2 | D+10 | Parcial | Erros ocasionais |
| 3 | D+5 | Maioria automática | Raro erro |
| 4 | D+3 | Quase tudo automático | Excepcional |
| 5 | D+1 | Continuous close | Real-time |

## Referências

- CPC (Comitê de Pronunciamentos Contábeis) - pronunciamentos técnicos
- "Financial Reporting and Analysis" - Lawrence Revsine et al.
- "The CFO Guidebook" - Steven Bragg
- BlackLine/FloQast best practices para close management
