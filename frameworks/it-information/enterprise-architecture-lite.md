# Enterprise Architecture Lite — Arquitetura Empresarial Pragmática

## Origem e Contexto

Enterprise Architecture (EA) tradicionalmente é associada ao TOGAF e seus 10 passos formais. Para organizações de médio porte e startups em escala, o modelo completo é excessivamente burocrático. O **EA Lite** adapta os princípios fundamentais — alinhamento business-IT, racionalização de sistemas, padrões tecnológicos e governança evolutiva — em uma versão pragmática e executável.

Inspirado em:
- **TOGAF ADM** (Architecture Development Method) — simplificado para 4 fases
- **Zachman Framework** — matriz de perspectivas (what, how, where, who, when, why)
- **Ross/Weill/Robertson** — Enterprise Architecture as Strategy (operating model)
- **Wardley Mapping** — evolução de componentes tecnológicos

---

## Quando Usar

### Situações Ideais
- A organização cresceu além de 50 pessoas e tem mais de 15 sistemas internos
- Existe dor de integração entre times e ferramentas
- Decisões tecnológicas estão sendo tomadas em silos
- Precisa justificar investimento em plataforma/modernização para o board
- Fusão, aquisição ou reestruturação organizacional em andamento
- CIO precisa racionalizar portfolio de sistemas
- Migração cloud ou modernização de legado está no roadmap

### Quando NÃO Usar
- Startups em estágio inicial (< 30 pessoas, < 5 sistemas)
- Quando a decisão é puramente técnica sem impacto organizacional
- Quando o escopo é limitado a um único microserviço
- Quando speed-to-market é mais importante que governança (early-stage)

---

## Estrutura / Modelo

### Os 4 Pilares do EA Lite

```
┌─────────────────────────────────────────────────────┐
│              ENTERPRISE ARCHITECTURE LITE            │
├─────────────┬─────────────┬───────────┬─────────────┤
│  BUSINESS   │   DATA      │ APPLICATION│ TECHNOLOGY  │
│ ARCHITECTURE│ ARCHITECTURE│ ARCHITECTURE│ARCHITECTURE│
│             │             │            │             │
│ Processos   │ Entidades   │ Sistemas   │ Infra       │
│ Capacidades │ Fluxos      │ Integrações│ Plataformas │
│ Org Model   │ Ownership   │ Portfolio  │ Padrões     │
│ Value Chain │ Qualidade   │ Roadmap    │ Segurança   │
└─────────────┴─────────────┴───────────┴─────────────┘
```

### Pilar 1: Business Architecture
- **Mapa de Capacidades de Negócio**: O que a organização faz (não como)
- **Cadeia de Valor**: Atividades primárias e de suporte
- **Processos Críticos**: Top 10 processos que geram receita ou reduzem risco
- **Operating Model**: Coordenação × Padronização (Ross/Weill matrix)

### Pilar 2: Data Architecture
- **Entidades Mestras**: Cliente, Produto, Transação, Usuário
- **Golden Source**: Fonte de verdade para cada entidade
- **Fluxo de Dados**: De onde vem, para onde vai, quem transforma
- **Data Ownership**: DRI de cada domínio (Data Product Owner)
- **Qualidade**: SLAs de completude, freshness, accuracy por entidade

### Pilar 3: Application Architecture
- **Portfolio de Sistemas**: Inventário com classificação (invest, tolerate, eliminate, migrate)
- **Integrações**: Mapa de dependências (quem consome de quem)
- **Application Roadmap**: Plano de evolução por sistema
- **Padrões de Integração**: API-first, event-driven, batch, file-based

### Pilar 4: Technology Architecture
- **Stack Padrão**: Linguagens, frameworks, databases, cloud services aprovados
- **Infraestrutura**: Cloud strategy, região, DR, backup
- **Segurança**: Camadas de proteção, zero-trust, compliance
- **Tech Radar**: Adopt, Trial, Assess, Hold

---

## Processo de Aplicação (step-by-step)

### Fase 1: Discovery (2-3 semanas)
1. **Mapear Capacidades de Negócio** — workshop com líderes: "o que faz a empresa funcionar?"
2. **Inventariar Sistemas** — lista de todos os sistemas com owner, criticidade, custo, contratos
3. **Mapear Integrações** — diagrama de fluxo de dados entre sistemas
4. **Classificar o Portfolio** — para cada sistema: invest, tolerate, eliminate, migrate

### Fase 2: Target State (1-2 semanas)
5. **Definir Operating Model** — coordenação alta ou baixa? padronização alta ou baixa?
6. **Desenhar Target Architecture** — como deveria ser em 18-24 meses
7. **Identificar Gaps** — delta entre current state e target state
8. **Priorizar Gaps** — usando RICE scoring ou impacto × esforço

### Fase 3: Roadmap (1 semana)
9. **Criar Transition Architecture** — estados intermediários viáveis
10. **Definir Quick Wins** — melhorias < 30 dias de alto impacto
11. **Definir Investimentos Estruturais** — projetos de 3-6 meses que removem débito
12. **Alinhar com Budget** — associar cada item a investimento via CFO

### Fase 4: Governance (contínua)
13. **ARB Lite** — reunião mensal de 1h para revisar ADRs e exceções
14. **ADR System** — toda decisão arquitetural registrada
15. **Compliance Check** — novo sistema/integração passa por checklist de EA
16. **Quarterly Review** — atualização trimestral do portfolio e roadmap

---

## Exemplos Práticos

### Exemplo 1: Racionalização de Ferramentas SaaS
**Situação**: Empresa de 200 pessoas, 47 ferramentas SaaS, muitas com overlap.

**Aplicação**:
1. Discovery: inventário (ferramenta, custo/mês, nº usuários, owner, criticidade)
2. Classificação: 12 invest, 20 tolerate, 10 eliminate, 5 migrate
3. Quick wins: cancelar 10 ferramentas = economia R$15K/mês
4. Investimento: migrar 5 para plataforma unificada em 6 meses

### Exemplo 2: Modernização de Legado
**Situação**: Sistema monolítico de 8 anos limitando velocidade.

**Aplicação**:
1. Application Portfolio: classificar como "migrate" (lógica de negócio crítica)
2. Strangler Fig Pattern: extrair funcionalidades incrementalmente
3. Transition Architecture: 3 estados intermediários em 12 meses
4. Governance: ADR para cada decisão de extração

### Exemplo 3: Pós-Aquisição
**Situação**: Aquisição de empresa menor com stack diferente.

**Aplicação**:
1. Inventário consolidado dos dois portfolios
2. Definir "winner" para cada capability (qual sistema sobrevive)
3. Integration roadmap: dados primeiro, depois processos, depois UI
4. Governance: ARB conjunto para decisões de consolidação

---

## Armadilhas Comuns

### 1. Overengineering
- **Erro**: Criar modelo TOGAF completo com 500 páginas
- **Correção**: EA Lite foca em decisions, não diagrams

### 2. Architecture Astronaut
- **Erro**: 6 meses desenhando "estado futuro perfeito" sem entregar
- **Correção**: Quick wins em paralelo. Valor em 30 dias

### 3. Ivory Tower
- **Erro**: Equipe de EA separada criando padrões que ninguém segue
- **Correção**: EA embarcada nos times. ARB inclui tech leads

### 4. Portfolio Estático
- **Erro**: Inventário feito uma vez e nunca atualizado
- **Correção**: Review trimestral obrigatório. Novos sistemas passam por checklist

### 5. Ignorar o Business
- **Erro**: Focar apenas em tecnologia sem entender operating model
- **Correção**: Sempre começar pelo Pilar 1 (Business Architecture)

### 6. Analysis Paralysis na Fase de Discovery
- **Erro**: Tentar mapear 100% dos sistemas antes de agir
- **Correção**: 80/20 — mapear os 20 sistemas críticos, agir sobre eles, depois expandir

---

## Integração com Outros Frameworks

| Framework | Como se Integra |
|-----------|----------------|
| `cio-systems-rationalization.md` | EA fornece inventário; racionalização executa |
| `cio-data-as-product.md` | Data Architecture define fundação; Data as Product define operação |
| `cio-integration-architecture.md` | EA mapeia; Integration Architecture implementa |
| `engineering-tech/adr-system.md` | ADRs são o mecanismo de governance do EA Lite |
| `engineering-tech/platform-engineering.md` | Technology Architecture define alvo; Platform executa |
| `engineering-tech/build-vs-buy-framework.md` | EA informa decisões com contexto completo |
| `vision-strategy/wardley-mapping.md` | Wardley Maps complementam EA com visão evolutiva |
| `cfo-strategist/cfo-capital-allocation.md` | EA informa decisões de investimento |

---

## Referências

- Ross, Weill, Robertson — *Enterprise Architecture as Strategy* (2006)
- TOGAF Standard, 10th Edition — The Open Group (simplificado)
- Zachman, John — *A Framework for Information Systems Architecture* (IBM, 1987)
- Wardley, Simon — *Wardley Maps* (2019, domínio público)
- Skelton, Pais — *Team Topologies* (2019) — alinhamento org/tech
- `reference/books/it-governance/ross-enterprise-architecture.md`
