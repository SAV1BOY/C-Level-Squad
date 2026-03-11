# Ficha de Definição de Dados (Data Definition / SSOT)

## Propósito
Documentar a definição oficial de cada métrica ou dado crítico do negócio, estabelecendo
a Single Source of Truth (SSOT), regras de cálculo, ownership e lineage, eliminando
ambiguidades e inconsistências entre relatórios.

## Quando Usar
- Ao definir ou redefinir métricas de negócio (KPIs, OKRs)
- Quando há divergência entre relatórios sobre o mesmo dado
- Para onboarding de novos analistas ou líderes
- Como governança de dados para compliance e auditoria

## Agente Responsável
- **Autor primário:** CIO/CISO Agent (governança) + CFO Agent (métricas financeiras)
- **Contribuidores:** Owners de cada métrica
- **Revisor:** CEO Agent
- **Aprovador:** Owner da métrica + CIO Agent

## Template

---

### FICHA DE DEFINIÇÃO DE DADOS

**Data de criação:** {{data_criacao}}
**Última atualização:** {{data_atualizacao}}
**Autor:** {{autor}}
**Versão:** {{versao}}

---

#### Definição: {{nome_metrica}}

| Atributo | Valor |
|----------|-------|
| **Nome oficial** | {{nome_oficial}} |
| **Sigla/Abreviação** | {{sigla}} |
| **Categoria** | {{financeira_operacional_produto_pessoas}} |
| **Owner** | {{owner_metrica}} |
| **Definição em linguagem natural** | {{definicao_natural}} |
| **Fórmula de cálculo** | {{formula_calculo}} |
| **Unidade de medida** | {{unidade}} |
| **Granularidade temporal** | {{diaria_semanal_mensal}} |
| **Granularidade dimensional** | {{por_produto_segmento_regiao}} |
| **Fonte de dados (SSOT)** | {{sistema_fonte}} |
| **Tabela/Dataset** | {{tabela_dataset}} |
| **Campos utilizados** | {{campos}} |
| **Filtros/Exclusões** | {{filtros}} |
| **Frequência de atualização** | {{frequencia_atualizacao}} |
| **Latência do dado** | {{latencia}} |
| **Data de início da série** | {{data_inicio_serie}} |

---

#### Regras de Negócio

| # | Regra | Exemplo |
|---|-------|---------|
| 1 | {{regra_1}} | {{exemplo_1}} |
| 2 | {{regra_2}} | {{exemplo_2}} |
| 3 | {{regra_3}} | {{exemplo_3}} |
| 4 | {{regra_4}} | {{exemplo_4}} |

---

#### O Que NÃO Está Incluído

- {{exclusao_1}}
- {{exclusao_2}}
- {{exclusao_3}}

---

#### Métricas Relacionadas

| Métrica Relacionada | Relação | Ficha |
|--------------------|---------|-------|
| {{metrica_rel_1}} | {{relacao_1}} | {{link_ficha_1}} |
| {{metrica_rel_2}} | {{relacao_2}} | {{link_ficha_2}} |
| {{metrica_rel_3}} | {{relacao_3}} | {{link_ficha_3}} |

---

#### Data Lineage (origem → destino)

```
{{sistema_origem}} → {{etl_processo}} → {{data_warehouse}} → {{ferramenta_bi}} → {{dashboard_relatorio}}
```

**Transformações aplicadas:**
1. {{transformacao_1}}
2. {{transformacao_2}}
3. {{transformacao_3}}

---

#### Qualidade do Dado

| Dimensão | Score (1-5) | Comentário |
|----------|-----------|-----------|
| Completude | {{score_completude}} | {{coment_completude}} |
| Precisão | {{score_precisao}} | {{coment_precisao}} |
| Consistência | {{score_consistencia}} | {{coment_consistencia}} |
| Atualidade | {{score_atualidade}} | {{coment_atualidade}} |
| Unicidade | {{score_unicidade}} | {{coment_unicidade}} |

---

#### Histórico de Mudanças

| Data | Mudança | Razão | Impacto na Série Histórica |
|------|---------|-------|---------------------------|
| {{data_mudanca_1}} | {{mudanca_1}} | {{razao_1}} | {{impacto_1}} |
| {{data_mudanca_2}} | {{mudanca_2}} | {{razao_2}} | {{impacto_2}} |

---

#### Controles e Alertas

| Controle | Threshold | Ação Automática | Responsável |
|----------|-----------|----------------|-------------|
| {{controle_1}} | {{threshold_1}} | {{acao_auto_1}} | {{resp_1}} |
| {{controle_2}} | {{threshold_2}} | {{acao_auto_2}} | {{resp_2}} |

---

## Instruções de Preenchimento

1. **Nome oficial:** Use nome padronizado. Evite sinônimos diferentes em diferentes relatórios.
2. **Fórmula:** Seja matematicamente preciso. Ex.: "MRR = Soma de (valor de cada assinatura ativa no
   último dia do mês, excluindo trials e clientes em período de graça)".
3. **Exclusões:** Tão importante quanto a definição. Documente explicitamente o que NÃO entra no cálculo.
4. **SSOT:** Deve haver UMA fonte oficial. Se há múltiplas, defina qual é a master.
5. **Lineage:** Documente todo o caminho do dado, da origem ao dashboard final.
6. **Qualidade:** Avalie periodicamente. Dados de baixa qualidade geram decisões ruins.
7. **Mudanças:** Sempre documente mudanças na definição. Quebras de série histórica devem ser sinalizadas.

## Exemplo Preenchido

---

### FICHA — MRR (Monthly Recurring Revenue)

| Atributo | Valor |
|----------|-------|
| **Nome oficial** | Monthly Recurring Revenue |
| **Sigla** | MRR |
| **Owner** | CFO Agent |
| **Definição** | Soma do valor mensal normalizado de todas as assinaturas ativas no último dia do mês |
| **Fórmula** | SUM(subscription_value_monthly) WHERE status = 'active' AND date = last_day_of_month |
| **Unidade** | R$ (BRL) |
| **Fonte (SSOT)** | Billing System (Stripe) |
| **Filtros** | Exclui trials, clientes em grace period, créditos |
| **Frequência** | Mensal (D+1) |

#### Regras
| # | Regra | Exemplo |
|---|-------|---------|
| 1 | Assinaturas anuais são divididas por 12 | R$ 12K/ano = R$ 1K MRR |
| 2 | Descontos são refletidos no MRR | Plano R$ 500 com 20% off = R$ 400 MRR |
| 3 | Upgrades mid-month entram pro-rata | Upgrade dia 15 = 50% do delta |

---

## Checklist de Qualidade

- [ ] Nome oficial é único e sem sinônimos conflitantes
- [ ] Fórmula é matematicamente precisa e reproduzível
- [ ] Exclusões estão explicitamente documentadas
- [ ] SSOT está definida (uma única fonte oficial)
- [ ] Data lineage completo documentado
- [ ] Qualidade do dado avaliada nas 5 dimensões
- [ ] Histórico de mudanças na definição registrado
- [ ] Métricas relacionadas referenciadas
- [ ] Controles e alertas configurados
- [ ] Owner da métrica revisou e aprovou a ficha
