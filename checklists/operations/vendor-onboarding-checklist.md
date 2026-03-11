# Checklist de Onboarding de Vendor/Fornecedor

## Objetivo
Estruturar o processo de avaliação, contratação e integração de novos fornecedores, garantindo compliance, segurança e alinhamento com padrões da empresa.

---

## Fase 1: Avaliação e Seleção

### Identificação de Necessidade
- [ ] Documentar necessidade de negócio que o vendor atenderá
- [ ] Verificar se já existe fornecedor aprovado para a categoria
- [ ] Avaliar opção de build interno vs buy/outsource
- [ ] Definir requisitos técnicos e funcionais obrigatórios
- [ ] Estabelecer budget aprovado para a contratação
- [ ] Definir timeline de implementação desejado
- [ ] Identificar owner interno do relacionamento com o vendor

### Pesquisa de Mercado
- [ ] Identificar 3-5 fornecedores candidatos
- [ ] Coletar referências de peers e empresas similares
- [ ] Verificar reviews em plataformas como G2, Gartner, Forrester
- [ ] Avaliar saúde financeira e estabilidade dos candidatos
- [ ] Verificar presença no mercado local e suporte em português
- [ ] Analisar roadmap de produto e visão de futuro

### Request for Proposal (RFP)
- [ ] Elaborar RFP com requisitos detalhados
- [ ] Enviar RFP para fornecedores shortlistados
- [ ] Definir critérios de avaliação com pesos
- [ ] Agendar demos e provas de conceito (POC)
- [ ] Avaliar propostas com matriz de decisão
- [ ] Selecionar finalista com justificativa documentada

---

## Fase 2: Due Diligence

### Avaliação Financeira
- [ ] Solicitar demonstrações financeiras dos últimos 3 anos
- [ ] Verificar CNPJ e situação fiscal na Receita Federal
- [ ] Consultar protestos e pendências em bureaus de crédito
- [ ] Avaliar dependência de receita (não ser 100% dependente de nós)
- [ ] Verificar se empresa possui seguros adequados
- [ ] Avaliar modelo de pricing e previsibilidade de custos

### Avaliação de Segurança
- [ ] Solicitar e revisar certificações (SOC2, ISO 27001)
- [ ] Aplicar questionário de segurança da informação
- [ ] Verificar políticas de proteção de dados e privacidade
- [ ] Avaliar compliance com LGPD/GDPR
- [ ] Verificar práticas de gestão de incidentes de segurança
- [ ] Avaliar processo de gestão de vulnerabilidades
- [ ] Verificar se realiza pentest periódico
- [ ] Revisar arquitetura de segurança e controles de acesso

### Avaliação Legal e Compliance
- [ ] Verificar existência de processos judiciais relevantes
- [ ] Avaliar compliance com regulamentações do setor
- [ ] Verificar políticas anticorrupção e antissuborno
- [ ] Avaliar práticas trabalhistas e compliance com CLT
- [ ] Verificar se possui código de conduta e ética
- [ ] Avaliar riscos de propriedade intelectual

---

## Fase 3: Contratação

### Negociação Comercial
- [ ] Negociar termos de pricing e condições de pagamento
- [ ] Definir SLAs de disponibilidade, performance e suporte
- [ ] Estabelecer penalidades por descumprimento de SLA
- [ ] Negociar cláusula de benchmark de preço periódico
- [ ] Definir modelo de faturamento e moeda
- [ ] Acordar processo de change request e custos adicionais

### Contrato
- [ ] Redigir ou revisar contrato com jurídico interno
- [ ] Incluir cláusula de proteção de dados (DPA)
- [ ] Definir termos de confidencialidade (NDA)
- [ ] Incluir cláusula de auditoria e direito de inspeção
- [ ] Definir condições de rescisão e transição
- [ ] Incluir cláusula de propriedade intelectual
- [ ] Definir limites de responsabilidade e indenização
- [ ] Obter assinaturas de ambas as partes
- [ ] Registrar contrato no sistema de gestão de contratos

### Aprovações Internas
- [ ] Aprovação do budget pelo gestor de área
- [ ] Aprovação financeira conforme alçada (procurement)
- [ ] Aprovação de segurança se dados sensíveis envolvidos
- [ ] Aprovação jurídica do contrato final
- [ ] Aprovação de compliance se regulamentações aplicáveis

---

## Fase 4: Integração Técnica

### Setup Inicial
- [ ] Criar contas e acessos na plataforma do vendor
- [ ] Configurar SSO/SAML se suportado
- [ ] Implementar integrações técnicas necessárias (APIs, webhooks)
- [ ] Configurar ambientes de desenvolvimento e produção
- [ ] Testar conectividade e performance das integrações
- [ ] Documentar arquitetura de integração

### Segurança e Compliance
- [ ] Configurar controles de acesso baseados em role (RBAC)
- [ ] Implementar logging e auditoria de acessos
- [ ] Configurar alertas de segurança
- [ ] Validar criptografia de dados em trânsito e repouso
- [ ] Testar processo de revogação de acessos
- [ ] Documentar fluxos de dados entre sistemas

### Operacional
- [ ] Definir processo de suporte e escalation com o vendor
- [ ] Configurar canais de comunicação (email, ticket, chat)
- [ ] Treinar equipe interna na ferramenta do vendor
- [ ] Criar runbook para operações comuns
- [ ] Definir processo de gestão de incidentes envolvendo vendor
- [ ] Agendar reunião periódica de review com account manager

---

## Fase 5: Gestão Contínua

### Monitoramento de Performance
- [ ] Monitorar SLAs mensalmente com dados do vendor e internos
- [ ] Realizar business review trimestral com o vendor
- [ ] Avaliar satisfação interna dos usuários semestralmente
- [ ] Revisar custos vs valor entregue anualmente
- [ ] Acompanhar roadmap do vendor e impacto para nós
- [ ] Documentar issues e resolução para histórico

### Renovação e Reavaliação
- [ ] Iniciar processo de renovação 3 meses antes do vencimento
- [ ] Reavaliar necessidade e satisfação antes de renovar
- [ ] Fazer benchmark de mercado antes de renegociar
- [ ] Revisar SLAs e ajustar conforme experiência
- [ ] Considerar alternativas se performance insatisfatória
- [ ] Documentar decisão de renovar, renegociar ou trocar
