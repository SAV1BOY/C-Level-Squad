# Decision Memo Framework — Memo de Decisão (Estilo Bezos 6-Pager)

> **Domínio:** Operating System
> **Autor de referência:** Jeff Bezos / Amazon — "Working Backwards"
> **Uso primário:** Estruturar decisões complexas com clareza, evidência e accountability.
> **Agente responsável:** coo-orchestrator / vision-chief

---

## Origem e Contexto

O Decision Memo é um formato de documento narrativo popularizado por Jeff Bezos na Amazon. Em 2004, Bezos baniu PowerPoints das reuniões executivas e os substituiu por memos narrativos de até 6 páginas. A razão: slides escondem pensamento raso atrás de bullet points bonitos. Prosa narrativa exige raciocínio completo — frases com sujeito, verbo e predicado forçam clareza.

O insight fundamental: **a qualidade de uma decisão é diretamente proporcional à qualidade do pensamento que a precede, e prosa narrativa é o melhor veículo para pensamento rigoroso.**

O C-Level Squad classifica decisões em dois tipos (framework de Bezos):

- **Type 1 (Irreversíveis):** Decisões de alta consequência e difícil reversão. Exemplos: M&A, pivots estratégicos, corte de produto. Requerem memo completo, múltiplas revisões, aprovação do vision-chief.
- **Type 2 (Reversíveis):** Decisões de impacto moderado e fácil reversão. Exemplos: teste de canal, mudança de pricing de um tier, nova feature. Memo simplificado ou estrutura rápida. Delegáveis.

O erro mais comum é tratar decisões Type 2 como Type 1 (paralisia) ou Type 1 como Type 2 (imprudência).

---

## Quando Usar

- Toda decisão Type 1 (irreversível, alto impacto) OBRIGATORIAMENTE requer memo.
- Decisões Type 2 com investimento > R$ 100K ou impacto cross-squad.
- Quando há discordância significativa entre líderes — o memo força articulação dos argumentos.
- Para documentar o raciocínio por trás de decisões para consulta futura (decision registry em `data/decisions/`).
- Em MBR/QBR quando decisões estratégicas precisam ser tomadas.

---

## Quando NÃO Usar

- Para decisões Type 2 simples (< R$ 50K, escopo individual, facilmente reversível). Use uma thread no Slack + DRI.
- Para reportar status — memo é para DECIDIR, não para informar. Status vai na WBR.
- Quando a decisão já foi tomada e o memo é apenas formalidade — nesse caso, é registro, não ferramenta de decisão.
- Para evitar tomar decisão — "preciso escrever um memo" não é desculpa para procrastinar.

---

## Estrutura / Modelo

### Memo Completo (Type 1 — 4-6 páginas)

```
┌─────────────────────────────────────────────────────────────────────┐
│                      DECISION MEMO                                   │
├─────────────────────────────────────────────────────────────────────┤
│ Título: [Decisão em questão]                                        │
│ Autor: [Nome]          Data: [YYYY-MM-DD]                           │
│ Tipo: Type 1 / Type 2  DRI: [Nome do decisor final]                │
│ Status: Draft / Review / Approved / Rejected                        │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│ 1. CONTEXTO E PROBLEMA (1 página)                                   │
│    - Qual é o problema ou oportunidade?                              │
│    - Por que agora? O que muda se não decidirmos?                   │
│    - Dados e evidências relevantes.                                  │
│                                                                      │
│ 2. OPÇÕES CONSIDERADAS (1-2 páginas)                                │
│    - Opção A: [descrição, prós, contras, riscos, custo]             │
│    - Opção B: [descrição, prós, contras, riscos, custo]             │
│    - Opção C: [descrição, prós, contras, riscos, custo]             │
│    - Opção D: Não fazer nada (sempre incluir)                       │
│                                                                      │
│ 3. RECOMENDAÇÃO (0.5-1 página)                                      │
│    - Qual opção o autor recomenda e POR QUÊ?                        │
│    - Trade-offs aceitos explicitamente.                              │
│    - Premissas que precisam ser verdadeiras.                         │
│    - Kill criteria: quando reverter/parar.                           │
│                                                                      │
│ 4. PLANO DE EXECUÇÃO (0.5-1 página)                                │
│    - Próximos passos com DRI, deadline e DoD.                       │
│    - Milestones e checkpoints.                                       │
│    - Dependências e riscos de execução.                              │
│                                                                      │
│ 5. APÊNDICES (opcional)                                              │
│    - Dados brutos, análises financeiras, pesquisas.                 │
│    - FAQs antecipadas.                                               │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

### Memo Simplificado (Type 2 — 1-2 páginas)

Para decisões reversíveis de médio impacto:

```
Título: [Decisão]
DRI: [Nome]
Contexto: [2-3 parágrafos]
Opções: [A vs B, prós/contras resumidos]
Recomendação: [1 parágrafo]
Próximos passos: [bullets com DRI e deadline]
Kill criteria: [quando reverter]
```

---

## Processo de Aplicação (step-by-step)

### Step 1: Classificar a Decisão (Type 1 ou Type 2)
Perguntar:
- É facilmente reversível? → Type 2 (delegar, decidir rápido)
- Tem consequências de longo prazo difíceis de desfazer? → Type 1 (memo completo)
- Na dúvida, tratar como Type 2 — a maioria das decisões é reversível.

### Step 2: Escrever o Memo
O autor (geralmente quem propõe) escreve o memo. Regras de escrita:
- **Prosa narrativa**, não bullet points. Frases completas com argumentação.
- **Dados e evidências** — "achamos" não é argumento. "Os dados mostram que..." é.
- **Incluir a opção de não fazer nada** — sempre. Muitas vezes é a melhor opção.
- **Ser honesto sobre trade-offs** — todo caminho tem custo. Quem esconde trade-offs está vendendo, não decidindo.

### Step 3: Revisar (Pre-Read)
Enviar o memo 24-48h antes da reunião de decisão. Participantes leem antes.

### Step 4: Reunião de Decisão
Formato Amazon:
1. **[20 min] Leitura silenciosa** — mesmo com pre-read, reler na hora garante que todos estão na mesma página.
2. **[30 min] Perguntas e discussão** — começar pelos mais juniores (para não serem influenciados pelos seniors).
3. **[10 min] Decisão** — O DRI decide. Pode ser: aprovar, rejeitar, pedir mais dados, ou "disagree and commit."

### Step 5: Documentar e Registrar
Após decisão:
- Atualizar status do memo (Approved/Rejected).
- Registrar em `data/decisions/` com metadata (data, DRI, rationale, kill criteria).
- Comunicar a decisão aos "I" (Informed) da matriz RASI.

### Step 6: Acompanhar Kill Criteria
No prazo definido, revisar se os kill criteria foram atingidos. Se sim, reverter/parar. Se não, continuar. Incluir na cadência WBR/MBR.

---

## Exemplos Práticos

### Exemplo 1: Type 1 — Aquisição de Startup

**Título:** Aquisição da StartupX para acelerar módulo de AI
**DRI:** Vision Chief
**Tipo:** Type 1

**Contexto:** StartupX tem tecnologia de NLP aplicada a documentos financeiros com 50 clientes enterprise. Nosso roadmap de AI precisa de 18 meses para chegar ao mesmo nível. Valuation pedido: R$ 15M. Nosso runway atual: 24 meses.

**Opções:**
- A: Adquirir StartupX por R$ 15M (70% cash + 30% equity)
- B: Acqui-hire do time técnico (5 engenheiros) por R$ 5M
- C: Build interno com contratação de 3 specialists + 18 meses
- D: Não fazer nada e focar no core product

**Recomendação:** Opção B (acqui-hire). Premissa: o valor principal está no time, não na base de clientes. Kill criteria: se < 3 dos 5 engenheiros aceitarem, abortar.

### Exemplo 2: Type 2 — Novo Canal de Aquisição

**Título:** Testar LinkedIn Ads como canal de aquisição B2B
**DRI:** CMO
**Contexto:** CAC via Google Ads subiu 30% nos últimos 2 trimestres. LinkedIn tem CPL historicamente mais alto mas melhor fit com ICP enterprise.
**Recomendação:** Investir R$ 30K em teste de 60 dias. Kill criteria: se CPL > 3x Google sem melhoria em SQL quality, encerrar.

---

## Armadilhas Comuns

1. **Memo como justificativa:** Escrever o memo para justificar decisão já tomada, em vez de explorar opções genuinamente. Se a conclusão vem antes da análise, é propaganda, não decisão.
2. **Paralisia por memo:** Exigir memo completo para toda decisão. Type 2 decisions devem ser rápidas. "Two-way door" = decide e ajusta.
3. **Memo sem dados:** Narrativa brilhante sem evidência é ficção. Todo argumento precisa de suporte factual.
4. **Não incluir "não fazer nada":** A opção de não agir é sempre válida e frequentemente subestimada. Inação é uma decisão.
5. **HiPPO effect:** A pessoa mais sênior fala primeiro e todos concordam. Juniors devem opinar primeiro.
6. **Memo sem kill criteria:** Sem critérios de quando parar/reverter, a decisão não tem safeguard. Kill criteria são obrigatórios.
7. **Não registrar a decisão:** Memo aprovado que não vai para `data/decisions/` é conhecimento perdido.
8. **"Disagree and commit" sem o commit:** Discordar é válido. Sabotar a execução depois da decisão não é.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/operating-system/wbr-mbr-qbr.md` | Memos são lidos e decididos na MBR/QBR. Kill criteria são monitorados na WBR. |
| `frameworks/operating-system/rasi-dri.md` | O memo define quem é DRI da decisão e os papéis RASI de execução. |
| `frameworks/operating-system/escalation-ladders.md` | Decisões que não podem ser resolvidas no nível atual escalam via memo para o nível seguinte. |
| `frameworks/vision-strategy/scenario-planning.md` | Memos de decisões estratégicas devem referenciar cenários e em qual estão apostando. |
| `checklists/exec-decision-memo-quality.md` | Checklist de qualidade para validar memos antes da reunião de decisão. |
| `templates/decision/decision-memo.md` | Template padrão do memo. |
| `data/decisions/` | Registry onde decisões aprovadas são registradas para consulta futura. |

---

## Referências

- Bryar, C. & Carr, B. (2021). *Working Backwards*. St. Martin's Press.
- Bezos, J. (1997-2020). Amazon Shareholder Letters. (Princípios de decisão Type 1/Type 2.)
- Kahneman, D. (2011). *Thinking, Fast and Slow*. Farrar, Straus and Giroux. (Vieses em decisão.)
- Heath, C. & Heath, D. (2013). *Decisive*. Crown Business. (Framework WRAP para melhor decisão.)
- C-Level Squad `config.yaml` — Princípio: "Se não está escrito, não é decisão — é conversa."
