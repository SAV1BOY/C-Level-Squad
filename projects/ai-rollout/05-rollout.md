# AI Rollout — Fase 05: Rollout em Escala

## Objetivo desta Fase

Escalar a solução de AI do grupo piloto para toda a organização ou segmento alvo,
garantindo que a performance se mantém, que os processos operacionais suportam o
volume e que a adoção pelos utilizadores finais é bem-sucedida. O rollout deve ser
gradual e controlado, com capacidade de pausar ou reverter se surgirem problemas
inesperados em escala. Escalar demasiado rápido é tão perigoso quanto não escalar.

## Agentes Envolvidos

- **CTO Agent**: Lidera o rollout técnico e garante estabilidade em escala
- **COO Agent**: Coordena o rollout operacional e formação de utilizadores
- **CMO Agent**: Gere comunicação externa sobre a nova capacidade (se aplicável)
- **CFO Agent**: Monitoriza custos de escala e valida unit economics
- **CHRO Agent**: Lidera o change management e programa de formação em massa
- **CEO Agent**: Remove bloqueios organizacionais e mantém prioridade do rollout
- **Chief of Staff Agent**: Coordena o plano de rollout e tracking de progresso

## Inputs Necessários

1. Pilot Results com decisão de scale aprovada (output da Fase 03)
2. Guardrails implementados e testados (output da Fase 04)
3. Plano de rollout com fases e critérios de expansão
4. Materiais de formação escaláveis (vídeos, guias, FAQs)
5. Infraestrutura escalada para suportar volume total
6. Equipa de suporte dimensionada para o volume do rollout
7. Plano de comunicação para stakeholders afetados

## Processo (step-by-step)

1. **Rollout wave planning**: COO Agent e CTO Agent definem as waves de rollout,
   tipicamente começando com departamentos mais recetivos e expandindo progressivamente
2. **Infrastructure scaling**: CTO Agent escala a infraestrutura técnica para suportar
   o volume total projetado, com margem de segurança e auto-scaling configurado
3. **Training program launch**: CHRO Agent lança o programa de formação escalável,
   incluindo e-learning, sessões hands-on e materiais de self-service
4. **Wave 1 rollout**: CTO Agent ativa a solução para o primeiro grupo pós-piloto,
   monitorizando de perto as métricas de performance e adoção
5. **Wave 1 assessment**: Após período de estabilização (1-2 semanas), todos os agentes
   avaliam os resultados da wave 1 e decidem se avançam para wave 2
6. **Subsequent waves**: Processo repetido para cada wave, com expansão progressiva
   e monitorização contínua de métricas e feedback
7. **Change management support**: CHRO Agent e COO Agent fornecem suporte contínuo
   durante o rollout, incluindo champions program e help desk dedicado
8. **Communication cadence**: Chief of Staff Agent mantém comunicação regular sobre
   progresso do rollout, quick wins e próximos passos
9. **Cost monitoring**: CFO Agent monitoriza custos reais vs projetados e alerta se
   custos por transação divergirem significativamente do modelo
10. **Full rollout completion**: Quando todas as waves estão concluídas, CTO Agent
    confirma que a solução está operacional em escala para todo o público alvo

## Outputs / Entregáveis

- **Rollout Plan**: Plano detalhado com waves, timelines e critérios de expansão
- **Training Program**: Programa de formação completo e escalável
- **Wave Progress Reports**: Relatório de progresso por wave do rollout
- **Adoption Dashboard**: Dashboard de métricas de adoção por grupo/departamento
- **Performance at Scale Report**: Relatório de performance técnica em escala
- **Cost at Scale Analysis**: Análise de custos reais em escala vs modelo
- **Change Management Report**: Relatório de adoção e resistência por grupo
- **Rollout Completion Certificate**: Certificação formal de rollout completo

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-05.1 | Cada wave atinge >60% de adoção antes de avançar | COO Agent |
| QG-05.2 | Performance técnica mantém-se dentro dos SLAs em escala | CTO Agent |
| QG-05.3 | Custos por transação dentro de 120% do modelado | CFO Agent |
| QG-05.4 | CSAT de utilizadores >7/10 em cada wave | COO Agent |
| QG-05.5 | Zero incidentes de segurança ou privacidade durante rollout | CTO Agent |
| QG-05.6 | Formação completada por >80% dos utilizadores de cada wave | CHRO Agent |

## Critérios para Avançar

Para progredir para a Fase 06 (Measure and Iterate), todos os critérios devem ser satisfeitos:

- [ ] Rollout completo para todo o público alvo
- [ ] Adoção global >60% dos utilizadores alvo
- [ ] Performance técnica estável em escala por 2+ semanas
- [ ] Custos de operação dentro do envelope orçamental
- [ ] Equipa de suporte operando em cadência normal
- [ ] Guardrails operacionais e sem incidentes significativos

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Performance degrada em escala (vs piloto) | Média | Alto | Scaling gradual com monitoring contínuo |
| Resistência massiva à adoção | Média | Alto | Champions program e executive sponsorship visível |
| Custos escalam mais que linearmente | Média | Médio | Monitorização de custos por transação desde wave 1 |
| Infraestrutura não suporta o volume | Baixa | Crítico | Load testing antes de cada wave e auto-scaling |
| Change fatigue na organização | Alta | Médio | Comunicar benefícios e quick wins consistentemente |

## Templates a Usar

- `templates/rollout-plan.md` — Template de plano de rollout por waves
- `templates/training-program.md` — Programa de formação escalável
- `templates/adoption-dashboard.md` — Dashboard de adoção
- `templates/wave-assessment.md` — Template de avaliação por wave

## Duração Estimada

- **Mínimo**: 4 semanas (organização pequena, 2-3 waves)
- **Típico**: 8-12 semanas (4-6 waves com estabilização entre cada)
- **Máximo**: 16 semanas (organização grande com muitos departamentos)

> **Nota**: A velocidade do rollout deve ser ditada pela capacidade da organização
> absorver a mudança, não pela pressão de mostrar resultados rápidos. Um rollout
> falhado é pior do que um rollout lento.
