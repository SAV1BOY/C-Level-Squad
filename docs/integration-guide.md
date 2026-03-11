# Guia de Integração com Ferramentas

> Como integrar o C-Level Squad com ferramentas de produtividade, gestão de projetos,
> comunicação e AI para maximizar o valor do conteúdo no dia a dia executivo.

---

## Visão Geral

O C-Level Squad é um repositório de conhecimento em Markdown. Para que o conteúdo
seja útil no dia a dia, ele precisa se integrar com as ferramentas que executivos
e suas equipes já usam. Este guia cobre as integrações mais comuns.

## 1. Integração com Git e GitHub

### Setup Básico
```bash
# Clonar o repositório
git clone [URL_DO_REPOSITÓRIO]

# Manter atualizado
git pull origin main
```

### Workflow de Contribuição
1. Criar branch: `git checkout -b feature/nome-do-conteudo`
2. Fazer mudanças e commitar
3. Push: `git push origin feature/nome-do-conteudo`
4. Abrir Pull Request no GitHub
5. Review e merge

### GitHub como Interface de Leitura
- GitHub renderiza Markdown automaticamente
- Use a busca do GitHub para encontrar conteúdo
- Stars e watches para acompanhar atualizações
- Issues para sugerir melhorias ou novos conteúdos

## 2. Integração com Notion

### Importação Manual
1. Copie o conteúdo Markdown de qualquer arquivo
2. No Notion, cole com Ctrl/Cmd+Shift+V (paste as text)
3. Notion converte Markdown automaticamente
4. Organize em databases por categoria

### Sincronização Automatizada
Para manter Notion sincronizado com o repositório:

**Opção A: GitHub Sync (nativo Notion)**
- Notion oferece sincronização com repositórios GitHub
- Configurar em Settings → Connections → GitHub
- Selecionar repositório e pastas para sincronizar

**Opção B: Script de Importação**
- Usar Notion API para importar arquivos automaticamente
- Script pode rodar via GitHub Actions em cada push
- Mapear diretórios do repo para databases do Notion

### Estrutura Recomendada no Notion
```
C-Level Squad (workspace)
├── Frameworks (database)
├── Swipe Files (database)
├── Tarefas (database com recurring dates)
├── Projetos (database com kanban)
└── Referência Rápida (page)
```

## 3. Integração com Obsidian

### Setup
1. Apontar um vault do Obsidian para o diretório clonado do repositório
2. Obsidian lê Markdown nativamente
3. Links entre arquivos funcionam automaticamente

### Vantagens do Obsidian
- Graph view mostra conexões entre conteúdos
- Busca full-text instantânea
- Tags e backlinks para navegação
- Templates do Obsidian podem referenciar templates do repo

### Configuração Recomendada
- Ativar "Wikilinks" para navegação entre arquivos
- Configurar "Daily Notes" referenciando tarefas do `/tasks`
- Usar "Canvas" para mapear relações entre frameworks

## 4. Integração com Slack

### Compartilhamento Manual
- Links do GitHub renderizam preview no Slack
- Copiar seções relevantes para canais de discussão
- Usar threads para discutir aplicação de frameworks

### Automação via Slack Bot
Configurar notificações automáticas para:
- Novos conteúdos adicionados ao repositório
- Lembretes de tarefas recorrentes (usando `/tasks`)
- Digest semanal de atualizações

### Workflow Sugerido
1. Canal `#c-level-playbook` para discussões sobre conteúdo
2. Canal `#c-level-updates` para notificações automáticas de changes
3. Slack workflow que puxa checklists de `/tasks` sob demanda

## 5. Integração com Agentes AI

### Claude / ChatGPT como Assistente
O repositório é otimizado para consumo por LLMs:

**Uso Direto:**
- Copie o conteúdo de um framework e peça ao AI para aplicar ao seu contexto
- "Aplique o framework de [arquivo] à situação [descrição]"
- "Crie um plano baseado no projeto [arquivo] para [contexto]"

**Uso como Contexto:**
- Carregue arquivos relevantes como contexto para o AI
- O AI pode combinar múltiplos frameworks para resolver problemas complexos
- Peça ao AI para adaptar templates ao seu caso específico

### Claude Code Integration
Se usando Claude Code (CLI):
- O repositório pode ser referenciado diretamente
- Claude Code pode ler, buscar e combinar conteúdos
- Útil para preparação de reuniões, análises e decisões

### Automação com AI
- GitHub Actions + AI para review de novos conteúdos
- AI para sugerir conteúdos relacionados quando um novo é adicionado
- Geração de resumos automáticos de conteúdos longos

## 6. Integração com Jira / Linear

### Tarefas como Templates
Conteúdos de `/tasks` podem ser importados como templates:

**No Jira:**
1. Criar "Issue Templates" baseados nos checklists de cada tarefa
2. Configurar recorrência (mensal, trimestral, anual)
3. Associar a épicos por área funcional

**No Linear:**
1. Criar templates de projeto baseados em `/projects`
2. Usar cycles para tarefas trimestrais
3. Labels por área: operations, engineering, ai, finance

### Automação
- Script que lê Markdown e cria issues automaticamente
- Sincronização de status entre ferramenta e repositório
- Relatório de completion rate por área

## 7. Integração com Google Workspace

### Google Docs
- Importar Markdown via extensões (Docs to Markdown)
- Manter versão editável de templates em Google Docs
- Colaboração em tempo real para preenchimento de frameworks

### Google Sheets
- Checklists podem ser convertidos em planilhas trackáveis
- Métricas de `/tasks` como dashboards em Sheets
- OKRs e KPIs baseados nos frameworks do repo

### Google Calendar
- Tarefas recorrentes de `/tasks` como eventos de calendário
- Lembretes de cadência (WBR semanal, QBR trimestral)
- Blocos de tempo para preparação usando templates

## 8. Integração com Ferramentas de Apresentação

### Google Slides / PowerPoint
Para transformar conteúdo em apresentações:

1. Use seções de frameworks como slides
2. Checklists como slide de ação
3. Tabelas comparativas como slides de análise
4. Referências como slide de backup

### Gamma / Beautiful.AI
- Ferramentas AI de apresentação podem consumir Markdown diretamente
- Cole conteúdo e a ferramenta gera slides formatados
- Ideal para transformar frameworks em decks de board meeting

## 9. Integração com Dashboards

### Metabase / Looker / Power BI
Métricas definidas em `/tasks` e `/frameworks` podem alimentar dashboards:

1. Definir métricas baseadas nos frameworks de operating review
2. Criar dashboards que espelham a estrutura do WBR
3. Alertas baseados em thresholds definidos nos frameworks

### Datadog / Grafana (para times de engenharia)
- Métricas técnicas de `/tasks/engineering` como monitors
- Dashboards de SLA baseados em frameworks de architecture review
- Alertas de chaos engineering integrados

## 10. Workflow de Integração Completo

### Exemplo: Preparação de Board Meeting

1. **Conteúdo Base:** Abrir frameworks e templates relevantes do repo
2. **Dados:** Puxar métricas do dashboard (Looker/Metabase)
3. **Análise:** Usar AI (Claude) para combinar dados com frameworks
4. **Apresentação:** Exportar para Gamma/Slides
5. **Distribuição:** Compartilhar via Slack + Google Drive
6. **Follow-up:** Criar action items no Linear/Jira baseados nos templates

### Exemplo: Quarterly Strategy Review

1. **Checklist:** Abrir `tasks/operations/quarterly-strategy-review.md`
2. **Dados:** Coletar métricas conforme checklist
3. **Análise:** Aplicar frameworks de estratégia do repo
4. **Documento:** Redigir narrativa usando template de 6-pager
5. **Review:** Distribuir via Notion/Google Docs
6. **Decisões:** Documentar no ADR log se relevante

## Troubleshooting

### "Markdown não renderiza corretamente"
- Verificar encoding UTF-8
- Garantir que headers têm espaço após `#`
- Checklists precisam de espaço: `- [ ]` não `- []`

### "Links entre arquivos não funcionam"
- Links relativos dependem da ferramenta
- GitHub: links relativos a partir do arquivo atual
- Obsidian: wikilinks `[[arquivo]]`
- Notion: links são internos ao workspace

### "Conteúdo está desatualizado"
- Fazer `git pull` regularmente
- Configurar notificações de updates no GitHub
- Contribuir com atualizações quando encontrar informação desatualizada
