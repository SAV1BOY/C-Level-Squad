# Framework: DACI Decision Framework

## Descrição

DACI é um framework de tomada de decisão que clarifica papéis e responsabilidades para decisões importantes. Desenvolvido pela Intuit e popularizado por empresas como Atlassian, DACI define quatro papéis: Driver (quem conduz), Approver (quem decide), Contributors (quem contribui) e Informed (quem é informado). Diferente do RACI (focado em execução de tarefas), DACI é especificamente desenhado para decisões, tornando-o ideal para o C-Level Squad onde clareza sobre quem decide o quê é fundamental.

## Quando Usar

### Situações Ideais
- Decisões cross-funcionais que envolvem múltiplas áreas
- Quando há ambiguidade sobre quem tem autoridade para decidir
- Decisões importantes que precisam de buy-in de múltiplos stakeholders
- Para evitar "decisão por comitê" onde ninguém realmente decide
- Onboarding de novos executivos (clarificar quem decide o quê)
- Resolução de conflitos entre áreas sobre escopo de decisão

### Quando NÃO Usar
- Decisões triviais do dia a dia
- Decisões dentro de uma única função (gestor decide, simples)
- Crises que requerem ação imediata sem processo
- Quando já existe um processo de decisão claro e funcional

## Como Aplicar

### Os Quatro Papéis

#### D - Driver
```
Quem: Uma pessoa que conduz o processo de decisão
Responsabilidades:
- Reunir informações e alternativas
- Facilitar discussões com Contributors
- Garantir que o Approver tem tudo para decidir
- Acompanhar implementação da decisão
- Comunicar decisão aos Informed

Não é quem decide — é quem organiza o processo
Geralmente é o PM, líder de projeto ou especialista no tema
```

#### A - Approver
```
Quem: Uma pessoa (idealmente) que tem autoridade para decidir
Responsabilidades:
- Ouvir Contributors e Driver
- Tomar a decisão final
- Assumir responsabilidade pelo resultado
- Resolver impasses entre Contributors

Regras:
- Idealmente UMA pessoa (evitar "approval by committee")
- Se mais de um Approver, definir como desempatar
- Deve ter autoridade real, não simbólica
```

#### C - Contributors
```
Quem: Pessoas com conhecimento ou stake relevante
Responsabilidades:
- Fornecer input, dados e perspectivas
- Levantar riscos e alternativas
- Apoiar o Driver na análise
- Comprometer-se com a decisão mesmo se discordar

Não têm veto — contribuem mas não decidem
Geralmente são líderes de áreas impactadas, especialistas técnicos
```

#### I - Informed
```
Quem: Pessoas que precisam saber da decisão
Responsabilidades:
- Não participam do processo de decisão
- São comunicadas após a decisão
- Podem fazer perguntas de esclarecimento
- Implementam ou se adaptam conforme necessário

Regras:
- Não devem poder vetar ou atrasar a decisão
- Comunicação clara e oportuna é essencial
```

### Processo de Decisão DACI
```
1. PREPARAR
   - Driver identifica a decisão a ser tomada
   - Definir papéis: quem é D, A, C, I
   - Driver coleta informações e prepara opções

2. DELIBERAR
   - Driver apresenta contexto, opções e recomendação
   - Contributors dão input e levantam preocupações
   - Debate aberto sobre trade-offs
   - Driver sintetiza inputs

3. DECIDIR
   - Approver toma a decisão (com ou sem consenso)
   - Decisão é documentada com rationale
   - "Disagree and commit" para quem discorda

4. COMUNICAR
   - Driver comunica decisão aos Informed
   - Inclui: decisão, rationale, próximos passos, impactos
   - Define timeline de implementação

5. IMPLEMENTAR
   - Driver acompanha execução
   - Revisão de eficácia em data pré-definida
```

## Exemplos

### Mapa de Decisões do C-Level Squad
```
DECISÃO: Entrar em novo mercado geográfico
  D: Head de Strategy/BizOps
  A: CEO
  C: CFO, CPO, VP Sales, VP Ops
  I: CTO, CHRO, board members

DECISÃO: Escolha de stack tecnológico principal
  D: VP Engineering
  A: CTO
  C: CPO, Tech Leads, Architect
  I: CEO, CFO

DECISÃO: Modelo de pricing
  D: CPO ou Head of Pricing
  A: CEO
  C: CFO, VP Sales, VP CS, CPO
  I: CTO, marketing, CS team

DECISÃO: Plano de hiring do trimestre
  D: CHRO
  A: CEO (headcount) / Hiring managers (candidatos)
  C: CFO (budget), líderes de área
  I: Board, equipe existente

DECISÃO: Resposta a incidente de segurança
  D: CISO/Head of Security
  A: CTO (técnico) + CEO (comunicação)
  C: Legal, PR, Customer Success
  I: Board, clientes afetados, reguladores
```

### Template de Documento DACI
```
# Decisão: [Nome da decisão]
Data: [data]
Status: [em preparação / em discussão / decidido]

## Papéis
- Driver: [nome]
- Approver: [nome]
- Contributors: [nomes]
- Informed: [nomes]

## Contexto
[Por que esta decisão é necessária agora?]

## Opções
1. [Opção A]: [descrição, prós, contras]
2. [Opção B]: [descrição, prós, contras]
3. [Opção C]: [descrição, prós, contras]

## Recomendação do Driver
[Opção X porque...]

## Decisão (preenchido pelo Approver)
[Opção escolhida + rationale]

## Próximos Passos
- [Ação 1 - responsável - prazo]
- [Ação 2 - responsável - prazo]

## Revisão
Data de revisão de eficácia: [data]
```

## Limitações

- **Overhead** - Formalizar toda decisão com DACI pode ser excessivo
- **Um Approver** - Algumas decisões genuinamente requerem co-approval
- **Político** - Designar papéis pode gerar conflitos sobre quem é A vs. C
- **Rígido** - Decisões emergentes podem não caber no processo formal
- **Não garante qualidade** - O processo é bom mas a qualidade da decisão depende das pessoas
- **Cultural** - Funciona melhor em culturas que valorizam clareza de responsabilidade
- **Contributor frustration** - Contributors que contribuem mas nunca decidem podem desengajar
