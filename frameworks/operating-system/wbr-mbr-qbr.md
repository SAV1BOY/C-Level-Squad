# WBR / MBR / QBR — Weekly, Monthly & Quarterly Business Reviews

> **Domínio:** Operating System
> **Autor de referência:** Amazon (popularização), Colin Bryar & Bill Carr — "Working Backwards"
> **Uso primário:** Sistema de cadência operacional que transforma dados em decisões e accountability.
> **Agente responsável:** coo-orchestrator

---

## Origem e Contexto

O sistema WBR/MBR/QBR foi popularizado pela Amazon sob a liderança de Jeff Bezos e Andy Jassy. Na Amazon, o WBR (Weekly Business Review) é considerado o "sistema operacional" da empresa — o mecanismo que permite escalar de uma livraria online para a empresa mais valiosa do mundo sem perder controle operacional.

O princípio fundacional: **cadência é o sistema operacional**. Sem cadência rigorosa de revisão, decisões ficam ad-hoc, problemas são descobertos tarde demais, e accountability se dilui. O sistema WBR/MBR/QBR cria três loops de feedback com frequências diferentes:

- **WBR (Weekly):** Loop rápido. Detectar desvios, resolver bloqueios, manter ritmo.
- **MBR (Monthly):** Loop médio. Analisar tendências, ajustar táticas, revisar alocação.
- **QBR (Quarterly):** Loop estratégico. Avaliar estratégia, realocar recursos, definir prioridades.

O segredo não é a reunião em si — é o **sistema**: dados padronizados, formato disciplinado, ownership claro, e decisões registradas com DRI e deadline.

---

## Quando Usar

- Sempre. Este é o sistema operacional base do C-Level Squad. Não é opcional.
- Qualquer organização com mais de 10 pessoas precisa de cadência formal de revisão.
- Especialmente crítico em fases de escala, quando a complexidade supera a capacidade de controle informal.
- Quando decisões estão sendo tomadas em "corredores e Slack" em vez de reuniões estruturadas com dados.

---

## Quando NÃO Usar

- Em empresas de 1-3 pessoas — nesse estágio, conversas diárias são suficientes. Adotar MBR apenas.
- WBR para áreas com ciclos naturalmente longos (ex.: P&D de 12 meses) — adaptar para bi-weekly ou monthly.
- Como ritual burocrático sem dados reais — se não há métricas, construa o sistema de dados primeiro.
- Para substituir 1:1s de gestão — WBR/MBR/QBR são revisões de negócio, não coaching sessions.

---

## Estrutura / Modelo

### WBR — Weekly Business Review

| Elemento | Detalhe |
|----------|---------|
| **Frequência** | Semanal, mesmo dia/hora. Inegociável. |
| **Duração** | 60-90 minutos |
| **Participantes** | C-Level + heads de área (DRIs de métricas) |
| **Formato** | Dados → Anomalias → Root-cause → Ações |
| **Artefato** | Dashboard padronizado + ata com decisões |

**Agenda WBR:**
1. **[5 min] Revisão de action items da semana anterior** — Status: done/blocked/at-risk.
2. **[20 min] Dashboard de métricas** — Cada DRI apresenta suas métricas vs target. Foco em ANOMALIAS (desvios > 10% do target ou da tendência).
3. **[20 min] Deep-dive em anomalias** — Para cada anomalia: root-cause, impacto, ação corretiva.
4. **[15 min] Bloqueios e escalations** — O que não pode ser resolvido pelo DRI sozinho? Decisões necessárias.
5. **[10 min] Ações e owners** — Cada ação com DRI, deadline e critério de sucesso. Registrar em `data/registries/`.

### MBR — Monthly Business Review

| Elemento | Detalhe |
|----------|---------|
| **Frequência** | Mensal, primeira semana do mês |
| **Duração** | 2-3 horas |
| **Participantes** | C-Level + líderes de squad |
| **Formato** | Memo (6-pager) → Leitura silenciosa → Discussão → Decisões |
| **Artefato** | Memo + decisões documentadas |

**Agenda MBR:**
1. **[20 min] Leitura silenciosa do memo mensal** — Cada área prepara seção do memo consolidado.
2. **[30 min] Financial review** — P&L, cash flow, burn rate, runway. CFO apresenta.
3. **[30 min] Operational review** — OKRs, pipeline, delivery, qualidade. COO coordena.
4. **[30 min] Growth review** — Funil, CAC/LTV, retention, pipeline. CMO apresenta.
5. **[20 min] Tech & Product review** — Velocity, debt, incidents, roadmap. CTO apresenta.
6. **[20 min] Decisões e priorização** — Ajustes táticos, realocação de recursos, novos investimentos.

### QBR — Quarterly Business Review

| Elemento | Detalhe |
|----------|---------|
| **Frequência** | Trimestral, última semana do trimestre |
| **Duração** | Meio dia (4-6 horas) ou full-day offsite |
| **Participantes** | C-Level + Board (se aplicável) |
| **Formato** | Retrospectiva + Forward-looking + Decisões estratégicas |
| **Artefato** | Strategic memo + OKRs do próximo trimestre |

**Agenda QBR:**
1. **[60 min] Retrospectiva do trimestre** — O que funcionou, o que não funcionou, o que aprendemos.
2. **[60 min] Revisão de OKRs** — Scoring de cada OKR. Celebrar wins. Analisar misses.
3. **[60 min] Revisão estratégica** — OGSM on track? Three Horizons balanceados? Cenários mudaram?
4. **[60 min] Planejamento do próximo trimestre** — Novos OKRs, alocação de recursos, kill list.
5. **[30 min] Decisões e commitments** — Documentar em `data/decisions/`.

---

## Processo de Aplicação (step-by-step)

### Step 1: Definir as Métricas da WBR
Selecionar 15-25 métricas que cobrem todas as áreas do negócio. Para cada métrica:
- **Owner (DRI):** Quem é responsável?
- **Target:** Qual o alvo semanal/mensal?
- **Source:** De onde vem o dado?
- **Threshold:** Qual desvio dispara deep-dive? (geralmente ±10%)

### Step 2: Construir o Dashboard
Dashboard padronizado e atualizado automaticamente (ou semi-automaticamente). Formato Amazon-style:
- Métrica vs target vs semana anterior vs mesma semana do ano anterior.
- Gráfico de tendência (últimas 12 semanas).
- Código de cores: verde (on-track), amarelo (at-risk), vermelho (off-track).

### Step 3: Estabelecer o Ritual
- Definir dia/hora fixa para WBR (ex.: toda segunda às 9h).
- Bloquear agenda de todos os participantes. Não cancelar exceto emergência real.
- Primeiro 3 meses são de construção de hábito — ser rigoroso com formato e horário.

### Step 4: Implementar o Ciclo de Accountability
Após cada WBR/MBR/QBR:
- Publicar ata com decisões e action items em até 24h.
- Cada action item tem DRI + deadline + DoD (Definition of Done).
- Revisão de action items abre a próxima WBR.
- Items não completados sem justificativa → escalation.

### Step 5: Iterar o Formato
Após 4-6 semanas, revisar:
- Quais métricas são realmente discutidas? Remover as ignoradas.
- A reunião acaba no tempo? Se não, reduzir escopo ou melhorar preparação.
- Decisões estão sendo tomadas? Se não, o formato não está funcionando.

---

## Exemplos Práticos

### Exemplo de Métricas WBR (SaaS B2B)

| Área | Métrica | DRI | Target Semanal |
|------|---------|-----|----------------|
| Revenue | New MRR | CMO | R$ 80K |
| Revenue | Churn MRR | CS Lead | < R$ 15K |
| Growth | SQLs gerados | Demand Gen Lead | 25 |
| Growth | Win rate | Sales Lead | > 30% |
| Product | Sprint velocity | Eng Lead | 85% planned |
| Product | P0 bugs open | QA Lead | < 3 |
| CS | NPS (rolling 30d) | CS Lead | ≥ 65 |
| Ops | Action items completion | COO | > 90% |

---

## Armadilhas Comuns

1. **Reunião sem dados:** WBR sem dashboard atualizado é reunião de opiniões. Dados primeiro, discussão depois.
2. **Apresentação em vez de discussão:** O formato ideal é leitura silenciosa + discussão. Apresentações PowerPoint desperdiçam tempo.
3. **Muitas métricas:** Mais de 25 métricas na WBR gera overload. Focar nas que realmente importam e variam semana a semana.
4. **Sem ownership:** Métrica sem DRI = métrica sem dono = métrica que ninguém melhora.
5. **Cancelar "quando não tem nada":** A cadência é o valor. Mesmo semanas "sem novidades" precisam de revisão — silêncio pode esconder problemas.
6. **QBR vira status update:** QBR é para decisões estratégicas, não para reportar o que já foi reportado na MBR. Elevar o nível da conversa.
7. **Atas sem follow-up:** Decisões documentadas que ninguém acompanha. A ata da WBR anterior ABRE a próxima WBR.
8. **Confundir WBR com daily standup:** WBR é business review com métricas. Standup é coordenação tática diária. São complementares.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/operating-system/okrs.md` | OKRs são revisados na MBR (progresso) e QBR (scoring + novos OKRs). |
| `frameworks/operating-system/rasi-dri.md` | Cada métrica e action item da WBR tem DRI claro. |
| `frameworks/operating-system/decision-memo-framework.md` | MBR usa formato de memo (6-pager). Decisões Type 1 geram memo dedicado. |
| `frameworks/operating-system/escalation-ladders.md` | WBR é o fórum padrão de escalation operacional. |
| `frameworks/vision-strategy/ogsm.md` | OGSM é revisado na QBR. Measures do OGSM alimentam o dashboard da WBR/MBR. |
| `frameworks/vision-strategy/three-horizons.md` | QBR revisa o portfólio dos três horizontes. |
| `checklists/operating-review-quality.md` | Checklist para garantir qualidade da WBR/MBR/QBR. |
| `templates/operating-system/wbr-dashboard.md` | Template de dashboard para a WBR. |

---

## Referências

- Bryar, C. & Carr, B. (2021). *Working Backwards: Insights, Stories, and Secrets from Inside Amazon*. St. Martin's Press.
- Anderson, B. (2024). *The Amazon Way: Leadership Principles*. (Cadência e métricas no estilo Amazon.)
- Grove, A. (1983). *High Output Management*. Vintage. (Fundamentos de meeting discipline e output-oriented management.)
- C-Level Squad `config.yaml` — Princípio: "Cadência é o sistema operacional. Sem cadência, sem controle."
