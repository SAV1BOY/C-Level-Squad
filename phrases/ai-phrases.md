# AI Phrases — Frases de Inteligência Artificial

## Princípio Central

AI é uma ferramenta poderosa que exige rigor. Estas frases mantêm a discussão
ancorada em evidência, evals, guardrails e ética. Nem hype, nem medo.

**Mantra: "Evals, guardrails, drift."**

---

## Frases de Avaliação (Evals)

1. **"Qual é o eval? Não aceito 'funciona bem'. Preciso de métricas."**
   Contexto: Exigir avaliação quantitativa de qualquer solução de AI.

2. **"Qual é o benchmark? Como se compara com uma regra simples?"**
   Contexto: Evitar complexidade desnecessária — às vezes uma heurística resolve.

3. **"Accuracy é vanity. Precision e recall são sanity. F1 é a métrica de equilíbrio."**
   Contexto: Ir além de accuracy para métricas que importam.

4. **"95% de accuracy com 10K decisões por dia = 500 erros por dia. Qual é o custo de cada erro?"**
   Contexto: Contextualizar accuracy em termos de impacto real.

5. **"Performance no test set é promessa. Performance em produção é realidade."**
   Contexto: A diferença entre offline e online performance.

6. **"Eval não é one-time. É contínuo. Modelos degradam. Dados mudam."**
   Contexto: Necessidade de avaliação contínua.

7. **"Qual é o baseline humano? Se o humano acerta 85%, o modelo precisa superar com margem."**
   Contexto: Comparar AI com alternativa humana, não com perfeição.

---

## Frases de Guardrails

8. **"Quais são os guardrails? O que acontece quando o modelo erra?"**
   Contexto: Planejar para falha, não apenas para sucesso.

9. **"Confidence threshold: abaixo de [X]%, escala para humano. Sem exceções."**
   Contexto: Definir limite de confiança para automação.

10. **"Kill switch: como desligamos em 5 minutos se algo der errado?"**
    Contexto: Plano de reversão rápida.

11. **"Human-in-the-loop para decisões de alto impacto. AI recomenda, humano decide."**
    Contexto: Princípio de supervisão humana.

12. **"Fallback plan: se o modelo cai, o que acontece? O serviço continua?"**
    Contexto: Graceful degradation quando AI falha.

13. **"Rate limiting: máximo de [X] decisões automáticas por [período]."**
    Contexto: Limitar blast radius de erros em escala.

---

## Frases de Data Quality

14. **"Garbage in, garbage out. Qual é a qualidade dos dados de treinamento?"**
    Contexto: Fundamento de qualquer projeto de AI.

15. **"De onde vêm os dados? São representativos? Estão enviesados?"**
    Contexto: Data provenance e bias assessment.

16. **"Volume não compensa qualidade. Mil dados ruins são piores que cem dados bons."**
    Contexto: Priorizar data quality sobre data quantity.

17. **"Data freshness: os dados de treinamento refletem o mundo de hoje?"**
    Contexto: Dados desatualizados produzem modelos desatualizados.

18. **"Label quality: quem rotulou os dados? Com que consistência?"**
    Contexto: Qualidade de anotação para supervised learning.

---

## Frases de Ethics e Fairness

19. **"Antes do deploy: fairness check, explicabilidade, opt-out. Nessa ordem."**
    Contexto: Checklist ético pré-deployment.

20. **"Para quem o modelo pode ser injusto? Quais grupos estão sub-representados?"**
    Contexto: Fairness assessment por grupo demográfico.

21. **"Se não podemos explicar, não devemos deployar para decisões que afetam pessoas."**
    Contexto: Explicabilidade como requisito para decisões impactantes.

22. **"Consent: o usuário sabe que AI está tomando/influenciando essa decisão?"**
    Contexto: Transparência com o usuário final.

23. **"LGPD compliance: dados pessoais no modelo? Consent existe? Opt-out funciona?"**
    Contexto: Regulação brasileira de dados pessoais.

---

## Frases de Monitoramento e Drift

24. **"Modelo em produção sem monitoring é bomba-relógio."**
    Contexto: Obrigatoriedade de monitoramento.

25. **"Data drift: os dados de produção mudaram em relação ao treinamento?"**
    Contexto: Detectar quando o mundo mudou e o modelo não acompanhou.

26. **"Concept drift: a relação entre features e target mudou?"**
    Contexto: Mudança no padrão subjacente que o modelo aprendeu.

27. **"Re-train cadence: com que frequência retreinamos? Baseado em que trigger?"**
    Contexto: Definir quando e por que retreinar modelos.

28. **"A/B test em produção: novo modelo vs modelo atual. Dados reais, não simulados."**
    Contexto: Validação de novos modelos em produção.

---

## Frases de Pragmatismo

29. **"AI não é mágica. É estatística aplicada com bons dados."**
    Contexto: Desmistificar AI para stakeholders.

30. **"Precisa ser AI? Uma regra if-then resolve? Um dashboard resolve?"**
    Contexto: Evitar AI solutionism.

31. **"Demo é marketing. Quero eval com nossos dados, nossos users, nosso contexto."**
    Contexto: Resistir a decisões baseadas em demos impressionantes.

32. **"AI roadmap depende de data readiness. Sem dados, sem modelo."**
    Contexto: Sequenciar investimento — dados antes de modelos.

33. **"O custo de usar AI mal é maior que o custo de não usar AI."**
    Contexto: Medir o risco de implementação ruim.

34. **"LLMs são excelentes para [X] e péssimos para [Y]. Saibamos a diferença."**
    Contexto: Conhecer limitações de cada tipo de modelo.

35. **"ROI de AI: custo de build + operate vs valor gerado. Se não fecha, não faz."**
    Contexto: Business case para investimento em AI.

---

## Uso e Contexto

Frases de AI são mais eficazes quando:
- O CAIO as usa com consistência e credibilidade técnica
- São acompanhadas de eval data real (não teórica)
- Combinam rigor com acessibilidade (não intimidar não-técnicos)
- São revisadas conforme a tecnologia evolui
