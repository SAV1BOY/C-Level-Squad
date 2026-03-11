# CAIO AI Vendor Evaluation

## Propósito
Avaliar vendors de AI com rigor: capability real (não apenas demos), custo total, risco de lock-in e alinhamento estratégico. O mercado de AI está saturado de vendors com promessas infladas — a diferença entre um vendor bom e um ruim pode ser milhões de reais e meses de tempo perdido.

## Quando Aplicar
- Sempre que um novo vendor de AI for considerado para adoção
- Na renovação de contratos existentes com vendors de AI
- Quando performance de vendor atual estiver abaixo do esperado
- Quando novas alternativas de mercado surgirem e precisarem ser avaliadas
- Trimestralmente como revisão do portfolio de vendors de AI

## Agente Responsável
**Agente CAIO (Chief AI Officer Agent)** — responsável por garantir que vendors de AI são selecionados com rigor e geridos com accountability.

## Checklist

### Seção 1: Avaliação de Capability
- [ ] Capabilities do vendor foram testadas com dados e casos reais (não apenas demo)
- [ ] Proof of Concept (PoC) foi realizado com dados próprios da organização
- [ ] Performance do vendor em PoC foi medida contra critérios pré-definidos
- [ ] Limitações do vendor foram identificadas (o que NÃO faz ou faz mal)
- [ ] Escalabilidade da solução foi testada (funciona com volume real, não apenas POC)
- [ ] Qualidade dos modelos/algorithms do vendor foi avaliada por equipe técnica
- [ ] Roadmap do vendor está alinhado com necessidades futuras da organização
- [ ] Referências de clientes similares foram consultadas

### Seção 2: Avaliação de Custo Total
- [ ] Custo de licenciamento/subscription está claro e previsível
- [ ] Custo de implementação e integração está estimado (incluindo tempo do time interno)
- [ ] Custo de compute/API calls está modelado para volume esperado
- [ ] Custos ocultos foram identificados: treinamento, customização, suporte premium
- [ ] Custo de migração futura (switching costs) está estimado
- [ ] TCO para 3 anos foi calculado e comparado com alternativas
- [ ] Modelo de pricing escala de forma previsível e razoável
- [ ] Custo de não-uso (se parar de usar, quanto custa desligar?) está avaliado

### Seção 3: Avaliação de Lock-in
- [ ] Portabilidade de dados está garantida (dados podem ser exportados facilmente)
- [ ] Formato dos dados é aberto e interoperável (não proprietário)
- [ ] Modelos treinados no vendor podem ser portados ou re-treinados internamente
- [ ] APIs seguem padrões abertos ou têm alternativas compatíveis
- [ ] Dependência do vendor para operação diária é minimizada
- [ ] Exit strategy está documentada (o que fazer se precisarmos trocar de vendor)
- [ ] O contrato permite saída sem penalidades excessivas
- [ ] Dados processados pelo vendor pertencem à organização (cláusula contratual)

### Seção 4: Segurança, Privacidade e Compliance
- [ ] Vendor tem certificações relevantes (SOC 2, ISO 27001, ou equivalente)
- [ ] Tratamento de dados do vendor é compliance com LGPD
- [ ] Dados enviados ao vendor são criptografados in transit e at rest
- [ ] Vendor não usa dados da organização para treinar seus próprios modelos (cláusula)
- [ ] Localização dos data centers do vendor é conhecida e aceitável
- [ ] Incident response do vendor está documentado e tem SLAs
- [ ] Pen testing ou security assessment do vendor foi revisado
- [ ] DPA (Data Processing Agreement) está assinado e cobre todos os requisitos

### Seção 5: Viabilidade e Estabilidade do Vendor
- [ ] Estabilidade financeira do vendor foi avaliada (funding, revenue, runway)
- [ ] O vendor não tem risco significativo de shutdown ou aquisição disruptiva
- [ ] SLA de uptime e performance está contratado e verificável
- [ ] Suporte técnico do vendor é responsivo e de qualidade
- [ ] Documentação do vendor é completa, atualizada e útil
- [ ] Comunidade e ecossistema do vendor são ativos e crescentes
- [ ] O vendor tem track record de manter promessas e roadmap
- [ ] Account management do vendor é proativo e estratégico (não apenas reactive)
- [ ] Plano de contingência existe para caso o vendor encerre operações
- [ ] Avaliação do vendor é revisada anualmente com dados de performance real

## Critérios de Aprovação
- PoC realizado com dados reais e resultados dentro dos critérios de sucesso
- TCO para 3 anos calculado e aprovado pelo budget
- Lock-in risk avaliado como baixo ou médio com exit strategy documentada
- Compliance com LGPD e segurança verificada
- Pelo menos 85% dos itens de todas as seções concluídos
- Pelo menos 2 referências de clientes similares consultadas com feedback positivo

## O que Fazer se Falhar
1. Se PoC falhar: descartar vendor e testar próxima alternativa
2. Se custo é proibitivo: negociar, buscar alternativas ou considerar build
3. Se lock-in é alto: exigir cláusulas contratuais de portabilidade ou escolher outro vendor
4. Se compliance é insuficiente: descartar vendor (compliance não é negociável)
5. Se vendor é instável: avaliar risco de continuidade e ter plano B
6. Nunca comprometer com contrato longo sem PoC validado
7. Manter pelo menos 1 alternativa avaliada para cada vendor crítico
8. Re-avaliar vendor em 90 dias após início da operação com dados reais de performance

## Referências
- Vendor Evaluation Scorecard (internal template)
- Gartner Magic Quadrant para a categoria do vendor
- G2, Capterra, TrustRadius reviews (validação de mercado)
- TCO calculation templates (internal)
- DPA template (jurídico)
- "The AI-Powered Organization" — Karim Lakhani
- Vendor management policy (internal)
