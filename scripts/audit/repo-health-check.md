# Script: Health Check do Repositório

## Objetivo
Verificar a saúde estrutural, completude e qualidade do repositório C-Level Squad. Identifica arquivos faltantes, referências quebradas, inconsistências de formatação e gaps de conteúdo.

## Inputs
- Caminho raiz do repositório (default: `.`)
- Nível de verificação: `quick` (estrutura) | `standard` (estrutura + conteúdo) | `deep` (tudo)
- Output format: `console` | `markdown` | `json`

## Outputs
- Relatório de saúde com score geral (0-100)
- Lista de issues encontradas por categoria e severidade
- Recomendações de correção priorizadas

---

## Lógica do Script

### Fase 1: Verificação de Estrutura

```
PARA cada diretório esperado em [templates/, lib/, scripts/, agents/]:
  VERIFICAR se diretório existe
  CONTAR arquivos .md no diretório
  REGISTRAR diretórios vazios como WARNING

PARA cada arquivo esperado no manifesto:
  VERIFICAR se arquivo existe
  VERIFICAR se tamanho > 0
  REGISTRAR arquivos faltantes como ERROR
  REGISTRAR arquivos vazios como WARNING
```

**Checklist de Estrutura:**
- [ ] `templates/` existe e contém subdiretórios
- [ ] `lib/components/` existe e contém blocos
- [ ] `scripts/` existe com subdiretórios audit/ e generators/
- [ ] `agents/` existe com configurações de agentes
- [ ] Todos os arquivos listados no manifesto estão presentes
- [ ] Nenhum arquivo está vazio (0 bytes)

### Fase 2: Verificação de Conteúdo

```
PARA cada arquivo .md no repositório:
  CONTAR linhas totais
  SE linhas < 20: REGISTRAR como WARNING ("conteúdo insuficiente")
  SE linhas < 5: REGISTRAR como ERROR ("arquivo praticamente vazio")
  
  VERIFICAR presença de seções obrigatórias:
    PARA templates: [Propósito, Instruções de Uso, Dicas de Uso]
    PARA lib/components: [Template, Exemplos, Variantes]
    PARA scripts: [Objetivo, Inputs, Outputs, Lógica]
  
  VERIFICAR formatação markdown:
    CONTAR headers (##) — mínimo esperado: 3
    VERIFICAR se há tabelas ou listas estruturadas
    VERIFICAR links internos (referências a outros arquivos)
```

**Critérios de Qualidade por Tipo:**

| Tipo | Linhas Mínimas | Seções Obrigatórias | Headers Mínimos |
|------|:-:|---|:-:|
| Template | 80 | Propósito, Instruções, Seções, Exemplo, Dicas | 5 |
| Lib Component | 80 | Pelo menos 3 blocos com template e variante | 4 |
| Script | 80 | Objetivo, Inputs, Outputs, Lógica, Exemplo | 4 |

### Fase 3: Verificação de Referências Cruzadas

```
PARA cada link interno encontrado nos arquivos:
  EXTRAIR caminho do link
  VERIFICAR se arquivo referenciado existe
  REGISTRAR links quebrados como ERROR

PARA cada referência textual a outro template/componente:
  VERIFICAR se o arquivo referenciado existe
  REGISTRAR referências a arquivos inexistentes como WARNING
```

### Fase 4: Verificação de Consistência

```
VERIFICAR padrões de nomenclatura:
  Todos os arquivos usam kebab-case? (nome-do-arquivo.md)
  Todos os templates começam com "# Template:"?
  Todos os componentes têm headers padronizados?

VERIFICAR idioma:
  Todos os arquivos estão em pt-BR?
  Há mistura de idiomas não intencional?

VERIFICAR datas e placeholders:
  Há placeholders não preenchidos em exemplos?
  Há datas hardcoded que deveriam ser placeholders?
```

---

## Scoring

### Cálculo do Score

```
Score = 100 - (Erros x 5) - (Warnings x 2) - (Info x 0.5)

Classificação:
  90-100: Excelente — repositório saudável
  75-89:  Bom — pequenos ajustes necessários
  50-74:  Atenção — problemas significativos
  0-49:   Crítico — ação urgente necessária
```

### Categorias de Issues

| Severidade | Exemplos | Penalidade |
|-----------|---------|:---:|
| ERROR | Arquivo faltante, arquivo vazio, link quebrado | -5 pts |
| WARNING | Conteúdo insuficiente (<20 linhas), seção faltante | -2 pts |
| INFO | Formatação inconsistente, nomenclatura diferente | -0.5 pts |

---

## Formato do Relatório

```markdown
# Relatório de Saúde — C-Level Squad Repository
**Data:** [DD/MM/AAAA HH:MM]
**Score:** [N/100] — [Classificação]

## Resumo
| Categoria | Erros | Warnings | Info |
|-----------|:---:|:---:|:---:|
| Estrutura | [N] | [N] | [N] |
| Conteúdo | [N] | [N] | [N] |
| Referências | [N] | [N] | [N] |
| Consistência | [N] | [N] | [N] |
| **Total** | **[N]** | **[N]** | **[N]** |

## Issues Encontradas
### Erros (ação obrigatória)
1. [ERROR] [Categoria] — [Descrição] — [Arquivo/Local]
2. [ERROR] ...

### Warnings (recomendado corrigir)
1. [WARNING] [Categoria] — [Descrição] — [Arquivo/Local]

### Info (melhoria opcional)
1. [INFO] [Categoria] — [Descrição] — [Arquivo/Local]

## Recomendações Priorizadas
1. [Ação mais impactante]
2. [Segunda ação]
3. [Terceira ação]
```

---

## Exemplo de Execução

```
$ ./repo-health-check.sh --level standard --format markdown

# Relatório de Saúde — C-Level Squad Repository
**Data:** 11/03/2026 14:30
**Score:** 87/100 — Bom

## Resumo
| Categoria | Erros | Warnings | Info |
|-----------|:---:|:---:|:---:|
| Estrutura | 0 | 1 | 0 |
| Conteúdo | 0 | 3 | 5 |
| Referências | 1 | 0 | 0 |
| Consistência | 0 | 0 | 2 |
| **Total** | **1** | **4** | **7** |

## Issues
1. [ERROR] Referência — Link quebrado para "lib/components/strategy-blocks.md" em annual-strategy-doc.md
2. [WARNING] Conteúdo — templates/crisis/recovery-plan.md tem apenas 45 linhas (mínimo: 80)
3. [WARNING] Conteúdo — Seção "Exemplo Preenchido" faltante em budget-request.md
```

---

## Cadência Recomendada
- **Semanal:** Quick check (estrutura)
- **Mensal:** Standard check (estrutura + conteúdo)
- **Trimestral:** Deep check (tudo) + correção de issues

---

## Dicas de Uso
- Execute antes de cada commit significativo para manter qualidade
- Use como CI check — falhar build se score < 75
- Mantenha um manifesto atualizado dos arquivos esperados
- Score caindo ao longo do tempo indica debt de documentação acumulando
- Automatize o máximo possível — checks manuais são esquecidos
