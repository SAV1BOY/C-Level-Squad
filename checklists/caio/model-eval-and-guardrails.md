# Model Eval and Guardrails

## Propósito
Garantir que modelos de AI em produção ou em preparação para produção passam por avaliação rigorosa (evals), red teaming e possuem guardrails de safety e compliance adequados. Modelos sem guardrails são bombas-relógio — podem gerar outputs perigosos, enviesados ou não-conformes que causam dano real a usuários e à reputação da empresa.

## Quando Aplicar
- Antes de qualquer modelo ir para produção (gate obrigatório)
- Mensalmente para modelos já em produção (revisão contínua)
- Quando inputs/dados de treinamento mudarem significativamente
- Quando novos riscos forem identificados (bias, segurança, compliance)
- Quando regulamentações de AI mudarem ou novas leis entrarem em vigor

## Agente Responsável
**Agente CAIO (Chief AI Officer Agent)** — responsável por garantir que todos os modelos de AI operam dentro de padrões de qualidade, segurança e compliance.

## Checklist

### Seção 1: Evaluation Framework (Evals)
- [ ] Framework de avaliação está definido e documentado para cada tipo de modelo
- [ ] Eval datasets são representativos do uso real e incluem edge cases
- [ ] Métricas de avaliação são definidas: accuracy, precision, recall, F1, custom metrics
- [ ] Baseline performance está estabelecido para comparação
- [ ] Evals são automatizados e rodam em CI/CD pipeline
- [ ] Evals cobrem funcionalidade (o modelo faz o que deveria) e robustez (mantém performance sob stress)
- [ ] Resultados de evals são documentados e versionados com cada release do modelo
- [ ] Degradação de performance trigger review automático antes de deploy

### Seção 2: Red Teaming
- [ ] Red teaming é realizado antes de todo modelo voltado para usuários
- [ ] Red team inclui: técnicos, não-técnicos, e idealmente especialistas em segurança
- [ ] Cenários de adversarial testing estão definidos e documentados
- [ ] Prompt injection e jailbreak attempts são testados sistematicamente
- [ ] Outputs tóxicos, enviesados ou inapropriados são testados
- [ ] Hallucination rate é medida e está dentro do threshold aceitável
- [ ] Findings de red teaming são documentados com severity e plano de mitigação
- [ ] Red teaming é repetido periodicamente (não apenas uma vez)

### Seção 3: Safety Guardrails
- [ ] Input validation filtra prompts maliciosos ou fora do escopo
- [ ] Output filtering previne conteúdo tóxico, enviesado ou perigoso
- [ ] Content moderation está implementada para interações com usuários
- [ ] O modelo sabe dizer "não sei" ou "não posso responder" quando apropriado
- [ ] Limites de uso estão implementados (rate limiting, session limits)
- [ ] Human-in-the-loop está implementado para decisões de alto impacto
- [ ] Fallback behavior está definido para quando o modelo falha
- [ ] Guardrails são testados como parte do eval pipeline

### Seção 4: Compliance e Governança
- [ ] Dados de treinamento são audíveis e compliance com LGPD
- [ ] PII não é exposta em outputs do modelo sem autorização
- [ ] Modelo não toma decisões automatizadas que violem regulamentações
- [ ] Transparency: usuários sabem que estão interagindo com AI
- [ ] Explicabilidade: decisões do modelo podem ser justificadas quando necessário
- [ ] Audit trail de inputs e outputs é mantido para modelos de alto risco
- [ ] Consentimento de uso de dados para AI está coberto pela política de privacidade
- [ ] Compliance com regulamentações de AI emergentes (EU AI Act, etc.) é monitorada

### Seção 5: Monitoramento Pós-Deploy
- [ ] Performance do modelo em produção é monitorada continuamente
- [ ] Data drift é detectado e alertas disparam quando significativo
- [ ] Model drift é monitorado (performance degradando ao longo do tempo)
- [ ] Feedback de usuários sobre qualidade dos outputs é coletado
- [ ] Incidentes de AI (outputs problemáticos) são rastreados e investigados
- [ ] Processo de rollback rápido existe para casos de falha crítica
- [ ] Modelo é re-treinado ou ajustado com frequência definida
- [ ] Métricas de qualidade de AI são reportadas ao CAIO e C-Level

## Critérios de Aprovação
- Eval framework implementado e rodando para 100% dos modelos em produção
- Red teaming realizado para modelos voltados a usuários
- Safety guardrails implementados e testados (input validation, output filtering)
- Compliance com LGPD verificada para todos os modelos que processam dados pessoais
- Pelo menos 85% dos itens de todas as seções concluídos
- Zero incidentes graves de AI sem post-mortem e remediação

## O que Fazer se Falhar
1. Para modelos sem evals: criar eval suite mínima em 1 semana antes de continuar
2. Para red teaming ausente: realizar sessão de red teaming em 2 semanas
3. Para guardrails ausentes: implementar input/output filtering como prioridade máxima
4. Para compliance gaps: engajar jurídico e DPO para avaliação imediata
5. Considerar pausar modelo em produção se riscos críticos forem identificados
6. Implementar monitoring básico se não existir (logs de inputs/outputs no mínimo)
7. Criar responsible AI policy se não existir
8. Re-auditar em 30 dias com foco nos modelos de maior risco

## Referências
- "Responsible AI" frameworks (Microsoft, Google, Anthropic)
- NIST AI Risk Management Framework
- EU AI Act (referência para regulamentação futura)
- OWASP Top 10 for LLM Applications
- Eval framework documentation (internal)
- Red teaming playbook (internal)
- LGPD e AI guidance (ANPD)
