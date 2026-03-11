# Template: Request for Comments (RFC)

## Propósito
Este template estrutura propostas técnicas que requerem input e aprovação de múltiplos stakeholders antes da implementação. RFCs são usadas para mudanças de grande escopo que impactam múltiplos times ou sistemas.

## Instruções de Uso
1. Autor escreve o RFC e compartilha com reviewers
2. Período de comentários: mínimo 5 dias úteis
3. Após endereçar comentários, RFC vai para aprovação
4. Implementação só começa após status "Aprovado"
5. RFC pode ser revisada se surgirem novos dados durante implementação

---

## RFC-[NNN]: [Título Descritivo]

### Metadados

| Campo | Valor |
|-------|-------|
| **Status** | [Rascunho / Em Revisão / Aprovado / Rejeitado / Implementado / Abandonado] |
| **Autor(es)** | [Nome(s) — Cargo(s)] |
| **Reviewers Obrigatórios** | [Nome(s) — por que são necessários] |
| **Data de Criação** | [DD/MM/AAAA] |
| **Deadline para Comentários** | [DD/MM/AAAA] |
| **Data de Decisão** | [DD/MM/AAAA] |
| **Impacto** | [Crítico / Alto / Médio] |
| **Esforço Estimado** | [N sprints / N pessoa-meses] |

---

### 1. Resumo

[2-3 parágrafos explicando O QUE está sendo proposto e POR QUE. Um leitor deve entender a essência da proposta apenas lendo esta seção.]

---

### 2. Motivação

#### 2.1 Problema Atual
[Descrever o problema em detalhes, com dados quando possível]
- **Impacto no negócio:** [Como o problema afeta métricas de negócio]
- **Impacto técnico:** [Dívida técnica, performance, confiabilidade]
- **Impacto no time:** [Produtividade, frustração, riscos]

#### 2.2 Por que Agora?
[O que mudou que torna esta proposta urgente ou relevante agora]

#### 2.3 O que Acontece se Não Fizermos Nada?
[Projeção do cenário de inação]

---

### 3. Proposta Detalhada

#### 3.1 Visão Geral da Solução
[Descrição de alto nível da solução proposta]

#### 3.2 Arquitetura / Design

```
[Diagrama ASCII ou referência a diagrama externo]

┌──────────┐     ┌──────────┐     ┌──────────┐
│ Service A │────▶│ Service B │────▶│ Service C │
└──────────┘     └──────────┘     └──────────┘
      │                                  │
      ▼                                  ▼
┌──────────┐                      ┌──────────┐
│  DB Write │                      │  DB Read  │
└──────────┘                      └──────────┘
```

#### 3.3 Componentes Envolvidos
| Componente | Mudança Necessária | Complexidade | Owner |
|-----------|-------------------|-------------|-------|
| [Componente 1] | [Descrição da mudança] | [Alta/Média/Baixa] | [Time] |
| [Componente 2] | [Descrição da mudança] | [Alta/Média/Baixa] | [Time] |
| [Componente 3] | [Descrição da mudança] | [Alta/Média/Baixa] | [Time] |

#### 3.4 Fluxo de Dados
[Descrever como os dados fluem pela solução proposta]

#### 3.5 APIs / Interfaces
```
[Definição de APIs novas ou alteradas — endpoints, payloads, contratos]
```

#### 3.6 Modelo de Dados
[Alterações em schema, novos modelos, migrações necessárias]

---

### 4. Alternativas Consideradas

#### Alternativa A: [Nome]
- **Descrição:** [Como funcionaria]
- **Prós:** [Vantagens]
- **Contras:** [Desvantagens]
- **Por que não:** [Razão principal para descartar]

#### Alternativa B: [Nome]
- **Descrição:** [Como funcionaria]
- **Prós:** [Vantagens]
- **Contras:** [Desvantagens]
- **Por que não:** [Razão principal para descartar]

---

### 5. Plano de Implementação

#### 5.1 Fases

| Fase | Escopo | Duração | Entregável | Critério de Sucesso |
|------|--------|---------|-----------|-------------------|
| 1 — Fundação | [Escopo] | [X sprints] | [Entregável] | [Critério] |
| 2 — Core | [Escopo] | [X sprints] | [Entregável] | [Critério] |
| 3 — Migração | [Escopo] | [X sprints] | [Entregável] | [Critério] |
| 4 — Cleanup | [Escopo] | [X sprints] | [Entregável] | [Critério] |

#### 5.2 Dependências
- [Dependência 1 — time/sistema e impacto no cronograma]
- [Dependência 2 — time/sistema e impacto no cronograma]

#### 5.3 Feature Flags / Rollout
- **Estratégia de rollout:** [Big bang / Canary / % gradual / Por região]
- **Feature flags:** [Listar flags necessárias]
- **Rollback plan:** [Como reverter se algo der errado]

---

### 6. Impacto Operacional

#### 6.1 Performance
- **Impacto esperado em latência:** [+/- Xms no p50/p99]
- **Impacto em throughput:** [+/- X req/s]
- **Impacto em armazenamento:** [+/- X GB/TB]

#### 6.2 Observabilidade
- **Métricas novas:** [Quais métricas precisam ser criadas]
- **Alertas novos:** [Quais alertas precisam ser configurados]
- **Dashboards:** [Quais dashboards precisam ser atualizados/criados]

#### 6.3 Segurança
- [Consideração de segurança 1]
- [Consideração de segurança 2]
- **Revisão de segurança necessária:** [Sim/Não]

#### 6.4 Custos de Infraestrutura
| Item | Custo Atual | Custo Estimado | Variação |
|------|-----------|---------------|----------|
| Compute | [R$/mês] | [R$/mês] | [+/- X%] |
| Storage | [R$/mês] | [R$/mês] | [+/- X%] |
| Network | [R$/mês] | [R$/mês] | [+/- X%] |
| **Total** | **[R$/mês]** | **[R$/mês]** | **[+/- X%]** |

---

### 7. Riscos

| Risco | Probabilidade | Impacto | Mitigação |
|-------|-------------|---------|-----------|
| [Risco 1] | [A/M/B] | [A/M/B] | [Plano] |
| [Risco 2] | [A/M/B] | [A/M/B] | [Plano] |
| [Risco 3] | [A/M/B] | [A/M/B] | [Plano] |

---

### 8. Perguntas em Aberto

- [ ] [Pergunta 1 — quem deve responder]
- [ ] [Pergunta 2 — quem deve responder]
- [ ] [Pergunta 3 — quem deve responder]

---

### 9. Registro de Decisões

| Data | Decisão | Contexto |
|------|---------|----------|
| [DD/MM] | [Decisão tomada durante revisão] | [Por quê] |

---

## Exemplo Preenchido (Resumo)

> **RFC-017:** Migração de monolito para microsserviços — módulo de pagamentos
> **Autor:** Carlos Lima, Staff Engineer | **Status:** Aprovado
> **Motivação:** Monolito atual limita deploys a 2x/semana; módulo de pagamentos precisa de 99.99% uptime independente
> **Proposta:** Extrair módulo de pagamentos para serviço independente com gRPC, DB dedicado (PostgreSQL), e event sourcing
> **Fases:** 4 fases em 16 sprints | **Custo adicional de infra:** +R$ 8K/mês
> **Risco principal:** Consistência eventual durante migração — mitigado com dual-write + reconciliação

---

## Dicas de Uso
- RFC não é spec de implementação — foque no "o quê" e "por quê", não em cada detalhe do "como"
- Período de review mínimo de 5 dias úteis — apressar é garantia de problemas
- Inclua pessoas de fora do seu time como reviewers — eles veem pontos cegos
- Se o RFC ficar com mais de 10 páginas, está grande demais — quebre em fases
- Documente alternativas descartadas — mostra que pensou no problema
- Mantenha a seção de perguntas atualizada durante o review
