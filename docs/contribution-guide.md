# Contribution Guide — Como Contribuir para o C-Level Squad

> Guia para contribuir com melhorias, correcções e novos conteúdos ao C-Level Squad OS.

---

## Filosofia de Contribuição

O C-Level Squad OS é um sistema vivo que melhora com contribuições de quem o
utiliza. Cada operador é incentivado a propor melhorias baseadas na sua
experiência. Contribuições são valorizadas e reconhecidas.

---

## Tipos de Contribuição

### 1. Bug Fix / Correcção
- Correcção de erros em documentação ou templates
- Dados incorrectos em referências
- Links quebrados
- Typos e erros gramaticais

### 2. Melhoria
- Melhorar clareza de documentação existente
- Adicionar exemplos a frameworks ou workflows
- Optimizar processos baseado em experiência
- Actualizar informação desactualizada

### 3. Nova Funcionalidade
- Novo workflow para cenário não coberto
- Novo framework ou adaptação
- Novo template para output recorrente
- Novo script de automação

### 4. Conteúdo de Autoridade
- Novo case study baseado em experiência real
- Novo essay sobre tema relevante
- Actualização de glossário ou FAQ
- Novo material para archive

---

## Processo de Contribuição

### Passo 1 — Identificar a Contribuição
Antes de começar, verifica:
- [ ] O problema ou gap existe realmente?
- [ ] Não existe já solução no repositório?
- [ ] A contribuição está alinhada com os princípios do OS?
- [ ] Tens contexto suficiente para contribuir bem?

### Passo 2 — Propor
Para contribuições significativas (novas funcionalidades, mudanças de processo):
```markdown
# Proposta de Contribuição

## Título
[Nome descritivo]

## Tipo
[Bug fix | Melhoria | Nova funcionalidade | Conteúdo]

## Problema / Gap
[O que está em falta ou incorrecto]

## Solução Proposta
[O que propões fazer]

## Impacto
[Quem beneficia e como]

## Esforço Estimado
[Pequeno: <1h | Médio: 1-4h | Grande: >4h]
```

Para correcções simples, avança directamente para o Passo 3.

### Passo 3 — Implementar
1. Cria ou edita os ficheiros relevantes
2. Segue os standards definidos (ver secção Standards)
3. Testa a contribuição (executa workflow, lê documento)
4. Documenta o que mudou e porquê

### Passo 4 — Review
1. Submete para review pelo owner do domínio afectado
2. Incorpora feedback
3. Obtém aprovação

### Passo 5 — Merge e Comunicação
1. Integra a contribuição no repositório
2. Actualiza `docs/changelog.md`
3. Comunica a alteração se afecta outros utilizadores

---

## Standards de Qualidade

### Para Documentação
- [ ] Escrita em português para conteúdo operacional, inglês para termos técnicos
- [ ] Segue convenções de nomenclatura (`docs/naming-conventions.md`)
- [ ] Estrutura clara com headers hierárquicos (H1, H2, H3)
- [ ] Mínimo 80 linhas (conteúdo substantivo, não padding)
- [ ] Inclui secção de Notas Técnicas quando relevante
- [ ] Links internos correctos
- [ ] Sem erros ortográficos graves
- [ ] Tom consistente com o resto do repositório

### Para Templates
- [ ] Todos os campos são necessários (sem campos decorativos)
- [ ] Instruções claras de preenchimento
- [ ] Exemplo preenchido quando possível
- [ ] Formato consistente com templates existentes

### Para Workflows
- [ ] Trigger claramente definido
- [ ] Passos sequenciais e lógicos
- [ ] Decision gates em pontos adequados
- [ ] Quality gate final presente
- [ ] Testado com cenário real ou simulado

### Para Scripts
- [ ] Objectivo claro e documentado
- [ ] Inputs e outputs definidos
- [ ] Processo passo-a-passo
- [ ] Tratamento de erros
- [ ] Integração com outros scripts indicada

### Para Conteúdo de Autoridade
- [ ] Baseado em factos verificáveis ou experiência real
- [ ] Fontes referenciadas quando aplicável
- [ ] Lições práticas e actionable
- [ ] Tom profissional e informativo

---

## O Que NÃO Contribuir

1. **Conteúdo genérico sem valor**: não adicionar texto só para preencher
2. **Opinião pessoal como facto**: opiniões são válidas em essays, não em docs
3. **Informação confidencial**: sem dados reais de clientes ou internos sensíveis
4. **Conteúdo copiado sem atribuição**: sempre citar fontes
5. **Alterações incompatíveis**: não quebrar workflows ou scripts existentes
6. **Over-engineering**: manter simplicidade, complexidade só quando justificada

---

## Governance de Contribuições

### Quem Aprova
| Tipo | Aprovador |
|------|----------|
| Docs (geral) | COO Orchestrator |
| Agent definitions | Vision Chief |
| Frameworks | Vision Chief + domínio owner |
| Workflows | COO Orchestrator |
| Scripts | CTO Architect ou CIO Engineer |
| Templates | Owner do domínio |
| Authority content | Vision Chief |
| Policies | Vision Chief + Board (se major) |

### Tempo de Review
- Bug fix / Correcções: 24h
- Melhorias: 48h
- Novas funcionalidades: 1 semana
- Conteúdo de autoridade: 1 semana
- Alterações de política: 2 semanas

---

## Reconhecimento

Contribuições são reconhecidas no:
- `docs/changelog.md`: cada entrada referencia o contribuidor
- Quarterly review: contribuições destacadas são mencionadas
- Contributor list: mantida actualizada (quando aplicável)

---

## Dicas para Boas Contribuições

1. **Começa pequeno**: primeira contribuição deve ser simples
2. **Pergunta antes**: se não tens a certeza, pergunta antes de fazer
3. **Mostra o problema**: antes da solução, mostra o problema claramente
4. **Testa**: executa o que mudaste antes de submeter
5. **Sê específico**: "melhorar documentação" não é contribuição — "adicionar exemplos ao framework X" é
6. **Itera**: é melhor submeter algo bom e melhorar depois do que esperar pela perfeição

---

## Notas Técnicas

- Contribuições versionadas via sistema de controlo de versão
- Changelog mantido em `docs/changelog.md`
- Histórico de contribuições mantido indefinidamente
- Disputes sobre contribuições resolvidos pelo COO Orchestrator
