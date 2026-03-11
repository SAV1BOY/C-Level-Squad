# AI Rollout — Fase 01: Data Readiness

## Objetivo desta Fase

Avaliar e preparar os dados necessários para o use case de AI selecionado, garantindo
qualidade, volume, acessibilidade e compliance suficientes para treinar ou configurar
modelos com resultados fiáveis. Esta fase é frequentemente o maior bottleneck em projetos
de AI — a máxima "garbage in, garbage out" é literal em machine learning. Investir
tempo na qualidade dos dados aqui previne meses de frustração nas fases seguintes.

## Agentes Envolvidos

- **CTO Agent**: Lidera a avaliação técnica de dados e infraestrutura de data
- **COO Agent**: Facilita acesso a dados operacionais e processos de data collection
- **CFO Agent**: Avalia custos de preparação de dados e infraestrutura
- **CEO Agent**: Remove bloqueios organizacionais de acesso a dados
- **CHRO Agent**: Endereça questões de dados de colaboradores e privacidade
- **Chief of Staff Agent**: Coordena o processo e documenta o data readiness assessment

## Inputs Necessários

1. Use Case Charters selecionados (output da Fase 00)
2. Inventário de fontes de dados existentes na organização
3. Data dictionary ou documentação de schemas existentes
4. Políticas de privacidade e data governance vigentes
5. Requisitos regulatórios aplicáveis (GDPR, LGPD, AI Act)
6. Infraestrutura de dados atual (data warehouse, lakes, pipelines)
7. Equipa de dados disponível e suas competências

## Processo (step-by-step)

1. **Data requirements definition**: CTO Agent define os dados exatos necessários para
   cada use case, incluindo features, labels, volume mínimo e freshness requirements
2. **Data source mapping**: CTO Agent e COO Agent mapeiam onde os dados necessários
   residem na organização, identificando sistemas fonte e owners
3. **Data quality assessment**: CTO Agent executa profiling dos dados existentes,
   avaliando completude, consistência, precisão e atualidade
4. **Data gap analysis**: CTO Agent identifica gaps entre os dados necessários e os
   disponíveis, classificando cada gap por criticidade e esforço de resolução
5. **Privacy and compliance review**: CTO Agent e CHRO Agent avaliam os dados sob a
   ótica de privacidade, consent e compliance regulatória (GDPR, AI Act)
6. **Data pipeline design**: CTO Agent desenha os pipelines de dados necessários para
   extrair, transformar e carregar dados dos sistemas fonte
7. **Data preparation execution**: CTO Agent executa a limpeza, transformação e
   enriquecimento dos dados, criando datasets prontos para uso
8. **Data validation**: CTO Agent valida os datasets preparados com testes de qualidade
   automatizados e revisão manual de amostras
9. **Infrastructure setup**: CTO Agent configura a infraestrutura necessária para
   armazenamento, processamento e serving dos dados preparados
10. **Data readiness sign-off**: CTO Agent apresenta o data readiness report e confirma
    que os dados estão prontos para a fase de build/buy

## Outputs / Entregáveis

- **Data Readiness Report**: Relatório completo de avaliação de dados
- **Data Quality Scorecard**: Scorecard com métricas de qualidade por dataset
- **Data Gap Analysis**: Análise de gaps com plano de remediação
- **Data Pipeline Documentation**: Documentação dos pipelines implementados
- **Privacy Impact Assessment**: Avaliação de impacto na privacidade
- **Prepared Datasets**: Datasets limpos e validados prontos para uso
- **Data Dictionary**: Dicionário de dados atualizado com todas as features

## Quality Gates

| Gate | Critério | Responsável |
|------|----------|-------------|
| QG-01.1 | Data quality score >80% em completude, consistência e precisão | CTO Agent |
| QG-01.2 | Volume de dados suficiente para o modelo pretendido | CTO Agent |
| QG-01.3 | Privacy impact assessment completo e aprovado | CHRO Agent |
| QG-01.4 | Data pipelines automatizados e testados end-to-end | CTO Agent |
| QG-01.5 | Nenhum gap de dados crítico sem plano de resolução | CTO Agent |
| QG-01.6 | Custos de infraestrutura de dados dentro do budget | CFO Agent |

## Critérios para Avançar

Para progredir para a Fase 02 (Build or Buy), todos os critérios devem ser satisfeitos:

- [ ] Datasets preparados e validados com quality score >80%
- [ ] Privacy e compliance aprovados sem bloqueadores
- [ ] Data pipelines operacionais e documentados
- [ ] Infrastructure de dados configurada e escalável
- [ ] Data gaps críticos resolvidos ou com workaround validado
- [ ] Custos de dados dentro do envelope orçamental

## Riscos desta Fase

| Risco | Probabilidade | Impacto | Mitigação |
|-------|--------------|---------|-----------|
| Dados existentes com qualidade insuficiente | Alta | Crítico | Assessment precoce e plano de limpeza realista |
| Dados necessários não existem na organização | Média | Alto | Identificar fontes externas ou plano de coleta |
| Compliance issues que bloqueiam uso dos dados | Média | Crítico | Envolver equipa legal desde o início da fase |
| Silos organizacionais que impedem acesso a dados | Alta | Alto | CEO Agent remove bloqueios de acesso |
| Custo de preparação de dados excede o esperado | Média | Médio | Budget de contingência de 30% para data prep |

## Templates a Usar

- `templates/data-readiness-assessment.md` — Template de avaliação de data readiness
- `templates/data-quality-scorecard.md` — Scorecard de qualidade de dados
- `templates/privacy-impact-assessment.md` — Avaliação de impacto de privacidade
- `templates/data-pipeline-doc.md` — Documentação de data pipeline

## Duração Estimada

- **Mínimo**: 5 dias úteis (dados de alta qualidade já disponíveis)
- **Típico**: 10-20 dias úteis
- **Máximo**: 30 dias úteis (dados dispersos que requerem limpeza extensiva)

> **Nota**: Se os dados não estão prontos, o projeto de AI não está pronto. Não há
> atalho para qualidade de dados. Modelos treinados com dados maus produzem resultados
> maus com uma confiança enganadora.
