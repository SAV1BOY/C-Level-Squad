# Relatório de Postmortem (Blameless)

## Propósito
Documentar incidentes significativos de forma blameless (sem culpa individual),
focando em entender causas raiz, impacto, timeline de resposta e ações preventivas,
promovendo cultura de aprendizado e melhoria contínua.

## Quando Usar
- Após qualquer incidente P0 (downtime total) ou P1 (degradação major)
- Após falhas significativas de processo (não apenas técnicas)
- Após near-misses que poderiam ter sido graves
- Para incidentes de segurança
- Dentro de 5 dias úteis após a resolução do incidente

## Agente Responsável
- **Facilitador:** CTO Agent (incidentes técnicos) ou agente da área impactada
- **Contribuidores:** Todos os envolvidos na resposta ao incidente
- **Revisor:** CEO Agent, CISO Agent (se segurança)
- **Distribuição:** Todos os agentes C-Level + equipes envolvidas

## Template

---

### POSTMORTEM — {{titulo_incidente}}

**ID do incidente:** {{id_incidente}}
**Data do incidente:** {{data_incidente}}
**Severidade:** {{P0_P1_P2}}
**Data do postmortem:** {{data_postmortem}}
**Facilitador:** {{facilitador}}
**Status:** {{rascunho_revisado_finalizado}}

---

#### 1. Resumo do Incidente

**O que aconteceu (2-3 frases):**
{{resumo_incidente}}

**Duração total:** {{duracao_total}}
**Tempo de detecção (TTD):** {{tempo_deteccao}}
**Tempo de resolução (TTR):** {{tempo_resolucao}}
**Impacto:** {{impacto_resumido}}

---

#### 2. Impacto

| Dimensão | Detalhes |
|----------|---------|
| Usuários afetados | {{usuarios_afetados}} |
| Receita perdida (estimada) | {{receita_perdida}} |
| SLA violado | {{sla_violado}} |
| Dados perdidos/comprometidos | {{dados_comprometidos}} |
| Reputação/PR | {{impacto_reputacao}} |
| Custo de resposta (horas-pessoa) | {{custo_resposta}} |

---

#### 3. Timeline Detalhado

| Hora (UTC) | Evento | Quem/O Que |
|-----------|--------|-----------|
| {{hora_1}} | {{evento_1}} | {{quem_1}} |
| {{hora_2}} | {{evento_2}} | {{quem_2}} |
| {{hora_3}} | {{evento_3}} | {{quem_3}} |
| {{hora_4}} | {{evento_4}} | {{quem_4}} |
| {{hora_5}} | {{evento_5}} | {{quem_5}} |
| {{hora_6}} | {{evento_6}} | {{quem_6}} |
| {{hora_7}} | {{evento_7}} | {{quem_7}} |
| {{hora_8}} | {{evento_8}} | {{quem_8}} |

---

#### 4. Análise de Causa Raiz

**Causa raiz primária:**
{{causa_raiz_primaria}}

**Causas contribuintes:**
1. {{causa_contribuinte_1}}
2. {{causa_contribuinte_2}}
3. {{causa_contribuinte_3}}

**Análise dos 5 Porquês:**
1. Por que o incidente ocorreu? → {{porque_1}}
2. Por que isso foi possível? → {{porque_2}}
3. Por que não detectamos antes? → {{porque_3}}
4. Por que a resposta demorou? → {{porque_4}}
5. Por que não tínhamos prevenção? → {{porque_5}}

---

#### 5. O Que Funcionou Bem

- {{funcionou_1}}
- {{funcionou_2}}
- {{funcionou_3}}

---

#### 6. O Que Pode Melhorar

- {{melhorar_1}}
- {{melhorar_2}}
- {{melhorar_3}}

---

#### 7. Onde Tivemos Sorte

- {{sorte_1}}
- {{sorte_2}}

*(Fatores que limitaram o impacto mas não estavam sob nosso controle)*

---

#### 8. Action Items

| # | Ação | Tipo | Prioridade | Owner | Prazo | Status |
|---|------|------|-----------|-------|-------|--------|
| 1 | {{acao_1}} | {{tipo_1}} | {{prior_1}} | {{owner_1}} | {{prazo_1}} | {{status_1}} |
| 2 | {{acao_2}} | {{tipo_2}} | {{prior_2}} | {{owner_2}} | {{prazo_2}} | {{status_2}} |
| 3 | {{acao_3}} | {{tipo_3}} | {{prior_3}} | {{owner_3}} | {{prazo_3}} | {{status_3}} |
| 4 | {{acao_4}} | {{tipo_4}} | {{prior_4}} | {{owner_4}} | {{prazo_4}} | {{status_4}} |
| 5 | {{acao_5}} | {{tipo_5}} | {{prior_5}} | {{owner_5}} | {{prazo_5}} | {{status_5}} |

**Tipos:** Preventivo (evita recorrência) | Detectivo (detecta mais rápido) | Mitigador (reduz impacto)

---

#### 9. Métricas de Resposta

| Métrica | Valor Neste Incidente | Target | Comentário |
|---------|----------------------|--------|-----------|
| Time to Detect (TTD) | {{ttd}} | {{target_ttd}} | {{coment_ttd}} |
| Time to Acknowledge (TTA) | {{tta}} | {{target_tta}} | {{coment_tta}} |
| Time to Mitigate (TTM) | {{ttm}} | {{target_ttm}} | {{coment_ttm}} |
| Time to Resolve (TTR) | {{ttr}} | {{target_ttr}} | {{coment_ttr}} |

---

#### 10. Prevenção de Recorrência

**Este incidente poderia ter sido prevenido?** {{sim_nao}}
**Se sim, como?** {{como_prevenir}}
**Custo de implementar a prevenção:** {{custo_prevencao}}
**Custo de recorrência (se não prevenir):** {{custo_recorrencia}}

---

## Instruções de Preenchimento

1. **Blameless:** NUNCA atribua culpa a indivíduos. O sistema falhou, não a pessoa.
   Use "o deploy foi executado" e não "fulano fez o deploy errado".
2. **Timeline:** Seja preciso com horários. O timeline é a base da análise.
3. **5 Porquês:** Vá além da causa superficial. A causa raiz raramente é óbvia.
4. **"Onde tivemos sorte":** Esta seção revela fragilidades ocultas que precisam de atenção.
5. **Action Items:** Cada um deve ser específico, com owner e prazo. "Melhorar monitoramento"
   é fraco. "Adicionar alerta para latência > 500ms no serviço X até data Y" é forte.
6. **Prazo:** Postmortem deve ser completado em até 5 dias úteis após resolução.

## Exemplo Preenchido

---

### POSTMORTEM — Downtime do sistema de pagamentos (47 minutos)

**ID:** INC-347 | **Severidade:** P0 | **Duração:** 47 min

**Resumo:** Deploy da versão 2.14.3 do payment service introduziu breaking change no schema
do banco de dados, causando 100% de falha nas transações de pagamento por 47 minutos.
Detectado pelo alerta de error rate em 4 minutos. Resolução via rollback do deploy.

**Causa raiz:** Migration script não foi testada contra dados reais. O campo `currency_code`
mudou de VARCHAR(3) para ENUM, mas 2.3% dos registros tinham valores fora do ENUM.

**Action Items:**
| # | Ação | Tipo | Owner | Prazo |
|---|------|------|-------|-------|
| 1 | Adicionar integration test com snapshot de prod | Preventivo | Tech Lead | 2 semanas |
| 2 | Implementar canary deployment para payment service | Preventivo | SRE Lead | 4 semanas |
| 3 | Criar runbook de rollback do payment service | Mitigador | On-call | 1 semana |

---

## Checklist de Qualidade

- [ ] O postmortem é genuinamente blameless (sem nomes culpados)
- [ ] Timeline é preciso e completo
- [ ] Causa raiz vai além da superfície (5 Porquês aplicados)
- [ ] Impacto está quantificado (usuários, receita, SLA)
- [ ] "O que funcionou" e "onde tivemos sorte" estão documentados
- [ ] Action items são específicos com owner e prazo
- [ ] Action items incluem preventivos, detectivos e mitigadores
- [ ] Métricas de resposta (TTD, TTR) estão documentadas
- [ ] O postmortem foi completado em até 5 dias úteis
- [ ] O documento foi compartilhado amplamente (não escondido)
