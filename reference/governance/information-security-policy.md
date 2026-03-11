# Information Security Policy — Template Executivo

## Visão Geral

Este documento serve como template para uma política de segurança da informação
adaptável a empresas de médio porte. Deve ser personalizado conforme o contexto,
tamanho e maturidade da organização.

Uma política de segurança não é um documento para engavetar. É o contrato social
da empresa sobre como proteger seus ativos de informação.

---

## 1. Objetivo e Escopo

### Objetivo
Estabelecer diretrizes, responsabilidades e controles para proteger os ativos de
informação da [EMPRESA] contra ameaças internas e externas, garantindo
confidencialidade, integridade e disponibilidade.

### Escopo
Esta política aplica-se a:
- Todos os colaboradores (CLT, PJ, estagiários, temporários)
- Terceiros com acesso a sistemas ou dados da empresa
- Todos os ativos de informação (digitais e físicos)
- Todos os ambientes (escritório, remoto, cloud, mobile)

### Definições
- **Ativos de Informação**: dados, sistemas, infraestrutura, documentos, código-fonte
- **Informação Confidencial**: qualquer dado não destinado ao público
- **Incidente de Segurança**: evento que compromete ou ameaça a segurança da informação
- **Owner de Dados**: responsável pela classificação e autorização de acesso a um conjunto de dados

---

## 2. Classificação de Dados

### Níveis de Classificação

**Público**
- Informação destinada ao público geral
- Exemplo: site institucional, blog posts, material de marketing
- Controles: nenhum controle especial de acesso

**Interno**
- Informação de uso geral dentro da empresa
- Exemplo: comunicados internos, políticas, organograma
- Controles: acesso restrito a colaboradores ativos

**Confidencial**
- Informação sensível ao negócio
- Exemplo: dados financeiros, planos estratégicos, dados de clientes, código-fonte
- Controles: acesso restrito por need-to-know, criptografia em trânsito e repouso

**Restrito**
- Informação altamente sensível com impacto crítico se exposta
- Exemplo: credenciais de produção, dados de cartão, informações de M&A, dados sensíveis LGPD
- Controles: acesso mínimo, criptografia obrigatória, audit log, aprovação explícita

### Responsabilidades de Classificação

- Cada área deve classificar seus dados conforme os níveis acima
- O owner de dados é responsável por definir quem tem acesso
- Dados não classificados devem ser tratados como Confidenciais por padrão
- Reclassificação deve ocorrer quando o contexto mudar

---

## 3. Controle de Acesso

### Princípios

- **Least Privilege**: conceder o mínimo de acesso necessário para a função
- **Need-to-Know**: acesso apenas a informações necessárias para o trabalho
- **Separation of Duties**: separar funções críticas para evitar fraude
- **Defense in Depth**: múltiplas camadas de proteção

### Autenticação

- Senhas devem ter mínimo de 12 caracteres com complexidade
- MFA (Multi-Factor Authentication) obrigatório para:
  - Todos os sistemas corporativos (email, Slack, cloud)
  - Acesso a ambientes de produção
  - VPN e acesso remoto
  - Contas administrativas
- SSO (Single Sign-On) deve ser utilizado sempre que disponível
- Senhas nunca devem ser compartilhadas ou armazenadas em texto puro

### Gestão de Acessos

- Acessos concedidos mediante solicitação formal (ticket ou aprovação documentada)
- Revisão trimestral de acessos por cada owner de sistema
- Revogação imediata em caso de desligamento (offboarding em até 4 horas)
- Contas de serviço devem ter owner definido e credenciais rotacionadas
- Acessos privilegiados (admin) devem ser temporários quando possível (just-in-time)

### Política de Senhas e Credenciais

- Uso obrigatório de password manager corporativo
- Proibido reutilizar senhas entre serviços
- API keys e secrets armazenados em vault (nunca em código ou repositórios)
- Rotação de credenciais de produção a cada 90 dias
- Credenciais comprometidas devem ser rotacionadas imediatamente

---

## 4. Segurança de Endpoints e Rede

### Dispositivos Corporativos

- Criptografia de disco obrigatória (FileVault / BitLocker)
- Antivírus/EDR instalado e atualizado
- Firewall do sistema operacional ativado
- Atualizações de segurança aplicadas em até 7 dias após lançamento
- Bloqueio automático de tela após 5 minutos de inatividade
- MDM (Mobile Device Management) para dispositivos móveis corporativos

### Dispositivos Pessoais (BYOD)

- Acesso a dados corporativos em dispositivos pessoais apenas via soluções containerizadas
- MFA obrigatório
- Capacidade de wipe remoto de dados corporativos
- Requisitos mínimos de segurança (SO atualizado, sem jailbreak/root)

### Rede

- Segregação de redes (corporativa, guest, produção)
- VPN obrigatória para acesso a recursos internos de redes externas
- Monitoramento de tráfego para detecção de anomalias
- Wi-Fi corporativo com WPA3 e autenticação por certificado quando possível

---

## 5. Segurança em Cloud e Desenvolvimento

### Cloud Security

- Ambientes de produção separados de desenvolvimento e staging
- Infrastructure as Code (IaC) para garantir consistência e auditabilidade
- Criptografia em trânsito (TLS 1.2+) e em repouso para todos os dados
- Backups automatizados com teste de restauração mensal
- Monitoramento de configurações (Cloud Security Posture Management)
- Logs centralizados com retenção mínima de 12 meses

### Desenvolvimento Seguro (Secure SDLC)

- Code review obrigatório antes de merge em branches protegidas
- Análise estática de segurança (SAST) no pipeline de CI/CD
- Scan de dependências para vulnerabilidades conhecidas
- Proibido credentials hardcoded em código-fonte
- Testes de segurança em funcionalidades que lidam com dados sensíveis
- Pen testing anual em aplicações críticas

---

## 6. Resposta a Incidentes

### Definição de Incidente

Qualquer evento que comprometa ou ameace a confidencialidade, integridade ou
disponibilidade dos ativos de informação. Exemplos:
- Acesso não autorizado a sistemas ou dados
- Malware ou ransomware
- Vazamento de dados
- Phishing bem-sucedido
- Indisponibilidade de sistemas críticos

### Processo de Resposta

**Fase 1: Detecção e Triagem**
- Identificar e confirmar o incidente
- Classificar severidade (Crítico / Alto / Médio / Baixo)
- Notificar o Security Lead e stakeholders conforme severidade

**Fase 2: Contenção**
- Isolar sistemas afetados
- Preservar evidências (logs, snapshots)
- Implementar medidas temporárias para limitar dano

**Fase 3: Erradicação**
- Identificar causa raiz
- Remover a ameaça completamente
- Corrigir vulnerabilidades exploradas

**Fase 4: Recuperação**
- Restaurar sistemas ao estado normal
- Validar integridade dos dados
- Monitorar de perto por recorrência

**Fase 5: Post-Mortem**
- Documentar timeline completa do incidente
- Análise de causa raiz (blameless)
- Definir e acompanhar ações corretivas
- Compartilhar learnings com a organização

### Notificações Obrigatórias

- ANPD: em caso de incidente envolvendo dados pessoais com risco relevante
- Titulares: quando o incidente puder causar dano significativo
- Parceiros/Clientes: conforme obrigações contratuais
- Reguladores: conforme legislação setorial aplicável

---

## 7. Uso Aceitável

### Regras Gerais

- Recursos de TI da empresa são para uso profissional (uso pessoal limitado e razoável)
- Proibido instalar software não autorizado em dispositivos corporativos
- Proibido compartilhar credenciais de acesso
- Proibido conectar dispositivos pessoais à rede corporativa sem autorização
- Proibido enviar dados confidenciais para email pessoal ou serviços não aprovados
- Proibido desativar controles de segurança (antivírus, firewall, atualizações)

### Email e Comunicação

- Não clicar em links ou anexos suspeitos (reportar ao time de segurança)
- Não enviar informações confidenciais por email sem criptografia
- Verificar destinatários antes de enviar informações sensíveis
- Usar canais oficiais para comunicação de negócios

### Redes Sociais

- Não divulgar informações internas ou confidenciais em redes sociais
- Publicações profissionais que mencionem a empresa devem seguir guidelines de comunicação
- Separar perfis pessoais de profissionais quando possível

---

## 8. Segurança de Fornecedores (Vendor Security)

### Avaliação Pré-Contratação

Para fornecedores que acessarão dados ou sistemas:
- Questionário de segurança antes da contratação
- Avaliação proporcional ao risco (acesso a dados sensíveis = avaliação mais rigorosa)
- Verificar certificações relevantes (SOC 2, ISO 27001)
- Revisão de política de privacidade e termos de serviço

### Requisitos Contratuais

- Cláusulas de proteção de dados e confidencialidade (NDA)
- Cláusulas LGPD (papel de operador, obrigações, responsabilidades)
- Direito de auditoria
- Obrigação de notificação de incidentes
- Cláusula de devolução/destruição de dados ao término do contrato
- SLA de disponibilidade e suporte para serviços críticos

### Monitoramento Contínuo

- Revisão anual de fornecedores críticos
- Monitorar notícias sobre incidentes de segurança em fornecedores
- Reavaliar em caso de mudanças significativas (aquisição, breach público)
- Manter inventário atualizado de todos os fornecedores com acesso a dados

---

## 9. Treinamento e Conscientização

### Programa Obrigatório

- Onboarding: treinamento de segurança na primeira semana
- Anual: reciclagem obrigatória para todos os colaboradores
- Simulações de phishing: trimestrais, com feedback educativo
- Treinamento especializado para times técnicos (dev, infra, dados)

### Tópicos Essenciais

- Reconhecimento de phishing e engenharia social
- Política de senhas e uso de MFA
- Classificação e manuseio de dados
- Reportar incidentes de segurança
- Trabalho remoto seguro
- Uso seguro de IA generativa (cuidado com dados confidenciais em prompts)

---

## 10. Governança e Revisão

### Responsabilidades

- **CEO**: sponsor executivo da política
- **CTO/CISO**: implementação e monitoramento técnico
- **DPO**: conformidade com LGPD
- **Gestores**: garantir que suas equipes conheçam e sigam a política
- **Todos**: cumprir a política e reportar violações

### Revisão e Atualização

- Revisão anual obrigatória da política
- Atualização ad hoc em caso de mudanças significativas (regulatórias, tecnológicas, incidentes)
- Versionamento e registro de alterações
- Comunicação de mudanças a todos os afetados

### Consequências de Violação

Violações desta política podem resultar em:
- Advertência formal
- Suspensão de acesso
- Medidas disciplinares conforme legislação trabalhista
- Rescisão contratual
- Responsabilização civil e criminal quando aplicável

---

## Anexos

- Anexo A: Inventário de ativos de informação
- Anexo B: Matriz de classificação de dados por área
- Anexo C: Lista de fornecedores com acesso a dados
- Anexo D: Plano de resposta a incidentes detalhado
- Anexo E: Checklist de onboarding/offboarding de segurança
