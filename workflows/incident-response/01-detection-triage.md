# Workflow: Detecção e Triagem de Incidentes

## Objetivo

Estabelecer um processo padronizado para detecção rápida, classificação e triagem inicial de incidentes, garantindo que cada ocorrência seja identificada, categorizada por severidade e direcionada ao time correto no menor tempo possível.

## Trigger

- Alerta automático de monitoramento (Datadog, PagerDuty, CloudWatch)
- Reporte de cliente via suporte (ticket, chat, telefone)
- Identificação manual por engenheiro durante operação
- Alerta de segurança (SIEM, WAF, IDS)
- Degradação detectada em health checks ou SLOs

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Engenheiro de Plantão (On-call) | **Responsible** — Primeira resposta e triagem |
| SRE Lead / Incident Commander | **Accountable** — Classificação e decisão de escalação |
| Time de Engenharia do Serviço | **Consulted** — Contexto técnico do componente |
| Customer Support | **Consulted** — Impacto em clientes reportado |
| VP de Engenharia | **Informed** — Para incidentes P1/P2 |
| CTO | **Informed** — Para incidentes P1 |

## Classificação de Severidade

| Severidade | Descrição | Impacto | Tempo de Resposta |
|-----------|-----------|---------|-------------------|
| **P1 - Crítico** | Sistema principal indisponível, perda de dados, brecha de segurança | Todos os clientes afetados | ≤ 15 minutos |
| **P2 - Alto** | Funcionalidade core degradada, impacto significativo em receita | Maioria dos clientes | ≤ 30 minutos |
| **P3 - Médio** | Funcionalidade secundária comprometida, workaround disponível | Grupo de clientes | ≤ 2 horas |
| **P4 - Baixo** | Issue cosmético, impacto mínimo, não afeta operação | Poucos clientes | ≤ 8 horas |

## Etapas do Workflow

### Etapa 1: Detecção
- Alerta recebido via canal de monitoramento configurado
- Sistema cria incidente automaticamente no Incident Management Tool
- Engenheiro de plantão é acionado via PagerDuty/Opsgenie
- Timer de SLA de resposta inicia automaticamente
- **SLA: Acknowledge do alerta em ≤ 5 minutos**

### Etapa 2: Avaliação Inicial
- On-call verifica dashboards e logs para entender escopo
- Perguntas-chave de triagem:
  - Qual serviço/componente está afetado?
  - Qual o impacto para o usuário final?
  - Quantos clientes estão afetados?
  - Existe perda de dados ou risco de segurança?
  - Há workaround disponível?
- **SLA: 10 minutos para avaliação inicial**

### Etapa 3: Classificação de Severidade
- Aplicar matriz de severidade baseada no impacto verificado
- Documentar razões da classificação no canal de incidente
- Ajustar severidade conforme novas informações surjam
- **Regra: Na dúvida, classificar com severidade MAIOR e ajustar depois**

### Etapa 4: Ações Imediatas de Contenção
- Verificar se há runbook disponível para o tipo de incidente
- Executar procedimentos de contenção documentados
- Se não houver runbook: estabilizar sistema com rollback, restart ou failover
- Documentar todas as ações tomadas em tempo real no canal do incidente
- **SLA: Contenção inicial em ≤ 30 min (P1) / ≤ 1h (P2)**

### Etapa 5: Decisão de Escalação
- P1/P2: Escalar automaticamente para Incident Commander e War Room
- P3: Escalar para tech lead do serviço afetado
- P4: Registrar como ticket e priorizar no backlog
- Comunicar impacto ao time de Customer Support
- **SLA: Decisão de escalação em ≤ 15 min após classificação**

### Etapa 6: Documentação Inicial
- Criar timeline do incidente com todas as ações e decisões
- Registrar impacto conhecido: clientes, receita, SLO
- Identificar componentes e times envolvidos
- Vincular alertas, logs e dashboards relevantes
- **SLA: Contínuo durante o incidente**

## Outputs / Entregáveis

- Incidente criado e classificado no Incident Management Tool
- Timeline inicial do incidente documentada
- Severidade definida e comunicada
- Contenção inicial executada (ou em andamento)
- Escalação realizada conforme matriz
- Status page atualizado para clientes (se P1/P2)

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| MTTA (Mean Time to Acknowledge) | ≤ 5 min (P1) / ≤ 15 min (P2) | Semanal |
| MTTD (Mean Time to Detect) | ≤ 10 min para alertas automáticos | Mensal |
| Classificação correta de severidade | ≥ 90% | Mensal |
| Incidentes com contenção no SLA | ≥ 85% | Mensal |
| Cobertura de runbooks por serviço | ≥ 80% | Trimestral |

## Integração com Outros Workflows

- **02-escalation-matrix.md**: Define caminhos de escalação por severidade
- **03-war-room-protocol.md**: P1/P2 acionam protocolo de war room
- **05-communication-cascade.md**: Comunicação externa iniciada na triagem
- **Tech Review / 05-production-readiness.md**: Serviços devem ter alertas configurados
- **Data Governance / 03-quality-monitoring.md**: Alertas de qualidade de dados integrados
