# Cross-Squad Collaboration Voice — Linguagem de Colaboração entre Squads

## Princípio Central

Colaboração cross-squad falha por comunicação, não por intenção. Handoffs claros,
SLAs explícitos, dependências declaradas e escalação definida são a base de
execução multi-team eficiente.

**Mantra: "Input claro, output definido, prazo combinado, escalação se necessário."**

---

## Os 4 Pilares da Comunicação Cross-Squad

### 1. Handoffs Claros
Todo handoff entre squads tem input, output, formato e prazo definidos.

- **Bom:** "Marketing entrega lista de 200 MQLs qualificados (com company name, contact, lead score > 70) no CRM até segunda 9h. Sales confirma recebimento e inicia outreach em < 4 horas."
- **Ruim:** "Marketing passa os leads para sales."

### 2. SLA Language
Todo acordo entre squads é um SLA com métrica, tempo e consequência.

- **Bom:** "Engenharia responde a bugs P1 em < 2 horas. Se não responde, escala para Engineering Manager automaticamente. Reportamos compliance semanal."
- **Ruim:** "Engenharia prioriza bugs urgentes."

### 3. Dependency Communication
Dependências são declaradas no início, não descobertas no final.

- **Bom:** "O lançamento de Q2 depende de: (1) API v2 de Engineering — ETA: 15 março, (2) Landing page de Design — ETA: 20 março, (3) Pricing approval de Finance — ETA: 10 março. Caminho crítico: API v2."
- **Ruim:** "Precisamos de algumas coisas de outros times para o lançamento."

### 4. Escalation Language
Quando SLAs são quebrados ou bloqueios aparecem, o caminho de escalação é claro.

- **Bom:** "Se a API v2 atrasa mais que 3 dias, escalo para CTO e COO na daily de terça. Se atrasa mais que 7 dias, o lançamento é revisado em reunião de C-Level."
- **Ruim:** "Se atrasar, a gente vê o que fazer."

---

## Estrutura de Handoff Cross-Squad

### Template de Handoff

```
HANDOFF: [Nome descritivo]
DE: [Squad/pessoa que entrega]
PARA: [Squad/pessoa que recebe]
INPUT: [O que é entregue — formato, qualidade, volume]
OUTPUT ESPERADO: [O que o receptor produz com esse input]
PRAZO DE ENTREGA: [Quando o input é entregue]
PRAZO DE PROCESSAMENTO: [Quanto tempo o receptor tem para processar]
SLA: [Métrica de qualidade e tempo]
ESCALAÇÃO: [O que acontece se o SLA é quebrado]
FEEDBACK LOOP: [Como o receptor comunica problemas com o input]
```

### Exemplo Completo

```
HANDOFF: MQL para Sales Outreach
DE: Marketing (Growth Squad)
PARA: Sales (Enterprise Squad)
INPUT: Lista de MQLs com lead score > 70, company name, contact info, engagement history
OUTPUT ESPERADO: First touch em < 4h, qualification call em < 48h
PRAZO DE ENTREGA: Segunda e quinta, 9h
PRAZO DE PROCESSAMENTO: 4h para first touch, 48h para qualification
SLA: 90% contacted em 4h, 80% qualified em 48h
ESCALAÇÃO: Se SLA < 80% por 2 semanas, reunião Marketing + Sales Directors
FEEDBACK LOOP: Sales reporta lead quality score semanal na quinta 16h
```

---

## SLA Framework Cross-Squad

### Como Definir SLAs

1. **Identifique o serviço:** O que um squad entrega para outro?
2. **Defina a métrica:** Como medimos qualidade e tempo?
3. **Estabeleça o target:** Qual é o nível aceitável?
4. **Defina a cadência de report:** Com que frequência reportamos compliance?
5. **Estabeleça a escalação:** O que acontece quando o target não é atingido?

### Exemplos de SLA Cross-Squad

| De → Para | Serviço | SLA | Report | Escalação |
|-----------|---------|-----|--------|-----------|
| Eng → Product | Bug fix P1 | < 4h response, < 24h fix | Diário | Engineering Manager |
| Eng → Product | Bug fix P2 | < 24h response, < 1 week fix | Semanal | Engineering Manager |
| Design → Eng | UI specs | 3 dias antes do sprint | Por sprint | Design Lead |
| Marketing → Sales | MQL delivery | 90% contacted em 4h | Semanal | Directors |
| Sales → CS | Customer handoff | Kick-off em < 48h pós-close | Semanal | VP Sales + VP CS |
| CS → Product | Feature request compile | Mensal, priorizado | Mensal | Product Lead |
| Data → All | Dashboard accuracy | 99.5% accuracy, < 1h delay | Semanal | Data Lead |
| Legal → All | Contract review | < 5 business days | Semanal | Legal Lead |

---

## Dependency Communication

### Dependency Map Template

```
PROJETO: [Nome do projeto]
LAUNCH DATE: [Data]
DEPENDENCIES:

1. [Squad/Team]: [Deliverable]
   Owner: [Nome]
   ETA: [Data]
   Status: [Green/Yellow/Red]
   If delayed: [Impacto no projeto + plano B]

2. [Squad/Team]: [Deliverable]
   Owner: [Nome]
   ETA: [Data]
   Status: [Green/Yellow/Red]
   If delayed: [Impacto no projeto + plano B]

CRITICAL PATH: [Qual dependência determina o prazo final]
BUFFER: [Quantos dias de buffer temos]
REVIEW CADENCE: [Quando revisamos status das dependências]
```

### Frases de Dependency Communication

| Situação | Frase |
|----------|-------|
| Declarar dependência | "Nosso deliverable depende de [X] do squad [Y]. Owner: [nome]. ETA: [data]. Sem isso, atrasamos [Z] dias." |
| Confirmar commitment | "[Nome], confirma que entrega [X] até [data]? Precisamos de commitment firme — é caminho crítico." |
| Early warning | "Risco de atraso na dependência [X]. Probabilidade: [%]. Impacto: [dias]. Plano B: [alternativa]." |
| Dependency at risk | "Dependência [X] está at risk. Não vamos receber [deliverable] até [nova data]. Opções: (A) atrasar launch, (B) reduzir scope, (C) [alternativa]." |
| Dependency missed | "Dependência [X] não foi entregue no prazo. Impacto no projeto: [Y]. Escalando para [nome]. Reunião amanhã às [hora]." |

---

## Escalation Language

### Níveis de Escalação

| Nível | Trigger | Para quem | Frase |
|-------|---------|-----------|-------|
| 1 — Informal | Atraso < 2 dias | Peer-to-peer | "Ei [nome], o deliverable era para [data]. Está vindo? Preciso para [motivo]." |
| 2 — Formal | SLA quebrado 1x | Leads/Managers | "[Serviço] SLA quebrado: esperado [X], realizado [Y]. Impacto: [Z]. Solicitamos review." |
| 3 — Director | SLA quebrado 2+ vezes | Directors | "SLA de [serviço] quebrado [N] vezes em [período]. Impacto acumulado: [Y]. Precisamos de intervenção." |
| 4 — VP/C-Level | Impacto em projeto estratégico | VP/C-Level | "Blocker cross-squad impactando [projeto estratégico]. Impacto: [quantificado]. Solicitamos arbitragem." |

### Regras de Escalação

1. **Escale cedo, não tarde.** Escalar não é falha — é responsabilidade.
2. **Escale com dados.** "SLA quebrado 3 vezes" é escalação. "Eles não colaboram" não é.
3. **Escale o problema, não a pessoa.** Foco no serviço e no impacto.
4. **Escale com proposta.** "O problema é X. Minha sugestão é Y. Preciso de Z."
5. **Não skip levels.** Nível 1 → 2 → 3 → 4. Pular níveis só em emergência.

---

## Reuniões Cross-Squad

### Sync Semanal Cross-Squad (30 min)

```
[0-5 min] Abertura: "Objetivo: alinhar handoffs, resolver blockers, confirmar SLAs."
[5-20 min] Por squad: status de commitments + blockers
[20-27 min] Ações e decisões
[27-30 min] Fechamento: "Próximos deliverables confirmados? Blockers resolvidos?"
```

### Frases para Reuniões Cross-Squad

- "Qual é o status do que foi commitado para esta semana?"
- "Algum handoff atrasado ou em risco?"
- "Quem precisa de quem para destravar?"
- "Vamos confirmar os deliverables da próxima semana. [Squad A]: [deliverable]. [Squad B]: [deliverable]."

---

## Templates de Comunicação Cross-Squad

### Request para Outro Squad
```
PARA: [Squad/pessoa]
REQUEST: [O que preciso — específico]
CONTEXTO: [Por que preciso — impacto se não receber]
INPUT QUE FORNEÇO: [O que entrego para facilitar]
PRAZO: [Quando preciso]
PRIORIDADE: [Alta/Média/Baixa — com justificativa]
ALTERNATIVA: [O que faço se não for possível no prazo]
```

### Status de Collaboration
```
PROJETO: [Nome]
SQUADS ENVOLVIDOS: [Lista]
STATUS GERAL: [Green/Yellow/Red]
HANDOFFS ON TRACK: [Lista]
HANDOFFS AT RISK: [Lista com motivo e ação]
BLOCKERS: [Lista com owner de resolução]
PRÓXIMA SYNC: [Data/hora]
```

---

## Anti-Padrões Cross-Squad

### Assumir Prioridade
- **Evitar:** "Isso é urgente, preciso para amanhã." (sem contexto do impacto no outro squad)
- **Preferir:** "Isso impacta o lançamento de Q2. Qual é a capacidade do seu time? Podemos negociar prazo?"

### Blame Cross-Squad
- **Evitar:** "Engenharia atrasou, por isso não entregamos."
- **Preferir:** "A dependência de API atrasou 5 dias. Estamos ajustando o timeline. Novo ETA: [data]."

### Comunicação Apenas em Crise
- **Evitar:** Só falar com outro squad quando há problema.
- **Preferir:** Cadência regular de sync, mesmo quando está tudo on track.

---

## Checklist de Colaboração Cross-Squad

- [ ] Handoffs documentados com input, output, prazo?
- [ ] SLAs definidos e aceitos por ambos os squads?
- [ ] Dependências mapeadas com owners e ETAs?
- [ ] Caminho de escalação definido e conhecido?
- [ ] Cadência de sync estabelecida?
- [ ] Feedback loop ativo entre os squads?
- [ ] Status reportado em formato consistente?
- [ ] Blockers comunicados proativamente (não reativamente)?
