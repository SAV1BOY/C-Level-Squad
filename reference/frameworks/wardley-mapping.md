# Framework: Wardley Mapping

## Descrição

Wardley Mapping, criado por Simon Wardley, é uma técnica de mapeamento estratégico que visualiza a cadeia de valor de um negócio no contexto da evolução tecnológica e de mercado. Diferente de ferramentas como SWOT ou Porter, Wardley Maps mostram explicitamente o movimento — como componentes evoluem de novidade para commodity ao longo do tempo. Isso permite antecipar mudanças, identificar oportunidades de inovação e tomar decisões estratégicas sobre onde investir, o que construir internamente e o que terceirizar.

## Quando Usar

### Situações Ideais
- Decisões de build vs. buy vs. partner para componentes tecnológicos
- Planejamento estratégico com horizonte de 2-5 anos
- Análise de cadeia de valor e dependências
- Identificar componentes que estão comoditizando (oportunidade ou ameaça)
- Comunicar estratégia tecnológica para não-técnicos
- Analisar posicionamento competitivo e movimentos de mercado

### Quando NÃO Usar
- Decisões operacionais de curto prazo
- Quando o panorama competitivo é simples e estável
- Como substituto de métricas quantitativas (é qualitativo)
- Para problemas que requerem análise financeira detalhada

## Como Aplicar

### Passo 1: Identificar Necessidades do Usuário
```
- Quem é o usuário?
- Que necessidades ele tem?
- Colocar necessidades no topo do mapa (eixo Y = cadeia de valor)
```

### Passo 2: Mapear a Cadeia de Valor
```
- Para cada necessidade, que componentes são necessários?
- Para cada componente, que sub-componentes são necessários?
- Descer na cadeia até chegar a componentes fundamentais
- Eixo Y: visibilidade (topo = visível ao usuário, base = invisível)
```

### Passo 3: Posicionar na Evolução
```
Eixo X representa estágio de evolução:
I.   Genesis → Novo, incerto, experimental
II.  Custom → Construído sob medida, diferenciador
III. Product → Produto disponível no mercado, funcional
IV.  Commodity → Utilidade, padronizado, barato

Para cada componente, posicionar no eixo X conforme sua maturidade
```

### Passo 4: Adicionar Movimento e Estratégia
```
- Setas indicando para onde componentes estão evoluindo
- Identificar inércia (resistência à mudança)
- Mapear ações estratégicas:
  - Componentes em Genesis/Custom: investir, inovar, diferenciar
  - Componentes em Product: otimizar, escalar
  - Componentes em Commodity: terceirizar, automatizar, reduzir custo
```

### Padrões Estratégicos Comuns
```
1. Componentização: algo que era custom vira produto/commodity
   Ação: parar de construir internamente, usar solução de mercado

2. ILC (Innovate-Leverage-Commoditize): Amazon pattern
   Ação: inovar internamente → produtizar → vender como commodity (AWS)

3. Ecosystem Play: construir plataforma em componente que comoditiza
   Ação: oferecer componente comoditizado para capturar ecossistema

4. Signal Distortion: incumbente tenta manter componente em estágio anterior
   Ação: resistir a vendor lock-in, adotar padrões abertos
```

## Exemplos

### Exemplo: Stack de Produto SaaS
```
[Necessidade do Usuário: Gestão de Projetos]
         ↓
[Aplicação Web] ← Custom/Product
         ↓
[Framework Frontend] ← Product (React, Vue)
         ↓
[API Backend] ← Custom/Product
         ↓
[Database] ← Product/Commodity (PostgreSQL, DynamoDB)
         ↓
[Compute] ← Commodity (AWS, GCP)
         ↓
[Eletricidade] ← Utility

Insight: Inovar na aplicação (custom), commoditizar infraestrutura
```

### Exemplo: Decisão Build vs. Buy
```
Componente: Sistema de autenticação
- Evolução: Product → Commodity
- Movimento: Auth0, Clerk, Firebase Auth comoditizaram
- Decisão: COMPRAR (não há diferenciação em auth)

Componente: Motor de recomendação personalizado
- Evolução: Custom → Product (em transição)
- Movimento: ainda é diferenciador competitivo
- Decisão: CONSTRUIR (vantagem competitiva)
```

## Limitações

- **Subjetividade** - Posicionamento no eixo de evolução é baseado em julgamento
- **Complexidade** - Mapas podem ficar muito complexos para sistemas grandes
- **Curva de aprendizado** - Requer prática para criar mapas úteis
- **Não quantitativo** - Não fornece números para tomada de decisão financeira
- **Estático** - Um mapa é um snapshot; a realidade muda rapidamente
- **Viés do mapeador** - Perspectiva limitada de quem cria o mapa
- **Poucos praticantes** - Comunidade ainda relativamente pequena comparado a outros frameworks
