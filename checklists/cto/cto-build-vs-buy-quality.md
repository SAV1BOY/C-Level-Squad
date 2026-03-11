# CTO Build vs Buy Quality

## Propósito
Garantir que decisões de build vs. buy são tomadas com rigor analítico: custo total (TCO), risco, time-to-value e alinhamento estratégico são avaliados sistematicamente. Construir o que deveria ser comprado desperdiça engenharia. Comprar o que deveria ser construído cria dependência e limita diferenciação.

## Quando Aplicar
- Sempre que uma nova necessidade de sistema ou ferramenta surgir
- Quando contratos de vendor estiverem próximos de renovação
- Quando soluções internas estiverem custando mais que alternativas de mercado
- Quando soluções de vendor estiverem limitando a capacidade de inovar
- Trimestralmente como revisão do portfolio de build vs. buy decisions

## Agente Responsável
**Agente CTO (Chief Technology Officer Agent)** — responsável por garantir que decisões de build vs. buy maximizam valor estratégico e minimizam custo total e risco.

## Checklist

### Seção 1: Análise de Necessidade
- [ ] A necessidade está claramente definida em termos de capability, não de solução
- [ ] Requirements funcionais e não-funcionais estão documentados
- [ ] A necessidade é core (diferenciador estratégico) ou commodity (table stakes)?
- [ ] O horizonte temporal da necessidade está definido (curto, médio, longo prazo)
- [ ] Stakeholders internos foram consultados sobre requirements
- [ ] A urgência da necessidade é genuína e não artificial
- [ ] Alternativas de "não fazer" ou "fazer o mínimo" foram consideradas
- [ ] A necessidade está alinhada com a estratégia tecnológica de longo prazo

### Seção 2: Avaliação de Build
- [ ] Custo de desenvolvimento está estimado (horas de engenharia × custo/hora)
- [ ] Timeline de desenvolvimento é realista e inclui margem para imprevistos
- [ ] Custo de manutenção ongoing está projetado (20-30% do custo de build por ano)
- [ ] O time tem as skills necessárias ou precisará contratar/treinar
- [ ] O custo de oportunidade de alocar engenharia nisto (vs. outras prioridades) foi avaliado
- [ ] Riscos de build estão identificados: complexidade, prazo, qualidade
- [ ] Ownership de longo prazo está definido (quem mantém depois de construído?)
- [ ] Build permite diferenciação competitiva real ou é apenas NIH syndrome?

### Seção 3: Avaliação de Buy
- [ ] Market scan foi realizado — pelo menos 3 opções de vendor foram avaliadas
- [ ] Custo total de buy inclui: licença, implementação, integração, treinamento, suporte
- [ ] Vendor lock-in risk foi avaliado (portabilidade de dados, switching costs)
- [ ] SLAs e reliability do vendor atendem aos requirements
- [ ] Security e compliance do vendor foram verificados
- [ ] Roadmap do vendor está alinhado com as necessidades futuras da organização
- [ ] Referências de outros clientes do vendor foram consultadas
- [ ] Flexibilidade de customização do vendor atende às necessidades

### Seção 4: Comparação e Decisão
- [ ] TCO (Total Cost of Ownership) foi calculado para build E para buy em horizonte de 3 anos
- [ ] Time-to-value foi comparado: quanto tempo para cada opção entregar valor?
- [ ] Risco foi comparado: qual opção tem maior risco de falha ou atraso?
- [ ] Flexibilidade foi comparada: qual opção permite mais adaptação futura?
- [ ] Alinhamento estratégico foi avaliado: qual opção fortalece mais o core do negócio?
- [ ] A decisão foi tomada com base em dados e framework, não apenas opinião
- [ ] A decisão foi documentada como ADR (Architecture Decision Record)
- [ ] Stakeholders relevantes concordam com a decisão

### Seção 5: Revisão de Decisões Passadas
- [ ] Decisões de build vs. buy dos últimos 12 meses foram revisadas
- [ ] Decisões que se provaram corretas estão documentadas como reforço
- [ ] Decisões que se provaram erradas foram analisadas com root cause
- [ ] Aprendizados foram incorporados no framework de decisão
- [ ] Custos reais vs. custos estimados foram comparados (calibração)
- [ ] Vendor contracts em renovação foram reavaliados com critérios atuais
- [ ] Build decisions que se tornaram maintenance burden estão identificadas
- [ ] O framework de decisão é atualizado periodicamente com novos aprendizados

## Critérios de Aprovação
- 100% das novas decisões de build vs. buy passaram pelo framework documentado
- TCO calculado para horizonte de pelo menos 3 anos em cada decisão
- ADR criado para cada decisão significativa
- Revisão de decisões passadas realizada nos últimos 6 meses
- Pelo menos 85% dos itens de todas as seções concluídos
- Nenhuma decisão pendente há mais de 30 dias sem resolução

## O que Fazer se Falhar
1. Para decisões pendentes: forçar timeline de decisão (máximo 2 semanas)
2. Se framework não existe: criar versão mínima e iterar
3. Se decisões passadas foram ruins: documentar aprendizados e ajustar framework
4. Para vendor lock-in: criar plano de migração ou mitigação
5. Para build maintenance burden: avaliar migração para solução de mercado
6. Implementar obrigatoriedade de ADR para toda decisão de build vs. buy
7. Envolver engenharia E negócio na decisão (não apenas um lado)
8. Re-auditar em 45 dias com foco nas decisões mais impactantes

## Referências
- Architecture Decision Records (internal wiki)
- "The Build Trap" — Melissa Perri
- TCO calculation templates
- Vendor evaluation scorecards (internal)
- "Technology Strategy Patterns" — Eben Hewitt
- Procurement and vendor management policies
- Historical build vs. buy decision outcomes
