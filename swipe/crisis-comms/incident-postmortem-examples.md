---
source: "Google SRE Book + PagerDuty Incident Response"
date_captured: 2026-03-11
category: crisis-comms
agents: [cto-architect, cio-engineer, coo-orchestrator]
tags: [incident, postmortem, blameless, sre]
quality: gold
---

# Incident Postmortem — Exemplos Blameless

## O que é um Postmortem Blameless

Um postmortem blameless foca em **sistemas e processos**, não em pessoas.
O objetivo é aprender e prevenir recorrência — nunca punir.

## Template Padrão (Google SRE)

```markdown
# Postmortem: [Título do Incidente]

**Date:** YYYY-MM-DD
**Duration:** Xh Ym
**Severity:** SEV-1/2/3
**Author:** [Nome]
**Status:** Complete / Action items pending

## Summary
[1-2 frases descrevendo o que aconteceu]

## Impact
- Users affected: X
- Revenue impact: $Y
- Duration: Xh Ym
- SLA impact: Z

## Timeline (UTC)
| Time | Event |
|------|-------|
| 14:00 | Deploy v2.3.1 iniciado |
| 14:05 | Erro rate subiu de 0.1% para 15% |
| 14:07 | Alerta PagerDuty disparado |
| 14:12 | Oncall acknowledged |
| 14:25 | Root cause identificado: migration script |
| 14:30 | Rollback iniciado |
| 14:35 | Serviço restaurado |

## Root Cause
[Descrição técnica detalhada da causa raiz]

## What Went Well
- Alerta disparou em < 2 minutos
- Rollback automatizado funcionou

## What Went Wrong
- Migration script não foi testado em staging
- Runbook desatualizado

## Action Items
| Action | Owner | Priority | Due Date |
|--------|-------|----------|----------|
| Add migration test to CI | @eng | P1 | 2026-03-18 |
| Update runbook | @oncall | P2 | 2026-03-25 |

## Lessons Learned
[Insights que transcendem este incidente específico]
```

## Exemplo Real: Database Migration Gone Wrong

**Summary:** Migration script adicionou index em tabela de 500M rows
durante horário de pico, causando lock que bloqueou todas as queries
por 45 minutos.

**Root Cause:** O comando `CREATE INDEX` sem `CONCURRENTLY` bloqueou
a tabela inteira. O playbook de migrations existia mas não cobria
tabelas acima de 100M rows.

**Action Items:**
1. Obrigar `CONCURRENTLY` para tabelas > 10M rows (P0)
2. Adicionar pre-commit hook que bloqueia migrations sem review (P1)
3. Criar runbook específico para large table migrations (P1)
4. Adicionar check no CI que estima tempo de migration (P2)

## O que Aprendemos

1. **Blameless não significa accountless** — ações corretivas têm owners
2. **Timeline é a seção mais valiosa** — mostra onde foram os delays
3. **Action items devem ser rastreados** — postmortem sem follow-up é teatro
4. **Compartilhe amplamente** — postmortems são ferramentas de aprendizado org
5. **Severity clara** — SEV definitions devem ser pré-definidas e objetivas

## Como Aplicar no C-Level Squad

- Template de postmortem em `templates/engineering/`
- Integrar com workflow de incident response
- Agentes `cto-architect` e `cio-engineer` devem referenciar em análises
