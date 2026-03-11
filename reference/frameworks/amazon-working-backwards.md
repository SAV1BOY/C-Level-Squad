# Framework: Amazon Working Backwards

## Descrição

Working Backwards é o processo de desenvolvimento de produtos da Amazon, descrito em detalhes no livro homônimo de Colin Bryar e Bill Carr (ex-executivos da Amazon). O princípio central é começar pela experiência do cliente e trabalhar de trás para frente até a solução técnica, em vez de começar pela tecnologia e procurar um cliente. O artefato principal é o PR/FAQ — um press release fictício e FAQ que descrevem o produto como se já estivesse lançado. Este documento força clareza de pensamento antes de escrever uma linha de código.

## Quando Usar

### Situações Ideais
- Avaliação de novos produtos ou features significativas
- Decisões de investimento em novas iniciativas
- Quando há risco de construir tecnologia sem demanda real
- Alinhamento de stakeholders sobre o que será construído e por quê
- Substituição de apresentações PowerPoint para propostas de produto
- Quando é necessário priorizar entre múltiplas oportunidades

### Quando NÃO Usar
- Melhorias incrementais e bug fixes
- Decisões operacionais de rotina
- Quando velocidade é mais importante que alinhamento (ex: crise)
- Para projetos de infraestrutura técnica sem impacto direto no cliente

## Como Aplicar

### Passo 1: Escrever o Press Release (PR)
```
Estrutura do Press Release:
1. Título: Nome do produto/feature (claro e cativante)
2. Subtítulo: Uma frase sobre benefício para o cliente
3. Parágrafo de abertura: O quê, para quem, por quê
4. Problema: Que dor do cliente resolve?
5. Solução: Como resolve (linguagem de cliente, não técnica)
6. Citação do líder: Por que isso importa para a empresa
7. Como funciona: Experiência do cliente passo a passo
8. Citação do cliente: Testemunho fictício de um cliente satisfeito
9. Call to action: Como começar

Regras:
- Máximo 1-1.5 páginas
- Linguagem simples que qualquer pessoa entende
- Zero jargão técnico
- Se não consegue escrever o PR, o produto não é claro o suficiente
```

### Passo 2: Escrever as FAQs
```
FAQ Externa (para clientes):
- Perguntas que clientes fariam sobre o produto
- Preço, disponibilidade, funcionalidades, limitações
- Comparação com alternativas existentes
- Como migrar/começar

FAQ Interna (para a organização):
- Tamanho do mercado e oportunidade de negócio
- Modelo econômico (P&L projetado)
- Dependências técnicas e riscos
- Recursos necessários (pessoas, tempo, dinheiro)
- Métricas de sucesso e timeline
- Razões pelas quais poderia falhar
```

### Passo 3: Revisão e Iteração
```
1. Autor escreve PR/FAQ individualmente
2. Distribui para revisores 24-48h antes da reunião
3. Reunião começa com 20-30 min de leitura silenciosa
4. Discussão e feedback focados no documento
5. Múltiplas iterações até clareza total
6. Decisão: prosseguir, pivotar ou matar a ideia
```

### Princípios Complementares da Amazon
```
- Narrativas > PowerPoint (documentos de 6 páginas)
- Customer obsession > Competitor obsession
- Two-pizza teams: equipes pequenas e autônomas
- Single-threaded leadership: um líder, uma missão
- Disagree and commit: debater e depois comprometer
- Bias for action: velocidade importa (decisões reversíveis)
- Two types of decisions:
  - Type 1: Irreversível → cuidadosa análise
  - Type 2: Reversível → mover rápido
```

## Exemplos

### Exemplo: PR/FAQ para Feature de IA
```
PRESS RELEASE

"C-Level Squad Lança Assistente de IA para Reuniões de Board"

São Paulo, Q3 2026 — C-Level Squad anuncia AI Board Prep, um assistente
inteligente que prepara executivos para reuniões de conselho em 30 minutos
em vez de 8 horas.

Problema: CEOs gastam em média 8-12 horas preparando materiais para reuniões
de board, compilando dados de múltiplas fontes e criando apresentações.

Solução: AI Board Prep analisa automaticamente métricas financeiras, OKRs,
pipeline e indicadores de mercado, gerando um board deck estruturado com
narrativa e dados, pronto para revisão e personalização.

[Citação CEO]: "Acreditamos que o tempo do CEO deve ser gasto pensando
estrategicamente, não compilando dados. AI Board Prep devolve 8 horas por
mês para cada executivo."

[Citação Cliente]: "Pela primeira vez, consegui focar na narrativa e nos
insights em vez de gastar dias puxando dados e formatando slides." — CFO,
empresa SaaS Series B.
```

## Limitações

- **Requer habilidade de escrita** - Nem todos os líderes escrevem bem, o que pode criar barreira
- **Time-consuming** - PR/FAQ pode levar dias para ficar bom, inadequado para decisões rápidas
- **Viés de otimismo** - Press release naturalmente inclina para o positivo
- **Cultural fit** - Requer cultura que valoriza escrita e leitura profunda
- **Não substitui discovery** - PR/FAQ é hipótese; ainda precisa validar com clientes reais
- **Escalabilidade** - Difícil aplicar para todas as decisões, precisa de threshold
- **Pode matar velocidade** - Em startups early-stage, pode ser processo demais
