# Gestão de Risco Compartilhada — Framework Corporativo de Riscos

## Propósito e Contexto

Risco é a probabilidade de algo dar errado multiplicada pelo impacto se der errado. Gestão de
risco não é evitar riscos — é tomar riscos conscientes e gerenciáveis enquanto se protege
contra riscos que podem ser fatais. Empresas de tecnologia em crescimento tendem a ignorar
gestão de risco (porque "somos ágeis e rápidos") até que uma crise revela que riscos ignorados
não desaparecem — acumulam.

Este framework cria um sistema leve mas eficaz de identificação, avaliação, mitigação e
monitoramento de riscos, compartilhado entre todas as áreas da organização. Cada C-level é
responsável pelos riscos de sua área; o framework garante que riscos cross-funcionais não
caiam nas lacunas entre áreas.

## Quando Usar

- No planejamento estratégico anual (identificação de riscos ao plano)
- Em reuniões trimestrais de risk review
- Ao tomar decisões Type 1 (irreversíveis e de alto impacto)
- Na preparação para fundraising ou IPO (risk disclosure)
- Quando eventos externos mudam o perfil de risco (regulação, mercado, competição)
- Na construção de plano de contingência

## Componentes do Framework

### 1. Taxonomia de Riscos

**Riscos Estratégicos:**
- Market risk: mercado não evolui como a tese prevê
- Competitive risk: concorrente com vantagem disruptiva
- Execution risk: incapacidade de executar a estratégia
- Concentration risk: dependência de poucos clientes/mercados

**Riscos Operacionais:**
- Technology risk: falha de sistemas críticos, security breach
- People risk: perda de talentos-chave, cultura tóxica
- Process risk: processos inadequados para a escala atual
- Vendor risk: dependência de fornecedores críticos

**Riscos Financeiros:**
- Liquidity risk: ficar sem caixa antes do próximo funding
- Currency risk: exposição cambial significativa
- Revenue concentration: top 3 clientes > 30% da receita
- Cost escalation: custos crescendo mais rápido que receita

**Riscos de Compliance:**
- Regulatory risk: mudanças regulatórias adversas (LGPD, AI Act)
- Legal risk: litígios, IP disputes
- Tax risk: contingências fiscais
- Labor risk: contingências trabalhistas

**Riscos Reputacionais:**
- Brand risk: incidente público que danifica a marca
- Trust risk: violação de confiança de clientes ou parceiros
- Ethics risk: decisões questionáveis eticamente (AI bias, etc.)

### 2. Matriz de Risco (Probabilidade × Impacto)

| | Impacto Baixo | Impacto Médio | Impacto Alto | Impacto Crítico |
|---|---|---|---|---|
| **Alta Probabilidade** | Aceitar | Mitigar | Mitigar urgente | Evitar |
| **Média Probabilidade** | Aceitar | Monitorar | Mitigar | Mitigar urgente |
| **Baixa Probabilidade** | Aceitar | Aceitar | Monitorar | Mitigar |
| **Muito Baixa** | Aceitar | Aceitar | Aceitar | Monitorar |

**Classificação de Impacto:**
- Baixo: < 5% de impacto em receita ou operação
- Médio: 5-15% de impacto
- Alto: 15-30% de impacto
- Crítico: > 30% de impacto ou risco existencial

### 3. Estratégias de Resposta

**Evitar:** Eliminar a causa do risco (mudar de abordagem)
**Mitigar:** Reduzir probabilidade ou impacto (controles, redundância)
**Transferir:** Passar o risco para terceiro (seguro, contrato)
**Aceitar:** Reconhecer e monitorar sem ação (risco dentro da tolerância)

### 4. Risk Register

```markdown
| ID | Risco | Categoria | Prob. | Impacto | Score | Owner | Estratégia | Status |
|----|-------|-----------|-------|---------|-------|-------|-----------|--------|
| R01 | [desc] | [cat] | [1-4] | [1-4] | [PxI] | [nome] | [E/M/T/A] | [status] |
```

## Processo Passo-a-Passo

### Ciclo Trimestral de Risk Review

**Semana 1: Atualização**
1. Cada C-level atualiza os riscos da sua área no register
2. Novos riscos identificados são adicionados
3. Riscos resolvidos são fechados
4. Probabilidade e impacto são re-avaliados

**Semana 2: Consolidação e Review**
1. CFO ou COO consolida o risk register
2. Sessão de risk review com C-level (2 horas)
3. Foco nos top 10 riscos por score
4. Validação de estratégias de mitigação
5. Identificação de riscos emergentes

**Semana 3: Ação**
1. Planos de mitigação atualizados para riscos priorizados
2. Owners confirmam ações e timelines
3. Dashboard de riscos atualizado
4. Comunicação para board (riscos relevantes)

### Processo Contínuo
1. Qualquer líder pode adicionar riscos ao register a qualquer momento
2. Riscos críticos disparam review imediata (não espera o ciclo trimestral)
3. Post-mortem de incidentes alimenta o risk register
4. Riscos fechados são arquivados com lições aprendidas

## Template de Risk Assessment

```markdown
# Risk Assessment: [Nome do Risco]

**ID:** R[XX]
**Categoria:** [Estratégico/Operacional/Financeiro/Compliance/Reputacional]
**Owner:** [C-level responsável]
**Data de Identificação:** [YYYY-MM-DD]

## Descrição
[O que pode acontecer e em que contexto]

## Avaliação
- Probabilidade: [1-Muito Baixa, 2-Baixa, 3-Média, 4-Alta]
- Impacto: [1-Baixo, 2-Médio, 3-Alto, 4-Crítico]
- Score: [Prob × Impacto]

## Cenário de Materialização
[O que acontece se o risco se materializar — em detalhe]

## Controles Existentes
[O que já temos que reduz probabilidade ou impacto]

## Plano de Mitigação
| Ação | Owner | Prazo | Status |
|------|-------|-------|--------|
| [ação] | [nome] | [data] | [TODO/DONE] |

## Trigger Indicators
[Sinais antecipados de que o risco está se materializando]

## Plano de Contingência
[O que fazer se o risco se materializar apesar da mitigação]
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Risk review completion | 100% trimestral | Trimestral |
| Riscos com owner definido | 100% | Contínuo |
| Riscos críticos com plano de mitigação | 100% | Contínuo |
| Riscos materializados com contingência pré-definida | > 80% | Por incidente |
| Time-to-identify (novo risco → registro) | < 1 semana | Contínuo |
| Risk register freshness | Atualizado < 90 dias | Trimestral |

## Referências Cruzadas

- `frameworks/shared/crisis-management.md` — Quando riscos se materializam
- `frameworks/shared/decision-framework.md` — Risco como input para decisões
- `frameworks/shared/stakeholder-management.md` — Comunicação de riscos para stakeholders
- `frameworks/cfo-strategist/scenario-planning.md` — Cenários baseados em riscos
- `frameworks/cfo-strategist/financial-planning.md` — Riscos financeiros
- `frameworks/cio-engineer/security-posture.md` — Riscos de segurança
- `frameworks/caio-architect/responsible-ai.md` — Riscos de AI
- `frameworks/vision-chief/board-communication.md` — Reporting de riscos para o board
