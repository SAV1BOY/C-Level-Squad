# AI Rollout — Fase 02: Build or Buy

## Objetivo desta Fase

Tomar a decisão estratégica entre construir internamente a solução de AI (build),
adquirir uma solução de mercado (buy), ou adotar uma abordagem híbrida, baseada numa
avaliação rigorosa de custos, capacidades, time-to-value, controle e risco. Esta decisão
tem implicações de longo prazo na estratégia tecnológica, competências internas e
estrutura de custos da organização. Decidir errado aqui custa meses e milhares de euros.

## Agentes Envolvidos

- **CTO Agent**: Lidera a avaliação técnica e apresenta recomendação fundamentada
- **CFO Agent**: Modela custos totais (TCO) de cada opção ao longo de 3-5 anos
- **CEO Agent**: Decide com base em alinhamento estratégico e vantagem competitiva
- **COO Agent**: Avalia impacto operacional de cada opção
- **CMO Agent**: Avalia impacto na experiência do cliente e diferenciação
- **CHRO Agent**: Avalia necessidades de contratação e upskilling por opção
- **Chief of Staff Agent**: Facilita o processo de decisão e documenta análise

## Inputs Necessários

1. Use Case Charters (output da Fase 00)
2. Data Readiness Report (output da Fase 01)
3. Inventário de soluções de mercado (vendors, plataformas, APIs)
4. Capacidades técnicas internas (equipa, infraestrutura, experiência ML)
5. Benchmark de mercado (o que concorrentes estão a usar)
6. Requisitos de performance, latency e scalability
7. Restrições de segurança, privacidade e data residency

## Processo (step-by-step)

1. **Requirements consolidation**: CTO Agent consolida os requisitos técnicos,
   funcionais e não-funcionais derivados do use case e data readiness assessment
2. **Build option assessment**: CTO Agent avalia a opção de construir internamente,
   incluindo stack tecnológica, timeline, equipa necessária e riscos técnicos
3. **Buy option market scan**: CTO Agent e COO Agent fazem um scan do mercado de
   soluções disponíveis, criando um shortlist de 3-5 vendors ou plataformas
4. **Vendor evaluation**: CTO Agent avalia cada vendor quanto a funcionalidade, fit
   técnico, integração com sistemas existentes, roadmap e referências
5. **TCO modeling**: CFO Agent modela o Total Cost of Ownership de cada opção ao longo
   de 3-5 anos, incluindo implementação, licenças, manutenção e evolução
6. **Strategic fit assessment**: CEO Agent avalia cada opção quanto a vantagem
   competitiva, diferenciação, controle sobre dados e dependência de terceiros
7. **People impact analysis**: CHRO Agent avalia as necessidades de contratação ou
   upskilling para cada opção, incluindo timeline de ramp-up
8. **Risk comparison**: Todos os agentes comparam os riscos de cada opção numa
   framework estruturada (técnico, financeiro, operacional, estratégico)
9. **Decision workshop**: Chief of Staff Agent facilita workshop de decisão com todos
   os agentes, usando weighted scoring para comparar opções objetivamente
10. **Decision documentation**: Chief of Staff Agent documenta a decisão, razões,
    trade-offs aceites e plano de implementação da opção escolhida

## Outputs / Entregáveis

- **Build vs Buy Analysis**: Documento comparativo detalhado das opções
- **Vendor Shortlist and Evaluation**: Avaliação estruturada dos vendors considerados
- **TCO Model**: Modelo de custo total por opção (3-5 anos)
- **Decision Document**: Decisão formal com justificação e trade-offs aceites
- **Implementation Plan (Draft)**: Plano preliminar para a opção escolhida
- **Risk Comparison Matrix**: Comparação de riscos por opção
- **Talent Plan**: Plano de contratação/upskilling baseado na opção escolhida

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-02.1 | Pelo menos 3 vendors avaliados se opção buy é considerada | CTO Agent |
| QG-02.2 | TCO modelado para 3+ anos com pressupostos explícitos | CFO Agent |
| QG-02.3 | POC ou demo realizada para opção preferida | CTO Agent |
| QG-02.4 | Impacto em segurança e privacidade avaliado para cada opção | CTO Agent |
| QG-02.5 | Decisão tomada com consensus ou maioria qualificada | CEO Agent |
| QG-02.6 | Plano de implementação preliminar viável com recursos disponíveis | COO Agent |

## Critérios para Avançar

Para progredir para a Fase 03 (Pilot), todos os critérios devem ser satisfeitos:

- [ ] Decisão build/buy/hybrid tomada e documentada
- [ ] TCO aprovado e budget alocado pelo CFO Agent
- [ ] Equipa identificada para implementação (interna ou vendor)
- [ ] Plano de implementação preliminar acordado
- [ ] Contratos com vendors negociados (se buy/hybrid)
- [ ] Riscos da opção escolhida documentados com mitigações

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Viés "build" por orgulho de engenharia | Alta | Alto | Incluir perspetiva financeira e time-to-value |
| Vendor lock-in com solução proprietária | Média | Alto | Avaliar portabilidade e exit strategies |
| Subestimar complexidade de build | Alta | Crítico | Buffer de 50% em estimativas de tempo e custo |
| Vendor não cumpre promessas comerciais | Média | Alto | POC obrigatória com dados reais antes de contrato |
| Decisão sem dados suficientes (analysis paralysis) | Média | Médio | Timebox de 10 dias para a decisão |

## Templates a Usar

- `templates/build-vs-buy-analysis.md` — Framework de análise build vs buy
- `templates/vendor-evaluation.md` — Template de avaliação de vendors
- `templates/tco-model.md` — Modelo de Total Cost of Ownership
- `templates/decision-document.md` — Documento de decisão estruturado

## Duração Estimada

- **Mínimo**: 5 dias úteis (decisão clara com poucas opções)
- **Típico**: 10-15 dias úteis
- **Máximo**: 20 dias úteis (incluindo POC com vendor)

> **Nota**: Não existe opção perfeita. Build dá controle mas custa tempo. Buy dá
> velocidade mas custa independência. A melhor decisão é a que equilibra estes trade-offs
> no contexto específico da organização.
