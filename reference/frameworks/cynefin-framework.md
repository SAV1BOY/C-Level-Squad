# Framework: Cynefin

## Descrição

O Cynefin Framework (pronuncia-se "kuh-NEV-in", galês para "habitat") foi criado por Dave Snowden na IBM nos anos 2000. É um framework de sense-making que ajuda líderes a entender em que tipo de contexto estão operando e, com base nisso, escolher a abordagem de gestão e decisão adequada. Cynefin distingue cinco domínios: Claro (Simple), Complicado, Complexo, Caótico e Desordem — cada um exigindo uma resposta diferente. É particularmente valioso para C-Levels que enfrentam diferentes tipos de problemas simultaneamente.

## Quando Usar

### Situações Ideais
- Antes de decidir que abordagem usar para resolver um problema
- Quando soluções tradicionais não estão funcionando e não se sabe por quê
- Para calibrar expectativas sobre previsibilidade e controle
- Em situações de crise para determinar tipo de resposta necessária
- Para alinhar time executivo sobre a natureza de desafios estratégicos
- Ao decidir entre planejamento detalhado vs. experimentação

### Quando NÃO Usar
- Quando o tipo de problema é óbvio (não precisa de framework para decidir)
- Como justificativa para não planejar ("é complexo, não dá para planejar")
- Para problemas puramente técnicos com solução conhecida

## Como Aplicar

### Os Cinco Domínios

#### 1. Claro (Simple/Obvious)
```
Características: Causa-efeito óbvia, melhores práticas existem
Abordagem: Perceber → Categorizar → Responder
Exemplo: Processo de onboarding documentado, checklist de deploy
Gestão: Procedimentos operacionais padrão, delegação, automação
Risco: Complacência — pode ser empurrado para Caótico se ignorado
```

#### 2. Complicado
```
Características: Causa-efeito existe mas requer análise especializada
Abordagem: Perceber → Analisar → Responder
Exemplo: Arquitetura de sistema, modelagem financeira, planejamento tributário
Gestão: Consultoria especializada, análise de dados, boas práticas (não "melhores")
Risco: Analysis paralysis — excesso de análise sem ação
```

#### 3. Complexo
```
Características: Causa-efeito só é compreensível em retrospecto
Abordagem: Sondar → Perceber → Responder
Exemplo: Cultura organizacional, product-market fit, posicionamento de mercado
Gestão: Experimentação, safe-to-fail probes, emergência, diversidade
Risco: Tentar aplicar planejamento detalhado a problemas complexos
```

#### 4. Caótico
```
Características: Sem relação causa-efeito perceptível, crise
Abordagem: Agir → Perceber → Responder
Exemplo: Crise de PR, breach de segurança, crash de mercado
Gestão: Ação imediata para estabilizar, liderança forte, comunicação clara
Risco: Paralisia por busca de informação em vez de ação
```

#### 5. Desordem (Centro)
```
Características: Não se sabe em que domínio está
Abordagem: Primeiro classificar, depois agir conforme o domínio
Risco: Cada pessoa aplica a abordagem do domínio que é mais confortável
```

### Processo para C-Level Squad
```
1. Listar os desafios/decisões atuais da organização
2. Para cada um, discutir: em que domínio está?
3. Verificar consenso — divergências revelam diferentes perspectivas
4. Aplicar a abordagem adequada ao domínio:
   - Claro: delegar, automatizar, SOPs
   - Complicado: chamar especialistas, analisar dados
   - Complexo: experimentar, testar hipóteses, pilotar
   - Caótico: agir agora, estabilizar, depois analisar
5. Reavaliar periodicamente: domínios mudam
```

## Exemplos

### Classificação de Decisões C-Level Típicas
```
CLARO:
- Processos de compliance e auditoria
- Relatórios financeiros mensais
- Renovação de ferramentas e licenças

COMPLICADO:
- Arquitetura de sistemas de larga escala
- Modelagem financeira e valuation
- Estratégia de compensação e benefícios
- Planejamento de capacidade técnica

COMPLEXO:
- Product-market fit em novo segmento
- Transformação cultural
- Entrada em novo mercado
- Adoção de IA na organização
- Estratégia de go-to-market

CAÓTICO:
- Vazamento de dados de clientes
- Perda súbita de cliente-chave (>30% receita)
- Crise de reputação viral
- Founder/C-Level saindo inesperadamente
```

### Aplicação em Decisão de Produto
```
Problema: "Taxa de churn está aumentando"

Se COMPLICADO: Analisar dados de cohort, entrevistar churned customers,
identificar causa raiz, implementar solução baseada em análise

Se COMPLEXO: Lançar múltiplos experimentos simultâneos (safe-to-fail),
observar o que funciona, amplificar o que dá certo, amortecer o que não dá
```

## Limitações

- **Classificação subjetiva** - Diferentes pessoas classificam o mesmo problema em domínios diferentes
- **Limites fluidos** - Problemas podem transitar entre domínios ou estar em múltiplos simultaneamente
- **Não prescritivo** - Diz COMO pensar, não O QUE fazer especificamente
- **Tentação de "tudo é complexo"** - Pode ser usado para evitar planejamento e análise quando são necessários
- **Difícil de operacionalizar** - Conceito intuitivo mas difícil de transformar em processo
- **Acadêmico** - Pode parecer abstrato demais para gestores orientados a ação
- **Não é modelo de implementação** - Precisa ser combinado com outros frameworks para execução
