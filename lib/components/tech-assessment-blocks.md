# Tech Assessment Blocks — Blocos Reutilizáveis para Avaliação Técnica

> Blocos padronizados para avaliações técnicas em documentos de liderança.
> Use em board decks, planejamento estratégico, due diligence e reviews trimestrais.

---

## 1. Bloco: Saúde Técnica do Produto

### Template
```markdown
## Saúde Técnica — Scorecard

| Dimensão | Score (1-5) | Tendência | Comentário |
|----------|:-----------:|:---------:|------------|
| Confiabilidade (uptime) | [1-5] | [Tendência] | [SLA: X%, uptime real: X%] |
| Performance (latência) | [1-5] | [Tendência] | [p50: Xms, p99: Xms] |
| Escalabilidade | [1-5] | [Tendência] | [Capacidade atual vs projetada] |
| Segurança | [1-5] | [Tendência] | [Vulnerabilidades abertas, compliance] |
| Dívida técnica | [1-5] | [Tendência] | [% do tempo gasto com tech debt] |
| Observabilidade | [1-5] | [Tendência] | [Cobertura de monitoramento] |
| DevEx (developer experience) | [1-5] | [Tendência] | [Tempo de build, deploy, feedback] |
| Qualidade de código | [1-5] | [Tendência] | [Cobertura de testes, code smells] |

**Score geral:** [X.X / 5.0]
**Áreas críticas:** [Top 2 com score mais baixo]
```

---

## 2. Bloco: Métricas de Engenharia (DORA)

### Template
```markdown
## Métricas DORA

| Métrica | Valor Atual | Meta | Benchmark (Elite) | Status |
|---------|------------|------|-------------------|--------|
| Deployment Frequency | [X/dia ou semana] | [X/dia] | [Múltiplos/dia] | [Status] |
| Lead Time for Changes | [X horas/dias] | [<X horas] | [<1 hora] | [Status] |
| Change Failure Rate | [X%] | [<X%] | [<15%] | [Status] |
| Time to Restore (MTTR) | [X horas] | [<X horas] | [<1 hora] | [Status] |

**Nível DORA geral:** [Elite / High / Medium / Low]
**Principal gargalo:** [O que mais impacta as métricas negativamente]
```

---

## 3. Bloco: Stack Tecnológico

### Template
```markdown
## Stack Tecnológico

| Camada | Tecnologia | Versão | Status | Risco |
|--------|-----------|--------|--------|-------|
| Frontend | [React / Vue / etc.] | [vX.X] | [Atual / Defasado] | [Baixo/Médio/Alto] |
| Backend | [Go / Node / Python] | [vX.X] | [Status] | [Risco] |
| Banco de Dados | [PostgreSQL / MongoDB] | [vX.X] | [Status] | [Risco] |
| Cache | [Redis / Memcached] | [vX.X] | [Status] | [Risco] |
| Message Broker | [Kafka / RabbitMQ] | [vX.X] | [Status] | [Risco] |
| Cloud | [AWS / GCP / Azure] | — | [Multi-region / Single] | [Risco] |
| CI/CD | [GitHub Actions / etc.] | — | [Status] | [Risco] |
| Observabilidade | [Datadog / Grafana] | — | [Status] | [Risco] |

**Vendor lock-in:** [Baixo / Médio / Alto — justificativa]
**Custo mensal de infra:** R$ [X]
**Custo por cliente:** R$ [X]
```

---

## 4. Bloco: Dívida Técnica

### Template
```markdown
## Inventário de Dívida Técnica

| Item | Severidade | Impacto se Não Tratado | Esforço para Resolver | Prioridade |
|------|:---------:|----------------------|:---:|:---------:|
| [Item 1 — ex: "Monolito precisa de decomposição"] | [Crítico] | [Limita velocidade de deploy] | [Alto — 6 meses] | [P1] |
| [Item 2 — ex: "Testes end-to-end frágeis"] | [Alto] | [Releases com medo] | [Médio — 2 meses] | [P1] |
| [Item 3 — ex: "Schema do DB não normalizado"] | [Médio] | [Performance degradando] | [Alto — 4 meses] | [P2] |

**% do tempo de eng alocado para tech debt:** [X%] (recomendado: 15-20%)
**Tendência:** [Acumulando / Estável / Reduzindo]
**Custo estimado para zerar backlog crítico:** [R$ X / N pessoa-meses]
```

---

## 5. Bloco: Avaliação de Segurança

### Template
```markdown
## Postura de Segurança

| Controle | Status | Última Auditoria | Próxima Ação |
|----------|:------:|:----------------:|-------------|
| Autenticação (MFA) | [Implementado / Parcial / Não] | [Data] | [Ação] |
| Criptografia em trânsito | [Sim / Parcial] | [Data] | [Ação] |
| Criptografia em repouso | [Sim / Parcial / Não] | [Data] | [Ação] |
| Gestão de secrets | [Vault / Env vars / Hardcoded] | [Data] | [Ação] |
| SAST/DAST em CI | [Sim / Parcial / Não] | [Data] | [Ação] |
| Pen test externo | [Data do último] | [Frequência] | [Próximo em data] |
| SOC 2 / ISO 27001 | [Certificado / Em progresso / Não] | [Data] | [Ação] |
| LGPD compliance | [Compliant / Parcial / Não] | [Data] | [Ação] |
| Incident response plan | [Documentado / Testado / Não] | [Data] | [Ação] |

**Vulnerabilidades abertas:** Críticas: [N] | Altas: [N] | Médias: [N]
**Tempo médio de correção:** Críticas: [X dias] | Altas: [X dias]
```

---

## 6. Bloco: Arquitetura de Alto Nível

### Template
```markdown
## Arquitetura Atual

```
[Usuários] → [CDN/WAF] → [Load Balancer]
                              │
              ┌───────────────┼───────────────┐
              ▼               ▼               ▼
         [API Gateway]  [Web App]       [Workers]
              │               │               │
              ▼               ▼               ▼
         [Service A]    [Service B]     [Service C]
              │               │               │
              ▼               ▼               ▼
         [DB Primary]   [DB Replica]    [Queue/Kafka]
                              │
                              ▼
                         [Data Lake]
```

**Pontos de falha únicos (SPOF):** [Listar]
**Gargalos conhecidos:** [Listar]
**Plano de evolução:** [Resumo da arquitetura alvo]
```

---

## 7. Bloco: Incidentes e Confiabilidade

### Template
```markdown
## Confiabilidade — Últimos [N] Meses

| Métrica | M1 | M2 | M3 | Média | Meta |
|---------|:---:|:---:|:---:|:---:|:---:|
| Uptime | [X%] | [X%] | [X%] | [X%] | [99.9%] |
| Incidentes P0 | [N] | [N] | [N] | [N/mês] | [0] |
| Incidentes P1 | [N] | [N] | [N] | [N/mês] | [<2] |
| MTTR (P0) | [Xh] | [Xh] | [Xh] | [Xh] | [<1h] |
| Error budget restante | [X%] | [X%] | [X%] | — | [>0%] |

**Top 3 causas de incidentes:**
1. [Causa 1 — frequência — ação]
2. [Causa 2 — frequência — ação]
3. [Causa 3 — frequência — ação]
```

---

## 8. Bloco: Capacidade e Escala

### Template
```markdown
## Capacidade e Projeção de Escala

| Recurso | Uso Atual | Capacidade Máxima | % Utilização | Projeção 6m | Ação |
|---------|----------|------------------|:---:|----------|------|
| Requests/s | [X K] | [Y K] | [X%] | [Z K] | [Nenhuma / Escalar] |
| DB connections | [N] | [M] | [X%] | [P] | [Ação] |
| Storage | [X TB] | [Y TB] | [X%] | [Z TB] | [Ação] |
| CPU (pico) | [X%] | [100%] | [X%] | [Y%] | [Ação] |
| Memória (pico) | [X GB] | [Y GB] | [X%] | [Z GB] | [Ação] |

**Projeção de custo de infra:**
- Atual: R$ [X]/mês
- Em 6 meses: R$ [X]/mês (+X%)
- Em 12 meses: R$ [X]/mês (+X%)
```

---

## Exemplos de Uso

### Para Due Diligence Técnica
```markdown
## Avaliação Técnica — Resumo

- **Stack:** Moderna (React + Go + PostgreSQL + K8s/AWS)
- **DORA Level:** High (deploy diário, MTTR <2h)
- **Tech Debt:** Moderada — principal item é migração do monolito (6 meses)
- **Segurança:** SOC 2 Type I, pen test anual, 0 vulnerabilidades críticas
- **Escala:** Suporta 10x o tráfego atual sem mudança arquitetural
- **Risco principal:** Key-person dependency no arquiteto principal
```

---

## Dicas de Uso
- Métricas DORA são o padrão do setor — use para benchmarking
- Dívida técnica invisível é a mais perigosa — façam inventário regular
- Segurança é binária na percepção do mercado — um incidente muda tudo
- Para board, simplifique para score + tendência — não entre em detalhes técnicos
- Capacidade deve ser avaliada contra PROJEÇÃO de crescimento, não uso atual
- Custo de infra por cliente é métrica essencial para unit economics
