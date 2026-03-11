# Google OKR System - Deep Dive

## Contexto

O sistema de OKRs (Objectives and Key Results) foi trazido para o Google por
John Doerr em 1999, quando a empresa tinha ~40 funcionários. Originado na Intel
por Andy Grove nos anos 1970, o sistema foi adotado pelo Google como principal
framework de goal-setting e se tornou referência global. Hoje, com 180K+
funcionários, o Google continua usando OKRs como espinha dorsal de alinhamento.

## Estrutura do Sistema

### Objective (O)
- **O que queremos alcançar**
- Qualitativo e inspiracional
- Ambicioso mas não impossível
- Claro o suficiente para que qualquer pessoa entenda
- Tempo-limitado (trimestral na maioria dos casos)

### Key Results (KR)
- **Como saberemos que alcançamos o objective**
- Quantitativo e mensurável (número, porcentagem, sim/não)
- 2-5 KRs por Objective
- Deve ser verificável sem ambiguidade
- Difícil mas alcançável (meta: atingir 60-70%)

### Exemplo Google Real (Simplificado)

**Objective:** Tornar o Gmail o serviço de email mais rápido do mundo

**Key Results:**
1. Reduzir latência de carregamento de inbox para <1 segundo (p95)
2. Alcançar 99.99% de uptime no trimestre
3. Reduzir tempo de busca em emails para <200ms
4. Zero downtime perceptível pelo usuário durante deploys

## Princípios Fundamentais

### 1. OKRs São Públicos
- Todos os OKRs de todos os funcionários são visíveis para toda a empresa
- Qualquer pessoa pode ver os OKRs do CEO, de VPs, de ICs
- Transparência cria alinhamento natural e accountability social
- Facilita colaboração cross-team

### 2. OKRs Não São Vinculados a Compensação
Esta é talvez a decisão mais importante e contra-intuitiva:
- Performance reviews consideram OKRs mas não são determinados por eles
- Isso permite que pessoas definam OKRs ambiciosos sem medo de "falhar"
- Se OKRs determinassem bônus, todos definiriam metas fáceis
- OKRs são ferramenta de alinhamento, não de avaliação

### 3. 60-70% É o Target Ideal
- Se você atinge 100% dos KRs, suas metas eram fáceis demais
- Se você atinge 30%, suas metas eram irrealistas
- O sweet spot de 60-70% significa ambição calibrada
- "Moonshots" (OKRs muito ambiciosos) podem ter target de 40-50%

### 4. Mix de Top-Down e Bottom-Up
- ~40% dos OKRs vêm de cima (alinhamento com estratégia da empresa)
- ~60% dos OKRs vêm de baixo (ownership e autonomia dos times)
- O processo de definição é iterativo: proposta → feedback → ajuste

### 5. Cadência Trimestral
- OKRs são definidos a cada trimestre
- Mid-quarter check-in para ajustar se necessário
- Score final no final do trimestre
- Company-level OKRs definidos anualmente com breakdown trimestral

## Processo de Definição no Google

### Semana 1-2: Company OKRs
- Liderança executiva define 3-5 OKRs company-level
- Apresentados em all-hands para toda a empresa
- Q&A aberto para esclarecimento

### Semana 2-3: Team OKRs
- Cada time/departamento define seus OKRs alinhados com company OKRs
- Discussão com times adjacentes para evitar conflitos
- Manager revisa com reports para garantir alinhamento e ambição

### Semana 3-4: Individual OKRs
- Cada pessoa define 3-5 OKRs pessoais
- Alinhados com team OKRs + contribuição individual
- Revisados com manager e publicados

### Semana 4+: Execução
- OKRs publicados e visíveis para toda a empresa
- Check-ins semanais informais
- Mid-quarter review formal
- End-of-quarter scoring

## Scoring e Avaliação

### Escala de Score
- **0.0:** Nenhum progresso
- **0.3:** Progresso mínimo, longe da meta
- **0.5:** Progresso significativo mas não atingiu
- **0.7:** Atingiu a meta (este é o target para OKRs ambiciosos)
- **1.0:** Excedeu a meta significativamente

### Regras de Scoring
- Self-assessment primeiro (o próprio dono do OKR pontua)
- Manager review para calibração
- Não existe "score perfeito" - 0.7 é excelente para OKRs ambiciosos
- Scores são input para reflexão, não para ranking

### O Que Fazer com Scores Baixos
- 0.0-0.3 consistentemente: OKRs mal definidos ou prioridades erradas
- Investigar: falta de recursos? Escopo errado? Dependência bloqueada?
- Não é fracasso: é informação sobre onde ajustar

### O Que Fazer com Scores Altos
- 0.9-1.0 consistentemente: OKRs não ambiciosos o suficiente
- Aumentar a ambição no próximo trimestre
- "Sandbagging" (definir metas fáceis) é culturalmente mal visto

## Armadilhas Comuns

### 1. OKRs Como Lista de Tarefas
**Errado:** KR = "Lançar feature X"
**Certo:** KR = "Aumentar retenção de 30 dias em 5% com feature X"

Lançar uma feature é uma tarefa, não um resultado. O resultado é o impacto.

### 2. OKRs Demais
**Errado:** 10 Objectives com 5 KRs cada = 50 itens para acompanhar
**Certo:** 3-5 Objectives com 2-3 KRs cada = 9-15 itens focados

Se tudo é prioridade, nada é prioridade.

### 3. OKRs Sem Ownership
**Errado:** "O time vai melhorar a experiência do cliente"
**Certo:** "[Nome] vai reduzir NPS detractors de 25% para 15%"

Sem owner individual, ninguém é accountable.

### 4. OKRs Vinculados a Bônus
Quando OKRs determinam compensação, as pessoas:
- Definem metas fáceis (sandbag)
- Evitam OKRs ambiciosos (risk aversion)
- Manipulam métricas (Goodhart's Law)
- Não compartilham OKRs publicamente (medo de falhar)

### 5. OKRs Definidos e Esquecidos
- Se OKRs só são revistos no final do trimestre, não funcionam
- Check-ins semanais (informais) e mid-quarter (formais) são essenciais
- OKRs devem influenciar priorização diária

## Evolução no Google (2000-Presente)

### 2000-2005: Adoção Inicial
- OKRs simples e company-wide
- Larry e Sergey definiam OKRs pessoalmente
- Cultura de ambição extrema ("10x thinking")

### 2005-2015: Escala
- Sistema formalizado para 50K+ funcionários
- Ferramentas internas para gerenciar OKRs
- Treinamento obrigatório para novos googlers
- Cross-functional OKRs para projetos complexos

### 2015-2020: Refinamento
- Separação mais clara entre "committed" e "aspirational" OKRs
- Committed: espera-se 100% de achievement
- Aspirational: espera-se 60-70% de achievement
- Maior foco em outcomes vs outputs

### 2020-Presente: Integração com AI
- AI assistindo na definição de OKRs (sugestão de métricas, benchmarks)
- Dashboards automatizados para tracking
- Alertas proativos para KRs em risco
- Análise de padrões cross-company para identificar conflitos

## Implementação na Sua Empresa

### Pré-Requisitos
1. **Buy-in da liderança:** CEO deve definir e publicar seus próprios OKRs
2. **Cultura de transparência:** OKRs públicos requerem segurança psicológica
3. **Separação de compensação:** OKRs NÃO determinam bônus
4. **Dados disponíveis:** KRs mensuráveis precisam de instrumentação

### Roadmap de Implementação

**Trimestre 1: Piloto**
- 1-2 times piloto
- Treinamento sobre princípios de OKR
- Definição de OKRs de time apenas (sem individual)
- Mid-quarter e end-of-quarter review

**Trimestre 2: Expansão**
- Expandir para todos os times
- Introduzir OKRs individuais
- Company OKRs definidos pela liderança
- Retrospectiva do piloto informa ajustes

**Trimestre 3: Maturidade**
- Cross-functional OKRs para projetos que cruzam times
- Dashboard de OKRs acessível a todos
- Check-ins semanais incorporados à rotina

**Trimestre 4: Otimização**
- Análise de scoring patterns (times sandbaggeando? ambição insuficiente?)
- Ajuste de processos baseado em 3 trimestres de dados
- Treinamento avançado para managers

## OKRs vs Outros Frameworks

| Aspecto | OKRs | KPIs | MBOs | SMART Goals |
|---------|------|------|------|-------------|
| Ambição | Stretch (60-70% = sucesso) | Realista (100% = sucesso) | Negociados | Achievable |
| Transparência | Públicos | Geralmente privados | Privados | Privados |
| Cadência | Trimestral | Contínuo | Anual | Variável |
| Vinculação a comp | Não | Frequentemente sim | Sim | Variável |
| Foco | Outcomes | Métricas operacionais | Metas individuais | Metas individuais |

## Referências

- "Measure What Matters" - John Doerr (2018)
- "High Output Management" - Andy Grove (1983)
- Google re:Work: "Guide to OKRs" (rework.withgoogle.com)
- "Radical Focus" - Christina Wodtke (2016)
- "Objectives and Key Results" - Paul Niven & Ben Lamorte (2016)
- Talks de Rick Klau (Google Ventures) sobre OKRs no YouTube
