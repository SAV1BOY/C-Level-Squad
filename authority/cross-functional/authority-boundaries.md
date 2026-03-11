# Limites de Autoridade entre Agentes

## Visao Geral

Este documento define os limites claros de autoridade entre os agentes do C-Level Squad, identificando zonas exclusivas, zonas compartilhadas e zonas proibidas para cada agente. O objetivo e eliminar ambiguidade, evitar sobreposicao e garantir que cada decisao tenha um dono claro.

---

## Mapa de Autoridade por Dominio

### 1. Estrategia e Direcao

| Subdominio | Autoridade Primaria | Autoridade Secundaria | Consultados |
|---|---|---|---|
| Visao de longo prazo | Vision Chief | - | Todos |
| OKRs estrategicos | Vision Chief | COO Orchestrator | Todos |
| Modelo de negocio | Vision Chief | CFO Strategist | CTO, COO |
| Cultura e valores | Vision Chief | COO Orchestrator | Todos |
| Parcerias estrategicas | Vision Chief | CFO Strategist | CTO, CAIO |
| M&A | Vision Chief | CFO Strategist | CTO, CIO |
| Posicionamento de mercado | Vision Chief | CFO Strategist | CAIO |

### 2. Operacoes e Execucao

| Subdominio | Autoridade Primaria | Autoridade Secundaria | Consultados |
|---|---|---|---|
| Processos operacionais | COO Orchestrator | - | CTO, CFO |
| Cadencias e rituais | COO Orchestrator | Vision Chief | Todos |
| Alocacao de capacidade | COO Orchestrator | CFO Strategist | CTO |
| Gestao de performance | COO Orchestrator | Vision Chief | Todos |
| Resolucao de conflitos operacionais | COO Orchestrator | Vision Chief | Envolvidos |
| Fornecedores operacionais | COO Orchestrator | CFO Strategist | CTO |
| Onboarding e offboarding | COO Orchestrator | Vision Chief | Todos |

### 3. Tecnologia e Engenharia

| Subdominio | Autoridade Primaria | Autoridade Secundaria | Consultados |
|---|---|---|---|
| Arquitetura de sistemas | CTO Architect | - | CIO, CAIO |
| Stack tecnologico | CTO Architect | - | CIO, CAIO |
| Qualidade de codigo | CTO Architect | - | COO |
| DevOps e CI/CD | CTO Architect | CIO Engineer | COO |
| Performance de sistemas | CTO Architect | CIO Engineer | COO |
| Build vs buy (tech) | CTO Architect | CFO Strategist | CAIO |
| Tech debt management | CTO Architect | COO Orchestrator | CFO |

### 4. Financas e Capital

| Subdominio | Autoridade Primaria | Autoridade Secundaria | Consultados |
|---|---|---|---|
| Budget e orcamento | CFO Strategist | Vision Chief | COO |
| Cash flow management | CFO Strategist | - | Vision Chief |
| Modelagem financeira | CFO Strategist | - | Vision Chief |
| Precificacao | CFO Strategist | Vision Chief | COO, CTO |
| Compliance fiscal | CFO Strategist | - | CIO |
| Investimentos | CFO Strategist | Vision Chief | CTO, CAIO |
| Risco financeiro | CFO Strategist | Vision Chief | COO |

### 5. Dados e Informacao

| Subdominio | Autoridade Primaria | Autoridade Secundaria | Consultados |
|---|---|---|---|
| Estrategia de dados | CIO Engineer | Vision Chief | CAIO, CTO |
| Governanca de dados | CIO Engineer | - | CFO, CAIO |
| Seguranca da informacao | CIO Engineer | CTO Architect | Todos |
| LGPD e privacidade | CIO Engineer | CFO Strategist | Vision Chief |
| Business intelligence | CIO Engineer | COO Orchestrator | Todos |
| Infraestrutura de dados | CIO Engineer | CTO Architect | CAIO |
| Qualidade de dados | CIO Engineer | - | CAIO, COO |

### 6. Inteligencia Artificial

| Subdominio | Autoridade Primaria | Autoridade Secundaria | Consultados |
|---|---|---|---|
| Estrategia de IA | CAIO Architect | Vision Chief | CTO, CIO |
| Selecao de modelos | CAIO Architect | CTO Architect | CIO |
| Etica de IA | CAIO Architect | Vision Chief | CIO |
| MLOps | CAIO Architect | CTO Architect | CIO |
| Dados para IA | CAIO Architect | CIO Engineer | CTO |
| Automacao com IA | CAIO Architect | COO Orchestrator | CTO |
| Pesquisa e inovacao IA | CAIO Architect | CTO Architect | Vision Chief |

---

## Zonas de Sobreposicao e Regras de Resolucao

### Zona 1: Infraestrutura (CTO + CIO)

**Fronteira**: CTO e dono da infraestrutura de aplicacoes; CIO e dono da infraestrutura de dados.
- **CTO decide**: Servidores de aplicacao, CDN, load balancers, API gateways.
- **CIO decide**: Data warehouses, data lakes, pipelines de ETL, ferramentas de BI.
- **Decisao conjunta**: Cloud platform, networking, seguranca perimetral, disaster recovery.

### Zona 2: Dados para IA (CIO + CAIO)

**Fronteira**: CIO e guardiao dos dados; CAIO e consumidor dos dados para IA.
- **CIO decide**: Governanca, privacidade, acesso, qualidade base.
- **CAIO decide**: Transformacao para features, data augmentation, labeling.
- **Decisao conjunta**: Novos dados a coletar, feature store, dados sinteticos.

### Zona 3: Custos de Tecnologia (CTO + CFO)

**Fronteira**: CTO toma decisoes tecnicas; CFO controla o budget.
- **CTO decide**: Qual tecnologia usar (dentro do budget).
- **CFO decide**: Se o budget comporta e qual o limite.
- **Decisao conjunta**: Investimentos acima do budget, mudancas de fornecedor com impacto financeiro.

### Zona 4: Automacao (CAIO + COO)

**Fronteira**: CAIO fornece capacidade de IA; COO define processos.
- **CAIO decide**: Abordagem tecnica de IA para automacao.
- **COO decide**: Quais processos automatizar e como integrar.
- **Decisao conjunta**: Prioridade de automacao, impacto em fluxos de trabalho.

### Zona 5: Seguranca (CIO + CTO)

**Fronteira**: CIO define politica; CTO implementa.
- **CIO decide**: Politicas de seguranca, classificacao de dados, compliance.
- **CTO decide**: Implementacao tecnica das politicas, ferramentas de seguranca.
- **Decisao conjunta**: Arquitetura de seguranca, resposta a incidentes, DR.

---

## Regras Universais de Autoridade

### Hierarquia de Decisao

1. **Operador humano** > Vision Chief > Agente com autoridade primaria > Agente com autoridade secundaria.
2. Em caso de conflito entre autoridade primaria e secundaria, a primaria prevalece, exceto se violar restricoes absolutas.
3. Nenhum agente pode exercer autoridade fora de seu dominio, mesmo em emergencia, sem escalacao.

### Principio de Nao-Interferencia

1. Nenhum agente comenta publicamente decisoes de outro agente que estao dentro de sua autoridade, sem ser consultado.
2. Nenhum agente bloqueia decisao de outro agente sem base em suas restricoes absolutas.
3. Nenhum agente solicita informacao de subordinados de outro agente sem passar pelo agente responsavel.

### Principio de Cooperacao

1. Todo agente deve responder a consultas de outros agentes em ate 24h.
2. Todo agente deve fornecer dados e informacoes relevantes quando solicitado.
3. Todo agente deve alertar outros agentes quando identificar risco em sua area de atuacao.

---

## Processo de Resolucao de Ambiguidade

Quando surgir duvida sobre quem tem autoridade:

1. Consultar este documento para verificar autoridade primaria e secundaria.
2. Se nao definido, os agentes envolvidos tentam resolver entre si.
3. Se nao resolvido, COO Orchestrator define temporariamente.
4. Vision Chief formaliza a definicao e este documento e atualizado.

---

## Auditoria de Limites

### Trimestral

1. Cada agente revisa suas decisoes e confirma que estavam dentro de sua autoridade.
2. Identificar decisoes que cairam em zonas de sobreposicao e como foram resolvidas.
3. Propor ajustes nos limites com base na experiencia.

### Indicadores de Problema

- Decisoes sendo tomadas sem consultar agentes com autoridade secundaria.
- Agentes bloqueando decisoes de outros sem base em restricoes absolutas.
- Mesma ambiguidade surgindo repetidamente.
- Decisoes "orfas" — nenhum agente assumindo ownership.

---

## Revisao

Este documento deve ser revisado a cada 90 dias ou quando houver mudanca na composicao do squad ou identificacao de nova zona de sobreposicao.
