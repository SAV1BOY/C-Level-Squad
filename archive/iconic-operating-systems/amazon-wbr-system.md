# Amazon WBR System — O Sistema Operacional da Amazon

> Análise do Weekly Business Review da Amazon como sistema operacional organizacional.

---

## Contexto Histórico

O WBR (Weekly Business Review) é o coração do sistema operacional da Amazon,
implementado desde os primeiros anos da empresa e refinado ao longo de mais
de duas décadas. Jeff Bezos e a equipa de liderança desenharam este sistema
para escalar a tomada de decisão à medida que a empresa crescia exponencialmente.

---

## Princípios Fundamentais

### 1. Input Metrics Over Output Metrics
A Amazon foca-se em métricas de input (o que controlamos) em vez de output
(o que observamos). Output metrics como revenue são consequência de inputs
como selection, price, convenience.

Exemplo:
- **Output**: revenue (não controlamos directamente)
- **Input**: número de items disponíveis, tempo de entrega, preço competitivo
  (controlamos directamente)

### 2. Andon Cord Mentality
Quando uma métrica está fora do esperado, qualquer pessoa pode "puxar o cord"
para escalar atenção. Inspirado na Toyota, este princípio garante que
problemas são visíveis rapidamente.

### 3. Narratives Over Slides
A Amazon famosamente proíbe PowerPoint em reuniões de decisão. Em vez disso,
usa documentos narrativos de 6 páginas (six-pagers) que são lidos em silêncio
no início da reunião. Isto força pensamento estruturado e elimina a ilusão
de compreensão que slides criam.

### 4. Working Backwards
Antes de construir algo, a Amazon escreve o press release do produto final.
Isto garante que o customer value é definido antes de investir recursos.

---

## Estrutura do WBR

### Frequência e Formato
- **Semanal**: sem excepções, mesmo durante crises
- **Duração**: 60-90 minutos
- **Participantes**: VP + directs + data analysts
- **Formato**: data pack distribuído 24h antes, discussão focada em anomalias

### Conteúdo do Data Pack
O data pack do WBR inclui:
1. **Métricas-chave** com trend lines (52 semanas)
2. **Week-over-week** e year-over-year comparisons
3. **Andon alerts**: métricas fora do threshold com root cause
4. **Action item tracker**: status de acções da semana anterior
5. **Deep dives**: análise detalhada de 1-2 temas seleccionados

### Processo da Reunião
```
0-10 min: Review do data pack (leitura individual)
10-30 min: Discussion de métricas com anomalias
30-50 min: Deep dive em 1-2 temas
50-60 min: Action items e decisões
```

---

## Métricas no Estilo Amazon

### Características das Métricas
- **Controllable**: a equipa pode influenciar directamente
- **Auditable**: dados podem ser verificados e rastreados
- **Timely**: disponíveis com frequência suficiente (idealmente diária/semanal)
- **Actionable**: se a métrica muda, sabemos o que fazer

### Exemplos de Input Metrics
| Área | Input Metric | Output Metric |
|------|-------------|---------------|
| Retail | Items in stock | Revenue |
| Delivery | On-time dispatch rate | Customer satisfaction |
| Hiring | Applications processed | Headcount vs plan |
| Tech | Deploy frequency | System reliability |
| Support | Average handle time | Customer resolution |

### O Conceito de "Metrics Ownership"
Cada métrica tem um owner individual que:
- Compreende a métrica profundamente
- Apresenta a métrica na WBR quando há anomalia
- É responsável por investigar desvios
- Propõe e implementa correcções

---

## Lições para o C-Level Squad

### O Que Adoptar
1. **Cadência semanal inegociável**: a WBR nunca é cancelada
2. **Data-driven discussion**: conversas baseadas em dados, não opiniões
3. **Input metrics focus**: controlar o que é controlável
4. **Anomaly-based agenda**: discutir o que está fora do normal, não tudo
5. **Action tracking rigoroso**: follow-through de cada item
6. **Written narratives**: documentos escritos sobre slides

### O Que Adaptar
1. **Escala**: Amazon opera com centenas de métricas; squad mais pequeno
   precisa de menos (5-15 métricas core)
2. **Formalidade**: Amazon é altamente formal; adaptar ao contexto cultural
3. **Andon cord**: implementar versão simplificada de alertas automáticos
4. **Six-pager**: adaptar extensão ao contexto (2-3 páginas pode ser suficiente)
5. **Data infrastructure**: Amazon tem sistemas massivos; começar com o possível

### O Que Evitar
1. **Copiar sem adaptar**: o sistema Amazon funciona na Amazon; adaptar é essencial
2. **Métricas sem owner**: cada métrica precisa de dono accountable
3. **Data pack como decoração**: se ninguém lê, não serve
4. **WBR como status meeting**: é para decidir e agir, não para reportar
5. **Excesso de métricas**: começar com poucas e expandir com maturidade

---

## Impacto Organizacional

O sistema WBR é creditado com vários resultados na Amazon:
- Velocidade de execução apesar de escala massiva
- Consistência operacional em centenas de equipas
- Detecção precoce de problemas (antes de se tornarem crises)
- Cultura de accountability baseada em dados
- Scalability: o mesmo sistema funciona de 10 a 100.000 pessoas

---

## Referências e Leitura Adicional

- "Working Backwards" — Colin Bryar & Bill Carr
- "The Amazon Way" — John Rossman
- Amazon's internal leadership principles
- Annual shareholder letters de Jeff Bezos

---

## Notas Técnicas

- O C-Level Squad adopta o espírito do WBR na sua cadência semanal
- Template de WBR em `templates/` é inspirado no modelo Amazon
- Métricas pack builder em `scripts/generation/` segue princípios Amazon
- Adaptações documentadas na secção de cadências do operating system
