# Checklist de Qualidade de Postmortem (Postmortem Quality)

## Propósito
Garantir que todo postmortem (análise pós-incidente ou pós-projeto) capture aprendizados
genuínos, atribua ações concretas e agende follow-up efetivo. Este checklist transforma
falhas e incidentes em oportunidades de melhoria sistêmica, prevenindo que os mesmos
erros se repitam e fortalecendo a cultura de aprendizado organizacional.

## Quando Aplicar
- Após todo incidente classificado como severidade alta ou crítica
- Após o encerramento de projetos estratégicos (sucesso ou fracasso)
- Após missed targets significativos em OKRs ou métricas de negócio
- Após crises que ativaram o protocolo de crisis response
- Sempre que um evento gera aprendizados relevantes para a organização

## Agente Responsável
- **Primário:** O líder da iniciativa ou incidente (incident commander, project owner)
- **Secundário:** Chief of Staff para garantir padronização e follow-up
- **Revisor:** O sponsor executivo da área afetada

## Checklist

### Seção 1 — Preparação do Postmortem
- [ ] Item 1: O postmortem foi agendado dentro de 2 semanas após o evento
- [ ] Item 2: Todos os envolvidos diretamente no evento foram convidados
- [ ] Item 3: A regra de blameless (sem culpabilização) foi comunicada previamente a todos
- [ ] Item 4: Timeline dos eventos foi reconstruído factualmente antes da reunião
- [ ] Item 5: Dados e métricas relevantes foram coletados e preparados
- [ ] Item 6: Um facilitador neutro foi designado (não o responsável direto)
- [ ] Item 7: Template de postmortem foi distribuído para pré-preenchimento
- [ ] Item 8: Tempo suficiente foi alocado (mínimo 90 minutos para incidentes complexos)

### Seção 2 — Captura de Aprendizados (Learnings Capture)
- [ ] Item 9: O que aconteceu está descrito factualmente sem interpretação ou blame
- [ ] Item 10: O timeline detalhado de eventos com timestamps está documentado
- [ ] Item 11: Root cause analysis (5 Whys ou Fishbone) foi conduzido formalmente
- [ ] Item 12: A root cause principal está identificada (não apenas os sintomas)
- [ ] Item 13: Causas contribuintes (contributing factors) estão listadas separadamente
- [ ] Item 14: O que funcionou bem está documentado (não apenas o que falhou)
- [ ] Item 15: O que poderia ter sido detectado antes (early warning signs) está identificado
- [ ] Item 16: O impacto total (financeiro, operacional, reputacional, em clientes) está quantificado
- [ ] Item 17: Padrões ou similaridades com incidentes anteriores foram identificados
- [ ] Item 18: Cada participante teve oportunidade de compartilhar sua perspectiva

### Seção 3 — Ações Atribuídas (Action Items)
- [ ] Item 19: Cada learning tem pelo menos uma ação concreta associada
- [ ] Item 20: Cada ação tem um owner único e específico (não "o time" genérico)
- [ ] Item 21: Cada ação tem deadline realista definido
- [ ] Item 22: Ações estão classificadas como preventivas (evitar recorrência) ou corretivas (resolver imediato)
- [ ] Item 23: Ações foram priorizadas por impacto e urgência
- [ ] Item 24: Ações que dependem de outros squads foram comunicadas e aceitas
- [ ] Item 25: O esforço necessário para cada ação foi estimado (small, medium, large)
- [ ] Item 26: Ações foram inseridas no sistema de tracking oficial (não apenas nas notas)
- [ ] Item 27: Nenhuma ação crítica ficou sem owner ou deadline

### Seção 4 — Follow-Up Estruturado
- [ ] Item 28: Data de follow-up review está agendada (4-6 semanas após o postmortem)
- [ ] Item 29: O Chief of Staff ou owner do processo monitora progresso das ações
- [ ] Item 30: Status de cada ação é atualizado semanalmente até conclusão
- [ ] Item 31: Ações atrasadas são escaladas após 1 semana de atraso
- [ ] Item 32: A reunião de follow-up verifica se ações foram efetivas (não apenas concluídas)
- [ ] Item 33: Se ações não resolveram o problema, novas ações são definidas
- [ ] Item 34: O postmortem é oficialmente fechado somente quando todas as ações estão concluídas

### Seção 5 — Disseminação de Aprendizados
- [ ] Item 35: O documento de postmortem está acessível no repositório central
- [ ] Item 36: Um resumo executivo foi compartilhado com o C-Level Squad
- [ ] Item 37: Learnings relevantes foram compartilhados com squads que podem se beneficiar
- [ ] Item 38: Se o learning é sistêmico, foi adicionado ao playbook ou checklist relevante
- [ ] Item 39: O postmortem é indexado por tema para facilitar busca futura
- [ ] Item 40: Novos membros do time são direcionados a ler postmortems relevantes da área

### Seção 6 — Cultura de Postmortem
- [ ] Item 41: A organização conduz postmortems consistentemente (não apenas após falhas graves)
- [ ] Item 42: A cultura blameless é respeitada na prática (não apenas no discurso)
- [ ] Item 43: Liderança participa de postmortems como aprendiz, não como juiz
- [ ] Item 44: Postmortems de sucesso também são conduzidos (o que fizemos certo?)
- [ ] Item 45: A taxa de conclusão de action items de postmortems anteriores é monitorada
- [ ] Item 46: Métricas de recorrência de incidentes similares são trackeadas

## Critérios de Aprovação
O postmortem é considerado de qualidade quando:

1. **Root cause analysis foi conduzido formalmente (Seção 2, Item 11)**
2. **100% das ações têm owner e deadline (Seção 3)**
3. **Follow-up review está agendado (Seção 4, Item 28)**
4. **O documento está no repositório central e acessível (Seção 5)**
5. **A cultura blameless foi respeitada durante todo o processo**
6. **Pelo menos 80% das ações de postmortems anteriores foram concluídas**
7. **O sponsor executivo aprovou a análise e as ações propostas**

## O que Fazer se Falhar
Se o postmortem não atinge os critérios:

1. **Refazer a sessão:** Se a análise foi superficial, agendar sessão adicional com mais profundidade
2. **External facilitator:** Se blame está presente, trazer facilitador externo
3. **Action forcing:** Se ações estão vagas, dedicar tempo para torná-las específicas
4. **Accountability reset:** Se follow-up não acontece, escalar para o sponsor
5. **Training:** Oferecer treinamento de root cause analysis e facilitação de postmortems
6. **Leadership example:** CEO e C-Level devem participar e modelar comportamento blameless
7. **Process automation:** Automatizar lembretes de follow-up e tracking de ações
8. **Retrospectiva do processo:** Conduzir retro sobre por que postmortems não estão funcionando

## Referências
- Google — SRE Book, "Postmortem Culture: Learning from Failure"
- Etsy — "Blameless PostMortems and a Just Culture"
- Sidney Dekker — "The Field Guide to Understanding Human Error"
- PagerDuty — Postmortem Guide and Templates
- Framework interno de Incident Management (documento em /execution/)
- Template de Postmortem (documento em /templates/postmortem-template.md)
- Repositório de postmortems anteriores (link: /postmortems/)
