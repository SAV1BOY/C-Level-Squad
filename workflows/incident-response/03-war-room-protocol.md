# Workflow: Protocolo de War Room

## Objetivo

Estabelecer procedimentos claros para coordenação de resposta a incidentes críticos (P1/P2) em ambiente de war room, garantindo comunicação eficiente, tomada de decisão rápida e resolução coordenada com múltiplos times.

## Trigger

- Incidente classificado como P1 ou P2 na triagem
- Escalação de P3 para P2 devido a agravamento
- Incidente de segurança confirmado (independente da severidade inicial)
- Decisão do Incident Commander de convocar war room

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Incident Commander (IC) | **Accountable** — Coordena toda a operação |
| Tech Lead de Investigação | **Responsible** — Lidera diagnóstico técnico |
| Escriba (Scribe) | **Responsible** — Documenta timeline em tempo real |
| Comunicação (Comms Lead) | **Responsible** — Updates internos e externos |
| Engenheiros Convocados | **Consulted** — Executam diagnóstico e correções |
| VP Engenharia / CTO | **Informed** — Recebem updates periódicos |

## Papéis Detalhados no War Room

### Incident Commander (IC)
- Coordena ações e prioridades — não executa tarefas técnicas
- Toma decisões de escalação, rollback, comunicação
- Garante que todos os participantes têm clareza sobre próximos passos
- Conduz status updates periódicos (a cada 15-30 min)
- Autoriza ações de alto risco (deploy em produção, desligar features)

### Tech Lead de Investigação
- Lidera investigação técnica e diagnóstico da causa raiz
- Coordena engenheiros em streams paralelas de investigação
- Reporta findings ao IC para tomada de decisão
- Propõe soluções (fix, rollback, workaround)

### Escriba (Scribe)
- Documenta TUDO na timeline: ações, decisões, hipóteses, resultados
- Mantém documento compartilhado atualizado em tempo real
- Registra quem fez o quê e quando
- Não participa de investigação — foco 100% em documentação

### Comms Lead
- Envia updates para stakeholders internos no cadência definida
- Coordena comunicação com clientes (status page, email, suporte)
- Prepara talking points para CS e Suporte
- Gerencia canal de perguntas externas ao war room

## Etapas do Workflow

### Etapa 1: Abertura do War Room (T+0 a T+15 min)
- IC cria canal dedicado no Slack: #incident-YYYY-MM-DD-titulo
- Convoca participantes obrigatórios via PagerDuty/telefone
- Inicia call de vídeo permanente (Zoom/Google Meet)
- Documenta contexto inicial: o que sabemos, o que não sabemos
- Define papéis: IC, Tech Lead, Scribe, Comms Lead
- **Primeiro status update em 15 minutos**

### Etapa 2: Diagnóstico e Investigação (T+15 min em diante)
- Tech Lead coordena streams de investigação paralelas
- Cada stream reporta ao IC a cada 15 minutos
- IC prioriza streams com maior probabilidade de resultado
- Hipóteses documentadas no canal com status: Investigando / Descartada / Confirmada
- **Cadência de status: a cada 15 min (P1) / 30 min (P2)**

### Etapa 3: Contenção e Mitigação
- IC decide estratégia: fix forward, rollback, feature flag, workaround
- Ações de alto risco requerem aprovação explícita do IC
- Buddy system: nenhuma mudança em produção sem peer review
- Monitorar métricas após cada ação para validar eficácia
- Documentar cada tentativa e resultado

### Etapa 4: Resolução e Verificação
- Causa raiz identificada e correção aplicada
- Monitoramento intensivo por 30-60 min pós-fix
- Verificar que todos os SLOs voltaram ao normal
- Confirmar com Customer Support que impacto cessou
- IC declara incidente resolvido formalmente

### Etapa 5: Encerramento do War Room
- IC conduz retrospectiva rápida (5 min): o que funcionou, o que melhorar
- Scribe finaliza timeline e publica no canal
- Comms Lead envia comunicação final para stakeholders
- IC agenda postmortem em até 72h
- Monitoramento elevado mantido por 24-48h
- **Comunicação de encerramento para toda a empresa**

## Regras do War Room

1. **IC é a autoridade final** — decisões passam pelo IC
2. **Foco na resolução** — discussões de causa raiz ficam para o postmortem
3. **Sem culpabilização** — cultura blameless durante o incidente
4. **Comunicação no canal** — nada em DMs paralelas
5. **Status updates regulares** — mesmo que não haja novidade
6. **Apenas participantes necessários** — observadores no canal, não na call
7. **Documentar tudo** — se não foi documentado, não aconteceu

## Outputs / Entregáveis

- Timeline completa do incidente publicada
- Comunicação de resolução enviada (interna e externa)
- Postmortem agendado com todos os participantes
- Ações imediatas de follow-up documentadas
- Métricas de impacto consolidadas (duração, clientes afetados, receita)

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| MTTR (Mean Time to Resolve) P1 | ≤ 4 horas | Mensal |
| MTTR P2 | ≤ 8 horas | Mensal |
| War room aberto dentro do SLA | ≥ 95% | Mensal |
| Qualidade da timeline (completude) | ≥ 90% | Por incidente |
| Postmortem agendado em 72h | 100% | Por incidente |

## Integração com Outros Workflows

- **01-detection-triage.md**: Triagem P1/P2 aciona war room
- **02-escalation-matrix.md**: Escalação segue matriz durante war room
- **04-postmortem-process.md**: War room alimenta postmortem com timeline
- **05-communication-cascade.md**: Comms Lead segue cascata de comunicação
