# Framework Selection Guide — Como Escolher o Framework Certo

> Guia para seleccionar o framework adequado a cada situação dentro do C-Level Squad.

---

## Objetivo

O C-Level Squad disponibiliza múltiplos frameworks para diferentes contextos.
Este guia ajuda a escolher o framework certo baseado na situação, evitando
o uso de ferramentas inadequadas ao problema.

---

## Inventário de Frameworks

### Frameworks de Decisão
| Framework | Quando Usar | Não Usar Quando |
|-----------|------------|----------------|
| RAPID | Decisões com múltiplos stakeholders | Decisões operacionais simples |
| Reversibility test | Classificar tipo de decisão | Decisão já classificada |
| Pre-mortem | Avaliar riscos antes de implementar | Decisões urgentes sem tempo |
| Decision matrix | Comparar opções com múltiplos critérios | Decisão binária simples |

### Frameworks Estratégicos
| Framework | Quando Usar | Não Usar Quando |
|-----------|------------|----------------|
| OKR | Definir e alinhar objectivos | Operações do dia-a-dia |
| SWOT | Análise de posição estratégica | Decisões operacionais |
| Porter's Five Forces | Análise competitiva de mercado | Decisões internas |
| Blue Ocean | Procurar espaço de mercado não contestado | Optimizar posição actual |
| Ansoff Matrix | Estratégia de crescimento (produto × mercado) | Contexto não-comercial |

### Frameworks Operacionais
| Framework | Quando Usar | Não Usar Quando |
|-----------|------------|----------------|
| WBR/MBR/QBR | Revisão periódica de performance | Análise pontual específica |
| PDCA | Melhoria contínua de processos | Mudanças radicais |
| Kanban | Gestão de fluxo de trabalho contínuo | Projectos com deadline fixo |
| Sprint | Delivery iterativo com timebox | Trabalho contínuo sem iteração |

### Frameworks de Análise
| Framework | Quando Usar | Não Usar Quando |
|-----------|------------|----------------|
| 5 Whys | Root cause analysis simples | Problemas complexos multi-causa |
| Fishbone / Ishikawa | Análise de causas categorizada | Causa já conhecida |
| Pareto (80/20) | Priorizar por impacto | Tudo tem impacto similar |
| MECE | Estruturar problema em partes exclusivas | Problema simples |

### Frameworks de Comunicação
| Framework | Quando Usar | Não Usar Quando |
|-----------|------------|----------------|
| Pyramid principle | Comunicação executiva top-down | Brainstorming ou exploração |
| SCQA | Estruturar narrativa persuasiva | Comunicação informal |
| BLUF | Comunicação militar/executiva directa | Contexto requer narrativa |

---

## Processo de Selecção

### Passo 1 — Diagnosticar a Situação
Responde a estas perguntas:
1. **O que preciso de fazer?** (decidir, analisar, planear, comunicar, executar)
2. **Qual o nível de complexidade?** (simples, moderado, complexo)
3. **Quantos stakeholders estão envolvidos?** (individual, equipa, cross-squad)
4. **Qual a urgência?** (imediata, dias, semanas)
5. **Que tipo de output preciso?** (decisão, plano, análise, comunicação)

### Passo 2 — Mapear a Categoria
Com base no diagnóstico, identifica a categoria:

```
DECIDIR → Frameworks de Decisão
PLANEAR → Frameworks Estratégicos ou Operacionais
ANALISAR → Frameworks de Análise
COMUNICAR → Frameworks de Comunicação
EXECUTAR → Frameworks Operacionais
MELHORAR → PDCA ou Retrospective
```

### Passo 3 — Seleccionar o Framework
Dentro da categoria, escolhe baseado em:
- **Fit com o contexto**: o framework aborda o tipo de problema?
- **Escala adequada**: não usar canhão para matar mosca
- **Familiaridade**: equipa conhece e sabe usar?
- **Tempo disponível**: framework cabe no tempo disponível?
- **Output match**: o output do framework é o que preciso?

### Passo 4 — Adaptar ao Contexto
Nenhum framework é one-size-fits-all:
- Simplifica se o contexto não justifica complexidade completa
- Combina frameworks se um único não cobre o necessário
- Documenta adaptações para aprendizagem futura
- Não forces o problema a caber no framework

---

## Árvore de Decisão Rápida

```
Preciso de TOMAR UMA DECISÃO?
├── É irreversível? → Processo completo Type 1 + RAPID
├── Tem múltiplas opções comparáveis? → Decision Matrix
├── Quero antecipar riscos? → Pre-mortem
└── É reversível e simples? → Decide e avança

Preciso de DEFINIR ESTRATÉGIA?
├── Objectivos para o trimestre? → OKR
├── Posição competitiva? → SWOT + Porter
├── Direcção de crescimento? → Ansoff + Blue Ocean
└── Visão de longo prazo? → Vision framework

Preciso de ANALISAR UM PROBLEMA?
├── Encontrar causa raiz? → 5 Whys ou Fishbone
├── Priorizar por impacto? → Pareto 80/20
├── Estruturar em partes? → MECE
└── Entender tendências? → Data analysis + trends

Preciso de COMUNICAR?
├── Para executivos? → Pyramid principle + BLUF
├── Para persuadir? → SCQA
├── Para stakeholders externos? → Stakeholder update framework
└── Para a equipa? → Transparente e directo

Preciso de EXECUTAR?
├── Projecto com prazo? → Sprint + milestones
├── Trabalho contínuo? → Kanban
├── Melhoria de processo? → PDCA
└── Coordenação cross-squad? → Contratos + cadências
```

---

## Erros Comuns na Selecção de Frameworks

### 1. Framework Overkill
**Problema**: usar framework complexo para decisão simples.
**Solução**: match a complexidade do framework com a do problema.

### 2. Framework Lock-in
**Problema**: usar sempre o mesmo framework para tudo.
**Solução**: ter repertório variado e escolher consciente.

### 3. Framework como Desculpa
**Problema**: usar o processo do framework para adiar decisão.
**Solução**: frameworks aceleram decisões, não as atrasam.

### 4. Framework sem Adaptação
**Problema**: seguir framework rigidamente ignorando contexto.
**Solução**: adaptar ao contexto mantendo a essência.

### 5. Framework sem Follow-Through
**Problema**: fazer a análise mas não implementar conclusões.
**Solução**: cada framework termina com action items.

---

## Referência Rápida

Para acesso rápido durante o trabalho:

| Situação | Framework Recomendado | Ficheiro |
|----------|---------------------|---------|
| Decisão estratégica | RAPID + Decision Matrix | `frameworks/` |
| OKR setting | OKR framework | `frameworks/` |
| Root cause | 5 Whys | `frameworks/` |
| Priorização | Pareto / ICE / RICE | `frameworks/` |
| Comunicação executiva | Pyramid + BLUF | `frameworks/` |
| Melhoria de processo | PDCA | `frameworks/` |

---

## Notas Técnicas

- Todos os frameworks estão documentados em `frameworks/`
- Templates de aplicação em `templates/`
- Exemplos reais em `authority/case-studies/`
- Feedback sobre eficácia de frameworks registado trimestralmente
