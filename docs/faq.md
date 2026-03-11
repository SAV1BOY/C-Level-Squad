# FAQ — Perguntas Frequentes

> Respostas às perguntas mais comuns sobre o C-Level Squad OS.

---

## Sobre o Sistema

### O que é o C-Level Squad OS?
É um sistema operacional organizacional composto por agentes de AI que
desempenham funções executivas. Inclui processos, frameworks, templates e
scripts que coordenam a operação de nível C-Level. Não é software — é um
sistema de ficheiros, processos e práticas.

### Quem deve usar o C-Level Squad?
Fundadores, CEOs, COOs, Chiefs of Staff e equipas de liderança que querem
estruturar operações executivas com suporte de AI. É especialmente útil para
organizações em crescimento que precisam de escalar processos de gestão.

### O C-Level Squad substitui líderes humanos?
Não. O squad amplifica liderança humana, não a substitui. Fornece estrutura,
consistência e capacidade analítica. Decisões críticas e julgamento humano
continuam a ser essenciais.

### Quanto tempo leva a implementar?
A configuração inicial leva 1-2 semanas. O período de calibração e adaptação
ao contexto é de 4-8 semanas. Resultados significativos começam a ser visíveis
após 1-2 trimestres de uso consistente.

### Preciso de usar todos os 6 agentes?
Não. Começa com 1-2 agentes mais relevantes para o teu contexto (tipicamente
Vision Chief + COO Orchestrator) e expande gradualmente conforme necessidade
e conforto.

---

## Sobre os Agentes

### Como é que os agentes comunicam entre si?
Através de contratos cross-squad que definem SLAs, DoR/DoD e protocolos de
handoff. A coordenação é feita via cadências regulares (WBR, MBR) e
comunicação assíncrona para itens do dia-a-dia.

### E se dois agentes discordarem?
O processo é: debate com dados → tentativa de compromisso → escalação ao
Vision Chief para decisão final. Dissent é registado mas não impede execução
após a decisão.

### Posso personalizar os agentes?
Sim e deveria. Os agentes vêm com configuração genérica que deve ser adaptada
ao contexto da tua organização: sector, tamanho, maturidade, prioridades.

### Os agentes aprendem com o tempo?
O sistema acumula memória organizacional através do decision log, forecasts,
health scores e post-mortems. Esta informação alimenta decisões futuras e
melhora a calibração dos agentes.

---

## Sobre Processos e Cadências

### O que acontece se perdermos uma WBR?
Uma WBR perdida não é o fim do mundo, mas o padrão é nunca perder. Se
necessário cancelar, o COO Orchestrator deve aprovar e comunicar. Dados e
decisões pendentes transitam para a próxima cadência.

### Quanto tempo deve demorar uma WBR?
60 minutos é o padrão. Pode ser ajustado para 45 (squad pequeno, poucas
decisões) ou 90 (muitos itens, período complexo). Nunca deve ultrapassar
90 minutos regularmente.

### Preciso de todas as cadências (daily, weekly, monthly, quarterly)?
O mínimo é semanal (WBR). Daily é recomendada mas pode ser assíncrona.
Monthly e quarterly são fortemente recomendadas para manter perspectiva
estratégica. Adapta a frequência ao tamanho e necessidade.

### Como lidar com excesso de action items?
Se action items acumulam consistentemente, é sintoma de sobrecarga ou má
priorização. Solução: repriorizar agressivamente, delegar mais, reduzir
scope, ou aumentar capacidade. Nunca ignores — trata a causa raiz.

---

## Sobre Decisões

### Todas as decisões precisam de ser registadas?
Não. Apenas decisões que cumprem o critério de relevância: impacto financeiro
significativo, afecta múltiplos squads, implicações estratégicas, altera
política ou é difícil de reverter. Decisões operacionais rotineiras não
precisam de registo formal.

### O que é uma decisão Type 1 vs Type 2?
Type 1 (one-way door): irreversível ou muito custosa de reverter. Requer
processo deliberado. Type 2 (two-way door): reversível. Deve ser tomada
rapidamente. A maioria das decisões é Type 2.

### Como sei quem deve decidir?
O framework RAPID define papéis. Por defeito: cada agente decide no seu
domínio. Decisões cross-domain escalam ao owner do domínio mais afectado ou
ao Vision Chief se impacto é transversal.

### E se tomarmos uma decisão errada?
Depende do tipo. Type 2: reverter rapidamente e aprender. Type 1: avaliar
impacto, mitigar consequências, fazer post-mortem. Em ambos: registar no
decision log com outcome e learnings. Nunca atribuir culpa — focar no sistema.

---

## Sobre Frameworks

### São obrigatórios os frameworks para decidir?
Não de forma rígida. Frameworks são ferramentas, não burocracia. Para decisões
simples, bom julgamento é suficiente. Para decisões complexas ou de alto
impacto, frameworks melhoram consistência e qualidade.

### Posso criar os meus próprios frameworks?
Sim. Segue o processo em `docs/contribution-guide.md`. Documenta o framework,
testa com cenário real, obtém review e aprovação.

### Como escolho o framework certo?
Consulta `docs/framework-selection-guide.md` que tem uma árvore de decisão
e mapeamento por situação.

---

## Sobre AI e Governance

### Que modelos de AI posso usar?
O CAIO Architect mantém uma lista de ferramentas aprovadas. Para risco baixo/
médio, a maioria das ferramentas modernas é aceitável. Para risco alto/crítico,
é necessária avaliação formal via `scripts/analysis/ai-eval-runner.md`.

### Como garantir que outputs de AI são fiáveis?
Human-in-the-loop para decisões importantes, verificação de factos, múltiplas
fontes, e audit trail. Nunca confies cegamente — valida sempre.

### Quais são os limites éticos do uso de AI?
Definidos em `docs/ai-governance.md`. Princípios-chave: transparência,
fairness, privacidade, accountability humana. Quando em dúvida, escala ao
CAIO Architect.

---

## Sobre Implementação

### Como migro processos existentes para o C-Level OS?
Gradualmente. Mantém processos actuais enquanto introduces elementos do OS
um de cada vez. Começa pelas cadências (WBR), depois decision logging,
depois frameworks. Nunca tentes migrar tudo ao mesmo tempo.

### O C-Level Squad funciona com equipas distribuídas?
Sim. O sistema é baseado em ficheiros e processos assíncronos, o que o torna
adequado para equipas remotas. Cadências síncronas podem ser virtuais.

### Que tamanho de organização é adequado?
O sistema escala desde organizações de 5 pessoas até centenas. Para equipas
muito pequenas (<5), simplifica as cadências. Para equipas grandes, cada
squad pode ter sub-squads com a mesma estrutura.

### Quanto custa implementar?
O sistema em si é baseado em ficheiros — sem custos de licença. Custos reais
são: tempo de configuração, tempo de formação, e custos de ferramentas de AI
que escolheres integrar.

---

## Troubleshooting

### As métricas estão desactualizadas — o que fazer?
Verificar fontes de dados (APIs, exports). Verificar frequência de
actualização. Se dados manuais, verificar que owners estão a actualizar.
Automação de data pull é a melhor solução de longo prazo.

### O squad está a ter reuniões improdutivas — como melhorar?
Consulta `scripts/analysis/meeting-effectiveness-analyzer.md`. Causas comuns:
agendas fracas, falta de pre-read, excesso de participantes, falta de
facilitação. Mede antes de intervir.

### Action items acumulam-se sem ser concluídos — porquê?
Causas comuns: sobrecarga, priorização fraca, action items ambíguos, falta
de accountability. Solução: menos items mas mais claros, owners explícitos,
follow-up na WBR, coragem para re-negociar prazos.

---

## Notas Técnicas

- FAQ actualizada quando novas perguntas recorrentes são identificadas
- Contribuições de perguntas e respostas seguem `docs/contribution-guide.md`
- Se a tua pergunta não está aqui, consulta a documentação específica
- FAQ revista trimestralmente para manter relevância
