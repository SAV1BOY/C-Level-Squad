# Run Weekly Business Review (WBR)

## Objetivo
Executar a Weekly Business Review, o ritmo operacional mais importante da organização. O WBR é uma sessão disciplinada de 60 minutos focada em métricas, anomalias e ações corretivas. Não é um status update — é um mecanismo de detecção precoce de problemas e tomada rápida de decisões.

## Agente Responsável
- **COO Agent** — Facilitação e disciplina do processo

## Agentes de Suporte
- **CFO Agent** — Financial metrics e variance analysis
- **CEO Agent** — Decisões estratégicas quando necessário
- **CTO Agent** — Engineering metrics e incident review
- **CPO Agent** — Product metrics e feature adoption
- **CMO Agent** — Growth e pipeline metrics
- **CHRO Agent** — People metrics (quando relevante)

## Pré-requisitos
1. Dashboard de métricas semanais atualizado até T-1 (dia anterior)
2. Cada área deve ter submetido seus dados até 24h antes do WBR
3. Anomalias detectadas devem ter root cause hypothesis documentada
4. Action items do WBR anterior devem ter status atualizado
5. Agenda publicada com pelo menos 12h de antecedência

## Processo (step-by-step)

### Fase 1: Preparação (Dia anterior ao WBR)
1. COO compila o WBR dashboard consolidado com todas as métricas semanais
2. Identificar automaticamente métricas fora do expected range (>1 standard deviation)
3. Para cada anomalia, solicitar ao owner uma hypothesis de root cause
4. Revisar action items do WBR anterior e coletar status updates
5. Definir agenda focada: métricas com anomalia vão primeiro, healthy metrics são skipped
6. Distribuir pre-read com dashboard e anomalias identificadas

### Fase 2: Execução do WBR (60 minutos)
7. **[0-5 min]** Open: status rápido dos action items do WBR anterior (done/not done)
8. **[5-15 min]** Financial pulse: revenue, cash, burn rate, pipeline — só anomalias
9. **[15-25 min]** Growth pulse: acquisition, activation, retention, expansion — só anomalias
10. **[25-35 min]** Product/Tech pulse: velocity, incidents, adoption — só anomalias
11. **[35-45 min]** Deep dive em 1-2 temas que requerem atenção executiva
12. **[45-55 min]** Decisions needed: itens que precisam de decisão hoje
13. **[55-60 min]** Action items: documentar owners e deadlines (max 72h para cada)

### Fase 3: Post-WBR (Mesmo dia)
14. Publicar WBR notes com métricas, anomalias discutidas e action items
15. Atualizar o action items tracker com novos itens e deadlines
16. Escalar itens que precisam de atenção imediata fora do WBR
17. Atualizar scorecards se necessário
18. Flag itens que podem precisar de escalação para MBR ou QBR

### Regras de Operação do WBR
19. Sem laptops abertos (exceto facilitador e note-taker)
20. Dados falam primeiro — não começar com opiniões, começar com números
21. Se o dado não está disponível, esse é o primeiro problema a resolver
22. Nenhuma métrica "verde" recebe airtime — foco exclusivo em vermelho e amarelo
23. Action items devem ter owner individual (não equipe) e deadline de max 72h
24. Se um action item do WBR anterior não foi completado, deve ter root cause

## Frameworks a Aplicar
- **Amazon WBR Model** — Input metrics over output metrics, variance analysis
- **Exception-Based Review** — Só discutir métricas fora do expected range
- **5 Whys** — Para root cause analysis de anomalias
- **RAPID Decision Framework** — Para decisões que precisam ser tomadas no WBR
- **Traffic Light System** — Red/Yellow/Green para quick visual triage
- **Leading vs Lagging Indicators** — Priorizar leading indicators na discussão

## Checklists de Qualidade
- [ ] Dashboard atualizado com dados até T-1
- [ ] Anomalias identificadas com hypothesis de root cause
- [ ] Action items do WBR anterior com status atualizado
- [ ] Agenda publicada 12h antes
- [ ] WBR completado em 60 minutos (hard stop)
- [ ] Máximo de 5 action items novos por WBR
- [ ] Cada action item tem owner individual e deadline ≤72h
- [ ] Notes publicadas no mesmo dia
- [ ] Escalations identificados e encaminhados
- [ ] Nenhuma métrica healthy consumiu tempo de discussão

## Template de Entrega
```markdown
# WBR Notes — [Date]

## Attendance
[Lista de participantes]

## Previous Action Items Status
| Item | Owner | Deadline | Status | Notes |
|------|-------|----------|--------|-------|

## Metrics Summary
### Financial Pulse
| Metric | Target | Actual | Variance | Status |
|--------|--------|--------|----------|--------|
| Weekly Revenue | | | | 🔴🟡🟢 |
| Cash Position | | | | 🔴🟡🟢 |
| Burn Rate | | | | 🔴🟡🟢 |

### Growth Pulse
| Metric | Target | Actual | Variance | Status |
|--------|--------|--------|----------|--------|
| New Customers | | | | 🔴🟡🟢 |
| Churn | | | | 🔴🟡🟢 |
| Pipeline | | | | 🔴🟡🟢 |

### Product/Tech Pulse
| Metric | Target | Actual | Variance | Status |
|--------|--------|--------|----------|--------|
| Deploy Frequency | | | | 🔴🟡🟢 |
| Incidents | | | | 🔴🟡🟢 |
| Feature Adoption | | | | 🔴🟡🟢 |

## Anomalies Discussed
### [Anomaly 1]
- **Metric:** [What's off]
- **Root Cause Hypothesis:** [Why]
- **Action:** [What we're doing]

## Decisions Made
| Decision | Rationale | Owner |
|----------|-----------|-------|

## New Action Items
| Item | Owner | Deadline |
|------|-------|----------|

## Escalations for MBR/QBR
[Items that need broader attention]
```

## Registries para Atualizar
- `registries/action-items.md` — Novos action items e status dos anteriores
- `registries/metrics-log.md` — Registro semanal de métricas chave
- `registries/decisions-log.md` — Decisões tomadas no WBR
- `registries/escalations.md` — Itens escalados para MBR ou QBR

## Critérios de Aceitação
1. WBR executado semanalmente sem falhas (exceto feriados nacionais)
2. Dashboard atualizado consistentemente até T-1
3. Duração máxima de 60 minutos respeitada
4. Action items com taxa de completion >80% na semana seguinte
5. Notes publicadas no mesmo dia do WBR
6. Anomalias têm root cause documentada antes da discussão

## Dependências e Handoffs
- **Recebe de:** Data team (dashboards), cada área (metrics input), previous WBR (action items)
- **Entrega para:** Action item owners, MBR (escalations), initiative teams
- **Cadência:** Semanal, mesmo dia e horário fixo (sugestão: segunda-feira 9h)
- **Escalation path:** Itens não resolvidos em 2 WBRs consecutivos escalam para MBR
- **Cancelamento:** WBR só pode ser cancelado pelo CEO, nunca simplesmente "pulado"
