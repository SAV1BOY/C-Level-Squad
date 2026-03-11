# Tarefa: Manutenção da Base de Conhecimento

## Objetivo
Garantir que a base de conhecimento da empresa permaneça atualizada, organizada e útil, servindo como fonte confiável de informação para toda a organização.

---

## 1. Escopo da Base de Conhecimento

### Conteúdo Coberto
- Frameworks estratégicos e operacionais
- Checklists de processos recorrentes
- Templates para atividades padrão
- Swipe files e referências externas
- Workflows de processos organizacionais
- Referências de livros e metodologias
- Políticas e guidelines internos
- Documentação técnica e de produto

### Princípios de Organização
- Estrutura consistente e intuitiva (fácil de navegar)
- Nomenclatura padronizada para arquivos e pastas
- Conteúdo acionável (não apenas teórico)
- Fonte única de verdade (evitar duplicação)
- Versionamento e histórico de mudanças
- Acessibilidade para toda a organização

---

## 2. Atividades de Manutenção

### Revisão Mensal (4-6 horas)

#### Auditoria de Conteúdo
- [ ] Verificar se documentos recentemente criados seguem template padrão
- [ ] Identificar conteúdo desatualizado que precisa de revisão
- [ ] Verificar se links internos e externos estão funcionando
- [ ] Identificar gaps de conteúdo (áreas sem documentação)
- [ ] Verificar consistência de formatação e estilo

#### Organização
- [ ] Garantir que novos arquivos estão nas pastas corretas
- [ ] Atualizar índices e tabelas de conteúdo se existirem
- [ ] Remover duplicatas ou versões conflitantes
- [ ] Verificar nomenclatura consistente de arquivos
- [ ] Arquivar conteúdo obsoleto (não deletar, mover para archive)

### Revisão Trimestral (1 dia)

#### Auditoria Profunda
- [ ] Revisar cada seção da base de conhecimento
- [ ] Atualizar frameworks com novas versões ou aprendizados
- [ ] Verificar se checklists refletem processos atuais
- [ ] Atualizar templates com base em feedback de uso
- [ ] Adicionar novos aprendizados de projetos recentes
- [ ] Revisar referências de livros e adicionar novos
- [ ] Coletar feedback de usuários sobre utilidade e gaps

#### Métricas de Saúde
| Métrica | Meta | Como Medir |
|---------|------|-----------|
| Documentos atualizados (< 6 meses) | >80% | Data de última revisão |
| Links funcionando | 100% | Link checker automatizado |
| Cobertura de processos documentados | >90% | Inventário vs documentado |
| Satisfação dos usuários | >4/5 | Pesquisa trimestral |
| Frequência de consulta | Crescente | Analytics se disponível |
| Novos documentos por mês | 3-5 | Contagem |

### Revisão Anual (2-3 dias)

#### Reestruturação
- [ ] Avaliar se estrutura de pastas ainda faz sentido
- [ ] Considerar reorganização baseada em feedback
- [ ] Atualizar README e guias de navegação
- [ ] Revisar e atualizar políticas de contribuição
- [ ] Planejar conteúdo prioritário para próximo ano
- [ ] Apresentar relatório de saúde da KB para liderança

---

## 3. Padrões de Qualidade

### Checklist de Qualidade por Documento
- [ ] Título claro e descritivo
- [ ] Objetivo/propósito definido no início
- [ ] Conteúdo acionável com checklists ou passos claros
- [ ] Formatação consistente (headers, listas, tabelas)
- [ ] Linguagem acessível (evitar jargão sem explicação)
- [ ] Data de criação e última atualização registrada
- [ ] Autor ou responsável identificado
- [ ] Links funcionando (internos e externos)
- [ ] Comprimento adequado (nem muito curto nem excessivo)

### Convenções de Nomenclatura
```
Formato: [categoria]/[subcategoria]/[nome-descritivo].md

Exemplos:
- checklists/strategy/annual-planning-checklist.md
- templates/operational/meeting-notes.md
- swipe/strategy-decks/microsoft-satya-transformation.md
- reference/books/leadership/brown-dare-to-lead.md
```

### Estilo de Escrita
- Usar português brasileiro consistente
- Voz ativa preferida sobre voz passiva
- Bullet points para listas de ações
- Tabelas para comparações e dados estruturados
- Headers hierárquicos (H1 para título, H2 para seções, H3 para subseções)
- Checklist format (- [ ]) para itens de ação

---

## 4. Contribuição de Conteúdo

### Como Contribuir
1. Identificar necessidade de novo conteúdo ou atualização
2. Usar template padrão da categoria correspondente
3. Redigir seguindo padrões de qualidade
4. Submeter para review do Knowledge Manager
5. Após aprovação, publicar na localização correta
6. Comunicar adição relevante para time

### Processo de Review
- Todo conteúdo novo passa por review antes de publicação
- Reviews devem ser completados em até 3 dias úteis
- Feedback fornecido via comentários ou edição sugerida
- Autor incorpora feedback e republica
- Knowledge Manager faz check final de formatação

### Incentivos à Contribuição
- Reconhecimento mensal do maior contribuidor
- Tempo alocado (2-4h/mês) para contribuição
- Menção em all-hands quando contribuição é especialmente útil
- Gamificação leve (badges, leaderboard)

---

## 5. Ferramentas e Automação

### Stack Recomendado
| Necessidade | Ferramenta | Justificativa |
|-------------|-----------|---------------|
| Repositório | Git (GitHub/GitLab) | Versionamento, PRs, reviews |
| Editor | VS Code, Notion, Confluence | Edição de markdown |
| Busca | Grep, search interno | Encontrar conteúdo rapidamente |
| Link check | Linkchecker, script custom | Verificar links quebrados |
| Analytics | Git stats, page views | Medir uso do conteúdo |

### Automações Úteis
- [ ] Alerta automático quando documento não é atualizado há 6+ meses
- [ ] Link checker semanal com relatório
- [ ] Template automático ao criar novo documento
- [ ] Notificação quando novo conteúdo é publicado
- [ ] Dashboard de métricas de saúde atualizado automaticamente

---

## 6. Responsabilidades

| Papel | Responsabilidade | Dedicação |
|-------|-----------------|-----------|
| Knowledge Manager | Manutenção, curadoria, qualidade | 8-12h/mês |
| Contribuidores | Criação e atualização de conteúdo | 2-4h/mês |
| Revisores | Review de novo conteúdo | 1-2h/mês |
| Sponsor (C-Level) | Direção estratégica, budget, priorização | 1h/mês |
