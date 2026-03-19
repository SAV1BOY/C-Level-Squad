# Workflow 11: Incident Response Executivo

## Objetivo

Orquestrar a resposta executiva a incidentes críticos que afetam operações, reputação ou receita da organização. Este workflow cobre o ciclo completo — desde a detecção e avaliação inicial até a contenção, comunicação com stakeholders, resolução e postmortem executivo — garantindo que o C-Level Squad atue de forma coordenada, rápida e documentada em situações de crise.

> **Princípio:** Incidentes mal geridos no nível executivo destroem confiança. A velocidade da resposta importa, mas a qualidade da comunicação e da contenção importam mais.

---

## Agentes Envolvidos

| Agente | Papel no Workflow |
|--------|-------------------|
| **Vision Chief (CEO)** | Decisor final em P1, porta-voz externo, comunicação com board/investidores |
| **COO Orchestrator** | Incident Commander executivo, coordenação de war room, tracking de ações |
| **CTO Architect** | Liderança técnica da contenção e resolução, interface com engenharia |
| **CIO Engineer** | Avaliação de impacto em sistemas, dados e compliance (LGPD) |
| **CAIO Architect** | Avaliação de incidentes envolvendo IA (bias, hallucination, data leakage) |
| **CMO Architect** | Comunicação externa, impacto em marca, gestão de percepção |
| **CFO Strategist** | Quantificação de impacto financeiro, acionamento de seguros |
| **Squad Coordinator** | Logística do war room, tracking de timeline, documentação em tempo real |

---

## Trigger (quando iniciar)

Este workflow é ativado quando qualquer uma das condições abaixo for verdadeira:

1. **Incidente P1 declarado** — sistema principal indisponível, perda de dados confirmada ou brecha de segurança
2. **Incidente P2 com escalação** — degradação significativa que não foi resolvida dentro do SLA de 2 horas
3. **Incidente de reputação** — exposição em mídia, redes sociais ou canais de stakeholders
4. **Incidente regulatório** — violação de LGPD, compliance ou requisitos contratuais
5. **Incidente de IA** — modelo em produção gerando outputs danosos, bias confirmado ou data leakage
6. **Acionamento manual pelo Vision Chief ou COO** — qualquer situação que demande resposta executiva coordenada

### Canais de Detecção

- Escalação via `workflows/incident-response/01-detection-triage.md`
- Alerta do Cybersecurity Squad via canal de incidentes
- Reporte direto de stakeholder externo (board, investidor, parceiro)
- Monitoramento de mídia e redes sociais (CMO Architect)
- Alerta de sistemas de monitoramento de modelos de IA (CAIO Architect)

---

## Pré-condições

- [ ] Canal de comunicação de emergência configurado (Slack #war-room ou equivalente)
- [ ] Lista de contatos de emergência atualizada (última atualização < 30 dias)
- [ ] Templates de comunicação pré-aprovados disponíveis (vide seção de templates abaixo)
- [ ] Playbooks técnicos de contenção documentados por serviço crítico
- [ ] Roles de Incident Commander e porta-voz designados e treinados
- [ ] Acesso a dashboards de status em tempo real configurado para todos os agentes
- [ ] Registro de incidentes anteriores acessível via `data/registries/lessons-learned.yaml`
- [ ] Seguro de cyber risk ativo e condições de acionamento conhecidas

---

## Processo (step-by-step com decision points)

### FASE 1: Detecção e Avaliação Inicial (0-15 min)

**Step 1.1 — Recebimento do Alerta**
- COO Orchestrator recebe notificação de incidente via canal de escalação
- Registrar timestamp exato de início do incidente
- Ativar canal de war room (#incident-YYYY-MM-DD)

**Step 1.2 — Classificação de Severidade Executiva**

| Severidade | Critérios | Tempo de Resposta Executiva |
|-----------|-----------|---------------------------|
| **SEV-1 (Crítico)** | Revenue impact > R$ 100K/hora, todos os clientes afetados, brecha de segurança confirmada, risco regulatório | Imediato (< 15 min) |
| **SEV-2 (Alto)** | Revenue impact > R$ 50K/hora, maioria dos clientes afetados, funcionalidade core degradada | < 30 min |
| **SEV-3 (Moderado)** | Revenue impact < R$ 50K/hora, grupo de clientes afetado, workaround disponível | < 2 horas |
| **SEV-4 (Baixo)** | Impacto mínimo, poucos clientes, issue cosmético | Próximo business day |

> **Decision Point 1:** Se SEV-1 ou SEV-2 → ativar War Room imediato (Step 2). Se SEV-3 → monitorar e escalar se necessário. Se SEV-4 → tratar no fluxo normal.

**Step 1.3 — Notificação Inicial da Liderança**
- COO Orchestrator notifica Vision Chief e agentes relevantes
- Formato da notificação inicial:

```
🔴 INCIDENTE [SEV-X] — [Título breve]
Início: [timestamp]
Impacto: [descrição do impacto]
Clientes afetados: [estimativa]
Status: Avaliando
Incident Commander: [nome]
War Room: [link do canal]
Próximo update: [timestamp + 15min]
```

### FASE 2: War Room e Contenção (15 min - 4 horas)

**Step 2.1 — Ativação do War Room**
- COO Orchestrator assume como Incident Commander (ou delega)
- Definir roles no war room:

| Role | Responsável | Função |
|------|------------|--------|
| Incident Commander | COO Orchestrator | Coordena tudo, toma decisões operacionais |
| Tech Lead | CTO Architect | Lidera investigação e contenção técnica |
| Comms Lead | CMO Architect | Prepara e distribui comunicações |
| Scribe | Squad Coordinator | Documenta timeline, decisões e ações |
| Business Impact Lead | CFO Strategist | Quantifica impacto financeiro em tempo real |

**Step 2.2 — Investigação Paralela**
- CTO Architect coordena com equipe técnica para identificar root cause
- CIO Engineer avalia impacto em dados, integrações e compliance
- CAIO Architect avalia se há componente de IA no incidente
- CMO Architect monitora impacto em canais externos e percepção

**Step 2.3 — Estratégia de Contenção**

> **Decision Point 2:** Qual estratégia de contenção aplicar?

| Opção | Quando Usar | Risco |
|-------|-------------|-------|
| **Rollback** | Deploy recente causou o problema | Perda de features recém-lançadas |
| **Feature Flag** | Funcionalidade específica defeituosa | Degradação parcial para usuários |
| **Scale Up** | Problema de capacidade | Custo adicional de infra |
| **Circuit Breaker** | Serviço downstream instável | Funcionalidade degradada |
| **Comunicação + Espera** | Fix em andamento, ETA conhecida | Desgaste com clientes |
| **Isolamento** | Brecha de segurança | Indisponibilidade temporária |

**Step 2.4 — Execução da Contenção**
- Tech Lead implementa a estratégia escolhida
- Incident Commander valida que contenção foi efetiva
- Scribe registra todas as ações com timestamp
- Update a cada 15 minutos para stakeholders internos

**Step 2.5 — Validação da Contenção**
- Confirmar que o impacto foi reduzido ou eliminado
- Verificar métricas de saúde do sistema voltaram ao baseline
- Confirmar com Customer Support que reclamações estão diminuindo

> **Decision Point 3:** Contenção efetiva? Se SIM → avançar para comunicação e resolução. Se NÃO → escalar para Vision Chief e considerar medidas extraordinárias.

### FASE 3: Comunicação com Stakeholders (paralelo à contenção)

**Step 3.1 — Mapeamento de Audiências**

| Audiência | Canal | Timing | Owner |
|-----------|-------|--------|-------|
| Time interno (engenharia) | Slack #war-room | Tempo real | COO Orchestrator |
| C-Level Squad | Slack #c-level-urgent | A cada 15 min | Squad Coordinator |
| All-hands (empresa) | Email + Slack #general | A cada 30 min ou mudança de status | CMO Architect |
| Clientes (status page) | Status page pública | A cada 30 min | CMO Architect |
| Clientes (enterprise) | Email direto + telefone | Imediato para P1 | CMO Architect + CS |
| Board / Investidores | Email + telefone | Se SEV-1 > 2 horas | Vision Chief |
| Mídia / Imprensa | Comunicado oficial | Se exposição pública | Vision Chief + CMO |
| Reguladores | Comunicação formal | Se exigido por lei (LGPD: 72h) | CIO Engineer |

**Step 3.2 — Templates de Comunicação**

**Template: Comunicação Inicial (Status Page)**
```
[Status: Investigando]
Título: [Descrição breve do impacto]
Identificamos um problema que está afetando [descrição do impacto para o usuário].
Nossa equipe está investigando ativamente e implementando medidas de contenção.
Próximo update: [horário]
```

**Template: Update em Andamento**
```
[Status: Contenção em andamento]
Título: [Descrição breve do impacto]
Identificamos a causa do problema: [descrição de alto nível, sem detalhes técnicos].
Medidas de contenção foram implementadas e estamos observando [melhora/estabilização].
Impacto atual: [status reduzido/mantido].
Próximo update: [horário]
```

**Template: Resolução**
```
[Status: Resolvido]
Título: [Descrição breve do impacto]
O problema foi resolvido às [horário].
Duração total: [X horas Y minutos].
Causa: [descrição de alto nível].
Ações tomadas: [resumo].
Conduziremos uma análise detalhada e compartilharemos aprendizados.
Pedimos desculpas pelo inconveniente.
```

**Template: Comunicação para Board (SEV-1)**
```
Assunto: [INCIDENTE SEV-1] — [Título] — Update [N]

Resumo Executivo:
- Início: [timestamp]
- Impacto estimado: [R$ / clientes / reputação]
- Status: [Investigando / Contendo / Resolvido]
- ETA para resolução: [estimativa]
- Risco regulatório: [sim/não — se sim, detalhar]
- Ações do C-Level: [o que estamos fazendo]
- Próximo update: [timestamp]

[Assinatura Vision Chief]
```

**Step 3.3 — Execução da Comunicação**
- CMO Architect aprova cada comunicação antes do envio
- Vision Chief aprova pessoalmente comunicações para board e mídia
- Squad Coordinator registra cada comunicação enviada com timestamp e audiência

### FASE 4: Resolução (variável)

**Step 4.1 — Implementação do Fix Definitivo**
- CTO Architect coordena a implementação da correção definitiva
- Code review acelerado mas obrigatório (mínimo 1 reviewer)
- Testes essenciais executados (smoke tests + testes de regressão críticos)

**Step 4.2 — Validação e Rollout do Fix**
- Deploy em ambiente de staging primeiro (mesmo em emergência)
- Validação com métricas de saúde por mínimo 15 minutos
- Rollout gradual em produção (canary → 10% → 50% → 100%)
- Monitoramento intensivo por 2 horas após full rollout

**Step 4.3 — Declaração de Resolução**

> **Decision Point 4:** Todas as métricas voltaram ao baseline? Clientes confirmam que o problema foi resolvido?

- Se SIM: Incident Commander declara incidente resolvido
- Se NÃO: Continuar investigação ou identificar novo problema

**Step 4.4 — Comunicação de Resolução**
- Enviar update final para todas as audiências (conforme template acima)
- Atualizar status page para "Resolvido"
- Agradecer equipe no war room

### FASE 5: Postmortem Executivo (24-72 horas após resolução)

**Step 5.1 — Coleta de Dados**
- Squad Coordinator compila timeline completa do incidente
- CTO Architect prepara análise técnica de root cause
- CFO Strategist finaliza cálculo de impacto financeiro
- CMO Architect compila feedback de clientes e percepção externa
- CIO Engineer avalia implicações de compliance

**Step 5.2 — Sessão de Postmortem (Blameless)**

> **REGRA: Postmortem blameless é inegociável. Foco em sistemas e processos, nunca em culpar indivíduos.**

Agenda do postmortem executivo (máximo 90 minutos):
1. Timeline factual do incidente (15 min)
2. Root Cause Analysis usando 5 Whys (20 min)
3. Impacto real: financeiro, clientes, reputação, compliance (10 min)
4. O que funcionou bem na resposta (10 min)
5. O que pode melhorar na resposta (15 min)
6. Action items com DRI e prazo (15 min)
7. Classificação final e lições aprendidas (5 min)

**Step 5.3 — Root Cause Analysis (RCA) Framework**

Utilizar o framework dos 5 Whys combinado com Fishbone (Ishikawa):

| Categoria | Perguntas de Investigação |
|-----------|--------------------------|
| **Tecnologia** | O que falhou tecnicamente? Qual componente? Havia monitoramento? |
| **Processo** | Qual processo falhou ou estava ausente? O runbook existia? |
| **Pessoas** | Houve gap de conhecimento? O treinamento era adequado? |
| **Comunicação** | A escalação foi rápida o suficiente? Os stakeholders foram informados? |
| **Prevenção** | Isso poderia ter sido detectado antes? Havia testes para este cenário? |

**Step 5.4 — Definição de Action Items**

Cada action item deve conter:
- Descrição clara da ação
- DRI (Directly Responsible Individual)
- Prazo (deadline)
- Tipo: preventivo (evitar recorrência) ou detectivo (detectar mais rápido)
- Prioridade: P1 (< 1 semana), P2 (< 1 mês), P3 (< 1 trimestre)

**Step 5.5 — Publicação do Postmortem**
- Documento de postmortem publicado internamente em até 5 business days
- Versão resumida compartilhada com clientes enterprise (se SEV-1)
- Lições aprendidas registradas em `data/registries/lessons-learned.yaml`

---

## Quality Gates

### Gate 1: Ativação do War Room (antes de prosseguir para contenção)
- [ ] Severidade classificada corretamente com base nos critérios definidos
- [ ] Incident Commander designado e war room ativado
- [ ] Todos os roles do war room preenchidos
- [ ] Primeira notificação enviada em < 15 minutos
- [ ] Referência: `checklists/governance-risk/crisis-response-quality.md`

### Gate 2: Contenção (antes de declarar estabilização)
- [ ] Impacto reduzido ou eliminado — métricas confirmam
- [ ] Clientes afetados notificados via canal apropriado
- [ ] Workaround documentado se fix definitivo não está disponível
- [ ] Nenhuma ação de contenção introduziu novo risco
- [ ] Referência: `checklists/incident-communication-quality.md`

### Gate 3: Resolução (antes de declarar resolvido)
- [ ] Fix definitivo implementado e validado em produção
- [ ] Métricas de saúde retornaram ao baseline por mínimo 2 horas
- [ ] Todas as audiências receberam comunicação de resolução
- [ ] Timeline do incidente documentada pelo Scribe

### Gate 4: Postmortem (antes de fechar o incidente)
- [ ] Sessão de postmortem blameless realizada em até 72 horas
- [ ] Root Cause Analysis documentada com 5 Whys completos
- [ ] Action items definidos com DRI, prazo e prioridade
- [ ] Impacto financeiro calculado pelo CFO Strategist
- [ ] Lições registradas em `data/registries/lessons-learned.yaml`
- [ ] Referência: `checklists/ralphloop-quality.md`

---

## Outputs / Artefatos

| Artefato | Formato | Responsável | Destino |
|----------|---------|-------------|---------|
| Timeline do incidente | Markdown | Squad Coordinator | `data/incidents/YYYY-MM-DD-titulo.md` |
| Postmortem Report | Template padrão | CTO Architect + COO | `templates/reports/postmortem-report.md` |
| Comunicações enviadas | Log com timestamps | CMO Architect | Anexo ao postmortem |
| Cálculo de impacto financeiro | Planilha | CFO Strategist | Anexo ao postmortem |
| Action items tracker | YAML | COO Orchestrator | `data/registries/initiative-registry.yaml` |
| RCA Document | Markdown | CTO Architect | Anexo ao postmortem |

---

## Registries Atualizados

- `data/registries/risk-registry.yaml` — Atualizar perfil de risco com base no incidente
- `data/registries/lessons-learned.yaml` — Registrar lições aprendidas do postmortem
- `data/registries/decision-registry.yaml` — Registrar decisões tomadas durante o incidente
- `data/registries/initiative-registry.yaml` — Action items de prevenção como novas iniciativas
- `data/registries/metric-registry.yaml` — Atualizar MTTR, MTTD e taxa de incidentes

---

## Próximos Passos

1. Action items do postmortem são incorporados aos backlogs dos squads responsáveis
2. COO Orchestrator faz follow-up semanal dos action items até conclusão
3. Próxima WBR inclui status dos action items do incidente
4. Próxima QBR inclui revisão agregada de incidentes do trimestre
5. Se incidente revelou gap sistêmico: acionar `workflows/12-risk-review-cycle.md`
6. Se incidente gerou aprendizado relevante: acionar `workflows/20-postmortem-and-learning.md`
7. Se comunicação com stakeholders precisa de follow-up: acionar `workflows/13-stakeholder-comms.md`

---

## Cross-squad Handoffs

| Squad | Handoff | Direção | SLA |
|-------|---------|---------|-----|
| **Cybersecurity Squad** | Alertas de segurança, análise forense, compliance assessment | Cyber → C-Level | 4h para assessment inicial |
| **Data Squad** | Dashboards de impacto em tempo real, métricas de incidente | Data → C-Level | 1h para dashboard de incidente |
| **Design Squad** | Status page UX, comunicação visual de incidentes | C-Level → Design | 24h para update de status page |
| **Brand Squad** | Impacto na marca, tom de comunicação externa | C-Level → Brand | 2h para aprovação de comunicação |
| **Copy Squad** | Textos de comunicação de crise, FAQ para CS | C-Level → Copy | 2h para entregas de crise |
| **Advisory Board** | Consulta em crises com implicação legal ou regulatória | C-Level → Advisory | 4h para orientação |
| **Traffic Squad** | Pausa de campanhas se necessário durante incidente | C-Level → Traffic | 30 min para pausa de emergência |

---

## Referências

- `workflows/incident-response/01-detection-triage.md` — Detecção e triagem inicial
- `workflows/incident-response/02-escalation-matrix.md` — Matriz de escalação
- `workflows/incident-response/03-war-room-protocol.md` — Protocolo de war room
- `workflows/incident-response/04-postmortem-process.md` — Processo de postmortem
- `workflows/incident-response/05-communication-cascade.md` — Cascata de comunicação
- `checklists/governance-risk/crisis-response-quality.md` — Checklist de qualidade de resposta a crise
- `checklists/incident-communication-quality.md` — Checklist de comunicação de incidentes
- `templates/reports/postmortem-report.md` — Template de postmortem
- `frameworks/operating-system/escalation-ladders.md` — Escadas de escalação
