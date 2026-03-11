# Checklist de Qualidade — Architecture Decision Record (ADR)

## Propósito
Garantir que decisões de arquitetura tecnológica sejam documentadas com rigor: contexto completo, opções avaliadas sistematicamente, consequências compreendidas em profundidade e reversibilidade avaliada antes de comprometer a organização. Este checklist transforma ADRs de documentos burocráticos em instrumentos de decisão e aprendizado que protegem contra tech debt acidental.

## Quando Aplicar
- Quando uma decisão de arquitetura tem impacto significativo em custo, performance ou manutenibilidade
- Na escolha de tecnologias, frameworks, linguagens ou plataformas
- Em decisões de build vs buy vs partner para componentes tecnológicos
- Quando padrões arquiteturais (microservices, monolith, event-driven) são definidos ou alterados
- Na revisão de ADRs existentes para validação ou atualização
- Quando agentes técnicos propõem mudanças arquiteturais para validação

## Agente Responsável
- **Primário:** CTO Agent ou Principal Engineer Agent
- **Revisor:** Architecture Review Board (se existente) ou pares técnicos seniores
- **Consultor:** CISO Agent para impacto em segurança
- **Aprovador:** CTO Agent para decisões acima do threshold de impacto

## Checklist

### Seção 1 — Contexto Documentado
- [ ] O problema ou necessidade que motiva a decisão está descrito claramente
- [ ] O estado atual (as-is) da arquitetura relevante está documentado
- [ ] Os drivers da decisão estão listados (performance, custo, scalability, time-to-market, etc.)
- [ ] Os constraints (restrições) estão explícitos: técnicos, financeiros, regulatórios, de prazo
- [ ] O escopo da decisão está delimitado (o que está e o que não está em discussão)
- [ ] Os stakeholders impactados pela decisão estão identificados
- [ ] O histórico de decisões anteriores relacionadas está referenciado
- [ ] As premissas técnicas estão declaradas explicitamente
- [ ] O volume de tráfego, dados ou transações esperado está documentado
- [ ] Os requisitos não-funcionais (latência, disponibilidade, throughput) estão especificados
- [ ] O horizonte temporal da decisão está definido (para quanto tempo deve servir)

### Seção 2 — Opções Avaliadas
- [ ] No mínimo 3 opções viáveis estão listadas (incluindo manter status quo)
- [ ] Cada opção tem descrição técnica suficiente para avaliação independente
- [ ] Os prós e contras de cada opção estão documentados de forma balanceada
- [ ] O custo estimado de cada opção está quantificado (implementação e operação)
- [ ] O esforço de implementação de cada opção está estimado (pessoa-meses ou story points)
- [ ] A maturidade de cada tecnologia avaliada está verificada (community, support, adoption)
- [ ] A compatibilidade com o stack tecnológico existente está avaliada
- [ ] O impacto em performance e scalability de cada opção está analisado
- [ ] As skills disponíveis na equipe para cada opção estão verificadas
- [ ] POCs ou protótipos foram realizados para opções de alta incerteza
- [ ] O vendor lock-in risk de cada opção está avaliado

### Seção 3 — Consequências Compreendidas
- [ ] As consequências positivas da decisão estão documentadas com métricas esperadas
- [ ] As consequências negativas (trade-offs) estão explicitamente articuladas
- [ ] O impacto em tech debt está avaliado (a decisão cria, reduz ou mantém tech debt)
- [ ] O impacto em complexidade do sistema está analisado
- [ ] O impacto em observability e debuggability está considerado
- [ ] O impacto em testing (testabilidade, cobertura) está avaliado
- [ ] O impacto em deployment e operação (CI/CD, monitoring, rollback) está documentado
- [ ] O impacto em segurança está avaliado e validado pelo CISO Agent
- [ ] O impacto em developer experience (DX) está considerado
- [ ] As consequências de segunda ordem estão exploradas (efeitos indiretos)
- [ ] O impacto em equipes adjacentes e sistemas dependentes está comunicado
- [ ] O custo de manutenção de longo prazo está estimado

### Seção 4 — Reversibilidade Avaliada
- [ ] A decisão está classificada como reversível (two-way door) ou irreversível (one-way door)
- [ ] O custo de reversão (se reversível) está estimado em tempo e dinheiro
- [ ] O ponto de não-retorno está identificado (após qual milestone a reversão fica inviável)
- [ ] O plano de migration/rollback está delineado caso a decisão precise ser revertida
- [ ] Os dados que seriam afetados por uma reversão estão identificados
- [ ] A estratégia de minimizar lock-in está documentada (abstractions, interfaces, adapters)
- [ ] O impacto de reversão em contratos ou compromissos externos está avaliado
- [ ] O nível de rigor requerido na decisão é proporcional à irreversibilidade
- [ ] Decisões irreversíveis passaram por review mais rigoroso

### Seção 5 — Decisão e Fundamentação
- [ ] A decisão está claramente declarada (qual opção foi escolhida)
- [ ] A fundamentação conecta a decisão aos drivers e constraints documentados
- [ ] Os dissenting opinions estão registrados com respeito
- [ ] O nível de confiança na decisão está declarado
- [ ] As condições que invalidariam a decisão estão listadas (review triggers)
- [ ] O owner da implementação está designado
- [ ] O timeline de implementação está estimado
- [ ] O plano de comunicação da decisão está definido

### Seção 6 — Formatação e Processo
- [ ] O ADR segue o template padrão (número, título, status, data, contexto, decisão, consequências)
- [ ] O ADR está armazenado no repositório de ADRs da organização
- [ ] O status do ADR está atualizado (proposed, accepted, deprecated, superseded)
- [ ] O ADR está linkado a ADRs relacionados (supersedes, depends-on, etc.)
- [ ] A peer review técnica foi realizada antes da aprovação
- [ ] O ADR foi comunicado às equipes impactadas

## Critérios de Aprovação
- Contexto completo com drivers, constraints e requisitos não-funcionais documentados
- Mínimo de 3 opções avaliadas com prós, contras e custos
- Consequências positivas e negativas compreendidas e documentadas
- Reversibilidade avaliada com plano de rollback para decisões reversíveis
- Decisão fundamentada e linkada aos drivers documentados
- Peer review técnico completado
- Score mínimo de completude: 85% dos itens marcados

## O que Fazer se Falhar
1. Se o contexto está incompleto, não aprovar até que drivers e constraints estejam claros
2. Se menos de 3 opções foram avaliadas, solicitar exploração adicional
3. Se consequências não foram analisadas, realizar sessão de análise de impacto
4. Se reversibilidade não foi avaliada, classificar como one-way door por precaução
5. Se não houve peer review, não aprovar — exigir pelo menos 2 revisores técnicos
6. Para decisões one-way door que falharem no checklist, escalar para o CTO Agent
7. Registrar padrões de falha no RalphLoop para melhorar o processo de ADR

## Referências
- Nygard, M. — "Documenting Architecture Decisions" (ADR format original)
- Richards, M. & Ford, N. — "Fundamentals of Software Architecture"
- Fowler, M. — "Patterns of Enterprise Application Architecture"
- Bezos, J. — One-way vs two-way door decisions
- Template interno: `/templates/adr-template.md`
- Repositório de ADRs: `/adrs/`
- Architecture principles: `/architecture/principles.md`
