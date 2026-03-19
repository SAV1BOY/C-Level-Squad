# ITIL Light — ITIL Essencial para Startups e Scale-ups

> **Domínio:** IT & Information
> **Autor de referência:** AXELOS / ITIL 4 Foundation, adaptação lean pelo C-Level Squad
> **Uso primário:** Implementar gestão de serviços de TI sem a burocracia do ITIL completo.
> **Agente responsável:** cio-engineer

---

## Origem e Contexto

ITIL (Information Technology Infrastructure Library) é o framework mais adotado globalmente para gestão de serviços de TI (IT Service Management — ITSM). A versão ITIL 4 (2019) modernizou o framework com princípios ágeis, mas o ITIL completo tem 34 práticas de gestão — overkill para startups e scale-ups.

O ITIL Light do C-Level Squad seleciona as **4 práticas essenciais** que toda empresa de tecnologia precisa, independente do tamanho:

1. **Incident Management:** Restaurar serviço normal o mais rápido possível quando algo quebra.
2. **Problem Management:** Identificar e eliminar a causa-raiz de incidentes recorrentes.
3. **Change Management:** Gerenciar mudanças em produção para minimizar risco.
4. **Service Request Management:** Atender solicitações padronizadas (acesso, provisionamento, etc.).

O princípio do ITIL Light: **adotar o mínimo necessário para ter controle, sem criar burocracia que mate a velocidade.** À medida que a organização cresce, mais práticas podem ser adicionadas incrementalmente.

---

## Quando Usar

- A partir de 20+ funcionários ou 10+ engenheiros — abaixo disso, processos informais são suficientes.
- Quando incidentes são frequentes e não há processo claro de resposta.
- Quando o mesmo problema recorre e ninguém investiga root-cause.
- Quando mudanças em produção causam falhas frequentes (change failure rate alto).
- Quando solicitações de TI (acessos, equipamentos) ficam perdidas em mensagens de Slack.
- Como complemento ao SRE (`frameworks/engineering-tech/sre-basics.md`) — ITIL foca em processo, SRE em engenharia.

---

## Quando NÃO Usar

- Em empresas de 1-5 pessoas — processo formal é overhead.
- Como burocracia — se o processo impede a resolução do problema, o processo está errado.
- Para controlar engenheiros — ITIL Light é para AJUDAR, não para policiar.
- O ITIL completo (34 práticas) — a menos que seja empresa regulada (banco, saúde) com requisitos de compliance.

---

## Estrutura / Modelo

### As 4 Práticas Essenciais

```
┌─────────────────────────────────────────────────────────────────────┐
│                    ITIL LIGHT — 4 PRÁTICAS                           │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  1. INCIDENT MANAGEMENT          2. PROBLEM MANAGEMENT              │
│  ┌──────────────────────┐       ┌──────────────────────┐           │
│  │ Algo quebrou → Ação  │       │ Por que quebra? →    │           │
│  │ imediata → Restaurar │       │ Root-cause analysis →│           │
│  │ serviço              │       │ Eliminar causa-raiz  │           │
│  └──────────────────────┘       └──────────────────────┘           │
│                                                                      │
│  3. CHANGE MANAGEMENT            4. SERVICE REQUEST MGMT            │
│  ┌──────────────────────┐       ┌──────────────────────┐           │
│  │ Mudança planejada →  │       │ Solicitação → Catálo-│           │
│  │ Avaliar risco →      │       │ go → Aprovação auto- │           │
│  │ Aprovar → Executar → │       │ mática → Entrega     │           │
│  │ Verificar            │       │                      │           │
│  └──────────────────────┘       └──────────────────────┘           │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

---

## Processo de Aplicação (step-by-step)

### Prática 1: Incident Management

**Objetivo:** Restaurar serviço normal o mais rápido possível. Foco em MITIGAÇÃO, não em root-cause (isso é Problem Management).

**Processo simplificado:**
1. **Detectar:** Alerta automático (monitoring) ou report de usuário.
2. **Classificar:** Severidade (SEV1-SEV4 conforme `frameworks/operating-system/escalation-ladders.md`).
3. **Designar:** On-call engineer assume como DRI do incidente.
4. **Comunicar:** Stakeholders informados conforme severidade.
5. **Mitigar:** Restaurar serviço (rollback, failover, workaround).
6. **Resolver:** Fix definitivo (pode ser pós-mitigação).
7. **Postmortem:** Para SEV1/SEV2, blameless postmortem em 48h.

**Ferramentas mínimas:**
- Alerting: PagerDuty, OpsGenie ou Grafana OnCall.
- Communication: Canal de Slack dedicado (#incidents).
- Tracking: Spreadsheet ou tool simples (Notion, Linear).
- Postmortem: Template padrão em repositório.

### Prática 2: Problem Management

**Objetivo:** Identificar e eliminar a causa-raiz de incidentes recorrentes. Diferença crítica: incident = apagar o fogo. Problem = prevenir o próximo fogo.

**Processo simplificado:**
1. **Identificar:** Analisar trends de incidentes. O mesmo tipo de incidente ocorreu 3+ vezes?
2. **Registrar:** Criar problem ticket linkado aos incidents relacionados.
3. **Investigar:** Root-cause analysis (5 Whys, Ishikawa, ou análise de timeline).
4. **Resolver:** Implementar fix que elimina a causa-raiz (pode ser tech debt, process change, ou architectural decision).
5. **Verificar:** O tipo de incidente parou de recorrer?

**Cadência:** Revisão mensal (MBR) dos top-5 problems abertos. Alocação de engineering time para problem resolution.

### Prática 3: Change Management

**Objetivo:** Gerenciar mudanças em produção para minimizar risco. NÃO é burocracia de aprovação — é risk management inteligente.

**Classificação de changes:**

| Tipo | Exemplo | Aprovação | Processo |
|------|---------|-----------|----------|
| **Standard** | Deploy de feature com CI/CD e feature flag | Automática (pipeline) | Pipeline padrão |
| **Normal** | Migração de database, mudança de infra | Peer review + Tech Lead | Change ticket + rollback plan |
| **Emergency** | Hotfix para SEV1 em produção | Retroativa (post-deploy) | Fix → Deploy → Review depois |

**Regra:** 80% dos changes devem ser Standard (automáticos via pipeline). Se muitos são Normal, a automação está falhando.

### Prática 4: Service Request Management

**Objetivo:** Atender solicitações padronizadas de forma eficiente e rastreável.

**Exemplos de service requests:**
- Acesso a ferramenta/sistema (onboarding).
- Provisionamento de ambiente de desenvolvimento.
- Criação de repositório.
- Solicitação de equipamento.
- Reset de credenciais.

**Processo simplificado:**
1. **Catálogo de serviços:** Lista de solicitações disponíveis com SLA de atendimento.
2. **Self-service:** Automatizar o máximo possível (ex.: acesso via RBAC group, não ticket manual).
3. **Tracking:** Ferramenta de ticketing (Jira, Linear, Freshservice) para rastreabilidade.
4. **SLA:** Tempo máximo de atendimento por tipo (ex.: acesso = 4h úteis, equipamento = 3 dias úteis).

---

## Exemplos Práticos

### Exemplo: Scale-up SaaS (80 funcionários, 30 engenheiros)

**Implementação ITIL Light:**

| Prática | Ferramenta | SLA | DRI |
|---------|-----------|-----|-----|
| Incident | PagerDuty + Slack #incidents | SEV1: 15min response | On-call engineer |
| Problem | Linear (label: problem) | Review mensal na MBR | SRE Lead |
| Change | GitHub PR + CI/CD pipeline | Standard: auto. Normal: 24h review. | Tech Lead do squad |
| Service Request | Freshservice | Acesso: 4h. Equipamento: 3d. | IT Manager |

**Métricas na WBR:**
- # incidents por semana, por severidade.
- MTTR por severidade.
- Change failure rate.
- Service request backlog e SLA compliance.

---

## Armadilhas Comuns

1. **ITIL completo para startup:** Implementar 34 práticas em empresa de 50 pessoas é suicídio burocrático. 4 práticas são suficientes.
2. **Change management como gatekeeper:** Se todo deploy precisa de "change approval board", a velocidade morre. Automatizar Standard changes.
3. **Incident sem postmortem:** Apagar fogo sem aprender é garantir que o fogo volta. Postmortem para SEV1/SEV2 é obrigatório.
4. **Problem management inexistente:** O incident se repete todo mês e ninguém investiga por quê. Alocar tempo dedicado.
5. **Service request via Slack DM:** Solicitações informais não são rastreáveis. Criar catálogo mínimo com self-service.
6. **Métricas sem ação:** Medir # incidents sem plano de redução é vanity metric. Cada métrica precisa de target e ação.
7. **Blame culture em incidents:** Se as pessoas são punidas por falhas, elas esconderão falhas. Blameless é essencial.
8. **Ignorar change risk:** "Sempre deployamos direto" até o dia que um deploy derruba o sistema. Change management é seguro de riscos.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/engineering-tech/sre-basics.md` | SRE e ITIL se complementam: SRE foca em engenharia de confiabilidade, ITIL em processo. |
| `frameworks/engineering-tech/dora-metrics.md` | Change failure rate é tanto DORA metric quanto ITIL metric. |
| `frameworks/engineering-tech/platform-engineering.md` | Plataforma automatiza Standard changes e service requests (self-service). |
| `frameworks/operating-system/escalation-ladders.md` | Severidade de incidents alinha com escalation ladder. |
| `frameworks/operating-system/wbr-mbr-qbr.md` | Incident/problem metrics na WBR. Problem review na MBR. |
| `frameworks/it-information/data-governance-lite.md` | Data incidents (breach, corruption) seguem incident management. |
| `checklists/incident-communication-quality.md` | Checklist para comunicação durante incidents. |

---

## Referências

- AXELOS. (2019). *ITIL Foundation: ITIL 4 Edition*. TSO.
- AXELOS. (2019). *ITIL 4: Create, Deliver and Support*. TSO.
- Google SRE. *Site Reliability Engineering*. (Complementar: engineering approach.)
- Kim, G. et al. (2016). *The DevOps Handbook*. IT Revolution. (DevOps + ITSM integration.)
- Forsgren, N. et al. (2018). *Accelerate*. IT Revolution. (Impacto de change management em DORA.)
