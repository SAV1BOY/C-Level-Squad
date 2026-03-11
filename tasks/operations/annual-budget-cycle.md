# Ciclo Orçamentário Anual

> Processo completo de planejamento, aprovação e gestão do orçamento anual
> da empresa, do kick-off ao acompanhamento contínuo.

## Objetivo

Traduzir a estratégia em números. O orçamento é o documento que expressa
as prioridades da empresa em termos financeiros, alocando recursos escassos
para as iniciativas de maior impacto.

## Timeline Típico

| Mês | Atividade | Responsável |
|-----|-----------|-------------|
| T-4 (Set) | Kick-off e guidelines | CFO |
| T-3 (Out) | Bottom-up requests dos departamentos | VPs |
| T-2 (Nov) | Consolidação e primeira iteração | FP&A |
| T-1 (Dez) | Aprovação do board e finalização | CEO + Board |
| T0 (Jan) | Início da execução | Todos |
| T1-T12 | Acompanhamento mensal | FP&A + VPs |

## Fase 1: Kick-off e Guidelines (Mês T-4)

### Preparação do CFO
- [ ] Definir premissas macroeconômicas (inflação, câmbio, juros)
- [ ] Estabelecer cenários (base, otimista, pessimista)
- [ ] Definir growth targets alinhados com board e CEO
- [ ] Preparar template padronizado para submissões
- [ ] Definir guardrails (ex: "opex não pode crescer mais que receita")

### Comunicação
- [ ] Apresentar guidelines em reunião com todos os VPs
- [ ] Distribuir template e instruções
- [ ] Abrir Q&A para dúvidas sobre premissas e processo
- [ ] Definir deadlines para cada etapa

### Guidelines Típicas
- Target de crescimento de receita: X%
- Margem operacional target: Y%
- Headcount growth limit: Z%
- Capex envelope: $W
- R&D como % da receita: máximo V%

## Fase 2: Bottom-Up Requests (Mês T-3)

### Cada VP/Departamento
- [ ] Revisar performance do ano corrente vs budget
- [ ] Projetar base case (manter operação atual) vs growth case
- [ ] Identificar investimentos necessários para atingir metas
- [ ] Priorizar pedidos em tiers: must-have, should-have, nice-to-have
- [ ] Submeter até deadline com justificativa para cada linha

### Categorias de Budget
1. **Headcount:** Novas posições + aumentos + bônus + benefícios
2. **Ferramentas/SaaS:** Software e assinaturas
3. **Infraestrutura:** Servidores, cloud, hardware
4. **Marketing:** Aquisição, brand, eventos
5. **Viagens:** Deslocamentos, offsites, conferências
6. **Serviços profissionais:** Consultoria, legal, contabilidade
7. **Capex:** Investimentos de capital

## Fase 3: Consolidação e Iteração (Mês T-2)

### FP&A Consolida
- [ ] Compilar todos os pedidos em um modelo financeiro consolidado
- [ ] Identificar gap entre total pedido e envelope disponível
- [ ] Preparar cenários de alocação (base, stretch, conservador)
- [ ] Modelar impacto no P&L, cash flow e runway

### Iteração com Liderança
- [ ] Apresentar consolidação para CEO e C-level
- [ ] Identificar trade-offs necessários
- [ ] Priorizar entre departamentos (onde alocar marginal $)
- [ ] Negociar ajustes com cada VP
- [ ] Segunda iteração: ajustar e reconsolidar

### Critérios de Priorização
1. Impacto em receita (ROI claro e mensurável)
2. Retenção de clientes (impacto em churn)
3. Fundação técnica (tech debt, segurança, compliance)
4. Capacidade organizacional (pessoas críticas, treinamento)
5. Inovação estratégica (bets de longo prazo)

## Fase 4: Aprovação (Mês T-1)

### Board Package
- [ ] P&L projetado (receita, custos, margens)
- [ ] Cash flow projetado (12 meses, mensal)
- [ ] Headcount plan (por departamento e quarter)
- [ ] Capex plan e amortização
- [ ] Cenários de sensibilidade (what-if)
- [ ] Comparação com benchmark do setor
- [ ] Key assumptions e riscos

### Processo de Aprovação
- [ ] Review com comitê financeiro do board (se houver)
- [ ] Apresentação em board meeting
- [ ] Aprovação formal com ata documentada
- [ ] Comunicação do budget aprovado para a organização

## Fase 5: Execução e Acompanhamento (Mês T0-T12)

### Acompanhamento Mensal
- [ ] Comparar actual vs budget (variance analysis)
- [ ] Para variações >10%, exigir explicação e plano
- [ ] Reprojetar forecast para meses restantes
- [ ] Identificar riscos de over/under-spending

### Re-forecast Trimestral
- [ ] A cada trimestre, atualizar a projeção anual
- [ ] Ajustar budget se premissas mudaram significativamente
- [ ] Realocar recursos entre departamentos se necessário
- [ ] Documentar razões para mudanças

### Processo de Aprovação de Gastos Fora do Budget
Para gastos não previstos no orçamento:
- < 5% do budget do departamento: VP aprova
- 5-15% do budget do departamento: CFO aprova
- > 15% do budget do departamento: CEO + CFO aprovam
- > 5% do budget total da empresa: Board aprova

## Template de Budget por Departamento

```
BUDGET REQUEST - [DEPARTAMENTO] - [ANO]
Preparado por: [VP]
Data: [Data]

RESUMO EXECUTIVO
- Budget atual: $X
- Budget pedido: $Y (+Z%)
- Justificativa em 1 parágrafo

HEADCOUNT
| Cargo | Qty | Salário | Total | Quarter | Justificativa |
|-------|-----|---------|-------|---------|---------------|

OPEX
| Categoria | Valor Mensal | Valor Anual | Novo/Existente | Justificativa |

CAPEX
| Item | Valor | Amortização | Justificativa |

PRIORIZAÇÃO
Tier 1 (Must-Have): $X - itens sem os quais não atingimos metas base
Tier 2 (Should-Have): $Y - itens que aceleram crescimento
Tier 3 (Nice-to-Have): $Z - itens que melhoram eficiência

RISCOS SE NÃO APROVADO
O que acontece se o budget for cortado em 10%? 20%? 30%?
```

## Erros Comuns

1. **Budget como exercício político:** Departamentos inflam pedidos esperando cortes
2. **Zero-based nunca feito:** Carregar ineficiências de anos anteriores
3. **Forecast = budget:** Não atualizar projeções ao longo do ano
4. **Micromanagement de linhas:** Focar em linhas pequenas e ignorar as grandes
5. **Sem cenários:** Budget único sem sensibilidade a variáveis-chave
6. **Aprovação tardia:** Começar o ano sem budget aprovado

## Referências

- "Financial Intelligence" - Karen Berman & Joe Knight
- "Budgeting Basics and Beyond" - Jae K. Shim & Joel G. Siegel
- FP&A Trends Report (annualizado)
