# Accelerate — Nicole Forsgren, Jez Humble & Gene Kim (2018)

## Resumo Executivo

Forsgren, Humble e Kim apresentam quatro anos de pesquisa empírica do programa DORA
(DevOps Research and Assessment) que identifica as capabilities e práticas que predizem
alta performance em software delivery e organizacional. O livro transforma DevOps de
buzzword em ciência, com métricas validadas e relações causais demonstradas.

A tese central: software delivery performance prediz performance organizacional (lucratividade,
market share, produtividade). E as capabilities que a impulsionam são mensuráveis e aprendíveis.

## Conceitos-Chave

### Four Key Metrics (DORA Metrics)
1. **Deployment Frequency**: Quão frequentemente a organização faz deploy em produção
2. **Lead Time for Changes**: Tempo do commit até o deploy em produção
3. **Change Failure Rate**: % de deploys que causam falha em produção
4. **Time to Restore Service**: Tempo para restaurar serviço após incidente

### Software Delivery Performance → Organizational Performance
- Correlação forte e causal entre delivery performance e resultados de negócio
- Elite performers: deploy múltiplas vezes por dia, lead time < 1 hora, CFR < 15%, restore < 1 hora
- Low performers: deploy menos que 1x/mês, lead time 1-6 meses, CFR 46-60%, restore > 6 meses
- A diferença entre elite e low performers está crescendo — não diminuindo

### 24 Key Capabilities (Agrupadas)
**Continuous Delivery:**
- Version control, deployment automation, continuous integration
- Trunk-based development, test automation, test data management
- Shift left on security, loosely coupled architecture
- Empowered teams, monitoring and observability

**Architecture:**
- Loosely coupled architecture permite deploys independentes
- Teams que podem testar e deployar independentemente performam melhor
- Architecture importa mais que tools — microservices não são requisito, loose coupling sim

**Product and Process:**
- Customer feedback loops, team experimentation
- Work in small batches, visibility of work
- Lightweight change approval (não approval committees pesados)

**Lean Management:**
- WIP limits, visual management, monitoring and proactive notification
- Lightweight change approval, work in small batches

**Culture (Westrum Model):**
- **Pathological**: Power-oriented, blame, silos, low cooperation
- **Bureaucratic**: Rule-oriented, modest cooperation, narrow responsibility
- **Generative**: Performance-oriented, high cooperation, shared risks, novelty encouraged
- Cultura generativa prediz tanto delivery performance quanto organizational performance

### Burnout e Deployment Pain
- Deployment pain é inversamente correlacionado com delivery performance
- Equipes que deployam com frequência sentem menos dor por deploy
- Burnout correlaciona com cultura patológica, não com carga de trabalho
- Investir em capabilities técnicas reduz burnout

### Transformational Leadership
- Líderes que inspiram, estimulam intelectualmente e demonstram consideration
- Correlação forte entre transformational leadership e adoption de capabilities
- O líder não faz o trabalho técnico — cria contexto para que o time faça
- Apoiar experimentação e tolerar falhas é responsabilidade da liderança

## Frameworks e Modelos

### DORA Metrics — Níveis de Performance
| Metric | Elite | High | Medium | Low |
|--------|-------|------|--------|-----|
| Deploy Frequency | Multiple/day | Weekly-Monthly | Monthly-Biannual | <1/6 months |
| Lead Time | <1 hour | 1 day-1 week | 1-6 months | >6 months |
| Change Failure Rate | 0-15% | 16-30% | 16-30% | 46-60% |
| Time to Restore | <1 hour | <1 day | 1 day-1 week | >6 months |

### Westrum Culture Assessment
Para cada afirmação, avalie (1-7):
1. Informação é ativamente buscada
2. Mensageiros não são punidos
3. Responsabilidades são compartilhadas
4. Cross-functional collaboration é incentivada
5. Falhas levam a inquiry, não blame
6. Novas ideias são bem-vindas

### Improvement Kata (Baseado em Toyota Kata)
1. **Understand the direction**: Onde queremos chegar? (DORA metrics targets)
2. **Grasp current condition**: Onde estamos hoje? (medição honest)
3. **Establish next target**: Que capability melhorar primeiro?
4. **Experiment toward target**: Pequenas melhorias iterativas
5. **Repeat**: Próxima capability após atingir target

## Aplicação ao C-Level Squad

### Para o CEO Agent
- Usar DORA metrics como indicador de health organizacional (não apenas técnica)
- Investir em cultura generativa (Westrum) como fundação de performance
- Reconhecer que software delivery performance prediz business outcomes

### Para o CTO Agent
- Implementar DORA metrics como North Star de engineering performance
- Priorizar capabilities que têm maior impacto nas métricas
- Loosely coupled architecture como decisão estratégica (não apenas técnica)
- Cultura generativa em engineering: blameless postmortems, experimentação, shared ownership

### Para o CFO Agent
- Justificar investimento em DevOps/platform com correlação a business outcomes
- DORA metrics como leading indicators de produtividade de engineering
- ROI de automação: menos deployment pain = menos burnout = menos turnover

### Para o CMO Agent
- Lead time reduzido permite experimentação mais rápida em produto e marketing
- Deployment frequency alta permite A/B testing e feature flags para marketing
- Feedback loops de cliente como capability que beneficia produto e marketing

### Para o COO Agent
- Monitoring e observability como capabilities operacionais críticas
- Incidence response (time to restore) como métrica operacional
- Visibility of work e WIP limits como práticas operacionais lean

## Takeaways Acionáveis (top 5)

1. **Meça DORA metrics** — Deployment frequency, lead time, change failure rate, time to
   restore. Se não mede, não pode melhorar. Comece medindo esta semana.

2. **Invista em cultura generativa** — Westrum model. Blame → learning. Silos → collaboration.
   Cultura é a capability com maior impacto sistêmico.

3. **Automate everything** — CI/CD, testing, deployment, monitoring. Automação é o investimento
   com maior retorno para delivery performance.

4. **Work in small batches** — Deploys menores são mais seguros, mais rápidos para entregar
   valor e mais fáceis de debugar quando falham.

5. **Loosely coupled architecture** — Permita que times façam deploy independentemente.
   Isso requer investment em architecture, mas o retorno é exponencial.

## Citações-Chave

> "High performers are doing significantly better at all four measures — they are
> not trading off speed for stability or vice versa."

> "There is no trade-off between improving performance and achieving higher levels
> of stability and quality."

> "Culture enables information processing through three mechanisms: it allows the
> organization to avoid making more of certain types of mistakes, it allows for
> more effective recovery, and it enhances the organization's ability to innovate."

> "Continuous delivery makes your software deployments painless, low-risk events
> that can be performed at any time, on demand."

## Quando Consultar

- Ao avaliar e melhorar performance de software delivery
- Na definição de métricas de engineering (DORA como standard)
- Para justificar investimento em DevOps, CI/CD, automação
- Ao diagnosticar burnout e deployment pain em engineering
- Na avaliação de cultura de engineering (Westrum model)
- Para argumentar que delivery performance impacta business outcomes

## Referências Cruzadas

- **Kim — Phoenix Project**: Narrativa ficcional dos princípios de Accelerate
- **Skelton — Team Topologies**: Organização de times para loose coupling
- **Martin — Clean Architecture**: Architecture decisions que habilitam loose coupling
- **Newman — Building Microservices**: Implementação de loosely coupled architecture
- **Grove — High Output Management**: Métricas e production principles
- **Goldratt — The Goal**: Flow e throughput como princípios fundamentais
