# Estratégia de Cloud — Framework de Infraestrutura e Operações

## Propósito e Contexto

Cloud não é uma decisão binária (on-premise vs. nuvem) — é um espectro de escolhas sobre
onde executar workloads, como gerenciá-los e quanto controle vs. conveniência aceitar. A
estratégia de cloud define essas escolhas de forma coerente, evitando dois extremos comuns:
"lift-and-shift" que apenas move problemas para a nuvem (e adiciona custo), e "cloud-native
a qualquer custo" que gera complexidade desnecessária.

Para empresas de tecnologia brasileiras, a estratégia de cloud precisa considerar fatores
específicos: localização de dados (LGPD), latência para usuários nacionais, disponibilidade
de regiões dos provedores e o ecossistema de talentos local.

## Quando Usar

- Na definição da estratégia de infraestrutura para novos produtos
- Em revisões anuais de custos de infraestrutura (cloud cost optimization)
- Ao avaliar migração de workloads entre provedores ou modelos
- Na preparação para scaling significativo (10x+ em carga)
- Quando custos de cloud crescem mais rápido que a receita
- Em decisões multi-cloud vs. single-cloud

## Componentes do Framework

### 1. Modelo de Decisão por Workload

Classifique cada workload para determinar o deployment model adequado:

| Workload Type | Modelo Recomendado | Justificativa |
|--------------|-------------------|---------------|
| Aplicações web stateless | Container orchestration (K8s) | Escalabilidade, portabilidade |
| APIs e microservices | Managed containers ou serverless | Simplicidade operacional |
| Batch processing / Data pipelines | Managed services + spot | Custo-eficiência |
| Databases | Managed DB services | Redução de ops burden |
| ML training | GPU instances (spot ou preemptible) | Custo, pay-per-use |
| ML inference | Serverless ou dedicated (depende de latência) | Latência vs. custo |
| Static content / CDN | Edge + Object Storage | Performance global |
| Compliance-sensitive | Região dedicada ou private cloud | LGPD, regulação |

### 2. Cloud Operating Model

**FinOps (Financial Operations):**
- Tagging obrigatório para todos os recursos (team, service, environment)
- Budget alerts por team/service
- Reserved instances / savings plans para workloads previsíveis
- Spot instances para workloads tolerantes a interrupção
- Revisão mensal de custos com owners

**DevOps / Platform:**
- Infrastructure as Code (Terraform, Pulumi) para todos os recursos
- GitOps para deployment e configuração
- Environments padronizados (dev, staging, production)
- Self-service para provisioning de recursos comuns
- Referência: `frameworks/cto-architect/platform-strategy.md`

**Security & Compliance:**
- Guardrails automatizados (service control policies, OPA)
- Encryption by default (at rest e in transit)
- Network segmentation (VPCs, security groups)
- Audit logging para todas as ações administrativas
- Compliance as Code (automated checks)
- Referência: `frameworks/cio-engineer/security-posture.md`

### 3. Multi-Cloud Decision Framework

| Fator | Single Cloud | Multi-Cloud |
|-------|-------------|-------------|
| Complexidade operacional | Menor | Significativamente maior |
| Vendor lock-in risk | Maior | Menor |
| Negotiation leverage | Menor | Maior |
| Talent requirements | Especialistas em 1 provider | Generalistas ou equipe maior |
| Disaster recovery | Cross-region | Cross-provider |
| Custo total | Geralmente menor | Geralmente maior |

**Recomendação para maioria das empresas em crescimento:** Single cloud primary + segundo cloud
apenas para workloads específicos (ex: ML em GCP, resto em AWS). Multi-cloud full é justificável
apenas para empresas muito grandes ou com requisitos regulatórios específicos.

### 4. Cloud Cost Model

```
Custo Total de Cloud =
  Compute (VMs, containers, serverless)
  + Storage (object, block, DB)
  + Network (egress, load balancing, CDN)
  + Managed Services (databases, queues, search, AI)
  + Support Plan
  + People (CloudOps team, training)
  - Savings (reserved, spot, committed use)
```

**Benchmark de custo:**
- Cloud cost como % da receita: 5-15% para SaaS (varia muito por tipo)
- Cloud cost per customer: deve ser decrescente com escala
- Cloud cost growth vs. revenue growth: cloud deve crescer mais devagar que receita

## Processo Passo-a-Passo

### Fase 1: Assessment (2 semanas)
1. Inventário de todos os workloads e seus requisitos
2. Análise de custos atuais (por serviço, time, ambiente)
3. Avaliação de skills do time (quais clouds dominam)
4. Requisitos de compliance e localização de dados

### Fase 2: Estratégia (2 semanas)
1. Definir cloud provider primário (se não definido)
2. Classificar workloads no modelo de decisão
3. Definir cloud operating model (FinOps, DevOps, Security)
4. Estabelecer targets de custo e eficiência

### Fase 3: Implementação
1. Infrastructure as Code para todos os novos recursos
2. Tagging strategy implementada
3. Cost monitoring e alertas configurados
4. Guardrails de segurança automatizados
5. Documentação de arquitetura e decisões

### Fase 4: Otimização Contínua
1. Revisão mensal de custos com FinOps
2. Right-sizing trimestral de recursos
3. Reservas e savings plans revisados semestralmente
4. Avaliação de novos serviços gerenciados (pode substituir self-managed)

## Template de Cloud Architecture Decision

```markdown
# Cloud Decision: [Nome do Workload/Serviço]

**Cloud Provider:** [AWS/GCP/Azure]
**Deployment Model:** [Containers/Serverless/VMs/Managed Service]
**Region:** [Região primária] + [DR region]

## Requisitos
- Availability: [SLA target]
- Latência: [p99 target]
- Compliance: [LGPD, SOC2, etc.]
- Scale: [current e projected]

## Arquitetura
[Diagrama simplificado]

## Custo Estimado
- Monthly: R$ [X]
- Per-unit: R$ [Y] por [transação/cliente/request]

## Alternativas Consideradas
[Lista de alternativas e por que foram descartadas]
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Cloud cost / Revenue | Decrescente | Mensal |
| Cloud cost / Customer | Decrescente | Mensal |
| Resource utilization | > 60% para compute | Semanal |
| IaC coverage | 100% dos recursos de produção | Contínuo |
| Tagging compliance | 100% | Semanal |
| Deployment frequency | Tendência crescente | Semanal |
| Availability (SLA compliance) | > 99.9% | Mensal |

## Referências Cruzadas

- `frameworks/cio-engineer/security-posture.md` — Segurança em cloud
- `frameworks/cio-engineer/data-platform.md` — Data platform em cloud
- `frameworks/cio-engineer/digital-transformation.md` — Cloud como enabler
- `frameworks/cto-architect/tech-radar.md` — Cloud services no radar
- `frameworks/cto-architect/platform-strategy.md` — Plataforma sobre cloud
- `frameworks/cfo-strategist/cost-optimization.md` — Cloud cost como alvo de otimização
- `frameworks/caio-architect/mlops-framework.md` — ML infrastructure em cloud
