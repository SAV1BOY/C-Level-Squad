# Protocolo de Escalacao entre Agentes

## Visao Geral

Este documento define o protocolo unificado de escalacao do C-Level Squad. Escalacao e um mecanismo de governanca, nao de fraqueza. Escalar cedo e com qualidade e sinal de maturidade operacional.

---

## Principios de Escalacao

1. **Escalar cedo, nao tarde**: O custo de escalar desnecessariamente e muito menor que o custo de escalar tarde demais.
2. **Escalar com solucao**: Nunca escale apenas o problema — sempre inclua analise e recomendacao.
3. **Escalar para o dono correto**: Cada tipo de problema tem um destinatario natural. Escalar para o errado atrasa a resolucao.
4. **Escalar uma vez**: Nao escale para multiplas pessoas simultaneamente sem definir quem e o dono.
5. **Registrar tudo**: Toda escalacao deve ser documentada para aprendizado e melhoria do processo.

---

## Niveis de Escalacao

### Nivel 0 - Auto-Resolucao

**Definicao**: Problema dentro da autoridade do agente que pode ser resolvido autonomamente.
**Acao**: Resolver, documentar e comunicar.
**Prazo**: Imediato.
**Registro**: No log de decisoes do agente.

### Nivel 1 - Escalacao Lateral (Peer-to-Peer)

**Definicao**: Problema que requer input ou acao de outro agente C-Level de mesmo nivel.
**Acao**: Comunicar diretamente ao agente relevante com contexto e pedido claro.
**Prazo**: Resposta em ate 4 horas, resolucao em ate 24 horas.
**Registro**: Comunicacao via formato padrao.

**Quando usar**:
- Necessidade de informacao que outro agente possui.
- Dependencia tecnica ou operacional entre areas.
- Decisao em zona de sobreposicao de autoridade.
- Alerta sobre risco identificado na area de outro agente.

### Nivel 2 - Escalacao para COO Orchestrator

**Definicao**: Problema operacional que requer coordenacao ou mediacao que os agentes nao conseguem resolver entre si.
**Acao**: Escalar ao COO com posicoes de ambos os lados e recomendacao.
**Prazo**: Resposta em ate 4 horas, resolucao em ate 24 horas.
**Registro**: Formato de escalacao padrao.

**Quando usar**:
- Conflito de prioridade entre areas nao resolvido em 4 horas.
- Necessidade de realocacao de recursos cross-squad.
- Bloqueio operacional impactando entregas.
- Processo cross-funcional que nao esta funcionando.

### Nivel 3 - Escalacao para Vision Chief

**Definicao**: Problema estrategico, conflito entre C-Level, ou decisao que excede autoridade dos agentes e do COO.
**Acao**: COO ou agente escala ao Vision Chief com analise completa.
**Prazo**: Resposta em ate 4 horas, decisao em ate 48 horas.
**Registro**: Memo de escalacao formal.

**Quando usar**:
- Conflito entre agentes C-Level nao resolvido pelo COO.
- Decisao que impacta a estrategia geral.
- Risco que ameaca OKRs ou direcao estrategica.
- Necessidade de mudanca de prioridade estrategica.

### Nivel 4 - Escalacao para Operador Humano

**Definicao**: Situacao que excede a capacidade decisoria do squad inteiro.
**Acao**: Vision Chief escala ao operador humano com analise e recomendacao.
**Prazo**: Conforme urgencia (imediato a 72 horas).
**Registro**: Documento formal com todas as perspectivas.

**Quando usar**:
- Risco existencial para a organizacao.
- Decisao que o squad nao tem autoridade para tomar.
- Conflito fundamental nao resolvido apos todas as tentativas.
- Violacao etica ou legal.
- Investimento acima do teto do squad.

---

## Formato Padrao de Escalacao

```
ESCALACAO - NIVEL [0-4]
Data/Hora: [Timestamp]
De: [Agente que escala]
Para: [Destinatario]
Urgencia: [P0/P1/P2/P3]

SITUACAO
[Descricao factual do que esta acontecendo]

IMPACTO
[O que acontece se nao resolver / o que ja foi impactado]
- Financeiro: [Impacto em R$ se aplicavel]
- Operacional: [Processos ou entregas impactadas]
- Estrategico: [Impacto em OKRs ou direcao]
- Reputacional: [Impacto em stakeholders externos]

TENTATIVAS DE RESOLUCAO
[O que ja foi tentado e por que nao funcionou]

ANALISE
[Causa raiz identificada ou hipoteses]

OPCOES
A) [Opcao 1 - pros, contras, custo, risco]
B) [Opcao 2 - pros, contras, custo, risco]
C) [Opcao 3 - pros, contras, custo, risco]

RECOMENDACAO
[Qual opcao o agente recomenda e por que]

PRAZO PARA DECISAO
[Ate quando a decisao precisa ser tomada]

INFORMACAO ADICIONAL NECESSARIA
[O que mais o decisor precisa saber]
```

---

## Matriz de Escalacao por Tipo de Problema

| Tipo de Problema | Nivel 1 (Lateral) | Nivel 2 (COO) | Nivel 3 (Vision Chief) | Nivel 4 (Humano) |
|---|---|---|---|---|
| Conflito de prioridade | Entre agentes | Se nao resolvido em 4h | Se COO nao resolver | N/A |
| Risco financeiro | CFO | Se impacto >10% budget | Se impacto >20% receita | Se risco existencial |
| Incidente tecnico | CTO + CIO | Se impacto operacional | Se impacto estrategico | Se dados comprometidos |
| Risco etico | CAIO + CIO | Se impacto operacional | Se impacto na marca | Se violacao legal |
| Bloqueio operacional | Agente dono | Se cross-squad | Se impacto em OKRs | N/A |
| Risco de seguranca | CIO | Se impacto >1 area | Se dados de clientes | Sempre (vazamento) |
| Oportunidade estrategica | CFO + CTO | Se requer recursos | Se muda direcao | Se investimento > teto |

---

## Regras de Escalacao

### Obrigacoes do Escalante

1. Tentar resolver no nivel mais baixo possivel antes de escalar.
2. Incluir analise, opcoes e recomendacao em toda escalacao.
3. Respeitar os SLAs de resposta e nao re-escalar antes do prazo.
4. Manter o destinatario atualizado sobre mudancas na situacao.
5. Documentar a escalacao e seu resultado.

### Obrigacoes do Receptor

1. Confirmar recebimento da escalacao dentro do SLA.
2. Solicitar informacoes adicionais se o contexto for insuficiente.
3. Tomar decisao ou acao dentro do prazo definido.
4. Comunicar a decisao de volta ao escalante e stakeholders.
5. Documentar a decisao e justificativa.

### Proibicoes

1. **Nao escalar sem contexto** — "temos um problema" nao e escalacao.
2. **Nao pular niveis** — ir do Nivel 1 direto ao Nivel 4 sem passar pelos intermediarios.
3. **Nao escalar por conveniencia** — para evitar trabalho ou responsabilidade.
4. **Nao escalar anonimamente** — toda escalacao tem um dono com nome.
5. **Nao re-escalar o mesmo problema** sem informacao nova.

**Excecao**: Escalacao direta ao Nivel 4 (operador humano) e permitida em caso de risco existencial, violacao etica ou vazamento de dados.

---

## SLAs de Escalacao

| Nivel | Tempo de Resposta | Tempo de Decisao | Follow-up |
|---|---|---|---|
| Nivel 1 | 4 horas | 24 horas | 48 horas |
| Nivel 2 | 4 horas | 24 horas | 48 horas |
| Nivel 3 | 4 horas | 48 horas | 72 horas |
| Nivel 4 | Conforme urgencia | Conforme urgencia | 1 semana |
| Emergencia (qualquer nivel) | 15-60 min | 1-4 horas | 24 horas |

---

## Pos-Escalacao

### Documentacao

Toda escalacao resolvida deve ter registro final com:
- Decisao tomada e justificativa.
- Quem tomou a decisao.
- Resultado esperado e metricas de sucesso.
- Licoes aprendidas.
- Acoes preventivas para evitar recorrencia.

### Retrospectiva

Mensalmente, o squad revisa:
- Numero de escalacoes por nivel.
- Escalacoes que poderiam ter sido evitadas.
- Escalacoes que foram tardias e causaram impacto adicional.
- Melhorias no processo de escalacao.

---

## Revisao

Este protocolo deve ser revisado a cada 60 dias ou apos qualquer incidente que revele gaps no processo de escalacao.
