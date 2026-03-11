# Review de Ética em AI

> Processo estruturado para avaliar implicações éticas de sistemas de AI
> antes e durante o deployment, garantindo que a tecnologia é usada de
> forma responsável e alinhada com os valores da organização.

## Objetivo

Garantir que sistemas de AI são desenvolvidos e operados de forma ética,
transparente e responsável, minimizando riscos de dano a indivíduos e
comunidades, e mantendo conformidade com regulamentações emergentes.

## Frequência

- **Pré-deploy:** Obrigatório para qualquer novo sistema ou feature de AI
- **Operação:** Semestral para sistemas em produção
- **Ad-hoc:** Quando complaints éticos são recebidos
- **Regulatório:** Conforme exigido por legislação (EU AI Act, etc.)

## Framework de Avaliação Ética

### 1. Transparência e Explicabilidade
- [ ] Usuários sabem que estão interagindo com AI?
- [ ] O sistema pode explicar suas decisões de forma compreensível?
- [ ] Existe documentação sobre como o modelo funciona?
- [ ] Limitações do modelo são comunicadas aos usuários?
- [ ] O grau de confiança do modelo é apresentado ao usuário?

### 2. Fairness e Não-Discriminação
- [ ] O sistema foi testado para bias contra grupos protegidos?
- [ ] Existe processo de bias audit (ver `tasks/ai/bias-audit.md`)?
- [ ] Dados de treinamento são representativos?
- [ ] Métricas de fairness são monitoradas continuamente?
- [ ] Há processo para complaints de discriminação?

### 3. Privacidade e Proteção de Dados
- [ ] Dados pessoais são tratados conforme LGPD/GDPR?
- [ ] Minimização de dados está implementada?
- [ ] Consentimento adequado foi obtido?
- [ ] Dados podem ser excluídos a pedido do titular?
- [ ] Modelo não memoriza/regurgita dados de treinamento?

### 4. Segurança e Robustez
- [ ] O sistema é resistente a ataques adversariais?
- [ ] Existem guardrails contra outputs prejudiciais?
- [ ] O sistema degrada gracefully em cenários inesperados?
- [ ] Há monitoramento de uso malicioso?
- [ ] Kill switch disponível para desativar o sistema rapidamente?

### 5. Accountability e Governança
- [ ] Existe um owner responsável pelo sistema?
- [ ] Decisões do modelo podem ser auditadas?
- [ ] Há processo de contestação para decisões automatizadas?
- [ ] Cadeia de responsabilidade está clara?
- [ ] Seguro ou reserva financeira para danos causados?

### 6. Impacto Social
- [ ] O sistema pode deslocar trabalhadores? Há plano de transição?
- [ ] O sistema pode ser usado para vigilância ou controle?
- [ ] Impacto ambiental (consumo de energia) foi avaliado?
- [ ] Dependência excessiva no sistema foi considerada?
- [ ] Grupos vulneráveis foram considerados no design?

### 7. Supervisão Humana
- [ ] Decisões de alto impacto têm human-in-the-loop?
- [ ] Usuários podem overridar o sistema quando necessário?
- [ ] Há processo de escalação para casos edge?
- [ ] O sistema informa quando não tem confiança suficiente?

## Classificação de Risco (Alinhado com EU AI Act)

### Risco Inaceitável (Proibido)
- Scoring social de pessoas
- Manipulação comportamental subliminar
- Exploração de vulnerabilidades de grupos específicos
- Identificação biométrica em massa em tempo real

### Alto Risco (Requer avaliação rigorosa)
- Decisões de crédito ou seguros
- Recrutamento e seleção
- Diagnóstico médico
- Decisões judiciais ou de aplicação da lei
- Acesso a educação ou serviços essenciais

### Risco Limitado (Requer transparência)
- Chatbots (usuário deve saber que é AI)
- Geração de conteúdo (deve ser labeled como AI-generated)
- Sistemas de recomendação
- Classificação de conteúdo

### Risco Mínimo (Sem requisitos especiais)
- Spam filters
- Otimização de inventário
- Previsão de demanda
- Automação de processos internos sem impacto em pessoas

## Processo de Review

### Fase 1: Self-Assessment (Time de Produto/Engenharia)
- [ ] Preencher questionário de ética (template abaixo)
- [ ] Classificar risco do sistema
- [ ] Documentar decisões de design com justificativa ética
- [ ] Identificar stakeholders afetados

### Fase 2: Review por Comitê de Ética AI
- [ ] Revisar self-assessment
- [ ] Entrevistar time sobre decisões de design
- [ ] Avaliar bias audit results (se disponível)
- [ ] Consultar stakeholders externos se necessário
- [ ] Emitir parecer: aprovado, condicionado, ou rejeitado

### Fase 3: Monitoramento Contínuo
- [ ] Métricas de ética incluídas no dashboard do modelo
- [ ] Processo de feedback de usuários ativo
- [ ] Review periódico conforme classificação de risco
- [ ] Atualização quando contexto muda

## Comitê de Ética AI

### Composição Recomendada
- CTO ou VP Engineering (decisão técnica)
- Head de Legal/Compliance (conformidade)
- Head de D&I ou representante (diversidade)
- Product lead (perspectiva do usuário)
- Membro externo independente (perspectiva não-enviesada)

### Mandato
- Revisar e aprovar todos os sistemas de AI de alto risco
- Definir políticas de uso ético de AI
- Investigar complaints éticos
- Aconselhar a liderança sobre riscos emergentes

## Template de Ethical Impact Assessment

```
ETHICAL IMPACT ASSESSMENT
Sistema: [Nome]
Data: [Data]
Avaliador: [Nome/Time]
Classificação de Risco: [Inaceitável/Alto/Limitado/Mínimo]

1. DESCRIÇÃO DO SISTEMA
O que faz, para quem, como funciona.

2. STAKEHOLDERS AFETADOS
Quem é impactado direta e indiretamente.

3. BENEFÍCIOS ESPERADOS
Valor que o sistema traz para usuários e negócio.

4. RISCOS ÉTICOS IDENTIFICADOS
| Risco | Probabilidade | Impacto | Mitigação |
|-------|---------------|---------|-----------|

5. TRANSPARÊNCIA
Como usuários são informados sobre o uso de AI.

6. FAIRNESS
Resultados de bias audit e mitigações.

7. PRIVACIDADE
Como dados pessoais são tratados.

8. SUPERVISÃO HUMANA
Quando e como humanos intervêm.

9. DECISÃO
[ ] Aprovado
[ ] Aprovado com condições: [listar]
[ ] Rejeitado: [justificativa]

Assinaturas:
- Avaliador: ___
- Comitê de Ética: ___
```

## Referências

- EU AI Act (2024)
- OECD AI Principles
- UNESCO Recommendation on AI Ethics (2021)
- "Ethics of Artificial Intelligence" - S. Matthew Liao (Oxford, 2020)
- "Responsible AI" - Microsoft AI Principles (microsoft.com/ai/responsible-ai)
- Brazil AI Strategy (EBIA)
