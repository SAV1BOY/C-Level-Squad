# Modelo de Maturidade AI — Framework de Evolução em Inteligência Artificial

## Propósito e Contexto

O modelo de maturidade AI ajuda organizações a entenderem onde estão na jornada de adoção de
inteligência artificial e o que precisam construir para avançar ao próximo nível. A maioria das
empresas superestima sua maturidade em AI (confundem usar ChatGPT com ter capacidade de AI) e
subestima o investimento necessário em fundações (dados, infra, governança) antes de colher
resultados significativos.

Este framework fornece uma avaliação honesta em 5 dimensões, um roadmap de evolução por estágio,
e critérios claros de quando investir mais agressivamente vs. quando fortalecer fundações. O CAIO
(Chief AI Officer) usa este modelo para comunicar progresso ao board, priorizar investimentos e
alinhar expectativas sobre timeline de impacto.

## Quando Usar

- Na definição da estratégia de AI da organização
- Em apresentações para board sobre investimentos em AI
- Na contratação de talentos de AI (entender que nível de maturidade atrai quais perfis)
- Ao avaliar companhias para M&A ou investimento (due diligence de AI)
- Quando há frustração com resultados de AI (geralmente diagnóstico de maturidade errado)
- No planejamento anual de investimento em dados e AI

## Componentes do Framework

### 1. Os 5 Níveis de Maturidade

**Nível 1: AI Curious**
- Uso individual de ferramentas de AI (ChatGPT, Copilot)
- Sem estratégia de AI formal
- Dados em silos, sem pipeline de ML
- Talento: generalistas curiosos, sem ML engineers
- Impacto: produtividade individual, não organizacional

**Nível 2: AI Experimental**
- Primeiros POCs de AI/ML com resultados localizados
- Data pipeline básica implementada
- 1-3 modelos em produção (simples: classificação, recomendação)
- Talento: 1-2 data scientists ou ML engineers
- Impacto: automação de tarefas específicas

**Nível 3: AI Operacional**
- AI integrada em processos core do negócio
- MLOps implementado (versionamento, monitoring, retraining)
- Feature store e data platform maduros
- Talento: time de ML dedicado (5-15 pessoas)
- Impacto: melhoria mensurável em métricas de negócio

**Nível 4: AI Estratégico**
- AI como diferencial competitivo reconhecido
- Múltiplos modelos em produção, A/B testing de modelos
- Governança de AI implementada (bias, fairness, explicabilidade)
- Talento: organização de AI com ML engineers, MLOps, researchers
- Impacto: novos produtos e capabilities baseados em AI

**Nível 5: AI Native**
- AI permeia todas as decisões e processos
- Autonomous systems em produção
- Research capabilities (contribuindo para estado da arte)
- AI governance como parte da cultura
- Impacto: moat competitivo baseado em AI/dados

### 2. As 5 Dimensões de Avaliação

| Dimensão | Nível 1 | Nível 3 | Nível 5 |
|----------|---------|---------|---------|
| **Dados** | Silos, sem pipeline | Data platform, quality | Data mesh, real-time |
| **Talento** | Generalistas | Time dedicado | Organização de AI |
| **Infraestrutura** | Notebooks locais | MLOps básico | ML Platform completa |
| **Governança** | Inexistente | Políticas definidas | Automatizada |
| **Impacto** | Individual | Processos específicos | Organização inteira |

### 3. Pré-requisitos por Nível

Para avançar de nível, os pré-requisitos do nível anterior precisam estar sólidos:

**1→2:** Dados básicos acessíveis, primeiro ML engineer contratado, sponsor executivo
**2→3:** Data platform funcional, MLOps básico, business alignment claro
**3→4:** Feature store maduro, governança implementada, ROI demonstrado
**4→5:** Cultura data-driven, research capability, AI embedded em produto

## Processo Passo-a-Passo

### Fase 1: Assessment (1-2 semanas)
1. Avaliar cada uma das 5 dimensões honestamente (1-5)
2. Identificar o nível limitante (a dimensão mais baixa limita o todo)
3. Mapear iniciativas de AI existentes e seu status
4. Benchmarking com empresas comparáveis do setor

### Fase 2: Target Setting (1 semana)
1. Definir target de maturidade para 12-18 meses (subir 1 nível é ambicioso)
2. Identificar gaps por dimensão entre atual e target
3. Priorizar dimensões limitantes primeiro (fundação antes de inovação)
4. Estimar investimento necessário (pessoas, infra, dados)

### Fase 3: Roadmap (2 semanas)
1. Quick wins: onde AI pode gerar valor com a maturidade atual
2. Foundational: investimentos em dados e infra necessários
3. Strategic: iniciativas de AI que requerem maturidade mais alta
4. Milestones trimestrais com métricas de progresso

### Fase 4: Execução e Medição
1. Review mensal de progresso em cada dimensão
2. ROI tracking de cada iniciativa de AI
3. Re-assessment semestral completo
4. Ajuste de roadmap baseado em learnings

## Template de AI Maturity Assessment

```markdown
# AI Maturity Assessment — [Empresa] — [Data]

## Score por Dimensão
| Dimensão | Score (1-5) | Evidência |
|----------|-------------|-----------|
| Dados | ___ | [justificativa] |
| Talento | ___ | [justificativa] |
| Infraestrutura | ___ | [justificativa] |
| Governança | ___ | [justificativa] |
| Impacto | ___ | [justificativa] |

## Nível Geral: [Menor score entre as dimensões]

## Dimensão Limitante: [Qual dimensão é o bottleneck]

## Gap Analysis
[Para cada dimensão, o que falta para o próximo nível]

## Roadmap Proposto
[Iniciativas priorizadas com timeline e investimento]
```

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Maturity score médio | Subir 1 nível em 12-18 meses | Semestral |
| Modelos em produção | Crescimento trimestral | Trimestral |
| AI revenue impact | Mensurável e crescente | Trimestral |
| Data quality score | > 90% nos datasets de ML | Mensal |
| ML engineer retention | > 90% anual | Anual |
| Time-to-production (novo modelo) | Tendência decrescente | Por modelo |

## Armadilhas

1. **Pular níveis** — Tentar Nível 4 sem ter Nível 2 sólido em dados
2. **AI theater** — POCs que nunca vão para produção
3. **Hire-first** — Contratar PhDs antes de ter dados e infra prontos
4. **Hype-driven** — Investir em AI porque "todo mundo está fazendo"
5. **Medir atividade, não impacto** — "Temos 10 modelos" vs. "AI gera R$X de valor"

## Referências Cruzadas

- `frameworks/caio-architect/responsible-ai.md` — Governança como dimensão de maturidade
- `frameworks/caio-architect/ai-product-development.md` — Desenvolvimento de produtos de AI
- `frameworks/caio-architect/mlops-framework.md` — Infraestrutura de ML
- `frameworks/caio-architect/ai-governance.md` — Governança detalhada
- `frameworks/cio-engineer/data-platform.md` — Fundação de dados para AI
- `frameworks/cto-architect/tech-radar.md` — Tecnologias de AI no radar
- `frameworks/vision-chief/competitive-moat-analysis.md` — AI como moat competitivo
