# Medição de ROI de AI

> Processo estruturado para medir o retorno sobre investimento de iniciativas
> de AI, justificando investimentos e orientando priorização de projetos.

## Objetivo

Quantificar o valor gerado por investimentos em AI, fornecendo dados para
decisões de alocação de recursos, expansão ou descontinuação de projetos,
e comunicação com stakeholders e investidores.

## Frequência

- **Pré-investimento:** Business case antes de iniciar projeto
- **Durante:** Check-in mensal de métricas
- **Pós-deploy:** Avaliação em 30, 90 e 180 dias
- **Anual:** Consolidação de ROI de todo o portfólio de AI

## Framework de ROI para AI

### Categorias de Valor

#### 1. Redução de Custo (Mais Fácil de Medir)
- Automação de tarefas manuais → redução de horas de trabalho
- Otimização de processos → redução de desperdício/erro
- Eficiência operacional → redução de custo por transação
- Self-service → redução de volume de suporte

#### 2. Aumento de Receita (Mensurável com Atribuição)
- Personalização → aumento de conversão
- Recomendação → aumento de ticket médio/cross-sell
- Precificação dinâmica → otimização de margem
- Lead scoring → aumento de win rate

#### 3. Melhoria de Experiência (Proxy Metrics)
- NPS/CSAT improvement
- Redução de churn
- Tempo de resolução de problemas
- Satisfaction com interações AI

#### 4. Capacidade Estratégica (Mais Difícil de Medir)
- Velocidade de decisão (time-to-insight)
- Capacidade de processar mais dados
- Novos produtos/serviços habilitados por AI
- Vantagem competitiva (difícil de quantificar)

## Cálculo de ROI

### Fórmula Básica
```
ROI = (Valor Gerado - Custo Total) / Custo Total × 100%
```

### Componentes de Custo

| Categoria | Itens | Como Calcular |
|-----------|-------|---------------|
| Desenvolvimento | Salários do time AI, consultoria | Horas × custo/hora |
| Dados | Aquisição, limpeza, labeling | Custo direto + horas internas |
| Infraestrutura | GPU, cloud, storage | Custo mensal × 12 |
| Ferramentas | Licenças, APIs de AI | Custo anual |
| Operação | Monitoramento, manutenção, re-training | Horas × custo/hora |
| Oportunidade | O que o time faria se não fizesse AI | Estimativa |

### Componentes de Valor

| Categoria | Como Medir | Exemplo |
|-----------|-----------|---------|
| Horas economizadas | (Tempo antes - Tempo depois) × Custo/hora | 500h/mês × $50/h = $25K/mês |
| Erros evitados | Redução de taxa de erro × Custo por erro | 50% menos erros × $200/erro |
| Receita incremental | A/B test: grupo AI vs controle | +5% conversão × $10M revenue |
| Churn evitado | Clientes retidos × LTV | 100 clientes × $5K LTV |

## Processo de Medição

### Pré-Investimento: Business Case

- [ ] Definir hipótese de valor (o que esperamos que AI resolva)
- [ ] Quantificar baseline (performance atual sem AI)
- [ ] Estimar valor potencial (cenários conservador, base, otimista)
- [ ] Estimar custos totais (desenvolvimento + operação por 12-24 meses)
- [ ] Calcular ROI esperado e payback period
- [ ] Definir métricas de sucesso e como serão medidas
- [ ] Aprovar com finance e liderança

### Template de Business Case

```
BUSINESS CASE: [NOME DO PROJETO AI]

HIPÓTESE
[O que acreditamos que AI pode resolver]

BASELINE ATUAL
- Métrica: [valor atual]
- Custo: [custo atual do processo]

PROJEÇÃO COM AI
Cenário Conservador: [valor] → ROI de X%
Cenário Base: [valor] → ROI de Y%
Cenário Otimista: [valor] → ROI de Z%

INVESTIMENTO NECESSÁRIO
Desenvolvimento: $___
Infraestrutura (12m): $___
Operação (12m): $___
Total: $___

PAYBACK PERIOD
Conservador: ___ meses
Base: ___ meses

RISCOS
1. [Risco] - [Mitigação]

GO/NO-GO DECISION
[ ] Go [ ] No-Go [ ] Mais informações necessárias
```

### Durante o Projeto: Check-ins Mensais

- [ ] Progresso do desenvolvimento vs timeline
- [ ] Custo acumulado vs budget
- [ ] Primeiros resultados de validação (se disponíveis)
- [ ] Riscos materializados ou novos
- [ ] Decisão: continuar, pivotar ou cancelar

### Pós-Deploy: Avaliação de Resultados

**30 dias:**
- [ ] Modelo operando conforme esperado?
- [ ] Primeiras métricas de impacto (mesmo que preliminares)
- [ ] Feedback de usuários
- [ ] Custos de operação conforme estimado?

**90 dias:**
- [ ] Métricas de impacto com significância estatística
- [ ] ROI parcial calculado
- [ ] Comparação com business case original
- [ ] Decisão: expandir, manter ou ajustar

**180 dias:**
- [ ] ROI completo calculado
- [ ] Comparação com cenários do business case
- [ ] Lições aprendidas documentadas
- [ ] Decisão: escalar, manter ou descontinuar

## Dashboard de ROI de AI

### Métricas do Portfólio
- Total investido em AI (YTD e acumulado)
- Total de valor gerado (por categoria)
- ROI agregado do portfólio
- Projetos por status (em desenvolvimento, em produção, descontinuados)
- Payback period médio

### Métricas por Projeto
- Investimento vs retorno (chart)
- Métricas de impacto (trend)
- Custo operacional mensal
- User adoption / utilização
- Satisfaction score

## Armadilhas Comuns

### 1. Medir Outputs, Não Outcomes
**Errado:** "O modelo tem 95% de accuracy"
**Certo:** "O modelo reduziu erros humanos em 40%, economizando $200K/ano"

### 2. Ignorar Custos de Operação
- Desenvolvimento é custo único; operação é contínuo
- Re-training, monitoramento, manutenção podem superar custo de dev

### 3. Atribuição Incorreta
- "Receita aumentou 10% após deploy de AI" ≠ "AI causou aumento de 10%"
- Usar A/B tests ou métodos causais quando possível
- Ser conservador na atribuição

### 4. Comparar com Zero ao Invés de Alternativa
- ROI de AI deve ser comparado com a melhor alternativa não-AI
- Se um processo manual custa $100K e AI custa $80K, o ganho é $20K
- Não comparar AI ($80K) com zero ($0)

### 5. Ignorar Valor Intangível
- Capacidade de tomar decisões mais rápidas tem valor
- Experiência do cliente melhorada tem valor
- Mas cuidado: se tudo é "intangível", o business case é fraco

## Comunicação de ROI para Stakeholders

### Para o Board/Investidores
- ROI agregado do portfólio de AI
- Top 3 projetos por impacto financeiro
- Investimento planejado vs realizado
- Projeção de valor para próximos 12 meses

### Para o CEO
- Como AI está impactando métricas estratégicas
- Onde o investimento está gerando mais valor
- Onde devemos investir mais (ou menos)
- Comparação com benchmarks do setor

### Para o CFO
- Total invested, total returned, net ROI
- Payback period por projeto
- Custo operacional mensal de AI
- Forecast de custos para próximo ano

## Referências

- "AI ROI" - Tom Davenport & Nitin Mittal (Harvard Business Review)
- "The AI-First Company" - Ash Fontana
- McKinsey: "The State of AI" (annual report)
- "Competing in the Age of AI" - Marco Iansiti & Karim Lakhani (HBS)
