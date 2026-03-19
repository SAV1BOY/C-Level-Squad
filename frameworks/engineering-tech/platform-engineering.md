# Platform Engineering — Engenharia de Plataforma Interna

> **Domínio:** Engineering & Tech
> **Autor de referência:** Team Topologies (Skelton & Pais), Humanitec, Gartner
> **Uso primário:** Construir plataforma interna de developer experience que acelera delivery e reduz cognitive load.
> **Agente responsável:** cto-architect

---

## Origem e Contexto

Platform Engineering é a disciplina de projetar e construir toolchains e workflows de self-service que habilitam engenheiros de software a entregar valor com autonomia. Segundo o Gartner, até 2026, 80% das organizações de engenharia terão times de plataforma interna.

O problema que Platform Engineering resolve: **conforme a organização cresce, a complexidade de infra, CI/CD, observability e compliance aumenta exponencialmente.** Sem plataforma, cada squad reinventa a roda — ou fica bloqueado esperando o "time de DevOps."

O conceito central é o **Golden Path** (caminho dourado): o caminho mais fácil, rápido e seguro para ir do código ao deploy em produção. O golden path é opinado (as decisões já foram tomadas) mas não mandatório (pode sair do caminho se tiver razão boa).

Platform Engineering NÃO é:
- Um time de DevOps renomeado.
- Infraestrutura como código (IaC) sozinha.
- Uma plataforma que ninguém usa porque não foi feita com o developer como cliente.

Platform Engineering É:
- Uma Internal Developer Platform (IDP) construída como produto.
- Self-service: developers fazem deploy sem ticket.
- Opinionated but not mandatory: golden paths são padrão, não prisão.
- Developer-centric: o "cliente" da plataforma é o engenheiro.

---

## Quando Usar

- Quando a organização de engenharia ultrapassa 30-50 developers.
- Quando o tempo de onboarding de novo dev é > 2 semanas.
- Quando times ficam bloqueados esperando "o time de infra" para deploy, ambiente ou acesso.
- Quando há fragmentação de tooling — cada squad usa ferramentas diferentes para o mesmo problema.
- Quando DORA metrics (`frameworks/engineering-tech/dora-metrics.md`) estão degradando por complexidade de infra.

---

## Quando NÃO Usar

- Com < 15-20 developers — nesse tamanho, DevOps compartilhado é suficiente.
- Quando não há buy-in do CTO — plataforma sem patrocínio executivo morre.
- Como projeto de 18 meses sem entrega incremental — plataforma deve ser construída iterativamente.
- Para resolver problemas que são organizacionais, não técnicos.

---

## Estrutura / Modelo

### Layers da Internal Developer Platform

```
┌─────────────────────────────────────────────────────────────────────┐
│                  INTERNAL DEVELOPER PLATFORM                         │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  LAYER 5: Developer Portal (UI/UX)                                  │
│  └── Catálogo de serviços, docs, status, self-service               │
│                                                                      │
│  LAYER 4: Golden Paths (Templates & Workflows)                      │
│  └── Scaffolding de novo serviço, pipeline padrão, deploy workflow  │
│                                                                      │
│  LAYER 3: Build & Deploy (CI/CD)                                    │
│  └── Pipeline automatizado, feature flags, rollback                 │
│                                                                      │
│  LAYER 2: Runtime (Compute & Networking)                            │
│  └── Kubernetes, serverless, service mesh, load balancing           │
│                                                                      │
│  LAYER 1: Infrastructure (Cloud Resources)                          │
│  └── IaC (Terraform/Pulumi), databases, storage, secrets            │
│                                                                      │
│  CROSS-CUTTING: Observability, Security, Compliance                 │
│  └── Logs, metrics, traces, RBAC, audit trail, vulnerability scan   │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

### Team Topologies Integration

| Tipo de Time | Papel na Plataforma |
|-------------|-------------------|
| **Platform Team** | Constrói e mantém a IDP. Trata developers como clientes. |
| **Stream-aligned Team** | Consome a plataforma. Foco em entregar valor de negócio. |
| **Enabling Team** | Ajuda stream-aligned a adotar a plataforma. Coaching, não execução. |
| **Complicated Subsystem Team** | Constrói componentes complexos (ML, criptografia) que a plataforma expõe como serviço. |

---

## Processo de Aplicação (step-by-step)

### Step 1: Mapear Developer Journey
Antes de construir, entender a experiência atual do developer:
- Quanto tempo para configurar ambiente local?
- Quantos passos para fazer deploy em produção?
- Onde ficam bloqueados? Onde esperam?
- Quais ferramentas usam? São consistentes entre squads?

Técnica: Developer survey + shadowing (acompanhar um dev por 1 dia).

### Step 2: Identificar o Maior Ponto de Dor
Da jornada mapeada, priorizar o maior ponto de dor:
- Se deploy é manual e lento → golden path de CI/CD primeiro.
- Se onboarding leva semanas → scaffolding de novo serviço primeiro.
- Se incidents são difíceis de diagnosticar → observability stack primeiro.

### Step 3: Construir o Primeiro Golden Path (MVP)
O primeiro golden path deve resolver o ponto de dor mais agudo:
- Criar template de novo serviço (cookiecutter/yeoman) com CI/CD pré-configurado.
- Pipeline que vai de commit → build → test → staging → production em < 30 minutos.
- Self-service: developer faz deploy sem abrir ticket.

### Step 4: Tratar a Plataforma como Produto
A plataforma tem "clientes" (developers) e precisa de product management:
- **Developer survey** trimestral: NPS da plataforma, maiores dores.
- **Roadmap** público: o que está sendo construído e por quê.
- **Documentation** de qualidade: se precisa perguntar no Slack, a doc falhou.
- **SLA** interno: "novos serviços deployados em < 2 horas."

### Step 5: Expandir Incrementalmente
Após o primeiro golden path funcionar, expandir:
- Golden path para diferentes stacks (Python, Node, Go).
- Self-service de banco de dados (criar DB sem ticket).
- Observability pré-configurada (logs, metrics, traces out-of-the-box).
- Security scanning automatizado no pipeline.

### Step 6: Medir Impacto
Métricas da plataforma:
- **Adoption rate:** % de squads usando a plataforma.
- **Developer satisfaction:** NPS/CSAT do developer.
- **DORA metrics improvement:** DF, LT, CFR, MTTR antes e depois.
- **Onboarding time:** Tempo para novo dev fazer primeiro deploy.
- **Self-service ratio:** % de operações feitas sem ticket/intervenção humana.

---

## Exemplos Práticos

### Exemplo: Scale-up com 60 Developers

**Antes da plataforma:**
- Deploy: 15 steps manuais, 2h, requer SRE presente.
- Novo serviço: 2 semanas para configurar infra, CI/CD, monitoring.
- Onboarding: 3 semanas até primeiro deploy produtivo.
- DORA: DF weekly, LT 5 dias.

**Depois da plataforma (12 meses):**
- Deploy: 1 click, 20 minutos, self-service.
- Novo serviço: Template + golden path = 2 horas até deploy.
- Onboarding: 3 dias até primeiro deploy produtivo.
- DORA: DF daily, LT 1 dia.

**Investimento:** 3 engineers dedicados (Platform Team) por 12 meses.
**ROI:** 57 engineers produzindo ~30% mais output = equivalente a +17 engineers. ROI > 5x.

---

## Armadilhas Comuns

1. **Build it and they won't come:** Plataforma construída sem ouvir os developers. Resultado: ninguém usa.
2. **Mandatório desde o dia 1:** Forçar adoção da plataforma antes de ela ser boa. Golden paths devem ser atrativos, não obrigatórios.
3. **Plataforma como gatekeeper:** Platform team que cria burocracia em vez de self-service. O objetivo é ACELERAR, não controlar.
4. **Over-engineering:** Construir plataforma para 1000 devs quando se tem 50. YAGNI (You Aren't Gonna Need It).
5. **Sem product management:** Tratar plataforma como projeto de infra, não como produto. Sem roadmap, sem feedback loop, sem priorização.
6. **Time de 1 pessoa:** Platform engineering requer investimento real. 1 dev part-time não constrói plataforma.
7. **Ignorar legacy:** Focar só em greenfield e esquecer que 80% do código é legacy rodando em infra antiga.
8. **Renomear DevOps:** Chamar o time de DevOps de "Platform Team" sem mudar o modelo de operação (ticket-based → self-service).

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/engineering-tech/dora-metrics.md` | Plataforma é o maior alavancador de melhoria em DORA metrics. |
| `frameworks/engineering-tech/architecture-patterns.md` | A plataforma suporta o padrão arquitetural escolhido. |
| `frameworks/engineering-tech/sre-basics.md` | Observability e incident management são layers da plataforma. |
| `frameworks/engineering-tech/adr-system.md` | Decisões de plataforma são documentadas como ADRs. |
| `frameworks/engineering-tech/build-vs-buy-framework.md` | Cada componente da plataforma é decisão build vs buy. |
| `frameworks/vision-strategy/wardley-mapping.md` | Plataforma comoditiza componentes internos via golden paths. |
| `frameworks/operating-system/okrs.md` | OKRs de plataforma medem adoption, satisfaction e DORA impact. |

---

## Referências

- Skelton, M. & Pais, M. (2019). *Team Topologies*. IT Revolution.
- Humanitec. "What is Platform Engineering?" platformengineering.org.
- Gartner. "Platform Engineering Will Transform Software Delivery." (2024 prediction.)
- Spotify. "Backstage: An Open Platform for Building Developer Portals." backstage.io.
- Forsgren, N. et al. (2018). *Accelerate*. IT Revolution. (DORA metrics impactados por plataforma.)
