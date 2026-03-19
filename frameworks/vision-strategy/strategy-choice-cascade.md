# Strategy Choice Cascade (Lafley & Martin)

> **Domínio:** Vision & Strategy
> **Autor de referência:** A.G. Lafley & Roger Martin — "Playing to Win"
> **Uso primário:** Definir estratégia competitiva de forma integrada e coerente.
> **Agente responsável:** vision-chief

---

## Origem e Contexto

O Strategy Choice Cascade foi desenvolvido por A.G. Lafley (ex-CEO da P&G) e Roger Martin (Rotman School of Management) no livro "Playing to Win" (2013). O modelo nasceu da prática real de transformação da Procter & Gamble em uma das empresas mais consistentemente vencedoras do mundo.

A premissa central é que **estratégia não é planejamento — é um conjunto integrado de escolhas** que posicionam a organização para vencer no mercado escolhido. Cada escolha reforça as outras, criando um sistema coerente e difícil de copiar.

O cascade é composto por 5 perguntas sequenciais e interdependentes:

1. **What is our Winning Aspiration?** — Qual é nossa aspiração de vitória?
2. **Where to Play?** — Onde vamos competir?
3. **How to Win?** — Como vamos vencer onde escolhemos jogar?
4. **What Capabilities Must Be in Place?** — Quais capacidades são essenciais?
5. **What Management Systems Are Required?** — Quais sistemas de gestão sustentam tudo isso?

---

## Quando Usar

- Quando a empresa precisa definir ou redefinir sua estratégia competitiva central.
- Durante ciclos de planejamento anual ou trienal.
- Quando há dispersão de foco — muitos mercados, muitos produtos, sem clareza de prioridade.
- Ao entrar em novos mercados ou segmentos (cada novo "Where to Play" exige um cascade completo).
- Para avaliar coerência entre iniciativas estratégicas existentes.
- Quando o board ou investidores pedem clareza sobre a tese estratégica.
- Em conjunto com `frameworks/vision-chief/vision-chief-strategic-thesis.md` para validar a tese.

---

## Quando NÃO Usar

- Para decisões operacionais do dia-a-dia — use `frameworks/operating-system/rasi-dri.md`.
- Como exercício puramente teórico sem commitment de execução.
- Quando o problema é de execução, não de direção — use `frameworks/operating-system/okrs.md`.
- Para planejamento tático de curto prazo (sprints, quarters isolados).
- Se a empresa está em modo de sobrevivência pura (cash < 3 meses) — primeiro resolva o burning platform.

---

## Estrutura / Modelo

### O Cascade Completo

```
┌─────────────────────────────────────────────┐
│  1. WINNING ASPIRATION                      │
│     "O que significa vencer para nós?"       │
├─────────────────────────────────────────────┤
│  2. WHERE TO PLAY                            │
│     Geographies │ Segments │ Channels │      │
│     Categories  │ Stages da value chain      │
├─────────────────────────────────────────────┤
│  3. HOW TO WIN                               │
│     Cost Leadership │ Differentiation │      │
│     Niche Focus │ Ecosystem Lock-in          │
├─────────────────────────────────────────────┤
│  4. MUST-HAVE CAPABILITIES                   │
│     Core competencies que habilitam o        │
│     "How to Win" escolhido                   │
├─────────────────────────────────────────────┤
│  5. MANAGEMENT SYSTEMS                       │
│     Cadências, métricas, estruturas,         │
│     processos que sustentam as capabilities  │
└─────────────────────────────────────────────┘
```

### Detalhamento de Cada Nível

**1. Winning Aspiration**
- Não é um mission statement genérico ("ser a melhor empresa do mundo").
- É uma declaração específica de vitória: "Ser o líder em X para o segmento Y no mercado Z."
- Deve ser ambiciosa mas plausível, e guiar todas as outras escolhas.

**2. Where to Play**
- Geografia: Brasil, LATAM, Global?
- Segmento de cliente: Enterprise, SMB, Consumer?
- Canal: Direct sales, PLG, marketplace, partners?
- Categoria de produto: Qual problema específico?
- Estágio da value chain: Design, produção, distribuição, pós-venda?

**3. How to Win**
- Cost leadership: Vencer por eficiência e preço.
- Differentiation: Vencer por valor percebido superior.
- Niche focus: Dominar um segmento específico melhor que todos.
- Ecosystem lock-in: Criar switching costs via plataforma/rede.
- A escolha deve ser **consistente** com o Where to Play.

**4. Must-Have Capabilities**
- 3 a 6 capacidades que são pré-requisitos para o How to Win funcionar.
- Exemplo: Se How to Win = PLG Differentiation, capabilities = product design excellence, data-driven experimentation, self-serve onboarding.
- Capacidades devem se reforçar mutuamente (activity system).

**5. Management Systems**
- Métricas que monitoram cada capability.
- Cadências de revisão — integrar com `frameworks/operating-system/wbr-mbr-qbr.md`.
- Estrutura organizacional que suporta as capabilities.
- Processos de alocação de recursos alinhados com as escolhas.

---

## Processo de Aplicação (step-by-step)

### Fase 1: Preparação (1-2 semanas)
1. Reúna dados de mercado, competidores, performance financeira.
2. Revise a tese estratégica atual (`frameworks/vision-chief/vision-chief-strategic-thesis.md`).
3. Identifique os 3-5 stakeholders que participarão do cascade.
4. Prepare o template de canvas (ver `templates/strategy/`).

### Fase 2: Workshop de Escolhas (2-3 dias)
5. Comece pelo Where to Play — é a escolha mais negligenciada.
6. Para cada Where to Play, defina o How to Win correspondente.
7. Teste coerência: "Se jogamos aqui e vencemos assim, qual é a aspiração implícita?"
8. Refine a Winning Aspiration com base nas escolhas de baixo para cima.
9. Liste as capabilities necessárias e avalie o gap atual (tem / não tem / parcial).
10. Defina os management systems necessários para construir cada capability.

### Fase 3: Stress-Test (1 semana)
11. Aplique o "Reverse Cascade": comece pelos systems atuais e suba — as escolhas são sustentáveis?
12. Teste contra cenários adversos (`frameworks/vision-strategy/scenario-planning.md`).
13. Valide com dados de mercado: o "where" é grande o suficiente? O "how" é defensável?
14. Use a kill list (`frameworks/vision-chief/vision-chief-kill-list.md`) para eliminar o que não se encaixa.

### Fase 4: Documentação e Cascading
15. Documente o cascade final em uma página (formato `frameworks/vision-strategy/ogsm.md`).
16. Cascade para cada área via OKRs (`frameworks/operating-system/okrs.md`).
17. Registre decisões em `data/decisions/` com o formato de decision memo.
18. Comunique via narrative cascade (`frameworks/vision-chief/vision-chief-narrative-cascade.md`).

---

## Exemplos Práticos

### Exemplo 1: SaaS B2B de Analytics

| Nível | Escolha |
|-------|---------|
| Winning Aspiration | Ser a plataforma de analytics preferida por PMEs brasileiras em 3 anos |
| Where to Play | Brasil, PMEs 50-500 funcionários, segmento varejo e serviços, canal PLG + inside sales |
| How to Win | Differentiation via simplicidade + preço acessível para mercado BR |
| Capabilities | (1) UX simplificada, (2) Onboarding self-serve em PT-BR, (3) Integrações com ERPs BR, (4) CS proativo |
| Systems | NPS semanal, onboarding funnel no WBR, capability review no QBR |

### Exemplo 2: Fintech de Crédito

| Nível | Escolha |
|-------|---------|
| Winning Aspiration | Ser o maior originador de crédito para micro-empreendedores no Brasil |
| Where to Play | Brasil, MEIs e MEs, crédito de capital de giro, canal 100% digital |
| How to Win | Cost leadership via scoring proprietário + custo de aquisição via embedded finance |
| Capabilities | (1) Modelo de crédito com dados alternativos, (2) Plataforma de embedded lending, (3) Cobrança automatizada, (4) Compliance escalável |
| Systems | Default rate no WBR, CAC/LTV no MBR, model performance review no QBR |

---

## Armadilhas Comuns

1. **Aspiração genérica demais**: "Ser a melhor empresa" não é aspiração — é platitude. Seja específico sobre o que vencer significa.
2. **Where to Play amplo demais**: Tentar jogar em todos os segmentos simultaneamente dilui recursos e impede excelência.
3. **How to Win desconectado do Where**: Escolher "cost leadership" num mercado premium é incoerente.
4. **Capabilities como wish list**: Listar 15 capabilities significa que nenhuma será construída com excelência. Máximo 5-6.
5. **Ignorar Management Systems**: Sem sistemas de gestão, capabilities viram PowerPoint, não realidade.
6. **Tratar como exercício único**: O cascade precisa ser revisitado a cada QBR (`frameworks/operating-system/wbr-mbr-qbr.md`).
7. **Não fazer escolhas difíceis**: Estratégia é sobre o que NÃO fazer. Se tudo é prioridade, nada é.
8. **Cascade sem kill list**: Toda nova escolha implica matar algo antigo. Use `frameworks/vision-chief/vision-chief-kill-list.md`.

---

## Integração com Outros Frameworks

| Framework | Relação |
|-----------|---------|
| `frameworks/vision-strategy/three-horizons.md` | O cascade se aplica a cada horizonte separadamente |
| `frameworks/vision-strategy/ogsm.md` | OGSM traduz o cascade em plano de uma página |
| `frameworks/vision-strategy/wardley-mapping.md` | Wardley Map informa Where to Play e How to Win |
| `frameworks/operating-system/okrs.md` | OKRs operacionalizam as escolhas do cascade |
| `frameworks/operating-system/wbr-mbr-qbr.md` | WBR/MBR/QBR monitoram execução das escolhas |
| `frameworks/operating-system/decision-memo-framework.md` | Decisões de mudança no cascade seguem formato de memo |
| `frameworks/vision-chief/vision-chief-strategic-thesis.md` | A tese é o input principal para o cascade |
| `frameworks/vision-chief/vision-chief-kill-list.md` | Kill list reflete o que o cascade elimina |
| `checklists/strategy-memo-quality.md` | Quality gate para documentação do cascade |

---

## Referências

1. Lafley, A.G. & Martin, Roger. "Playing to Win: How Strategy Really Works." Harvard Business Review Press, 2013.
2. Martin, Roger. "A New Way to Think." Harvard Business Review Press, 2022.
3. Rumelt, Richard. "Good Strategy Bad Strategy." Crown Business, 2011.
4. Porter, Michael. "What Is Strategy?" Harvard Business Review, 1996.
5. Registros internos: `data/decisions/`, `data/registries/strategy-registry.md`
