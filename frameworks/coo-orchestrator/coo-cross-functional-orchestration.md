# Orquestração Cross-Funcional — Framework de Coordenação entre Áreas

## Origem e Contexto

À medida que organizações crescem, a complexidade de coordenação cresce exponencialmente.
Uma empresa com 5 equipes tem 10 interfaces possíveis entre elas. Com 10 equipes, são 45.
Com 20 equipes, são 190. Cada interface é um ponto potencial de desalinhamento, atraso,
conflito e perda de informação.

A Orquestração Cross-Funcional resolve o problema de coordenar equipes que precisam
trabalhar juntas mas respondem a líderes diferentes, têm prioridades diferentes, e
frequentemente falam "idiomas" diferentes (engenharia fala em sprints, vendas fala em
pipeline, finanças fala em budget).

O framework se inspira em: teoria de organizações matriciais (Jay Galbraith), o modelo
de Team Topologies (Matthew Skelton), protocolos de comunicação em sistemas distribuídos,
e práticas de orquestração de APIs — tratando equipes como serviços com interfaces definidas.

## Quando Usar

- Quando projetos cross-functional atrasam consistentemente
- Quando há "guerra entre áreas" ou finger-pointing sobre responsabilidades
- Quando equipes reclamam de "dependências bloqueantes" de outras equipes
- Na implementação de iniciativas que requerem 3+ equipes coordenadas
- Quando a organização cresce além de 50 pessoas e coordenação informal falha
- Após reorganizações que mudam interfaces entre equipes

## Quando NÃO Usar

- Em equipes pequenas (< 15 pessoas) onde conversa direta resolve
- Para substituir ownership claro (orquestração complementa, não substitui)
- Como burocracia adicional em cima de processos que já funcionam
- Para controlar equipes autônomas que estão performando bem

## Estrutura / Modelo

### Mapa de Dependências Organizacionais

```
              ┌──────────┐
              │ PRODUTO  │
              │ (define) │
              └────┬─────┘
                   │
         ┌─────────┼─────────┐
         ▼         ▼         ▼
    ┌─────────┐ ┌─────┐ ┌────────┐
    │ DESIGN  │ │ ENG │ │ DATA   │
    │(desenha)│ │(constrói)│ │(instrumenta)│
    └────┬────┘ └──┬──┘ └───┬────┘
         │         │        │
         └─────────┼────────┘
                   ▼
              ┌─────────┐
              │   QA    │
              │(valida) │
              └────┬────┘
                   ▼
         ┌─────────┼─────────┐
         ▼         ▼         ▼
    ┌─────────┐ ┌──────┐ ┌─────────┐
    │MARKETING│ │VENDAS│ │CUSTOMER │
    │(comunica)│ │(vende)│ │ SUCCESS │
    └─────────┘ └──────┘ └─────────┘

INTERFACES CRÍTICAS (onde mais há atrito):
  → Produto ↔ Engenharia (escopo e prazo)
  → Engenharia ↔ QA (qualidade e velocidade)
  → Produto ↔ Marketing (posicionamento e timing)
  → Vendas ↔ Customer Success (handoff de cliente)
  → Data ↔ Todos (demandas de analytics)
```

### Modelo de Interface entre Equipes

```
INTERFACE: [Equipe A] ↔ [Equipe B]
Owner da interface: [Nome — geralmente um dos dois líderes]

CONTRATO DE SERVIÇO (inspirado em API design):
┌────────────────────────────────────────────────┐
│ INPUT (o que A entrega para B)                  │
│   Formato: [spec, ticket, briefing, dados]      │
│   Qualidade mínima: [critérios de acceptance]   │
│   Cadência: [quando é entregue]                 │
│   SLA: [tempo máximo de resposta de B]          │
│                                                  │
│ OUTPUT (o que B devolve para A)                  │
│   Formato: [deliverable, feedback, dados]       │
│   Cadência: [quando é devolvido]                │
│   SLA: [tempo máximo de entrega]                │
│                                                  │
│ SYNC POINTS (quando A e B se encontram)         │
│   Regular: [reunião semanal / async update]     │
│   Escalação: [quando e para quem escalar]       │
│                                                  │
│ MÉTRICAS DA INTERFACE                           │
│   Lead time: [tempo de request a delivery]      │
│   Rework rate: [% de devoluções por qualidade]  │
│   Satisfaction: [NPS mútuo trimestral]          │
└────────────────────────────────────────────────┘
```

### Framework DACI para Decisões Cross-Functional

```
D — DRIVER (quem conduz a decisão — 1 pessoa)
  → Responsável por chegar à decisão no prazo
  → Organiza as informações e facilita o processo
  → NÃO necessariamente toma a decisão

A — APPROVER (quem decide — 1 pessoa, máximo 2)
  → Tem autoridade para tomar a decisão final
  → Pode vetar, mas deve explicar o porquê
  → Se há 2 approvers e discordam, 1 desempata

C — CONTRIBUTORS (quem contribui — quantos necessário)
  → Fornecem input, perspectiva, dados
  → São consultados antes da decisão
  → Não têm poder de veto

I — INFORMED (quem é informado — after the fact)
  → São notificados após a decisão
  → Podem questionar mas não bloquear
  → Recebem contexto suficiente para executar
```

## Processo de Aplicação (step-by-step)

### Passo 1: Mapear o Ecossistema de Dependências (1 semana)

Crie o mapa de dependências da organização:

**Método de entrevista**:
- Para cada equipe, pergunte: "De quem vocês dependem para entregar?" e
  "Quem depende de vocês?"
- Classifique cada dependência: blocking (para tudo), supporting (atrasa mas não para),
  informational (precisa saber mas não bloqueia)

**Método de análise de tickets**:
- Examine tickets/requests entre equipes nos últimos 3 meses
- Quantifique: volume, tempo de resolução, frequência de escalação
- Identifique os handoffs mais problemáticos (alto volume + alto tempo)

**Output**: mapa visual de dependências com classificação de criticidade.

### Passo 2: Identificar Interfaces Problemáticas (2-3 dias)

Priorize as interfaces que mais causam atrito:

**Sinais de interface problemática**:
- Reclamações recorrentes de ambos os lados
- Tempo de handoff > 2x o razoável
- Rework rate > 20% (volta e meia o trabalho é devolvido)
- Escalações frequentes para liderança sênior
- Pessoas duplicando trabalho por não confiarem na outra equipe

**Priorize**: selecione as 3-5 interfaces mais críticas para intervenção.
Não tente consertar todas ao mesmo tempo.

### Passo 3: Definir Contratos de Interface (1-2 semanas)

Para cada interface prioritária:

**Workshop de definição (2h por interface)**:
- Reúna os líderes e representantes de ambas as equipes
- Trabalhe o template de contrato de serviço
- Negocie SLAs realistas (baseados em dados, não aspirações)
- Defina critérios de qualidade mínima do input
- Combine cadência de sync e protocolo de escalação

**Regras de design de interface**:
- **Minimize handoffs**: se possível, elimine a transferência completamente
  (equipe cross-functional > handoff entre equipes)
- **Defina formato**: quando o input está em formato claro, o processamento é mais rápido
- **Automatize o trivial**: se o handoff é padronizado, automatize
- **Bufferise o variável**: se o handoff é variável, crie fila com SLA

### Passo 4: Implementar Mecanismos de Coordenação (2-4 semanas)

Escolha os mecanismos adequados para cada situação:

**Para coordenação leve (interfaces de baixa criticidade)**:
- Async updates em canal compartilhado (Slack/Teams)
- Dashboard de status visível para ambas as equipes
- Representante de cada equipe com ponto de contato claro

**Para coordenação média (interfaces de média criticidade)**:
- Sync semanal de 30 min entre representantes
- Kanban compartilhado para requests entre equipes
- Review mensal de métricas da interface

**Para coordenação pesada (interfaces de alta criticidade)**:
- Equipe cross-functional dedicada para a iniciativa
- Daily sync enquanto durar a iniciativa
- DACI definido para todas as decisões
- Retrospectiva quinzenal de eficácia da coordenação

**Para projetos temporários cross-functional**:
- War room (físico ou virtual) com representantes dedicados
- Project manager/driver neutro (não pertence a nenhuma das equipes)
- Cadência mais frequente com timeline definido
- Clear definition of done e critérios de sucesso

### Passo 5: Implementar DACI para Decisões (1-2 semanas)

Para as decisões mais frequentes entre equipes, pré-defina o DACI:

```
DECISÃO                          │ DRIVER  │ APPROVER │ CONTRIBUTORS    │ INFORMED
─────────────────────────────────┼─────────┼──────────┼─────────────────┼──────────
Prioridade do roadmap            │ PM      │ CPO      │ Eng, Design, CS │ All
Arquitetura técnica              │ Tech Lead│ CTO     │ PM, DevOps      │ All
Precificação                     │ Rev Ops │ CFO      │ Sales, PM, Mkt  │ CS, All
Posicionamento de mercado        │ PMM     │ CMO      │ PM, Sales, CEO  │ All
Contratação > gerente            │ Hiring Mgr│ VP Área│ HR, Finance     │ Team
Resposta a incidente P1          │ On-call │ VP Eng   │ CS, Comms       │ CEO, All
```

### Passo 6: Medir e Otimizar (ongoing)

Métricas de saúde da orquestração:

**Métricas quantitativas**:
- Lead time de requests cross-functional (target: diminuindo)
- Escalation rate (target: < 10% de requests precisam escalar)
- Rework rate entre equipes (target: < 15%)
- % de projetos cross-functional entregues no prazo (target: > 70%)

**Métricas qualitativas**:
- NPS entre equipes (trimestral): "De 0-10, como avalia a colaboração com [equipe]?"
- Survey de atrito: "Qual interface mais te atrasa no dia-a-dia?"
- Retrospectiva cross-team: o que está funcionando, o que não está?

## Exemplos Práticos

### Exemplo 1: Interface Produto-Engenharia

**Problema**: PMs escreviam specs vagas, engenheiros reclamavam de retrabalho.
Engenheiros questionavam decisões de produto mid-sprint. Atrito constante.

**Solução**:
- Contrato: PM entrega spec no formato PRD com criterios de aceitação + wireframe
- Critério mínimo: spec revisada por 1 engenheiro antes de entrar na sprint
- SLA: engenharia responde com estimativa em 48h após receber spec aprovada
- Sync: planning meeting com PM + Tech Lead + Designer toda segunda
- DACI: PM é driver, CPO é approver, Eng é contributor
- Métrica: rework rate caiu de 35% para 12% em 2 trimestres

### Exemplo 2: Handoff Vendas → Customer Success

**Problema**: vendedores prometiam funcionalidades que não existiam. CS herdava
clientes frustrados. NPS caía 30 dias após o onboarding.

**Solução**:
- Handoff document obrigatório: o que foi prometido, expectativas, perfil do cliente
- Período de overlap: vendedor participa do primeiro call de onboarding
- Shared CRM com campos de "promessas feitas" visíveis para CS
- Feedback loop mensal: CS reporta "promises vs reality" para Sales leadership
- Métrica: NPS 30-day subiu de 32 para 58 em 3 meses

### Exemplo 3: Orquestração de Lançamento de Produto

**Coordenação necessária**: Produto + Eng + Design + Marketing + Vendas + CS + Legal

**Mecanismo**:
- Launch driver: PMM (Product Marketing Manager) como DACI driver
- Launch checklist compartilhada com owners por item
- T-30 days: marketing materials review
- T-14 days: sales enablement e CS training
- T-7 days: beta feedback review + go/no-go decision (CPO approves)
- T-1 day: all-systems check
- T-0: coordinated launch
- T+7 days: launch retrospective

## Armadilhas Comuns

1. **Processo como substituto para conversa**: criar processos formais quando uma
   conversa de 10 minutos resolveria. Reserve formalização para interfaces recorrentes.

2. **DACI sem enforcement**: definir DACI e ignorá-lo quando inconveniente. O poder
   do DACI está na previsibilidade. Se o Approver muda toda hora, DACI é ficção.

3. **Overhead de coordenação**: tantas reuniões de sync que ninguém tem tempo de
   trabalhar. Regra: sync hours < 20% do tempo de qualquer pessoa.

4. **Culpar a outra equipe**: orquestração não elimina conflito — canaliza. Se o
   padrão é "eles não entregaram", investigue a interface, não as pessoas.

5. **Interfaces estáticas**: interfaces definidas uma vez e nunca revisadas. As
   necessidades mudam; revise contratos trimestralmente.

6. **Ignorar interfaces informais**: as dependências mais perigosas são as que ninguém
   mapeou. Faça auditorias semestrais de dependências.

7. **Excesso de stakeholders**: incluir todo mundo em tudo "para não excluir ninguém".
   Mais stakeholders = mais lentidão. Minimize Contributors e Informed no DACI.

## Integração com Outros Frameworks

- **Operating Rhythm** (`coo-operating-rhythm.md`): a cadência operacional inclui os
  pontos de sincronização cross-functional.
- **Execution Engine** (`coo-execution-engine.md`): a execução cross-functional precisa
  de accountability clara por interface.
- **Bottleneck Theory** (`coo-bottleneck-theory.md`): gargalos frequentemente estão
  nos handoffs entre equipes — a orquestração alivia.
- **Narrative Cascade** (`vision-chief-narrative-cascade.md`): comunicação cross-functional
  eficaz depende de narrativa compartilhada.
- **Integration Architecture** (`cio-integration-architecture.md`): integrações técnicas
  entre sistemas espelham integrações organizacionais entre equipes.
- **Developer Experience** (`cto-developer-experience.md`): interfaces de equipe afetam
  diretamente a experiência do desenvolvedor.

## Referências

- Jay Galbraith, *Designing Organizations* — organizational design e lateral processes
- Matthew Skelton & Manuel Pais, *Team Topologies* — team interaction modes
- Mik Kersten, *Project to Product* — flow entre equipes de produto
- Stanley McChrystal, *Team of Teams* — shared consciousness e empowered execution
- DACI Framework — adaptado de RACI pela Intuit e popularizado no Silicon Valley
- Spotify Model — squads, tribes, chapters, guilds
- Amazon, *Two-Pizza Teams* — autonomia com interfaces definidas
