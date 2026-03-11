# Checklist de Qualidade — Vendor Selection (Seleção de Fornecedores)

## Propósito
Garantir que a seleção de fornecedores seja rigorosa: fit com necessidades avaliado sistematicamente, custos analisados com TCO (Total Cost of Ownership), riscos de dependência avaliados, SLAs definidos com clareza e plano de saída documentado antes da contratação. Este checklist protege a organização contra vendor lock-in, custos ocultos e riscos operacionais de dependência excessiva.

## Quando Aplicar
- Antes de selecionar qualquer fornecedor acima do threshold de materialidade definido
- Na renovação de contratos existentes com fornecedores críticos
- Quando há consolidação de fornecedores ou mudança de vendor estratégico
- Na avaliação de parceiros de tecnologia, serviços ou infraestrutura
- Quando agentes de procurement geram recomendações de vendor para validação
- Em auditorias periódicas de vendor management

## Agente Responsável
- **Primário:** COO Agent ou Procurement Agent
- **Co-responsável:** O C-Level Agent da área requisitante (CTO para tech vendors, CMO para marketing vendors, etc.)
- **Revisor:** CFO Agent (para análise financeira) e Legal Agent (para termos contratuais)
- **Aprovador:** CEO Agent para vendors estratégicos ou acima de threshold financeiro

## Checklist

### Seção 1 — Fit Avaliado
- [ ] Os requisitos do negócio estão documentados de forma clara e priorizados (must-have vs nice-to-have)
- [ ] O RFP (Request for Proposal) ou RFI (Request for Information) foi emitido quando aplicável
- [ ] No mínimo 3 vendors foram avaliados para garantir competitividade
- [ ] Cada vendor foi avaliado contra os mesmos critérios de forma consistente
- [ ] A capacidade técnica do vendor atende aos requisitos funcionais e não-funcionais
- [ ] A compatibilidade com o stack tecnológico e processos existentes está verificada
- [ ] A escalabilidade da solução do vendor atende às projeções de crescimento
- [ ] A experiência do vendor com empresas do mesmo porte e setor está verificada
- [ ] As referências de clientes atuais do vendor foram consultadas
- [ ] O POC (Proof of Concept) ou trial foi realizado para validar fit antes da decisão
- [ ] A estabilidade financeira e viabilidade de longo prazo do vendor está avaliada
- [ ] O roadmap do vendor está alinhado com as necessidades futuras da organização

### Seção 2 — Custos Analisados
- [ ] O TCO (Total Cost of Ownership) está calculado para 3-5 anos
- [ ] Os custos de licenciamento ou assinatura estão detalhados por componente
- [ ] Os custos de implementação e integração estão estimados (incluindo interno)
- [ ] Os custos de migração de dados estão incluídos
- [ ] Os custos de treinamento e change management estão estimados
- [ ] Os custos operacionais recorrentes estão projetados (suporte, manutenção, upgrades)
- [ ] Os custos de customização estão estimados (se aplicável)
- [ ] O comparativo de custos entre vendors finalistas está documentado
- [ ] Os custos ocultos foram investigados (overage fees, hidden charges, minimum commitments)
- [ ] O modelo de pricing está claro e previsível (sem surpresas de escala)
- [ ] O impacto em budget está validado pelo CFO Agent
- [ ] O ROI esperado da contratação está calculado com premissas explícitas

### Seção 3 — Riscos Avaliados
- [ ] O risco de vendor lock-in está avaliado e classificado (alto, médio, baixo)
- [ ] O risco de descontinuidade do vendor ou produto está analisado
- [ ] O risco de segurança e compliance (data privacy, LGPD, SOC2) está verificado
- [ ] O risco de performance e disponibilidade está avaliado contra requisitos
- [ ] O risco de dependência operacional (single point of failure) está mapeado
- [ ] Os riscos geopolíticos ou regulatórios do vendor estão considerados
- [ ] O risco de integração com sistemas existentes está avaliado
- [ ] O risco de change management (adoção, resistência) está considerado
- [ ] Os planos de mitigação para riscos de alta severidade estão definidos
- [ ] O impacto de falha do vendor na operação da empresa está modelado
- [ ] A capacidade de suporte do vendor em horários críticos está verificada

### Seção 4 — SLAs Definidos
- [ ] Os SLAs de disponibilidade (uptime) estão definidos com percentuais específicos
- [ ] Os SLAs de performance (latência, throughput) estão especificados e mensuráveis
- [ ] Os SLAs de suporte (tempo de resposta, tempo de resolução) estão definidos por severidade
- [ ] As penalidades por descumprimento de SLA estão negociadas e documentadas
- [ ] Os SLAs de segurança (response time para vulnerabilidades) estão definidos
- [ ] O mecanismo de medição e reporting de SLAs está acordado
- [ ] A frequência de revisão de SLAs está definida (tipicamente anual)
- [ ] Os SLAs estão alinhados com os SLAs que a organização promete aos próprios clientes
- [ ] Os SLAs de migração e onboarding estão definidos (go-live timeline)
- [ ] As exclusões de SLA (manutenção planejada, force majeure) estão documentadas

### Seção 5 — Exit Plan Definido
- [ ] As condições de saída (termination clauses) estão negociadas no contrato
- [ ] O período de notice para cancelamento está definido e razoável
- [ ] O custo de saída (early termination fees, migration costs) está estimado
- [ ] O plano de migração de dados para outro vendor ou in-house está delineado
- [ ] O formato e timing de export de dados estão definidos contratualmente
- [ ] O período de transição pós-cancelamento está acordado
- [ ] Os riscos de lock-in que dificultam a saída estão mitigados (abstractions, APIs abertas)
- [ ] As alternativas ao vendor atual estão identificadas e mantidas como opção
- [ ] O vendor não possui ownership sobre dados, customizações ou propriedade intelectual gerada
- [ ] O plano de continuidade de negócio se o vendor falhar abruptamente está definido

### Seção 6 — Processo e Governança
- [ ] O processo de seleção foi competitivo e documentado
- [ ] Os conflitos de interesse foram verificados e declarados
- [ ] A due diligence do vendor está completa (financeira, legal, operacional)
- [ ] O contrato foi revisado pelo jurídico antes da assinatura
- [ ] A aprovação segue o governance model (thresholds de aprovação por valor)
- [ ] O vendor está registrado no vendor management system da organização
- [ ] A revisão periódica do vendor está agendada (anual no mínimo)
- [ ] Os KPIs de performance do vendor estão definidos para monitoramento contínuo
- [ ] O relationship owner (ponto focal interno para o vendor) está designado

## Critérios de Aprovação
- Fit avaliado com POC ou trial completado e referências verificadas
- TCO calculado para 3-5 anos e aprovado pelo CFO Agent
- Riscos avaliados com planos de mitigação para riscos de alta severidade
- SLAs definidos e alinhados com necessidades operacionais
- Exit plan documentado com custos estimados e plano de migração
- Contrato revisado pelo jurídico e aprovado conforme governance model
- Score mínimo de completude: 90% dos itens marcados

## O que Fazer se Falhar
1. Se o fit não está comprovado, não avançar sem POC — o custo de erro é muito alto
2. Se TCO não está claro, solicitar detalhamento ao vendor e recalcular antes de decidir
3. Se SLAs não estão definidos, não assinar contrato — SLAs são negociados antes, não depois
4. Se exit plan não está documentado, exigir cláusulas contratuais antes da assinatura
5. Se riscos de lock-in são altos, investigar alternativas ou negociar mitigações contratuais
6. Registrar experiências de vendor selection no RalphLoop para calibrar processos futuros
7. Nunca selecionar vendor sob pressão de tempo sem diligência mínima completada

## Referências
- Weele, A. — "Purchasing and Supply Chain Management" (procurement best practices)
- ITIL — Service Level Management framework
- Gartner — Magic Quadrant methodology (vendor evaluation)
- Template interno: `/templates/vendor-evaluation-template.md`
- RFP template: `/templates/rfp-template.md`
- Vendor management dashboard: `/dashboards/vendor-tracker.md`
