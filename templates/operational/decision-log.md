# Template de Log de Decisões

## Instruções de Uso
Este template documenta decisões importantes de forma estruturada, criando um registro histórico consultável que ajuda a entender o contexto e racional por trás de cada escolha.

---

## Índice de Decisões

| ID | Data | Título | Status | Área |
|----|------|--------|--------|------|
| DEC-001 | [DD/MM/AAAA] | [Título resumido] | Aprovada / Pendente / Revisada | [Área] |
| DEC-002 | [DD/MM/AAAA] | [Título resumido] | Aprovada / Pendente / Revisada | [Área] |
| DEC-003 | [DD/MM/AAAA] | [Título resumido] | Aprovada / Pendente / Revisada | [Área] |

---

## Registro de Decisões

### DEC-001: [Título Descritivo da Decisão]

| Campo | Valor |
|-------|-------|
| **ID** | DEC-001 |
| **Data** | [DD/MM/AAAA] |
| **Status** | Proposta / Em discussão / Aprovada / Revisada / Descontinuada |
| **Decisor** | [Nome e cargo de quem tomou a decisão final] |
| **Participantes** | [Nomes de quem participou da discussão] |
| **Área** | [Engenharia / Produto / Pessoas / Finanças / Estratégia] |

#### Contexto
[Descrever a situação que levou à necessidade desta decisão. Qual problema estávamos enfrentando? O que mudou no ambiente que tornou essa decisão necessária?]

#### Opções Consideradas

**Opção A: [Nome da opção]**
- Descrição: [O que essa opção envolve]
- Prós: [Vantagens desta opção]
- Contras: [Desvantagens e riscos]
- Custo estimado: [Se aplicável]
- Timeline: [Se aplicável]

**Opção B: [Nome da opção]**
- Descrição: [O que essa opção envolve]
- Prós: [Vantagens desta opção]
- Contras: [Desvantagens e riscos]
- Custo estimado: [Se aplicável]
- Timeline: [Se aplicável]

**Opção C: [Nome da opção]**
- Descrição: [O que essa opção envolve]
- Prós: [Vantagens desta opção]
- Contras: [Desvantagens e riscos]
- Custo estimado: [Se aplicável]
- Timeline: [Se aplicável]

#### Decisão
[Qual opção foi escolhida e o racional detalhado da decisão]

#### Consequências
- [Impacto positivo esperado 1]
- [Impacto positivo esperado 2]
- [Trade-off aceito 1]
- [Trade-off aceito 2]

#### Critérios de Revisão
- [Em que circunstâncias essa decisão deve ser reavaliada]
- [Data ou trigger para revisão: DD/MM/AAAA ou evento X]

#### Referências
- [Link para documento de suporte]
- [Link para ata de reunião onde foi discutida]
- [Link para dados que embasaram a decisão]

---

### DEC-002: [Título da Segunda Decisão]

| Campo | Valor |
|-------|-------|
| **ID** | DEC-002 |
| **Data** | [DD/MM/AAAA] |
| **Status** | [Status] |
| **Decisor** | [Nome] |
| **Participantes** | [Nomes] |
| **Área** | [Área] |

#### Contexto
[Descrição do contexto]

#### Opções Consideradas
[Seguir mesmo formato acima]

#### Decisão
[Decisão tomada e racional]

#### Consequências
[Impactos esperados]

#### Critérios de Revisão
[Quando reavaliar]

---

## Categorias de Decisão

### Por Impacto
- **Tipo 1 (Irreversível)**: Decisões difíceis de reverter, requerem análise profunda
  - Exemplos: Mudança de stack, M&A, mudança de modelo de negócio
  - Processo: Documento completo, múltiplos stakeholders, prazo de cooling off
- **Tipo 2 (Reversível)**: Decisões que podem ser facilmente ajustadas
  - Exemplos: Feature flag, pricing de teste, processo interno
  - Processo: Documento simplificado, decisão rápida, experimentação

### Por Área
- **Estratégica**: Direção da empresa, modelo de negócio, mercados
- **Técnica**: Arquitetura, stack, infraestrutura
- **Produto**: Features, roadmap, priorização
- **Pessoas**: Estrutura, hiring, políticas
- **Financeira**: Budget, investimentos, cortes

---

## Boas Práticas para Documentação de Decisões

### O que Documentar
- Decisões que afetam múltiplas pessoas ou áreas
- Decisões com impacto financeiro significativo
- Decisões técnicas de arquitetura (ADRs)
- Mudanças de estratégia ou direção
- Decisões que geram precedente para futuras escolhas
- Decisões que foram contestadas ou polêmicas

### O que Não Documentar
- Decisões triviais do dia a dia
- Escolhas operacionais de baixo impacto
- Decisões que já são cobertas por políticas existentes

### Como Manter o Log
- Revisar decisões abertas mensalmente
- Marcar decisões revisadas ou descontinuadas
- Usar IDs consistentes para referência cruzada
- Manter acessível para toda a organização
- Incluir links para documentos de suporte
- Registrar aprendizados quando decisão é revisada
- Usar tags ou categorias para facilitar busca futura

### Frameworks de Decisão Úteis
- **DACI**: Driver, Approver, Contributors, Informed
- **RAPID**: Recommend, Agree, Perform, Input, Decide
- **Eisenhower**: Urgente/Importante para priorização
- **Reversibility**: Tipo 1 (irreversível) vs Tipo 2 (reversível)
- **Pre-mortem**: Imaginar falha futura antes de decidir
