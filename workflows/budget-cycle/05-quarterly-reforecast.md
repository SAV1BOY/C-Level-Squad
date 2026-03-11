# Workflow: Reforecast Trimestral

## Objetivo

Atualizar trimestralmente as projeções financeiras com base nos resultados reais acumulados e nas mudanças de cenário, permitindo ajustes de alocação de recursos, identificação de riscos e oportunidades, e comunicação transparente ao board sobre a trajetória financeira.

## Trigger

- Fechamento contábil do trimestre concluído
- Dados reais de receita, custo e investimento disponíveis
- Calendário de reforecast definido na aprovação do budget anual

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| FP&A | **Responsible** — Conduz análise, consolida reforecast |
| CFO | **Accountable** — Aprova reforecast e comunica ao board |
| VPs / Heads | **Consulted** — Fornecem input sobre perspectivas da área |
| Controller | **Consulted** — Dados contábeis reais e ajustes |
| CEO | **Informed** — Alinhamento sobre ajustes estratégicos |
| Board | **Informed** — Recebe atualização trimestral |

## Etapas do Workflow

### Etapa 1: Fechamento e Baseline
- Controller fecha contabilidade do trimestre (real vs budget)
- FP&A extrai dados reais e calcula variações (por departamento e linha)
- Preparar análise de variância: volume, preço, timing, scope
- Identificar top 10 variações (positivas e negativas) para investigação
- **SLA: 5 dias úteis após fechamento contábil**

### Etapa 2: Coleta de Input dos Departamentos
- FP&A solicita perspectivas atualizadas de cada VP/Head
- Template simplificado (vs budget anual): foco nas mudanças
- Perguntas-chave: novos projetos, atrasos, cortes, headcount atualizado
- Revisar pipeline de vendas para atualizar projeção de receita
- **SLA: 5 dias úteis**

### Etapa 3: Modelagem do Reforecast
- FP&A atualiza modelo financeiro com dados reais + novas projeções
- Reforecast dos trimestres restantes do ano
- Simular cenários: bear case, base case, bull case
- Calcular impacto em EBITDA, cash flow e métricas-chave
- Identificar necessidade de realocações entre departamentos
- **SLA: 5 dias úteis**

### Etapa 4: Review com CFO
- FP&A apresenta reforecast consolidado ao CFO
- Discussão sobre pontos de atenção e decisões necessárias
- CFO define se há necessidade de ajustes de alocação
- Aprovar mensagem para comunicação ao board e VPs
- **SLA: 2 dias úteis**

### Etapa 5: Comunicação e Alinhamento
- CFO comunica resultados para C-Level em reunião executiva
- FP&A compartilha análise detalhada com cada VP
- Ajustes de alocação formalizados (se aplicável)
- Atualizar projeções no sistema financeiro
- Preparar slide de atualização para o board
- **SLA: 3 dias úteis**

### Etapa 6: Ações Corretivas (se necessário)
- Para variações negativas significativas (>10% do budget):
  - Plano de contenção de custos com timeline
  - Revisão de headcount (freeze, postpone, redução)
  - Renegociação de contratos com fornecedores
- Para variações positivas:
  - Avaliar oportunidades de investimento acelerado
  - Atualizar targets de vendas e marketing
- **SLA: Plano de ação em 1 semana**

## Outputs / Entregáveis

- Reforecast financeiro atualizado (P&L, Cash Flow, Balance Sheet)
- Análise de variância real vs budget com explicações
- Cenários atualizados (bear/base/bull)
- Ações corretivas documentadas com donos e prazos
- Comunicação para board e liderança
- Sistema financeiro atualizado

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Reforecast concluído no prazo | 100% | Trimestral |
| Acurácia do reforecast vs real | ≤ 5% de variação | Trimestral |
| Input departamental recebido no prazo | ≥ 90% | Trimestral |
| Ações corretivas executadas | ≥ 80% | Trimestral |
| Tempo total do ciclo de reforecast | ≤ 20 dias úteis | Trimestral |

## Integração com Outros Workflows

- **04-board-approval.md**: Reforecast atualiza projeções do orçamento aprovado
- **01-planning-kickoff.md**: Q3 reforecast informa premissas do próximo ciclo
- **OKR Cycle / 04-mid-quarter-review.md**: Dados financeiros informam review de OKRs
- **Hiring / 01-requisition-approval.md**: Reforecast pode resultar em hiring freeze
- **Vendor Management / 05-renewal-exit.md**: Cortes podem impactar renovações
