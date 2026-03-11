# CTO Tech Debt Audit

## Propósito
Avaliar o estado da dívida técnica da organização: seu impacto real na capacidade de entrega, a priorização de pagamento e a existência de um plano sustentável de redução. Tech debt não gerida é como dívida financeira com juros compostos — cresce exponencialmente e eventualmente paralisa a operação.

## Quando Aplicar
- Trimestralmente como parte da revisão técnica estratégica
- Quando velocity de engenharia estiver em declínio consistente
- Quando o custo de implementar mudanças simples estiver desproporcionalmente alto
- Quando incidentes de produção forem causados por código legado ou arquitetura obsoleta
- Antes de grandes ciclos de planejamento para informar alocação de recursos

## Agente Responsável
**Agente CTO (Chief Technology Officer Agent)** — responsável por manter a dívida técnica em níveis gerenciáveis e garantir que seu pagamento é priorizado estrategicamente.

## Checklist

### Seção 1: Inventário de Tech Debt
- [ ] Existe um registry centralizado de tech debt catalogado e categorizado
- [ ] Categorias estão definidas: código, arquitetura, infraestrutura, dependências, documentação
- [ ] Cada item de tech debt tem severidade classificada (crítica, alta, média, baixa)
- [ ] Cada item tem owner designado e responsável por acompanhar
- [ ] A idade de cada item de tech debt é rastreada (há quanto tempo existe)
- [ ] O inventário é atualizado pelo menos mensalmente
- [ ] Novos itens de tech debt são registrados quando criados conscientemente
- [ ] Itens resolvidos são removidos e documentados como pagos

### Seção 2: Avaliação de Impacto
- [ ] O impacto de cada item de tech debt na velocity de entrega está estimado
- [ ] O impacto na reliability e incidentes está quantificado
- [ ] O impacto na developer experience e moral está avaliado
- [ ] O custo do "juros" — quanto custa manter o debt a cada mês — está calculado
- [ ] Tech debt que causa incidentes de produção está marcado como crítico
- [ ] Tech debt que bloqueia features de alto valor está identificado
- [ ] O custo total estimado de todo o tech debt está calculado
- [ ] A tendência do tech debt está clara: crescendo, estável ou diminuindo

### Seção 3: Priorização de Pagamento
- [ ] Framework de priorização está definido (impacto × esforço, RICE, ou equivalente)
- [ ] Os top 10 itens de tech debt prioritários estão identificados
- [ ] A priorização considera impacto no negócio, não apenas complexidade técnica
- [ ] Quick wins (alto impacto, baixo esforço) estão identificados e agendados
- [ ] Items de alto esforço estão decompostos em incrementos menores
- [ ] A priorização é revisada trimestralmente com input de product e engenharia
- [ ] Tech debt de segurança tem prioridade sobre tech debt de conveniência
- [ ] A priorização está alinhada com o roadmap de produto

### Seção 4: Plano de Pagamento
- [ ] Pelo menos 20% do capacity de engenharia é dedicado a tech debt
- [ ] A alocação é consistente (não apenas quando "sobra tempo")
- [ ] O plano de pagamento tem metas trimestrais mensuráveis
- [ ] Progresso é reportado ao CTO e ao C-Level regularmente
- [ ] Grandes refactorings estão planejados com business case documentado
- [ ] Tech debt é tratado em sprint planning como trabalho legítimo
- [ ] A organização entende que tech debt payment é investimento, não custo
- [ ] Existe balance entre pagar tech debt existente e evitar criar novo

### Seção 5: Prevenção de Novo Tech Debt
- [ ] Code review inclui avaliação de tech debt potencial
- [ ] Decisões de acumular tech debt são conscientes e documentadas (ADR)
- [ ] Deadlines que geram tech debt têm plano de pagamento pré-aprovado
- [ ] Architecture standards previnem as formas mais comuns de tech debt
- [ ] Automated tools detectam padrões de tech debt (complexity, duplicação, coverage)
- [ ] Retrospectivas incluem discussão sobre tech debt criado no sprint
- [ ] A cultura valoriza qualidade sustentável, não apenas entrega rápida
- [ ] Métricas de qualidade (code coverage, complexity, duplication) são rastreadas
- [ ] O rate de criação de novo tech debt é monitorado
- [ ] Existe um processo de "tech debt budget" por sprint ou ciclo

## Critérios de Aprovação
- Tech debt registry atualizado e categorizado com 100% dos itens conhecidos
- Pelo menos 20% do capacity alocado para tech debt payment
- Top 10 itens priorizados com plano de pagamento
- Tendência de tech debt estável ou em declínio
- Pelo menos 85% dos itens de todas as seções concluídos
- Nenhum item de tech debt crítico sem plano de ação

## O que Fazer se Falhar
1. Se o registry não existe: realizar tech debt discovery sprint de 1 semana
2. Se capacity não é alocado: escalar para CEO/COO com business case de impacto
3. Se tech debt está crescendo: congelar novos features e dedicar 1 sprint a pagamento
4. Se priorização é ruim: workshop com product e engenharia para alinhar critérios
5. Para itens críticos não tratados: criar war room com deadline de resolução
6. Implementar automated tools se a detecção for manual e inconsistente
7. Criar cultura de "leave the codebase better than you found it"
8. Re-auditar em 30 dias com foco nos itens mais impactantes

## Referências
- "Managing Technical Debt" — Philippe Kruchten, Robert Nord, Ipek Ozkaya
- Tech Debt Registry (internal wiki)
- "A Philosophy of Software Design" — John Ousterhout
- DORA metrics e correlação com tech debt
- Code quality metrics dashboard (SonarQube, CodeClimate, etc.)
- Sprint retrospective reports
- "Refactoring" — Martin Fowler
