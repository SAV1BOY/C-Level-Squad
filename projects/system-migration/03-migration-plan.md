# Migração de Sistema — Fase 03: Plano de Migração

## Objetivo desta Fase

Desenvolver o plano detalhado de migração que cobre todos os aspectos: migração de dados,
configuração do novo sistema, desenvolvimento de integrações, formação de utilizadores,
cutover strategy e plano de rollback. O plano deve ser suficientemente detalhado para
permitir execução previsível e suficientemente robusto para lidar com os inevitáveis
imprevistos que surgem em toda migração de sistema.

## Agentes Envolvidos

- **CTO Agent**: Lidera o planeamento técnico de migração de dados e integrações
- **COO Agent**: Planeia o cutover operacional e formação de utilizadores
- **CFO Agent**: Detalha o budget por fase e controles financeiros
- **CMO Agent**: Planeia comunicação aos clientes sobre eventuais impactos
- **CHRO Agent**: Planeia a formação e change management para toda a organização
- **CEO Agent**: Aprova o plano e garante prioridade organizacional
- **Chief of Staff Agent**: Consolida o plano integrado e configura governance

## Inputs Necessários

1. Audit Report completo (output da Fase 01)
2. Vendor Selection Decision (output da Fase 02)
3. Contrato com vendor finalizado
4. Acesso ao novo sistema para configuração
5. Data mapping entre sistema atual e novo (campos, schemas)
6. Lista de integrações a implementar no novo sistema
7. Calendário da organização (blackout periods, picos de atividade)

## Processo (step-by-step)

1. **Migration strategy selection**: CTO Agent define a estratégia de migração:
   big bang, phased, parallel run ou hybrid, com justificação para a escolha
2. **Data migration planning**: CTO Agent planeia a migração de dados incluindo
   extraction, transformation, loading, validation e reconciliation procedures
3. **Integration development plan**: CTO Agent planeia o desenvolvimento de cada
   integração com o novo sistema, incluindo APIs, middleware e data sync
4. **System configuration plan**: CTO Agent e COO Agent planeiam a configuração do
   novo sistema: workflows, business rules, templates, permissões e customizações
5. **Testing strategy**: CTO Agent define a estratégia de testes: unit testing,
   integration testing, UAT, performance testing e migration dry-runs
6. **Cutover planning**: COO Agent planeia o cutover detalhado, incluindo timeline
   hora-a-hora do dia de migração, responsáveis e verificações de cada passo
7. **Rollback plan**: CTO Agent desenvolve o plano de rollback completo para cada
   fase da migração, garantindo que é possível reverter a qualquer momento
8. **Training plan**: CHRO Agent desenvolve o programa de formação para todos os
   utilizadores, incluindo materiais, schedule e critérios de readiness
9. **Communication plan**: CMO Agent e Chief of Staff Agent definem o plano de
   comunicação para stakeholders internos, externos e clientes afetados
10. **Plan approval and baseline**: Chief of Staff consolida o plano final, estabelece
    o baseline e obtém aprovação formal para iniciar a execução

## Outputs / Entregáveis

- **Migration Plan Document**: Plano completo e integrado de migração
- **Data Migration Specification**: Especificação técnica de migração de dados
- **Integration Development Plan**: Plano de desenvolvimento de integrações
- **Testing Strategy**: Estratégia e plano de testes completo
- **Cutover Runbook**: Runbook detalhado hora-a-hora para o cutover
- **Rollback Plan**: Plano de rollback testável para cada fase
- **Training Program**: Programa de formação com materiais e schedule
- **Communication Plan**: Plano de comunicação para todos os stakeholders

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-03.1 | Data mapping completo entre sistema atual e novo | CTO Agent |
| QG-03.2 | Cutover runbook com timeline hora-a-hora e verificações | COO Agent |
| QG-03.3 | Rollback plan documentado e testável | CTO Agent |
| QG-03.4 | Programa de formação completo e schedule definido | CHRO Agent |
| QG-03.5 | Budget detalhado por fase dentro do envelope aprovado | CFO Agent |
| QG-03.6 | Plano aprovado por todos os agentes sem objeções bloqueadoras | Chief of Staff |

## Critérios para Avançar

Para progredir para a Fase 04 (Execution), todos os critérios devem ser satisfeitos:

- [ ] Plano de migração completo e aprovado por todos os agentes
- [ ] Data mapping validado com dry-run de amostra
- [ ] Integrações especificadas com owners e timelines
- [ ] Programa de formação pronto para lançar
- [ ] Rollback plan documentado e validado tecnicamente
- [ ] Equipa de migração confirmada e disponível

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Data mapping incompleto que causa perda de dados | Alta | Crítico | Validação campo-a-campo com sample data |
| Plano demasiado otimista em timeline | Alta | Alto | Buffer de 30% em todas as estimativas |
| Cutover window insuficiente para o volume de dados | Média | Alto | Dry-run com dados reais para calibrar duração |
| Rollback plan não testado que falha quando necessário | Média | Crítico | Teste obrigatório do rollback antes da execução |
| Formação insuficiente que resulta em resistência | Alta | Médio | Formação hands-on com dados reais do negócio |

## Templates a Usar

- `templates/migration-plan.md` — Template de plano de migração
- `templates/data-migration-spec.md` — Especificação de migração de dados
- `templates/cutover-runbook.md` — Runbook de cutover
- `templates/migration-testing-plan.md` — Plano de testes de migração

## Duração Estimada

- **Mínimo**: 5 dias úteis (para migrações simples com pouca customização)
- **Típico**: 10-15 dias úteis
- **Máximo**: 20 dias úteis (para migrações complexas multi-sistema)

> **Nota**: O plano de migração é o investimento mais importante do projeto. Um plano
> detalhado e realista é a diferença entre uma migração bem-sucedida e um desastre.
> Resiste à tentação de "começar logo" sem um plano sólido.
