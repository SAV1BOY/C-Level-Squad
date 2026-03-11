# Formulário de Solicitação de Acesso

## Propósito
Padronizar o processo de solicitação, aprovação e registro de acessos a sistemas,
dados e ambientes, garantindo compliance com políticas de segurança, princípio de
menor privilégio e rastreabilidade completa.

## Quando Usar
- Para qualquer novo acesso a sistemas ou dados
- Para elevação de privilégios em sistemas existentes
- Para acesso temporário (projetos, auditorias, suporte)
- Para revisão periódica de acessos (recertificação)
- Quando um colaborador muda de área ou função

## Agente Responsável
- **Processamento:** CIO/CISO Agent
- **Aprovação nível 1:** Gestor direto do solicitante
- **Aprovação nível 2:** Owner do sistema/dado
- **Execução:** IT Operations
- **Auditoria:** CISO Agent

## Template

---

### SOLICITAÇÃO DE ACESSO

**ID da solicitação:** {{id_solicitacao}}
**Data:** {{data_solicitacao}}
**Status:** {{pendente_aprovado_rejeitado_executado_revogado}}
**Urgência:** {{normal_urgente_emergencial}}

---

#### 1. Informações do Solicitante

| Campo | Valor |
|-------|-------|
| Nome | {{nome_solicitante}} |
| E-mail | {{email_solicitante}} |
| Cargo | {{cargo_solicitante}} |
| Departamento | {{departamento}} |
| Gestor direto | {{nome_gestor}} |
| Data de admissão | {{data_admissao}} |

---

#### 2. Acesso Solicitado

| # | Sistema/Recurso | Tipo de Acesso | Nível de Permissão | Ambiente |
|---|----------------|---------------|-------------------|----------|
| 1 | {{sistema_1}} | {{tipo_acesso_1}} | {{permissao_1}} | {{ambiente_1}} |
| 2 | {{sistema_2}} | {{tipo_acesso_2}} | {{permissao_2}} | {{ambiente_2}} |
| 3 | {{sistema_3}} | {{tipo_acesso_3}} | {{permissao_3}} | {{ambiente_3}} |

**Tipos de acesso:** Leitura | Escrita | Admin | API | Dados sensíveis
**Ambientes:** Produção | Staging | Desenvolvimento | Analytics

---

#### 3. Justificativa

**Por que este acesso é necessário:**
{{justificativa_acesso}}

**Atividades que serão realizadas:**
- {{atividade_1}}
- {{atividade_2}}
- {{atividade_3}}

**Projeto/Iniciativa vinculada:** {{projeto_vinculado}}

---

#### 4. Temporalidade

| Campo | Valor |
|-------|-------|
| Tipo | {{permanente_temporario}} |
| Data de início | {{data_inicio_acesso}} |
| Data de expiração (se temporário) | {{data_expiracao}} |
| Próxima recertificação | {{data_recertificacao}} |

---

#### 5. Classificação de Dados

| Dado/Sistema | Classificação | Contém PII? | Regulação Aplicável |
|-------------|---------------|-------------|-------------------|
| {{dado_1}} | {{classificacao_1}} | {{pii_1}} | {{regulacao_1}} |
| {{dado_2}} | {{classificacao_2}} | {{pii_2}} | {{regulacao_2}} |

**Classificações:** Público | Interno | Confidencial | Restrito

---

#### 6. Avaliação de Risco

| Critério | Avaliação |
|----------|----------|
| Princípio do menor privilégio atendido? | {{sim_nao_1}} |
| Há segregation of duties conflict? | {{sim_nao_2}} |
| O acesso pode ser reduzido e ainda atender? | {{sim_nao_3}} |
| Dados sensíveis estão envolvidos? | {{sim_nao_4}} |
| Necessita treinamento de compliance? | {{sim_nao_5}} |

**Nível de risco:** {{baixo_medio_alto_critico}}

---

#### 7. Fluxo de Aprovação

| Etapa | Aprovador | Status | Data | Comentário |
|-------|----------|--------|------|-----------|
| 1. Gestor direto | {{gestor}} | {{status_1}} | {{data_1}} | {{coment_1}} |
| 2. Owner do sistema | {{owner_sistema}} | {{status_2}} | {{data_2}} | {{coment_2}} |
| 3. Segurança (se risco alto) | {{ciso}} | {{status_3}} | {{data_3}} | {{coment_3}} |
| 4. Compliance (se PII) | {{compliance}} | {{status_4}} | {{data_4}} | {{coment_4}} |

---

#### 8. Execução

| Campo | Valor |
|-------|-------|
| Executado por | {{executado_por}} |
| Data de execução | {{data_execucao}} |
| Credencial criada | {{tipo_credencial}} |
| MFA configurado | {{sim_nao_mfa}} |
| Treinamento completado | {{sim_nao_treinamento}} |

---

#### 9. Registro de Revogação (quando aplicável)

| Campo | Valor |
|-------|-------|
| Data de revogação | {{data_revogacao}} |
| Motivo | {{motivo_revogacao}} |
| Revogado por | {{revogado_por}} |
| Confirmação de revogação | {{confirmado}} |

---

## Instruções de Preenchimento

1. **Menor privilégio:** Solicite apenas o nível de acesso mínimo necessário.
2. **Temporário:** Prefira acessos temporários. Acessos permanentes requerem justificativa mais forte.
3. **PII:** Se envolve dados pessoais, compliance deve aprovar antes da execução.
4. **Urgência:** "Emergencial" requer post-approval dentro de 24h. Não abuse desta classificação.
5. **Recertificação:** Todos os acessos devem ser recertificados a cada 90 dias (ou 180 para baixo risco).
6. **Segregation of Duties:** Verifique se o acesso não cria conflito (ex.: mesmo usuário pode criar E aprovar pagamentos).

## Exemplo Preenchido

---

### SOLICITAÇÃO DE ACESSO — #AR-2026-0342

**Solicitante:** João Silva — Analista de Dados, Equipe de BI
**Urgência:** Normal

#### 2. Acesso Solicitado
| Sistema | Tipo | Permissão | Ambiente |
|---------|------|-----------|----------|
| Data Warehouse (BigQuery) | Leitura | Dataset: sales_analytics | Produção |
| Metabase | Escrita | Workspace: Revenue | Analytics |

#### 3. Justificativa
Necessário para construir dashboards de revenue para o MBR mensal. O projeto "Revenue
Intelligence" requer acesso aos dados de vendas agregados (sem PII de clientes).

#### 4. Temporalidade
- Tipo: Permanente (enquanto na função)
- Recertificação: A cada 90 dias

---

## Checklist de Qualidade

- [ ] Justificativa é clara e vinculada a atividade/projeto específico
- [ ] Nível de acesso segue princípio do menor privilégio
- [ ] Classificação de dados está correta
- [ ] Conflitos de segregation of duties foram verificados
- [ ] Todas as aprovações necessárias foram obtidas
- [ ] MFA está configurado (obrigatório para produção)
- [ ] Data de expiração definida para acessos temporários
- [ ] Recertificação agendada
- [ ] Treinamento de compliance concluído (se necessário)
- [ ] Registro está completo para auditoria
