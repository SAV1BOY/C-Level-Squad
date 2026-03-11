# Workflow: Cascata de Comunicação

## Objetivo

Garantir comunicação rápida, transparente e coordenada durante incidentes, assegurando que stakeholders internos e externos recebam informações precisas no momento adequado, preservando a confiança de clientes e a reputação da empresa.

## Trigger

- Incidente classificado como P1 ou P2 na triagem
- Incidente P3 com impacto visível para clientes
- Qualquer incidente de segurança confirmado
- Decisão do Incident Commander de ativar comunicação externa

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Comms Lead (do War Room) | **Responsible** — Redige e publica comunicações |
| Incident Commander | **Accountable** — Aprova comunicações antes do envio |
| Customer Success Lead | **Consulted** — Comunicação direta com clientes enterprise |
| Head de Marketing/PR | **Consulted** — Para incidentes com impacto público |
| Suporte ao Cliente | **Informed** — Recebe talking points para atendimento |
| Jurídico | **Consulted** — Para incidentes com implicação regulatória |

## Camadas de Comunicação

### Camada 1: Comunicação Interna Técnica
- **Canal**: Slack #incident-[ID]
- **Audiência**: Time de engenharia envolvido
- **Cadência**: Contínua durante o incidente
- **Conteúdo**: Detalhes técnicos, hipóteses, ações em andamento

### Camada 2: Comunicação Interna Executiva
- **Canal**: Slack #incidents-exec + email para C-Level
- **Audiência**: Liderança executiva
- **Cadência**: A cada 30 min (P1) / 1h (P2)
- **Conteúdo**: Impacto, timeline resumida, ETA, decisões necessárias

### Camada 3: Comunicação para Suporte e CS
- **Canal**: Slack #incidents-support + talking points doc
- **Audiência**: Times de Suporte e Customer Success
- **Cadência**: A cada atualização significativa
- **Conteúdo**: Talking points, respostas para perguntas frequentes, impacto no cliente

### Camada 4: Comunicação Externa para Clientes
- **Canal**: Status page + email para clientes afetados
- **Audiência**: Clientes
- **Cadência**: Update a cada 30 min (P1) / 1h (P2)
- **Conteúdo**: Impacto, status atual, workarounds, ETA (quando disponível)

### Camada 5: Comunicação Pública
- **Canal**: Status page pública + redes sociais (se necessário)
- **Audiência**: Público geral, imprensa
- **Cadência**: Conforme necessidade
- **Conteúdo**: Statement aprovado por Marketing e Jurídico

## Etapas do Workflow

### Etapa 1: Primeira Comunicação (T+15 min para P1, T+30 min para P2)
- Comms Lead redige primeira comunicação baseada na triagem
- Template: "Identificamos um [problema] que está afetando [serviço]. Estamos investigando e forneceremos atualizações a cada [X] minutos."
- IC aprova antes do envio
- Publicar em status page e notificar canais internos
- **SLA: 15 min (P1) / 30 min (P2) após abertura do incidente**

### Etapa 2: Updates Regulares
- Seguir cadência definida por severidade, mesmo sem novidades
- Template de update: "Status: [Investigando/Identificado/Monitorando]. Último update: [ação tomada]. Próximo update em [X] minutos."
- Incluir workarounds quando disponíveis
- Atualizar ETA conforme evolução do diagnóstico
- **Regra: Nunca prometer ETA que não pode cumprir**

### Etapa 3: Comunicação de Resolução
- Confirmar que impacto cessou antes de comunicar resolução
- Template: "O incidente que afetava [serviço] foi resolvido às [hora]. [Breve explicação]. Continuamos monitorando."
- Incluir ações tomadas (sem detalhes técnicos excessivos)
- Oferecer canal para clientes reportarem problemas residuais
- **SLA: 30 min após IC declarar incidente resolvido**

### Etapa 4: Comunicação Pós-Incidente (D+1 a D+5)
- Enviar nota detalhada para clientes enterprise afetados
- Publicar RCA (Root Cause Analysis) simplificado no status page
- CS agenda calls com clientes críticos se necessário
- Incluir: o que aconteceu, por que aconteceu, o que estamos fazendo para prevenir
- **SLA: Até 5 dias úteis para comunicação pós-incidente**

### Etapa 5: Comunicação para Reguladores (se aplicável)
- Jurídico avalia necessidade de notificação regulatória
- LGPD: notificação à ANPD em até 72h para incidentes com dados pessoais
- PCI-DSS: notificação conforme requisitos do padrão
- SOC2: documentação no sistema de controles

## Templates de Comunicação

### Status Page — Investigando
> Estamos investigando relatos de [descrição do problema] no [serviço afetado]. Nosso time está trabalhando para identificar a causa e restaurar o serviço. Atualizaremos este status a cada [X] minutos.

### Status Page — Identificado
> Identificamos a causa do [problema] e estamos implementando a correção. [Workaround disponível: descrição]. Próximo update em [X] minutos.

### Email para Clientes Enterprise
> Prezado(a) [Nome], gostaríamos de informar sobre um incidente que afetou [serviço] entre [hora início] e [hora fim] em [data]. [Descrição do impacto]. [Ações tomadas]. [Medidas preventivas]. Estamos à disposição para agendar uma call caso deseje mais detalhes.

## Outputs / Entregáveis

- Histórico de comunicações publicado na timeline do incidente
- Status page atualizado com resolução e RCA simplificado
- Talking points documentados para time de suporte
- Comunicação pós-incidente enviada para clientes afetados
- Notificações regulatórias enviadas (se aplicável)

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Tempo até primeira comunicação externa | ≤ 15 min (P1) | Por incidente |
| Updates dentro da cadência prometida | ≥ 95% | Por incidente |
| CSAT pós-incidente | ≥ 3.5/5.0 | Por incidente P1 |
| Reclamações sobre falta de comunicação | 0 | Mensal |
| Comunicação pós-incidente no prazo | ≥ 90% | Mensal |

## Integração com Outros Workflows

- **03-war-room-protocol.md**: Comms Lead participa do war room
- **04-postmortem-process.md**: RCA alimenta comunicação pós-incidente
- **02-escalation-matrix.md**: Escalação executiva dispara comunicação C-Level
- **Change Management / 03-communication-plan.md**: Templates alinhados com plano de comunicação
