# Workflow: Architecture Council

## Objetivo

Manter governança técnica de alto nível através de um conselho de arquitetura que avalia decisões cross-funcionais, define padrões tecnológicos e garante coerência arquitetural em toda a organização, equilibrando autonomia dos times com consistência sistêmica.

## Trigger

- RFC classificada como Large submetida para aprovação
- Proposta de adoção de nova tecnologia core
- Conflito arquitetural entre times que não foi resolvido localmente
- Revisão periódica de tech radar e padrões (trimestral)
- Solicitação do VP de Engenharia ou CTO

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| CTO ou VP de Engenharia | **Accountable** — Preside o council e arbitra impasses |
| Tech Leads seniores (3-5) | **Responsible** — Membros votantes do council |
| Staff Engineers | **Consulted** — Especialistas convocados por domínio |
| Autor da proposta | **Consulted** — Apresenta e defende a proposta |
| Engineering Managers | **Informed** — Visibilidade sobre decisões técnicas |

## Composição do Council

- **Presidente**: CTO ou VP de Engenharia (mandato contínuo)
- **Membros permanentes**: 3-5 Tech Leads/Staff Engineers seniores (mandato de 1 ano, rotativo)
- **Membros ad hoc**: Especialistas convocados conforme o tema da pauta
- **Secretário**: Engenheiro designado para documentar decisões

### Critérios para Membros Permanentes
- Experiência mínima de 5 anos em arquitetura de software
- Visão cross-funcional (não apenas expertise em um domínio)
- Capacidade de tomar decisões orientadas ao negócio
- Respeito e influência entre pares de engenharia

## Etapas do Workflow

### Etapa 1: Submissão de Pauta
- Propostas submetidas via formulário com 2 semanas de antecedência
- Cada proposta deve conter: problema, solução proposta, impacto, alternativas
- Secretário prioriza pauta conforme urgência e impacto
- Agenda publicada para toda a engenharia com 1 semana de antecedência
- **SLA: Proposta submetida 2 semanas antes da sessão**

### Etapa 2: Preparação
- Membros do council revisam materiais previamente
- Autor disponível para esclarecer dúvidas assíncronas
- Especialistas ad hoc confirmados e briefados
- Secretário prepara template de decisão
- **SLA: Materiais distribuídos 1 semana antes**

### Etapa 3: Sessão do Council (90 min, quinzenal ou mensal)
- Revisão de ações e decisões da sessão anterior (15 min)
- Apresentação de cada item de pauta pelo autor (15 min cada)
- Discussão e Q&A com membros do council (15 min cada)
- Deliberação e votação (decisão por consenso ou maioria)
- **Formato: Reunião presencial preferencial, virtual se necessário**

### Etapa 4: Deliberação
- Decisões possíveis: Aprovado / Rejeitado / Necessita revisão / Deferido
- Documentar justificativa para cada decisão
- Para decisões sem consenso: CTO tem voto de desempate
- Condições de aprovação claras e mensuráveis
- **SLA: Decisão na sessão ou em até 3 dias úteis se necessitar análise adicional**

### Etapa 5: Comunicação e Enforcement
- Decisões publicadas no canal #architecture-decisions
- ADR (Architecture Decision Record) atualizado
- Times impactados notificados diretamente
- Padrões e guidelines atualizados conforme decisões
- **SLA: 2 dias úteis após sessão**

### Etapa 6: Acompanhamento
- Decisões aprovadas rastreadas até implementação
- Review semestral de decisões passadas e seus outcomes
- Atualização do tech radar com novas tecnologias aprovadas/deprecadas
- **Cadência: contínua**

## Escopo de Decisões do Council

### Dentro do Escopo
- Adoção ou deprecação de tecnologias core
- Padrões de comunicação entre serviços
- Estratégia de dados e armazenamento
- Padrões de segurança e compliance técnico
- Decisões de build vs buy para componentes críticos
- Estratégia de cloud e infraestrutura

### Fora do Escopo
- Decisões internas de um único time (coberto pelo Tech Lead)
- Priorização de backlog de produto (coberto pelo PM)
- Escolha de bibliotecas menores sem impacto cross-funcional

## Outputs / Entregáveis

- Ata de cada sessão com decisões documentadas
- ADRs atualizados para cada decisão arquitetural
- Tech radar atualizado trimestralmente
- Guidelines e padrões técnicos publicados
- Comunicação de decisões para engenharia

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Sessões realizadas conforme cadência | 100% | Mensal |
| Itens de pauta resolvidos por sessão | ≥ 80% | Por sessão |
| Decisões implementadas conforme aprovado | ≥ 90% | Trimestral |
| Tempo médio de resolução (submissão à decisão) | ≤ 4 semanas | Mensal |
| Satisfação dos times com o council | ≥ 3.5/5.0 | Semestral |

## Integração com Outros Workflows

- **01-rfc-submission.md**: RFCs Large são escaladas para o council
- **02-design-review.md**: Designs cross-funcionais revisados pelo council
- **04-implementation-gates.md**: Council define gates técnicos obrigatórios
- **05-production-readiness.md**: Council define padrões de production readiness
