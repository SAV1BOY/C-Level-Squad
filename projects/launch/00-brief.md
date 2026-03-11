# Lançamento de Produto — Fase 00: Brief de Lançamento

## Objetivo desta Fase

Definir o escopo, objetivos e contexto do lançamento de um novo produto, feature ou
serviço. O brief de lançamento serve como o documento fundacional que alinha todas as
equipas sobre o que será lançado, para quem, quando e com que expectativas de resultado.
Um brief claro evita o caos que tipicamente caracteriza lançamentos mal planeados e
garante que marketing, tecnologia e operações trabalham a partir da mesma base.

## Agentes Envolvidos

- **CEO Agent**: Define a importância estratégica do lançamento e o nível de investimento
- **CMO Agent**: Lidera a definição do posicionamento e audiência alvo
- **CTO Agent**: Confirma o estado de desenvolvimento e readiness técnica
- **COO Agent**: Avalia capacidade operacional para suportar o lançamento
- **CFO Agent**: Define o orçamento disponível e métricas financeiras esperadas
- **Chief of Staff Agent**: Coordena o processo de briefing e documenta decisões

## Inputs Necessários

1. Product requirements document ou feature specification
2. Análise de mercado e competitive landscape
3. Dados de clientes e segmentação de audiência
4. Estado atual de desenvolvimento (% completo, features prontas)
5. Capacidade operacional disponível (suporte, infraestrutura, logística)
6. Orçamento de marketing e go-to-market aprovado
7. Calendário corporativo e de mercado (eventos, sazonalidade)

## Processo (step-by-step)

1. **Product readiness assessment**: CTO Agent apresenta o estado atual do produto,
   features disponíveis, bugs conhecidos e timeline para completion
2. **Market opportunity sizing**: CMO Agent apresenta a análise de mercado, TAM/SAM/SOM,
   audiência alvo e posicionamento competitivo proposto
3. **Strategic framing**: CEO Agent enquadra o lançamento na estratégia global da empresa,
   definindo o nível de prioridade e investimento justificado
4. **Financial framework**: CFO Agent define o envelope orçamental para o lançamento,
   incluindo marketing spend, infra costs e projeções de revenue
5. **Operational capacity check**: COO Agent avalia a capacidade de suportar o volume
   esperado (suporte ao cliente, infraestrutura, supply chain se aplicável)
6. **Launch brief drafting**: CMO Agent redige o brief de lançamento consolidando
   todas as perspetivas e definindo os elementos chave
7. **Date and scope commitment**: Todos os agentes validam a data de lançamento
   proposta e o escopo de features incluídas no MVP de lançamento
8. **Risk identification**: Chief of Staff facilita uma sessão rápida de identificação
   de riscos do lançamento com input de todos os agentes
9. **Brief approval**: Todos os agentes revisam e aprovam o brief final

## Outputs / Entregáveis

- **Launch Brief Document**: Documento principal com todos os elementos do lançamento
- **Market Analysis Summary**: Resumo da análise de mercado e oportunidade
- **Launch Budget**: Orçamento detalhado do lançamento por categoria
- **Feature Scope Agreement**: Lista de features incluídas no lançamento (in/out)
- **Launch Date Commitment**: Data comprometida com condições de go/no-go
- **Initial Risk Register**: Riscos identificados com classificação preliminar
- **Success Metrics Definition**: KPIs de sucesso do lançamento e targets

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-00.1 | Audiência alvo definida com precisão (personas documentadas) | CMO Agent |
| QG-00.2 | Data de lançamento viável confirmada pelo CTO Agent | CTO Agent |
| QG-00.3 | Orçamento aprovado e alocado por área | CFO Agent |
| QG-00.4 | Feature scope locked (sem mudanças após aprovação) | CTO Agent |
| QG-00.5 | Capacidade operacional confirmada para volume projetado | COO Agent |
| QG-00.6 | Brief claro e compreensível por qualquer stakeholder | Chief of Staff |

## Critérios para Avançar

Para progredir para a Fase 01 (GTM Plan), todos os critérios devem ser satisfeitos:

- [ ] Brief de lançamento aprovado por todos os agentes
- [ ] Data de lançamento comprometida (com critérios de no-go definidos)
- [ ] Orçamento alocado e disponível
- [ ] Feature scope finalizado e locked
- [ ] Métricas de sucesso definidas e aceites
- [ ] Riscos principais identificados e owners atribuídos

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Scope creep de features no brief | Alta | Alto | Feature freeze após aprovação do brief |
| Data de lançamento irrealista definida por pressão | Alta | Crítico | CTO Agent tem veto sobre data técnica |
| Mercado muda entre brief e lançamento | Média | Médio | Revisão rápida de mercado 2 semanas antes do launch |
| Orçamento insuficiente para impacto desejado | Média | Alto | CMO Agent propõe plano escalável com prioridades |
| Desalinhamento entre produto real e expectativa do brief | Média | Alto | Demo do produto durante a sessão de briefing |

## Templates a Usar

- `templates/launch-brief.md` — Template do brief de lançamento
- `templates/market-analysis.md` — Template de análise de mercado
- `templates/launch-budget.md` — Template de orçamento de lançamento
- `templates/feature-scope.md` — Template de escopo de features

## Duração Estimada

- **Mínimo**: 2 dias úteis (para lançamentos simples de features)
- **Típico**: 3-5 dias úteis
- **Máximo**: 10 dias úteis (para lançamentos de produtos completamente novos)

> **Nota**: O brief de lançamento deve ser um documento vivo até ser aprovado, e
> congelado após aprovação. Mudanças pós-aprovação requerem change request formal.
