# Checklist de Qualidade — AI Initiative (Iniciativa de Inteligência Artificial)

## Propósito
Garantir que iniciativas de AI/ML sejam avaliadas com rigor: use case claro e vinculado ao negócio, dados avaliados quanto à disponibilidade e qualidade, plano de evaluation definido, guardrails de segurança e ética implementados, ROI projetado com premissas realistas e governança revisada. Este checklist protege contra o "AI hype" e assegura que investimentos em AI gerem valor real.

## Quando Aplicar
- Antes de aprovar qualquer nova iniciativa de AI/ML
- Na avaliação de buy vs build para soluções de AI
- Quando modelos existentes são repropostos para novos use cases
- Na revisão trimestral do portfólio de iniciativas de AI
- Antes de colocar qualquer modelo em produção
- Quando agentes de AI propõem novas aplicações ou automações

## Agente Responsável
- **Primário:** CAIO Agent (Chief AI Officer) ou CTO Agent
- **Co-responsável:** CPO Agent (para use cases de produto)
- **Revisor:** CEO Agent (para alinhamento estratégico), CFO Agent (para ROI)
- **Consultor:** Data Ethics Agent ou Responsible AI Agent (se existente)

## Checklist

### Seção 1 — Use Case Claro
- [ ] O problema de negócio que a AI resolve está articulado em linguagem não-técnica
- [ ] O use case está vinculado a uma métrica de negócio específica (revenue, cost, NPS, etc.)
- [ ] O benefício incremental da AI sobre a solução atual (manual, rule-based) está estimado
- [ ] O usuário final (end user) está identificado e suas necessidades documentadas
- [ ] O workflow onde a AI será integrada está mapeado (não é AI isolada)
- [ ] Alternativas mais simples (heurísticas, regras, RPA) foram avaliadas antes de recorrer a ML
- [ ] O use case tem sponsor executivo que garante adoção e change management
- [ ] O volume e frequência de uso esperados justificam o investimento
- [ ] O use case está priorizado contra outros use cases candidatos
- [ ] O impacto em processos e pessoas afetados pela automação está avaliado

### Seção 2 — Dados Avaliados
- [ ] Os dados necessários para o modelo estão identificados e documentados (data catalog)
- [ ] A disponibilidade dos dados está verificada (existem, são acessíveis, estão atualizados)
- [ ] A qualidade dos dados está avaliada (completude, consistência, acurácia, timeliness)
- [ ] O volume de dados é suficiente para o approach de ML escolhido
- [ ] Os data pipelines necessários estão implementados ou têm timeline para implementação
- [ ] Os dados sensíveis (PII, financeiros) estão identificados e protegidos conforme regulação
- [ ] O data labeling (se necessário) tem plano e budget definidos
- [ ] As limitações e vieses dos dados estão documentados
- [ ] O plano de data refresh e manutenção contínua está definido
- [ ] A governança de dados (ownership, acesso, retenção) está resolvida
- [ ] Os data dependencies com outros times estão mapeados

### Seção 3 — Evaluation Plan
- [ ] As métricas de avaliação do modelo estão definidas (accuracy, precision, recall, F1, AUC, etc.)
- [ ] O threshold mínimo de performance para ir a produção está estabelecido
- [ ] O baseline de comparação está definido (performance sem AI ou com modelo simples)
- [ ] O plano de A/B testing ou experiment design está documentado
- [ ] O dataset de teste (holdout) está separado e protegido contra data leakage
- [ ] O plano de avaliação offline (backtesting) E online (production) está definido
- [ ] As métricas de negócio (não apenas técnicas) que validam o sucesso estão identificadas
- [ ] O critério de "bom o suficiente para produção" está definido e acordado
- [ ] O plano de monitoramento contínuo pós-deploy (model monitoring) está definido
- [ ] A frequência de retraining está planejada com triggers de retraining definidos
- [ ] O plano de human-in-the-loop evaluation está considerado

### Seção 4 — Guardrails Definidos
- [ ] Os guardrails de segurança estão implementados (input validation, output filtering)
- [ ] Os failure modes do modelo estão identificados e documentados
- [ ] O comportamento do sistema quando o modelo falha está definido (graceful degradation)
- [ ] O fallback para decisão humana está implementado para casos de baixa confiança
- [ ] Os vieses do modelo estão avaliados e mitigados (fairness assessment)
- [ ] O impacto de outputs incorretos está analisado e o risco é aceitável
- [ ] Os limites de autonomia do modelo estão definidos (o que pode decidir vs o que escala)
- [ ] A transparência do modelo (explainability) atende aos requisitos do use case
- [ ] Os riscos de adversarial attacks estão avaliados quando aplicável
- [ ] A política de uso responsável de AI da organização está sendo seguida
- [ ] O plano de desligamento do modelo (kill switch) está definido e testado
- [ ] Os guardrails de custo operacional (compute costs) estão implementados

### Seção 5 — ROI Projetado
- [ ] O custo total da iniciativa está estimado: desenvolvimento, infraestrutura, dados, pessoas
- [ ] O custo operacional contínuo (inference, storage, monitoring, retraining) está projetado
- [ ] O benefício financeiro está quantificado: aumento de receita, redução de custo, eficiência
- [ ] O payback period está estimado com premissas explícitas
- [ ] O comparativo custo-benefício com alternativas não-AI está documentado
- [ ] Os cenários otimista, base e pessimista de ROI estão modelados
- [ ] O custo de oportunidade (o que mais poderíamos fazer com o mesmo investimento) está avaliado
- [ ] Os custos ocultos (manutenção, edge cases, suporte) estão incluídos
- [ ] O ROI está ajustado ao risco (probabilidade de sucesso técnico x adoção)
- [ ] O investimento está alinhado com o budget aprovado para AI/inovação

### Seção 6 — Governança Revisada
- [ ] A iniciativa está registrada no inventário de modelos de AI da organização
- [ ] O compliance com regulações de AI aplicáveis (AI Act, LGPD, etc.) está verificado
- [ ] A revisão ética da aplicação foi realizada
- [ ] O processo de aprovação para uso em produção está definido e seguido
- [ ] Os logs de decisão do modelo são mantidos para auditoria
- [ ] O responsável pelo modelo em produção (model owner) está designado
- [ ] O plano de incident response para falhas do modelo está definido
- [ ] A comunicação para usuários finais sobre o uso de AI está planejada (transparência)
- [ ] O impacto em propriedade intelectual e termos de serviço está avaliado

## Critérios de Aprovação
- Use case vinculado a métrica de negócio com benefício incremental estimado
- Dados disponíveis, com qualidade suficiente e governança resolvida
- Evaluation plan completo com baseline, métricas e thresholds definidos
- Guardrails implementados com failure modes documentados e kill switch testado
- ROI positivo no cenário base com downside protegido
- Governança e compliance revisados e aprovados
- Score mínimo de completude: 90% dos itens marcados

## O que Fazer se Falhar
1. Se o use case não está claro, retornar à etapa de discovery e validação com stakeholders
2. Se dados não estão disponíveis ou com qualidade, investir em data engineering antes de ML
3. Se guardrails estão ausentes, não aprovar deploy em produção
4. Se ROI não está justificado, reconsiderar o use case ou a abordagem
5. Se a governança não está resolvida, escalar para o comitê de ética/compliance
6. Registrar learnings de iniciativas de AI no RalphLoop para calibrar futuras propostas
7. Considerar POC/MVP antes de investimento total se a incerteza for alta

## Referências
- Google — "Rules of Machine Learning" (best practices de ML engineering)
- Agrawal, A., Gans, J. & Goldfarb, A. — "Prediction Machines" (economia de AI)
- NIST AI Risk Management Framework
- EU AI Act — classificação de riscos e requisitos
- Template interno: `/templates/ai-initiative-template.md`
- Model registry: `/registry/ai-model-registry.md`
- AI governance policy: `/governance/ai-governance-policy.md`
