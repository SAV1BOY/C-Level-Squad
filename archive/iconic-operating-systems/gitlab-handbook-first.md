# GitLab Handbook-First — Documentação como Sistema Operacional

> Análise do modelo handbook-first do GitLab como referência de transparência radical.

---

## Contexto

O GitLab opera como a maior empresa all-remote do mundo (2000+ funcionários
em 65+ países) com um princípio radical: tudo é documentado publicamente.
O seu handbook, com mais de 2000 páginas, é o sistema operacional da empresa
— acessível a qualquer pessoa no mundo.

---

## Princípios Fundamentais

### 1. Handbook-First
Qualquer processo, decisão ou política existe primeiro no handbook. Se não
está no handbook, não existe oficialmente. Conversas verbais e decisões em
reuniões devem ser documentadas no handbook para serem válidas.

### 2. Transparency by Default
Informação é pública por defeito. O threshold para classificar algo como
confidencial é alto. Salários, processos, estratégia — quase tudo é público.
A pergunta não é "porquê partilhar?" mas "porquê esconder?"

### 3. Iteration
Fazer a coisa mais pequena possível e iterar. Não esperar pela solução perfeita.
Ship, learn, iterate. Isto aplica-se a produto, processos e ao próprio handbook.

### 4. Everyone Can Contribute
Qualquer pessoa (dentro ou fora da empresa) pode propor alterações ao handbook
via merge request. Esta democratização do processo resulta em melhoria contínua
constante.

### 5. Async-First
Comunicação assíncrona é preferida sobre síncrona. Reuniões são último recurso.
Isto permite trabalho distribuído globalmente e respeita diferentes fusos horários.

---

## O Handbook como Sistema Operacional

### Estrutura
O handbook do GitLab inclui:
- **Company**: missão, visão, valores, estratégia
- **People**: processos de RH, benefícios, políticas
- **Engineering**: processos técnicos, standards, ferramentas
- **Product**: roadmap, processos de produto, design
- **Marketing**: estratégia, campanhas, brand guidelines
- **Sales**: processos de venda, playbooks, territory
- **Finance**: orçamento, procurement, expense policies
- **Legal**: políticas legais, compliance, contracts

### Como Funciona na Prática
```
1. Problema ou necessidade identificada
2. Verificar handbook para solução existente
3. Se existe: seguir o processo documentado
4. Se não existe: propor adição via merge request
5. Review e aprovação pelo owner da secção
6. Merge e comunicação
7. Handbook actualizado = novo standard operacional
```

### Merge Request como Unidade de Mudança
- Toda alteração ao handbook é um merge request
- Requer review (pelo menos 1 aprovação)
- Histórico completo de todas as alterações
- Qualquer pessoa pode ver o que mudou, quando e porquê
- Rollback é possível para qualquer versão anterior

---

## Práticas Operacionais

### Comunicação
- **Async by default**: documentos, issues, merge requests
- **Sync quando necessário**: video calls para discussões complexas
- **Always recorded**: reuniões gravadas e acessíveis
- **Low context communication**: escrever como se o leitor não tem contexto
- **Public channels**: discussões em canais públicos, não DMs

### Decisões
- **Proposal via MR**: proposta escrita com rationale
- **DRI (Directly Responsible Individual)**: cada decisão tem 1 DRI
- **Short toes**: pisar nos pés dos outros é aceitável (não territorial)
- **Two-way door**: decisões reversíveis tomadas rapidamente pelo DRI
- **Disagree, commit, and disagree**: pode continuar a discordar após commit

### Reuniões
- **Agenda obrigatória**: sem agenda, sem reunião
- **Google Doc colaborativo**: notas em tempo real num doc partilhado
- **Gravação**: todas as reuniões gravadas para quem não pôde assistir
- **15 minutos default**: reuniões curtas por defeito
- **No presentations**: informação lida antes, tempo para discussão

---

## Lições para o C-Level Squad

### O Que Adoptar
1. **Documentation-first**: processos e decisões existem porque estão escritos
2. **Single source of truth**: handbook/repositório como fonte autoritativa
3. **Contribution model**: qualquer agente pode propor melhorias
4. **Version control**: todas as alterações rastreadas e reversíveis
5. **Async-first**: comunicação assíncrona como default
6. **DRI model**: owner individual claro para cada área

### O Que Adaptar
1. **Escala de transparência**: publicar tudo pode não ser adequado para todos
   os contextos; adaptar nível de transparência
2. **Merge request process**: para squad de 6, pode ser simplificado
3. **Público vs interno**: decidir o que é público e o que fica interno
4. **Handbook size**: 2000 páginas não é necessário; foco em essenciais
5. **Tooling**: GitLab usa GitLab; escolher ferramenta adequada ao contexto

### O Que Evitar
1. **Documentation for documentation's sake**: documentar o que é útil, não tudo
2. **Process as bureaucracy**: processos devem acelerar, não travar
3. **Async extremismo**: algumas coisas são melhor resolvidas em conversa
4. **Perfeição antes de publicação**: publicar WIP é melhor que não publicar
5. **Copiar sem adaptar**: all-remote tem desafios específicos

---

## Impacto e Legado

O GitLab demonstrou que:
- Uma organização de 2000+ pode operar sem escritório físico
- Transparência radical é possível e vantajosa
- Documentação pode substituir muitos processos informais
- Open source principles aplicam-se a gestão, não apenas código
- Async-first permite acesso a talento global

---

## Referências

- GitLab Handbook: handbook.gitlab.com (público)
- "The GitLab Way" — artigos e talks de Sid Sijbrandij
- GitLab Unfiltered YouTube channel
- "Remote: Office Not Required" — Jason Fried & DHH (contexto broader)

---

## Notas Técnicas

- O C-Level Squad segue principio handbook-first com o repositório como SSoT
- Contribution guide em `docs/contribution-guide.md` é inspirada no modelo GitLab
- Changelog em `docs/changelog.md` segue principio de rastreabilidade
- Versionamento de todos os ficheiros é prática core do squad
