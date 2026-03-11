# Gestão de Dívida Técnica — Framework de Classificação e Pagamento

## Propósito e Contexto

Dívida técnica é o custo futuro de escolhas técnicas que priorizam velocidade de entrega
sobre qualidade ou sustentabilidade. Como dívida financeira, não é inerentemente ruim — pode
ser uma decisão estratégica consciente. O problema é dívida técnica não gerenciada: aquela que
se acumula silenciosamente até que a velocidade de desenvolvimento cai pela metade e cada
mudança simples se torna arriscada.

Este framework trata dívida técnica como um portfólio a ser gerenciado: classificar por tipo,
medir o custo de carregar, priorizar o pagamento e estabelecer limites saudáveis de
endividamento. O objetivo não é zero dívida — é dívida consciente e gerenciável.

Referências: Ward Cunningham (metáfora original), Martin Fowler (quadrante de dívida técnica),
Google SRE (error budgets como conceito análogo).

## Quando Usar

- Na definição de alocação de capacidade de engenharia (quanto para features vs. debt)
- Quando velocidade de entrega está diminuindo sem explicação óbvia
- Após incidentes recorrentes causados por sistemas frágeis
- Em onboarding de novos CTOs ou tech leads que herdam codebase
- Na preparação para scaling (10x users, 10x equipe)
- Em due diligence técnica para M&A ou investimento

## Componentes do Framework

### 1. Quadrante de Classificação (Fowler Adaptado)

| | Deliberada | Inadvertida |
|---|---|---|
| **Prudente** | "Sabemos o trade-off e vamos pagar depois" | "Agora que entendemos melhor, faríamos diferente" |
| **Imprudente** | "Não temos tempo para fazer direito" | "O que é arquitetura limpa?" |

- **Prudente-Deliberada:** Aceitável e gerenciável. Documentar e agendar pagamento.
- **Prudente-Inadvertida:** Natural e inevitável. Aprendizado gerou insight para melhorar.
- **Imprudente-Deliberada:** Perigosa. Precisa de guardrails organizacionais.
- **Imprudente-Inadvertida:** Sintoma de falta de skills. Resolver com hiring/treinamento.

### 2. Taxonomia de Dívida Técnica

**Dívida de Código:** Código complexo, duplicado, sem testes, mal documentado
- Custo de carregar: tempo extra em cada mudança, bugs recorrentes
- Indicadores: cyclomatic complexity, code coverage, tempo de review

**Dívida de Arquitetura:** Decisões estruturais que limitam evolução
- Custo de carregar: impossibilidade de scaling, acoplamento entre equipes
- Indicadores: blast radius de mudanças, deployment coupling

**Dívida de Infraestrutura:** Infra desatualizada, sem automação, sem observabilidade
- Custo de carregar: incidentes, tempo de deploy, custos excessivos de cloud
- Indicadores: MTTR, frequência de deploy, custo por transação

**Dívida de Dependências:** Libraries desatualizadas, vulnerabilidades conhecidas
- Custo de carregar: risco de segurança, incompatibilidades
- Indicadores: versões atrás do stable, CVEs abertas

**Dívida de Conhecimento:** Documentação ausente, tribal knowledge
- Custo de carregar: onboarding lento, bus factor, decisões sem contexto
- Indicadores: tempo de onboarding, concentração de PRs por autor

### 3. Modelo de Custo de Carregamento

Para priorizar pagamento, estime o "juros" que cada dívida cobra:

```
Custo Mensal de Carregar =
  (Horas extras por sprint por causa da dívida) × (Custo/hora da equipe)
  + (Incidentes atribuíveis × Custo médio por incidente)
  + (Risco de segurança × Probabilidade × Impacto estimado)
```

Compare com o custo de pagamento (resolver a dívida) para calcular "payback period":
- Payback < 3 meses: prioridade máxima
- Payback 3-12 meses: planejar no próximo trimestre
- Payback > 12 meses: monitorar, resolver oportunisticamente

## Processo Passo-a-Passo

### Fase 1: Inventário (1-2 semanas, depois contínuo)
1. Cada time identifica as top 5 dívidas técnicas na sua área
2. Classificar usando o quadrante e a taxonomia
3. Estimar custo de carregamento e custo de pagamento
4. Consolidar em backlog centralizado de dívida técnica

### Fase 2: Priorização (1 semana)
1. Ordenar por payback period (menor primeiro)
2. Considerar risco: dívidas com impacto catastrófico sobem na prioridade
3. Agrupar dívidas relacionadas que podem ser resolvidas juntas
4. Selecionar itens para o próximo ciclo baseado em capacidade alocada

### Fase 3: Alocação de Capacidade
Modelo recomendado por estágio da empresa:
- **Startup (< 50 eng):** 10-15% da capacidade para debt
- **Growth (50-200 eng):** 15-25% da capacidade para debt
- **Scale (> 200 eng):** 20-30% da capacidade para debt

Implementação:
- Opção A: Time dedicado (Tech Foundations / Platform)
- Opção B: Alocação por sprint (ex: 1 sprint em 4 é debt sprint)
- Opção C: 20% time individual + projetos grandes trimestrais
- Opção D: Resolver debt junto com features relacionadas (boy scout rule)

### Fase 4: Prevenção
1. Definition of Done inclui: testes, documentação, code review
2. Tech radar define tecnologias aprovadas (evita dívida de escolha)
3. Architecture Decision Records para decisões de trade-off
4. Debt budget: cada feature pode gerar até X story points de dívida consciente

## Template de Registro de Dívida Técnica

```markdown
## [ID] — [Nome descritivo da dívida]

**Tipo:** [Código | Arquitetura | Infra | Dependências | Conhecimento]
**Quadrante:** [Prudente-Deliberada | Prudente-Inadvertida | etc.]
**Severidade:** [Crítica | Alta | Média | Baixa]
**Owner:** [Time responsável]
**Criada em:** [Data]

### Descrição
[O que é a dívida e como ela surgiu]

### Impacto Atual
- Custo mensal estimado: R$ [X] ou [Y] horas/sprint
- Incidentes relacionados nos últimos 3 meses: [N]
- Equipes afetadas: [lista]

### Plano de Pagamento
- Esforço estimado: [story points ou dias de engenharia]
- Payback period: [meses]
- Dependências: [outras dívidas ou projetos]
- Abordagem: [big bang | incremental | rewrite | refactor]

### Decisão
- [ ] Pagar agora
- [ ] Agendar para Q[X]
- [ ] Monitorar
- [ ] Aceitar (risco gerenciável)
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| % de capacidade em debt reduction | Dentro do range por estágio | Mensal |
| Velocity trend | Estável ou crescente | Mensal |
| Incidentes por dívida conhecida | Tendência decrescente | Mensal |
| Debt backlog age | < 20% dos itens com > 6 meses | Trimestral |
| Developer satisfaction com codebase | > 3.5/5 | Semestral |
| Payback period médio dos itens pagos | < 6 meses | Trimestral |

## Armadilhas

1. **Zero debt como meta** — Impossível e contraproducente; o objetivo é debt gerenciável
2. **Debt sprint como punição** — Tratar como investimento estratégico, não limpeza
3. **Inventário sem ação** — Listar dívidas sem resolver é desperdício
4. **Rewrite como solução padrão** — Refatoração incremental é quase sempre preferível
5. **Esconder dívida** — Criar cultura onde reportar debt é positivo, não vergonhoso

## Referências Cruzadas

- `frameworks/cto-architect/tech-radar.md` — Tecnologias em HOLD que geram debt
- `frameworks/cto-architect/build-vs-buy.md` — Builds que viraram debt
- `frameworks/cto-architect/engineering-excellence.md` — Práticas que previnem debt
- `frameworks/cto-architect/platform-strategy.md` — Plataforma como redutor de debt
- `frameworks/cfo-strategist/cost-optimization.md` — Debt como driver de custos
- `frameworks/shared/risk-management.md` — Debt como risco operacional
