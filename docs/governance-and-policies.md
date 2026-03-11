# Governance & Policies — Políticas Mínimas e Governance

> Conjunto mínimo de políticas e regras de governance para o C-Level Squad.

---

## Filosofia de Governance

O C-Level Squad adopta governance mínima mas suficiente: poucas regras,
rigorosamente cumpridas. Excesso de regras gera burocracia. Ausência de
regras gera caos. O equilíbrio está em regras essenciais bem desenhadas.

---

## Estrutura de Governance

### Níveis de Governance
```
Nível 1: PRINCÍPIOS — Valores e crenças fundamentais (raramente mudam)
Nível 2: POLÍTICAS — Regras formais de comportamento (mudam anualmente)
Nível 3: PROCESSOS — Como as coisas são feitas (mudam trimestralmente)
Nível 4: GUIDELINES — Orientações flexíveis (mudam conforme necessário)
```

### Quem Governa
| Área | Governance Owner | Aprovação |
|------|-----------------|-----------|
| Estratégia | Vision Chief | Board |
| Operações | COO Orchestrator | Vision Chief |
| Tecnologia | CTO Architect | Vision Chief |
| Dados e Segurança | CIO Engineer | Vision Chief |
| AI | CAIO Architect | Vision Chief + Board |
| Pessoas e Cultura | Vision Chief | Board |
| Financeiro | COO Orchestrator | Vision Chief + Board |
| Marketing e Brand | CMO Architect | Vision Chief |

---

## Políticas Mínimas Obrigatórias

### Política 1 — Decisão e Accountability
- Toda decisão significativa tem um owner registado
- Decisões Type 1 requerem registo completo no decision log
- Accountability é individual: "nós decidimos" não existe — alguém decidiu
- Decisões podem ser delegadas, mas accountability não
- Inacção deliberada é uma decisão e deve ser registada como tal

### Política 2 — Transparência de Informação
- Informação é aberta por defeito dentro do squad
- Classificação de confidencialidade: public, internal, confidential, restricted
- Acesso a informação não requer justificação para nível internal
- Informação confidential e restricted requer need-to-know
- Nenhuma decisão pode ser tomada com informação deliberadamente ocultada

### Política 3 — Cadência e Rituais
- Cadências definidas (daily, weekly, monthly, quarterly) são obrigatórias
- Cancelamento de cadência requer justificação e aprovação do COO
- Cada cadência tem agenda publicada com antecedência mínima definida
- Outputs de cadências (decisões, action items) são registados
- Frequência de cadências é revista trimestralmente

### Política 4 — Gestão de Riscos
- Risk register é mantido activo e actualizado semanalmente
- Riscos com severidade high ou critical requerem owner e plano de mitigação
- Escalação de riscos segue path definido sem excepções
- Risk appetite é definido e revisto anualmente
- Nenhum risco crítico pode ser aceite sem aprovação do Vision Chief

### Política 5 — Qualidade e Standards
- Todos os outputs seguem templates e DoD definidos
- Self-review obrigatório antes de qualquer entrega
- Peer review para entregas com impacto cross-squad
- Standards de qualidade são documentados e acessíveis
- Non-conformidades são registadas e corrigidas

### Política 6 — Confidencialidade e Segurança
- Dados pessoais tratados conforme regulação aplicável (GDPR, LGPD)
- Credenciais nunca partilhadas em clear text
- Acesso a sistemas segue princípio de least privilege
- Incidentes de segurança reportados imediatamente ao CIO
- Auditorias de segurança realizadas semestralmente

### Política 7 — Conflito de Interesses
- Conflitos de interesse declarados proactivamente
- Agentes recusam-se em decisões onde há conflito
- Registo de declarações mantido pelo Vision Chief
- Revisão anual de potenciais conflitos

### Política 8 — Melhoria Contínua
- Retrospectives obrigatórias após cada trimestre
- Post-mortems obrigatórios para incidentes P1/P2
- Feedback é recolhido sistematicamente de stakeholders
- Learnings são registados e accionados
- O próprio sistema de governance é revisto anualmente

---

## Compliance e Regulação

### Framework de Compliance
1. **Identificar**: mapear regulações aplicáveis ao contexto
2. **Implementar**: definir controles para cada requisito
3. **Monitorizar**: verificação contínua de cumprimento
4. **Reportar**: reporting regular ao Vision Chief e Board
5. **Remediar**: correcção imediata de non-conformidades

### Áreas de Compliance Típicas
- Protecção de dados (GDPR, LGPD, CCPA)
- Regulação sectorial (conforme indústria)
- Governance de AI (EU AI Act, guidelines internas)
- Financeira (reporting, auditoria)
- Laboral (direitos dos trabalhadores)
- Propriedade intelectual (IP, licenças)

---

## Processo de Criação de Políticas

### Quando Criar Nova Política
Uma nova política é justificada quando:
1. Risco significativo sem controle formal
2. Requisito regulatório novo
3. Incidente que revela gap de governance
4. Crescimento organizacional requer formalização
5. Stakeholders externos exigem (investidores, clientes)

### Processo
1. **Proposta**: owner identifica necessidade e propõe draft
2. **Consulta**: squad revê e comenta (5 dias úteis)
3. **Refinamento**: incorporar feedback relevante
4. **Aprovação**: Vision Chief aprova (board para políticas major)
5. **Comunicação**: distribuição a todos os affected
6. **Implementação**: processos e controles activados
7. **Revisão**: data de revisão definida (máximo 12 meses)

### Critérios para Boa Política
- [ ] Resolve um problema real e identificado
- [ ] É clara e não ambígua
- [ ] É praticável com recursos disponíveis
- [ ] Tem owner e data de revisão
- [ ] É proporcional ao risco
- [ ] Não duplica política existente

---

## Enforcement

### Como as Políticas São Cumpridas
1. **Educação**: todos conhecem e entendem as políticas
2. **Sistemas**: automação previne violações onde possível
3. **Auditoria**: verificação regular de cumprimento
4. **Feedback**: non-conformidades comunicadas ao owner
5. **Escalação**: violações repetidas escaladas ao Vision Chief

### Consequências de Não-Cumprimento
- Primeira ocorrência: feedback e coaching
- Segunda ocorrência: plano de correcção formal
- Terceira ocorrência: escalação ao Vision Chief para acção
- Violação grave: acção imediata conforme severidade

---

## Notas Técnicas

- Políticas armazenadas em `data/policies/`
- Cada política versionada com changelog
- Índice de políticas mantido actualizado
- Audit trail de todas as alterações
- Review calendar mantido pelo COO Orchestrator
