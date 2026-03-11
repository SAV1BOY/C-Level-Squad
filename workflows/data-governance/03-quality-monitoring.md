# Workflow: Monitoramento de Qualidade de Dados

## Objetivo

Implementar monitoramento contínuo da qualidade dos dados da organização, detectando problemas de integridade, completude e consistência de forma proativa, garantindo que decisões de negócio sejam baseadas em dados confiáveis.

## Trigger

- Novo pipeline de dados em produção
- Incidente causado por dados incorretos ou incompletos
- Cadência periódica de quality checks (diária/semanal)
- Integração com novo sistema ou fonte de dados
- Reclamação de usuário sobre qualidade de dados

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Data Engineer | **Responsible** — Implementa e mantém quality checks |
| Data Steward | **Accountable** — Define regras de qualidade e investiga issues |
| Data Analyst | **Consulted** — Reporta problemas encontrados no uso |
| Data Owner (VP) | **Informed** — Recebe relatórios de qualidade |
| Analytics Lead | **Informed** — Visibilidade sobre impacto em reports |

## Dimensões de Qualidade de Dados

| Dimensão | Definição | Exemplo de Regra |
|----------|-----------|-----------------|
| **Completude** | Dados presentes sem campos vazios | Campo email preenchido em ≥ 99% dos registros |
| **Unicidade** | Sem duplicatas indevidas | IDs únicos sem repetição |
| **Validade** | Formato e valores dentro do esperado | CPF com 11 dígitos, email com @ |
| **Consistência** | Dados coerentes entre sistemas | Receita no CRM = receita no ERP |
| **Acurácia** | Dados refletem a realidade | Endereço válido e atualizado |
| **Tempestividade** | Dados atualizados no prazo | Pipeline executado até 6h da manhã |

## Etapas do Workflow

### Etapa 1: Definição de Regras de Qualidade
- Data Steward define regras por dataset crítico
- Regras documentadas: dimensão, campo, condição, threshold, severidade
- Priorizar datasets que alimentam decisões de negócio
- Regras codificadas em ferramenta de data quality (Great Expectations, dbt tests, Monte Carlo)
- **SLA: 5 regras por dataset crítico; contínuo para novos datasets**

### Etapa 2: Implementação de Quality Checks
- Data Engineer implementa checks no pipeline de dados
- Checks executam automaticamente em cada run do pipeline
- Configurar alertas para violações por severidade:
  - Crítico: bloqueia pipeline, notifica imediatamente
  - Alto: notifica time, não bloqueia
  - Médio: registra para revisão periódica
- **SLA: 1 semana por dataset**

### Etapa 3: Monitoramento Contínuo
- Dashboard de qualidade atualizado em tempo real
- Alertas enviados para canal específico (#data-quality)
- Tendências monitoradas: quality score ao longo do tempo
- Anomalias detectadas automaticamente (schema changes, volume drops)
- **Cadência: Contínua com review semanal**

### Etapa 4: Investigação e Resolução de Issues
- Alerta disparado: Data Steward investiga causa raiz
- Categorizar issue: erro de fonte, bug de pipeline, mudança de schema, erro humano
- Documentar impacto: quais reports/decisões foram afetados
- Corrigir dados (backfill se necessário) e pipeline
- Implementar check adicional para prevenir recorrência
- **SLA: Crítico ≤ 4h; Alto ≤ 24h; Médio ≤ 1 semana**

### Etapa 5: Relatório Periódico de Qualidade
- Report semanal para Data Stewards: issues abertos, tendências, scores
- Report mensal para Data Owners: quality score por dataset, incidentes, ações
- Report trimestral para liderança: health geral do ecossistema de dados
- Benchmarking interno: comparar quality score entre áreas
- **Cadência: Semanal/Mensal/Trimestral**

### Etapa 6: Melhoria Contínua
- Revisão trimestral de regras de qualidade (adicionar, ajustar, remover)
- Feedback de Data Analysts sobre problemas encontrados no uso
- Priorizar investimentos em qualidade de dados por impacto de negócio
- Treinamento de times de entrada de dados quando erro é humano
- **Cadência: Trimestral**

## Outputs / Entregáveis

- Dashboard de data quality por dataset e dimensão
- Regras de qualidade codificadas e documentadas
- Alertas configurados por severidade
- Relatórios periódicos de qualidade (semanal/mensal/trimestral)
- Registro de issues e resoluções

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Quality score geral | ≥ 95% | Semanal |
| Datasets críticos com monitoring | 100% | Trimestral |
| Issues críticos resolvidos no SLA | ≥ 95% | Mensal |
| Incidentes causados por dados ruins | Tendência decrescente | Mensal |
| Cobertura de quality checks | ≥ 80% dos datasets | Trimestral |

## Integração com Outros Workflows

- **01-data-classification.md**: Datasets classificados priorizam quality checks
- **04-compliance-audit.md**: Quality reports são evidência de auditoria
- **Incident Response / 01-detection-triage.md**: Issues de dados podem ser incidentes
- **OKR Cycle / 03-weekly-check-in.md**: Quality score como métrica operacional
