# Checklist de Prontidão para Lançamento (Launch Readiness Quality)

## Propósito
Garantir que todo lançamento significativo (produto, feature, campanha, expansão)
tenha todas as áreas prontas: produto, marketing, operações, suporte e dados.
Este checklist previne lançamentos prematuros que danificam a experiência do cliente
e a reputação da marca, ou lançamentos atrasados por falta de coordenação.

## Quando Aplicar
- 4 semanas antes de qualquer lançamento classificado como Tier 1 ou Tier 2
- 2 semanas antes como checkpoint final antes do go/no-go decision
- No dia do lançamento como checklist de execução final
- Após o lançamento para verificar estabilização e early metrics
- Na retrospectiva de lançamento (1-2 semanas após)

## Agente Responsável
- **Primário:** Launch Manager ou Project Owner designado
- **Secundário:** Cada Squad Lead para readiness do seu domínio
- **Revisor:** CEO ou CPO como aprovador final do go/no-go

## Checklist

### Seção 1 — Product Readiness (Prontidão de Produto)
- [ ] Item 1: O produto ou feature está feature-complete conforme spec aprovada
- [ ] Item 2: Todos os bugs de severidade P0 e P1 estão resolvidos
- [ ] Item 3: Bugs de severidade P2 conhecidos estão documentados com workarounds
- [ ] Item 4: Testes de QA (funcional, regressão, performance) foram concluídos com aprovação
- [ ] Item 5: Testes de load e stress foram conduzidos para capacidade esperada de lançamento
- [ ] Item 6: Security review foi conduzida e aprovada (vulnerabilities endereçadas)
- [ ] Item 7: A/B tests ou beta testing com usuários reais foram concluídos com resultados positivos
- [ ] Item 8: Documentação técnica (API docs, release notes) está completa e publicada
- [ ] Item 9: Rollback plan está definido e testado (como reverter se algo der errado)
- [ ] Item 10: Feature flags estão configurados para controlar o rollout gradual

### Seção 2 — Marketing Readiness (Prontidão de Marketing)
- [ ] Item 11: Estratégia de lançamento (launch strategy) está documentada e aprovada
- [ ] Item 12: Messaging e positioning estão finalizados e aprovados por stakeholders
- [ ] Item 13: Materiais de marketing (landing page, emails, ads) estão produzidos e revisados
- [ ] Item 14: Blog post ou press release está redigido e agendado
- [ ] Item 15: Social media plan está pronto com conteúdo e calendário
- [ ] Item 16: Email campaigns para base existente estão configuradas e testadas
- [ ] Item 17: Enablement materials para equipe de vendas estão prontos (pitch deck, one-pager)
- [ ] Item 18: Pricing page atualizada (se houver mudança de pricing ou tier)
- [ ] Item 19: Analytics e tracking estão configurados para medir performance do lançamento
- [ ] Item 20: Paid media campaigns estão preparadas e orçadas (se aplicável)

### Seção 3 — Operations Readiness (Prontidão Operacional)
- [ ] Item 21: Processos operacionais novos ou alterados estão documentados e treinados
- [ ] Item 22: Capacidade operacional comporta o volume esperado pós-lançamento
- [ ] Item 23: SLAs operacionais estão definidos para o novo produto ou feature
- [ ] Item 24: Billing e invoicing estão configurados e testados end-to-end
- [ ] Item 25: Processos de provisioning e onboarding de novos clientes estão prontos
- [ ] Item 26: Integrations com sistemas de terceiros estão testadas e estáveis
- [ ] Item 27: Monitoramento de infraestrutura e alertas estão configurados

### Seção 4 — Support Readiness (Prontidão de Suporte)
- [ ] Item 28: Equipe de suporte foi treinada no novo produto ou feature
- [ ] Item 29: FAQ e knowledge base estão atualizados e publicados
- [ ] Item 30: Fluxos de troubleshooting estão documentados para cenários comuns
- [ ] Item 31: Escalation paths para issues técnicos pós-lançamento estão definidos
- [ ] Item 32: Capacidade de suporte foi reforçada para absorver pico pós-lançamento
- [ ] Item 33: Chatbot ou self-service foi atualizado com informações do lançamento
- [ ] Item 34: SLA de resposta para issues do lançamento está definido (mais rápido que normal)

### Seção 5 — Data Readiness (Prontidão de Dados)
- [ ] Item 35: Métricas de sucesso do lançamento estão definidas (north star + supporting)
- [ ] Item 36: Dashboard de launch metrics está configurado e testado
- [ ] Item 37: Event tracking está implementado e validado para todas as ações relevantes
- [ ] Item 38: Baseline de métricas pré-lançamento está registrado para comparação
- [ ] Item 39: Plano de análise pós-lançamento está definido (o que analisar, quando, quem)
- [ ] Item 40: Alertas automáticos para métricas anômalas estão configurados
- [ ] Item 41: Data privacy compliance foi verificada para novos dados coletados

### Seção 6 — Go/No-Go Decision
- [ ] Item 42: Launch readiness review foi conduzida com todos os squad leads
- [ ] Item 43: Cada área confirmou readiness formalmente (sign-off por escrito)
- [ ] Item 44: Riscos residuais estão documentados e aceitos pelo decision-maker
- [ ] Item 45: Plano de contingência para os top 3 cenários de falha está pronto
- [ ] Item 46: A decisão de go/no-go foi tomada e documentada no decision log
- [ ] Item 47: Comunicação interna pré-lançamento foi enviada a toda a empresa
- [ ] Item 48: War room pós-lançamento está configurado para as primeiras 48 horas

## Critérios de Aprovação
O lançamento é autorizado (go decision) quando:

1. **100% dos itens P0 da Seção 1 (Product Readiness) estão completos**
2. **Pelo menos 90% dos itens de cada seção estão completos**
3. **Rollback plan está testado e pronto (Seção 1, Item 9)**
4. **Equipe de suporte está treinada e reforçada (Seção 4)**
5. **Dashboard de métricas está funcional (Seção 5)**
6. **Cada squad lead assinou readiness formalmente (Seção 6)**
7. **O decision-maker final (CEO ou CPO) aprovou o go**

## O que Fazer se Falhar
Se o lançamento não atinge os critérios de readiness:

1. **Delay decision:** Adiar o lançamento com nova data e plano de correção
2. **Scope reduction:** Lançar com escopo reduzido (MVP do lançamento)
3. **Phased rollout:** Lançar para subset de usuários (beta, early access)
4. **War room pre-launch:** Sessão intensiva para resolver gaps em 24-48 horas
5. **Partial launch:** Lançar componentes que estão prontos, segurar os que não estão
6. **Communication:** Se delay, comunicar a stakeholders internos e externos afetados
7. **Root cause:** Entender por que o lançamento não está pronto (planejamento, execução, scope creep)
8. **Postmortem antecipado:** Conduzir análise do que deu errado no processo de preparação

## Referências
- Marty Cagan — "Inspired" (product launch practices)
- April Dunford — "Obviously Awesome" (positioning for launch)
- Amazon — "Working Backwards" (PR/FAQ for launch preparation)
- Framework interno de Launch Playbook (documento em /execution/)
- Template de Launch Plan (documento em /templates/launch-plan.md)
- Template de Go/No-Go Checklist (documento em /templates/go-no-go.md)
- Calendário de lançamentos (documento em /execution/launch-calendar.md)
