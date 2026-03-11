# Board Prep Builder

> Script para construção de materiais preparatórios para reuniões de Board/Conselho.

---

## Objetivo

Automatizar e padronizar a preparação de materiais para reuniões de Board,
garantindo que a narrativa estratégica, dados financeiros e métricas operacionais
estejam alinhados, revisados e distribuídos dentro dos prazos exigidos.

---

## Calendário de Preparação

| Dia Relativo | Atividade | Responsável |
|-------------|-----------|-------------|
| D-21 | Kick-off da preparação, definição de temas | Vision Chief |
| D-14 | Coleta de dados e primeira versão de narrativas | Todos os agents |
| D-10 | Revisão cruzada entre agents | COO Orchestrator |
| D-7 | Consolidação do board pack draft | Vision Chief + COO |
| D-5 | Revisão final e aprovação | Vision Chief |
| D-5 | Distribuição aos membros do Board | COO Orchestrator |
| D-2 | Sessão de preparação interna (dry run) | C-Level Squad completo |
| D-0 | Reunião do Board | Vision Chief apresenta |

---

## Coleta de Dados

### Dados Financeiros (Owner: CFO / Finance)
- P&L do período com variance analysis contra budget
- Cash flow statement e projeção de 12 meses
- Balance sheet highlights e ratios-chave
- Capital allocation e investment tracking
- Runway analysis com cenários (base, optimistic, pessimistic)

### Dados Estratégicos (Owner: Vision Chief)
- Progresso contra OKRs estratégicos
- Status de iniciativas prioritárias
- Mudanças no cenário competitivo
- Oportunidades e ameaças identificadas
- Decisões estratégicas pendentes para aprovação do Board

### Dados Operacionais (Owner: COO Orchestrator)
- KPIs operacionais com tendência de 12 meses
- Health scores de todas as iniciativas críticas
- Risk register atualizado com mitigações
- Cross-squad performance metrics
- Capacity e resource utilization

### Dados de Produto e Tecnologia (Owner: CTO Architect)
- Roadmap progress e desvios
- Métricas de qualidade e reliability
- Tech debt assessment
- Security posture update
- Infrastructure cost optimization

### Dados de AI e Inovação (Owner: CAIO Architect)
- AI adoption metrics e ROI
- Pipeline de inovação e experimentos
- AI governance compliance status
- Emerging technology assessment
- AI risk assessment atualizado

### Dados de Mercado e Growth (Owner: CMO Architect)
- Market share e positioning
- Customer acquisition e retention metrics
- Brand health indicators
- Competitive intelligence summary
- Growth projections e assumptions

---

## Estrutura Narrativa

O board pack deve seguir a estrutura narrativa abaixo. Cada seção deve ser
escrita em formato narrativo (memo style), não em bullet points ou slides.

### 1. Executive Summary (máximo 2 páginas)
- Estado do negócio em uma frase
- 3-5 highlights do período
- 3-5 desafios ou riscos principais
- Decisões que requerem aprovação do Board
- Outlook para o próximo período

### 2. Financial Review (3-5 páginas)
- Performance financeira vs. plano
- Análise de drivers de receita e custo
- Unit economics evolution
- Cash position e necessidades de capital
- Financial projections atualizadas

### 3. Strategic Update (3-5 páginas)
- Progresso contra prioridades estratégicas
- Mudanças no mercado e resposta
- Portfolio de iniciativas e priorização
- Decisões estratégicas para discussão

### 4. Operational Deep Dive (2-3 páginas)
- 1-2 temas operacionais relevantes
- Análise root cause de problemas
- Planos de ação e timeline

### 5. People & Culture (1-2 páginas)
- Talent metrics e hiring plan
- Organizational health indicators
- Leadership team updates

### 6. Risk & Compliance (1-2 páginas)
- Top risks com probabilidade e impacto
- Compliance status e issues
- Mitigations em andamento

### 7. Appendix
- Dados detalhados de suporte
- Glossário de métricas
- Minutes da reunião anterior

---

## Processo de Revisão

### Revisão em Camadas
1. **Self-review**: cada agent revisa sua seção individualmente
2. **Peer review**: agents revisam seções de outros agents para consistência
3. **Integration review**: COO verifica que a narrativa é coerente entre seções
4. **Final review**: Vision Chief aprova o documento completo
5. **Quality check**: verificação de dados, ortografia e formatação

### Critérios de Qualidade
- Dados são consistentes entre seções (mesmos números em diferentes contextos)
- Narrativa é honest e balanced (não excessivamente otimista ou pessimista)
- Decisões são claramente articuladas com opções e recomendações
- Linguagem é acessível para membros do Board sem jargão excessivo
- Visualizações são claras e self-explanatory

---

## Dry Run (D-2)

A sessão de preparação interna deve incluir:

- Apresentação completa como se fosse a reunião real
- Role-play de perguntas difíceis que o Board pode fazer
- Verificação de que todos os dados estão atualizados
- Alinhamento sobre mensagens-chave e narrativa
- Definição de quem responde a cada tipo de pergunta
- Preparação de materiais de backup para perguntas específicas

---

## Output e Armazenamento

- Board pack final armazenado em `data/board-packs/YYYY-QN-board-pack.md`
- Versão PDF gerada automaticamente para distribuição
- Minutes da reunião armazenadas em `data/board-packs/YYYY-QN-minutes.md`
- Action items do Board registrados no decision log
