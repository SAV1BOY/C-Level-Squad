# Análise de Variação Orçamentária

> Processo estruturado para comparar resultados reais com orçamento aprovado,
> identificar causas de desvios e tomar ações corretivas quando necessário.

## Objetivo

Garantir que a execução financeira está alinhada com o plano, identificar
desvios cedo para correção de curso, e alimentar o processo de re-forecast
com dados reais.

## Frequência

- **Análise mensal:** Completa, todas as linhas
- **Flash report:** Semanal para linhas de maior variabilidade
- **Deep dive:** Trimestral para análise de tendências
- **Re-forecast:** Trimestral com base nas variações observadas

## Processo

### Passo 1: Coleta de Dados (Dia 1-3 do mês)
- [ ] Fechar contabilidade do mês anterior
- [ ] Extrair P&L realizado por departamento e linha
- [ ] Importar budget aprovado para o mesmo período
- [ ] Calcular variações absolutas e percentuais

### Passo 2: Cálculo de Variações (Dia 3-4)
Para cada linha do P&L:

```
Variação Absoluta = Real - Budget
Variação % = (Real - Budget) / Budget × 100%
```

Classificação:
- **Favorável:** Real melhor que budget (receita acima ou custo abaixo)
- **Desfavorável:** Real pior que budget (receita abaixo ou custo acima)

### Passo 3: Análise de Materialidade (Dia 4)
Nem toda variação merece atenção. Filtrar por materialidade:

| Tamanho da Linha | Threshold de Investigação |
|------------------|--------------------------|
| > $100K/mês | Variação > 5% |
| $50K-$100K/mês | Variação > 10% |
| $10K-$50K/mês | Variação > 15% |
| < $10K/mês | Variação > 25% |

### Passo 4: Root Cause Analysis (Dia 4-5)
Para cada variação material, investigar:

- [ ] **Timing:** O gasto/receita vai acontecer, mas em outro mês?
- [ ] **Volume:** Mais/menos atividade que o planejado?
- [ ] **Preço:** Custo unitário diferente do planejado?
- [ ] **Mix:** Composição diferente do planejado?
- [ ] **One-time:** Evento não-recorrente?
- [ ] **Structural:** Mudança permanente vs temporária?

### Passo 5: Ação e Comunicação (Dia 5-7)
- [ ] Documentar explicação para cada variação material
- [ ] Propor ações corretivas quando aplicável
- [ ] Atualizar forecast para meses restantes
- [ ] Preparar report para liderança

## Template de Report

```
BUDGET VARIANCE ANALYSIS - [MÊS/ANO]

RESUMO
Receita: $X real vs $Y budget (variação: +/-Z%)
Despesa: $X real vs $Y budget (variação: +/-Z%)
EBITDA: $X real vs $Y budget (variação: +/-Z%)

P&L RESUMIDO COM VARIAÇÕES
| Linha | Budget | Real | Var $ | Var % | F/D | Comentário |
|-------|--------|------|-------|-------|-----|------------|
| Receita Total | | | | | | |
| COGS | | | | | | |
| Margem Bruta | | | | | | |
| S&M | | | | | | |
| R&D | | | | | | |
| G&A | | | | | | |
| EBITDA | | | | | | |

F = Favorável, D = Desfavorável

VARIAÇÕES MATERIAIS
1. [Linha]: [variação] - [causa] - [ação]
2. [Linha]: [variação] - [causa] - [ação]
3. [Linha]: [variação] - [causa] - [ação]

IMPACTO NO FORECAST ANUAL
Budget anual original: $X
Forecast atualizado: $Y
Diferença: $Z (+/-W%)

AÇÕES RECOMENDADAS
1. [Ação] - [Owner] - [Deadline]
2. [Ação] - [Owner] - [Deadline]
```

## Análise de Tendências (Trimestral)

### YTD (Year-to-Date) Analysis
- [ ] Acumular variações desde o início do ano
- [ ] Identificar linhas com variação persistente (não timing)
- [ ] Calcular run-rate para projetar ano completo
- [ ] Comparar run-rate com budget anual

### Trend Analysis
- [ ] Plotar real vs budget mês a mês (gráfico)
- [ ] Identificar padrões (sazonal? crescente? decrescente?)
- [ ] Para tendências claras, ajustar forecast
- [ ] Comunicar tendências que afetam decisões estratégicas

## Tipos de Variação

### Variação de Volume
```
Volume Variance = (Volume Real - Volume Budget) × Preço Budget
```
Exemplo: Vendemos 100 unidades vs 80 planejadas, a $50 cada
Volume variance = (100-80) × $50 = $1.000 favorável

### Variação de Preço
```
Price Variance = (Preço Real - Preço Budget) × Volume Real
```
Exemplo: Preço médio foi $45 vs $50 planejado, com 100 unidades
Price variance = ($45-$50) × 100 = -$500 desfavorável

### Variação de Mix
Quando o mix de produtos/serviços difere do planejado,
afetando margem média mesmo com volume e preço similares.

### Variação de Eficiência
Mais/menos recursos consumidos por unidade de output.
Exemplo: Custo de cloud por transação maior que planejado.

## Automação

### Dashboards Automatizados
- [ ] Conectar sistema contábil ao dashboard (Looker, Power BI)
- [ ] Budget importado como dataset estático
- [ ] Variações calculadas automaticamente
- [ ] Alertas automáticos para variações > threshold

### Processo Semi-Automatizado
- [ ] ETL mensal de dados contábeis
- [ ] Template de análise pré-preenchido
- [ ] Comentários e ações são manuais (requerem julgamento)
- [ ] Report gerado automaticamente após input de comentários

## Erros Comuns

1. **Analisar tudo com mesma profundidade** - Foco em variações materiais
2. **Confundir timing com tendência** - Gasto adiado não é economia
3. **Não atualizar forecast** - Se o real diverge, o forecast deve mudar
4. **Budget como meta rígida** - É um plano, não uma lei; circunstâncias mudam
5. **Culpar departamentos** - Variação deve gerar entendimento, não punição
6. **Ignorar variações favoráveis** - Receita acima do budget também merece análise

## Referências

- "Financial Intelligence" - Karen Berman & Joe Knight
- "Budgeting and Financial Management for Nonprofit Organizations" - Maddox
- "The CFO Guidebook" - Steven Bragg
- Adaptive Planning best practices
