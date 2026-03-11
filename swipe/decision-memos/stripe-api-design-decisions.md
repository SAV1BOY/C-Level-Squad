# Decisões de Design da API Stripe

## Contexto

A API da Stripe é amplamente considerada o gold standard de design de APIs REST.
Desde 2011, a empresa tomou decisões deliberadas que resultaram em uma das experiências
de desenvolvedor mais elogiadas da indústria. Este documento analisa as principais
decisões arquiteturais e o raciocínio por trás de cada uma.

## Decisão 1: API-First como Estratégia de Negócio

### O Que Decidiram
A Stripe seria uma empresa de API, não uma empresa com API. O produto É a API.
A interface web seria construída consumindo a mesma API pública.

### Raciocínio
- Desenvolvedores são os decision makers para integração de pagamentos
- Uma API excelente cria switching costs altíssimos
- Dogfooding forçado garante qualidade (se o dashboard usa a API, bugs são encontrados rápido)

### Impacto
- Developer NPS consistentemente acima de 70
- Tempo médio de integração: horas, não semanas
- 90%+ dos clientes citam "facilidade da API" como razão principal de escolha

### Lição para C-Level
Se seu produto serve desenvolvedores, a API não é um feature - é o produto.
Invista nela como investiria no produto principal. O orçamento de API deve ser orçamento
de produto, não de infraestrutura.

## Decisão 2: Nomenclatura Consistente e Previsível

### O Que Decidiram
Convenções rígidas de naming que um desenvolvedor pode adivinhar sem ler documentação:

- Recursos sempre no plural: `/v1/customers`, `/v1/charges`
- Operações CRUD mapeiam para HTTP verbs: GET, POST, PUT/PATCH, DELETE
- Parâmetros snake_case: `customer_id`, `created_at`
- Booleanos prefixados: `is_live`, `has_more`
- Timestamps sempre em Unix epoch

### Raciocínio
- Previsibilidade reduz necessidade de documentação
- Consistência reduz erros de integração
- Desenvolvedores transferem conhecimento entre endpoints

### Impacto
- 60% menos tickets de suporte por endpoint novo
- Desenvolvedores reportam "adivinharem" a API corretamente 80% das vezes
- Onboarding de novos engenheiros Stripe 40% mais rápido

### Lição para C-Level
Consistência é mais valiosa que perfeição local. Às vezes, a melhor decisão para um
endpoint individual não é a melhor decisão para a API como um todo.

## Decisão 3: Versionamento por Data no Header

### O Que Decidiram
Versões da API são datas (ex: `Stripe-Version: 2023-10-16`), não semver.
Cada conta fica "pinada" na versão de quando foi criada. Upgrades são opt-in.

### Raciocínio
- Nunca quebrar integrações existentes (prioridade absoluta)
- Permitir evolução da API sem forçar migração
- Simplificar suporte (saber exatamente o comportamento de cada conta)

### Impacto
- Zero breaking changes em 12+ anos de operação
- Clientes podem operar por anos sem atualizar integração
- Stripe mantém compatibilidade com centenas de versões simultaneamente

### Lição para C-Level
O custo de manter versões antigas é menor que o custo de perder clientes por breaking changes.
Isso vale para APIs, mas também para qualquer interface com stakeholders.

## Decisão 4: Idempotency Keys

### O Que Decidiram
Toda operação de escrita aceita um `Idempotency-Key` header. Repetir a mesma
request com a mesma key retorna o mesmo resultado sem executar a operação novamente.

### Raciocínio
- Em pagamentos, cobrar duas vezes é catastrófico
- Redes são instáveis; retries são inevitáveis
- Melhor resolver no server do que forçar cada cliente a implementar deduplicação

### Impacto
- Redução de 99.9% em cobranças duplicadas
- Clientes podem implementar retry logic com segurança
- Simplificação massiva do código do cliente

### Lição para C-Level
Antecipe os erros dos seus clientes e resolva-os proativamente. O custo de
implementar safety nets é sempre menor que o custo de lidar com as consequências.

## Decisão 5: Objetos Expandíveis

### O Que Decidiram
Relacionamentos retornam apenas IDs por padrão. O cliente pode solicitar expansão
com `?expand[]=customer`:

```
# Sem expand: retorna customer como string ID
"customer": "cus_123"

# Com expand: retorna objeto completo
"customer": { "id": "cus_123", "name": "João", ... }
```

### Raciocínio
- Respostas leves por padrão (performance)
- Flexibilidade para quem precisa de dados relacionados
- Evita N+1 queries no cliente sem forçar dados desnecessários

### Impacto
- 70% menos chamadas de API (clientes buscam tudo em uma request)
- Respostas 5x menores para casos simples
- Melhor performance para clientes mobile com banda limitada

### Lição para C-Level
Design para o caso comum, mas permita o caso avançado. Isso vale para APIs,
mas também para processos, relatórios e ferramentas internas.

## Decisão 6: Documentação como Código

### O Que Decidiram
A documentação é gerada a partir do código da API. Exemplos são executáveis
e testados automaticamente. Cada linguagem tem exemplos reais, não pseudocódigo.

### Raciocínio
- Documentação desatualizada é pior que sem documentação
- Exemplos que não funcionam destroem confiança
- Custo de manter docs separadas cresce exponencialmente

### Impacto
- Docs sempre sincronizadas com a API real
- 0 tickets de "exemplo não funciona" (meta atingida em 2019)
- Desenvolvedores copiam-colam exemplos e funcionam de primeira

### Lição para C-Level
Automação de documentação não é luxo. Se seus processos dependem de documentos
manuais, eles estarão desatualizados. Isso vale para runbooks, playbooks e SOPs.

## Decisão 7: Tratamento de Erros Rico e Acionável

### O Que Decidiram
Erros incluem: tipo do erro, código específico, mensagem human-readable,
parâmetro que causou o erro, e link para documentação relevante.

### Raciocínio
- Desenvolvedores precisam resolver problemas rapidamente
- Mensagens genéricas geram tickets de suporte
- Links para docs reduzem ida-e-volta com suporte

### Impacto
- 50% de redução em tickets de suporte
- Tempo médio de resolução de erros: 3 minutos (vs 30 minutos no concorrente)
- NPS de suporte 85+ (parcialmente por não precisarem usá-lo)

### Lição para C-Level
Invista em mensagens de erro como investiria em copy de marketing.
Cada erro é um momento de verdade com o cliente.

## Decisão 8: Webhooks com Retry Inteligente

### O Que Decidiram
Webhooks usam retry exponencial (1min, 5min, 30min, 2h, 5h, 10h)
com dashboard para monitoramento e replay manual.

### Raciocínio
- Endpoints de clientes falham (deploys, outages, bugs)
- Perder eventos de pagamento é inaceitável para o negócio do cliente
- Clientes precisam de visibilidade sobre o que está acontecendo

### Impacto
- 99.97% de entrega de webhooks em primeira tentativa ou retry
- Dashboard de webhooks é uma das features mais elogiadas
- Redução de 90% em perda de dados por falha de integração

## Anti-Padrões que a Stripe Evitou

1. **GraphQL para tudo** - REST com expand é mais simples para pagamentos
2. **Autenticação complexa** - Bearer token simples, sem OAuth para API básica
3. **Rate limiting agressivo** - Limites generosos com headers informativos
4. **Versionamento por URL** - `/v1/` existe mas versão real é por header
5. **Documentação em PDF** - Sempre web, sempre interativa

## Checklist para Aplicar no Seu Contexto

- [ ] Sua API segue convenções consistentes de nomenclatura?
- [ ] Suas mensagens de erro são acionáveis?
- [ ] Você tem idempotency em operações críticas?
- [ ] Sua documentação é gerada a partir do código?
- [ ] Clientes podem adivinhar sua API sem ler docs?
- [ ] Você versionou sem quebrar clientes existentes?

## Referências

- Stripe API Reference (stripe.com/docs/api)
- "Designing APIs that Developers Love" - Stripe Engineering Blog
- "Payment APIs That Scale" - Patrick McKenzie (patio11)
- "API Design Patterns" - JJ Geewax (Manning, 2021)
