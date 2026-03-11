# Mapa de Portfólio de Sistemas

## Propósito
Catalogar todos os sistemas em uso na organização com informações de ownership,
custo, saúde, integrações e ciclo de vida, fornecendo visibilidade para decisões
de investimento, consolidação e modernização.

## Quando Usar
- Anualmente como exercício de governança de TI
- Ao avaliar consolidação ou substituição de sistemas
- Para onboarding de novos líderes de tecnologia
- Como input para planejamento de budget de TI
- Quando avaliando impacto de mudanças cross-system

## Agente Responsável
- **Autor primário:** CIO/CISO Agent
- **Contribuidores:** CTO Agent, Owners de cada sistema
- **Revisor:** CFO Agent (custos), CEO Agent
- **Atualização:** Semestral (mínimo)

## Template

---

### PORTFÓLIO DE SISTEMAS

**Data de atualização:** {{data_atualizacao}}
**Autor:** {{autor}}
**Total de sistemas:** {{total_sistemas}}
**Custo anual total:** {{custo_anual_total}}

---

#### 1. Resumo do Portfólio

| Classificação | Quantidade | % do Total | Custo Anual |
|--------------|-----------|-----------|-------------|
| Crítico (Tier 1) | {{qtd_tier1}} | {{pct_tier1}} | {{custo_tier1}} |
| Importante (Tier 2) | {{qtd_tier2}} | {{pct_tier2}} | {{custo_tier2}} |
| Suporte (Tier 3) | {{qtd_tier3}} | {{pct_tier3}} | {{custo_tier3}} |
| Legado / Sunset | {{qtd_legado}} | {{pct_legado}} | {{custo_legado}} |
| **Total** | **{{qtd_total}}** | **100%** | **{{custo_total}}** |

---

#### 2. Catálogo de Sistemas

**Sistema: {{nome_sistema_1}}**
| Atributo | Valor |
|----------|-------|
| Categoria | {{categoria_1}} |
| Tier | {{tier_1}} |
| Vendor/Tipo | {{vendor_1}} |
| Owner (Business) | {{owner_business_1}} |
| Owner (Técnico) | {{owner_tecnico_1}} |
| Usuários | {{usuarios_1}} |
| Custo anual | {{custo_anual_1}} |
| Contrato até | {{contrato_ate_1}} |
| Status de saúde | {{saude_1}} |
| Versão atual | {{versao_1}} |
| Integrações | {{integracoes_1}} |
| Dados sensíveis | {{dados_sensiveis_1}} |
| Compliance | {{compliance_1}} |
| Última avaliação | {{ultima_avaliacao_1}} |

**Sistema: {{nome_sistema_2}}**
| Atributo | Valor |
|----------|-------|
| Categoria | {{categoria_2}} |
| Tier | {{tier_2}} |
| Vendor/Tipo | {{vendor_2}} |
| Owner (Business) | {{owner_business_2}} |
| Owner (Técnico) | {{owner_tecnico_2}} |
| Usuários | {{usuarios_2}} |
| Custo anual | {{custo_anual_2}} |
| Contrato até | {{contrato_ate_2}} |
| Status de saúde | {{saude_2}} |
| Versão atual | {{versao_2}} |
| Integrações | {{integracoes_2}} |
| Dados sensíveis | {{dados_sensiveis_2}} |
| Compliance | {{compliance_2}} |
| Última avaliação | {{ultima_avaliacao_2}} |

---

#### 3. Mapa de Integrações

| Sistema Origem | Sistema Destino | Tipo de Integração | Protocolo | Frequência | Criticidade |
|---------------|----------------|-------------------|-----------|-----------|-------------|
| {{origem_1}} | {{destino_1}} | {{tipo_int_1}} | {{protocolo_1}} | {{freq_1}} | {{crit_1}} |
| {{origem_2}} | {{destino_2}} | {{tipo_int_2}} | {{protocolo_2}} | {{freq_2}} | {{crit_2}} |
| {{origem_3}} | {{destino_3}} | {{tipo_int_3}} | {{protocolo_3}} | {{freq_3}} | {{crit_3}} |

---

#### 4. Avaliação de Saúde

| Sistema | Performance | Segurança | Manutenção | Adequação | Score Total |
|---------|-----------|-----------|-----------|-----------|-------------|
| {{sistema_1}} | {{perf_1}} | {{seg_1}} | {{manut_1}} | {{adeq_1}} | {{score_1}} |
| {{sistema_2}} | {{perf_2}} | {{seg_2}} | {{manut_2}} | {{adeq_2}} | {{score_2}} |
| {{sistema_3}} | {{perf_3}} | {{seg_3}} | {{manut_3}} | {{adeq_3}} | {{score_3}} |

**Escala:** 1 (Crítico) | 2 (Preocupante) | 3 (Adequado) | 4 (Bom) | 5 (Excelente)

---

#### 5. Ciclo de Vida e Roadmap

| Sistema | Status Atual | Ação Planejada | Timeline | Investimento |
|---------|-------------|---------------|----------|-------------|
| {{sistema_cv_1}} | {{status_cv_1}} | {{acao_cv_1}} | {{timeline_cv_1}} | {{invest_cv_1}} |
| {{sistema_cv_2}} | {{status_cv_2}} | {{acao_cv_2}} | {{timeline_cv_2}} | {{invest_cv_2}} |
| {{sistema_cv_3}} | {{status_cv_3}} | {{acao_cv_3}} | {{timeline_cv_3}} | {{invest_cv_3}} |

**Status:** Estratégico | Tático | Manutenção | Sunset | Substituição Planejada

---

#### 6. Oportunidades de Consolidação

| Oportunidade | Sistemas Envolvidos | Economia Estimada | Esforço | Prioridade |
|-------------|--------------------|--------------------|---------|-----------|
| {{oportunidade_1}} | {{sistemas_1}} | {{economia_1}} | {{esforco_1}} | {{prior_1}} |
| {{oportunidade_2}} | {{sistemas_2}} | {{economia_2}} | {{esforco_2}} | {{prior_2}} |

---

#### 7. Contratos e Renovações

| Sistema | Vendor | Valor Anual | Vencimento | Ação Recomendada |
|---------|--------|-----------|-----------|-----------------|
| {{sistema_cont_1}} | {{vendor_cont_1}} | {{valor_1}} | {{venc_1}} | {{acao_1}} |
| {{sistema_cont_2}} | {{vendor_cont_2}} | {{valor_2}} | {{venc_2}} | {{acao_2}} |
| {{sistema_cont_3}} | {{vendor_cont_3}} | {{valor_3}} | {{venc_3}} | {{acao_3}} |

---

## Instruções de Preenchimento

1. **Tier:** Tier 1 = downtime impacta receita diretamente. Tier 2 = impacta produtividade. Tier 3 = suporte.
2. **Owner:** Sempre defina owner de negócio (quem decide) E owner técnico (quem mantém).
3. **Integrações:** Mapeie todas. Integrações são os maiores pontos de falha e complexidade.
4. **Saúde:** Avalie semestralmente com critérios consistentes.
5. **Consolidação:** Busque ativamente. Shadow IT e redundâncias custam mais do que parecem.
6. **Contratos:** Revise 90 dias antes do vencimento para ter poder de negociação.

## Exemplo Preenchido

---

### PORTFÓLIO — Março 2026

**Total:** 34 sistemas | **Custo anual:** R$ 2.8M

| Sistema | Tier | Custo | Saúde | Ação |
|---------|------|-------|-------|------|
| Production Platform | 1 | R$ 480K | Bom | Manter |
| Salesforce CRM | 1 | R$ 360K | Adequado | Otimizar licenças |
| Legacy ERP | 2 | R$ 280K | Preocupante | Substituição planejada Q3 |
| Jira | 2 | R$ 85K | Bom | Manter |

---

## Checklist de Qualidade

- [ ] Todos os sistemas estão catalogados (incluindo shadow IT identificado)
- [ ] Cada sistema tem owner de negócio E técnico definidos
- [ ] Custos são reais (não estimativas) e incluem licenças + suporte + infra
- [ ] Integrações estão mapeadas entre todos os sistemas
- [ ] Avaliação de saúde é recente (< 6 meses)
- [ ] Ciclo de vida está definido para cada sistema
- [ ] Oportunidades de consolidação identificadas
- [ ] Contratos com vencimento em 90 dias estão destacados
- [ ] Dados sensíveis e compliance mapeados por sistema
- [ ] CFO Agent validou os custos totais
