# CIO Data as Product — Mentalidade de Dados como Produto

## Origem e Contexto

A maioria das organizações trata dados como subproduto de sistemas operacionais — dados existem
porque sistemas funcionam, não porque foram projetados para gerar valor. A mentalidade "Data as
Product" inverte essa lógica: dados são tratados como produtos de primeira classe, com owner,
SLA de qualidade, documentação e consumidores definidos.

O resultado da abordagem tradicional é previsível: data lakes que viram data swamps, relatórios
que ninguém confia, decisões tomadas no "achismo" porque dados estão sujos ou indisponíveis, e
times de dados sobrecarregados atendendo requests ad-hoc.

Este framework se baseia nos princípios de Data Mesh (Zhamak Dehghani), Data Contracts (Andrew
Jones), e Data Quality Management (DAMA-DMBOK). Adaptado para organizações que querem
democratizar acesso a dados sem sacrificar qualidade ou governança.

## Quando Usar

- Na implementação de estratégia de dados organizacional
- Quando a qualidade dos dados é uma reclamação recorrente
- Ao construir ou evoluir plataforma de dados/analytics
- Quando times de dados estão sobrecarregados com requests
- Na transição de data lake centralizado para modelo distribuído
- Ao implementar self-serve analytics

## Quando NÃO Usar

- Em organizações com poucos dados e necessidades simples
- Como substituto para data warehouse bem implementado (complementar)
- Quando não há data literacy mínima na organização
- Sem sponsorship executivo e governance clara

## Estrutura / Modelo

### Modelo Data Product Canvas

```
┌─────────────────────────────────────────────────────┐
│           DATA AS PRODUCT MODEL                      │
│                                                      │
│  ┌──────────┐   ┌──────────┐   ┌──────────┐       │
│  │  DATA    │──→│  DATA    │──→│  DATA    │       │
│  │ PRODUCER │   │ PRODUCT  │   │ CONSUMER │       │
│  │ (domain) │   │(curated) │   │ (user)   │       │
│  └──────────┘   └────┬─────┘   └──────────┘       │
│                      │                              │
│               ┌──────▼──────┐                       │
│               │   DATA      │                       │
│               │  CONTRACT   │                       │
│               │(SLA+schema) │                       │
│               └──────┬──────┘                       │
│                      │                              │
│         ┌────────────┼────────────┐                 │
│         │            │            │                 │
│    ┌────▼────┐  ┌────▼────┐  ┌───▼─────┐          │
│    │QUALITY  │  │DISCOVERY│  │GOVERNANCE│          │
│    │MONITORING│  │ CATALOG │  │ ACCESS  │          │
│    └─────────┘  └─────────┘  └─────────┘          │
└─────────────────────────────────────────────────────┘
```

### Princípios de Data Mesh (adaptados)

| Princípio | Descrição | Implicação |
|-----------|-----------|-----------|
| **Domain Ownership** | Cada domínio é dono dos seus dados | Times de produto gerenciam seus dados |
| **Data as Product** | Dados tratados como produto com UX | Owner, SLA, documentação, versioning |
| **Self-serve Platform** | Plataforma que democratiza acesso | Data platform team como enabler |
| **Federated Governance** | Governança distribuída + padrões globais | Standards centrais, execução local |

### Data Product Card

```
DATA PRODUCT CARD
━━━━━━━━━━━━━━━━━
Nome: [ex: customer_360]
Owner (DRI): [time/pessoa]
Domínio: [ex: Customer]
Descrição: [o que este data product contém e para que serve]
Consumers: [quais times/dashboards usam]

Schema:
- customer_id (string, PK)
- name (string)
- ltv (decimal)
- segment (enum: enterprise|mid|smb)
- last_activity_date (date)

SLA:
- Freshness: atualizado a cada 1h
- Completeness: >99% dos campos obrigatórios
- Accuracy: >98% validado por sample audit
- Availability: 99.9% uptime

Data Contract Version: 2.1
Breaking Changes Policy: 30 dias de deprecation notice
```

## Processo de Aplicação (step-by-step)

### Step 1: Inventário de Dados Existentes

Mapear todos os dados da organização:

| Domínio | Fonte | Tipo | Owner Atual | Qualidade | Consumers |
|---------|-------|------|-------------|-----------|-----------|
| Customer | CRM | Relacional | Vendas | Média | Marketing, CS, Finance |
| Product | Backend DB | Relacional | Engineering | Alta | Product, Analytics |
| Financial | ERP | Relacional | Finance | Alta | CFO, Board |
| Marketing | Multiple SaaS | Semi-estruturado | Marketing | Baixa | Growth, Exec |
| Usage | Event stream | Streaming | Engineering | Alta | Product, ML |

### Step 2: Identificar Data Products Prioritários

Critérios de priorização:

| Critério | Peso | Escala |
|----------|------|--------|
| Número de consumers | 30% | 1-10 |
| Impacto em decisões | 30% | 1-10 |
| Qualidade atual (inverso) | 20% | 1-10 |
| Facilidade de implementar | 20% | 1-10 |

**Começar com 3-5 data products de maior impacto.**

### Step 3: Definir Data Contracts

Para cada data product, formalizar contrato:

- **Schema**: campos, tipos, validações
- **SLA de qualidade**: freshness, completeness, accuracy
- **Access patterns**: como consumidores acessam (API, query, export)
- **Breaking changes policy**: como mudanças são comunicadas
- **Support**: quem contatar em caso de problema

### Step 4: Implementar Data Quality Monitoring

Monitorar qualidade continuamente:

| Dimensão | Métrica | Ferramenta |
|----------|---------|-----------|
| **Freshness** | Última atualização vs SLA | Automático |
| **Completeness** | % de campos non-null | Great Expectations |
| **Accuracy** | Sample audit vs source of truth | Manual + automático |
| **Consistency** | Cross-source validation | Automático |
| **Uniqueness** | Duplicatas detectadas | Automático |

**Alertas**: quando qualidade cai abaixo do SLA, owner é notificado.

### Step 5: Construir Data Catalog (Discovery)

Implementar catálogo de dados para discovery:

- Cada data product documentado e pesquisável
- Lineage: de onde vem, para onde vai
- Popularidade: quais data products são mais usados
- Quality score: score de qualidade visível
- Owner: quem contatar para dúvidas

**Ferramentas**: DataHub, Atlan, Amundsen, ou seção no wiki interno.

### Step 6: Self-Serve Analytics

Democratizar acesso com segurança:

| Nível | Quem | Acesso | Ferramenta |
|-------|------|--------|-----------|
| **L1** | Todos | Dashboards pré-construídos | Metabase/Looker |
| **L2** | Power users | SQL em datasets curados | Query tool |
| **L3** | Analysts | Acesso a data warehouse | dbt + SQL |
| **L4** | Data engineers | Acesso a raw data | Spark/dbt |

**Princípio**: dados sensíveis requerem permissão explícita em todos os níveis.

### Step 7: Governança Federada

Modelo de governança que equilibra autonomia e controle:

**Global (definido centralmente)**:
- Naming conventions
- PII/data classification standards
- Access control policies
- Quality SLA mínimos

**Local (definido por domínio)**:
- Schema específico do data product
- Qualidade acima do mínimo
- Schedule de atualização
- Documentação específica

**Referência**: `checklists/cio/data-governance-audit.md`

## Exemplos Práticos

### Exemplo 1: Customer 360 como Data Product

**Antes**: dados de cliente espalhados em CRM, backend, billing, support
**Depois**: data product `customer_360` com:
- Todos os dados consolidados e deduplicados
- Atualização a cada 30 minutos
- Consumido por 8 times diferentes
- Quality score: 96%
- Owner: time de Customer Data

**Impacto**: tempo para responder "quem é esse cliente?" caiu de horas para segundos.

### Exemplo 2: Revenue Metrics como Data Product

**Antes**: cada time calculava receita de forma diferente (5 versões da verdade)
**Depois**: data product `revenue_metrics` com:
- Definição única e documentada de cada métrica
- ARR, MRR, NRR, churn calculados centralmente
- Data contract versionado
- Consumido por Finance, Board, Product, Marketing

**Impacto**: zero discrepância em reuniões de board. Confiança nas métricas.

## Armadilhas Comuns

1. **Data swamp**: data lake sem governança vira pântano inutilizável
2. **Centralizar tudo**: time central de dados vira bottleneck
3. **Descentralizar tudo**: sem padrões, cada time faz de um jeito
4. **Qualidade como afterthought**: data product sem SLA de qualidade
5. **Build it and they will come**: data product que ninguém usa
6. **Schema sem contrato**: mudança quebra consumidores sem aviso
7. **Governance como bloqueio**: governança tão pesada que impede acesso
8. **Ignorar PII**: dados pessoais sem classificação e controle

## Integração com Outros Frameworks

| Framework | Relação |
|-----------|---------|
| `frameworks/cio-engineer/cio-systems-rationalization.md` | Dados nos sistemas racionalizados |
| `frameworks/cio-engineer/cio-integration-architecture.md` | Integração de dados entre sistemas |
| `frameworks/cio-engineer/cio-automation-first.md` | Automação de data pipelines |
| `frameworks/ai/ai-strategy.md` | Dados como foundation para IA |
| `frameworks/ai/mlops.md` | Feature store e data pipelines de ML |
| `checklists/cio/data-governance-audit.md` | Auditoria de governança de dados |

## Referências

- Zhamak Dehghani, "Data Mesh" (O'Reilly, 2022)
- Andrew Jones, "Driving Data Quality with Data Contracts" (2023)
- DAMA International, "DAMA-DMBOK: Data Management Body of Knowledge"
- DJ Patil, "Data Jujitsu" (O'Reilly, 2012)
- Maxime Beauchemin, "The Rise of the Data Engineer" (2017)
- Chad Sanderson, "Data Contracts" blog series
- C-Level Squad: `checklists/cio/data-governance-audit.md`
