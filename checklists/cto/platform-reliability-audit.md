# Platform Reliability Audit

## Propósito
Avaliar a confiabilidade da plataforma: SLOs e SLIs definidos e cumpridos, gestão de incidentes eficaz e observabilidade adequada para detectar e resolver problemas rapidamente. Reliability é uma feature — sem ela, nenhuma outra feature importa.

## Quando Aplicar
- Mensalmente como parte da revisão de operações de engenharia
- Após qualquer incidente de severidade alta (P1/P2)
- Quando SLOs estiverem sendo violados consistentemente
- Antes de eventos de alta demanda (lançamentos, sazonalidade)
- Quando clientes reportarem problemas de disponibilidade ou performance

## Agente Responsável
**Agente CTO (Chief Technology Officer Agent)** — responsável por garantir que a plataforma atende aos padrões de confiabilidade necessários para o negócio.

## Checklist

### Seção 1: SLOs e SLIs
- [ ] SLOs (Service Level Objectives) estão definidos para todos os serviços críticos
- [ ] SLIs (Service Level Indicators) estão instrumentados e coletados automaticamente
- [ ] SLOs estão alinhados com as necessidades do negócio (não são arbitrários)
- [ ] Error budget está calculado e rastreado para cada serviço
- [ ] Error budget policy está definida (o que acontece quando esgota)
- [ ] SLOs são revisados trimestralmente e ajustados se necessário
- [ ] SLOs cobrem: availability, latency, throughput, correctness
- [ ] Clientes internos e externos conhecem os SLOs e como verificá-los
- [ ] Histórico de compliance com SLOs está documentado e visível

### Seção 2: Gestão de Incidentes
- [ ] Processo de gestão de incidentes está definido e documentado
- [ ] Severidades estão classificadas (P1, P2, P3, P4) com critérios claros
- [ ] Escalation path está definido para cada nível de severidade
- [ ] On-call rotation está ativa com cobertura 24/7 para serviços críticos
- [ ] Runbooks de resposta existem para cenários de incidente conhecidos
- [ ] MTTD (Mean Time to Detect) é rastreado e otimizado
- [ ] MTTR (Mean Time to Recover) é rastreado e dentro do target
- [ ] Comunicação durante incidentes segue processo definido (stakeholders, clientes)
- [ ] Post-mortems são realizados para todos os incidentes P1/P2
- [ ] Action items de post-mortems são rastreados até conclusão

### Seção 3: Observabilidade
- [ ] Os 3 pilares estão implementados: logs, metrics, traces
- [ ] Logs são estruturados, centralizados e pesquisáveis
- [ ] Métricas de sistema e aplicação são coletadas em real-time
- [ ] Distributed tracing está implementado para requests cross-service
- [ ] Dashboards de saúde existem para todos os serviços críticos
- [ ] Alertas estão configurados para anomalias e thresholds críticos
- [ ] Alert fatigue é gerenciada — alertas são acionáveis e com baixo false positive rate
- [ ] Synthetic monitoring está ativo para flows críticos do usuário

### Seção 4: Disaster Recovery e Resiliência
- [ ] DR plan está documentado com RTO e RPO definidos
- [ ] Backups são realizados com frequência adequada e testados regularmente
- [ ] Recovery foi testado nos últimos 90 dias (não apenas backup, mas restore)
- [ ] Failover para região/zona secundária está configurado e testado
- [ ] Chaos engineering ou fault injection são praticados (mesmo que básico)
- [ ] Dependências externas (APIs, SaaS) têm fallback ou degradation plan
- [ ] Circuit breakers estão implementados para dependências não confiáveis
- [ ] Capacity planning é realizado trimestralmente

### Seção 5: Cultura de Reliability
- [ ] Reliability é tratada como feature, não como overhead
- [ ] Engenheiros participam de on-call e entendem o impacto operacional
- [ ] Reliability work é priorizado no roadmap junto com features
- [ ] Métricas de reliability são visíveis para toda a engenharia
- [ ] Blameless post-mortems são a norma cultural
- [ ] Investimento em reliability é proporcional ao impacto no negócio
- [ ] O time de SRE/platform tem mandato e recursos adequados
- [ ] Reliability goals são parte dos objetivos de engenharia (OKRs, KPIs)

## Critérios de Aprovação
- SLOs definidos para 100% dos serviços críticos com compliance >99%
- MTTR dentro do target para cada nível de severidade
- Observabilidade completa (logs, metrics, traces) para serviços críticos
- DR testado nos últimos 90 dias com resultado documentado
- Pelo menos 85% dos itens de todas as seções concluídos
- Zero incidentes P1 sem post-mortem e action items

## O que Fazer se Falhar
1. Priorizar por impacto no cliente: disponibilidade > latência > features
2. Se SLOs não existem: definir para os top 5 serviços mais críticos em 2 semanas
3. Se observabilidade é fraca: implementar métricas básicas e alertas primeiro
4. Se incidentes recorrem: investir em automação de detecção e recovery
5. Se DR não foi testado: agendar DR drill nos próximos 30 dias
6. Considerar contratação de SRE se não houver capability interna
7. Implementar error budget policy para forçar investimento em reliability
8. Re-auditar em 30 dias com foco nos serviços mais críticos

## Referências
- "Site Reliability Engineering" — Google (SRE Book)
- "Implementing Service Level Objectives" — Alex Hidalgo
- Incident management runbooks (internal wiki)
- Post-mortem repository (internal)
- SLO dashboard
- "Release It!" — Michael Nygard
- PagerDuty Incident Response documentation
