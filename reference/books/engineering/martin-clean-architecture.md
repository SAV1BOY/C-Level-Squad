# Clean Architecture — Robert C. Martin (2017)

## Resumo Executivo

"Uncle Bob" Martin apresenta princípios de design de software que produzem sistemas
maintainables, testáveis e flexíveis. A Clean Architecture organiza código em camadas
concêntricas onde dependências apontam sempre para dentro (das camadas externas para
as internas), isolando business logic de frameworks, databases e UI.

A tese central: a arquitetura de software deve servir ao negócio, não à tecnologia.
Decisões sobre frameworks e databases são detalhes que devem poder ser adiados e trocados
sem impactar as regras de negócio.

## Conceitos-Chave

### SOLID Principles
- **S**ingle Responsibility: Um módulo deve ter apenas uma razão para mudar
- **O**pen-Closed: Aberto para extensão, fechado para modificação
- **L**iskov Substitution: Subtipos devem ser substituíveis por seus tipos base
- **I**nterface Segregation: Dependa de interfaces específicas, não genéricas
- **D**ependency Inversion: Dependa de abstrações, não de concretizações

### Clean Architecture Layers (de fora para dentro)
1. **Frameworks & Drivers**: Web frameworks, DB, UI, devices (mais externa)
2. **Interface Adapters**: Controllers, presenters, gateways (adaptam formatos)
3. **Application Business Rules**: Use cases (orquestram entities)
4. **Enterprise Business Rules**: Entities (regras de negócio puras) — mais interna

### Dependency Rule
- Dependências SEMPRE apontam para dentro (das camadas externas para internas)
- Entities não conhecem use cases; use cases não conhecem frameworks
- A inversão é feita via dependency inversion e interfaces/abstrações
- Isso permite trocar database, UI ou framework sem mudar business logic

### Use Cases (Application Business Rules)
- Orquestram o fluxo de dados de/para entities
- Contêm regras de negócio específicas da aplicação (não da empresa)
- São independentes de UI, database, framework e qualquer external agency
- Representam as intenções do sistema (verbo): "CreateOrder", "ApprovePayment"

### Entities (Enterprise Business Rules)
- Regras de negócio mais gerais e de mais alto nível
- Poderiam existir mesmo sem automação (regras do domínio puro)
- Mais estáveis — mudam raramente
- Não dependem de NADA externo

### Component Principles
- **Reuse/Release Equivalence**: Granularidade de reuso = granularidade de release
- **Common Closure**: Classes que mudam juntas devem estar no mesmo componente
- **Common Reuse**: Classes usadas juntas devem estar no mesmo componente
- **Acyclic Dependencies**: Não pode haver ciclos no grafo de dependências entre componentes
- **Stable Dependencies**: Dependa na direção da estabilidade
- **Stable Abstractions**: Componentes estáveis devem ser abstratos

### Boundaries
- Linhas que separam componentes/layers e controlam a direção das dependências
- Decidir onde colocar boundaries é a decisão arquitetural mais importante
- Too many boundaries = over-engineering; too few = coupling
- Boundaries devem proteger business rules de mudanças em detalhes técnicos

### Architecture is About Decisions You Can Defer
- Boa arquitetura permite adiar decisões sobre database, UI, framework
- Se a arquitetura força decisões prematuras sobre detalhes, está errada
- "The database is a detail. The web is a detail."
- Adiar decisões preserva opções e permite melhor informação quando decidir

## Frameworks e Modelos

### Clean Architecture Decision Checklist
1. As business rules estão isoladas de frameworks e UI?
2. O sistema pode ser testado sem database ou web server?
3. O database pode ser trocado sem mudar business logic?
4. O framework pode ser trocado com mudanças limitadas às camadas externas?
5. As dependências apontam sempre para dentro?

### Boundary Placement Framework
1. Identifique o que é business rule e o que é detail
2. Coloque boundary entre business rules e details
3. Garanta que dependências apontam de details para rules
4. Use interfaces para inverter dependências quando necessário
5. Teste business rules sem nenhum detail (in-memory, sem I/O)

## Aplicação ao C-Level Squad

### Para o CEO Agent
- Arquitetura limpa reduz custo de mudança — adaptabilidade estratégica
- Decisões de negócio (mudar database, trocar provider) tornam-se mais baratas
- Investimento em arquitetura é investimento em agilidade de longo prazo

### Para o CTO Agent
- Implementar Clean Architecture como guideline (não dogma) em novos serviços
- SOLID como fundação para code reviews e tech standards
- Adiar decisões de infraestrutura: escolha de DB, cloud provider, framework
- Testabilidade como proxy de qualidade arquitetural

### Para o CFO Agent
- Clean Architecture reduz custo de manutenção (80% do custo de software é manutenção)
- Investimento upfront em arquitetura tem ROI positivo compounding
- Sistemas mal arquitetados acumulam tech debt que cresce exponencialmente

### Para o CMO Agent
- Arquitetura limpa permite mudar UI e experiência sem refazer backend
- Experimentação em produto mais rápida quando business logic está desacoplada

### Para o COO Agent
- Sistemas limpos são mais confiáveis (menos bugs em produção)
- Troca de fornecedores de infra é operacionalmente mais simples
- Testabilidade reduz incidentes operacionais

## Takeaways Acionáveis (top 5)

1. **Dependency Rule é lei** — Dependências SEMPRE para dentro. Se business logic depende
   de framework ou database, a arquitetura precisa de refactoring.

2. **SOLID é fundação** — Antes de patterns sofisticados, domine os cinco princípios.
   São a base de toda decisão de design.

3. **Isole business rules** — O teste definitivo: consigo testar regras de negócio sem
   database, web server ou framework? Se não, as regras não estão isoladas.

4. **Adie decisões** — Boa arquitetura preserva opções. Se precisa decidir database
   antes de escrever business logic, a arquitetura está errada.

5. **Boundaries no lugar certo** — Nem demais (over-engineering) nem de menos (coupling).
   Proteja business rules de detalhes; não proteja detalhes de detalhes.

## Citações-Chave

> "The goal of software architecture is to minimize the human resources required
> to build and maintain the required system."

> "Good architecture makes the system easy to understand, easy to develop, easy
> to maintain, and easy to deploy."

> "A good architect maximizes the number of decisions not made."

> "The database is a detail. The web is a detail. The OS is a detail.
> The framework is a detail."

> "Architecture is about the important stuff. Whatever that is."

## Quando Consultar

- Ao iniciar design de novo sistema ou serviço
- Em code review de decisões arquiteturais
- Quando tech debt está acumulando por coupling excessivo
- Na avaliação de frameworks e ferramentas (são detalhes, não decisões)
- Para treinar engenheiros em princípios de design
- Ao refatorar sistemas legados

## Referências Cruzadas

- **Newman — Building Microservices**: Boundaries entre serviços complementam Clean Architecture
- **Skelton — Team Topologies**: Team boundaries alinhadas com architecture boundaries
- **Forsgren — Accelerate**: Loosely coupled architecture como capability chave
- **Ross — Enterprise Architecture**: Architecture decisions em escala organizacional
- **Goldratt — The Goal**: Minimizar coupling como forma de aumentar throughput
- **Meadows — Thinking in Systems**: Architecture como design de sistema
