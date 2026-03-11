# Análise: Modelo de Health Check do Spotify

## Contexto
O Spotify desenvolveu um modelo de health check para squads que se tornou referência mundial para avaliação de saúde de times. O Squad Health Check Model permite que times reflitam sobre diferentes aspectos do seu funcionamento de forma visual, facilitando conversas difíceis e identificação de áreas que precisam de atenção.

---

## 1. O Modelo Spotify de Squads

### Estrutura Organizacional
- **Squads**: Times autônomos de 6-12 pessoas (unidade básica)
- **Tribes**: Agrupamento de squads com missão relacionada (50-150 pessoas)
- **Chapters**: Grupo funcional cross-squad (ex: todos os backend engineers)
- **Guilds**: Comunidades de interesse cross-tribe (ex: guild de testing)
- Autonomia alta para squads na escolha de como trabalhar
- Alinhamento via missão, OKRs e dependency management

### Evolução e Realidade
- O modelo original de 2012 foi amplamente copiado pela indústria
- Na prática, Spotify evoluiu significativamente além do modelo original
- Muitas empresas copiaram a estrutura sem a cultura (e falharam)
- O valor real está nos princípios, não na nomenclatura específica

---

## 2. Squad Health Check Model

### O que É
- Ferramenta de auto-avaliação para times refletirem sobre sua saúde
- Avaliação em múltiplas dimensões relevantes para eficácia do time
- Formato visual com semáforo (verde, amarelo, vermelho) e tendência
- Facilitada periodicamente (recomendado: trimestral)
- Foco em gerar conversa, não em gerar score

### As Dimensões Originais

| # | Dimensão | O que Avalia |
|---|----------|-------------|
| 1 | Entregando valor | Estamos entregando coisas valiosas para usuários? |
| 2 | Velocidade | Conseguimos entregar rápido quando queremos? |
| 3 | Adequação para o propósito | Nosso código/produto funciona bem? Poucos bugs? |
| 4 | Diversão | Gostamos de vir trabalhar? |
| 5 | Saúde do codebase | Temos orgulho da qualidade do nosso código? |
| 6 | Aprendizado | Estamos aprendendo coisas interessantes? |
| 7 | Missão | Sabemos por que existimos e o que inspira? |
| 8 | Peões ou Players | Controlamos o que fazemos e como? |
| 9 | Teamwork | Trabalhamos bem juntos? |
| 10 | Suporte | Temos ajuda quando precisamos e temos acesso rápido? |
| 11 | Processo | Nosso processo funciona bem? |

### Escala de Avaliação
- **Verde**: Estamos bem nessa dimensão
- **Amarelo**: Alguns problemas, precisa de atenção
- **Vermelho**: Realmente ruim, precisa de ação urgente

### Indicador de Tendência
- **Seta para cima**: Está melhorando
- **Seta horizontal**: Estável
- **Seta para baixo**: Está piorando

---

## 3. Como Facilitar o Health Check

### Preparação
- Agendar sessão de 60-90 minutos com todo o squad
- Reservar sala com quadro branco ou usar ferramenta digital
- Facilitador idealmente alguém de fora do squad (Agile Coach, outro líder)
- Preparar cards com descrições de cada dimensão
- Criar ambiente seguro para honestidade (não será usado para avaliar pessoas)

### Execução Passo a Passo

**Passo 1: Introdução (5 min)**
- Explicar o propósito: gerar conversa e identificar melhorias
- Reforçar que não é avaliação de performance individual
- Estabelecer psychological safety

**Passo 2: Votação Individual (10 min)**
- Para cada dimensão, cada pessoa vota: verde, amarelo ou vermelho
- Votação simultânea e anônima (post-its virados)
- Depois de todos votarem, revelar simultaneamente
- Registrar distribuição de votos e tendência

**Passo 3: Discussão por Dimensão (40-60 min)**
- Discutir dimensões com maior divergência primeiro
- Perguntar: por que votou vermelho? O que faria mudar para verde?
- Facilitador garante que todos participam
- Documentar insights e sugestões
- Não tentar resolver tudo na sessão (identificar, não resolver)

**Passo 4: Priorização de Ações (15 min)**
- Selecionar 2-3 dimensões para focar no próximo período
- Definir ações concretas com owners
- Compromisso do time com as melhorias

**Passo 5: Encerramento (5 min)**
- Feedback sobre a sessão
- Definir data da próxima sessão
- Agradecimento pela participação e honestidade

---

## 4. Visualização e Tracking

### Dashboard de Health Check

```
Squad Alpha - Health Check Q1 2026

Dimensão          | Status | Trend | Ação
-------------------+--------+-------+------------------
Entregando valor   | Verde  |  -->  |
Velocidade         | Amarelo|  ↓    | Reduzir WIP
Qualidade          | Verde  |  ↑    | Manter práticas
Diversão           | Amarelo|  -->  | Social events
Codebase health    | Vermelho| ↓   | Sprint de debt
Aprendizado        | Verde  |  ↑    |
Missão             | Verde  |  -->  |
Autonomia          | Amarelo|  ↓    | Discuss com mgmt
Teamwork           | Verde  |  -->  |
Suporte            | Verde  |  ↑    |
Processo           | Amarelo|  -->  | Simplificar retro
```

### Evolução ao Longo do Tempo

| Dimensão | Q3 2025 | Q4 2025 | Q1 2026 | Tendência |
|----------|---------|---------|---------|-----------|
| Entregando valor | Amarelo | Verde | Verde | Estável |
| Velocidade | Vermelho | Amarelo | Amarelo | Melhorando |
| Qualidade | Amarelo | Amarelo | Verde | Melhorando |
| Codebase health | Amarelo | Amarelo | Vermelho | Piorando |

---

## 5. Adaptações e Extensões

### Dimensões Adicionais Sugeridas
- **Comunicação**: Nos comunicamos bem dentro e fora do squad?
- **Visão de produto**: Temos clareza sobre para onde o produto vai?
- **Bem-estar**: Estamos com workload sustentável?
- **Impacto**: Sentimos que nosso trabalho faz diferença?
- **Segurança psicológica**: Podemos tomar riscos sem medo?
- **Ferramentas**: Nossas ferramentas nos ajudam ou atrapalham?

### Health Check para Liderança
Adaptação para avaliar saúde do time de liderança:
- Alinhamento estratégico entre líderes
- Qualidade da comunicação entre áreas
- Velocidade de tomada de decisão
- Gestão de conflitos e prioridades
- Visão compartilhada de futuro
- Confiança entre os membros

### Health Check para a Organização
Adaptação para avaliar saúde organizacional:
- Employee NPS e engajamento
- Velocidade de delivery end-to-end
- Satisfação de clientes
- Eficácia de processos cross-team
- Capacidade de inovação
- Sustentabilidade do ritmo de trabalho

---

## 6. Lições e Aplicabilidade

### Por que Funciona
- É simples e visual (qualquer pessoa entende)
- Gera conversa ao invés de apenas números
- Ownership do time (eles definem melhorias)
- Tracking ao longo do tempo mostra evolução
- Não é punitivo (foco em melhoria, não em julgamento)
- Identifica problemas antes que se tornem crises

### Erros Comuns na Implementação
- Usar como ferramenta de avaliação de performance do time
- Management usar os dados para comparar times e ranquear
- Não agir sobre os resultados (gera cinismo)
- Fazer muito frequentemente (fadiga de health check)
- Facilitador do time influenciar as respostas
- Ignorar contexto: um vermelho pode ser aceitável temporariamente

### Implementação Recomendada
- [ ] Treinar facilitadores internos no modelo
- [ ] Adaptar dimensões para o contexto da empresa
- [ ] Começar com 1-2 squads piloto antes de escalar
- [ ] Garantir que ações são acompanhadas e executadas
- [ ] Revisar e adaptar dimensões anualmente
- [ ] Compartilhar aprendizados entre times (sem comparar scores)
- [ ] Usar como input para retrospectivas mais profundas
- [ ] Manter cadência trimestral para tracking de tendências
