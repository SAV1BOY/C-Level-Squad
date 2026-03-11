# AI Responsável — Framework de Ética, Fairness e Transparência

## Propósito e Contexto

AI responsável é o conjunto de práticas que garantem que sistemas de inteligência artificial
sejam justos, transparentes, seguros e alinhados com valores humanos. Não é um nice-to-have
ético — é um requisito de negócio. Modelos enviesados causam danos reais a pessoas, expõem a
empresa a risco legal (especialmente com regulamentações como o AI Act da EU e a futura
regulação brasileira), destroem confiança de clientes e geram crises reputacionais.

Este framework operacionaliza princípios de AI responsável em práticas concretas integradas ao
ciclo de desenvolvimento. O objetivo é que responsabilidade não seja uma etapa extra, mas uma
propriedade do sistema desde o design.

## Quando Usar

- No design de qualquer sistema que usa ML para decisões que afetam pessoas
- Na revisão de modelos existentes para bias e fairness
- Na preparação para regulamentação de AI (compliance)
- Quando há preocupações de stakeholders sobre uso de AI
- No desenvolvimento de AI policies corporativas
- Em treinamento de equipes de AI sobre práticas responsáveis

## Componentes do Framework

### 1. Os 6 Princípios de AI Responsável

**Princípio 1: Fairness (Justiça)**
- Modelos não discriminam com base em características protegidas
- Disparate impact é medido e mitigado
- Métricas de fairness definidas por caso de uso (demographic parity, equal opportunity, etc.)
- Datasets de treinamento auditados para representatividade

**Princípio 2: Transparency (Transparência)**
- Usuários sabem quando estão interagindo com AI
- Decisões de AI podem ser explicadas em linguagem acessível
- Documentação de modelos (model cards) mantida atualizada
- Limitações conhecidas são comunicadas proativamente

**Princípio 3: Accountability (Responsabilização)**
- Cada modelo em produção tem um owner humano responsável
- Decisões de alto impacto têm human-in-the-loop
- Processos de contestação e recurso para decisões de AI
- Audit trail de decisões automatizadas

**Princípio 4: Privacy (Privacidade)**
- Minimização de dados: coletar apenas o necessário
- Anonimização e pseudonimização de dados sensíveis
- Consentimento informado para uso de dados em ML
- Compliance com LGPD e regulações aplicáveis
- Direito ao esquecimento implementado em pipelines de ML

**Princípio 5: Safety (Segurança)**
- Testes adversariais antes de deploy em produção
- Guardrails para outputs de modelos generativos
- Fallback para sistemas não-AI quando modelo falha
- Monitoring contínuo de drift e degradação

**Princípio 6: Beneficence (Benefício)**
- AI deve gerar valor mensurável para usuários, não apenas para a empresa
- Impactos negativos potenciais avaliados antes do desenvolvimento
- Net positive impact como critério de go/no-go

### 2. AI Impact Assessment

Antes de desenvolver qualquer sistema de AI, responda:

| Dimensão | Avaliação |
|----------|-----------|
| Quem é afetado pela decisão do modelo? | [populações impactadas] |
| Qual o dano potencial de uma decisão errada? | [financeiro, reputacional, físico] |
| Existem grupos que podem ser desproporcionalmente afetados? | [lista] |
| O modelo substitui ou auxilia decisão humana? | [substitui / augmenta] |
| Existe recurso/contestação disponível? | [sim/não, como] |
| Quais dados são usados e com que consentimento? | [tipos de dados, base legal] |

**Classificação de Risco:**
- **Baixo Risco:** Recomendação de conteúdo, classificação de tickets
- **Médio Risco:** Pricing, priorização de atendimento, marketing targeting
- **Alto Risco:** Crédito, seguros, contratação, diagnóstico médico
- **Proibido:** Scoring social, manipulação de vulneráveis, vigilância massiva

### 3. Model Card (Documentação Obrigatória)

```markdown
# Model Card: [Nome do Modelo]

## Visão Geral
- Propósito: [para que serve]
- Owner: [pessoa responsável]
- Versão: [X.Y]
- Data de deploy: [YYYY-MM-DD]

## Performance
- Métrica principal: [accuracy, F1, etc.] = [valor]
- Performance por subgrupo: [tabela com breakdown]

## Dados de Treinamento
- Dataset: [nome/fonte]
- Período: [range temporal]
- Volume: [N amostras]
- Representatividade: [análise de distribuição]

## Fairness
- Métricas avaliadas: [demographic parity, equal opportunity, etc.]
- Resultados: [tabela por grupo]
- Mitigações aplicadas: [lista]

## Limitações
- Casos onde o modelo NÃO deve ser usado: [lista]
- Known biases: [lista com plano de mitigação]
- Performance degradada em: [condições]

## Monitoring
- Drift detection: [método e threshold]
- Retraining schedule: [cadência]
- Incident escalation: [processo]
```

## Processo Passo-a-Passo

### Fase 1: Governance Setup (1 vez)
1. Definir AI Ethics Board ou comitê responsável
2. Publicar AI principles da empresa
3. Estabelecer classificação de risco para casos de uso
4. Treinar equipe de AI em práticas responsáveis

### Fase 2: Pre-Development (por projeto)
1. Conduzir AI Impact Assessment
2. Classificar nível de risco do caso de uso
3. Definir métricas de fairness relevantes
4. Aprovar desenvolvimento (go/no-go baseado em risco)

### Fase 3: Development
1. Auditar dataset para representatividade e bias
2. Implementar fairness constraints no treinamento
3. Gerar model card com documentação completa
4. Realizar testes adversariais
5. Review por AI Ethics Board (para alto risco)

### Fase 4: Production & Monitoring
1. Deploy com guardrails e fallbacks
2. Monitoring de drift e fairness metrics contínuo
3. Processo de contestação acessível a afetados
4. Audit trimestral de modelos em produção
5. Retraining com avaliação de fairness

## Checklist de AI Responsável

- [ ] AI Impact Assessment realizado e documentado?
- [ ] Nível de risco classificado e aprovado?
- [ ] Dataset auditado para representatividade?
- [ ] Fairness metrics definidas e calculadas?
- [ ] Model card completo e atualizado?
- [ ] Human-in-the-loop para decisões de alto risco?
- [ ] Processo de contestação disponível?
- [ ] Monitoring de drift e fairness ativo?
- [ ] Compliance com LGPD verificado?
- [ ] AI Ethics Board consultado (se alto risco)?

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| AI Impact Assessment completion | 100% dos novos modelos | Por projeto |
| Model card coverage | 100% dos modelos em produção | Trimestral |
| Fairness metrics compliance | 100% dentro dos thresholds | Mensal |
| AI-related complaints/incidents | Tendência zero | Mensal |
| Ethics training completion | 100% do time de AI | Anual |
| Regulatory readiness score | > 80% | Semestral |

## Referências Cruzadas

- `frameworks/caio-architect/ai-governance.md` — Governance structure detalhado
- `frameworks/caio-architect/ai-maturity-model.md` — Governança como dimensão de maturidade
- `frameworks/caio-architect/mlops-framework.md` — Monitoring e retraining
- `frameworks/caio-architect/ai-product-development.md` — Responsible AI no ciclo de produto
- `frameworks/cio-engineer/security-posture.md` — Segurança de sistemas de AI
- `frameworks/cio-engineer/data-platform.md` — Governança de dados que alimenta AI
- `frameworks/shared/risk-management.md` — AI risk no framework corporativo
