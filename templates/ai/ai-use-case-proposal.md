# Template: Proposta de Use Case de IA

## Propósito
Este template estrutura a proposição de novos casos de uso de inteligência artificial na organização. Garante que propostas sejam avaliadas com rigor técnico, viabilidade de dados, impacto no negócio e considerações éticas antes de receberem investimento.

## Instruções de Uso
1. Preencha com dados reais sobre o problema e a oportunidade
2. Valide viabilidade de dados com time de dados/ML antes de submeter
3. Inclua estimativa de ROI para priorização junto a outros use cases
4. Revisão de ética/compliance obrigatória antes de aprovação

---

## Informações da Proposta

| Campo | Valor |
|-------|-------|
| **Título do Use Case** | [Nome descritivo — ex: "Previsão de churn por ML"] |
| **Proponente** | [Nome — Cargo] |
| **Data** | [DD/MM/AAAA] |
| **Área Beneficiada** | [Produto / Vendas / CS / Ops / etc.] |
| **Classificação** | [Automação / Predição / Geração / Recomendação / Classificação / Extração] |
| **Prioridade Sugerida** | [Alta / Média / Baixa] |
| **Status** | [Proposto / Em Avaliação / Aprovado / Em Desenvolvimento / Produção / Rejeitado] |

---

## 1. Problema e Oportunidade

### 1.1 Problema Atual
[Descrever o problema que IA pode resolver]
- **Quem é afetado:** [Usuários, clientes, equipe interna]
- **Frequência:** [Quantas vezes o problema ocorre — diário/semanal/etc.]
- **Impacto atual:** [Custo, tempo perdido, experiência degradada]

### 1.2 Como é Feito Hoje
[Processo atual — manual, semi-automático, regras estáticas]
- **Custo atual:** [R$ X / N horas por período]
- **Qualidade atual:** [Acurácia, tempo de resposta, consistência]
- **Limitações:** [Por que o método atual não é suficiente]

### 1.3 Oportunidade com IA
[Como IA pode melhorar significativamente sobre o método atual]
- **Melhoria esperada:** [Quantificar — ex: "Reduzir tempo de 2h para 5min" ou "Aumentar acurácia de 60% para 90%"]
- **Escala possível:** [O que IA permite que seria impossível manualmente]

---

## 2. Solução Proposta

### 2.1 Abordagem Técnica
- **Tipo de modelo:** [Classificação / Regressão / NLP / Computer Vision / GenAI / etc.]
- **Abordagem sugerida:** [Modelo treinado do zero / Fine-tuning / API de LLM / Regras + ML híbrido]
- **Complexidade:** [Baixa — API existente / Média — fine-tuning / Alta — modelo proprietário]

### 2.2 Dados Necessários

| Dado | Fonte | Disponível? | Volume | Qualidade |
|------|-------|:-----------:|--------|-----------|
| [Dataset 1] | [Sistema/DB] | [Sim/Parcial/Não] | [N registros] | [Alta/Média/Baixa] |
| [Dataset 2] | [Sistema/DB] | [Sim/Parcial/Não] | [N registros] | [Qualidade] |
| [Dataset 3] | [Sistema/DB] | [Sim/Parcial/Não] | [N registros] | [Qualidade] |

**Gaps de dados:** [Dados que não temos e precisamos coletar/comprar]
**Dados sensíveis:** [Sim/Não — se sim, quais e como serão protegidos]

### 2.3 Integração

| Ponto de Integração | Sistema | Tipo | Complexidade |
|---------------------|---------|------|-------------|
| [Input — de onde vem dados] | [Sistema] | [API / Batch / Stream] | [A/M/B] |
| [Output — onde resultado é usado] | [Sistema] | [API / UI / Notificação] | [A/M/B] |
| [Feedback loop] | [Sistema] | [Como capturar qualidade] | [A/M/B] |

### 2.4 Experiência do Usuário
[Como o usuário final interage com a solução de IA]
- **Interface:** [Dashboard / Notificação / Automação invisível / Chat / etc.]
- **Nível de automação:** [Totalmente automatizado / Humano no loop / Sugestão para humano decidir]
- **Explicabilidade:** [Modelo precisa explicar suas decisões? Como?]

---

## 3. Métricas de Sucesso

### 3.1 Métricas Técnicas

| Métrica | Baseline Atual | Meta Mínima | Meta Alvo |
|---------|---------------|-------------|----------|
| Acurácia / F1 Score | [X%] | [X%] | [X%] |
| Latência de inferência | [N/A] | [<X ms] | [<X ms] |
| Taxa de falso positivo | [X%] | [<X%] | [<X%] |
| Cobertura | [X%] | [>X%] | [>X%] |

### 3.2 Métricas de Negócio

| Métrica | Antes | Esperado | Impacto em R$ |
|---------|-------|---------|--------------|
| [Métrica 1 — ex: Churn rate] | [X%] | [Y%] | [R$ X/ano] |
| [Métrica 2 — ex: Tempo de resposta] | [X min] | [Y min] | [R$ X/ano] |
| [Métrica 3 — ex: Conversão] | [X%] | [Y%] | [R$ X/ano] |

---

## 4. Estimativa de Investimento e ROI

| Item | Custo |
|------|-------|
| Desenvolvimento (N pessoas x M meses) | [R$ X] |
| Infraestrutura de ML (GPU, storage) | [R$ X/mês] |
| Dados (aquisição, labeling) | [R$ X] |
| APIs externas (OpenAI, etc.) | [R$ X/mês] |
| **Custo total (12 meses)** | **[R$ X]** |

**Benefício esperado (12 meses):** [R$ X]
**ROI:** [X%]
**Payback:** [X meses]

---

## 5. Riscos e Considerações Éticas

### 5.1 Riscos Técnicos

| Risco | Probabilidade | Impacto | Mitigação |
|-------|-------------|---------|-----------|
| Dados insuficientes/qualidade ruim | [A/M/B] | [A/M/B] | [Plano] |
| Modelo não atinge performance mínima | [A/M/B] | [A/M/B] | [Plano] |
| Drift do modelo ao longo do tempo | [A/M/B] | [A/M/B] | [Monitoramento + retrain] |
| Dependência de API externa (uptime) | [A/M/B] | [A/M/B] | [Fallback] |

### 5.2 Considerações Éticas

| Dimensão | Avaliação | Mitigação |
|----------|----------|-----------|
| Viés/Discriminação | [Risco de viés nos dados ou modelo?] | [Como testar e mitigar] |
| Privacidade | [Dados pessoais envolvidos?] | [Anonimização / Consentimento] |
| Transparência | [Usuário sabe que IA está sendo usada?] | [Como comunicar] |
| Impacto em empregos | [Substitui trabalho humano?] | [Plano de transição] |
| Segurança | [Pode ser explorado por adversários?] | [Medidas de segurança] |

### 5.3 Compliance
- **LGPD/GDPR:** [Aplicável? Como será atendido?]
- **Regulação setorial:** [Há regulação específica para uso de IA neste setor?]
- **Política interna de IA:** [Em conformidade com a política da empresa?]

---

## 6. Plano de Implementação

| Fase | Atividades | Duração | Entregável |
|------|-----------|---------|-----------|
| 1 — Exploração | Análise de dados, POC rápida | [X semanas] | Relatório de viabilidade |
| 2 — MVP | Modelo mínimo, integração básica | [X semanas] | MVP em staging |
| 3 — Piloto | Teste com grupo restrito | [X semanas] | Resultados do piloto |
| 4 — Produção | Rollout completo | [X semanas] | Modelo em produção |
| 5 — Otimização | Monitoramento e melhoria | Contínuo | Dashboards e retrain |

---

## Exemplo Preenchido (Resumo)

> **Use Case:** Classificação automática de tickets de suporte por categoria e urgência
> **Abordagem:** Fine-tuning de LLM (GPT-4o) com histórico de 50K tickets
> **Acurácia esperada:** 92% (vs 78% com regras atuais)
> **Impacto:** Redução de 40% no tempo de triagem = economia de R$ 280K/ano (2 FTEs)
> **Investimento:** R$ 120K (dev + infra 12 meses) | **ROI:** 133% | **Payback:** 5 meses
> **Risco ético:** Baixo — não envolve decisões sobre pessoas, apenas routing de tickets

---

## Dicas de Uso
- Nem todo problema precisa de IA — se regras simples resolvem, use regras
- Dados são mais importantes que modelo — invista em qualidade de dados primeiro
- Sempre tenha fallback para quando o modelo falhar — IA não é 100%
- Comece com POC rápida (2-4 semanas) para validar viabilidade antes de investir pesado
- Human-in-the-loop é quase sempre melhor que automação total no início
- Monitore performance em produção continuamente — modelos degradam com o tempo
