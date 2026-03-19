# ADR System — Architecture Decision Records

> **Domínio:** Engineering & Tech
> **Autor de referência:** Michael Nygard — "Documenting Architecture Decisions"
> **Uso primário:** Registrar decisões de arquitetura com contexto, rationale e consequências para consulta futura.
> **Agente responsável:** cto-architect

---

## Origem e Contexto

Architecture Decision Records (ADRs) foram propostos por Michael Nygard em 2011 como uma forma leve e prática de documentar decisões de arquitetura. O problema que ADRs resolvem: **em 6 meses, ninguém lembra por que uma decisão foi tomada. Em 18 meses, alguém reverte a decisão sem entender as consequências. Em 3 anos, a nova equipe refaz os mesmos erros.**

ADRs são documentos curtos (1-2 páginas) que capturam:
- O **contexto** em que a decisão foi tomada.
- A **decisão** em si.
- As **consequências** (positivas e negativas) esperadas.

O formato é intencionalmente simples para reduzir a barreira de adoção. Um ADR ruim é melhor que nenhum ADR.

O princípio fundamental do C-Level Squad se aplica aqui: **"Se não está escrito, não é decisão — é conversa."** ADRs transformam decisões técnicas em registros permanentes.

---

## Quando Usar

- Toda decisão de arquitetura significativa: escolha de framework, padrão, linguagem, infra.
- Decisões de build vs buy (`frameworks/engineering-tech/build-vs-buy-framework.md`).
- Mudanças de padrão arquitetural (`frameworks/engineering-tech/architecture-patterns.md`).
- Escolha de fornecedores de infra ou ferramentas.
- Decisões de data model ou schema significativas.
- Qualquer decisão técnica que alguém possa questionar em 6 meses.

---

## Quando NÃO Usar

- Para decisões triviais (nome de variável, estilo de código — use linter).
- Para documentação de API — use OpenAPI/Swagger.
- Para runbooks operacionais — use documentação operacional.
- Para decisões de produto/negócio — use Decision Memo (`frameworks/operating-system/decision-memo-framework.md`).

---

## Estrutura / Modelo

### Template ADR

```markdown
# ADR-[NNN]: [Título da Decisão]

## Status
[Proposed | Accepted | Deprecated | Superseded by ADR-XXX]

## Data
[YYYY-MM-DD]

## Contexto
[Qual é o problema ou oportunidade que motivou esta decisão?
Quais forças estão em jogo? Requisitos, restrições, contexto técnico e de negócio.]

## Decisão
[O que decidimos fazer. Ser específico e direto.]

## Alternativas Consideradas
### Alternativa A: [Nome]
- Prós: [...]
- Contras: [...]

### Alternativa B: [Nome]
- Prós: [...]
- Contras: [...]

## Consequências
### Positivas
- [O que melhora com esta decisão]

### Negativas
- [O que piora ou que trade-off aceitamos]

### Riscos
- [Riscos conhecidos e mitigações planejadas]

## Participantes
- Decisor (DRI): [Nome]
- Consultados: [Nomes]
- Informados: [Nomes]

## Revisão Planejada
[Data ou trigger para re-avaliar esta decisão]
```

---

## Processo de Aplicação (step-by-step)

### Step 1: Identificar Decisão que Merece ADR
Critérios para criar ADR:
- Afeta mais de um squad ou serviço?
- É difícil de reverter (> 1 sprint para desfazer)?
- Tem trade-offs significativos que precisam ser documentados?
- Alguém pode questionar em 6 meses?

Se a resposta a qualquer dessas perguntas for sim, crie ADR.

### Step 2: Escrever o ADR
O autor (geralmente o tech lead ou arquiteto propondo a mudança) escreve o ADR:
- **Contexto:** Ser honesto sobre as forças em jogo. Incluir constraints.
- **Decisão:** Ser direto. "Decidimos usar PostgreSQL como banco principal."
- **Alternativas:** Documentar o que foi considerado e rejeitado, com razões.
- **Consequências:** Ser honesto sobre trade-offs. Toda decisão tem custo.

### Step 3: Revisar com Peers
Antes de aceitar, o ADR passa por review:
- Tech leads dos squads impactados.
- CTO para decisões cross-system.
- Formato: pull request ou documento compartilhado com comentários.

### Step 4: Aceitar e Publicar
- Mudar status para "Accepted".
- Adicionar ao índice de ADRs (ver Step 6).
- Comunicar aos "Informed" da matriz RASI.

### Step 5: Implementar e Referenciar
- Ao implementar, referenciar o ADR nos PRs e documentação.
- "Implementação do ADR-042" no commit message ou PR description.

### Step 6: Manter o Índice
Criar e manter um índice de todos os ADRs:

```markdown
# Índice de ADRs

| ADR | Título | Status | Data | DRI |
|-----|--------|--------|------|-----|
| 001 | PostgreSQL como banco principal | Accepted | 2024-01-15 | Tech Lead A |
| 002 | Adotar trunk-based development | Accepted | 2024-02-01 | Eng Manager B |
| 003 | Migrar de Heroku para AWS ECS | Accepted | 2024-03-10 | SRE Lead C |
| 004 | Usar Redis para cache de sessions | Deprecated (→ 008) | 2024-04-01 | Tech Lead A |
```

### Step 7: Revisar e Atualizar
ADRs não são eternos:
- **Deprecated:** A decisão não é mais relevante (tecnologia foi descontinuada).
- **Superseded:** Uma nova decisão substituiu esta (ADR-008 supersedes ADR-004).
- **Revisão programada:** O ADR definiu uma data de revisão — honrar.
- Trigggers: mudança significativa de contexto, novo membro questionando a decisão.

---

## Exemplos Práticos

### Exemplo 1: Escolha de Banco de Dados

**ADR-001: PostgreSQL como banco de dados principal**

**Status:** Accepted
**Contexto:** Precisamos de banco relacional para o core do produto. Temos 3 devs com experiência em PostgreSQL, 1 em MySQL. Volume esperado: 10K transações/dia no primeiro ano, projeção de 500K em 3 anos. Budget para managed service.
**Decisão:** Usar PostgreSQL (AWS RDS) como banco principal.
**Alternativas:** MySQL (menos features avançadas), MongoDB (não ideal para dados transacionais), CockroachDB (over-engineering para nosso volume).
**Consequências positivas:** Ecossistema maduro, bom suporte a JSON, extensões ricas, time experiente.
**Consequências negativas:** Vendor lock-in em AWS RDS (mitigação: usar standard SQL, evitar features proprietárias do RDS).
**Revisão:** Quando volume ultrapassar 100K tx/dia.

### Exemplo 2: Adoção de Feature Flags

**ADR-007: Adotar LaunchDarkly para feature flags**

**Status:** Accepted
**Contexto:** Deploy frequency está limitada porque features incompletas bloqueiam o deploy. Time quer trunk-based development mas precisa separar deploy de release.
**Decisão:** Adotar LaunchDarkly como sistema de feature flags para todos os squads.
**Alternativas:** Build interno (custo de manutenção alto), Unleash open-source (hosting e operação por conta própria), sem feature flags (status quo).
**Consequências positivas:** Deploy frequency deve dobrar. Rollbacks instantâneos via flag toggle. A/B testing habilitado.
**Consequências negativas:** Custo de R$ 3K/mês. Complexidade de gerenciar flags (flag debt). Dependência de serviço externo.
**Revisão:** Em 6 meses — avaliar se DF melhorou e se o custo é justificado.

---

## Armadilhas Comuns

1. **ADR como burocracia:** Se o processo de criar ADR leva mais de 1h, está over-engineered. Manter simples.
2. **ADR sem alternativas:** Documentar apenas a decisão sem as alternativas consideradas perde o valor de entender por que NÃO foi escolhido o caminho B.
3. **ADR sem consequências negativas:** Toda decisão tem trade-offs. Se não há consequências negativas documentadas, a análise foi superficial.
4. **ADR depois do fato:** Escrever ADR após implementar é melhor que nada, mas o ideal é ANTES da implementação.
5. **ADR órfão:** ADR sem índice, sem referência e sem revisão é documento perdido. Manter índice atualizado.
6. **Medo de depreciar:** Decisões mudam. Depreciar ou superceder um ADR é sinal de maturidade, não de erro.
7. **ADR demais:** Não é preciso ADR para cada decisão micro. Focar em decisões significativas e difíceis de reverter.
8. **Não referenciar em PRs:** Se a implementação não referencia o ADR, a rastreabilidade se perde.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/engineering-tech/architecture-patterns.md` | Escolha de padrão arquitetural é ADR obrigatório. |
| `frameworks/engineering-tech/build-vs-buy-framework.md` | Decisão de build vs buy gera ADR. |
| `frameworks/engineering-tech/dora-metrics.md` | ADRs podem incluir impacto esperado em DORA metrics. |
| `frameworks/engineering-tech/platform-engineering.md` | Decisões de plataforma interna são documentadas como ADRs. |
| `frameworks/operating-system/decision-memo-framework.md` | ADR é a versão tech do Decision Memo. Para decisões cross-funcional, usar Decision Memo. |
| `frameworks/operating-system/rasi-dri.md` | Cada ADR tem um DRI claro. |
| `checklists/tech-architecture-decision-quality.md` | Checklist para validar qualidade do ADR. |

---

## Referências

- Nygard, M. (2011). "Documenting Architecture Decisions." cognitect.com/blog.
- Keeling, M. (2017). *Design It!*. Pragmatic Programmers.
- Richards, M. & Ford, N. (2020). *Fundamentals of Software Architecture*. O'Reilly.
- ADR GitHub Template: github.com/joelparkerhenderson/architecture-decision-record.
- ThoughtWorks Technology Radar. "Lightweight Architecture Decision Records." (Adoção recomendada.)
