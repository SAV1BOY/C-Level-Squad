# Workflow: Renewal ou Exit de Fornecedor

## Objetivo

Avaliar de forma estruturada a decisão de renovar, renegociar ou encerrar contratos com fornecedores, garantindo continuidade operacional, otimização de custos e transição suave quando necessário.

## Trigger

- Alerta automático: 90-120 dias antes do vencimento do contrato
- Avaliação de governança contínua indicando rating D
- Mudança estratégica que torna fornecedor desnecessário
- Alternativa significativamente melhor identificada no mercado
- Solicitação de exit pela área usuária

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Procurement | **Responsible** — Conduz análise de renovação e negociação |
| Gestor do Relacionamento | **Accountable** — Recomenda renovação ou exit |
| Jurídico | **Consulted** — Revisão de termos de saída e renovação |
| TI | **Consulted** — Plano de migração técnica se exit |
| FP&A | **Consulted** — Impacto financeiro e budget |
| VP da Área | **Informed** — Aprovação da decisão |

## Etapas do Workflow

### Etapa 1: Análise de Renovação (D-120)
- Procurement alerta gestor sobre vencimento iminente
- Consolidar dados: scorecard de governança, SLA compliance, ROI, satisfação
- Comparar custo atual com benchmarks de mercado
- Levantar alternativas disponíveis (substituição ou internalização)
- Preparar recomendação: Renovar / Renegociar / Exit
- **SLA: Análise completa até D-90**

### Etapa 2: Decisão de Renovação vs Exit
- Gestor apresenta análise para VP e stakeholders
- Critérios de decisão:
  - Performance histórica (SLA, satisfação, inovação)
  - Custo-benefício vs alternativas
  - Switching cost (custo e risco de troca)
  - Alinhamento estratégico futuro
- Decisão: Renovar (mesmo termos) / Renegociar / Exit
- **SLA: Decisão até D-75**

### Etapa 3A: Renegociação (se aplicável)
- Procurement define termos desejados para renovação
- Negociar preço, escopo, SLA e prazo do novo contrato
- Alavancas: volume, prazo maior, redução de escopo, competição
- Meta de redução: 5-15% sobre contrato vigente
- Se acordo: assinar aditivo ou novo contrato
- **SLA: Conclusão até D-30**

### Etapa 3B: Planejamento de Exit (se aplicável)
- Revisar cláusulas contratuais de término (notice period, penalidades)
- Definir plano de transição técnica com timeline
- Identificar fornecedor substituto (pode requerer novo RFP)
- Plano de migração de dados conforme DPA
- Comunicar fornecedor sobre decisão de não renovar
- **SLA: Plano de exit definido até D-60**

### Etapa 4: Execução de Exit (se aplicável)
- Migração de dados para novo fornecedor ou sistema interno
- Desativação de acessos e integrações
- Transferência de conhecimento documentada
- Confirmação de destruição de dados pelo fornecedor (certificado)
- Encerramento formal do contrato com quitação
- **SLA: Exit concluído até data de término do contrato**

### Etapa 5: Post-Mortem de Fornecedor
- Documentar razões da decisão (renovação ou exit)
- Lições aprendidas para futuras contratações
- Atualizar critérios de avaliação do processo de RFP
- Feedback compartilhado com Procurement para base de conhecimento
- **SLA: 2 semanas após conclusão**

## Outputs / Entregáveis

- Análise de renovação documentada com recomendação
- Contrato renovado ou notificação de término enviada
- Plano de transição (se exit) executado
- Certificado de destruição de dados (se exit)
- Post-mortem documentado com lições aprendidas
- Base de fornecedores atualizada

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Análises iniciadas no prazo (D-120) | 100% | Por contrato |
| Renovações renegociadas com redução de custo | ≥ 60% | Anual |
| Desconto médio em renegociação | 5-15% | Anual |
| Exits sem interrupção operacional | 100% | Por exit |
| Tempo de transição no exit | ≤ 90 dias | Por exit |

## Integração com Outros Workflows

- **04-ongoing-governance.md**: Scorecard de governança informa decisão
- **01-evaluation-rfp.md**: Exit pode acionar novo RFP
- **Budget Cycle / 05-quarterly-reforecast.md**: Mudanças de contrato impactam reforecast
- **Data Governance / 05-retention-disposal.md**: Destruição de dados do fornecedor
