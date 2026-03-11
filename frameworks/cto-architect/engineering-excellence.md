# Framework de Excelência em Engenharia — Cultura, Práticas e Métricas

## Propósito e Contexto

Excelência em engenharia não é perfeição técnica — é a capacidade consistente de entregar
software de alta qualidade, de forma sustentável, com velocidade crescente ao longo do tempo.
É o resultado de cultura (como pensamos), práticas (como trabalhamos) e métricas (como
medimos). Organizações com excelência em engenharia atraem melhores talentos, entregam mais
rápido, têm menos incidentes e mantêm a moral alta mesmo sob pressão.

Este framework organiza as dimensões de excelência em engenharia, fornece um modelo de
maturidade para auto-avaliação e estabelece um roadmap para evolução contínua. Não é
prescritivo sobre tecnologias — é prescritivo sobre práticas e princípios.

Inspiração: DORA metrics (Google), Engineering Effectiveness (Stripe), Developer Joy (Spotify).

## Quando Usar

- Na construção da cultura de engenharia de uma nova organização
- Em avaliações periódicas de maturidade de engenharia (semestral)
- Ao diagnosticar problemas de entrega, qualidade ou retenção de talentos
- Na definição de investimentos em developer experience e tooling
- Em processos de due diligence técnica
- No planejamento de scaling da equipe de engenharia

## Componentes do Framework

### 1. Os 6 Pilares de Excelência

**Pilar 1: Entrega Contínua (Delivery)**
- Deploy frequency: múltiplas vezes por dia como alvo
- Lead time for changes: < 1 dia (commit → produção)
- Change failure rate: < 5%
- Mean time to recovery (MTTR): < 1 hora
- Práticas: trunk-based development, feature flags, canary deploys, CI/CD automatizado

**Pilar 2: Qualidade de Código (Craft)**
- Code review como prática universal (100% do código é revisado)
- Test coverage significativo (não 100%, mas cobertura dos paths críticos)
- Documentação como código (ADRs, READMEs atualizados, API docs geradas)
- Linting e formatting automatizados (zero debates de estilo)
- Práticas: pair/mob programming, refactoring contínuo, design reviews

**Pilar 3: Observabilidade (Reliability)**
- Logging estruturado em todos os serviços
- Métricas de negócio e técnicas expostas
- Distributed tracing para debug cross-service
- Alertas baseados em SLOs (não thresholds arbitrários)
- Práticas: SLO-based alerting, error budgets, chaos engineering, runbooks

**Pilar 4: Segurança (Security)**
- Shift-left: segurança incorporada no desenvolvimento, não bolt-on
- Dependency scanning automatizado
- Secrets management centralizado
- Least privilege como default
- Práticas: threat modeling, security champions por time, pen testing regular

**Pilar 5: Developer Experience (DX)**
- Tempo de setup de ambiente < 30 minutos
- Build time local < 5 minutos
- Documentação interna searchable e atualizada
- Ferramentas internas tratadas como produto (com UX)
- Práticas: developer surveys, DX team, golden paths, internal tech talks

**Pilar 6: Cultura de Engenharia (Culture)**
- Blameless post-mortems após incidentes
- Technical career ladder clara (IC track e management track)
- Tempo protegido para aprendizado e experimentação
- Feedback técnico frequente e construtivo
- Práticas: guilds/chapters, tech talks internos, hack days, RFCs abertos

### 2. Modelo de Maturidade (por pilar)

**Nível 1 — Inicial:** Processos ad hoc, dependem de heróis individuais
**Nível 2 — Repetível:** Práticas básicas estabelecidas, mas inconsistentes entre times
**Nível 3 — Definido:** Padrões documentados e seguidos por todos os times
**Nível 4 — Gerenciado:** Métricas coletadas e usadas para melhoria contínua
**Nível 5 — Otimizado:** Melhoria contínua é parte do DNA; organização como referência

### 3. Assessment Matrix

| Pilar | Nível Atual | Nível Alvo (12m) | Gap | Prioridade |
|-------|-------------|-------------------|-----|------------|
| Entrega Contínua | ___ | ___ | ___ | ___ |
| Qualidade de Código | ___ | ___ | ___ | ___ |
| Observabilidade | ___ | ___ | ___ | ___ |
| Segurança | ___ | ___ | ___ | ___ |
| Developer Experience | ___ | ___ | ___ | ___ |
| Cultura | ___ | ___ | ___ | ___ |

## Processo Passo-a-Passo

### Fase 1: Assessment (2 semanas)
1. Aplicar survey anônimo com todos os engenheiros
2. Coletar métricas DORA automaticamente (via CI/CD)
3. Entrevistar tech leads e engineering managers
4. Preencher a Assessment Matrix com liderança técnica

### Fase 2: Priorização (1 semana)
1. Identificar os 2-3 pilares com maior gap e maior impacto
2. Definir iniciativas concretas para cada pilar priorizado
3. Estimar investimento (tempo, ferramentas, headcount)
4. Alinhar com roadmap de produto (não pode ser 100% separado)

### Fase 3: Execução (trimestres)
1. Cada iniciativa tem um champion e métricas de progresso
2. Quick wins nos primeiros 30 dias (ex: setup linting, primeiro SLO)
3. Investimentos médios em 60-90 dias (ex: CI/CD pipeline, observabilidade)
4. Transformações culturais em 6-12 meses (ex: blameless culture, career ladder)

### Fase 4: Medição e Iteração
1. Re-assessment semestral com mesma metodologia
2. Celebrar progressos — engineering excellence precisa de momentum
3. Compartilhar resultados com toda a organização (não só engenharia)
4. Ajustar prioridades baseado em dados

## Checklist de Excelência (Quick Scan)

- [ ] Todo código passa por code review antes de merge?
- [ ] Existe CI/CD automatizado para todos os serviços?
- [ ] Deploy para produção acontece pelo menos semanalmente?
- [ ] Existe monitoramento e alertas configurados para serviços críticos?
- [ ] Post-mortems são conduzidos sem blame após incidentes?
- [ ] Novo engenheiro faz primeiro deploy em < 1 semana?
- [ ] Existe career ladder técnica documentada?
- [ ] Dependências são atualizadas regularmente (< 2 versões atrás)?
- [ ] Existe processo de threat modeling para features sensíveis?
- [ ] Developer survey é aplicado pelo menos semestralmente?

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Deploy Frequency | Múltiplos por dia por time | Semanal |
| Lead Time for Changes | < 1 dia | Semanal |
| Change Failure Rate | < 5% | Mensal |
| MTTR | < 1 hora | Por incidente |
| Developer NPS | > 40 | Semestral |
| Engineering Attrition | < 10% anual | Trimestral |
| Time to First Deploy (novos eng) | < 5 dias | Por onboarding |

## Referências Cruzadas

- `frameworks/cto-architect/tech-radar.md` — Stack tecnológica e práticas aprovadas
- `frameworks/cto-architect/tech-debt-management.md` — Debt como barreira para excelência
- `frameworks/cto-architect/platform-strategy.md` — Plataforma como enabler de DX
- `frameworks/cio-engineer/security-posture.md` — Pilar de segurança em profundidade
- `frameworks/cio-engineer/it-service-management.md` — Gestão de incidentes
- `frameworks/caio-architect/mlops-framework.md` — Excelência aplicada a ML
- `frameworks/shared/change-leadership.md` — Liderar mudança cultural em engenharia
