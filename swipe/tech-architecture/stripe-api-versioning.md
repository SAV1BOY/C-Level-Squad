# Stripe API Versioning Strategy - Análise Completa

## Contexto

A Stripe processa centenas de bilhões de dólares em pagamentos anuais. Qualquer
breaking change na API pode causar falhas em transações financeiras para milhões
de empresas. A estratégia de versionamento da Stripe é referência na indústria
por manter compatibilidade retroativa por mais de uma década.

## O Modelo de Versionamento

### Versão por Data, Não por Semver
Em vez de v1, v2, v3 (semver), a Stripe usa datas:
- `Stripe-Version: 2024-10-28.acacia`
- Cada versão é uma "snapshot" do comportamento da API naquela data
- O sufixo (acacia, etc.) identifica o release codename

### Pin por Conta
- Quando uma conta é criada, ela é automaticamente "pinada" na versão atual
- Todas as requests daquela conta usam aquela versão por padrão
- Para usar uma versão diferente, envie o header `Stripe-Version`
- Upgrade é opt-in, nunca forçado

### Compatibilidade Interna
- O dashboard da Stripe usa a mesma API pública
- Mas o dashboard sempre usa a versão mais recente
- Isso garante que a API nova funciona (dogfooding)

## Arquitetura Técnica

### O "Version Gates" Pattern
Internamente, a Stripe implementa "version gates" - condicionais no código que
alteram o comportamento baseado na versão da request:

```
Conceito simplificado:
if request.version >= "2023-10-16"
  # Novo comportamento
  retornar campo "amount" como inteiro em centavos
else
  # Comportamento antigo
  retornar campo "amount" como string com decimais
end
```

### Benefícios da Abordagem
- Código vive em um único codebase (não branches separados)
- Cada gate é documentado com a razão da mudança
- Gates podem ser removidos quando versões antigas são sunset

### Custo Técnico
- Centenas de version gates acumulam complexidade
- Cada gate precisa de testes para ambas as versões
- Novos engenheiros precisam entender o sistema de gates

## Tipos de Mudanças

### Mudanças Não-Breaking (Sem Nova Versão)
- Adicionar novos campos em respostas
- Adicionar novos endpoints
- Adicionar novos valores aceitos em enums existentes
- Adicionar novos eventos de webhook

**Princípio:** Adição nunca quebra; remoção sempre quebra.

### Mudanças Breaking (Requerem Nova Versão)
- Remover ou renomear campos existentes
- Mudar tipo de um campo (string para integer)
- Mudar comportamento padrão (default values)
- Alterar formato de resposta de erro
- Mudar regras de validação (aceitar menos input)

### Mudanças Impossíveis (Nunca Fazer)
- Mudar o significado de um campo existente sem renomear
- Alterar autenticação sem período de transição
- Remover endpoints sem deprecation notice de 12+ meses

## Processo de Deprecation

### Timeline Padrão
1. **Anúncio:** 12 meses antes, comunicação via email, changelog e docs
2. **Soft Deprecation:** API continua funcionando mas retorna warning header
3. **Dashboard Alert:** Clientes usando versão deprecated veem alerta
4. **Hard Deprecation:** API retorna erro (apenas após 24+ meses)
5. **Removal:** Código da versão antiga é removido

### Na Prática
- A Stripe raramente faz hard deprecation
- Muitas versões "deprecated" continuam funcionando indefinidamente
- Custo de manter > custo de quebrar clientes

## Documentação de Versões

### Changelog
- Cada versão tem changelog detalhado
- Mudanças organizadas por recurso (Charges, Customers, etc.)
- Exemplos de antes/depois para cada mudança
- Guia de migração passo-a-passo

### API Reference Versionada
- Documentação permite selecionar versão
- Exemplos de código ajustados para cada versão
- Campos deprecated são marcados visualmente

### Migration Guides
- Para cada par de versões, guia específico de migração
- Scripts de migração automatizados quando possível
- Estimativa de esforço para cada mudança

## Lições para C-Level

### 1. Backward Compatibility É Estratégia de Negócio
A Stripe gasta milhões mantendo versões antigas. Mas o custo de perder
um cliente por breaking change é muito maior. Para pagamentos, um erro
pode significar transações perdidas, receita não capturada.

**Aplicação:** Qualquer interface com clientes (API, UI, processos de atendimento)
deve tratar mudanças com o mesmo cuidado. "Upgrade forçado" é perda de clientes.

### 2. Opt-In > Opt-Out para Mudanças
Clientes da Stripe escolhem quando migrar. Isso transfere o controle
para quem tem mais contexto sobre o impacto (o próprio cliente).

**Aplicação:** Ao mudar processos, ferramentas ou interfaces internas,
ofereça período de transição onde ambas as versões coexistem.

### 3. Documentação É Produto
A documentação de versionamento da Stripe é tão boa quanto a API.
Cada mudança tem contexto, exemplos e guia de migração.

**Aplicação:** Mudanças organizacionais precisam do mesmo nível de documentação.
Uma reorganização sem "guia de migração" claro é um breaking change sem changelog.

### 4. Custo de Manter vs Custo de Quebrar
É tentador "limpar" versões antigas. Mas o cálculo quase sempre favorece manter.

**Aplicação:** Antes de descontinuar qualquer processo, ferramenta ou serviço:
- Quantos stakeholders dependem?
- Qual o custo de migração para cada um?
- Qual o custo de manter por mais 6-12 meses?

### 5. Additive-Only Como Princípio
A regra "adição nunca quebra" é aplicável muito além de APIs:
- Adicionar opções a um formulário: seguro
- Remover opções de um formulário: breaking change
- Adicionar um campo em um report: seguro
- Remover um campo de um report: breaking change

## Framework de Decisão: Quando Criar Nova Versão

Use este checklist para decidir se uma mudança requer nova versão:

| Pergunta | Se Sim |
|----------|--------|
| Algum campo existente muda de formato? | Nova versão |
| Algum campo existente é removido? | Nova versão |
| O comportamento padrão muda? | Nova versão |
| Um endpoint existente muda de semântica? | Nova versão |
| Validação se torna mais restritiva? | Nova versão |
| Apenas campos novos são adicionados? | Sem nova versão |
| Apenas endpoints novos são adicionados? | Sem nova versão |
| Validação se torna mais permissiva? | Sem nova versão |

## Comparação com Outras Abordagens

| Abordagem | Exemplo | Pros | Cons |
|-----------|---------|------|------|
| Versão por URL | `/v1/`, `/v2/` | Simples | Codebase duplicado |
| Versão por Header (data) | Stripe | Granular, sem duplicação | Complexity de gates |
| GraphQL (sem versão) | GitHub | Adição natural | Deprecation é difícil |
| Versão por Query Param | Twilio | Simples | Poluição da URL |

## Implementação Prática

### Para APIs Internas
Mesmo APIs internas entre microserviços devem ter versionamento:
- Evita "big bang" migrations
- Permite deploy independente de serviços
- Reduz coordenação entre times

### Para Produtos SaaS
- Considere "feature flags" como versões de produto
- Permita que clientes liguem/desliguem features novas
- Mantenha a experiência anterior disponível durante transição

### Para Processos Organizacionais
- Ao mudar um processo, rode ambas as versões em paralelo por 1-2 ciclos
- Colete feedback antes de descontinuar a versão anterior
- Documente o changelog do processo (o que mudou e por quê)

## Referências

- "APIs You Won't Hate" - Phil Sturgeon (2015)
- Stripe API Changelog (stripe.com/docs/upgrades)
- Stripe Engineering Blog: "API Versioning"
- "Designing Web APIs" - Brenda Jin, Saurabh Sahni, Amir Shevat (O'Reilly, 2018)
- Brandur Leach: "API Versioning Has No Right Answers"
