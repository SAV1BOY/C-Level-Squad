# Migração de Sistema — Fase 01: Auditoria do Sistema Atual

## Objetivo desta Fase

Realizar uma auditoria completa e detalhada do sistema atual para compreender todas as
funcionalidades, integrações, dados, customizações e dependências que terão de ser
migradas. A auditoria é o mapa que guia toda a migração — funcionalidades não mapeadas
são funcionalidades que serão perdidas. Esta fase previne o cenário mais comum de falha
em migrações: descobrir dependências críticas demasiado tarde no processo.

## Agentes Envolvidos

- **CTO Agent**: Lidera a auditoria técnica e documenta a arquitetura completa
- **COO Agent**: Documenta todos os processos de negócio que dependem do sistema
- **CFO Agent**: Audita integrações financeiras e processos de billing/reporting
- **CMO Agent**: Identifica todas as funcionalidades de front-end e customer-facing
- **CHRO Agent**: Mapeia utilizadores, permissões e processos de RH no sistema
- **Chief of Staff Agent**: Coordena a auditoria e garante completude

## Inputs Necessários

1. Migration Brief aprovado (output da Fase 00)
2. Documentação técnica existente do sistema (se disponível)
3. Acesso completo ao sistema atual (admin level)
4. Lista de todos os utilizadores e seus papéis
5. Contratos de integrações com sistemas terceiros
6. Logs de utilização do sistema (últimos 6-12 meses)
7. Histórico de incidentes e problemas conhecidos

## Processo (step-by-step)

1. **Technical architecture mapping**: CTO Agent mapeia toda a arquitetura técnica:
   servidores, bases de dados, APIs, microservices, dependências de infraestrutura
2. **Integration inventory**: CTO Agent inventaria todas as integrações com sistemas
   externos, documentando protocolos, data flows e frequências de sincronização
3. **Data audit**: CTO Agent audita todas as bases de dados, incluindo volumes, schemas,
   qualidade de dados, dados órfãos e regras de negócio embebidas em data
4. **Functionality mapping**: COO Agent mapeia todas as funcionalidades usadas por
   cada grupo de utilizadores, classificando por criticidade (must-have vs nice-to-have)
5. **Customization inventory**: CTO Agent documenta todas as customizações, scripts,
   workflows automatizados e configurações específicas do sistema
6. **Business process mapping**: COO Agent documenta todos os processos de negócio que
   dependem do sistema, identificando inputs, outputs e handoffs
7. **User and access audit**: CHRO Agent audita todos os utilizadores, papéis, permissões
   e políticas de acesso que terão de ser recriadas no novo sistema
8. **Hidden dependency discovery**: CTO Agent procura dependências escondidas como
   scheduled jobs, email triggers, file exports automáticos e scripts de backup
9. **Audit report compilation**: Chief of Staff Agent consolida todos os findings num
   relatório de auditoria abrangente com inventário completo
10. **Gap identification**: CTO Agent identifica funcionalidades do sistema atual que
    podem não existir no sistema alvo, criando um gap register

## Outputs / Entregáveis

- **Technical Architecture Map**: Diagrama completo da arquitetura atual
- **Integration Inventory**: Inventário de todas as integrações com detalhes
- **Data Audit Report**: Relatório de auditoria de dados (volume, qualidade, schemas)
- **Functionality Matrix**: Matriz de funcionalidades por grupo de utilizadores
- **Customization Inventory**: Lista de todas as customizações documentadas
- **Business Process Map**: Documentação de processos de negócio dependentes
- **Gap Register**: Registo de gaps entre sistema atual e sistema alvo
- **Complete Audit Report**: Relatório consolidado da auditoria

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-01.1 | Todas as integrações mapeadas com owner e SLA documentado | CTO Agent |
| QG-01.2 | Volume de dados quantificado e estratégia de migração definida | CTO Agent |
| QG-01.3 | Funcionalidades classificadas por criticidade com input dos users | COO Agent |
| QG-01.4 | Customizações documentadas com business justification | CTO Agent |
| QG-01.5 | Processos de negócio mapeados com dependências do sistema | COO Agent |
| QG-01.6 | Gap register completo com classificação de impacto | Chief of Staff |

## Critérios para Avançar

Para progredir para a Fase 02 (Vendor Selection), todos os critérios devem ser satisfeitos:

- [ ] Auditoria técnica completa e validada pelo CTO Agent
- [ ] Todas as integrações inventariadas e priorizadas
- [ ] Dados auditados com plano de migração de dados preliminar
- [ ] Gap register completo e priorizado
- [ ] Business processes documentados e validados pelos owners
- [ ] Relatório de auditoria distribuído a todos os agentes

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Integrações não documentadas que são descobertas tarde | Alta | Crítico | Análise de logs de rede e API calls para descobrir |
| Dados corrompidos ou inconsistentes no sistema atual | Média | Alto | Data profiling automatizado antes da migração |
| Customizações não documentadas por developer que saiu | Alta | Alto | Code review e análise de changelog completo |
| Subestimar o volume de dados a migrar | Média | Médio | Medição precisa de volumes com crescimento projetado |
| Processos de negócio que ninguém sabe que existem | Média | Alto | Entrevistas com super-users e análise de scheduled jobs |

## Templates a Usar

- `templates/system-audit-report.md` — Relatório de auditoria de sistema
- `templates/integration-inventory.md` — Inventário de integrações
- `templates/data-audit.md` — Template de auditoria de dados
- `templates/gap-register.md` — Registo de gaps funcional

## Duração Estimada

- **Mínimo**: 5 dias úteis (para sistemas simples com documentação existente)
- **Típico**: 10-15 dias úteis
- **Máximo**: 20 dias úteis (para sistemas legacy complexos sem documentação)

> **Nota**: A tentação de "acelerar" a auditoria para chegar mais rápido à migração é
> a causa número um de migrações falhadas. Cada hora investida em auditoria evita dias
> de problemas durante a execução.
