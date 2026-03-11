# Checklist de Auditoria de Routing Cross-Squad (Cross-Squad Routing Audit)

## Propósito
Garantir que o roteamento de demandas, decisões e informações entre squads esteja
funcionando corretamente — que o squad certo seja acionado no momento certo com o
contexto adequado. Este checklist identifica falhas de routing que causam atrasos,
retrabalho e frustração entre equipes.

## Quando Aplicar
- Na auditoria trimestral de efetividade do operating system
- Quando incidentes cross-squad revelam falhas de roteamento
- Após reorganizações que mudam responsabilidades entre squads
- Quando feedback recorrente indica confusão sobre "quem faz o quê"
- Na revisão semestral de RACI e ownership maps

## Agente Responsável
- **Primário:** Chief of Staff como orquestrador do operating system cross-squad
- **Secundário:** Cada Squad Lead para routing de entrada e saída do seu squad
- **Revisor:** CEO para validação do modelo de routing organizacional

## Checklist

### Seção 1 — Mapeamento de Routing (Routing Map)
- [ ] Item 1: O mapa de responsabilidades (ownership map) entre squads está documentado e atualizado
- [ ] Item 2: Para cada tipo de demanda comum, o squad responsável está claramente indicado
- [ ] Item 3: Zonas cinzentas (gray areas) de responsabilidade foram identificadas e resolvidas
- [ ] Item 4: O ownership map está acessível a todos os membros do C-Level Squad
- [ ] Item 5: Mudanças no ownership map são comunicadas proativamente quando ocorrem
- [ ] Item 6: Cada squad tem um ponto de contato único (single point of contact) para routing externo
- [ ] Item 7: O catálogo de serviços de cada squad está documentado (o que cada squad entrega)
- [ ] Item 8: Interfaces entre squads (inputs esperados, outputs entregues) estão definidas

### Seção 2 — Qualidade do Routing (Routing Quality)
- [ ] Item 9: Demandas estão chegando ao squad correto na primeira tentativa (first-touch accuracy)
- [ ] Item 10: O tempo entre uma demanda surgir e chegar ao squad correto está dentro do SLA
- [ ] Item 11: Demandas roteadas incorretamente são redirecionadas em até 24 horas
- [ ] Item 12: O contexto necessário acompanha a demanda (não chega "pelada" ao squad destino)
- [ ] Item 13: A prioridade da demanda é classificada pelo solicitante e validada pelo squad destino
- [ ] Item 14: Demandas duplicadas (enviadas a múltiplos squads) são identificadas e consolidadas
- [ ] Item 15: Feedback sobre routing incorreto é capturado e usado para melhorar o mapa
- [ ] Item 16: O volume de rerouting (demandas que mudam de squad) é monitorado como indicador

### Seção 3 — Timing de Acionamento (Timing Quality)
- [ ] Item 17: Squads são acionados no momento correto do processo (não muito cedo, não muito tarde)
- [ ] Item 18: Critérios de quando acionar cada squad estão documentados (trigger criteria)
- [ ] Item 19: Acionamentos de última hora (urgências evitáveis) são monitorados e reduzidos
- [ ] Item 20: Lead time necessário para cada tipo de demanda por squad está definido
- [ ] Item 21: Acionamentos proativos (antes de virar urgência) são incentivados e praticados
- [ ] Item 22: O calendário de cadências cross-squad garante pontos regulares de sincronização
- [ ] Item 23: Dependências com timing crítico têm alertas ou reminders automáticos

### Seção 4 — Resolução de Conflitos de Routing
- [ ] Item 24: Quando dois squads disputam ownership, existe processo claro de resolução
- [ ] Item 25: O Chief of Staff arbitra conflitos de routing em até 48 horas
- [ ] Item 26: Conflitos de routing resolvidos atualizam permanentemente o ownership map
- [ ] Item 27: Demandas que nenhum squad quer assumir têm processo de atribuição
- [ ] Item 28: Conflitos de prioridade entre squads são escalados com framework definido
- [ ] Item 29: Histórico de conflitos de routing é mantido para identificar padrões
- [ ] Item 30: Ajustes estruturais são propostos quando conflitos são recorrentes

### Seção 5 — Ferramentas e Processos de Routing
- [ ] Item 31: Existe um canal padronizado para routing de demandas entre squads (não ad-hoc)
- [ ] Item 32: Templates de request entre squads existem e são usados (context, priority, deadline)
- [ ] Item 33: O workflow de routing está parcial ou totalmente automatizado onde possível
- [ ] Item 34: Visibilidade do status de demandas cross-squad existe para ambos os lados
- [ ] Item 35: Métricas de routing (volume, accuracy, SLA compliance) são dashboarded
- [ ] Item 36: O processo de routing é revisado e simplificado trimestralmente

### Seção 6 — Efetividade Geral do Routing
- [ ] Item 37: Survey de satisfação com routing cross-squad é conduzida semestralmente
- [ ] Item 38: First-touch routing accuracy está acima de 85%
- [ ] Item 39: Tempo médio de rerouting (quando necessário) está abaixo de 24 horas
- [ ] Item 40: Volume de escalações por routing incorreto está diminuindo quarter-over-quarter
- [ ] Item 41: Novos membros da organização entendem o routing em seu primeiro mês
- [ ] Item 42: O modelo de routing suporta a escala atual da organização
- [ ] Item 43: Plano de evolução do routing para o próximo estágio de escala existe

## Critérios de Aprovação
O routing cross-squad é considerado saudável quando:

1. **Ownership map está 100% atualizado e acessível (Seção 1)**
2. **First-touch routing accuracy está acima de 85% (Seção 6)**
3. **Tempo de rerouting está dentro do SLA de 24 horas**
4. **Conflitos de routing são resolvidos em até 48 horas (Seção 4)**
5. **Survey de satisfação mostra score acima de 7/10**
6. **O Chief of Staff validou o mapa de routing no último trimestre**
7. **Nenhuma zona cinzenta significativa permanece sem resolução**

## O que Fazer se Falhar
Se o routing cross-squad não atinge os critérios:

1. **Ownership map workshop:** Reunir todos os squad leads para atualizar o mapa
2. **Gray area resolution sprint:** Dedicar uma sessão para resolver todas as zonas cinzentas
3. **Routing training:** Treinar times sobre como rotear corretamente e que informações incluir
4. **Process simplification:** Se o routing é muito complexo, simplificar canais e processos
5. **Chief of Staff empowerment:** Dar ao Chief of Staff autoridade para arbitrar rapidamente
6. **Automation:** Investir em automação de routing onde volume justifica
7. **Structural change:** Se routing crônico falha, considerar reorganização de squads
8. **Feedback loop:** Implementar mecanismo fácil para reportar routing incorreto

## Referências
- Team Topologies — Matthew Skelton & Manuel Pais (team interaction modes)
- ITIL — Service catalog and routing practices
- Spotify Model — Squad dependencies and interactions
- Framework interno de Cross-Squad Operating System (documento em /operating-system/)
- Ownership Map (documento em /cross-squad/ownership-map.md)
- Template de Cross-Squad Request (documento em /templates/)
