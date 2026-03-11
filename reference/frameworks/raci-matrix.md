# Framework: RACI Matrix

## Descrição

RACI é uma matriz de atribuição de responsabilidades que clarifica quem faz o quê em processos, projetos e atividades organizacionais. O acrônimo representa Responsible (quem executa), Accountable (quem responde pelo resultado), Consulted (quem é consultado antes) e Informed (quem é informado depois). Diferente do DACI (focado em decisões), o RACI é focado em execução e processos, tornando-o essencial para escalar organizações onde papéis começam a se sobrepor.

## Quando Usar

### Situações Ideais
- Definição de papéis em processos cross-funcionais
- Quando há confusão sobre quem é responsável por quê
- Onboarding de novos membros ou reestruturações organizacionais
- Documentação de processos operacionais
- Projetos envolvendo múltiplas equipes ou departamentos
- Resolução de conflitos sobre escopo e responsabilidade

### Quando NÃO Usar
- Equipes muito pequenas onde comunicação informal funciona
- Atividades criativas que requerem flexibilidade de papéis
- Como ferramenta de microgerenciamento
- Para decisões (usar DACI em vez de RACI)

## Como Aplicar

### Os Quatro Papéis

#### R - Responsible (Quem Faz)
```
Definição: A pessoa que executa o trabalho
Regras:
- Pode haver múltiplos R's para uma tarefa (subdivida se possível)
- Pelo menos um R por tarefa
- Se muitos R's, considerar se a tarefa deve ser decomposta

Exemplo: "Engenheiro desenvolve a feature"
```

#### A - Accountable (Quem Responde)
```
Definição: A pessoa que responde pelo resultado final
Regras:
- APENAS UMA pessoa A por tarefa (fundamental)
- Tem autoridade para aprovar o trabalho
- É o "dono" final do resultado
- Pode ser também R (mas não deve, se possível)

Exemplo: "Tech Lead responde pela qualidade da entrega"
```

#### C - Consulted (Quem é Consultado)
```
Definição: Pessoas consultadas ANTES de executar/decidir
Regras:
- Comunicação bidirecional (diálogo)
- Input é considerado mas não vinculante
- Não ter C demais — atrasa execução

Exemplo: "Designer consultado antes de implementar UI"
```

#### I - Informed (Quem é Informado)
```
Definição: Pessoas informadas DEPOIS da execução/decisão
Regras:
- Comunicação unidirecional (notificação)
- Não precisa de input deles
- Informar no momento certo, não depois demais

Exemplo: "Customer Success informado sobre lançamento"
```

### Construindo a Matriz

#### Passo 1: Listar Atividades/Tarefas
```
Listar todas as atividades do processo ou projeto
Ser específico o suficiente para ter clareza, não tão granular que vire micro
Agrupar atividades relacionadas se necessário
```

#### Passo 2: Listar Papéis/Pessoas
```
Listar todos os papéis (não pessoas, se possível) envolvidos
Usar papéis genéricos: CEO, CTO, PM, Designer, Eng Lead, etc.
Evitar usar nomes individuais para longevidade do documento
```

#### Passo 3: Atribuir RACI
```
Para cada célula (atividade x papel), atribuir R, A, C, I ou vazio
Validar regras:
- Cada linha tem exatamente 1 A
- Cada linha tem pelo menos 1 R
- Minimizar C's (máximo 2-3 por atividade)
- Verificar se alguém tem todos os A's (sobrecarga)
```

### Validação da Matriz
```
Checklist:
□ Cada tarefa tem exatamente 1 Accountable?
□ Cada tarefa tem pelo menos 1 Responsible?
□ Há tarefas sem nenhum R? (gap)
□ Algum papel tem A em tudo? (bottleneck)
□ Muitos C's atrasam execução?
□ Há papéis que são apenas I em tudo? (precisam estar envolvidos?)
□ A matriz foi validada com todos os envolvidos?
```

## Exemplos

### RACI do Processo de Lançamento de Feature
```
| Atividade           | PM  | Design | Eng Lead | QA  | CS  | Mktg | CEO |
|---------------------|-----|--------|----------|-----|-----|------|-----|
| Discovery           | A/R | R      | C        |     |  C  |      |  I  |
| Design UX/UI        | C   | A/R    | C        |     |     |      |     |
| Desenvolvimento     | C   | C      | A        | C   |     |      |     |
| Code Review         |     |        | A/R      |     |     |      |     |
| QA & Testes         | I   |        | C        | A/R |     |      |     |
| Documentação        | C   |        | C        |     | A/R |      |     |
| Go-to-Market        | C   |        | I        |     | C   | A/R  |  I  |
| Comunicação Cliente | I   |        |          |     | A/R | C    |     |
| Análise de Impacto  | A/R |        | C        |     | C   | C    |  I  |
```

### RACI do C-Level Squad
```
| Decisão/Processo         | CEO | CFO | CTO | CPO | CHRO |
|--------------------------|-----|-----|-----|-----|------|
| Estratégia corporativa   | A   | C   | C   | C   | C    |
| Budget anual             | A   | R   | C   | C   | C    |
| Roadmap tecnológico      | I   | C   | A   | C   |      |
| Roadmap de produto       | C   | C   | C   | A   |      |
| Hiring plan              | A   | C   | C   | C   | R    |
| Investor relations       | A   | R   |     |     |      |
| Cultura & valores        | A   | I   | C   | C   | R    |
| Pricing                  | A   | C   |     | R   |      |
| Segurança & compliance   | I   | C   | A   |     | C    |
| Comunicação interna      | A   |     |     |     | R    |
```

## Limitações

- **Burocrático** - Pode se tornar exercício de checkbox sem impacto real
- **Estático** - Organizações mudam rápido, RACI pode ficar desatualizado
- **Oversimplificado** - 4 categorias podem não capturar nuances de colaboração
- **Político** - Atribuir A pode gerar conflitos de poder
- **Não captura intensidade** - Ser C em uma tarefa pode ser 5 minutos ou 2 semanas
- **Foco em processo, não resultado** - Pode criar mentalidade de "fiz minha parte"
- **Escala** - Matrizes grandes ficam impossíveis de manter
- **Cultural** - Em culturas de alta colaboração, RACI pode parecer rígido demais
