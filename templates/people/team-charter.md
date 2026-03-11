# Template: Team Charter

## Propósito
Este template define identidade, missão, normas de trabalho e acordos operacionais de um time. O charter é criado coletivamente e serve como contrato social do time, alinhando expectativas e reduzindo conflitos.

## Instruções de Uso
1. Facilite uma sessão de 2-3 horas com todo o time para criar o charter
2. Todos devem contribuir — charter imposto não funciona
3. Revisão a cada quarter ou quando houver mudança significativa no time
4. Novos membros devem ler e discutir o charter no onboarding

---

## Informações do Time

| Campo | Valor |
|-------|-------|
| **Nome do Time** | [Nome — ex: "Time Atlas"] |
| **Missão** | [Uma frase que define por que o time existe] |
| **Líder** | [Nome — Cargo] |
| **Membros** | [Lista de nomes e cargos] |
| **Data de Criação** | [DD/MM/AAAA] |
| **Última Revisão** | [DD/MM/AAAA] |

---

## 1. Missão e Escopo

### 1.1 Missão do Time
[Declaração clara e concisa de 1-2 frases sobre o propósito do time]

*Exemplo: "Garantir que clientes completem a jornada de onboarding com sucesso, medido por taxa de ativação em 7 dias > 60%"*

### 1.2 Escopo de Atuação
**O que é responsabilidade do nosso time:**
- [Domínio/serviço/processo 1]
- [Domínio/serviço/processo 2]
- [Domínio/serviço/processo 3]

**O que NÃO é responsabilidade do nosso time:**
- [Clarificar fronteiras com outros times]
- [Áreas que frequentemente geram confusão de ownership]

### 1.3 Stakeholders Principais
| Stakeholder | Relação | Cadência de Interação |
|------------|---------|----------------------|
| [Time/Pessoa X] | [Dependência / Consumidor / etc.] | [Semanal / Quinzenal / etc.] |
| [Time/Pessoa Y] | [Relação] | [Cadência] |

---

## 2. Valores e Princípios do Time

### Nossos Valores (definidos coletivamente)
1. **[Valor 1 — ex: "Transparência radical"]:** [O que significa na prática para nós]
2. **[Valor 2 — ex: "Qualidade > Velocidade"]:** [O que significa na prática]
3. **[Valor 3 — ex: "Feedback direto e respeitoso"]:** [O que significa na prática]
4. **[Valor 4 — ex: "Ownership coletivo"]:** [O que significa na prática]

### Como Tomamos Decisões
- **Decisões técnicas do dia a dia:** [Quem decide — ex: "Quem implementa decide, com pair review"]
- **Decisões de design/arquitetura:** [Processo — ex: "RFC com revisão do time em 3 dias"]
- **Decisões de priorização:** [Processo — ex: "Product Owner define, time pode questionar"]
- **Decisões de people/processo:** [Processo — ex: "Consenso do time na retro"]

### Como Lidamos com Conflito
- [Passo 1 — ex: "Conversa direta entre as partes envolvidas"]
- [Passo 2 — ex: "Se não resolver, mediação com Tech Lead/EM"]
- [Passo 3 — ex: "Escalonamento para liderança como último recurso"]

---

## 3. Normas de Trabalho

### 3.1 Comunicação

| Canal | Uso | SLA de Resposta |
|-------|-----|----------------|
| Slack #[canal-time] | Comunicação geral do time | [Xh — horário comercial] |
| Slack #[canal-alertas] | Alertas de produção | [Imediato — horário de plantão] |
| E-mail | Comunicação formal / externa | [24h] |
| Reunião síncrona | Decisões complexas, brainstorming | [Agendado com 24h antecedência] |
| Doc/RFC | Propostas técnicas e decisões | [Feedback em 3 dias úteis] |

### 3.2 Reuniões

| Reunião | Frequência | Duração | Participantes | Objetivo |
|---------|-----------|---------|-------------|----------|
| Daily standup | Diária | 15 min | Todo o time | Sync rápido — bloqueios e progresso |
| Planning | [Semanal/Quinzenal] | [Xh] | Todo o time | Planejar próximo ciclo |
| Retro | [Quinzenal/Mensal] | [Xh] | Todo o time | Melhorar processos |
| Refinamento | [Semanal] | [Xh] | Todo o time | Detalhar e estimar trabalho |
| 1:1 com líder | [Semanal/Quinzenal] | [30-60 min] | Individual | Desenvolvimento e suporte |

### 3.3 Horários e Disponibilidade
- **Core hours (todos online):** [ex: 10h-16h BRT]
- **Política de foco:** [ex: "Sem reuniões às quartas — dia de focus time"]
- **Política de férias:** [ex: "Máximo 2 pessoas do time simultaneamente"]
- **Plantão:** [ex: "Rotação semanal — escalado no PagerDuty"]

### 3.4 Code Review e Padrões Técnicos
- **SLA de code review:** [ex: "Primeiro review em até 4h úteis"]
- **Quem faz review:** [ex: "Qualquer membro do time, min 1 aprovação"]
- **Cobertura de testes mínima:** [ex: "80% para novos códigos"]
- **Definition of Done:**
  - [ ] Código revisado e aprovado
  - [ ] Testes escritos e passando
  - [ ] Documentação atualizada (se aplicável)
  - [ ] Deploy em staging validado
  - [ ] Métricas/alertas configurados (se aplicável)

---

## 4. Objetivos Atuais

### OKRs do Período ([Quarter/Semestre])

| Objetivo | Key Results | Progresso |
|----------|-----------|-----------|
| [O1] | KR1: [Métrica e meta] | [X%] |
| | KR2: [Métrica e meta] | [X%] |
| [O2] | KR1: [Métrica e meta] | [X%] |
| | KR2: [Métrica e meta] | [X%] |

---

## 5. Papéis e Responsabilidades

| Papel | Pessoa | Responsabilidades |
|-------|--------|------------------|
| Tech Lead | [Nome] | Decisões de arquitetura, qualidade técnica, mentoria |
| Product Owner | [Nome] | Priorização, backlog, stakeholder management |
| Eng Manager | [Nome] | Desenvolvimento de pessoas, processo, hiring |
| SRE/On-call | [Rotação] | Saúde de produção, incidentes, observabilidade |
| Scrum Master | [Nome/Rotação] | Facilitação de cerimônias, remoção de bloqueios |

---

## 6. Acordo de Feedback

- **Como damos feedback:** [ex: "Direto, específico, em privado para construtivo, em público para positivo"]
- **Quando damos feedback:** [ex: "O mais próximo do evento possível, não acumular para a review"]
- **Framework:** [ex: "SBI — Situação, Comportamento, Impacto"]

---

## Exemplo Preenchido (Resumo)

> **Time:** Time Pagamentos | **Missão:** "Garantir que todo pagamento seja processado com segurança e em menos de 3 segundos"
> **Membros:** 6 (1 TL, 1 PO, 4 Engenheiros) | **Core hours:** 10h-16h BRT
> **Valor #1:** "Zero tolerância para falha silenciosa — alertar sempre"
> **Decision making:** Decisões técnicas no PR, decisões de prioridade com PO, processo na retro
> **Code review SLA:** 4h úteis | **Plantão:** rotação semanal

---

## Dicas de Uso
- Charter criado pelo time, não pelo líder — ownership coletivo é fundamental
- Mantenha curto e prático — ninguém relê um charter de 20 páginas
- Revise na retro trimestral — times mudam, normas devem acompanhar
- Use como referência em conflitos — "combinamos que..."
- Novos membros leem e discutem com o time na primeira semana
- Se uma norma não está sendo seguida, discuta na retro — talvez precise mudar
