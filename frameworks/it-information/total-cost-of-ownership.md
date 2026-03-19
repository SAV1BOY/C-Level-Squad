# Total Cost of Ownership (TCO) — Framework de Análise de Custo Total

## Origem e Contexto

O Total Cost of Ownership (TCO) é uma metodologia de análise financeira que captura todos os custos
associados à aquisição, operação e desativação de um ativo tecnológico ao longo de seu ciclo de vida
completo. Criado originalmente pelo Gartner Group nos anos 1980 para avaliar custos de PCs corporativos,
o conceito evoluiu para abranger qualquer decisão de investimento em tecnologia — de infraestrutura
on-premises a cloud, de software proprietário a open-source, de build interno a SaaS.

O erro mais comum em decisões de TI é comparar apenas o preço de aquisição. Um servidor on-premises
"mais barato" pode custar 3x mais quando se incluem energia, refrigeração, espaço físico, equipe de
manutenção, licenciamento, e custo de oportunidade. Da mesma forma, cloud "barata" pode explodir em
custos de egress, storage e compute mal dimensionados.

O princípio fundamental: o preço de compra é apenas a ponta do iceberg. Os custos ocultos — operação,
oportunidade, risco, descarte — tipicamente representam 60-80% do custo total. Sem TCO, toda decisão
de investimento em TI é um tiro no escuro.

## Quando Usar

- Decisões de cloud vs on-premises (IaaS, PaaS, SaaS)
- Avaliação de renovação vs substituição de sistemas legados
- Comparação entre build interno vs comprar solução de mercado
- Justificativa de investimento em infraestrutura (CAPEX vs OPEX)
- Análise de consolidação de fornecedores
- Planejamento orçamentário de TI de médio/longo prazo (3-5 anos)
- Decisões de migração de plataforma
- Avaliação de propostas de fornecedores em processos de RFP

## Quando NÃO Usar

- Para decisões de baixo impacto financeiro (< R$ 50K em 3 anos)
- Quando o fator decisivo é puramente estratégico (ex.: competência core vs não-core)
- Como única ferramenta de decisão — TCO deve ser combinado com análise de valor
- Para justificar uma decisão já tomada (viés de confirmação)
- Em cenários de altíssima incerteza onde projeções são especulativas

## Estrutura / Modelo

### Categorias de Custo TCO

```
CUSTOS DIRETOS (Visíveis)
├── Aquisição / Licenciamento
│   ├── Hardware (servidores, storage, rede)
│   ├── Software (licenças, subscrições)
│   ├── Implementação (consultoria, integração)
│   └── Migração de dados
│
├── Operação Recorrente
│   ├── Subscrições / licenças anuais
│   ├── Suporte e manutenção (vendor)
│   ├── Infraestrutura (energia, cooling, rack space)
│   └── Conectividade (bandwidth, links dedicados)
│
CUSTOS INDIRETOS (Parcialmente Visíveis)
├── Pessoas
│   ├── FTEs dedicados à operação
│   ├── Treinamento e certificações
│   ├── Recrutamento de especialistas
│   └── Custo de retenção (mercado aquecido)
│
├── Gestão e Governança
│   ├── Tempo de gestão de contratos
│   ├── Compliance e auditoria
│   ├── Gestão de fornecedores
│   └── Reporting e monitoramento
│
CUSTOS OCULTOS (Frequentemente Ignorados)
├── Oportunidade
│   ├── Tempo de equipe alocado em manutenção vs inovação
│   ├── Time-to-market perdido
│   └── Features não desenvolvidas
│
├── Risco
│   ├── Downtime (custo por hora de indisponibilidade)
│   ├── Breach de segurança (custo médio de incidente)
│   ├── Vendor lock-in (custo de saída)
│   └── Obsolescência tecnológica
│
├── Transição e Descarte
│   ├── Custo de migração futura
│   ├── Descomissionamento
│   ├── Descarte seguro de dados
│   └── Penalidades contratuais de saída
```

### Modelo de Projeção 3-5 Anos

```
                    Ano 0      Ano 1      Ano 2      Ano 3      Ano 4      Ano 5
                  (Setup)   (Operação) (Operação) (Operação) (Operação) (Operação)
─────────────────────────────────────────────────────────────────────────────────
Diretos           ████████   ████       ████       ████       ████       ████
Indiretos         ██         ████       ████       ████       ████       ████
Ocultos           █          ██         ██         ███        ███        ███
─────────────────────────────────────────────────────────────────────────────────
TCO Acumulado     ████████   ████████████████████████████████████████████████████
```

## Processo de Aplicação (step-by-step)

### Passo 1: Definir Escopo e Horizonte Temporal

- Identificar o ativo ou solução a ser avaliada
- Definir alternativas comparáveis (mínimo 2, idealmente 3)
- Estabelecer horizonte temporal (3 anos para SaaS, 5 anos para infra)
- Definir taxa de desconto para cálculo de valor presente (VPL)

### Passo 2: Mapear Custos Diretos

- Levantar todos os custos de aquisição e implementação
- Projetar custos recorrentes com inflação e reajustes contratuais
- Incluir custos de migração de dados e integração
- Documentar premissas de crescimento (usuários, volume, storage)

### Passo 3: Quantificar Custos Indiretos

- Calcular FTEs necessários (horas × custo/hora fully-loaded)
- Estimar custos de treinamento e ramp-up
- Projetar custos de gestão de vendor e compliance
- Incluir overhead organizacional (procurement, legal, finance)

### Passo 4: Estimar Custos Ocultos

- Modelar custo de downtime (receita/hora × probabilidade × horas esperadas)
- Calcular custo de oportunidade (o que a equipe faria se não estivesse mantendo)
- Estimar custo de saída do vendor (migração, penalidades, retrabalho)
- Projetar custo de obsolescência (refresh cycles, end-of-life)

### Passo 5: Consolidar e Comparar

- Somar todos os custos por ano para cada alternativa
- Calcular VPL (Valor Presente Líquido) com taxa de desconto definida
- Calcular custo mensal equivalente por usuário ou por unidade de negócio
- Fazer análise de sensibilidade (cenários otimista, base, pessimista)

### Passo 6: Apresentar e Decidir

- Criar one-pager executivo com comparação visual
- Destacar top 3 drivers de custo por alternativa
- Explicitar premissas e riscos de cada cenário
- Recomendar com base em TCO + fatores estratégicos

## Exemplos Práticos

### Exemplo 1: Cloud vs On-Premises para ERP

| Componente           | On-Premises (5 anos) | Cloud SaaS (5 anos)  |
|----------------------|----------------------|----------------------|
| Licenças/Subscrição  | R$ 800K (perpétua)   | R$ 1.200K (5×R$240K) |
| Infra (HW/DC)        | R$ 400K              | R$ 0                 |
| Equipe dedicada       | R$ 1.500K (3 FTEs)   | R$ 500K (1 FTE)      |
| Implementação         | R$ 600K              | R$ 400K              |
| Upgrades/Patches      | R$ 300K              | R$ 0 (incluído)      |
| Downtime estimado     | R$ 200K              | R$ 50K               |
| Custo de saída        | R$ 100K              | R$ 300K              |
| **TCO Total**         | **R$ 3.900K**        | **R$ 2.450K**        |

Conclusão: Cloud é 37% mais barato no horizonte de 5 anos, mas tem custo de saída 3x maior.

### Exemplo 2: Build vs Buy para Plataforma de Dados

| Componente             | Build Interno (3 anos) | Plataforma SaaS (3 anos) |
|------------------------|------------------------|--------------------------|
| Desenvolvimento         | R$ 1.800K (6 devs/6m)  | R$ 0                     |
| Subscrição              | R$ 0                   | R$ 720K (R$20K/mês)      |
| Manutenção/Evolução     | R$ 900K (3 devs)       | R$ 0 (incluído)          |
| Infra                   | R$ 180K                | R$ 0 (incluído)          |
| Time-to-market perdido  | R$ 500K (6 meses)      | R$ 80K (1 mês)           |
| Risco de turnover       | R$ 400K                | R$ 50K                   |
| **TCO Total**           | **R$ 3.780K**          | **R$ 850K**              |

## Armadilhas Comuns

1. **Comparar preço de etiqueta**: Ignorar custos indiretos e ocultos é o erro #1.
2. **Horizonte temporal curto demais**: Cloud parece cara no ano 1, barata no ano 3.
3. **Ignorar custo de pessoas**: FTEs dedicados são frequentemente o maior componente.
4. **Esquecer o custo de saída**: Vendor lock-in pode transformar uma decisão reversível em armadilha.
5. **Não ajustar por crescimento**: Projetar custos lineares quando o crescimento é exponencial.
6. **Viés de status quo**: Superestimar custos de mudança e subestimar custos de manter.
7. **Não incluir custo de oportunidade**: O que sua equipe faria se não estivesse mantendo legado?
8. **Usar premissas do vendor sem validar**: Vendors otimizam a apresentação, não a realidade.
9. **Ignorar compliance e segurança**: Custos regulatórios podem ser significativos.
10. **Não fazer análise de sensibilidade**: Uma única projeção é uma ilusão de precisão.

## Integração com Outros Frameworks

- **`frameworks/cfo-strategist/cost-optimization.md`**: TCO alimenta análise de otimização de custos
- **`frameworks/cto-architect/build-vs-buy.md`**: TCO é input fundamental para decisão build vs buy
- **`frameworks/cio-engineer/cloud-strategy.md`**: TCO guia decisões de cloud strategy
- **`frameworks/cio-engineer/cio-systems-rationalization.md`**: TCO suporta decisões de racionalização
- **`checklists/finance/budget-approval-quality.md`**: Checklist de qualidade para aprovação de budget
- **`templates/finance/`**: Templates de análise financeira
- **`frameworks/shared/decision-framework.md`**: TCO é input para decisões Type 2

## Referências

- Gartner — "Total Cost of Ownership: A Critical Tool for IT Decision Making"
- Forrester — "Total Economic Impact (TEI) Methodology"
- AWS — "Cloud Economics: Total Cost of Ownership"
- McKinsey — "Cloud Cost Optimization: Principles and Best Practices"
- ITIL 4 — "Financial Management for IT Services"
