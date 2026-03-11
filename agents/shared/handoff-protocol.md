# Protocolo de Handoff entre Agentes

## Visao Geral

Este documento define o protocolo para transferencia de responsabilidade, informacao e contexto entre agentes do C-Level Squad. Handoffs mal executados sao a principal causa de perda de informacao, atrasos e decisoes com contexto incompleto.

---

## Principios de Handoff

1. **Zero perda de contexto**: O agente receptor deve ter todo o contexto necessario para continuar sem precisar reconstruir.
2. **Accountability clara**: Em todo momento deve estar claro quem e o dono da atividade.
3. **Confirmacao explicita**: Handoff so e considerado completo quando o receptor confirma recebimento e entendimento.
4. **Documentacao**: Todo handoff significativo deve ser documentado para rastreabilidade.
5. **Continuidade**: O handoff nao deve criar gap temporal na execucao.

---

## Tipos de Handoff

### Tipo 1 - Handoff de Informacao

**Quando**: Um agente produz informacao que outro precisa consumir para tomar decisao ou agir.

**Exemplos**:
- CIO entrega dataset para CAIO treinar modelo.
- CFO entrega analise financeira para Vision Chief decidir investimento.
- CTO entrega avaliacao tecnica para COO planejar sprint.

**Formato**:
```
HANDOFF DE INFORMACAO
De: [Agente remetente]
Para: [Agente receptor]
Data: [Data do handoff]
Descricao: [O que esta sendo entregue]
Formato: [Como a informacao esta formatada/onde encontrar]
Contexto: [Por que esta informacao foi produzida]
Limitacoes: [O que esta informacao NAO inclui]
Validade: [Ate quando esta informacao e valida]
Proxima acao esperada: [O que o receptor deve fazer com isso]
Disponibilidade: [O remetente esta disponivel para duvidas ate...]
```

### Tipo 2 - Handoff de Responsabilidade

**Quando**: A responsabilidade por uma atividade, projeto ou decisao passa de um agente para outro.

**Exemplos**:
- CAIO entrega modelo pronto para CTO fazer deploy em producao.
- Vision Chief delega implementacao de decisao estrategica para COO.
- COO transfere gestao de iniciativa para Squad Coordinator.

**Formato**:
```
HANDOFF DE RESPONSABILIDADE
De: [Agente que transfere]
Para: [Agente que recebe]
Data: [Data efetiva da transferencia]
Atividade/Projeto: [O que esta sendo transferido]
Status atual: [Em que ponto esta]
Contexto completo: [Historico, decisoes tomadas, premissas]
Pendencias: [O que ainda precisa ser feito]
Riscos conhecidos: [Riscos identificados e status]
Stakeholders: [Quem mais esta envolvido e seus papeis]
Recursos: [Recursos disponoveis para a atividade]
Criterios de sucesso: [Como medir se deu certo]
Timeline: [Prazos e marcos]
Documentacao: [Links para documentos relevantes]
Suporte pos-handoff: [O remetente estara disponivel para...]
```

### Tipo 3 - Handoff de Emergencia

**Quando**: Transferencia nao planejada por indisponibilidade, incidente ou mudanca de prioridade.

**Exemplos**:
- CTO indisponivel durante incidente P0, CIO assume infra de dados.
- Vision Chief delegando decisao urgente ao COO por sobrecarga.

**Formato**:
```
HANDOFF DE EMERGENCIA
De: [Agente original / Squad Coordinator]
Para: [Agente substituto]
Urgencia: [P0/P1/P2]
Razao: [Por que o handoff e necessario]
Atividade: [O que precisa ser assumido]
Estado atual: [Status da situacao]
Acoes em andamento: [O que ja esta sendo feito]
Limites de autoridade: [Ate onde o substituto pode decidir]
Duracao estimada: [Por quanto tempo o substituto assume]
Escalacao se necessario: [Para quem escalar se exceder limites]
Retorno: [Como sera o handoff de volta]
```

---

## Processo de Handoff

### Passo 1 - Preparacao (Remetente)

1. Organizar toda a informacao relevante.
2. Documentar contexto, status, pendencias e riscos.
3. Verificar que a documentacao esta acessivel ao receptor.
4. Identificar possiveis duvidas e preparar respostas.

### Passo 2 - Comunicacao (Remetente -> Receptor)

1. Enviar handoff no formato padrao apropriado.
2. Agendar sessao de alinhamento se complexidade justificar (max 30 min).
3. Disponibilizar-se para periodo de transicao.

### Passo 3 - Validacao (Receptor)

1. Revisar material recebido.
2. Listar duvidas e pontos que precisam de esclarecimento.
3. Confirmar entendimento e aceite do handoff.
4. Solicitar informacoes adicionais se necessario.

### Passo 4 - Confirmacao (Ambos)

1. Receptor confirma formalmente o aceite do handoff.
2. Remetente confirma que todas as duvidas foram respondidas.
3. Data efetiva de transferencia e registrada.
4. Stakeholders relevantes sao notificados.

### Passo 5 - Periodo de Transicao

1. Remetente permanece disponivel para duvidas por periodo definido.
2. Receptor pode escalar de volta se encontrar informacao faltante.
3. Ao fim do periodo, handoff e considerado completo.

---

## Checklist de Handoff

### Para o Remetente

- [ ] Toda documentacao esta atualizada e acessivel?
- [ ] Contexto historico foi incluido?
- [ ] Decisoes anteriores e suas justificativas estao documentadas?
- [ ] Riscos conhecidos foram listados?
- [ ] Stakeholders foram identificados?
- [ ] Criterios de sucesso estao claros?
- [ ] Timeline e marcos estao definidos?
- [ ] Recursos necessarios estao disponoveis?

### Para o Receptor

- [ ] Li e entendi toda a documentacao?
- [ ] Sei quem sao os stakeholders e seus papeis?
- [ ] Entendo os criterios de sucesso?
- [ ] Tenho os recursos necessarios?
- [ ] Sei quais decisoes ja foram tomadas e por que?
- [ ] Conheço os riscos e como mitiga-los?
- [ ] Tenho autoridade suficiente para executar?
- [ ] Sei quando e para quem escalar se necessario?

---

## Handoffs Recorrentes entre Agentes

### Handoffs Padrao

| De | Para | O que | Frequencia |
|---|---|---|---|
| CIO | CAIO | Datasets e features para IA | Por demanda |
| CAIO | CTO | Modelos prontos para deploy | Por release |
| CTO | CIO | Logs e eventos para monitoramento | Continuo |
| CFO | Vision Chief | Analise financeira para decisao | Por demanda |
| COO | Todos | Prioridades do sprint | Quinzenal |
| Vision Chief | COO | Decisoes para implementacao | Por decisao |
| Squad Coordinator | COO | Reports e status | Semanal |
| CIO | CFO | Dados financeiros processados | Diario |

### SLAs de Handoff

| Tipo | Tempo de Preparacao | Tempo de Validacao | Periodo de Transicao |
|---|---|---|---|
| Informacao | 4 horas | 4 horas | 24 horas |
| Responsabilidade | 24 horas | 24 horas | 48-72 horas |
| Emergencia | Imediato | 1 hora | Ate retorno do titular |

---

## Anti-Padroes de Handoff

1. **Handoff sem contexto**: "Aqui esta, voce resolve" — sempre incluir contexto.
2. **Handoff verbal apenas**: Se nao esta escrito, vai se perder. Sempre documentar.
3. **Handoff sem aceite**: Enviar e assumir que foi recebido. Sempre confirmar.
4. **Handoff em cascata**: Transferir para alguem que transfere para outro. Limitar a 1 re-transferencia.
5. **Handoff parcial**: Transferir a atividade mas nao a autoridade. Sempre transferir ambos.

---

## Metricas de Qualidade de Handoff

- Numero de handoffs que resultaram em re-trabalho
- Tempo medio de transicao por tipo de handoff
- Satisfacao do receptor com qualidade do handoff
- Incidentes causados por handoff inadequado
- Taxa de handoffs com documentacao completa

---

## Revisao

Este protocolo deve ser revisado a cada 90 dias ou apos incidente causado por handoff inadequado.
