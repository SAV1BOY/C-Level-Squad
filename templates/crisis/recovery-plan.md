# Template: Plano de Recuperação

## Propósito
Este template estrutura o plano de recuperação após um incidente significativo, crise ou evento disruptivo. Cobre desde a estabilização imediata até o retorno à operação normal e implementação de melhorias para prevenir recorrência.

## Instruções de Uso
1. Inicie o plano assim que o incidente estiver sob controle (não precisa estar resolvido)
2. Envolva todas as áreas afetadas na elaboração
3. Defina responsáveis e prazos para cada ação
4. Revisão semanal até conclusão de todas as ações

---

## Informações do Plano

| Campo | Valor |
|-------|-------|
| **Incidente de Referência** | [ID e título do incidente] |
| **Data do Incidente** | [DD/MM/AAAA] |
| **Data de Criação do Plano** | [DD/MM/AAAA] |
| **Líder da Recuperação** | [Nome — Cargo] |
| **Equipe de Recuperação** | [Nomes e áreas] |
| **Prazo para Recuperação Total** | [DD/MM/AAAA] |
| **Status** | [Em planejamento / Em execução / Concluído] |

---

## 1. Avaliação de Danos

### 1.1 Impacto Atual

| Dimensão | Impacto | Severidade | Status de Recuperação |
|----------|---------|-----------|---------------------|
| Operações | [Descrever impacto] | [Crítico/Alto/Médio/Baixo] | [% recuperado] |
| Clientes | [Descrever impacto] | [Severidade] | [% recuperado] |
| Financeiro | [R$ impactados] | [Severidade] | [% recuperado] |
| Dados/Sistemas | [Descrever impacto] | [Severidade] | [% recuperado] |
| Reputação | [Descrever impacto] | [Severidade] | [Qualitativo] |
| Legal/Regulatório | [Descrever impacto] | [Severidade] | [Status] |
| Pessoas/Moral | [Descrever impacto] | [Severidade] | [Qualitativo] |

### 1.2 Sistemas/Processos Afetados

| Sistema/Processo | Status Atual | Criticidade | Workaround Disponível |
|-----------------|-------------|------------|---------------------|
| [Sistema 1] | [Indisponível / Degradado / Normal] | [P0/P1/P2] | [Sim: descrever / Não] |
| [Sistema 2] | [Status] | [Criticidade] | [Workaround] |
| [Sistema 3] | [Status] | [Criticidade] | [Workaround] |

---

## 2. Fases de Recuperação

### Fase 1: Estabilização (primeiras 24-72h)
**Objetivo:** Parar o sangramento e restaurar operações mínimas viáveis

| Ação | Prioridade | Owner | Prazo | Status | Notas |
|------|-----------|-------|-------|--------|-------|
| [Ação 1 — ex: Restaurar serviço core de backup] | P0 | [Nome] | [Data/Hora] | [Status] | [Detalhes] |
| [Ação 2 — ex: Ativar workarounds para clientes] | P0 | [Nome] | [Data/Hora] | [Status] | [Detalhes] |
| [Ação 3 — ex: Comunicar status a stakeholders] | P0 | [Nome] | [Data/Hora] | [Status] | [Detalhes] |

**Critério de conclusão da Fase 1:** [O que define que estabilizamos — ex: "Serviço core disponível com performance > 80% do normal"]

### Fase 2: Restauração (1-2 semanas)
**Objetivo:** Retornar todas as operações ao nível pré-incidente

| Ação | Prioridade | Owner | Prazo | Status | Notas |
|------|-----------|-------|-------|--------|-------|
| [Ação 1 — ex: Migrar de workaround para sistema definitivo] | P1 | [Nome] | [Data] | [Status] | |
| [Ação 2 — ex: Reconciliar dados perdidos/corrompidos] | P1 | [Nome] | [Data] | [Status] | |
| [Ação 3 — ex: Restaurar integrações de terceiros] | P1 | [Nome] | [Data] | [Status] | |
| [Ação 4 — ex: Resolver backlog de tickets de suporte] | P1 | [Nome] | [Data] | [Status] | |

**Critério de conclusão da Fase 2:** [Ex: "Todos os sistemas operando em 100%, sem workarounds ativos, backlog de suporte zerado"]

### Fase 3: Fortalecimento (2-8 semanas)
**Objetivo:** Implementar melhorias para prevenir recorrência e aumentar resiliência

| Ação | Prioridade | Owner | Prazo | Status | Notas |
|------|-----------|-------|-------|--------|-------|
| [Ação 1 — ex: Implementar redundância no sistema X] | P1 | [Nome] | [Data] | [Status] | |
| [Ação 2 — ex: Melhorar monitoramento e alertas] | P1 | [Nome] | [Data] | [Status] | |
| [Ação 3 — ex: Atualizar runbooks e documentação] | P2 | [Nome] | [Data] | [Status] | |
| [Ação 4 — ex: Treinar time em novos procedimentos] | P2 | [Nome] | [Data] | [Status] | |
| [Ação 5 — ex: Realizar teste de disaster recovery] | P2 | [Nome] | [Data] | [Status] | |

**Critério de conclusão da Fase 3:** [Ex: "Todas as ações do postmortem implementadas e testadas"]

### Fase 4: Revisão e Encerramento
**Objetivo:** Validar recuperação completa e documentar lições

| Ação | Owner | Prazo | Status |
|------|-------|-------|--------|
| Postmortem completo publicado | [Nome] | [Data] | [Status] |
| Revisão de todas as ações corretivas | [Nome] | [Data] | [Status] |
| Comunicação final para stakeholders | [Nome] | [Data] | [Status] |
| Atualização de plano de continuidade de negócio | [Nome] | [Data] | [Status] |
| Retrospectiva da resposta ao incidente | [Nome] | [Data] | [Status] |

---

## 3. Comunicação Durante Recuperação

| Stakeholder | Frequência | Canal | Responsável | Próximo Update |
|------------|-----------|-------|-------------|---------------|
| Clientes afetados | [Diária/Semanal] | [E-mail/Status page] | [Nome] | [Data] |
| Toda a empresa | [Diária] | [Slack] | [Nome] | [Data] |
| Board | [Semanal] | [E-mail] | [CEO] | [Data] |
| Reguladores | [Conforme exigido] | [Ofício] | [Jurídico] | [Data] |

---

## 4. Recursos Necessários

| Recurso | Tipo | Disponibilidade | Custo | Aprovação |
|---------|------|----------------|-------|-----------|
| [Time de engenharia dedicado] | Pessoas | [X pessoas por Y semanas] | [Custo de oportunidade] | [Aprovado/Pendente] |
| [Consultoria externa] | Serviço | [Disponível em X dias] | [R$ X] | [Status] |
| [Infraestrutura adicional] | Tecnologia | [Disponível em X dias] | [R$ X/mês] | [Status] |
| [Horas extras / plantão especial] | Pessoas | [Imediato] | [R$ X] | [Status] |

---

## 5. Riscos da Recuperação

| Risco | Impacto | Mitigação |
|-------|---------|-----------|
| Recuperação demora mais que o planejado | [Descrever impacto] | [Plano B / Comunicação proativa] |
| Novo incidente durante recuperação | [Descrever impacto] | [Equipe reserva / Priorização] |
| Dados não recuperáveis | [Descrever impacto] | [Processo de reconciliação manual] |
| Perda de confiança de clientes | [Churn aumentado] | [Programa de compensação / CS proativo] |

---

## 6. Métricas de Acompanhamento

| Métrica | Baseline (pré-incidente) | Atual | Meta de Recuperação | Prazo |
|---------|------------------------|-------|-------------------|-------|
| [Uptime do serviço] | [99.9%] | [X%] | [99.9%] | [Data] |
| [Latência p99] | [Xms] | [Xms] | [Xms] | [Data] |
| [Tickets de suporte/dia] | [N] | [N] | [N] | [Data] |
| [NPS/CSAT] | [Score] | [Score] | [Score] | [Data] |
| [Taxa de churn mensal] | [X%] | [X%] | [X%] | [Data] |

---

## Exemplo Preenchido (Resumo)

> **Incidente:** Corrupção de dados de billing após falha em migração de banco
> **Impacto:** 2.300 clientes com faturas incorretas, R$ 450K em cobranças erradas
> **Fase 1 (24h):** Pausar cobranças, comunicar clientes, ativar billing manual para enterprise
> **Fase 2 (10 dias):** Reconciliar dados, reprocessar faturas, creditar diferenças
> **Fase 3 (6 semanas):** Implementar validação pré-migração, backup point-in-time, teste de regressão de billing

---

## Dicas de Uso
- Priorize ESTABILIZAÇÃO sobre investigação — pare o sangramento primeiro
- Defina critérios claros de conclusão para cada fase — evite recuperação infinita
- Comunique proativamente — silêncio durante recuperação gera mais ansiedade
- Aloque recursos dedicados — recuperação em "tempo livre" nunca funciona
- Documente workarounds formalmente — eles podem virar permanentes sem querer
- A Fase 3 (fortalecimento) é a mais importante e a mais negligenciada — não corte
