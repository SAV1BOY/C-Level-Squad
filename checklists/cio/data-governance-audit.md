# Data Governance Audit

## Propósito
Avaliar a maturidade da governança de dados da organização: definições padronizadas, owners designados, compliance com LGPD, controle de acesso implementado e lineage rastreável. Dados sem governança são um risco — decisões baseadas em dados ruins são piores que decisões baseadas em intuição.

## Quando Aplicar
- Trimestralmente como revisão de data governance
- Quando decisões de negócio estiverem sendo questionadas por problemas de dados
- Quando requisitos regulatórios mudarem (LGPD enforcement, novas regulações)
- Após incidentes de data breach ou exposição de dados sensíveis
- Quando novos data sources ou integrações forem adicionados

## Agente Responsável
**Agente CIO (Chief Information Officer Agent)** — responsável por estabelecer e manter os padrões de governança de dados da organização.

## Checklist

### Seção 1: Data Definitions e Data Catalog
- [ ] Data catalog existe e está acessível a quem precisa de dados
- [ ] Termos de negócio (business glossary) estão definidos e padronizados
- [ ] Definição de cada métrica-chave é única e não ambígua
- [ ] Não há "múltiplas versões da verdade" para a mesma métrica
- [ ] Data dictionary cobre todos os datasets principais
- [ ] Schemas e data models estão documentados e atualizados
- [ ] Metadados (origem, frequência, qualidade) estão registrados por dataset
- [ ] O catálogo é mantido atualizado com processo definido

### Seção 2: Data Ownership e Stewardship
- [ ] Cada dataset tem um data owner designado (accountability)
- [ ] Cada domínio de dados tem um data steward responsável pela qualidade
- [ ] Roles e responsabilidades de data owners e stewards estão documentados
- [ ] Data owners têm autoridade para definir políticas de acesso
- [ ] Data stewards monitoram qualidade e resolvem issues proativamente
- [ ] Existe um data governance council ou fórum equivalente
- [ ] Disputas sobre dados são escaladas e resolvidas com processo definido
- [ ] Treinamento em data governance é fornecido aos owners e stewards

### Seção 3: Compliance e LGPD
- [ ] Dados pessoais (PII) estão mapeados em todos os sistemas
- [ ] Base legal para processamento de cada tipo de dado pessoal está documentada
- [ ] Consentimento é coletado e gerido conforme LGPD
- [ ] Direitos do titular (acesso, correção, exclusão, portabilidade) são atendidos
- [ ] Data Processing Impact Assessment (DPIA) foi realizado para processos de risco
- [ ] DPO (Data Protection Officer) ou equivalente está designado
- [ ] Contratos com terceiros incluem cláusulas de proteção de dados
- [ ] Incidentes de dados têm processo de notificação conforme LGPD
- [ ] Retenção de dados segue política definida e é enforced
- [ ] Treinamento de LGPD é realizado anualmente para todo o time

### Seção 4: Controle de Acesso
- [ ] Acesso a dados segue princípio de least privilege
- [ ] Access policies estão definidas por dataset e role
- [ ] Access reviews são realizadas pelo menos trimestralmente
- [ ] Acesso a dados sensíveis requer aprovação do data owner
- [ ] Logs de acesso a dados sensíveis são mantidos e auditáveis
- [ ] Contas de ex-colaboradores são revogadas em até 24 horas
- [ ] Acesso de terceiros é controlado e limitado no tempo
- [ ] Self-service de dados é permitido para dados não sensíveis

### Seção 5: Data Lineage e Qualidade
- [ ] Data lineage está documentado para métricas críticas (de onde vem cada dado)
- [ ] Transformações de dados são documentadas e versionadas
- [ ] Data quality rules estão definidas e monitoradas automaticamente
- [ ] Anomalias de dados geram alertas e são investigadas
- [ ] Data quality score é calculado e rastreado para datasets críticos
- [ ] Problemas de qualidade de dados têm root cause analysis e correção
- [ ] Pipeline de dados tem testes automatizados (data tests)
- [ ] O impacto de dados de má qualidade no negócio é quantificado

## Critérios de Aprovação
- Data catalog ativo e cobrindo pelo menos 80% dos datasets principais
- 100% dos datasets críticos com data owner designado
- LGPD compliance verificada e documentada para todos os processos com PII
- Access policies definidas e enforced para dados sensíveis
- Data lineage documentado para métricas de decisão do C-Level
- Pelo menos 85% dos itens de todas as seções concluídos

## O que Fazer se Falhar
1. Priorizar: LGPD compliance primeiro (risco regulatório), qualidade depois
2. Se data owners não existem: designar para os top 10 datasets mais críticos
3. Se PII não está mapeado: realizar data discovery focado em dados pessoais
4. Se access control é fraco: implementar least privilege para dados sensíveis primeiro
5. Se não há data catalog: começar com os 20 datasets mais usados
6. Engajar consultoria jurídica para validar compliance com LGPD
7. Criar plano de 90 dias para atingir baseline de data governance
8. Re-auditar em 45 dias com foco nos itens de maior risco regulatório

## Referências
- LGPD (Lei Geral de Proteção de Dados) — texto completo e guidelines
- DAMA-DMBOK2 (Data Management Body of Knowledge)
- Data Catalog e Business Glossary (internal wiki)
- Data Governance Policy (internal)
- GDPR guidelines (referência complementar à LGPD)
- "Data Governance: How to Design, Deploy, and Sustain" — John Ladley
- ANPD (Autoridade Nacional de Proteção de Dados) guidelines
