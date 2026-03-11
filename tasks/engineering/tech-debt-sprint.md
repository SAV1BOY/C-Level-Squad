# Sprint de Dívida Técnica

> Processo estruturado para identificar, priorizar e resolver dívida técnica
> de forma sistemática, equilibrando manutenção com entrega de features.

## Objetivo

Reduzir dívida técnica de forma previsível e sustentável, prevenindo a degradação
progressiva da codebase que leva a lentidão de entrega, bugs frequentes e
dificuldade de retenção de engenheiros.

## Frequência e Alocação

- **Cadência recomendada:** 1 sprint a cada 4-6 sprints de feature
- **Alternativa:** 20% do tempo de engenharia contínuo para tech debt
- **Duração:** 2 semanas (sprint padrão)
- **Participantes:** Time de engenharia completo (não apenas os seniores)

## Tipos de Dívida Técnica

### 1. Deliberada e Prudente
"Sabemos que não é ideal, mas precisamos lançar agora e corrigir depois"
- Atalhos conscientes com prazo de correção definido
- Documentados como TODOs com justificativa
- **Prioridade de resolução:** Alta (a dívida foi aceita com prazo)

### 2. Deliberada e Imprudente
"Não temos tempo para fazer direito"
- Atalhos sem plano de correção
- Geralmente resultado de pressão de prazo sem trade-off explícito
- **Prioridade de resolução:** Média-Alta (precisa de avaliação de impacto)

### 3. Inadvertida e Prudente
"Agora que terminamos, vemos uma forma melhor"
- Aprendizado pós-implementação que revela design melhor
- Natural e inevitável em qualquer projeto
- **Prioridade de resolução:** Média (avaliar custo-benefício)

### 4. Inadvertida e Imprudente
"Não sabíamos que existia um padrão para isso"
- Falta de conhecimento ou experiência
- Frequentemente encontrada em code reviews tardias
- **Prioridade de resolução:** Alta (pode indicar problemas maiores)

## Processo de Identificação

### Fontes de Identificação
- [ ] Retrospectivas de sprint (o que nos atrasou?)
- [ ] Code review comments recorrentes
- [ ] Bug clustering (áreas do código com mais bugs)
- [ ] Tempo de deploy (se está aumentando, tech debt pode ser a causa)
- [ ] Complexidade ciclomática e outras métricas de código
- [ ] Feedback de onboarding de novos engenheiros
- [ ] Dependências desatualizadas (security + funcionalidade)

### Inventário de Tech Debt
Manter registro contínuo em backlog dedicado:

```
TECH DEBT ITEM
ID: TD-[número]
Título: [Descrição curta]
Tipo: [Deliberada/Inadvertida] + [Prudente/Imprudente]
Impacto: [Alto/Médio/Baixo]
Esforço: [P/M/G]
Área do código: [Módulo/Serviço]
Risco se não resolver: [Descrição]
Reportado por: [Nome]
Data: [Data]
```

## Processo do Sprint de Tech Debt

### Semana Anterior: Planejamento

**Dia 1-2: Priorização**
- [ ] Revisar backlog completo de tech debt
- [ ] Pontuar cada item usando framework de priorização
- [ ] Selecionar itens para o sprint com base em capacidade
- [ ] Balancear quick wins com melhorias estruturais

**Framework de Priorização:**
| Critério | Peso | Score 1-5 |
|----------|------|-----------|
| Impacto na velocidade de entrega | 30% | |
| Risco de incidente/segurança | 25% | |
| Impacto na experiência do desenvolvedor | 20% | |
| Custo de adiar mais | 15% | |
| Complexidade de resolver agora vs depois | 10% | |

**Dia 3: Sprint Planning**
- [ ] Quebrar itens selecionados em tarefas estimadas
- [ ] Atribuir tarefas a engenheiros (considerar expertise)
- [ ] Definir critérios de "done" para cada item
- [ ] Alinhar com stakeholders que não haverá features neste sprint

### Semana 1-2: Execução

- [ ] Daily standups focados em progresso e bloqueios
- [ ] Code review rigoroso (tech debt mal resolvido cria mais debt)
- [ ] Testes automatizados para cada mudança
- [ ] Documentação de decisões arquiteturais tomadas
- [ ] Métricas before/after quando possível

### Após o Sprint: Retrospectiva

- [ ] O que resolvemos e qual o impacto mensurável?
- [ ] O que aprendemos sobre nossas fontes de tech debt?
- [ ] O que podemos fazer diferentemente para prevenir?
- [ ] O que sobrou para o próximo sprint de tech debt?

## Métricas de Tech Debt

### Leading Indicators (prevenção)
- Code coverage trend (subindo = bom)
- Dependências desatualizadas (count)
- Complexidade ciclomática média
- TODOs no código (count e age)

### Lagging Indicators (impacto)
- Tempo médio para implementar feature (increasing = debt growing)
- Bug rate por release
- Deploy frequency e lead time
- Tempo de onboarding de novo engenheiro

### Sprint-Specific Metrics
- Itens de debt resolvidos vs planejados
- Impacto mensurável (ex: deploy 2x mais rápido após fix de CI)
- Novos itens de debt criados vs resolvidos

## Comunicação com Stakeholders Não-Técnicos

### Como Explicar Tech Debt para o CEO/Board
Analogia: "Tech debt é como manutenção de uma fábrica. Se você nunca para a linha
para manutenção, eventualmente a linha quebra e o custo é muito maior."

### Dados para Justificar
- "Nosso deploy leva 45 min quando deveria levar 5 (custo: X horas/semana)"
- "Bugs em produção aumentaram 30% nos últimos 3 meses"
- "Engenheiros gastam 25% do tempo em workarounds por debt conhecida"
- "2 dos últimos 3 engenheiros que saíram citaram qualidade do código"

### Framework de ROI
```
Custo de não resolver:
- Horas/semana gastas em workarounds: X
- Custo por bug em produção: Y
- Custo de turnover de engenheiros: Z
Total anual: $A

Custo de resolver:
- Sprint de 2 semanas: B engenheiros × C semanas × D custo
Total: $E

ROI: ($A - $E) / $E
```

## Anti-Padrões

1. **"Vamos resolver tech debt quando tivermos tempo"** - Nunca terá tempo; agende
2. **Tech debt sprint sem métricas** - Se não mede, não sabe se resolveu
3. **Só seniors no sprint** - Juniors aprendem muito e podem contribuir
4. **Resolver debt sem testes** - Cria mais debt
5. **Sprint de debt sem priorização** - Resolver o fácil ao invés do impactante
6. **Nunca comunicar para o negócio** - Sem buy-in, sprints de debt são cancelados

## Referências

- "Managing Technical Debt" - Philippe Kruchten, Robert Nord, Ipek Ozkaya
- "Refactoring" - Martin Fowler
- "A Philosophy of Software Design" - John Ousterhout
- Martin Fowler's TechnicalDebt bliki post
