# Framework de Plataforma de Dados — Arquitetura e Governança

## Propósito e Contexto

A plataforma de dados é a infraestrutura que permite à organização coletar, armazenar, processar,
analisar e governar dados de forma confiável e escalável. Não é um projeto — é um produto
interno que serve toda a organização. Sem uma plataforma de dados sólida, a empresa opera com
decisões baseadas em intuição, reports que ninguém confia, e silos de dados que impedem
colaboração cross-funcional.

Este framework estrutura a construção e evolução de uma plataforma de dados moderna, seguindo
princípios de data mesh (ownership distribuído) com governança federada. O objetivo é que
qualquer pessoa na organização consiga acessar dados confiáveis em minutos, não dias.

## Quando Usar

- Na construção da primeira plataforma de dados da empresa
- Quando há proliferação de planilhas, exports manuais e "fontes de verdade" conflitantes
- Ao preparar a organização para uso de AI/ML (dados são o combustível)
- Quando requisitos de compliance exigem governança de dados (LGPD)
- Na integração de dados pós-M&A
- Quando a equipe de dados gasta mais tempo limpando do que analisando

## Componentes do Framework

### 1. Arquitetura de Referência (Modern Data Stack)

```
FONTES                    INGESTÃO           ARMAZENAMENTO        TRANSFORMAÇÃO
├── Bancos de Produção    ├── CDC/Debezium   ├── Data Lake        ├── dbt
├── APIs de SaaS          ├── Fivetran/      │   (S3/GCS)         ├── Spark
├── Event Streams         │   Airbyte        ├── Data Warehouse   └── SQL Models
├── Arquivos/Planilhas    └── Kafka          │   (BigQuery/
└── IoT/Devices                              │    Snowflake/
                                             │    Redshift)
                                             └── Feature Store
                                                 (para ML)

SERVINDO                  GOVERNANÇA          OBSERVABILIDADE
├── BI / Dashboards       ├── Catálogo        ├── Data Quality
│   (Metabase/Looker)     │   (DataHub/       │   (Great
├── Self-service          │    Amundsen)       │    Expectations)
│   Analytics             ├── Linhagem        ├── Pipeline
├── Reverse ETL           ├── Classificação   │   Monitoring
├── APIs de Dados         ├── Access Control  └── SLAs de
└── ML Platform           └── LGPD/Privacy        Freshness
```

### 2. Modelo de Governança (Data Mesh Adaptado)

**Princípio 1: Domain Ownership**
Cada time de produto é dono dos dados que gera. Não existe "time de dados" que cuida de tudo.
- O time de pagamentos é dono dos dados de transações
- O time de produto é dono dos dados de engagement
- O time de vendas é dono dos dados de pipeline

**Princípio 2: Data as a Product**
Dados compartilhados são tratados como produtos:
- Documentação clara (schema, significado de cada campo)
- SLAs de freshness e qualidade
- Versionamento e backward compatibility
- Discoverability via catálogo

**Princípio 3: Self-Service Platform**
O time de data platform fornece a infraestrutura, não os dados:
- Ferramentas de ingestão configuráveis
- Templates de transformação (dbt models)
- Ambiente self-service para queries
- Pipelines como código (CI/CD para dados)

**Princípio 4: Federated Governance**
Governança centralizada em políticas, descentralizada em execução:
- Políticas de classificação e acesso são centrais
- Implementação de classificação é responsabilidade do domain owner
- Compliance (LGPD) é verificado automaticamente

### 3. Data Quality Framework

**Dimensões de Qualidade:**
| Dimensão | Definição | Teste Automatizado |
|----------|-----------|-------------------|
| Completeness | Campos obrigatórios preenchidos | NOT NULL checks |
| Uniqueness | Sem duplicatas em chaves únicas | Unique constraints |
| Timeliness | Dados atualizados dentro do SLA | Freshness checks |
| Accuracy | Valores dentro de ranges esperados | Range e distribution checks |
| Consistency | Mesma informação igual em fontes diferentes | Cross-source validation |

**SLAs de Dados:**
- Dados operacionais (real-time): < 5 minutos de atraso
- Dados analíticos (batch): < 4 horas após o fechamento do dia
- Dados de ML features: definido por caso (real-time a diário)

## Processo Passo-a-Passo

### Fase 1: Foundation (mês 1-2)
1. Escolher stack tecnológica (warehouse, ingestão, transformação)
2. Implementar primeira pipeline end-to-end (um domain crítico)
3. Setup de data quality checks básicos
4. Documentar schema e significado dos dados

### Fase 2: Expansion (mês 3-4)
1. Onboardar 2-3 domains adicionais
2. Implementar catálogo de dados
3. Self-service analytics para stakeholders-chave
4. Classificação de dados para LGPD

### Fase 3: Maturidade (mês 5-8)
1. Data quality automatizado em todas as pipelines
2. Linhagem de dados (lineage) implementada
3. Reverse ETL para ativar dados em ferramentas operacionais
4. Feature store para ML (se aplicável)

### Fase 4: Otimização (ongoing)
1. Performance tuning de queries e pipelines
2. Cost optimization (storage tiers, compute scheduling)
3. Adoção de data mesh principles (domain ownership)
4. Advanced governance (privacy, compliance automatizado)

## Template de Data Product Spec

```markdown
# Data Product: [Nome]

**Domain Owner:** [Time responsável]
**Steward:** [Pessoa responsável pela qualidade]

## Descrição
[O que este dataset representa e para que serve]

## Schema
| Campo | Tipo | Descrição | PII? | Obrigatório? |
|-------|------|-----------|------|-------------|
| [nome] | [tipo] | [desc] | [S/N] | [S/N] |

## SLA
- Freshness: [intervalo de atualização]
- Quality score target: > [X]%
- Availability: [SLA]

## Consumers
- [Time/pessoa que usa este dataset e para quê]

## Linhagem
- Sources: [de onde vêm os dados]
- Dependências: [outros datasets que dependem deste]
```

## Checklist de Data Platform

- [ ] Warehouse/Lake implementado e acessível?
- [ ] Pelo menos 1 pipeline end-to-end funcionando?
- [ ] Data quality checks automatizados?
- [ ] Catálogo de dados acessível?
- [ ] Classificação LGPD implementada para dados PII?
- [ ] Self-service analytics disponível para stakeholders?
- [ ] Backup e disaster recovery para dados críticos?
- [ ] Custos monitorados e otimizados?

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Data freshness SLA compliance | > 95% | Diário |
| Data quality score (média) | > 90% | Semanal |
| Self-service adoption | > 50% das queries feitas por não-data-team | Mensal |
| Time-to-insight (novo report) | < 1 dia | Por request |
| Pipeline failures | < 5% das execuções | Semanal |
| Catálogo coverage | > 80% dos datasets documentados | Trimestral |
| LGPD compliance | 100% dos dados PII classificados | Contínuo |

## Referências Cruzadas

- `frameworks/cio-engineer/cloud-strategy.md` — Infraestrutura cloud para dados
- `frameworks/cio-engineer/security-posture.md` — Segurança e classificação de dados
- `frameworks/cio-engineer/digital-transformation.md` — Dados como pilar da transformação
- `frameworks/caio-architect/ai-maturity-model.md` — Dados como fundação para AI
- `frameworks/caio-architect/mlops-framework.md` — Feature store e data pipelines para ML
- `frameworks/caio-architect/ai-governance.md` — Governança de dados para AI
- `frameworks/cfo-strategist/unit-economics.md` — Dados para cálculo de unit economics
