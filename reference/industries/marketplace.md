# Marketplace

## Visão Geral

Marketplaces conectam dois ou mais lados de um mercado — tipicamente compradores
e vendedores — facilitando transações e capturando valor no meio. É um dos modelos
mais poderosos quando funciona (network effects criam moats defensáveis), mas
também um dos mais difíceis de construir (o problema chicken-and-egg).

---

## 1. Métricas Fundamentais

### Volume Metrics

**GMV (Gross Merchandise Value)**
Valor total das transações que passam pela plataforma.
- É a métrica de escala do marketplace
- GMV ≠ Revenue: revenue = GMV × take rate
- GMV pode ser enganoso sem considerar unit economics

**Take Rate**
Percentual do GMV que o marketplace retém como receita.
- Fórmula: Revenue / GMV
- Benchmark varia por vertical:
  - E-commerce marketplace: 10-20%
  - Serviços: 15-30%
  - Travel: 10-15%
  - Fintech/payments: 1-3%
  - Real estate: 3-6%
- Take rate é limitado pelo valor que o marketplace adiciona

**Net Revenue**
Receita líquida do marketplace: GMV × take rate - custos diretos de transação.
- Custos diretos: payment processing, fraud, customer support por transação
- É a receita real disponível para cobrir custos fixos e gerar lucro

### Liquidity Metrics

**Liquidity**
Probabilidade de um participant completar uma transação com sucesso.
- Para compradores: encontrar o que busca em tempo razoável
- Para vendedores: conseguir vendas suficientes para justificar presença
- Medir: search-to-fill rate, time-to-transaction, match rate

**Supply-Demand Balance**
Equilíbrio entre oferta e demanda em cada mercado/categoria.
- Excesso de oferta: sellers competem, preços caem, muitos não vendem
- Excesso de demanda: compradores não encontram, abandonam plataforma
- Monitorar por região, categoria e período

**Utilization Rate**
Para marketplaces de serviços: % do tempo/capacidade do supply que é utilizado.
- Uber: % das horas online que o motorista está em viagem
- Airbnb: % dos dias disponíveis que são reservados
- Alta utilization = supply satisfeito = mais supply = mais demanda

### Engagement Metrics

**Repeat Rate**
Percentual de transações feitas por usuários recorrentes.
- Benchmark saudável: >50% de GMV vem de repeat users
- Indica product-market fit e hábito formado
- Separar repeat de supply side e demand side

**Cohort Retention**
Retenção de coortes ao longo do tempo.
- Ideal: curvas que se estabilizam (não caem a zero)
- Analisar separadamente para supply e demand
- Comparar coortes: as mais recentes retêm melhor? (sinal de melhoria de produto)

---

## 2. O Problema Chicken-and-Egg

### O Dilema Fundamental

Marketplace sem supply não atrai demand. Marketplace sem demand não atrai supply.
Resolver este ciclo é o desafio #1 de todo marketplace.

### Estratégias de Resolução

**Subsidiar um Lado**
Oferecer incentivos para o lado mais difícil de atrair.
- Uber: subsidiou motoristas no início (garantias de ganho mínimo)
- Rappi: subsidiou entregadores e descontos para usuários
- Risco: dependência de subsídio que nunca se paga

**Single-Player Mode**
Criar valor para um lado independente do outro.
- OpenTable: sistema de reservas para restaurantes (útil mesmo sem demanda online)
- Yelp: reviews úteis para consumidores independente de booking
- O lado que usa em single-player mode se torna a base para atrair o outro

**Constrain the Market**
Começar em mercado muito restrito onde é possível atingir liquidity rapidamente.
- Airbnb: começou em eventos de conferências em SF
- Uber: começou em SF com black cars
- Mercado Livre: começou com leilões de colecionáveis
- Expandir gradualmente a partir do nicho com liquidez

**Fake Supply / Curated Supply**
No início, o próprio marketplace opera parte do supply.
- Curar manualmente os melhores providers
- Operar como "managed marketplace" no início
- Migrar para open marketplace quando liquidity se estabelecer

**Incentivos Financeiros Temporários**
- Desconto para primeiros compradores
- Taxa zero ou bônus para primeiros sellers
- Referral programs agressivos nos dois lados
- Com prazo definido e meta de liquidity

---

## 3. Network Effects

### Tipos de Network Effects em Marketplaces

**Same-Side (Direct)**
Mais users do mesmo lado = mais valor para esse lado.
- Raro em marketplaces puros (mais compradores não ajudam outros compradores)
- Existe em social marketplaces: reviews, community

**Cross-Side (Indirect)**
Mais users de um lado = mais valor para o outro.
- Mais sellers → mais variedade → mais compradores
- Mais compradores → mais demanda → mais sellers
- É o core network effect de marketplaces

**Local vs Global**
- Global: benefício para qualquer user independente de localização (Etsy)
- Local: benefício apenas para users na mesma região (Uber, iFood)
- Local network effects são mais difíceis de construir (precisa vencer market by market)

### Defensibilidade dos Network Effects

Network effects nem sempre são moats permanentes:
- **Multi-homing**: users podem usar múltiplos marketplaces simultaneamente
- **Switching costs baixos**: especialmente quando não há lock-in de dados
- **Winner-take-most vs winner-take-all**: muitos mercados suportam 2-3 players
- **Regulação**: pode limitar concentração de mercado

### Fortalecendo Network Effects

- Aumentar switching costs: ratings/reviews, histórico, loyalty programs
- Aumentar custo de multi-homing: exclusividade, features únicas, integração profunda
- Criar data network effects: mais transações = melhor matching = mais valor
- Builds ecosystem: APIs, ferramentas, serviços adjacentes que aumentam lock-in

---

## 4. Unit Economics do Marketplace

### Framework de Análise

Para cada transação, calcular:
```
GMV (valor bruto da transação)
- Repasse ao seller
= Revenue (take rate × GMV)
- Payment processing (~2-3%)
- Fraud/chargebacks (~0.5-1%)
- Customer support (variável)
- Logistics (se aplicável)
= Contribution Margin por transação
```

### Economias de Escala

Marketplaces têm custos fixos altos e custos variáveis baixos:
- Tecnologia: custo relativamente fixo (plataforma serve 1K ou 1M users)
- Trust & Safety: escala com transações, mas sublinearmente
- Marketing: CAC pode cair com network effects e brand
- Operations: depende do nível de "managed" vs "open"

### Caminho para Rentabilidade

1. Atingir liquidity em mercados-chave
2. Reduzir subsídios gradualmente
3. Aumentar take rate conforme valor entregue justifica
4. Adicionar revenue streams (ads, fintech, SaaS tools para sellers)
5. Expandir para categorias adjacentes com infraestrutura existente

---

## 5. Modelos de Marketplace

### Classificação por Nível de Curadoria

**Open Marketplace**: qualquer pessoa pode vender (Mercado Livre, Etsy)
- Escala rápida, mas qualidade inconsistente
- Trust & safety é desafio constante

**Managed Marketplace**: plataforma controla qualidade e processo (Uber, Airbnb)
- Experiência mais consistente
- Mais caro para operar

**Curated Marketplace**: plataforma seleciona sellers (Farfetch, 1stDibs)
- Alta qualidade, premium positioning
- Escala mais lenta

### Classificação por Transação

**Transactional**: marketplace facilita a transação financeira
- Revenue via take rate
- Mais controle e dados

**Lead-Gen**: marketplace gera leads, transação acontece off-platform
- Revenue via listing fees ou referral fees
- Menor controle, risco de disintermediation

**SaaS-Enabled**: marketplace oferece software tools além de transações
- Revenue via subscription + take rate
- Maior lock-in e valor agregado

---

## 6. Desafios Comuns

### Disintermediation

Risco de buyers e sellers transacionarem fora da plataforma após o primeiro contato.
- **Prevenção**: tornar a plataforma indispensável (pagamento, seguro, dispute resolution)
- **Monitoramento**: detectar padrões de disintermediation
- **Valor contínuo**: ferramentas que justificam a taxa em cada transação

### Qualidade e Trust

- Ratings e reviews: essenciais mas manipuláveis
- Verificação de identidade e qualidade
- Dispute resolution justa e eficiente
- Garantias e proteção ao consumidor

### Regulação

- Marketplaces de trabalho: questões de vínculo empregatício
- Marketplaces financeiros: regulação BACEN, CVM
- Marketplaces de saúde: regulação sanitária
- Responsabilidade da plataforma por atos de sellers

### Scaling Challenges

- Cada novo mercado/cidade requer cold start de liquidity
- Operations locais vs padronizadas
- Cultural differences entre mercados
- Capital intensivo para expansão geográfica

---

## 7. Contexto Brasil

### Oportunidades

- Mercado fragmentado em muitas verticais (oportunidade de agregação)
- Penetração digital crescente em todas as faixas de renda
- PIX facilitou transações peer-to-peer e marketplace
- Economia informal que pode ser formalizada via marketplace

### Desafios Específicos

- **Logística**: custo de frete em país continental
- **Pagamento**: split payment complexo (divisão entre marketplace e seller)
- **Fiscal**: nota fiscal, retenções, responsabilidade tributária
- **Fraude**: taxa mais alta que mercados maduros
- **Informalidade**: muitos sellers potenciais são informais
- **Regulação trabalhista**: marketplace de serviços enfrenta riscos de vínculo

---

## Referências

- "The Platform Revolution" — Parker, Van Alstyne, Choudary
- "Platform Scale" — Sangeet Paul Choudary
- a16z Marketplace 100
- Lenny Rachitsky — Marketplace content
- Bill Gurley — "All Markets Are Not Created Equal"
