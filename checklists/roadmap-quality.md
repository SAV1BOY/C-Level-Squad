# Checklist de Qualidade — Roadmap de Produto/Tecnologia

## Propósito
Garantir que o roadmap defina outcomes claros (não apenas features), mapeie dependências entre equipes e sistemas, documente trade-offs de priorização e verifique a capacidade real das equipes antes de comprometer entregas. Este checklist transforma roadmaps de listas de desejos em planos de execução realistas e estrategicamente alinhados.

## Quando Aplicar
- Na criação ou atualização do roadmap trimestral ou semestral
- Antes de apresentar o roadmap a stakeholders (board, investidores, clientes)
- Quando há replanejamento por mudança significativa de contexto
- Na revisão de roadmaps de squads ou product areas para alinhamento
- Quando agentes de produto geram drafts de roadmap para validação

## Agente Responsável
- **Primário:** CPO Agent (Chief Product Officer) ou CTO Agent
- **Co-responsável:** Engineering Lead Agent para viabilidade técnica
- **Revisor:** CEO Agent para alinhamento estratégico
- **Consultor:** CFO Agent para impacto financeiro das prioridades

## Checklist

### Seção 1 — Outcomes Definidos
- [ ] Cada item do roadmap tem um outcome esperado (resultado para o negócio ou usuário)
- [ ] Os outcomes estão expressos em termos de impacto, não de atividade (ex: "reduzir churn em 15%" em vez de "lançar feature X")
- [ ] As métricas de sucesso de cada outcome estão definidas com baseline e target
- [ ] O vínculo entre cada outcome e os OKRs/estratégia está explícito
- [ ] Os outcomes estão priorizados por impacto estratégico e valor para o cliente
- [ ] O método de validação de cada outcome está definido (como saberemos que funcionou)
- [ ] Os outcomes são independentes quando possível (podem ser entregues e medidos separadamente)
- [ ] Outcomes que são hypotheses (ainda não validados) estão sinalizados como tal
- [ ] O impacto financeiro estimado de cada outcome está documentado
- [ ] Os outcomes estão agrupados por tema estratégico para facilitar comunicação

### Seção 2 — Dependências Mapeadas
- [ ] As dependências entre itens do roadmap estão mapeadas visualmente
- [ ] As dependências entre squads/equipes estão identificadas e owners notificados
- [ ] As dependências de plataforma ou infraestrutura estão documentadas
- [ ] As dependências externas (parceiros, fornecedores, APIs de terceiros) estão identificadas
- [ ] O caminho crítico (critical path) está destacado e monitorado
- [ ] As dependências de dados (data pipeline, analytics) estão mapeadas
- [ ] Os riscos de cada dependência estão avaliados (o que acontece se a dependência atrasar)
- [ ] Os planos de desacoplamento estão definidos quando possível (como reduzir dependências)
- [ ] As dependências regulatórias ou de compliance estão incluídas
- [ ] O impacto de mudanças em dependências upstream no roadmap está modelado

### Seção 3 — Trade-offs Documentados
- [ ] Os trade-offs de priorização estão explícitos (o que foi priorizado e o que foi desprioritizado)
- [ ] O framework de priorização utilizado está documentado (RICE, ICE, MoSCoW, etc.)
- [ ] Os itens despriorizados estão listados com justificativa e possível futuro timeline
- [ ] Os trade-offs de scope vs timeline vs quality estão articulados para cada iniciativa
- [ ] O trade-off entre investimento em tech debt vs features novas está explícito
- [ ] O trade-off entre plataforma/infra vs produto está documentado
- [ ] Os stakeholders que serão impactados negativamente por trade-offs estão informados
- [ ] O impacto dos trade-offs em métricas de negócio está estimado
- [ ] Os trade-offs foram validados com o CEO Agent e CFO Agent
- [ ] Existe mecanismo para revisitar trade-offs se premissas mudarem

### Seção 4 — Capacidade Verificada
- [ ] A capacidade real das equipes (story points, throughput histórico) está documentada
- [ ] O buffer para imprevistos está incluído (tipicamente 15-20% do capacity)
- [ ] O impacto de vacações, feriados e onboarding de novos membros está considerado
- [ ] O tempo alocado para tech debt e manutenção está separado e protegido
- [ ] O tempo para suporte, bugs e incidents está estimado e reservado
- [ ] A capacidade foi validada pelos engineering leads (não apenas estimada top-down)
- [ ] O velocity histórico da equipe justifica os commitments feitos
- [ ] O plano de contratação está alinhado com a capacidade necessária para o roadmap
- [ ] Os skills gaps que afetam a capacidade estão identificados com plano de mitigação
- [ ] A sobrecarga (over-commitment) foi verificada e corrigida antes da publicação

### Seção 5 — Comunicação e Transparência
- [ ] O roadmap tem visões adaptadas para diferentes audiências (técnica, executiva, cliente)
- [ ] A legenda e nomenclatura estão claras e consistentes
- [ ] O nível de confiança de cada item está indicado (committed, planned, exploratory)
- [ ] As datas são ranges realistas, não datas fixas falsamente precisas
- [ ] O roadmap está acessível no repositório ou ferramenta oficial
- [ ] O mecanismo de atualização e comunicação de mudanças está definido
- [ ] O roadmap distingue entre o que está committed externamente vs planejamento interno
- [ ] O version control está aplicado com histórico de mudanças preservado

### Seção 6 — Alinhamento e Validação
- [ ] O roadmap está alinhado com o Q-Plan e os OKRs vigentes
- [ ] O roadmap foi revisado por todos os stakeholders-chave antes da publicação
- [ ] Os conflitos de prioridade entre equipes foram resolvidos com arbitragem explícita
- [ ] O roadmap está integrado com o roadmap de outras áreas (marketing, vendas, operações)
- [ ] O feedback de clientes e mercado informou as prioridades do roadmap
- [ ] A revisão do roadmap anterior (retrospectiva) informou o planejamento atual

## Critérios de Aprovação
- 100% dos itens do roadmap têm outcome definido com métricas de sucesso
- Dependências mapeadas e owners notificados
- Trade-offs documentados e validados com stakeholders-chave
- Capacidade verificada e buffer incluído (nenhuma equipe acima de 80% de alocação)
- Roadmap revisado por CPO/CTO Agent e CEO Agent
- Score mínimo de completude: 90% dos itens marcados

## O que Fazer se Falhar
1. Se outcomes não estão claros, não publicar até definição com métricas
2. Se dependências não estão mapeadas, realizar dependency mapping workshop
3. Se capacidade está overcommitted, forçar priorização e cortar escopo
4. Se trade-offs não estão explícitos, documentar antes de comunicar externamente
5. Registrar padrões de falha no RalphLoop para calibrar o próximo ciclo de planejamento
6. Nunca comunicar roadmap como committed sem verificação de capacidade
7. Se o roadmap muda frequentemente, reavaliar o processo de planejamento

## Referências
- Cagan, M. — "Inspired" (roadmap orientado a outcomes)
- Perri, M. — "Escaping the Build Trap" (product-led roadmapping)
- Torres, T. — "Continuous Discovery Habits" (discovery-driven roadmap)
- Template interno: `/templates/roadmap-template.md`
- Capacity planning tool: `/tools/capacity-planner.md`
- Dependency map: `/maps/dependency-map.md`
