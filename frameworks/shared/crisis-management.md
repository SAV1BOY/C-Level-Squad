# Framework de Gestão de Crise Compartilhada

## Objetivo

Este framework estabelece o protocolo unificado de gestão de crises para todo o C-Level Squad.
Todas as áreas — financeira, tecnológica, de pessoas e de IA — seguem este mesmo fluxo,
garantindo coordenação, velocidade e comunicação consistente durante eventos críticos.

## Classificação de Severidade

### Nível 1 — Crítico (War Room Imediato)
- Indisponibilidade total de sistemas em produção
- Vazamento confirmado de dados sensíveis
- Fraude financeira detectada
- Risco iminente de insolvência
- Incidente regulatório com prazo legal inferior a 24 horas

### Nível 2 — Alto (Resposta em até 2 horas)
- Degradação severa de performance (>50% dos usuários afetados)
- Perda de cliente estratégico (top 10 em receita)
- Falha em auditoria externa com achados materiais
- Demissão inesperada de liderança-chave
- Vulnerabilidade de segurança com exploit ativo

### Nível 3 — Moderado (Resposta em até 24 horas)
- Atraso significativo em entrega de projeto estratégico
- Desvio orçamentário acima de 15%
- Turnover acima do benchmark por dois meses consecutivos
- Incidente de marca em redes sociais com viralização

### Nível 4 — Baixo (Monitoramento Ativo)
- Indicadores de alerta precoce fora da faixa
- Reclamações recorrentes sem resolução
- Dependência técnica identificada sem mitigação

## Protocolo de Ativação

### Passo 1 — Detecção e Triagem
1. Qualquer membro do squad pode acionar o protocolo de crise
2. O acionador deve preencher o template de incidente com informações iniciais
3. O coordenador do squad faz a triagem e classifica a severidade
4. Notificação automática é disparada para os stakeholders relevantes

### Passo 2 — Formação do Time de Resposta
- **Nível 1:** Todos os C-levels + coordenador + assessoria jurídica
- **Nível 2:** C-levels diretamente envolvidos + coordenador
- **Nível 3:** Líder da área afetada + coordenador
- **Nível 4:** Líder da área afetada com reporte semanal ao coordenador

### Passo 3 — Contenção Imediata
1. Isolar o problema para evitar propagação
2. Documentar todas as ações tomadas com timestamp
3. Estabelecer canal de comunicação dedicado (war room virtual ou físico)
4. Definir porta-voz único para comunicação externa

### Passo 4 — Investigação e Diagnóstico
1. Levantar timeline completa do incidente
2. Identificar causa raiz (ou causas contribuintes)
3. Mapear impacto em todas as áreas (financeiro, operacional, reputacional, legal)
4. Documentar evidências de forma preservável

### Passo 5 — Resolução e Recuperação
1. Implementar correção definitiva ou workaround temporário documentado
2. Validar que a correção não introduz novos riscos
3. Restaurar operações normais de forma gradual e monitorada
4. Comunicar resolução a todos os stakeholders

### Passo 6 — Post-Mortem
1. Realizar sessão de post-mortem em até 5 dias úteis após a resolução
2. Documentar lições aprendidas sem atribuição de culpa individual
3. Definir ações preventivas com responsáveis e prazos
4. Atualizar este framework se necessário

## Matriz de Comunicação

| Audiência         | Canal               | Frequência (Nível 1) | Responsável         |
|-------------------|----------------------|-----------------------|---------------------|
| Board             | E-mail + call        | A cada 4 horas        | CEO / Coordenador   |
| Investidores      | E-mail formal        | A cada 12 horas       | CFO                 |
| Clientes          | Status page + e-mail | A cada 2 horas        | CIO                 |
| Colaboradores     | Slack + all-hands    | A cada 6 horas        | CHRO                |
| Imprensa          | Nota oficial         | Conforme necessidade  | Assessoria          |
| Reguladores       | Ofício formal        | Conforme exigência    | Jurídico + CFO      |

## Templates Obrigatórios

### Template de Acionamento
```
INCIDENTE #[número]
Data/Hora detecção: [timestamp]
Severidade estimada: [1-4]
Descrição resumida: [máximo 3 linhas]
Áreas impactadas: [lista]
Acionador: [nome e cargo]
Ações imediatas tomadas: [lista]
```

### Template de Atualização
```
ATUALIZAÇÃO #[sequencial] — INCIDENTE #[número]
Data/Hora: [timestamp]
Status atual: [Contenção | Investigação | Resolução | Encerrado]
Progresso desde última atualização: [descrição]
Próximos passos: [lista com ETA]
Riscos pendentes: [lista]
```

## Indicadores de Efetividade

- **Tempo médio de detecção (MTTD):** meta < 15 minutos para Nível 1
- **Tempo médio de resposta (MTTR):** meta < 30 minutos para Nível 1
- **Tempo médio de resolução:** meta < 4 horas para Nível 1
- **Taxa de recorrência:** meta < 5% de incidentes repetidos
- **Completude de post-mortem:** meta 100% em até 5 dias úteis

## Revisão do Framework

Este framework deve ser revisado trimestralmente pelo coordenador do squad,
com input de todos os C-levels. Simulações de crise (tabletop exercises) devem
ser realizadas semestralmente para validar a efetividade dos protocolos.
