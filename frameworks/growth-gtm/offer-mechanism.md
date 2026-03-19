# Offer Mechanism — Arquitetura de Oferta

> **Domínio:** Growth & GTM
> **Autor de referência:** Alex Hormozi — "$100M Offers", adaptação B2B pelo C-Level Squad
> **Uso primário:** Construir ofertas irresistíveis que maximizam valor percebido e conversão.
> **Agente responsável:** cmo-architect

---

## Origem e Contexto

O conceito de Offer Mechanism foi popularizado por Alex Hormozi em "$100M Offers" (2021), focado inicialmente em negócios locais e B2C. O princípio central: **o problema não é falta de leads — é uma oferta fraca. Uma Grand Slam Offer é tão boa que a pessoa se sente estúpida dizendo não.**

A fórmula de valor de Hormozi:

```
                    Dream Outcome × Perceived Likelihood of Achievement
Valor Percebido = ──────────────────────────────────────────────────────
                         Time Delay × Effort and Sacrifice
```

Para aumentar valor percebido: maximizar o numerador (resultado + confiança) e minimizar o denominador (tempo + esforço).

O C-Level Squad adapta este framework para contextos B2B SaaS, enterprise e scale-ups, onde a dinâmica de compra envolve múltiplos decisores, ciclos longos, e value metrics complexas.

A oferta não é só preço — é o pacote completo: o que está incluído, como é entregue, quais garantias existem, qual o risco percebido, e por que agora.

---

## Quando Usar

- Ao lançar um novo produto ou tier de pricing.
- Quando a conversão de trials ou demos é baixa — a oferta não está comunicando valor suficiente.
- Ao reposicionar produto existente — mesma solução, oferta redesenhada.
- Para criar diferenciação quando o produto é similar à concorrência.
- Em campanhas de aquisição — a oferta é o ativo mais importante do funil.
- No redesign de pricing e packaging (`frameworks/growth-gtm/pricing-value-metric.md`).

---

## Quando NÃO Usar

- Para justificar produto ruim — oferta brilhante com produto fraco = churn alto.
- Em mercados enterprise com RFP rígido — o mecanismo de oferta é limitado pelo processo do comprador.
- Como tática de curto prazo sem estratégia — "oferta irresistível" sem positioning claro vira promoção.
- Para manipular — ofertas devem entregar valor real. Over-promise gera reputação negativa.

---

## Estrutura / Modelo

### Componentes da Oferta

```
┌─────────────────────────────────────────────────────────────────────┐
│                      ARQUITETURA DE OFERTA                           │
├─────────────────────────────────────────────────────────────────────┤
│                                                                      │
│  1. CORE OFFER (Produto/Serviço principal)                          │
│     └── O que o cliente recebe como entrega central.                │
│                                                                      │
│  2. VALUE STACK (Elementos adicionais de valor)                     │
│     ├── Bonus 1: Onboarding acelerado (reduz Time Delay)           │
│     ├── Bonus 2: Templates prontos (reduz Effort)                  │
│     ├── Bonus 3: Acesso a comunidade (aumenta Likelihood)          │
│     └── Bonus 4: Sessão de estratégia 1:1 (aumenta Dream Outcome) │
│                                                                      │
│  3. GUARANTEE (Redução de risco percebido)                          │
│     └── O que acontece se não funcionar?                            │
│                                                                      │
│  4. URGENCY / SCARCITY (Razão para agir agora)                     │
│     └── Por que decidir hoje e não daqui 3 meses?                  │
│                                                                      │
│  5. NAMING (Como a oferta é apresentada)                            │
│     └── Nome que comunica o resultado, não a feature.              │
│                                                                      │
│  6. PRICING (Preço e modelo de cobrança)                            │
│     └── Alinhado ao valor percebido e value metric.                │
│                                                                      │
└─────────────────────────────────────────────────────────────────────┘
```

---

## Processo de Aplicação (step-by-step)

### Step 1: Identificar o Dream Outcome do Cliente
Usando JTBD (`frameworks/growth-gtm/jtbd.md`):
- Qual é o resultado final que o cliente quer?
- Qual é o "antes" e o "depois" na vida/negócio do cliente?
- Ser específico: "Reduzir tempo de fechamento fiscal de 15 dias para 2 dias" > "Automatizar finanças."

### Step 2: Construir o Value Stack
Listar tudo que pode aumentar o valor percebido da oferta. Para cada item:
- **Nome:** Dar nome proprietário (ex.: "Programa de Aceleração 90 Dias", não "onboarding").
- **Valor atribuído:** Quanto o cliente pagaria por isso separadamente?
- **Custo para entregar:** Qual o custo real? (Itens de alto valor percebido e baixo custo são os melhores.)
- **Qual alavanca aciona?** Dream Outcome↑, Likelihood↑, Time Delay↓, ou Effort↓?

**Exemplos de items no value stack (B2B SaaS):**
- Implementação white-glove em 48h (Time Delay↓)
- Playbooks e templates prontos para o segmento (Effort↓)
- Migração gratuita da ferramenta anterior (Effort↓, Anxiety↓)
- Sessão de estratégia com especialista (Dream Outcome↑)
- Dashboard de ROI automático (Likelihood↑)
- Acesso a comunidade de pares (Social Job↑)
- SLA de suporte prioritário (Likelihood↑)

### Step 3: Desenhar a Garantia
Tipos de garantia para B2B:
- **Unconditional:** "Se não gostar em 30 dias, devolvemos 100%." (Mais forte, maior risco.)
- **Conditional:** "Se implementar os 3 passos em 60 dias e não ver resultado X, devolvemos." (Reduz risco do vendedor, mantém compromisso do comprador.)
- **Performance-based:** "Pagamento atrelado a resultado." (Ex.: comissão sobre receita gerada.)
- **Anti-guarantee:** "Se você não está disposto a investir 2h/semana, não vamos aceitar você como cliente." (Exclusividade aumenta valor percebido.)

### Step 4: Criar Urgência Real (Não Falsa)
Urgência artificial (countdown timers falsos) destrói confiança. Urgência real:
- **Cohort-based:** "Turma de janeiro fecha dia 15." (Real se há limite de capacidade.)
- **Pricing evolution:** "Preço de early-adopter disponível para os primeiros 50 clientes." (Real se o preço vai subir.)
- **Custo de inação:** "Cada mês sem solução custa X em ineficiência." (Calculadora de ROI.)
- **Evento externo:** "Regulação LGPD entra em vigor em 6 meses." (Real e verificável.)

### Step 5: Nomear a Oferta
O nome comunica resultado, não feature:
- Ruim: "Plano Enterprise"
- Bom: "Programa de Aceleração de Revenue — 90 Dias"
- Ruim: "Pacote Premium"
- Bom: "Revenue Operations Engine — Para Times que Querem Dobrar em 12 Meses"

### Step 6: Precificar Baseado em Valor
Usar `frameworks/growth-gtm/pricing-value-metric.md` para definir:
- Value metric (por que o cliente paga).
- Tier structure (good/better/best).
- Preço como % do valor entregue (regra: cobrar 10-20% do valor gerado).

### Step 7: Testar e Iterar
- A/B test de diferentes value stacks.
- Win/loss analysis: o que os clientes citam como decisivo?
- Iterar trimestralmente baseado em dados.

---

## Exemplos Práticos

### Exemplo: SaaS de Analytics B2B

**Core Offer:** Plataforma de analytics com dashboards customizáveis.

**Value Stack:**
| Item | Valor Percebido | Custo Real | Alavanca |
|------|-----------------|------------|----------|
| Setup em 48h (vs 4 semanas do concorrente) | R$ 15K | R$ 2K | Time Delay↓ |
| 10 dashboards pré-configurados para SaaS | R$ 8K | R$ 500 | Effort↓ |
| Sessão de estratégia de dados (2h) | R$ 5K | R$ 1K | Dream Outcome↑ |
| Migração gratuita do Google Analytics | R$ 3K | R$ 800 | Effort↓ |
| Comunidade de 200+ líderes de growth | R$ 2K/ano | R$ 200 | Likelihood↑ |

**Garantia:** "Se em 60 dias você não tiver pelo menos 3 insights acionáveis que impactam receita, devolvemos o primeiro mês."

**Pricing:** R$ 3.500/mês (valor total percebido: R$ 33K. Ratio: ~10x.)

---

## Armadilhas Comuns

1. **Over-promise, under-deliver:** Oferta maravilhosa que não se sustenta na entrega. Churn explode.
2. **Value stack como lixo:** Adicionar itens sem valor real (ebooks genéricos, templates ruins) desvaloriza a oferta.
3. **Garantia sem enforcement:** Oferecer garantia e dificultar o reembolso destrói confiança permanentemente.
4. **Urgência falsa:** Countdown timers que resetam todo dia. O mercado percebe e descredibiliza.
5. **Preço baseado em custo, não valor:** Cobrar markup sobre custo ignora o valor do outcome para o cliente.
6. **Oferta única para todos:** Segmentos diferentes têm jobs diferentes. A oferta deve ser adaptada por segmento (STP).
7. **Ignorar o processo de compra B2B:** Em enterprise, o comprador precisa justificar internamente. A oferta deve incluir business case e ROI calculator.
8. **Não atualizar:** A oferta que funcionou em 2024 pode ser commodity em 2025. Iterar constantemente.

---

## Integração com Outros Frameworks

| Framework | Integração |
|-----------|-----------|
| `frameworks/growth-gtm/jtbd.md` | O Dream Outcome vem do job funcional/emocional/social do cliente. |
| `frameworks/growth-gtm/stp.md` | O segmento alvo define qual oferta ressoará. Ofertas diferentes por segmento. |
| `frameworks/growth-gtm/pricing-value-metric.md` | Pricing é componente da oferta. Value metric alinha preço ao valor entregue. |
| `frameworks/growth-gtm/brand-to-demand.md` | A oferta é o asset central de demand generation. |
| `frameworks/growth-gtm/growth-loops.md` | A oferta pode ser desenhada para alimentar growth loops (referral, viral). |
| `frameworks/vision-strategy/strategy-choice-cascade.md` | "How to Win" pode ser via oferta superior, não só via produto. |
| `checklists/cmo/campaign-quality.md` | Checklist para validar que campanhas comunicam a oferta corretamente. |

---

## Referências

- Hormozi, A. (2021). *$100M Offers: How To Make Offers So Good People Feel Stupid Saying No*. Acquisition.com.
- Hormozi, A. (2023). *$100M Leads*. Acquisition.com.
- Cialdini, R. (2021). *Influence: The Psychology of Persuasion*. Revised Ed. Harper Business.
- Thaler, R. & Sunstein, C. (2009). *Nudge*. Penguin. (Arquitetura de escolha.)
