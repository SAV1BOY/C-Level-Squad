# Migração de Sistema — Fase 04: Execução da Migração

## Objetivo desta Fase

Executar o plano de migração com precisão e disciplina, completando a migração de dados,
configuração do novo sistema, implementação de integrações, formação de utilizadores e
cutover para o novo sistema. A execução de uma migração requer coordenação minuciosa e
capacidade de resposta rápida a problemas imprevistos. O objetivo é minimizar disruption
para o negócio enquanto se garante que nenhum dado é perdido e nenhuma funcionalidade
crítica fica sem cobertura.

## Agentes Envolvidos

- **CTO Agent**: Lidera a execução técnica de migração e integrações
- **COO Agent**: Coordena o cutover operacional e suporte aos utilizadores
- **CFO Agent**: Monitoriza custos de implementação e valida billing no novo sistema
- **CMO Agent**: Gere comunicação com clientes sobre a transição
- **CHRO Agent**: Executa o programa de formação e gere o change management
- **CEO Agent**: Disponível para decisões críticas e comunicação de crise
- **Chief of Staff Agent**: Opera o war room de migração e tracking de progresso

## Inputs Necessários

1. Migration Plan completo e aprovado (output da Fase 03)
2. Novo sistema configurado e pronto para testes
3. Data migration scripts desenvolvidos e testados
4. Integrações desenvolvidas e testadas em staging
5. Materiais de formação prontos
6. Equipa de migração em standby
7. War room configurado e canais de comunicação ativados

## Processo (step-by-step)

1. **Pre-migration dry-run**: CTO Agent executa um dry-run completo da migração com
   dados de produção num ambiente de staging, validando timing e completude
2. **System configuration final**: CTO Agent e COO Agent completam a configuração do
   novo sistema incluindo workflows, permissões, templates e business rules
3. **Integration deployment**: CTO Agent deploya e testa todas as integrações no
   ambiente de staging, validando data flow end-to-end
4. **User Acceptance Testing (UAT)**: COO Agent coordena UAT com representantes de
   cada grupo de utilizadores usando cenários reais de negócio
5. **Training execution**: CHRO Agent executa o programa de formação por grupos,
   garantindo que todos os utilizadores estão prontos para o cutover
6. **Pre-cutover preparation**: Chief of Staff Agent executa o checklist de
   pré-cutover, confirmando readiness de todos os componentes
7. **Data migration execution**: CTO Agent executa a migração de dados em produção
   seguindo o runbook, com verificações de completude a cada fase
8. **Cutover execution**: COO Agent coordena o cutover seguindo o runbook hora-a-hora,
   com checkpoints de validação e decisões go/no-go em cada etapa
9. **Post-cutover verification**: CTO Agent e COO Agent executam verificações completas
   pós-cutover: dados migrados, integrações operacionais, funcionalidades ativas
10. **Hypercare period**: Toda a equipa mantém suporte intensivo durante as primeiras
    2 semanas pós-migração, com presença no war room e resposta rápida a issues

## Outputs / Entregáveis

- **Dry-run Results Report**: Relatório do dry-run com issues encontrados e resolvidos
- **UAT Sign-off**: Documento de aceitação assinado pelos representantes de utilizadores
- **Training Completion Report**: Relatório de formação com taxas de conclusão
- **Data Migration Reconciliation**: Relatório de reconciliação de dados migrados
- **Cutover Execution Log**: Log detalhado da execução do cutover
- **Post-Cutover Verification Report**: Relatório de verificação pós-cutover
- **Hypercare Issue Log**: Log de issues durante o período de hypercare
- **Old System Decommission Plan**: Plano de descomissionamento do sistema antigo

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-04.1 | Dry-run completado com sucesso e issues resolvidos | CTO Agent |
| QG-04.2 | UAT sign-off de todos os grupos de utilizadores | COO Agent |
| QG-04.3 | 100% dos dados migrados e reconciliados sem perda | CTO Agent |
| QG-04.4 | Todas as integrações operacionais pós-cutover | CTO Agent |
| QG-04.5 | >90% dos utilizadores formados antes do cutover | CHRO Agent |
| QG-04.6 | Issues P0/P1 do hypercare resolvidos em <24 horas | CTO Agent |

## Critérios para Avançar

Para progredir para a Fase 05 (Validation), todos os critérios devem ser satisfeitos:

- [ ] Cutover completo e novo sistema operacional em produção
- [ ] 100% dos dados migrados e reconciliados
- [ ] Todas as integrações funcionais e validadas
- [ ] Issues P0 e P1 do hypercare resolvidos
- [ ] Utilizadores a usar o novo sistema com suporte adequado
- [ ] Hypercare period completado (mínimo 2 semanas)

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Perda de dados durante a migração | Média | Crítico | Backup completo antes de iniciar; reconciliation |
| Cutover excede a janela planeada | Alta | Alto | Critério claro de rollback se exceder 150% do tempo |
| Integrações falham em produção com dados reais | Média | Alto | Testar com dados de produção no dry-run |
| Utilizadores não conseguem trabalhar no novo sistema | Média | Alto | Hypercare com suporte dedicado por departamento |
| Performance do novo sistema inferior ao antigo | Média | Médio | Performance testing com carga realística antes do cutover |

## Templates a Usar

- `templates/cutover-runbook.md` — Runbook de execução do cutover
- `templates/data-reconciliation.md` — Template de reconciliação de dados
- `templates/uat-signoff.md` — Documento de sign-off de UAT
- `templates/hypercare-tracker.md` — Tracker de issues do hypercare

## Duração Estimada

- **Mínimo**: 2 semanas (migração simples com pouca customização)
- **Típico**: 4-8 semanas (incluindo hypercare)
- **Máximo**: 12 semanas (migração complexa com parallel run)

> **Nota**: O dia do cutover é o dia mais stressante de uma migração. Preparação
> meticulosa e dry-runs realistas são a melhor forma de reduzir esse stress.
> Ter o rollback plan pronto é o seguro que esperamos nunca usar.
