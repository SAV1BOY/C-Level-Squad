# DORA Metrics — As 4 Métricas de DevOps Performance

> **Domínio:** Engineering & Tech
> **Autor de referência:** Nicole Forsgren, Jez Humble, Gene Kim — "Accelerate"
> **Uso primário:** Medir e melhorar a performance de delivery de software.
> **Agente responsável:** cto-architect

---

## Origem e Contexto

As DORA Metrics (DevOps Research and Assessment) foram desenvolvidas pela Dra. Nicole Forsgren, Jez Humble e Gene Kim, baseadas em 7 anos de pesquisa com mais de 36.000 profissionais. Publicadas no livro "Accelerate" (2018) e no annual State of DevOps Report (Google Cloud), as 4 métricas provaram estatisticamente que **times de alta performance em software delivery também geram melhores resultados de negócio** — mais receita, maior satisfação do cliente e melhor retenção de talentos.

As 4 métricas dividem-se em dois pares:

**Throughput (Velocidade):**
1. **Deployment Frequency (DF):** Com que frequência código chega a produção.
2. **Lead Time for Changes (LT):** Tempo entre commit e código rodando em produção.

**Stability (Estabilidade):**
3. **Change Failure Rate (CFR):** % de deploys que causam falha em produção.
4. **Mean Time to Restore (MTTR):** Tempo para restaurar serviço após falha.

O insight contra-intuitivo: **velocidade e estabilidade NÃO são trade-offs.** Times elite são rápidos E estáveis. Ir devagar não é mais seguro — é mais arriscado, porque deploys grandes e infrequentes são mais propensos a falha.

---

## Quando Usar

- Como baseline de performance de engenharia — medir antes de melhorar.
- Na WBR/MBR do CTO — as 4 métricas são KPIs obrigatórios de engenharia.
- Para justificar investimento em developer experience, CI/CD, observability.
- Como benchmarking — comparar com os níveis Elite/High/Medium/Low do State of DevOps Report.
- Na avaliação de maturidade técnica para decisões de M&A ou due diligence.
- Para identificar gargalos no pipeline de delivery — qual das 4 métricas é o bottleneck?

---

## Quando NÃO Usar

- Como ferramenta de avaliação individual — DORA mede TIMES, não pessoas.
- Para comparar times com contextos radicalmente diferentes — time de infra vs time de produto têm realidades distintas.
- Como meta absoluta — "Elite em tudo" não é necessariamente o objetivo. O contexto importa.
- Sem entender a cadeia de valor — a métrica sem entendimento do pipeline é número sem ação.

---

## Estrutura / Modelo

### As 4 Métricas e Benchmarks

```
┌─────────────────────────────────────────────────────────────────────┐
│                    DORA METRICS BENCHMARK                            │
├──────────────────┬──────────┬──────────┬──────────┬────────────────┤
│ Métrica          │  Elite   │   High   │  Medium  │     Low        │
├──────────────────┼──────────┼──────────┼──────────┼────────────────┤
│ Deployment       │ On-demand│ Weekly-  │ Monthly- │ Monthly-       │
│ Frequency        │ (múltiplos│ Monthly  │ Semestral│ Semestral      │
│                  │ por dia) │          │          │ (menos freq.)  │
├──────────────────┼──────────┼──────────┼──────────┼────────────────┤
│ Lead Time for    │ < 1 hora │ 1 dia-   │ 1 semana-│ 1 mês-        │
│ Changes          │          │ 1 semana │ 1 mês   │ 6 meses        │
├──────────────────┼──────────┼──────────┼──────────┼────────────────┤
│ Change Failure   │ 0-15%    │ 16-30%   │ 16-30%  │ 16-30%         │
│ Rate             │          │          │          │ (> mais comum) │
├──────────────────┼──────────┼──────────┼──────────┼────────────────┤
│ Mean Time to     │ < 1 hora │ < 1 dia  │ 1 dia-  │ 1 semana-      │
│ Restore (MTTR)   │          │          │ 1 semana │ 1 mês          │
└──────────────────┴──────────┴──────────┴──────────┴────────────────┘
```

### Relação entre Métricas

```
                    THROUGHPUT
                 (mais é melhor)
                       ↑
    Deployment ────────┤
    Frequency          │
                       │
    Lead Time ─────────┤         ← O objetivo é estar
    for Changes        │            no quadrante SUPERIOR
                       │            DIREITO (rápido e estável)
    ───────────────────┼──────────────────→ STABILITY
                       │              (mais é melhor)
    Change Failure ────┤
    Rate (inverso)     │
                       │
    MTTR ──────────────┘
    (inverso)
```

---

## Processo de Aplicação (step-by-step)

### Step 1: Medir o Baseline
Antes de melhorar, medir onde o time está hoje. Para cada métrica:

**Deployment Frequency:**
- Contar deploys para produção por semana/mês.
- Incluir todos os serviços (não apenas o principal).
- Fonte: CI/CD pipeline logs, deploy tracker.

**Lead Time for Changes:**
- Medir tempo entre primeiro commit da feature e deploy em produção.
- Incluir: code review, QA, staging, deploy.
- Fonte: Git logs + CI/CD timestamps.

**Change Failure Rate:**
- % de deploys que resultam em: rollback, hotfix, incident, ou degradação de serviço.
- Fonte: incident tracker, deploy logs, rollback counter.

**MTTR:**
- Tempo entre detecção da falha e restauração completa do serviço.
- Fonte: alerting system timestamps, incident management tool.

### Step 2: Identificar o Bottleneck
Das 4 métricas, qual é a mais fraca? Priorizar:
- Se DF é baixo → foco em CI/CD, feature flags, trunk-based development.
- Se LT é alto → foco em review process, test automation, pipeline efficiency.
- Se CFR é alto → foco em test coverage, code review, canary deploys.
- Se MTTR é alto → foco em observability, alerting, runbooks, incident management.

### Step 3: Definir Target
Usando os benchmarks DORA, definir target para os próximos 6-12 meses:
- Ser realista: pular de Low para Elite em 1 trimestre não é factível.
- Focar em subir 1 nível por vez no bottleneck.
- Exemplo: DF de monthly → weekly em 6 meses.

### Step 4: Implementar Práticas de Melhoria

**Para melhorar Deployment Frequency:**
- Trunk-based development (branches curtas, < 1 dia).
- Feature flags para separar deploy de release.
- Automatizar pipeline de CI/CD end-to-end.

**Para melhorar Lead Time:**
- Limitar WIP (Work in Progress) — menos coisas ao mesmo tempo, mais fluxo.
- Pair programming ou async code review com SLA (< 4h para review).
- Testes automatizados como gate, não manual QA.

**Para melhorar Change Failure Rate:**
- Aumentar test coverage (unit + integration).
- Canary deployments e progressive rollouts.
- Pre-production environments que espelham produção.

**Para melhorar MTTR:**
- Observability stack (logs, metrics, traces) — ver `frameworks/engineering-tech/sre-basics.md`.
- Runbooks atualizados para cenários comuns.
- On-call rotation com escalation clara (`frameworks/operating-system/escalation-ladders.md`).
- Blameless postmortems para aprendizado contínuo.

### Step 5: Monitorar na Cadência WBR
Incluir as 4 métricas na WBR do CTO:
- Dashboard atualizado semanalmente.
- Anomalias (ex.: CFR spike após deploy de quarta) discutidas em real-time.
- Trends (melhoria ou degradação ao longo de semanas).

### Step 6: Correlacionar com Métricas de Negócio
O poder real do DORA é a correlação com negócio:
- DF alta → features chegam ao cliente mais rápido → time-to-value menor.
- MTTR baixo → menos downtime → melhor NPS e retenção.
- Apresentar esta correlação na MBR/QBR para C-Level.

---

## Exemplos Práticos

### Exemplo: Scale-up SaaS (50 engenheiros)

**Baseline (Q1):** DF: bi-weekly, LT: 5 dias, CFR: 25%, MTTR: 8h. Classificação: Medium.
**Target (Q4):** DF: 2x/semana, LT: 2 dias, CFR: 15%, MTTR: 2h. Classificação: High.

**Ações implementadas:**
- CI/CD automatizado end-to-end (reduz LT).
- Feature flags (habilita DF mais alto sem risco).
- Canary deploys para 5% do tráfego antes de full rollout (reduz CFR).
- Observability stack com Datadog (reduz MTTR).

**Resultado Q4:** DF: 3x/semana, LT: 1.5 dias, CFR: 12%, MTTR: 1.5h. High.

---

## Armadilhas Comuns

1. **Gamificar as métricas:** Times que inflam DF com deploys triviais ou classificam incidents como "não-incidents" para reduzir CFR. Métricas honestas > métricas bonitas.
2. **Medir sem agir:** Dashboard bonito sem plano de melhoria é vanity metric.
3. **Usar como rank:** Comparar Squad A vs Squad B sem considerar contexto (complexidade, legacy, tamanho) é injusto.
4. **Focar apenas em velocidade:** DF e LT sem CFR e MTTR é "mover rápido e quebrar coisas." Não mais aceitável.
5. **Ignorar a cultura:** DORA melhora com práticas técnicas E culturais (psychological safety, blameless culture).
6. **Automatizar sem entender:** Automatizar um processo ruim apenas faz ele ser ruim mais rápido.
7. **MTTR como única métrica de confiabilidade:** Complementar com SLOs e error budgets (`frameworks/engineering-tech/sre-basics.md`).

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/engineering-tech/sre-basics.md` | SRE (SLOs, error budgets) complementa DORA com perspectiva de confiabilidade do cliente. |
| `frameworks/engineering-tech/architecture-patterns.md` | Arquitetura impacta DORA — monolito vs microservices afeta DF e LT. |
| `frameworks/engineering-tech/platform-engineering.md` | Developer platform reduz LT e melhora DF com golden paths. |
| `frameworks/engineering-tech/adr-system.md` | Decisões de arquitetura que impactam DORA devem ser registradas como ADR. |
| `frameworks/operating-system/wbr-mbr-qbr.md` | DORA metrics são KPIs obrigatórios na WBR do CTO. |
| `frameworks/operating-system/okrs.md` | OKRs de engenharia frequentemente incluem targets DORA. |
| `checklists/tech-architecture-decision-quality.md` | Checklist inclui impacto em DORA metrics. |

---

## Referências

- Forsgren, N., Humble, J. & Kim, G. (2018). *Accelerate: The Science of Lean Software and DevOps*. IT Revolution.
- Google Cloud. *State of DevOps Report* (annual). cloud.google.com/devops.
- Humble, J. & Farley, D. (2010). *Continuous Delivery*. Addison-Wesley.
- Kim, G. et al. (2016). *The DevOps Handbook*. IT Revolution.
