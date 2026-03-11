# Framework Build vs Buy — Decisão de Construir ou Comprar

## Propósito e Contexto

A decisão entre construir internamente (build) ou adquirir soluções prontas (buy) é uma das
mais frequentes e consequentes na gestão de tecnologia. Construir demais gera custo de
manutenção insustentável e distrai do core business. Comprar demais cria dependência de
fornecedores, limita diferenciação e pode gerar custos crescentes. A resposta nunca é
absoluta — depende de contexto, momento da empresa e natureza da capability.

Este framework fornece critérios objetivos, um scoring model e um processo de decisão que
reduz o viés (engenheiros tendem a preferir build; gestores tendem a preferir buy) e documenta
o rationale para revisão futura.

## Quando Usar

- Ao iniciar qualquer projeto significativo de software (> 2 semanas de engenharia)
- Quando um time pede para construir algo que já existe no mercado
- Quando um contrato de SaaS está para renovar (re-avaliar a decisão)
- Em revisões de tech debt que envolvem sistemas legados internos
- Ao avaliar M&A de capabilities tecnológicas (forma extrema de buy)
- Quando custos de infraestrutura crescem além do esperado

## Componentes do Framework

### 1. Classificação da Capability

Antes de decidir build vs buy, classifique a capability:

**Core Differentiator** — O que torna seu produto único para o cliente
- Tendência: BUILD — investir em ownership total
- Exemplo: algoritmo de recomendação de um marketplace, motor de pricing

**Core Supporting** — Essencial para operar, mas não é diferencial
- Tendência: BUY premium — investir em melhor solução disponível
- Exemplo: autenticação, pagamentos, comunicação com cliente

**Context** — Necessário mas genérico, sem impacto competitivo
- Tendência: BUY commodity — menor custo, menor atenção
- Exemplo: email corporativo, gestão de despesas, ATS

### 2. Scoring Model

Avalie cada dimensão de 1-5 (1 = favorece BUY, 5 = favorece BUILD):

| Dimensão | Peso | Score | Ponderado |
|----------|------|-------|-----------|
| Diferenciação competitiva | 3x | ___ | ___ |
| Disponibilidade de mercado | 2x | ___ | ___ |
| Custo total de ownership (3 anos) | 2x | ___ | ___ |
| Velocidade de entrega | 2x | ___ | ___ |
| Controle e customização necessários | 2x | ___ | ___ |
| Disponibilidade de equipe | 1x | ___ | ___ |
| Risco de lock-in do fornecedor | 1x | ___ | ___ |
| Maturidade do mercado de soluções | 1x | ___ | ___ |

**Interpretação:**
- Score < 28: Forte indicação para BUY
- Score 28-42: Zona de análise detalhada (considerar hybrid)
- Score > 42: Forte indicação para BUILD

### 3. Análise de Custo Total (TCO - 3 anos)

**Custo de BUILD:**
- Desenvolvimento inicial (equipe × tempo × custo carregado)
- Manutenção anual (tipicamente 15-25% do custo inicial por ano)
- Infraestrutura (hosting, monitoramento, segurança)
- Custo de oportunidade (o que essa equipe faria se não construísse isso?)
- Risco de projeto (atraso, complexidade subestimada — adicionar 30-50%)

**Custo de BUY:**
- Licenciamento (considerar escalas de preço com crescimento)
- Implementação e integração
- Customizações necessárias
- Treinamento da equipe
- Custos de migração (se trocar de fornecedor no futuro)
- Dependência operacional (SLA, suporte, evolução do produto)

### 4. Opção Hybrid (Build on Buy)

Muitas vezes a melhor resposta não é binária:
- **API-first buy:** Comprar serviço via API, construir experiência própria por cima
- **Fork and own:** Usar open source como base, customizar e manter internamente
- **Buy now, build later:** Comprar para validar o espaço, construir quando escalar
- **Build core, buy edges:** Construir o motor diferencial, integrar serviços auxiliares

## Processo Passo-a-Passo

### Fase 1: Definição do Escopo (1-2 dias)
1. Descrever a capability necessária em termos de negócio (não técnicos)
2. Classificar como Core Differentiator, Core Supporting ou Context
3. Definir requisitos funcionais e não-funcionais
4. Estabelecer timeline desejada

### Fase 2: Market Scan (3-5 dias)
1. Pesquisar soluções disponíveis (SaaS, open source, serviços gerenciados)
2. Solicitar demos/trials das top 3 opções
3. Conversar com referências (empresas similares que usam a solução)
4. Avaliar roadmap e viabilidade do fornecedor (vai existir daqui a 3 anos?)

### Fase 3: Análise Comparativa (3-5 dias)
1. Preencher o Scoring Model com dados reais
2. Calcular TCO de 3 anos para BUILD e BUY
3. Avaliar opções hybrid viáveis
4. Documentar riscos específicos de cada caminho

### Fase 4: Decisão e Documentação (1-2 dias)
1. Apresentar análise para tech lead + product + finance
2. Tomar decisão com base no scoring + TCO + contexto estratégico
3. Documentar decision record (ADR) com rationale
4. Definir critérios de revisão (quando re-avaliar a decisão)

## Template de Decision Record

```markdown
# ADR: Build vs Buy — [Nome da Capability]

**Data:** [YYYY-MM-DD]
**Decisão:** [BUILD | BUY | HYBRID]
**Status:** [Proposta | Aceita | Superseded]

## Contexto
[Qual problema estamos resolvendo? Por que agora?]

## Classificação
[Core Differentiator | Core Supporting | Context]

## Opções Avaliadas
1. BUILD: [descrição da abordagem]
2. BUY — [Fornecedor X]: [descrição]
3. BUY — [Fornecedor Y]: [descrição]
4. HYBRID: [descrição]

## Análise
- Scoring: BUILD [X] vs BUY [Y]
- TCO 3 anos: BUILD R$ [X] vs BUY R$ [Y]
- Timeline: BUILD [X meses] vs BUY [Y semanas]

## Decisão
[Qual opção e por quê]

## Consequências
- Positivas: [lista]
- Negativas/Riscos: [lista]

## Critérios de Revisão
Reavaliar em [data] ou se [condição mudar]
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Decisões documentadas (ADR) | 100% de decisões build/buy | Contínuo |
| Precisão de estimativa TCO | Variação < 30% do planejado | Anual |
| Satisfação com decisões passadas | > 80% seriam repetidas | Anual |
| Tempo de decisão | < 2 semanas do pedido à decisão | Contínuo |
| Vendor health check | 100% dos fornecedores avaliados anualmente | Anual |

## Armadilhas Comuns

1. **Not Invented Here** — Rejeitar soluções externas por orgulho técnico
2. **Subestimar manutenção** — Build parece barato no dia 1; manutenção é para sempre
3. **Ignorar custo de oportunidade** — Sua melhor equipe deveria estar construindo isso?
4. **Lock-in invisível** — Custos de migração não contabilizados na análise de buy
5. **Build para aprender** — Válido como spike/POC, não como decisão de produção
6. **Comparar v1 build com v10 buy** — O produto comprado teve anos de desenvolvimento

## Referências Cruzadas

- `frameworks/cto-architect/tech-radar.md` — Tecnologias aprovadas para build
- `frameworks/cto-architect/tech-debt-management.md` — Builds antigos que viraram dívida
- `frameworks/cto-architect/platform-strategy.md` — Build como investimento em plataforma
- `frameworks/cfo-strategist/cost-optimization.md` — Otimização de custos de SaaS
- `frameworks/cfo-strategist/financial-planning.md` — Orçamento para build vs buy
- `frameworks/shared/decision-framework.md` — Processo de decisão estruturado
- `frameworks/cio-engineer/cloud-strategy.md` — Build vs buy em contexto de cloud
