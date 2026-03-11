# Lean Thinking - James Womack & Daniel Jones

## Resumo

"Lean Thinking" (1996) de James Womack e Daniel Jones expandiu os conceitos introduzidos em "The Machine That Changed the World" para além da manufatura automotiva. O livro codifica os cinco princípios fundamentais do pensamento enxuto e demonstra como aplicá-los em qualquer indústria. A obra é uma referência obrigatória para líderes que buscam eliminar desperdício, criar fluxo contínuo e entregar valor superior ao cliente com menos recursos. O impacto do Lean se estendeu de fábricas para hospitais, governo, software e startups.

## Conceitos-Chave

### Os Cinco Princípios Lean
1. **Definir Valor** - Valor é definido pelo cliente final, não pela empresa. Especificar valor em termos de produto/serviço específico com capacidades específicas a preço específico
2. **Mapear a Cadeia de Valor** - Identificar todas as etapas necessárias para entregar valor. Classificar em: cria valor, não cria valor mas necessário, desperdício puro
3. **Criar Fluxo** - Fazer as etapas que criam valor fluir continuamente, sem interrupções, esperas ou lotes desnecessários
4. **Estabelecer Pull (Puxar)** - Deixar o cliente puxar o valor. Produzir apenas quando há demanda real, não baseado em previsões
5. **Buscar Perfeição** - Melhoria contínua (kaizen). Os quatro princípios anteriores interagem em ciclo virtuoso

### Os Sete Desperdícios (Muda)
1. **Superprodução** - Produzir mais que o necessário ou antes do necessário
2. **Espera** - Tempo ocioso entre etapas do processo
3. **Transporte** - Movimentação desnecessária de materiais/informação
4. **Processamento excessivo** - Etapas que não agregam valor
5. **Inventário** - Acúmulo de trabalho em progresso ou produto acabado
6. **Movimento** - Movimentação desnecessária de pessoas
7. **Defeitos** - Retrabalho, correções, problemas de qualidade

### Mura e Muri
- **Mura** (Irregularidade) - Variação no processo que gera desperdício
- **Muri** (Sobrecarga) - Exigir mais de pessoas ou equipamentos do que podem entregar
- Eliminar mura e muri previne muda

### Kaizen vs. Kaikaku
- **Kaizen** - Melhoria contínua incremental, todos os dias, por todos
- **Kaikaku** - Transformação radical, redesenho completo de processo
- Ambos são necessários; kaizen sustenta ganhos de kaikaku

## Frameworks Extraídos

### Value Stream Mapping (VSM)
```
Para mapear a cadeia de valor:
1. Selecionar família de produto/serviço
2. Mapear estado atual (current state):
   - Cada etapa do processo
   - Tempo de processamento vs. tempo de espera
   - Inventário entre etapas
   - Taxa de defeito por etapa
3. Calcular lead time total vs. tempo de valor agregado
4. Identificar os maiores desperdícios
5. Desenhar estado futuro (future state)
6. Criar plano de implementação
```

### Framework de Eliminação de Desperdício
```
Para cada processo/atividade:
1. Esta atividade cria valor para o cliente?
   - SIM → Otimizar
   - NÃO → Ir para 2
2. É necessária por regulação/tecnologia/processo atual?
   - SIM → Minimizar (Tipo 1 muda)
   - NÃO → Eliminar (Tipo 2 muda)
```

### A3 Problem Solving
```
Em uma folha A3:
1. Background: contexto e importância do problema
2. Condição atual: dados e fatos sobre a situação
3. Objetivo: meta específica e mensurável
4. Análise de causa raiz: 5 porquês, diagrama Ishikawa
5. Contramedidas propostas: ações específicas
6. Plano de implementação: quem, quando, como
7. Acompanhamento: métricas e checkpoints
```

## Como Aplicar no C-Level Squad

### Para o CEO
- Adotar pensamento Lean como filosofia organizacional, não projeto isolado
- Fazer gemba walks: ir ao local onde valor é criado
- Definir claramente o que é "valor" para cada segmento de cliente
- Criar cultura de melhoria contínua em todos os níveis

### Para o CFO
- Medir eficiência pelo ratio valor-agregado/lead-time total
- Reduzir inventário financeiro (trabalho em progresso sem conclusão)
- Aplicar VSM a processos financeiros (fechamento, orçamento, reporting)
- Quantificar custo do desperdício para justificar investimentos em melhoria

### Para o CTO
- Aplicar princípios Lean ao desenvolvimento de software (Lean Software Development)
- Reduzir work-in-progress (WIP) no pipeline de desenvolvimento
- Criar fluxo contínuo de deploy (CI/CD como lean aplicado)
- Eliminar desperdício: features não usadas, retrabalho, handoffs desnecessários

### Para o CPO
- Mapear cadeia de valor do discovery ao delivery
- Pull system: desenvolver baseado em demanda real, não em backlog inflado
- Eliminar features que não criam valor (lean product development)
- Iterações rápidas como kaizen de produto

### Para o CHRO
- Treinar toda a organização nos princípios lean
- Criar sistemas de sugestão de melhoria (kaizen individual)
- Eliminar desperdício em processos de RH (contratação, onboarding)
- Medir e reduzir lead time de contratação

## Citações Relevantes

> "Lean thinking é lean porque fornece uma maneira de fazer cada vez mais com cada vez menos — menos esforço humano, menos equipamento, menos tempo e menos espaço — enquanto se aproxima de oferecer exatamente o que os clientes querem."

> "O antídoto para muda é o pensamento lean, que fornece uma maneira de especificar valor, alinhar ações que criam valor na melhor sequência, conduzir essas atividades sem interrupção e realizá-las de forma cada vez mais eficaz."

> "A maioria das pessoas pensa que sabe o que seus clientes querem. E a maioria está errada."

> "O primeiro passo é especificar valor. E esse é um passo surpreendentemente difícil."

## Críticas e Limitações
- Origens na manufatura podem limitar aplicação direta em serviços complexos
- Foco em eficiência pode prejudicar inovação e experimentação
- Implementação superficial ("Lean washing") é comum e ineficaz
- Pode criar pressão excessiva sobre trabalhadores quando mal aplicado
- Pull system é difícil em ambientes com alta variabilidade de demanda
