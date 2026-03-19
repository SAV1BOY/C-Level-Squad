# CIO Systems Rationalization — Racionalização do Portfólio de Sistemas

## Origem e Contexto

Toda organização com mais de 5 anos de vida acumula sistemas como uma casa acumula objetos: cada
um entrou por uma boa razão, mas o conjunto se torna caótico, redundante e caro. Systems
rationalization é o processo disciplinado de inventariar, avaliar e otimizar o portfólio de
aplicações e sistemas da organização.

O CIO que não faz rationalization opera no escuro — não sabe quanto custa cada sistema, quantos
são redundantes, quais estão em risco de fim de suporte, e quais geram dependências perigosas.
O resultado: 30-40% do budget de TI gasta em manter sistemas que deveriam ter sido aposentados.

Este framework se baseia no modelo TIME (Gartner — Tolerate, Invest, Migrate, Eliminate), nos
princípios de Application Portfolio Management (APM), e nas práticas de modernização de legacy
systems. Adaptado para CIOs que precisam justificar investimentos de racionalização.

## Quando Usar

- Na revisão anual do portfólio de sistemas
- Quando custos de TI crescem sem aumento proporcional de valor
- Após M&A (merge de dois portfólios de sistemas)
- Quando há sistemas redundantes para mesma função
- Na preparação para migração cloud ou modernização
- Quando sistemas legados bloqueiam inovação

## Quando NÃO Usar

- Como justificativa para cortar custos sem análise (cortar tudo não é racionalizar)
- Durante crise operacional (estabilizar primeiro)
- Sem sponsorship executivo (racionalização afeta toda a empresa)
- Como projeto único (deve ser prática contínua)

## Estrutura / Modelo

### Modelo TIME de Classificação

```
┌─────────────────────────────────────────────────────┐
│           APPLICATION PORTFOLIO MATRIX                │
│                                                      │
│  Alto  │ INVEST          │ MIGRATE                   │
│  Valor │ (modernizar,    │ (migrar para              │
│  Negócio│ escalar)       │ plataforma melhor)        │
│        │─────────────────│──────────────────────────  │
│  Baixo │ TOLERATE        │ ELIMINATE                  │
│  Valor │ (manter         │ (aposentar,               │
│  Negócio│ como está)     │ consolidar)               │
│        └────────────────────────────────────────────  │
│          Bom Estado           Mau Estado              │
│               QUALIDADE TÉCNICA                      │
└─────────────────────────────────────────────────────┘
```

### Critérios de Avaliação por Sistema

| Dimensão | Critério | Peso | Escala |
|----------|---------|------|--------|
| **Valor de Negócio** | Quantos processos críticos suporta? | 25% | 1-10 |
| | Quantos usuários dependem dele? | 15% | 1-10 |
| | Há alternativa interna? | 10% | 1-10 |
| **Qualidade Técnica** | Estado da tecnologia (current/legacy/EOL) | 15% | 1-10 |
| | Custo de manutenção (TCO anual) | 15% | 1-10 |
| | Risco de segurança/compliance | 10% | 1-10 |
| | Capacidade de integração | 10% | 1-10 |

### Custo Real de Manter Sistemas

| Componente de Custo | Visível? | Exemplo |
|--------------------|---------|---------| 
| Licenças/assinaturas | Sim | R$ X/ano |
| Infraestrutura (hosting) | Sim | R$ Y/ano |
| Suporte vendor | Sim | R$ Z/ano |
| Time de manutenção | Parcial | FTEs dedicados × custo |
| Integração e workarounds | Não | Horas de dev em gambiarras |
| Treinamento contínuo | Não | Onboarding lento, erros |
| Risco de security breach | Não | Custo potencial de incidente |
| Custo de oportunidade | Não | O que faria com recursos liberados? |

## Processo de Aplicação (step-by-step)

### Step 1: Inventário Completo (Application Inventory)

Catalogar TODOS os sistemas da organização:

```
APPLICATION INVENTORY
━━━━━━━━━━━━━━━━━━━━
Sistema        | Categoria  | Owner  | Usuários | TCO/Ano  | Tech Stack | Status
───────────────|────────────|────────|──────────|──────────|────────────|──────
ERP [nome]     | Core       | [DRI]  | 200      | R$500K   | SAP/Oracle | Invest
CRM [nome]     | Core       | [DRI]  | 80       | R$200K   | Salesforce | Invest
Legacy Portal  | Custom     | [DRI]  | 30       | R$150K   | PHP 5.6   | Eliminate
Planilhas X    | Shadow IT  | [DRI]  | 15       | R$0*     | Excel     | Migrate
BI Tool        | Analytics  | [DRI]  | 50       | R$100K   | Tableau   | Tolerate
```

### Step 2: Classificação TIME

Para cada sistema, aplicar classificação:

- **Tolerate**: sistema funciona, valor razoável, não é prioridade mexer
- **Invest**: sistema core, precisa evoluir para suportar estratégia
- **Migrate**: valor alto mas qualidade técnica baixa — migrar para plataforma melhor
- **Eliminate**: baixo valor, alto custo — aposentar ou consolidar

### Step 3: Análise de Redundância

Mapear sistemas redundantes por função:

```
REDUNDANCY MAP
━━━━━━━━━━━━━━━
Função              | Sistemas         | Decisão
────────────────────|──────────────────|────────────────
Project Management  | Jira, Asana, Monday | Consolidar em 1
Email Marketing     | Mailchimp, HubSpot  | Migrar para HubSpot
BI/Analytics       | Tableau, Metabase, Excel | Investir em Metabase
File Storage       | Drive, Dropbox, SharePoint | Consolidar em 1
```

### Step 4: Roadmap de Racionalização

Priorizar ações com base em impacto e esforço:

| Prioridade | Ação | Impacto | Esforço | Timeline |
|-----------|------|---------|---------|----------|
| P1 | Eliminar sistema X (R$150K/ano saving) | Alto | Baixo | Q1 |
| P2 | Consolidar BI tools (R$80K saving + data quality) | Alto | Médio | Q2 |
| P3 | Migrar legacy portal para stack moderno | Alto | Alto | Q2-Q3 |
| P4 | Renegociar contrato ERP | Médio | Baixo | Q1 |

### Step 5: Plano de Sunset (Aposentadoria)

Para cada sistema a ser eliminado:

```
SUNSET PLAN — [Nome do Sistema]
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Data de sunset: [data]
Owner: [DRI]
Usuários atuais: [lista]
Dados a migrar: [sim/não, para onde]
Integrações a desconectar: [lista]
Alternativa para usuários: [sistema substituto]
Comunicação: [plano de comunicação]
Rollback plan: [se der errado]
Kill criteria: [quando considerar concluído]
```

### Step 6: Shadow IT Discovery

Mapear sistemas não oficiais (shadow IT):

- Planilhas compartilhadas que funcionam como sistemas
- SaaS contratados por áreas sem TI saber
- Automações em ferramentas pessoais (Zapier, Make)
- Databases locais ou em cloud pessoal

**Abordagem**: não punir, incorporar ou oferecer alternativa melhor.

### Step 7: Governança Contínua

Estabelecer processo para evitar recorrência:

- **Approval process**: novo sistema requer aprovação do CIO
- **Annual review**: revisão anual do portfólio completo
- **Consolidation check**: antes de comprar novo, verificar se já existe
- **Sunset calendar**: datas de sunset planejadas e rastreadas

**Checklist**: `checklists/cio/systems-portfolio-audit.md`

## Exemplos Práticos

### Exemplo 1: Scale-up com 150 Funcionários

**Inventário**: 47 sistemas catalogados, 12 eram shadow IT
**Ações**:
- Eliminar 8 sistemas redundantes (saving R$280K/ano)
- Consolidar 3 tools de PM em 1 (Jira)
- Migrar 2 legacy apps para stack moderno
**Resultado**: 22% redução no custo de TI, 30% menos integrações a manter

### Exemplo 2: Pós-M&A

**Contexto**: empresa A (SAP) adquiriu empresa B (Oracle ERP)
**Racionalização**: 
- Manteve SAP como sistema principal (maior base)
- Migrou dados de Oracle para SAP (12 meses)
- Eliminou 15 sistemas duplicados entre as empresas
**Resultado**: R$2M saving anual, operação unificada em 18 meses

## Armadilhas Comuns

1. **Inventário incompleto**: não catalogar shadow IT e sistemas informais
2. **Subestimar custos de migração**: eliminar parece fácil até calcular custo de transição
3. **Ignorar usuários**: aposentar sistema sem alternativa gera shadow IT novo
4. **Big bang migration**: migrar tudo de uma vez é receita para desastre
5. **Foco só em custo**: racionalizar só por custo ignora valor estratégico
6. **Sem sponsorship**: racionalização sem apoio executivo não funciona
7. **One-time project**: fazer uma vez e não repetir (sistemas acumulam de novo)
8. **Não medir resultado**: não rastrear savings e benefícios realizados

## Integração com Outros Frameworks

| Framework | Relação |
|-----------|---------|
| `frameworks/cio-engineer/cio-integration-architecture.md` | Integração entre sistemas |
| `frameworks/cio-engineer/cio-automation-first.md` | Automatizar antes de racionalizar |
| `frameworks/cio-engineer/cio-data-as-product.md` | Dados nos sistemas racionalizados |
| `frameworks/it-information/total-cost-of-ownership.md` | TCO de cada sistema |
| `frameworks/cio-engineer/cloud-strategy.md` | Cloud como destino de migração |
| `checklists/cio/systems-portfolio-audit.md` | Auditoria do portfólio |
| `checklists/cio/cio-total-cost-of-ownership-audit.md` | Auditoria de TCO |

## Referências

- Gartner, "TIME Model for Application Rationalization"
- McKinsey, "Application Portfolio Optimization"
- Forrester, "Application Modernization" research
- Martin Fowler, "Strangler Fig Pattern" (para migração de legados)
- C-Level Squad: `checklists/cio/systems-portfolio-audit.md`
