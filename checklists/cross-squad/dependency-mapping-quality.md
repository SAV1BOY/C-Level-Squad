# Checklist de Qualidade de Mapeamento de Dependências (Dependency Mapping Quality)

## Propósito
Garantir que todas as dependências entre squads estejam documentadas, com SLAs
definidos e mecanismos de monitoramento ativos. Este checklist previne que dependências
não gerenciadas se tornem blockers invisíveis que atrasam entregas e geram conflitos
entre equipes.

## Quando Aplicar
- No início de cada ciclo de planejamento (quarterly planning)
- Quando novas iniciativas cross-squad são iniciadas
- Na revisão mensal de portfólio de projetos cross-squad
- Após incidentes causados por dependências não gerenciadas
- Quando reorganizações mudam a estrutura de squads

## Agente Responsável
- **Primário:** Chief of Staff como orquestrador de dependências cross-squad
- **Secundário:** Cada Squad Lead para dependências de entrada e saída do seu squad
- **Revisor:** CEO para resolução de conflitos de dependência de alto nível

## Checklist

### Seção 1 — Inventário de Dependências (Dependency Inventory)
- [ ] Item 1: Todas as dependências entre squads estão listadas em um registro central
- [ ] Item 2: Cada dependência tem um squad provider (quem entrega) e consumer (quem consome)
- [ ] Item 3: O tipo de dependência está classificado (dados, serviço, decisão, recurso, expertise)
- [ ] Item 4: A criticidade de cada dependência está avaliada (alta, média, baixa)
- [ ] Item 5: A frequência da dependência está documentada (one-time, recorrente, contínua)
- [ ] Item 6: Dependências novas são adicionadas ao registro conforme surgem
- [ ] Item 7: Dependências resolvidas ou eliminadas são arquivadas com documentação
- [ ] Item 8: O inventário é revisado integralmente pelo menos uma vez por trimestre

### Seção 2 — SLAs de Dependência (Dependency SLAs)
- [ ] Item 9: Cada dependência de alta criticidade tem SLA definido e acordado entre as partes
- [ ] Item 10: O SLA inclui prazo de resposta (response time) e prazo de entrega (delivery time)
- [ ] Item 11: O formato e a qualidade esperada do entregável estão especificados no SLA
- [ ] Item 12: O processo de request (como pedir) está padronizado e documentado
- [ ] Item 13: Exceções ao SLA e como tratá-las estão previstas
- [ ] Item 14: SLAs foram acordados bilateralmente (não impostos unilateralmente)
- [ ] Item 15: SLAs são revisados e ajustados pelo menos semestralmente
- [ ] Item 16: O custo de atender cada SLA está estimado pelo squad provider

### Seção 3 — Monitoramento de Dependências
- [ ] Item 17: Compliance com SLAs é medida e reportada mensalmente
- [ ] Item 18: Desvios de SLA geram alertas para ambos os squads (provider e consumer)
- [ ] Item 19: Tendências de compliance estão sendo rastreadas (melhorando ou piorando)
- [ ] Item 20: Blockers causados por dependências são registrados com impacto quantificado
- [ ] Item 21: O número total de dependências ativas é monitorado (muitas é sinal de problema)
- [ ] Item 22: Dependências de alto risco (único provider, sem backup) estão sinalizadas
- [ ] Item 23: Dashboard de dependências está acessível para todo o C-Level Squad

### Seção 4 — Gestão de Riscos de Dependência
- [ ] Item 24: Dependências de single point of failure estão identificadas
- [ ] Item 25: Para cada dependência crítica, existe um plano B (alternativa se falhar)
- [ ] Item 26: A capacidade do squad provider é compatível com o volume de demandas
- [ ] Item 27: Quando um squad está sobrecarregado de dependências, a situação é escalada
- [ ] Item 28: Impacto de indisponibilidade de cada dependência foi estimado
- [ ] Item 29: Dependências circulares (A depende de B que depende de A) foram eliminadas
- [ ] Item 30: Dependências externas (vendors, partners) estão incluídas no mapeamento

### Seção 5 — Redução de Dependências
- [ ] Item 31: Há uma meta ativa para reduzir o número de dependências entre squads
- [ ] Item 32: Self-service é implementado onde possível (squad consumer resolve sozinho)
- [ ] Item 33: APIs e interfaces padronizadas reduzem dependência de interação humana
- [ ] Item 34: Documentação permite que squads resolvam questões simples sem acionar o provider
- [ ] Item 35: A arquitetura organizacional é avaliada para minimizar dependências desnecessárias
- [ ] Item 36: Transferência de conhecimento ocorre para eliminar dependências de expertise
- [ ] Item 37: Dependências que existem apenas por razões históricas são candidatas a eliminação

### Seção 6 — Comunicação e Alinhamento
- [ ] Item 38: Reunião periódica cross-squad de sincronização de dependências existe
- [ ] Item 39: Mudanças no roadmap que afetam dependências são comunicadas com antecedência
- [ ] Item 40: O impacto de mudanças de prioridade em dependências é avaliado antes da decisão
- [ ] Item 41: Provider e consumer têm visibilidade mútua de roadmaps e prioridades
- [ ] Item 42: Conflitos de prioridade em dependências são escalados com processo claro
- [ ] Item 43: Retrospectiva de dependências é conduzida ao final de cada ciclo de planning

## Critérios de Aprovação
O mapeamento de dependências é considerado saudável quando:

1. **100% das dependências de alta criticidade estão no inventário (Seção 1)**
2. **SLAs estão definidos e acordados para todas as dependências de alta criticidade (Seção 2)**
3. **Compliance com SLAs está acima de 85% (Seção 3)**
4. **Dependências de single point of failure têm plano B (Seção 4)**
5. **O número total de dependências está estável ou diminuindo (Seção 5)**
6. **Dashboard de dependências está funcional e atualizado (Seção 3)**
7. **O Chief of Staff validou o mapeamento no último trimestre**

## O que Fazer se Falhar
Se o mapeamento de dependências não atinge os critérios:

1. **Dependency mapping session:** Reunir todos os squad leads para atualizar o inventário
2. **SLA negotiation:** Facilitar negociação de SLAs para dependências sem acordo
3. **Capacity review:** Avaliar se squads providers estão com capacidade adequada
4. **Dependency reduction sprint:** Identificar e eliminar dependências desnecessárias
5. **Automation:** Investir em automação de interfaces entre squads
6. **Architecture review:** Se dependências são excessivas, revisar arquitetura organizacional
7. **Chief of Staff intervention:** Chief of Staff média conflitos de prioridade ativamente
8. **Escalation to CEO:** Se conflitos persistem, CEO arbitra alocação de capacidade

## Referências
- Team Topologies — Matthew Skelton & Manuel Pais (minimizing cognitive load)
- SAFe — Scaled Agile Framework (dependency management in PI planning)
- Spotify Model — Squad autonomy and dependency reduction
- Framework interno de Cross-Squad Dependencies (documento em /cross-squad/)
- Template de Dependency Register (documento em /templates/)
- Template de SLA Agreement (documento em /templates/sla-template.md)
