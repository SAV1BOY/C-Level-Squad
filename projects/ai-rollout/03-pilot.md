# AI Rollout — Fase 03: Piloto

## Objetivo desta Fase

Implementar e testar a solução de AI num ambiente controlado com utilizadores reais,
validando que a solução funciona conforme esperado, que os resultados são de qualidade
aceitável e que o processo de integração nos workflows existentes é viável. O piloto
é o teste de realidade — transforma expectativas teóricas em evidência empírica que
fundamenta a decisão de escalar ou pivotar. Um piloto bem desenhado minimiza risco e
maximiza aprendizagem com investimento controlado.

## Agentes Envolvidos

- **CTO Agent**: Lidera a implementação técnica do piloto e monitorização de performance
- **COO Agent**: Coordena a integração nos processos operacionais e recruta pilot users
- **CMO Agent**: Avalia impacto na experiência do cliente (se aplicável)
- **CFO Agent**: Monitoriza custos do piloto e valida unit economics preliminares
- **CHRO Agent**: Gere o change management e formação dos pilot users
- **CEO Agent**: Remove bloqueios e garante suporte organizacional ao piloto
- **Chief of Staff Agent**: Coordena o piloto e documenta resultados

## Inputs Necessários

1. Decisão build/buy documentada (output da Fase 02)
2. Datasets preparados e validados (output da Fase 01)
3. Solução implementada ou configurada (modelo treinado, API integrada, etc.)
4. Grupo de pilot users identificado e comprometido
5. Métricas de sucesso do piloto definidas (KPIs e thresholds)
6. Workflow atual documentado (para comparação antes/depois)
7. Plano de formação para pilot users

## Processo (step-by-step)

1. **Pilot scope definition**: CTO Agent e COO Agent definem o escopo exato do piloto:
   quem participa, que processos são afetados, durante quanto tempo e com que métricas
2. **Environment setup**: CTO Agent configura o ambiente de piloto, que pode ser uma
   instância separada ou um feature flag em produção com rollout controlado
3. **Pilot user training**: CHRO Agent e CTO Agent conduzem sessões de formação para
   os pilot users, explicando como usar a solução e como dar feedback
4. **Baseline measurement**: COO Agent captura métricas baseline dos processos atuais
   (sem AI) para comparação objetiva com os resultados do piloto
5. **Pilot launch**: CTO Agent ativa a solução de AI para o grupo piloto, monitorizando
   de perto a performance técnica nas primeiras horas e dias
6. **Daily monitoring**: CTO Agent monitoriza métricas técnicas diariamente (latency,
   accuracy, error rates) e COO Agent acompanha adoção e feedback dos users
7. **Weekly check-ins**: Chief of Staff Agent facilita check-ins semanais com pilot
   users para recolher feedback qualitativo e identificar issues
8. **Iterative improvements**: CTO Agent implementa melhorias incrementais baseadas
   no feedback, documentando cada alteração e o seu impacto
9. **Results analysis**: Após o período definido, todos os agentes analisam os
   resultados quantitativos e qualitativos do piloto
10. **Pilot decision**: CEO Agent lidera a decisão de scale, pivot ou stop baseada
    nos resultados objetivos do piloto

## Outputs / Entregáveis

- **Pilot Design Document**: Documento detalhado do design do piloto
- **Training Materials**: Materiais de formação para pilot users
- **Pilot Dashboard**: Dashboard de monitorização do piloto em tempo real
- **Weekly Pilot Reports**: Relatórios semanais de progresso e métricas
- **Pilot Results Analysis**: Análise completa dos resultados do piloto
- **User Feedback Summary**: Compilação de feedback dos pilot users
- **Scale/Pivot/Stop Recommendation**: Recomendação fundamentada de próximos passos
- **Lessons Learned**: Lições aprendidas durante o piloto

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-03.1 | Accuracy/precision do modelo acima do threshold definido | CTO Agent |
| QG-03.2 | Pilot users com adoção >70% após formação | COO Agent |
| QG-03.3 | Latency e performance dentro dos SLAs definidos | CTO Agent |
| QG-03.4 | Custos por transação dentro do budget modelado | CFO Agent |
| QG-03.5 | Feedback dos pilot users net positive (NPS >0) | CHRO Agent |
| QG-03.6 | Zero incidentes de segurança ou privacidade durante o piloto | CTO Agent |

## Critérios para Avançar

Para progredir para a Fase 04 (Eval and Guardrails), todos os critérios devem ser satisfeitos:

- [ ] Piloto executado pelo período completo definido (mínimo 2 semanas)
- [ ] Métricas de performance acima dos thresholds mínimos
- [ ] Feedback dos pilot users predominantemente positivo
- [ ] Custos do piloto dentro do budget
- [ ] Nenhum incidente de segurança ou privacidade
- [ ] Decisão de avançar para scale tomada com base em dados

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Modelo com accuracy insuficiente em dados reais | Média | Alto | Threshold de accuracy definido antes do piloto |
| Pilot users resistentes à mudança de processo | Alta | Médio | Change management proativo e suporte dedicado |
| Dados de produção diferentes dos dados de treino | Média | Alto | Monitorização de data drift desde o dia 1 |
| Custos de inferência maiores que o modelado | Média | Médio | Tracking de custos por transação desde o início |
| Piloto enviesado por seleção de users favoráveis | Média | Alto | Seleção aleatória ou representativa de pilot users |

## Templates a Usar

- `templates/pilot-design.md` — Template de design do piloto
- `templates/pilot-dashboard.md` — Dashboard de monitorização do piloto
- `templates/pilot-report.md` — Relatório semanal do piloto
- `templates/pilot-results.md` — Análise de resultados do piloto

## Duração Estimada

- **Mínimo**: 2 semanas (piloto mínimo viável)
- **Típico**: 4-6 semanas
- **Máximo**: 8 semanas (para use cases complexos com sazonalidade)

> **Nota**: O piloto deve ser longo o suficiente para capturar variabilidade real,
> mas curto o suficiente para manter momentum. Definir a duração antes de iniciar e
> resistir à tentação de encurtá-lo quando os primeiros resultados são bons.
