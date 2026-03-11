# Checklist de Migração de Dados

## Objetivo
Guiar o processo de migração de dados entre sistemas ou plataformas, garantindo integridade, completude e mínimo impacto no negócio.

---

## 1. Planejamento

### Escopo e Inventário
- [ ] Catalogar todos os bancos e datastores a serem migrados
- [ ] Documentar volume de dados por tabela/coleção
- [ ] Classificar dados por sensibilidade (PII, financeiro, público)
- [ ] Mapear relações e dependências entre entidades de dados
- [ ] Identificar dados obsoletos que podem ser arquivados ou descartados
- [ ] Definir critérios de qualidade de dados aceitáveis
- [ ] Estimar janela de migração necessária por volume

### Mapeamento Origem-Destino
- [ ] Documentar schema de origem para cada fonte de dados
- [ ] Documentar schema de destino na nova plataforma
- [ ] Criar matriz de mapeamento campo-a-campo
- [ ] Identificar transformações necessárias (tipos, formatos, encoding)
- [ ] Documentar regras de negócio para derivação de dados
- [ ] Identificar dados que não têm equivalente no destino
- [ ] Definir valores default para campos novos no destino

### Estratégia de Migração
- [ ] Escolher abordagem: big bang, incremental ou paralela
- [ ] Definir se migração será online (com sistema ativo) ou offline
- [ ] Planejar mecanismo de sincronização se migração incremental
- [ ] Definir ordem de migração baseada em dependências
- [ ] Estabelecer janela de downtime aceitável com o negócio
- [ ] Planejar estratégia de rollback para cada fase
- [ ] Definir critérios de go/no-go para cutover

---

## 2. Preparação Técnica

### Infraestrutura
- [ ] Provisionar ambiente de staging para testes de migração
- [ ] Garantir capacidade de rede entre origem e destino
- [ ] Configurar storage temporário para dados intermediários
- [ ] Provisionar capacidade de processamento para transformação
- [ ] Configurar backup completo da origem antes de iniciar
- [ ] Preparar monitoramento de progresso da migração

### Desenvolvimento de Scripts
- [ ] Desenvolver scripts de extração de dados (idempotentes)
- [ ] Implementar transformações e limpeza de dados
- [ ] Desenvolver scripts de carga no destino (com upsert)
- [ ] Implementar tratamento de erros e retry logic
- [ ] Criar scripts de validação de integridade pós-migração
- [ ] Desenvolver scripts de rollback automatizado
- [ ] Code review de todos os scripts por pelo menos 2 pessoas

### Validação de Scripts
- [ ] Testar scripts com subset pequeno de dados (1%)
- [ ] Testar com dados de borda (nulos, caracteres especiais, unicode)
- [ ] Testar com volume representativo (10-20% da produção)
- [ ] Validar performance: tempo estimado para volume completo
- [ ] Testar scripts de rollback end-to-end
- [ ] Documentar dependências e pré-requisitos de execução

---

## 3. Qualidade de Dados

### Profiling de Dados
- [ ] Executar profiling na base de origem (completude, distribuição)
- [ ] Identificar dados duplicados e definir estratégia de dedup
- [ ] Identificar valores inconsistentes e regras de limpeza
- [ ] Documentar dados com formato não-padrão
- [ ] Mapear referências órfãs entre tabelas
- [ ] Avaliar encoding de caracteres (UTF-8, Latin1, etc.)

### Regras de Limpeza
- [ ] Definir regras de tratamento para dados inválidos
- [ ] Criar lookup tables para padronização de valores
- [ ] Definir tratamento para registros duplicados
- [ ] Estabelecer regras para dados nulos ou vazios
- [ ] Documentar exceções e tratamentos especiais
- [ ] Criar log de decisões sobre dados problemáticos

---

## 4. Execução

### Pre-flight Checks
- [ ] Backup completo da origem verificado e testado
- [ ] Backup completo do destino (se já contém dados)
- [ ] Confirmar janela de migração com todos os stakeholders
- [ ] Verificar que scripts foram atualizados após último teste
- [ ] Confirmar acessos e permissões em todos os sistemas
- [ ] Notificar equipes sobre início da migração
- [ ] Desabilitar jobs e processos que possam interferir

### Execução da Migração
- [ ] Executar scripts na ordem documentada de dependências
- [ ] Monitorar progresso em tempo real (registros/segundo, erros)
- [ ] Registrar início e fim de cada fase da migração
- [ ] Pausar e investigar se taxa de erro exceder threshold
- [ ] Salvar logs completos de execução para auditoria
- [ ] Comunicar progresso a cada milestone significativo

### Validação Pós-Migração
- [ ] Contar registros: origem vs destino por tabela/entidade
- [ ] Validar somas de controle (checksums) para dados numéricos
- [ ] Verificar integridade referencial entre tabelas relacionadas
- [ ] Executar queries de amostragem para validação visual
- [ ] Testar funcionalidades da aplicação com dados migrados
- [ ] Validar dados sensíveis mantêm criptografia/mascaramento
- [ ] Verificar que dados obsoletos não foram migrados
- [ ] Validar datas, timestamps e fusos horários

---

## 5. Cutover e Pós-Migração

### Cutover
- [ ] Executar sincronização final (delta) desde último snapshot
- [ ] Validar delta migrado com mesmos controles de qualidade
- [ ] Redirecionar aplicações para nova fonte de dados
- [ ] Verificar que aplicações funcionam corretamente com novos dados
- [ ] Executar smoke tests em funcionalidades críticas
- [ ] Monitorar logs de erro da aplicação nas primeiras horas

### Pós-Migração
- [ ] Manter base de origem em read-only por 30 dias (safety net)
- [ ] Monitorar performance de queries na nova base
- [ ] Verificar que jobs e processos batch funcionam normalmente
- [ ] Coletar feedback de usuários sobre dados migrados
- [ ] Documentar issues encontrados e correções aplicadas
- [ ] Após período de estabilização, definir data para descomissionar origem

### Documentação Final
- [ ] Relatório de migração com volumes, tempos e issues
- [ ] Mapeamento final de dados documentado
- [ ] Regras de transformação registradas para referência
- [ ] Lições aprendidas e recomendações para futuras migrações
- [ ] Atualizar documentação de arquitetura de dados
- [ ] Atualizar catálogo de dados com novos schemas
