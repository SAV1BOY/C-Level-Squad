# Workflow: Avaliação e RFP (Request for Proposal)

## Objetivo

Estruturar o processo de identificação, avaliação e seleção de fornecedores através de um RFP padronizado, garantindo que a escolha seja baseada em critérios objetivos de adequação técnica, custo, risco e alinhamento estratégico.

## Trigger

- Necessidade de novo fornecedor identificada por área funcional
- Contrato existente próximo de expiração sem renovação automática
- Insatisfação com fornecedor atual documentada
- Novo projeto que requer capacidade externa
- Budget aprovado para aquisição de solução

## Participantes (RACI)

| Papel | Responsabilidade |
|-------|-----------------|
| Gestor Solicitante | **Responsible** — Define requisitos e avalia propostas |
| Procurement / Compras | **Accountable** — Conduz processo de RFP e negociação |
| TI / Security | **Consulted** — Avaliação técnica e de segurança |
| Jurídico | **Consulted** — Revisão de termos contratuais |
| FP&A | **Consulted** — Validação de impacto orçamentário |
| VP da Área | **Informed** — Aprovação da decisão final |

## Etapas do Workflow

### Etapa 1: Definição de Requisitos
- Gestor documenta necessidade de negócio e requisitos funcionais
- TI define requisitos técnicos: integrações, segurança, compliance
- Classificar requisitos: obrigatórios (must-have) vs desejáveis (nice-to-have)
- Definir critérios de avaliação com pesos
- Estimar budget disponível e timeline esperada
- **SLA: 1 semana**

### Etapa 2: Pesquisa de Mercado
- Procurement pesquisa fornecedores potenciais (5-10 candidatos)
- Fontes: Gartner, G2, referências de mercado, network
- Short-list de 3-5 fornecedores para receber RFP
- Validar que fornecedores atendem requisitos mínimos
- **SLA: 1 semana**

### Etapa 3: Elaboração e Envio do RFP
- Procurement prepara documento de RFP padronizado
- Seções: contexto da empresa, requisitos, critérios de avaliação, timeline, SLA esperado
- Incluir NDA para informações confidenciais
- Enviar RFP para fornecedores selecionados
- Q&A period: 1 semana para perguntas dos fornecedores
- **SLA: 1 semana para elaboração + 2-3 semanas para resposta**

### Etapa 4: Avaliação de Propostas
- Comitê avaliador revisa cada proposta contra scorecard
- Critérios típicos e pesos:
  - Adequação funcional: 30%
  - Qualidade técnica: 25%
  - Custo total (TCO): 20%
  - Experiência e referências: 15%
  - Suporte e SLA: 10%
- Scoring independente por cada avaliador, depois calibração
- **SLA: 2 semanas**

### Etapa 5: Shortlist e Demonstrações
- Top 2-3 fornecedores convidados para demo/apresentação
- Demonstração focada nos use cases específicos da empresa
- Sessão técnica com TI para avaliar integrações
- Verificação de referências com clientes do fornecedor
- **SLA: 2 semanas**

### Etapa 6: Recomendação e Aprovação
- Procurement consolida avaliação final com ranking
- Preparar recomendação com justificativa detalhada
- Apresentar para VP da área e stakeholders
- Aprovação formal para avançar com fornecedor selecionado
- **SLA: 1 semana**

## Outputs / Entregáveis

- Documento de requisitos aprovado
- RFP enviado e respostas recebidas
- Scorecard de avaliação preenchido por fornecedor
- Relatório de referências
- Recomendação final com ranking e justificativa
- Aprovação formal para avançar com POC ou contrato

## Métricas de Sucesso

| Métrica | Meta | Frequência |
|---------|------|------------|
| Processo de RFP concluído no prazo | ≥ 85% | Por RFP |
| Propostas recebidas vs enviadas | ≥ 60% de resposta | Por RFP |
| Fornecedor selecionado atende must-haves | 100% | Por RFP |
| Satisfação com fornecedor após 6 meses | ≥ 4.0/5.0 | Semestral |
| Tempo total do processo (requisitos a seleção) | ≤ 8 semanas | Por RFP |

## Integração com Outros Workflows

- **02-poc-pilot.md**: Fornecedor selecionado avança para POC
- **03-contract-negotiation.md**: Proposta aceita vai para negociação contratual
- **Budget Cycle / 02-department-submissions.md**: Novo fornecedor previsto no budget
- **Data Governance / 04-compliance-audit.md**: Compliance do fornecedor avaliada
