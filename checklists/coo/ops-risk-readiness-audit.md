# Ops Risk Readiness Audit

## Propósito
Verificar que a organização está preparada para riscos operacionais: runbooks existem e estão testados, back-ups de processos e pessoas estão definidos, e drills (simulações) são realizados regularmente. Preparação para risco não é paranoia — é profissionalismo operacional.

## Quando Aplicar
- Trimestralmente como parte do ciclo de gestão de riscos
- Após qualquer incidente operacional significativo (post-mortem trigger)
- Antes de períodos de alta demanda ou sazonalidade
- Quando houver mudanças significativas na infraestrutura ou processos
- Quando novos riscos forem identificados por qualquer área da organização

## Agente Responsável
**Agente COO (Chief Operating Officer Agent)** — responsável por garantir a preparação operacional para cenários de risco e a capacidade de resposta da organização.

## Checklist

### Seção 1: Inventário de Riscos Operacionais
- [ ] Mapa de riscos operacionais existe e está atualizado nos últimos 90 dias
- [ ] Riscos estão classificados por probabilidade e impacto (matriz de risco)
- [ ] Os 10 maiores riscos operacionais estão identificados e priorizados
- [ ] Cada risco tem owner designado responsável pela mitigação
- [ ] Riscos de terceiros e fornecedores estão incluídos no mapeamento
- [ ] Riscos regulatórios e de compliance estão mapeados
- [ ] Riscos de pessoas (key person risk) estão identificados
- [ ] O mapa de riscos é revisado em fórum de liderança pelo menos trimestralmente

### Seção 2: Runbooks e Procedimentos de Resposta
- [ ] Runbook existe para cada um dos 10 maiores riscos operacionais
- [ ] Cada runbook contém: trigger, passos de resposta, escalação, comunicação
- [ ] Runbooks são acionáveis por qualquer membro treinado (não apenas experts)
- [ ] Contact lists de emergência estão atualizadas e acessíveis offline
- [ ] Procedimentos de comunicação de crise estão definidos (interna e externa)
- [ ] Runbooks incluem critérios de severidade e níveis de escalação
- [ ] Templates de comunicação para diferentes cenários estão pré-aprovados
- [ ] Runbooks estão versionados com data da última revisão e teste

### Seção 3: Back-ups e Redundância
- [ ] Cada processo crítico tem pelo menos 1 pessoa de back-up treinada
- [ ] Documentação permite que back-ups assumam sem dependência do titular
- [ ] Acessos e permissões de back-up estão configurados preventivamente
- [ ] Fornecedores críticos têm alternativas identificadas (vendor diversification)
- [ ] Dados críticos têm back-up testado e recovery time validado
- [ ] Sistemas críticos têm failover ou degradation plan documentado
- [ ] Cash reserves ou linhas de crédito estão disponíveis para emergências
- [ ] Informações críticas não estão concentradas em um único repositório

### Seção 4: Drills e Simulações
- [ ] Pelo menos 1 drill/simulação foi realizado nos últimos 90 dias
- [ ] O cenário do drill era realista e baseado em riscos mapeados
- [ ] Participantes do drill incluíram decision-makers relevantes
- [ ] O tempo de resposta foi medido e comparado com o target
- [ ] Gaps identificados no drill foram documentados e corrigidos
- [ ] Runbooks foram atualizados com base nos aprendizados do drill
- [ ] O drill testou comunicação além de execução técnica
- [ ] Próximo drill está agendado com cenário definido
- [ ] Resultados de drills são reportados ao C-Level

### Seção 5: Post-Mortem e Aprendizado
- [ ] Todo incidente significativo gera um post-mortem formal
- [ ] Post-mortems são blameless (focam em sistema, não em pessoas)
- [ ] Cada post-mortem gera action items com owners e prazos
- [ ] Action items de post-mortems têm taxa de conclusão >90%
- [ ] Aprendizados são compartilhados com toda a organização relevante
- [ ] Padrões recorrentes de incidentes são identificados e tratados na raiz
- [ ] Existe um repositório de post-mortems acessível para aprendizado
- [ ] Métricas de incidentes (MTTR, frequência, impacto) são acompanhadas

## Critérios de Aprovação
- Mapa de riscos atualizado nos últimos 90 dias com top 10 priorizados
- Runbooks existem para 100% dos top 10 riscos
- Pelo menos 1 drill realizado nos últimos 90 dias com resultados documentados
- Zero single points of failure em processos críticos
- Pelo menos 85% dos itens de todas as seções concluídos
- Post-mortems de incidentes recentes com action items >90% concluídos

## O que Fazer se Falhar
1. Priorizar: criar runbooks para os top 3 riscos sem cobertura imediatamente
2. Agendar drill de emergência nos próximos 30 dias
3. Identificar e resolver single points of failure em processos críticos
4. Atualizar mapa de riscos com participação multifuncional
5. Designar owners de risco para itens sem responsável
6. Implementar cadência mensal de revisão de riscos até estabilizar
7. Investir em treinamento de resposta a incidentes para liderança
8. Re-auditar em 30 dias com foco nos gaps mais críticos

## Referências
- Mapa de Riscos Operacionais (internal wiki)
- Repositório de Runbooks (internal wiki)
- Histórico de Post-Mortems
- "The Phoenix Project" — Gene Kim (gestão de operações e riscos)
- ISO 22301 — Business Continuity Management
- NIST Cybersecurity Framework (aspectos operacionais)
- Incident management best practices (PagerDuty, Google SRE)
