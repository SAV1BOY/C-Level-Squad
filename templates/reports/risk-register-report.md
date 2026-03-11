# Relatório de Registro de Riscos

## Propósito
Manter um registro centralizado e atualizado de todos os riscos significativos
da organização, classificados por probabilidade e impacto, com owners, mitigações
e status de acompanhamento, servindo como ferramenta de governança e decisão.

## Quando Usar
- Mensalmente como parte do MBR (revisão de riscos)
- Trimestralmente para revisão detalhada no QBR
- Quando novos riscos são identificados
- Para preparação de reuniões de Board
- Como input para decisões de investimento e priorização

## Agente Responsável
- **Autor primário:** Chief of Staff Agent (CoS)
- **Contribuidores:** Todos os agentes C-Level (cada um contribui riscos de sua área)
- **Revisor:** CEO Agent
- **Aprovador:** CEO Agent

## Template

---

### REGISTRO DE RISCOS — {{data_atualizacao}}

**Última atualização:** {{data_atualizacao}}
**Autor:** {{autor}}
**Período de revisão:** {{periodo}}
**Total de riscos ativos:** {{total_riscos}}

---

#### 1. Resumo Executivo de Riscos

**Distribuição por severidade:**
| Severidade | Quantidade | Variação vs. Anterior |
|-----------|-----------|----------------------|
| Crítica | {{qtd_critica}} | {{var_critica}} |
| Alta | {{qtd_alta}} | {{var_alta}} |
| Média | {{qtd_media}} | {{var_media}} |
| Baixa | {{qtd_baixa}} | {{var_baixa}} |

**Top 3 riscos que requerem atenção imediata:**
1. **{{risco_top_1}}** — {{resumo_top_1}}
2. **{{risco_top_2}}** — {{resumo_top_2}}
3. **{{risco_top_3}}** — {{resumo_top_3}}

---

#### 2. Heat Map de Riscos

|  | Impacto Baixo | Impacto Médio | Impacto Alto | Impacto Crítico |
|--|-------------|-------------|-------------|----------------|
| **Prob. Alta** | {{celula_ab}} | {{celula_am}} | {{celula_aa}} | {{celula_ac}} |
| **Prob. Média** | {{celula_mb}} | {{celula_mm}} | {{celula_ma}} | {{celula_mc}} |
| **Prob. Baixa** | {{celula_bb}} | {{celula_bm}} | {{celula_ba}} | {{celula_bc}} |

---

#### 3. Registro Detalhado de Riscos

**RISCO-{{id_1}}: {{titulo_risco_1}}**
| Atributo | Valor |
|----------|-------|
| Categoria | {{categoria_1}} |
| Descrição | {{descricao_1}} |
| Probabilidade | {{probabilidade_1}} |
| Impacto | {{impacto_1}} |
| Severidade | {{severidade_1}} |
| Owner | {{owner_1}} |
| Causa potencial | {{causa_1}} |
| Consequência se materializar | {{consequencia_1}} |
| Mitigação atual | {{mitigacao_atual_1}} |
| Mitigação adicional planejada | {{mitigacao_plan_1}} |
| Status da mitigação | {{status_mit_1}} |
| Indicador de monitoramento | {{indicador_1}} |
| Última revisão | {{ultima_revisao_1}} |

**RISCO-{{id_2}}: {{titulo_risco_2}}**
| Atributo | Valor |
|----------|-------|
| Categoria | {{categoria_2}} |
| Descrição | {{descricao_2}} |
| Probabilidade | {{probabilidade_2}} |
| Impacto | {{impacto_2}} |
| Severidade | {{severidade_2}} |
| Owner | {{owner_2}} |
| Causa potencial | {{causa_2}} |
| Consequência se materializar | {{consequencia_2}} |
| Mitigação atual | {{mitigacao_atual_2}} |
| Mitigação adicional planejada | {{mitigacao_plan_2}} |
| Status da mitigação | {{status_mit_2}} |
| Indicador de monitoramento | {{indicador_2}} |
| Última revisão | {{ultima_revisao_2}} |

**RISCO-{{id_3}}: {{titulo_risco_3}}**
| Atributo | Valor |
|----------|-------|
| Categoria | {{categoria_3}} |
| Descrição | {{descricao_3}} |
| Probabilidade | {{probabilidade_3}} |
| Impacto | {{impacto_3}} |
| Severidade | {{severidade_3}} |
| Owner | {{owner_3}} |
| Causa potencial | {{causa_3}} |
| Consequência se materializar | {{consequencia_3}} |
| Mitigação atual | {{mitigacao_atual_3}} |
| Mitigação adicional planejada | {{mitigacao_plan_3}} |
| Status da mitigação | {{status_mit_3}} |
| Indicador de monitoramento | {{indicador_3}} |
| Última revisão | {{ultima_revisao_3}} |

---

#### 4. Categorias de Risco

| Categoria | Quantidade | Exemplos |
|----------|-----------|---------|
| Estratégico | {{qtd_estrategico}} | Mercado, competição, tese |
| Financeiro | {{qtd_financeiro}} | Cash, receita, câmbio |
| Operacional | {{qtd_operacional}} | Execução, processos, qualidade |
| Tecnológico | {{qtd_tecnologico}} | Infra, segurança, reliability |
| Pessoas | {{qtd_pessoas}} | Retenção, contratação, cultura |
| Regulatório | {{qtd_regulatorio}} | Compliance, legal, fiscal |
| Reputacional | {{qtd_reputacional}} | Marca, PR, confiança do cliente |

---

#### 5. Riscos Materializados no Período

| Risco | Data | Impacto Real | Resposta | Aprendizado |
|-------|------|-------------|----------|-------------|
| {{risco_mat_1}} | {{data_mat_1}} | {{impacto_mat_1}} | {{resposta_mat_1}} | {{learn_mat_1}} |
| {{risco_mat_2}} | {{data_mat_2}} | {{impacto_mat_2}} | {{resposta_mat_2}} | {{learn_mat_2}} |

---

#### 6. Novos Riscos Identificados

| Risco | Categoria | Probabilidade | Impacto | Owner | Mitigação Proposta |
|-------|----------|--------------|---------|-------|-------------------|
| {{novo_risco_1}} | {{cat_novo_1}} | {{prob_novo_1}} | {{imp_novo_1}} | {{owner_novo_1}} | {{mit_novo_1}} |
| {{novo_risco_2}} | {{cat_novo_2}} | {{prob_novo_2}} | {{imp_novo_2}} | {{owner_novo_2}} | {{mit_novo_2}} |

---

#### 7. Riscos Encerrados

| Risco | Razão de Encerramento | Data |
|-------|-----------------------|------|
| {{risco_enc_1}} | {{razao_enc_1}} | {{data_enc_1}} |
| {{risco_enc_2}} | {{razao_enc_2}} | {{data_enc_2}} |

---

#### 8. Ações Prioritárias

| # | Ação | Risco Relacionado | Owner | Prazo | Status |
|---|------|------------------|-------|-------|--------|
| 1 | {{acao_1}} | {{risco_rel_1}} | {{owner_a1}} | {{prazo_1}} | {{status_1}} |
| 2 | {{acao_2}} | {{risco_rel_2}} | {{owner_a2}} | {{prazo_2}} | {{status_2}} |
| 3 | {{acao_3}} | {{risco_rel_3}} | {{owner_a3}} | {{prazo_3}} | {{status_3}} |

---

## Instruções de Preenchimento

1. **Probabilidade:** Alta (>60%) | Média (30-60%) | Baixa (<30%). Use dados quando disponíveis.
2. **Impacto:** Crítico (>30% da receita) | Alto (10-30%) | Médio (5-10%) | Baixo (<5%).
3. **Owner:** Cada risco deve ter um único owner responsável pela mitigação.
4. **Indicadores:** Defina leading indicators que sinalizam quando o risco está se materializando.
5. **Revisão:** Todo risco deve ser revisado pelo menos mensalmente.
6. **Novos vs. Encerrados:** Monitore o saldo. Se novos > encerrados consistentemente, investigate.

## Exemplo Preenchido

---

### REGISTRO DE RISCOS — Março 2026

**RISCO-12: Concentração de receita em top 3 clientes**
| Atributo | Valor |
|----------|-------|
| Categoria | Financeiro |
| Probabilidade | Média |
| Impacto | Crítico |
| Owner | CRO Agent |
| Descrição | Top 3 clientes representam 35% do ARR. Perda de qualquer um impacta significativamente |
| Mitigação | Programa de customer success dedicado + diversificação acelerada do pipeline |
| Indicador | % do ARR nos top 3 (target: < 25% até Q4) |

---

## Checklist de Qualidade

- [ ] Todos os riscos têm owner individual definido
- [ ] Probabilidade e impacto estão classificados consistentemente
- [ ] Heat map está atualizado e visual
- [ ] Mitigações são específicas e acionáveis
- [ ] Indicadores de monitoramento definidos para riscos altos/críticos
- [ ] Riscos materializados estão documentados com aprendizado
- [ ] Novos riscos e riscos encerrados estão registrados
- [ ] Todos os riscos foram revisados no último mês
- [ ] Ações prioritárias têm owners e prazos
- [ ] O registro foi revisado pelo CEO Agent
