# Workflow 19 — Culture Health Cycle

> **Monitorar, medir e melhorar continuamente a saúde cultural da organização.**
> Cultura é o que acontece quando ninguém está olhando. Este workflow garante que estamos olhando.

---

## Objetivo

Estabelecer um ciclo contínuo de monitoramento e melhoria da saúde cultural da organização. O workflow garante que:

1. **Saúde cultural é medida regularmente** — não por feeling, mas por dados
2. **Sinais de alerta são detectados proativamente** — antes de virar crise
3. **Ações corretivas são rápidas e específicas** — não genéricas
4. **Valores declarados e comportamentos observados estão alinhados** — walk the talk
5. **A cultura suporta a estratégia** — não a contradiz

> **Princípio:** Cultura come estratégia no café da manhã (Drucker). Se não mede, não gerencia.

---

## Agentes Envolvidos

| Agente | Papel no Workflow |
|--------|-------------------|
| **COO Orchestrator** | Lead — coordena ciclo, consolida dados, drives action plans |
| **Vision Chief (CEO)** | Reviewer — alinhamento com valores e visão, decisões de cultura |
| **CMO Architect** | Support — employer brand, cultura externamente comunicada |
| **CTO Architect** | Support — cultura de engenharia, developer experience |
| **CAIO Architect** | Support — cultura de inovação e experimentação com IA |
| **CFO Strategist** | Support — impacto financeiro de turnover, engagement em investimento |
| **Squad Coordinator** | Logística — administração de surveys, compilação de dados |

---

## Trigger (quando iniciar)

### Triggers Periódicos
- Cadência trimestral: pulse survey + review (alinhado ao QBR)
- Cadência anual: deep culture assessment
- Cadência semestral: engagement survey completo

### Triggers por Evento
- Turnover spike (> 2x da média em qualquer equipe)
- Engagement score drop > 15% em qualquer métrica
- Incidente cultural (harassment, discrimination, ethics violation)
- Pós-layoff ou reorganização significativa
- Feedback negativo em plataformas públicas (Glassdoor, etc.)
- M&A ou integração de nova equipe

---

## Pré-condições

- [ ] Valores organizacionais definidos e comunicados
- [ ] Baseline de engagement medido (primeiro survey feito)
- [ ] Canal confidencial para feedback estabelecido
- [ ] Org Health Registry inicializado (`data/registries/org-health-registry.yaml`)
- [ ] Budget para ferramentas de survey e intervenção

---

## Processo (step-by-step)

### Stage 1: Pulse Survey Design (2-3 dias)

**Owner**: COO Orchestrator

1. **Definir Dimensões de Medição**
   ```
   ┌──────────────────────────────────────────────────┐
   │           CULTURE HEALTH DIMENSIONS               │
   ├────────────┬────────────┬────────────┬────────────┤
   │ ENGAGEMENT │  ALIGNMENT │   SAFETY   │  GROWTH    │
   │            │            │            │            │
   │ Motivação  │ Com valores│ Psicológica│ Aprendizado│
   │ Pertenci.  │ Com missão │ Para errar │ Carreira   │
   │ Orgulho    │ Com líderes│ Para falar │ Feedback   │
   │ Retenção   │ Com equipe │ Diversidade│ Autonomia  │
   └────────────┴────────────┴────────────┴────────────┘
   ```

2. **Desenhar Survey**
   - Máximo 15 perguntas (respeitar tempo das pessoas)
   - Mix: Likert scale (quantitativo) + open-ended (qualitativo)
   - Perguntas core mantidas para tracking longitudinal
   - 2-3 perguntas rotativas por tema do momento

3. **Testar Survey**
   - Piloto com Squad Coordinator e 2-3 voluntários
   - Verificar clareza, tempo de resposta, anonimato

### Stage 2: Data Collection (5-7 dias)

**Owner**: Squad Coordinator

1. **Distribuir Survey**
   - Comunicação clara: por quê, para quê, anonimato garantido
   - Deadline: 5 dias úteis
   - Reminders: dia 3 e dia 5
   - Meta de response rate: > 70%

2. **Dados Complementares**
   - Turnover data (voluntário vs involuntário)
   - Absenteísmo
   - Internal mobility
   - Tempo médio de fechamento de vagas
   - eNPS se disponível

3. **Qualitative Data**
   - Open-ended responses categorizadas
   - Feedback de exit interviews
   - Feedback de 1-on-1s agregado (temas, não individuais)
   - Menções em canais internos (Slack, etc.)

### Stage 3: Analysis (2-3 dias)

**Owner**: COO Orchestrator

1. **Quantitative Analysis**
   - Scores por dimensão
   - Trend vs quarter anterior
   - Breakdown por equipe/departamento (se N > 5 para anonimato)
   - Correlações (ex: engagement × tenure, safety × team size)

2. **Qualitative Analysis**
   - Temas emergentes das respostas abertas
   - Sentimento geral: positivo, neutro, negativo
   - Verbatims impactantes (anonimizados)
   - Contradições entre quanti e quali

3. **Benchmark**
   - vs baseline da organização
   - vs período anterior
   - vs benchmarks da indústria (se disponível)

### Stage 4: Pattern Identification (1-2 dias)

**Owner**: COO Orchestrator + Vision Chief

1. **Identify Hotspots**
   - Equipes com scores significativamente abaixo da média
   - Dimensões com queda > 10%
   - Temas recorrentes em feedback qualitativo
   - Gaps entre diferentes níveis hierárquicos

2. **Root Cause Hypothesis**
   - Para cada hotspot: o que pode estar causando?
   - Fatores: liderança, workload, change fatigue, communication, tools
   - Validar hipóteses com dados complementares

3. **Priorizar**
   - Urgência × Impacto matrix
   - Quick wins vs mudanças estruturais
   - Must-fix (cultural risks) vs nice-to-have (optimization)

### Stage 5: Action Planning (2-3 dias)

**Owner**: COO Orchestrator

1. **Para Cada Hotspot**
   - Definir ação específica e mensurável
   - Atribuir DRI e deadline
   - Definir como medir sucesso

2. **Tipos de Ações**
   | Tipo | Exemplo | Timeline |
   |------|---------|----------|
   | Quick win | Ajustar cadência de 1-on-1s | 1-2 semanas |
   | Comunicação | Town hall para endereçar concerns | 1 semana |
   | Processo | Redesenhar processo de feedback | 1 mês |
   | Estrutural | Reorganizar equipe com conflito | 1-3 meses |
   | Cultural shift | Programa de psychological safety | 3-6 meses |

3. **Validar com Vision Chief**
   - Ações alinhadas com valores?
   - Budget necessário aprovado?
   - Communication plan para mudanças visíveis?

### Stage 6: Intervention Design (3-5 dias)

**Owner**: COO Orchestrator + DRIs das ações

1. **Desenhar Intervenções**
   - Para mudanças estruturais: plano detalhado com milestones
   - Para comunicação: talking points e Q&A preparados
   - Para processos: novo processo documentado e comunicado

2. **Prepare Leaders**
   - Briefing para managers sobre resultados (confidencial)
   - Guidelines de como discutir com equipes
   - Training se necessário (feedback, difficult conversations)

3. **Communication Plan**
   - O que comunicar: resultados agregados (transparência)
   - O que fazer: ações definidas (accountability)
   - Quando medir de novo: próximo pulse survey (follow-through)

### Stage 7: Execution (duração variável)

**Owner**: DRIs das ações

1. **Implementar Ações**
   - Seguir plano definido no Stage 5
   - Check-in semanal com COO
   - Ajustar se necessário (ação não está funcionando)

2. **Track Progress**
   - Status de cada ação no tracking
   - Feedback informal de equipes
   - Leading indicators de melhoria

3. **Escalation se Bloqueado**
   - DRI → COO → Vision Chief
   - Se ação requer budget não previsto → CFO
   - Se ação envolve mudança organizacional → Vision Chief

### Stage 8: Follow-up Measurement (próximo cycle)

**Owner**: COO Orchestrator

1. **Next Pulse Survey**
   - Incluir perguntas específicas sobre mudanças implementadas
   - Comparar scores das dimensões onde houve intervenção
   - Medir se ações tiveram impacto

2. **Close the Loop**
   - Comunicar resultados do follow-up para a organização
   - Reconhecer melhorias
   - Ser transparente sobre o que ainda precisa melhorar
   - Registrar aprendizados

3. **Alimentar Próximo Ciclo**
   - Lessons learned → `data/registries/lessons-learned.yaml`
   - Org health data → `data/registries/org-health-registry.yaml`
   - Ajustar survey se necessário

---

## Quality Gates

### Gate 1: Survey Quality
- [ ] Response rate > 70%
- [ ] Survey completado em < 10 minutos
- [ ] Anonimato garantido e comunicado
- [ ] Dados quantitativos e qualitativos coletados

### Gate 2: Analysis Quality
- [ ] Todas as dimensões analisadas
- [ ] Trends comparadas com período anterior
- [ ] Hotspots identificados com root cause hypothesis
- [ ] Breakdown por equipe (respeitando anonimato)

### Gate 3: Action Plan Quality
- [ ] Cada hotspot tem ação definida
- [ ] Cada ação tem DRI e deadline
- [ ] Budget confirmado para ações que precisam
- [ ] Vision Chief validou alinhamento com valores

### Gate 4: Execution Quality
- [ ] Ações implementadas dentro do prazo
- [ ] Follow-up measurement planejado
- [ ] Aprendizados registrados
- [ ] `checklists/ralphloop-quality.md` — PASS ✅

---

## Outputs

| Output | Template | Destino |
|--------|----------|---------|
| Culture Health Report | (custom) | Vision Chief, COO |
| Action Plan | (custom) | DRIs, managers |
| Org Health Dashboard | `data/registries/org-health-registry.yaml` | QBR, Board |
| Lessons Learned | `data/registries/lessons-learned.yaml` | All agents |

---

## Registries Atualizados

| Registry | Quando Atualizar |
|----------|-----------------|
| `data/registries/org-health-registry.yaml` | Cada survey cycle |
| `data/registries/lessons-learned.yaml` | Cada cycle de aprendizado |
| `data/registries/decision-registry.yaml` | Decisões de intervenção cultural |

---

## Métricas do Workflow

| Métrica | Target |
|---------|--------|
| Survey response rate | > 70% |
| eNPS | > 30 |
| Voluntary turnover | < 15% anual |
| Engagement score | > 7.5/10 |
| Psychological safety score | > 7/10 |
| Action plan completion rate | > 80% |
| Time to act on critical issue | < 2 semanas |

---

## Referências Cruzadas

### Frameworks
- `frameworks/operating-system/wbr-mbr-qbr.md` — Cadências de revisão
- `frameworks/operating-system/rasi-dri.md` — Ownership de ações

### Checklists
- `checklists/coo/coo-execution-rhythm-audit.md` — Ritmo de execução
- `checklists/ralphloop-quality.md` — Loop de aprendizado

### Templates
- `templates/coo/operating-review-template.md` — Review operacional

### Workflows Relacionados
- `workflows/06-qbr-loop.md` — QBR inclui org health review
- `workflows/09-org-design-workflow.md` — Redesenho organizacional
- `workflows/10-30-60-90-onboarding.md` — Onboarding e cultura
- `workflows/20-postmortem-and-learning.md` — Postmortem de incidentes culturais
