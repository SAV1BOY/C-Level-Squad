# Engineering Execution Audit

## Propósito
Avaliar a qualidade da execução de engenharia usando DORA metrics como referência, além de qualidade de código, throughput de entregas e gestão de tech debt. Engenharia de excelência não é sobre escrever código perfeito — é sobre entregar valor ao negócio de forma sustentável e rápida.

## Quando Aplicar
- Mensalmente como parte da revisão de engenharia
- Quando velocity de entrega estiver abaixo do esperado por 2+ sprints
- Quando bugs em produção estiverem acima do threshold aceitável
- Quando tech debt estiver impactando visivelmente a capacidade de entrega
- Após mudanças significativas na organização de engenharia

## Agente Responsável
**Agente CTO (Chief Technology Officer Agent)** — responsável por garantir que a engenharia entrega com velocidade, qualidade e sustentabilidade.

## Checklist

### Seção 1: DORA Metrics
- [ ] Deployment Frequency é medida e está dentro do target (daily para high performers)
- [ ] Lead Time for Changes é medido (commit → production) e rastreado
- [ ] Change Failure Rate é medida e está abaixo de 15%
- [ ] Mean Time to Restore (MTTR) é medido e está dentro do target
- [ ] DORA metrics são visíveis para toda a engenharia em dashboard
- [ ] Tendência das DORA metrics está clara (melhorando, estável, piorando)
- [ ] DORA metrics são benchmarked contra o estado da arte do setor
- [ ] Ações de melhoria para DORA metrics abaixo do target estão definidas

### Seção 2: Qualidade de Código e Entrega
- [ ] Code review é obrigatório e realizado por pelo menos 1 peer
- [ ] Cobertura de testes automatizados está acima do threshold (>70% para código crítico)
- [ ] CI/CD pipeline está funcionando e é confiável (flaky tests <5%)
- [ ] Testes rodam em menos de 15 minutos (fast feedback)
- [ ] Feature flags são usados para deploys de baixo risco
- [ ] Rollback é possível e testado em menos de 15 minutos
- [ ] Static analysis e linters estão integrados no pipeline
- [ ] Security scanning (SAST, dependency check) roda automaticamente

### Seção 3: Throughput e Produtividade
- [ ] Velocity ou throughput por squad é medido e rastreado
- [ ] WIP (Work in Progress) limits estão definidos e respeitados
- [ ] Cycle time por tipo de work item é medido (bug fix, feature, tech debt)
- [ ] Bloqueios são rastreados e resolvidos com SLA definido
- [ ] Meetings overhead não excede 30% do tempo dos engenheiros
- [ ] Contexto switching é minimizado (engenheiros trabalham em 1-2 projetos, não 5+)
- [ ] Developer tooling é adequado e não é fonte de fricção
- [ ] Pair programming ou mob programming é praticado quando apropriado

### Seção 4: Tech Debt Management
- [ ] Tech debt está catalogado com impacto estimado e esforço de resolução
- [ ] Pelo menos 20% do capacity de engineering é alocado para tech debt
- [ ] Tech debt que impacta velocity de entrega tem prioridade alta
- [ ] Tech debt que impacta reliability tem prioridade máxima
- [ ] O custo de manter tech debt (interest) é quantificado
- [ ] Decisões de acumular tech debt são conscientes e documentadas
- [ ] Tech debt é revisado em sprint planning como candidato a trabalho
- [ ] Métricas de tech debt são reportadas ao CTO regularmente

### Seção 5: Cultura de Engenharia
- [ ] Engenheiros têm ownership sobre o que constroem (you build it, you run it)
- [ ] Documentação técnica é atualizada como parte do processo de desenvolvimento
- [ ] Knowledge sharing é ativo (tech talks, RFCs, design docs)
- [ ] Experimentação e inovação técnica são encorajadas (hack days, 20% time)
- [ ] Onboarding técnico permite que novos engenheiros contribuam em <2 semanas
- [ ] Feedback técnico é dado de forma construtiva e frequente
- [ ] Decisões técnicas são tomadas com dados e trade-off analysis
- [ ] O time se sente produtivo e empoderado para resolver problemas

## Critérios de Aprovação
- DORA metrics dentro ou acima do benchmark "High" para o setor
- Change Failure Rate abaixo de 15%
- Cobertura de testes automatizados acima de 70% para código crítico
- Tech debt allocation de pelo menos 20% do capacity
- Pelo menos 85% dos itens de todas as seções concluídos
- Developer satisfaction acima de 7/10 em pesquisa interna

## O que Fazer se Falhar
1. Identificar qual dimensão é a mais crítica: velocidade, qualidade ou sustentabilidade
2. Para velocidade baixa: reduzir WIP, eliminar bloqueios, simplificar processos
3. Para qualidade baixa: investir em testes, code review e CI/CD
4. Para tech debt alto: alocar sprint dedicado e criar plano de pagamento
5. Implementar weekly engineering metrics review
6. Considerar ajuste de squad composition ou estrutura se o problema for organizacional
7. Investir em developer experience (DX) se ferramentas forem o gargalo
8. Re-auditar em 30 dias com foco nas métricas que falharam

## Referências
- "Accelerate" — Nicole Forsgren, Jez Humble, Gene Kim
- DORA State of DevOps Reports
- "A Philosophy of Software Design" — John Ousterhout
- Engineering metrics dashboard (internal)
- Tech debt registry (internal wiki)
- Sprint retrospective reports
- "An Elegant Puzzle" — Will Larson
