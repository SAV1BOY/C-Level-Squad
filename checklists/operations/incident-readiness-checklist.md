# Checklist de Prontidão para Incidentes

## Objetivo
Garantir que a organização esteja preparada para detectar, responder e resolver incidentes de forma rápida e eficaz, minimizando impacto no negócio.

---

## 1. Framework de Classificação de Incidentes

### Definição de Severidades
- [ ] Definir critérios claros para cada nível de severidade:
  - **SEV1 (Crítico)**: Sistema principal indisponível, impacto em todos os clientes
  - **SEV2 (Alto)**: Funcionalidade crítica degradada, impacto em muitos clientes
  - **SEV3 (Médio)**: Funcionalidade não-crítica indisponível, workaround disponível
  - **SEV4 (Baixo)**: Issue menor, sem impacto significativo para clientes
- [ ] Documentar exemplos concretos para cada severidade
- [ ] Definir SLAs de resposta e resolução por severidade
- [ ] Treinar equipe na classificação correta de incidentes
- [ ] Revisar classificação trimestralmente com base em dados reais

### Critérios de Escalation
- [ ] Definir matriz de escalation por severidade e tempo
- [ ] SEV1: Notificar VP Engineering e CTO imediatamente
- [ ] SEV2: Notificar Engineering Manager em até 15 minutos
- [ ] Definir quando envolver C-Level na comunicação externa
- [ ] Documentar contatos de emergência atualizados (24/7)
- [ ] Definir processo para escalar para fornecedores externos

---

## 2. Equipe e Roles

### On-Call
- [ ] Estabelecer rotação de on-call com pelo menos 2 pessoas
- [ ] Garantir cobertura 24/7 com handoffs claros
- [ ] Definir compensação por on-call (folga, adicional)
- [ ] Treinar todos os membros elegíveis para on-call
- [ ] Garantir que on-call tem acesso a todos os sistemas necessários
- [ ] Testar processo de notificação (PagerDuty, OpsGenie) mensalmente
- [ ] Definir backup para quando on-call primário não responder

### Roles Durante Incidente
- [ ] **Incident Commander (IC)**: Coordena resposta, decisões, comunicação
- [ ] **Tech Lead**: Lidera investigação e resolução técnica
- [ ] **Communicator**: Gerencia comunicação com stakeholders e clientes
- [ ] **Scribe**: Documenta timeline, ações e decisões em tempo real
- [ ] Definir quem assume cada role por default e como rotacionar
- [ ] Treinar pelo menos 5 pessoas para cada role
- [ ] Documentar responsabilidades de cada role em runbook

---

## 3. Ferramentas e Infraestrutura

### Monitoramento
- [ ] Dashboards de saúde do sistema atualizados e acessíveis
- [ ] Alertas configurados para métricas críticas (uptime, latência, errors)
- [ ] Logging centralizado com busca rápida (ELK, Datadog, Splunk)
- [ ] Tracing distribuído para debug de sistemas complexos
- [ ] Status page pública configurada e testada
- [ ] Alertas com threshold bem calibrados (evitar alert fatigue)
- [ ] Runbooks linkados nos alertas para ação imediata

### Comunicação
- [ ] Canal dedicado de incidentes no Slack/Teams (auto-criação por bot)
- [ ] Bridge de voz (Zoom, Meet) para SEV1/SEV2 com link fixo
- [ ] Template de comunicação para clientes pré-aprovado
- [ ] Lista de distribuição atualizada para notificações internas
- [ ] Ferramenta de status page (Statuspage.io, Instatus)
- [ ] Bot de incidentes para automatizar workflow (Rootly, incident.io)

### Acesso de Emergência
- [ ] Processo de break-glass para acesso privilegiado documentado
- [ ] Credenciais de emergência armazenadas de forma segura
- [ ] VPN e acesso remoto testados para toda equipe de on-call
- [ ] Acesso a consoles de cloud (AWS, GCP, Azure) validado
- [ ] Processo de rollback de deploy documentado e testado
- [ ] Feature flags configuradas para desabilitar funcionalidades

---

## 4. Runbooks e Procedimentos

### Runbooks Obrigatórios
- [ ] Runbook de resposta a incidente genérico (passo a passo)
- [ ] Runbook por sistema crítico (como diagnosticar e resolver)
- [ ] Runbook de rollback de deploy
- [ ] Runbook de failover para DR site
- [ ] Runbook de comunicação para clientes durante incidente
- [ ] Runbook de restore de backup de banco de dados
- [ ] Runbook de scaling de emergência (adicionar capacidade)

### Qualidade dos Runbooks
- [ ] Cada runbook testado por alguém que não o escreveu
- [ ] Runbooks acessíveis offline (PDF, impresso) para cenários extremos
- [ ] Runbooks revisados e atualizados trimestralmente
- [ ] Tempo estimado de execução documentado em cada runbook
- [ ] Pré-requisitos e acessos necessários documentados
- [ ] Pontos de decisão e escalation claramente marcados

---

## 5. Drills e Simulações

### Game Days
- [ ] Agendar simulação de incidente pelo menos trimestralmente
- [ ] Simular diferentes tipos: outage, data breach, deploy ruim
- [ ] Testar processo end-to-end: detecção, resposta, comunicação, resolução
- [ ] Incluir cenários que testam escalation e comunicação executiva
- [ ] Documentar aprendizados e gaps encontrados
- [ ] Implementar melhorias identificadas antes do próximo drill

### Chaos Engineering
- [ ] Avaliar adoção de chaos engineering (Chaos Monkey, Gremlin)
- [ ] Começar com experimentos em ambiente de staging
- [ ] Definir steady-state hypothesis antes de cada experimento
- [ ] Gradualmente expandir para produção com controle
- [ ] Documentar resiliências descobertas e vulnerabilidades

---

## 6. Post-Mortem

### Processo de Post-Mortem
- [ ] Realizar post-mortem para todo incidente SEV1 e SEV2
- [ ] Post-mortem em até 5 dias úteis após resolução
- [ ] Usar framework blameless (sem culpar indivíduos)
- [ ] Template padronizado: timeline, impacto, causa raiz, ações
- [ ] Participação de todos os envolvidos na resposta
- [ ] Publicar post-mortem internamente para aprendizado organizacional
- [ ] Tracking de action items até conclusão

### Métricas de Incidentes
- [ ] MTTD (Mean Time to Detect): meta < 5 minutos
- [ ] MTTR (Mean Time to Resolve): meta por severidade
- [ ] MTBF (Mean Time Between Failures): tendência de melhoria
- [ ] Número de incidentes por severidade por mês
- [ ] Percentual de action items de post-mortem completados
- [ ] Revisão mensal de métricas com leadership team
