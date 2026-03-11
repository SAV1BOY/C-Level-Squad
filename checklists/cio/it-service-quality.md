# IT Service Quality

## Propósito
Avaliar a qualidade dos serviços de TI usando princípios ITIL como referência: gestão de incidentes, gestão de mudanças, gestão de problemas e cumprimento de SLAs. Serviço de TI de baixa qualidade impacta toda a organização — é infraestrutura invisível até que falhe.

## Quando Aplicar
- Mensalmente como revisão de operações de TI
- Quando satisfação dos usuários internos com TI estiver abaixo do aceitável
- Quando incidentes de TI estiverem impactando produtividade recorrentemente
- Após mudanças que causaram interrupções inesperadas
- Quando SLAs de TI estiverem sendo descumpridos

## Agente Responsável
**Agente CIO (Chief Information Officer Agent)** — responsável pela qualidade e confiabilidade dos serviços de TI entregues à organização.

## Checklist

### Seção 1: Gestão de Incidentes (Incident Management)
- [ ] Processo de gestão de incidentes está definido e documentado
- [ ] Canal de reporte de incidentes é claro e acessível a todos os usuários
- [ ] Classificação de severidade está definida com critérios objetivos
- [ ] SLA de resposta está definido por severidade e é cumprido (>90%)
- [ ] SLA de resolução está definido por severidade e é cumprido (>85%)
- [ ] Escalonamento automático ocorre quando SLA está em risco
- [ ] Comunicação proativa com usuários afetados é realizada durante incidentes
- [ ] Métricas de incidentes (volume, MTTR, MTBF) são rastreadas e reportadas
- [ ] Incidentes recorrentes são identificados e escalados para Problem Management
- [ ] Satisfação do usuário com resolução de incidentes é medida (CSAT)

### Seção 2: Gestão de Mudanças (Change Management)
- [ ] Processo de change management está definido para mudanças em sistemas de TI
- [ ] Mudanças são classificadas: standard, normal, emergency
- [ ] Standard changes têm processo simplificado e pré-aprovado
- [ ] Normal changes passam por avaliação de impacto e risco antes de implementação
- [ ] Emergency changes têm processo expedito com post-review obrigatória
- [ ] Change calendar é mantido e consultado para evitar conflitos
- [ ] Rollback plan é obrigatório para toda mudança significativa
- [ ] Taxa de sucesso de mudanças é rastreada (target: >95%)
- [ ] Mudanças que causam incidentes são analisadas para melhoria

### Seção 3: Gestão de Problemas (Problem Management)
- [ ] Problemas (root causes de incidentes recorrentes) são investigados proativamente
- [ ] Known errors database existe e é mantida atualizada
- [ ] Root cause analysis é realizada para problemas de alto impacto
- [ ] Workarounds são documentados e comunicados enquanto o fix permanente não está pronto
- [ ] Problemas resolvidos são verificados e fechados formalmente
- [ ] Tendências de problemas são analisadas para prevenção
- [ ] O backlog de problemas abertos é gerido e priorizado
- [ ] Problemas críticos têm deadline de resolução definido

### Seção 4: SLAs e Service Catalog
- [ ] Service catalog existe e documenta todos os serviços de TI oferecidos
- [ ] Cada serviço tem SLA definido (disponibilidade, tempo de resposta, suporte)
- [ ] SLAs são mensuráveis, rastreados e reportados
- [ ] Compliance com SLAs é acima de 90% para serviços críticos
- [ ] Usuários conhecem os serviços disponíveis e como solicitá-los
- [ ] Serviços são revisados periodicamente para relevância e qualidade
- [ ] Custo por serviço é conhecido (ou estimado) para FinOps
- [ ] Self-service portal está disponível para requests comuns

### Seção 5: Satisfação e Melhoria Contínua
- [ ] Satisfação dos usuários com serviços de TI é medida regularmente
- [ ] Score de satisfação está acima do target definido (ex: >7/10)
- [ ] Top 3 reclamações são conhecidas e têm plano de melhoria
- [ ] Feedback é coletado após resolução de incidentes e requests
- [ ] Melhorias implementadas com base em feedback são documentadas
- [ ] Benchmarking de serviços de TI contra melhores práticas é realizado
- [ ] Report de qualidade de serviço é apresentado à liderança mensalmente
- [ ] O time de TI é capacitado e tem recursos adequados para atender a demanda

## Critérios de Aprovação
- SLAs de incidentes cumpridos em >90% dos casos
- Taxa de sucesso de mudanças >95%
- Service catalog atualizado e acessível
- Satisfação dos usuários >7/10
- Pelo menos 85% dos itens de todas as seções concluídos
- Zero incidentes recorrentes sem Problem Management ativo

## O que Fazer se Falhar
1. Priorizar: resolução de incidentes recorrentes primeiro (maior impacto na satisfação)
2. Se SLAs são descumpridos: analisar capacity e processo — falta de recurso ou de processo?
3. Se satisfação é baixa: coletar feedback qualitativo direto com usuários afetados
4. Se change management é fraco: implementar processo mínimo antes de escalar
5. Criar service catalog mínimo se não existir (top 10 serviços)
6. Investir em self-service para reduzir carga do time de TI
7. Considerar outsourcing parcial se demand exceder capacity interna
8. Re-auditar em 30 dias com foco nos SLAs e satisfação

## Referências
- ITIL 4 Foundation (framework de referência)
- Service Catalog (internal wiki)
- SLA Registry e compliance reports
- User satisfaction survey results
- Incident and change management tool reports
- "The Phoenix Project" — Gene Kim
- "IT Service Management" — ITIL official publications
