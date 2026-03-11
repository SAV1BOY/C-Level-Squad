# Workflow: POC e Piloto

## Objetivo

Validar a solução do fornecedor selecionado em ambiente controlado antes do compromisso contratual completo, reduzindo riscos de implementação e garantindo que a solução atenda às necessidades reais do negócio.

## Trigger

- Fornecedor selecionado na fase de avaliação/RFP
- Aprovação para investir em POC (tempo e recursos)
- Acordo de POC assinado com fornecedor (termos, escopo, duração)

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Gestor Solicitante | **Accountable** — Define critérios de sucesso e avalia resultado |
| Time Técnico | **Responsible** — Executa POC e testa funcionalidades |
| Fornecedor | **Responsible** — Suporta implementação e tira dúvidas |
| Procurement | **Consulted** — Monitora termos do acordo de POC |
| TI / Security | **Consulted** — Valida requisitos técnicos e de segurança |
| VP da Área | **Informed** — Recebe relatório de resultado |

## Estrutura da POC

### Definição de Escopo
- Selecionar 2-3 use cases representativos (não todos os requisitos)
- Use cases devem cobrir cenários críticos e de maior risco
- Definir métricas de sucesso para cada use case
- Estabelecer ambiente de teste (sandbox, staging, produção limitada)

### Critérios de Go/No-Go
- Definir ANTES de iniciar a POC, não depois
- Cada critério: obrigatório (deal breaker) ou desejável
- Critérios típicos: performance, usabilidade, integração, suporte, custo
- Threshold de aprovação: 100% dos obrigatórios + ≥ 70% dos desejáveis

## Etapas do Workflow

### Etapa 1: Planejamento da POC
- Definir escopo, critérios de sucesso e timeline
- Acordar com fornecedor: recursos dedicados, suporte, custos
- Configurar ambiente de teste com dados representativos (anonimizados)
- Designar team lead interno para coordenar
- Kick-off meeting com todas as partes
- **SLA: 1 semana**

### Etapa 2: Execução da POC (2-4 semanas)
- Time técnico implementa e testa use cases definidos
- Fornecedor disponibiliza suporte dedicado
- Reuniões de sync: 2x por semana com fornecedor
- Documentar todos os issues encontrados e resoluções
- Coletar feedback de usuários que testam a solução
- **SLA: 2-4 semanas conforme complexidade**

### Etapa 3: Avaliação de Resultados
- Avaliar cada critério de sucesso contra resultados obtidos
- Documentar: funcionalidades testadas, performance medida, issues encontrados
- Coletar NPS ou feedback estruturado dos testadores internos
- Comparar resultado real vs expectativa do fornecedor
- **SLA: 3 dias úteis após fim da POC**

### Etapa 4: Decisão de Go/No-Go
- Gestor apresenta resultados para comitê decisor
- Recomendação: Go (avançar para contrato) / No-Go (buscar alternativa) / Extend (ampliar POC)
- Se Go: transição para negociação de contrato
- Se No-Go: documentar razões e avaliar segundo fornecedor do ranking
- **SLA: 1 semana**

### Etapa 5: Piloto (se aplicável)
- Para soluções de maior impacto: piloto em produção limitada antes do rollout
- Escopo: 1 time ou 1 unidade de negócio
- Duração: 1-3 meses
- Monitorar adoção, satisfação e ROI incremental
- Decisão final de rollout completo baseada nos resultados do piloto

## Outputs / Entregáveis

- Relatório de POC com resultados vs critérios de sucesso
- Scorecard preenchido com evidências
- Lista de issues encontrados e status de resolução
- Recomendação de Go/No-Go documentada
- Plano de implementação (se Go)
- Relatório de piloto (se aplicável)

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| POCs concluídas no prazo | ≥ 85% | Por POC |
| Critérios obrigatórios atendidos | 100% para Go | Por POC |
| Satisfação dos testadores | ≥ 4.0/5.0 | Por POC |
| POCs que resultam em contrato | ≥ 60% | Trimestral |
| Fornecedores contratados pós-POC com satisfação 6m | ≥ 80% satisfeitos | Semestral |

## Integração com Outros Workflows

- **01-evaluation-rfp.md**: Recebe fornecedor selecionado
- **03-contract-negotiation.md**: POC aprovada inicia negociação
- **Tech Review / 02-design-review.md**: Integração com fornecedor pode requerer design review
- **Data Governance / 02-access-control.md**: Acesso do fornecedor ao ambiente controlado
