# 04. Construção e Engenharia de Prompt

Este documento apresenta a estrutura e as decisões adotadas na construção do **System Prompt** do agente **Chegô**, assistente virtual da plataforma fictícia **Chegaê**.

O desenvolvimento utilizou técnicas de Engenharia de Prompt para definir a identidade do agente, seu contexto de atuação, suas responsabilidades, o comportamento esperado e os limites durante o atendimento.

---

## 🏗️ Metodologia de Construção

A construção do prompt foi organizada em seções específicas, permitindo separar as instruções de identidade, contexto, comportamento e segurança.

A estrutura considera os seguintes elementos:

```text
┌────────────────────────────────────────┐
│ 1. Identidade e Contexto               │
├────────────────────────────────────────┤
│ 2. Público Atendido                    │
├────────────────────────────────────────┤
│ 3. Escopo de Atuação                   │
├────────────────────────────────────────┤
│ 4. Integração com a Plataforma         │
├────────────────────────────────────────┤
│ 5. Objetivo do Atendimento             │
├────────────────────────────────────────┤
│ 6. Tom de Voz e Formato das Respostas  │
├────────────────────────────────────────┤
│ 7. Regras e Segurança                  │
├────────────────────────────────────────┤
│ 8. Encaminhamento para Atendimento     │
│    Humano                              │
└────────────────────────────────────────┘
```

---

## 🔍 Estrutura do System Prompt

O prompt utilizado no projeto está disponível em [`prompts/agente-atendimento-chegae.md`](../prompts/agente-atendimento-chegae.md) e foi estruturado nas seguintes seções:

1. **Identidade e Contexto**<br>
Identificação como agente **Chegô** agente virtual de atendimento da **Chegaê**, estabelecendo o contexto da plataforma fictícia e seu segmento de atuação.

2. **Público Atendido**<br>
Identifica os consumidores que utilizam a plataforma e podem precisar de suporte durante ou após uma compra.

3. **Escopo de Atuação**<br>
Define os assuntos que fazem parte do atendimento, incluindo:
- Consultas e acompanhamento de pedidos.
- Problemas relacionados à entrega.
- Pagamentos e reembolsos.
- Cancelamentos.
- Dúvidas sobre a plataforma.
  
4. **Integração com a Plataforma**<br>
Estabelece o contexto de atuação do agente como integrado aos sistemas da Chegaê, com acesso aos recursos necessários para consultar pedidos, verificar informações e registrar ou encaminhar solicitações.
As instruções determinam que o agente utilize os dados e as confirmações retornados pelos sistemas, sem simular consultas ou operações.

5. **Objetivo do Atendimento**<br>
Orienta o agente a oferecer um atendimento rápido, cordial e eficiente, identificando a necessidade do consumidor e apresentando orientações adequadas.

6. **Tom de Voz e Formato das Respostas**<br>
Define o padrão de comunicação do Chegô:
- Linguagem simples, cordial e profissional.
- Respostas objetivas, com limite de cinco linhas.
- Listas numeradas para orientações com várias etapas.
- Demonstração de empatia diante de problemas relatados.
- Pergunta de encerramento para verificar se o consumidor precisa de mais ajuda, exceto quando houver uma solicitação pendente.

7. **Regras e Segurança**<br>
Estabelece limites para evitar respostas incorretas e proteger os consumidores. Entre as instruções estão:
- Não solicitar senhas, códigos de autenticação ou dados financeiros sensíveis.
- Não inventar valores, taxas, prazos, protocolos ou políticas.
- Não confirmar cancelamentos ou reembolsos sem confirmação do sistema.
- Não atribuir responsabilidades sem evidências.
- Não prometer soluções que dependam de outras áreas.
- Diferenciar orientações de operações efetivamente realizadas.reincidência, pedido explícito do cliente).
  
8. **Encaminhamento para Atendimento Humano**<br>
Define as situações em que o agente deve reconhecer seus limites e indicar atendimento humano, como suspeitas de fraude, cobranças contestadas, problemas recorrentes e solicitações explícitas do consumidor. Também estabelece que o agente não deve afirmar que o encaminhamento foi realizado sem a confirmação correspondente.

---

## 🧠 Decisões de Engenharia de Prompt

Durante a construção do System Prompt, foram adotadas decisões para organizar e controlar o comportamento do agente:
- Separação das instruções: identidade, escopo, comportamento e regras foram organizados em seções próprias.
- Definição de limites: foram estabelecidas situações em que o agente não deve presumir informações ou prometer ações.
- Contexto de integração: o agente foi configurado para atuar considerando acesso aos sistemas da empresa fictícia.
- Padronização da comunicação: foram definidas orientações de linguagem, objetividade e formato das respostas.
- Segurança no atendimento: foram estabelecidas restrições para proteger informações pessoais e financeiras.
- Encaminhamento humano: foram definidos critérios para reconhecer situações que ultrapassam o escopo do agente.

---

## 🧪 Ambiente de Experimentação

O System Prompt foi configurado e experimentado no ChatGPT por meio de simulações manuais de atendimento.

As situações utilizadas para observar o comportamento do agente incluem:
- Atrasos na entrega.
- Solicitações de reembolso.
- Cobranças não reconhecidas.
As simulações permitiram observar as respostas produzidas pelo agente diante de diferentes solicitações, considerando as instruções e os limites estabelecidos no prompt.

**Limitação técnica:** o contexto de integração com os sistemas da Chegaê faz parte das instruções do agente. Não foi desenvolvida uma conexão real com APIs, bancos de dados ou sistemas externos.
