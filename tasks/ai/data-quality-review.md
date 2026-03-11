# Review de Qualidade de Dados

> Processo estruturado para avaliar e melhorar a qualidade dos dados utilizados
> em sistemas de AI/ML e analytics, garantindo que decisões são baseadas em
> dados confiáveis.

## Objetivo

Dados de baixa qualidade levam a modelos de AI ruins, decisões erradas e perda
de confiança. Este processo garante que os dados que alimentam sistemas de AI
e analytics são completos, corretos, consistentes e atualizados.

## Frequência

- **Monitoramento contínuo:** Automatizado para métricas críticas
- **Review profundo:** Trimestral por dataset
- **Pré-training:** Obrigatório antes de treinar/fine-tunar modelos
- **Ad-hoc:** Quando anomalias são detectadas em modelos ou reports

## Dimensões de Qualidade de Dados

### 1. Completeness (Completude)
- % de registros sem valores nulos em campos obrigatórios
- % de entidades com todos os atributos essenciais preenchidos
- Cobertura temporal (há gaps em séries temporais?)
- **Target:** >95% para campos críticos, >80% para campos secundários

### 2. Accuracy (Acurácia)
- % de registros que correspondem à realidade (validação contra fonte externa)
- Erros de digitação/input em campos textuais
- Valores numéricos dentro de ranges esperados
- **Target:** >99% para dados financeiros, >95% para dados operacionais

### 3. Consistency (Consistência)
- Mesmo dado em diferentes sistemas tem o mesmo valor?
- Formatos padronizados (datas, endereços, moedas)?
- Referências cruzadas íntegras (foreign keys válidas)?
- **Target:** >99% de consistência entre sistemas

### 4. Timeliness (Atualidade)
- Dados são atualizados na frequência necessária?
- Lag entre evento real e registro no sistema
- Dados stale que não refletem realidade atual
- **Target:** Depende do use case (real-time a diário)

### 5. Uniqueness (Unicidade)
- % de registros duplicados
- Lógica de deduplicação efetiva
- Entity resolution para mesma entidade com dados diferentes
- **Target:** <1% de duplicatas em datasets primários

### 6. Validity (Validade)
- Dados conformam com schema e regras de negócio?
- Enums e categorias contêm apenas valores válidos?
- Constraints de integridade respeitados?
- **Target:** 100% de conformidade com schema

## Processo de Review

### Fase 1: Profiling Automatizado
- [ ] Executar data profiling em todos os datasets críticos
- [ ] Gerar estatísticas descritivas (distribuições, nulls, cardinalidade)
- [ ] Identificar anomalias automáticas (outliers, padrões incomuns)
- [ ] Comparar com profile anterior (drift detection)

### Fase 2: Avaliação por Dimensão
Para cada dataset, avaliar as 6 dimensões:

- [ ] Completeness check com queries automatizadas
- [ ] Accuracy sampling (verificar amostra contra fonte verdadeira)
- [ ] Consistency check entre sistemas
- [ ] Timeliness check (freshness dos dados)
- [ ] Uniqueness check (deduplicação)
- [ ] Validity check (conformidade com schema)

### Fase 3: Root Cause Analysis
Para issues encontrados:
- [ ] Identificar origem do problema (input, transformação, integração)
- [ ] Classificar como sistêmico ou pontual
- [ ] Avaliar impacto downstream (quais modelos/reports afetados?)
- [ ] Propor correção na origem (não apenas nos sintomas)

### Fase 4: Remediação e Melhoria
- [ ] Corrigir dados problemáticos (quando possível e seguro)
- [ ] Implementar validações na origem para prevenir recorrência
- [ ] Atualizar data contracts entre produtores e consumidores
- [ ] Configurar alertas automatizados para novas ocorrências

## Data Quality Scorecard

```
DATA QUALITY SCORECARD - [DATASET] - [DATA]

| Dimensão | Score (1-5) | Target | Status | Notas |
|----------|-------------|--------|--------|-------|
| Completeness | ___ | 4.5 | | |
| Accuracy | ___ | 4.5 | | |
| Consistency | ___ | 4.0 | | |
| Timeliness | ___ | 4.0 | | |
| Uniqueness | ___ | 4.5 | | |
| Validity | ___ | 5.0 | | |
| TOTAL | ___ | 26.5 | | |

Score 25-30: Excelente - dados confiáveis para AI e decisões
Score 20-24: Bom - maioria dos usos é segura, atenção a gaps
Score 15-19: Adequado - usar com cautela, plano de melhoria necessário
Score <15: Insuficiente - não usar para AI sem remediação significativa
```

## Data Contracts

Para cada dataset crítico, manter um contrato entre produtor e consumidor:

```
DATA CONTRACT: [NOME DO DATASET]

Produtor: [Time/Sistema]
Consumidores: [Times/Modelos que usam]
SLA de freshness: [ex: atualizado a cada 1 hora]
SLA de completeness: [ex: >95% de campos obrigatórios]
Schema: [link para schema definition]
Responsável: [Nome]
Revisão: [Cadência de revisão do contrato]

Alertas configurados:
- Completeness < 90%: [quem é alertado]
- Freshness > 2x SLA: [quem é alertado]
- Schema break: [quem é alertado]
```

## Automação de Data Quality

### Ferramentas Recomendadas
- **Great Expectations:** Framework de validação de dados Python
- **dbt tests:** Testes integrados ao pipeline de transformação
- **Monte Carlo/Anomalo:** Observabilidade de dados automatizada
- **Apache Griffin:** Data quality open-source
- **Custom scripts:** Para validações específicas de negócio

### Testes Automatizados Essenciais
- [ ] Null check em campos obrigatórios
- [ ] Range check em campos numéricos
- [ ] Uniqueness check em chaves primárias
- [ ] Referential integrity entre tabelas
- [ ] Freshness check (última atualização)
- [ ] Volume check (número de registros vs esperado)
- [ ] Schema validation (tipos, formato)
- [ ] Distribution check (comparar com histórico)

## Impacto de Dados Ruins em AI

### Quantificação
- Modelos treinados com 10% de dados incorretos perdem ~15-25% de accuracy
- Dados duplicados inflam métricas de training e criam overfitting
- Missing data em features críticas pode causar viés de seleção
- Dados stale em modelos de recomendação degradam relevância

### Regra Prática
"Garbage in, garbage out" - nenhuma quantidade de engenharia de modelo
compensa dados de baixa qualidade. Investir em data quality tem ROI
maior que investir em modelos mais sofisticados.

## Referências

- "Data Quality" - Jack E. Olson
- "Fundamentals of Data Engineering" - Joe Reis & Matt Housley
- Great Expectations Documentation (greatexpectations.io)
- DAMA DMBOK (Data Management Body of Knowledge)
- "The Data Quality Imperative" - McKinsey (2023)
