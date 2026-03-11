# Anti-Patterns Guide — O Que NÃO Fazer

> Catálogo de anti-patterns comuns no C-Level Squad OS e como evitá-los.

---

## Objetivo

Anti-patterns são práticas que parecem razoáveis mas que prejudicam a eficácia
do squad. Reconhecê-los é tão importante quanto conhecer as boas práticas.
Este guia documenta os mais comuns com sinais de alerta e correcções.

---

## Anti-Patterns de Decisão

### 1. Analysis Paralysis
**O que é**: sobre-analisar ao ponto de não decidir.
**Sinais**: reuniões repetidas sobre o mesmo tema sem resolução; pedidos
constantes de "mais dados"; decisões Type 2 tratadas como Type 1.
**Impacto**: oportunidades perdidas, moral baixa, perda de momentum.
**Correcção**: definir deadline para decisão; aplicar teste de reversibilidade;
perguntar "que informação mudaria fundamentalmente a decisão?"

### 2. HiPPO (Highest Paid Person's Opinion)
**O que é**: a opinião do mais sénior domina independentemente dos dados.
**Sinais**: dados apresentados mas ignorados; ninguém discorda em reunião;
decisões "validam" conclusão pré-determinada.
**Impacto**: decisões de baixa qualidade, desengagement da equipa, cultura de compliance.
**Correcção**: exigir dados antes de opiniões; usar técnicas anónimas; sénior
fala por último em deliberações.

### 3. Decision Amnesia
**O que é**: esquecer ou reabrir decisões já tomadas.
**Sinais**: mesma decisão tomada várias vezes; decisões revertidas sem motivo
novo; ninguém sabe o que foi decidido.
**Impacto**: desperdício de tempo, inconsistência, perda de confiança.
**Correcção**: decision log obrigatório e consultado; decisões documentadas
não são reabertas sem informação nova significativa.

### 4. Consensus Trap
**O que é**: exigir concordância de todos para avançar.
**Sinais**: decisões atrasadas porque "ainda não há consenso"; veto informal
de qualquer membro; compromissos que não satisfazem ninguém.
**Impacto**: lentidão, decisões diluídas, frustração.
**Correcção**: usar RAPID com 1 Decider claro; "disagree and commit" como
norma; consenso é desejável, não obrigatório.

### 5. Urgency Addiction
**O que é**: tratar tudo como urgente, impedindo trabalho estratégico.
**Sinais**: constante firefighting; nada é planeado, tudo é reactivo;
important but not urgent nunca é endereçado.
**Impacto**: burnout, negligência estratégica, problemas que podiam ser
prevenidos tornam-se crises.
**Correcção**: classificar urgência objectivamente; proteger tempo para
trabalho estratégico; dizer "não" a falsas urgências.

---

## Anti-Patterns de Reunião

### 6. Meeting for Meeting's Sake
**O que é**: reuniões sem propósito claro ou que podiam ser um email.
**Sinais**: agenda vaga ou ausente; "sync" sem objectivos; nenhuma decisão
ou action item resulta da reunião.
**Impacto**: desperdício de tempo, fadiga de reuniões, cynicism.
**Correcção**: toda reunião tem agenda e propósito explícito; "esta reunião
podia ser async?" é pergunta legítima; cancelar reuniões sem agenda.

### 7. Information Waterfall
**O que é**: reunião usada para transmissão unidireccional de informação.
**Sinais**: 1 pessoa fala 80% do tempo; nenhuma pergunta ou discussão;
informação podia ter sido enviada por escrito.
**Impacto**: desperdício de tempo, desengagement, informação não retida.
**Correcção**: info de contexto enviada como pre-read; tempo de reunião para
discussão e decisão; formatos async para informação.

### 8. Decision Deferral
**O que é**: reunião termina sem decidir o que estava agendado para decisão.
**Sinais**: "vamos pensar mais sobre isto"; "precisamos de mais dados";
mesmos decision points aparecem semana após semana.
**Impacto**: backlog de decisões, bloqueios, perda de velocidade.
**Correcção**: decision rate tracking; deadline para cada decision point;
princípio: decidir é melhor que não decidir para Type 2.

---

## Anti-Patterns de Processo

### 9. Process Theater
**O que é**: seguir processos por formalismo sem extrair valor.
**Sinais**: checkboxes marcadas sem reflexão; templates preenchidos com
mínimo esforço; ninguém lê os outputs.
**Impacto**: overhead sem benefício, cynicism sobre processos.
**Correcção**: cada processo deve ter consumidor identificado; outputs devem
ser usados; processos sem valor são eliminados.

### 10. Tool Fetishism
**O que é**: focar em ferramentas em vez de resultados.
**Sinais**: constante procura da "ferramenta perfeita"; migração frequente
entre tools; mais tempo a configurar que a executar.
**Impacto**: produtividade baixa, overhead de transição, distracção.
**Correcção**: "a melhor ferramenta é a que usas"; avaliar antes de mudar;
resultado primeiro, ferramenta segundo.

### 11. Documentation Debt
**O que é**: não documentar decisões, processos e conhecimento.
**Sinais**: conhecimento existe apenas nas cabeças das pessoas; onboarding
é "fala com o fulano"; decisões passadas são desconhecidas.
**Impacto**: knowledge loss, onboarding lento, decisões inconsistentes.
**Correcção**: documentar como parte do processo, não como tarefa separada;
decision log obrigatório; "se não está escrito, não aconteceu".

### 12. Over-Engineering
**O que é**: criar processos e sistemas mais complexos que o necessário.
**Sinais**: frameworks com 20 passos para decisões simples; dashboards com
50 métricas; templates com campos que ninguém preenche.
**Impacto**: overhead, resistência ao uso, abandono do sistema.
**Correcção**: simplicidade como princípio; começar simples e adicionar
complexidade apenas quando necessário e justificado por dados.

---

## Anti-Patterns de Comunicação

### 13. Transparency Theater
**O que é**: aparentar transparência sem ser genuinamente transparente.
**Sinais**: informação partilhada mas sanitizada; más notícias suavizadas
ao ponto de perder significado; dados selectivos.
**Impacto**: desconfiança, decisões baseadas em informação incompleta.
**Correcção**: bad news travel fast (sem filtro); dados completos disponíveis;
cultura que não penaliza quem traz más notícias.

### 14. Silo Communication
**O que é**: informação não flui entre squads.
**Sinais**: squads surpreendidos por decisões de outros; duplicação de
esforço; conflitos por falta de coordenação.
**Impacto**: ineficiência, desalinhamento, conflitos evitáveis.
**Correcção**: cadências cross-squad; contratos com requisitos de comunicação;
canais partilhados; princípio de "share by default".

### 15. Jargon Overflow
**O que é**: usar terminologia complexa que exclui ou confunde.
**Sinais**: novos membros perdidos em reuniões; mesmos termos usados com
significados diferentes; comunicação ineficaz com stakeholders.
**Impacto**: exclusão, mal-entendidos, decisões baseadas em interpretação errada.
**Correcção**: glossário mantido e consultado; comunicação clara como valor;
verificar entendimento proactivamente.

---

## Anti-Patterns de AI

### 16. AI Worship
**O que é**: confiar cegamente em outputs de AI sem verificação.
**Sinais**: outputs usados directamente sem review; decisões baseadas
exclusivamente em AI; "a AI disse" como argumento final.
**Impacto**: erros propagados, decisões de baixa qualidade, risco.
**Correcção**: human-in-the-loop obrigatório; verificação de factos; AI como
input, nunca como decisor final.

### 17. AI Avoidance
**O que é**: recusar adoptar AI por medo ou desconfiança.
**Sinais**: processos manuais para tarefas automatizáveis; resistência sem
justificação; "sempre fizemos assim".
**Impacto**: ineficiência, desvantagem competitiva, oportunidade perdida.
**Correcção**: formação e awareness; pilotos de baixo risco; demonstrar valor
em casos concretos; respeitar preocupações genuínas.

---

## Como Usar Este Guia

1. **Leitura regular**: rever trimestralmente como equipa
2. **Self-assessment**: cada agente avalia se pratica algum anti-pattern
3. **Safe call-out**: membros do squad podem apontar anti-patterns sem retaliação
4. **Retrospectives**: anti-patterns como tema regular em retros
5. **Onboarding**: novos membros lêem como parte do onboarding

---

## Notas Técnicas

- Anti-patterns adicionados quando padrão recorrente é identificado
- Cada anti-pattern tem: definição, sinais, impacto e correcção
- Contribuições seguem `docs/contribution-guide.md`
- Revisão semestral para actualizar e adicionar novos patterns
