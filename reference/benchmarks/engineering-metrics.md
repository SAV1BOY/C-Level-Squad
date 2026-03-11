# Benchmarks: Metricas de Engenharia

## Visao Geral

Este documento compila benchmarks para metricas de engenharia de software, cobrindo produtividade, qualidade, velocidade e saude da equipe. Os ranges sao baseados em pesquisas como DORA, State of DevOps Report e dados internos de empresas de tecnologia.

## DORA Metrics (DevOps Research and Assessment)

### 1. Deployment Frequency (Frequencia de Deploy)
| Performance | Frequencia |
|-------------|-----------|
| Elite | Sob demanda (multiplas vezes por dia) |
| High | 1 vez por dia a 1 vez por semana |
| Medium | 1 vez por semana a 1 vez por mes |
| Low | 1 vez por mes a 1 vez por semestre |

**Como medir:** Numero de deploys em producao / periodo

### 2. Lead Time for Changes (Tempo de Entrega)
| Performance | Lead Time |
|-------------|-----------|
| Elite | Menos de 1 hora |
| High | 1 dia a 1 semana |
| Medium | 1 semana a 1 mes |
| Low | 1 mes a 6 meses |

**Como medir:** Tempo do primeiro commit ate producao

### 3. Change Failure Rate (Taxa de Falha)
| Performance | Taxa de Falha |
|-------------|--------------|
| Elite | 0-5% |
| High | 5-10% |
| Medium | 10-15% |
| Low | Acima de 15% |

**Como medir:** Deploys que causam incidente / total de deploys

### 4. Time to Restore Service (Tempo de Restauracao)
| Performance | MTTR |
|-------------|------|
| Elite | Menos de 1 hora |
| High | Menos de 1 dia |
| Medium | 1 dia a 1 semana |
| Low | Mais de 1 semana |

## Metricas de Fluxo de Desenvolvimento

### Cycle Time (Tempo de Ciclo)
- Elite: menos de 1 dia
- Bom: 1-3 dias
- Mediano: 3-7 dias
- Lento: mais de 7 dias

Decomposicao: coding time + pickup time + review time + deploy time

### PR Size (Tamanho de Pull Request)
- Ideal: menos de 200 linhas alteradas
- Aceitavel: 200-400 linhas
- Grande: 400-1000 linhas
- Muito grande: mais de 1000 linhas (deve ser quebrado)

### Review Time (Tempo de Code Review)
- Elite: menos de 2 horas (media)
- Bom: 2-8 horas
- Mediano: 8-24 horas
- Lento: mais de 24 horas

### Work in Progress (WIP) por Desenvolvedor
- Ideal: 1-2 PRs abertos simultaneamente
- Aceitavel: 2-3 PRs
- Alto: mais de 3 PRs (context switching excessivo)

## Metricas de Qualidade

### Bug Rate
- Excelente: menos de 1 bug por 1000 linhas de codigo
- Bom: 1-5 bugs/KLOC
- Aceitavel: 5-10 bugs/KLOC
- Ruim: mais de 10 bugs/KLOC

### Test Coverage
- Excelente: acima de 80%
- Bom: 60-80%
- Aceitavel: 40-60%
- Baixo: abaixo de 40%

### Uptime / Disponibilidade
- 99.99% (four nines): 52 min downtime/ano
- 99.95%: 4.4 horas downtime/ano
- 99.9% (three nines): 8.8 horas/ano
- 99.5%: 1.8 dias/ano
- 99%: 3.7 dias/ano

### Metricas de Incidentes
- MTBF (Mean Time Between Failures): bom se acima de 30 dias para P1
- MTTA (Mean Time to Acknowledge): bom se abaixo de 15 minutos para P1
- MTTR (Mean Time to Resolve): bom se abaixo de 4 horas para P1
- SEV1 por mes: 0-1 bom, 2-3 aceitavel, acima de 4 preocupante

## Metricas de Produtividade

### Developer Experience (DX)
- Satisfacao do desenvolvedor (eNPS): acima de 30 e bom
- Onboarding: novo dev produtivo em menos de 30 dias e bom
- Build time local: menos de 5 minutos e bom
- CI pipeline time: menos de 15 minutos e bom

## Metricas Organizacionais

### Ratio de Engenharia por Estagio
- Seed/Series A: 60-80% da empresa e engenharia
- Series B: 40-60%
- Series C+: 30-50%
- Scale (mais de 500 pessoas): 25-40%

### Alocacao de Engenharia
- New features: 40-60%
- Manutencao e bugs: 15-25%
- Debito tecnico: 10-20%
- Infraestrutura: 10-20%
- R&D: 5-10%

## Fontes de Referencia
- DORA / State of DevOps Report (Google)
- LinearB Engineering Benchmarks
- Accelerate (Forsgren, Humble, Kim)
- DX Developer Experience survey
