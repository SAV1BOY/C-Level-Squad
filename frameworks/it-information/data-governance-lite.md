# Data Governance Lite — Governança Pragmática de Dados

> **Domínio:** IT & Information
> **Origem:** DAMA-DMBOK, Data Mesh (Zhamak Dehghani), adaptado para empresas de tecnologia
> **Uso primário:** Estabelecer ownership, qualidade, catalogação e lineage de dados de forma pragmática.
> **Agente responsável:** cio-engineer

---

## Origem e Contexto

Governança de dados é o conjunto de políticas, processos e responsabilidades que garantem que dados sejam tratados como ativo estratégico — confiáveis, acessíveis, seguros e úteis para decisão. O DAMA-DMBOK (Data Management Body of Knowledge) é a referência acadêmica; o Data Mesh de Zhamak Dehghani é a referência moderna para empresas descentralizadas.

O problema: **governança de dados tradicional é pesada demais para empresas ágeis.** Comitês de governança, processos de aprovação de 6 etapas e ferramentas enterprise que custam mais do que o valor que entregam. O Data Governance Lite extrai os princípios essenciais e os torna operacionais para contextos de 50-500 pessoas.

### Os 4 Pilares do Data Governance Lite

| Pilar | Pergunta | Resultado |
|-------|---------|----------|
| **Ownership** | Quem é responsável por este dado? | DRI claro para cada dataset |
| **Quality** | Os dados são confiáveis? | Métricas de qualidade monitoradas |
| **Catalog** | Que dados existem e onde? | Catálogo acessível e atualizado |
| **Lineage** | De onde vem o dado e para onde vai? | Mapa de origem → transformação → consumo |

---

## Quando Usar

- **Quando decisões são baseadas em dados inconsistentes** — "Os números do marketing não batem com os de finance."
- **Quando ninguém sabe onde encontrar dados** — "Quem tem o dado de churn atualizado?"
- **Para compliance (LGPD, GDPR)** — governança é pré-requisito para privacidade e compliance.
- **Quando dados duplicados proliferam** — múltiplas fontes de verdade para a mesma métrica.
- **Quando o time de dados cresce** — com mais de 3-5 pessoas mexendo em dados, governança evita caos.

---

## Quando NÃO Usar

- **Empresas com < 5 pessoas usando dados** — nessa escala, um spreadsheet e comunicação resolvem.
- **Como projeto big-bang** — governança implementada de uma vez falha. Faça incremental.
- **Para burocratizar acesso** — governança deve facilitar acesso a dados, não dificultar.
- **Sem problema real** — se os dados são confiáveis e acessíveis, não adicione processo por adicionar.

---

## Estrutura / Modelo

### 1. Data Ownership

**Princípio:** Todo dataset tem exatamente um DRI (Data Owner) que responde pela qualidade e definição.

**Modelo de papéis:**
| Papel | Responsabilidade | Quem |
|-------|-----------------|------|
| **Data Owner** | Define o que o dado significa, quem pode acessar, e é DRI da qualidade | Líder de domínio (produto, finance, marketing) |
| **Data Steward** | Operacionaliza as políticas do Owner: monitora qualidade, corrige problemas | Analista de dados ou engenheiro |
| **Data Consumer** | Usa os dados para análise e decisão | Qualquer pessoa autorizada |
| **Data Engineer** | Constrói e mantém pipelines de dados | Time de engenharia de dados |

**Regra fundamental:** O Data Owner é do domínio de negócio, não do time de dados. O time de dados facilita; o negócio é dono.

### 2. Data Quality

**As 6 Dimensões de Qualidade de Dados:**

| Dimensão | Definição | Como Medir | Exemplo |
|----------|-----------|-----------|---------|
| **Accuracy** | Dados refletem a realidade | % de registros corretos vs. source of truth | Revenue no dashboard = revenue no ERP? |
| **Completeness** | Campos obrigatórios preenchidos | % de nulls/blanks em campos críticos | % de leads com email válido |
| **Consistency** | Mesmo dado = mesmo valor em sistemas diferentes | Comparação cross-system | Número de clientes no CRM vs. no billing |
| **Timeliness** | Dados disponíveis quando necessário | Freshness (delay entre evento e disponibilidade) | Dashboard de revenue atualizado em < 1h |
| **Uniqueness** | Sem duplicatas | % de duplicatas identificadas | Mesmo cliente aparece 2x no CRM? |
| **Validity** | Dados seguem formato e regras de negócio | % de registros que passam em data validation | CPF com formato válido? |

**Data Quality Score:**
- Calcule score por dataset (0-100) com peso para cada dimensão.
- Defina threshold: datasets com score < 80 entram em plano de correção.
- Monitore no MBR.

### 3. Data Catalog

**O que catalogar (mínimo viável):**

```
Para cada dataset:
├── Nome e descrição
├── Data Owner (DRI)
├── Localização (sistema, schema, tabela)
├── Classificação de sensibilidade (público, interno, confidencial, PII)
├── Frequência de atualização
├── Métricas de qualidade
├── Consumidores principais
└── Políticas de retenção
```

**Ferramentas (por estágio):**
| Estágio | Ferramenta | Custo |
|---------|-----------|-------|
| Início | Spreadsheet/Notion | Zero |
| Crescimento | DataHub, Amundsen, OpenMetadata (open-source) | Infra |
| Escala | Atlan, Alation, Collibra | SaaS enterprise |

### 4. Data Lineage

**Objetivo:** Saber de onde cada dado veio, que transformações sofreu e para onde vai.

```
Source (ERP, CRM, API)
    │
    ▼
Ingestion (ETL/ELT)
    │
    ▼
Transformation (dbt, Spark)
    │
    ▼
Storage (Data Warehouse)
    │
    ▼
Consumption (Dashboard, Report, ML Model)
```

**Por que lineage importa:**
- Quando um número no dashboard está errado, lineage mostra onde o erro pode estar.
- Quando uma source muda, lineage mostra quais consumidores são afetados.
- Para compliance (LGPD): lineage mostra onde dados pessoais estão.

---

## Processo de Aplicação (step-by-step)

### Passo 1: Inventariar datasets críticos
- Liste os 10-20 datasets mais usados na organização.
- Para cada um: nome, localização, quem usa, para que serve.
- Priorize por impacto no negócio.

### Passo 2: Atribuir Data Owners
- Para cada dataset, defina o DRI (do negócio, não de TI).
- O Owner define: o que o dado significa, quem acessa, qual o SLO de qualidade.
- Publique a lista de ownership (transparência).

### Passo 3: Medir qualidade baseline
- Rode checks de qualidade nos datasets críticos.
- Meça as 6 dimensões para cada um.
- Calcule Data Quality Score.
- Identifique os datasets com pior qualidade — esses são prioridade.

### Passo 4: Catalogar
- Comece com o catálogo dos datasets críticos (spreadsheet é OK no início).
- Inclua: nome, descrição, owner, localização, sensibilidade, freshness.
- Torne acessível para toda a organização (não em uma pasta escondida).

### Passo 5: Mapear lineage dos datasets críticos
- Para os 5 datasets mais importantes, mapeie source → transformation → consumption.
- Use ferramentas de lineage automático se possível (dbt lineage, Great Expectations).
- Documente manualmente onde automação não é possível.

### Passo 6: Implementar monitoramento contínuo
- Data quality checks automatizados rodando diariamente.
- Alertas quando qualidade cai abaixo do threshold.
- Dashboard de Data Quality Score visível no MBR.

### Passo 7: Políticas de LGPD/privacidade
- Classifique dados por sensibilidade (público, interno, confidencial, PII).
- Defina políticas de acesso por classificação.
- Implemente retenção: por quanto tempo cada tipo de dado é mantido?
- Documente: onde estão dados pessoais (PII)? Quem acessa? Qual a base legal?

---

## Exemplos Práticos

### Exemplo: Data Quality Dashboard (MBR)

| Dataset | Owner | Accuracy | Completeness | Freshness | Score | Status |
|---------|-------|----------|-------------|-----------|-------|--------|
| Revenue | CFO | 98% | 100% | Real-time | 96 | 🟢 |
| Leads | CMO | 85% | 78% | 2h delay | 72 | 🔴 |
| Users | CPO | 95% | 92% | 30min | 88 | 🟢 |
| Tickets | COO | 90% | 65% | 1h delay | 70 | 🔴 |

**Ação:** Leads e Tickets com score < 80 → plano de correção com DRI e prazo.

---

## Armadilhas Comuns

1. **Governança como projeto** — governança é prática contínua, não projeto com data de fim.
2. **TI como Data Owner** — TI facilita; o negócio é dono. O CFO é dono dos dados financeiros, não o DBA.
3. **Catálogo que ninguém usa** — se o catálogo não é fácil de encontrar e usar, não existe.
4. **Qualidade sem monitoramento** — medir qualidade uma vez e nunca mais é inútil. Automatize checks.
5. **Governança que bloqueia acesso** — o objetivo é tornar dados confiáveis E acessíveis, não apenas seguros.
6. **Big-bang implementation** — tentar governar todos os dados de uma vez. Comece com os 10-20 datasets críticos.
7. **Ignorar LGPD** — não saber onde estão dados pessoais é risco legal real.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| **Enterprise Architecture Lite** | EA mapeia sistemas; governance define qualidade dos dados dentro deles |
| **ITIL Light** | Configuration Management inclui ativos de dados |
| **WBR/MBR/QBR** | Data Quality Score é métrica do scorecard operacional |
| **OKRs** | Data quality pode ser KR de OKRs do CIO |
| **Decision Memo** | Decisões baseadas em dados devem referenciar qualidade dos dados usados |
| **RASI/DRI** | Data Ownership segue o modelo RASI com DRI claro |

---

## Referências

1. DAMA International. (2017). *DAMA-DMBOK: Data Management Body of Knowledge*. 2nd ed. Technics Publications.
2. Dehghani, Z. (2022). *Data Mesh*. O'Reilly.
3. Redman, T. (2008). *Data Driven: Profiting from Your Most Important Business Asset*. Harvard Business Review Press.
4. Brasil. (2018). *Lei Geral de Proteção de Dados Pessoais (LGPD)*. Lei 13.709/2018.
5. Atlan. "Data Governance for Modern Data Teams." atlan.com.
