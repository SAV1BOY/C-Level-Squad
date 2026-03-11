# Discovery de Migracao de Plataforma

## Objetivo

Conduzir um processo completo de descoberta para migracao de plataforma, mapeando
todos os sistemas, dependencias, riscos e requisitos necessarios para fundamentar
o planejamento da migracao com seguranca e previsibilidade.

## Escopo do Discovery

### 1. Inventario da Plataforma Atual

#### 1.1 Mapeamento de Sistemas

- Catalogar todos os sistemas em producao com versao, responsavel e criticidade
- Documentar integracoes entre sistemas (APIs REST/GraphQL, filas, bancos compartilhados)
- Mapear fluxos de dados criticos entre componentes e sistemas externos
- Identificar sistemas legados sem documentacao ou sem manutencao ativa
- Catalogar bibliotecas e dependencias externas com licenciamento e versoes
- Registrar jobs agendados, crons, processos batch e suas dependencias
- Mapear servicos de terceiros (SaaS) com contratos e datas de renovacao

#### 1.2 Infraestrutura Atual

- Documentar servidores fisicos e virtuais, clusters e configuracoes de rede
- Mapear uso de cloud por provedor (regioes, servicos, custos mensais por servico)
- Identificar certificados SSL/TLS, dominios e configuracoes de DNS
- Documentar politicas de backup, frequencia e tempo de retencao
- Mapear disaster recovery existente (RTO e RPO atuais vs desejados)
- Catalogar ferramentas de monitoramento e observabilidade em uso
- Registrar custos de infraestrutura por componente e tendencia de crescimento

#### 1.3 Dados e Armazenamento

- Catalogar todos os bancos de dados com tamanho, crescimento mensal e tecnologia
- Identificar dados sensiveis (PII, financeiros, saude) e suas localizacoes
- Mapear pipelines de ETL/ELT e transformacao de dados existentes
- Documentar politicas de retencao, arquivamento e expurgo
- Avaliar qualidade dos dados (completude, acuracia, consistencia, unicidade)
- Mapear data lakes, data warehouses e ferramentas de BI em uso
- Estimar volume total de dados a migrar e taxa de crescimento

### 2. Mapeamento de Stakeholders

#### 2.1 Identificacao

| Grupo | Exemplos | Nivel de Envolvimento |
|-------|---------|----------------------|
| Sponsors executivos | CTO, CEO, CFO | Decisao e aprovacao |
| Lideres tecnicos | Tech Leads, Arquitetos | Decisoes tecnicas |
| Equipes de operacao | SRE, DevOps, Suporte | Execucao e operacao |
| Usuarios internos | Product, Vendas, CS | Validacao funcional |
| Usuarios externos | Clientes, Parceiros | Comunicacao e testes |
| Fornecedores | Cloud providers, SaaS | Suporte tecnico |

#### 2.2 Entrevistas Estruturadas

- Roteiro especifico por perfil de stakeholder (executivo, tecnico, negocio)
- Sessoes de 45-60 minutos por grupo com documentacao padronizada
- Coleta de pain points da plataforma atual com priorizacao
- Requisitos nao-funcionais: performance, disponibilidade, escalabilidade
- Expectativas de timeline, budget e niveis de servico pos-migracao
- Identificacao de riscos percebidos por cada grupo

#### 2.3 Consolidacao de Inputs

- Matriz de requisitos priorizados por impacto e frequencia
- Identificacao de conflitos entre expectativas de grupos diferentes
- Documentacao de premissas e restricoes levantadas
- Validacao cruzada de entendimento com cada grupo antes de prosseguir

### 3. Analise Tecnica Profunda

#### 3.1 Assessment de Codigo

- Analise estatica de codigo em todos os repositorios (SonarQube, CodeClimate)
- Medicao de cobertura de testes existente por servico
- Identificacao de divida tecnica critica que bloquearia migracao
- Avaliacao de portabilidade do codigo para nova plataforma
- Documentacao de padroes de arquitetura em uso (monolito, microservicos, serverless)
- Analise de complexidade ciclomatica e pontos de acoplamento
- Identificacao de codigo morto e funcionalidades sem uso

#### 3.2 Assessment de Performance

- Coleta de metricas baseline (latencia P50/P95/P99, throughput, error rate)
- Identificacao de gargalos conhecidos e workarounds existentes
- Documentacao de SLAs atuais e historico de compliance
- Mapeamento de picos de uso e sazonalidade ao longo do ano
- Estimativa de requisitos de capacidade na nova plataforma
- Testes de carga na plataforma atual para estabelecer limites

#### 3.3 Assessment de Seguranca

- Revisao de politicas de autenticacao e autorizacao (RBAC, OAuth, SSO)
- Mapeamento de certificacoes e compliance (SOC2, LGPD, PCI-DSS, ISO 27001)
- Identificacao de vulnerabilidades conhecidas na plataforma atual
- Documentacao de processos de gestao de secrets e credenciais
- Requisitos de seguranca para a nova plataforma
- Revisao de politicas de acesso e segregacao de ambientes

### 4. Analise de Riscos do Discovery

#### 4.1 Riscos Tecnicos

| Risco | Probabilidade | Impacto | Mitigacao |
|-------|-------------|---------|----------|
| Dependencias de tecnologias obsoletas | Alta | Alto | Inventario completo, POC de alternativas |
| Integracoes nao documentadas | Media | Alto | Entrevistas tecnicas, analise de trafego |
| Dados corrompidos entre sistemas | Media | Alto | Auditoria de dados, scripts de validacao |
| Falta de ambientes de teste | Alta | Medio | Provisionar ambientes antes da migracao |
| Performance degradada na nova plataforma | Media | Alto | Benchmarks e POCs antes do cutover |

#### 4.2 Riscos Organizacionais

| Risco | Probabilidade | Impacto | Mitigacao |
|-------|-------------|---------|----------|
| Resistencia a mudanca | Media | Medio | Comunicacao frequente, envolvimento early |
| Perda de conhecimento tribal | Alta | Alto | Documentacao e pair programming |
| Conflito de prioridades com roadmap | Alta | Medio | Alinhamento com product e lideranca |
| Budget insuficiente | Media | Alto | Business case robusto, contingencia 25% |
| Turnover de pessoas-chave durante migracao | Media | Alto | Retencao e cross-training |

#### 4.3 Riscos de Negocio

| Risco | Probabilidade | Impacto | Mitigacao |
|-------|-------------|---------|----------|
| Downtime afetando receita | Baixa | Critico | Migracao incremental, rollback plan |
| Perda de funcionalidades na transicao | Media | Alto | Testes de regressao completos |
| Impacto em clientes e parceiros | Media | Medio | Comunicacao proativa, beta testing |
| Requisitos regulatorios nao mapeados | Baixa | Alto | Revisao juridica e compliance |

### 5. Entregaveis do Discovery

#### 5.1 Documentacao Obrigatoria

- [ ] Diagrama de arquitetura atual (as-is) detalhado
- [ ] Catalogo completo de sistemas, servicos e integracoes
- [ ] Matriz RACI de stakeholders e responsabilidades
- [ ] Inventario de dados com classificacao de sensibilidade
- [ ] Relatorio de assessment tecnico (codigo, performance, seguranca)
- [ ] Registro de riscos com severidade, owners e mitigacoes
- [ ] Estimativa preliminar de esforco, custo e timeline
- [ ] Business case com ROI projetado

#### 5.2 Criterios de Saida do Discovery

- Todos os sistemas em escopo mapeados e documentados
- Stakeholders entrevistados e requisitos consolidados
- Riscos identificados com owners atribuidos
- Business case preliminar aprovado pelo sponsor
- Equipe tecnica validou viabilidade da migracao
- Decisao de go/no-go documentada e comunicada

### 6. Cronograma do Discovery

| Fase | Duracao | Atividades Principais |
|------|---------|----------------------|
| Kickoff | 1 semana | Alinhamento, formacao de equipe, planejamento |
| Inventario | 2-3 semanas | Mapeamento tecnico, dados e infraestrutura |
| Entrevistas | 2 semanas | Stakeholder interviews e consolidacao |
| Assessment | 2-3 semanas | Analise tecnica, seguranca, performance |
| Consolidacao | 1-2 semanas | Documentacao, riscos, business case |
| Decisao | 1 semana | Apresentacao e decisao go/no-go |

**Total estimado: 9-12 semanas dependendo do tamanho da plataforma**

### 7. Ferramentas Recomendadas

| Categoria | Ferramenta | Uso |
|-----------|-----------|-----|
| Diagramas | Miro, Lucidchart | Arquitetura as-is e to-be |
| Analise de codigo | SonarQube, CodeClimate | Qualidade e divida tecnica |
| Inventario | ServiceNow, Backstage | Catalogo de servicos |
| Documentacao | Confluence, Notion | Registro centralizado |
| Gestao de riscos | Planilha/Jira | Registro e tracking |

## Proximo Passo

Apos conclusao do discovery, os resultados alimentam diretamente o documento
`02-planning.md` para planejamento detalhado da migracao.
