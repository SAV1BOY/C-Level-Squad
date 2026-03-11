# Workflow: Negociação de Contrato

## Objetivo

Conduzir a negociação contratual com fornecedores selecionados de forma estruturada, protegendo os interesses da empresa em termos comerciais, jurídicos e de SLA, enquanto mantém um relacionamento construtivo com o fornecedor.

## Trigger

- POC aprovada com recomendação de Go
- Renovação de contrato existente com necessidade de renegociação
- Upgrade ou downgrade de serviço com fornecedor atual

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Procurement | **Responsible** — Conduz negociação comercial |
| Jurídico | **Responsible** — Revisão e negociação de termos legais |
| Gestor Solicitante | **Accountable** — Valida escopo e SLAs técnicos |
| TI / Security | **Consulted** — Requisitos de segurança e DPA |
| CFO / FP&A | **Consulted** — Aprovação de valor acima de threshold |
| VP da Área | **Informed** — Aprovação final |

## Etapas do Workflow

### Etapa 1: Definição de Termos Desejados
- Procurement define posição de negociação: ideal, aceitável, walk-away
- Termos-chave: preço, prazo, SLA, penalidades, saída, DPA
- Gestor define SLAs técnicos obrigatórios (uptime, response time, suporte)
- Jurídico define cláusulas obrigatórias (responsabilidade, propriedade intelectual, LGPD)
- Security define requisitos de proteção de dados (DPA, certificações)
- **SLA: 5 dias úteis**

### Etapa 2: Recebimento e Análise da Proposta Comercial
- Fornecedor envia proposta comercial e contrato padrão
- Procurement analisa pricing: valor total, modelo de cobrança, reajustes
- Jurídico analisa termos legais e identifica pontos de risco
- Comparar com benchmarks de mercado e contratos similares
- Documentar todos os pontos de negociação
- **SLA: 5 dias úteis**

### Etapa 3: Rodadas de Negociação
- Procurement conduz negociação comercial (preço, escopo, prazo)
- Jurídico negocia termos legais em paralelo (redline do contrato)
- Máximo de 3 rodadas de negociação recomendado
- Cada rodada: contraproposta documentada com justificativa
- Escalar pontos de impasse para VP ou CFO se necessário
- **SLA: 2-4 semanas para conclusão**

### Etapa 4: Validação de Segurança e Compliance
- Security review do fornecedor: SOC2, ISO 27001, penetration tests
- DPA (Data Processing Agreement) negociado conforme LGPD
- Avaliação de risco de terceiro: financeiro, operacional, reputacional
- Questionário de segurança preenchido pelo fornecedor
- **SLA: Paralelo às rodadas de negociação**

### Etapa 5: Aprovação Interna
- Procurement consolida termos finais negociados
- Aprovação conforme alçada:
  - Até R$ 50K/ano: Gestor + Procurement
  - R$ 50K-500K/ano: VP + Procurement
  - Acima R$ 500K/ano: CFO + VP + Procurement
  - Acima R$ 2M/ano: CEO + Board (se necessário)
- **SLA: 3 dias úteis**

### Etapa 6: Assinatura e Onboarding do Fornecedor
- Contrato assinado digitalmente por ambas as partes
- Registrar contrato no sistema de gestão de contratos
- Configurar alertas de vencimento e marcos de revisão
- Kick-off de implementação agendado
- Comunicar internamente a contratação
- **SLA: 5 dias úteis para formalização**

## Outputs / Entregáveis

- Contrato assinado com todos os anexos (SLA, DPA, escopo)
- Registro no sistema de gestão de contratos
- Avaliação de risco do fornecedor documentada
- Plano de implementação acordado
- Alertas de vencimento e revisão configurados

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Negociações concluídas no prazo | ≥ 80% | Trimestral |
| Desconto médio obtido vs proposta inicial | ≥ 10% | Por contrato |
| SLA contratual atendido pelo fornecedor | ≥ 95% | Trimestral |
| Contratos com DPA conforme LGPD | 100% | Contínuo |
| Tempo médio de negociação | ≤ 6 semanas | Trimestral |

## Integração com Outros Workflows

- **02-poc-pilot.md**: POC aprovada inicia negociação
- **04-ongoing-governance.md**: Contrato assinado inicia governança contínua
- **Budget Cycle / 03-review-negotiation.md**: Contratos grandes revisados no budget
- **Data Governance / 04-compliance-audit.md**: Fornecedor incluído no escopo de auditoria
