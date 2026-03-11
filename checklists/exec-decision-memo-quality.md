# Checklist de Qualidade — Decision Memo Executivo

## Propósito
Garantir que todo decision memo produzido por agentes ou executivos contenha contexto suficiente, opções claras, trade-offs explícitos, recomendação fundamentada, owner definido, data de execução e riscos identificados. Este checklist funciona como quality gate antes de qualquer decisão material ser ratificada.

## Quando Aplicar
- Antes de submeter qualquer decision memo para aprovação do CEO, CFO ou board.
- Quando um agente gera um memo de decisão automatizado e precisa de validação.
- Em qualquer ponto de inflexão estratégica, operacional ou financeira que exija registro formal.
- Sempre que o valor em jogo exceder o threshold definido na política de governance.

## Agente Responsável
- **Primário:** Chief of Staff Agent (CoS Agent)
- **Revisor:** CEO Agent ou CFO Agent, conforme a natureza da decisão
- **Escalation:** Board Liaison Agent

## Checklist

### Contexto e Enquadramento
- [ ] O memo começa com um resumo executivo de no máximo 3 parágrafos
- [ ] O problema ou oportunidade está descrito de forma clara e objetiva
- [ ] O histórico relevante está documentado com datas e referências
- [ ] Os stakeholders impactados estão listados explicitamente
- [ ] O urgency level está classificado (critical, high, medium, low)
- [ ] O escopo da decisão está delimitado — o que está dentro e fora
- [ ] Os dados de suporte estão referenciados com fontes verificáveis
- [ ] O contexto competitivo ou de mercado está incluído, quando aplicável

### Opções Apresentadas
- [ ] Pelo menos 3 opções viáveis estão listadas (incluindo "não fazer nada")
- [ ] Cada opção tem uma descrição de 2-5 linhas com clareza suficiente
- [ ] Os custos estimados de cada opção estão quantificados (budget, headcount, tempo)
- [ ] O timeline de implementação de cada opção está especificado
- [ ] As dependências de cada opção estão mapeadas
- [ ] A reversibilidade de cada opção está classificada (one-way door vs two-way door)
- [ ] Opções descartadas precocemente estão listadas com justificativa

### Trade-offs Explícitos
- [ ] Os trade-offs entre opções estão documentados em formato comparativo
- [ ] O impacto em velocidade vs qualidade está avaliado
- [ ] O impacto em custo vs benefício está quantificado
- [ ] Os trade-offs de curto prazo vs longo prazo estão articulados
- [ ] Os custos de oportunidade estão identificados para cada opção
- [ ] O impacto em outras iniciativas em andamento está avaliado
- [ ] Os trade-offs técnicos (tech debt, scalability) estão documentados

### Recomendação
- [ ] Existe uma recomendação clara e inequívoca
- [ ] A recomendação está fundamentada com dados e lógica explícita
- [ ] O grau de confiança na recomendação está declarado (high/medium/low)
- [ ] Os pressupostos da recomendação estão listados
- [ ] O cenário de sucesso está descrito com métricas esperadas
- [ ] A recomendação foi stress-tested com perspectivas contrárias
- [ ] O dissent ou opiniões divergentes estão registrados

### Owner e Accountability
- [ ] O owner da decisão está nomeado com nome e cargo
- [ ] O owner da execução está nomeado (pode ser diferente do decisor)
- [ ] A data-limite para a decisão está definida
- [ ] A data de início da execução está definida
- [ ] Os milestones de acompanhamento estão listados com datas
- [ ] O mecanismo de reporting está definido (frequência, formato, destinatários)
- [ ] O escalation path está documentado caso o owner não entregue

### Riscos Identificados
- [ ] Os riscos foram categorizados (financeiro, operacional, reputacional, regulatório, técnico)
- [ ] Cada risco tem probabilidade e impacto estimados
- [ ] Os planos de mitigação estão definidos para riscos de alta severidade
- [ ] Os early warning signals estão identificados
- [ ] O worst-case scenario está descrito com plano de contingência
- [ ] Os riscos de não-decisão (inação) estão documentados
- [ ] O risk owner está atribuído para cada risco material

### Formatação e Compliance
- [ ] O memo segue o template padrão da organização
- [ ] A linguagem é clara, sem jargão desnecessário
- [ ] O memo tem no máximo 2 páginas (excluindo anexos)
- [ ] Os anexos de suporte estão referenciados e acessíveis
- [ ] O memo foi revisado por pelo menos um par antes da submissão
- [ ] O version control está aplicado (data, versão, autor)
- [ ] O memo está armazenado no repositório oficial de decisões

## Critérios de Aprovação
- Todos os itens marcados como obrigatórios devem estar completos (100%).
- Nenhum risco de alta severidade pode estar sem plano de mitigação.
- A recomendação deve ter fundamentação quantitativa ou qualitativa verificável.
- O owner e a data-limite devem estar definidos sem ambiguidade.
- Pelo menos uma revisão por pares deve ter sido realizada.

## O que Fazer se Falhar
1. Devolver o memo ao autor com os itens faltantes destacados.
2. Definir um prazo de 24-48h para correção, conforme urgência.
3. Se o memo falhar duas vezes, escalar para o CoS Agent para mentoria.
4. Registrar o padrão de falha no learning loop (RalphLoop) para melhoria contínua.
5. Não aprovar decisões com memos incompletos — sem exceção.

## Referências
- Bezos, J. — "Six-Page Memo" framework (Amazon)
- Lafley, A.G. & Martin, R. — "Playing to Win" (decisões estratégicas)
- Template interno: `/templates/decision-memo-template.md`
- Política de governance: `/governance/decision-authority-matrix.md`
- RalphLoop registro: `/loops/decision-quality-loop.md`
