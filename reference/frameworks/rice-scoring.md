# Framework: RICE Scoring

## Descrição

RICE é um framework de priorização desenvolvido pela Intercom para classificar e comparar iniciativas de produto de forma objetiva. O acrônimo representa Reach (Alcance), Impact (Impacto), Confidence (Confiança) e Effort (Esforço). O score RICE = (Reach x Impact x Confidence) / Effort, produzindo um número comparável que reduz o viés na priorização. É especialmente útil quando há muitas ideias competindo por recursos limitados e decisões precisam ser justificadas com dados.

## Quando Usar

### Situações Ideais
- Priorização de backlog de produto com muitas iniciativas
- Comparação objetiva entre features, projetos ou investimentos
- Quando stakeholders discordam sobre prioridades e é necessário critério comum
- Planning trimestral ou semestral de roadmap
- Avaliação de oportunidades de investimento em startups (adaptado)
- Qualquer decisão onde múltiplas opções competem por recursos limitados

### Quando NÃO Usar
- Decisões estratégicas de alto nível (RICE é tático, não estratégico)
- Quando todas as opções são igualmente importantes (ex: compliance obrigatório)
- Para comparar coisas fundamentalmente diferentes (ex: feature vs. infra)
- Quando não há dados minimamente confiáveis para estimar os componentes

## Como Aplicar

### Os Quatro Componentes

#### Reach (Alcance)
```
Definição: Quantas pessoas/transações serão impactadas em um período definido?
Unidade: Número de clientes, transações, usuários por trimestre

Exemplos:
- "Esta feature será usada por 500 clientes/trimestre" → Reach = 500
- "Este email atingirá 10.000 pessoas/trimestre" → Reach = 10.000
- "Esta melhoria afeta 100% dos usuários (50.000)" → Reach = 50.000

Dica: usar dados reais de analytics, não estimativas otimistas
```

#### Impact (Impacto)
```
Definição: Quanto cada pessoa impactada será afetada?
Escala padronizada:
- 3 = Impacto massivo (game-changer para o cliente)
- 2 = Impacto alto
- 1 = Impacto médio
- 0.5 = Impacto baixo
- 0.25 = Impacto mínimo

Dica: medir em relação à métrica-alvo (conversão, retenção, NPS, etc.)
```

#### Confidence (Confiança)
```
Definição: Quão confiantes estamos nas estimativas de Reach e Impact?
Escala padronizada:
- 100% = Alta confiança (dados sólidos, pesquisa feita)
- 80% = Média confiança (alguma evidência)
- 50% = Baixa confiança (intuição, pouca evidência)

Dica: quanto menos evidence, menor a confidence
Se confidence < 50%, talvez seja melhor fazer discovery primeiro
```

#### Effort (Esforço)
```
Definição: Quanto trabalho será necessário? (em pessoa-meses ou story points)
Unidade: Pessoa-meses (1 pessoa trabalhando 1 mês = 1)

Exemplos:
- Design (0.5) + Dev (2) + QA (0.5) = 3 pessoa-meses
- Uma sprint de 1 dev = 0.5 pessoa-mês

Dica: incluir todas as disciplinas (design, dev, QA, launch)
```

### Fórmula
```
RICE Score = (Reach × Impact × Confidence) / Effort

Exemplo 1: Feature de onboarding
- Reach: 2.000 novos users/trimestre
- Impact: 2 (alto)
- Confidence: 80%
- Effort: 2 pessoa-meses
- RICE = (2000 × 2 × 0.8) / 2 = 1.600

Exemplo 2: Dashboard avançado
- Reach: 300 power users/trimestre
- Impact: 1 (médio)
- Confidence: 50%
- Effort: 4 pessoa-meses
- RICE = (300 × 1 × 0.5) / 4 = 37.5

Prioridade clara: Feature de onboarding (1.600 >> 37.5)
```

## Exemplos

### Tabela de Priorização
```
| Iniciativa          | Reach | Impact | Conf | Effort | RICE  |
|---------------------|-------|--------|------|--------|-------|
| Onboarding wizard   | 2000  | 2      | 80%  | 2      | 1600  |
| Mobile app          | 5000  | 1      | 50%  | 8      | 312   |
| API v2              | 800   | 3      | 80%  | 6      | 320   |
| SSO integration     | 400   | 2      | 100% | 1      | 800   |
| Dashboard avançado  | 300   | 1      | 50%  | 4      | 37.5  |

Ordem de prioridade: Onboarding > SSO > API v2 > Mobile > Dashboard
```

### Adaptação para Decisões de Investimento
```
| Investimento        | Reach   | Impact | Conf | Effort | Score |
|---------------------|---------|--------|------|--------|-------|
| Automação vendas    | R$500K  | 2      | 80%  | R$100K | 8.0   |
| Novo mercado LATAM  | R$2M    | 1      | 50%  | R$500K | 2.0   |
| Upgrade infra       | R$300K  | 3      | 90%  | R$200K | 4.05  |

(Reach em receita potencial, Effort em investimento necessário)
```

## Limitações

- **Falsa objetividade** - Os inputs (especialmente Impact) são subjetivos
- **Gaming** - Equipes podem inflar Reach/Impact para suas iniciativas favoritas
- **Não captura interdependências** - Projetos que habilitam outros não pontuam bem
- **Viés de curto prazo** - Favorece quick wins sobre investimentos estratégicos de longo prazo
- **Não captura risco** - Confidence tenta, mas não substitui análise de risco real
- **Comparação entre domínios** - Difícil comparar feature de produto com projeto de infra
- **Escala de Impact** - Escala de 0.25-3 é arbitrária e difícil de calibrar
- **Não substitui julgamento** - RICE deve informar decisão, não substituí-la
