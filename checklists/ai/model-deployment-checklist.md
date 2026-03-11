# Checklist de Deploy de Modelo AI

> Checklist completo para garantir que o deploy de modelos de inteligência artificial
> seja executado com segurança, rastreabilidade e qualidade.

---

## 1. Preparação Pré-Deploy

- [ ] Modelo treinado e validado em ambiente de staging
- [ ] Métricas de performance documentadas (accuracy, precision, recall, F1)
- [ ] Threshold de confiança definido e aprovado pelo time de dados
- [ ] Dataset de validação separado do dataset de treino
- [ ] Teste de regressão executado contra versão anterior do modelo
- [ ] Análise de drift de dados realizada (comparação treino vs. produção)
- [ ] Documentação do modelo atualizada (Model Card)
- [ ] Revisão de código do pipeline de inferência concluída
- [ ] Dependências e versões de bibliotecas travadas (pinned)
- [ ] Licenças de todas as dependências verificadas

## 2. Infraestrutura e Ambiente

- [ ] Ambiente de produção provisionado e testado
- [ ] Recursos computacionais dimensionados (CPU/GPU/memória)
- [ ] Auto-scaling configurado com limites mínimos e máximos
- [ ] Health checks configurados no load balancer
- [ ] Timeout de inferência definido (recomendado: < 500ms para real-time)
- [ ] Rate limiting implementado para proteger o serviço
- [ ] Certificados SSL/TLS configurados para endpoints
- [ ] Variáveis de ambiente configuradas (sem segredos hardcoded)
- [ ] Container image escaneada para vulnerabilidades
- [ ] Rede e firewall rules configuradas corretamente

## 3. Monitoramento e Observabilidade

- [ ] Logging estruturado implementado (JSON format)
- [ ] Métricas de latência de inferência sendo coletadas
- [ ] Métricas de throughput (requests/segundo) configuradas
- [ ] Alertas configurados para degradação de performance
- [ ] Dashboard de monitoramento criado e acessível ao time
- [ ] Rastreamento de predições para auditoria habilitado
- [ ] Monitoramento de drift de dados em produção ativo
- [ ] Alerta para taxa de erro acima do threshold (recomendado: > 1%)
- [ ] Logs de input/output armazenados para debugging
- [ ] Métricas de negócio conectadas às predições do modelo

## 4. Testes em Produção

- [ ] Canary deployment configurado (recomendado: 5% do tráfego inicial)
- [ ] Testes A/B definidos com métricas de sucesso claras
- [ ] Shadow mode testado (modelo novo rodando em paralelo sem impacto)
- [ ] Teste de carga executado simulando pico de tráfego
- [ ] Teste de falha (chaos testing) realizado
- [ ] Validação de respostas do modelo com dados reais de produção
- [ ] Verificação de consistência entre ambientes (staging vs. produção)

## 5. Rollback e Contingência

- [ ] Plano de rollback documentado e testado
- [ ] Versão anterior do modelo disponível para rollback imediato
- [ ] Critérios de rollback automático definidos
- [ ] Feature flag implementada para desligar o modelo rapidamente
- [ ] Procedimento de rollback praticado pelo time de operações
- [ ] Comunicação de rollback preparada para stakeholders
- [ ] SLA de tempo de rollback definido (recomendado: < 5 minutos)

## 6. Compliance e Governança

- [ ] Aprovação do Data Protection Officer (DPO) obtida
- [ ] Avaliação de impacto de privacidade (DPIA) concluída
- [ ] Conformidade com LGPD verificada para dados de entrada
- [ ] Registro no inventário de modelos AI da organização
- [ ] Responsável pelo modelo (Model Owner) designado
- [ ] Frequência de re-treino definida e agendada
- [ ] Política de retenção de dados de inferência documentada
- [ ] Auditabilidade das decisões do modelo garantida

## 7. Documentação e Comunicação

- [ ] Model Card publicada no repositório central
- [ ] README do serviço atualizado com instruções de operação
- [ ] Runbook de operações criado para o time de plantão
- [ ] Changelog atualizado com detalhes da nova versão
- [ ] Stakeholders notificados sobre o deploy
- [ ] Treinamento do time de suporte realizado
- [ ] API documentation atualizada (Swagger/OpenAPI)
- [ ] SLA do serviço documentado e comunicado

## 8. Pós-Deploy (Primeiras 72 horas)

- [ ] Monitorar métricas de performance a cada hora nas primeiras 24h
- [ ] Verificar ausência de anomalias nos logs de erro
- [ ] Confirmar que métricas de negócio estão dentro do esperado
- [ ] Coletar feedback inicial dos usuários ou sistemas consumidores
- [ ] Documentar lições aprendidas do processo de deploy
- [ ] Agendar review de performance para 7 e 30 dias após deploy
- [ ] Confirmar que pipeline de re-treino está funcional
- [ ] Fechar tickets relacionados ao deploy

---

## Critérios de Go/No-Go

| Critério | Threshold Mínimo |
|----------|-----------------|
| Accuracy em validação | >= versão anterior |
| Latência p99 | < 500ms |
| Taxa de erro | < 1% |
| Cobertura de testes | > 80% |
| Vulnerabilidades críticas | 0 |
| Aprovações necessárias | Tech Lead + Model Owner |

---

*Última atualização: Março 2026*
*Responsável: CAIO Architect*
