# RASI Matrix com DRI (Directly Responsible Individual)

> **Domínio:** Operating System
> **Origem:** Variação de RACI (Responsible, Accountable, Consulted, Informed) com overlay de DRI (Apple/Amazon)
> **Uso primário:** Eliminar ambiguidade de responsabilidade em decisões, projetos e processos.
> **Agente responsável:** coo-orchestrator

---

## Origem e Contexto

A matriz RACI é uma das ferramentas de gestão mais utilizadas no mundo corporativo para esclarecer papéis e responsabilidades. A variação RASI (Responsible, Accountable, Support, Informed) simplifica a distinção entre consultado e apoio, tornando-a mais operacional.

O overlay de DRI (Directly Responsible Individual) vem da cultura da Apple e foi popularizado por Steve Jobs. A premissa é radical na sua simplicidade: **para cada decisão, entrega ou problema, existe exatamente uma pessoa cujo nome está ao lado**. Não é um comitê, não é "o time" — é uma pessoa com nome e sobrenome.

No C-Level Squad, combinamos RASI com DRI porque:
- RASI define quem faz o quê no processo.
- DRI garante que existe **uma** pessoa cuja cabeça está em jogo.

### Definição dos Papéis RASI

| Papel | Sigla | Definição | Regra |
|-------|-------|-----------|-------|
| **Responsible** | R | Quem faz o trabalho. Executa a tarefa. | Pode haver mais de um R |
| **Accountable** | A | Quem responde pelo resultado. O DRI. | Exatamente UM por entrega |
| **Support** | S | Quem apoia com recursos, dados ou expertise | Contribui sem ser dono |
| **Informed** | I | Quem precisa saber do resultado | Recebe comunicação, não decide |

---

## Quando Usar

- **Lançamento de nova iniciativa** — antes de começar, esclarecer quem é A (DRI) para cada entrega.
- **Processos cross-squad** — quando múltiplos squads participam, RASI elimina o "achei que era responsabilidade deles."
- **Decisões com múltiplos stakeholders** — quando muita gente opina mas ninguém decide, DRI resolve.
- **Onboarding de executivo** — para mostrar ao novo líder exatamente onde ele é A, R, S ou I.
- **Resolução de conflitos de escopo** — quando dois times disputam (ou nenhum assume) responsabilidade.
- **Cadências operacionais (WBR/MBR/QBR)** — cada métrica no scorecard precisa de um A claro.

---

## Quando NÃO Usar

- **Para microgerenciar** — RASI define accountability, não controle. Não use para tirar autonomia.
- **Em times muito pequenos** — se são 3 pessoas, uma conversa resolve melhor que uma matriz.
- **Como burocracia** — se preencher a matriz leva mais tempo que executar a tarefa, você está errando.
- **Para evitar conversa** — RASI não substitui alinhamento; complementa.
- **Como ferramenta estática** — RASI deve ser revisada quando o contexto muda.

---

## Estrutura / Modelo

### Template da Matriz RASI

```
┌──────────────────┬────────┬────────┬────────┬────────┬────────┐
│ Entrega/Decisão  │ Vision │  COO   │  CMO   │  CTO   │  CIO   │
│                  │ Chief  │        │        │        │        │
├──────────────────┼────────┼────────┼────────┼────────┼────────┤
│ Tese estratégica │   A    │   S    │   S    │   I    │   I    │
│ Cadência WBR     │   I    │   A    │   R    │   R    │   R    │
│ GTM plan         │   S    │   S    │   A    │   I    │   I    │
│ Arquitetura tech │   I    │   I    │   I    │   A    │   S    │
│ Data governance  │   I    │   S    │   I    │   S    │   A    │
│ AI strategy      │   S    │   S    │   I    │   S    │   I    │
└──────────────────┴────────┴────────┴────────┴────────┴────────┘
                                                     A = DRI
```

### Regras de Preenchimento

1. **Exatamente um A por linha** — se tem dois A's, ninguém é responsável.
2. **A pode ser R também** — o DRI pode executar, mas não necessariamente.
3. **Mínimo de S e I** — não inclua gente que não precisa saber. Over-informing é ruído.
4. **Sem linha vazia** — toda entrega precisa de pelo menos um A e um R.
5. **A aprova, R executa** — o R faz o trabalho; o A garante que ficou bom e responde pelo resultado.

---

## Processo de Aplicação (step-by-step)

### Passo 1: Listar entregas e decisões
- Identifique todas as entregas, decisões e processos que precisam de clareza de ownership.
- Seja específico: "GTM plan" é melhor que "marketing".
- Agrupe por domínio se necessário.

### Passo 2: Identificar participantes
- Liste todas as pessoas/papéis que podem estar envolvidos.
- No C-Level Squad: Vision Chief, COO, CMO, CTO, CIO, CAIO.
- Para cross-squad: inclua squad leads relevantes.

### Passo 3: Atribuir o DRI (A) primeiro
- Para cada entrega, pergunte: "Se isso falhar, quem eu procuro?"
- Essa pessoa é o A. Exatamente uma.
- O DRI tem autoridade para tomar decisões dentro do escopo e responde pelo resultado.

### Passo 4: Preencher R, S, I
- R: Quem executa o trabalho? (pode ser o próprio A ou outros)
- S: Quem contribui com expertise, dados ou recursos?
- I: Quem precisa saber do resultado, mas não participa da execução?
- Regra: na dúvida, I > S > R. Minimize envolvimento.

### Passo 5: Validar com o time
- Compartilhe a matriz com todos os envolvidos.
- Verifique: alguém se surpreendeu com seu papel? Algum conflito?
- Ajuste antes de oficializar.

### Passo 6: Publicar e referenciar
- A matriz RASI fica visível e acessível.
- Referencie nos workflows e tasks relevantes.
- Revise trimestralmente ou quando o contexto mudar significativamente.

---

## Exemplos Práticos

### Exemplo 1: Quarterly Planning

| Entrega | Vision Chief | COO | CMO | CTO | CIO | CAIO |
|---------|-------------|-----|-----|-----|-----|------|
| Definir bets do Q | A | S | S | S | I | I |
| Definir OKRs corporativos | A | R | S | S | S | S |
| Definir OKRs de growth | S | S | A | I | I | I |
| Definir OKRs de tech | S | S | I | A | S | I |
| Alocar budget | A | R | S | S | S | I |
| Publicar quarterly plan | I | A | I | I | I | I |

### Exemplo 2: Incident Response

| Entrega | Vision Chief | COO | CTO | CIO |
|---------|-------------|-----|-----|-----|
| Contenção técnica | I | I | A | S |
| Comunicação interna | I | A | S | S |
| Comunicação externa | A | S | I | I |
| Postmortem report | I | S | A | S |
| Ações corretivas | I | A | R | R |
| Atualização de runbooks | I | I | A | S |

### Exemplo 3: DRI em Ação

**Situação:** O deploy de sexta causou degradação de performance no sábado.

- **Sem DRI:** "Quem era responsável por monitorar o deploy?" → Silêncio. → "Achei que era do SRE." → "Não, era do time de produto." → Ninguém resolveu rápido.
- **Com DRI:** O ADR do deploy diz que o DRI de observabilidade pós-deploy é o Tech Lead do squad Alpha. Ele recebe o alerta, aciona o runbook e comunica o COO. Resolvido em 2h.

---

## Armadilhas Comuns

1. **Dois A's na mesma linha** — Se o CEO e o COO são ambos "Accountable" por uma entrega, ninguém é. Force a escolha de um.
2. **A sem autoridade** — Dar responsabilidade sem autoridade para decidir é crueldade organizacional. Se é A, pode decidir.
3. **Muitos S's** — Se todo mundo é Support, a entrega vira comitê. Limite S a quem realmente contribui.
4. **RASI na gaveta** — Matriz que ninguém consulta depois de pronta é desperdício. Referencie ativamente.
5. **Confundir R com A** — R faz o trabalho; A responde pelo resultado. O CEO pode ser A do quarterly plan mesmo que o COO (R) monte o documento.
6. **Não revisar** — Quando pessoas mudam de papel ou iniciativas evoluem, a RASI deve ser atualizada.
7. **DRI como culpado** — DRI não é bode expiatório. É a pessoa que garante que o resultado acontece e pede ajuda quando precisa.
8. **Esquecer o I** — Pessoas que deveriam saber do resultado mas não foram informadas criam surpresas organizacionais.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| **WBR/MBR/QBR** | Cada métrica no scorecard tem um A (DRI) da matriz RASI |
| **OKRs** | Todo OKR tem um A claro; KRs podem ter R's diferentes |
| **Decision Memo** | O memo identifica quem é A (decisor) e quem é S (consulted) |
| **Escalation Ladders** | A escalação segue a cadeia de A's na RASI |
| **Cross-squad Handoffs** | RASI define quem é A em cada lado do handoff |
| **Performance Review** | Accountability no performance review referencia o papel A na RASI |

---

## Referências

1. Smith, M. & Erwin, J. (2005). "Role & Responsibility Charting (RACI)." Project Management Forum.
2. Isaacson, W. (2011). *Steve Jobs*. Simon & Schuster. — Origem do conceito DRI na Apple.
3. Amazon. "Single Threaded Leadership." Prática interna de DRI.
4. Lencioni, P. (2002). *The Five Dysfunctions of a Team*. Jossey-Bass. — Contexto de accountability em times.
5. Grove, A. (1983). *High Output Management*. Vintage Books. — Base para gestão de output e accountability.
