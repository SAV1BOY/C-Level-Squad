# Workflow: Auditoria de Compliance

## Objetivo

Conduzir auditorias regulares para verificar conformidade com regulamentações (LGPD, SOC2, ISO 27001, PCI-DSS), políticas internas de dados e requisitos contratuais, identificando gaps e gerando planos de remediação antes que se tornem riscos.

## Trigger

- Calendário anual de auditorias (cadência fixa)
- Auditoria externa agendada (SOC2, ISO, reguladores)
- Incidente de segurança ou vazamento de dados
- Nova regulamentação ou mudança significativa de lei
- Novo contrato com cláusulas de compliance específicas
- Solicitação do board ou investidores

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| DPO / Compliance Officer | **Accountable** — Coordena auditorias e garante conformidade |
| Internal Audit | **Responsible** — Executa auditorias internas |
| Security Team | **Responsible** — Evidências técnicas e controles |
| Data Stewards | **Consulted** — Evidências de governança de dados |
| Jurídico | **Consulted** — Interpretação regulatória |
| C-Level / Board | **Informed** — Resultados e riscos |

## Frameworks de Compliance

| Framework | Escopo | Cadência |
|-----------|--------|----------|
| **LGPD** | Dados pessoais de titulares brasileiros | Contínuo + auditoria anual |
| **SOC2 Type II** | Controles de segurança, disponibilidade, confidencialidade | Anual |
| **ISO 27001** | Sistema de gestão de segurança da informação | Anual + surveillance |
| **PCI-DSS** | Dados de cartão de pagamento | Anual ou trimestral |
| **HIPAA** | Dados de saúde (se aplicável) | Anual |

## Etapas do Workflow

### Etapa 1: Planejamento da Auditoria
- Definir escopo: frameworks, sistemas, processos e período
- Agendar com auditores (internos ou externos)
- Identificar responsáveis por cada controle a ser auditado
- Preparar checklist de evidências necessárias
- Comunicar áreas envolvidas sobre timeline e expectativas
- **SLA: 4 semanas antes da auditoria**

### Etapa 2: Coleta de Evidências
- Cada responsável coleta evidências para seus controles
- Tipos de evidência: logs, screenshots, políticas, atas, configurações
- Evidências organizadas em repositório centralizado e seguro
- Pre-review: DPO/Compliance verifica completude antes da auditoria
- Gap analysis: identificar controles sem evidência adequada
- **SLA: 2 semanas antes da auditoria**

### Etapa 3: Execução da Auditoria
- Auditores revisam evidências e entrevistam responsáveis
- Testes de controle: verificar se funcionam como documentado
- Documentar findings: conformidades, não-conformidades, observações
- Classificar findings por severidade: Crítico, Alto, Médio, Baixo
- **SLA: 1-4 semanas dependendo do escopo**

### Etapa 4: Relatório de Auditoria
- Auditor emite relatório com findings detalhados
- Para cada finding: descrição, evidência, risco, recomendação
- Opinião geral: Conforme / Conforme com ressalvas / Não conforme
- DPO revisa relatório e discute com auditor se necessário
- Relatório apresentado ao C-Level e board
- **SLA: 2 semanas após conclusão da auditoria**

### Etapa 5: Plano de Remediação
- Para cada finding não-conforme, definir:
  - Ação corretiva específica
  - Responsável pela implementação
  - Prazo de conclusão
  - Prioridade (baseada na severidade)
- Plano aprovado pelo DPO e sponsor executivo
- Findings críticos: prazo máximo de 30 dias
- Findings altos: prazo máximo de 90 dias
- **SLA: 2 semanas após recebimento do relatório**

### Etapa 6: Acompanhamento e Re-teste
- Monitorar progresso das remediações mensalmente
- Re-teste de controles após remediação (pelo auditor ou compliance)
- Atualizar status de findings no tracker
- Report mensal de progresso para DPO e liderança
- Findings não resolvidos no prazo: escalação automática
- **SLA: Conforme prazos definidos no plano**

## Outputs / Entregáveis

- Relatório de auditoria com findings classificados
- Plano de remediação com ações, donos e prazos
- Evidências organizadas e arquivadas
- Certificações renovadas (SOC2, ISO) quando aplicável
- Relatório de ROPA (Record of Processing Activities) para LGPD
- Dashboard de compliance com status de findings

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Auditorias realizadas conforme calendário | 100% | Anual |
| Findings críticos resolvidos em 30 dias | 100% | Mensal |
| Findings totais remediados no prazo | ≥ 90% | Trimestral |
| Certificações mantidas sem interrupção | 100% | Anual |
| Quantidade de findings por auditoria | Tendência decrescente | Anual |

## Integração com Outros Workflows

- **01-data-classification.md**: Catálogo de dados é base para ROPA
- **02-access-control.md**: Controles de acesso auditados
- **03-quality-monitoring.md**: Quality reports como evidência
- **05-retention-disposal.md**: Políticas de retenção auditadas
- **Vendor Management / 04-ongoing-governance.md**: Compliance de fornecedores auditado
