# Checklist de Avaliação de Bias em Modelos AI

> Checklist para identificar, medir e mitigar vieses em sistemas de inteligência
> artificial, garantindo equidade e responsabilidade nas decisões automatizadas.

---

## 1. Avaliação dos Dados de Treino

- [ ] Composição demográfica do dataset documentada
- [ ] Representatividade de grupos minoritários verificada
- [ ] Distribuição de classes balanceada ou estratégia de balanceamento definida
- [ ] Fontes de dados avaliadas quanto a vieses históricos conhecidos
- [ ] Labels/anotações revisadas por múltiplos anotadores
- [ ] Inter-annotator agreement medido e documentado
- [ ] Proxy variables para atributos protegidos identificadas
- [ ] Dados sintéticos avaliados quanto à propagação de vieses
- [ ] Período temporal dos dados analisado (viés de época)
- [ ] Viés de seleção na coleta de dados documentado

## 2. Definição de Fairness

- [ ] Atributos protegidos definidos (gênero, raça, idade, região, etc.)
- [ ] Métricas de fairness selecionadas e justificadas
  - [ ] Demographic Parity (paridade demográfica)
  - [ ] Equalized Odds (chances equalizadas)
  - [ ] Equal Opportunity (oportunidade igual)
  - [ ] Predictive Parity (paridade preditiva)
  - [ ] Individual Fairness (fairness individual)
- [ ] Trade-offs entre métricas de fairness documentados
- [ ] Threshold de aceitabilidade definido para cada métrica
- [ ] Stakeholders alinhados sobre a definição de fairness adotada
- [ ] Contexto regulatório mapeado (LGPD, regulações setoriais)
- [ ] Impacto potencial de decisões enviesadas documentado

## 3. Análise Pré-Treino

- [ ] Análise exploratória segmentada por grupos protegidos
- [ ] Correlações entre features e atributos protegidos medidas
- [ ] Disparate Impact Ratio calculado nos dados brutos
- [ ] Distribuição de features comparada entre grupos
- [ ] Missing data patterns analisados por grupo
- [ ] Feature importance preliminar avaliada para proxy detection
- [ ] Amostragem estratificada garantida no split treino/teste
- [ ] Documentação de decisões de inclusão/exclusão de features

## 4. Análise Durante o Treino

- [ ] Regularização de fairness considerada no treinamento
- [ ] Métricas de fairness monitoradas durante o treino
- [ ] Adversarial debiasing avaliado como técnica
- [ ] Re-weighting de amostras implementado se necessário
- [ ] Calibração do modelo verificada por subgrupo
- [ ] Underfitting em subgrupos específicos verificado
- [ ] Ensemble methods avaliados para redução de viés
- [ ] Hyperparameter tuning considerando métricas de fairness

## 5. Análise Pós-Treino

- [ ] Performance do modelo avaliada por subgrupo
  - [ ] Accuracy por grupo
  - [ ] Precision por grupo
  - [ ] Recall por grupo
  - [ ] F1-Score por grupo
  - [ ] AUC-ROC por grupo
- [ ] Confusion matrix gerada por subgrupo
- [ ] Disparate Impact Ratio calculado nas predições
- [ ] False Positive Rate comparada entre grupos
- [ ] False Negative Rate comparada entre grupos
- [ ] Análise de erro qualitativa em casos de fronteira
- [ ] SHAP/LIME analysis para explicabilidade por grupo
- [ ] Interseccionalidade analisada (combinações de atributos)

## 6. Mitigação de Viés

- [ ] Técnicas de pré-processamento aplicadas se necessário
  - [ ] Resampling
  - [ ] Reweighting
  - [ ] Feature transformation
- [ ] Técnicas de in-processing aplicadas se necessário
  - [ ] Constrained optimization
  - [ ] Adversarial learning
  - [ ] Fair representation learning
- [ ] Técnicas de pós-processamento aplicadas se necessário
  - [ ] Threshold adjustment por grupo
  - [ ] Reject option classification
  - [ ] Calibrated equalized odds
- [ ] Impacto da mitigação na performance geral documentado
- [ ] Trade-off fairness vs. accuracy aceito pelos stakeholders

## 7. Testes e Validação

- [ ] Teste com dados sintéticos de estresse para cada grupo
- [ ] Teste de robustez com perturbações nos atributos protegidos
- [ ] Validação com especialistas de domínio
- [ ] Teste com dados de produção recentes (shadow mode)
- [ ] Análise de casos edge com revisão humana
- [ ] Benchmark contra baseline não-enviesado
- [ ] Red teaming para identificar cenários de viés oculto
- [ ] Teste de estabilidade temporal do viés

## 8. Monitoramento Contínuo

- [ ] Métricas de fairness monitoradas em produção
- [ ] Alertas para degradação de fairness configurados
- [ ] Dashboard de fairness acessível aos stakeholders
- [ ] Drift de distribuição por grupo monitorado
- [ ] Feedback loop implementado para reportar viés percebido
- [ ] Frequência de re-avaliação definida (mínimo: trimestral)
- [ ] Processo de escalation para viés detectado documentado
- [ ] Canal de denúncia para usuários afetados disponível

## 9. Documentação e Governança

- [ ] Bias Assessment Report publicado
- [ ] Model Card atualizada com seção de fairness
- [ ] Decisões de trade-off documentadas com justificativas
- [ ] Aprovação do comitê de ética obtida (se aplicável)
- [ ] Registro no inventário de AI responsável
- [ ] Plano de ação para vieses identificados mas não mitigados
- [ ] Treinamento do time sobre viés em AI realizado
- [ ] Revisão legal das implicações de viés concluída

---

## Métricas de Referência

| Métrica | Threshold Aceitável |
|---------|-------------------|
| Disparate Impact Ratio | 0.8 - 1.25 (regra dos 4/5) |
| Equal Opportunity Difference | < 0.1 |
| Demographic Parity Difference | < 0.1 |
| Equalized Odds Difference | < 0.1 |
| Predictive Parity Difference | < 0.05 |

---

## Ferramentas Recomendadas

- **AI Fairness 360 (IBM)**: Suite completa de métricas e mitigação
- **Fairlearn (Microsoft)**: Integrado com scikit-learn
- **What-If Tool (Google)**: Visualização interativa de fairness
- **Aequitas**: Auditoria de viés para decision-making systems
- **SHAP/LIME**: Explicabilidade para detectar proxy variables

---

*Última atualização: Março 2026*
*Responsável: CAIO Architect / Comitê de AI Responsável*
