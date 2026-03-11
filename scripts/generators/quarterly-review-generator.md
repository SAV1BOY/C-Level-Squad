# Script: Gerador de Review Trimestral

## Objetivo
Gerar automaticamente o documento de review trimestral consolidando performance financeira, progresso de OKRs, métricas de produto/pessoas e análise estratégica. Serve como base para reuniões de board e planning do próximo trimestre.

## Inputs
| Input | Tipo | Obrigatório | Descrição |
|-------|------|:-----------:|-----------|
| `quarter` | string | Sim | Quarter (ex: "Q1-2026") |
| `financial_data` | JSON/CSV | Sim | Dados financeiros do trimestre |
| `okr_scores` | JSON/YAML | Sim | OKRs com scores finais |
| `people_metrics` | JSON | Não | Headcount, turnover, eNPS |
| `product_metrics` | JSON | Não | NPS, DAU, feature adoption |
| `incidents` | JSON | Não | Lista de incidentes P0/P1 |
| `competitor_updates` | JSON | Não | Movimentos competitivos |
| `risks` | JSON | Não | Registro de riscos atualizado |

## Outputs
- Review trimestral completo em Markdown (20-30 páginas)
- Executive summary (2 páginas) para board
- Apresentação condensada (deck format) para all-hands
- Dados exportados para próximo ciclo de planning

---

## Lógica do Script

### Fase 1: Coleta e Consolidação

```
1. CARREGAR dados financeiros:
   - Receita (MRR, ARR, por segmento, por produto)
   - Custos (por área, por tipo)
   - Unit economics (CAC, LTV, payback)
   - Cash position e burn rate
   - COMPARAR com budget e trimestre anterior

2. CARREGAR OKRs:
   - Para cada OKR: target, resultado, score (0.0-1.0)
   - Calcular score médio por Objective e geral
   - Classificar: Exceeded | Met | Partially Met | Missed

3. CARREGAR métricas complementares:
   - People: HC, turnover, eNPS, hiring velocity
   - Produto: NPS, DAU/MAU, feature adoption, bugs
   - Engenharia: DORA metrics, incidentes, uptime
   - Vendas: pipeline, win rate, cycle time

4. CARREGAR contexto qualitativo:
   - Principais conquistas (do input ou extraído de weekly reports)
   - Principais desafios enfrentados
   - Lições aprendidas
```

### Fase 2: Análise

```
PARA cada métrica:
  CALCULAR variação QoQ (quarter over quarter)
  CALCULAR variação vs budget/plan
  DETERMINAR tendência (3+ quarters)
  CLASSIFICAR status: Green | Yellow | Red
  GERAR commentary automático para variações significativas

PARA OKRs:
  CALCULAR distribuição de scores
  IDENTIFICAR padrões (times consistentemente atingindo/falhando)
  GERAR análise de calibração (OKRs fáceis demais? Difíceis demais?)

PARA riscos:
  COMPARAR com registro do quarter anterior
  IDENTIFICAR riscos novos, mitigados e materializados
  ATUALIZAR severidade com base em dados reais
```

### Fase 3: Geração dos Documentos

```
GERAR review completo:
  APLICAR template de review trimestral
  INSERIR dados calculados em todas as tabelas
  GERAR gráficos em texto/ASCII para tendências
  ADICIONAR commentary automático + placeholders para input humano

GERAR executive summary:
  EXTRAIR top 5 métricas mais relevantes
  RESUMIR OKRs em 1 tabela
  LISTAR top 3 conquistas e top 3 riscos
  INCLUIR forecast atualizado e pedidos ao board

GERAR versão all-hands:
  SIMPLIFICAR métricas para audiência ampla
  DESTACAR conquistas do time
  INCLUIR preview de prioridades do próximo quarter
```

---

## Template do Review Trimestral

```markdown
# Review Trimestral — {quarter}
**Empresa:** {company_name}
**Data de Geração:** {date}
**Classificação:** {classification}

---

## 1. Executive Summary

**Status Geral:** {overall_status}

| Métrica | Meta | Realizado | Var | Status |
|---------|------|-----------|:---:|:-----:|
| Receita (ARR) | {target} | {actual} | {var}% | {status} |
| Margem Bruta | {target} | {actual} | {var}pp | {status} |
| EBITDA | {target} | {actual} | {var}% | {status} |
| NRR | {target} | {actual} | {var}pp | {status} |
| NPS | {target} | {actual} | {var} | {status} |
| Headcount | {target} | {actual} | {var} | {status} |

**Top 3 Conquistas:**
1. {achievement_1}
2. {achievement_2}
3. {achievement_3}

**Top 3 Preocupações:**
1. {concern_1}
2. {concern_2}
3. {concern_3}

---

## 2. Performance Financeira
{seção gerada com financial_analysis_blocks}

## 3. Progresso de OKRs
{seção gerada com okr_blocks}

## 4. Produto e Clientes
{seção gerada com product_metrics}

## 5. People e Organização
{seção gerada com team_assessment_blocks}

## 6. Engenharia e Tecnologia
{seção gerada com tech_assessment_blocks}

## 7. Cenário Competitivo
{seção gerada com competitive_intel_blocks}

## 8. Riscos
{seção gerada com risk_assessment_blocks}

## 9. Forecast Atualizado
{seção com projeções para restante do ano}

## 10. Prioridades do Próximo Trimestre
{seção com preview de OKRs e iniciativas Q+1}

## 11. Pedidos e Decisões
{seção com decisões necessárias do board/C-level}
```

---

## Exemplo de Execução

```
$ ./quarterly-review-generator.sh \
  --quarter "Q1-2026" \
  --financial data/q1-2026-financial.json \
  --okrs data/q1-2026-okrs.yaml \
  --people data/q1-2026-people.json \
  --output reviews/q1-2026/

Processando dados...
  - Financeiro: 12 métricas calculadas, 3 com variação significativa
  - OKRs: 4 objectives, 14 KRs — score médio: 0.72
  - People: HC 185 (+22), turnover 14% (acima do target)
  - Produto: NPS 45 (+3 vs Q anterior)

Gerando documentos...
  - Full review: reviews/q1-2026/quarterly-review.md (847 linhas)
  - Executive summary: reviews/q1-2026/executive-summary.md (95 linhas)
  - All-hands version: reviews/q1-2026/all-hands.md (120 linhas)
  - Data export: reviews/q1-2026/data-export.json

Review gerado com sucesso.

Ação necessária: 
  - Preencher commentary qualitativo nas seções marcadas com [HUMAN INPUT NEEDED]
  - Revisar forecast atualizado com CFO
  - Adicionar pedidos ao board
```

---

## Cadência
- **Geração inicial:** Dia 5 do mês seguinte ao quarter (dados financeiros fechados)
- **Revisão humana:** Dias 5-10 (C-Level preenche commentary e valida)
- **Apresentação ao board:** Até dia 15 do mês seguinte ao quarter

---

## Dicas de Uso
- O gerador cria 80% do documento — os 20% restantes (commentary e contexto) são humanos
- Marque claramente o que é gerado vs o que precisa de input humano
- Mantenha o formato consistente quarter a quarter — facilita comparação
- Automatize a coleta de dados de ferramentas (Stripe, Jira, Datadog, BambooHR)
- Comece simples e adicione automações incrementalmente
- O valor real está na CONSISTÊNCIA, não na sofisticação
