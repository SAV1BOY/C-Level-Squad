# Script: Validador de Referências Cruzadas

## Objetivo
Verificar integridade das referências entre arquivos do repositório, garantindo que links internos, menções a templates e dependências entre documentos estejam corretos e atualizados.

## Inputs
- Diretório raiz do repositório
- Modo: `links` (apenas links markdown) | `mentions` (referências textuais) | `full` (ambos)
- Flag `--fix` para sugerir correções automáticas

## Outputs
- Lista de referências quebradas com localização exata
- Lista de referências órfãs (arquivos não referenciados por ninguém)
- Mapa de dependências entre arquivos
- Sugestões de correção

---

## Lógica do Script

### Fase 1: Extração de Referências

```
PARA cada arquivo .md no repositório:
  
  1. EXTRAIR links markdown: [texto](caminho/arquivo.md)
     REGEX: \[([^\]]+)\]\(([^)]+\.md)\)
  
  2. EXTRAIR referências textuais a outros documentos:
     REGEX: (templates|lib|scripts|agents)/[a-z-]+/[a-z-]+\.md
  
  3. EXTRAIR menções a seções de outros documentos:
     REGEX: (ver|consulte|referência|use|veja)\s+.*\.(md|template|bloco)
  
  4. ARMAZENAR em estrutura:
     {
       arquivo_origem: "path/to/file.md",
       linha: N,
       tipo: "link" | "menção" | "referência",
       destino: "path/to/target.md",
       texto: "texto original da referência"
     }
```

### Fase 2: Validação de Referências

```
PARA cada referência extraída:
  
  1. VERIFICAR se arquivo destino existe:
     SE não existe: REGISTRAR como ERROR "Link quebrado"
     SE existe mas caminho relativo está errado: REGISTRAR como ERROR + SUGERIR correção
  
  2. VERIFICAR se seção referenciada existe (se link com #anchor):
     EXTRAIR anchor do link
     VERIFICAR se header correspondente existe no arquivo destino
     SE não existe: REGISTRAR como WARNING "Anchor quebrado"
  
  3. VERIFICAR consistência de caminhos:
     Links usando caminho absoluto vs relativo
     Links com/sem extensão .md
     NORMALIZAR e comparar
```

### Fase 3: Detecção de Órfãos

```
PARA cada arquivo .md no repositório:
  CONTAR quantas vezes é referenciado por outros arquivos
  SE referências == 0 E arquivo não é index/README:
    REGISTRAR como INFO "Arquivo órfão — não referenciado por nenhum outro"

GERAR lista de arquivos mais referenciados (top 10)
GERAR lista de arquivos nunca referenciados
```

### Fase 4: Mapa de Dependências

```
CONSTRUIR grafo de dependências:
  Nós = arquivos
  Arestas = referências (origem → destino)

IDENTIFICAR:
  - Clusters de arquivos altamente conectados
  - Arquivos hub (muitas referências recebidas)
  - Arquivos folha (referenciados mas não referenciam outros)
  - Dependências circulares (A → B → C → A)

GERAR representação visual em texto:

templates/strategy/annual-strategy-doc.md
  ├── referencia → lib/components/okr-blocks.md
  ├── referencia → lib/components/risk-assessment-blocks.md
  └── referencia → templates/finance/budget-request.md
```

### Fase 5: Sugestões de Melhoria

```
ANALISAR o mapa de dependências:
  
  1. Arquivos que DEVERIAM se referenciar mas não se referenciam:
     Ex: annual-strategy-doc.md deveria referenciar competitive-analysis.md
     REGRA: Templates da mesma categoria devem cross-referenciar
  
  2. Componentes não utilizados por nenhum template:
     Se um bloco em lib/ não é referenciado por nenhum template, sugerir inclusão
  
  3. Templates sem referência a componentes:
     Se um template não usa nenhum bloco de lib/, pode estar duplicando conteúdo
```

---

## Formato do Relatório

```markdown
# Validação de Referências Cruzadas
**Data:** [DD/MM/AAAA]
**Arquivos analisados:** [N]
**Referências encontradas:** [N]

## Resumo
| Categoria | Total | Válidas | Quebradas | Órfãs |
|-----------|:---:|:---:|:---:|:---:|
| Links markdown | [N] | [N] | [N] | — |
| Referências textuais | [N] | [N] | [N] | — |
| Arquivos no repo | [N] | — | — | [N] |

## Links Quebrados (ERROR)
| # | Arquivo Origem | Linha | Link Destino | Sugestão |
|---|---------------|:-----:|-------------|---------|
| 1 | [path/file.md] | [42] | [path/broken.md] | [Correção sugerida] |
| 2 | [path/file.md] | [87] | [path/missing.md] | [Não encontrado — remover?] |

## Arquivos Órfãos (INFO)
| # | Arquivo | Linhas | Categoria | Sugestão |
|---|---------|:------:|-----------|---------|
| 1 | [path/orphan.md] | [120] | [template] | [Referenciar a partir de X] |

## Mapa de Dependências (Top 10 mais referenciados)
| # | Arquivo | Referências Recebidas | Por Quem |
|---|---------|:---:|---------|
| 1 | [lib/components/okr-blocks.md] | [12] | [lista de arquivos] |
| 2 | [lib/components/risk-blocks.md] | [8] | [lista] |

## Cross-References Sugeridas
| Arquivo | Deveria Referenciar | Por Quê |
|---------|-------------------|---------|
| [annual-strategy-doc.md] | [competitive-analysis.md] | [Templates complementares] |
| [business-case.md] | [roi-analysis.md] | [Análise financeira relacionada] |
```

---

## Exemplo de Execução

```
$ ./cross-reference-validator.sh --mode full --fix

Analisando 45 arquivos...
Extraindo referências... 187 encontradas
Validando links... 3 quebrados
Detectando órfãos... 2 encontrados
Gerando mapa de dependências...

ERROS:
  [1] templates/strategy/annual-strategy-doc.md:95
      Link para "lib/components/strategy-blocks.md" — arquivo não existe
      Sugestão: Remover link ou criar arquivo
  
  [2] templates/finance/business-case.md:42
      Link para "templates/finance/roi-template.md" — arquivo renomeado
      Sugestão: Atualizar para "templates/finance/roi-analysis.md"

ÓRFÃOS:
  [1] scripts/generators/risk-report-generator.md — 0 referências recebidas

Score de integridade: 96% (184/187 referências válidas)
```

---

## Cadência Recomendada
- **Por commit:** Verificação automática de links (quick mode)
- **Semanal:** Validação completa com mapa de dependências
- **Mensal:** Análise de cross-references sugeridas e arquivos órfãos

---

## Dicas de Uso
- Integre no CI/CD para evitar merge de links quebrados
- Links quebrados são a forma mais rápida de degradar confiança no repositório
- Arquivos órfãos podem indicar conteúdo duplicado ou desnecessário
- Use o mapa de dependências para entender a arquitetura de informação
- Cross-references melhoram discoverability — se dois templates são relacionados, conecte-os
- Revise sugestões de cross-reference mensalmente — são melhorias de alto impacto
