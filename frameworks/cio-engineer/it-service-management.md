# ITSM Framework — Gestão de Serviços de TI para Empresas em Crescimento

## Propósito e Contexto

IT Service Management (ITSM) é o conjunto de práticas para planejar, entregar, operar e
controlar os serviços de TI oferecidos pela organização. Em empresas de tecnologia jovens,
ITSM é frequentemente negligenciado — "somos ágeis, não precisamos de ITIL". O resultado é
caos quando a empresa cresce: ninguém sabe quem tem acesso a quê, incidentes não são rastreados,
mudanças em produção não são coordenadas, e o onboarding de novos colaboradores leva semanas.

Este framework oferece uma versão pragmática e enxuta de ITSM, inspirada em ITIL v4 mas
adaptada para empresas de tecnologia. Não é burocracia — é o mínimo de estrutura para operar
de forma confiável em escala.

## Quando Usar

- Quando a empresa ultrapassa ~50 colaboradores (ponto de inflexão)
- Quando incidentes começam a repetir sem resolução definitiva
- Quando o onboarding de novos colaboradores é lento e inconsistente
- Quando há confusão sobre quem é responsável por quais serviços
- Na preparação para auditorias (SOC2, ISO 27001)
- Quando shadow IT está proliferando sem controle

## Componentes do Framework

### 1. Catálogo de Serviços

Documente todos os serviços de TI oferecidos:

```markdown
| Serviço | Descrição | Owner | SLA | Nível de Suporte |
|---------|-----------|-------|-----|-----------------|
| Email & Calendar | Google Workspace/M365 | IT Ops | 99.9% | L1 |
| Code Repository | GitHub/GitLab | Platform | 99.9% | L2 |
| CI/CD Pipeline | GitHub Actions | Platform | 99.5% | L2 |
| Access Management | Okta/Auth0 | Security | 99.9% | L1 |
| Monitoring | Datadog/Grafana | SRE | 99.5% | L2 |
| Endpoint Mgmt | MDM | IT Ops | 99.0% | L1 |
```

### 2. Gestão de Incidentes

**Classificação de Severidade:**
| Sev | Critério | Tempo de Resposta | Tempo de Resolução |
|-----|----------|------------------|-------------------|
| SEV1 | Serviço crítico fora do ar, impacto em clientes | 15 min | 1 hora |
| SEV2 | Serviço degradado, impacto significativo | 30 min | 4 horas |
| SEV3 | Problema limitado, workaround disponível | 4 horas | 24 horas |
| SEV4 | Inconveniente menor, sem impacto em negócio | 24 horas | 5 dias |

**Processo de Incidente:**
1. Detecção (alerta automático ou reporte manual)
2. Classificação (severidade + área afetada)
3. Comunicação (stakeholders notificados conforme severidade)
4. Investigação e resolução
5. Post-mortem (para SEV1 e SEV2 — blameless)
6. Follow-up de ações preventivas

### 3. Gestão de Mudanças

Nem toda mudança precisa de processo pesado. Classifique:

**Standard Changes:** Pré-aprovadas, baixo risco, procedimento documentado
- Exemplo: atualização de dependências, scaling de infra, novo usuário
- Processo: executar seguindo runbook, registrar

**Normal Changes:** Risco moderado, precisa de review
- Exemplo: nova integração, mudança de arquitetura, nova ferramenta
- Processo: RFC (Request for Change) → Review → Aprovação → Execução → Validação

**Emergency Changes:** Urgente, risco alto mas necessário
- Exemplo: fix de segurança, rollback de deploy problemático
- Processo: executar → registrar → review posterior

### 4. Gestão de Requisições

Centralize requisições com self-service sempre que possível:

**Requisições Comuns:**
- Acesso a sistemas (self-service via Okta/similar)
- Novo equipamento (workflow aprovação → procurement → setup)
- Instalação de software (catálogo aprovado com MDM)
- Novo ambiente de desenvolvimento (self-service via IDP)
- Certificados e licenças (workflow automatizado)

### 5. Gestão de Ativos e Configuração

**CMDB Simplificada:**
- Inventário de hardware (laptops, servidores, devices)
- Inventário de software (licenças, SaaS, open source)
- Mapa de dependências entre serviços
- Compliance de configuração (baseline vs. actual)

## Processo Passo-a-Passo

### Fase 1: Foundation (mês 1-2)
1. Documentar catálogo de serviços atual
2. Implementar ferramenta de service desk (Jira SM, Zendesk, etc.)
3. Definir processo de incidentes com severidades
4. Estabelecer on-call rotation para serviços críticos

### Fase 2: Estruturação (mês 3-4)
1. Implementar gestão de mudanças (standard/normal/emergency)
2. Criar runbooks para incidentes recorrentes
3. Automatizar requisições mais comuns (self-service)
4. Implementar inventário de ativos

### Fase 3: Otimização (mês 5-6)
1. Implementar SLOs e error budgets para serviços internos
2. Automatizar detecção e resposta a incidentes comuns
3. Dashboard de saúde de serviços (service health)
4. Revisão de processos com feedback dos usuários

### Fase 4: Maturidade (ongoing)
1. Continuous improvement baseado em métricas
2. Automação avançada (AIOps para detecção)
3. Integração com gestão de mudanças de produto
4. Preparação para certificações (SOC2, ISO)

## Template de Post-Mortem

```markdown
# Post-Mortem: [Título do Incidente]
**Data:** [YYYY-MM-DD] | **Severidade:** [SEV1/2] | **Duração:** [X horas]

## Resumo
[1-2 frases sobre o que aconteceu e o impacto]

## Timeline
| Hora | Evento |
|------|--------|
| HH:MM | [Primeiro sinal do problema] |
| HH:MM | [Detecção/alerta] |
| HH:MM | [Início da resposta] |
| HH:MM | [Resolução] |

## Root Cause
[Causa raiz técnica e organizacional]

## Impacto
- Clientes afetados: [número]
- Receita impactada: [estimativa]
- SLA breach: [sim/não]

## O Que Funcionou
- [Ponto positivo na resposta]

## O Que Pode Melhorar
- [Ponto de melhoria]

## Action Items
| Ação | Owner | Prazo | Status |
|------|-------|-------|--------|
| [Ação preventiva] | [Nome] | [Data] | [TODO/DONE] |
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| MTTR (SEV1) | < 1 hora | Por incidente |
| MTTR (SEV2) | < 4 horas | Por incidente |
| SLA compliance | > 95% | Mensal |
| First-contact resolution rate | > 60% | Mensal |
| Post-mortem completion (SEV1/2) | 100% em 48h | Por incidente |
| Self-service adoption | > 70% das requisições | Trimestral |
| Incidentes recorrentes | Tendência decrescente | Mensal |
| User satisfaction (CSAT) | > 4/5 | Trimestral |

## Referências Cruzadas

- `frameworks/cio-engineer/security-posture.md` — Segurança nos processos de ITSM
- `frameworks/cio-engineer/cloud-strategy.md` — Infraestrutura que suporta ITSM
- `frameworks/cio-engineer/digital-transformation.md` — ITSM como fundação da transformação
- `frameworks/cto-architect/engineering-excellence.md` — Práticas de reliability engineering
- `frameworks/cto-architect/platform-strategy.md` — Plataforma e self-service
- `frameworks/shared/crisis-management.md` — Escalação de incidentes para crise
- `frameworks/shared/communication-framework.md` — Comunicação durante incidentes
