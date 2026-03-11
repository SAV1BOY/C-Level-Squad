# Workflow: Aprovação de Requisição de Vaga

## Objetivo

Garantir que toda nova contratação passe por um processo estruturado de aprovação, validando necessidade de negócio, disponibilidade orçamentária e alinhamento estratégico antes de iniciar o processo seletivo.

## Trigger

- Gestor identifica necessidade de nova contratação (expansão, substituição ou reestruturação)
- Aprovação prévia em planejamento de headcount trimestral
- Solicitação ad hoc com justificativa de negócio

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Gestor Solicitante | **Responsible** — Preenche requisição e justificativa |
| HRBP (Business Partner) | **Accountable** — Valida aderência à estrutura organizacional |
| Diretor da Área | **Consulted** — Aprova necessidade funcional |
| CFO / FP&A | **Consulted** — Valida disponibilidade orçamentária |
| VP de People | **Informed** — Visibilidade sobre pipeline de contratação |

## Pré-requisitos

1. Headcount aprovado no ciclo de planejamento OU justificativa ad hoc documentada
2. Job description atualizada e validada pelo HRBP
3. Faixa salarial definida conforme política de remuneração vigente
4. Orçamento de recrutamento disponível (agência, ferramentas, anúncios)

## Etapas do Workflow

### Etapa 1: Abertura da Requisição
- Gestor preenche formulário de requisição no sistema de ATS
- Campos obrigatórios: título do cargo, nível, departamento, localidade, modelo (remoto/híbrido/presencial)
- Justificativa de negócio: impacto em receita, produtividade ou risco operacional
- Prazo esperado para preenchimento da vaga
- **SLA: 1 dia útil para preenchimento completo**

### Etapa 2: Validação pelo HRBP
- HRBP revisa aderência à estrutura organizacional aprovada
- Verifica se o cargo está mapeado na arquitetura de cargos e salários
- Confirma que a job description reflete competências e requisitos reais
- Sugere ajustes se necessário (nível, escopo, reporting line)
- **SLA: 2 dias úteis**

### Etapa 3: Aprovação Orçamentária
- FP&A valida impacto no budget de pessoal do centro de custo
- Calcula custo total da posição: salário base + benefícios + encargos + bônus
- Verifica se há espaço no headcount planejado ou necessidade de realocação
- Sinaliza riscos orçamentários se aplicável
- **SLA: 2 dias úteis**

### Etapa 4: Aprovação do Diretor
- Diretor da área revisa e aprova a requisição
- Para posições de nível gerencial ou superior, aprovação adicional do VP
- Para posições de diretoria, aprovação do CEO
- **SLA: 2 dias úteis**

### Etapa 5: Aprovação Final e Publicação
- HRBP confirma todas as aprovações no sistema
- Requisição muda de status para "Aprovada"
- Time de Talent Acquisition é notificado automaticamente
- Briefing de kick-off agendado entre TA e gestor solicitante
- **SLA: 1 dia útil**

### Etapa 6: Kick-off com Talent Acquisition
- Reunião de alinhamento entre recruiter designado e gestor
- Definição de estratégia de sourcing (canais, perfil ideal, diferencial competitivo)
- Acordo sobre cronograma e cadência de updates
- Definição do painel de entrevistadores
- **SLA: 3 dias úteis após aprovação**

## Outputs / Entregáveis

- Requisição aprovada e registrada no ATS com todas as informações
- Job description final publicável
- Faixa salarial aprovada e documentada
- Cronograma de recrutamento acordado
- Painel de entrevistadores definido
- Estratégia de sourcing documentada

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Tempo médio de aprovação (abertura a aprovação) | ≤ 5 dias úteis | Mensal |
| Taxa de requisições devolvidas para ajuste | < 15% | Mensal |
| Aderência ao headcount planejado | > 90% | Trimestral |
| Satisfação do gestor com o processo | ≥ 4.0/5.0 | Trimestral |
| Requisições canceladas após aprovação | < 5% | Trimestral |

## Regras de Exceção

- **Contratações emergenciais**: processo acelerado com aprovação verbal do VP + formalização em 48h
- **Posições confidenciais**: fluxo restrito com acesso limitado no ATS
- **Posições internacionais**: etapa adicional de validação jurídica e de compliance

## Integração com Outros Workflows

- **02-sourcing-pipeline.md**: Alimenta o pipeline de sourcing após aprovação
- **Budget Cycle / 02-department-submissions.md**: Requisições devem estar alinhadas ao headcount aprovado
- **OKR Cycle / 02-quarterly-planning.md**: Contratações estratégicas linkadas a OKRs do quarter
- **Change Management / 01-impact-assessment.md**: Reestruturações que geram novas vagas passam por avaliação de impacto

## Ferramentas Recomendadas

- ATS (Greenhouse, Lever, Gupy) para gestão do fluxo
- Sistema de aprovação integrado (Pipefy, ServiceNow)
- Planilha de headcount no FP&A (integração com ERP)

## Revisão do Workflow

- Revisão semestral pelo time de People Operations
- Feedback contínuo dos gestores via pesquisa de satisfação
- Ajustes baseados em métricas de eficiência do processo
