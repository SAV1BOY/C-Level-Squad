# Migração de Sistema — Fase 02: Seleção de Vendor/Plataforma

## Objetivo desta Fase

Selecionar o sistema, plataforma ou vendor de destino da migração através de um processo
estruturado de avaliação que considera funcionalidades, fit técnico, custo, roadmap,
suporte e viabilidade de migração. A seleção do sistema alvo é uma das decisões mais
consequenciais porque define a infraestrutura tecnológica da organização para os
próximos 5-10 anos. Errar aqui resulta em outra migração prematura.

## Agentes Envolvidos

- **CTO Agent**: Lidera a avaliação técnica e testes de vendors
- **CFO Agent**: Modela TCO e negoceia termos comerciais
- **COO Agent**: Avalia fit operacional e facilidade de uso
- **CMO Agent**: Avalia impacto na experiência do cliente e integrações de marketing
- **CEO Agent**: Toma a decisão final alinhada com estratégia de longo prazo
- **CHRO Agent**: Avalia facilidade de adoção e necessidades de formação
- **Chief of Staff Agent**: Facilita o processo de seleção e documenta avaliações

## Inputs Necessários

1. Audit Report completo (output da Fase 01)
2. Gap Register com requisitos priorizados
3. Lista de vendors/plataformas candidatos
4. Budget aprovado para licenciamento e implementação
5. Requisitos não-funcionais (performance, security, compliance, scalability)
6. Timeline desejada para a migração
7. Restrições de data residency e compliance

## Processo (step-by-step)

1. **Requirements finalization**: CTO Agent e COO Agent finalizam a lista de requisitos
   (must-have e nice-to-have) baseada na auditoria e gap analysis
2. **Long-list creation**: CTO Agent cria uma long-list de 5-10 soluções candidatas
   baseada em pesquisa de mercado, analyst reports e recomendações
3. **Pre-screening**: CTO Agent faz pre-screening eliminando soluções que não cumprem
   requisitos must-have, reduzindo para um shortlist de 3-5 candidatos
4. **RFP/RFI process**: Chief of Staff Agent coordena o processo de Request for
   Proposal/Information com os candidatos do shortlist
5. **Demo sessions**: CTO Agent e COO Agent organizam sessões de demo com cada vendor,
   usando cenários reais baseados nos processos auditados
6. **Technical evaluation**: CTO Agent avalia profundamente cada candidato quanto a
   arquitetura, APIs, integrações, performance, segurança e roadmap
7. **Commercial evaluation**: CFO Agent avalia e negocia termos comerciais incluindo
   pricing model, licenciamento, SLAs e condições contratuais
8. **Reference checks**: COO Agent contacta clientes de referência de cada vendor para
   validar experiências reais de implementação e operação
9. **Scoring and ranking**: Chief of Staff Agent facilita sessão de scoring onde cada
   agente pontua os candidatos nos critérios da sua área
10. **Selection decision**: CEO Agent lidera a decisão final, equilibrando fit técnico,
    custo, risco e alinhamento estratégico

## Outputs / Entregáveis

- **Requirements Document**: Lista final de requisitos priorizados
- **Vendor Long-list**: Lista inicial de candidatos com pre-screening
- **Vendor Shortlist and Evaluation**: Avaliação detalhada dos finalistas
- **TCO Comparison**: Comparação de Total Cost of Ownership por candidato
- **Demo Results Summary**: Resumo dos resultados das sessões de demo
- **Reference Check Report**: Relatório de verificação de referências
- **Selection Decision Document**: Decisão final com justificação detalhada
- **Contract Terms Summary**: Resumo dos termos comerciais negociados

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-02.1 | Pelo menos 3 candidatos avaliados em profundidade | CTO Agent |
| QG-02.2 | Demos realizadas com cenários reais do negócio | COO Agent |
| QG-02.3 | TCO modelado para 5 anos com pressupostos documentados | CFO Agent |
| QG-02.4 | Referências verificadas com pelo menos 2 clientes por vendor | COO Agent |
| QG-02.5 | Security e compliance avaliados para o candidato selecionado | CTO Agent |
| QG-02.6 | Decisão aprovada com consensus ou maioria qualificada | CEO Agent |

## Critérios para Avançar

Para progredir para a Fase 03 (Migration Plan), todos os critérios devem ser satisfeitos:

- [ ] Vendor/plataforma selecionado e decisão documentada
- [ ] Contrato comercial negociado ou em fase final de negociação
- [ ] TCO aprovado e dentro do budget disponível
- [ ] Viabilidade técnica de migração confirmada pelo vendor
- [ ] Equipa de implementação identificada (interna e/ou vendor)
- [ ] Nenhum bloqueador de compliance ou security identificado

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Viés para o vendor mais "popular" sem fit real | Média | Alto | Avaliação baseada em critérios objetivos e ponderados |
| Vendor overpromise em funcionalidades durante demo | Alta | Alto | Testar com dados reais; verificar referências |
| Custos escondidos não incluídos no TCO | Alta | Médio | CFO Agent exige breakdown completo de todos os custos |
| Vendor lock-in severo sem exit strategy | Média | Alto | Avaliar portabilidade de dados e standard APIs |
| Decisão apressada por pressão de timeline | Média | Crítico | Manter rigor do processo mesmo sob pressão |

## Templates a Usar

- `templates/vendor-evaluation-scorecard.md` — Scorecard de avaliação de vendors
- `templates/rfp-template.md` — Template de Request for Proposal
- `templates/tco-comparison.md` — Comparação de Total Cost of Ownership
- `templates/vendor-selection-decision.md` — Documento de decisão de seleção

## Duração Estimada

- **Mínimo**: 10 dias úteis (poucas opções, decisão clara)
- **Típico**: 15-20 dias úteis
- **Máximo**: 30 dias úteis (processo formal de RFP com muitos candidatos)

> **Nota**: O vendor perfeito não existe. A melhor seleção equilibra funcionalidade,
> custo, risco e parceria. Um vendor com 80% do fit mas excelente suporte e roadmap
> é frequentemente melhor que um com 95% do fit mas suporte medíocre.
