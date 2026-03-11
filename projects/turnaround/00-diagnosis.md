# Turnaround — Fase 00: Diagnóstico

## Objetivo desta Fase

Realizar um diagnóstico rápido e abrangente da situação atual da empresa ou unidade de
negócio em crise, identificando as causas raiz dos problemas, a gravidade financeira e
operacional, e o horizonte temporal disponível antes de um ponto de não retorno. O
diagnóstico deve ser brutalmente honesto, baseado em dados e livre de viés político.
Velocidade é crítica nesta fase — cada dia conta quando a organização está em dificuldade.

## Agentes Envolvidos

- **CEO Agent**: Comissiona o diagnóstico e garante acesso irrestrito a informação
- **CFO Agent**: Lidera a análise financeira, cash flow e runway disponível
- **COO Agent**: Avalia a saúde operacional, eficiência e capacidade de entrega
- **CTO Agent**: Diagnostica a saúde tecnológica e riscos de infraestrutura
- **CMO Agent**: Analisa posição de mercado, percepção de marca e pipeline de vendas
- **CHRO Agent**: Avalia moral da equipa, retenção de talento crítico e cultura
- **Chief of Staff Agent**: Coordena o diagnóstico e consolida findings

## Inputs Necessários

1. Demonstrações financeiras dos últimos 12-24 meses (P&L, Balance Sheet, Cash Flow)
2. KPIs operacionais com tendência temporal
3. Pipeline de vendas e projeções de revenue
4. Dados de churn de clientes e de colaboradores
5. Contratos e obrigações legais vigentes
6. Dados de mercado e posição competitiva
7. Feedback não filtrado de colaboradores chave e clientes

## Processo (step-by-step)

1. **Declaração de urgência**: CEO Agent declara formalmente o estado de urgência e
   concede poderes extraordinários para acesso a dados e tomada de decisão rápida
2. **Financial deep-dive**: CFO Agent analisa cash position, burn rate, runway, dívidas,
   obrigações e identifica o "cash zero date" — a data em que o dinheiro acaba
3. **Revenue analysis**: CMO Agent e CFO Agent analisam a decomposição de revenue por
   cliente, produto e canal, identificando concentrações perigosas e tendências
4. **Cost structure analysis**: CFO Agent e COO Agent mapeiam todos os custos fixos e
   variáveis, identificando oportunidades imediatas de redução
5. **Operational health check**: COO Agent avalia processos críticos, identifica
   bottlenecks, ineficiências e riscos operacionais imediatos
6. **Technology assessment**: CTO Agent avalia estabilidade de sistemas críticos,
   riscos de segurança e dívida técnica que possa causar falhas
7. **People assessment**: CHRO Agent mede engagement, identifica flight risks de
   talento crítico e avalia a capacidade da organização para executar mudanças
8. **Market position review**: CMO Agent avalia posicionamento competitivo, tendências
   de mercado e percepção dos clientes sobre a empresa
9. **Synthesis e priorização**: Chief of Staff Agent consolida todos os findings num
   diagnóstico integrado, classificando problemas por urgência e impacto

## Outputs / Entregáveis

- **Diagnostic Report**: Relatório executivo com findings consolidados e classificados
- **Cash Flow Projection**: Projeção de cash flow para 90 dias com cenários
- **Problem Hierarchy**: Classificação de problemas por urgência e impacto (matriz)
- **Root Cause Map**: Mapa visual de causas raiz e interdependências
- **Critical Risk Register**: Riscos que ameaçam a sobrevivência da organização
- **Quick Wins List**: Ações de impacto imediato que podem ser executadas em <1 semana
- **Runway Assessment**: Tempo disponível antes do ponto de não retorno

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-00.1 | Cash position verificada e reconciliada com extratos bancários | CFO Agent |
| QG-00.2 | Top 5 problemas consensuais entre todos os agentes | CEO Agent |
| QG-00.3 | Root cause analysis completada (não apenas sintomas) | Chief of Staff |
| QG-00.4 | Runway calculado com 3 cenários (otimista, base, pessimista) | CFO Agent |
| QG-00.5 | Feedback de pelo menos 10 stakeholders internos recolhido | CHRO Agent |
| QG-00.6 | Diagnóstico completado em menos de 5 dias úteis | Chief of Staff |

## Critérios para Avançar

Para progredir para a Fase 01 (Triage), todos os critérios devem ser satisfeitos:

- [ ] Diagnóstico completo apresentado a todos os agentes
- [ ] Cash runway quantificado e aceite pelo CFO Agent
- [ ] Problemas priorizados por urgência e impacto
- [ ] Quick wins identificados com owners atribuídos
- [ ] Nenhum agente discorda dos findings factuais (opiniões sobre soluções podem divergir)
- [ ] Comunicação interna sobre o estado da situação preparada

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Dados financeiros incompletos ou incorretos | Alta | Crítico | Verificação cruzada com múltiplas fontes |
| Resistência interna a partilhar informação real | Alta | Alto | CEO Agent garante ambiente de transparência total |
| Diagnóstico demasiado lento face à urgência | Média | Crítico | Timebox absoluto de 5 dias |
| Foco em sintomas em vez de causas raiz | Alta | Alto | Usar técnica "5 Whys" sistematicamente |
| Pânico desnecessário por diagnóstico alarmista | Média | Alto | Basear tudo em dados verificáveis |

## Templates a Usar

- `templates/turnaround-diagnostic.md` — Template de diagnóstico de turnaround
- `templates/cash-flow-projection.md` — Projeção de cash flow a 90 dias
- `templates/root-cause-map.md` — Mapa de causas raiz
- `templates/urgency-impact-matrix.md` — Matriz de urgência vs impacto

## Duração Estimada

- **Mínimo**: 2 dias úteis (crise aguda com dados acessíveis)
- **Típico**: 3-5 dias úteis
- **Máximo**: 7 dias úteis (nunca mais, dados os constrangimentos de tempo)

> **Nota**: Num turnaround, velocidade supera perfeição. Um diagnóstico 80% correto em
> 3 dias é infinitamente mais valioso que um diagnóstico 95% correto em 3 semanas.
