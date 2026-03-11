# Engineering Phrases — Frases de Engenharia

## Princípio Central

Engenharia é sobre resolver problemas de negócio com tecnologia, gerenciando
trade-offs de forma explícita. Estas frases mantêm o foco em SLOs, trade-offs,
debt e pragmatismo.

**Mantra: "SLO, trade-off, debt."**

---

## Frases de Trade-offs

1. **"Qual é o trade-off? Não existe almoço grátis em engenharia."**
   Contexto: Exigir que toda proposta técnica explicite custos.

2. **"Rápido, bom, barato — escolha dois."**
   Contexto: Clássico triângulo de constraints.

3. **"Complexidade é custo. Cada abstração que adicionamos, alguém precisa manter."**
   Contexto: Resistir a over-engineering.

4. **"Build vs buy: tempo de build + manutenção vs custo de vendor + lock-in."**
   Contexto: Decisão recorrente de make or buy.

5. **"Qual é a solução mais simples que resolve o problema?"**
   Contexto: Preferir simplicidade sobre elegância.

6. **"Micro-serviço ou módulo? A pergunta certa é: qual é o custo operacional de cada?"**
   Contexto: Decisões de arquitetura.

7. **"Escalabilidade para quê? Para o tráfego de hoje ou para o de daqui 3 anos?"**
   Contexto: Right-sizing de soluções técnicas.

---

## Frases de SLOs e Reliability

8. **"Qual é o SLO? Não o que queremos — o que o negócio precisa."**
   Contexto: Definir SLOs baseados em necessidade real.

9. **"Error budget: quanto podemos errar antes de impactar o cliente?"**
   Contexto: Conceito de SRE para balancear velocity e reliability.

10. **"P99 importa mais que average. O pior caso define a experiência."**
    Contexto: Foco em tail latencies.

11. **"Monitoramento primeiro. Se não monitora, não sabe que está quebrado."**
    Contexto: Observability como pré-requisito.

12. **"Alertas devem ser acionáveis. Se o alerta toca e ninguém age, está errado."**
    Contexto: Alert hygiene.

13. **"MTTR > MTBF. Falhas vão acontecer. Velocidade de recovery é o que importa."**
    Contexto: Investir em recuperação, não apenas em prevenção.

---

## Frases de Tech Debt

14. **"Tech debt é dívida financeira. Tem juros. Quantifique: horas, risco, velocidade."**
    Contexto: Justificar investimento em tech debt reduction.

15. **"Quanto custa NÃO pagar essa dívida? Em horas de engenharia perdidas por semana?"**
    Contexto: Business case para refactoring.

16. **"Dívida intencional é ferramenta. Dívida acidental é negligência."**
    Contexto: Distinguir entre tech debt estratégico e descuido.

17. **"Tech debt sprint: 20% do capacity para pagar dívida. Não negociável."**
    Contexto: Proteger tempo de melhoria contínua.

18. **"Se não pagamos a dívida, eventualmente a dívida nos paga — com juros compostos."**
    Contexto: Warning sobre acúmulo de tech debt.

---

## Frases de Arquitetura e Design

19. **"O melhor código é o código que não escrevemos."**
    Contexto: Menos código = menos bugs = menos manutenção.

20. **"Premature optimization is the root of all evil — mas negligenciar performance é pior."**
    Contexto: Balance entre over e under optimization.

21. **"Interfaces claras, implementações substituíveis. Contratos antes de código."**
    Contexto: API-first design.

22. **"Se não cabe na cabeça de um dev, está complexo demais."**
    Contexto: Cognitive load como critério de design.

23. **"Reversibilidade de decisões técnicas: se posso mudar depois, escolho rápido agora."**
    Contexto: Two-way door decisions.

24. **"Qual é o blast radius se essa decisão estiver errada?"**
    Contexto: Avaliar impacto de decisões de arquitetura.

---

## Frases de Processo e Delivery

25. **"Ship daily. Se não fazemos deploy todo dia, há um problema no pipeline."**
    Contexto: Continuous delivery como norma.

26. **"Feature flag tudo. Deploy is not release."**
    Contexto: Separar deployment de feature enablement.

27. **"Code review não é burocracia. É o último check de qualidade antes de produção."**
    Contexto: Defender code review como investimento.

28. **"Testes automatizados não são opcionais. Se não testa, não funciona."**
    Contexto: Testing como parte do definition of done.

29. **"On-call é responsabilidade, não castigo. Se construiu, opera."**
    Contexto: You build it, you run it.

30. **"Incidents são aprendizado. Blameless post-mortems. Sempre."**
    Contexto: Cultura de aprendizado sem culpa.

---

## Frases de Comunicação Técnica para Não-Técnicos

31. **"Em termos de negócio: isso significa que [impacto em tempo, custo ou capacidade]."**
    Contexto: Traduzir técnico para business impact.

32. **"Não é mágica. É estatística aplicada com bons dados."**
    Contexto: Desmistificar AI/ML para stakeholders não-técnicos.

33. **"A escolha técnica é entre [tempo], [custo] e [risco]. Qual priorizamos?"**
    Contexto: Apresentar decisão técnica em termos de trade-off de negócio.

34. **"Escala: suportamos [X] hoje. Para [Y], precisamos de [investimento Z]."**
    Contexto: Comunicar capacity e investment needs.

35. **"A dívida técnica é como manutenção de um prédio. Ignorar não faz desaparecer."**
    Contexto: Analogia para explicar tech debt para não-técnicos.

---

## Uso e Contexto

Frases de engenharia funcionam quando:
- O CTO as usa consistentemente (modela o vocabulário)
- São acompanhadas de dados (quantificar trade-offs)
- O business context é explícito (não só tecnicalidade)
- A equipe inteira as adota (vocabulário compartilhado)
