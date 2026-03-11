# Benchmarks: Métricas de Engenharia

## Visão Geral

Este documento compila benchmarks para métricas de engenharia de software, cobrindo produtividade, qualidade, velocidade e saúde da equipe. Os ranges são baseados em pesquisas como DORA (DevOps Research and Assessment), State of DevOps Report, LinearB, Sleuth, Haystack e dados internos de empresas de tecnologia. Use como referência para avaliar a saúde da engenharia e identificar oportunidades de melhoria.

## DORA Metrics (DevOps Research and Assessment)

### As Quatro Métricas DORA
As métricas DORA são o padrão de mercado para medir a performance de entrega de software, validadas por pesquisa rigorosa com milhares de equipes.

#### 1. Deployment Frequency (Frequência de Deploy)
| Performance | Frequência |
|-------------|-----------|
| Elite | Sob demanda (múltiplas vezes por dia) |
| High | 1 vez por dia a 1 vez por semana |
| Medium | 1 vez por semana a 1 vez por mês |
| Low | 1 vez por mês a 1 vez por semestre |

**Como medir:** Número de deploys em produção / período

#### 2. Lead Time for Changes (Tempo de Entrega)
| Performance | Lead Time |
|-------------|-----------|
| Elite | <1 hora |
| High | 1 dia a 1 semana |
| Medium | 1 semana a 1 mês |
| Low | 1 mês a 6 meses |

**Como medir:** Tempo do primeiro commit até produção

#### 3. Change Failure Rate (Taxa de Falha de Mudanças)
| Performance | Taxa de Falha |
|-------------|--------------|
| Elite | 0-5% |
| High | 5-10% |
| Medium | 10-15% |
| Low | >15% |

**Como medir:** Deploys que causam incidente / total de deploys

#### 4. Time to Restore Service (Tempo de Restauração)
| Performance | MTTR |
|-------------|------|
| Elite | <1 hora |
| High | <1 dia |
| Medium | 1 dia a 1 semana |
| Low | >1 semana |

**Como medir:** Tempo médio entre detecção do incidente e restauração do serviço

## Métricas de Fluxo de Desenvolvimento

### Cycle Time (Tempo de Ciclo)
```
Cycle Time = Tempo do início do trabalho até merge em produção

Benchmarks:
- Elite: <1 dia
- Bom: 1-3 dias
- Mediano: 3-7 dias
- Lento: >7 dias

Decomposição:
- Coding time: tempo escrevendo código
- Pickup time: tempo até revisão começar
- Review time: tempo em code review
- Deploy time: tempo até produção

Fonte: LinearB, Sleuth
```

### PR Size (Tamanho de Pull Request)
```
Benchmarks:
- Ideal: <200 linhas de código alteradas
- Aceitável: 200-400 linhas
- Grande: 400-1000 linhas
- Muito grande: >1000 linhas (deve ser quebrado)

Impacto: PRs maiores têm review mais lento e mais bugs
Fonte: Google Engineering Practices, LinearB
```

### Review Time (Tempo de Code Review)
```
Benchmarks:
- Elite: <2 horas (média)
- Bom: 2-8 horas
- Mediano: 8-24 horas
- Lento: >24 horas

Meta: Primeiro review em <4 horas durante horário de trabalho
Fonte: LinearB, Google
```

### Work in Progress (WIP)
```
Benchmarks por desenvolvedor:
- Ideal: 1-2 PRs abertos simultaneamente
- Aceitável: 2-3 PRs
- Alto: >3 PRs (context switching, gargalo)

Impacto: Alto WIP correlaciona com maior cycle time
```

## Métricas de Qualidade

### Bug Rate
```
Benchmarks:
- Bugs por 1000 linhas de código (KLOC):
  - Excelente: <1 bug/KLOC
  - Bom: 1-5 bugs/KLOC
  - Aceitável: 5-10 bugs/KLOC
  - Ruim: >10 bugs/KLOC

- Bugs por sprint:
  - Baixo: <5% do backlog é bugs
  - Médio: 5-15% do backlog é bugs
  - Alto: >15% do backlog é bugs (provavelmente débito técnico)
```

### Test Coverage
```
Benchmarks:
- Excelente: >80% code coverage
- Bom: 60-80%
- Aceitável: 40-60%
- Baixo: <40%

Nota: Coverage alto não garante qualidade de testes
Foco deve ser em testes de paths críticos, não % puro
```

### Uptime / Availability
```
Benchmarks (SLA):
- 99.99% ("four nines"): 52 min downtime/ano — top tier
- 99.95%: 4.4 horas downtime/ano — excelente
- 99.9% ("three nines"): 8.8 horas/ano — bom para maioria
- 99.5%: 1.8 dias/ano — aceitável para não-crítico
- 99%: 3.7 dias/ano — abaixo do padrão para SaaS

Fonte: AWS, Google Cloud SLAs
```

### Incident Metrics
```
- MTBF (Mean Time Between Failures): tempo médio entre incidentes
  Bom: >30 dias para P1

- MTTA (Mean Time to Acknowledge): tempo para reconhecer incidente
  Bom: <15 minutos para P1

- MTTR (Mean Time to Resolve): tempo para resolver
  Bom: <4 horas para P1, <24h para P2

- SEV1/P1 por mês:
  Bom: 0-1
  Aceitável: 2-3
  Preocupante: >4
```

## Métricas de Produtividade

### Velocity e Throughput
```
Cuidado: velocity é uma métrica de planejamento, não de produtividade

Métricas mais úteis:
- Throughput: itens concluídos por sprint (tendência, não valor absoluto)
- Deployment frequency: deploys por semana por equipe
- Story points entregues: usar para previsibilidade, não para comparar equipes
```

### Developer Experience (DX)
```
Métricas de pesquisa (survey-based):
- Satisfação do desenvolvedor (eNPS): >30 é bom
- Facilidade de onboarding: novo dev produtivo em <30 dias é bom
- Build time local: <5 minutos é bom, >15 minutos é ruim
- CI pipeline time: <15 minutos é bom, >30 minutos é ruim
- "Ease of shipping": percepção de facilidade de entregar

Fonte: DX survey, Spotify Engineering
```

## Métricas Organizacionais

### Ratio de Engenharia
```
Benchmarks por estágio:
- Seed/Series A: 60-80% da empresa é engenharia
- Series B: 40-60%
- Series C+: 30-50%
- Scale (>500 pessoas): 25-40%

Engineering Manager span of control:
- Ideal: 5-8 reports diretos
- Aceitável: 4-10
- Preocupante: >12 (muito amplo) ou <3 (muito caro)
```

### Investimento por Categoria
```
Benchmarks de alocação de engenharia:
- New features: 40-60%
- Manutenção e bugs: 15-25%
- Débito técnico: 10-20%
- Infraestrutura e plataforma: 10-20%
- Experimentação/R&D: 5-10%

Se manutenção > 30%: provavelmente muito débito técnico acumulado
Se new features > 70%: provavelmente gerando débito técnico
```

## Fontes de Referência
- DORA / State of DevOps Report (Google)
- LinearB Engineering Benchmarks
- Sleuth DORA Metrics
- Haystack Analytics
- Accelerate (Forsgren, Humble, Kim)
- DX Developer Experience survey
- Spotify Engineering Culture
- Google Engineering Practices
