# Lançamento de Produto — Fase 03: Ops Readiness

## Objetivo desta Fase

Garantir que todas as operações de suporte ao lançamento estão prontas para funcionar
no dia do lançamento e nos dias seguintes. Isto inclui suporte ao cliente, processos
de fulfillment, logística, billing, onboarding de utilizadores e processos internos
de escalação. A readiness operacional é frequentemente a diferença entre um lançamento
que encanta clientes e um que gera frustração e churn precoce.

## Agentes Envolvidos

- **COO Agent**: Lidera toda a preparação operacional e toma decisão go/no-go ops
- **CTO Agent**: Suporta com ferramentas e automação para processos operacionais
- **CMO Agent**: Coordena messaging de suporte alinhado com comunicação de marketing
- **CFO Agent**: Valida processos de billing, pricing e financial reconciliation
- **CHRO Agent**: Garante que equipa operacional está treinada e dimensionada
- **Chief of Staff Agent**: Coordena checklist integrado de readiness operacional

## Inputs Necessários

1. Launch Brief com volume esperado de clientes/utilizadores
2. Tech Readiness Report confirmando que produto está pronto
3. Processos operacionais desenhados no GTM plan
4. Equipa de suporte dimensionada e alocada
5. Ferramentas de suporte configuradas (ticketing, chat, knowledge base)
6. Pricing e billing configuração finalizada
7. SLAs de suporte definidos e comunicados

## Processo (step-by-step)

1. **Support team preparation**: CHRO Agent e COO Agent garantem que a equipa de suporte
   está contratada, treinada e familiarizada com o produto através de sessões hands-on
2. **Knowledge base creation**: COO Agent cria e publica a knowledge base com FAQs,
   troubleshooting guides e how-to articles para self-service
3. **Support tools configuration**: CTO Agent e COO Agent configuram e testam ferramentas
   de ticketing, live chat, email support e telefone se aplicável
4. **Escalation paths definition**: COO Agent define os paths de escalação claros desde
   L1 support até engenharia e C-Level para issues críticos
5. **Billing and pricing validation**: CFO Agent valida que o pricing está correto em
   todos os planos, que billing funciona corretamente e que reconciliation está automatizada
6. **Onboarding flow testing**: CMO Agent e COO Agent testam end-to-end o fluxo de
   onboarding de novos utilizadores, desde signup até first value
7. **Capacity stress test**: COO Agent simula cenários de volume alto para validar que
   a equipa e processos suportam picos esperados no launch day
8. **Internal communication**: Chief of Staff Agent garante que toda a organização sabe
   do lançamento, quando acontece e que fazer se forem contactados por clientes
9. **War room setup for launch**: COO Agent configura o war room operacional para o
   dia de lançamento com canais de comunicação dedicados
10. **Ops go/no-go decision**: COO Agent apresenta o readiness report operacional e
    toma a decisão de go ou no-go operacional

## Outputs / Entregáveis

- **Ops Readiness Report**: Relatório completo de readiness operacional
- **Knowledge Base**: Base de conhecimento publicada e acessível
- **Support Playbook**: Guia operacional para a equipa de suporte
- **Escalation Matrix**: Matriz de escalação com contactos e critérios
- **Billing Validation Report**: Confirmação de pricing e billing corretos
- **Onboarding Checklist**: Checklist validada do fluxo de onboarding
- **Launch Day War Room Plan**: Plano do war room para o dia de lançamento
- **Ops Go/No-Go Document**: Decisão formal de readiness operacional

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-03.1 | Equipa de suporte treinada e aprovada em teste prático | COO Agent |
| QG-03.2 | Knowledge base com cobertura >80% dos cenários previstos | COO Agent |
| QG-03.3 | Billing testado end-to-end para todos os planos e cenários | CFO Agent |
| QG-03.4 | Onboarding flow testado com 5+ utilizadores reais | CMO Agent |
| QG-03.5 | Escalation paths testados com simulação de incidente | COO Agent |
| QG-03.6 | War room configurado e canais de comunicação testados | Chief of Staff |

## Critérios para Avançar

Para progredir para a Fase 04 (Launch Day), todos os critérios devem ser satisfeitos:

- [ ] Go operacional confirmado pelo COO Agent
- [ ] Equipa de suporte pronta e em standby para o launch day
- [ ] Knowledge base publicada e acessível
- [ ] Billing e pricing validados sem erros
- [ ] Onboarding flow testado e funcional
- [ ] War room configurado para o dia de lançamento

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Equipa de suporte subdimensionada para o volume | Média | Alto | Escalar equipa temporária para o launch week |
| Knowledge base incompleta gerando tickets evitáveis | Alta | Médio | Priorizar top 20 FAQs baseadas em beta feedback |
| Billing errors que afetam confiança do cliente | Baixa | Crítico | Teste exaustivo de todos os cenários de billing |
| Onboarding flow com friction que causa drop-off | Média | Alto | Simplificar ao máximo; otimizar após dados reais |
| Comunicação interna falha e equipa não sabe do launch | Média | Médio | Múltiplos canais de comunicação interna |

## Templates a Usar

- `templates/ops-readiness-checklist.md` — Checklist de readiness operacional
- `templates/support-playbook.md` — Playbook de suporte ao cliente
- `templates/escalation-matrix.md` — Matriz de escalação
- `templates/war-room-plan.md` — Plano do war room de lançamento

## Duração Estimada

- **Mínimo**: 3 dias úteis (para lançamentos simples com equipa existente)
- **Típico**: 5-10 dias úteis
- **Máximo**: 15 dias úteis (para lançamentos complexos com nova equipa)

> **Nota**: Ops readiness é frequentemente subestimada porque é "menos glamorosa" que
> o marketing ou a tecnologia. Mas é nas operações que o cliente experimenta o valor
> real do produto. Um suporte excelente pode salvar um produto imperfeito.
