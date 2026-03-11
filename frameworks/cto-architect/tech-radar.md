# Tech Radar — Framework de Avaliação e Adoção Tecnológica

## Propósito e Contexto

O Tech Radar é um instrumento de governança tecnológica que classifica tecnologias, ferramentas,
linguagens, plataformas e práticas em quatro anéis de maturidade (Adopt, Trial, Assess, Hold),
organizadas em quatro quadrantes. Inspirado no modelo da ThoughtWorks, este framework adapta o
conceito para o contexto de empresas de tecnologia brasileiras, incorporando critérios de
ecossistema local, disponibilidade de talentos e restrições regulatórias.

Sem um Tech Radar explícito, organizações sofrem de dois problemas opostos: "resume-driven
development" (engenheiros escolhem tecnologias por interesse pessoal) ou "technology freeze"
(a organização nunca evolui sua stack por medo de risco). O radar cria um caminho do meio:
exploração disciplinada com critérios claros de promoção e descontinuação.

## Quando Usar

- Na definição ou revisão da estratégia tecnológica semestral
- Ao avaliar adoção de nova tecnologia proposta por um time
- Em processos de due diligence técnica (M&A, investimento)
- No onboarding de novos engenheiros (entender o que usamos e por quê)
- Quando há proliferação descontrolada de tecnologias
- Na construção do tech brand da empresa (atração de talentos)

## Componentes do Framework

### 1. Os Quatro Anéis

**ADOPT (Adotar)**
Tecnologias maduras que recomendamos fortemente. Devem ser o default para novos projetos.
- Critérios: comprovada em produção por ≥ 6 meses, equipe treinada, suporte disponível
- Exemplo: Kubernetes para orquestração, PostgreSQL para dados relacionais

**TRIAL (Experimentar)**
Tecnologias promissoras em uso controlado. Podem ser usadas em projetos não-críticos.
- Critérios: POC bem-sucedida, sponsor técnico identificado, plano de rollback
- Exemplo: nova versão de framework, serviço gerenciado em teste

**ASSESS (Avaliar)**
Tecnologias interessantes que merecem investigação. Ainda não para uso em projetos reais.
- Critérios: relevância estratégica identificada, pesquisa em andamento
- Exemplo: tecnologias emergentes, novas abordagens arquiteturais

**HOLD (Evitar)**
Tecnologias que não devem ser adotadas em novos projetos. Podem estar em uso legado.
- Critérios: alternativa melhor disponível, ou riscos identificados
- Inclui: tecnologias em sunset, com vulnerabilidades conhecidas, ou sem comunidade

### 2. Os Quatro Quadrantes

**Linguagens & Frameworks:** Linguagens de programação, frameworks web/mobile, SDKs
**Plataformas & Infra:** Cloud services, orquestração, bancos de dados, mensageria
**Ferramentas:** DevTools, CI/CD, observabilidade, IDEs, ferramentas de produtividade
**Técnicas & Práticas:** Patterns arquiteturais, metodologias, práticas de engenharia

### 3. Ficha de Avaliação

Para cada tecnologia avaliada, preencher:

```markdown
## [Nome da Tecnologia]
- **Quadrante:** [Linguagens|Plataformas|Ferramentas|Técnicas]
- **Anel:** [Adopt|Trial|Assess|Hold]
- **Movimento:** [Novo|Mantido|Promovido|Rebaixado]
- **Sponsor:** [Nome do tech lead responsável]
- **Última avaliação:** [Data]

### Avaliação
- Maturidade (1-5): ___
- Ecossistema/Comunidade (1-5): ___
- Disponibilidade de talentos no Brasil (1-5): ___
- Fit estratégico (1-5): ___
- Custo de adoção (1-5, onde 5 = baixo custo): ___
- Risco de lock-in (1-5, onde 5 = baixo risco): ___

### Justificativa
[Por que está neste anel? O que precisaria mudar para ser promovida/rebaixada?]

### Experiências Internas
[Resumo de uso interno, se houver]
```

## Processo Passo-a-Passo

### Fase 1: Inventário Tecnológico (2 semanas)
1. Catalogar todas as tecnologias em uso na organização
2. Identificar owners/sponsors para cada tecnologia
3. Coletar feedback de equipes sobre dores e oportunidades
4. Mapear gaps: áreas onde faltam boas ferramentas/práticas

### Fase 2: Avaliação e Classificação (1-2 semanas)
1. Tech leads preenchem fichas de avaliação para suas áreas
2. Sessão de calibração com liderança técnica (cross-team)
3. Resolução de divergências com critérios objetivos
4. Classificação final nos anéis e quadrantes

### Fase 3: Publicação e Comunicação (1 semana)
1. Publicar radar visual (ferramenta: Zalando Tech Radar, ou custom)
2. Escrever blips narrativos para cada tecnologia
3. Comunicar mudanças relevantes para toda engenharia
4. Atualizar guidelines de novos projetos

### Fase 4: Governança Contínua
1. Revisão semestral completa
2. Processo fast-track para tecnologias urgentes (aprovação por comitê)
3. Retrospectiva de adoções passadas: acertamos?
4. Atualização incremental conforme novas avaliações

## Template do Tech Radar

```
ADOPT                    TRIAL
├── Kubernetes           ├── Deno (runtime)
├── PostgreSQL           ├── Temporal (workflows)
├── TypeScript           ├── OpenTelemetry
├── React                ├── Rust (serviços críticos)
├── Terraform            └── LangChain (AI apps)
├── GitHub Actions
└── Datadog              ASSESS
                         ├── WebAssembly
HOLD                     ├── Qdrant (vector DB)
├── Jenkins              ├── Bun (runtime)
├── jQuery               ├── Effect-TS
├── MongoDB (novos)      └── WASI
├── Heroku
└── CoffeeScript
```

## Checklist de Governança

- [ ] O radar é revisado pelo menos semestralmente?
- [ ] Cada tecnologia em TRIAL tem um sponsor e timeline para decisão?
- [ ] Tecnologias em HOLD têm plano de migração para alternativas?
- [ ] O radar é público internamente e acessível a todos os engenheiros?
- [ ] Novos projetos consultam o radar antes de escolher tecnologias?
- [ ] Exceções ao radar são documentadas e aprovadas por liderança técnica?
- [ ] Existe processo fast-track para avaliação de tecnologias urgentes?
- [ ] O radar considera disponibilidade de talentos no mercado local?

## Métricas de Sucesso

| Métrica | Alvo | Frequência |
|---------|------|------------|
| Compliance com radar | > 90% dos novos projetos usam tech do anel Adopt | Trimestral |
| Tecnologias em HOLD com migration plan | 100% | Semestral |
| Tempo médio de avaliação (Assess → Trial) | < 3 meses | Contínuo |
| Developer satisfaction com tech stack | > 4/5 em pesquisa | Semestral |
| Tecnologias orphaned (sem sponsor) | 0 | Contínuo |
| Diversidade controlada (tech por categoria) | ≤ 2 opções Adopt por categoria | Semestral |

## Referências Cruzadas

- `frameworks/cto-architect/build-vs-buy.md` — Decisão de construir vs. comprar
- `frameworks/cto-architect/tech-debt-management.md` — Tecnologias em HOLD geram dívida técnica
- `frameworks/cto-architect/platform-strategy.md` — Radar como insumo para plataforma
- `frameworks/cto-architect/engineering-excellence.md` — Práticas no quadrante Técnicas
- `frameworks/cio-engineer/cloud-strategy.md` — Plataformas cloud no radar
- `frameworks/caio-architect/mlops-framework.md` — Ferramentas de ML no radar
- `frameworks/shared/decision-framework.md` — Critérios de decisão para promoção no radar
