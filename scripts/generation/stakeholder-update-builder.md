# Stakeholder Update Builder

> Script para construção e distribuição de updates a stakeholders.

---

## Objetivo

Gerar comunicações regulares e ad hoc para diferentes grupos de stakeholders,
adaptando mensagem, nível de detalhe e formato ao perfil de cada audiência.
Este script garante consistência, relevância e timing adequado.

---

## Audience Segmentation — Segmentação de Audiência

### Tier 1 — Governance
- **Quem**: Board members, advisory board, investidores
- **Frequência**: Mensal (escrita) + Trimestral (presencial)
- **Nível de detalhe**: Estratégico, financeiro, high-level
- **Tom**: Formal, transparente, orientado a resultados
- **Formato**: PDF estruturado, máximo 5 páginas

### Tier 2 — Leadership
- **Quem**: C-Level, VPs, Directors
- **Frequência**: Semanal
- **Nível de detalhe**: Táctico e operacional
- **Tom**: Directo, action-oriented
- **Formato**: Email estruturado ou dashboard link

### Tier 3 — Teams
- **Quem**: Squad leads, team members, ICs
- **Frequência**: Semanal ou bi-semanal
- **Nível de detalhe**: Operacional, específico ao contexto
- **Tom**: Colaborativo, transparente, motivacional
- **Formato**: Slack/Teams post, wiki update

### Tier 4 — External
- **Quem**: Clientes, parceiros, fornecedores
- **Frequência**: Conforme necessidade ou mensal
- **Nível de detalhe**: Curado, orientado ao valor para eles
- **Tom**: Profissional, positivo, orientado ao futuro
- **Formato**: Email, newsletter, portal update

### Tier 5 — Public
- **Quem**: Mercado, media, comunidade
- **Frequência**: Conforme eventos ou trimestral
- **Nível de detalhe**: Público, não confidencial
- **Tom**: Inspirador, factual, brand-aligned
- **Formato**: Blog post, press release, social media

---

## Message Tailoring — Adaptação da Mensagem

### Framework ADAPT
Para cada update, aplicar o framework:
- **A**udiência: quem vai ler? O que lhes interessa?
- **D**ados: que informação é relevante para esta audiência?
- **A**cção: que acção esperamos do leitor?
- **P**rioridade: qual a ordem de importância dos tópicos?
- **T**om: qual o registo adequado para este grupo?

### Regras de Filtragem de Conteúdo
| Tipo de Info | Tier 1 | Tier 2 | Tier 3 | Tier 4 | Tier 5 |
|-------------|--------|--------|--------|--------|--------|
| Financial details | Sim | Sim | Resumo | Não | Público |
| Strategy changes | Sim | Sim | Impacto | Relevante | PR |
| Operational metrics | Resumo | Sim | Sim | SLA | Não |
| People changes | Senior | Sim | Equipa | Relevante | Senior |
| Risk updates | Sim | Sim | Impacto | Relevante | Não |
| Product roadmap | High-level | Detalhe | Detalhe | Relevante | Public |
| Incidents | Major | Todos | Equipa | Impactados | Major |

### Templates por Tier

#### Tier 1 — Investor Update Template
```
SUBJECT: [Company] — [Month] Update

1. Highlights do Período
   - [3-5 bullet points principais]

2. Financial Snapshot
   - Revenue: [actual] vs [target] ([variação]%)
   - Burn rate: [valor] | Runway: [meses]
   - Key financial metrics

3. Strategic Progress
   - [Iniciativa 1]: [status em 1 linha]
   - [Iniciativa 2]: [status em 1 linha]

4. Key Decisions & Changes
   - [Decisões tomadas com contexto]

5. Asks & Needs
   - [O que precisamos do board/investidores]

6. Outlook
   - [Perspectiva para próximo período]
```

#### Tier 2 — Leadership Update Template
```
SUBJECT: Weekly Leadership Update — W[número]

Estado Geral: [emoji status] [1 frase]

Wins da Semana:
- [Win 1]
- [Win 2]

Atenção Requerida:
- [Item 1 — owner — deadline]
- [Item 2 — owner — deadline]

Métricas-Chave:
- [KPI 1]: [valor] [trend]
- [KPI 2]: [valor] [trend]

Decisões Tomadas:
- [Decisão 1]

Próxima Semana:
- [Prioridade 1]
- [Prioridade 2]
```

#### Tier 3 — Team Update Template
```
Hey equipa,

Resumo da semana:
[2-3 parágrafos com contexto e highlights]

O que correu bem:
- [Item 1]
- [Item 2]

O que podemos melhorar:
- [Item 1]

Action items:
- [Owner]: [Acção] — [Prazo]

Obrigado a [reconhecimento específico].
```

---

## Distribution — Processo de Distribuição

### Workflow de Criação
1. **Trigger**: calendário automático ou evento específico
2. **Data pull**: recolher dados relevantes das fontes definidas
3. **Draft**: gerar primeiro draft usando template apropriado
4. **Review**: revisão pelo owner da comunicação
5. **Approval**: aprovação conforme tier (Tier 1/4/5 requerem CEO sign-off)
6. **Send**: distribuição via canal definido
7. **Track**: confirmar entrega e engagement

### Canais de Distribuição
| Tier | Canal Primário | Canal Secundário | Arquivo |
|------|---------------|-----------------|---------|
| Tier 1 | Email personalizado | Portal investidor | Board pack |
| Tier 2 | Email / Slack | Dashboard | Wiki |
| Tier 3 | Slack / Teams | Wiki | Confluence |
| Tier 4 | Email | Portal cliente | CRM |
| Tier 5 | Blog / PR wire | Social media | Website |

### Timing
- **Tier 1**: enviar entre terça e quinta, manhã (9-11h)
- **Tier 2**: segunda-feira de manhã (start of week)
- **Tier 3**: sexta-feira tarde (wrap da semana) ou segunda manhã
- **Tier 4**: conforme SLA do contrato ou relação
- **Tier 5**: conforme calendário editorial ou evento

---

## Quality Assurance

### Checklist Pré-Envio
- [ ] Audiência correctamente identificada
- [ ] Dados verificados e actualizados
- [ ] Tom adequado ao tier
- [ ] Nenhuma informação confidencial em tier inadequado
- [ ] Links funcionam
- [ ] Formatação correcta no canal de destino
- [ ] Aprovações obtidas (se necessárias)
- [ ] Spell check completo

### Feedback Loop
- Recolher open rates e engagement metrics
- Solicitar feedback directo trimestralmente
- Ajustar formato e conteúdo baseado em feedback
- Manter log de updates enviados para auditoria

---

## Comunicações de Crise

Em situação de crise, o processo normal é substituído por:
1. **Activação**: identificação de evento que requer comunicação urgente
2. **War room**: reunião imediata do C-Level Squad
3. **Messaging**: definição de mensagem central (1 frase)
4. **Cascade**: comunicação simultânea a todos os tiers relevantes
5. **Follow-up**: updates regulares até resolução
6. **Post-mortem**: análise e comunicação de lições aprendidas

---

## Notas Técnicas

- Templates guardados em `templates/stakeholder-updates/`
- Automação de data pull via APIs dos sistemas fonte
- Distribuição pode ser automatizada com workflows pré-configurados
- Arquivo de todos os updates para compliance e auditoria
- Métricas de engagement monitorizadas via analytics integrado
