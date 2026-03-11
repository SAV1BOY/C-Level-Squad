# Estratégia de Plataforma — Framework de Plataformização Interna e Externa

## Propósito e Contexto

Plataforma, no contexto de engenharia, tem dois significados complementares: (1) plataforma
interna — a infraestrutura e tooling que aceleram o desenvolvimento de produtos; e (2)
plataforma externa — o modelo de negócio onde terceiros constroem sobre seus serviços (APIs,
marketplace, ecossistema). Este framework endereça ambos, com foco na decisão de quando e
como investir em plataformização.

A tentação de "construir plataforma" é uma das maiores armadilhas em engenharia. Plataformas
prematuras consomem recursos enormes para servir um único cliente interno. Plataformas tardias
deixam times reinventando a roda por anos. O timing e o escopo são tudo.

Regra de ouro: construa plataforma quando o mesmo problema foi resolvido de forma diferente
por pelo menos 3 times. Antes disso, é pattern recognition; depois, é negligência.

## Quando Usar

- Quando múltiplos times resolvem problemas similares de formas inconsistentes
- Ao planejar scaling de engenharia (dobrar ou triplicar o time)
- Na decisão de abrir APIs para terceiros
- Quando o tempo de onboarding de novos engenheiros é excessivo
- Ao avaliar investimento em developer experience (DX)
- Na construção de estratégia de ecossistema/marketplace

## Componentes do Framework

### 1. Maturidade de Plataforma (Modelo de 4 Estágios)

**Estágio 1: Ad Hoc (1-20 engenheiros)**
- Cada time escolhe suas ferramentas e padrões
- Não há infra compartilhada além do cloud provider
- OK neste estágio — premature platforming é desperdício

**Estágio 2: Padrões Emergentes (20-60 engenheiros)**
- Templates de projeto e boilerplates compartilhados
- CI/CD padronizado, mas sem self-service
- Documentação de best practices
- Investimento: 1-2 engenheiros dedicados a DX

**Estágio 3: Plataforma Interna (60-200 engenheiros)**
- Self-service para provisioning de serviços, ambientes, observabilidade
- Internal Developer Platform (IDP) com portal e abstrações
- Golden paths: caminhos recomendados para casos comuns
- Investimento: time dedicado de Platform Engineering (5-10% do headcount)

**Estágio 4: Plataforma como Produto (200+ eng ou estratégia de ecossistema)**
- APIs públicas com documentação, SDKs e developer relations
- Marketplace ou ecossistema de extensões
- SLAs formais para consumidores internos e externos
- Investimento: organização de plataforma com PM, design e engenharia

### 2. Framework de Decisão: O Que Plataformizar

Para cada candidato a plataforma, avalie:

| Critério | Score (1-5) |
|----------|-------------|
| Número de times que precisam dessa capability | ___ |
| Frequência de uso (diária vs. eventual) | ___ |
| Custo atual da inconsistência (bugs, retrabalho) | ___ |
| Complexidade de fazer certo (segurança, compliance) | ___ |
| Estabilidade do domínio (vai mudar muito?) | ___ |

Score ≥ 18: Forte candidato para plataformização
Score 12-17: Considerar, mas validar com POC
Score < 12: Cedo demais — documentar padrões, não construir plataforma

### 3. Princípios de Design de Plataforma

**Self-service como default:** Developers não devem precisar de ticket para provisionar
**Opinativa com escape hatches:** Golden paths para 80% dos casos, flexibilidade para 20%
**API-first:** Toda capability de plataforma acessível via API antes de ter UI
**Observável:** Métricas de uso e satisfação built-in
**Evolutiva:** Contratos versionados, backward compatibility, deprecation gradual
**Documentada:** Se não está documentado, não existe para o usuário

## Processo Passo-a-Passo

### Fase 1: Assessment (2-3 semanas)
1. Mapear pain points dos times de produto (surveys, entrevistas)
2. Identificar duplicação de esforço entre times
3. Avaliar maturidade atual no modelo de 4 estágios
4. Benchmarking com empresas de porte similar

### Fase 2: Estratégia (2-3 semanas)
1. Definir target state (qual estágio em 12-18 meses)
2. Priorizar capabilities usando o framework de decisão
3. Definir team topology: stream-aligned, platform, enabling
4. Estabelecer investment thesis para o board/CFO

### Fase 3: Execução Incremental (ongoing)
1. MVP da primeira capability de plataforma (< 6 semanas)
2. Adoção por 1-2 times early adopters
3. Iteração baseada em feedback real
4. Expansão gradual (não forçar adoção — conquistar)

### Fase 4: Operação e Evolução
1. Métricas de adoção e satisfação
2. Roadmap de plataforma alinhado com roadmap de produto
3. Feedback loops formais com times consumidores
4. Revisão trimestral de investimento vs. impacto

## Template de Platform Charter

```markdown
# Platform Charter: [Nome da Plataforma]

## Missão
[Uma frase sobre o que essa plataforma resolve e para quem]

## Usuários
- Primários: [ex: engenheiros de backend]
- Secundários: [ex: SREs, data engineers]

## Capabilities Oferecidas
1. [Capability]: [descrição em 1 linha]
2. [Capability]: [descrição em 1 linha]

## SLAs
- Disponibilidade: [target]
- Tempo de resposta a pedidos: [target]
- Tempo de onboarding: [target]

## Métricas de Sucesso
- Adoção: [X% dos times usando em Y meses]
- Satisfação: [NPS > X]
- Impacto: [redução de Y% em tempo de setup]

## Investimento
- Headcount: [N engenheiros]
- Infra: [R$ X/mês]
- Timeline para v1: [X semanas]
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Developer NPS da plataforma | > 40 | Trimestral |
| Tempo de provisioning (novo serviço) | < 1 dia (vs. semanas) | Contínuo |
| Adoção dos golden paths | > 80% dos novos projetos | Trimestral |
| Tempo de onboarding de novos engenheiros | Redução de 30%+ | Semestral |
| Incidentes causados por inconsistência | Tendência decrescente | Mensal |
| % do headcount em plataforma | 5-12% (dependendo do estágio) | Trimestral |

## Armadilhas

1. **Plataforma prematura** — Construir antes de ter 3+ consumidores reais
2. **Platform tax** — Forçar adoção sem provar valor; equipes contornam
3. **Ivory tower platform** — Time de plataforma desconectado dos problemas reais
4. **Over-abstraction** — Abstrair demais torna a plataforma difícil de debugar
5. **Build everything** — Plataforma pode compor serviços externos (buy no radar)

## Referências Cruzadas

- `frameworks/cto-architect/tech-radar.md` — Tecnologias que compõem a plataforma
- `frameworks/cto-architect/build-vs-buy.md` — Decisão build/buy para cada capability
- `frameworks/cto-architect/tech-debt-management.md` — Plataforma como redutor de dívida
- `frameworks/cto-architect/engineering-excellence.md` — Golden paths como veículo de excelência
- `frameworks/cio-engineer/cloud-strategy.md` — Cloud foundation layer da plataforma
- `frameworks/caio-architect/mlops-framework.md` — ML platform como extensão
- `frameworks/shared/stakeholder-management.md` — Times consumidores como stakeholders
