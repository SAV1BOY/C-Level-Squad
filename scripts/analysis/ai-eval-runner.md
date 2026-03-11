# AI Eval Runner

> Script para execução de avaliações de sistemas de AI dentro do C-Level Squad.

---

## Objetivo

Executar avaliações estruturadas de ferramentas e sistemas de AI utilizados
pelo squad, definindo setup de avaliação, benchmarks de referência, sistema
de scoring e formato de reporting dos resultados.

---

## Eval Setup — Configuração da Avaliação

### Tipos de Avaliação
1. **Pre-adoption eval**: antes de adoptar uma nova ferramenta AI
2. **Periodic eval**: avaliação regular de ferramentas em uso (trimestral)
3. **Comparative eval**: comparação entre ferramentas concorrentes
4. **Regression eval**: verificar se updates degradaram performance
5. **Use-case eval**: avaliar AI para um caso de uso específico

### Definição do Eval
```yaml
eval_id: "EVAL-YYYY-NNNN"
type: "pre_adoption | periodic | comparative | regression | use_case"
tool_name: "Nome da ferramenta / modelo"
tool_version: "Versão específica"
eval_date: "YYYY-MM-DD"
evaluator: "Nome / Role"
use_cases:
  - id: "UC-001"
    description: "Descrição do caso de uso"
    weight: 0.3                        # Peso relativo
    acceptance_criteria: "Critério mínimo"
test_set:
  size: 50                             # Número de test cases
  source: "Descrição da origem dos testes"
  diversity: "Como foi garantida diversidade"
environment:
  hardware: "Specs relevantes"
  configuration: "Parâmetros de configuração"
  constraints: "Limitações conhecidas"
```

### Test Set Design
Cada test set deve incluir:
- **Happy path cases** (40%): cenários normais e esperados
- **Edge cases** (25%): cenários limítrofes e incomuns
- **Adversarial cases** (15%): tentativas de confundir o sistema
- **Real-world samples** (20%): casos reais do histórico do squad

---

## Benchmarks — Referências de Avaliação

### Benchmark Categories

#### 1. Accuracy & Quality
- **Factual accuracy**: % de outputs factualmente correctos
- **Relevance**: % de outputs relevantes para o input
- **Completeness**: % de outputs que cobrem todos os aspectos necessários
- **Consistency**: outputs similares para inputs similares
- **Hallucination rate**: % de outputs com informação fabricada

#### 2. Performance
- **Latency**: tempo de resposta (p50, p90, p99)
- **Throughput**: requests processados por unidade de tempo
- **Reliability**: uptime e taxa de erros
- **Scalability**: performance sob carga crescente
- **Cost per request**: custo unitário de utilização

#### 3. Usability
- **Ease of integration**: complexidade técnica de integração
- **Documentation quality**: qualidade da documentação disponível
- **Error handling**: como lida com inputs inválidos ou ambíguos
- **Configurability**: flexibilidade de configuração
- **Learning curve**: tempo para proficiência da equipa

#### 4. Safety & Governance
- **Bias detection**: presença de vieses nos outputs
- **PII handling**: tratamento de dados pessoais
- **Content safety**: outputs seguros e apropriados
- **Audit trail**: rastreabilidade de inputs/outputs
- **Compliance**: conformidade com políticas internas e regulação

#### 5. Business Value
- **Time saved**: tempo poupado vs processo manual
- **Quality improvement**: melhoria de qualidade vs baseline humano
- **Cost reduction**: redução de custos vs alternativas
- **Adoption rate**: facilidade de adopção pela equipa
- **ROI projection**: retorno estimado do investimento

---

## Scoring — Sistema de Pontuação

### Scoring por Test Case
```
Cada test case recebe scores em dimensões relevantes:

Score por dimensão: 0-5
  5 = Excelente (supera expectativas)
  4 = Bom (atende completamente)
  3 = Aceitável (atende parcialmente)
  2 = Fraco (abaixo do aceitável)
  1 = Falha (não atende)
  0 = Erro/crash (falha técnica)
```

### Scoring Agregado
```
Category Score = média_ponderada(test_cases × pesos_use_case)

Overall Eval Score = Accuracy(30%) + Performance(20%) +
                     Usability(15%) + Safety(20%) + Business_Value(15%)
```

### Classificação Final
| Score | Classificação | Recomendação |
|-------|--------------|-------------|
| 4.0-5.0 | Excelente | Adoptar / Manter |
| 3.0-3.9 | Bom | Adoptar com ressalvas / Monitorar |
| 2.0-2.9 | Aceitável | Considerar alternativas |
| 1.0-1.9 | Fraco | Não adoptar / Descontinuar |
| 0.0-0.9 | Inaceitável | Rejeitar / Substituir imediatamente |

---

## Processo de Execução

### Passo 1 — Preparação
1. Definir scope e objectivos da avaliação
2. Seleccionar ou criar test set
3. Configurar ambiente de teste
4. Definir baseline de comparação (humano ou ferramenta anterior)
5. Preparar scoring rubric específica

### Passo 2 — Execução
1. Executar test set completo
2. Registar todos os outputs com timestamps
3. Registar métricas de performance (latency, errors)
4. Documentar anomalias durante execução
5. Garantir reprodutibilidade (seeds, configs)

### Passo 3 — Scoring
1. Avaliar cada output contra critérios definidos
2. Multiple evaluators para reduzir bias (mínimo 2)
3. Resolver discrepâncias por consenso
4. Calcular scores agregados
5. Comparar com benchmarks e baseline

### Passo 4 — Análise
1. Identificar pontos fortes e fracos
2. Analisar padrões de falha
3. Comparar com ferramentas concorrentes (se applicable)
4. Calcular ROI e business case
5. Formular recomendação

### Passo 5 — Reporting
1. Produzir eval report completo
2. Apresentar resultados ao C-Level Squad
3. Registar decisão no decision log
4. Arquivar eval data para referência futura
5. Planear próxima avaliação

---

## Reporting Format

```markdown
# AI Eval Report — [Tool Name] v[Version]

## Metadata
- Eval ID: [ID]
- Data: [data]
- Tipo: [tipo]
- Avaliadores: [nomes]

## Executive Summary
[2-3 parágrafos com conclusão e recomendação]

## Scores
| Categoria | Score | Benchmark | Delta |
|-----------|-------|-----------|-------|
| Accuracy | [X.X] | [Y.Y] | [±Z.Z] |
| Performance | [X.X] | [Y.Y] | [±Z.Z] |
| Usability | [X.X] | [Y.Y] | [±Z.Z] |
| Safety | [X.X] | [Y.Y] | [±Z.Z] |
| Business Value | [X.X] | [Y.Y] | [±Z.Z] |
| **Overall** | **[X.X]** | **[Y.Y]** | **[±Z.Z]** |

## Detailed Findings
[Por categoria, com exemplos]

## Recommendation
[Adoptar / Manter / Monitorar / Substituir / Rejeitar]
[Condições e próximos passos]
```

---

## Notas Técnicas

- Test sets armazenados em `data/ai-evals/test-sets/`
- Resultados em `data/ai-evals/results/`
- Eval scripts automatizados quando possível
- Dados sensíveis anonimizados antes de usar em test sets
- Resultados partilhados internamente, nunca externamente sem aprovação
