# Drill de Disaster Recovery

> Processo estruturado para testar a capacidade de recuperação da organização
> frente a desastres tecnológicos, garantindo que planos de DR funcionam
> quando mais importam.

## Objetivo

Validar que os planos de disaster recovery funcionam na prática, identificar
gaps antes que um desastre real aconteça, e treinar a equipe para responder
com velocidade e confiança em cenários de crise.

## Frequência

- **Tabletop exercise:** Trimestral (discussão sem execução)
- **Partial drill:** Semestral (teste de componentes específicos)
- **Full drill:** Anual (simulação completa de desastre)
- **Backup restore test:** Mensal (automatizado quando possível)

## Tipos de Cenários

### Cenário 1: Perda de Região Cloud
- Uma região inteira do cloud provider fica indisponível
- Todos os serviços e dados naquela região inacessíveis
- RPO/RTO targets: definidos por criticidade do serviço

### Cenário 2: Ransomware / Comprometimento de Segurança
- Atacante criptografa dados e sistemas
- Backups podem estar comprometidos
- Necessidade de reconstruir do zero

### Cenário 3: Corrupção de Dados
- Bug em produção corrompe dados de clientes
- Necessidade de restaurar dados para ponto anterior
- Identificar scope da corrupção

### Cenário 4: Perda de Pessoas-Chave
- Principal SRE/DBA não está disponível
- Documentação e runbooks são a única referência
- Time secundário precisa executar DR

### Cenário 5: Falha em Cascata
- Um serviço falha e causa efeito dominó
- Circuit breakers e fallbacks testados
- Comunicação de incidente sob pressão

## Processo do Drill

### 2 Semanas Antes: Preparação

**Para Tabletop Exercise:**
- [ ] Selecionar cenário (não revelar detalhes aos participantes)
- [ ] Preparar injects (novos dados durante o exercício para manter tensão)
- [ ] Confirmar participantes (devem incluir on-call, management, comms)
- [ ] Reservar sala/call de 2-3 horas

**Para Partial/Full Drill:**
- [ ] Definir janela de execução (preferencialmente fora de pico)
- [ ] Comunicar stakeholders sobre possível impacto
- [ ] Preparar kill switch para abortar se impacto real
- [ ] Designar observadores (não participam, apenas documentam)
- [ ] Garantir que backups recentes estão verificados

### Durante o Drill

**Tabletop (2-3 horas):**
1. [ ] Facilitador apresenta cenário inicial (15 min)
2. [ ] Time discute resposta (30 min)
3. [ ] Inject 1: nova informação muda o cenário (10 min)
4. [ ] Time ajusta resposta (20 min)
5. [ ] Inject 2: escalação do cenário (10 min)
6. [ ] Time responde à escalação (20 min)
7. [ ] Wrap-up e lições aprendidas (30 min)

**Partial Drill (4-8 horas):**
1. [ ] Anunciar cenário e iniciar timer
2. [ ] Time executa runbook de DR
3. [ ] Observadores documentam cada passo
4. [ ] Medir tempos: detecção, decisão, execução, validação
5. [ ] Validar que serviços funcionam após recovery
6. [ ] Restaurar estado normal

**Full Drill (8-24 horas):**
1. [ ] Simular desastre (failover de região, restore de backup)
2. [ ] Time executa DR completo sem assistência
3. [ ] Testar todos os serviços críticos no ambiente DR
4. [ ] Rodar tráfego real (ou shadow) no ambiente DR
5. [ ] Medir RTO e RPO reais
6. [ ] Failback para ambiente primário

### Após o Drill: Retrospectiva

- [ ] Compilar timeline do que aconteceu
- [ ] Identificar o que funcionou bem
- [ ] Identificar gaps e falhas
- [ ] Para cada gap: root cause, ação corretiva, owner, deadline
- [ ] Atualizar runbooks e documentação
- [ ] Compartilhar learnings com toda a engenharia

## Métricas do Drill

### Tempos
- **Time to Detect (TTD):** Quanto tempo para perceber o problema
- **Time to Decide (TTDec):** Quanto tempo para decidir a ação
- **Time to Execute (TTE):** Quanto tempo para executar o DR
- **Time to Validate (TTV):** Quanto tempo para confirmar que funciona
- **RTO Real:** TTD + TTDec + TTE + TTV
- **RPO Real:** Quanto dado foi perdido na restauração

### Qualidade
- % de serviços restaurados com sucesso
- % de dados restaurados sem corrupção
- Número de passos do runbook que falharam
- Número de decisões que precisaram de escalação

### Comparação
- Melhoria vs drill anterior
- RTO real vs RTO target (SLA)
- RPO real vs RPO target (SLA)

## Classificação de Serviços por Criticidade

| Tier | Definição | RTO Target | RPO Target | Exemplo |
|------|-----------|-----------|-----------|---------|
| 1 | Impacto direto em receita | < 15 min | < 5 min | Pagamentos, checkout |
| 2 | Impacto em operação core | < 1 hora | < 30 min | Dashboard, APIs principais |
| 3 | Impacto em produtividade | < 4 horas | < 1 hora | Ferramentas internas |
| 4 | Impacto mínimo | < 24 horas | < 24 horas | Analytics, reports |

## Checklist de DR Readiness

### Backup e Restauração
- [ ] Backups automatizados para todos os datastores críticos
- [ ] Backups testados (restore funciona e dados estão íntegros)
- [ ] Backups em região diferente do primário
- [ ] Retention policy definida e implementada
- [ ] Processo de restore documentado passo a passo

### Infraestrutura
- [ ] Multi-região configurada para Tier 1-2
- [ ] DNS failover automático ou com procedimento rápido
- [ ] Infrastructure as Code (IaC) permite recriação rápida
- [ ] Secrets e configurações disponíveis em ambiente DR
- [ ] Capacidade computacional reservada ou provisionável

### Documentação
- [ ] Runbook de DR atualizado e acessível offline
- [ ] Diagrama de arquitetura atual e correto
- [ ] Lista de contatos de emergência atualizada
- [ ] Procedimentos de comunicação documentados
- [ ] Dependências externas documentadas com fallbacks

### Comunicação
- [ ] War room virtual configurado (funciona sem infra principal)
- [ ] Template de comunicação para clientes pronto
- [ ] Cadeia de escalação definida
- [ ] Canal de comunicação alternativo se Slack/Teams cair

## Anti-Padrões

1. **"Nosso cloud provider nunca cai"** - Todos caem; prepare-se
2. **Drill avisado com meses de antecedência** - Perde o efeito de teste real
3. **Drill apenas com equipe senior** - Quem está de on-call pode ser junior
4. **Backups nunca testados** - Backup não testado = backup que não existe
5. **Runbook desatualizado** - Pior que não ter runbook
6. **Drill cancelado "porque estamos ocupados"** - Quando mais ocupado, mais precisa

## Referências

- "Release It!" - Michael Nygard (Pragmatic, 2018)
- "Site Reliability Engineering" - Google (O'Reilly, 2016)
- AWS Well-Architected Framework - Reliability Pillar
- "Chaos Engineering" - Casey Rosenthal & Nora Jones
- NIST SP 800-34: Contingency Planning Guide
