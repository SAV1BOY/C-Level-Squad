# Workflow: Governança Contínua de Fornecedores

## Objetivo

Monitorar continuamente o desempenho, compliance e valor entregue por fornecedores contratados, garantindo que SLAs sejam cumpridos, riscos sejam gerenciados e o relacionamento permaneça produtivo e alinhado às necessidades do negócio.

## Trigger

- Contrato com fornecedor assinado e implementação concluída
- Cadência periódica de review (mensal, trimestral ou semestral)
- Incidente ou falha de SLA reportada
- Mudança regulatória que impacta fornecedor

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Gestor do Relacionamento | **Responsible** — Monitora performance e conduz reviews |
| Procurement | **Accountable** — Garante compliance contratual |
| TI / Security | **Consulted** — Monitora segurança e acessos |
| Jurídico | **Consulted** — Issues contratuais e regulatórios |
| VP da Área | **Informed** — Decisões sobre continuidade |

## Etapas do Workflow

### Etapa 1: Monitoramento Contínuo de SLA
- Rastrear métricas de SLA definidas no contrato
- Dashboard automatizado com indicadores do fornecedor
- Alertas para violações de SLA
- Registrar tickets e incidentes envolvendo o fornecedor
- **Cadência: Contínua com report mensal**

### Etapa 2: Review Periódico de Performance
- Reunião de QBR (Quarterly Business Review) com fornecedor
- Agenda: performance vs SLA, roadmap, issues, oportunidades
- Coletar feedback interno dos usuários da solução
- Documentar satisfação e áreas de melhoria
- **Cadência: Trimestral para fornecedores tier 1, semestral para tier 2**

### Etapa 3: Gestão de Riscos
- Avaliar saúde financeira do fornecedor periodicamente
- Monitorar mudanças em certificações de segurança (SOC2, ISO)
- Verificar atualizações de política de privacidade e DPA
- Plano de contingência: o que fazer se fornecedor falhar ou sair do mercado
- **Cadência: Semestral ou quando há sinal de risco**

### Etapa 4: Gestão de Escalações
- Canal definido para escalar issues com o fornecedor
- Níveis: suporte padrão → account manager → executivo do fornecedor
- Documentar todas as escalações e resoluções
- SLA de resposta para escalações definido em contrato
- **Cadência: Conforme necessidade**

### Etapa 5: Avaliação de Valor (ROI)
- Medir valor entregue vs custo do contrato anualmente
- Comparar com alternativas de mercado (benchmark)
- Identificar oportunidades de otimização de uso
- Avaliar se escopo contratado está adequado (over/under-provisioned)
- **Cadência: Anual, 3 meses antes da renovação**

### Etapa 6: Scorecard do Fornecedor
- Consolidar todas as dimensões em scorecard unificado
- Dimensões: SLA compliance, satisfação interna, custo-benefício, inovação, risco
- Rating: A (excelente) / B (bom) / C (regular) / D (insatisfatório)
- Fornecedores D: plano de melhoria ou avaliação de troca
- Publicar ranking para Procurement e liderança
- **Cadência: Trimestral**

## Outputs / Entregáveis

- Dashboard de SLA por fornecedor
- Atas de QBR com ações documentadas
- Scorecard trimestral do fornecedor
- Relatório anual de valor (ROI) por fornecedor
- Registro de escalações e resoluções
- Avaliação de risco atualizada

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| SLA compliance do fornecedor | ≥ 95% | Mensal |
| QBRs realizados no prazo | 100% | Trimestral |
| Satisfação interna com fornecedor | ≥ 4.0/5.0 | Trimestral |
| ROI positivo | > 1.0 | Anual |
| Fornecedores com rating D | < 10% do portfólio | Trimestral |

## Integração com Outros Workflows

- **03-contract-negotiation.md**: Performance informa renegociações
- **05-renewal-exit.md**: Scorecard e ROI alimentam decisão de renovação
- **Incident Response / 01-detection-triage.md**: Incidentes de fornecedor na triagem
- **Data Governance / 04-compliance-audit.md**: Fornecedores no escopo de auditoria
