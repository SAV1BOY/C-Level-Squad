# Template: Charter de Projeto de IA

## Propósito
Este template define escopo, objetivos, governança e critérios de sucesso para projetos de inteligência artificial. O charter é o documento de autorização do projeto, alinhando stakeholders sobre o que será feito, como, por quem e por quê.

## Instruções de Uso
1. Elabore antes de iniciar qualquer desenvolvimento
2. Sponsor executivo deve aprovar o charter
3. Use como referência para decisões de escopo durante o projeto
4. Revise se houver mudança significativa em premissas ou contexto

---

## Informações do Projeto

| Campo | Valor |
|-------|-------|
| **Nome do Projeto** | [Nome descritivo] |
| **ID** | [AI-AAAA-NNN] |
| **Sponsor** | [Nome — Cargo (VP/C-Level)] |
| **Project Lead** | [Nome — Cargo] |
| **ML Lead** | [Nome — Cargo] |
| **Data de Início** | [DD/MM/AAAA] |
| **Data Estimada de Conclusão** | [DD/MM/AAAA] |
| **Status** | [Planejamento / Em Execução / Piloto / Produção / Encerrado] |

---

## 1. Visão e Objetivos

### 1.1 Declaração de Visão
[1-2 frases descrevendo o resultado final desejado — em linguagem de negócio, não técnica]

### 1.2 Objetivos do Projeto

| Objetivo | Métrica de Sucesso | Meta | Prazo |
|----------|-------------------|------|-------|
| [Objetivo 1 — negócio] | [Métrica mensurável] | [Valor alvo] | [Data] |
| [Objetivo 2 — técnico] | [Métrica mensurável] | [Valor alvo] | [Data] |
| [Objetivo 3 — operacional] | [Métrica mensurável] | [Valor alvo] | [Data] |

### 1.3 Não-Objetivos (Explicitamente fora de escopo)
- [O que este projeto NÃO vai fazer]
- [Funcionalidade que será considerada em fase futura]
- [Caso de uso que não será endereçado]

---

## 2. Justificativa de Negócio

### 2.1 Problema que Estamos Resolvendo
[Descrição detalhada do problema de negócio]

### 2.2 Por que IA é a Abordagem Certa
[Justificar por que métodos tradicionais (regras, heurísticas) não são suficientes]

### 2.3 Impacto Esperado

| Dimensão | Antes (baseline) | Depois (meta) | Valor Gerado |
|----------|-----------------|---------------|-------------|
| [Métrica de negócio 1] | [Valor atual] | [Valor esperado] | [R$ / %] |
| [Métrica de negócio 2] | [Valor atual] | [Valor esperado] | [R$ / %] |
| [Métrica de negócio 3] | [Valor atual] | [Valor esperado] | [R$ / %] |

### 2.4 ROI Esperado
- **Investimento total:** [R$ X]
- **Benefício projetado (anual):** [R$ X]
- **ROI:** [X%]
- **Payback:** [X meses]

---

## 3. Escopo e Abordagem

### 3.1 Escopo Detalhado

**Dados:**
- [Quais dados serão utilizados]
- [Quais dados precisam ser coletados/criados]
- [Volume estimado]

**Modelo:**
- [Tipo de modelo / abordagem técnica]
- [Frameworks e ferramentas]
- [Build vs Buy — justificativa]

**Integração:**
- [Onde o modelo se integra no fluxo existente]
- [Sistemas que precisam ser modificados]
- [APIs novas necessárias]

**UX / Interface:**
- [Como o usuário interage com os resultados do modelo]
- [Nível de explicabilidade necessário]

### 3.2 Fases do Projeto

| Fase | Objetivo | Duração | Entregável | Gate de Decisão |
|------|---------|---------|-----------|----------------|
| 0 — Discovery | Validar viabilidade de dados | [X semanas] | Relatório de viabilidade | Go/No-go para MVP |
| 1 — MVP | Modelo mínimo funcional | [X semanas] | Modelo em staging | Performance > baseline? |
| 2 — Piloto | Teste com usuários reais | [X semanas] | Resultados do piloto | Métricas de negócio melhoram? |
| 3 — Produção | Deploy e escala | [X semanas] | Modelo em produção | Aprovação de ética e segurança |
| 4 — Otimização | Melhoria contínua | Contínuo | Dashboards de monitoramento | — |

### 3.3 Critérios de Go/No-Go por Fase

| Fase | Critério para Prosseguir | Critério para Parar |
|------|--------------------------|---------------------|
| Discovery → MVP | [Dados existem e modelo é viável] | [Dados insuficientes ou problema não é ML-friendly] |
| MVP → Piloto | [Performance > baseline + X%] | [Performance não supera métodos atuais] |
| Piloto → Produção | [Métricas de negócio melhoram + ética aprovada] | [Sem impacto em negócio ou riscos éticos] |

---

## 4. Equipe e Governança

### 4.1 Equipe do Projeto

| Papel | Nome | Dedicação | Responsabilidade |
|-------|------|----------|-----------------|
| Sponsor | [Nome] | [X%] | Direção estratégica, remoção de bloqueios |
| Project Lead | [Nome] | [X%] | Gestão do projeto, stakeholders |
| ML Engineer | [Nome] | [X%] | Desenvolvimento e treinamento do modelo |
| Data Engineer | [Nome] | [X%] | Pipelines de dados |
| Backend Engineer | [Nome] | [X%] | Integração e APIs |
| Product Designer | [Nome] | [X%] | UX e interface com o usuário |
| Product Manager | [Nome] | [X%] | Priorização e requisitos de negócio |

### 4.2 Governança

| Fórum | Frequência | Participantes | Objetivo |
|-------|-----------|-------------|----------|
| Standup do projeto | Diário | Time core | Sync e bloqueios |
| Review técnica | Semanal | ML + Eng | Decisões técnicas |
| Steering committee | Quinzenal | Sponsor + leads | Direção e aprovações |
| Update para stakeholders | Mensal | Amplo | Status e resultados |

### 4.3 Matriz RACI

| Decisão | Sponsor | Project Lead | ML Lead | Eng | PM |
|---------|:---:|:---:|:---:|:---:|:---:|
| Escolha de abordagem técnica | I | C | A/R | C | I |
| Priorização de features | I | C | C | I | A/R |
| Go/No-go entre fases | A | R | C | C | C |
| Aprovação de budget | A | R | I | I | I |
| Decisões de UX | I | C | I | I | A/R |

*R=Responsible, A=Accountable, C=Consulted, I=Informed*

---

## 5. Recursos e Investimento

| Categoria | Estimativa | Detalhamento |
|-----------|-----------|-------------|
| Headcount (pessoas x meses) | [R$ X] | [N pessoas x M meses x custo médio] |
| Infraestrutura de ML | [R$ X] | [GPU, storage, MLOps tooling] |
| Dados (aquisição, labeling) | [R$ X] | [Compra de dados, serviço de anotação] |
| APIs externas | [R$ X/mês] | [OpenAI, AWS Bedrock, etc.] |
| Ferramentas e licenças | [R$ X] | [MLflow, Weights & Biases, etc.] |
| **Total** | **[R$ X]** | |

---

## 6. Riscos

| Risco | Probabilidade | Impacto | Mitigação | Owner |
|-------|-------------|---------|-----------|-------|
| Dados insuficientes ou baixa qualidade | [A/M/B] | [A/M/B] | [Discovery phase valida antes de investir] | [ML Lead] |
| Modelo não atinge performance aceitável | [A/M/B] | [A/M/B] | [Gates de go/no-go entre fases] | [ML Lead] |
| Resistência de usuários à IA | [A/M/B] | [A/M/B] | [Change management + piloto gradual] | [PM] |
| Questões éticas/regulatórias | [A/M/B] | [A/M/B] | [Review de ética antes de produção] | [Project Lead] |
| Dependência de API externa | [A/M/B] | [A/M/B] | [Fallback + SLA contratual] | [Eng Lead] |

---

## 7. Comunicação

| Audiência | Formato | Frequência | Responsável |
|----------|---------|-----------|-------------|
| Time do projeto | Standup | Diário | Project Lead |
| Stakeholders | Update escrito | Quinzenal | Project Lead |
| C-Level | Steering committee | Mensal | Sponsor |
| Toda a empresa | Demo / Show & Tell | Ao final de cada fase | PM |

---

## Aprovação

| Papel | Nome | Aprovação | Data |
|-------|------|----------|------|
| Sponsor Executivo | [Nome] | [ ] Aprovado | [DD/MM/AAAA] |
| CFO (se budget > R$ X) | [Nome] | [ ] Aprovado | [DD/MM/AAAA] |
| ML/AI Lead | [Nome] | [ ] Viável tecnicamente | [DD/MM/AAAA] |

---

## Exemplo Preenchido (Resumo)

> **Projeto:** AI-2026-003 — Recomendação personalizada de conteúdo educacional
> **Visão:** Cada aluno recebe trilha personalizada que maximiza engajamento e aprendizado
> **Equipe:** 5 pessoas (1 ML, 1 Data, 1 Backend, 1 Design, 1 PM) — 6 meses
> **Investimento:** R$ 580K | **ROI esperado:** 210% em 18 meses
> **Fase atual:** Discovery (validando dados de comportamento de 200K alunos)

---

## Dicas de Uso
- Charter é contrato — mudanças de escopo devem ser explícitas e aprovadas
- Gates entre fases são essenciais — não invista em produção sem validar viabilidade
- IA tem mais incerteza que projetos tradicionais — planeje para pivots
- Invista em Discovery — é melhor gastar 2 semanas descobrindo que não é viável do que 6 meses
- Sponsor engajado é diferença entre projeto que vira produto e projeto que morre
- Comunique frequentemente — projetos de IA geram expectativas altas e ansiedade
