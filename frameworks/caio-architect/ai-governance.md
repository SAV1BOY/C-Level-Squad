# Governança de AI — Framework de Controle e Compliance

## Propósito e Contexto

Governança de AI é o sistema de estruturas, políticas e processos que garantem que o uso de
inteligência artificial na organização seja controlado, auditável e alinhado com objetivos
de negócio, requisitos legais e princípios éticos. Diferente de "AI responsável" (que foca
em ética e fairness no nível do modelo), governança foca na estrutura organizacional: quem
decide o quê, quem é responsável por quê, e como garantimos compliance em escala.

Com a crescente regulamentação de AI globalmente (EU AI Act, regulação brasileira em discussão),
governança de AI deixou de ser opção para empresas que querem operar em mercados regulados ou
servir clientes enterprise. Este framework cria a estrutura mínima necessária sem burocratizar
a inovação.

## Quando Usar

- Na criação da primeira estrutura de governança de AI
- Na preparação para compliance regulatório (EU AI Act, regulação brasileira)
- Ao escalar o número de modelos em produção (de poucos para muitos)
- Quando incidentes de AI ocorrem e não há processo claro de resposta
- Em auditorias internas ou externas de práticas de AI
- Na preparação para clientes enterprise que exigem AI governance

## Componentes do Framework

### 1. Estrutura de Governança

**AI Governance Board**
- Composição: CAIO, CTO, CPO, Legal/Compliance, representante de ética
- Cadência: mensal + ad hoc para aprovações de alto risco
- Responsabilidades:
  - Aprovar AI policies
  - Revisar casos de uso de alto risco
  - Resolver escalações
  - Monitorar compliance regulatório

**AI Product Owners**
- Cada modelo/sistema de AI tem um owner de negócio (não técnico)
- Responsável por: valor de negócio, decisões de go/no-go, métricas
- Accountability pela performance e impacto do modelo

**ML Engineers / Data Scientists**
- Responsáveis pela implementação técnica
- Seguem os padrões definidos pela governança
- Documentam modelos conforme model card template
- Reportam problemas e riscos proativamente

### 2. Policies e Standards

**Policy 1: AI Use Policy**
- Casos de uso permitidos, restritos e proibidos
- Processo de aprovação por nível de risco
- Requisitos de documentação por tipo de projeto
- Uso de AI por colaboradores (GenAI, Copilot, etc.)

**Policy 2: Data for AI Policy**
- Dados permitidos para treinamento de modelos
- Requisitos de consentimento e base legal (LGPD)
- Retenção e exclusão de dados de treinamento
- Uso de dados de clientes vs. dados sintéticos

**Policy 3: Model Lifecycle Policy**
- Requisitos para deploy em produção (checklist)
- Cadência mínima de revalidação de modelos
- Critérios de descomissionamento
- Processo de rollback e incident response

**Policy 4: Third-Party AI Policy**
- Avaliação de fornecedores de AI (due diligence)
- Requisitos de contrato (IP, dados, SLA, liability)
- Monitoramento de serviços de AI terceirizados
- Uso de APIs de LLMs (OpenAI, Anthropic, etc.)

### 3. Registro de Modelos (AI Inventory)

Manter um inventário centralizado de todos os modelos/sistemas de AI:

| Campo | Descrição |
|-------|-----------|
| ID | Identificador único |
| Nome | Nome descritivo |
| Owner (negócio) | Responsável de negócio |
| Owner (técnico) | ML engineer responsável |
| Classificação de risco | Baixo / Médio / Alto |
| Status | Development / Staging / Production / Deprecated |
| Data de deploy | Quando entrou em produção |
| Última validação | Data da última review |
| Próxima validação | Data agendada |
| Model card | Link para documentação |
| Dependências | Modelos ou dados dos quais depende |

### 4. Processo de Aprovação por Risco

**Baixo Risco:** Aprovação pelo ML Lead
- Documentação: model card básico
- Review: code review + test results
- Timeline: < 1 semana

**Médio Risco:** Aprovação pelo AI Product Owner + ML Lead
- Documentação: model card completo + impact assessment
- Review: code review + fairness testing + security review
- Timeline: 1-2 semanas

**Alto Risco:** Aprovação pelo AI Governance Board
- Documentação: model card + impact assessment + legal review
- Review: todas as anteriores + external audit (se necessário)
- Timeline: 2-4 semanas

## Processo Passo-a-Passo

### Fase 1: Fundação (mês 1-2)
1. Formar AI Governance Board
2. Publicar AI Use Policy (versão 1.0 — pragmática e iterável)
3. Criar template de model card e impact assessment
4. Inventário de todos os modelos/sistemas de AI existentes

### Fase 2: Estruturação (mês 3-4)
1. Implementar processo de aprovação por risco
2. Classificar modelos existentes por nível de risco
3. Remediar gaps de documentação em modelos de alto risco
4. Treinar equipe de AI em processos de governança

### Fase 3: Automação (mês 5-8)
1. Automatizar checklist de deploy (integrado ao CI/CD)
2. Dashboard de AI inventory com status de compliance
3. Alertas automáticos para modelos que precisam de revalidação
4. Integração com MLOps pipeline para audit trail

### Fase 4: Maturidade (ongoing)
1. Auditorias internas regulares (trimestral)
2. Atualização de policies baseada em regulamentação e aprendizados
3. Benchmark de governance practices com mercado
4. Preparação para auditorias externas/certificações

## Template de AI Governance Report

```markdown
# AI Governance Report — [Trimestre/Ano]

## Resumo
- Total de modelos em produção: [N]
- Novos modelos deployados: [N]
- Modelos descomissionados: [N]
- Incidentes de AI: [N]

## Compliance Status
| Métrica | Status |
|---------|--------|
| Modelos com model card atualizado | [X]% |
| Modelos com risk classification | [X]% |
| Modelos dentro do prazo de revalidação | [X]% |
| Impact assessments completos (alto risco) | [X]% |

## Incidentes
[Resumo de incidentes e ações tomadas]

## Riscos Identificados
[Novos riscos e plano de mitigação]

## Policy Updates
[Mudanças em policies e justificativa]

## Ações para Próximo Trimestre
[Lista de ações com owners]
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| AI inventory completeness | 100% dos modelos registrados | Contínuo |
| Model card coverage | 100% dos modelos em produção | Trimestral |
| Risk classification coverage | 100% dos modelos | Contínuo |
| Revalidation compliance | 100% no prazo | Mensal |
| Governance review time (baixo risco) | < 1 semana | Por review |
| AI incidents responded within SLA | 100% | Por incidente |
| Policy update frequency | Pelo menos anual | Anual |

## Referências Cruzadas

- `frameworks/caio-architect/responsible-ai.md` — Ética e fairness por modelo
- `frameworks/caio-architect/ai-maturity-model.md` — Governança como dimensão de maturidade
- `frameworks/caio-architect/mlops-framework.md` — Pipeline com governance integrado
- `frameworks/caio-architect/ai-product-development.md` — Governance no ciclo de produto
- `frameworks/cio-engineer/security-posture.md` — Segurança de sistemas AI
- `frameworks/cio-engineer/data-platform.md` — Governança de dados
- `frameworks/shared/risk-management.md` — AI risk no framework corporativo
- `frameworks/shared/stakeholder-management.md` — Board e reguladores como stakeholders
