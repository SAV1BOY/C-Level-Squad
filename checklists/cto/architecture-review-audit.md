# Architecture Review Audit

## Propósito
Avaliar a qualidade da arquitetura de software e sistemas da organização em quatro dimensões críticas: modularidade, escalabilidade, custo e segurança. Decisões de arquitetura são as mais caras de reverter — investir tempo em revisão previne anos de dívida técnica.

## Quando Aplicar
- Trimestralmente como parte do ciclo de revisão técnica
- Antes de decisões arquiteturais significativas (nova plataforma, migração, redesign)
- Quando problemas de performance, custo ou segurança se tornarem recorrentes
- Quando o sistema precisar suportar 10x o volume atual no próximo horizonte
- Após incidentes graves relacionados a limitações arquiteturais

## Agente Responsável
**Agente CTO (Chief Technology Officer Agent)** — responsável por garantir que a arquitetura de sistemas suporta a estratégia de negócio com qualidade, eficiência e segurança.

## Checklist

### Seção 1: Modularidade e Manutenibilidade
- [ ] Sistemas estão decompostos em módulos/serviços com responsabilidades claras
- [ ] Boundaries entre módulos são bem definidos (API contracts, interfaces)
- [ ] Acoplamento entre módulos é baixo — mudanças em um não quebram outros
- [ ] Cada módulo pode ser desenvolvido, testado e deployado independentemente
- [ ] Código segue princípios SOLID e padrões consistentes
- [ ] Documentação de arquitetura está atualizada (C4 model, ADRs)
- [ ] Novos desenvolvedores conseguem entender e contribuir em menos de 2 semanas
- [ ] Shared libraries e dependências estão geridas e versionadas adequadamente

### Seção 2: Escalabilidade
- [ ] O sistema escala horizontalmente para os componentes de maior carga
- [ ] Bottlenecks de escalabilidade estão identificados e documentados
- [ ] Load testing foi realizado nos últimos 90 dias com resultados documentados
- [ ] O sistema suporta pelo menos 3x a carga atual sem degradação significativa
- [ ] Database scaling strategy está definida (sharding, read replicas, caching)
- [ ] Caching strategy está implementada nos pontos de maior impacto
- [ ] Asynchronous processing é usado onde latência não é crítica
- [ ] Auto-scaling está configurado e testado para componentes críticos
- [ ] CDN e edge computing são utilizados onde aplicável
- [ ] O custo de escalar é linear ou sub-linear em relação ao crescimento

### Seção 3: Custo e Eficiência
- [ ] Custo de infraestrutura por mês está rastreado e dentro do budget
- [ ] Custo por transação/usuário/request está calculado e otimizado
- [ ] Recursos subutilizados estão identificados e right-sized
- [ ] Reserved instances ou committed use discounts são utilizados onde aplicável
- [ ] Custo de infraestrutura como % da receita está dentro de benchmarks
- [ ] Alertas de custo estão configurados para anomalias (cost overrun)
- [ ] FinOps practices estão implementadas (tagging, showback, optimization)
- [ ] Trade-offs entre custo e performance estão documentados e aceitos

### Seção 4: Segurança Arquitetural
- [ ] Princípio de least privilege está implementado em todos os níveis
- [ ] Defense in depth — múltiplas camadas de segurança estão presentes
- [ ] Dados sensíveis estão criptografados at rest e in transit
- [ ] Secrets management está implementado (vault, KMS, não hardcoded)
- [ ] Network segmentation isola componentes críticos
- [ ] Authentication e authorization estão centralizados e padronizados
- [ ] API security best practices estão implementadas (rate limiting, input validation)
- [ ] Audit logging está ativo para operações sensíveis

### Seção 5: Governança Arquitetural
- [ ] Architecture Decision Records (ADRs) são criados para decisões significativas
- [ ] Existe um Tech Radar ou Technology Standards document atualizado
- [ ] Novos serviços/componentes passam por review arquitetural antes de iniciar
- [ ] Existe um Architecture Review Board ou processo equivalente
- [ ] Diagrama de arquitetura atual está atualizado e acessível
- [ ] Roadmap de evolução arquitetural está definido para os próximos 12 meses
- [ ] Decisões de build vs. buy seguem framework definido
- [ ] Technical debt relacionada a arquitetura está catalogada e priorizada

## Critérios de Aprovação
- Documentação de arquitetura atualizada nos últimos 90 dias
- Load testing realizado com sistema suportando 3x carga atual
- Custo de infraestrutura dentro do budget e com tendência controlada
- Zero vulnerabilidades críticas de segurança arquitetural ativas
- Pelo menos 85% dos itens de todas as seções concluídos
- ADRs existem para todas as decisões significativas dos últimos 6 meses

## O que Fazer se Falhar
1. Priorizar: segurança primeiro, escalabilidade segundo, custo terceiro, modularidade quarto
2. Para problemas de segurança: remediar imediatamente com war room se necessário
3. Para escalabilidade: criar plano de capacity com horizonte de 12 meses
4. Para custo: implementar FinOps básico e right-sizing em 30 dias
5. Para modularidade: criar roadmap de refactoring com business case
6. Documentar a arquitetura atual se não existir documentação (as-is antes do to-be)
7. Realizar Architecture Review com participação de senior engineers
8. Re-auditar em 45 dias com foco nos itens críticos que falharam

## Referências
- "Fundamentals of Software Architecture" — Mark Richards & Neal Ford
- "Designing Data-Intensive Applications" — Martin Kleppmann
- Architecture Decision Records (internal wiki)
- Cloud provider best practices (AWS Well-Architected, GCP Architecture)
- "Building Evolutionary Architectures" — Neal Ford et al.
- Cost optimization guides (FinOps Foundation)
- OWASP Architecture Security Guide
