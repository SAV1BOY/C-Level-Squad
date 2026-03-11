# COO Execution Velocity Audit

## Propósito
Avaliar o equilíbrio entre velocidade de execução e qualidade de entrega na organização. Execução rápida sem qualidade gera retrabalho. Qualidade perfeita sem velocidade gera irrelevância. O objetivo é encontrar e manter o ponto ótimo para o estágio atual da empresa.

## Quando Aplicar
- Mensalmente como parte da revisão operacional
- Quando projetos consistentemente atrasarem em relação ao planejado
- Quando a qualidade das entregas estiver abaixo do aceitável
- Quando houver percepção de que "estamos lentos" ou "estamos cortando corners"
- Após mudanças significativas no time ou na estrutura de squads

## Agente Responsável
**Agente COO (Chief Operating Officer Agent)** — responsável por otimizar a velocidade de execução sem comprometer a qualidade necessária para o estágio da empresa.

## Checklist

### Seção 1: Métricas de Velocidade
- [ ] Cycle time médio de projetos está medido e benchmarked
- [ ] Lead time de decisões críticas está rastreado (da identificação à ação)
- [ ] Throughput de entregas por sprint/ciclo está medido por squad
- [ ] A tendência de velocidade está clara: acelerando, estável ou desacelerando
- [ ] Projetos concluídos no prazo representam pelo menos 70% do total
- [ ] O tempo entre decisão e início de execução é inferior a 48 horas
- [ ] Não há projetos "zumbis" — iniciados mas sem progresso há mais de 2 semanas
- [ ] A velocidade é medida por valor entregue, não apenas por volume de atividade

### Seção 2: Métricas de Qualidade
- [ ] Taxa de retrabalho está medida e abaixo de 15%
- [ ] Bugs/defeitos em produção estão dentro dos limites aceitáveis
- [ ] Customer satisfaction (CSAT/NPS) está dentro ou acima do target
- [ ] Escapes de qualidade (problemas que chegaram ao cliente) são rastreados
- [ ] Cada squad tem definição clara de "done" (definition of done)
- [ ] Code review, QA e validação estão integrados no fluxo sem serem gargalos
- [ ] A qualidade é medida de forma objetiva, não apenas por percepção
- [ ] Standards de qualidade são proporcionais ao impacto da entrega

### Seção 3: Equilíbrio Velocidade × Qualidade
- [ ] Existe uma política clara de quando priorizar velocidade sobre qualidade
- [ ] Existe uma política clara de quando priorizar qualidade sobre velocidade
- [ ] A decisão de trade-off é feita pelo DRI com base em critérios definidos
- [ ] O trade-off é comunicado e aceito pelos stakeholders antes da execução
- [ ] Technical debt gerada por priorização de velocidade está registrada e planejada
- [ ] Não há qualidade excessiva (gold plating) em entregas de baixo impacto
- [ ] O custo do retrabalho é menor que o custo de atraso (validação econômica)
- [ ] O equilíbrio é revisado por contexto — não há regra universal permanente

### Seção 4: Identificação de Atrasos e Causas
- [ ] Causas recorrentes de atraso estão identificadas e catalogadas
- [ ] Atrasos por dependência entre times estão mapeados e mitigados
- [ ] Atrasos por falta de decisão estão rastreados e escalados
- [ ] Atrasos por falta de recurso (pessoas, budget, ferramentas) são visíveis
- [ ] Atrasos por scope creep são prevenidos com processos de change management
- [ ] O impacto de cada atraso é quantificado (custo de oportunidade)
- [ ] Existe um processo de fast-track para projetos críticos que estão atrasados
- [ ] Root cause analysis é feita para atrasos significativos (não apenas sintomas)

### Seção 5: Cultura de Execução
- [ ] O time valoriza entrega concreta acima de planejamento extenso
- [ ] Bias for action é praticado: decidir rápido com informação imperfeita
- [ ] Retrospectivas focam em como melhorar velocidade e qualidade juntas
- [ ] Bloqueios são escalados rapidamente, não tolerados silenciosamente
- [ ] Wins de execução são celebrados e reconhecidos publicamente
- [ ] A organização aprende com cada ciclo de entrega (melhoria contínua)
- [ ] Ferramentas e processos estão a serviço da execução, não ao contrário
- [ ] O overhead de gestão de projetos é proporcional ao tamanho do projeto

## Critérios de Aprovação
- Cycle time médio dentro ou abaixo do benchmark para o tipo de entrega
- Taxa de retrabalho abaixo de 15%
- Pelo menos 70% dos projetos concluídos no prazo
- Zero projetos "zumbis" há mais de 2 semanas sem progresso
- Equilíbrio velocidade × qualidade documentado e aceito por cada squad
- Pelo menos 85% dos itens de todas as seções concluídos

## O que Fazer se Falhar
1. Identificar os top 3 fatores que mais impactam velocidade e qualidade
2. Para velocidade baixa: eliminar burocracia, reduzir WIP, resolver dependências
3. Para qualidade baixa: reforçar definition of done, investir em automação de testes
4. Implementar WIP limits por squad para melhorar flow
5. Realizar value stream mapping dos processos de entrega mais lentos
6. Considerar ajuste de squad composition se o problema for estrutural
7. Criar plano de melhoria com metas de 30/60/90 dias
8. Re-auditar em 30 dias com foco nas métricas que falharam

## Referências
- "Accelerate" — Nicole Forsgren, Jez Humble, Gene Kim (DORA metrics)
- "The Goal" — Eliyahu Goldratt (Theory of Constraints)
- Sprint/cycle metrics dashboards (internal)
- Retrospectiva reports dos últimos 3 ciclos
- Quality metrics dashboard
- "Shape Up" — Basecamp (ciclos de execução)
- Value stream mapping templates
