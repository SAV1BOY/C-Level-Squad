# Script: Auditoria de Qualidade de Conteúdo

## Objetivo
Avaliar a qualidade, utilidade e completude do conteúdo dos templates, componentes e scripts do repositório. Vai além da verificação estrutural para analisar se o conteúdo é realmente útil, acionável e mantém padrão de qualidade.

## Inputs
- Diretório ou arquivo específico a auditar
- Tipo de conteúdo: `template` | `component` | `script` | `all`
- Critérios de qualidade customizáveis (pesos por dimensão)

## Outputs
- Relatório de qualidade por arquivo e agregado
- Score de qualidade por dimensão (0-5)
- Lista de melhorias sugeridas priorizadas

---

## Lógica do Script

### Dimensões de Qualidade

| Dimensão | Peso | O que Avalia |
|----------|:----:|-------------|
| Completude | 25% | Todas as seções necessárias estão presentes? |
| Acionabilidade | 25% | Alguém consegue usar o template sem ajuda? |
| Profundidade | 20% | Conteúdo tem substância suficiente? |
| Exemplos | 15% | Há exemplos concretos e realistas? |
| Formatação | 15% | Estrutura é clara, scannable e consistente? |

### Regras de Avaliação por Dimensão

#### 1. Completude (25%)
```
PARA cada arquivo:
  VERIFICAR seções obrigatórias por tipo:
    Template: [Propósito, Instruções, Seções com placeholders, Exemplo, Dicas]
    Component: [Template formatado, Variantes, Exemplos de uso]
    Script: [Objetivo, Inputs, Outputs, Lógica, Exemplo de execução]
  
  CALCULAR: seções presentes / seções obrigatórias = % completude
  
  Score:
    5 = 100% completo + seções extras de valor
    4 = 100% completo
    3 = 80-99% completo
    2 = 60-79% completo
    1 = <60% completo
```

#### 2. Acionabilidade (25%)
```
VERIFICAR presença de:
  - Placeholders claros [entre colchetes] para preenchimento
  - Instruções passo-a-passo (numbered lists)
  - Tabelas com campos definidos
  - Exemplos de preenchimento
  - Indicação de quem usa e quando
  
  Score:
    5 = Alguém sem contexto consegue usar imediatamente
    4 = Requer mínima explicação adicional
    3 = Requer contexto moderado
    2 = Confuso — precisa de reescrita parcial
    1 = Inutilizável sem ajuda significativa
```

#### 3. Profundidade (20%)
```
VERIFICAR:
  - Número de linhas (mínimo 80 para qualidade)
  - Variedade de seções e subseções
  - Presença de tabelas detalhadas
  - Cobertura de edge cases e cenários
  - Presença de anti-padrões ou "o que NÃO fazer"
  
  Score:
    5 = >150 linhas, cobertura exaustiva, edge cases tratados
    4 = 100-150 linhas, boa cobertura
    3 = 80-100 linhas, cobertura adequada
    2 = 40-80 linhas, superficial
    1 = <40 linhas, insuficiente
```

#### 4. Exemplos (15%)
```
VERIFICAR presença de:
  - Seção "Exemplo Preenchido" com dados realistas
  - Exemplos inline dentro de seções
  - Exemplos de variantes por contexto
  - Exemplos de uso combinado (para componentes)
  
  Score:
    5 = Múltiplos exemplos realistas e variados
    4 = Exemplo completo + exemplos inline
    3 = Um exemplo preenchido adequado
    2 = Exemplo superficial ou genérico
    1 = Sem exemplos
```

#### 5. Formatação (15%)
```
VERIFICAR:
  - Hierarquia de headers consistente (##, ###, ####)
  - Tabelas markdown bem formatadas
  - Uso de bold/italic para destaque
  - Listas estruturadas (bulleted e numbered)
  - Separadores (---) entre seções
  - Código/snippets em blocos (```)
  - Escaneabilidade (leitor encontra informação rapidamente)
  
  Score:
    5 = Formatação impecável, altamente scannable
    4 = Bem formatado com pequenos ajustes
    3 = Formatação adequada
    2 = Formatação inconsistente
    1 = Mal formatado, difícil de ler
```

---

## Formato do Relatório

```markdown
# Auditoria de Qualidade de Conteúdo
**Data:** [DD/MM/AAAA]
**Escopo:** [N arquivos auditados]
**Score médio:** [X.X / 5.0]

## Ranking de Qualidade

### Top 5 (melhores)
| # | Arquivo | Score | Destaque |
|---|---------|:-----:|----------|
| 1 | [caminho] | [X.X] | [O que torna excelente] |
| 2 | [caminho] | [X.X] | [Destaque] |

### Bottom 5 (precisam de atenção)
| # | Arquivo | Score | Principal Gap |
|---|---------|:-----:|-------------|
| 1 | [caminho] | [X.X] | [O que precisa melhorar] |
| 2 | [caminho] | [X.X] | [Gap] |

## Detalhamento por Arquivo

### [Nome do arquivo]
| Dimensão | Score | Comentário |
|----------|:-----:|-----------|
| Completude | [1-5] | [Detalhe] |
| Acionabilidade | [1-5] | [Detalhe] |
| Profundidade | [1-5] | [Detalhe] |
| Exemplos | [1-5] | [Detalhe] |
| Formatação | [1-5] | [Detalhe] |
| **Média Ponderada** | **[X.X]** | |

**Melhorias sugeridas:**
1. [Melhoria prioritária]
2. [Segunda melhoria]

## Resumo por Categoria
| Categoria | N Arquivos | Score Médio | Pior Dimensão |
|-----------|:---------:|:----------:|--------------|
| templates/strategy | [N] | [X.X] | [Dimensão] |
| templates/engineering | [N] | [X.X] | [Dimensão] |
| lib/components | [N] | [X.X] | [Dimensão] |
| scripts | [N] | [X.X] | [Dimensão] |

## Top 10 Melhorias Priorizadas
| # | Arquivo | Melhoria | Impacto | Esforço |
|---|---------|---------|:------:|:------:|
| 1 | [arquivo] | [O que fazer] | [Alto] | [Baixo] |
| 2 | [arquivo] | [O que fazer] | [Alto] | [Médio] |
```

---

## Exemplo de Execução

```
$ ./content-quality-audit.sh --type all --output report.md

Auditando 45 arquivos...

templates/strategy/annual-strategy-doc.md .......... 4.3/5.0
templates/strategy/competitive-analysis.md ......... 4.5/5.0
templates/engineering/adr-template.md .............. 4.2/5.0
...

Score médio: 4.1/5.0

Top melhoria: Adicionar exemplos preenchidos em 3 templates de finance (impacto alto, esforço baixo)
```

---

## Cadência Recomendada
- **Mensal:** Auditoria completa com relatório para a equipe
- **Por commit:** Verificação automatizada de novos/alterados
- **Trimestral:** Revisão profunda com plano de melhorias

---

## Dicas de Uso
- Score < 3.0 em qualquer arquivo é inaceitável — priorize correção
- Exemplos são a dimensão mais impactante para usuários — invista nela
- Acionabilidade é o critério mais difícil — teste com alguém que nunca viu o template
- Mantenha um backlog de melhorias de conteúdo priorizado
- Compare scores ao longo do tempo — qualidade deve subir, não cair
