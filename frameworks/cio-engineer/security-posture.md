# Postura de Segurança — Framework de Cybersecurity para Empresas de Tecnologia

## Propósito e Contexto

Postura de segurança é a capacidade geral da organização de prevenir, detectar e responder a
ameaças cibernéticas. Não é uma checklist — é um sistema vivo que evolui com as ameaças e com
o crescimento da empresa. Em empresas de tecnologia, onde o produto é software e os dados são
o ativo mais valioso, segurança não é um departamento — é uma propriedade do sistema inteiro.

Este framework estrutura a postura de segurança em camadas (defense in depth), com foco
pragmático: não é para transformar a empresa em um bunker, é para proteger o que importa sem
paralisar a agilidade. O lema é "secure by default, not secure by friction".

## Quando Usar

- Na construção ou revisão da estratégia de segurança anual
- Na preparação para certificações (SOC2, ISO 27001, PCI-DSS)
- Após incidentes de segurança (para remediar gaps)
- Em due diligence de investidores ou clientes enterprise
- Ao avaliar riscos de novos produtos ou features
- No onboarding de CISOs ou security leads

## Componentes do Framework

### 1. Defense in Depth (Camadas de Proteção)

**Camada 1: Identidade e Acesso**
- Single Sign-On (SSO) para todos os serviços
- Multi-Factor Authentication (MFA) obrigatório
- Least privilege como default
- Access reviews trimestrais
- Just-in-time access para operações sensíveis

**Camada 2: Endpoint**
- MDM (Mobile Device Management) em todos os dispositivos corporativos
- Disk encryption obrigatório
- EDR (Endpoint Detection and Response) em endpoints
- Patch management automatizado
- BYOD policy definida e comunicada

**Camada 3: Rede**
- Zero trust network (nunca confiar, sempre verificar)
- Segmentação de rede (produção isolada de corporate)
- VPN ou ZTNA para acesso a recursos internos
- DNS filtering e web proxy
- DDoS protection em serviços públicos

**Camada 4: Aplicação**
- SAST (Static Analysis) no CI/CD
- DAST (Dynamic Analysis) em ambientes de staging
- Dependency scanning (Snyk, Dependabot)
- Secret scanning (evitar credentials em código)
- WAF (Web Application Firewall) em serviços públicos
- Referência: `frameworks/cto-architect/engineering-excellence.md`

**Camada 5: Dados**
- Encryption at rest e in transit
- Data classification (público, interno, confidencial, restrito)
- Data Loss Prevention (DLP) para dados sensíveis
- Backup e disaster recovery testados
- Data retention policy implementada

**Camada 6: Monitoramento e Resposta**
- SIEM ou log aggregation centralizado
- Alertas para eventos de segurança críticos
- Incident response plan documentado e praticado
- Threat intelligence feeds relevantes
- Security on-call rotation

### 2. Modelo de Maturidade de Segurança

**Nível 1: Básico** (mínimo para operar)
- SSO + MFA implementados
- Disk encryption em endpoints
- Secret scanning no CI/CD
- Backup básico funcionando
- Incident response plan existente (mesmo que simples)

**Nível 2: Estruturado** (necessário para clientes enterprise)
- Access reviews regulares
- Vulnerability scanning automatizado
- Security training para toda a empresa
- Pen testing anual
- Logging centralizado

**Nível 3: Gerenciado** (necessário para certificações)
- SOC2 Type II ou ISO 27001
- SIEM com detecção de anomalias
- Threat modeling para features críticas
- Bug bounty ou VDP (Vulnerability Disclosure Program)
- Disaster recovery testado semestralmente

**Nível 4: Otimizado** (best-in-class)
- Security champions em cada time de engenharia
- Purple team exercises regulares
- Zero trust fully implemented
- Automated compliance monitoring
- Security como enabler, não blocker

### 3. Risk Assessment Simplificado

Para cada ativo ou processo, avalie:

| Dimensão | Score (1-5) |
|----------|-------------|
| Valor do ativo (dados, sistema, reputação) | ___ |
| Exposição (acessível da internet? por quantas pessoas?) | ___ |
| Probabilidade de ataque (baseado em threat intelligence) | ___ |
| Impacto se comprometido (financeiro, legal, reputacional) | ___ |
| Controles existentes (quão protegido está hoje?) | ___ (inverso) |

Risk Score = (Valor × Exposição × Probabilidade × Impacto) / Controles

## Processo Passo-a-Passo

### Fase 1: Assessment (2-3 semanas)
1. Inventário de ativos (sistemas, dados, acessos)
2. Avaliar maturidade atual no modelo de 4 níveis
3. Risk assessment dos ativos mais críticos
4. Gap analysis vs. framework de compliance alvo (SOC2, ISO)

### Fase 2: Priorização (1 semana)
1. Classificar gaps por risk score
2. Definir quick wins (alto impacto, baixo esforço)
3. Roadmap de 12 meses com milestones trimestrais
4. Budget e headcount necessários

### Fase 3: Implementação por Waves
**Wave 1 (mês 1-3): Fundação**
- SSO + MFA universal
- Secret scanning e dependency scanning
- Incident response plan documentado
- Security awareness training básico

**Wave 2 (mês 4-6): Proteção**
- MDM e endpoint protection
- Logging centralizado
- Vulnerability management program
- Access reviews implementadas

**Wave 3 (mês 7-12): Detecção e Resposta**
- SIEM ou detecção automatizada
- Pen testing e threat modeling
- Disaster recovery testado
- Preparação para certificação

### Fase 4: Operação Contínua
1. Vulnerability scanning semanal
2. Access reviews trimestrais
3. Pen testing anual
4. Security awareness training contínuo
5. Incident response drills semestrais

## Checklist de Postura de Segurança

- [ ] SSO + MFA implementados para todos os serviços?
- [ ] Secrets scanning ativo no CI/CD?
- [ ] Dependency scanning com alertas automáticos?
- [ ] Backup testado nos últimos 30 dias?
- [ ] Incident response plan documentado e comunicado?
- [ ] Access review realizada nos últimos 90 dias?
- [ ] Security training realizado nos últimos 12 meses?
- [ ] Pen test realizado nos últimos 12 meses?
- [ ] Disk encryption ativo em todos os endpoints?
- [ ] Logging centralizado para serviços críticos?

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| MFA coverage | 100% dos usuários | Contínuo |
| Mean time to patch (critical vulns) | < 48 horas | Por vulnerabilidade |
| Security training completion | > 95% dos colaboradores | Anual |
| Pen test findings (critical/high) | 0 críticos, trend decrescente | Anual |
| Incident response time | < 1 hora para SEV1 | Por incidente |
| Access review completion | 100% no prazo | Trimestral |
| Security maturity level | Subir 1 nível por ano | Anual |

## Referências Cruzadas

- `frameworks/cio-engineer/it-service-management.md` — Gestão de incidentes de segurança
- `frameworks/cio-engineer/cloud-strategy.md` — Segurança em ambiente cloud
- `frameworks/cio-engineer/data-platform.md` — Segurança de dados
- `frameworks/cto-architect/engineering-excellence.md` — Security como pilar de engenharia
- `frameworks/caio-architect/responsible-ai.md` — Segurança em sistemas de AI
- `frameworks/shared/risk-management.md` — Cybersecurity no framework de risco
- `frameworks/shared/crisis-management.md` — Resposta a crises de segurança
