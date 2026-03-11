# Workflow: Processo de Postmortem

## Objetivo

Conduzir análises estruturadas pós-incidente para identificar causas raiz, documentar lições aprendidas e gerar ações corretivas que previnam recorrência, mantendo uma cultura blameless que incentive transparência e melhoria contínua.

## Trigger

- Encerramento de qualquer incidente P1 ou P2
- Incidentes P3 que resultaram em impacto inesperado
- Incidentes recorrentes (mesmo serviço, 3+ ocorrências em 30 dias)
- Solicitação de postmortem pela liderança de engenharia

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Incident Commander original | **Responsible** — Facilita sessão e redige documento |
| Engenheiros envolvidos | **Responsible** — Contribuem com análise técnica |
| SRE Lead | **Accountable** — Garante qualidade e follow-up de ações |
| VP de Engenharia | **Consulted** — Aprova ações corretivas com impacto em roadmap |
| Product Manager | **Informed** — Visibilidade sobre impacto em produto |

## Princípios Fundamentais

1. **Blameless**: Foco em processos e sistemas, nunca em indivíduos
2. **Honestidade**: Documentar o que realmente aconteceu, sem suavizar
3. **Ações concretas**: Todo postmortem deve gerar pelo menos 1 ação mensurável
4. **Compartilhamento**: Postmortems são públicos internamente por padrão
5. **Follow-up**: Ações sem dono e prazo não existem

## Etapas do Workflow

### Etapa 1: Preparação (D+1 a D+3 após incidente)
- IC revisa timeline documentada durante o war room
- Coleta logs, métricas e evidências adicionais
- Prepara rascunho do documento de postmortem
- Agenda sessão de postmortem com todos os envolvidos
- Distribui rascunho para revisão prévia dos participantes
- **SLA: Sessão agendada em até 72h após resolução**

### Etapa 2: Sessão de Postmortem (60-90 minutos)
- **Revisão da timeline** (15 min): Percorrer cronologia dos eventos
- **Análise de causa raiz** (30 min): Técnica dos 5 Porquês ou Diagrama de Ishikawa
- **Fatores contribuintes** (15 min): Identificar condições que permitiram o incidente
- **O que funcionou bem** (10 min): Reconhecer acertos na resposta
- **Ações corretivas** (20 min): Definir ações com dono, prazo e prioridade

### Etapa 3: Análise de Causa Raiz (5 Porquês)
Exemplo de estrutura:
- Por quê 1: Por que o sistema ficou indisponível?
- Por quê 2: Por que o deploy causou falha?
- Por quê 3: Por que o teste não detectou o problema?
- Por quê 4: Por que o cenário não estava coberto?
- Por quê 5: Por que o processo de review não exigiu esse teste?
- **Causa raiz**: Lacuna no processo de code review para cenários de edge case

### Etapa 4: Definição de Ações Corretivas
Cada ação deve conter:
- **Descrição clara** da ação a ser tomada
- **Tipo**: Prevenção (evitar recorrência) / Detecção (detectar mais rápido) / Mitigação (reduzir impacto)
- **Dono**: Pessoa responsável pela execução
- **Prazo**: Data limite para conclusão
- **Prioridade**: P1 (esta sprint) / P2 (próxima sprint) / P3 (quarter)
- **Ticket**: Link para o ticket criado no backlog

### Etapa 5: Documentação Final
- IC finaliza documento de postmortem no template padrão
- Revisão por SRE Lead para garantir completude e qualidade
- Publicação no repositório interno de postmortems
- Comunicação para toda a engenharia (email ou Slack)
- **SLA: Documento publicado em até 5 dias úteis após incidente**

### Etapa 6: Follow-up de Ações
- Ações de P1 revisadas na próxima daily/standup do time
- Review semanal pelo SRE Lead de todas as ações em aberto
- Report mensal de progresso para VP de Engenharia
- Ações não concluídas no prazo são escaladas automaticamente
- **Meta: 90% das ações concluídas no prazo definido**

## Template do Documento de Postmortem

```
# Postmortem: [Título do Incidente]
## Metadata
- Data do incidente:
- Duração total:
- Severidade:
- Incident Commander:
- Serviços afetados:
- Impacto: (clientes, receita, SLO)

## Resumo Executivo
(2-3 parágrafos descrevendo o ocorrido e impacto)

## Timeline Detalhada
(Cronologia com timestamps)

## Análise de Causa Raiz
(5 Porquês ou método escolhido)

## Fatores Contribuintes
(Condições que permitiram o incidente)

## O que Funcionou Bem
(Reconhecimento de acertos)

## Ações Corretivas
| # | Ação | Tipo | Dono | Prazo | Ticket |

## Lições Aprendidas
(Insights para compartilhar com toda a organização)
```

## Outputs / Entregáveis

- Documento de postmortem publicado e acessível
- Ações corretivas criadas como tickets no backlog
- Comunicação enviada para engenharia
- Métricas de impacto atualizadas no dashboard de incidentes
- Runbooks atualizados se aplicável

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Postmortems publicados no prazo | ≥ 95% | Mensal |
| Ações corretivas concluídas no prazo | ≥ 90% | Mensal |
| Recorrência de incidentes com mesma causa raiz | < 5% | Trimestral |
| Participação na sessão de postmortem | 100% dos envolvidos | Por incidente |
| Qualidade do documento (review pelo SRE Lead) | ≥ 4/5 | Por incidente |

## Integração com Outros Workflows

- **03-war-room-protocol.md**: Timeline do war room alimenta o postmortem
- **01-detection-triage.md**: Melhorias em detecção são ações comuns de postmortem
- **Tech Review / 04-implementation-gates.md**: Gates podem ser reforçados baseado em postmortems
- **OKR Cycle / 03-weekly-check-in.md**: Ações de postmortem rastreadas no check-in semanal
