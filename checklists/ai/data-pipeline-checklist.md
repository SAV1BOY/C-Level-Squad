# Checklist de Pipeline de Dados

> Checklist para construção, validação e manutenção de pipelines de dados
> robustos e confiáveis para alimentar sistemas de AI e analytics.

---

## 1. Design e Arquitetura do Pipeline

- [ ] Fontes de dados identificadas e documentadas
- [ ] Esquema de dados de entrada definido e versionado
- [ ] Esquema de dados de saída definido e versionado
- [ ] Frequência de execução definida (batch, micro-batch, streaming)
- [ ] SLA de latência de dados definido com stakeholders
- [ ] Diagrama de arquitetura do pipeline criado
- [ ] Dependências entre pipelines mapeadas (DAG)
- [ ] Volume esperado de dados estimado (GB/dia, registros/hora)
- [ ] Estratégia de particionamento definida (por data, região, etc.)
- [ ] Formato de armazenamento escolhido (Parquet, Avro, Delta, etc.)

## 2. Ingestão de Dados

- [ ] Conectores de fonte configurados e testados
- [ ] Autenticação para fontes de dados configurada via secrets manager
- [ ] Tratamento de dados incrementais implementado (CDC ou timestamp)
- [ ] Mecanismo de retry com backoff exponencial configurado
- [ ] Dead letter queue configurada para registros com falha
- [ ] Rate limiting respeitado nas APIs de origem
- [ ] Compressão de dados habilitada na transferência
- [ ] Validação de schema na ingestão (schema enforcement)
- [ ] Deduplicação de registros implementada
- [ ] Watermark para dados atrasados configurado (streaming)

## 3. Transformação e Processamento

- [ ] Lógica de transformação documentada em linguagem de negócio
- [ ] Regras de limpeza de dados definidas e implementadas
- [ ] Tratamento de valores nulos documentado (drop, fill, flag)
- [ ] Normalização e padronização de campos aplicada
- [ ] Joins entre datasets validados (sem duplicação ou perda)
- [ ] Agregações verificadas com cálculos manuais de amostra
- [ ] Tratamento de timezone consistente (recomendado: UTC)
- [ ] Encoding de caracteres padronizado (UTF-8)
- [ ] Feature engineering documentado com justificativa
- [ ] Transformações idempotentes (re-execução segura)

## 4. Qualidade de Dados

- [ ] Testes de completude implementados (% de nulos por coluna)
- [ ] Testes de unicidade para chaves primárias
- [ ] Testes de integridade referencial entre tabelas
- [ ] Testes de range para valores numéricos
- [ ] Testes de formato para strings (email, CPF, telefone)
- [ ] Testes de freshness (dados não mais antigos que X horas)
- [ ] Testes de volume (variação > 20% gera alerta)
- [ ] Testes de distribuição estatística para colunas críticas
- [ ] Framework de data quality integrado (dbt tests, Great Expectations)
- [ ] Relatório de qualidade gerado automaticamente a cada execução

## 5. Orquestração e Agendamento

- [ ] Orquestrador configurado (Airflow, Prefect, Dagster)
- [ ] DAG de dependências definido corretamente
- [ ] Agendamento (schedule) configurado com timezone
- [ ] Política de retry definida (tentativas, intervalo)
- [ ] Timeout por tarefa configurado
- [ ] Concorrência máxima definida para evitar sobrecarga
- [ ] Sensor de disponibilidade de dados upstream configurado
- [ ] Notificações de falha configuradas (Slack, email, PagerDuty)
- [ ] Backfill strategy documentada e testada
- [ ] SLA monitoring ativo no orquestrador

## 6. Segurança e Compliance

- [ ] Dados sensíveis identificados e classificados
- [ ] Mascaramento ou anonimização aplicado em PII
- [ ] Criptografia at-rest habilitada no armazenamento
- [ ] Criptografia in-transit habilitada (TLS)
- [ ] Controle de acesso baseado em roles (RBAC) configurado
- [ ] Logs de acesso a dados habilitados
- [ ] Política de retenção de dados implementada
- [ ] Conformidade com LGPD verificada
- [ ] Data lineage rastreável de ponta a ponta
- [ ] Consentimento de uso verificado para dados pessoais

## 7. Performance e Escalabilidade

- [ ] Benchmark de performance executado com volume realista
- [ ] Particionamento otimizado para queries frequentes
- [ ] Índices criados para colunas de filtro comum
- [ ] Compactação de small files configurada
- [ ] Auto-scaling de workers configurado
- [ ] Custos de processamento estimados e dentro do budget
- [ ] Otimização de shuffle em processamento distribuído
- [ ] Cache implementado para dados de referência estáticos
- [ ] Monitoramento de uso de recursos (CPU, memória, I/O)

## 8. Monitoramento e Alertas

- [ ] Dashboard de status do pipeline criado
- [ ] Métricas de duração de execução coletadas
- [ ] Métricas de volume de dados processados coletadas
- [ ] Alertas para falha de execução configurados
- [ ] Alertas para SLA breach configurados
- [ ] Alertas para anomalia de volume configurados
- [ ] Log centralizado com busca (ELK, CloudWatch, Datadog)
- [ ] Runbook de troubleshooting documentado
- [ ] Escalation path definido para falhas críticas

## 9. Documentação e Governança

- [ ] Catálogo de dados atualizado com novos datasets
- [ ] Data dictionary publicado para consumidores
- [ ] Owner do pipeline designado
- [ ] SLA documentado e comunicado
- [ ] Processo de change management definido
- [ ] Versionamento do código do pipeline no Git
- [ ] Code review obrigatório para mudanças
- [ ] Testes automatizados no CI/CD

---

## Métricas de Saúde do Pipeline

| Métrica | Target |
|---------|--------|
| Taxa de sucesso de execução | > 99% |
| Latência de dados (freshness) | < SLA definido |
| Cobertura de testes de qualidade | > 90% das tabelas |
| Tempo médio de recuperação (MTTR) | < 30 minutos |
| Custo por GB processado | Dentro do budget |

---

*Última atualização: Março 2026*
*Responsável: CAIO Architect / CIO Engineer*
