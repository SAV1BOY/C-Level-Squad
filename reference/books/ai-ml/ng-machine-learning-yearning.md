# Machine Learning Yearning - Andrew Ng

## Resumo

"Machine Learning Yearning" (2018) de Andrew Ng, cofundador do Google Brain e ex-VP de Baidu, é um guia prático para estruturar projetos de machine learning. Diferente de livros acadêmicos, foca em decisões estratégicas e práticas: como dividir dados, priorizar o que trabalhar, diagnosticar erros e iterar rapidamente. É essencial para líderes técnicos e executivos que precisam tomar decisões sobre projetos de ML sem se perder em detalhes algorítmicos. O livro é disponibilizado gratuitamente por Ng.

## Conceitos-Chave

### Abordagem Iterativa para ML
- ML é fundamentalmente iterativo: ideia → código → experimento → análise → repetir
- Velocidade de iteração é mais importante que o algoritmo inicial escolhido
- Ter um baseline rápido é melhor que gastar meses no "modelo perfeito"
- Pipeline completo (end-to-end) funcionando > componente perfeito isolado

### Divisão de Dados
- **Training set** - Dados para treinar o modelo (maior porção)
- **Dev set (validation)** - Dados para ajustar hiperparâmetros e decisões
- **Test set** - Dados para avaliação final imparcial
- Dev e test devem vir da mesma distribuição
- Dev e test devem refletir dados reais de produção

### Análise de Erro
- Examinar manualmente exemplos que o modelo erra
- Categorizar erros para priorizar melhorias
- Ceiling analysis: entender o ganho máximo de cada melhoria
- Gastar tempo analisando erros, não apenas treinando modelos

### Bias vs. Variance
- **High bias (underfitting)** - Modelo muito simples, não aprende os padrões
- **High variance (overfitting)** - Modelo memoriza training data, não generaliza
- Diagnóstico: comparar erro de training vs. dev
- Receitas diferentes para cada problema

### Desempenho Humano como Referência
- Bayes optimal error: o melhor desempenho possível
- Performance humana como proxy para Bayes error
- Avoidable bias = gap entre humano e training error
- Se erro ainda é alto vs. humano: focar em reduzir bias
- Se erro é baixo vs. humano mas alto em dev: focar em reduzir variance

## Frameworks Extraídos

### Framework de Priorização de Projetos ML
```
Para cada projeto ML proposto, avaliar:
1. Impacto no negócio se funcionar (alto/médio/baixo)
2. Viabilidade técnica (dados disponíveis? problema bem definido?)
3. Dados existentes (quantidade, qualidade, rotulagem)
4. Baseline humano (qual a performance humana na tarefa?)
5. Velocidade de iteração (quão rápido podemos testar?)

Priorizar: Alto impacto + Alta viabilidade + Dados existentes
```

### Diagnóstico de Problemas em ML
```
1. Medir training error e dev error
2. Comparar com performance humana (ou baseline)

Se training error >> human error:
  → High bias (underfitting)
  → Soluções: modelo maior, treinar mais tempo, features melhores

Se training error ≈ human error mas dev error >> training error:
  → High variance (overfitting)
  → Soluções: mais dados, regularização, modelo mais simples

Se dev error ≈ training error mas ambos >> human error:
  → High bias
  → Precisa de abordagem fundamentalmente diferente

Se dev error << test error:
  → Overfitting ao dev set
  → Dev set muito pequeno ou muito usado
```

### Processo de Error Analysis
```
1. Coletar 100 exemplos que o modelo errou no dev set
2. Examinar manualmente cada um
3. Categorizar em tipos de erro
4. Contar frequência de cada categoria
5. Priorizar: categoria com mais erros = maior oportunidade
6. Para cada categoria: que dados ou features resolveriam?
7. Implementar melhoria e medir impacto
```

## Como Aplicar no C-Level Squad

### Para o CEO
- Entender que ML é processo iterativo, não projeto waterfall
- Definir métricas de negócio claras antes de iniciar projetos ML
- Não esperar perfeição: começar com baseline e iterar
- Avaliar projetos ML por impacto de negócio, não sofisticação técnica

### Para o CFO
- Orçar projetos ML como iterações, não como projetos com entrega fixa
- Medir ROI de ML por melhoria incremental em métricas de negócio
- Investir em infraestrutura de dados como pré-requisito para ML
- Entender que dados são o ativo mais valioso, não o modelo

### Para o CTO
- Implementar infraestrutura que permita iteração rápida
- Garantir pipeline de dados robusto antes de investir em modelos
- Criar processos de error analysis sistemáticos
- Monitorar performance em produção (data drift, model decay)

### Para o CPO
- Definir métricas de sucesso de produto que ML deve otimizar
- Entender trade-offs: precision vs. recall impacta experiência do usuário
- Planejar fallbacks para quando ML falha (graceful degradation)
- User research como análise de erro qualitativa

### Para o CHRO
- Recrutar ML engineers com habilidade prática, não apenas teórica
- Investir em upskilling da equipe existente em ML/data
- Criar cultura de experimentação e tolerância a falhas em ML
- Entender que ML requer perfis diversos: engenharia, ciência, domínio

## Citações Relevantes

> "A maioria dos problemas de ML pode ser resolvida com mais dados ou dados melhores, não com algoritmos mais sofisticados."

> "Não tente construir o sistema perfeito de primeira. Construa algo que funciona e itere."

> "Se você não pode fazer análise de erro manualmente, você está voando às cegas."

> "A habilidade mais importante em ML é saber o que fazer a seguir quando as coisas não estão funcionando."

## Críticas e Limitações
- Foco em supervised learning; menos cobertura de unsupervised, RL e LLMs
- Escrito antes da revolução de foundation models e transformers
- Algumas recomendações (ex: sempre mais dados) podem não aplicar a modelos modernos pré-treinados
- Menos relevante para aplicações que usam APIs de LLMs (fine-tuning vs. prompting)
- Assume acesso a dados rotulados, que nem sempre é viável
