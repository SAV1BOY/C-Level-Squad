# AI Readiness Rubric — Rubrica de Prontidão para Inteligência Artificial

> Referência do C-Level Squad para avaliar a prontidão organizacional para adoção de AI.
> Agente primário: CAIO (Chief AI Officer), com input de CTO (infra), CIO (dados), COO (processos).

---

## 1. Visão geral

A prontidão para AI não é apenas tecnológica. Organizações que investem apenas em tecnologia sem preparar dados, pessoas, processos e cultura alcançam menos de 20% do potencial de AI (McKinsey AI Survey, 2024).

### As 5 dimensões de AI Readiness

```
AI Readiness Score = f(Data, Talent, Infrastructure, Process, Culture)

Cada dimensão: Score 1-5
Score máximo: 25 pontos
```

### Faixas de prontidão

| Score  | Nível          | Descrição                                                  |
|--------|---------------|-----------------------------------------------------------|
| 21-25  | AI-Native     | Organização opera com AI como core capability. Diferencial competitivo |
| 16-20  | AI-Ready      | Fundações sólidas. Pronta para escalar use cases complexos  |
| 11-15  | AI-Emerging   | Progresso em algumas dimensões. Gaps significativos em outras |
| 6-10   | AI-Aware      | Consciência sobre AI mas pouca maturidade operacional       |
| 1-5    | AI-Nascent    | Estágio inicial. Precisa de investimento fundamental        |

---

## 2. Dimensão 1: Data Readiness (Prontidão de Dados)

### Score 1 — Caótico

- **Qualidade:** Dados inconsistentes, duplicados, sem validação. Ninguém confia nos dados
- **Volume:** Dados insuficientes para treinar ou fine-tunar modelos. Histórico limitado
- **Acesso:** Dados em silos isolados. Cada departamento tem sua própria "verdade". Sem APIs de acesso
- **Governança:** Sem data owner definido. Sem políticas de qualidade, retenção ou acesso
- **Catalogação:** Ninguém sabe que dados existem ou onde estão

### Score 2 — Reativo

- **Qualidade:** Problemas conhecidos mas tratados ad hoc. Limpeza manual quando necessário
- **Volume:** Dados suficientes para analytics básico. Histórico de 6-12 meses
- **Acesso:** Alguns dados centralizados (data warehouse básico). Acesso sob demanda
- **Governança:** Data owners informais. Políticas básicas de privacidade (reativo à LGPD)
- **Catalogação:** Inventário parcial. Equipe de dados conhece os principais datasets

### Score 3 — Estruturado

- **Qualidade:** Pipeline de qualidade com validação automática. Score de qualidade medido. >70% dos datasets críticos com qualidade aceitável
- **Volume:** Dados suficientes para ML. Histórico de 1-3 anos. Feature store básico
- **Acesso:** Data warehouse/lake moderno. APIs para datasets principais. Self-service para analistas
- **Governança:** Data owners formais. Políticas documentadas. Compliance LGPD proativo
- **Catalogação:** Data catalog implementado. Metadata básica. Lineage parcial

### Score 4 — Otimizado

- **Qualidade:** >90% dos datasets críticos com alta qualidade. Monitoramento contínuo. Alertas de degradação. Data contracts entre times
- **Volume:** Datasets ricos para ML. Feature store robusto. Data augmentation quando necessário
- **Acesso:** Plataforma de dados moderna (Lakehouse). Real-time e batch. APIs documentadas. RBAC implementado
- **Governança:** Data governance framework maduro. DPO ativo. Auditorias regulares. Data lineage completo
- **Catalogação:** Catalog completo com busca, ownership, SLA, qualidade, e uso documentados

### Score 5 — Excelente

- **Qualidade:** Data quality como produto. Métricas de qualidade em SLAs. Zero tolerance para dados críticos abaixo do threshold. Feedback loop automático
- **Volume:** Datasets continuamente enriquecidos. Data flywheel ativo (mais uso → mais dados → melhor modelo → mais uso)
- **Acesso:** Plataforma self-service para data scientists. Sandbox environments. Acesso federado cross-team
- **Governança:** Governança como enabler (não como blocker). AI-specific governance (model cards, bias audit). Compliance by design
- **Catalogação:** Catalog com autodiscovery. ML feature catalog integrado. Uso e impacto rastreados automaticamente

### Checklist de avaliação de Data Readiness

```
□ Existe um data warehouse/lake centralizado?
□ Os dados mais críticos para AI estão acessíveis via API?
□ Existe pipeline de qualidade de dados automatizado?
□ O score de qualidade dos top 10 datasets é medido?
□ Existe data catalog com ownership definido?
□ O histórico de dados é suficiente (>12 meses para time series)?
□ Existe feature store ou repositório de features para ML?
□ A governança de dados inclui considerações de AI (bias, fairness)?
□ O acesso a dados para data scientists é self-service?
□ Existe data lineage end-to-end?
```

---

## 3. Dimensão 2: Talent Readiness (Prontidão de Talentos)

### Score 1 — Inexistente

- **Skills:** Nenhum profissional com expertise em ML/AI na organização
- **Hiring:** Sem pipeline de recrutamento para roles de AI. Job descriptions inexistentes
- **Upskilling:** Nenhum programa de treinamento em AI para colaboradores existentes
- **Estrutura:** Sem time dedicado a AI. Iniciativas dependem de consultoria externa
- **Literacy:** Liderança não entende conceitos básicos de AI (supervisionado vs. não-supervisionado, overfitting, etc.)

### Score 2 — Inicial

- **Skills:** 1-3 data scientists/ML engineers, geralmente isolados em um time de analytics
- **Hiring:** Recrutamento reativo. Dificuldade em atrair talento por falta de maturidade
- **Upskilling:** Treinamentos genéricos (cursos online) sem aplicação prática direcionada
- **Estrutura:** AI é responsabilidade informal de alguém que "se interessa pelo tema"
- **Literacy:** Alguns líderes entendem AI superficialmente. Maioria confunde AI com automação

### Score 3 — Funcional

- **Skills:** Time de AI com 5-10 pessoas (data scientists, ML engineers, data engineers). Competências core cobertas
- **Hiring:** Pipeline de recrutamento ativo. Consegue contratar mid-level com consistência
- **Upskilling:** Programa estruturado de AI literacy para toda a organização. Treinamento prático para power users
- **Estrutura:** Time ou squad de AI formal com liderança definida. Roadmap próprio
- **Literacy:** C-Level entende o potencial e limitações de AI. Capaz de avaliar business cases

### Score 4 — Avançado

- **Skills:** Time de AI com 10-20+ pessoas incluindo especialistas (NLP, computer vision, MLOps). Capacidade de pesquisa aplicada
- **Hiring:** Employer brand forte para AI talent. Consegue atrair seniors e specialists
- **Upskilling:** AI champions em cada área de negócio. Citizen data scientist program ativo
- **Estrutura:** Centro de Excelência em AI (CoE) ou equivalente. Modelo hub-and-spoke (CoE + embedded)
- **Literacy:** Liderança participa ativamente de decisões de AI. Product managers escrevem PRDs com AI components

### Score 5 — World-class

- **Skills:** Time de AI completo com pesquisadores, applied scientists, ML platform engineers, AI ethicists. Publicações e contribuições open-source
- **Hiring:** Referência no mercado. Top talent busca a empresa proativamente. Retention alta
- **Upskilling:** AI é skill transversal esperada de todos. Hackathons de AI regulares. Mentoria interna entre experts
- **Estrutura:** AI distribuído em toda a organização com governance centralizado. Cada time tem AI capability
- **Literacy:** Toda a organização entende como AI funciona e quando usá-la. Data-driven decision making é a norma

### Checklist de avaliação de Talent Readiness

```
□ Existe ao menos 1 ML engineer/data scientist sênior?
□ O time de AI tem capacidade de levar modelo do protótipo à produção?
□ Existe pipeline de recrutamento ativo para roles de AI?
□ Há programa de upskilling em AI para o time existente?
□ A liderança (C-Level) tem AI literacy suficiente para tomar decisões?
□ Existe orçamento dedicado para treinamento em AI?
□ Os product managers/business owners sabem escrever use cases de AI?
□ Há plano de retenção para talentos-chave de AI?
□ Existe mentoria ou comunidade de prática interna de AI?
□ O time consegue operar modelos em produção com SLA?
```

---

## 4. Dimensão 3: Infrastructure Readiness (Prontidão de Infraestrutura)

### Score 1-5 Progression

| Score | Compute               | Tools/MLOps                      | Deployment                      |
|-------|----------------------|----------------------------------|---------------------------------|
| 1     | Sem GPU. Laptops pessoais | Jupyter notebooks locais. Sem versionamento | Modelos nunca chegam a produção |
| 2     | GPU compartilhada ou cloud esporádico | Experimentos no notebook. Git básico. Sem registry | Deploy manual, "works on my machine" |
| 3     | Cloud compute dedicado (AWS/GCP/Azure). Budget definido | MLflow ou similar. Feature store básico. CI/CD para modelos | Deploy semi-automatizado. Staging environment |
| 4     | GPU clusters. Auto-scaling. Spot instances otimizados | ML platform madura: experiment tracking, model registry, feature store, monitoring | Deploy automatizado com canary/shadow. A/B testing de modelos |
| 5     | Multi-cloud/hybrid otimizado. Edge computing quando necessário | ML platform completa: AutoML, model catalog, drift detection, retraining automation | Deploy one-click. Multi-model serving. Realtime + batch. Governance integrada |

### Checklist de avaliação de Infrastructure Readiness

```
□ Existe compute dedicado (GPU) para treinamento de modelos?
□ O custo de infraestrutura de AI é monitorado e otimizado?
□ Existe environment de desenvolvimento separado de produção?
□ Há experiment tracking (MLflow, W&B, etc.)?
□ Existe model registry com versionamento?
□ O deploy de modelos é automatizado (CI/CD para ML)?
□ Existe monitoring de modelos em produção (drift, performance)?
□ O time pode escalar compute sob demanda?
□ Existe feature store compartilhado?
□ Há capacidade de A/B test de modelos em produção?
```

---

## 5. Dimensão 4: Process Readiness (Prontidão de Processos)

### Score 1-5 Progression

| Score | Workflows                           | Governance                            | Integration                       |
|-------|-------------------------------------|---------------------------------------|-----------------------------------|
| 1     | Nenhum processo para AI. Ad hoc total | Sem governance de AI. Sem review de modelos | AI desconectada dos processos de negócio |
| 2     | Processo informal: "peça ao data scientist" | Awareness de riscos mas sem processo formal | Integração pontual, manual |
| 3     | Processo definido: intake → priorização → desenvolvimento → deploy. SLA básico | Model review checklist. Bias check básico antes de deploy | API de modelos consumida por 2-3 sistemas |
| 4     | Processo maduro com gates: business case → POC → MVP → Scale. Kill criteria em cada gate | AI governance board. Model cards obrigatórios. Audit trail. Impact assessment para modelos de alto risco | AI integrada nos processos-chave. Feedback loop dos usuários para melhoria do modelo |
| 5     | Processo ágil e escalável: from idea to production em <4 semanas para use cases padrão | Responsible AI framework completo: fairness, transparency, accountability, privacy. External audit quando necessário | AI é componente natural de todos os processos. Self-service AI para power users. Continuous learning |

### Framework de governance mínimo para AI

```markdown
## AI Governance Checklist — Antes do deploy

### Mandatório para todos os modelos
- [ ] Model card preenchido (propósito, dados, limitações, métricas)
- [ ] Data privacy review (LGPD compliance)
- [ ] Bias check básico (performance across demographic groups)
- [ ] Rollback plan definido
- [ ] Monitoring configurado (performance metrics, drift detection)
- [ ] Owner do modelo definido

### Adicional para modelos de alto risco
- [ ] Impact assessment completo
- [ ] Explicabilidade testada (SHAP/LIME ou equivalente)
- [ ] Fairness audit por grupo protegido
- [ ] Human-in-the-loop para decisões críticas
- [ ] Stress test com edge cases
- [ ] Legal review (discriminação, responsabilidade)
- [ ] Communication plan para usuários afetados
```

---

## 6. Dimensão 5: Culture Readiness (Prontidão Cultural)

### Score 1-5 Progression

| Score | Adoção                              | Change Management                     | Mindset                           |
|-------|-------------------------------------|---------------------------------------|-----------------------------------|
| 1     | Resistência ativa a AI. "Vai tomar nossos empregos". Medo predomina | Nenhum esforço de change management | "Sempre fizemos assim". Data-driven não é valorizado |
| 2     | Curiosidade passiva. Interesse individual mas sem momentum organizacional | Comunicação sobre AI esporádica. Sem sponsorship claro | Dados usados para justificar decisões já tomadas (confirmation bias) |
| 3     | Adoção em pockets. 2-3 times usando AI ativamente. Restante observando | Change management básico: comunicação regular, early adopter program | Data-informed decision making em alguns times. Experimentação tolerada |
| 4     | Adoção ampla. Maioria dos times usa AI em alguma capacidade. Champions em cada área | Change management estruturado: comunicação, treinamento, suporte, celebração de wins. Resistência tratada proativamente | Data-driven é a norma. Experimentação encorajada. Falha tolerada se aprendida |
| 5     | AI-first mindset. Times proativamente buscam oportunidades de AI. AI é expectativa, não exceção | Cultura de aprendizado contínuo. AI embedded na identidade da organização. Pessoas orgulhosas de serem AI-forward | Growth mindset universal. Dados são commodity. Insight é diferencial. Humildade sobre limitações de AI |

### Checklist de avaliação de Culture Readiness

```
□ A liderança comunica ativamente a importância de AI?
□ Existe programa de change management para adoção de AI?
□ Os colaboradores entendem como AI pode ajudá-los (não substituí-los)?
□ Existem early adopters/champions de AI em cada área?
□ A organização celebra wins de AI publicamente?
□ Existe tolerância a falha em experimentos de AI?
□ Os colaboradores confiam nos outputs de AI? (nem demais, nem de menos)
□ Há canais para feedback sobre ferramentas de AI?
□ A cultura valoriza decisões baseadas em dados?
□ Existe narrativa positiva sobre AI no futuro da organização?
```

---

## 7. Scoring agregado e roadmap

### Template de avaliação

```markdown
## AI Readiness Assessment — [Organização/Squad]

**Data:** [YYYY-MM-DD]
**Assessor:** CAIO + [outros agentes]

### Scores

| # | Dimensão       | Score (1-5) | Evidência principal               |
|---|---------------|-------------|-----------------------------------|
| 1 | Data          |             |                                   |
| 2 | Talent        |             |                                   |
| 3 | Infrastructure|             |                                   |
| 4 | Process       |             |                                   |
| 5 | Culture       |             |                                   |
|   | **TOTAL**     | **/25**     |                                   |

### Classificação: [AI-Nascent / AI-Aware / AI-Emerging / AI-Ready / AI-Native]

### Radar chart (visual)

         Data
          5
         /|\
        / | \
       /  |  \
Culture---+---Talent
       \  |  /
        \ | /
         \|/
          5
    Infra     Process

### Dimensão mais forte: [X] — Score: [Y]
### Dimensão mais fraca: [X] — Score: [Y]
### Gap mais crítico: [descrição]
```

### Roadmap de melhoria por nível

| De          | Para         | Prioridade de investimento (em ordem)         | Timeline típica |
|-------------|-------------|-----------------------------------------------|-----------------|
| AI-Nascent  | AI-Aware    | 1. Culture (awareness), 2. Data (foundations), 3. Talent (hire 1st DS) | 6-12 meses |
| AI-Aware    | AI-Emerging | 1. Data (quality + access), 2. Talent (build team), 3. Infra (cloud ML) | 6-12 meses |
| AI-Emerging | AI-Ready    | 1. Process (governance), 2. Infra (MLOps), 3. Talent (specialists) | 9-18 meses |
| AI-Ready    | AI-Native   | 1. Culture (AI-first), 2. Process (scale), 3. All (optimize) | 12-24 meses |

### Quick wins por dimensão

| Dimensão       | Quick win (implementável em <30 dias)                           |
|---------------|----------------------------------------------------------------|
| Data          | Auditar qualidade dos top 5 datasets. Definir data owners       |
| Talent        | AI literacy workshop para C-Level (4h). Contratar 1 DS sênior   |
| Infrastructure| Configurar cloud ML environment (SageMaker/Vertex). MLflow setup |
| Process       | Criar template de AI use case (ver ai-use-case-blocks.md)       |
| Culture       | CEO comunicar visão de AI. Criar canal de compartilhamento de wins |

---

## 8. Riscos específicos de AI a monitorar

| Risco                    | Indicador                                      | Mitigação                          |
|--------------------------|------------------------------------------------|-----------------------------------|
| Model bias/fairness      | Performance desigual entre grupos demográficos  | Bias audit antes do deploy         |
| Data drift               | Distribuição dos dados de input mudou           | Monitoring + alertas automáticos   |
| Model degradation        | Métricas de performance caindo ao longo do tempo| Retraining automatizado            |
| Over-reliance            | Humanos param de questionar output do modelo    | Human-in-the-loop para decisões críticas |
| Privacy violation        | Dados pessoais usados sem consentimento          | Privacy by design, LGPD compliance |
| Hallucination (LLMs)     | Modelo gera informação falsa com confiança      | Grounding, RAG, fact-checking      |
| Vendor lock-in           | Dependência de um único provider de AI          | Multi-model strategy, abstractions |
| Shadow AI                | Times usando AI não aprovada/governada          | Policy clara + alternativa aprovada |
| Talent flight            | Key AI people saindo                            | Compensation review, growth paths  |
| Cost overrun             | Custo de compute/API escalando sem controle     | Budget caps, cost monitoring       |

---

## 9. Integração com outros frameworks

- **Use cases:** Usar `ai-use-case-blocks.md` para documentar cada caso de uso
- **Riscos:** Usar `risk-scoring.md` para avaliar riscos de AI com P×I
- **Iniciativas:** Usar `initiative-health-rubric.md` para monitorar projetos de AI
- **Decisões:** Usar `decision-quality-rubric.md` para avaliar decisões de investimento em AI
- **Cross-squad:** Usar `cross-squad-effectiveness-rubric.md` para avaliar colaboração entre CAIO e outros agentes
