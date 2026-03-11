# Ciclo de Review de Vendors

> Processo estruturado para avaliar, renovar ou substituir fornecedores
> críticos da empresa, garantindo valor, qualidade e alinhamento estratégico.

## Objetivo

Garantir que todos os fornecedores estratégicos estão entregando valor
proporcional ao investimento, com termos competitivos e SLAs adequados.
Evitar vendor lock-in e manter poder de negociação.

## Frequência e Timing

- **Cadência:** Anual para vendors estratégicos, semestral para vendors críticos
- **Timing:** 90 dias antes do vencimento de contratos
- **Duração:** 2-4 semanas por vendor (dependendo da complexidade)

## Classificação de Vendors

### Tier 1: Estratégicos (Review anual profundo)
- Cloud providers (AWS, Azure, GCP)
- CRM (Salesforce, HubSpot)
- ERP/Financial systems
- Plataformas de dados e analytics
- Ferramentas de segurança core
- **Critério:** Gasto anual > $100K ou impacto operacional crítico

### Tier 2: Importantes (Review anual padrão)
- SaaS de produtividade (Slack, Notion, Jira)
- Ferramentas de marketing (SEO, email, ads)
- Benefícios e RH
- Consultorias recorrentes
- **Critério:** Gasto anual $20K-$100K

### Tier 3: Operacionais (Review a cada 2 anos)
- SaaS menores
- Fornecedores de escritório e facilities
- Serviços pontuais
- **Critério:** Gasto anual < $20K

## Processo de Review

### Fase 1: Coleta de Dados (Semana 1)

**Performance**
- [ ] Compliance com SLAs contratados
- [ ] Uptime e disponibilidade (se tech vendor)
- [ ] Tempo de resposta de suporte
- [ ] Qualidade de entregáveis
- [ ] Incidentes e como foram resolvidos

**Financeiro**
- [ ] Gasto total (contrato + overage + hidden costs)
- [ ] Comparação com benchmark de mercado
- [ ] ROI estimado do vendor
- [ ] Condições de pagamento atuais vs desejadas

**Satisfação Interna**
- [ ] Survey com usuários internos do vendor (NPS)
- [ ] Feedback qualitativo de principais stakeholders
- [ ] Comparação com alternativas testadas

### Fase 2: Análise e Benchmark (Semana 2)

- [ ] Comparar pricing com 2-3 alternativas do mercado
- [ ] Avaliar funcionalidades vs necessidades atuais (over-buying? under-serving?)
- [ ] Analisar tendências do vendor (crescendo? perdendo mercado? sendo adquirido?)
- [ ] Avaliar riscos de continuidade (saúde financeira do vendor)
- [ ] Calcular custo de switching (migração, treinamento, downtime)

### Fase 3: Decisão (Semana 3)

Três possíveis outcomes:

**Renovar (com ou sem renegociação)**
- [ ] Definir pontos de negociação (preço, SLAs, features)
- [ ] Preparar argumentos com dados de benchmark
- [ ] Negociar antes do vencimento (leverage)
- [ ] Documentar novos termos

**Substituir**
- [ ] RFP para alternativas
- [ ] Piloto com 1-2 alternativas
- [ ] Plano de migração com timeline
- [ ] Comunicação interna sobre mudança

**Expandir**
- [ ] Identificar usos adicionais do vendor
- [ ] Negociar volume discount
- [ ] Plano de rollout para novos use cases

### Fase 4: Execução (Semana 4)

- [ ] Formalizar decisão em contrato/PO
- [ ] Atualizar registro de vendors
- [ ] Comunicar mudanças aos stakeholders
- [ ] Definir próxima data de review

## Template de Scorecard de Vendor

```
VENDOR SCORECARD - [NOME DO VENDOR]
Data do Review: [Data]
Reviewer: [Nome]
Contrato atual: $[Valor]/ano, vence em [Data]

PERFORMANCE (peso 40%)
- SLA compliance: ___/5
- Uptime/disponibilidade: ___/5
- Qualidade de suporte: ___/5
- Velocidade de resolução: ___/5
Score Performance: ___/20

VALOR (peso 30%)
- Preço vs mercado: ___/5
- ROI percebido: ___/5
- Hidden costs: ___/5
Score Valor: ___/15

ESTRATÉGICO (peso 20%)
- Roadmap alinhado com nossas necessidades: ___/5
- Saúde financeira do vendor: ___/5
Score Estratégico: ___/10

RELACIONAMENTO (peso 10%)
- Account management: ___/5
- Flexibilidade contratual: ___/5
Score Relacionamento: ___/10

SCORE TOTAL: ___/55
- 45-55: Excelente - renovar e considerar expandir
- 35-44: Bom - renovar com pontos de melhoria
- 25-34: Adequado - renegociar ou considerar alternativas
- <25: Insatisfatório - iniciar substituição
```

## Negociação com Vendors

### Táticas de Negociação
1. **Multi-year discount:** Comprometer 2-3 anos em troca de desconto
2. **Annual prepay:** Pagar anualmente vs mensalmente para desconto
3. **Volume commitment:** Garantir volume em troca de preço unitário menor
4. **Competitive quotes:** Ter proposta de concorrente em mãos
5. **End of quarter:** Negociar no final do quarter fiscal do vendor

### Red Flags em Contratos
- [ ] Auto-renewal sem opt-out claro
- [ ] Aumentos de preço sem cap definido
- [ ] Lock-in de dados (difícil exportar)
- [ ] SLAs vagos ou sem penalidades
- [ ] Termos de propriedade intelectual desfavoráveis

## Registro de Vendors

Manter registro centralizado com:
- Nome do vendor e contato principal
- Valor do contrato e data de vencimento
- SLA score e compliance histórico
- Decisões de review anteriores
- Próxima data de review

## Referências

- "Vendor Management Best Practices" - Gartner
- "Negotiating SaaS Contracts" - SaaStr
- "The Art of Negotiation" - Michael Wheeler (HBS)
