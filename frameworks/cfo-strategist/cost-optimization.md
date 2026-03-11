# Framework de Otimização de Custos — Eficiência sem Sacrificar Crescimento

## Propósito e Contexto

Otimização de custos não é cortar despesas — é maximizar o retorno por real investido. Em
momentos de crescimento, significa investir cada real onde gera mais impacto. Em momentos de
contração, significa preservar as capabilities estratégicas enquanto elimina o desperdício.
A diferença entre empresas que sobrevivem crises e as que não sobrevivem raramente é a receita
— é a disciplina de custos que foi (ou não) construída durante os tempos bons.

Este framework fornece um processo estruturado para identificar oportunidades de otimização,
priorizar ações por impacto vs. risco, e implementar mudanças sem destruir a capacidade de
crescimento futuro.

## Quando Usar

- Em revisões trimestrais de budget (proativo, não reativo)
- Quando burn rate excede o planejado por 2+ meses consecutivos
- Na preparação para downturn econômico ou redução de mercado
- Pós-fundraising para estender runway
- Quando gross margin está abaixo do benchmark da indústria
- Ao integrar empresa adquirida (sinergias de custo)

## Componentes do Framework

### 1. Mapa de Custos (Cost Map)

Organize todos os custos em uma matriz 2×2:

| | Estratégico (gera diferenciação) | Operacional (mantém o negócio) |
|---|---|---|
| **Variável** | Investimento em growth | Custos de atendimento |
| **Fixo** | Salários de core team | Overhead e administração |

**Regra:** Proteja custos estratégicos. Otimize custos operacionais. Questione custos fixos
que não são mais estratégicos.

### 2. Framework de Priorização (Impact vs. Effort)

Para cada oportunidade de otimização:
- **Impacto Financeiro:** R$/mês de savings
- **Risco Operacional:** Chance de impactar negativamente a operação (1-5)
- **Esforço de Implementação:** Tempo e recursos necessários (1-5)
- **Reversibilidade:** Facilidade de reverter se der errado (1-5)

Score = Impacto × (5 - Risco) × (5 - Esforço) × Reversibilidade

### 3. As 7 Alavancas de Otimização

**Alavanca 1: Renegociação de Contratos**
- SaaS: volume discounts, annual vs. monthly, competitive bids
- Cloud: reserved instances, committed use discounts, spot instances
- Fornecedores: consolidação, renegociação de termos
- Impacto típico: 10-30% de redução em contratos renegociados

**Alavanca 2: Eliminação de Waste**
- SaaS não utilizado (shadow IT, licenças ociosas)
- Cloud resources over-provisioned
- Processos que ninguém sabe por que existem
- Meetings sem output definido
- Impacto típico: 5-15% do total de custos operacionais

**Alavanca 3: Automação**
- Tarefas manuais repetitivas (reports, provisioning, onboarding)
- Processos que podem ser self-service
- Testes manuais que podem ser automatizados
- Impacto típico: 20-40% de redução em custo da tarefa automatizada

**Alavanca 4: Consolidação**
- Múltiplas ferramentas que fazem a mesma coisa
- Times redundantes em estruturas diferentes
- Ambientes e infraestrutura duplicados
- Impacto típico: 15-25% de redução por consolidação

**Alavanca 5: Rightsizing**
- Headcount: funções que podem ser combinadas
- Infra: instances que podem ser redimensionados
- Office: espaço físico vs. modelo híbrido
- Impacto típico: 10-20% de redução na área rightsized

**Alavanca 6: Shift de Modelo**
- Fixed → Variable: transformar custo fixo em variável
- In-house → Outsource: para atividades não-core
- On-premise → Cloud (ou vice-versa, dependendo do estágio)
- Impacto típico: varia significativamente por caso

**Alavanca 7: Otimização de Unit Economics**
- Reduzir COGS por transação/cliente
- Melhorar conversão (mais receita, mesmo CAC)
- Reduzir churn (estender LTV sem custo adicional)
- Impacto típico: 5-15% de melhoria em gross margin

## Processo Passo-a-Passo

### Fase 1: Diagnóstico (1-2 semanas)
1. Extrair todos os custos dos últimos 6 meses (por fornecedor, por categoria)
2. Classificar no Cost Map (estratégico/operacional × fixo/variável)
3. Benchmarking: comparar % de custos por categoria com peers
4. Identificar os top 20 fornecedores (tipicamente 80% do gasto)

### Fase 2: Identificação de Oportunidades (1 semana)
1. Aplicar cada uma das 7 alavancas sistematicamente
2. Para cada oportunidade, estimar impacto, risco e esforço
3. Priorizar usando o scoring model
4. Validar com owners das áreas (eles conhecem a realidade)

### Fase 3: Plano de Execução (1-2 semanas)
1. Quick wins (< 1 mês): implementar imediatamente
2. Projetos médios (1-3 meses): planejar e alocar recursos
3. Transformações (3-6 meses): business case e aprovação executiva
4. Definir savings target por trimestre

### Fase 4: Implementação e Monitoramento
1. Owner designado para cada iniciativa de otimização
2. Tracking mensal de savings realizados vs. planejados
3. Ajustes baseados em impacto real (algumas otimizações não entregam)
4. Comunicação transparente — otimização, não austeridade punitiva

## Template de Oportunidade de Otimização

```markdown
# Oportunidade: [Nome descritivo]

**Alavanca:** [1-7, qual das alavancas]
**Categoria:** [Quick win | Projeto | Transformação]
**Owner:** [Responsável]

## Situação Atual
- Custo atual: R$ [X]/mês
- Descrição: [O que é e por que custa isso]

## Proposta
- Ação: [O que fazer]
- Custo alvo: R$ [Y]/mês
- Saving: R$ [Z]/mês ([W]% redução)

## Análise de Risco
- Risco operacional: [descrição e mitigação]
- Reversibilidade: [sim/parcialmente/não]
- Dependências: [o que precisa acontecer antes]

## Timeline
- Início: [data]
- Saving realizado a partir de: [data]
- Saving anualizado: R$ [X]
```

## Checklist de Otimização

- [ ] Todos os custos foram mapeados e categorizados?
- [ ] SaaS audit realizado (licenças ativas vs. necessárias)?
- [ ] Cloud cost review nos últimos 3 meses?
- [ ] Top 20 contratos revisados para renegociação?
- [ ] Custos estratégicos estão protegidos explicitamente?
- [ ] Impacto em moral e cultura foi considerado?
- [ ] Savings targets são realistas e mensuráveis?
- [ ] Comunicação para a equipe está planejada?

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Savings realizados vs. target | > 80% do planejado | Mensal |
| Burn rate trend | Decrescente ou estável com crescimento | Mensal |
| Gross margin | Trend de melhoria | Trimestral |
| Cost per employee | Dentro de benchmark | Trimestral |
| Cloud cost per transaction | Decrescente | Mensal |
| Revenue per employee | Crescente | Trimestral |

## Referências Cruzadas

- `frameworks/cfo-strategist/financial-planning.md` — Budget como referência para otimização
- `frameworks/cfo-strategist/unit-economics.md` — Impact on COGS and margins
- `frameworks/cfo-strategist/scenario-planning.md` — Cenários que trigam otimização
- `frameworks/cto-architect/build-vs-buy.md` — Build decisions com implicação de custo
- `frameworks/cto-architect/tech-debt-management.md` — Debt que gera custo desnecessário
- `frameworks/cio-engineer/cloud-strategy.md` — Otimização de custos de cloud
- `frameworks/shared/change-leadership.md` — Comunicação de mudanças de custo
