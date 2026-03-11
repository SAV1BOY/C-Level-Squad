# Politica de Versionamento do C-Level Squad

## Objetivo

Este documento define as regras de versionamento para todos os documentos, frameworks, templates e artefatos produzidos pelo C-Level Squad. Uma politica clara de versionamento garante rastreabilidade, consistencia e confianca nos materiais utilizados.

## Esquema de Versionamento

### Formato de Versao
Utilizamos versionamento semantico adaptado: MAJOR.MINOR.PATCH

- **MAJOR** (X.0.0): Mudancas estruturais significativas que alteram fundamentalmente o conteudo ou abordagem do documento. Requer revisao e aprovacao do coordenador do squad.
- **MINOR** (0.X.0): Adicoes de conteudo relevante, novas secoes, atualizacao de benchmarks ou metricas significativas. Requer revisao por pelo menos um agente alem do autor.
- **PATCH** (0.0.X): Correcoes de erros, ajustes de formatacao, atualizacoes menores de dados, melhorias de clareza. Pode ser aplicado diretamente pelo autor.

### Exemplos de Classificacao
| Mudanca | Tipo | Exemplo |
|---------|------|---------|
| Reestruturacao completa de framework | MAJOR | Framework de decisao reescrito com nova metodologia |
| Nova secao adicionada a documento | MINOR | Adicao de secao sobre AI em documento de estrategia |
| Atualizacao de benchmarks anuais | MINOR | Atualizacao de metricas DORA com dados mais recentes |
| Correcao de erro em numero | PATCH | Correcao de percentual incorreto em tabela |
| Melhoria de formatacao | PATCH | Reorganizacao de bullets para maior clareza |
| Correcao ortografica | PATCH | Correcao de erros de digitacao |

## Controle de Versao por Tipo de Artefato

### Frameworks e Guias Fundamentais
- Versionamento completo (MAJOR.MINOR.PATCH)
- Changelog obrigatorio para mudancas MAJOR e MINOR
- Revisao trimestral programada
- Aprovacao do coordenador para MAJOR
- Notificacao ao squad para MINOR

### Templates e Checklists
- Versionamento simplificado (MINOR.PATCH)
- Changelog para mudancas MINOR
- Revisao semestral programada
- Qualquer agente pode atualizar com revisao de pares

### Dados de Referencia e Benchmarks
- Versionamento por data (AAAA-MM)
- Atualizacao minima anual obrigatoria
- Fontes devem ser revalidadas a cada atualizacao
- Marcar dados desatualizados com aviso

### Frases e Vocabulario
- Versionamento simplificado (MINOR.PATCH)
- Adicoes frequentes sao esperadas
- Revisao semestral para remover itens obsoletos

## Registro de Mudancas (Changelog)

### Formato do Changelog
Cada documento com versionamento completo deve ter uma secao de changelog no final:

```
## Historico de Versoes

### v2.1.0 - 2026-03-15
- Adicionada secao sobre metricas de AI
- Atualizado benchmark de DORA metrics com dados 2025
- Autor: CAIO Architect | Revisor: CIO Engineer

### v2.0.0 - 2026-01-10
- Reestruturacao completa do framework
- Nova abordagem baseada em pesquisa atualizada
- Autor: Squad Coordinator | Aprovador: CEO

### v1.3.2 - 2025-11-20
- Correcao de taxa de conversao na tabela de hiring
- Autor: CFO Strategist
```

### Informacoes Obrigatorias no Changelog
- Numero da versao e data
- Descricao concisa das mudancas
- Autor da mudanca
- Revisor/aprovador (para MAJOR e MINOR)

## Fluxo de Aprovacao

### Para Mudancas MAJOR
1. Autor prepara a nova versao com justificativa
2. Solicita revisao ao coordenador do squad
3. Coordenador designa revisores relevantes
4. Revisores fornecem feedback em ate 5 dias uteis
5. Autor incorpora feedback e prepara versao final
6. Coordenador aprova e publica
7. Notificacao enviada ao squad completo

### Para Mudancas MINOR
1. Autor prepara a mudanca
2. Solicita revisao a pelo menos 1 agente do squad
3. Revisor valida em ate 3 dias uteis
4. Autor publica e registra no changelog
5. Notificacao enviada aos agentes afetados

### Para Mudancas PATCH
1. Autor realiza a correcao
2. Registra no changelog (se houver)
3. Publica diretamente

## Politica de Deprecacao

### Quando Deprecar
- Documento foi substituido por versao significativamente diferente
- Conteudo nao e mais relevante ou correto
- Framework foi descontinuado

### Como Deprecar
1. Marcar documento como DEPRECATED no titulo
2. Incluir nota no topo: "Este documento foi descontinuado em [data]. Consulte [novo documento] para a versao atual."
3. Mover para diretorio /archive apos 90 dias
4. Manter no arquivo por pelo menos 12 meses
5. Atualizar referencias cruzadas em outros documentos

## Nomenclatura de Arquivos

### Convencoes
- Usar kebab-case: `nome-do-documento.md`
- Sem acentos ou caracteres especiais no nome do arquivo
- Prefixo numerico para documentos sequenciais: `01-preparacao.md`
- Nao incluir versao no nome do arquivo (versao fica no conteudo)

### Estrutura de Diretorios
- Manter a hierarquia existente de diretorios
- Criar subdiretorios apenas quando ha 3+ documentos relacionados
- Documentos de uso geral ficam no diretorio pai

## Revisao Programada

### Calendario de Revisao
| Tipo de Artefato | Frequencia | Responsavel |
|-----------------|------------|-------------|
| Frameworks fundamentais | Trimestral | Coordenador + Agente especialista |
| Guias de voz | Semestral | Coordenador |
| Benchmarks e dados | Anual (minimo) | Agente da area |
| Templates | Semestral | Agente da area |
| Checklists | Trimestral | Agente da area |
| Politicas | Anual | Coordenador |

### Processo de Revisao Programada
1. Coordenador envia lembrete 2 semanas antes da data
2. Agente responsavel revisa e propoe mudancas
3. Mudancas seguem fluxo de aprovacao conforme tipo
4. Data de proxima revisao atualizada no documento
5. Se nenhuma mudanca necessaria, registrar "Revisado em [data] - sem alteracoes"
