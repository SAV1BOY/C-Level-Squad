# Workflow 12: Risk Review Cycle

## Objetivo

Estabelecer um ciclo periódico e disciplinado de revisão de riscos organizacionais, garantindo que o risk register esteja sempre atualizado, que riscos emergentes sejam identificados proativamente, que planos de mitigação estejam ativos e que o board receba reports de risco com frequência adequada. Este workflow transforma a gestão de risco de reativa para proativa, conectando riscos a decisões, métricas e ownership.

> **Princípio:** Risco não gerido é risco aceito por omissão. Todo risco deve ter dono, score, plano e revisão periódica.

---

## Agentes Envolvidos

| Agente | Papel no Workflow |
|--------|-------------------|
| **COO Orchestrator** | Owner do risk register, coordena ciclo de revisão, garante follow-up |
| **Vision Chief (CEO)** | Aprova risk appetite, decide sobre riscos estratégicos, reporta ao board |
| **CTO Architect** | Identifica e avalia riscos tecnológicos, de plataforma e de engenharia |
| **CIO Engineer** | Identifica riscos de dados, compliance (LGPD), sistemas e integrações |
| **CAIO Architect** | Identifica riscos de IA: bias, hallucination, data leakage, vendor lock-in |
| **CMO Architect** | Identifica riscos de mercado, marca, reputação e canais de aquisição |
| **CFO Strategist** | Quantifica impacto financeiro dos riscos, avalia cobertura de seguros |
| **Squad Coordinator** | Logística das sessões, consolidação de inputs, tracking de ações |

---

## Trigger (quando iniciar)

### Cadência Regular
- **Mensal:** Risk review operacional (COO + agentes relevantes)
- **Trimestral:** Risk review estratégico completo (todos os agentes)
- **Anual:** Risk appetite review e atualização de política de risco

### Triggers Ad-hoc
- Incidente SEV-1 ou SEV-2 resolvido → revisão de risco imediata
- Mudança significativa no mercado ou ambiente regulatório
- Nova bet estratégica aprovada que altera perfil de risco
- Entrada em novo mercado, lançamento de produto ou M&A
- Resultado de auditoria externa que identifique novos riscos

---

## Pré-condições

- [ ] Risk register atual disponível em `data/registries/risk-registry.yaml`
- [ ] Últimas métricas de KPIs atualizadas em `data/registries/metric-registry.yaml`
- [ ] Postmortems de incidentes recentes revisados (se houver)
- [ ] Inputs de cada agente sobre riscos do seu domínio coletados (máximo 48h antes)
- [ ] Relatório de status dos planos de mitigação em andamento
- [ ] Framework de scoring de risco definido e calibrado
- [ ] Acesso ao template: `templates/operational/action-items-tracker.md`

---

## Processo (step-by-step com decision points)

### FASE 1: Preparação e Coleta de Inputs (D-7 a D-2)

**Step 1.1 — Kick-off do Ciclo**
- COO Orchestrator envia solicitação de inputs a todos os agentes
- Cada agente deve reportar:
  - Novos riscos identificados no último período
  - Mudanças em riscos existentes (probabilidade ou impacto)
  - Status dos planos de mitigação sob sua responsabilidade
  - Riscos que podem ser removidos (mitigados ou irrelevantes)

**Step 1.2 — Coleta Estruturada por Domínio**

| Domínio | Agente Owner | Categorias de Risco |
|---------|-------------|-------------------|
| **Estratégico** | Vision Chief | Mercado, competição, tese invalidada, concentração de receita |
| **Operacional** | COO Orchestrator | Execução, processos, dependências, pessoas-chave |
| **Tecnológico** | CTO Architect | Plataforma, dívida técnica, SLOs, vendor de infra |
| **Dados / Compliance** | CIO Engineer | LGPD, governança de dados, integrações, sistemas legados |
| **IA** | CAIO Architect | Modelos em produção, bias, vendor lock-in, regulação de IA |
| **Mercado / Marca** | CMO Architect | Reputação, canais, churn, dependência de canal |
| **Financeiro** | CFO Strategist | Cash flow, unit economics, exposição cambial, inadimplência |
| **Pessoas** | COO Orchestrator | Retenção, key-person risk, cultura, burnout |

**Step 1.3 — Consolidação pelo Squad Coordinator**
- Compilar todos os inputs em formato padronizado
- Identificar riscos duplicados ou correlacionados
- Preparar agenda da sessão de revisão

### FASE 2: Scoring e Priorização (sessão de revisão)

**Step 2.1 — Metodologia de Scoring**

Cada risco é avaliado em duas dimensões:

**Probabilidade (P):**
| Score | Nível | Descrição |
|-------|-------|-----------|
| 1 | Raro | < 5% de chance no próximo trimestre |
| 2 | Improvável | 5-20% de chance |
| 3 | Possível | 20-50% de chance |
| 4 | Provável | 50-80% de chance |
| 5 | Quase certo | > 80% de chance |

**Impacto (I):**
| Score | Nível | Financeiro | Operacional | Reputação |
|-------|-------|-----------|-------------|-----------|
| 1 | Negligível | < R$ 10K | Sem impacto operacional | Sem impacto externo |
| 2 | Baixo | R$ 10K-100K | Degradação menor | Reclamações isoladas |
| 3 | Moderado | R$ 100K-500K | Interrupção parcial | Cobertura negativa local |
| 4 | Alto | R$ 500K-2M | Interrupção significativa | Cobertura negativa nacional |
| 5 | Crítico | > R$ 2M | Parada total | Crise pública / regulatória |

**Risk Score = P x I**

| Score | Classificação | Ação Requerida |
|-------|--------------|----------------|
| 1-4 | Baixo (verde) | Monitorar, revisar trimestralmente |
| 5-9 | Moderado (amarelo) | Plano de mitigação, revisar mensalmente |
| 10-15 | Alto (laranja) | Plano de mitigação ativo, revisar semanalmente |
| 16-25 | Crítico (vermelho) | Ação imediata, escalar para Vision Chief |

**Step 2.2 — Sessão de Scoring Coletivo**
- Cada risco é apresentado pelo agente owner
- Scoring é feito coletivamente para calibrar percepções
- Divergências > 2 pontos no score devem ser debatidas
- Vision Chief tem voto de minerva em caso de empate

> **Decision Point 1:** Para cada risco com score >= 10: plano de mitigação obrigatório existe? Se NÃO → criar plano com DRI e prazo antes de encerrar a sessão.

**Step 2.3 — Heat Map de Riscos**
- Gerar heat map visual (P x I) com todos os riscos mapeados
- Identificar clusters de risco (áreas com múltiplos riscos correlacionados)
- Comparar com heat map do ciclo anterior para identificar tendências

### FASE 3: Planos de Mitigação

**Step 3.1 — Definição de Estratégia por Risco**

| Estratégia | Quando Usar | Exemplo |
|-----------|-------------|---------|
| **Evitar** | Risco inaceitável, possível mudar o plano | Cancelar feature que viola LGPD |
| **Mitigar** | Reduzir probabilidade ou impacto | Redundância de infra, backup, seguro |
| **Transferir** | Passar o risco para terceiro | Seguro, outsourcing, SLA contratual |
| **Aceitar** | Risco dentro do appetite, custo de mitigação > impacto | Documentar e monitorar |

**Step 3.2 — Estrutura do Plano de Mitigação**

Para cada risco com score >= 10, o plano deve conter:

```yaml
risco:
  id: RISK-YYYY-NNN
  titulo: "[Descrição clara do risco]"
  categoria: "[Estratégico/Operacional/Tecnológico/...]"
  probabilidade: [1-5]
  impacto: [1-5]
  score: [P x I]
  owner: "[Agente DRI]"
  estrategia: "[Evitar/Mitigar/Transferir/Aceitar]"
  plano_mitigacao:
    acoes:
      - descricao: "[Ação específica]"
        dri: "[Pessoa]"
        prazo: "[Data]"
        status: "[Não iniciado/Em andamento/Concluído]"
    indicadores_antecedentes:
      - "[Métrica que sinaliza aumento do risco]"
    trigger_escalacao: "[Condição que dispara escalação]"
  revisao_proxima: "[Data]"
```

**Step 3.3 — Atribuição de Ownership**

> **Decision Point 2:** Todo risco com score >= 5 deve ter um DRI designado. Sem dono = sem accountability = sem mitigação.

- Owner é o agente com maior autoridade sobre o domínio do risco
- Owner é responsável por: monitorar, executar mitigação, reportar status
- COO Orchestrator é o "meta-owner" que garante que todos os owners estão atuando

### FASE 4: Board Reporting

**Step 4.1 — Preparação do Risk Report para Board**
- CFO Strategist consolida impacto financeiro agregado
- COO Orchestrator prepara resumo executivo
- Formato do report:

```
RISK REPORT — [Período]

1. RESUMO EXECUTIVO
   - Total de riscos mapeados: [N]
   - Riscos críticos (>=16): [N] → [lista]
   - Riscos altos (10-15): [N] → [lista top 5]
   - Novos riscos no período: [N]
   - Riscos eliminados/mitigados: [N]

2. TOP 5 RISCOS POR SCORE
   [Tabela com id, título, score, owner, status do plano]

3. TENDÊNCIAS
   - Riscos com score crescente: [lista]
   - Riscos com score decrescente: [lista]
   - Novos riscos emergentes: [lista]

4. IMPACTO FINANCEIRO AGREGADO
   - Exposição total estimada: R$ [valor]
   - Cobertura por seguros: R$ [valor]
   - Exposição líquida: R$ [valor]

5. PLANOS DE MITIGAÇÃO — STATUS
   [Tabela com ação, DRI, prazo, status]

6. RECOMENDAÇÕES
   [Decisões que precisam de aprovação do board]
```

**Step 4.2 — Revisão e Aprovação**
- Vision Chief revisa e aprova o report antes de enviar ao board
- Informações sensíveis são classificadas adequadamente
- Report é incluído no board pack via `workflows/17-board-prep-and-delivery.md`

### FASE 5: Tracking e Follow-up

**Step 5.1 — Monitoramento Contínuo**
- COO Orchestrator revisa status dos planos de mitigação semanalmente
- Action items de mitigação são incluídos na WBR
- Indicadores antecedentes são monitorados nos dashboards

**Step 5.2 — Revisão de Efetividade**
- Na próxima revisão mensal, avaliar:
  - Planos de mitigação estão sendo executados no prazo?
  - Score dos riscos mudou? Por quê?
  - Novos riscos surgiram que não foram previstos?
  - Algum risco se materializou? Aprendizados?

> **Decision Point 3:** Se um risco se materializou → acionar `workflows/11-incident-response-exec.md`. Se a revisão mostra gaps sistemáticos → acionar revisão de processo de gestão de risco.

---

## Quality Gates

### Gate 1: Completude do Risk Register
- [ ] Todos os domínios de risco foram revisados por seus agentes owners
- [ ] Cada risco tem ID único, descrição clara, owner e scoring
- [ ] Nenhum risco com score >= 10 está sem plano de mitigação
- [ ] Risk register está atualizado em `data/registries/risk-registry.yaml`
- [ ] Referência: `checklists/risk-register-quality.md`

### Gate 2: Qualidade dos Planos de Mitigação
- [ ] Cada plano tem ações específicas com DRI e prazo
- [ ] Indicadores antecedentes definidos para riscos altos e críticos
- [ ] Trigger de escalação definido para cada risco crítico
- [ ] Estratégia de mitigação é proporcional ao score do risco

### Gate 3: Board Reporting
- [ ] Report segue formato padronizado com dados atualizados
- [ ] Impacto financeiro quantificado pelo CFO Strategist
- [ ] Vision Chief revisou e aprovou o report
- [ ] Recomendações incluem ask claro para o board
- [ ] Referência: `checklists/board-prep-quality.md`

### Gate 4: RalphLoop Integration
- [ ] Riscos materializados foram analisados (o que aprendemos?)
- [ ] Efetividade das mitigações anteriores foi avaliada
- [ ] Processo de risk review foi auto-avaliado (o que melhorar?)
- [ ] Lições registradas em `data/registries/lessons-learned.yaml`
- [ ] Referência: `checklists/ralphloop-quality.md`

---

## Outputs / Artefatos

| Artefato | Formato | Responsável | Destino |
|----------|---------|-------------|---------|
| Risk Register atualizado | YAML | COO Orchestrator | `data/registries/risk-registry.yaml` |
| Heat Map de riscos | Visual (markdown table) | Squad Coordinator | Anexo ao risk report |
| Board Risk Report | Markdown | COO + CFO Strategist | Board pack |
| Planos de mitigação | YAML | Agentes owners | `data/registries/risk-registry.yaml` |
| Ata da sessão de revisão | Markdown | Squad Coordinator | `data/meeting-minutes/` |
| Action items de mitigação | YAML | COO Orchestrator | `data/registries/initiative-registry.yaml` |

---

## Registries Atualizados

- `data/registries/risk-registry.yaml` — Riscos atualizados com novo scoring e planos
- `data/registries/decision-registry.yaml` — Decisões de mitigação e aceitação de risco
- `data/registries/initiative-registry.yaml` — Ações de mitigação como iniciativas
- `data/registries/lessons-learned.yaml` — Aprendizados de riscos materializados
- `data/registries/metric-registry.yaml` — Métricas de risk management (total exposure, mitigação %)

---

## Próximos Passos

1. Planos de mitigação entram no tracking semanal da WBR (`workflows/04-wbr-loop.md`)
2. Risk report é incluído na preparação do board (`workflows/17-board-prep-and-delivery.md`)
3. Riscos materializados alimentam postmortem (`workflows/20-postmortem-and-learning.md`)
4. Riscos de IA alimentam o ciclo de evals (`workflows/15-evals-and-guardrails-loop.md`)
5. Novos riscos estratégicos são incorporados no planejamento trimestral (`workflows/06-qbr-loop.md`)
6. Próximo ciclo de risk review é agendado conforme cadência definida

---

## Cross-squad Handoffs

| Squad | Handoff | Direção | SLA |
|-------|---------|---------|-----|
| **Cybersecurity Squad** | Risk assessments de segurança, vulnerabilidades, compliance status | Cyber → C-Level | 24h para assessments |
| **Data Squad** | Dados de monitoramento, dashboards de risco, métricas de saúde | Data → C-Level | 48h para análises |
| **Advisory Board** | Orientação sobre risk appetite, riscos regulatórios, estratégicos | C-Level ↔ Advisory | 1 semana para orientações |
| **Brand Squad** | Riscos reputacionais, monitoramento de marca, sentiment analysis | Brand → C-Level | 48h para reports |
| **Traffic Squad** | Riscos de dependência de canal, mudanças em plataformas | Traffic → C-Level | 48h para alertas |
| **Design Squad** | Riscos de UX, acessibilidade, compliance de design | Design → C-Level | 48h para assessments |

---

## Referências

- `templates/operational/action-items-tracker.md` — Template do risk register
- `checklists/risk-register-quality.md` — Checklist de qualidade do risk register
- `checklists/governance-risk/crisis-response-quality.md` — Checklist de resposta a crise
- `frameworks/operating-system/escalation-ladders.md` — Escadas de escalação
- `frameworks/coo-orchestrator/coo-bottleneck-theory.md` — Teoria de gargalos
