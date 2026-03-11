# AI Governance — Guia de Governance Específica para AI

> Políticas, processos e standards para utilização responsável de AI no C-Level Squad.

---

## Objetivo

Estabelecer um framework de governance que permita aproveitar o potencial da AI
enquanto gere os riscos associados. AI governance não é burocracia — é a condição
para adopção sustentável e confiável.

---

## Princípios de AI Governance

### 1. Human-in-the-Loop (Humano no Circuito)
- Decisões críticas requerem validação humana
- AI recomenda, humano decide (para decisões Type 1)
- Escalação automática quando confiança do modelo é baixa
- Override humano é sempre possível

### 2. Transparência e Explicabilidade
- Outputs de AI incluem indicação de confiança
- Raciocínio do modelo é documentado quando possível
- Stakeholders sabem quando AI está envolvida no processo
- Audit trail completo de inputs, outputs e decisões

### 3. Fairness e Não-Discriminação
- Outputs avaliados para vieses antes de uso em decisões
- Dados de treino revistos para representatividade
- Impacto diferencial monitorizado por grupos relevantes
- Correcção de vieses detectados é prioritária

### 4. Privacidade e Segurança
- Dados pessoais não usados sem consentimento adequado
- Minimização de dados: usar apenas o necessário
- Encriptação e controlo de acesso para dados sensíveis
- Retenção limitada ao necessário

### 5. Accountability
- Cada uso de AI tem um owner humano responsável
- Responsabilidade por outputs de AI é do owner, não da AI
- Decisões baseadas em AI são registadas no decision log
- Incidentes de AI são analisados com post-mortem

---

## Classificação de Risco de AI

### Níveis de Risco
```
CRÍTICO: AI afecta decisões sobre pessoas, saúde, segurança, direitos
  → Governance máxima, aprovação do board, auditoria externa

ALTO: AI afecta decisões financeiras significativas ou estratégicas
  → Governance forte, aprovação C-Level, auditoria interna

MÉDIO: AI automatiza processos operacionais com impacto moderado
  → Governance standard, aprovação squad lead, self-audit

BAIXO: AI assiste em tarefas de baixo impacto e facilmente reversíveis
  → Governance mínima, guidelines seguidas, uso responsável
```

### Exemplos por Nível
| Nível | Exemplos |
|-------|---------|
| Crítico | Decisões de contratação/despedimento, scoring de crédito, diagnóstico |
| Alto | Previsões financeiras, pricing, alocação de recursos, estratégia |
| Médio | Geração de reports, análise de dados, automação de workflows |
| Baixo | Assistência de escrita, pesquisa, sumarização, brainstorming |

---

## Processo de Aprovação para Uso de AI

### Para Risco Baixo e Médio
1. Utilizador verifica que o uso está dentro das guidelines
2. Aplica boas práticas (ver secção seguinte)
3. Regista uso significativo no log
4. Nenhuma aprovação formal necessária

### Para Risco Alto
1. Proposta escrita com: objectivo, dados, modelo, riscos
2. Revisão pelo CAIO Architect
3. Aprovação pelo squad lead + CAIO
4. Implementação com monitoring definido
5. Review periódica (trimestral)

### Para Risco Crítico
1. Proposta detalhada com impact assessment
2. Revisão pelo CAIO + CIO (segurança e dados)
3. Aprovação pelo Vision Chief
4. Board notification ou aprovação
5. Auditoria externa antes de production
6. Monitoring contínuo com thresholds
7. Review mensal no primeiro trimestre, depois trimestral

---

## Boas Práticas de Utilização

### Do's
- Verificar outputs de AI antes de usar em decisões
- Indicar quando um output foi gerado ou assistido por AI
- Usar prompts claros e específicos para melhores resultados
- Manter registo de interacções significativas
- Reportar comportamentos inesperados ou preocupantes
- Combinar AI output com julgamento humano
- Actualizar prompts e workflows com base em resultados

### Don'ts
- Não confiar cegamente em outputs sem verificação
- Não inserir dados pessoais sensíveis sem autorização
- Não usar AI para decisões que requerem empatia humana exclusiva
- Não ignorar sinais de viés ou erro sistemático
- Não usar modelos não aprovados para tarefas de risco alto/crítico
- Não partilhar outputs confidenciais sem classificação adequada
- Não automatizar decisões Type 1 sem human-in-the-loop

---

## Avaliação e Monitorização

### Métricas de AI Governance
| Métrica | Target | Frequência |
|---------|--------|-----------|
| AI incidents | 0 críticos | Contínuo |
| Compliance com guidelines | >95% | Trimestral |
| Bias checks realizados | 100% (alto/crítico) | Por deployment |
| Audit trail completude | >99% | Mensal |
| User satisfaction com AI tools | >4.0/5 | Trimestral |
| ROI de AI initiatives | Positivo | Semestral |
| AI literacy score da equipa | >70/100 | Anual |

### Monitorização Contínua
Para cada sistema de AI em produção:
1. **Performance monitoring**: accuracy, latency, error rate
2. **Bias monitoring**: outputs analisados por fairness
3. **Drift detection**: degradação de performance ao longo do tempo
4. **Usage monitoring**: quem usa, quanto, para quê
5. **Cost monitoring**: custo vs budget vs valor gerado

---

## Incidentes de AI

### Classificação de Incidentes
| Tipo | Descrição | Severidade |
|------|----------|-----------|
| Hallucination | AI gera informação falsa usada em decisão | Alta |
| Bias | Output discriminatório detectado | Alta |
| Data leak | Dados sensíveis expostos via AI | Crítica |
| Misuse | AI usada para fim não autorizado | Variável |
| Failure | AI falha em completar tarefa crítica | Média-Alta |
| Drift | Performance degrada sem detecção | Média |

### Processo de Resposta
1. **Detectar**: identificar incidente (automático ou reportado)
2. **Conter**: limitar impacto imediato (suspender se necessário)
3. **Analisar**: root cause analysis
4. **Remediar**: corrigir causa e consequências
5. **Comunicar**: informar stakeholders afectados
6. **Prevenir**: implementar controles adicionais
7. **Registar**: documentar incidente e learnings

---

## Formação e Awareness

### Programa de AI Literacy
- **Nível 1 — Awareness**: o que é AI, capabilities e limitações (todos)
- **Nível 2 — User**: como usar ferramentas de AI efectivamente (users)
- **Nível 3 — Builder**: como construir e avaliar sistemas de AI (técnicos)
- **Nível 4 — Governance**: como governar AI responsavelmente (leaders)

### Frequência
- Onboarding: Nível 1 obrigatório para todos
- Trimestral: update sobre novas ferramentas e guidelines
- Ad hoc: quando nova ferramenta é adoptada ou incidente ocorre

---

## Notas Técnicas

- Políticas de AI em `data/policies/ai-governance/`
- Log de AI usage em `data/ai-usage-log/`
- Eval results em `data/ai-evals/`
- Review calendar gerido pelo CAIO Architect
- Integração com AI eval runner para avaliações sistemáticas
