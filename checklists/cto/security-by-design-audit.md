# Security by Design Audit

## Propósito
Garantir que segurança está integrada no design e no ciclo de desenvolvimento (SDLC), não adicionada como afterthought. Inclui threat modeling, gates de segurança no pipeline e práticas de AppSec. Segurança retroativa é 10x mais cara e 100x menos eficaz que segurança by design.

## Quando Aplicar
- Trimestralmente como revisão de postura de segurança
- Antes de lançar novos serviços ou features que processam dados sensíveis
- Após qualquer incidente de segurança ou vulnerabilidade crítica descoberta
- Quando novos requisitos regulatórios afetarem a organização (LGPD, SOC2, etc.)
- Quando a superfície de ataque mudar significativamente (novas integrações, APIs)

## Agente Responsável
**Agente CTO (Chief Technology Officer Agent)** — responsável por garantir que segurança é um princípio de design, não uma camada adicional.

## Checklist

### Seção 1: Threat Modeling
- [ ] Threat model existe para todos os serviços que processam dados sensíveis
- [ ] Threat model é atualizado quando a arquitetura muda
- [ ] Metodologia de threat modeling está definida (STRIDE, PASTA, ou equivalente)
- [ ] Assets críticos estão identificados e classificados por sensibilidade
- [ ] Attack vectors conhecidos estão documentados com mitigação
- [ ] Threat model inclui ameaças internas (insider threat)
- [ ] Resultados de threat modeling alimentam backlog de segurança
- [ ] Novos serviços passam por threat model antes de ir para produção

### Seção 2: Secure SDLC
- [ ] Security requirements são definidos junto com functional requirements
- [ ] Secure coding guidelines existem e são acessíveis a todos os desenvolvedores
- [ ] SAST (Static Application Security Testing) roda automaticamente no CI
- [ ] DAST (Dynamic Application Security Testing) é realizado periodicamente
- [ ] Dependency scanning detecta vulnerabilidades em bibliotecas de terceiros
- [ ] Container/image scanning é realizado antes do deploy
- [ ] Security review é obrigatório para changes que afetam autenticação, autorização ou dados sensíveis
- [ ] Vulnerabilidades encontradas no pipeline bloqueiam o deploy (para severidade alta/crítica)

### Seção 3: AppSec Gates
- [ ] Critérios de segurança para deploy estão definidos e automatizados
- [ ] Vulnerabilidades críticas têm SLA de correção (ex: 24h para crítica, 7 dias para alta)
- [ ] SLA de correção é cumprido em pelo menos 90% dos casos
- [ ] Vulnerabilidades abertas são rastreadas em dashboard visível
- [ ] Penetration testing é realizado pelo menos anualmente (externo)
- [ ] Bug bounty program ou responsible disclosure policy está ativo
- [ ] Resultados de pen test são corrigidos com prioridade e rastreados
- [ ] Security champions estão designados em cada squad de engenharia

### Seção 4: Identity, Access e Data Protection
- [ ] Autenticação multi-fator (MFA) é obrigatória para sistemas críticos
- [ ] Princípio de least privilege é aplicado em IAM policies
- [ ] Access reviews são realizados trimestralmente
- [ ] Dados sensíveis são criptografados at rest e in transit
- [ ] PII (Personally Identifiable Information) é tratada conforme LGPD
- [ ] Data classification está implementada (público, interno, confidencial, restrito)
- [ ] Logs de acesso a dados sensíveis são mantidos e auditáveis
- [ ] API keys e secrets são geridos via vault (nunca hardcoded)

### Seção 5: Cultura e Capacitação em Segurança
- [ ] Treinamento de segurança é obrigatório para todos os desenvolvedores (anual)
- [ ] Awareness de segurança é mantido com comunicações regulares
- [ ] Incidentes de segurança são tratados como aprendizado (sem blame culture)
- [ ] O time de segurança é visto como enabler, não como bloqueador
- [ ] Engenheiros sabem como reportar vulnerabilidades internamente
- [ ] Security postmortem é realizado após incidentes com ações corretivas
- [ ] Investimento em segurança é proporcional ao risco e ao estágio da empresa
- [ ] Métricas de segurança são reportadas ao C-Level regularmente

## Critérios de Aprovação
- Threat model atualizado para 100% dos serviços que processam dados sensíveis
- SAST e dependency scanning integrados no CI/CD e rodando em 100% dos repos
- Zero vulnerabilidades críticas abertas por mais de 24 horas
- Pen test realizado nos últimos 12 meses com findings corrigidos
- Pelo menos 85% dos itens de todas as seções concluídos
- 100% dos desenvolvedores com treinamento de segurança atualizado

## O que Fazer se Falhar
1. Priorizar por risco: vulnerabilidades críticas primeiro, compliance segundo
2. Se threat model não existe: realizar para os 3 serviços mais críticos em 2 semanas
3. Se SDLC não tem security gates: implementar SAST e dependency scanning primeiro
4. Se vulnerabilidades estão abertas: criar war room para correção das críticas
5. Contratar ou consultar AppSec specialist se não houver expertise interna
6. Implementar security champions program se não existir
7. Criar plano de 90 dias para atingir baseline de segurança
8. Re-auditar em 30 dias com foco nas vulnerabilidades e gaps mais críticos

## Referências
- OWASP Top 10 e OWASP ASVS
- NIST Cybersecurity Framework
- "Threat Modeling" — Adam Shostack
- LGPD compliance requirements
- SOC 2 Type II controls
- Security metrics dashboard (internal)
- Pen test reports (confidential — internal)
