# Architecture Decision Record (ADR)

## Propósito
Registrar decisões arquiteturais significativas com contexto, alternativas consideradas,
decisão tomada e consequências esperadas, criando um histórico navegável que explica
por que o sistema é como é.

## Quando Usar
- Para qualquer decisão arquitetural que impacte múltiplos times ou sistemas
- Quando há trade-offs significativos entre alternativas técnicas
- Para decisões que seriam difíceis ou caras de reverter
- Quando a decisão precisa ser compreendida por futuros membros da equipe

## Agente Responsável
- **Autor primário:** CTO Agent
- **Contribuidores:** Tech Leads, Staff Engineers
- **Revisor:** CEO Agent (impacto em negócio), CISO Agent (segurança)
- **Aprovador:** CTO Agent

## Template

---

### ADR-{{numero_sequencial}}: {{titulo_decisao}}

**Data:** {{data_decisao}}
**Status:** {{proposto_aceito_depreciado_substituido}}
**Decisores:** {{lista_decisores}}
**Substitui:** {{adr_anterior}} *(se aplicável)*

---

#### 1. Contexto

{{descricao_contexto_tecnico}}

**Drivers técnicos:**
- {{driver_tecnico_1}}
- {{driver_tecnico_2}}
- {{driver_tecnico_3}}

**Drivers de negócio:**
- {{driver_negocio_1}}
- {{driver_negocio_2}}

**Restrições:**
- {{restricao_1}}
- {{restricao_2}}
- {{restricao_3}}

---

#### 2. Opções Consideradas

**Opção 1: {{nome_opcao_1}}**
- Descrição: {{descricao_opcao_1}}
- Prós: {{pros_1}}
- Contras: {{contras_1}}
- Estimativa de esforço: {{esforco_1}}

**Opção 2: {{nome_opcao_2}}**
- Descrição: {{descricao_opcao_2}}
- Prós: {{pros_2}}
- Contras: {{contras_2}}
- Estimativa de esforço: {{esforco_2}}

**Opção 3: {{nome_opcao_3}}**
- Descrição: {{descricao_opcao_3}}
- Prós: {{pros_3}}
- Contras: {{contras_3}}
- Estimativa de esforço: {{esforco_3}}

---

#### 3. Decisão

**Escolhemos:** {{opcao_escolhida}}

**Justificativa:**
{{justificativa_detalhada}}

**Trade-offs aceitos:**
- {{tradeoff_aceito_1}}
- {{tradeoff_aceito_2}}

---

#### 4. Consequências

**Positivas:**
- {{consequencia_positiva_1}}
- {{consequencia_positiva_2}}
- {{consequencia_positiva_3}}

**Negativas:**
- {{consequencia_negativa_1}}
- {{consequencia_negativa_2}}

**Riscos:**
| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| {{risco_1}} | {{prob_1}} | {{imp_1}} | {{mit_1}} |
| {{risco_2}} | {{prob_2}} | {{imp_2}} | {{mit_2}} |

---

#### 5. Impacto nos Sistemas

| Sistema/Serviço | Tipo de Impacto | Esforço de Adaptação | Owner |
|----------------|----------------|---------------------|-------|
| {{sistema_1}} | {{impacto_1}} | {{esforco_adapt_1}} | {{owner_1}} |
| {{sistema_2}} | {{impacto_2}} | {{esforco_adapt_2}} | {{owner_2}} |
| {{sistema_3}} | {{impacto_3}} | {{esforco_adapt_3}} | {{owner_3}} |

---

#### 6. Plano de Implementação

| Fase | Ação | Timeline | Owner | Dependência |
|------|------|----------|-------|-------------|
| 1 | {{acao_impl_1}} | {{timeline_1}} | {{owner_impl_1}} | {{dep_1}} |
| 2 | {{acao_impl_2}} | {{timeline_2}} | {{owner_impl_2}} | {{dep_2}} |
| 3 | {{acao_impl_3}} | {{timeline_3}} | {{owner_impl_3}} | {{dep_3}} |
| 4 | {{acao_impl_4}} | {{timeline_4}} | {{owner_impl_4}} | {{dep_4}} |

---

#### 7. Métricas de Validação

| Métrica | Antes | Meta (após implementação) | Como Medir |
|---------|-------|--------------------------|-----------|
| {{metrica_1}} | {{antes_1}} | {{meta_1}} | {{como_medir_1}} |
| {{metrica_2}} | {{antes_2}} | {{meta_2}} | {{como_medir_2}} |
| {{metrica_3}} | {{antes_3}} | {{meta_3}} | {{como_medir_3}} |

---

#### 8. Revisão Futura

**Data de revisão:** {{data_revisao}}
**Condições para revisitar esta decisão:**
- {{condicao_revisao_1}}
- {{condicao_revisao_2}}

---

## Instruções de Preenchimento

1. **Numeração:** Use numeração sequencial (ADR-001, ADR-002). Nunca reutilize números.
2. **Status:** Proposto → Aceito → (opcionalmente) Depreciado ou Substituído.
3. **Contexto:** Descreva como se estivesse explicando para alguém que entrou na empresa amanhã.
4. **Opções:** Sempre liste pelo menos 2 alternativas. Inclua "não fazer nada" quando relevante.
5. **Consequências:** Seja honesto sobre as negativas. ADRs parciais geram decisões ruins no futuro.
6. **Imutabilidade:** ADRs aceitos não devem ser editados. Se a decisão mudar, crie um novo ADR que substitui.

## Exemplo Preenchido

---

### ADR-017: Migração de monólito para microserviços (domínio de pagamentos)

**Status:** Aceito
**Decisores:** CTO Agent, Head of Platform, Staff Engineer

#### 1. Contexto
O módulo de pagamentos no monólito é o bottleneck de deploy — 40% dos rollbacks são causados
por mudanças neste módulo. O time de pagamentos precisa de autonomia para deploy independente
e o módulo tem requisitos de compliance (PCI-DSS) que adicionam overhead a todo o monólito.

#### 3. Decisão
**Escolhemos:** Strangler Fig pattern para extrair o domínio de pagamentos como microserviço.
Migração gradual mantendo backward compatibility durante 6 meses de transição.

**Trade-offs aceitos:**
- Complexidade operacional adicional (mais um serviço para monitorar)
- 3 meses de esforço de engenharia dedicado

---

## Checklist de Qualidade

- [ ] Contexto é compreensível para alguém novo na equipe
- [ ] Pelo menos 2 alternativas foram documentadas com prós/contras
- [ ] Decisão está claramente indicada com justificativa
- [ ] Trade-offs aceitos estão explícitos
- [ ] Consequências positivas E negativas documentadas
- [ ] Impacto em outros sistemas mapeado
- [ ] Plano de implementação com owners e timeline
- [ ] Métricas de validação definidas
- [ ] Data de revisão futura agendada
- [ ] ADR numerado e indexado no repositório de ADRs
