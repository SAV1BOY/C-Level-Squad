# Template: Relatório de Incidente

## Propósito
Este template documenta incidentes de qualquer natureza (técnicos, de segurança, operacionais, regulatórios) de forma estruturada para registro, análise e compliance. Diferente do postmortem (focado em aprendizado técnico), o relatório de incidente é o documento formal para stakeholders, reguladores e auditores.

## Instruções de Uso
1. Inicie o preenchimento durante o incidente (timeline em tempo real)
2. Complete em até 72h após resolução
3. Revisão de jurídico obrigatória para incidentes de segurança/dados
4. Armazene com controle de acesso adequado à classificação

---

## Classificação e Metadados

| Campo | Valor |
|-------|-------|
| **ID do Incidente** | [INC-AAAA-NNN] |
| **Classificação** | [Confidencial / Interno / Público] |
| **Tipo** | [Técnico / Segurança / Dados / Operacional / Financeiro / Regulatório] |
| **Severidade** | [Crítica / Alta / Média / Baixa] |
| **Data/Hora de Início** | [DD/MM/AAAA HH:MM UTC-3] |
| **Data/Hora de Resolução** | [DD/MM/AAAA HH:MM UTC-3] |
| **Duração Total** | [Xh Ymin] |
| **Autor do Relatório** | [Nome — Cargo] |
| **Data do Relatório** | [DD/MM/AAAA] |
| **Aprovador** | [Nome — Cargo] |

---

## 1. Resumo Executivo

[3-5 frases descrevendo: o que aconteceu, quem foi afetado, qual foi o impacto, como foi resolvido e status atual.]

---

## 2. Cronologia Detalhada

| Data/Hora | Evento | Fonte | Responsável |
|-----------|--------|-------|-------------|
| [DD/MM HH:MM] | [Evento que iniciou o incidente] | [Alerta/Ticket/Observação] | [Sistema/Pessoa] |
| [DD/MM HH:MM] | [Detecção do incidente] | [Como foi detectado] | [Quem detectou] |
| [DD/MM HH:MM] | [Incidente declarado formalmente] | [Canal] | [Quem declarou] |
| [DD/MM HH:MM] | [Primeira ação de resposta] | [Ação tomada] | [Quem executou] |
| [DD/MM HH:MM] | [Escalonamento] | [Para quem e por quê] | [Quem escalou] |
| [DD/MM HH:MM] | [Identificação da causa] | [Como foi encontrada] | [Quem identificou] |
| [DD/MM HH:MM] | [Ação de resolução] | [O que foi feito] | [Quem resolveu] |
| [DD/MM HH:MM] | [Confirmação de resolução] | [Como validamos] | [Quem validou] |
| [DD/MM HH:MM] | [Incidente encerrado] | [Comunicação final] | [Quem encerrou] |

---

## 3. Impacto

### 3.1 Impacto em Clientes
| Dimensão | Detalhes |
|----------|---------|
| Clientes diretamente afetados | [N clientes / X% da base] |
| Funcionalidades impactadas | [Lista de features/serviços] |
| Duração do impacto para clientes | [Xh Ymin] |
| Perda de dados | [Sim: descrever / Não] |
| SLA violado | [Sim: qual SLA e quanto / Não] |

### 3.2 Impacto Financeiro
| Item | Valor Estimado |
|------|---------------|
| Receita perdida diretamente | [R$ X] |
| Créditos/compensações concedidos | [R$ X] |
| Penalidades de SLA | [R$ X] |
| Custo de resposta (horas extras, consultoria) | [R$ X] |
| **Impacto financeiro total estimado** | **[R$ X]** |

### 3.3 Impacto Reputacional
- Cobertura de mídia: [Sim/Não — listar se aplicável]
- Menções em redes sociais: [Volume e sentimento]
- Reclamações formais: [N — canais]
- Impacto em NPS/CSAT: [Estimado]

### 3.4 Impacto Regulatório
- Notificação obrigatória: [Sim — órgão e prazo / Não]
- LGPD/GDPR aplicável: [Sim — detalhes / Não]
- Status da notificação: [Enviada / Pendente / N/A]

---

## 4. Análise de Causa

### 4.1 Causa Raiz
[Descrição técnica detalhada da causa raiz]

### 4.2 Fatores Contribuintes
1. [Fator 1 — ex: "Falta de monitoramento na camada X"]
2. [Fator 2 — ex: "Processo de deploy sem gate de qualidade"]
3. [Fator 3 — ex: "Documentação desatualizada"]

### 4.3 Categorização
- **Categoria primária:** [Erro humano / Bug de software / Falha de infra / Ataque externo / Falha de processo / Terceiro]
- **Subcategoria:** [Detalhar]
- **Prevenível:** [Sim / Parcialmente / Não]

---

## 5. Resposta e Resolução

### 5.1 Ações de Contenção (durante o incidente)
| Ação | Resultado | Executado por |
|------|----------|--------------|
| [Ação 1] | [Efetivo / Parcial / Ineficaz] | [Nome] |
| [Ação 2] | [Resultado] | [Nome] |

### 5.2 Ação de Resolução Definitiva
[Descrever o que foi feito para resolver completamente o incidente]

### 5.3 Comunicações Realizadas
| Stakeholder | Canal | Data/Hora | Conteúdo |
|------------|-------|-----------|----------|
| [Clientes] | [E-mail] | [DD/MM HH:MM] | [Resumo do que foi comunicado] |
| [Interno] | [Slack] | [DD/MM HH:MM] | [Resumo] |
| [Board] | [E-mail] | [DD/MM HH:MM] | [Resumo] |
| [Regulador] | [Ofício] | [DD/MM HH:MM] | [Resumo] |

---

## 6. Ações Corretivas e Preventivas

| # | Ação | Tipo | Prioridade | Owner | Prazo | Status |
|---|------|------|-----------|-------|-------|--------|
| 1 | [Ação] | [Corretiva/Preventiva] | [P0/P1/P2] | [Nome] | [Data] | [Pendente/Concluído] |
| 2 | [Ação] | [Tipo] | [Prioridade] | [Nome] | [Data] | [Status] |
| 3 | [Ação] | [Tipo] | [Prioridade] | [Nome] | [Data] | [Status] |
| 4 | [Ação] | [Tipo] | [Prioridade] | [Nome] | [Data] | [Status] |

---

## 7. Lições Aprendidas

1. [Lição 1 — o que funciona e deve ser mantido/replicado]
2. [Lição 2 — o que precisa ser mudado em processos]
3. [Lição 3 — investimento técnico necessário]

---

## 8. Aprovações e Distribuição

| Papel | Nome | Data | Aprovação |
|-------|------|------|-----------|
| Autor | [Nome] | [Data] | Elaborado |
| Gestor da área | [Nome] | [Data] | Revisado |
| Jurídico | [Nome] | [Data] | Revisado |
| CISO (se segurança) | [Nome] | [Data] | Revisado |
| DPO (se dados pessoais) | [Nome] | [Data] | Revisado |

**Lista de distribuição:** [Quem recebe cópia deste relatório]

---

## Exemplo Preenchido (Resumo)

> **INC-2026-015:** Indisponibilidade de 4h no módulo de pagamentos
> **Severidade:** Crítica | **Clientes afetados:** 8.200 (35% da base)
> **Causa raiz:** Certificado SSL expirado no gateway de pagamento externo
> **Impacto financeiro:** R$ 95K (receita perdida) + R$ 20K (créditos)
> **Ações:** 4 corretivas — automação de renovação de certificados (P0), alerta de expiração (P0)

---

## Dicas de Uso
- Comece a documentar DURANTE o incidente — memória é perecível
- Fatos primeiro, análise depois — não especule no relatório
- Para incidentes de segurança/dados: jurídico revisa ANTES de qualquer distribuição
- Mantenha versão interna (detalhada) e externa (resumida) se necessário
- Incidentes sem ações corretivas vão se repetir — garanta follow-through
- Arquivo permanente — relatórios de incidente são documentos de compliance
