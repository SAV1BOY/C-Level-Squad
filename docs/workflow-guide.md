# Workflow Guide — Como Executar Workflows

> Guia prático para entender, executar e criar workflows no C-Level Squad.

---

## O Que São Workflows

Workflows são processos estruturados que transformam inputs em outputs
através de passos definidos. São a forma como o C-Level Squad executa
trabalho de forma consistente e repetível.

---

## Anatomia de um Workflow

### Estrutura Padrão
Cada workflow segue esta estrutura:

```
NOME DO WORKFLOW
├── Trigger: O que inicia o workflow
├── Owner: Quem é responsável pela execução
├── Inputs: O que é necessário para começar
├── Passos: Sequência de acções
│   ├── Passo 1: [Acção] → [Output parcial]
│   ├── Passo 2: [Acção] → [Output parcial]
│   ├── Decision Gate: [Critério para avançar]
│   └── Passo N: [Acção] → [Output final]
├── Outputs: O que é produzido
├── Quality Gate: Verificação antes de concluir
└── Next: O que acontece depois
```

### Elementos-Chave
- **Trigger**: pode ser temporal (cadência), evento (incidente) ou manual
- **Owner**: responsável por garantir execução, pode delegar passos
- **Decision gates**: pontos onde se decide continuar, ajustar ou parar
- **Quality gates**: verificações de qualidade antes de avançar
- **Handoffs**: quando responsabilidade passa para outra pessoa/squad

---

## Como Executar um Workflow

### Passo 1 — Identificar o Workflow
Determina qual workflow aplicar à situação:
- Consulta `workflows/` para lista de workflows disponíveis
- Usa `docs/framework-selection-guide.md` para orientação
- Se não existe workflow adequado, avalia se é necessário criar

### Passo 2 — Verificar Pré-Condições
Antes de iniciar, confirma:
- [ ] Trigger condition é verdadeira
- [ ] Inputs necessários estão disponíveis
- [ ] Owner está identificado e disponível
- [ ] Dependências estão satisfeitas
- [ ] Não há bloqueio que impeça execução

### Passo 3 — Executar os Passos
Para cada passo do workflow:
1. Lê a descrição completa do passo
2. Reúne os inputs específicos desse passo
3. Executa a acção descrita
4. Verifica o output parcial contra critérios
5. Documenta resultado e observações
6. Avança para o passo seguinte ou decision gate

### Passo 4 — Decision Gates
Em cada decision gate:
- Avalia o critério definido objectivamente
- Se critério cumprido: avança
- Se não cumprido: identifica o que falta e resolve
- Se impossível resolver: escala ao owner ou squad lead
- Documenta a decisão tomada no gate

### Passo 5 — Quality Gate Final
Antes de declarar workflow completo:
- [ ] Todos os outputs estão produzidos
- [ ] Qualidade dos outputs verificada
- [ ] Documentação actualizada
- [ ] Stakeholders relevantes informados
- [ ] Handoffs concluídos (se aplicável)

### Passo 6 — Fechar
- Registar conclusão do workflow
- Distribuir outputs aos destinatários
- Actualizar status no tracking system
- Identificar melhorias para próxima execução

---

## Tipos de Workflows no C-Level Squad

### Workflows de Geração
Produzem artefactos e documentos:
- Agenda generation (WBR/MBR/QBR)
- Metrics pack building
- Board prep building
- Stakeholder update building

### Workflows de Tracking
Monitorizam e actualizam registos:
- Decision log updating
- Initiative health tracking
- Risk scanning
- Roadmap diffing
- Forecast accuracy tracking

### Workflows de Análise
Produzem insights e recomendações:
- Decision quality analysis
- Meeting effectiveness analysis
- AI evaluation
- Cross-squad effectiveness analysis
- Quarterly review building

### Workflows Operacionais
Gerem operações do dia-a-dia:
- Daily standup
- WBR execution
- Incident response
- Onboarding
- Offboarding

---

## Criação de Novos Workflows

### Quando Criar
Criar um novo workflow quando:
1. Processo é executado regularmente (>3 vezes)
2. Consistência é importante (múltiplas pessoas executam)
3. Qualidade varia entre execuções
4. Complexidade justifica documentação
5. Onboarding de novos membros requer guia

### Template para Novo Workflow
```markdown
# [Nome do Workflow]

> [Descrição em 1 linha]

## Trigger
[O que inicia este workflow]

## Owner
[Quem é responsável]

## Inputs
- [Input 1]
- [Input 2]

## Passos

### Passo 1 — [Nome]
- Acção: [O que fazer]
- Input: [O que é necessário]
- Output: [O que é produzido]
- Notas: [Dicas ou cuidados]

### Passo 2 — [Nome]
...

### Decision Gate — [Critério]
- Se [condição]: avançar para Passo N
- Se não: [acção alternativa]

## Outputs
- [Output 1]
- [Output 2]

## Quality Gate
- [ ] [Critério 1]
- [ ] [Critério 2]
```

### Processo de Aprovação
1. Draft do workflow pelo autor
2. Review por peer que poderia executá-lo
3. Test run com cenário real
4. Ajustes baseados no test run
5. Aprovação pelo owner do domínio
6. Publicação em `workflows/`

---

## Melhoria Contínua de Workflows

### Quando Melhorar
- Após cada execução: nota rápida sobre o que funcionou e não funcionou
- Trimestralmente: review formal dos workflows mais usados
- Quando falha: análise de root cause e ajuste

### Processo de Melhoria
1. Recolher feedback de quem executa
2. Identificar passos problemáticos (lentos, confusos, falham)
3. Propor melhoria específica
4. Testar melhoria em próxima execução
5. Se eficaz, actualizar workflow
6. Comunicar alteração aos utilizadores

### Métricas de Workflow
- Tempo de execução (actual vs esperado)
- Taxa de conclusão com sucesso
- Número de re-works ou iterações
- Satisfação do executor
- Qualidade do output

---

## Erros Comuns

1. **Saltar passos**: cada passo existe por uma razão
2. **Ignorar quality gates**: verificações previnem erros downstream
3. **Não documentar**: observações durante execução são valiosas
4. **Rigidez excessiva**: adaptar ao contexto é permitido e encorajado
5. **Não fechar**: registar conclusão é essencial para tracking

---

## Notas Técnicas

- Workflows armazenados em `workflows/`
- Versionados com data de última actualização
- Referências cruzadas com scripts em `scripts/`
- Templates de suporte em `templates/`
- Métricas de execução em `data/workflow-metrics/`
