# Systems Portfolio Audit

## Propósito
Avaliar o portfolio de sistemas da organização: inventário completo, redundâncias identificadas e riscos mapeados. Um portfolio de sistemas não gerido acumula redundâncias, custos ocultos e riscos de segurança. Cada sistema sem owner é um passivo, não um ativo.

## Quando Aplicar
- Semestralmente como revisão estratégica de TI
- Quando custos de licenciamento estiverem crescendo sem justificativa proporcional
- Quando integrações entre sistemas começarem a falhar com frequência
- Após fusões, aquisições ou reorganizações que tragam novos sistemas
- Quando novos sistemas forem propostos para aquisição

## Agente Responsável
**Agente CIO (Chief Information Officer Agent)** — responsável por manter um portfolio de sistemas racional, eficiente e alinhado com as necessidades do negócio.

## Checklist

### Seção 1: Inventário de Sistemas
- [ ] Todos os sistemas em uso estão catalogados em registry centralizado
- [ ] Cada sistema tem: nome, vendor, versão, owner, custo, propósito documentados
- [ ] Sistemas são classificados por criticidade: mission-critical, important, nice-to-have
- [ ] Cada sistema tem número de usuários ativos rastreado
- [ ] Sistemas shadow IT (não sancionados) foram identificados e avaliados
- [ ] Sistemas legacy estão identificados com plano de modernização ou decommission
- [ ] O inventário inclui SaaS, on-premise, custom-built e planilhas críticas
- [ ] A última atualização do inventário foi há menos de 90 dias

### Seção 2: Análise de Redundâncias
- [ ] Sistemas com funcionalidades sobrepostas estão identificados
- [ ] O custo de manter redundâncias está calculado
- [ ] Para cada redundância, a decisão de consolidar ou manter está documentada
- [ ] Não há mais de 2 sistemas para a mesma funcionalidade core
- [ ] Dados duplicados entre sistemas estão mapeados e os riscos avaliados
- [ ] Plano de consolidação para redundâncias prioritárias existe e tem timeline
- [ ] Usuários afetados por consolidação foram comunicados e estão preparados
- [ ] O custo de consolidação vs. o custo de manter redundância foi comparado

### Seção 3: Avaliação de Riscos
- [ ] Cada sistema tem risk assessment atualizado
- [ ] Sistemas com vendor único de alto risco (single vendor dependency) estão identificados
- [ ] Sistemas end-of-life ou sem suporte do vendor estão identificados
- [ ] Riscos de segurança por sistema estão avaliados (compliance, vulnerabilidades)
- [ ] Disponibilidade e SLA de cada sistema crítico são monitorados
- [ ] Plano de contingência existe para falha de cada sistema mission-critical
- [ ] Integrações frágeis entre sistemas estão identificadas como pontos de risco
- [ ] Dados sensíveis armazenados em cada sistema estão mapeados

### Seção 4: Lifecycle Management
- [ ] Cada sistema tem fase do lifecycle identificada (deploy, mature, retire)
- [ ] Sistemas em fase de retire têm plano de decommission com timeline
- [ ] Novos sistemas passam por processo de avaliação antes de aquisição
- [ ] Contratos e licenças têm renovação tracking ativo
- [ ] Datas de renovação são alertadas com antecedência mínima de 90 dias
- [ ] Avaliação de alternativas é realizada antes de cada renovação significativa
- [ ] Sistemas que não são mais usados ativamente são identificados e removidos
- [ ] Custos por lifecycle phase são rastreados (investment, operation, retirement)

### Seção 5: Alinhamento com Negócio
- [ ] Cada sistema está conectado a pelo menos 1 processo de negócio documentado
- [ ] Sistemas que não suportam processos de negócio atuais estão questionados
- [ ] O roadmap de sistemas está alinhado com o roadmap do negócio
- [ ] Necessidades de negócio não atendidas por sistemas existentes estão mapeadas
- [ ] Satisfação dos usuários com os sistemas principais é medida
- [ ] Gap analysis entre capabilities necessárias e capabilities existentes foi realizada
- [ ] Investimento em sistemas é proporcional ao valor do processo que suportam
- [ ] O CIO tem visibilidade sobre necessidades futuras de sistemas por área

## Critérios de Aprovação
- Inventário 100% atualizado com todos os sistemas catalogados
- Zero sistemas mission-critical sem owner designado
- Redundâncias identificadas com plano de consolidação para as top 5
- Risk assessment atualizado para todos os sistemas críticos
- Pelo menos 85% dos itens de todas as seções concluídos
- Lifecycle management ativo com tracking de contratos e renovações

## O que Fazer se Falhar
1. Se inventário não existe: realizar discovery sprint de 2 semanas
2. Se redundâncias são excessivas: priorizar consolidação por custo e risco
3. Se sistemas críticos estão sem owner: designar owners imediatamente
4. Se riscos não estão avaliados: começar pelos sistemas que processam dados sensíveis
5. Implementar processo obrigatório de avaliação para novas aquisições de sistemas
6. Criar dashboard de portfolio de sistemas visível para liderança
7. Engajar procurement para renegociar contratos de sistemas subutilizados
8. Re-auditar em 45 dias com foco nos sistemas de maior risco e custo

## Referências
- ITIL Service Asset and Configuration Management
- Systems Registry (internal wiki)
- Vendor management policies
- "Enterprise Architecture as Strategy" — Jeanne Ross et al.
- License and contract registry
- Security assessment reports por sistema
- Gartner/Forrester evaluation reports
