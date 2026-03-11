# Workflow: Classificação de Dados

## Objetivo

Estabelecer um processo padronizado para identificar, classificar e catalogar todos os ativos de dados da organização por nível de sensibilidade, garantindo que controles adequados de proteção sejam aplicados conforme a classificação e requisitos regulatórios.

## Trigger

- Novo sistema ou banco de dados sendo implementado
- Novo tipo de dado sendo coletado ou processado
- Auditoria de compliance identificando dados não classificados
- Revisão periódica do catálogo de dados (semestral)
- Incidente de segurança envolvendo dados

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Data Owner (VP da área) | **Accountable** — Responsável pela classificação dos dados da área |
| Data Steward | **Responsible** — Executa classificação e mantém catálogo |
| DPO (Data Protection Officer) | **Consulted** — Orientação sobre LGPD e privacidade |
| Security Team | **Consulted** — Define controles por nível de classificação |
| Data Engineer | **Informed** — Implementa controles técnicos |

## Níveis de Classificação

| Nível | Descrição | Exemplos | Controles |
|-------|-----------|----------|-----------|
| **Público** | Pode ser divulgado externamente | Blog posts, dados do site público | Nenhum controle especial |
| **Interno** | Uso geral dentro da empresa | Políticas, organogramas, comunicados | Autenticação corporativa |
| **Confidencial** | Acesso restrito por necessidade | Dados financeiros, estratégias, contratos | Criptografia + ACL restrita |
| **Altamente Confidencial** | Acesso mínimo necessário | PII sensível, dados de saúde, senhas | Criptografia + MFA + audit log |

## Etapas do Workflow

### Etapa 1: Inventário de Ativos de Dados
- Mapear todos os repositórios de dados: bancos, data lakes, planilhas, drives
- Catalogar tipos de dados armazenados em cada repositório
- Identificar data owners por repositório
- Ferramenta: catálogo de dados (Collibra, Alation, DataHub)
- **SLA: 2 semanas para inventário inicial; contínuo para novos ativos**

### Etapa 2: Classificação por Tipo de Dado
- Data Steward classifica cada tipo de dado conforme níveis
- Atenção especial para dados pessoais (LGPD):
  - Dados pessoais: nome, email, telefone, CPF
  - Dados pessoais sensíveis: saúde, biometria, orientação, religião
  - Dados de menores: proteção adicional obrigatória
- Registrar classificação no catálogo de dados
- **SLA: 5 dias úteis por sistema/repositório**

### Etapa 3: Validação pelo Data Owner
- Data Owner revisa e aprova classificação
- Verificar se classificação está alinhada com uso de negócio
- Resolver discrepâncias entre classificação e controles existentes
- Assinar responsabilidade como Data Owner formal
- **SLA: 3 dias úteis**

### Etapa 4: Mapeamento de Fluxo de Dados
- Documentar como dados fluem entre sistemas
- Identificar pontos de entrada, processamento e saída
- Mapear transferências para terceiros (fornecedores, parceiros)
- Verificar se controles são mantidos em cada ponto do fluxo
- **SLA: 1 semana por fluxo crítico**

### Etapa 5: Aplicação de Controles
- Security define e aplica controles conforme classificação
- Implementar: criptografia, masking, ACLs, audit logs
- Configurar DLP (Data Loss Prevention) para dados confidenciais
- Testar eficácia dos controles implementados
- **SLA: 2 semanas para controles técnicos**

### Etapa 6: Publicação e Manutenção
- Catálogo de dados publicado e acessível
- Treinamento para colaboradores sobre política de classificação
- Revisão semestral de classificações existentes
- Processo de classificação integrado ao ciclo de vida de sistemas
- **Cadência: Revisão semestral; classificação contínua para novos dados**

## Outputs / Entregáveis

- Catálogo de dados atualizado com classificação por ativo
- Política de classificação de dados publicada
- Mapa de fluxo de dados documentado
- Controles implementados por nível de classificação
- Registro de Data Owners assinados
- Relatório de cobertura de classificação

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Ativos de dados classificados | ≥ 95% | Semestral |
| Dados pessoais com classificação correta | 100% | Trimestral |
| Data Owners designados por repositório | 100% | Contínua |
| Controles implementados conforme classificação | ≥ 90% | Trimestral |
| Tempo para classificar novo ativo | ≤ 5 dias úteis | Por ativo |

## Integração com Outros Workflows

- **02-access-control.md**: Classificação define níveis de acesso
- **04-compliance-audit.md**: Catálogo é base para auditoria
- **05-retention-disposal.md**: Classificação informa políticas de retenção
- **Hiring / 03-interview-process.md**: Dados de candidatos classificados como PII
- **Vendor Management / 03-contract-negotiation.md**: DPA baseado na classificação de dados compartilhados
