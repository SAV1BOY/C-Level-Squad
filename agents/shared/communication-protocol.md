# Protocolo de Comunicacao entre Agentes

## Visao Geral

Este documento define os padroes, canais e formatos de comunicacao entre os agentes do C-Level Squad. Comunicacao eficiente e a base de coordenacao — sem ela, ate as melhores decisoes falham na execucao.

---

## Principios de Comunicacao

1. **Clareza acima de tudo**: Prefira ser explicito a ser breve. Ambiguidade e o inimigo da execucao.
2. **Assincrono primeiro**: Use comunicacao assincrona como padrao. Reunioes sao excecao, nao regra.
3. **Context-rich**: Toda comunicacao deve incluir contexto suficiente para acao sem perguntas de retorno.
4. **Destinatario correto**: Comunique para quem precisa agir, nao para todos. CC e informacao, nao acao.
5. **Registro permanente**: Toda decisao comunicada deve ser registrada para referencia futura.

---

## Canais de Comunicacao

### Canal 1 - Comunicacao Direta (1:1)

**Quando usar**: Alinhamento entre dois agentes sobre tema especifico.
**Formato**: Mensagem estruturada com contexto, pedido e prazo.
**SLA de resposta**: 4 horas em dias uteis.

```
De: [Agente remetente]
Para: [Agente destinatario]
Assunto: [Tema claro e especifico]
Contexto: [Por que esta comunicacao e necessaria]
Pedido: [O que voce precisa do destinatario]
Prazo: [Quando precisa da resposta/acao]
Prioridade: [Alta / Media / Baixa]
```

### Canal 2 - Comunicacao de Squad (Broadcast)

**Quando usar**: Informacoes relevantes para todo o squad.
**Formato**: Memo curto com informacao e implicacoes.
**SLA de leitura**: 24 horas.

```
De: [Agente remetente]
Para: Squad
Tipo: [Informativo / Decisao / Alerta]
Resumo: [1-2 frases do conteudo]
Detalhes: [Informacao completa]
Acao requerida: [O que cada agente precisa fazer, se algo]
```

### Canal 3 - Alertas e Escalacoes

**Quando usar**: Situacoes que requerem atencao imediata.
**Formato**: Alerta estruturado conforme protocolo de escalacao.
**SLA de resposta**: Conforme severidade (15min a 48h).

```
ALERTA - [SEVERIDADE P0/P1/P2/P3]
De: [Agente]
Para: [Destinatario(s)]
Trigger: [Qual trigger foi ativado]
Situacao: [O que esta acontecendo]
Impacto: [O que acontece se nao resolver]
Acao imediata: [O que ja foi feito]
Necessidade: [O que precisa dos destinatarios]
```

### Canal 4 - Rituais (Reunioes)

**Quando usar**: Cadencias definidas (WBR, MBR, QBR) e sessoes de decisao.
**Formato**: Agenda pre-definida, ata pos-reuniao.
**Regras**:
- Agenda enviada 24h antes (48h para QBR)
- Materiais de leitura enviados com a agenda
- Ata com action items enviada em ate 2h apos a reuniao
- Action items com dono e prazo definidos

---

## Formatos Padrao de Comunicacao

### Status Update (Atualizacao de Status)

```
STATUS - [Area/Projeto]
Periodo: [Data inicio - Data fim]
Progresso: [% concluido ou marco atingido]
Destaques: [1-3 conquistas do periodo]
Bloqueios: [0-3 bloqueios ativos com impacto]
Proximos passos: [1-3 acoes planejadas]
Riscos: [0-3 riscos identificados]
Necessidade de suporte: [Sim/Nao - detalhar se sim]
```

### Request (Solicitacao)

```
REQUEST - [Tipo de solicitacao]
De: [Solicitante]
Para: [Responsavel pela acao]
Descricao: [O que precisa ser feito]
Contexto: [Por que e necessario]
Criterios de aceite: [Como saber se foi atendido]
Prazo: [Quando precisa estar pronto]
Prioridade: [Alta / Media / Baixa]
Dependencias: [O que precisa estar pronto antes]
```

### Decision Record (Registro de Decisao)

```
DECISAO - [Titulo]
Data: [Data da decisao]
Decidido por: [Agente(s)]
Contexto: [Situacao que levou a decisao]
Opcoes consideradas: [Lista de alternativas]
Decisao tomada: [O que foi decidido]
Justificativa: [Por que esta opcao]
Impacto esperado: [Resultado projetado]
Revisao: [Quando revisar esta decisao]
```

---

## Regras de Comunicacao

### O que Fazer

1. Iniciar toda comunicacao com o ponto principal (bottom-line up front).
2. Incluir dados e evidencias quando relevante.
3. Ser especifico sobre o que precisa do destinatario.
4. Definir prazos explicitos para respostas e acoes.
5. Confirmar recebimento de comunicacoes criticas.
6. Atualizar stakeholders quando situacao muda.

### O que Nao Fazer

1. Nao enviar comunicacao sem acao clara ou informacao nova.
2. Nao usar jargao sem definicao quando comunicando cross-funcional.
3. Nao assumir que o destinatario tem contexto — sempre incluir.
4. Nao enviar comunicacao critica apenas verbalmente — sempre registrar.
5. Nao copiar agentes que nao precisam agir ou saber.
6. Nao responder a alerta com pergunta — responder com acao ou plano.

---

## SLAs de Comunicacao

| Tipo | Prioridade | SLA de Resposta | SLA de Acao |
|---|---|---|---|
| Alerta P0 | Critica | 15 minutos | 1 hora |
| Alerta P1 | Alta | 1 hora | 4 horas |
| Alerta P2 | Media | 4 horas | 24 horas |
| Request Alta | Alta | 4 horas | 24-48 horas |
| Request Media | Media | 24 horas | 3-5 dias |
| Request Baixa | Baixa | 48 horas | 5-10 dias |
| Status Update | Informativa | Leitura em 24h | N/A |
| Decision Record | Informativa | Leitura em 24h | N/A |

---

## Cadencias de Comunicacao

### Diaria
- Daily standup (15 min) — status e bloqueios

### Semanal
- WBR (60 min) — metricas e decisoes operacionais
- Status update por area — progresso e riscos

### Quinzenal
- Sprint review / retrospectiva (45 min)
- 1:1 entre agentes com dependencias fortes

### Mensal
- MBR (90 min) — revisao de metricas e estrategia
- Report financeiro completo

### Trimestral
- QBR (3h) — revisao estrategica e planejamento
- Avaliacao de performance dos agentes
- Revisao de OKRs

---

## Metricas de Comunicacao

- Tempo medio de resposta por tipo de comunicacao
- Taxa de comunicacoes com acao clara definida
- Numero de reunioes vs comunicacoes assincronas
- Satisfacao dos agentes com fluxo de informacao
- Decisoes que falharam por falta de comunicacao (post-mortem)

---

## Revisao

Este protocolo deve ser revisado a cada 90 dias ou quando houver feedback significativo sobre ineficiencias de comunicacao.
