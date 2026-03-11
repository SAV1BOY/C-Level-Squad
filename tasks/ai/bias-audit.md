# Auditoria de Bias em AI

> Processo estruturado para identificar, medir e mitigar vieses em sistemas
> de AI, garantindo equidade, conformidade regulatória e confiança dos stakeholders.

## Objetivo

Identificar vieses prejudiciais em modelos de AI antes e depois do deploy,
implementar mitigações efetivas e manter registro auditável de conformidade.
Vieses não detectados podem causar dano a grupos vulneráveis, risco legal
e dano reputacional.

## Frequência

- **Pré-deploy:** Obrigatório para qualquer modelo novo
- **Produção:** Trimestral para modelos em operação
- **Ad-hoc:** Quando complaints ou anomalias são detectadas
- **Regulatório:** Conforme exigido por regulamentações aplicáveis

## Tipos de Bias a Avaliar

### 1. Bias de Dados (Data Bias)
- **Representação:** Dataset sub-representa grupos específicos
- **Histórico:** Dados refletem discriminação passada
- **Medição:** Variáveis proxy para atributos protegidos
- **Seleção:** Amostragem não representativa da população

### 2. Bias Algorítmico
- **Amplificação:** Modelo amplifica padrões discriminatórios dos dados
- **Proxy:** Modelo usa features correlacionadas com atributos protegidos
- **Feedback loop:** Outputs do modelo influenciam futuros dados de treino

### 3. Bias de Implementação
- **Design:** Escolhas de produto que prejudicam grupos específicos
- **Interface:** UX que não funciona para certos grupos
- **Acessibilidade:** Modelo não funciona bem para certos idiomas/dialetos

## Processo de Auditoria

### Fase 1: Scoping (Semana 1)
- [ ] Identificar atributos protegidos relevantes (gênero, raça, idade, etc.)
- [ ] Definir métricas de fairness aplicáveis
- [ ] Identificar stakeholders afetados
- [ ] Definir critérios de aceitação
- [ ] Selecionar dados de avaliação representativos

### Fase 2: Avaliação Quantitativa (Semana 2)
Para cada atributo protegido e para cada decisão do modelo:

- [ ] **Demographic Parity:** O modelo toma decisões positivas com a mesma
  taxa para todos os grupos?
- [ ] **Equalized Odds:** O modelo tem as mesmas taxas de verdadeiro positivo
  e falso positivo entre grupos?
- [ ] **Predictive Parity:** A precisão do modelo é a mesma entre grupos?
- [ ] **Individual Fairness:** Indivíduos similares recebem resultados similares?
- [ ] **Counterfactual Fairness:** Mudar apenas o atributo protegido muda o resultado?

### Fase 3: Avaliação Qualitativa (Semana 3)
- [ ] Review de outputs por especialistas em diversidade e inclusão
- [ ] Teste com cenários adversariais (inputs designados para expor bias)
- [ ] Entrevistas com representantes dos grupos afetados
- [ ] Análise de complaints e feedback de usuários

### Fase 4: Relatório e Remediação (Semana 4)
- [ ] Documentar findings com evidências quantitativas
- [ ] Classificar por severidade e impacto
- [ ] Propor mitigações específicas para cada finding
- [ ] Plano de ação com timeline e owners
- [ ] Comunicação para stakeholders

## Métricas de Fairness

### Métricas Fundamentais
| Métrica | Fórmula Simplificada | Quando Usar |
|---------|---------------------|-------------|
| Demographic Parity | P(ŷ=1 \| A=a) = P(ŷ=1 \| A=b) | Decisões de alocação |
| Equal Opportunity | P(ŷ=1 \| Y=1, A=a) = P(ŷ=1 \| Y=1, A=b) | Quando falsos negativos são custosos |
| Equalized Odds | TPR e FPR iguais entre grupos | Quando ambos tipos de erro importam |
| Predictive Parity | PPV igual entre grupos | Quando confiança no resultado importa |
| Calibration | P(Y=1 \| ŷ=s, A=a) = P(Y=1 \| ŷ=s, A=b) | Quando scores são usados |

### Thresholds de Aceitação
- Disparidade entre grupos > 20%: **Crítico** - não deploy sem mitigação
- Disparidade entre grupos 10-20%: **Alto** - mitigação necessária
- Disparidade entre grupos 5-10%: **Médio** - monitorar e planejar mitigação
- Disparidade entre grupos < 5%: **Aceitável** - monitorar continuamente

## Estratégias de Mitigação

### Pré-Processamento (nos dados)
1. **Resampling:** Balancear representação de grupos no dataset
2. **Reweighting:** Dar mais peso a grupos sub-representados
3. **Data augmentation:** Gerar dados sintéticos para grupos minoritários
4. **Feature selection:** Remover features que são proxy para atributos protegidos

### In-Processing (no modelo)
1. **Regularização de fairness:** Adicionar penalidade por disparidade na loss function
2. **Adversarial debiasing:** Treinar adversário que tenta prever grupo do output
3. **Constrained optimization:** Otimizar accuracy sujeito a restrições de fairness

### Pós-Processamento (nos outputs)
1. **Threshold adjustment:** Diferentes thresholds de decisão por grupo
2. **Calibração por grupo:** Ajustar probabilidades para equalizar métricas
3. **Reject option:** Não decidir quando o modelo não tem confiança

### Para LLMs Especificamente
1. **Prompt engineering:** Instruções explícitas contra viés
2. **Constitutional AI:** Regras de segurança e equidade no sistema
3. **Human review:** Revisão humana de outputs sensíveis
4. **Red teaming:** Times dedicados a encontrar vieses

## Template de Relatório de Bias Audit

```
BIAS AUDIT REPORT
Modelo: [Nome/Versão]
Data: [Data]
Auditor: [Nome/Equipe]
Status: [Aprovado / Aprovado com Condições / Reprovado]

ESCOPO
- Atributos protegidos avaliados: [lista]
- Dataset de avaliação: [descrição]
- Métricas utilizadas: [lista]

FINDINGS
| # | Finding | Severidade | Métrica | Grupo Afetado | Ação |
|---|---------|-----------|---------|---------------|------|

RECOMENDAÇÕES
1. [Ação específica com owner e prazo]

PRÓXIMOS PASSOS
- Data da próxima auditoria
- Métricas a monitorar continuamente
```

## Governança

### Responsabilidades
- **AI Ethics Officer/Committee:** Aprovar resultados e exceções
- **Data Scientists:** Executar avaliações técnicas
- **Legal/Compliance:** Validar conformidade regulatória
- **Product:** Avaliar impacto em experiência do usuário
- **D&I Team:** Perspectiva de diversidade e inclusão

### Registro e Documentação
Manter para cada modelo:
- Todos os relatórios de bias audit
- Decisões tomadas e justificativas
- Mitigações implementadas e resultados
- Complaints recebidos e como foram tratados

## Referências

- "Fairness and Machine Learning" - Barocas, Hardt, Narayanan (fairmlbook.org)
- AI Fairness 360 (IBM) - Toolkit open-source
- "Weapons of Math Destruction" - Cathy O'Neil
- EU AI Act - Requisitos de bias para sistemas de alto risco
- NIST AI Risk Management Framework
