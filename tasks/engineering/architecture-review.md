# Review de Arquitetura

> Processo estruturado para avaliar, documentar e evoluir a arquitetura
> de sistemas, garantindo que decisões técnicas suportam os objetivos de negócio.

## Objetivo

Garantir que a arquitetura dos sistemas evolui de forma intencional, sustentável
e alinhada com as necessidades de escala, segurança e agilidade do negócio.

## Frequência

- **Review completo:** Semestral
- **Review de novos projetos/features:** Antes do início do desenvolvimento
- **Review de incidentes:** Após incidentes com causa raiz arquitetural
- **Ad-hoc:** Quando mudanças significativas de contexto ocorrem

## Tipos de Architecture Review

### 1. Design Review (Pré-Implementação)
Para novos projetos, features significativas ou mudanças arquiteturais:
- Acontece antes do código ser escrito
- Foco: a proposta é adequada para o problema?
- Output: aprovação, aprovação com condições, ou redesign

### 2. Health Check (Periódico)
Avaliação da arquitetura existente:
- Acontece semestralmente
- Foco: a arquitetura atual ainda atende às necessidades?
- Output: lista de melhorias priorizadas

### 3. Post-Incident Review (Reativo)
Quando um incidente revela fragilidade arquitetural:
- Acontece após o post-mortem do incidente
- Foco: o que na arquitetura permitiu esse incidente?
- Output: mudanças arquiteturais para prevenir recorrência

## Processo de Design Review

### Preparação (Proponente)
O engenheiro ou tech lead que propõe a mudança prepara:

- [ ] **Documento de design** (template abaixo)
- [ ] **Diagrama de arquitetura** (atual e proposto)
- [ ] **Análise de alternativas** (pelo menos 2 opções consideradas)
- [ ] **Distribuir para reviewers** 3-5 dias antes da sessão

### Sessão de Review (60-90 min)
- [ ] Leitura silenciosa do documento (15-20 min)
- [ ] Apresentação do proponente (10 min)
- [ ] Perguntas e discussão (30-40 min)
- [ ] Decisão e próximos passos (10 min)

### Participantes
- Proponente (autor do design)
- Tech lead do time
- 1-2 engenheiros seniores de outros times (perspectiva cross-team)
- Arquiteto de plataforma (se houver)
- Product manager (para contexto de negócio)

### Decisões Possíveis
1. **Aprovado:** Proceder com implementação
2. **Aprovado com condições:** Proceder com ajustes documentados
3. **Revisão necessária:** Redesign e nova sessão
4. **Rejeitado:** Abordagem fundamentalmente inadequada

## Template de Design Document

```
# Design Document: [Título]

## Metadata
- Autor: [Nome]
- Reviewers: [Nomes]
- Status: Draft | In Review | Approved | Implemented
- Data: [Data]

## 1. Contexto e Motivação
Por que esta mudança é necessária? Qual problema de negócio ou técnico resolve?

## 2. Requisitos
### Funcionais
- [Lista de requisitos funcionais]
### Não-Funcionais
- Performance: [targets específicos]
- Escalabilidade: [targets específicos]
- Disponibilidade: [targets específicos]
- Segurança: [requisitos]

## 3. Proposta
Descrição detalhada da solução proposta com diagramas.

## 4. Alternativas Consideradas
### Alternativa A: [Nome]
- Descrição, prós, contras
### Alternativa B: [Nome]
- Descrição, prós, contras
### Por que a proposta foi escolhida
- Justificativa

## 5. Impacto
- Sistemas afetados
- Migração necessária
- Riscos e mitigações
- Rollback plan

## 6. Plano de Implementação
- Fases
- Timeline estimado
- Dependências

## 7. Métricas de Sucesso
- Como saberemos que a implementação foi bem-sucedida?
- Métricas antes e depois

## 8. FAQ
Perguntas antecipadas e respostas.
```

## Processo de Health Check Semestral

### Dimensões Avaliadas

**1. Escalabilidade (Score 1-5)**
- [ ] Os sistemas suportam 2x o tráfego atual?
- [ ] Bottlenecks conhecidos estão documentados?
- [ ] Auto-scaling está configurado adequadamente?
- [ ] Database pode crescer sem redesign?

**2. Resiliência (Score 1-5)**
- [ ] Single points of failure identificados e mitigados?
- [ ] Circuit breakers e fallbacks implementados?
- [ ] Disaster recovery testado recentemente?
- [ ] Graceful degradation funciona sob carga?

**3. Segurança (Score 1-5)**
- [ ] Autenticação e autorização robustas?
- [ ] Dados sensíveis criptografados em trânsito e em repouso?
- [ ] Dependências sem vulnerabilidades conhecidas críticas?
- [ ] Logs de auditoria adequados?

**4. Observabilidade (Score 1-5)**
- [ ] Métricas, logs e traces implementados?
- [ ] Alertas configurados para cenários críticos?
- [ ] Dashboards de saúde atualizados?
- [ ] On-call tem ferramentas para diagnosticar problemas rapidamente?

**5. Manutenibilidade (Score 1-5)**
- [ ] Código é compreensível para novo engenheiro?
- [ ] Testes automatizados cobrem cenários críticos?
- [ ] Deploy é automatizado e rápido?
- [ ] Documentação arquitetural está atualizada?

**6. Custo (Score 1-5)**
- [ ] Custos de infraestrutura são proporcionais ao valor gerado?
- [ ] Right-sizing de recursos está otimizado?
- [ ] Savings oportunidades identificadas?

### Score e Ações
- **25-30:** Arquitetura saudável, manutenção preventiva
- **18-24:** Áreas de melhoria identificadas, plano de ação necessário
- **12-17:** Riscos significativos, sprint de melhoria urgente
- **6-11:** Crítico, parar features e priorizar arquitetura

## ADR (Architecture Decision Records)

Toda decisão arquitetural significativa deve ser registrada como ADR:

```
# ADR-[número]: [Título]
- Data: [Data]
- Status: [Proposed | Accepted | Deprecated | Superseded]
- Deciders: [Nomes]

## Contexto
[Situação que motivou a decisão]

## Decisão
[O que decidimos]

## Consequências
[O que muda, positivo e negativo]
```

## Comunicação de Resultados

### Para o CTO/VP Engineering
- Score por dimensão com tendência (melhorou/piorou)
- Top 3 riscos identificados com recomendação
- Investimento necessário para endereçar (sprints, headcount)

### Para o CEO/Board
- Traduzir em linguagem de negócio
- "Nossa arquitetura suporta dobrar os usuários sem re-design"
- "Identificamos 2 riscos que podem causar downtime se não endereçados"
- "Recomendamos investir X sprints para melhorar resiliência"

## Referências

- "Fundamentals of Software Architecture" - Mark Richards & Neal Ford
- "Designing Data-Intensive Applications" - Martin Kleppmann
- "Software Architecture: The Hard Parts" - Neal Ford et al.
- C4 Model (c4model.com) para diagramas
