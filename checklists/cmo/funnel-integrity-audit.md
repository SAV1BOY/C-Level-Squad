# Funnel Integrity Audit

## Propósito
Garantir a integridade do funil de conversão: tracking correto em todas as etapas, pontos de fricção identificados e tratados, e taxas de conversão por estágio monitoradas e otimizadas. Um funil sem integridade de dados gera decisões erradas — garbage in, garbage out.

## Quando Aplicar
- Semanalmente como parte do monitoramento de performance de marketing
- Quando taxas de conversão mostrarem variação inexplicável (>20% vs. média)
- Após mudanças em ferramentas, integrações ou fluxos de conversão
- Quando houver discrepância entre dados de marketing e dados de vendas
- Antes de escalar investimento em qualquer canal de aquisição

## Agente Responsável
**Agente CMO (Chief Marketing Officer Agent)** — responsável pela integridade dos dados de funil e pela otimização contínua das taxas de conversão.

## Checklist

### Seção 1: Tracking e Instrumentação
- [ ] Todos os pontos de conversão do funil estão instrumentados com tracking
- [ ] UTM parameters estão padronizados e aplicados em todas as campanhas
- [ ] Pixel/tag de conversão está funcionando corretamente em todas as páginas
- [ ] Eventos de conversão estão definidos e disparando corretamente no analytics
- [ ] Dados de CRM e analytics estão sincronizados e consistentes
- [ ] Não há "buracos" no funil onde leads desaparecem sem explicação
- [ ] Attribution model está definido e implementado (first-touch, last-touch, multi-touch)
- [ ] Dados de conversão são validados diariamente por amostragem
- [ ] Tracking cross-device e cross-session está implementado
- [ ] Consent e privacy compliance (LGPD) estão respeitados no tracking

### Seção 2: Definição de Etapas do Funil
- [ ] Cada etapa do funil tem definição clara e não ambígua
- [ ] Critérios de passagem entre etapas estão documentados e acordados
- [ ] Marketing e vendas concordam sobre as definições de MQL, SQL, SAL
- [ ] Lead scoring está calibrado e revisado nos últimos 30 dias
- [ ] Não há etapas redundantes ou que não agregam valor ao processo
- [ ] Cada etapa tem um owner responsável pela conversão
- [ ] Tempo médio em cada etapa está definido como benchmark
- [ ] Leads que ficam "presos" em uma etapa por muito tempo são tratados

### Seção 3: Análise de Conversão por Etapa
- [ ] Taxa de conversão de cada etapa está calculada e visível em dashboard
- [ ] Tendência de conversão por etapa está analisada (melhorando, piorando, estável)
- [ ] Variações significativas de conversão têm root cause analysis
- [ ] Conversão é analisada por segmento/canal/persona (não apenas aggregate)
- [ ] Benchmarks de mercado são conhecidos e usados como referência
- [ ] A etapa com pior conversão está identificada e com plano de melhoria
- [ ] Sazonalidade e fatores externos são considerados na análise
- [ ] Cohort analysis é realizada para entender evolução temporal

### Seção 4: Identificação e Remoção de Fricção
- [ ] Pontos de fricção em cada etapa foram identificados e catalogados
- [ ] Formulários estão otimizados (campos mínimos necessários)
- [ ] Landing pages têm load time inferior a 3 segundos
- [ ] Mobile experience está testada e otimizada
- [ ] CTAs são claros, visíveis e testados
- [ ] Processo de signup/onboarding foi testado end-to-end como se fosse um novo usuário
- [ ] Emails de nurturing são relevantes e têm open/click rates aceitáveis
- [ ] Pontos de abandono estão identificados com ações de recovery implementadas
- [ ] A/B tests estão rodando nos pontos de maior fricção
- [ ] Quick wins de remoção de fricção foram implementados

### Seção 5: Qualidade e Integridade dos Dados
- [ ] Dados de funil são auditados mensalmente para consistência
- [ ] Duplicatas de leads são identificadas e tratadas
- [ ] Dados enriquecidos (enrichment) estão corretos e atualizados
- [ ] Segmentação de dados está correta (leads no segmento certo)
- [ ] Dados de conversão batem entre sistemas (analytics ↔ CRM ↔ financeiro)
- [ ] Relatórios de funil são confiáveis para tomada de decisão
- [ ] Existe processo de data hygiene rodando regularmente
- [ ] Anomalias de dados são detectadas e investigadas rapidamente

## Critérios de Aprovação
- 100% dos pontos de conversão instrumentados e funcionando
- Definições de etapas acordadas entre marketing e vendas
- Dashboard de funil ativo e atualizado em real-time ou daily
- Dados consistentes entre sistemas (variação <5%)
- Pelo menos 85% dos itens de todas as seções concluídos
- Nenhum ponto de fricção crítico sem plano de melhoria

## O que Fazer se Falhar
1. Priorizar correção de tracking — sem dados corretos, nada mais importa
2. Para inconsistência de dados: reconciliar sistemas e definir single source of truth
3. Para conversão baixa: focar na etapa de pior performance primeiro
4. Implementar weekly funnel review com marketing e vendas juntos
5. Realizar session recordings e heatmaps nos pontos de maior abandono
6. Simplificar funil se houver etapas demais (princípio do mínimo necessário)
7. Investir em ferramentas de automação se tracking manual for a causa dos problemas
8. Re-auditar em 15 dias (ciclo curto por ser operacional)

## Referências
- Funnel Metrics Dashboard (internal)
- Google Analytics / Mixpanel / Amplitude setup documentation
- CRM configuration guide (HubSpot, Salesforce, etc.)
- A/B testing results repository
- "Lean Analytics" — Alistair Croll & Benjamin Yoskovitz
- Attribution model documentation
- LGPD compliance guidelines para tracking
