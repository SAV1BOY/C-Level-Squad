# Architecture Patterns — Padrões de Arquitetura de Software

> **Domínio:** Engineering & Tech
> **Autor de referência:** Martin Fowler, Sam Newman, Mark Richards & Neal Ford
> **Uso primário:** Selecionar o padrão arquitetural correto para o contexto, estágio e trade-offs do negócio.
> **Agente responsável:** cto-architect

---

## Origem e Contexto

A escolha de padrão arquitetural é uma das decisões Type 1 mais impactantes em tecnologia — difícil de reverter e com consequências de longo prazo em velocidade de desenvolvimento, custo operacional, confiabilidade e capacidade de escala.

Os 4 padrões principais que toda organização de tecnologia deve entender:

1. **Monolith (Monolito):** Toda a aplicação em um único deployment unit.
2. **Modular Monolith:** Monolito com módulos internos bem definidos e boundaries claros.
3. **Microservices:** Serviços independentes, cada um com seu deploy, dados e ciclo de vida.
4. **Event-Driven Architecture (EDA):** Comunicação assíncrona via eventos entre componentes.

A regra de ouro de Martin Fowler: **"Don't start with microservices."** A maioria das empresas começa com monolito, evolui para modular monolith, e migra seletivamente para microservices quando a escala exige. Pular etapas gera complexidade prematura.

Não existe padrão "melhor" — existe o padrão certo para o contexto. E o contexto muda com o tempo.

---

## Quando Usar

- Ao iniciar um novo produto — escolher o padrão inicial correto poupa anos de retrabalho.
- Quando o monolito está sufocando a velocidade de delivery — sinais de que migração pode ser necessária.
- Na avaliação de arquitetura para M&A ou due diligence.
- Ao planejar escala significativa (10x users, 10x transactions).
- Como ADR (`frameworks/engineering-tech/adr-system.md`) quando se decide mudar de padrão.

---

## Quando NÃO Usar

- Para decidir por moda — "todo mundo usa microservices" não é argumento.
- Sem considerar o tamanho do time — microservices requer times grandes e maduros.
- Para resolver problemas organizacionais — arquitetura reflete a organização (Lei de Conway), não o contrário.
- Como decisão puramente técnica — arquitetura é decisão de negócio com implicações técnicas.

---

## Estrutura / Modelo

### Comparativo dos 4 Padrões

```
┌──────────────────┬──────────────┬──────────────┬──────────────┬──────────────┐
│ Dimensão         │  Monolith    │  Modular     │ Microservices│  Event-Driven│
│                  │              │  Monolith    │              │              │
├──────────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ Complexidade     │ Baixa        │ Média        │ Alta         │ Alta         │
│ inicial          │              │              │              │              │
├──────────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ Deploy           │ Único        │ Único        │ Independente │ Independente │
│                  │              │ (podendo     │ por serviço  │ por serviço  │
│                  │              │  ser modular)│              │              │
├──────────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ Escala           │ Vertical     │ Vertical     │ Horizontal   │ Horizontal   │
│                  │              │              │ por serviço  │ por consumer │
├──────────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ Team size ideal  │ 1-15 devs    │ 5-50 devs    │ 20-500+ devs │ 20-500+ devs │
├──────────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ Data             │ Shared DB    │ Schemas      │ DB por       │ Event store +│
│                  │              │ separados    │ serviço      │ eventual     │
│                  │              │              │              │ consistency  │
├──────────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ Comunicação      │ In-process   │ In-process   │ API/gRPC     │ Eventos      │
│                  │              │ (interfaces) │ (síncrono)   │ (assíncrono) │
├──────────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ Melhor para      │ MVP, early-  │ Scale-up,    │ Grande escala│ Sistemas     │
│                  │ stage, time  │ crescendo    │ múltiplos    │ distribuídos │
│                  │ pequeno      │ sem complexi-│ times        │ alto volume  │
│                  │              │ dade prematura│             │              │
├──────────────────┼──────────────┼──────────────┼──────────────┼──────────────┤
│ DORA impact      │ DF alto se   │ DF alto com  │ DF alto por  │ DF alto,     │
│                  │ time pequeno │ boas         │ serviço, LT  │ debugging    │
│                  │              │ boundaries   │ pode subir   │ complexo     │
└──────────────────┴──────────────┴──────────────┴──────────────┴──────────────┘
```

---

## Processo de Aplicação (step-by-step)

### Step 1: Avaliar o Contexto
Responder honestamente:
- Quantos desenvolvedores temos? (< 15 → monolith; 15-50 → modular monolith; 50+ → considerar microservices)
- Qual o estágio do produto? (Pre-PMF → monolith; Growth → modular; Scale → micro/EDA)
- Qual o nível de maturidade DevOps? (DORA Low → monolith; DORA High → pode ser micro)
- Quais são os requisitos de escala? (1K req/s → qualquer; 100K+ → micro/EDA)

### Step 2: Escolher o Padrão Base
Use a decision tree:
```
Time < 15 devs E pré-PMF?
  → MONOLITH (simples, rápido, barato)

Time 15-50 devs E product-market fit?
  → MODULAR MONOLITH (estrutura sem complexidade distribuída)

Time 50+ devs E escala provada?
  → MICROSERVICES (independência de deploy por time)

Alto volume de eventos assíncronos? (filas, notificações, data pipeline)
  → EVENT-DRIVEN (pode ser overlayed em qualquer padrão acima)
```

### Step 3: Documentar como ADR
Registrar a decisão de arquitetura em `frameworks/engineering-tech/adr-system.md`:
- Contexto (por que este padrão)
- Decisão (qual padrão)
- Consequências (trade-offs aceitos)
- Revisão planejada (quando re-avaliar)

### Step 4: Definir Boundaries (para Modular Monolith e Micro)
Para padrões modulares:
- Definir domain boundaries usando Domain-Driven Design (Bounded Contexts).
- Cada módulo/serviço tem: interface pública clara, dados próprios, contrato de API.
- Minimizar acoplamento entre módulos.

### Step 5: Planejar Migração (quando necessário)
Migração de monolith para microservices:
1. **Strangler Fig Pattern:** Novas features como serviços; migrar features antigas gradualmente.
2. **Database-first:** Separar dados antes de separar código.
3. **Branch by abstraction:** Criar interfaces abstratas, implementar novo backend por trás.
4. **Nunca reescrever do zero** — migrar incrementalmente. Rewrite = projeto de 18 meses que nunca termina.

### Step 6: Revisar Regularmente
Arquitetura não é decisão one-shot:
- Revisar na QBR de tecnologia.
- Trigggers de re-avaliação: time dobrou de tamanho, latência crítica, deploy friction.

---

## Exemplos Práticos

### Exemplo 1: Startup SaaS (Série Seed, 8 devs)
**Decisão:** Monolith em Rails/Django/Next.js.
**Razão:** Velocidade de iteração máxima. Time pequeno. Product-market fit não comprovado.
**ADR registrado:** "Monolith até atingir 50K users ou 15 devs, o que vier primeiro."

### Exemplo 2: Scale-up (Série B, 35 devs)
**Decisão:** Migrar de monolith para modular monolith.
**Razão:** Monolith está com conflitos de merge frequentes, deploy demorado, coupling alto.
**Ação:** Definir 5 bounded contexts, separar schemas no DB, criar interfaces entre módulos.
**Não fazer:** Pular para microservices — o time não tem maturidade DevOps (DORA: Medium).

### Exemplo 3: Enterprise (200 devs, 20 squads)
**Decisão:** Microservices + Event-Driven para domínios de alto volume.
**Razão:** Times independentes precisam deploy independente. Volume de transações requer escala horizontal.
**Ação:** 15 microservices para domínios core, event bus (Kafka) para comunicação assíncrona.
**Cuidado:** Service mesh, distributed tracing e contract testing são obrigatórios nessa escala.

---

## Armadilhas Comuns

1. **Microservices prematuros:** 5 devs com 15 microservices = complexidade distribuída sem benefício.
2. **Monolith distribuído:** "Microservices" que são altamente acoplados — pior dos dois mundos.
3. **Ignorar Lei de Conway:** A arquitetura vai espelhar a estrutura de comunicação da organização.
4. **Rewrite completo:** "Vamos reescrever tudo em microservices" é o projeto que mata empresas.
5. **Sem observability:** Microservices sem tracing distribuído é debugar no escuro.
6. **Data sharing via DB:** Microservices acessando o mesmo banco destrói a independência.
7. **Over-engineering de eventos:** Event-driven para CRUD simples é complexidade desnecessária.
8. **Não documentar decisão:** Sem ADR, a próxima pessoa não sabe por que foi escolhido.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/engineering-tech/dora-metrics.md` | Padrão arquitetural impacta diretamente DORA metrics. Medir antes e depois. |
| `frameworks/engineering-tech/adr-system.md` | Toda decisão de arquitetura é registrada como ADR. |
| `frameworks/engineering-tech/build-vs-buy-framework.md` | Componentes comprados devem integrar com o padrão escolhido. |
| `frameworks/engineering-tech/platform-engineering.md` | A plataforma interna suporta o padrão escolhido (templates, pipelines). |
| `frameworks/engineering-tech/sre-basics.md` | SRE practices variam por padrão (SLOs por serviço em micro). |
| `frameworks/vision-strategy/wardley-mapping.md` | Wardley map mostra quais componentes são custom vs commodity. |
| `checklists/tech-architecture-decision-quality.md` | Checklist para validar decisões de arquitetura. |

---

## Referências

- Fowler, M. "MonolithFirst." martinfowler.com.
- Newman, S. (2021). *Building Microservices*. 2nd Ed. O'Reilly.
- Richards, M. & Ford, N. (2020). *Fundamentals of Software Architecture*. O'Reilly.
- Vernon, V. (2013). *Implementing Domain-Driven Design*. Addison-Wesley.
- Skelton, M. & Pais, M. (2019). *Team Topologies*. IT Revolution.
