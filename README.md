# 💜 Chegaê — AI Customer Support Agent

<p align="center">
  <img src="assets/logo/logo-chegae.png" alt="Logo Chegaê" width="220">
</p>

<h3 align="center">Peça. Receba. Resolva. 🛵</h3>

<p align="center">
  <strong>Um protótipo de agente de atendimento ao cliente desenvolvido com Engenharia de Prompt e Inteligência Artificial Generativa.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Projeto-Protótipo-8B5CF6">
  <img src="https://img.shields.io/badge/IA-Generativa-FF782F">
  <img src="https://img.shields.io/badge/Prompt%20Engineering-Em%20desenvolvimento-A855F7">
  <img src="https://img.shields.io/badge/Status-Em%20desenvolvimento-FF782F">
</p>

---

## 📌 Sobre o projeto

A **Chegaê** é uma empresa fictícia criada para o desenvolvimento de um projeto prático de Inteligência Artificial Generativa.

Inspirada nas plataformas digitais de delivery e conveniência, a Chegaê conecta consumidores a restaurantes, supermercados, farmácias, lojas e outros estabelecimentos parceiros.

O projeto consiste na criação de um **Agente de Atendimento ao Cliente com IA**, capaz de interpretar solicitações, identificar problemas e fornecer orientações de maneira cordial, objetiva e segura.

A proposta é explorar como a Engenharia de Prompt pode orientar o comportamento de um modelo de linguagem em situações reais de atendimento, considerando regras de negócio, limites de atuação, segurança e experiência do usuário.

## 🎯 Objetivos

- Desenvolver um agente de atendimento utilizando Engenharia de Prompt.
- Definir papel, contexto, escopo e responsabilidades do agente.
- Estabelecer regras de negócio e critérios de segurança.
- Simular diferentes situações de atendimento ao cliente.
- Avaliar as respostas geradas pelo modelo.
- Identificar limitações e oportunidades de melhoria.
- Planejar a evolução do protótipo para uma solução funcional.

## 🛵 Conheça a Chegaê

A Chegaê é uma plataforma fictícia de delivery e conveniência que oferece diferentes categorias de produtos e serviços.

Seu agente de atendimento foi pensado para auxiliar consumidores em situações como:

| Categoria | Exemplos de atendimento |
|---|---|
| 📦 Pedidos | Consulta de status e acompanhamento |
| 🛵 Entregas | Atrasos, pedidos não recebidos ou incorretos |
| 💳 Pagamentos | Dúvidas sobre cobranças e pagamentos |
| 💰 Reembolsos | Orientações sobre solicitações de reembolso |
| ❌ Cancelamentos | Dúvidas sobre cancelamento de pedidos |
| 🙋 Suporte | Encaminhamento de situações que exigem atendimento humano |

## 🧠 Como o agente foi desenvolvido

O desenvolvimento começou pela Engenharia de Prompt, com a definição de instruções para orientar o comportamento do modelo.

O prompt foi estruturado considerando:

1. **Papel e contexto:** definição da identidade do agente e da plataforma.
2. **Público-alvo:** consumidores que utilizam os serviços da Chegaê.
3. **Escopo de atuação:** situações que o agente deve atender.
4. **Tom e formato:** comunicação simples, cordial, direta e profissional.
5. **Regras de negócio:** limites e responsabilidades durante o atendimento.
6. **Segurança:** proteção de informações pessoais e financeiras.
7. **Encaminhamento humano:** identificação de situações que exigem intervenção de uma pessoa.

O objetivo foi criar instruções que reduzissem respostas genéricas, informações inventadas e promessas que o agente não pudesse cumprir.

## ⚙️ Fluxo de funcionamento

O fluxo conceitual representa as etapas de atendimento previstas para o agente.

<p align="center">
  <a href="assets/portfolio/diagrama-funcionamento.png">
    <img src="assets/portfolio/diagrama-funcionamento.png" width="85%" alt="Diagrama de funcionamento do agente">
  </a>
</p>

**Etapas principais:**

- Recebimento da solicitação do cliente.
- Interpretação da intenção e do contexto.
- Identificação do problema e aplicação das regras.
- Elaboração de uma resposta ou proposta de encaminhamento humano.

> O fluxo representa a lógica conceitual do protótipo, não uma arquitetura de software já implementada.

## 💬 O agente em ação

As simulações abaixo foram realizadas no ChatGPT. Antes do atendimento, o modelo recebeu as instruções completas do [Prompt de Atendimento Chegaê](prompts/agente-atendimento-chegae.md), definindo persona, tom de voz, regras de negócio e critérios de transbordo.

Abaixo estão os prompts enviados pelo cliente (entradas), as respostas reais obtidas e a análise do comportamento observado.

### 01. Atraso na entrega

**Objetivo:** avaliar como o agente reage diante de um cliente insatisfeito com a demora na entrega.

> **👤 Mensagem do cliente (Prompt):**  
> *"Fiz um pedido há 40 minutos e gostaria de saber se ele já saiu para entrega. Essa demora é um desrespeito com o cliente."*

> **🤖 Resposta do agente:**  
> *"Olá! Sinto muito pela demora e entendo sua insatisfação. 💗*  
> *Consultei seu último pedido e ele ainda consta como **em preparação**, sem confirmação de saída para entrega.*  
> *Como já se passaram 40 minutos, vou encaminhar sua solicitação para atendimento humano, que poderá verificar diretamente com o estabelecimento o motivo do atraso e buscar uma solução.*  
> *Posso prosseguir?"*

**Comportamento observado:**
- Demonstra empatia com a situação de insatisfação.
- Consulta o status do pedido no contexto simulado.
- Identifica que o pedido ainda está em preparação e não culpa o parceiro sem evidências.
- Propõe proativamente o encaminhamento para atendimento humano respeitando a regra de transbordo.

<p align="center">
  <a href="assets/screenshots/01-atraso-entrega.png">
    <img src="assets/screenshots/01-atraso-entrega.png" width="75%" alt="Simulação de atendimento sobre atraso na entrega">
  </a>
</p>

### 02. Solicitação de reembolso

**Objetivo:** avaliar se o agente evita informar valores que não estão disponíveis (anti-alucinação).

> **👤 Mensagem do cliente (Prompt):**  
> *"Qual é o valor exato que vou receber de reembolso pelo meu pedido cancelado?"*

> **🤖 Resposta do agente:**  
> *"Consultei o histórico do seu último pedido cancelado, mas o valor do reembolso não está disponível nos dados que consigo visualizar.*  
> *Para não informar um valor incorreto, recomendo consultar os detalhes do pedido na seção **Meus Pedidos** do aplicativo, onde constam as informações do cancelamento e do reembolso. 😊"*

**Comportamento observado:**
- Consulta o histórico do pedido cancelado no contexto da simulação.
- Identifica com transparência que o valor exato não está visível.
- **Evita inventar informações:** cumpre a diretriz estrita de nunca inventar valores monetários ou prazos.
- Orienta o cliente a consultar a fonte oficial dentro do aplicativo.

<p align="center">
  <a href="assets/screenshots/02-reembolso.png">
    <img src="assets/screenshots/02-reembolso.png" width="75%" alt="Simulação de atendimento sobre reembolso">
  </a>
</p>

### 03. Cobrança não reconhecida

**Objetivo:** avaliar o comportamento do agente diante de uma possível situação de fraude ou problema de segurança.

> **👤 Mensagem do cliente (Prompt):**  
> *"Identifiquei uma cobrança no meu cartão que não reconheço. Não fiz esse pedido e quero saber quem utilizou meus dados!"*

> **🤖 Resposta do agente:**  
> *"Sinto muito por essa situação! Entendo sua preocupação, principalmente por envolver uma cobrança que você não reconhece. 💗*  
> *Por segurança, vou encaminhar o caso para atendimento humano, que poderá investigar a transação, verificar a origem do pedido e orientar sobre a contestação da cobrança.*  
> *As informações sobre a cobrança não reconhecida e a possível utilização indevida dos seus dados já foram registradas nesta conversa."*

**Comportamento observado:**
- Demonstra acolhimento imediato e reconhece a gravidade da queixa.
- Não solicita informações financeiras sensíveis (número do cartão, CVV, senhas).
- Aciona o escalonamento para o time humano de segurança.
- Não faz promessas falsas de cancelamento financeiro direto e confirma o registro do contexto na conversa.

<p align="center">
  <a href="assets/screenshots/03-cobranca-nao-reconhecida.png">
    <img src="assets/screenshots/03-cobranca-nao-reconhecida.png" width="75%" alt="Simulação de atendimento sobre cobrança não reconhecida">
  </a>
</p>

## 🧪 Testes e avaliação

Foram realizadas simulações manuais para observar se o agente seguia as instruções definidas no prompt.

Os principais critérios de avaliação foram:

| Critério | O que foi avaliado |
|---|---|
| Clareza | Respostas simples e objetivas |
| Empatia | Reconhecimento da insatisfação do cliente |
| Precisão | Não inventar valores, prazos ou informações |
| Segurança | Não solicitar dados sensíveis |
| Limites | Reconhecer quando não consegue resolver uma situação |
| Encaminhamento | Identificar casos que exigem atendimento humano |

<p align="center">
  <a href="assets/portfolio/painel-testes.png">
    <img src="assets/portfolio/painel-testes.png" width="85%" alt="Painel de testes">
  </a>
</p>

Os testes foram avaliados manualmente. A avaliação não representa métricas automatizadas nem resultados de produção.

## 📚 Estudo de caso

O projeto parte de um desafio comum em plataformas de atendimento: oferecer respostas rápidas e consistentes sem comprometer a segurança e a confiança do consumidor.

A solução proposta foi desenvolver um agente orientado por instruções específicas, com responsabilidades e limites bem definidos.

**Principais decisões de desenvolvimento:**

- Separar o papel do agente de suas regras de atuação.
- Definir situações que exigem atendimento humano.
- Evitar respostas baseadas em informações não disponíveis.
- Diferenciar orientações de operações efetivamente realizadas.
- Priorizar a segurança dos dados do consumidor.

<p align="center">
  <a href="assets/portfolio/estudo-de-caso.png">
    <img src="assets/portfolio/estudo-de-caso.png" width="85%" alt="Estudo de caso Chegaê">
  </a>
</p>

## 🛠️ Tecnologias e ferramentas

| Tecnologia / Ferramenta | Utilização |
|---|---|
| ChatGPT | Ambiente de experimentação e simulação do agente |
| Engenharia de Prompt | Estruturação das instruções e regras |
| GitHub | Versionamento e apresentação do projeto |
| Markdown | Documentação técnica |
| Canva / ferramentas gráficas | Desenvolvimento dos materiais visuais |

## 🚀 Próximos passos

O projeto está em sua primeira etapa, focada na construção e avaliação do comportamento do agente por meio de Engenharia de Prompt.

As próximas etapas planejadas são:

- [ ] Refinar o prompt a partir dos resultados das simulações.
- [ ] Ampliar os cenários de teste.
- [ ] Desenvolver uma versão funcional utilizando Python e uma API de LLM.
- [ ] Criar uma base simulada de pedidos para consultas.
- [ ] Explorar integração com ferramentas (tool calling).
- [ ] Implementar testes automatizados para avaliar as respostas.
- [ ] Explorar RAG para recuperação de informações de documentos e regras da plataforma.
- [ ] Desenvolver métricas de qualidade e consistência.

## 📂 Estrutura do projeto

```text
chegae-ai-customer-support/
│
├── README.md
├── prompts/
├── docs/
├── tests/
└── assets/
    ├── logo/
    ├── screenshots/
    └── portfolio/
```

## 💡 Aprendizados

O desenvolvimento deste projeto permitiu explorar, na prática, a importância de estruturar instruções para modelos de linguagem.

Durante as simulações, foi possível observar que criar um agente não significa apenas definir o que ele deve responder, mas também estabelecer o que ele não pode fazer, como deve lidar com situações inesperadas e quando precisa reconhecer seus próprios limites.

O processo também reforçou a importância de testar, avaliar e refinar as instruções para melhorar a consistência das respostas.

## 📌 Status do projeto

**Protótipo em desenvolvimento — Etapa de Engenharia de Prompt e simulações.**

Até o momento, o agente foi configurado e avaliado manualmente no ChatGPT. Não possui integração com sistemas reais, API própria, banco de dados conectado, treinamento ou implantação em produção.

---

<p align="center">
  <strong>Chegaê — Peça. Receba. Resolva. 💜🧡</strong>
  <br>
  Projeto desenvolvido para estudos e portfólio em Inteligência Artificial e Engenharia de IA.
</p>

