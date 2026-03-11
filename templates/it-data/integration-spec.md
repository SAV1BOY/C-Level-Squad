# Especificação de Integração

## Propósito
Documentar os requisitos técnicos e de negócio para integrações entre sistemas,
definindo fluxo de dados, protocolo, SLA, tratamento de erros e plano de testes,
servindo como contrato entre equipes e sistemas.

## Quando Usar
- Para qualquer nova integração entre sistemas internos ou com terceiros
- Ao redesenhar integrações existentes
- Para documentar APIs e contratos de dados
- Como referência para troubleshooting e manutenção

## Agente Responsável
- **Autor primário:** CTO Agent ou CIO Agent
- **Contribuidores:** Tech Leads dos sistemas envolvidos
- **Revisor:** CISO Agent (segurança), Owner de negócio
- **Aprovador:** CTO Agent

## Template

---

### ESPECIFICAÇÃO DE INTEGRAÇÃO

**Nome da integração:** {{nome_integracao}}
**ID:** {{id_integracao}}
**Data:** {{data}}
**Autor:** {{autor}}
**Status:** {{rascunho_em_revisao_aprovado_implementado}}
**Versão:** {{versao}}

---

#### 1. Visão Geral

**Objetivo de negócio:**
{{objetivo_negocio}}

**Sistemas envolvidos:**
| Sistema | Papel | Owner | Versão |
|---------|-------|-------|--------|
| {{sistema_origem}} | Origem (Producer) | {{owner_origem}} | {{versao_origem}} |
| {{sistema_destino}} | Destino (Consumer) | {{owner_destino}} | {{versao_destino}} |

**Fluxo resumido:**
```
{{sistema_origem}} → [{{metodo_transporte}}] → {{sistema_destino}}
```

---

#### 2. Requisitos de Negócio

| # | Requisito | Prioridade | Critério de Aceite |
|---|----------|-----------|-------------------|
| R1 | {{req_1}} | {{prior_1}} | {{criterio_1}} |
| R2 | {{req_2}} | {{prior_2}} | {{criterio_2}} |
| R3 | {{req_3}} | {{prior_3}} | {{criterio_3}} |

---

#### 3. Especificação Técnica

**Protocolo:** {{rest_graphql_grpc_webhook_sftp_mq}}
**Formato de dados:** {{json_xml_csv_protobuf}}
**Autenticação:** {{oauth2_apikey_mtls_basic}}
**Direção:** {{unidirecional_bidirecional}}
**Padrão:** {{sync_async_batch_streaming}}

**Endpoint(s):**
| Método | Endpoint | Descrição |
|--------|----------|-----------|
| {{metodo_1}} | {{endpoint_1}} | {{desc_1}} |
| {{metodo_2}} | {{endpoint_2}} | {{desc_2}} |

---

#### 4. Modelo de Dados

**Payload de request:**
```json
{
  "{{campo_1}}": "{{tipo_1}} — {{descricao_campo_1}}",
  "{{campo_2}}": "{{tipo_2}} — {{descricao_campo_2}}",
  "{{campo_3}}": "{{tipo_3}} — {{descricao_campo_3}}",
  "{{campo_4}}": "{{tipo_4}} — {{descricao_campo_4}}"
}
```

**Payload de response:**
```json
{
  "{{resp_campo_1}}": "{{resp_tipo_1}} — {{resp_desc_1}}",
  "{{resp_campo_2}}": "{{resp_tipo_2}} — {{resp_desc_2}}",
  "{{resp_campo_3}}": "{{resp_tipo_3}} — {{resp_desc_3}}"
}
```

**Mapeamento de campos:**
| Campo Origem | Campo Destino | Transformação | Obrigatório |
|-------------|-------------|--------------|-------------|
| {{orig_1}} | {{dest_1}} | {{transf_1}} | {{obrig_1}} |
| {{orig_2}} | {{dest_2}} | {{transf_2}} | {{obrig_2}} |
| {{orig_3}} | {{dest_3}} | {{transf_3}} | {{obrig_3}} |

---

#### 5. SLA e Performance

| Métrica | Target | Monitoramento |
|---------|--------|--------------|
| Disponibilidade | {{sla_disponibilidade}} | {{monitor_disp}} |
| Latência máxima | {{latencia_max}} | {{monitor_lat}} |
| Throughput mínimo | {{throughput_min}} | {{monitor_throughput}} |
| Taxa de erro máxima | {{erro_max}} | {{monitor_erro}} |
| Janela de manutenção | {{janela_manutencao}} | — |

---

#### 6. Tratamento de Erros

| Cenário | Código/Tipo | Ação | Retry? | Alerta |
|---------|------------|------|--------|--------|
| {{cenario_1}} | {{codigo_1}} | {{acao_1}} | {{retry_1}} | {{alerta_1}} |
| {{cenario_2}} | {{codigo_2}} | {{acao_2}} | {{retry_2}} | {{alerta_2}} |
| {{cenario_3}} | {{codigo_3}} | {{acao_3}} | {{retry_3}} | {{alerta_3}} |
| {{cenario_4}} | {{codigo_4}} | {{acao_4}} | {{retry_4}} | {{alerta_4}} |

**Política de retry:** {{politica_retry}}
**Dead letter queue:** {{dlq_config}}
**Circuit breaker:** {{circuit_breaker_config}}

---

#### 7. Segurança

| Aspecto | Implementação |
|---------|-------------|
| Autenticação | {{detalhe_autenticacao}} |
| Autorização | {{detalhe_autorizacao}} |
| Criptografia em trânsito | {{criptografia_transito}} |
| Criptografia em repouso | {{criptografia_repouso}} |
| Rate limiting | {{rate_limiting}} |
| IP allowlisting | {{ip_allowlist}} |
| Logging/Auditoria | {{logging}} |
| PII/Dados sensíveis | {{pii_handling}} |

---

#### 8. Plano de Testes

| Tipo de Teste | Escopo | Ferramenta | Responsável | Status |
|--------------|--------|-----------|-------------|--------|
| Unit tests | {{escopo_unit}} | {{tool_unit}} | {{resp_unit}} | {{status_unit}} |
| Integration tests | {{escopo_int}} | {{tool_int}} | {{resp_int}} | {{status_int}} |
| Load tests | {{escopo_load}} | {{tool_load}} | {{resp_load}} | {{status_load}} |
| Security tests | {{escopo_sec}} | {{tool_sec}} | {{resp_sec}} | {{status_sec}} |
| E2E tests | {{escopo_e2e}} | {{tool_e2e}} | {{resp_e2e}} | {{status_e2e}} |

---

#### 9. Plano de Rollout

| Fase | Descrição | Timeline | Critério de Passagem |
|------|----------|----------|---------------------|
| 1 | {{fase_1}} | {{timeline_1}} | {{criterio_fase_1}} |
| 2 | {{fase_2}} | {{timeline_2}} | {{criterio_fase_2}} |
| 3 | {{fase_3}} | {{timeline_3}} | {{criterio_fase_3}} |

**Rollback plan:** {{plano_rollback}}

---

## Instruções de Preenchimento

1. **Modelo de dados:** Documente todos os campos, tipos e validações. O contrato de dados é o cerne.
2. **SLA:** Defina antes de implementar. Construa monitoramento junto com a integração.
3. **Erros:** Pense em todos os cenários de falha. Retry com backoff exponencial é padrão.
4. **Segurança:** CISO Agent deve revisar antes da implementação. Nunca exponha credenciais.
5. **Testes:** Load test antes de ir para produção. A integração deve suportar 3x o pico esperado.
6. **Versionamento:** Use versionamento semântico na API. Breaking changes = nova major version.

## Exemplo Preenchido

---

### Integração: Stripe → Data Warehouse (pagamentos)

**Protocolo:** Webhook (Stripe → API interna) + Batch (API → BigQuery)
**Formato:** JSON
**Autenticação:** Webhook signature verification + OAuth2

#### 5. SLA
| Métrica | Target |
|---------|--------|
| Disponibilidade | 99.95% |
| Latência máxima (webhook processing) | < 5 segundos |
| Throughput | 500 eventos/minuto |

---

## Checklist de Qualidade

- [ ] Objetivo de negócio está claro
- [ ] Modelo de dados está completo com tipos e validações
- [ ] SLA definido e monitoramento configurado
- [ ] Tratamento de erros cobre cenários principais
- [ ] Política de retry e circuit breaker definidas
- [ ] Segurança revisada pelo CISO Agent
- [ ] Plano de testes cobre unit, integration, load e security
- [ ] Rollback plan documentado
- [ ] Versionamento da API definido
- [ ] Documentação acessível para ambas as equipes
