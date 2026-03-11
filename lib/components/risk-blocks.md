# Risk Blocks — Blocos Reutilizáveis para Gestão de Riscos

> Referência do C-Level Squad para documentar, avaliar e gerenciar riscos individuais.
> Complementa `risk-scoring.md` (metodologia) com templates práticos para cada componente do risk management.

---

## 1. Risk Description Template

### Propósito
Descrever um risco de forma clara, completa e não ambígua, seguindo um formato padronizado que facilita avaliação e comunicação.

### Template

```markdown
## Risk: [ID] — [Título curto e descritivo]

### Descrição estruturada
**Evento:** [O QUE pode acontecer]
**Causa(s):** [POR QUE pode acontecer — pode haver múltiplas causas]
**Consequência(s):** [O impacto SE acontecer — em termos concretos]

### Frase-resumo (formato padrão)
"Existe o risco de que [EVENTO] ocorra devido a [CAUSA], resultando em [CONSEQUÊNCIA]
para [ÁREA/STAKEHOLDER AFETADO]."

### Metadados
- **ID:** [R-YYYY-NNN — ex: R-2026-015]
- **Categoria:** [Estratégico / Operacional / Tecnológico / Informacional / AI / Mercado / Financeiro / Regulatório / Pessoas]
- **Data de identificação:** [YYYY-MM-DD]
- **Identificado por:** [Agente]
- **Status:** [Aberto / Em mitigação / Aceito / Transferido / Fechado]
```

### Regras de boa descrição de risco
1. **Específico:** "Falha no banco de dados" é vago. "Corrupção de dados no PostgreSQL RDS da AWS por falha de disco sem backup validado em <24h" é específico
2. **Causa raiz:** Não descrever sintomas. Usar 5 Whys se necessário
3. **Consequência tangível:** Quantificar quando possível (R$, horas, clientes afetados)
4. **Não confundir risco com problema:** Risco é incerto (pode acontecer). Problema já aconteceu
5. **Não confundir risco com constraint:** "Temos pouco budget" é constraint, não risco

### Exemplos por categoria

```markdown
## Estratégico
"Existe o risco de que um competidor bem-financiado entre no segmento de AI para PMEs
no Brasil, devido ao crescimento atrativo do mercado (40% ao ano), resultando em
guerra de preços e compressão de margens de 30% para a área comercial."

## Tecnológico
"Existe o risco de que a plataforma sofra downtime prolongado (>4h) durante pico de
uso, devido à arquitetura monolítica não ter sido testada para >5.000 usuários
simultâneos, resultando em perda estimada de R$200K em receita e queda de NPS."

## AI/ML
"Existe o risco de que o modelo de credit scoring apresente viés contra determinados
grupos demográficos, devido a dados de treinamento historicamente enviesados,
resultando em violação regulatória (LGPD) e dano reputacional."

## Pessoas
"Existe o risco de que o Tech Lead principal (único com conhecimento da arquitetura
core) saia da empresa, devido a oferta competitiva do mercado e falta de plano de
crescimento interno, resultando em atraso de 3-6 meses no roadmap técnico."
```

---

## 2. Probability Assessment Block

### Propósito
Avaliar a probabilidade de um risco se materializar de forma estruturada e justificada.

### Template

```markdown
## Probability Assessment — [Risk ID]

### Score de probabilidade: [1-5]

| Score | Nível        | Probabilidade | Frequência esperada        |
|-------|-------------|---------------|---------------------------|
| 1     | Raro        | <5%           | Menos de 1× em 5 anos     |
| 2     | Improvável  | 5-20%         | 1× em 2-5 anos            |
| 3     | Possível    | 20-50%        | 1× em 1-2 anos            |
| 4     | Provável    | 50-80%        | 1-3× por ano              |
| 5     | Quase certo | >80%          | Múltiplas vezes por ano    |

### Justificativa do score

#### Evidências que aumentam a probabilidade
- [Evidência 1: ex. "Já aconteceu 2× nos últimos 12 meses"]
- [Evidência 2: ex. "Controles preventivos inexistentes"]
- [Evidência 3: ex. "Tendência de mercado aponta nesta direção"]

#### Evidências que diminuem a probabilidade
- [Evidência 1: ex. "Temos monitoramento em tempo real"]
- [Evidência 2: ex. "Investimos em redundância"]

#### Analogias e base rates
- Base rate para este tipo de risco: [X%] (fonte: [referência])
- Ajuste para nosso contexto: [+/-Y%] porque [razão]
- Probabilidade estimada final: [Z%] → Score [N]

### Fatores de volatilidade
[O que poderia mudar rapidamente a probabilidade?]
- [Fator 1: ex. "Mudança regulatória em discussão no Congresso"]
- [Fator 2: ex. "Entrada de novo competidor rumored"]

### Próxima reavaliação: [data]
```

### Técnicas de estimativa de probabilidade
1. **Base rate:** Consultar `base-rate-checks.md` para frequência histórica
2. **Análise de cenários:** Listar condições necessárias e avaliar probabilidade de cada
3. **Expert judgment:** Consultar 2-3 especialistas independentemente, usar mediana
4. **Histórico interno:** Quantas vezes eventos similares ocorreram na organização
5. **Pre-mortem:** "Se isso acontecer, olhando para trás, qual caminho nos levou lá?"

---

## 3. Impact Assessment Block

### Propósito
Avaliar o impacto caso o risco se materialize, considerando múltiplas dimensões.

### Template

```markdown
## Impact Assessment — [Risk ID]

### Score de impacto geral: [1-5]

### Avaliação por dimensão

| Dimensão        | Score (1-5) | Descrição do impacto              | Quantificação          |
|-----------------|-------------|-----------------------------------|------------------------|
| Financeiro      | [1-5]       | [descrição]                       | R$ [valor]             |
| Operacional     | [1-5]       | [descrição]                       | [horas de interrupção] |
| Reputacional    | [1-5]       | [descrição]                       | [alcance/severidade]   |
| Legal/Regulatório| [1-5]      | [descrição]                       | [tipo de exposição]    |
| Pessoas         | [1-5]       | [descrição]                       | [turnover/moral]       |
| Estratégico     | [1-5]       | [descrição]                       | [impacto em bets]      |

### Score final: [Maior score entre as dimensões — worst case drives the rating]

### Cascata de impacto (efeitos de segunda ordem)
[Se este risco se materializar, que OUTROS riscos ele dispara?]
1. [Efeito cascata 1: ex. "Downtime → perda de cliente enterprise → pressão de revenue"]
2. [Efeito cascata 2: ex. "Viés em modelo → ação regulatória → restrição em todos os modelos"]

### Cenários de impacto

| Cenário       | Probabilidade | Impacto estimado | Descrição                          |
|---------------|---------------|------------------|------------------------------------|
| Melhor caso   | [%]           | [R$/descrição]   | [O risco se materializa de forma contida] |
| Caso esperado | [%]           | [R$/descrição]   | [Impacto médio, sem agravantes]    |
| Pior caso     | [%]           | [R$/descrição]   | [Múltiplos agravantes, cascata]    |

### Reversibilidade
- **Tempo para recuperação:** [horas/dias/semanas/meses]
- **Custo de recuperação:** [R$]
- **Dano permanente:** [Sim/Não — se sim, qual]
```

---

## 4. Mitigation Strategy Block

### Propósito
Definir ações proativas para reduzir a probabilidade ou o impacto do risco antes que ele se materialize.

### Template

```markdown
## Mitigation Strategy — [Risk ID]

### Tipo de estratégia

| Estratégia   | Descrição                                          | Quando usar                        |
|-------------|----------------------------------------------------|------------------------------------|
| **Evitar**  | Eliminar a causa ou mudar o plano para não expor   | Risco inaceitável e evitável       |
| **Reduzir** | Diminuir probabilidade e/ou impacto               | Risco tolerável com controles      |
| **Transferir** | Passar o risco para terceiro (seguro, contrato)| Risco financeiro quantificável     |
| **Aceitar** | Reconhecer o risco sem ação de mitigação           | Risco baixo ou custo de mitigação > impacto |

### Estratégia escolhida: [Evitar / Reduzir / Transferir / Aceitar]

### Ações de mitigação

| # | Ação                              | Tipo        | Reduz P ou I? | Custo     | DRI     | Deadline   | Status       |
|---|-----------------------------------|-------------|---------------|-----------|---------|------------|-------------|
| 1 | [Ação concreta]                   | [Preventiva/Detectiva] | [P/I/Ambos] | [R$]  | [agente]| [data]     | [status]    |
| 2 | [Ação 2]                          | [tipo]      | [P/I]         | [R$]     | [agente]| [data]     | [status]    |

### Tipos de ação
- **Preventiva:** Reduz a probabilidade de o risco acontecer
- **Detectiva:** Identifica o risco mais cedo (permite resposta rápida)
- **Corretiva:** Reduz o impacto após materialização

### Risco residual após mitigação
- **P original:** [1-5] → **P residual:** [1-5]
- **I original:** [1-5] → **I residual:** [1-5]
- **Risk Score original:** [P×I] → **Risk Score residual:** [P×I]
- **O risco residual é aceitável?** [Sim / Não — se não, mais mitigação necessária]

### Custo total de mitigação: R$ [soma das ações]
### Custo vs. benefício: [Custo de mitigação] vs. [EMV do risco] = [vale a pena? Sim/Não]
```

---

## 5. Contingency Plan Block

### Propósito
Definir o plano de resposta caso o risco se materialize apesar das mitigações. É o "Plano B" preparado antecipadamente.

### Template

```markdown
## Contingency Plan — [Risk ID]

### Trigger de ativação
**O plano de contingência é ativado quando:**
[Condição específica e observável que indica que o risco se materializou]
- Indicador: [métrica ou evento que dispara o plano]
- Threshold: [valor ou condição específica]
- Quem detecta: [sistema automático / pessoa / processo]

### Ações de resposta imediata (primeiras 24h)

| # | Ação                              | Responsável | Timeline | Dependência |
|---|-----------------------------------|-------------|----------|-------------|
| 1 | [Ação de contenção imediata]      | [agente]    | [0-2h]   | —           |
| 2 | [Comunicação para stakeholders]   | [agente]    | [0-4h]   | #1          |
| 3 | [Ação de investigação]            | [agente]    | [0-24h]  | #1          |

### Ações de recuperação (dias 2-14)

| # | Ação                              | Responsável | Timeline  | Critério de done |
|---|-----------------------------------|-------------|-----------|------------------|
| 4 | [Ação de correção da causa raiz]  | [agente]    | [2-5 dias]| [critério]       |
| 5 | [Ação de restauração do serviço]  | [agente]    | [3-7 dias]| [critério]       |

### Comunicação durante contingência

| Audiência           | Canal        | Frequência     | Responsável | Conteúdo                     |
|--------------------|-------------|----------------|-------------|------------------------------|
| CEO / Squad        | [canal]     | [a cada Xh]    | [agente]    | Status + ETA + decisões      |
| Clientes afetados  | [canal]     | [frequência]   | [agente]    | Impacto + ações + ETA        |
| Time interno       | [canal]     | [frequência]   | [agente]    | Status + o que fazer/não fazer|

### Recursos pré-autorizados para contingência
- **Budget emergencial:** Até R$ [X] sem aprovação adicional
- **Pessoas:** [quem pode ser mobilizado]
- **Fornecedores:** [parceiros que podem ajudar — com contato]

### Post-mortem (obrigatório após ativação)
- Conduzir em até 5 dias úteis após resolução
- Template: blameless post-mortem
- Objetivo: prevenir recorrência, não atribuir culpa
```

---

## 6. Risk Owner Block

### Propósito
Definir claramente quem é responsável por cada aspecto da gestão do risco.

### Template

```markdown
## Risk Ownership — [Risk ID]

### Papéis

| Papel             | Agente  | Responsabilidade                                     |
|-------------------|---------|------------------------------------------------------|
| **Risk Owner**    | [agente]| Responsável por monitorar e gerenciar o risco. Ponto focal para escalação |
| **Mitigação DRI** | [agente]| Executa as ações de mitigação no dia-a-dia           |
| **Escalação para**| [agente]| Recebe escalação se risco mudar de nível ou se materializar |
| **Sponsor**       | [agente]| Aprova budget e recursos para mitigação               |

### Responsabilidades do Risk Owner
1. Manter a avaliação de P×I atualizada (mínimo: conforme cadência do nível do risco)
2. Garantir que ações de mitigação estão sendo executadas no prazo
3. Reportar status conforme cadência:
   - Risco Baixo: mensal
   - Risco Médio: quinzenal
   - Risco Alto: semanal
   - Risco Crítico: diário
4. Escalar imediatamente se:
   - Risco muda de nível (ex: de Médio para Alto)
   - Mitigação está bloqueada ou atrasada
   - Risco se materializa (ativar contingency plan)
5. Conduzir review trimestral: o risco ainda é relevante? Score precisa atualizar?
6. Propor fechamento quando o risco não é mais relevante

### Handoff protocol
Se o Risk Owner mudar (ex: rotação, saída):
1. Sessão de handoff de 30 minutos com novo owner
2. Documentar todo o histórico do risco no risk register
3. Novo owner confirma entendimento e aceita ownership
4. Comunicar mudança de ownership a todos os stakeholders
```

---

## 7. Monitoring Trigger Block

### Propósito
Definir quais indicadores antecedentes monitorar e quais thresholds ativam ação.

### Template

```markdown
## Monitoring Triggers — [Risk ID]

### Indicadores monitorados

| # | Indicador                    | Fonte           | Frequência | Threshold amarelo | Threshold vermelho |
|---|------------------------------|-----------------|------------|-------------------|--------------------|
| 1 | [Indicador early warning 1]  | [sistema/manual]| [diário/semanal] | [valor]     | [valor]            |
| 2 | [Indicador 2]                | [fonte]         | [freq]     | [valor]           | [valor]            |
| 3 | [Indicador 3]                | [fonte]         | [freq]     | [valor]           | [valor]            |

### Ações por threshold

**Threshold amarelo atingido:**
1. Risk Owner notificado automaticamente
2. Reavaliação de P×I em 48h
3. Verificar se mitigações estão ativas e efetivas
4. Reportar no próximo risk review

**Threshold vermelho atingido:**
1. Risk Owner + Escalação notificados imediatamente
2. Avaliar se contingency plan deve ser ativado
3. Reunião de avaliação em 24h
4. Comunicação ampla se necessário

### Alertas configurados
- [ ] Alerta automático para threshold amarelo: [canal]
- [ ] Alerta automático para threshold vermelho: [canal]
- [ ] Dashboard de monitoramento: [link]
- [ ] Responsável por verificar manualmente: [agente]
```

---

## 8. Review Cadence Block

### Propósito
Definir quando e como o risco será revisado para garantir que avaliações permaneçam atuais.

### Template

```markdown
## Review Cadence — [Risk ID]

### Frequência de review

| Nível do risco | Frequência  | Formato              | Participantes           |
|---------------|-------------|----------------------|-------------------------|
| Crítico (16-25)| Diário     | Standup dedicado 15m | Risk Owner + CEO        |
| Alto (10-15)  | Semanal     | Item na weekly review | Risk Owner + Sponsor    |
| Médio (5-9)   | Quinzenal   | Atualização no register | Risk Owner            |
| Baixo (1-4)   | Mensal      | Review no risk register | Risk Owner            |

### Checklist de review

Em cada review, o Risk Owner responde:
- [ ] A probabilidade mudou? [Sim → novo score + justificativa]
- [ ] O impacto mudou? [Sim → novo score + justificativa]
- [ ] As mitigações estão progredindo conforme planejado?
- [ ] Novos fatores surgiram (positivos ou negativos)?
- [ ] Os monitoring triggers estão funcionando?
- [ ] O contingency plan precisa de atualização?
- [ ] Este risco ainda é relevante? [Se não → propor fechamento]

### Histórico de reviews

| Data       | P   | I   | Score | Status        | Observação                      |
|------------|-----|-----|-------|---------------|---------------------------------|
| [data 1]   | [P] | [I] | [S]   | [status]      | [nota]                          |
| [data 2]   | [P] | [I] | [S]   | [status]      | [nota]                          |

### Gatilhos de review extraordinária (fora da cadência regular)
- Qualquer evento relevante no mercado/indústria
- Mudança significativa na organização (re-org, M&A, pivô)
- Resultado de mitigação significativamente diferente do esperado
- Solicitação de qualquer agente do Squad
```

---

## 9. Montagem — Risk Register Entry completo

```markdown
## [R-2026-XXX] — [Título do Risco]

### Descrição (Risk Description Template)
[Evento + Causa + Consequência]

### Avaliação
| P | I | Score | Nível   | Trend |
|---|---|-------|---------|-------|
| [X]|[X]| [XX] | [nível] | [↑↓→] |

### Probability Assessment
[Justificativa breve]

### Impact Assessment
[Dimensões mais relevantes]

### Mitigation Strategy
[Ações em andamento — resumo]

### Contingency Plan
[Resumo do plano B]

### Ownership
| Owner | Mitigação DRI | Escalação | Sponsor |
|-------|---------------|-----------|---------|
| [ag]  | [ag]          | [ag]      | [ag]    |

### Monitoring
[Indicadores e thresholds — resumo]

### Review
[Próxima review: data] | [Cadência: frequência]

### Status: [Aberto / Em mitigação / Aceito / Transferido / Fechado]
### Última atualização: [data]
```
