# Protocolo de Decisao Conjunta

## Visao Geral

Este documento define o protocolo para decisoes que requerem participacao de multiplos agentes C-Level. Decisoes conjuntas sao necessarias quando o impacto cruza fronteiras de autoridade ou quando a complexidade exige perspectivas multidisciplinares.

---

## Quando Usar Decisao Conjunta

### Criterios de Ativacao

Uma decisao deve seguir o protocolo conjunto quando:

1. **Impacto cross-funcional**: Afeta diretamente 2 ou mais areas de autoridade.
2. **Investimento significativo**: Valor acima de R$ 200.000 ou comprometimento acima de 6 meses.
3. **Risco elevado**: Decisao irreversivel com impacto potencial superior a 10% da receita.
4. **Mudanca de direcao**: Alteracao que modifica premissas fundamentais de uma ou mais areas.
5. **Precedente novo**: Situacao sem precedente que pode definir padrao futuro.

---

## Tipos de Decisao Conjunta

### Tipo 1 - Decisao Consultiva (1 dono + consultores)

**Quando usar**: Decisao claramente dentro da autoridade de um agente, mas com impacto em outras areas.

**Processo**:
1. Agente dono identifica necessidade de consulta.
2. Solicita input escrito dos agentes relevantes com prazo de 24-48h.
3. Agentes consultados enviam perspectiva, riscos e recomendacoes.
4. Agente dono toma a decisao incorporando (ou nao) os inputs.
5. Decisao documentada com justificativa de inputs aceitos e rejeitados.

**Exemplos**:
- CTO decide migrar infraestrutura (consulta CFO para custo, CIO para dados, COO para operacoes).
- CFO define politica de gastos (consulta COO para viabilidade operacional).

### Tipo 2 - Decisao Colaborativa (Co-ownership)

**Quando usar**: Decisao na intersecao de duas areas de autoridade, sem dono claro.

**Processo**:
1. Agentes co-donos identificam a decisao conjunta.
2. Ambos preparam analise escrita com perspectiva da sua area.
3. Reuniao conjunta para alinhar posicoes (max 1 hora).
4. Se acordo: documentam e implementam em conjunto.
5. Se desacordo: COO Orchestrator media. Se persistir, Vision Chief decide.

**Exemplos**:
- CAIO + CIO decidem sobre estrategia de dados para IA.
- CTO + CAIO decidem sobre infraestrutura de ML.
- CFO + COO decidem sobre otimizacao de custos operacionais.

### Tipo 3 - Decisao de Squad (Todos os C-Level)

**Quando usar**: Decisao estrategica que afeta todo o squad ou redefine prioridades.

**Processo**:
1. Vision Chief ou agente solicitante prepara memo de decisao (formato Amazon 6-pager simplificado).
2. Memo distribuido 24h antes da reuniao.
3. Reuniao de deliberacao (max 90 minutos):
   - 15 min: Leitura silenciosa do memo.
   - 30 min: Perguntas e esclarecimentos.
   - 30 min: Debate e posicionamento.
   - 15 min: Decisao e proximos passos.
4. Vision Chief toma decisao final se nao houver consenso.
5. Decisao documentada e comunicada em 24h.

**Exemplos**:
- Mudanca de modelo de negocio.
- Entrada em novo mercado.
- Reestruturacao do squad.
- Definicao de OKRs trimestrais.

---

## Formato do Memo de Decisao

```markdown
# Memo de Decisao: [Titulo]

## Contexto
[Por que esta decisao precisa ser tomada agora?]

## Problema/Oportunidade
[Descricao clara do problema ou oportunidade]

## Opcoes Consideradas
### Opcao A: [Nome]
- Descricao: [...]
- Pros: [...]
- Contras: [...]
- Custo estimado: [R$]
- Timeline: [...]
- Risco: [Alto/Medio/Baixo]

### Opcao B: [Nome]
[Mesmo formato]

### Opcao C: [Nome]
[Mesmo formato]

## Recomendacao
[Opcao recomendada e justificativa]

## Inputs Necessarios
[Quais agentes precisam opinar e sobre o que]

## Decisao Requerida Ate
[Data limite]

## Impacto em Cada Area
- Vision/Estrategia: [...]
- Operacoes (COO): [...]
- Tecnologia (CTO): [...]
- Financas (CFO): [...]
- Dados (CIO): [...]
- IA (CAIO): [...]
```

---

## Regras de Votacao e Consenso

### Consenso Preferido

1. O squad busca consenso sempre que possivel.
2. Consenso = todos concordam que a decisao e aceitavel, mesmo que nao seja a primeira opcao de todos.
3. Consenso NAO e unanimidade — e acordo de que a decisao e boa o suficiente para prosseguir.

### Quando Consenso Nao e Atingido

1. Vision Chief tem voto de Minerva em decisoes estrategicas.
2. Para decisoes tecnicas: CTO tem voto de Minerva com input do CAIO.
3. Para decisoes financeiras: CFO tem voto de Minerva com input do Vision Chief.
4. Para decisoes operacionais: COO tem voto de Minerva com input do Vision Chief.
5. Para decisoes de dados: CIO tem voto de Minerva com input do CTO.
6. Para decisoes de IA: CAIO tem voto de Minerva com input do CTO e CIO.

### Direito de Veto

- Qualquer agente pode exercer veto sobre decisao que viole suas restricoes absolutas.
- Veto deve ser justificado por escrito, citando a restricao especifica.
- Veto nao resolvido escala automaticamente ao Vision Chief em 24h.
- Vision Chief pode override veto com justificativa documentada, exceto em questoes de compliance, seguranca ou etica.

---

## SLAs de Decisao Conjunta

| Tipo de Decisao | Tempo Maximo | Formato |
|---|---|---|
| Consultiva (Tipo 1) | 48 horas | Assincrono |
| Colaborativa (Tipo 2) | 72 horas | 1 reuniao + follow-up |
| Squad (Tipo 3) | 5 dias uteis | Memo + reuniao formal |
| Emergencial | 4 horas | Chamada imediata |

---

## Decisoes Emergenciais

Para decisoes conjuntas urgentes (janela < 24h):

1. Agente que identifica urgencia convoca reuniao imediata via protocolo de comunicacao.
2. Quorum minimo: 3 agentes C-Level incluindo o Vision Chief.
3. Decisao tomada com informacao disponivel — perfeiçao nao e requisito em emergencia.
4. Documentacao pode ser feita apos a decisao (max 24h).
5. Revisao obrigatoria na proxima WBR.

---

## Registro e Acompanhamento

### Decision Registry

Toda decisao conjunta deve ser registrada com:
- Data da decisao
- Agentes participantes
- Tipo de decisao (1, 2 ou 3)
- Opcoes consideradas
- Decisao tomada e justificativa
- Dono da implementacao
- Metricas de sucesso
- Data de revisao

### Revisao de Decisoes

- Decisoes Tipo 1: Revisadas se metricas nao atingidas em 60 dias.
- Decisoes Tipo 2: Revisadas na proxima MBR (Monthly Business Review).
- Decisoes Tipo 3: Revisadas na proxima QBR (Quarterly Business Review).

---

## Revisao

Este protocolo deve ser revisado a cada 90 dias ou quando houver mudanca na composicao do squad.
