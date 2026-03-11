# COO Bottleneck Detection

## Propósito
Identificar, diagnosticar e resolver gargalos operacionais que limitam o throughput da organização. Seguindo a Theory of Constraints, o output de qualquer sistema é determinado pelo seu gargalo mais limitante. Encontrar e explorar o constraint é o caminho mais rápido para melhorar performance.

## Quando Aplicar
- Quinzenalmente como parte do monitoramento operacional contínuo
- Quando o throughput da organização estiver abaixo do esperado
- Quando filas de trabalho estiverem crescendo consistentemente
- Quando lead times estiverem aumentando sem aumento proporcional de complexidade
- Após mudanças organizacionais que possam ter criado novos gargalos

## Agente Responsável
**Agente COO (Chief Operating Officer Agent)** — responsável por identificar constraints sistêmicos e criar planos de exploração e elevação de gargalos.

## Checklist

### Seção 1: Identificação de Gargalos
- [ ] Mapa de fluxo de valor (value stream map) atualizado nos últimos 60 dias
- [ ] Tempo de espera em cada etapa do fluxo está medido e visível
- [ ] Etapas com filas crescentes estão identificadas como potenciais gargalos
- [ ] Gargalos de pessoas (sobrecarga de indivíduos/times específicos) mapeados
- [ ] Gargalos de processo (aprovações, handoffs, burocracia) identificados
- [ ] Gargalos de tecnologia (sistemas lentos, falta de automação) catalogados
- [ ] Gargalos de decisão (espera por aprovação, falta de autoridade) rastreados
- [ ] O constraint principal (THE bottleneck) está identificado e comunicado

### Seção 2: Diagnóstico do Constraint Principal
- [ ] Root cause analysis foi realizada para o constraint principal
- [ ] O impacto do constraint no throughput total foi quantificado
- [ ] A causa é estrutural (design do sistema) ou circunstancial (temporária)?
- [ ] Dados de utilização do recurso-gargalo estão coletados e analisados
- [ ] O tempo que o recurso-gargalo gasta em atividades de valor foi calculado
- [ ] Desperdícios no recurso-gargalo foram identificados (espera, retrabalho, multitasking)
- [ ] Dependências que alimentam ou são alimentadas pelo gargalo estão mapeadas
- [ ] O custo do gargalo por semana/mês está estimado (custo de oportunidade)

### Seção 3: Plano de Exploração (Exploit the Constraint)
- [ ] O recurso-gargalo está sendo usado em 100% de capacidade para atividades de valor
- [ ] Atividades de não-valor foram removidas do recurso-gargalo
- [ ] O gargalo nunca fica ocioso — existe buffer de trabalho preparado
- [ ] Qualidade do input que chega ao gargalo é maximizada (sem retrabalho no gargalo)
- [ ] O gargalo é protegido de interrupções e contexto switching desnecessários
- [ ] Outros recursos estão subordinados ao ritmo do gargalo (não empurram mais do que ele processa)
- [ ] Quick wins para aumentar capacidade do gargalo foram implementados
- [ ] O plano de exploração tem métricas de sucesso definidas

### Seção 4: Plano de Elevação (Elevate the Constraint)
- [ ] Se exploit não for suficiente, plano de elevação está definido
- [ ] Opções de elevação avaliadas: mais recursos, automação, redesenho, terceirização
- [ ] Custo-benefício de cada opção de elevação está calculado
- [ ] Timeline de implementação da elevação é realista e acordado
- [ ] Riscos de cada opção de elevação estão mapeados
- [ ] O plano de elevação não cria um novo gargalo em outro ponto do sistema
- [ ] Budget para elevação está aprovado ou em processo de aprovação
- [ ] Após elevação, o próximo constraint foi identificado proativamente

### Seção 5: Monitoramento Contínuo
- [ ] Dashboard de gargalos está ativo e atualizado automaticamente
- [ ] Alertas automáticos disparam quando filas excedem thresholds definidos
- [ ] Revisão de gargalos é pauta fixa em pelo menos 1 cadência regular
- [ ] A organização entende que gargalos migram — resolver um revela o próximo
- [ ] Histórico de gargalos resolvidos e seu impacto está documentado
- [ ] Métricas de throughput do sistema total são acompanhadas (não apenas por área)
- [ ] O time está treinado para identificar e reportar gargalos proativamente
- [ ] Lições aprendidas de gargalos anteriores são referenciadas em novos casos

## Critérios de Aprovação
- Value stream map atualizado nos últimos 60 dias
- Constraint principal identificado com root cause analysis completa
- Plano de exploit implementado e gerando resultado mensurável
- Plano de elevação definido (se exploit insuficiente) com budget e timeline
- Pelo menos 85% dos itens de todas as seções concluídos
- Throughput do sistema mostrando tendência de melhoria

## O que Fazer se Falhar
1. Se o gargalo não foi identificado: investir em instrumentação e medição do fluxo
2. Se o gargalo é de pessoas: avaliar redistribuição, contratação ou automação
3. Se o gargalo é de processo: simplificar, eliminar etapas, reduzir handoffs
4. Se o gargalo é de decisão: descentralizar autoridade, definir DRIs
5. Realizar workshop de Theory of Constraints com líderes das áreas afetadas
6. Implementar WIP limits imediatamente para evitar sobrecarga do sistema
7. Considerar consultoria especializada se o gargalo for crônico e resistente
8. Re-auditar em 15 dias (ciclo mais curto por ser operacional)

## Referências
- "The Goal" — Eliyahu Goldratt (Theory of Constraints)
- "The Phoenix Project" — Gene Kim
- Value Stream Mapping templates e guias
- Kanban Method — David Anderson
- Throughput metrics dashboards (internal)
- Histórico de gargalos identificados e resolvidos
- "This is Lean" — Niklas Modig & Pär Åhlström
