# Teoria dos Gargalos — Theory of Constraints Aplicada a Operações

## Origem e Contexto

A Teoria das Restrições (Theory of Constraints — TOC) foi desenvolvida por Eliyahu Goldratt
no livro *The Goal* (1984) e é uma das contribuições mais poderosas para o pensamento
operacional. A premissa central é elegante e contra-intuitiva: todo sistema tem exatamente
um gargalo (constraint) que determina o throughput total do sistema. Melhorar qualquer coisa
que NÃO seja o gargalo é desperdício — pode até piorar o sistema.

Imagine uma fábrica com 5 estações. Se a estação 3 processa 50 unidades/hora e todas as
outras processam 100, o throughput total é 50 unidades/hora. Duplicar a capacidade da
estação 1 (para 200/h) não muda nada — apenas acumula inventário antes da estação 3.
Só melhorar a estação 3 melhora o sistema.

Nas organizações modernas, o gargalo raramente é uma máquina. É tipicamente: atenção da
liderança, capacidade de decisão, um time específico que todo mundo depende, um processo
de aprovação, ou um sistema técnico legacy. O framework adapta TOC para identificar e
explorar esses gargalos organizacionais.

O conceito de Drum-Buffer-Rope (Tambor-Buffer-Corda) complementa: o gargalo define o
ritmo (tambor), protege-se o gargalo com buffer, e a corda puxa trabalho no ritmo do
gargalo para evitar acumulação de work-in-progress.

## Quando Usar

- Quando a organização está "ocupada" mas resultados não melhoram proporcionalmente
- Quando há acumulação de trabalho em algum ponto do processo
- Quando investimentos em melhorias não geram o retorno esperado
- Para priorizar iniciativas de melhoria operacional
- Quando equipes diferentes culpam umas às outras por atrasos
- Na análise de capacidade para scaling

## Quando NÃO Usar

- Em sistemas verdadeiramente paralelos sem dependência (raro em organizações)
- Quando o problema é falta de direção, não falta de throughput
- Como justificativa para não investir em nada além do gargalo (outras áreas precisam
  de manutenção mínima)
- Quando a organização precisa de inovação radical, não otimização de fluxo

## Estrutura / Modelo

### Os 5 Passos de Focusing da TOC

```
PASSO 1: IDENTIFICAR o gargalo
  → Onde o trabalho acumula? Onde há fila?
  → Qual recurso está a 100% de utilização?
  → Que passo do processo, se melhorado, desbloquearia tudo?
      │
PASSO 2: EXPLOITAR o gargalo
  → Extrair o máximo do gargalo atual sem investimento
  → Eliminar desperdícios no gargalo (reuniões, interrupções, retrabalho)
  → Garantir que o gargalo nunca fica idle
      │
PASSO 3: SUBORDINAR tudo ao gargalo
  → Todos os outros processos alimentam o gargalo no ritmo certo
  → Não produzir mais do que o gargalo pode processar
  → Proteger o gargalo de variabilidade com buffers
      │
PASSO 4: ELEVAR o gargalo
  → Investir para aumentar capacidade do gargalo
  → Contratar, automatizar, terceirizar, redesenhar
  → Só depois de esgotar exploit e subordinate
      │
PASSO 5: REPETIR (não deixar inércia ser o novo gargalo)
  → Quando o gargalo muda (e vai mudar), volte ao passo 1
  → O novo gargalo pode ser em qualquer lugar do sistema
  → Cuidado: políticas criadas para o gargalo antigo viram restrições artificiais
```

### Drum-Buffer-Rope para Organizações

```
DRUM (Tambor) — O gargalo define o ritmo
├── Se o time de data science é o gargalo, toda a organização planeja
│   no ritmo da capacidade de data science
├── Sprint planning ajustado à capacidade real do gargalo
└── Pipeline de demandas dimensionado para o throughput do gargalo

BUFFER (Proteção) — Proteja o gargalo de variabilidade
├── Buffer de tempo: deadlines do gargalo têm folga upstream
├── Buffer de trabalho: backlog priorizado sempre pronto para o gargalo
├── Buffer de qualidade: input para o gargalo é pré-validado
└── Buffer de capacidade: pequena reserva para variações

ROPE (Corda) — Controle o início do trabalho
├── Novos projetos só entram quando o gargalo tem capacidade
├── WIP limits baseados no throughput do gargalo
├── Pull system: gargalo puxa trabalho quando está pronto
└── Evita acumulação de inventário (trabalho parcialmente feito)
```

### Mapa de Fluxo de Valor Simplificado

```
ETAPA 1        ETAPA 2        ETAPA 3        ETAPA 4        ETAPA 5
[Ideação]  →  [Design]   →  [Dev]      →  [QA]       →  [Deploy]
Cap: 20/sem   Cap: 15/sem   Cap: 8/sem    Cap: 12/sem   Cap: 25/sem
Util: 60%     Util: 80%     Util: 100%    Util: 65%     Util: 30%
Fila: 0       Fila: 5       Fila: 12 ←GARGALO  Fila: 0  Fila: 0

DIAGNÓSTICO:
→ Dev é o gargalo (100% utilização, fila crescente)
→ Ideação produz mais do que o sistema pode absorver
→ QA e Deploy estão subutilizados (esperando Dev)
→ Investir em QA ou Deploy não melhora throughput
```

## Processo de Aplicação (step-by-step)

### Passo 1: Mapear o Fluxo de Valor (3-5 dias)

Desenhe o fluxo completo de como valor é entregue ao cliente:
- Identifique cada etapa do processo (da ideia ao cliente)
- Para cada etapa, meça: capacidade, utilização, tempo de fila
- Marque onde trabalho acumula (filas visíveis e invisíveis)
- Identifique handoffs entre equipes (pontos de transferência)

**Ferramentas**: value stream mapping, kanban boards com WIP visível,
análise de cycle time por etapa.

**Onde procurar gargalos organizacionais**:
- Onde está a maior fila de trabalho esperando processamento?
- Qual recurso/pessoa/equipe todo mundo precisa e está sempre lotado?
- Que processo de aprovação mais atrasa entregas?
- Que sistema técnico mais causa espera?
- Onde há mais reclamações de "estamos esperando por X"?

### Passo 2: Validar o Gargalo (1-2 dias)

Cuidado com gargalos falsos. Valide:
- **Teste da fila**: há trabalho acumulado antes do gargalo? (deve haver)
- **Teste do downstream**: há capacidade ociosa depois do gargalo? (deve haver)
- **Teste de sensibilidade**: se melhorar 10% o gargalo, o throughput total melhora?
- **Teste de remoção**: se removesse o gargalo magicamente, o sistema fluiria melhor?

**Gargalos comuns em organizações de tecnologia**:
- **Decisão**: liderança não decide, tudo espera aprovação
- **Design**: um designer servindo 5 squads
- **Code review**: pull requests esperando revisão por dias
- **Dados**: equipe de data com backlog de 3 meses
- **Infraestrutura**: deploy manual que leva horas
- **Compliance**: revisão legal/security como porta estreita

### Passo 3: Exploitar — Extrair Máximo sem Investir (1-2 semanas)

Antes de investir, otimize o gargalo existente:

**Para gargalos humanos (pessoas/equipes)**:
- Elimine reuniões desnecessárias do gargalo (cada hora liberada = throughput)
- Remova trabalho não-essencial (relatórios que ninguém lê, burocracia)
- Melhore a qualidade do input (menos retrabalho = mais throughput)
- Implemente focus time protegido (blocos de 4h sem interrupção)
- Automatize tarefas repetitivas do gargalo

**Para gargalos de processo (aprovações, handoffs)**:
- Reduza o escopo da aprovação (o que realmente precisa ser aprovado?)
- Delegue autoridade (quem mais pode aprovar?)
- Crie fast-track para itens de baixo risco
- Elimine handoffs desnecessários (quem pode fazer end-to-end?)

**Para gargalos técnicos (sistemas, infraestrutura)**:
- Otimize o sistema existente antes de substituir
- Crie workarounds temporários para os casos mais frequentes
- Priorize fixes que desbloqueiam o maior volume

### Passo 4: Subordinar — Alinhar o Sistema ao Gargalo (2-4 semanas)

Ajuste todo o resto do sistema para servir o gargalo:

- **WIP limits**: limite trabalho em progresso ao que o gargalo pode absorver
- **Pull system**: gargalo puxa trabalho quando está pronto, não recebe push
- **Input quality**: etapas anteriores preparam trabalho para facilitar o gargalo
- **Priorização rigorosa**: o gargalo trabalha apenas no mais importante
- **Buffer management**: mantenha backlog priorizado pronto para o gargalo

**Exemplo**: se Dev é o gargalo com capacidade de 8 itens/semana, não adianta
Design preparar 15 itens/semana. Design deve preparar 10 (8 + buffer de 2) e
usar o tempo restante para melhorar qualidade dos specs (menos retrabalho em Dev).

### Passo 5: Elevar — Investir para Aumentar Capacidade (timeline variável)

Quando exploit e subordinate não são suficientes, invista:

- **Contratar**: mais pessoas no gargalo (mas cuidado com ramp-up time)
- **Automatizar**: se o gargalo é repetitivo, automatize
- **Terceirizar**: se o gargalo é commoditizado, terceirize
- **Redesenhar**: se o gargalo é estrutural, mude o processo
- **Tecnologia**: se o gargalo é técnico, invista em tooling

**Cuidado com a elevação prematura**: se não fez exploit e subordinate primeiro,
a nova capacidade pode ser desperdiçada com o mesmo tipo de desperdício.

### Passo 6: Repetir — O Gargalo Vai Mudar (ongoing)

Quando o gargalo é resolvido, outro ponto do sistema se torna o novo gargalo.
Isso é esperado e saudável — significa que o sistema está melhorando.

**Ciclo de melhoria contínua**:
```
Trimestre 1: Gargalo = Code Review → Implementar PR automation + pair review
Trimestre 2: Gargalo = QA → Implementar automated testing + shift-left
Trimestre 3: Gargalo = Design → Contratar + design system
Trimestre 4: Gargalo = Decisão de produto → Implementar DACI framework
```

## Exemplos Práticos

### Exemplo 1: Scale-up de Produto

**Sintoma**: time de produto entregando metade do planejado por sprint.
**Análise**: code review era o gargalo. PRs esperavam em média 2.3 dias para review.
Apenas 2 seniors faziam reviews, cada um revisando 15+ PRs/semana.

**Exploit**: eliminar PRs de < 50 linhas do processo formal (auto-merge com testes).
**Subordinar**: limitar PRs abertos por dev a 2 (reduz fila e context switching).
**Elevar**: treinar 3 mid-levels para review, com mentoria dos seniors.
**Resultado**: cycle time de PR caiu de 2.3 dias para 4 horas. Throughput de
entrega aumentou 80%.

### Exemplo 2: Operação Comercial

**Sintoma**: pipeline de vendas travado com propostas esperando aprovação comercial.
**Análise**: diretor comercial aprovava todas as propostas > R$10K pessoalmente.
70% das propostas eram entre R$10K-R$50K com formato padrão.

**Exploit**: criar template pré-aprovado para deals standard R$10K-R$50K.
**Subordinar**: vendedores preparam proposta em formato padronizado (menos retrabalho).
**Elevar**: delegar aprovação até R$50K para gerentes (com guidelines claros).
**Resultado**: tempo de aprovação de 5 dias para 4 horas. Win rate aumentou 12%
(menos deals perdidos por demora).

### Exemplo 3: Gargalo de Atenção da Liderança

O gargalo mais sutil e mais comum em scale-ups: a atenção do CEO/fundador.
Todo mundo precisa de 30 minutos do CEO. O CEO tem 10h de reunião por dia.

**Exploit**: CEO define office hours (não aceita reuniões fora de slots designados).
**Subordinar**: equipe aprende a tomar decisões sem o CEO usando DACI framework.
**Elevar**: CEO contrata COO e delega decisões operacionais.

## Armadilhas Comuns

1. **Otimizar não-gargalos**: investir em melhorias fora do gargalo não melhora o
   throughput total. É o erro mais comum e mais caro.

2. **Gargalo flutuante**: confundir variabilidade temporária com gargalo real. O
   verdadeiro gargalo é consistente, não episódico. Meça por 4+ semanas.

3. **Policy constraints**: o gargalo pode ser uma política, não um recurso. "Todo
   código precisa de review de um senior" pode ser o gargalo real, não a falta de seniors.

4. **Subordinação sem comunicação**: dizer para uma equipe "produza menos" sem explicar
   por que gera resistência. Explique a teoria, mostre o sistema.

5. **Elevar antes de exploitar**: contratar pessoas antes de otimizar o processo
   existente. Os novos herdam os mesmos desperdícios.

6. **Inércia pós-elevação**: quando o gargalo muda, as políticas criadas para o gargalo
   antigo viram restrições desnecessárias. Revise regras quando o gargalo muda.

7. **Confundir ocupação com gargalo**: uma pessoa ocupada não é necessariamente gargalo.
   Gargalo é quem tem fila de trabalho esperando E cujo throughput limita o sistema.

## Integração com Outros Frameworks

- **Execution Engine** (`coo-execution-engine.md`): o engine identifica onde a execução
  trava; TOC direciona onde intervir para destravar.
- **Operating Rhythm** (`coo-operating-rhythm.md`): o weekly sync é onde gargalos são
  reportados e ações corretivas são decididas.
- **Process Antifragility** (`coo-process-antifragility.md`): buffers da TOC contribuem
  para antifragilidade do sistema.
- **Cross-Functional Orchestration** (`coo-cross-functional-orchestration.md`): gargalos
  frequentemente estão nos handoffs entre áreas.
- **Engineering Excellence** (`cto-engineering-excellence.md`): DORA metrics revelam
  gargalos técnicos no fluxo de entrega.
- **Automation First** (`cio-automation-first.md`): automação é uma ferramenta para
  elevar gargalos de processo repetitivo.

## Referências

- Eliyahu Goldratt, *The Goal* — romance que ensina TOC de forma narrativa
- Eliyahu Goldratt, *Critical Chain* — TOC aplicada a gestão de projetos
- Eliyahu Goldratt, *It's Not Luck* — thinking processes da TOC
- Gene Kim et al, *The Phoenix Project* — TOC aplicada a IT/DevOps
- Donald Reinertsen, *The Principles of Product Development Flow* — economia de filas
- Taiichi Ohno, *Toyota Production System* — pull system e WIP limits
- W. Edwards Deming, *Out of the Crisis* — pensamento sistêmico em operações
