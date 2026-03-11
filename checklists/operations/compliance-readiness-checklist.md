# Checklist de Prontidão para Compliance

## Objetivo
Garantir que a organização esteja preparada para atender requisitos regulatórios, auditorias e certificações, mantendo compliance contínuo.

---

## 1. Fundação de Compliance

### Governança
- [ ] Definir compliance officer ou responsável pela função
- [ ] Estabelecer comitê de compliance com representantes das áreas
- [ ] Criar política de compliance aprovada pela diretoria
- [ ] Definir código de conduta e ética da empresa
- [ ] Implementar canal de denúncias confidencial
- [ ] Agendar reuniões trimestrais do comitê de compliance
- [ ] Reportar status de compliance ao board periodicamente

### Mapeamento Regulatório
- [ ] Identificar todas as regulamentações aplicáveis ao negócio
- [ ] LGPD (Lei Geral de Proteção de Dados)
- [ ] Marco Civil da Internet
- [ ] SOC 2 Type II (se atende clientes enterprise)
- [ ] PCI-DSS (se processa dados de cartão de crédito)
- [ ] ISO 27001 (segurança da informação)
- [ ] Regulamentações setoriais específicas (BACEN, ANVISA, etc.)
- [ ] Documentar gap analysis entre estado atual e requisitos
- [ ] Priorizar gaps por risco e impacto no negócio

---

## 2. Proteção de Dados (LGPD)

### Documentação
- [ ] Manter registro de atividades de tratamento de dados (ROPA)
- [ ] Documentar bases legais para cada tratamento de dados
- [ ] Criar e publicar política de privacidade atualizada
- [ ] Estabelecer política interna de proteção de dados
- [ ] Nomear DPO (Data Protection Officer) ou encarregado
- [ ] Publicar canal de contato do DPO para titulares

### Processos
- [ ] Implementar processo de atendimento a direitos dos titulares
  - Direito de acesso, correção, eliminação, portabilidade
  - SLA de resposta dentro do prazo legal (15 dias)
- [ ] Estabelecer processo de DPIA (Data Protection Impact Assessment)
- [ ] Implementar privacy by design em novos projetos
- [ ] Definir processo de gestão de consentimento
- [ ] Criar processo de notificação de incidentes de dados
- [ ] Revisar contratos com fornecedores para cláusulas de dados

### Técnico
- [ ] Implementar criptografia de dados em trânsito e repouso
- [ ] Configurar controles de acesso baseados em papel (RBAC)
- [ ] Implementar anonimização ou pseudonimização onde necessário
- [ ] Configurar logging de acesso a dados pessoais
- [ ] Implementar retenção e expurgo automático de dados
- [ ] Testar processo de eliminação de dados (right to delete)

---

## 3. Segurança da Informação

### Políticas
- [ ] Política de segurança da informação aprovada
- [ ] Política de classificação de informações
- [ ] Política de uso aceitável de recursos de TI
- [ ] Política de gestão de senhas e autenticação
- [ ] Política de trabalho remoto e BYOD
- [ ] Política de gestão de incidentes de segurança
- [ ] Política de continuidade de negócios

### Controles Técnicos
- [ ] MFA habilitado para todos os acessos críticos
- [ ] Gestão centralizada de identidades (SSO/IAM)
- [ ] Firewall e segmentação de rede configurados
- [ ] Antivírus e EDR em todos os endpoints
- [ ] Patching automatizado com SLA definido
- [ ] Backup com teste de restore periódico
- [ ] WAF para aplicações web expostas
- [ ] DLP implementado para dados sensíveis

### Processos de Segurança
- [ ] Vulnerability scanning periódico (semanal/mensal)
- [ ] Penetration testing anual por empresa externa
- [ ] Revisão de acessos trimestral (user access review)
- [ ] Gestão de mudanças com aprovação documentada
- [ ] Gestão de terceiros com avaliação de risco
- [ ] Treinamento de security awareness para todos os colaboradores
- [ ] Simulação de phishing periódica

---

## 4. SOC 2 (se aplicável)

### Trust Service Criteria
- [ ] **Segurança**: Controles de proteção contra acesso não autorizado
- [ ] **Disponibilidade**: Controles para garantir uptime conforme SLA
- [ ] **Integridade de processamento**: Controles de acurácia e completude
- [ ] **Confidencialidade**: Controles de proteção de informações confidenciais
- [ ] **Privacidade**: Controles de gestão de dados pessoais

### Preparação para Auditoria
- [ ] Selecionar auditor credenciado (CPA firm)
- [ ] Definir escopo: quais sistemas e processos serão auditados
- [ ] Implementar controles mínimos para cada critério
- [ ] Coletar evidências por pelo menos 3-6 meses (Type II)
- [ ] Realizar readiness assessment antes da auditoria formal
- [ ] Designar ponto focal interno para a auditoria
- [ ] Preparar documentação e evidências organizadas

---

## 5. Treinamento e Cultura

### Programas de Treinamento
- [ ] Treinamento de compliance obrigatório para todos (anual)
- [ ] Treinamento de LGPD para equipes que tratam dados pessoais
- [ ] Treinamento de segurança da informação para toda empresa
- [ ] Treinamento anticorrupção para áreas de risco (vendas, compras)
- [ ] Treinamento específico por papel (developers, RH, finance)
- [ ] Registro de participação e certificados de conclusão

### Cultura de Compliance
- [ ] Comunicação regular sobre importância de compliance
- [ ] Reconhecimento de boas práticas de compliance
- [ ] Tolerância zero para violações intencionais
- [ ] Proteção contra retaliação para denunciantes
- [ ] Liderança pelo exemplo (tone from the top)

---

## 6. Monitoramento e Melhoria Contínua

### Monitoramento
- [ ] Dashboard de compliance com indicadores-chave
- [ ] Auditoria interna pelo menos anual
- [ ] Monitoramento contínuo de controles automatizados
- [ ] Revisão de incidentes e quase-incidentes
- [ ] Tracking de mudanças regulatórias que impactam a empresa
- [ ] Revisão periódica de políticas (anual no mínimo)

### Métricas
- [ ] Percentual de colaboradores treinados em compliance
- [ ] Número de incidentes de compliance por período
- [ ] Tempo médio de resposta a solicitações de titulares
- [ ] Número de vulnerabilidades abertas por severidade
- [ ] Percentual de controles operacionais e efetivos
- [ ] Status de remediação de findings de auditoria
