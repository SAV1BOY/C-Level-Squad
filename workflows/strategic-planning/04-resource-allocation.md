# Workflow: Alocação de Recursos

## Objetivo
Traduzir escolhas estratégicas em alocação concreta de recursos (pessoas, dinheiro e tempo), garantindo que investimento esteja alinhado com prioridades estratégicas.

---

## 1. Princípios de Alocação

### Regras Fundamentais
- Recursos devem seguir a estratégia, não o inverso
- Dizer sim para tudo é o mesmo que não ter estratégia
- Alocação é um exercício de trade-offs, não de consenso
- Investir desproporcionalmente nas apostas mais importantes
- Manter buffer para oportunidades e emergências (10-15%)

### Anti-patterns Comuns
- **Peanut butter spreading**: Distribuir recursos igualmente entre tudo
- **Legacy tax**: Manter investimento em produtos legados por inércia
- **Squeaky wheel**: Quem reclama mais alto recebe mais recursos
- **Democracy of priorities**: Tudo é prioridade 1, nada é prioridade
- **Sunk cost**: Continuar investindo porque já gastou muito

---

## 2. Framework de Alocação

### 2.1 Categorias de Investimento (Horizons)

| Horizonte | Descrição | % do Budget | % do Headcount | Exemplos |
|-----------|-----------|------------|---------------|---------|
| H1: Core Business | Manter e crescer negócio atual | 60-70% | 60-70% | Produto core, vendas, CS |
| H2: Emerging | Escalar novas oportunidades validadas | 20-25% | 20-25% | Novo módulo, novo mercado |
| H3: Future | Explorar apostas de longo prazo | 5-15% | 5-10% | R&D, AI experimental |

### 2.2 Mapeamento de Iniciativas por Horizonte

| Iniciativa | Horizonte | Investimento (R$) | Headcount | ROI Esperado | Timeline |
|-----------|-----------|-------------------|-----------|-------------|----------|
| [Iniciativa 1] | H1 | [R$ X] | [X pessoas] | [X% em Y meses] | [Q1-Q4] |
| [Iniciativa 2] | H1 | [R$ X] | [X pessoas] | [X% em Y meses] | [Q1-Q2] |
| [Iniciativa 3] | H2 | [R$ X] | [X pessoas] | [Validação] | [Q1-Q3] |
| [Iniciativa 4] | H3 | [R$ X] | [X pessoas] | [Aprendizado] | [Q2-Q4] |

---

## 3. Alocação de Pessoas

### Inventário de Capacidade

| Área | Headcount Atual | Vagas Abertas | Capacidade Total | Utilização |
|------|----------------|--------------|-----------------|-----------|
| Engineering | [X] | [Y] | [X+Y] | [Z%] |
| Produto | [X] | [Y] | [X+Y] | [Z%] |
| Design | [X] | [Y] | [X+Y] | [Z%] |
| Data/AI | [X] | [Y] | [X+Y] | [Z%] |
| Vendas | [X] | [Y] | [X+Y] | [Z%] |
| CS | [X] | [Y] | [X+Y] | [Z%] |
| Marketing | [X] | [Y] | [X+Y] | [Z%] |

### Alocação por Iniciativa Estratégica

| Iniciativa | Eng | Produto | Design | Data | Total | % do Total |
|-----------|-----|---------|--------|------|-------|-----------|
| [Core Product] | [X] | [Y] | [Z] | [W] | [T] | [P%] |
| [New Module] | [X] | [Y] | [Z] | [W] | [T] | [P%] |
| [AI R&D] | [X] | [Y] | [Z] | [W] | [T] | [P%] |
| [Platform] | [X] | [Y] | [Z] | [W] | [T] | [P%] |
| [Innovation] | [X] | [Y] | [Z] | [W] | [T] | [P%] |

### Decisões de Headcount
- [ ] Definir prioridade de contratação por posição
- [ ] Identificar realocações internas possíveis
- [ ] Definir contractors vs full-time para cada necessidade
- [ ] Planejar timeline de contratação por trimestre
- [ ] Calcular custo total de pessoal com encargos

---

## 4. Alocação Financeira

### Budget por Categoria

| Categoria | Q1 | Q2 | Q3 | Q4 | Total Anual | % do Total |
|----------|----|----|----|----|------------|-----------|
| Pessoal | [R$] | [R$] | [R$] | [R$] | [R$] | [X%] |
| Infraestrutura | [R$] | [R$] | [R$] | [R$] | [R$] | [X%] |
| Marketing | [R$] | [R$] | [R$] | [R$] | [R$] | [X%] |
| Vendas (comissões) | [R$] | [R$] | [R$] | [R$] | [R$] | [X%] |
| Ferramentas/SaaS | [R$] | [R$] | [R$] | [R$] | [R$] | [X%] |
| R&D | [R$] | [R$] | [R$] | [R$] | [R$] | [X%] |
| Contingência | [R$] | [R$] | [R$] | [R$] | [R$] | [X%] |
| **Total** | **[R$]** | **[R$]** | **[R$]** | **[R$]** | **[R$]** | **100%** |

### Cenários
| Cenário | Trigger | Ação |
|---------|---------|------|
| Base | Plano atual se mantém | Executar conforme planejado |
| Otimista | Receita 20% acima do plano | Acelerar H2, contratar mais rápido |
| Pessimista | Receita 20% abaixo do plano | Cortar H3, pausar contratações H2 |
| Crise | Receita 40% abaixo | Reduzir para core, freeze total |

---

## 5. Gestão de Portfolio

### Framework de Priorização (WSJF)

Para cada iniciativa, calcular WSJF:
- **WSJF = Cost of Delay / Job Size**
- Cost of Delay = User/Business Value + Time Criticality + Risk Reduction
- Job Size = Esforço estimado em story points, semanas ou headcount-months

| Iniciativa | Business Value | Time Criticality | Risk Reduction | CoD | Job Size | WSJF | Rank |
|-----------|---------------|-----------------|---------------|-----|----------|------|------|
| [Init A] | [1-10] | [1-10] | [1-10] | [Soma] | [T-shirt] | [CoD/Size] | [#] |
| [Init B] | [1-10] | [1-10] | [1-10] | [Soma] | [T-shirt] | [CoD/Size] | [#] |

### Kill Criteria
Definir antecipadamente quando cancelar ou pausar uma iniciativa:
- Milestone 1 não atingido até data X: revisar investimento
- Métrica Y não atinge threshold Z em 90 dias: pausar e avaliar
- Budget excede 150% do planejado: escalate para decisão executiva
- Market conditions mudam significativamente: reavaliação completa

---

## 6. Governance e Review

### Cadência de Review
| Forum | Frequência | Participantes | Decisões |
|-------|-----------|---------------|----------|
| Portfolio Review | Mensal | C-Level | Ajuste de alocação entre iniciativas |
| Budget Review | Trimestral | CFO + áreas | Rebalanceamento de budget |
| Strategic Review | Semestral | C-Level + Board | Mudanças significativas de alocação |
| Planning | Anual | Organização | Definição completa de alocação |

### Métricas de Eficiência de Alocação
- ROI por iniciativa vs planejado
- % de recursos em H1/H2/H3 vs meta
- Custo por engineering hour
- Revenue per employee
- Velocidade de contratação vs plano
- Burn rate vs runway

### Próximo Passo
Alocação de recursos alimenta o workflow 05 (Tracking de Execução).
