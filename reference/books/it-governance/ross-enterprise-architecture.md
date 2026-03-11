# Enterprise Architecture as Strategy — Jeanne Ross, Peter Weill & David Robertson

## Resumo Executivo

Ross, Weill e Robertson demonstram que empresas com foundation for execution madura —
IT infrastructure e dados compartilhados padronizados — superam significativamente seus
peers em lucratividade, time-to-market e eficiência operacional. O livro introduz o
conceito de Operating Model como base para decisões de enterprise architecture.

A tese central: antes de escolher tecnologia, defina o Operating Model. A arquitetura
empresarial deve refletir escolhas sobre integração e padronização dos processos de negócio.

## Conceitos-Chave

### Operating Model (4 Quadrantes)
Definido por duas dimensões:
- **Standardization** (eixo Y): Processos são padronizados entre unidades de negócio?
- **Integration** (eixo X): Dados/processos são compartilhados entre unidades?

| | Baixa Integração | Alta Integração |
|---|---|---|
| Alta Padronização | **Replication** (McDonald's) | **Unification** (UPS) |
| Baixa Padronização | **Diversification** (Conglomerado) | **Coordination** (Merrill Lynch) |

### Foundation for Execution
- **IT Infrastructure**: Plataforma tecnológica compartilhada
- **Data**: Dados compartilhados e padronizados (master data)
- **Core Processes**: Processos de negócio digitized e embedded
- Maturidade crescente: Silos → Standardized → Optimized → Modular

### Architecture Maturity Stages
1. **Business Silos**: Cada unidade tem seus próprios sistemas, dados isolados
2. **Standardized Technology**: Plataforma tecnológica compartilhada, mas processos ainda locais
3. **Optimized Core**: Processos padronizados e dados compartilhados enterprise-wide
4. **Business Modularity**: Componentes reusáveis que permitem recombinação ágil

### Engagement Model
- Como IT e negócio interagem na tomada de decisões de arquitetura
- Três mecanismos: governance, project management, linking mechanisms
- O engagement model deve evoluir com a maturidade da arquitetura
- Sem engagement model, architecture decisions são ad hoc e inconsistentes

### Core Diagram
- Representação visual dos core processes, data e tecnologia da empresa
- Uma página que mostra o "foundation for execution"
- Ferramenta de comunicação entre IT e business — linguagem comum
- Deve ser compreensível por executivos não-técnicos

## Frameworks e Modelos

### Operating Model Selection
1. Listar as unidades de negócio/processos chave
2. Para cada par, perguntar: devem ser padronizados? Devem compartilhar dados?
3. O padrão dominante define o operating model
4. O operating model orienta TODAS as decisões de arquitetura subsequentes

### Architecture Maturity Assessment
1. Em que estágio cada área/processo está? (silos, standardized, optimized, modular)
2. Qual o estágio-alvo para os próximos 2-3 anos?
3. Que investimentos são necessários para avançar de estágio?
4. O engagement model suporta a evolução?

## Aplicação ao C-Level Squad

### Para o CEO Agent
- Definir o Operating Model como decisão estratégica (não técnica)
- Garantir que investimento em architecture se alinhe com o operating model
- Usar Core Diagram como ferramenta de comunicação com board e stakeholders

### Para o CTO Agent
- Traduzir Operating Model em enterprise architecture decisions
- Gerenciar maturidade: mover da fase atual para a próxima fase sistematicamente
- Construir foundation for execution (infra, data, processos) como plataforma

### Para o CFO Agent
- Justificar investimento em architecture pelo retorno em eficiência e agilidade
- Empresas com foundation madura têm 25% maior lucratividade (dados do MIT CISR)
- Alocar budget para architecture maturity, não apenas para projetos pontuais

### Para o CMO Agent
- Architecture madura permite personalização em escala (dados compartilhados)
- Customer data platform como componente de integration no operating model

### Para o COO Agent
- Operating Model define grau de padronização operacional
- Foundation for execution automatiza e padroniza core processes
- Maturidade arquitetural reduz custo operacional e aumenta consistência

## Takeaways Acionáveis (top 5)

1. **Defina o Operating Model** — Antes de qualquer decisão de arquitetura, responda:
   padronizamos processos? Integramos dados? A resposta determina o modelo.

2. **Avalie a maturidade atual** — Em que estágio está? Silos, standardized, optimized
   ou modular? O gap entre atual e desejado é seu roadmap de investimento.

3. **Crie o Core Diagram** — Uma página que mostra processos core, dados compartilhados
   e plataforma tecnológica. Ferramenta de alinhamento IT-business.

4. **Invista em foundation** — Infrastructure, dados e processos compartilhados antes de
   projetos pontuais. Foundation madura acelera tudo depois.

5. **Evolua o engagement model** — Como IT e negócio decidem juntos sobre arquitetura?
   Sem governance e linking mechanisms, architecture é acidental.

## Citações-Chave

> "Companies with more mature architectures achieved 25% greater profitability
> than industry average."

> "The operating model is the necessary level of business process integration
> and standardization for delivering goods and services to customers."

> "IT architecture is the organizing logic for data, applications, and infrastructure."

> "Don't start with technology. Start with the operating model."

## Quando Consultar

- Na definição de estratégia de IT e enterprise architecture
- Ao avaliar investimentos em plataformas e infraestrutura compartilhada
- Quando há tensão entre padronização e autonomia local
- Na decisão de build vs. buy para sistemas core
- Para comunicar valor de investimento em arquitetura para stakeholders de negócio

## Referências Cruzadas

- **Weill — IT Governance**: Governance como enabler do operating model
- **Newman — Building Microservices**: Microservices como business modularity
- **Skelton — Team Topologies**: Organização de times alinhada com architecture
- **Martin — Clean Architecture**: Princípios de design dentro do enterprise context
- **Kim — Phoenix Project**: DevOps como caminho para architecture maturity
- **Forsgren — Accelerate**: Capabilities que habilitam foundation for execution
