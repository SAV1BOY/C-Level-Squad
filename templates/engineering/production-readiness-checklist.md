# Template: Production Readiness Checklist

## Propósito
Este checklist garante que novos serviços ou features atendem aos padrões mínimos de qualidade, observabilidade, segurança e operabilidade antes de ir para produção. Nenhum serviço deve ir a produção sem passar por esta revisão.

## Instruções de Uso
1. O time de desenvolvimento preenche o checklist durante desenvolvimento
2. Tech Lead revisa e valida cada item
3. SRE/Platform valida itens de infra e observabilidade
4. Todos os itens P0 devem estar completos para deploy em produção
5. Itens P1 devem ter plano com data para conclusão pós-launch

---

## Informações do Serviço

| Campo | Valor |
|-------|-------|
| **Nome do Serviço** | [Nome] |
| **Time Responsável** | [Nome do time] |
| **Tech Lead** | [Nome] |
| **Data Prevista de Launch** | [DD/MM/AAAA] |
| **Revisor SRE** | [Nome] |
| **Criticidade** | [P0 / P1 / P2 / P3] |

---

## 1. Arquitetura e Design

| # | Item | Prioridade | Status | Notas |
|---|------|-----------|--------|-------|
| 1.1 | ADR documentado para decisões arquiteturais significativas | P0 | [ ] | |
| 1.2 | Diagrama de arquitetura atualizado | P0 | [ ] | |
| 1.3 | Dependências mapeadas com SLAs definidos | P0 | [ ] | |
| 1.4 | Comportamento em caso de falha de cada dependência documentado | P0 | [ ] | |
| 1.5 | Limites de escala definidos e testados | P1 | [ ] | |
| 1.6 | Plano de capacidade para 6 meses documentado | P1 | [ ] | |

---

## 2. Código e Build

| # | Item | Prioridade | Status | Notas |
|---|------|-----------|--------|-------|
| 2.1 | Code review aprovado por pelo menos 2 engenheiros | P0 | [ ] | |
| 2.2 | Cobertura de testes unitários > [X%] | P0 | [ ] | |
| 2.3 | Testes de integração cobrindo fluxos críticos | P0 | [ ] | |
| 2.4 | Testes end-to-end para happy path | P0 | [ ] | |
| 2.5 | Pipeline de CI/CD configurado e funcional | P0 | [ ] | |
| 2.6 | Build reproduzível e determinístico | P1 | [ ] | |
| 2.7 | Sem secrets hardcoded no código | P0 | [ ] | |
| 2.8 | Dependências de terceiros auditadas (licenças e vulnerabilidades) | P1 | [ ] | |

---

## 3. Observabilidade

| # | Item | Prioridade | Status | Notas |
|---|------|-----------|--------|-------|
| 3.1 | Health check endpoint implementado (/health) | P0 | [ ] | |
| 3.2 | Métricas RED (Rate, Errors, Duration) expostas | P0 | [ ] | |
| 3.3 | Logs estruturados (JSON) com correlation ID | P0 | [ ] | |
| 3.4 | Distributed tracing implementado | P1 | [ ] | |
| 3.5 | Dashboard de monitoramento criado | P0 | [ ] | |
| 3.6 | Alertas configurados para SLOs | P0 | [ ] | |
| 3.7 | SLIs e SLOs definidos e documentados | P0 | [ ] | |
| 3.8 | Error budget tracking configurado | P1 | [ ] | |

---

## 4. Resiliência e Performance

| # | Item | Prioridade | Status | Notas |
|---|------|-----------|--------|-------|
| 4.1 | Timeouts configurados para todas as chamadas externas | P0 | [ ] | |
| 4.2 | Circuit breaker implementado para dependências críticas | P0 | [ ] | |
| 4.3 | Retry com backoff exponencial e jitter | P0 | [ ] | |
| 4.4 | Rate limiting configurado | P1 | [ ] | |
| 4.5 | Graceful shutdown implementado | P0 | [ ] | |
| 4.6 | Teste de carga executado (resultados documentados) | P0 | [ ] | |
| 4.7 | Teste de estresse para identificar ponto de quebra | P1 | [ ] | |
| 4.8 | Fallback definido para degradação graciosa | P1 | [ ] | |

---

## 5. Segurança

| # | Item | Prioridade | Status | Notas |
|---|------|-----------|--------|-------|
| 5.1 | Autenticação e autorização implementadas | P0 | [ ] | |
| 5.2 | Input validation em todos os endpoints | P0 | [ ] | |
| 5.3 | Dados sensíveis criptografados em trânsito (TLS) | P0 | [ ] | |
| 5.4 | Dados sensíveis criptografados em repouso | P0 | [ ] | |
| 5.5 | OWASP Top 10 verificado | P0 | [ ] | |
| 5.6 | Scan de vulnerabilidades executado (SAST/DAST) | P1 | [ ] | |
| 5.7 | Secrets gerenciados via vault/secrets manager | P0 | [ ] | |
| 5.8 | Audit log implementado para ações sensíveis | P1 | [ ] | |
| 5.9 | LGPD/GDPR compliance verificado | P0 | [ ] | |

---

## 6. Deploy e Operação

| # | Item | Prioridade | Status | Notas |
|---|------|-----------|--------|-------|
| 6.1 | Deploy automatizado via pipeline | P0 | [ ] | |
| 6.2 | Rollback testado e documentado | P0 | [ ] | |
| 6.3 | Feature flags para controle de rollout | P1 | [ ] | |
| 6.4 | Canary/blue-green deployment configurado | P1 | [ ] | |
| 6.5 | Runbook operacional criado | P0 | [ ] | |
| 6.6 | On-call configurado com escalonamento | P0 | [ ] | |
| 6.7 | Procedimento de DR (Disaster Recovery) testado | P1 | [ ] | |
| 6.8 | Backup configurado e restore testado | P0 | [ ] | |

---

## 7. Documentação

| # | Item | Prioridade | Status | Notas |
|---|------|-----------|--------|-------|
| 7.1 | README atualizado com setup local | P0 | [ ] | |
| 7.2 | API documentation (OpenAPI/Swagger) publicada | P0 | [ ] | |
| 7.3 | Runbook operacional completo | P0 | [ ] | |
| 7.4 | Diagrama de arquitetura em repositório central | P1 | [ ] | |
| 7.5 | Guia de troubleshooting | P1 | [ ] | |

---

## Resultado da Revisão

### Sumário

| Categoria | Total Itens | P0 Completos | P1 Completos | Status |
|-----------|-----------|-------------|-------------|--------|
| Arquitetura | [N] | [N/M] | [N/M] | [OK/Pendente] |
| Código | [N] | [N/M] | [N/M] | [OK/Pendente] |
| Observabilidade | [N] | [N/M] | [N/M] | [OK/Pendente] |
| Resiliência | [N] | [N/M] | [N/M] | [OK/Pendente] |
| Segurança | [N] | [N/M] | [N/M] | [OK/Pendente] |
| Deploy | [N] | [N/M] | [N/M] | [OK/Pendente] |
| Documentação | [N] | [N/M] | [N/M] | [OK/Pendente] |

### Decisão

- [ ] **Aprovado para produção** — todos P0 completos
- [ ] **Aprovado com ressalvas** — P0 completos, P1 com plano de data
- [ ] **Não aprovado** — P0 pendentes, lista abaixo

### P0 Pendentes (se aplicável)
| Item | Ação Necessária | Prazo | Owner |
|------|----------------|-------|-------|
| [Item] | [O que falta] | [Data] | [Nome] |

### Aprovações

| Papel | Nome | Data | Assinatura |
|-------|------|------|-----------|
| Tech Lead | [Nome] | [DD/MM/AAAA] | _________ |
| SRE Reviewer | [Nome] | [DD/MM/AAAA] | _________ |
| Security Reviewer | [Nome] | [DD/MM/AAAA] | _________ |

---

## Dicas de Uso
- Não trate este checklist como burocracia — cada item existe por um incidente real
- Comece a preencher no início do projeto, não na véspera do launch
- P0 é inegociável — se não está completo, não vai para produção
- Automatize verificações quando possível (lint rules, CI checks)
- Revise o checklist a cada 6 meses — novos padrões surgem
- Mantenha exemplos de "como fazer" para cada item — facilita adoção
