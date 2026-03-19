# Workflow 18 — Decision Quality Review

> **Revisar sistematicamente a qualidade das decisões tomadas, medir outcomes vs expectations, e alimentar o loop de aprendizado organizacional.**
> Decisões não revisadas são decisões das quais não se aprende.

---

## Objetivo

Estabelecer um processo recorrente de revisão da qualidade das decisões tomadas pelo C-Level Squad. O workflow garante que:

1. **Decisões são rastreadas** — toda decisão significativa é registrada com expected outcome
2. **Outcomes são medidos** — após período adequado, resultado real é comparado com esperado
3. **Padrões são identificados** — vieses, gaps de informação, falhas de processo recorrentes
4. **Processos são ajustados** — o sistema de decisão melhora com cada ciclo
5. **Aprendizados são distribuídos** — toda a organização se beneficia

> **Princípio:** A qualidade do sistema de decisão é mais importante que qualquer decisão individual. Melhorar o sistema melhora todas as decisões futuras.

---

## Agentes Envolvidos

| Agente | Papel no Workflow |
|--------|-------------------|
| **Vision Chief (CEO)** | Lead — decisões Type 1 (irreversíveis), pattern recognition estratégica |
| **COO Orchestrator** | Lead — decisões Type 2 (reversíveis), operational pattern recognition |
| **CMO Architect** | Support — decisões de mercado, positioning, growth |
| **CTO Architect** | Support — decisões técnicas, arquiteturais, platform |
| **CIO Engineer** | Support — decisões de sistemas, dados, infraestrutura |
| **CAIO Architect** | Support — decisões de IA, modelos, governance |
| **CFO Strategist** | Support — decisões financeiras, investment, allocation |
| **Squad Coordinator** | Logística — data collection, scheduling, report compilation |

---

## Trigger (quando iniciar)

### Triggers Periódicos
- Cadência mensal: review de decisões dos últimos 30 dias
- Cadência trimestral: deep review integrado ao QBR
- Cadência anual: revisão completa do sistema de decisão

### Triggers por Evento
- Postmortem de decisão que falhou significativamente
- Request do board para análise de decisão específica
- Padrão de decisões ruins identificado (3+ misses consecutivos)
- Novo agente/líder que precisa calibrar decision-making

---

## Pré-condições

- [ ] Decision registry ativo (`data/registries/decision-registry.yaml`)
- [ ] Decision memo framework em uso (`frameworks/operating-system/decision-memo-framework.md`)
- [ ] Período mínimo de 30 dias desde as decisões a serem revisadas
- [ ] Outcome data disponível (métricas, results, feedback)

---

## Processo (step-by-step)

### Stage 1: Decision Inventory (1 dia)

**Owner**: Squad Coordinator

1. **Extrair Decisões do Período**
   - Query `data/registries/decision-registry.yaml` para período de revisão
   - Filtrar por status: `implemented` ou `in_progress`
   - Classificar por tipo: Type 1 vs Type 2
   - Classificar por domínio: strategy, operations, tech, finance, etc.

2. **Selecionar para Review**
   - Todas as decisões Type 1 são obrigatórias
   - Decisões Type 2 com impacto > threshold
   - Decisões que geraram controvérsia ou dúvida
   - Amostra aleatória de decisões Type 2 rotineiras (10-20%)

3. **Preparar Dossier**
   - Para cada decisão: memo original, contexto, expected outcome, timeline
   - Compilar em formato de review
   - Distribuir para agentes reviewers

### Stage 2: Outcome Measurement (2-3 dias)

**Owner**: Cada agente (decisões do seu domínio)

1. **Coletar Outcome Data**
   - Resultado real vs resultado esperado
   - Métricas quantitativas (receita, custo, performance, etc.)
   - Feedback qualitativo (stakeholders, equipes, clientes)
   - Timeline: entregou no prazo?

2. **Classificar Outcome**
   ```
   ┌──────────────────────────────────────────────┐
   │          OUTCOME CLASSIFICATION               │
   ├──────────┬─────────────────────────────────────┤
   │  HIT     │ Resultado ≥ 80% do esperado         │
   │  PARTIAL │ Resultado 40-79% do esperado         │
   │  MISS    │ Resultado < 40% do esperado          │
   │  PIVOT   │ Direção mudou (decisão foi revertida)│
   │  TBD     │ Muito cedo para avaliar              │
   └──────────┴─────────────────────────────────────┘
   ```

3. **Documentar Evidence**
   - Para cada classificação, evidência que suporta
   - Fontes de dados utilizadas
   - Caveats e limitações da medição

### Stage 3: Gap Analysis (1-2 dias)

**Owner**: Vision Chief (Type 1) / COO (Type 2)

1. **Para Cada MISS ou PIVOT**
   - O que sabíamos no momento da decisão?
   - O que NÃO sabíamos?
   - O que deveríamos ter sabido? (information gap)
   - O processo de decisão foi seguido? (process gap)
   - Houve viés que influenciou? (bias gap)

2. **Análise de Informação**
   - A informação estava disponível e não foi considerada?
   - A informação não existia (uncertainty legítima)?
   - A informação foi mal interpretada?

3. **Análise de Processo**
   - O decision memo foi preparado corretamente?
   - Os stakeholders certos foram consultados?
   - Houve tempo suficiente para deliberação?
   - Alternativas foram genuinamente consideradas?

4. **Análise de Viés**
   - Confirmation bias: buscou-se apenas informação que confirmava?
   - Anchoring: primeira informação dominou?
   - Sunk cost: custos passados influenciaram?
   - Authority bias: decisão foi aceita sem questionamento?
   - Groupthink: houve dissent genuíno?

### Stage 4: Root Cause Analysis (1 dia)

**Owner**: Vision Chief + COO

1. **Para Misses Significativos**
   - Aplicar 5 Whys
   - Identificar root cause: information, process, people, timing, external
   - Distinguir entre: erro evitável vs incerteza legítima

2. **Categorizar Root Causes**
   | Categoria | Exemplo | Ação |
   |-----------|---------|------|
   | Information gap | Não sabíamos que competidor lançaria feature | Melhorar intel |
   | Process gap | Memo não incluiu analysis de riscos | Fortalecer checklist |
   | Bias | Sunk cost influenciou decisão de continuar | Treinar awareness |
   | Timing | Decidimos rápido demais/devagar demais | Ajustar timebox |
   | External | Mudança de mercado imprevisível | Cenários mais amplos |
   | Execution | Decisão correta, execução falhou | Separar de decision quality |

### Stage 5: Pattern Recognition (1 dia)

**Owner**: Vision Chief + COO

1. **Cross-Decision Patterns**
   - Há domínios com mais misses? (ex: tech decisions > market decisions)
   - Há agentes com mais misses? (calibração necessária)
   - Há tipos de decisão com mais misses? (Type 1 vs Type 2)
   - Há vieses recorrentes?

2. **Trend Analysis**
   - Decision quality está melhorando, estável, ou piorando?
   - Comparar hit rate: este mês vs últimos 3 meses vs últimos 6 meses
   - Comparar por domínio e por agente

3. **Benchmark**
   - Taxa de acerto esperada: > 70% para Type 2, > 50% para Type 1
   - Se abaixo: problema sistêmico que requer intervenção
   - Se acima: sistema funcionando, otimizar marginalmente

### Stage 6: Process Improvement (1-2 dias)

**Owner**: COO Orchestrator

1. **Para Cada Root Cause Recorrente**
   - Definir melhoria de processo específica
   - Exemplos:
     - Se information gap → adicionar data check ao decision memo
     - Se bias recorrente → adicionar devil's advocate ao processo
     - Se timing → ajustar timebox por tipo de decisão
     - Se process gap → fortalecer checklist

2. **Implementar Melhorias**
   - Atualizar `checklists/exec-decision-memo-quality.md` se necessário
   - Atualizar `frameworks/operating-system/decision-memo-framework.md` se necessário
   - Comunicar mudanças a todos os agentes

3. **Testar Melhorias**
   - Aplicar nas próximas decisões
   - Medir impacto no próximo ciclo de review

### Stage 7: Knowledge Update (1 dia)

**Owner**: Squad Coordinator

1. **Registrar Aprendizados**
   - Atualizar `data/registries/lessons-learned.yaml`
   - Para cada lesson: contexto, aprendizado, ação, DRI
   - Categorizar: decision-making, strategy, operations, tech, etc.

2. **Atualizar Decision Registry**
   - `data/registries/decision-registry.yaml`
   - Adicionar outcome classification para cada decisão revisada
   - Adicionar root cause para misses
   - Adicionar lessons linked

3. **Distribuir Aprendizados**
   - Summary de top 3 lessons para todos os agentes
   - Deep dive para domínio específico se pattern significativo
   - Feed para WBR/MBR/QBR conforme relevância

### Stage 8: Report (1 dia)

**Owner**: Vision Chief + Squad Coordinator

1. **Monthly Decision Quality Report**
   - Decisões revisadas: N total, N Type 1, N Type 2
   - Hit rate: overall, by type, by domain
   - Top misses e root causes
   - Process improvements implementados
   - Trend vs meses anteriores

2. **Quarterly Deep Report (para QBR)**
   - Análise de 3 meses de decisões
   - Pattern analysis
   - System-level recommendations
   - Decision quality score trend

3. **Annual Decision System Review**
   - Revisão completa do sistema de decisão
   - Efetividade dos process improvements
   - Benchmark contra melhores práticas
   - Recommendations para próximo ano

---

## Quality Gates

### Gate 1: Inventory Quality
- [ ] Todas as decisões Type 1 incluídas
- [ ] Amostra adequada de Type 2
- [ ] Dossier preparado com memos originais

### Gate 2: Outcome Measurement
- [ ] Outcome data coletado para cada decisão
- [ ] Classification aplicada (HIT/PARTIAL/MISS/PIVOT/TBD)
- [ ] Evidence documentada

### Gate 3: Analysis Quality
- [ ] Root cause analysis para todos os misses
- [ ] Pattern recognition cross-decision executada
- [ ] Vieses identificados e documentados

### Gate 4: Report Quality
- [ ] `checklists/ralphloop-quality.md` — PASS ✅
- [ ] Report completo com todos os campos
- [ ] Action items com DRI e deadline
- [ ] Trend analysis incluída

---

## Outputs

| Output | Template | Destino |
|--------|----------|---------|
| Decision Quality Report | (custom) | Vision Chief, COO, Board |
| Lessons Learned | `data/registries/lessons-learned.yaml` | All agents |
| Process Improvements | (inline) | Checklists, frameworks |
| Updated Decision Registry | `data/registries/decision-registry.yaml` | System of record |

---

## Registries Atualizados

| Registry | Quando Atualizar |
|----------|-----------------|
| `data/registries/decision-registry.yaml` | Outcome classification + root cause |
| `data/registries/lessons-learned.yaml` | Cada lesson extraída |
| `data/registries/okr-registry.yaml` | Se OKR afetado por decisão revisada |

---

## Métricas do Workflow

| Métrica | Target |
|---------|--------|
| Decision review completion rate | 100% Type 1, >80% Type 2 |
| Hit rate Type 1 | > 50% |
| Hit rate Type 2 | > 70% |
| Time from decision to outcome measurement | < 90 dias |
| Lessons learned per cycle | ≥ 3 |
| Process improvements implemented per quarter | ≥ 2 |

---

## Referências Cruzadas

### Frameworks
- `frameworks/operating-system/decision-memo-framework.md` — Como decisões são tomadas
- `frameworks/operating-system/wbr-mbr-qbr.md` — Cadências de revisão

### Checklists
- `checklists/exec-decision-memo-quality.md` — Quality gate de decisão
- `checklists/ralphloop-quality.md` — Quality gate de aprendizado

### Templates
- `templates/vision-chief/decision-memo-template.md` — Template de decisão

### Workflows Relacionados
- `workflows/06-qbr-loop.md` — QBR inclui decision quality review
- `workflows/20-postmortem-and-learning.md` — Postmortem de falhas
- `workflows/04-wbr-loop.md` — WBR pode surfar decision issues
