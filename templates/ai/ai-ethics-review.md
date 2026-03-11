# Template: Review de Ética de IA

## Propósito
Este template estrutura a avaliação ética de projetos e sistemas de inteligência artificial antes do deploy em produção. Garante que a organização considere impactos em pessoas, sociedade e grupos vulneráveis, alinhando inovação com responsabilidade.

## Instruções de Uso
1. Obrigatório para todo projeto de IA antes de ir a produção
2. Preenchido pelo time de desenvolvimento com revisão do comitê de ética
3. Reavaliação necessária a cada mudança significativa no modelo ou uso
4. Resultado deve ser documentado e armazenado para compliance

---

## Informações do Projeto

| Campo | Valor |
|-------|-------|
| **Projeto / Modelo** | [Nome] |
| **Versão** | [Versão sob avaliação] |
| **Responsável pelo Projeto** | [Nome — Cargo] |
| **Revisor de Ética** | [Nome — Cargo] |
| **Data da Revisão** | [DD/MM/AAAA] |
| **Resultado** | [Aprovado / Aprovado com Condições / Reprovado / Pendente] |

---

## 1. Descrição do Sistema

### 1.1 O que o Sistema Faz
[Descrição em linguagem acessível — evite jargão técnico]

### 1.2 Quem é Afetado
| Grupo | Como é Afetado | Volume |
|-------|---------------|--------|
| [Usuários diretos] | [Descrição do impacto] | [N pessoas] |
| [Usuários indiretos] | [Descrição do impacto] | [N pessoas] |
| [Grupos vulneráveis potencialmente afetados] | [Descrição] | [Estimativa] |

### 1.3 Nível de Automação
- [ ] **Totalmente automatizado** — decisão sem intervenção humana
- [ ] **Semi-automatizado** — IA recomenda, humano decide
- [ ] **Assistivo** — IA fornece informação, humano age
- [ ] **Monitoramento** — IA detecta padrões, humano interpreta

### 1.4 Criticidade da Decisão
- [ ] **Alta** — Impacta direitos, saúde, finanças ou oportunidades de pessoas
- [ ] **Média** — Impacta experiência do usuário significativamente
- [ ] **Baixa** — Impacto limitado e facilmente reversível

---

## 2. Avaliação de Viés e Fairness

### 2.1 Fontes Potenciais de Viés

| Fonte | Risco | Avaliação | Mitigação |
|-------|-------|----------|-----------|
| Dados de treinamento | [Dados refletem viéses históricos?] | [Alto/Médio/Baixo] | [Ação] |
| Features / variáveis proxy | [Alguma feature é proxy de atributo protegido?] | [Risco] | [Ação] |
| Labeling | [Anotadores trouxeram viéses nas labels?] | [Risco] | [Ação] |
| Representatividade | [Todos os grupos relevantes estão representados?] | [Risco] | [Ação] |
| Feedback loop | [O modelo pode amplificar viéses ao longo do tempo?] | [Risco] | [Ação] |

### 2.2 Análise de Fairness

| Métrica de Fairness | Grupo A | Grupo B | Gap | Aceitável? |
|---------------------|---------|---------|-----|:---------:|
| Taxa de falso positivo | [X%] | [X%] | [X pp] | [Sim/Não] |
| Taxa de falso negativo | [X%] | [X%] | [X pp] | [Sim/Não] |
| Demographic parity | [X%] | [X%] | [X pp] | [Sim/Não] |
| Equalized odds | [X%] | [X%] | [X pp] | [Sim/Não] |

### 2.3 Testes de Viés Realizados
- [Teste 1 — metodologia e resultado]
- [Teste 2 — metodologia e resultado]
- [Teste 3 — metodologia e resultado]

---

## 3. Privacidade e Proteção de Dados

### 3.1 Dados Pessoais Utilizados

| Tipo de Dado | Categoria LGPD | Necessário? | Base Legal | Minimização |
|-------------|---------------|:-----------:|-----------|------------|
| [Dado 1] | [Pessoal / Sensível] | [Sim/Não] | [Consentimento/Legítimo interesse/etc.] | [Como minimizamos] |
| [Dado 2] | [Categoria] | [Sim/Não] | [Base legal] | [Minimização] |

### 3.2 Checklist de Privacidade
- [ ] Dados anonimizados ou pseudonimizados quando possível
- [ ] Minimização de dados — apenas dados necessários são coletados
- [ ] Consentimento obtido quando exigido
- [ ] DPIA (Data Protection Impact Assessment) realizado
- [ ] Período de retenção definido
- [ ] Direito de exclusão implementado
- [ ] Dados não são compartilhados com terceiros sem base legal
- [ ] Criptografia em trânsito e em repouso

---

## 4. Transparência e Explicabilidade

### 4.1 Nível de Explicabilidade

| Dimensão | Status |
|----------|--------|
| O usuário sabe que IA está sendo usada? | [Sim / Não — plano para comunicar] |
| O usuário entende como a decisão foi tomada? | [Sim / Parcialmente / Não] |
| Explicações individuais estão disponíveis? | [Sim (SHAP/LIME) / Não] |
| Documentação do modelo é pública? | [Sim / Apenas interna] |

### 4.2 Como Comunicamos ao Usuário
[Descrever como o usuário é informado sobre o uso de IA e como pode entender as decisões]

### 4.3 Direito de Contestação
- **O usuário pode contestar uma decisão do modelo?** [Sim / Não]
- **Processo de contestação:** [Descrever canal e procedimento]
- **Tempo de resposta:** [X dias úteis]
- **Alternativa humana disponível:** [Sim / Não]

---

## 5. Segurança e Robustez

| Risco | Avaliação | Mitigação |
|-------|----------|-----------|
| Adversarial attacks | [O modelo é vulnerável a inputs maliciosos?] | [Medidas] |
| Data poisoning | [Dados de treino podem ser manipulados?] | [Medidas] |
| Model extraction | [O modelo pode ser copiado via API?] | [Rate limiting, etc.] |
| Prompt injection (se LLM) | [Aplicável?] | [Guardrails implementados] |
| Alucinação (se generativo) | [Modelo pode gerar informação falsa?] | [Grounding, verificação] |

---

## 6. Impacto Social e Ambiental

### 6.1 Impacto no Trabalho
- **O sistema substitui trabalho humano?** [Sim / Parcialmente / Não]
- **Quantas pessoas são impactadas:** [N]
- **Plano de transição:** [Requalificação / Realocação / N/A]

### 6.2 Impacto Ambiental
- **Custo computacional de treinamento:** [X kWh / kg CO2]
- **Custo computacional de inferência:** [X kWh/dia]
- **Medidas de eficiência:** [Model distillation, quantization, etc.]

### 6.3 Impacto em Grupos Vulneráveis
[Análise específica de como o sistema pode afetar desproporcionalmente grupos vulneráveis]

---

## 7. Decisão do Comitê de Ética

### 7.1 Resultado
- [ ] **Aprovado** — Sem restrições
- [ ] **Aprovado com Condições** — Implementar ações listadas antes do deploy
- [ ] **Reprovado** — Riscos éticos inaceitáveis no estado atual
- [ ] **Pendente** — Informações adicionais necessárias

### 7.2 Condições (se aplicável)
| # | Condição | Prazo | Responsável |
|---|---------|-------|-------------|
| 1 | [Condição obrigatória] | [Data] | [Nome] |
| 2 | [Condição] | [Data] | [Nome] |

### 7.3 Data da Próxima Revisão
[DD/MM/AAAA — revisões regulares para sistemas de IA em produção]

### 7.4 Assinaturas

| Papel | Nome | Data |
|-------|------|------|
| Responsável pelo Projeto | [Nome] | [Data] |
| Revisor de Ética | [Nome] | [Data] |
| DPO | [Nome] | [Data] |
| Sponsor Executivo | [Nome] | [Data] |

---

## Exemplo Preenchido (Resumo)

> **Sistema:** Scoring automático de candidatos em processo seletivo
> **Resultado:** Aprovado com condições
> **Condição 1:** Remover feature "CEP" (proxy para renda/etnia) — prazo: 15 dias
> **Condição 2:** Auditoria de fairness por gênero trimestral
> **Condição 3:** Decisão final sempre humana — modelo apenas rankeia, não elimina

---

## Dicas de Uso
- Ética não é checklist — é um exercício de reflexão genuína sobre impactos
- Envolva pessoas diversas na revisão — perspectivas diferentes identificam riscos diferentes
- "Não temos dados de viés" não significa "não há viés" — investigue
- Reavalie periodicamente — contexto social muda, o que era aceitável pode deixar de ser
- Documente decisões e trade-offs — auditores e reguladores vão perguntar
- Na dúvida, seja conservador — é melhor limitar uso do que causar dano
