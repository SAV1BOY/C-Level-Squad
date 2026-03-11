# Registro de Dívida Técnica (Tech Debt Register)

## Propósito
Catalogar e priorizar a dívida técnica da organização de forma transparente, permitindo
decisões informadas sobre quando e como pagá-la, conectando tech debt a impacto em
negócio e velocidade de entrega.

## Quando Usar
- Como documento vivo atualizado continuamente pela engenharia
- No planejamento trimestral para decidir alocação de tech debt
- Quando tech debt começa a impactar velocidade ou reliability
- Para justificar investimento em plataforma ao C-Level

## Agente Responsável
- **Autor primário:** CTO Agent
- **Contribuidores:** Tech Leads, Staff Engineers
- **Revisor:** CEO Agent (priorização estratégica)
- **Atualização:** Contínua (mínimo quinzenal)

## Template

---

### TECH DEBT REGISTER

**Data de atualização:** {{data_atualizacao}}
**Autor:** {{autor}}
**Total de itens catalogados:** {{total_itens}}
**Custo estimado total de resolução:** {{custo_total_estimado}}

---

#### 1. Resumo Executivo

**Saúde geral do tech debt:** {{critica_preocupante_gerenciavel_saudavel}}
**Tendência:** {{piorando_estavel_melhorando}}

| Severidade | Quantidade | % do Total | Custo Estimado |
|-----------|-----------|-----------|----------------|
| Crítica | {{qtd_critica}} | {{pct_critica}} | {{custo_critica}} |
| Alta | {{qtd_alta}} | {{pct_alta}} | {{custo_alta}} |
| Média | {{qtd_media}} | {{pct_media}} | {{custo_media}} |
| Baixa | {{qtd_baixa}} | {{pct_baixa}} | {{custo_baixa}} |
| **Total** | **{{qtd_total}}** | **100%** | **{{custo_total}}** |

---

#### 2. Impacto do Tech Debt em Métricas

| Métrica | Valor Atual | Valor sem Tech Debt (est.) | Gap |
|---------|-------------|--------------------------|-----|
| Deploy frequency | {{deploy_atual}} | {{deploy_ideal}} | {{gap_deploy}} |
| Lead time for changes | {{leadtime_atual}} | {{leadtime_ideal}} | {{gap_leadtime}} |
| Change failure rate | {{cfr_atual}} | {{cfr_ideal}} | {{gap_cfr}} |
| MTTR | {{mttr_atual}} | {{mttr_ideal}} | {{gap_mttr}} |
| Developer satisfaction | {{devsat_atual}} | {{devsat_ideal}} | {{gap_devsat}} |

---

#### 3. Registro Detalhado

**TD-{{id_1}}: {{titulo_1}}**
| Atributo | Valor |
|----------|-------|
| Severidade | {{severidade_1}} |
| Tipo | {{tipo_1}} |
| Sistema/Serviço | {{sistema_1}} |
| Descrição | {{descricao_1}} |
| Impacto atual | {{impacto_1}} |
| Custo de não resolver (mensal) | {{custo_nao_resolver_1}} |
| Esforço para resolver | {{esforco_resolver_1}} |
| Benefício esperado | {{beneficio_1}} |
| Owner | {{owner_1}} |
| Status | {{status_1}} |
| Data de identificação | {{data_ident_1}} |

**TD-{{id_2}}: {{titulo_2}}**
| Atributo | Valor |
|----------|-------|
| Severidade | {{severidade_2}} |
| Tipo | {{tipo_2}} |
| Sistema/Serviço | {{sistema_2}} |
| Descrição | {{descricao_2}} |
| Impacto atual | {{impacto_2}} |
| Custo de não resolver (mensal) | {{custo_nao_resolver_2}} |
| Esforço para resolver | {{esforco_resolver_2}} |
| Benefício esperado | {{beneficio_2}} |
| Owner | {{owner_2}} |
| Status | {{status_2}} |
| Data de identificação | {{data_ident_2}} |

**TD-{{id_3}}: {{titulo_3}}**
| Atributo | Valor |
|----------|-------|
| Severidade | {{severidade_3}} |
| Tipo | {{tipo_3}} |
| Sistema/Serviço | {{sistema_3}} |
| Descrição | {{descricao_3}} |
| Impacto atual | {{impacto_3}} |
| Custo de não resolver (mensal) | {{custo_nao_resolver_3}} |
| Esforço para resolver | {{esforco_resolver_3}} |
| Benefício esperado | {{beneficio_3}} |
| Owner | {{owner_3}} |
| Status | {{status_3}} |
| Data de identificação | {{data_ident_3}} |

---

#### 4. Matriz de Priorização

| ID | Título | Custo de Não Resolver (mês) | Esforço | ROI Score | Prioridade |
|----|--------|---------------------------|---------|-----------|-----------|
| TD-{{id_1}} | {{titulo_1}} | {{custo_nr_1}} | {{esforco_1}} | {{roi_1}} | {{prior_1}} |
| TD-{{id_2}} | {{titulo_2}} | {{custo_nr_2}} | {{esforco_2}} | {{roi_2}} | {{prior_2}} |
| TD-{{id_3}} | {{titulo_3}} | {{custo_nr_3}} | {{esforco_3}} | {{roi_3}} | {{prior_3}} |

*ROI Score = (Custo mensal de não resolver x 12) / Esforço de resolução*

---

#### 5. Plano de Pagamento de Tech Debt

| Quarter | Itens Planejados | Esforço Total | Investimento | Benefício Esperado |
|---------|-----------------|---------------|-------------|-------------------|
| {{quarter_1}} | {{itens_q1}} | {{esforco_q1}} | {{invest_q1}} | {{beneficio_q1}} |
| {{quarter_2}} | {{itens_q2}} | {{esforco_q2}} | {{invest_q2}} | {{beneficio_q2}} |
| {{quarter_3}} | {{itens_q3}} | {{esforco_q3}} | {{invest_q3}} | {{beneficio_q3}} |

---

#### 6. Tipos de Tech Debt

| Tipo | Definição | Exemplos |
|------|-----------|---------|
| Arquitetural | Decisões estruturais que limitam evolução | Monólito, acoplamento |
| Código | Qualidade de código abaixo do padrão | Duplicação, complexidade ciclomática |
| Infraestrutura | Infra desatualizada ou sub-dimensionada | Versões antigas, single point of failure |
| Teste | Cobertura insuficiente ou testes frágeis | Falta de testes, testes flaky |
| Documentação | Falta de documentação técnica | APIs sem docs, runbooks ausentes |
| Dependências | Libraries desatualizadas ou vulneráveis | CVEs conhecidas, end-of-life |

---

#### 7. Tendências (últimos 4 quarters)

| Quarter | Novos Itens | Itens Resolvidos | Saldo | Custo Acumulado |
|---------|------------|-----------------|-------|----------------|
| {{q_4}} | {{novos_q4}} | {{resolvidos_q4}} | {{saldo_q4}} | {{custo_acum_q4}} |
| {{q_3}} | {{novos_q3}} | {{resolvidos_q3}} | {{saldo_q3}} | {{custo_acum_q3}} |
| {{q_2}} | {{novos_q2}} | {{resolvidos_q2}} | {{saldo_q2}} | {{custo_acum_q2}} |
| {{q_1}} | {{novos_q1}} | {{resolvidos_q1}} | {{saldo_q1}} | {{custo_acum_q1}} |

---

## Instruções de Preenchimento

1. **Custo de não resolver:** Quantifique em horas de engenharia, incidentes causados ou receita perdida.
2. **Esforço:** Use story points ou semanas-engenheiro. Seja conservador (multiplique por 1.5).
3. **ROI Score:** Priorize itens com alto custo de não resolver e baixo esforço de resolução.
4. **Tipos:** Categorize para identificar padrões. Se 80% é "código", talvez precisamos de code review melhor.
5. **Tendência:** Se novos itens > resolvidos consistentemente, o problema está crescendo.
6. **Atualização:** Trate como documento vivo. Revise pelo menos quinzenalmente.

## Exemplo Preenchido

---

### TECH DEBT REGISTER — Março 2026

**Saúde geral:** Preocupante
**Tendência:** Estável (entrando 3-4 itens/mês, resolvendo 3-4)

**TD-042: Database queries N+1 no módulo de relatórios**
| Atributo | Valor |
|----------|-------|
| Severidade | Alta |
| Impacto | Relatórios > 1000 registros levam >30s. 15 tickets/mês de suporte |
| Custo de não resolver | R$ 8K/mês (suporte) + 20h eng/mês (workarounds) |
| Esforço | 3 semanas-engenheiro |
| ROI Score | 3.2x (resolve-se em 3 meses) |

---

## Checklist de Qualidade

- [ ] Todos os itens têm severidade e tipo classificados
- [ ] Custo de não resolver está quantificado (não apenas "alto")
- [ ] Esforço de resolução tem estimativa realista
- [ ] ROI Score calculado para priorização
- [ ] Tendência de 4+ quarters documentada
- [ ] Plano de pagamento com alocação por quarter
- [ ] Impacto em DORA metrics documentado
- [ ] Documento atualizado nos últimos 15 dias
- [ ] Tipos de tech debt categorizados para análise de padrões
- [ ] CTO Agent e CEO Agent revisaram as prioridades
