# Strategy Blocks — Blocos Reutilizáveis para Documentos Estratégicos

> Referência do C-Level Squad para articular e documentar estratégia de forma clara e acionável.
> Estratégia sem documentação clara é apenas intenção. Documentação sem clareza é apenas burocracia.

---

## 1. Vision Statement Block

### Propósito
Articular o futuro desejado de forma inspiradora mas concreta. A visão responde: "Para onde estamos indo e por quê?"

### Template

```markdown
## Visão

### Declaração de visão
[Uma frase que descreve o estado futuro que a organização busca criar]

**Formato recomendado:**
"Criar um mundo onde [grupo de pessoas] pode [fazer algo transformador] sem [barreira atual]."

### Horizonte temporal
[Quando esperamos nos aproximar desta visão: 3, 5 ou 10 anos]

### Como saberemos que estamos progredindo
[3-5 indicadores concretos que mostram progresso em direção à visão]
1. [Indicador 1]
2. [Indicador 2]
3. [Indicador 3]

### O que NÃO é nossa visão
[Explicitar o que estamos conscientemente deixando de fora — tão importante quanto o que incluímos]
- Não estamos tentando [X]
- Não atendemos [Y segmento] intencionalmente
```

### Critérios de qualidade de uma boa visão
- **Inspiradora:** Motiva as pessoas a investir energia
- **Direcionadora:** Ajuda a priorizar (se não ajuda a dizer "não", é vaga demais)
- **Memorável:** Pode ser repetida de memória
- **Ambiciosa mas credível:** Stretching mas não fantasiosa
- **Estável:** Não muda a cada quarter (muda a cada 3-5 anos no máximo)

### Exemplo

```markdown
## Visão

### Declaração
"Tornar cada PME brasileira capaz de tomar decisões baseadas em dados com a mesma sofisticação de uma Fortune 500."

### Horizonte: 5 anos (2031)

### Indicadores de progresso
1. 10.000+ PMEs ativas na plataforma
2. >70% das decisões de negócio dos clientes informadas pela plataforma
3. Clientes com +30% de crescimento vs. peers sem a plataforma

### O que NÃO é
- Não somos uma consultoria (produto self-service)
- Não atendemos Enterprise (foco exclusivo em PME)
- Não fazemos BI genérico (foco em decisão, não em dashboards)
```

---

## 2. Strategic Thesis Block

### Propósito
Articular a hipótese central que fundamenta a estratégia. A tese responde: "Qual é nossa aposta fundamental sobre como o mundo funciona?"

### Template

```markdown
## Tese Estratégica

### Declaração da tese
"Acreditamos que [tendência/insight sobre o mercado/mundo], portanto [consequência lógica],
o que cria a oportunidade de [o que vamos fazer] para [para quem], capturando valor através de [como monetizamos]."

### Evidências que suportam a tese
| # | Evidência                              | Tipo       | Força     |
|---|----------------------------------------|------------|-----------|
| 1 | [dado, tendência, ou observação]       | [quant/qual]| [forte/média/fraca] |
| 2 | [...]                                  | [...]      | [...]     |

### Premissas implícitas
[Quais coisas precisam ser verdade para a tese funcionar?]
1. [Premissa 1]
2. [Premissa 2]
3. [Premissa 3]

### O que invalidaria a tese
[Quais evidências ou eventos fariam a tese cair por terra?]
1. [Kill signal 1]
2. [Kill signal 2]

### Revisão da tese
**Última validação:** [data]
**Próxima revisão:** [data — no mínimo trimestral]
**Responsável:** [CEO]
```

### Exemplo

```markdown
## Tese Estratégica

### Declaração
"Acreditamos que a explosão de dados em PMEs (crescimento de 40% ao ano) combinada com a
democratização de modelos de AI criará uma janela de 3-5 anos onde PMEs adotarão ferramentas
de decisão AI-powered em massa. Quem capturar esta onda primeiro com UX simples e preço
acessível dominará o segmento, pois os custos de switching serão altos após integração
de dados."

### Evidências
| # | Evidência                                    | Tipo  | Força |
|---|----------------------------------------------|-------|-------|
| 1 | 73% das PMEs dizem querer usar dados para decisão (Pesquisa Distrito 2025) | Qual | Forte |
| 2 | Custo de compute de AI caiu 90% em 3 anos   | Quant | Forte |
| 3 | Nenhum player dominante em AI para PME LATAM | Mercado | Forte |
| 4 | Nosso piloto com 50 PMEs: 85% continuaram após trial | Quant | Forte |

### Premissas
1. PMEs têm dados suficientes para AI gerar valor (mínimo 6 meses de histórico)
2. Preço <R$500/mês é viável com unit economics saudáveis
3. Self-service funciona (PMEs não precisam de consultoria para implementar)

### O que invalidaria
1. PMEs preferem consultoria humana a ferramentas self-service (adoption <10%)
2. Big techs lançam solução gratuita que atende o mesmo job-to-be-done
3. Regulação de AI para PMEs torna compliance inviável
```

---

## 3. Bet Description Block

### Propósito
Documentar cada "aposta" estratégica — uma iniciativa significativa com resultado incerto mas potencialmente transformador.

### Template

```markdown
## Bet: [Nome da Aposta]

### Classificação
- **Tipo:** [Core (70% dos recursos) / Adjacent (20%) / Transformational (10%)]
- **Horizonte:** [H1: 0-12 meses / H2: 12-24 meses / H3: 24-36 meses]
- **Investimento:** [R$ ou % do budget]
- **Reversibilidade:** [Type 1 (irreversível) / Type 2 (reversível)]

### Hipótese
"Se fizermos [ação], então [resultado esperado], porque [razão/mecanismo]."

### Métricas de sucesso
| Métrica          | Baseline | Target (6m) | Target (12m) | Como medir      |
|------------------|----------|-------------|--------------|-----------------|
| [métrica 1]      | [atual]  | [target]    | [target]     | [método]        |
| [métrica 2]      | [atual]  | [target]    | [target]     | [método]        |

### Kill criteria
[Em quais condições matamos esta aposta?]
- Se [condição 1] até [data]: KILL
- Se [condição 2]: PIVOT para [alternativa]

### Riscos específicos da aposta
| Risco                  | P | I | Mitigação              |
|------------------------|---|---|------------------------|
| [risco 1]              |   |   | [mitigação]            |

### DRI e recursos
- **DRI:** [agente]
- **Time:** [quem está alocado]
- **Budget:** [R$]
- **Dependências:** [de quem/o que depende]

### Status tracking
**Checkpoint 1 ([data]):** [Go/Pivot/Kill — critério]
**Checkpoint 2 ([data]):** [Go/Pivot/Kill — critério]
```

---

## 4. Arena Definition Block

### Propósito
Definir claramente o "campo de batalha" onde a empresa compete — qual mercado, segmento, geografia.

### Template

```markdown
## Arena: [Nome do Mercado/Segmento]

### Definição
- **Mercado:** [descrição do mercado]
- **TAM:** [Total Addressable Market — valor]
- **SAM:** [Serviceable Addressable Market — valor]
- **SOM:** [Serviceable Obtainable Market — valor e % share]

### Segmento-alvo
- **Perfil do cliente ideal (ICP):**
  - Tamanho: [faixa de receita/funcionários]
  - Vertical: [indústria(s)]
  - Geografia: [regiões]
  - Maturidade: [estágio de desenvolvimento]
  - Pain point primário: [problema que resolvemos]
  - Willingness to pay: [faixa de preço]

### Onde NÃO competimos (explicitamente)
- **Segmentos fora do escopo:** [quais e por quê]
- **Geografias fora do escopo:** [quais e por quê]
- **Use cases fora do escopo:** [quais e por quê]

### Dinâmica do mercado
- **Crescimento:** [X% ao ano]
- **Concentração:** [fragmentado / concentrado / monopólio]
- **Maturidade:** [emergente / crescimento / maduro / declínio]
- **Regulação:** [leve / moderada / pesada]
- **Tendência principal:** [o que está mudando no mercado]

### Competidores na arena
| Competidor       | Share (est.) | Positioning              | Força principal        | Fraqueza principal     |
|------------------|-------------|--------------------------|------------------------|------------------------|
| [competidor 1]   | [%]         | [como se posiciona]      | [força]                | [fraqueza]             |
| [competidor 2]   | [%]         | [posicionamento]         | [força]                | [fraqueza]             |
| [nós]            | [%]         | [nosso posicionamento]   | [força]                | [fraqueza]             |
```

---

## 5. Competitive Advantage Block

### Propósito
Articular qual é a vantagem competitiva sustentável da organização — o que nos permite vencer e continuar vencendo.

### Template

```markdown
## Vantagem Competitiva

### Tipo de vantagem
- [ ] **Custo:** Operamos com custos estruturalmente menores
- [ ] **Diferenciação:** Oferecemos algo que ninguém mais oferece
- [ ] **Network effects:** Quanto mais gente usa, melhor fica para todos
- [ ] **Switching costs:** É caro/difícil para o cliente trocar
- [ ] **Escala:** Nossa escala gera eficiências que menores não alcançam
- [ ] **Dados/AI:** Nossos dados/modelos melhoram com uso (data flywheel)
- [ ] **Brand:** Nossa marca tem valor intrínseco que demora para construir
- [ ] **Regulatório:** Temos licenças/aprovações difíceis de replicar

### Descrição da vantagem
[Parágrafo explicando COMO a vantagem funciona na prática]

### Moat (fosso defensivo)
[O que impede competidores de replicar nossa vantagem?]
- **Tempo:** Levaria [X] meses/anos para replicar porque [razão]
- **Investimento:** Custaria [R$X] para replicar
- **Conhecimento:** Requer [expertise específica] que é escassa

### Sustainability test
| Pergunta                                               | Resposta | Preocupação? |
|--------------------------------------------------------|----------|-------------|
| Um competidor pode replicar em <12 meses?              | [S/N]    |             |
| Um substituto pode tornar nossa vantagem irrelevante?  | [S/N]    |             |
| A vantagem depende de uma pessoa/contrato específico?  | [S/N]    |             |
| A vantagem se fortalece com o tempo e uso?             | [S/N]    |             |

### Investimento para manter/fortalecer a vantagem
[O que precisamos continuar investindo para que a vantagem não eroda?]
- [Investimento 1]
- [Investimento 2]
```

---

## 6. Capability Requirement Block

### Propósito
Identificar quais capacidades a organização precisa desenvolver ou adquirir para executar a estratégia.

### Template

```markdown
## Capacidades Necessárias

### Mapa de capacidades

| Capacidade                | Importância (1-5) | Maturidade atual (1-5) | Gap | Como fechar               | Timeline | Owner |
|--------------------------|-------------------|----------------------|-----|---------------------------|----------|-------|
| [Capacidade 1]           | [1-5]             | [1-5]                | [X] | [Build/Buy/Partner]       | [meses]  | [DRI] |
| [Capacidade 2]           | [1-5]             | [1-5]                | [X] | [Build/Buy/Partner]       | [meses]  | [DRI] |

### Priorização
**Gaps críticos (importância ≥4, gap ≥2):**
1. [Capacidade]: [plano de ação resumido]

**Gaps secundários (para próximo ciclo):**
1. [Capacidade]: [plano preliminar]

### Build vs. Buy vs. Partner decision

| Critério            | Build (interno) | Buy (aquisição) | Partner (parceria) |
|--------------------|----------------|-----------------|-------------------|
| Tempo até resultado | Longo (6-18m)  | Médio (3-6m)    | Curto (1-3m)      |
| Custo upfront      | Baixo-Médio    | Alto            | Baixo             |
| Controle            | Total          | Alto            | Parcial           |
| Melhor quando       | Core capability, longo prazo | Competência escassa, urgente | Non-core, validação |
```

---

## 7. Risk Factor Block (estratégico)

### Propósito
Identificar riscos estratégicos que ameaçam a execução ou validade da estratégia.

### Template

```markdown
## Riscos Estratégicos

### Riscos externos (não controlamos)

| # | Risco                          | Probabilidade | Impacto | Indicador antecedente       | Contingência              |
|---|-------------------------------|---------------|---------|----------------------------|---------------------------|
| 1 | [Mudança regulatória]         | [B/M/A]       | [B/M/A] | [o que monitorar]          | [plano B se acontecer]    |
| 2 | [Novo entrante / big tech]    | [B/M/A]       | [B/M/A] | [o que monitorar]          | [plano B]                 |
| 3 | [Mudança de mercado]          | [B/M/A]       | [B/M/A] | [o que monitorar]          | [plano B]                 |

### Riscos internos (controlamos ou influenciamos)

| # | Risco                          | Probabilidade | Impacto | Mitigação ativa            | Owner |
|---|-------------------------------|---------------|---------|----------------------------|-------|
| 1 | [Perda de talento chave]      | [B/M/A]       | [B/M/A] | [ação]                     | [DRI] |
| 2 | [Falha de execução]           | [B/M/A]       | [B/M/A] | [ação]                     | [DRI] |
| 3 | [Tese invalidada]             | [B/M/A]       | [B/M/A] | [ação]                     | [DRI] |

### Cenários de risco combinado
**Worst case plausível:** [Descreva o cenário onde múltiplos riscos se materializam]
**Impacto:** [O que acontece com o negócio neste cenário]
**Resiliência:** [Sobrevivemos? Por quanto tempo? O que muda?]
```

---

## 8. Montagem de documento estratégico completo

### Strategy on a Page

```markdown
# Estratégia — [Período]

## Visão (5 anos)
[Vision Statement Block — 2-3 frases]

## Tese estratégica
[Strategic Thesis Block — 1 parágrafo]

## Arena
[Arena Definition Block — resumo de onde competimos]

## Vantagem competitiva
[Competitive Advantage Block — 1-2 frases sobre nosso moat]

## Apostas estratégicas (máximo 3-5)
1. [Bet 1]: [1 frase] — R$[X] — H[1/2/3]
2. [Bet 2]: [1 frase] — R$[X] — H[1/2/3]
3. [Bet 3]: [1 frase] — R$[X] — H[1/2/3]

## Capacidades a desenvolver
1. [Capability 1] — Gap: [X] — Via: [Build/Buy/Partner]
2. [Capability 2]

## Riscos estratégicos (top 3)
1. [Risco 1] — Mitigação: [ação]
2. [Risco 2]
3. [Risco 3]

## Métricas estratégicas
| Métrica | Hoje | Target 12m | Target 24m |
|---------|------|-----------|------------|
| [m1]    |      |           |            |

## Próxima revisão: [data]
```

### Frequência de revisão

| Bloco                  | Frequência de revisão | Responsável |
|-----------------------|-----------------------|-------------|
| Vision Statement      | Anual                 | CEO         |
| Strategic Thesis      | Trimestral            | CEO         |
| Bet Description       | Mensal (status)       | DRI de cada bet |
| Arena Definition      | Semestral             | CEO + CMO   |
| Competitive Advantage | Trimestral            | CEO + CTO   |
| Capability Requirement| Trimestral            | COO         |
| Risk Factors          | Mensal                | CEO + COO   |
