# Workflow: Matriz de Escalação

## Objetivo

Definir caminhos claros e automatizados de escalação para garantir que incidentes sejam direcionados às pessoas certas no tempo certo, evitando atrasos na resolução e garantindo visibilidade adequada para a liderança conforme a severidade.

## Trigger

- Incidente classificado na triagem com severidade definida
- Falha no cumprimento de SLA de resposta ou resolução
- Incidente que muda de severidade (upgrade ou downgrade)
- Solicitação manual de escalação por qualquer participante

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Incident Commander | **Responsible** — Executa escalações conforme matriz |
| SRE Lead | **Accountable** — Garante que matriz está atualizada e funcional |
| VP de Engenharia | **Consulted** — Acionado em P1, decide alocação de recursos |
| CTO | **Consulted** — Acionado em P1 prolongado ou com impacto em receita |
| CEO | **Informed** — Acionado em P1 com impacto reputacional ou regulatório |

## Matriz de Escalação por Severidade

### P1 — Crítico
| Tempo | Ação | Quem é Notificado |
|-------|------|-------------------|
| T+0 min | Alerta automático | Engenheiro on-call |
| T+5 min | Acknowledge obrigatório | On-call + backup on-call |
| T+15 min | War Room aberto | Incident Commander + SRE Lead |
| T+30 min | Escalação funcional | Tech Lead do serviço + VP Eng |
| T+1h | Escalação executiva | CTO + Head de Customer Success |
| T+2h | Escalação C-Level | CEO + CFO (se impacto em receita) |
| T+4h | Status update obrigatório | Board (se impacto regulatório) |

### P2 — Alto
| Tempo | Ação | Quem é Notificado |
|-------|------|-------------------|
| T+0 min | Alerta automático | Engenheiro on-call |
| T+15 min | Acknowledge obrigatório | On-call |
| T+30 min | Escalação técnica | SRE Lead + Tech Lead |
| T+2h | Escalação gerencial | Engineering Manager |
| T+4h | Escalação diretoria | VP de Engenharia |
| T+8h | Status update executivo | CTO |

### P3 — Médio
| Tempo | Ação | Quem é Notificado |
|-------|------|-------------------|
| T+0 min | Alerta automático | Engenheiro on-call |
| T+2h | Escalação técnica | Tech Lead do serviço |
| T+8h | Escalação gerencial | Engineering Manager |
| T+24h | Review de progresso | SRE Lead |

### P4 — Baixo
| Tempo | Ação | Quem é Notificado |
|-------|------|-------------------|
| T+0 min | Ticket criado | Engenheiro on-call |
| T+24h | Priorização no backlog | Tech Lead |
| T+5 dias | Review se não resolvido | Engineering Manager |

## Etapas do Workflow

### Etapa 1: Escalação Automática
- Ferramentas de on-call (PagerDuty/Opsgenie) executam escalação por tempo
- Se on-call não responde em 5 min, backup é acionado automaticamente
- Se backup não responde em 5 min, SRE Lead é acionado
- Todas as escalações são registradas automaticamente na timeline

### Etapa 2: Escalação Funcional
- Incident Commander identifica times técnicos necessários
- Aciona especialistas do serviço afetado e dependências
- Convoca SMEs (Subject Matter Experts) conforme necessidade
- Garante que todos os envolvidos tenham acesso ao canal do incidente

### Etapa 3: Escalação Hierárquica
- Acionada por tempo (conforme matriz) ou por decisão do IC
- Motivos para escalação antecipada:
  - Impacto maior que o estimado inicialmente
  - Necessidade de decisão de negócio (ex: desligar feature)
  - Risco regulatório ou de segurança identificado
  - Necessidade de comunicação externa
- Formato: mensagem no canal executivo + ligação telefônica para P1

### Etapa 4: Escalação para Terceiros
- Fornecedores de infraestrutura (AWS, GCP, Azure): ticket de suporte enterprise
- Parceiros de software: canal de suporte premium
- Consultores de segurança: para incidentes de segurança
- Manter registro de todos os tickets abertos com fornecedores

### Etapa 5: De-escalação
- Quando incidente é contido e impacto cessou
- Incident Commander comunica de-escalação formalmente
- Times liberados gradualmente conforme necessidade diminui
- Status page atualizado para refletir resolução
- Transição para monitoramento pós-incidente (24-48h)

## Outputs / Entregáveis

- Registro completo de escalações na timeline do incidente
- Comunicações de escalação documentadas (quem, quando, por quê)
- SLAs de escalação cumpridos ou exceções documentadas
- Relatório de eficácia da matriz (revisão pós-incidente)

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Escalações dentro do SLA | ≥ 95% | Mensal |
| Tempo médio de escalação P1 | ≤ 15 min | Mensal |
| Falhas de escalação automática | 0 | Mensal |
| Cobertura de on-call (rotação sem gaps) | 100% | Semanal |
| Escalações desnecessárias (falsos positivos) | < 10% | Trimestral |

## Manutenção da Matriz

- Revisão mensal da lista de contatos e rotação de on-call
- Teste trimestral de escalação (fire drill simulado)
- Atualização imediata quando há mudança organizacional
- Validação de números de telefone e canais de contato trimestralmente

## Integração com Outros Workflows

- **01-detection-triage.md**: Triagem define severidade que aciona a matriz
- **03-war-room-protocol.md**: Escalação P1/P2 abre war room automaticamente
- **05-communication-cascade.md**: Escalação executiva dispara comunicação externa
- **Change Management / 02-stakeholder-mapping.md**: Mapa de stakeholders alinhado à matriz
