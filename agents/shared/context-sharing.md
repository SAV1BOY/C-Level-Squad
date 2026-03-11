# Compartilhamento de Contexto entre Agentes

## Visao Geral

Este documento define como os agentes do C-Level Squad compartilham contexto para garantir que decisoes sejam tomadas com informacao completa. A falta de contexto compartilhado e a causa raiz de decisoes desalinhadas, re-trabalho e conflitos evitaveis.

---

## Principios de Context Sharing

1. **Default e compartilhar**: Na duvida, compartilhe. O custo de informacao em excesso e menor que o custo de decisao com informacao faltante.
2. **Proativo, nao reativo**: Nao espere alguem pedir — se a informacao e relevante para outro agente, compartilhe antes.
3. **Estruturado**: Contexto desestruturado e ruido. Use formatos padrao para maximizar absorcao.
4. **Atualizado**: Contexto desatualizado e pior que nenhum contexto — pode levar a decisoes erradas.
5. **Acessivel**: Informacao deve estar onde os agentes procuram, nao em silos isolados.

---

## Tipos de Contexto

### 1. Contexto Estrategico

**O que inclui**: Visao, missao, OKRs, estrategia, bets, kill criteria, direcao de longo prazo.
**Dono**: Vision Chief.
**Frequencia de atualizacao**: Trimestral (ou quando mudar).
**Acessivel para**: Todos os agentes.

**Formato de compartilhamento**:
```
CONTEXTO ESTRATEGICO - Atualizado em [Data]
Visao: [1 frase]
Missao: [1 frase]
Bets atuais: [Lista com status]
OKRs do trimestre: [Lista com progresso]
Mudancas desde ultima atualizacao: [Delta]
Premissas chave: [O que estamos assumindo]
Riscos estrategicos: [Top 3]
```

### 2. Contexto Operacional

**O que inclui**: Status de projetos, capacidade, bloqueios, metricas operacionais, cadencias.
**Dono**: COO Orchestrator.
**Frequencia de atualizacao**: Semanal.
**Acessivel para**: Todos os agentes.

**Formato de compartilhamento**:
```
CONTEXTO OPERACIONAL - Semana [Numero]
Iniciativas ativas: [Lista com status e % progresso]
Capacidade utilizada: [% por area]
Bloqueios ativos: [Lista com dono e prazo]
Metricas chave: [Dashboard link ou resumo]
Entregas da semana: [Concluidas e planejadas]
Riscos operacionais: [Top 3]
```

### 3. Contexto Tecnico

**O que inclui**: Arquitetura atual, tech radar, divida tecnica, capacidades, limitacoes.
**Dono**: CTO Architect.
**Frequencia de atualizacao**: Mensal.
**Acessivel para**: Todos os agentes.

**Formato de compartilhamento**:
```
CONTEXTO TECNICO - Atualizado em [Data]
Arquitetura atual: [Diagrama ou descricao]
Mudancas recentes: [O que mudou e por que]
Tech debt status: [Score e areas criticas]
Capacidades novas: [O que agora e possivel]
Limitacoes conhecidas: [O que NAO e possivel ou e dificil]
Tech radar: [Adopt / Trial / Assess / Hold]
Riscos tecnicos: [Top 3]
```

### 4. Contexto Financeiro

**O que inclui**: Saude financeira, runway, budget, metricas financeiras, riscos.
**Dono**: CFO Strategist.
**Frequencia de atualizacao**: Semanal (resumo) e mensal (completo).
**Acessivel para**: Todos os agentes.

**Formato de compartilhamento**:
```
CONTEXTO FINANCEIRO - [Periodo]
Runway: [Meses]
Burn rate: [R$/mes]
Receita: [R$ atual vs target]
Budget utilizado: [% por area]
Desvios: [Areas com desvio > 10%]
Alertas financeiros ativos: [Lista]
Riscos financeiros: [Top 3]
```

### 5. Contexto de Dados

**O que inclui**: Data assets, qualidade, seguranca, compliance, capacidades de BI.
**Dono**: CIO Engineer.
**Frequencia de atualizacao**: Mensal.
**Acessivel para**: Todos os agentes.

**Formato de compartilhamento**:
```
CONTEXTO DE DADOS - Atualizado em [Data]
Data assets: [Datasets disponiveis e status]
Data quality score: [Score geral e por dataset]
Seguranca: [Alertas ativos, incidentes recentes]
Compliance LGPD: [Status e gaps]
Capacidades de BI: [O que esta disponivel]
Pipelines: [Status e SLAs]
Riscos de dados: [Top 3]
```

### 6. Contexto de IA

**O que inclui**: Modelos em producao, performance, roadmap, experimentos, riscos.
**Dono**: CAIO Architect.
**Frequencia de atualizacao**: Mensal.
**Acessivel para**: Todos os agentes.

**Formato de compartilhamento**:
```
CONTEXTO DE IA - Atualizado em [Data]
Modelos em producao: [Lista com performance vs baseline]
Experimentos ativos: [Lista com status]
Roadmap de IA: [Proximos 90 dias]
Custos de IA: [Atual vs budget]
Riscos eticos: [Alertas ativos]
Oportunidades identificadas: [Lista priorizada]
Maturidade de IA: [Score atual]
```

---

## Mecanismos de Compartilhamento

### 1. Base de Conhecimento Centralizada

**O que e**: Repositorio central onde todo contexto e armazenado e atualizado.
**Estrutura**:
```
/context
  /strategic     -- Mantido pelo Vision Chief
  /operational   -- Mantido pelo COO
  /technical     -- Mantido pelo CTO
  /financial     -- Mantido pelo CFO
  /data          -- Mantido pelo CIO
  /ai            -- Mantido pelo CAIO
  /decisions     -- Decision registry compartilhado
  /rituals       -- Atas e action items
```

### 2. Context Briefings em Rituais

| Ritual | Context Shared | Por Quem | Duracao |
|---|---|---|---|
| Daily Standup | Bloqueios e prioridades do dia | Todos | 2 min cada |
| WBR | Metricas operacionais e financeiras | COO + CFO | 15 min |
| MBR | Contexto completo de todas as areas | Todos | 30 min |
| QBR | Contexto estrategico + revisao | Vision Chief + Todos | 60 min |

### 3. Context Updates Assincronos

- Cada agente publica context update na base centralizada conforme cadencia definida.
- Notificacao enviada ao squad quando contexto e atualizado.
- Agentes devem ler updates de outras areas em ate 24 horas.

### 4. Context on Demand

- Qualquer agente pode solicitar contexto adicional de outro agente.
- SLA de resposta: 4 horas para contexto operacional, 24 horas para contexto estrategico.
- Formato: Request padrao com especificacao do que precisa e por que.

---

## Regras de Context Sharing

### Obrigacoes de Cada Agente

1. Manter seu contexto atualizado conforme cadencia definida.
2. Notificar o squad quando contexto mudar significativamente fora da cadencia regular.
3. Responder a requests de contexto dentro do SLA.
4. Incluir contexto relevante de outras areas em suas decisoes (mostrar que leu).
5. Alertar quando identificar que contexto de outro agente parece desatualizado.

### Classificacao de Sensibilidade

| Classificacao | Exemplo | Acesso |
|---|---|---|
| Aberto | OKRs, metricas operacionais, tech radar | Todo o squad |
| Interno | Detalhes financeiros, custos por area | Squad + operador humano |
| Confidencial | Dados de M&A, estrategia pre-lancamento | Agentes especificos |
| Restrito | Dados pessoais, credenciais, chaves | Apenas CIO + autorizado |

---

## Anti-Padroes de Context Sharing

1. **Information hoarding**: Acumular informacao como fonte de poder. Viola o principio de transparencia.
2. **Context dumping**: Compartilhar tudo sem filtro ou estrutura. Gera ruido, nao clareza.
3. **Stale context**: Manter contexto desatualizado publicado. Pior que nao ter.
4. **Assumption-based decisions**: Tomar decisao sem verificar contexto atualizado de areas impactadas.
5. **Silo mentality**: Tratar informacao da sua area como irrelevante para outros agentes.

---

## Metricas de Efetividade

- Frequencia de atualizacao de contexto por area (aderencia a cadencia)
- Decisoes tomadas com contexto desatualizado (incidentes)
- Satisfacao dos agentes com qualidade e acessibilidade do contexto
- Tempo medio para obter contexto quando solicitado
- Conflitos causados por falta de contexto compartilhado

---

## Integracao com Outros Protocolos

- **Handoff**: Todo handoff inclui contexto relevante automaticamente.
- **Escalacao**: Escalacao inclui link para contexto atualizado da area.
- **Decisao conjunta**: Memo de decisao referencia contexto de todas as areas impactadas.
- **Comunicacao**: Status updates alimentam a base de contexto.
- **Feedback**: Feedback sobre qualidade do context sharing melhora o processo.

---

## Revisao

Este protocolo deve ser revisado a cada 90 dias ou quando pesquisa de satisfacao indicar problemas de acesso a informacao.
