# Automation-First — RPA, Workflow Automation e Self-Service

## Origem e Contexto

O mindset automation-first inverte a lógica tradicional de operações: em vez de perguntar
"como fazemos isso manualmente e depois automatizamos?", pergunta "como automatizamos isso
desde o início e mantemos humanos apenas onde agregam valor?". É a evolução natural de lean
manufacturing para o mundo digital — eliminar waste, reduzir variabilidade e liberar pessoas
para trabalho de maior valor.

O conceito ganhou tração com a convergência de três forças: RPA (Robotic Process Automation)
tornando acessível a automação de processos repetitivos, workflow automation (Zapier, n8n,
Make) democratizando integrações, e AI/LLMs adicionando capacidade de lidar com inputs não
estruturados. Juntos, esses enablers permitem automatizar processos que antes requeriam
julgamento humano.

O princípio fundamental: tempo humano em tarefas repetitivas é o desperdício mais caro de
uma organização. Cada minuto de um profissional qualificado gasto em copiar dados entre
sistemas, gerar relatórios manuais ou processar aprovações rotineiras é um minuto roubado
de trabalho estratégico. Automation-first não é eliminar empregos — é eliminar tarefas
que não deveriam ser feitas por humanos.

Referências: UiPath (RPA framework), Gartner (Hyperautomation), Zapier (workflow automation),
Toyota Production System (lean aplicado a operações digitais).

## Quando Usar

- Na avaliação de processos operacionais para otimização
- Ao escalar operações sem aumentar headcount proporcionalmente
- Quando erro humano em processos repetitivos causa problemas
- Na redução de tempo de onboarding e provisionamento
- Ao criar self-service para operações internas de TI
- Na integração de sistemas que não têm APIs nativas
- Quando a equipe reclama de "trabalho manual" que poderia ser automatizado

## Quando NÃO Usar

- Para automatizar processos quebrados (conserte o processo antes)
- Quando o processo muda frequentemente (automação frágil = mais trabalho)
- Para decisões que requerem julgamento humano genuíno (nuance, contexto)
- Se o volume é tão baixo que o custo de automação > custo manual
- Como substituto para redesenho de processo (às vezes o processo não deveria existir)

## Estrutura / Modelo

### Espectro de Automação

```
NÍVEL DE AUTOMAÇÃO
│
├── NÍVEL 0: MANUAL
│   Humano faz tudo, sem assistência
│   Exemplo: copiar dados de email para planilha
│
├── NÍVEL 1: ASSISTIDA
│   Ferramenta ajuda, humano decide e executa
│   Exemplo: template de email com campos pré-preenchidos
│
├── NÍVEL 2: PARCIAL
│   Automação faz parte, humano complementa
│   Exemplo: bot coleta dados, humano revisa e aprova
│
├── NÍVEL 3: CONDICIONAL
│   Automação faz tudo em cenários simples, humano nos complexos
│   Exemplo: aprovação automática se < R$5K, humana se > R$5K
│
├── NÍVEL 4: ALTA AUTOMAÇÃO
│   Automação faz quase tudo, humano supervisiona
│   Exemplo: processamento de invoices com human-in-the-loop para exceções
│
└── NÍVEL 5: AUTÔNOMA
    Automação end-to-end, humano monitora
    Exemplo: CI/CD pipeline que builda, testa e deploya sem intervenção
```

### Framework de Avaliação de Processos

```
CANDIDATO A AUTOMAÇÃO?
│
├── FREQUÊNCIA: Quantas vezes por dia/semana/mês?
│   > 10x/dia = alta prioridade
│   1-10x/dia = média prioridade
│   < 1x/dia = baixa prioridade (a menos que seja muito lento)
│
├── VOLUME: Quantas unidades (registros, documentos, transações)?
│   > 100/dia = alta prioridade
│
├── REGRAS: O processo segue regras claras e documentáveis?
│   Sim = automatizável
│   Parcialmente = automatizável com exceções
│   Não = requer AI ou redesign antes
│
├── VARIABILIDADE: O input é padronizado ou varia muito?
│   Padronizado = automação clássica (RPA, workflow)
│   Variável = necessita AI/ML para processar
│
├── CUSTO DO ERRO: O que acontece se a automação errar?
│   Baixo impacto = automatizar agressivamente
│   Alto impacto = automatizar com human-in-the-loop
│
└── SISTEMAS: Os sistemas envolvidos têm APIs ou interfaces acessíveis?
    APIs = workflow automation
    Sem API = RPA (simula interface humana)
    Nenhum = pode necessitar redesign
```

### Stack de Automação

```
CAMADAS DE AUTOMAÇÃO
│
├── CAMADA 1: WORKFLOW AUTOMATION
│   Ferramentas: n8n, Zapier, Make (Integromat), Power Automate
│   Use cases: integrações entre SaaS, triggers e actions
│   Exemplo: novo lead no CRM → criar canal no Slack → agendar follow-up
│
├── CAMADA 2: RPA (Robotic Process Automation)
│   Ferramentas: UiPath, Automation Anywhere, Power Automate Desktop
│   Use cases: sistemas sem API, interfaces legadas, processos cross-system
│   Exemplo: extrair dados do ERP legado → preencher formulário web
│
├── CAMADA 3: INTELLIGENT AUTOMATION (AI + Automação)
│   Ferramentas: Document AI, LLMs, Computer Vision + RPA
│   Use cases: inputs não estruturados, decisões com julgamento
│   Exemplo: extrair dados de invoices em PDF → categorizar → inserir no ERP
│
├── CAMADA 4: SELF-SERVICE PLATFORMS
│   Ferramentas: Service Catalog (ServiceNow), Internal Developer Platform
│   Use cases: provisionamento, acesso, configuração
│   Exemplo: novo funcionário → self-service para setup de acessos
│
└── CAMADA 5: AUTONOMOUS OPERATIONS (AIOps)
    Ferramentas: PagerDuty + AI, Datadog AI, auto-remediation
    Use cases: operações de TI self-healing
    Exemplo: detectar anomalia → diagnosticar → remediar → notificar
```

## Processo de Aplicação (step-by-step)

### Passo 1: Mapear Processos Candidatos (2-3 semanas)

- Entrevistar cada área: "quais tarefas repetitivas consomem mais tempo?"
- Listar processos com frequência, volume, tempo gasto e custo
- Classificar cada processo no framework de avaliação
- Priorizar por: (tempo economizado × frequência) / complexidade de automação

### Passo 2: Quick Wins (4-6 semanas)

- Selecionar 3-5 processos simples e de alto impacto
- Implementar com workflow automation (Zapier/n8n) — sem over-engineering
- Medir antes/depois: tempo gasto, erros, satisfação
- Documentar e comunicar resultados (advocacy)

### Passo 3: Construir Capabilities (3-6 meses)

- Definir stack de automação (ferramentas por camada)
- Treinar team de automação (ou community of practice)
- Criar standards: como documentar, como testar, como monitorar automações
- Implementar automações de média complexidade

### Passo 4: Self-Service Catalog (3-6 meses)

- Identificar operações mais requisitadas por tickets/requests
- Construir self-service para as top 10 operações (ex: acesso a sistemas, provisionamento)
- Automatizar aprovações quando possível (approval policy engine)
- Medir: redução de tickets, tempo de atendimento

### Passo 5: Intelligent Automation (6-12 meses)

- Adicionar AI para processos com inputs não estruturados
- Exemplo: document processing (invoices, contratos) com Document AI
- Human-in-the-loop para revisão de exceções
- Treinar modelos com feedback do loop humano

### Passo 6: Medir e Escalar (ongoing)

- Dashboard de automação: processos automatizados, horas economizadas, ROI
- Revisão trimestral: novos candidatos, evolução de existentes
- Target: automatizar 50%+ de tarefas repetitivas em 2 anos
- Cultura: todo novo processo começa com "como automatizamos?"

## Exemplos Práticos

### Exemplo 1: Automation Portfolio (12 meses)

| Processo | Camada | Antes | Depois | Saving/mês |
|----------|--------|-------|--------|------------|
| Onboarding de funcionário | Self-Service | 4h/caso, 20 casos/mês | 15min/caso | 75h |
| Processamento de invoices | AI + RPA | 10min/invoice, 500/mês | 1min/invoice | 75h |
| Report mensal consolidado | Workflow | 8h/mês, 1 analista | Automático | 8h |
| Provisionamento de infra | Self-Service | 3 dias (ticket) | 30min (self-service) | 40h |
| Reconciliação financeira | RPA | 2 dias/mês, 2 analistas | 4h/mês supervisão | 28h |
| **Total** | | | | **226h/mês = ~1.4 FTEs** |

### Exemplo 2: Self-Service IT Catalog

| Request | Volume/mês | Antes (SLA) | Depois (SLA) | Satisfação |
|---------|-----------|-------------|-------------|-----------|
| Acesso a sistema | 80 | 2 dias | 15 min | 4.8/5 |
| Reset de senha | 120 | 4 horas | Imediato | 5.0/5 |
| Novo ambiente dev | 30 | 5 dias | 1 hora | 4.7/5 |
| VPN setup | 25 | 1 dia | 30 min | 4.5/5 |
| Software install | 50 | 3 dias | Self-service | 4.6/5 |

## Armadilhas Comuns

1. **Automatizar processo ruim**: Automatizar waste é waste mais rápido. Simplifique antes.
2. **RPA como band-aid permanente**: RPA em sistema legado deveria ser temporário, não permanente.
3. **Automação frágil**: Bot que quebra toda vez que a UI muda = mais trabalho que manual.
4. **Ignorar exceções**: Automatizar o happy path e ignorar os 20% de exceções que consomem 80% do tempo.
5. **Sem monitoramento**: Automação que falha silenciosamente é pior que processo manual.
6. **Over-automation**: Automatizar decisões que requerem julgamento humano genuíno.
7. **Shadow automation**: Cada departamento cria suas automações sem standards ou segurança.
8. **ROI inflado**: "Economizamos 100 horas/mês" sem subtrair custo de manter a automação.
9. **Não treinar pessoas**: Automação funciona, mas ninguém entende quando dá problema.
10. **Medo de automação**: Equipe resiste porque acha que vai ser substituída.

## Integração com Outros Frameworks

- **`frameworks/cio-engineer/it-service-management.md`**: Self-service como evolução de ITSM
- **`frameworks/cio-engineer/cio-systems-rationalization.md`**: Automação como parte de racionalização
- **`frameworks/cio-engineer/cio-integration-architecture.md`**: APIs e integrações como enabler
- **`frameworks/cto-architect/cto-developer-experience.md`**: Self-service para engenharia
- **`frameworks/cto-architect/platform-strategy.md`**: Platform como enabler de self-service
- **`frameworks/ai/adoption-playbook.md`**: AI + automação como capability combinada
- **`frameworks/cfo-strategist/cost-optimization.md`**: Automação como alavanca de custo

## Referências

- Gartner — "Hyperautomation" (Top Strategic Technology Trend)
- UiPath — "Automation First Era" (whitepaper)
- Zapier — "The State of Business Automation"
- Toyota Production System — Taiichi Ohno (princípios de lean aplicados)
- Camunda — "Business Process Automation" (framework)
- McKinsey — "Intelligent Process Automation" (IPA)
- Thoughtworks — "Automation" (Technology Radar insights)
