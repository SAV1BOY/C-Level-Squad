# Gold Standard & State of the Art

> Definição do que constitui Gold Standard no C-Level Squad e como se relaciona com o estado da arte.

---

## Conceitos Fundamentais

### Gold Standard — O Nosso Padrão de Excelência
O Gold Standard define o nível de qualidade que o C-Level Squad aspira em todos
os seus outputs e processos. É o benchmark interno contra o qual avaliamos
tudo o que produzimos.

### State of the Art (SOTA) — O Melhor que Existe
SOTA representa as melhores práticas e os melhores resultados conhecidos numa
determinada área, independentemente de quem os produz. É o benchmark externo
que informa o nosso Gold Standard.

### Relação Entre os Dois
```
SOTA = O que é possível (externo, evolui com o mercado)
Gold Standard = O que exigimos de nós (interno, evolui com o SOTA)
Gold Standard ≤ SOTA (aspiramos ao SOTA, mas aceitamos limitações práticas)
```

---

## Gold Standard por Área

### 1. Decisões
O gold standard de uma decisão no C-Level Squad:
- **Enquadramento claro**: problema definido em 1 frase
- **Evidência robusta**: dados quantitativos + qualitativos
- **Alternativas genuínas**: mínimo 2 opções viáveis consideradas
- **Vieses mitigados**: checklist de vieses aplicada
- **Registo completo**: todos os campos do decision log preenchidos
- **Outcome tracking**: resultado acompanhado vs expectativa
- **Learning captured**: lição aprendida registada

### 2. Reuniões
O gold standard de uma reunião:
- **Agenda pré-publicada**: 24h antes com pre-read
- **Início pontual**: ≤2 min de atraso
- **Decision rate**: ≥90% das decisões agendadas resolvidas
- **Participação activa**: >80% dos participantes contribuem
- **Overhead mínimo**: ≤15% do tempo em admin/tangentes
- **Action items claros**: owner + acção + prazo para cada
- **Minutes em 24h**: registo distribuído no dia seguinte

### 3. Documentação
O gold standard de um documento:
- **Propósito claro**: leitor sabe porquê existe e para quem é
- **Estrutura lógica**: headers hierárquicos, progressão natural
- **Conteúdo substantivo**: sem padding, cada linha agrega valor
- **Actionable**: leitor sabe o que fazer com a informação
- **Actualizado**: data de última revisão visível
- **Referenciado**: links para documentos relacionados
- **Testado**: pelo menos 1 pessoa além do autor validou

### 4. Métricas e Reports
O gold standard de um metrics pack:
- **Precisão**: dados verificados contra fonte original
- **Contexto**: actual vs target vs período anterior vs trend
- **Visualização**: gráfico adequado ao tipo de dado
- **Insight**: não apenas dados, mas interpretação e implicação
- **Timeliness**: distribuído dentro do prazo acordado
- **Actionability**: cada métrica fora do target tem owner e plano

### 5. Comunicação
O gold standard de uma comunicação:
- **Audiência-aware**: adaptada ao receptor
- **BLUF**: conclusão/pedido no primeiro parágrafo
- **Concisa**: sem palavras desnecessárias
- **Completa**: toda a informação necessária incluída
- **Tone-right**: tom adequado ao contexto e relação
- **Actionable**: claro o que o receptor deve fazer

### 6. Processos
O gold standard de um processo:
- **Documentado**: passos escritos e acessíveis
- **Testado**: executado pelo menos 3 vezes com sucesso
- **Eficiente**: sem passos redundantes
- **Quality gated**: verificações em pontos críticos
- **Medido**: métricas de performance do processo definidas
- **Melhorado**: revisto periodicamente com base em dados

---

## Como Medir Aderência ao Gold Standard

### Scoring Framework
Para cada área, cada critério do gold standard é avaliado:
```
5 = Exemplar (supera o gold standard)
4 = Cumpre (atinge o gold standard)
3 = Próximo (maioria dos critérios cumpridos)
2 = Abaixo (vários critérios não cumpridos)
1 = Falha (não atinge mínimos)
```

### Gold Standard Score (GSS)
```
GSS por área = média dos scores dos critérios × 20 (escala 0-100)
GSS geral = média ponderada das áreas
```

### Targets
| Classificação | GSS | Interpretação |
|--------------|-----|---------------|
| World-class | 90+ | Referência para outros |
| Excellent | 80-89 | Consistentemente alto |
| Good | 70-79 | Sólido, espaço para melhorar |
| Developing | 60-69 | Em progresso |
| Below standard | <60 | Requer acção |

---

## State of the Art — Referências Externas

### Fontes de SOTA
Para manter o gold standard actualizado, monitorizamos:
1. **Publicações académicas**: pesquisa em management, AI, org design
2. **Empresas de referência**: Amazon, Netflix, Spotify, Stripe, GitLab
3. **Conferências**: talks e workshops do sector
4. **Livros**: literatura recente em liderança e operações
5. **Benchmarks do sector**: estudos comparativos publicados
6. **Communities of practice**: grupos profissionais e fóruns

### Áreas SOTA Monitorizadas
| Área | Referência SOTA | Frequência de Review |
|------|----------------|---------------------|
| Operating cadence | Amazon WBR system | Anual |
| Decision-making | Behavioral economics research | Semestral |
| AI governance | EU AI Act + industry standards | Trimestral |
| Remote/hybrid ops | GitLab handbook + research | Semestral |
| Metrics & analytics | Data-driven management lit. | Semestral |
| Org design | Spotify model + evolutions | Anual |

---

## Evolução do Gold Standard

### Processo de Actualização
1. **Trigger**: nova SOTA identificada, ou GSS abaixo de target por 2 trimestres
2. **Análise**: avaliar gap entre gold standard actual e SOTA
3. **Proposta**: definir novo gold standard para a área
4. **Aprovação**: Vision Chief aprova alteração
5. **Comunicação**: squad informado das novas expectativas
6. **Período de adaptação**: 1 trimestre para atingir novo standard
7. **Medição**: GSS recalculado com novos critérios

### Princípios de Evolução
- Gold standard sobe gradualmente, nunca desce
- Cada subida é baseada em dados, não aspiração
- Período de adaptação antes de accountability
- Recursos e formação disponibilizados para atingir novo standard

---

## Notas Técnicas

- Critérios de gold standard documentados neste ficheiro
- GSS calculado trimestralmente como parte do quarterly review
- Referências SOTA mantidas em `reference/`
- Histórico de GSS em `data/quality/gold-standard-scores/`
- Review anual completa do gold standard pelo Vision Chief
