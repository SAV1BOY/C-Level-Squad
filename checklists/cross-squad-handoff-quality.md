# Checklist de Qualidade — Cross-Squad Handoff

## Propósito
Garantir que handoffs entre squads, equipes ou agentes sejam completos e sem ambiguidade: inputs e outputs claramente definidos, DoD (Definition of Done) e DoR (Definition of Ready) respeitados, owners atribuídos em ambos os lados, e evidências fornecidas para validação. Este checklist elimina a "terra de ninguém" que surge em interfaces entre equipes e reduz retrabalho, atrasos e frustração.

## Quando Aplicar
- Sempre que um entregável passa de uma equipe/squad para outra
- Em transições de fase de projeto (discovery > delivery, design > engineering)
- Quando agentes transferem outputs para outros agentes processarem
- Em integrações entre sistemas mantidos por equipes diferentes
- Na transferência de ownership de produtos, serviços ou clientes
- Em handoffs operacionais (turnos, on-call rotations, suporte)

## Agente Responsável
- **Primário:** O owner do entregável na equipe de origem (sending team)
- **Receptor:** O owner designado na equipe de destino (receiving team)
- **Facilitador:** CoS Agent ou Scrum Master Agent para handoffs bloqueados
- **Arbitrador:** CPO Agent ou CTO Agent para conflitos de escopo

## Checklist

### Seção 1 — Inputs e Outputs Claros
- [ ] O entregável (output) está descrito com especificidade suficiente para ser verificado
- [ ] O formato do entregável está definido (documento, código, design, dados, API, etc.)
- [ ] Os inputs que a equipe receptora precisa fornecer estão documentados
- [ ] As premissas da equipe de origem estão comunicadas à equipe receptora
- [ ] Os artefatos de suporte estão incluídos (documentação, specs, test cases, exemplos)
- [ ] O contexto de negócio do entregável está comunicado (por que isso existe, para quem)
- [ ] As limitações conhecidas do entregável estão documentadas (known issues, edge cases)
- [ ] O entregável está acessível no repositório ou sistema oficial (não em comunicações informais)
- [ ] A versão do entregável está controlada e claramente identificada
- [ ] Os dados de teste ou ambientes de teste estão disponíveis para a equipe receptora

### Seção 2 — DoD e DoR Definidos
- [ ] A Definition of Done (DoD) do entregável está escrita e acordada por ambas as equipes
- [ ] A Definition of Ready (DoR) para a equipe receptora iniciar trabalho está definida
- [ ] Os critérios de aceite do entregável são verificáveis e não subjetivos
- [ ] A qualidade mínima aceitável está especificada (coverage, performance, completude)
- [ ] Os testes realizados pela equipe de origem estão documentados com resultados
- [ ] A conformidade com padrões e guidelines está verificada
- [ ] A revisão de código ou design review (quando aplicável) foi completada
- [ ] O entregável atende aos requisitos não-funcionais especificados
- [ ] A aprovação formal do DoD foi registrada (sign-off)
- [ ] Divergências entre DoD esperado e entregue estão documentadas e aceitas

### Seção 3 — Owners Designados
- [ ] O owner do handoff na equipe de origem está nomeado e contactável
- [ ] O owner do handoff na equipe receptora está nomeado e contactável
- [ ] Ambos os owners concordaram com o timeline e escopo do handoff
- [ ] O canal de comunicação entre os owners está definido e ativo
- [ ] O escalation path para bloqueios está documentado
- [ ] O owner de suporte pós-handoff está definido (para dúvidas e issues pós-transição)
- [ ] A duração do suporte pós-handoff está acordada (ex: 2 semanas de support period)
- [ ] O backup owner está designado para cada lado em caso de indisponibilidade
- [ ] A transferência de conhecimento (knowledge transfer) está planejada quando necessário
- [ ] O ponto de "handoff completo" está definido (quando a equipe de origem é desonerada)

### Seção 4 — Evidências Fornecidas
- [ ] A evidência de que o DoD foi atingido está documentada e acessível
- [ ] Os resultados de testes estão publicados (automated tests, manual tests, QA sign-off)
- [ ] Os screenshots, logs ou métricas de validação estão incluídos quando aplicável
- [ ] A demo ou walkthrough do entregável foi realizada com a equipe receptora
- [ ] A documentação técnica está atualizada e reflete o estado atual do entregável
- [ ] O runbook operacional está incluído (se o entregável é um serviço ou sistema)
- [ ] Os riscos conhecidos e dívidas técnicas estão documentados e aceitos
- [ ] O feedback da equipe receptora sobre a qualidade do handoff está registrado
- [ ] A evidência de conformidade regulatória está incluída quando aplicável
- [ ] O check de segurança (security review) está incluído quando aplicável

### Seção 5 — Processo e Cadência
- [ ] O handoff segue o processo padrão definido para a organização
- [ ] O handoff foi agendado com antecedência adequada (não de última hora)
- [ ] O calendário de handoffs recorrentes está publicado e acessível
- [ ] O lead time entre disponibilidade do entregável e necessidade da equipe receptora está respeitado
- [ ] O status do handoff está visível no dashboard ou board de acompanhamento
- [ ] Os handoffs anteriores foram retrospectivados e lições incorporadas
- [ ] O template de handoff está sendo utilizado de forma consistente
- [ ] A métrica de qualidade de handoffs (taxa de retrabalho, satisfação) está sendo medida

### Seção 6 — Resolução de Conflitos
- [ ] O processo para disputas sobre qualidade do handoff está definido
- [ ] Os critérios objetivos para aceitação ou rejeição do handoff estão claros
- [ ] O tempo máximo para a equipe receptora aceitar ou rejeitar está definido
- [ ] O processo de retorno (handoff rejeitado) tem feedback específico e construtivo
- [ ] A escalação para arbitragem tem dono e timeline definidos

## Critérios de Aprovação
- Inputs e outputs claramente definidos e acessíveis no repositório oficial
- DoD e DoR acordados por ambas as equipes com critérios verificáveis
- Owners nomeados em ambos os lados com canais de comunicação ativos
- Evidências de qualidade fornecidas e verificáveis
- Equipe receptora confirmou que tem o necessário para iniciar trabalho
- Score mínimo de completude: 85% dos itens marcados

## O que Fazer se Falhar
1. Se inputs/outputs não estão claros, pausar o handoff e realizar sessão de clarificação
2. Se DoD/DoR não estão acordados, agendar sessão de alinhamento entre os owners
3. Se evidências estão ausentes, retornar o entregável para complementação
4. Se a equipe receptora rejeita o handoff, fornecer feedback específico para correção
5. Se conflitos de escopo persistem, escalar para o arbitrador designado
6. Registrar padrões de falha no RalphLoop para melhorar o processo de handoff
7. Se handoffs estão consistentemente problemáticos entre certas equipes, revisar interfaces no org design

## Referências
- Reinertsen, D. — "The Principles of Product Development Flow" (managing queues and handoffs)
- Forsgren, N., Humble, J. & Kim, G. — "Accelerate" (eliminação de handoffs desnecessários)
- Framework de DoD/DoR: Scrum Guide e extensões
- Template interno: `/templates/handoff-template.md`
- Dashboard de handoffs: `/dashboards/cross-squad-handoffs.md`
- Guia de interfaces: `/guides/squad-interface-guide.md`
