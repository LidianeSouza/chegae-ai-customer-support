# 01. Visão Geral do Projeto — Chegô | Chegaê

## 🎯 Introdução

O projeto consiste no desenvolvimento do **Chegô**, um agente virtual de atendimento ao cliente com Inteligência Artificial Generativa, criado para a **Chegaê**, uma plataforma fictícia de delivery e conveniência.

O objetivo é explorar como a Engenharia de Prompt pode orientar um modelo de linguagem a realizar atendimentos mais claros, empáticos e seguros, considerando diferentes situações enfrentadas pelos consumidores.

O desenvolvimento foi realizado por meio da construção de um **System Prompt**, com definição de identidade, escopo de atuação, tom de voz, regras de atendimento e limites de segurança.

---

## 🛵 Sobre a Plataforma Chegaê

A Chegaê é uma empresa fictícia criada como contexto para o desenvolvimento e a experimentação do agente.

- **Segmento:** Delivery de refeições, alimentos, conveniência, farmácia e varejo.
- **Agente virtual:** Chegô.
- **Slogan:** Precisou? Chegaê!

---

## 🚩 Problemas Identificados no Atendimento Tradicional

1. **Longas filas de espera:** Clientes aguardando atendimento humano para resolver dúvidas frequentes, como o status de um pedido.
2. **Respostas pouco contextualizadas:** Chatbots baseados em fluxos rígidos podem apresentar dificuldades para compreender diferentes situações e necessidades.
3. **Respostas incorretas de IAs generativas:** Modelos de linguagem sem instruções adequadas podem inventar prazos, valores de reembolso ou informações sobre pedidos.
4. **Riscos à segurança dos dados:** Possibilidade de solicitar ou expor informações pessoais e financeiras durante o atendimento.

---

## 💡 Solução Desenvolvida

Foi desenvolvido o **Chegô**, um agente de atendimento orientado por Engenharia de Prompt.

O System Prompt estabelece instruções para que o agente atue como se estivesse integrado aos sistemas da Chegaê, podendo consultar informações de pedidos, verificar dados e orientar solicitações dos consumidores.

A configuração também define:

- Identidade e contexto da plataforma.
- Público atendido e escopo de atuação.
- Tom de voz e formato das respostas.
- Regras de negócio e segurança.
- Limites de atuação e encaminhamento para atendimento humano.

---

## ⚙️ Escopo do Protótipo

O agente foi configurado e experimentado no ChatGPT por meio de simulações manuais de atendimento.

As situações trabalhadas incluem:

- Atrasos na entrega.
- Solicitações de reembolso.
- Cobranças não reconhecidas.

O projeto demonstra a aplicação prática de Engenharia de Prompt na definição do comportamento de um agente conversacional, considerando um cenário de atendimento integrado aos sistemas de uma empresa fictícia.

**Limitação técnica:** embora o modelo de atuação considere acesso aos sistemas da Chegaê, o protótipo não possui integração real com APIs, bancos de dados ou sistemas externos. As simulações foram realizadas no ambiente do ChatGPT.
