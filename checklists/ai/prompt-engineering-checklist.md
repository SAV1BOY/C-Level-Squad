# Checklist de Prompt Engineering

> Checklist para criar, otimizar e manter prompts de alta qualidade para sistemas
> de IA generativa, garantindo consistência, segurança e eficácia.

---

## 1. Design do Prompt

### 1.1 Estrutura Básica
- [ ] Objetivo do prompt claramente definido em uma frase
- [ ] Persona/role do modelo definida (ex: "Você é um analista financeiro senior")
- [ ] Contexto relevante fornecido sem excesso de informação
- [ ] Instrução principal clara e sem ambiguidade
- [ ] Formato de saída esperado especificado (JSON, markdown, lista, etc.)
- [ ] Exemplos (few-shot) incluídos quando necessário
- [ ] Restrições e limitações explicitadas
- [ ] Tom e estilo de linguagem definidos

### 1.2 Técnicas Avançadas
- [ ] Chain-of-thought prompting aplicado para raciocínio complexo
- [ ] Step-by-step instructions para tarefas multi-etapa
- [ ] Delimitadores claros para separar seções (```, ---, XML tags)
- [ ] Variáveis de template marcadas e documentadas ({nome_variavel})
- [ ] System prompt separado do user prompt quando aplicável
- [ ] Instruções de fallback para cenários inesperados
- [ ] Prompt negativo incluído ("NÃO faça X, Y, Z")
- [ ] Self-consistency check instruído ("Revise sua resposta antes de enviar")

## 2. Qualidade e Consistência

- [ ] Prompt testado com pelo menos 20 inputs variados
- [ ] Resultados avaliados por pelo menos 2 pessoas do time
- [ ] Taxa de acerto medida contra golden dataset
- [ ] Consistência de output verificada (mesmo input = output similar)
- [ ] Edge cases testados (inputs vazios, muito longos, em outro idioma)
- [ ] Robustez a variações de formulação testada
- [ ] Qualidade do output em português brasileiro verificada
- [ ] Alucinações documentadas e mitigadas
- [ ] Grounding implementado quando dados factuais são necessários
- [ ] Temperatura e top-p otimizados para o caso de uso

## 3. Segurança e Guardrails

- [ ] Prompt injection testado e mitigado
- [ ] Jailbreak attempts testados e bloqueados
- [ ] Conteúdo sensível/tóxico filtrado na saída
- [ ] PII handling definido (mascarar, não incluir, etc.)
- [ ] Output validation implementada (schema, regex, etc.)
- [ ] Rate limiting configurado para prevenir abuso
- [ ] Logging de prompts sensíveis desabilitado ou anonimizado
- [ ] Escalation path definido para outputs problemáticos
- [ ] Content moderation layer implementada
- [ ] Limites de tamanho de input/output definidos

## 4. Otimização de Performance

### 4.1 Custo
- [ ] Token count do prompt monitorado e otimizado
- [ ] Informações redundantes removidas do contexto
- [ ] Modelo adequado selecionado (não usar o maior para tudo)
- [ ] Caching implementado para prompts frequentes com mesma resposta
- [ ] Batch processing utilizado quando latência não é crítica
- [ ] Custo por chamada calculado e dentro do budget
- [ ] Compressão de contexto aplicada quando possível

### 4.2 Latência
- [ ] Streaming habilitado para respostas longas
- [ ] Max tokens definido para evitar respostas excessivamente longas
- [ ] Prompt otimizado para respostas concisas quando apropriado
- [ ] Paralelização de chamadas implementada quando possível
- [ ] Fallback para modelo mais rápido em caso de timeout

## 5. Versionamento e Gestão

- [ ] Prompts versionados no controle de versão (Git)
- [ ] Changelog mantido para cada prompt
- [ ] Nomenclatura padronizada para prompts (ex: domain-task-version)
- [ ] Metadados documentados (autor, data, modelo alvo, versão)
- [ ] A/B testing framework configurado para comparar versões
- [ ] Prompt registry centralizado e acessível ao time
- [ ] Processo de review para mudanças em prompts de produção
- [ ] Rollback rápido para versão anterior disponível
- [ ] Templates base definidos para casos de uso comuns
- [ ] Library de prompts reutilizáveis mantida

## 6. Avaliação e Métricas

- [ ] Métricas de avaliação definidas para o caso de uso
  - [ ] Relevância (a resposta atende ao pedido?)
  - [ ] Completude (todos os pontos foram cobertos?)
  - [ ] Acurácia (informações factualmente corretas?)
  - [ ] Formato (output no formato especificado?)
  - [ ] Tom (linguagem adequada ao contexto?)
- [ ] Avaliação automática implementada (quando possível)
- [ ] Avaliação humana periódica agendada
- [ ] Benchmark dataset criado e mantido
- [ ] Relatório de qualidade gerado mensalmente
- [ ] Comparação entre modelos documentada
- [ ] Feedback de usuários coletado e incorporado

## 7. Manutenção Contínua

- [ ] Monitoramento de qualidade em produção ativo
- [ ] Drift de performance detectado e alertado
- [ ] Atualização programada conforme novos modelos são lançados
- [ ] Compatibilidade testada ao migrar entre modelos
- [ ] Documentação de lições aprendidas mantida
- [ ] Treinamento do time sobre melhores práticas realizado
- [ ] Review trimestral de todos os prompts em produção
- [ ] Deprecated prompts removidos do registro

---

## Template Base de Prompt

```
[SYSTEM]
Você é {persona}. Seu objetivo é {objetivo}.

Regras:
1. {regra_1}
2. {regra_2}
3. {regra_3}

Formato de resposta: {formato}

[USER]
Contexto: {contexto}

Tarefa: {tarefa}

Dados de entrada:
{dados}

[EXEMPLOS]
Input: {exemplo_input_1}
Output: {exemplo_output_1}

Input: {exemplo_input_2}
Output: {exemplo_output_2}
```

---

## Métricas de Referência

| Métrica | Target |
|---------|--------|
| Taxa de output válido (formato correto) | > 95% |
| Taxa de relevância (avaliação humana) | > 90% |
| Taxa de alucinação | < 5% |
| Custo médio por chamada | Dentro do budget |
| Latência p95 | < SLA definido |

---

*Última atualização: Março 2026*
*Responsável: CAIO Architect*
