# Escalation Ladders — Escadas de Escalação Multi-Nível

> **Domínio:** Operating System
> **Autor de referência:** ITIL (escalation management), Amazon (Andon cord), práticas de incident management
> **Uso primário:** Garantir que problemas cheguem à pessoa certa, no tempo certo, com a informação certa.
> **Agente responsável:** coo-orchestrator

---

## Origem e Contexto

Escalation Ladders são estruturas que definem quando, como e para quem escalar problemas, decisões ou bloqueios. O conceito vem de múltiplas fontes: ITIL (IT Service Management), cultura militar (chain of command), e práticas de manufacturing lean (Andon cord da Toyota).

O problema que Escalation Ladders resolvem: **em organizações sem regras claras de escalação, duas coisas acontecem:**
1. **Problemas escalam tarde demais** — quando já são crises. O líder descobre na WBR que o problema existe há 3 semanas.
2. **Problemas escalam cedo demais** — tudo vai para o CEO. O líder gasta 80% do tempo resolvendo problemas que deveriam ser resolvidos pelo nível abaixo.

A solução é uma escada com critérios objetivos: baseada em **tempo** (quanto tempo sem resolução), **severidade** (impacto no negócio), e **autoridade** (quem tem poder de decisão para resolver).

O equivalente moderno do Andon cord da Toyota: qualquer pessoa pode puxar a corda (escalar), mas há regras claras sobre quando puxar e o que acontece depois.

---

## Quando Usar

- Em TODA operação com mais de 10 pessoas — sem escalação formal, problemas se perdem.
- Quando há reclamações de que "o líder não sabia do problema" ou "demorou para chegar no nível certo."
- Em operações 24/7 ou com SLA rígido — incident management requer escalação automática.
- Quando decisões ficam presas por falta de autoridade no nível atual.
- Em cross-squad handoffs — quando o problema cruza fronteiras de responsabilidade.
- Para criar cultura de "escalar não é fraqueza, é responsabilidade."

---

## Quando NÃO Usar

- Para bypass político — usar escalação para "pular" o gestor direto é disfunção, não processo.
- Quando o problema está dentro da autoridade do DRI — resolver primeiro, escalar depois se necessário.
- Como mecanismo de blame — "eu escalei, agora não é mais meu problema." Escalar não transfere ownership.
- Em situações triviais — escalar que o café acabou na copa não é bom uso do sistema.

---

## Estrutura / Modelo

### 1. Escalação por Tempo (Timeline-Based)

```
┌─────────────────────────────────────────────────────────────────────┐
│              ESCALATION LADDER — TIMELINE-BASED                      │
├──────────┬──────────────────────┬───────────────────────────────────┤
│ Tempo    │ Nível de Escalação   │ Ação Esperada                     │
├──────────┼──────────────────────┼───────────────────────────────────┤
│ 0-2h     │ DRI / IC             │ Investigar, mitigar, resolver     │
│ 2-4h     │ Tech Lead / Manager  │ Alocar recursos, priorizar       │
│ 4-8h     │ Director / Head      │ Decisão de trade-off, comunicação│
│ 8-24h    │ VP / C-Level         │ Mobilizar cross-squad, decidir   │
│ 24h+     │ CEO / Vision Chief   │ War room, comunicação executiva  │
└──────────┴──────────────────────┴───────────────────────────────────┘
```

### 2. Escalação por Severidade (Severity-Based)

```
┌─────────────────────────────────────────────────────────────────────┐
│              ESCALATION LADDER — SEVERITY-BASED                      │
├──────┬──────────────────────────┬───────────────────┬───────────────┤
│ Sev  │ Definição                │ Resposta Inicial  │ Escala Para   │
├──────┼──────────────────────────┼───────────────────┼───────────────┤
│ SEV1 │ Impacto total no negócio │ Imediata (< 15min)│ C-Level       │
│      │ (sistema down, breach,   │ War room ativado  │               │
│      │  perda financeira ativa) │                   │               │
├──────┼──────────────────────────┼───────────────────┼───────────────┤
│ SEV2 │ Impacto parcial          │ < 30 min          │ Director/Head │
│      │ (funcionalidade crítica  │ DRI designado     │               │
│      │  degradada, SLA breach)  │                   │               │
├──────┼──────────────────────────┼───────────────────┼───────────────┤
│ SEV3 │ Impacto limitado         │ < 2h              │ Manager       │
│      │ (workaround disponível,  │ Ticket criado     │               │
│      │  experiência degradada)  │                   │               │
├──────┼──────────────────────────┼───────────────────┼───────────────┤
│ SEV4 │ Impacto mínimo           │ Próximo sprint    │ Tech Lead     │
│      │ (cosmético, edge case)   │ Backlog           │               │
└──────┴──────────────────────────┴───────────────────┴───────────────┘
```

### 3. Escalação por Autoridade (Decision-Based)

```
┌─────────────────────────────────────────────────────────────────────┐
│              ESCALATION LADDER — AUTHORITY-BASED                     │
├──────────────────────┬──────────────────────────────────────────────┤
│ Decisão              │ Autoridade para Decidir                      │
├──────────────────────┼──────────────────────────────────────────────┤
│ < R$ 10K, reversível │ IC / Manager (não precisa escalar)          │
│ R$ 10K-50K           │ Director / Head                              │
│ R$ 50K-200K          │ VP / C-Level do domínio                     │
│ > R$ 200K            │ Vision Chief (com memo de decisão)          │
│ Contratação/demissão │ Hiring manager + skip-level approval        │
│ Mudança de roadmap   │ CTO (tech) / CMO (growth) + Vision Chief   │
│ Compromisso com      │ Vision Chief + C-Level do domínio           │
│ cliente enterprise   │                                              │
│ Kill de iniciativa   │ DRI da iniciativa + 1 nível acima           │
└──────────────────────┴──────────────────────────────────────────────┘
```

---

## Processo de Aplicação (step-by-step)

### Step 1: Mapear os Tipos de Escalação Relevantes
Identificar quais dos 3 tipos (tempo, severidade, autoridade) são mais relevantes para sua operação. A maioria das empresas precisa dos 3, mas com pesos diferentes:
- **Tech-heavy:** Severidade + Tempo (incident management).
- **Operations-heavy:** Autoridade + Tempo (decisão e bloqueios).
- **Customer-facing:** Severidade + Autoridade (impacto no cliente).

### Step 2: Definir Níveis e Critérios
Para cada tipo, definir:
- **Quantos níveis?** (geralmente 4-5, não mais)
- **Qual o critério objetivo para cada nível?** (tempo, impacto financeiro, # usuários afetados)
- **Quem é o ponto focal em cada nível?** (pessoa, não departamento)

### Step 3: Definir o Formato de Escalação
Quando alguém escala, o que deve comunicar? Padronizar:
- **O que aconteceu?** (fato, não interpretação)
- **Qual o impacto atual?** (quantificado)
- **O que já foi feito?** (ações tomadas)
- **O que precisa do próximo nível?** (decisão, recurso, aprovação)

### Step 4: Definir Canais
Como a escalação acontece na prática:
- SEV1: Telefone + canal de emergência (não Slack — Slack é assíncrono demais).
- SEV2-3: Canal de Slack dedicado + menção ao DRI.
- Authority: Memo + conversa 1:1 ou thread assíncrona.
- Nunca: email para escalação urgente.

### Step 5: Treinar e Simular
Documentar é necessário mas insuficiente. Treinar:
- Tabletop exercises: simular cenários e praticar escalação.
- Game days: simular incidentes reais em ambiente controlado.
- Retrospectivas: após cada escalação real, revisar se o processo funcionou.

### Step 6: Integrar na Cadência WBR
Na WBR, incluir:
- Quantas escalações aconteceram na semana?
- Foram resolvidas no nível adequado?
- Alguma deveria ter escalado mais rápido?
- Alguma não deveria ter escalado?

---

## Exemplos Práticos

### Exemplo 1: Incidente de Performance (SEV2)

**12:15** — Alerta de latência > 2s no checkout. DRI de plantão investiga.
**12:30** — Root-cause identificado: query N+1 no novo deploy. Rollback iniciado.
**12:45** — Rollback completo. Latência normalizada. Escalação para Tech Lead: "rollback feito, preciso que avalie se o fix pode ir pro próximo deploy."
**13:00** — Tech Lead revisa, aprova fix, planeja redeploy para amanhã.
**13:15** — COO informado via canal de incidents. Nenhuma escalação adicional necessária.

### Exemplo 2: Bloqueio de Decisão (Authority-Based)

**Situação:** CMO quer investir R$ 150K em patrocínio de evento, mas CTO argumenta que o budget deveria ir para infra de analytics.
**Nível 1:** CMO e CTO não chegam a acordo em 48h.
**Escalação:** Ambos escrevem memo de 1 página com argumentos. Memo vai para Vision Chief na próxima MBR.
**Decisão:** Vision Chief avalia trade-offs, decide alocar R$ 100K para evento e R$ 50K para analytics. Documenta em `data/decisions/`.

### Exemplo 3: Quando NÃO Escalar

**Situação:** Developer encontra bug de UI em produção. Workaround existe. Impacto: 2% dos usuários em cenário edge-case.
**Classificação:** SEV4. Não escalar — adicionar ao backlog do próximo sprint. Tech Lead prioriza.

---

## Armadilhas Comuns

1. **Escalar tudo:** Se tudo é urgente, nada é urgente. Critérios claros de severidade previnem escalação inflacionária.
2. **Não escalar por medo:** Cultura de "resolver sozinho" que esconde problemas. Escalar não é fraqueza. Não escalar um SEV1 é negligência.
3. **Escalar sem informação:** "Temos um problema" sem dados é inútil para quem recebe. Formato padronizado resolve.
4. **Escalação como transferência:** "Escalei, não é mais meu problema." Escalar é pedir ajuda, não abandonar. O DRI original continua envolvido.
5. **Muitos níveis:** Mais de 5 níveis cria burocracia. 4 níveis são suficientes para a maioria das organizações.
6. **Canais errados:** Escalar SEV1 por email às 22h é garantia de resposta lenta. Canal deve ser proporcional à urgência.
7. **Não treinar:** Documentar a ladder sem treinar o time é como ter extintor sem ninguém saber usar.
8. **Não fazer retrospectiva:** Após cada escalação significativa, revisar o processo. O que funcionou? O que não funcionou?

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/operating-system/wbr-mbr-qbr.md` | WBR é o fórum padrão de escalação operacional. Escalações da semana são revisadas. |
| `frameworks/operating-system/rasi-dri.md` | A escalação segue a cadeia de DRIs. Se o DRI do nível 1 não resolve, escala para o DRI do nível 2. |
| `frameworks/operating-system/decision-memo-framework.md` | Escalações de autoridade usam memo simplificado para apresentar o trade-off ao decisor. |
| `frameworks/engineering-tech/sre-basics.md` | Incident management (SRE) usa a ladder de severidade para classificar e escalar. |
| `frameworks/it-information/itil-light.md` | ITIL define processos de escalação funcional e hierárquica que complementam esta ladder. |
| `checklists/incident-communication-quality.md` | Checklist de comunicação durante escalações de incident. |
| `checklists/risk-register-quality.md` | Riscos com probabilidade alta devem ter planos de escalação pré-definidos. |

---

## Referências

- Axelos. *ITIL Foundation: ITIL 4 Edition*. (Escalation management em service management.)
- Liker, J. (2004). *The Toyota Way*. McGraw-Hill. (Andon cord e cultura de parar para resolver.)
- Bryar, C. & Carr, B. (2021). *Working Backwards*. (Escalation e ownership na Amazon.)
- Google SRE. *Site Reliability Engineering: How Google Runs Production Systems*. (Incident severity e escalation.)
- C-Level Squad `config.yaml` — Princípio: "Cadência é o sistema operacional."
