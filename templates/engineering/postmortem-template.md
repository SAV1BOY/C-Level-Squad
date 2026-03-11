# Template: Postmortem de Incidente

## Propósito
Este template documenta a análise pós-incidente de forma blameless (sem culpa individual). O objetivo é aprender com falhas, prevenir recorrências e melhorar a resiliência dos sistemas. Cada incidente P0/P1 deve gerar um postmortem.

## Instruções de Uso
1. Inicie o documento nas primeiras 24h após resolução do incidente
2. Reúna o time envolvido para preencher colaborativamente (max 48h após resolução)
3. Revisão com Engineering Manager em até 5 dias úteis
4. Publique internamente — transparência gera confiança
5. Track action items até conclusão

---

## Postmortem: [Título Descritivo do Incidente]

### Metadados

| Campo | Valor |
|-------|-------|
| **ID do Incidente** | [INC-AAAA-NNN] |
| **Data do Incidente** | [DD/MM/AAAA HH:MM — timezone] |
| **Duração Total** | [Xh Ymin] |
| **Severidade** | [P0 / P1 / P2] |
| **Impacto** | [N usuários afetados / R$ perdidos / % de degradação] |
| **Serviços Afetados** | [Lista de serviços] |
| **Autor do Postmortem** | [Nome — Cargo] |
| **Data do Postmortem** | [DD/MM/AAAA] |
| **Status** | [Rascunho / Em Revisão / Publicado / Action Items Completos] |

---

### Resumo Executivo

[3-5 linhas descrevendo o que aconteceu, impacto e resolução. Um executivo deve entender o incidente lendo apenas esta seção.]

---

### Impacto

| Dimensão | Detalhes |
|----------|---------|
| **Usuários afetados** | [N usuários — X% da base] |
| **Duração do impacto** | [Xh Ymin — do início da degradação até recuperação total] |
| **Funcionalidades afetadas** | [Lista de features/fluxos impactados] |
| **Impacto financeiro** | [R$ em receita perdida / créditos concedidos / SLA penalties] |
| **Impacto reputacional** | [Menções em redes sociais / reclamações / cobertura de mídia] |
| **SLA status** | [Dentro do SLA / SLA violado — por quanto] |

---

### Timeline Detalhada

| Horário (UTC-3) | Evento | Ação Tomada | Por Quem |
|-----------------|--------|------------|----------|
| [HH:MM] | Primeiro sinal de problema (alerta/ticket) | [Ação] | [Sistema/Pessoa] |
| [HH:MM] | Incidente declarado | [Canal de guerra aberto] | [Nome] |
| [HH:MM] | Diagnóstico inicial | [Hipótese levantada] | [Nome] |
| [HH:MM] | Primeiro tentativa de mitigação | [O que foi feito] | [Nome] |
| [HH:MM] | Causa raiz identificada | [Descoberta] | [Nome] |
| [HH:MM] | Fix aplicado | [Ação de resolução] | [Nome] |
| [HH:MM] | Monitoramento confirma recuperação | [Métricas normalizaram] | [Nome] |
| [HH:MM] | Incidente encerrado | [Comunicação final] | [Nome] |

---

### Análise de Causa Raiz (Root Cause Analysis)

#### Causa Raiz
[Descrição detalhada da causa raiz técnica. Seja específico.]

#### Cadeia Causal (5 Porquês)
1. **Por que o incidente aconteceu?** [Resposta — ex: "O serviço X ficou indisponível"]
2. **Por que o serviço ficou indisponível?** [Resposta — ex: "Memory leak causou OOM"]
3. **Por que houve memory leak?** [Resposta — ex: "Conexões ao DB não estavam sendo fechadas"]
4. **Por que conexões não eram fechadas?** [Resposta — ex: "Bug introduzido no PR #1234"]
5. **Por que o bug não foi detectado antes?** [Resposta — ex: "Teste de carga não cobria cenário X"]

#### Fatores Contribuintes
- [Fator 1 — ex: "Monitoramento não cobria métrica de conexões ativas"]
- [Fator 2 — ex: "Rollout sem canary — 100% de tráfego no novo código"]
- [Fator 3 — ex: "Runbook desatualizado — procedimento de restart estava errado"]

---

### O que Funcionou Bem

- [Item 1 — ex: "Alertas dispararam em menos de 2 minutos"]
- [Item 2 — ex: "Comunicação no canal de guerra foi clara e organizada"]
- [Item 3 — ex: "Rollback foi executado em 5 minutos"]

### O que Não Funcionou

- [Item 1 — ex: "Levamos 45 min para identificar a causa raiz"]
- [Item 2 — ex: "Dashboard não mostrava a métrica-chave"]
- [Item 3 — ex: "Escalonamento demorou — engenheiro L2 não respondeu"]

### Onde Tivemos Sorte

- [Item 1 — ex: "Incidente aconteceu em horário de baixo tráfego"]
- [Item 2 — ex: "Engenheiro que conhecia o sistema estava online por acaso"]

---

### Action Items

| ID | Ação | Tipo | Prioridade | Owner | Prazo | Status |
|----|------|------|-----------|-------|-------|--------|
| 1 | [Ação — ex: "Adicionar alerta de conexões ao DB"] | Detecção | P1 | [Nome] | [Data] | [Pendente/Em progresso/Concluído] |
| 2 | [Ação — ex: "Implementar canary deployment"] | Prevenção | P1 | [Nome] | [Data] | [Status] |
| 3 | [Ação — ex: "Atualizar runbook do serviço X"] | Processo | P2 | [Nome] | [Data] | [Status] |
| 4 | [Ação — ex: "Adicionar teste de carga para cenário Y"] | Prevenção | P2 | [Nome] | [Data] | [Status] |
| 5 | [Ação — ex: "Revisar configuração de escalonamento"] | Processo | P3 | [Nome] | [Data] | [Status] |

**Tipos de ação:**
- **Prevenção:** Evitar que a causa raiz ocorra novamente
- **Detecção:** Detectar o problema mais rápido
- **Mitigação:** Reduzir o impacto quando ocorrer
- **Processo:** Melhorar procedimentos operacionais

---

### Métricas do Incidente

| Métrica | Valor | Meta/Benchmark |
|---------|-------|---------------|
| Time to Detect (TTD) | [X min] | [<Y min] |
| Time to Engage (TTE) | [X min] | [<Y min] |
| Time to Mitigate (TTM) | [X min] | [<Y min] |
| Time to Resolve (TTR) | [X min] | [<Y min] |

---

### Lições Aprendidas

1. [Lição 1 — insight que pode ser aplicado em outros sistemas/times]
2. [Lição 2 — mudança de processo ou cultura recomendada]
3. [Lição 3 — investimento técnico necessário]

---

## Exemplo Preenchido (Resumo)

> **INC-2026-042:** Indisponibilidade do checkout por 47 minutos
> **Severidade:** P0 | **Impacto:** 12.000 usuários, R$ 180K em vendas perdidas
> **Causa raiz:** Deploy com bug em validação de cupom causou crash loop no serviço de checkout
> **TTD:** 3 min | **TTR:** 47 min (rollback em 12 min, mas cache precisou expirar)
> **Action items:** 5 itens — canary deploy, teste de regressão para cupons, alerta de crash rate

---

## Dicas de Uso
- BLAMELESS sempre — foque em sistemas e processos, nunca em pessoas
- Seja brutalmente honesto sobre o que não funcionou — é assim que melhoramos
- Action items sem owner e prazo são inúteis — atribua tudo
- Publique internamente — outros times aprendem com nossos incidentes
- Revise action items em 30 dias — garantir que foram implementados
- Mantenha um repositório centralizado de postmortems para referência futura
