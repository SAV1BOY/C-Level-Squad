# Workflow: Controle de Acesso

## Objetivo

Garantir que o acesso a dados e sistemas seja concedido com base no princípio do menor privilégio, assegurando que cada colaborador tenha apenas os acessos necessários para sua função, com revisões periódicas e processos claros de concessão e revogação.

## Trigger

- Admissão de novo colaborador (provisionamento inicial)
- Mudança de cargo ou departamento (ajuste de acessos)
- Desligamento de colaborador (revogação total)
- Solicitação de acesso adicional por colaborador ou gestor
- Revisão periódica de acessos (trimestral)

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| TI / Identity & Access | **Responsible** — Provisiona e revoga acessos |
| Gestor do Colaborador | **Accountable** — Aprova acessos para sua equipe |
| Data Owner | **Consulted** — Aprova acesso a dados de sua responsabilidade |
| Security Team | **Consulted** — Define políticas e audita compliance |
| DPO | **Informed** — Visibilidade sobre acessos a dados pessoais |

## Modelo de Controle de Acesso (RBAC)

### Perfis Padrão por Nível
| Perfil | Acesso Base | Dados |
|--------|------------|-------|
| **Colaborador** | Email, Slack, intranet, ferramentas da área | Interno |
| **Gestor** | + dashboards, relatórios da área, people analytics | Interno + Confidencial da área |
| **Diretor/VP** | + dados financeiros, planejamento estratégico | Confidencial cross-funcional |
| **C-Level** | + board materials, dados sensíveis de negócio | Altamente Confidencial |

### Acessos Adicionais (Role-Based)
- Definidos por função específica, não por nível hierárquico
- Exemplos: acesso a PII para time de suporte, acesso a produção para SRE
- Requerem justificativa e aprovação do Data Owner

## Etapas do Workflow

### Etapa 1: Provisionamento (Admissão)
- RH informa admissão via sistema integrado (HRIS → IAM)
- TI provisiona automaticamente acessos do perfil base
- Gestor solicita acessos adicionais específicos da função
- Data Owners aprovam acessos a dados sensíveis
- Colaborador recebe credenciais e guia de primeiro acesso
- **SLA: Acessos base em D-1; adicionais em D+3**

### Etapa 2: Solicitação de Acesso Adicional
- Colaborador ou gestor solicita via portal de self-service
- Formulário: sistema, nível de acesso, justificativa, período (temporário ou permanente)
- Aprovação do gestor direto (obrigatória)
- Aprovação do Data Owner (para dados Confidenciais ou superior)
- Aprovação de Security (para acessos de alto risco: produção, PII massivo)
- **SLA: 24h para aprovações; 4h para provisão após aprovação**

### Etapa 3: Ajuste por Mudança de Função
- RH notifica mudança de cargo/departamento via HRIS
- TI revoga acessos do cargo anterior
- Provisiona acessos do novo cargo conforme perfil base
- Gestor anterior confirma que não há acessos pendentes
- Novo gestor solicita acessos adicionais se necessário
- **SLA: 48h após efetivação da mudança**

### Etapa 4: Revogação (Desligamento)
- RH notifica desligamento com antecedência (quando possível)
- TI revoga todos os acessos no momento do desligamento
- Checklist de revogação: email, Slack, VPN, sistemas, cloud, repositórios
- Backup de dados do colaborador conforme política de retenção
- Confirmação de revogação completa registrada
- **SLA: Revogação imediata no momento do desligamento**

### Etapa 5: Revisão Periódica de Acessos (Access Review)
- Trimestral: gestores revisam acessos de seus diretos
- Para cada acesso: Manter / Revogar / Ajustar
- Data Owners revisam quem tem acesso a dados sensíveis
- Security audita acessos privilegiados (admin, produção)
- Acessos não confirmados são revogados automaticamente após 14 dias
- **Cadência: Trimestral**

### Etapa 6: Auditoria e Compliance
- Logs de acesso mantidos por 12 meses (mínimo)
- Relatório de acessos por classificação de dados
- Verificação de segregação de funções (SoD)
- Evidências geradas para auditorias SOC2, ISO 27001
- **Cadência: Contínua; relatório mensal**

## Outputs / Entregáveis

- Registro atualizado de acessos por colaborador
- Dashboard de cobertura de access review
- Relatório de acessos privilegiados
- Logs de concessão e revogação para auditoria
- Evidências de compliance (SOC2, ISO 27001, LGPD)

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Provisionamento no prazo (admissão) | ≥ 95% | Mensal |
| Revogação no desligamento (mesmo dia) | 100% | Mensal |
| Access reviews concluídos no prazo | ≥ 90% | Trimestral |
| Acessos orphan (colaboradores desligados) | 0 | Mensal |
| Solicitações de acesso atendidas no SLA | ≥ 90% | Mensal |

## Integração com Outros Workflows

- **01-data-classification.md**: Classificação define controles de acesso
- **03-quality-monitoring.md**: Acesso controlado a dados de qualidade
- **Hiring / 05-onboarding-30-60-90.md**: Provisionamento integrado ao onboarding
- **Vendor Management / 02-poc-pilot.md**: Acessos de fornecedores controlados
