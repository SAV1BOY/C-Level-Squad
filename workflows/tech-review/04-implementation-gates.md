# Workflow: Gates de Implementação

## Objetivo

Definir checkpoints obrigatórios durante o ciclo de implementação que validem qualidade, segurança e prontidão antes de avançar para a próxima fase, prevenindo que problemas técnicos cheguem a produção e reduzindo o custo de correção.

## Trigger

- Início de implementação de feature aprovada no design review
- Sprint planning incluindo épicos com gates definidos
- Automação de CI/CD executando validações em cada commit/PR

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Engenheiro Desenvolvedor | **Responsible** — Garante que código atende gates |
| Tech Lead | **Accountable** — Valida passagem pelos gates |
| QA Engineer | **Consulted** — Executa validações de qualidade |
| SRE | **Consulted** — Valida gates de operabilidade |
| Security Engineer | **Consulted** — Valida gates de segurança |

## Gates Definidos

### Gate 1: Code Quality (Automatizado)
- **Quando**: Em cada Pull Request
- **Critérios**:
  - Testes unitários passando (100%)
  - Cobertura de testes ≥ 80% em código novo
  - Lint e formatação conforme padrão (sem warnings)
  - Análise estática sem issues críticos (SonarQube, CodeClimate)
  - Build compilando sem erros
- **Bloqueante**: Sim — PR não pode ser mergeada sem passar

### Gate 2: Code Review (Manual + Automatizado)
- **Quando**: Em cada Pull Request
- **Critérios**:
  - Mínimo 1 aprovação de reviewer (2 para código crítico)
  - Reviewer verificou: lógica, performance, segurança, testes
  - Comentários resolvidos ou reconhecidos
  - PR description clara com contexto e link para ticket
- **Bloqueante**: Sim — merge requer aprovação

### Gate 3: Integration Testing (Automatizado)
- **Quando**: Após merge na branch de desenvolvimento
- **Critérios**:
  - Testes de integração passando no CI
  - Testes de contrato entre serviços validados
  - Smoke tests em ambiente de staging
  - Sem regressões em funcionalidades existentes
- **Bloqueante**: Sim — deploy para staging bloqueado se falhar

### Gate 4: Security Review (Manual para features sensíveis)
- **Quando**: Antes do deploy para staging de features com impacto em segurança
- **Critérios**:
  - SAST (Static Application Security Testing) sem vulnerabilidades críticas
  - DAST (Dynamic Application Security Testing) executado
  - Dependências verificadas contra CVEs conhecidos
  - Revisão manual para features que lidam com dados sensíveis ou autenticação
- **Bloqueante**: Sim para features sensíveis, warning para demais

### Gate 5: Performance Validation (Automatizado + Manual)
- **Quando**: Antes do deploy para produção
- **Critérios**:
  - Testes de carga executados (latência p95 ≤ baseline + 10%)
  - Sem memory leaks detectados em testes de stress
  - Queries de banco otimizadas (sem full table scans)
  - Cache configurado conforme padrão
- **Bloqueante**: Sim para serviços de alta carga

### Gate 6: Production Readiness (Manual)
- **Quando**: Antes do primeiro deploy de novo serviço ou mudança major
- **Critérios**:
  - Checklist de production readiness completo
  - Feature flags configuradas
  - Plano de rollback testado
  - Alertas e dashboards configurados
  - Runbook documentado
- **Bloqueante**: Sim — vinculado ao workflow 05-production-readiness

## Etapas do Workflow

### Etapa 1: Configuração dos Gates
- Tech Lead configura gates aplicáveis no CI/CD para o projeto
- QA define estratégia de testes para cada gate
- Security define critérios de escaneamento
- Documentar quais gates são bloqueantes vs informativos
- **SLA: Configuração antes do início do Sprint 1**

### Etapa 2: Execução Contínua
- Gates automatizados executam em cada commit/PR/merge
- Resultados visíveis no PR e no pipeline de CI/CD
- Engenheiros corrigem falhas antes de solicitar merge
- Tech Lead monitora taxa de passagem nos gates
- **Cadência: Contínua**

### Etapa 3: Exceções e Overrides
- Gates podem ser bypassados apenas com aprovação do Tech Lead + justificativa
- Override documentado com ticket de follow-up obrigatório
- Overrides frequentes sinalizam necessidade de ajustar o gate
- Relatório mensal de overrides revisado pelo VP de Engenharia
- **Regra: Zero overrides em gates de segurança sem aprovação do Security Lead**

### Etapa 4: Evolução dos Gates
- Revisão trimestral de eficácia dos gates
- Adicionar gates baseado em postmortems e incidentes
- Remover gates obsoletos ou de baixo valor
- Benchmark com práticas de mercado

## Outputs / Entregáveis

- Pipeline de CI/CD configurado com todos os gates
- Dashboard de taxa de passagem por gate
- Relatório mensal de overrides e exceções
- Documentação de critérios por gate atualizada

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Taxa de passagem no Gate 1 (primeira tentativa) | ≥ 85% | Semanal |
| Tempo médio de code review (Gate 2) | ≤ 24h | Semanal |
| Bugs em produção vs encontrados nos gates | ≥ 80% encontrados antes | Mensal |
| Overrides de gates | < 5% dos deploys | Mensal |
| Tempo do pipeline de CI (todos os gates) | ≤ 30 min | Semanal |

## Integração com Outros Workflows

- **02-design-review.md**: Design aprovado define quais gates são obrigatórios
- **05-production-readiness.md**: Gate 6 vinculado ao checklist de produção
- **Incident Response / 04-postmortem-process.md**: Postmortems geram novos gates
- **Product Launch / 02-build-phase.md**: Gates integrados ao processo de build
