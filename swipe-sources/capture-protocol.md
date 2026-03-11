# Protocolo de Captura de Swipe Files

## Propósito

Este documento define o processo padrão para captura, curadoria e
organização de swipe files no C-Level Squad.

## Processo de Captura

### 1. Identificação
- Fonte reconhecida e confiável
- Conteúdo aplicável a pelo menos 1 agente do Squad
- Qualidade excepcional (não capturamos mediocridade)

### 2. Classificação

**Categorias:**
- `strategy-decks` — decks de estratégia de referência
- `decision-memos` — memos de decisão icônicos
- `operating-reviews` — WBR/MBR/QBR exemplares
- `org-design` — modelos organizacionais de referência
- `hiring` — scorecards e frameworks de entrevista
- `crisis-comms` — comunicações de crise exemplares
- `ai-use-cases` — cases de IA em negócio
- `tech-architecture` — ADRs e docs de arquitetura

**Qualidade:**
- `gold` — referência definitiva, aplicável diretamente
- `silver` — boa referência, requer adaptação
- `bronze` — útil como contexto ou contraste

### 3. Documentação

Todo swipe file DEVE conter:

```yaml
---
source: "[Nome da fonte original]"
url: "[URL se disponível]"
date_captured: YYYY-MM-DD
category: [uma das categorias acima]
agents: [lista de agentes relevantes]
tags: [tags descritivas]
quality: [gold|silver|bronze]
---
```

Corpo do arquivo DEVE conter:
1. **Contexto** — por que este exemplo é relevante
2. **Conteúdo** — o swipe em si (análise, não cópia)
3. **O que Aprendemos** — insights extraídos
4. **Como Aplicar** — integração com o C-Level Squad

### 4. Review
- Todo swipe novo deve ser revisado antes de merge
- Verificar que não é cópia direta (análise + adaptação)
- Confirmar que metadata está completa

## Cadência de Atualização

| Fonte | Frequência | Responsável |
|-------|------------|-------------|
| First Round Review | Semanal | coo-orchestrator |
| Lenny's Newsletter | Semanal | vision-chief |
| Stratechery | Semanal | vision-chief |
| Reforge | Mensal | coo-orchestrator |
| Pragmatic Engineer | Semanal | cto-architect |
| AI Research | Semanal | caio-architect |

## Regras

1. **Swipe não é plágio** — sempre analise e adapte
2. **Qualidade sobre quantidade** — 10 swipes gold > 100 bronze
3. **Vincule a agentes** — swipe sem vínculo é swipe perdido
4. **Atualize o índice** — todo swipe novo deve estar indexado na source correspondente
