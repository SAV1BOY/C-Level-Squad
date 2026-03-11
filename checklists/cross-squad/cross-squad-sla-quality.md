# Checklist de Qualidade de SLAs Cross-Squad (Cross-Squad SLA Quality)

## Propósito
Garantir que os acordos de nível de serviço (SLAs) entre squads estejam definidos
em três dimensões fundamentais: tempo de resposta e entrega, formato e especificação
do entregável, e qualidade esperada do output. Este checklist formaliza as expectativas
entre squads e cria mecanismos de accountability mútua que previnem atrito e retrabalho.

## Quando Aplicar
- No início de cada ciclo de planejamento trimestral (durante PI planning ou equivalente)
- Quando novos squads são criados ou responsabilidades são redistribuídas
- Após incidentes causados por falta de clareza em SLAs entre squads
- Na revisão semestral de efetividade do operating system cross-squad
- Quando feedback de squads indica insatisfação com serviços de outros squads

## Agente Responsável
- **Primário:** Chief of Staff como facilitador e guardião dos SLAs cross-squad
- **Secundário:** Cada Squad Lead como co-signatário dos SLAs do seu squad
- **Revisor:** CEO para arbitragem quando squads não conseguem acordar SLAs

## Checklist

### Seção 1 — Definição de SLAs de Tempo (Time SLAs)
- [ ] Item 1: Cada interação recorrente entre squads tem SLA de tempo definido
- [ ] Item 2: SLA de acknowledgment (confirmação de recebimento) está especificado
- [ ] Item 3: SLA de delivery (prazo de entrega) está especificado e realista
- [ ] Item 4: SLAs diferenciam por prioridade da demanda (P0, P1, P2, P3)
- [ ] Item 5: Tempos de SLA consideram a capacidade real do squad provider
- [ ] Item 6: Horários de atendimento estão definidos (business hours, 24/7 para P0, etc.)
- [ ] Item 7: Buffer para demandas inesperadas está previsto no capacity planning
- [ ] Item 8: SLAs de tempo são medidos automaticamente onde possível (não manualmente)
- [ ] Item 9: Exceções temporárias (ex: durante sprints intensos) estão previstas no acordo
- [ ] Item 10: SLAs foram benchmark com o que é razoável para o tipo de serviço

### Seção 2 — Definição de SLAs de Formato (Format SLAs)
- [ ] Item 11: O formato de request (como pedir) está padronizado com template
- [ ] Item 12: As informações obrigatórias em cada request estão listadas (campos requeridos)
- [ ] Item 13: O formato de delivery (como entregar) está especificado
- [ ] Item 14: Documentação mínima que acompanha a entrega está definida
- [ ] Item 15: Canais de comunicação para requests e deliveries estão padronizados
- [ ] Item 16: O processo de handoff entre squads está descrito passo a passo
- [ ] Item 17: Nomenclatura e taxonomia são consistentes entre squads
- [ ] Item 18: Templates são acessíveis e fáceis de usar (baixa friction)
- [ ] Item 19: Exemplos de requests e deliveries bem-feitos estão disponíveis
- [ ] Item 20: O formato é revisado quando feedback indica problemas de clareza

### Seção 3 — Definição de SLAs de Qualidade (Quality SLAs)
- [ ] Item 21: Critérios de qualidade para cada tipo de entregável estão definidos
- [ ] Item 22: Definition of done para cada tipo de interação cross-squad está documentada
- [ ] Item 23: O nível de completude esperado está especificado (rascunho, revisado, final)
- [ ] Item 24: Padrões de acuracidade estão definidos (margem de erro aceitável)
- [ ] Item 25: Critérios de rejeição estão claros (quando o consumer pode devolver)
- [ ] Item 26: Processo de revisão de qualidade antes da entrega está definido
- [ ] Item 27: Feedback de qualidade é coletado após cada interação significativa
- [ ] Item 28: Métricas de qualidade (rework rate, defect rate) são monitoradas
- [ ] Item 29: Melhoria contínua de qualidade é discutida em retros cross-squad
- [ ] Item 30: Padrões de qualidade são realistas dado o capacity e recursos disponíveis

### Seção 4 — Acordos Bilaterais (Bilateral Agreements)
- [ ] Item 31: Cada SLA é assinado formalmente por ambos os squad leads (provider e consumer)
- [ ] Item 32: O SLA é justo e equilibrado (não impõe carga excessiva em um lado)
- [ ] Item 33: Responsabilidades de ambas as partes estão claras (não apenas do provider)
- [ ] Item 34: O consumer entende o custo de seus requests para o provider
- [ ] Item 35: O provider entende o impacto de falhas de SLA no consumer
- [ ] Item 36: Processo de renegociação de SLAs está definido (como mudar se necessário)
- [ ] Item 37: SLAs são revisados pelo menos semestralmente para adequação
- [ ] Item 38: Conflitos de SLA entre múltiplos consumers do mesmo provider são arbitrados

### Seção 5 — Monitoramento e Reporting de SLAs
- [ ] Item 39: Compliance com SLAs é medida e reportada com frequência mínima mensal
- [ ] Item 40: Dashboard de SLA compliance está disponível para todos os squad leads
- [ ] Item 41: Violações de SLA são registradas com root cause e action items
- [ ] Item 42: Tendência de compliance é rastreada (melhorando, estável, deteriorando)
- [ ] Item 43: SLAs com compliance abaixo de 80% são sinalizados para revisão urgente
- [ ] Item 44: Relatório consolidado de SLA cross-squad é apresentado ao C-Level mensalmente
- [ ] Item 45: Dados de SLA alimentam decisões de capacity planning e priorização

### Seção 6 — Melhoria Contínua de SLAs
- [ ] Item 46: Retrospectiva de SLAs é conduzida pelo menos semestralmente
- [ ] Item 47: SLAs que são consistentemente over-achieved são ajustados para liberar capacidade
- [ ] Item 48: SLAs que são consistentemente under-achieved são analisados (problema de SLA ou de capacidade)
- [ ] Item 49: Automação é implementada para reduzir esforço manual em atendimento de SLAs
- [ ] Item 50: Best practices de squads com alta compliance são compartilhadas como benchmark

## Critérios de Aprovação
Os SLAs cross-squad são considerados adequados quando:

1. **100% das interações recorrentes entre squads têm SLA definido nas 3 dimensões**
2. **SLAs estão assinados bilateralmente por ambos os squad leads (Seção 4)**
3. **Compliance geral com SLAs está acima de 85% (Seção 5)**
4. **Dashboard de monitoramento está funcional e atualizado (Seção 5)**
5. **Violações de SLA têm root cause documentada e action items**
6. **Retrospectiva de SLAs foi conduzida no último semestre (Seção 6)**
7. **O Chief of Staff validou os SLAs como adequados e justos**

## O que Fazer se Falhar
Se os SLAs cross-squad não atingem os critérios:

1. **SLA definition workshop:** Reunir squad leads para definir ou redefinir SLAs faltantes
2. **Capacity review:** Se compliance é baixa, avaliar se o problema é de capacidade
3. **SLA right-sizing:** Se SLAs são irrealistas, ajustar para níveis atingíveis e melhorar gradualmente
4. **Tooling investment:** Se medição é manual e imprecisa, investir em automação
5. **Chief of Staff mediation:** Mediar entre squads que não conseguem acordar SLAs
6. **Incentive alignment:** Garantir que compliance com SLAs está nas métricas de cada squad
7. **CEO arbitration:** Se conflitos persistem, CEO arbitra prioridades e alocação
8. **Structural review:** Se SLAs falham sistematicamente, revisar se a estrutura de squads é adequada

## Referências
- ITIL — Service Level Management framework
- Team Topologies — Matthew Skelton & Manuel Pais (team APIs and interaction modes)
- SRE — Google Site Reliability Engineering (SLA/SLO/SLI framework)
- Framework interno de Cross-Squad SLA Management (documento em /cross-squad/)
- Template de SLA Agreement (documento em /templates/sla-template.md)
- Dashboard de SLA Compliance (link: /dashboards/sla-compliance)
- Ownership Map (documento em /cross-squad/ownership-map.md)
