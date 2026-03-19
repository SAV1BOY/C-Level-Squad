# OKRs — Objectives and Key Results

> **Domínio:** Operating System
> **Autor de referência:** Andy Grove (Intel), John Doerr — "Measure What Matters"
> **Uso primário:** Alinhar a organização em ciclos trimestrais de execução com foco e accountability.
> **Agente responsável:** coo-orchestrator

---

## Origem e Contexto

OKR (Objectives and Key Results) é um sistema de gestão por metas criado por Andy Grove na Intel nos anos 1970 e popularizado por John Doerr, que o levou ao Google em 1999. Desde então, foi adotado por centenas de empresas de tecnologia (LinkedIn, Twitter, Spotify, Nubank) e se tornou o padrão de facto para gestão de metas em startups e scale-ups.

O sistema é composto por dois elementos:
- **Objective (O):** O QUÊ queremos alcançar. Qualitativo, inspirador, direcionado. Deve gerar energia.
- **Key Results (KR):** COMO sabemos que alcançamos. Quantitativo, mensurável, com prazo. 2-5 KRs por Objective.

A mecânica central: OKRs são definidos trimestralmente, revisados semanalmente (WBR), e scored no final do trimestre. O scoring usa escala 0.0-1.0, onde 0.7 é "bom" — se você atinge 1.0 em tudo, seus OKRs eram fáceis demais.

O poder do OKR não está no template — está no sistema: **cadência de definição, alinhamento vertical/horizontal, revisão disciplinada, e aprendizado contínuo.**

---

## Quando Usar

- Sempre. OKRs são o mecanismo de execução trimestral do C-Level Squad.
- Para traduzir estratégia (OGSM) em metas acionáveis de 90 dias.
- Para alinhar múltiplas áreas em torno das mesmas prioridades.
- Para criar accountability sem microgerenciamento — o DRI define COMO atingir o KR.
- Em momentos de foco — OKRs forçam priorização. 3-5 OKRs, não 15.

---

## Quando NÃO Usar

- Como lista de tarefas — OKRs são outcomes, não outputs. "Lançar feature X" é output. "Aumentar ativação em 20%" é outcome.
- Para trabalho BAU (Business As Usual) — OKR é para mover o ponteiro, não para manter as luzes acesas.
- Sem cadência de revisão — OKR sem WBR é decoração. Definir em janeiro e revisar em março não funciona.
- Em organizações que punem metas não atingidas — OKRs são aspiracionais. Atingir 70% é bom. Se 100% = obrigatório, as metas serão conservadoras.
- Como avaliação de performance direta — OKRs informam performance, mas atrelar bônus diretamente a KRs incentiva sandbagging.

---

## Estrutura / Modelo

### Anatomia de um OKR

```
┌─────────────────────────────────────────────────────────────────────┐
│ OBJECTIVE: Tornar-se referência em experiência do cliente no Brasil │
│ (Qualitativo, inspirador, tempo-bound por trimestre)                │
├─────────────────────────────────────────────────────────────────────┤
│ KR1: Aumentar NPS de 55 para 70                                    │
│ KR2: Reduzir tempo médio de resposta de suporte de 4h para 1h      │
│ KR3: Atingir 90% de resolução no primeiro contato (FCR)            │
│ (Quantitativo, mensurável, com baseline e target)                   │
├─────────────────────────────────────────────────────────────────────┤
│ DRI: Head de Customer Success                                       │
│ Cadência: Revisão semanal na WBR, scoring na QBR                   │
└─────────────────────────────────────────────────────────────────────┘
```

### Tipos de KR

| Tipo | Exemplo | Quando Usar |
|------|---------|-------------|
| **Métrica** | "De X para Y" | Quando há baseline mensurável. Preferido. |
| **Milestone** | "Lançar MVP até DD/MM" | Quando o outcome é binário (fez ou não fez). Usar com parcimônia. |
| **Qualidade** | "Score ≥ 80 no audit" | Quando há rubric de avaliação definida. |

### Hierarquia de OKRs

```
Company OKRs (Vision Chief + C-Level)
    ├── Area OKR: Growth (CMO)
    │       ├── Squad OKR: Demand Gen
    │       └── Squad OKR: Product Marketing
    ├── Area OKR: Engineering (CTO)
    │       ├── Squad OKR: Platform
    │       └── Squad OKR: Product A
    └── Area OKR: Operations (COO)
            ├── Squad OKR: CS
            └── Squad OKR: Finance
```

---

## Processo de Aplicação (step-by-step)

### Step 1: Input Estratégico
Antes de definir OKRs, revisar:
- OGSM (`frameworks/vision-strategy/ogsm.md`) — os Goals e Strategies do ano.
- Resultado do trimestre anterior — o que aprendemos? O que precisa continuar?
- Three Horizons (`frameworks/vision-strategy/three-horizons.md`) — H1, H2, H3 representados nos OKRs?

### Step 2: Definir OKRs Corporativos (Top-Down)
Vision Chief + C-Level definem 3-5 OKRs corporativos para o trimestre:
- Devem cobrir as prioridades mais importantes do trimestre.
- Cada OKR tem um DRI do C-Level.
- Regra: se não cabe em 5 OKRs, está tentando fazer demais.

### Step 3: Cascatear para Áreas (Bottom-Up + Top-Down)
Cada área propõe seus OKRs alinhados aos corporativos:
- **Alignment vertical:** Pelo menos 1 OKR da área conecta diretamente a um OKR corporativo.
- **Alignment horizontal:** OKRs cross-squad que requerem colaboração são identificados e alinhados.
- **Autonomia:** Cada área pode ter 1-2 OKRs "locais" que não derivam do corporativo, mas são importantes.

### Step 4: Negociar e Alinhar
Processo de alinhamento em 2 rodadas:
1. **Rodada 1:** Áreas apresentam propostas de OKRs. COO facilita.
2. **Rodada 2:** Feedback, ajustes, resolução de dependências cross-squad.
3. **Publicação:** OKRs finalizados e publicados em local acessível a todos.

### Step 5: Executar com Cadência
- **Semanal (WBR):** Revisar progresso dos KRs. Identificar bloqueios. Ajustar ações.
- **Mensal (MBR):** Avaliar tendências. Algum KR precisa de intervenção? Realocar recursos?
- **Fim do trimestre (QBR):** Scoring oficial. Retrospectiva. Definir OKRs do próximo trimestre.

### Step 6: Scoring
Para cada KR, score de 0.0 a 1.0:
- **0.0-0.3:** Falha significativa. O que impediu?
- **0.4-0.6:** Progresso parcial. O que poderia ser diferente?
- **0.7-0.8:** Bom resultado. Target quase ou totalmente atingido.
- **0.9-1.0:** Excepcional. Verificar se o target era ambicioso o suficiente.

Score do Objective = média dos KRs. Score "saudável" da organização: 0.6-0.7 na média.

---

## Exemplos Práticos

### Exemplo 1: OKR Corporativo (SaaS B2B)
**O:** Acelerar crescimento sustentável com unit economics saudáveis.
- KR1: Aumentar MRR de R$ 800K para R$ 1.1M.
- KR2: Manter CAC Payback ≤ 12 meses.
- KR3: Atingir Net Revenue Retention ≥ 110%.
- DRI: Vision Chief. Reviewed: WBR.

### Exemplo 2: OKR de Área — Engineering
**O:** Entregar infra confiável que habilite crescimento 2x sem degradação.
- KR1: Uptime ≥ 99.95% (de 99.8% atual).
- KR2: Deploy frequency de 2x/semana para 1x/dia.
- KR3: Zero incidentes SEV1 no trimestre.
- DRI: CTO. Reviewed: WBR.

### Exemplo 3: OKR de Área — Growth
**O:** Construir máquina de aquisição previsível e escalável.
- KR1: Gerar 300 SQLs/trimestre (de 180 atual).
- KR2: Reduzir CAC de R$ 3.500 para R$ 2.800.
- KR3: Lançar 2 growth loops documentados e medidos.
- DRI: CMO. Reviewed: WBR.

---

## Armadilhas Comuns

1. **OKRs demais:** Mais de 5 OKRs por nível = falta de priorização. Se tudo é prioridade, nada é.
2. **KRs como tarefas:** "Lançar feature X" é output, não outcome. O KR deve medir o RESULTADO do lançamento.
3. **Sem baseline:** "Melhorar NPS" sem saber o NPS atual é impossível de medir e de saber se atingiu.
4. **Sandbagging:** Definir KRs fáceis para garantir 1.0. Score médio de 1.0 = OKRs sem ambição.
5. **OKR orphan:** OKR sem revisão semanal é documento morto. A cadência WBR é essencial.
6. **Binary OKR:** "Lançar produto até março" — ou fez ou não fez. Preferir KRs com gradação (% de conclusão, métricas).
7. **Cascading mecânico:** Copiar o OKR corporativo para a área sem adaptação. Cada nível traduz para seu contexto.
8. **OKR como avaliação de performance:** Se bônus é atrelado diretamente ao score do OKR, as pessoas definem metas fáceis.
9. **Esquecer BAU:** OKRs são para mover o ponteiro. O trabalho de manutenção existe mas não é OKR. Não ignore BAU, apenas não o misture.
10. **Não celebrar:** Atingir 0.7 é bom. Se a cultura só reconhece 1.0, ninguém arrisca.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/vision-strategy/ogsm.md` | OGSM é o plano anual. OKRs são o desdobramento trimestral. |
| `frameworks/operating-system/wbr-mbr-qbr.md` | WBR revisa progresso semanal dos KRs. QBR faz scoring e define novos OKRs. |
| `frameworks/operating-system/rasi-dri.md` | Cada OKR e KR tem um DRI claro na matriz RASI. |
| `frameworks/vision-strategy/three-horizons.md` | OKRs devem cobrir H1 (execução), H2 (escala) e H3 (exploração). |
| `frameworks/operating-system/decision-memo-framework.md` | Decisões de mudança de OKR mid-quarter requerem memo. |
| `checklists/okr-quality.md` | Checklist para validar qualidade dos OKRs antes de publicar. |
| `checklists/quarterly-planning-quality.md` | Checklist para o processo de planejamento trimestral. |

---

## Referências

- Doerr, J. (2018). *Measure What Matters*. Portfolio/Penguin.
- Grove, A. (1983). *High Output Management*. Vintage Books.
- Wodtke, C. (2016). *Radical Focus*. Cucina Media.
- Niven, P. & Lamorte, B. (2016). *Objectives and Key Results*. Wiley.
- Google re:Work. "Guide: Set goals with OKRs." (Disponível em rework.withgoogle.com.)
