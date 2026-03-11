# Workflow: Retenção e Descarte de Dados

## Objetivo

Definir e implementar políticas de retenção de dados que atendam requisitos legais, regulatórios e de negócio, e garantir o descarte seguro de dados quando o período de retenção expira, reduzindo riscos de exposição e custos de armazenamento.

## Trigger

- Dados atingindo fim do período de retenção definido
- Nova regulamentação com requisitos de retenção específicos
- Solicitação de exclusão de titular de dados (LGPD - direito ao esquecimento)
- Encerramento de contrato com cliente ou fornecedor
- Descomissionamento de sistema ou banco de dados
- Revisão periódica de política de retenção (anual)

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| DPO | **Accountable** — Define política e garante conformidade legal |
| Data Steward | **Responsible** — Executa processos de retenção e descarte |
| Jurídico | **Consulted** — Requisitos legais de retenção |
| Data Engineer | **Responsible** — Implementa automação de descarte |
| Data Owner (VP) | **Consulted** — Valida que dados podem ser descartados |
| Security Team | **Informed** — Verifica que descarte é seguro |

## Tabela de Retenção por Tipo de Dado

| Tipo de Dado | Retenção Mínima | Retenção Máxima | Base Legal |
|-------------|-----------------|-----------------|------------|
| Dados financeiros/contábeis | 5 anos | 10 anos | Código Civil / Tributário |
| Contratos comerciais | Vigência + 5 anos | Vigência + 10 anos | Código Civil |
| Dados de empregados (CLT) | Desligamento + 5 anos | Desligamento + 30 anos (FGTS) | CLT / Previdência |
| Dados de candidatos (recrutamento) | 6 meses | 2 anos | LGPD - consentimento |
| Dados de clientes (transacionais) | Vigência + 5 anos | Vigência + 10 anos | LGPD + Código Civil |
| Logs de sistema | 90 dias | 12 meses | SOC2 / Política interna |
| Dados de analytics (anonimizados) | Indefinido | Indefinido | N/A (anonimizado) |
| Dados pessoais sensíveis (saúde) | Conforme finalidade | Finalidade + 5 anos | LGPD Art. 11 |

## Etapas do Workflow

### Etapa 1: Definição da Política de Retenção
- DPO e Jurídico definem períodos de retenção por tipo de dado
- Considerar: requisitos legais, regulatórios, contratuais e de negócio
- Documentar base legal para cada período de retenção
- Política aprovada pelo C-Level e publicada internamente
- Revisão anual da política (ou quando há mudança regulatória)
- **SLA: Política definida antes da implementação de qualquer sistema**

### Etapa 2: Implementação de Controles de Retenção
- Data Engineer implementa labels/tags de retenção nos repositórios
- Configurar lifecycle policies em cloud storage (S3, GCS, Azure Blob)
- Implementar soft delete antes de hard delete (período de graça de 30 dias)
- Configurar automação para identificar dados que atingiram fim de retenção
- Alertas automáticos para Data Stewards sobre dados a vencer
- **SLA: 2 semanas por sistema**

### Etapa 3: Processo de Descarte Regular
- Sistema identifica automaticamente dados no fim do período de retenção
- Data Steward revisa lista de dados para descarte
- Data Owner confirma que não há retenção legal (litigation hold)
- Execução do descarte conforme método apropriado:
  - Dados digitais: deleção segura com certificado
  - Dados em backup: remoção do backup ou criptografia da chave
  - Dados físicos: destruição certificada
- **Cadência: Mensal para dados digitais; trimestral para revisão geral**

### Etapa 4: Atendimento a Solicitações de Exclusão (LGPD)
- Titular solicita exclusão de dados pessoais
- DPO avalia: há base legal para manter os dados?
- Se não há base legal: proceder com exclusão em todos os sistemas
- Se há base legal (ex: obrigação legal): informar titular e documentar razão
- Confirmar exclusão ao titular dentro do prazo legal (15 dias)
- Documentar solicitação e resultado no registro de atendimento
- **SLA: 15 dias conforme LGPD**

### Etapa 5: Descarte em Descomissionamento de Sistemas
- Inventariar todos os dados no sistema a ser descomissionado
- Classificar: migrar, arquivar ou descartar
- Dados a migrar: transferir para sistema substituto com integridade
- Dados a arquivar: mover para cold storage com controles de acesso
- Dados a descartar: deleção segura com certificado
- Verificação final: sistema completamente limpo antes de desligar
- **SLA: Conforme timeline de descomissionamento**

### Etapa 6: Auditoria e Compliance
- Manter registro de todos os descartes realizados (quê, quando, como, por quem)
- Certificados de destruição arquivados por 5 anos
- Relatório anual de retenção e descarte para DPO
- Evidências disponíveis para auditorias de compliance
- **Cadência: Contínuo; relatório anual**

## Outputs / Entregáveis

- Política de retenção de dados publicada e aprovada
- Tabela de retenção por tipo de dado documentada
- Automação de lifecycle policies implementada
- Registros de descarte com certificados
- Relatório de atendimento a solicitações de exclusão
- Dashboard de dados por estágio de retenção

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Dados descartados conforme política | ≥ 95% | Mensal |
| Solicitações de exclusão atendidas no prazo (15 dias) | 100% | Mensal |
| Cobertura de lifecycle policies | ≥ 90% dos repositórios | Trimestral |
| Redução de custo de armazenamento | Tendência decrescente | Trimestral |
| Dados retidos além do necessário | < 5% | Semestral |
| Certificados de descarte arquivados | 100% | Contínuo |

## Integração com Outros Workflows

- **01-data-classification.md**: Classificação informa política de retenção
- **02-access-control.md**: Acessos revogados com descarte do dado
- **04-compliance-audit.md**: Registros de descarte são evidência de auditoria
- **Vendor Management / 05-renewal-exit.md**: Descarte de dados ao encerrar com fornecedor
- **Hiring / 02-sourcing-pipeline.md**: Dados de candidatos com retenção limitada
