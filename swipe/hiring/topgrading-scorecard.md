---
source: "Who: The A Method for Hiring (Geoff Smart & Randy Street)"
date_captured: 2026-03-11
category: hiring
agents: [vision-chief, coo-orchestrator]
tags: [hiring, scorecard, topgrading, talent]
quality: gold
---

# Topgrading Scorecard — Framework de Referência

## Contexto

O método Topgrading, popularizado por Geoff Smart, é o padrão-ouro em
contratação executiva. A scorecard substitui a job description tradicional
por um documento orientado a outcomes.

## Estrutura da Scorecard

### 1. Missão do Cargo
Uma frase que define o propósito fundamental da posição.

**Exemplo (VP Engineering):**
> "Escalar a organização de engenharia de 30 para 120 pessoas em 18 meses,
> mantendo velocidade de entrega e qualidade acima de 99.5% uptime."

### 2. Outcomes (Resultados Esperados)
Lista de 5-8 resultados mensuráveis para os primeiros 12-18 meses.

| # | Outcome | Métrica | Prazo |
|---|---------|---------|-------|
| 1 | Reduzir tempo de deploy | De 2h para 15min | 6 meses |
| 2 | Implementar on-call rotation | 100% cobertura | 3 meses |
| 3 | Atingir hiring plan | 90 contratações | 12 meses |
| 4 | Reduzir turnover voluntário | < 10% anualizado | 12 meses |
| 5 | Implementar eng levels | Framework completo | 6 meses |

### 3. Competências
Behaviors e skills necessários para atingir os outcomes.

**Competências Universais:**
- Eficiência — faz mais com menos
- Honestidade/Integridade — padrão ético inabalável
- Organização/Planejamento — gerencia complexidade
- Proatividade — antecipa e age
- Follow-through — executa até o fim

**Competências Específicas:**
- Liderança técnica em escala
- Comunicação cross-funcional
- Gestão de stakeholders C-Level
- Decisão baseada em dados

### 4. Fit Cultural
Alinhamento com valores da organização — elimina candidatos tecnicamente
excelentes mas culturalmente destrutivos.

## O que Aprendemos

1. **Scorecards > Job Descriptions** — JDs descrevem atividades; scorecards
   descrevem resultados esperados
2. **Outcomes mensuráveis eliminam ambiguidade** — tanto para o candidato
   quanto para o hiring manager
3. **Competências são preditivas** — comportamentos passados são o melhor
   preditor de comportamentos futuros
4. **Fit cultural é eliminatório** — não compensável por excelência técnica

## Como Aplicar no C-Level Squad

- Usar scorecard como base para prompts do agente `vision-chief` ao
  avaliar estrutura de times
- Template disponível em `templates/people/hiring-scorecard.md`
- Integrar com o framework de succession planning em `tasks/people/`
- Toda posição senior deve ter scorecard antes de abrir vaga
