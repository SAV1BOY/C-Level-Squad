# Workflow: Medição de Adoção

## Objetivo

Medir sistematicamente a adoção de mudanças implementadas, identificando gaps entre o estado desejado e o real, permitindo intervenções corretivas e garantindo que a mudança se sustente a longo prazo.

## Trigger

- Mudança implementada e treinamento concluído
- 30 dias após go-live de nova ferramenta ou processo
- Cadência periódica de medição (mensal durante estabilização)
- Sinal de baixa adoção via métricas automáticas ou feedback

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Change Manager | **Responsible** — Define métricas, coleta dados, analisa |
| Sponsor Executivo | **Accountable** — Recebe reports e decide intervenções |
| Data Analyst | **Consulted** — Extrai métricas quantitativas de sistemas |
| Gestores de Área | **Responsible** — Reforçam adoção em seus times |
| L&D | **Consulted** — Suporte adicional de treinamento se necessário |

## Framework de Medição (ADKAR)

| Estágio | O que mede | Como mede | Quando |
|---------|-----------|-----------|--------|
| Awareness | Sabem da mudança | Pesquisa pulse | Pré e pós comunicação |
| Desire | Querem mudar | Pesquisa pulse + entrevistas | Pós comunicação |
| Knowledge | Sabem como fazer | Avaliação pós-treinamento | Pós treinamento |
| Ability | Conseguem fazer | Métricas de uso, observação | 30-60 dias |
| Reinforcement | Mantêm a mudança | Métricas de uso contínuo | 90+ dias |

## Etapas do Workflow

### Etapa 1: Definição de Métricas de Adoção
- Definir métricas leading (preditivas) e lagging (resultado)
- Exemplos de métricas por tipo de mudança:
  - **Nova ferramenta**: % logins, % features usadas, frequência de uso
  - **Novo processo**: % aderência ao processo, tempo de execução, erros
  - **Reorganização**: engajamento, produtividade, turnover voluntário
- Definir baseline (estado atual) e target (estado desejado)
- Configurar dashboards de monitoramento
- **SLA: 1 semana antes do go-live**

### Etapa 2: Medição Pré-Mudança (Baseline)
- Capturar métricas antes da implementação
- Pesquisa de awareness e desire (ADKAR nível 1 e 2)
- Registrar métricas operacionais de baseline
- Documentar para comparação futura
- **SLA: 1 semana antes da mudança**

### Etapa 3: Medição de Curto Prazo (Semana 1-4)
- Monitorar métricas de uso diariamente na primeira semana
- Pesquisa pulse semanal: satisfação, dificuldades, sugestões
- Identificar early adopters e resistentes
- Intervenções rápidas: suporte extra, treinamento adicional, ajustes
- Report semanal para sponsor e gestores
- **Cadência: Semanal**

### Etapa 4: Medição de Médio Prazo (Mês 2-3)
- Métricas de uso e aderência estabilizando
- Avaliação de ability (ADKAR nível 4): conseguem executar sem ajuda?
- Comparar performance pré vs pós mudança
- Identificar gaps persistentes por área ou grupo
- Plano de reforço para áreas com baixa adoção
- **Cadência: Quinzenal**

### Etapa 5: Medição de Longo Prazo (Mês 3-6)
- Verificar sustentabilidade da mudança (reinforcement)
- Métricas de negócio impactadas pela mudança
- ROI da mudança: benefícios realizados vs custo do programa
- Pesquisa final de satisfação e feedback
- Documentar caso de sucesso ou lições de insucesso
- **Cadência: Mensal**

### Etapa 6: Relatório Final e Handoff
- Consolidar resultados em relatório de adoção final
- Comparar com targets definidos na avaliação de impacto
- Recomendar: encerrar programa (adoção sustentada) ou estender
- Handoff de monitoramento para operação regular
- Lições aprendidas compartilhadas com toda a empresa
- **SLA: 6 meses após go-live**

## Dashboard de Adoção

| Métrica | Baseline | Target | Atual | Status |
|---------|----------|--------|-------|--------|
| Awareness | 0% | ≥ 90% | - | - |
| Desejo de mudança | - | ≥ 70% | - | - |
| Score de conhecimento | - | ≥ 80% | - | - |
| Taxa de uso da ferramenta | 0% | ≥ 85% | - | - |
| Aderência ao processo | - | ≥ 80% | - | - |
| Satisfação com a mudança | - | ≥ 3.5/5 | - | - |

## Outputs / Entregáveis

- Dashboard de adoção atualizado continuamente
- Reports periódicos para sponsor (semanal → quinzenal → mensal)
- Planos de intervenção para gaps identificados
- Relatório final de adoção com ROI
- Lições aprendidas documentadas
- Caso de sucesso para compartilhar internamente

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Taxa de adoção geral | ≥ 80% em 90 dias | Mensal |
| Sustentação da adoção | Estável ou crescente em 6 meses | Mensal |
| ROI da mudança | Positivo em 12 meses | Anual |
| NPS da mudança | ≥ 20 | Trimestral |
| Mudanças que atingem target de adoção | ≥ 75% | Anual |

## Integração com Outros Workflows

- **04-training-enablement.md**: Gaps de ability acionam treinamento adicional
- **03-communication-plan.md**: Baixa awareness aciona mais comunicação
- **01-impact-assessment.md**: Resultados informam futuros assessments
- **OKR Cycle / 05-quarterly-retrospective.md**: Adoção avaliada nos OKRs
