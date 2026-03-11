# Onboarding — Como Entrar no C-Level OS

> Processo estruturado de onboarding para novos utilizadores do C-Level Squad.

---

## Objetivo

Garantir que novos membros ou utilizadores do C-Level OS atingem produtividade
rapidamente, compreendem o sistema e os seus princípios, e se integram
efectivamente na cadência operacional.

---

## Tipos de Onboarding

### Tipo A — Novo Agente (AI Agent)
Quando um novo agente AI é adicionado ao squad:
- Configuração do agente com contexto organizacional
- Calibração com histórico de decisões e métricas
- Integração com outros agentes (contratos, SLAs)
- Período de teste assistido

### Tipo B — Novo Operador (Humano)
Quando uma pessoa nova vai operar o sistema:
- Formação sobre a estrutura e princípios do OS
- Walkthrough prático de workflows principais
- Período de shadowing com operador experiente
- Avaliação de competência

### Tipo C — Nova Organização
Quando uma organização adopta o C-Level OS:
- Setup inicial e personalização
- Formação da equipa operadora
- Migração de dados e processos existentes
- Período de estabilização

---

## Percurso de Onboarding — Tipo B (Operador Humano)

### Semana 1 — Fundamentos

#### Dia 1 — Orientação
- [ ] Ler `docs/getting-started.md` (30 min)
- [ ] Ler `docs/c-level-overview.md` (20 min)
- [ ] Explorar a estrutura de directórios (15 min)
- [ ] Ler `docs/glossary.md` (15 min)
- [ ] Sessão de Q&A com operador experiente (30 min)

#### Dia 2 — Agentes
- [ ] Ler `docs/agent-roles-guide.md` (30 min)
- [ ] Explorar ficheiros de cada agente em `agents/` (30 min)
- [ ] Ler summaries em `authority/agent-summaries/` (30 min)
- [ ] Entender interacções entre agentes (15 min)

#### Dia 3 — Operating System
- [ ] Ler `docs/operating-system.md` (30 min)
- [ ] Ler `docs/decision-making.md` (30 min)
- [ ] Ler `docs/cross-squad-contracts.md` (20 min)
- [ ] Compreender cadência operacional (15 min)

#### Dia 4 — Frameworks e Workflows
- [ ] Ler `docs/framework-selection-guide.md` (20 min)
- [ ] Ler `docs/workflow-guide.md` (20 min)
- [ ] Explorar `frameworks/` e escolher 2-3 para aprofundar (30 min)
- [ ] Explorar `workflows/` e escolher 1 para entender em detalhe (30 min)

#### Dia 5 — Governance e Prática
- [ ] Ler `docs/governance-and-policies.md` (20 min)
- [ ] Ler `docs/ai-governance.md` (20 min)
- [ ] Ler `docs/anti-patterns-guide.md` (20 min)
- [ ] Primeiro exercício prático: gerar uma agenda WBR simulada (60 min)

### Semana 2 — Prática Assistida

#### Objectivos
- Executar workflows com supervisão
- Participar em cadências (WBR) como observador
- Executar 1 workflow de geração completo
- Executar 1 workflow de tracking completo
- Registar 1 decisão no decision log

#### Actividades Diárias
- Manhã: executar tarefa prática com guidance
- Tarde: review e feedback com mentor/operador experiente
- End of day: documentar learnings e dúvidas

### Semana 3 — Autonomia Supervisionada

#### Objectivos
- Executar workflows de forma independente (com review)
- Participar activamente na WBR
- Identificar e propor 1 melhoria ao sistema
- Executar 1 workflow de análise

#### Critérios de Conclusão da Semana
- Workflow de geração executado sem erros significativos
- Workflow de tracking actualizado correctamente
- Participação construtiva na WBR
- Feedback positivo do mentor

### Semana 4 — Independência

#### Objectivos
- Operar autonomamente os workflows atribuídos
- Servir de ponto de contacto para o seu domínio
- Contribuir com 1 melhoria implementada
- Passar no assessment de competência

---

## Assessment de Competência

### Avaliação ao Final do Onboarding
O novo operador deve demonstrar:

| Competência | Critério | Peso |
|------------|---------|------|
| Conhecimento do OS | Quiz de 20 perguntas, >80% correcto | 20% |
| Execução de workflows | 3 workflows executados com qualidade | 30% |
| Tomada de decisão | 1 decisão registada correctamente | 15% |
| Uso de frameworks | Aplicação correcta de 2 frameworks | 15% |
| Colaboração | Feedback positivo de peers | 10% |
| Melhoria | 1 sugestão aceite de melhoria | 10% |

### Resultado
- **Pass**: ≥75% — acesso completo e autonomia
- **Conditional**: 60-74% — 2 semanas adicionais com mentoria
- **Retry**: <60% — repetir semanas 2-4 com ajustes

---

## Materiais de Onboarding

### Leitura Obrigatória (por ordem)
1. `docs/getting-started.md`
2. `docs/c-level-overview.md`
3. `docs/agent-roles-guide.md`
4. `docs/operating-system.md`
5. `docs/decision-making.md`
6. `docs/workflow-guide.md`
7. `docs/governance-and-policies.md`
8. `docs/anti-patterns-guide.md`
9. `docs/glossary.md`

### Leitura Recomendada
- `docs/ai-governance.md`
- `docs/framework-selection-guide.md`
- `docs/cross-squad-contracts.md`
- `docs/naming-conventions.md`
- `authority/essays/c-level-as-operating-system.md`

### Exercícios Práticos
1. Gerar agenda de WBR com dados simulados
2. Criar metrics pack para cenário fictício
3. Registar decisão no decision log
4. Executar risk scan com dados de exemplo
5. Analisar effectiveness de reunião fictícia

---

## Responsabilidades do Mentor

O mentor/operador experiente deve:
1. Estar disponível para perguntas (response time: <4h)
2. Fazer check-in diário durante semanas 1-2
3. Fazer check-in bi-semanal durante semanas 3-4
4. Rever outputs do novo operador com feedback
5. Conduzir assessment final e dar recomendação

---

## Feedback de Onboarding

Ao final do processo, o novo operador completa:
```
1. O processo de onboarding foi claro? [1-5]
2. Sentes-te preparado para operar? [1-5]
3. O que funcionou melhor? [texto]
4. O que pode ser melhorado? [texto]
5. Quanto tempo levaste para te sentir produtivo? [dias]
```

Feedback é usado para melhorar o processo continuamente.

---

## Notas Técnicas

- Checklist de onboarding em `checklists/onboarding/`
- Materiais de assessment em `data/onboarding/assessments/`
- Histórico de onboardings em `data/onboarding/history/`
- Processo revisto semestralmente baseado em feedback acumulado
