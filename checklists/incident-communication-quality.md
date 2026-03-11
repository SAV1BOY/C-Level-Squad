# Checklist de Qualidade — Comunicação de Incidentes (Incident Communication)

## Propósito
Garantir que a comunicação durante e após incidentes seja clara, oportuna, direcionada aos canais corretos, com owners definidos, atualizações regulares e post-mortem agendado. Este checklist protege a reputação da organização, mantém a confiança dos stakeholders e garante aprendizado organizacional a partir de cada incidente.

## Quando Aplicar
- Imediatamente após a identificação de qualquer incidente de severidade média ou alta
- Durante o gerenciamento ativo do incidente (para atualizações)
- Após a resolução do incidente (para comunicação de encerramento)
- Na preparação do post-mortem e comunicação de lições aprendidas
- Em exercícios de simulação de incidentes (tabletop exercises)
- Quando agentes de monitoramento detectam anomalias e precisam comunicar

## Agente Responsável
- **Primário:** Incident Commander Agent ou On-Call Agent
- **Comunicação externa:** CMO Agent ou PR Agent
- **Comunicação interna:** CoS Agent
- **Decisão de escalação:** CEO Agent
- **Post-mortem:** CTO Agent ou Engineering Lead Agent

## Checklist

### Seção 1 — Clareza da Comunicação
- [ ] A mensagem inicial descreve o que aconteceu em linguagem simples e objetiva
- [ ] O impacto nos usuários/clientes está descrito de forma concreta (não vaga)
- [ ] A severidade do incidente está classificada e comunicada (Sev1, Sev2, Sev3)
- [ ] O que está sendo feito para resolver está explicado (ações em andamento)
- [ ] O que NÃO está afetado está comunicado (delimitar o escopo do impacto)
- [ ] A comunicação evita jargão técnico para audiências não-técnicas
- [ ] A comunicação evita especulação — relata apenas fatos confirmados
- [ ] A causa raiz é comunicada apenas quando confirmada (não hipóteses)
- [ ] A comunicação é honesta sobre o que sabemos e o que ainda não sabemos
- [ ] O tom é empático, responsável e profissional (sem defensividade)
- [ ] Links para status pages ou dashboards em tempo real estão incluídos quando aplicável
- [ ] Cada comunicação tem número de referência do incidente para rastreabilidade

### Seção 2 — Timing e Cadência
- [ ] A primeira comunicação é emitida dentro de 15 minutos da identificação (Sev1) ou 30 minutos (Sev2)
- [ ] A cadência de atualizações está definida e comunicada (ex: a cada 30 min para Sev1)
- [ ] As atualizações são enviadas mesmo quando não há novidades (para confirmar que estamos trabalhando)
- [ ] A comunicação de resolução é emitida assim que o incidente está resolvido e confirmado
- [ ] O timeline do incidente está documentado com timestamps precisos
- [ ] A comunicação proativa é priorizada sobre a reativa (informar antes que clientes reclamem)
- [ ] O horário do incidente (fuso horário, horário comercial vs fora de horário) está considerado na estratégia
- [ ] A cadência de comunicação está ajustada à severidade (mais frequente para mais severo)

### Seção 3 — Canais Apropriados
- [ ] Os canais de comunicação por tipo de stakeholder estão definidos e mapeados
- [ ] Comunicação interna usa canais corporativos (Slack, email, war room)
- [ ] Comunicação para clientes usa canais oficiais (status page, email, in-app notification)
- [ ] Comunicação para parceiros/fornecedores usa canais B2B definidos
- [ ] Comunicação para reguladores segue os protocolos legais e compliance
- [ ] Comunicação para imprensa/público passa pelo filtro de PR/comunicação corporativa
- [ ] Os canais de comunicação estão testados e funcionais (não depender de sistemas afetados)
- [ ] A escalação para canais de maior alcance é feita conforme a severidade
- [ ] Os canais sociais são monitorados para responder questões e corrigir desinformação
- [ ] Existe um canal dedicado para comunicação do war room (apenas equipe de resposta)

### Seção 4 — Owners e Papéis
- [ ] O Incident Commander está designado e visível para toda a equipe de resposta
- [ ] O Communication Lead está designado (separado do Incident Commander quando possível)
- [ ] Os engenheiros de resposta estão identificados por área de expertise
- [ ] O decision-maker para trade-offs de impacto vs velocidade de resolução está definido
- [ ] O ponto focal para comunicação com clientes está designado
- [ ] O ponto focal para comunicação com parceiros está designado
- [ ] O ponto focal para comunicação regulatória está designado
- [ ] Os backup owners estão definidos para cada papel (cobertura 24/7 se necessário)
- [ ] Os handoffs entre turnos estão planejados para incidentes prolongados
- [ ] O executive sponsor do incidente está informado e acessível para decisões de alto impacto

### Seção 5 — Atualizações Estruturadas
- [ ] Cada atualização segue template padrão: status, impacto, ações, próxima atualização
- [ ] As atualizações incluem o que mudou desde a última comunicação
- [ ] As ações em andamento estão listadas com ETA quando possível
- [ ] Os workarounds disponíveis para clientes estão comunicados
- [ ] A comunicação de resolução confirma que o serviço está restaurado com evidência
- [ ] A comunicação de encerramento inclui agradecimento e próximos passos (post-mortem)
- [ ] As métricas de impacto estão incluídas quando disponíveis (downtime, users affected)
- [ ] O registro completo de comunicações está preservado para auditoria
- [ ] Cada atualização é revisada por um segundo par de olhos antes do envio (para Sev1/Sev2)

### Seção 6 — Post-mortem Agendado
- [ ] O post-mortem está agendado dentro de 5 dias úteis após a resolução do incidente
- [ ] O owner do post-mortem está designado
- [ ] Os participantes do post-mortem estão convocados (equipe de resposta + stakeholders-chave)
- [ ] O formato é blameless (sem culpabilização, foco em sistemas e processos)
- [ ] O template de post-mortem inclui: timeline, causa raiz, impacto, ações corretivas
- [ ] As ações corretivas do post-mortem têm owner e deadline definidos
- [ ] O post-mortem é publicado internamente para aprendizado organizacional
- [ ] As métricas de incidente (MTTR, MTTD, impacto) são registradas no dashboard
- [ ] O follow-up de ações corretivas está agendado (30 e 60 dias pós-incidente)
- [ ] As lições aprendidas são incorporadas ao processo de prevenção e detecção
- [ ] O post-mortem é compartilhado com clientes/parceiros quando o impacto foi significativo

## Critérios de Aprovação
- Comunicação inicial emitida dentro do SLA de tempo definido por severidade
- Todos os stakeholders relevantes informados nos canais apropriados
- Owners e papéis claramente designados e funcionais durante o incidente
- Atualizações regulares emitidas conforme cadência definida
- Post-mortem agendado e confirmado com owner designado
- Registro completo de comunicações preservado para auditoria

## O que Fazer se Falhar
1. Se a comunicação inicial atrasou, documentar o motivo e ajustar processo para próximo incidente
2. Se canais incorretos foram usados, corrigir imediatamente e notificar nos canais corretos
3. Se atualizações foram irregulares, designar Communication Lead exclusivo para cadência
4. Se o post-mortem não foi agendado, escalar para o CTO Agent e agendar imediatamente
5. Se ações corretivas de post-mortems anteriores não foram implementadas, escalar para CEO Agent
6. Registrar falhas de comunicação no RalphLoop para melhoria do incident response process
7. Realizar tabletop exercise se falhas sistemáticas foram identificadas

## Referências
- Google — "Site Reliability Engineering" (SRE book, incident management)
- PagerDuty — Incident Response Documentation (open source)
- Dekker, S. — "The Field Guide to Understanding Human Error" (just culture)
- Template interno: `/templates/incident-communication-template.md`
- Runbook de incidentes: `/runbooks/incident-response-runbook.md`
- Template de post-mortem: `/templates/postmortem-template.md`
