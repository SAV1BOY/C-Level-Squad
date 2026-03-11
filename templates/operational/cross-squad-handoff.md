# Template de Handoff Cross-Squad

## Propósito
Padronizar a transferência de responsabilidade, contexto e artefatos entre squads
ou agentes do C-Level, garantindo continuidade, clareza sobre o que está sendo
transferido e evitando perda de informação durante transições.

## Quando Usar
- Quando uma iniciativa muda de owner entre squads ou agentes
- Na transição de fases (ex.: design → implementação, piloto → produção)
- Quando um agente precisa delegar responsabilidade temporariamente
- Para transições de liderança em iniciativas

## Agente Responsável
- **Autor primário:** Agente/squad que está entregando (remetente)
- **Receptor:** Agente/squad que está recebendo
- **Facilitador:** Chief of Staff Agent (CoS)
- **Validador:** Ambas as partes devem concordar com o handoff

## Template

---

### HANDOFF CROSS-SQUAD

**ID do handoff:** {{id_handoff}}
**Data:** {{data_handoff}}
**Iniciativa/Projeto:** {{nome_iniciativa}}

**De (remetente):**
| Campo | Valor |
|-------|-------|
| Agente/Squad | {{remetente}} |
| Contato | {{contato_remetente}} |

**Para (receptor):**
| Campo | Valor |
|-------|-------|
| Agente/Squad | {{receptor}} |
| Contato | {{contato_receptor}} |

**Facilitador:** {{facilitador}}
**Tipo de handoff:** {{completo_parcial_temporario}}

---

#### 1. O Que Está Sendo Transferido

**Escopo do handoff:**
{{descricao_escopo_handoff}}

**O que ESTÁ incluído:**
- {{incluido_1}}
- {{incluido_2}}
- {{incluido_3}}
- {{incluido_4}}

**O que NÃO está incluído (permanece com remetente):**
- {{nao_incluido_1}}
- {{nao_incluido_2}}

---

#### 2. Contexto e Estado Atual

**Resumo do projeto/iniciativa:**
{{resumo_contexto}}

**Estado atual:**
| Aspecto | Status | Comentário |
|---------|--------|-----------|
| Progresso geral | {{progresso}} | {{coment_progresso}} |
| Budget consumido | {{budget_consumido}} / {{budget_total}} | {{coment_budget}} |
| Timeline | {{status_timeline}} | {{coment_timeline}} |
| Riscos ativos | {{qtd_riscos}} | {{coment_riscos}} |
| Decisões pendentes | {{qtd_decisoes}} | {{coment_decisoes}} |

---

#### 3. Histórico Relevante

**Decisões já tomadas:**
| Decisão | Data | Racional | Referência |
|---------|------|----------|-----------|
| {{decisao_1}} | {{data_d1}} | {{racional_1}} | {{ref_1}} |
| {{decisao_2}} | {{data_d2}} | {{racional_2}} | {{ref_2}} |
| {{decisao_3}} | {{data_d3}} | {{racional_3}} | {{ref_3}} |

**Lições aprendidas até aqui:**
- {{licao_1}}
- {{licao_2}}
- {{licao_3}}

**O que tentamos e não funcionou:**
- {{nao_funcionou_1}}
- {{nao_funcionou_2}}

---

#### 4. Artefatos e Documentação

| # | Artefato | Tipo | Localização | Status |
|---|---------|------|------------|--------|
| 1 | {{artefato_1}} | {{tipo_art_1}} | {{local_1}} | {{status_art_1}} |
| 2 | {{artefato_2}} | {{tipo_art_2}} | {{local_2}} | {{status_art_2}} |
| 3 | {{artefato_3}} | {{tipo_art_3}} | {{local_3}} | {{status_art_3}} |
| 4 | {{artefato_4}} | {{tipo_art_4}} | {{local_4}} | {{status_art_4}} |
| 5 | {{artefato_5}} | {{tipo_art_5}} | {{local_5}} | {{status_art_5}} |

---

#### 5. Stakeholders e Relacionamentos

| Stakeholder | Papel | Nível de Envolvimento | Contexto Relevante |
|------------|-------|---------------------|-------------------|
| {{stakeholder_1}} | {{papel_1}} | {{envolvimento_1}} | {{contexto_sh_1}} |
| {{stakeholder_2}} | {{papel_2}} | {{envolvimento_2}} | {{contexto_sh_2}} |
| {{stakeholder_3}} | {{papel_3}} | {{envolvimento_3}} | {{contexto_sh_3}} |

---

#### 6. Riscos e Pendências

**Riscos ativos:**
| Risco | Probabilidade | Impacto | Mitigação em Curso |
|-------|--------------|---------|-------------------|
| {{risco_1}} | {{prob_1}} | {{imp_1}} | {{mit_1}} |
| {{risco_2}} | {{prob_2}} | {{imp_2}} | {{mit_2}} |

**Pendências/Action items abertos:**
| # | Pendência | Prazo | Prioridade | Contexto |
|---|----------|-------|-----------|----------|
| 1 | {{pendencia_1}} | {{prazo_1}} | {{prior_1}} | {{ctx_1}} |
| 2 | {{pendencia_2}} | {{prazo_2}} | {{prior_2}} | {{ctx_2}} |
| 3 | {{pendencia_3}} | {{prazo_3}} | {{prior_3}} | {{ctx_3}} |

---

#### 7. Expectativas e Próximos Passos

**O que o receptor precisa fazer primeiro:**
1. {{primeiro_passo_1}}
2. {{primeiro_passo_2}}
3. {{primeiro_passo_3}}

**Próximos marcos esperados:**
| Marco | Data | Critério de Sucesso |
|-------|------|---------------------|
| {{marco_1}} | {{data_marco_1}} | {{criterio_1}} |
| {{marco_2}} | {{data_marco_2}} | {{criterio_2}} |

**Disponibilidade do remetente pós-handoff:**
{{disponibilidade_remetente}}

---

#### 8. Aceite do Handoff

**Remetente confirma:**
- [ ] Toda a documentação relevante foi transferida
- [ ] Contexto foi explicado em sessão de transferência
- [ ] Acessos necessários foram compartilhados
- [ ] Stakeholders foram informados da mudança

**Receptor confirma:**
- [ ] Entendi o escopo e estado atual
- [ ] Tenho acesso a todos os artefatos necessários
- [ ] Conheço os stakeholders relevantes
- [ ] Entendi os riscos e pendências
- [ ] Sei quem contactar para dúvidas

**Assinaturas:**
- Remetente: {{assinatura_remetente}} — Data: {{data_aceite_rem}}
- Receptor: {{assinatura_receptor}} — Data: {{data_aceite_rec}}
- Facilitador: {{assinatura_facilitador}} — Data: {{data_aceite_fac}}

---

## Instruções de Preenchimento

1. **Sessão de transferência:** Realize uma reunião de handoff (30-60 min) além deste documento.
2. **Artefatos:** Garanta que todos são acessíveis ao receptor ANTES do handoff.
3. **Histórico:** Inclua decisões e falhas passadas. O receptor precisa do contexto completo.
4. **Stakeholders:** Faça introduções quando necessário. Não basta listar nomes.
5. **Disponibilidade:** O remetente deve estar disponível por pelo menos 2 semanas pós-handoff.
6. **Aceite:** Ambas as partes devem confirmar. Handoff unilateral gera perda de informação.

## Exemplo Preenchido

---

### HANDOFF — Projeto de Migração de CRM

**De:** CTO Agent (fase de avaliação técnica)
**Para:** CRO Agent (fase de implementação e adoção)

**Estado:** Avaliação técnica concluída. Salesforce selecionado. Contrato assinado.
Fase de implementação requer liderança de vendas para customização de workflows.

**Primeiro passo do receptor:**
1. Revisar os requisitos de workflow documentados no brief técnico
2. Agendar kickoff com o implementation partner (Accenture)
3. Definir o change management plan para o time de vendas

---

## Checklist de Qualidade

- [ ] Escopo do handoff é claro (o que está e o que não está incluído)
- [ ] Estado atual está documentado com dados reais
- [ ] Decisões passadas estão registradas com racional
- [ ] Todos os artefatos são acessíveis ao receptor
- [ ] Stakeholders foram apresentados (não apenas listados)
- [ ] Riscos e pendências estão transparentes
- [ ] Sessão de transferência foi realizada
- [ ] Primeiros passos do receptor estão definidos
- [ ] Remetente estará disponível por 2+ semanas pós-handoff
- [ ] Aceite formal de ambas as partes está documentado
