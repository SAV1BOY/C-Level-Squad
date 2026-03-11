# Analise de Variacao Orcamentaria

## Objetivo

Comparar sistematicamente resultados financeiros reais com o orcamento aprovado,
identificar causas raiz de desvios materiais e tomar acoes corretivas tempestivas
para manter a execucao financeira alinhada ao plano estrategico.

## Frequencia

- **Analise mensal completa**: Todas as linhas do P&L (ate D+7)
- **Flash report semanal**: Linhas de maior variabilidade (receita, marketing)
- **Deep dive trimestral**: Analise de tendencias e ajuste de forecast
- **Re-forecast**: Trimestral com base nas variacoes observadas

## Processo Detalhado

### Passo 1: Coleta de Dados (Dia 1-3 do mes)

- [ ] Confirmar fechamento contabil do mes anterior (controller)
- [ ] Extrair P&L realizado por departamento, centro de custo e linha
- [ ] Importar budget aprovado para o mesmo periodo e granularidade
- [ ] Calcular variacoes absolutas (R$) e percentuais (%)
- [ ] Preparar base comparativa (mes anterior e mesmo mes ano anterior)

### Passo 2: Calculo de Variacoes (Dia 3-4)

Para cada linha do P&L:
```
Variacao Absoluta = Real - Budget
Variacao % = (Real - Budget) / Budget x 100%
```

Classificacao:
- **Favoravel (F)**: Real melhor que budget (receita acima OU custo abaixo)
- **Desfavoravel (D)**: Real pior que budget (receita abaixo OU custo acima)

### Passo 3: Analise de Materialidade (Dia 4)

Nem toda variacao merece investigacao. Filtrar por materialidade:

| Tamanho da Linha | Threshold de Investigacao |
|------------------|--------------------------|
| > R$ 500K/mes | Variacao > 5% |
| R$ 100K-500K/mes | Variacao > 10% |
| R$ 50K-100K/mes | Variacao > 15% |
| < R$ 50K/mes | Variacao > 25% |

### Passo 4: Root Cause Analysis (Dia 4-5)

Para cada variacao material, investigar sistematicamente:

- [ ] **Timing**: O gasto/receita vai acontecer, mas em outro mes?
- [ ] **Volume**: Mais ou menos atividade que o planejado?
- [ ] **Preco**: Custo unitario diferente do planejado (inflacao, cambio)?
- [ ] **Mix**: Composicao diferente do planejado (produtos, segmentos)?
- [ ] **One-time**: Evento nao-recorrente que nao se repetira?
- [ ] **Estrutural**: Mudanca permanente que afeta meses futuros?

### Passo 5: Acao e Comunicacao (Dia 5-7)

- [ ] Documentar explicacao para cada variacao material
- [ ] Classificar cada variacao: temporaria vs estrutural
- [ ] Propor acoes corretivas para variacoes desfavoraveis estruturais
- [ ] Atualizar forecast para meses restantes do ano
- [ ] Preparar report para lideranca e apresentar em reuniao

## Template de Report

```
ANALISE DE VARIACAO ORCAMENTARIA - [MES/ANO]
Preparado por: [FP&A] | Revisado por: [CFO]

RESUMO EXECUTIVO
Receita: R$ X real vs R$ Y budget (variacao: +/-Z%)
Despesa Operacional: R$ X real vs R$ Y budget (variacao: +/-Z%)
EBITDA: R$ X real vs R$ Y budget (variacao: +/-Z%)
Cash Flow Operacional: R$ X real vs R$ Y budget

P&L RESUMIDO COM VARIACOES
| Linha          | Budget | Real   | Var R$ | Var % | F/D | Comentario        |
|---------------|--------|--------|--------|-------|-----|-------------------|
| Receita Total |        |        |        |       |     |                   |
|   Recorrente  |        |        |        |       |     |                   |
|   Servicos    |        |        |        |       |     |                   |
| (-) COGS      |        |        |        |       |     |                   |
| = Margem Bruta|        |        |        |       |     |                   |
| (-) S&M       |        |        |        |       |     |                   |
| (-) R&D       |        |        |        |       |     |                   |
| (-) G&A       |        |        |        |       |     |                   |
| = EBITDA      |        |        |        |       |     |                   |

VARIACOES MATERIAIS (TOP 5)
1. [Linha]: R$ X variacao - [Causa raiz] - [Temporaria/Estrutural] - [Acao]
2. [Linha]: R$ X variacao - [Causa raiz] - [Temporaria/Estrutural] - [Acao]
3. [Linha]: R$ X variacao - [Causa raiz] - [Temporaria/Estrutural] - [Acao]
4. [Linha]: R$ X variacao - [Causa raiz] - [Temporaria/Estrutural] - [Acao]
5. [Linha]: R$ X variacao - [Causa raiz] - [Temporaria/Estrutural] - [Acao]

IMPACTO NO FORECAST ANUAL
Budget anual original: R$ X
Forecast atualizado: R$ Y
Diferenca: R$ Z (+/-W%)
Principais drivers da mudanca: [lista]

ACOES CORRETIVAS
1. [Acao] - [Owner] - [Deadline] - [Impacto esperado]
2. [Acao] - [Owner] - [Deadline] - [Impacto esperado]
```

## Analise de Tendencias (Trimestral)

### Year-to-Date (YTD) Analysis

- [ ] Acumular variacoes desde o inicio do ano fiscal
- [ ] Identificar linhas com variacao persistente (nao apenas timing)
- [ ] Calcular run-rate para projetar ano completo
- [ ] Comparar run-rate com budget anual
- [ ] Identificar se ha mudanca estrutural no modelo

### Tipos de Variacao

#### Variacao de Volume
```
Volume Variance = (Volume Real - Volume Budget) x Preco Budget
```
Exemplo: Vendemos 120 assinaturas vs 100 planejadas, a R$ 500 cada
Volume variance = (120-100) x R$ 500 = R$ 10.000 favoravel

#### Variacao de Preco
```
Price Variance = (Preco Real - Preco Budget) x Volume Real
```
Exemplo: Preco medio foi R$ 450 vs R$ 500 planejado, com 120 vendas
Price variance = (R$ 450-R$ 500) x 120 = -R$ 6.000 desfavoravel

#### Variacao de Mix
Quando o mix de produtos/servicos difere do planejado, afetando
margem media mesmo com volume e preco similares.

#### Variacao de Eficiencia
Mais ou menos recursos consumidos por unidade de output.
Exemplo: Custo de cloud por transacao 20% maior que planejado.

## Automacao e Ferramentas

### Dashboard Automatizado
- [ ] Conectar ERP/sistema contabil ao dashboard (Looker, Power BI, Metabase)
- [ ] Budget importado como dataset estatico no inicio do ano
- [ ] Variacoes calculadas automaticamente ao fechar o mes
- [ ] Alertas automaticos para variacoes acima do threshold de materialidade
- [ ] Drill-down por departamento, centro de custo e linha contabil

### Processo Semi-Automatizado
- [ ] ETL mensal de dados contabeis para ferramenta de analise
- [ ] Template de analise pre-preenchido com calculos automaticos
- [ ] Comentarios e acoes sao manuais (requerem julgamento humano)
- [ ] Report final gerado automaticamente apos input dos comentarios

## Erros Comuns a Evitar

1. **Analisar tudo com mesma profundidade**: Foco em variacoes materiais
2. **Confundir timing com tendencia**: Gasto adiado nao e economia real
3. **Nao atualizar o forecast**: Se o real diverge, o forecast deve refletir
4. **Tratar budget como meta rigida**: E um plano, circunstancias mudam
5. **Culpar departamentos por variacoes**: Objetivo e entender, nao punir
6. **Ignorar variacoes favoraveis**: Receita acima tambem merece analise
7. **Nao conectar variacao a acao**: Toda variacao material precisa de resposta
