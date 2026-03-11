# Checklist de Avaliação de Vendor AI

> Checklist estruturado para avaliar fornecedores de soluções de inteligência
> artificial, garantindo alinhamento técnico, comercial e estratégico.

---

## 1. Avaliação Técnica

### 1.1 Capacidades do Modelo
- [ ] Tipo de modelo adequado ao caso de uso (NLP, visão, previsão, etc.)
- [ ] Benchmarks de performance publicados e verificáveis
- [ ] Suporte a fine-tuning ou customização do modelo
- [ ] Capacidade de processar dados em português brasileiro
- [ ] Latência de inferência dentro dos requisitos (< SLA definido)
- [ ] Throughput suportado compatível com volume esperado
- [ ] Suporte a batch e real-time inference
- [ ] Capacidade de lidar com dados multimodais (se necessário)
- [ ] Versionamento de modelos disponível
- [ ] Explicabilidade das predições (XAI) disponível

### 1.2 Infraestrutura e Integração
- [ ] API REST/gRPC disponível e bem documentada
- [ ] SDKs disponíveis para linguagens utilizadas pelo time
- [ ] Suporte a deployment on-premises (se necessário)
- [ ] Opção de cloud privada ou VPC dedicada
- [ ] Rate limits adequados ao volume de uso
- [ ] Uptime SLA >= 99.9%
- [ ] Redundância geográfica disponível
- [ ] Integração com ferramentas existentes (MLflow, Databricks, etc.)
- [ ] Webhooks ou event-driven integration disponível
- [ ] Suporte a containerização (Docker, Kubernetes)

### 1.3 Qualidade e Monitoramento
- [ ] Ferramentas de monitoramento de modelo incluídas
- [ ] Detecção de drift de dados automática
- [ ] Dashboard de métricas de performance
- [ ] Logging e auditoria de chamadas disponível
- [ ] Alertas configuráveis para degradação
- [ ] A/B testing nativo suportado

## 2. Avaliação de Segurança

- [ ] Certificações de segurança (SOC 2, ISO 27001)
- [ ] Criptografia de dados at-rest e in-transit
- [ ] Política de retenção de dados clara
- [ ] Dados de input NÃO utilizados para re-treino (opt-out garantido)
- [ ] Controle de acesso granular (RBAC)
- [ ] Penetration testing recente disponível para revisão
- [ ] Política de resposta a incidentes documentada
- [ ] Conformidade com LGPD confirmada
- [ ] Data Processing Agreement (DPA) disponível
- [ ] Localização dos servidores compatível com requisitos legais
- [ ] Suporte a SSO/SAML para autenticação
- [ ] Audit logs disponíveis e exportáveis

## 3. Avaliação Comercial

### 3.1 Modelo de Pricing
- [ ] Modelo de precificação transparente e previsível
- [ ] Custo por chamada/token/unidade documentado
- [ ] Descontos por volume disponíveis
- [ ] Período de teste gratuito ou créditos iniciais
- [ ] Sem custos ocultos (egress, armazenamento, suporte)
- [ ] Projeção de custo para 12, 24 e 36 meses realizada
- [ ] Comparação de TCO com alternativas (build vs. buy)
- [ ] Flexibilidade para ajustar plano conforme crescimento

### 3.2 Termos Contratuais
- [ ] Duração mínima do contrato aceitável
- [ ] Cláusula de saída sem penalidades excessivas
- [ ] SLA com penalidades financeiras por descumprimento
- [ ] Propriedade intelectual dos dados e modelos customizados clara
- [ ] Cláusula de portabilidade de dados incluída
- [ ] Proteção contra mudanças unilaterais de preço
- [ ] Direitos sobre modelos fine-tunados definidos
- [ ] Cláusula de continuidade em caso de descontinuação do produto

## 4. Avaliação de Suporte e Parceria

- [ ] Canais de suporte disponíveis (chat, email, telefone)
- [ ] Tempo de resposta garantido (SLA de suporte)
- [ ] Suporte técnico em português disponível
- [ ] Customer Success Manager designado
- [ ] Documentação técnica completa e atualizada
- [ ] Comunidade ativa de desenvolvedores
- [ ] Roadmap de produto compartilhado
- [ ] Programa de early access para novas features
- [ ] Treinamento e onboarding incluídos
- [ ] Suporte para migração de solução anterior

## 5. Avaliação Estratégica

- [ ] Vendor alinhado com a estratégia de AI da organização
- [ ] Posição no mercado sólida (Gartner, Forrester, etc.)
- [ ] Saúde financeira do vendor verificada
- [ ] Base de clientes referenciável (especialmente no setor)
- [ ] Histórico de inovação e investimento em P&D
- [ ] Risco de lock-in avaliado e mitigado
- [ ] Plano de exit strategy definido
- [ ] Compatibilidade com arquitetura multi-vendor
- [ ] Capacidade de escalar com o crescimento da empresa
- [ ] Alinhamento cultural e de valores

## 6. Proof of Concept (PoC)

- [ ] Escopo do PoC definido com métricas de sucesso claras
- [ ] Dados representativos preparados para o PoC
- [ ] Duração do PoC definida (recomendado: 2-4 semanas)
- [ ] Time dedicado ao PoC alocado
- [ ] Critérios de Go/No-Go definidos antes do início
- [ ] Ambiente de teste isolado configurado
- [ ] Métricas de performance coletadas durante o PoC
- [ ] Comparação com baseline documentada
- [ ] Feedback de usuários finais coletado
- [ ] Relatório final do PoC com recomendação

## 7. Due Diligence Final

- [ ] Referências de clientes existentes contactadas (mín. 3)
- [ ] Reviews públicos analisados (G2, Gartner Peer Insights)
- [ ] Análise de risco do vendor documentada
- [ ] Aprovação do CISO/time de segurança obtida
- [ ] Aprovação do time jurídico obtida
- [ ] Aprovação do CFO/Finance obtida
- [ ] Business case final documentado com ROI projetado
- [ ] Plano de implementação acordado com o vendor

---

## Scorecard de Avaliação

| Dimensão | Peso | Nota (1-5) | Score |
|----------|------|-----------|-------|
| Capacidade técnica | 30% | __ | __ |
| Segurança e compliance | 20% | __ | __ |
| Custo-benefício | 20% | __ | __ |
| Suporte e parceria | 15% | __ | __ |
| Alinhamento estratégico | 15% | __ | __ |
| **Total** | **100%** | | **__** |

> Score mínimo recomendado para aprovação: **3.5 / 5.0**

---

*Última atualização: Março 2026*
*Responsável: CAIO Architect / CIO Engineer*
