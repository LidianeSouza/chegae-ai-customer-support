# 💜 Chegaê — AI Customer Support Agent

<h1 align="center">💜 Chegaê — AI Customer Support Agent</h1>

<p align="center">
  <img src="assets/logo/logo-chegae.png" alt="Logo Chegaê" width="280">
</p>

<p align="center">
  <strong>Precisou? Chegaê!</strong>
  <br>
  Agilidade e inteligência no atendimento ao cliente.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Projeto-Protótipo-8B5CF6">
  <img src="https://img.shields.io/badge/IA-Generativa-FF782F">
  <img src="https://img.shields.io/badge/Prompt%20Engineering-LLMs-A855F7">
  <img src="https://img.shields.io/badge/Status-Em%20desenvolvimento-FF782F">
</p>

---

## 📌 Sobre o projeto

A **Chegaê** é uma empresa fictícia criada para o desenvolvimento de um projeto prático de Inteligência Artificial Generativa.

Inspirada nas plataformas digitais de delivery e conveniência, a Chegaê conecta consumidores a restaurantes, supermercados, farmácias, lojas e outros estabelecimentos parceiros.

O projeto consiste na criação de um **Agente de Atendimento ao Cliente com IA**, utilizando Engenharia de Prompt para orientar o comportamento de um modelo de linguagem em diferentes situações de atendimento.

O agente, chamado **Chegô**, foi configurado para interpretar solicitações, oferecer orientações, demonstrar empatia e reconhecer situações que exigem atendimento humano.

O desenvolvimento explora a estruturação de instruções, definição de regras de comportamento, limites de atuação e avaliação das respostas geradas por meio de simulações manuais no ChatGPT.

## 🎯 Objetivos

- Desenvolver um protótipo de agente de atendimento utilizando IA Generativa.
- Aplicar técnicas de Engenharia de Prompt na estruturação de instruções para LLMs.
- Definir papel, contexto, escopo, tom de comunicação e regras de comportamento.
- Estabelecer limites para evitar respostas incorretas ou informações inventadas.
- Simular diferentes situações de atendimento ao cliente.
- Avaliar as respostas geradas pelo modelo.
- Identificar limitações e oportunidades de melhoria.
- Planejar a evolução do protótipo para uma solução funcional.

## 🛵 Conheça a Chegaê

A **Chegaê** é uma plataforma fictícia de delivery e conveniência que conecta consumidores a diferentes estabelecimentos parceiros.

O projeto utiliza esse cenário para explorar como um agente de IA pode auxiliar no atendimento ao cliente, oferecendo orientações e identificando situações que exigem suporte especializado.

Entre os principais cenários de atendimento considerados no projeto estão:

| Categoria | Exemplos de atendimento |
|---|---|
| 📦 Pedidos | Dúvidas sobre status e acompanhamento |
| 🛵 Entregas | Atrasos, pedidos não recebidos ou incorretos |
| 💳 Pagamentos | Dúvidas sobre cobranças e pagamentos |
| 💰 Reembolsos | Orientações sobre solicitações de reembolso |
| ❌ Cancelamentos | Dúvidas sobre cancelamento de pedidos |
| 🙋 Suporte | Identificação de situações que exigem atendimento humano |

## 🧠 Como o agente foi desenvolvido

O agente **Chegô** foi configurado no ChatGPT por meio de um conjunto estruturado de instruções, conhecido como **System Prompt**.

A Engenharia de Prompt foi utilizada para definir a identidade do agente, o contexto de atuação, o estilo de comunicação, as regras de segurança e os limites das respostas.

A estrutura foi organizada em quatro camadas principais:

### 📐 Estrutura de Engenharia do Prompt

O comportamento do modelo foi orientado a partir de uma estrutura modular de diretrizes e guardrails:

| Camada do Prompt | Foco da Instrução | Diretrizes Aplicadas |
|---|---|---|
| 🎭 **1. Papel & Contexto** | Identidade da Marca | Representar a Chegaê; foco em delivery de refeições, mercado, farmácia e conveniência. |
| 💬 **2. Tom & Formato** | Experiência do Cliente | Cordialidade, linguagem simples e próxima, empatia ativa, **máximo de 5 linhas** e listas numeradas. |
| 🛡️ **3. Guardrails Críticos** | Segurança & Anti-alucinação | **Proibido inventar prazos, valores ou taxas**; nunca solicitar senhas ou dados de cartão (LGPD). |
| 🚨 **4. Matriz de Transbordo** | Limites Operacionais | Encaminhamento para atendimento humano em suspeitas de fraude, contestações ou pedido do cliente. |

<details>
  <summary>📜 <b>Clique aqui para visualizar o Prompt de Instruções completo (System Prompt)</b></summary>
  <br>

```markdown
```markdown
# 💜 Agente de Atendimento ao Cliente – Chegô | Chegaê

Você é **Chegô**, o agente virtual de atendimento ao cliente da **Chegaê**, uma plataforma digital de delivery e conveniência que conecta consumidores a restaurantes, supermercados, farmácias, lojas e outros estabelecimentos parceiros.

A plataforma tem como principal foco a entrega de refeições e alimentos, mas também oferece produtos de diferentes segmentos, proporcionando praticidade e conveniência para atender às diversas necessidades do dia a dia dos consumidores.

## 👤 Quem fala com você

Consumidores que utilizam a plataforma Chegaê para pedir refeições, comprar alimentos, produtos de supermercado, farmácia, lojas e outros itens disponíveis nos estabelecimentos parceiros.

São pessoas que podem ter dúvidas sobre produtos, pedidos, pagamentos e prazos de entrega, além de enfrentar problemas como pedidos incompletos, atrasos, entregas não realizadas, cobranças indevidas, cancelamentos ou outras situações que exijam suporte durante ou após a compra.

## 🛵 Os pedidos que você resolve são:

- Consultar o status e acompanhar pedidos em andamento.
- Ajudar em problemas com entregas, como atrasos, pedidos não recebidos ou entregues incorretamente.
- Orientar sobre pagamentos, cobranças e solicitações de reembolso.
- Esclarecer dúvidas sobre cancelamentos e funcionamento da plataforma.

## 🔗 Integração com a Plataforma

Você atua integrado aos sistemas da Chegaê, com acesso aos recursos necessários para consultar pedidos, verificar informações e registrar ou encaminhar solicitações. Utilize os dados e as confirmações retornados pelos sistemas para orientar o cliente. Nunca simule consultas ou operações nem informe que uma ação foi concluída sem a confirmação correspondente.

## 🎯 Seu objetivo em cada conversa

Oferecer um atendimento rápido, cordial e eficiente, identificando a necessidade do cliente e orientando-o para a melhor solução, proporcionando uma experiência positiva na utilização do aplicativo.

## 💬 Tom e formato

- Fale de forma cordial, simpática, direta e profissional, utilizando uma linguagem simples e próxima do cliente.
- Use no máximo 5 linhas por resposta, evitando explicações muito longas.
- Quando a solução tiver mais de uma etapa, responda em lista numerada.
- Demonstre empatia quando o cliente relatar algum problema, principalmente em casos de atraso, cobrança ou pedido não recebido.
- Evite respostas genéricas. Identifique o problema e apresente orientações adequadas à situação relatada.
- Ao finalizar o atendimento, pergunte se a dúvida ou problema foi resolvido, exceto quando ainda houver alguma etapa pendente.

## 🛡️ Regras que você sempre segue

- Nunca solicite senha, códigos de autenticação, dados completos do cartão ou outras informações financeiras sensíveis.
- Se alguma informação não estiver disponível nos sistemas, explique a situação ao cliente e indique o próximo passo.
- Nunca invente valores, taxas, prazos de entrega, prazos de reembolso, números de protocolo ou políticas da empresa.
- Nunca confirme um cancelamento ou reembolso sem que a operação tenha sido efetivamente realizada e confirmada pelo sistema.
- Não responsabilize o restaurante, estabelecimento parceiro ou entregador sem ter informações que comprovem o ocorrido.
- Não prometa soluções que dependam de aprovação de outros setores.
- Consulte e informe dados de pedidos utilizando os sistemas da plataforma. Caso não consiga obter as informações necessárias, não presuma resultados nem invente dados.
- Diferencie orientações de operações efetivamente realizadas. Nunca afirme que executou uma ação quando apenas explicou como o cliente pode fazê-la.

## 🤝 Encaminhamento para atendimento humano

Encaminhe para atendimento humano quando:

- O cliente relatar suspeita de fraude, cobrança indevida ou problemas relacionados à segurança da conta.
- O cliente solicitar uma contestação de cobrança ou de uma decisão anterior que não possa ser resolvida pelo agente.
- Houver problemas recorrentes com o pedido ou situações que exijam análise individual.
- O cliente demonstrar insatisfação e solicitar expressamente falar com uma pessoa.
- O cliente solicitar uma ação que dependa de contato direto com o estabelecimento.

Ao encaminhar, explique em uma frase o motivo e informe quais informações sobre o problema já foram registradas na conversa. Nunca diga que o encaminhamento foi realizado se não houver confirmação do sistema.

## 📌 Instrução final

Se faltar alguma informação para responder com segurança, faça uma pergunta objetiva antes de responder. Se não tiver acesso aos dados necessários ou não puder resolver a solicitação, seja transparente e oriente o cliente sobre o próximo passo. Nunca invente informações para completar uma resposta.
```
```

</details>

## ⚙️ Fluxo de funcionamento

O diagrama abaixo representa o fluxo conceitual de atendimento definido para o agente Chegô, desde o recebimento da solicitação até a elaboração de uma resposta ou identificação da necessidade de atendimento humano.

<p align="center">
  <a href="assets/portfolio/diagrama-funcionamento.png">
    <img src="assets/portfolio/diagrama-funcionamento.png" width="85%" alt="Diagrama conceitual de funcionamento do agente Chegô">
  </a>
</p>

**Etapas principais:**

- Recebimento da solicitação do cliente.
- Interpretação da intenção e do contexto.
- Identificação do problema e aplicação das instruções do prompt.
- Elaboração de uma resposta ou orientação sobre a necessidade de atendimento humano.

> O fluxo representa a lógica prevista nas instruções do agente. Não corresponde a uma arquitetura de software implementada nem contempla integrações com sistemas externos.

## 💬 O agente em ação

As simulações abaixo foram realizadas no ChatGPT com o agente Chegô, inicializado a partir do System Prompt da Chegaê. Cada cenário apresenta o registro real da interação e uma análise do comportamento observado.

### 01. Atraso na entrega

| Simulação Real (ChatGPT) | Análise do Cenário |
|:---:|---|
| <a href="assets/screenshots/01-atraso-entrega.png"><img src="assets/screenshots/01-atraso-entrega.png" width="380" alt="Simulação 01 - Atraso"></a> | **🎯 Objetivo:** Avaliar como o agente responde a uma reclamação de atraso, considerando empatia, consulta do pedido e encaminhamento para atendimento humano.<br><br>**👤 Entrada do Cliente:**<br>"Fiz um pedido há 40 minutos e gostaria de saber se ele já saiu para entrega. Essa demora é um desrespeito com o cliente."<br><br>**🤖 Resposta registrada:**<br>O agente demonstrou empatia, afirmou ter consultado o pedido, informou que ele estava em preparação e propôs encaminhar o caso ao atendimento humano.<br><br>**🔍 Análise do resultado:**<br>• **Acerto:** reconheceu a insatisfação do cliente e respondeu com empatia.<br>• **Acerto:** apresentou uma informação objetiva sobre o status do pedido.<br>• **Acerto:** identificou a possibilidade de encaminhamento para atendimento humano.<br><br>**Conclusão:** o comportamento observado está alinhado à proposta de atendimento do Chegô, com atenção à experiência do cliente e à necessidade de suporte humano. |

---

### 02. Solicitação de reembolso

| Simulação Real (ChatGPT) | Análise do Cenário |
|:---:|---|
| <a href="assets/screenshots/02-reembolso.png"><img src="assets/screenshots/02-reembolso.png" width="380" alt="Simulação 02 - Reembolso"></a> | **🎯 Objetivo:** Avaliar se o agente fornece informações sobre reembolso sem inventar valores ou prazos e orienta o cliente adequadamente.<br><br>**👤 Entrada do Cliente:**<br>"Qual é o valor exato que vou receber de reembolso pelo meu pedido cancelado?"<br><br>**🤖 Resposta registrada:**<br>O agente informou que o valor do reembolso não estava disponível nas informações que conseguia visualizar e orientou o cliente a consultar a seção Meus Pedidos do aplicativo.<br><br>**🔍 Análise do resultado:**<br>• **Acerto:** não inventou o valor do reembolso.<br>• **Acerto:** não apresentou prazo sem confirmação.<br>• **Acerto:** orientou o cliente sobre onde buscar a informação.<br><br>**Conclusão:** o agente demonstrou cautela ao lidar com informações financeiras e priorizou a transparência diante da indisponibilidade do valor. |

---

### 03. Cobrança não reconhecida

| Simulação Real (ChatGPT) | Análise do Cenário |
|:---:|---|
| <a href="assets/screenshots/03-cobranca-nao-reconhecida.png"><img src="assets/screenshots/03-cobranca-nao-reconhecida.png" width="380" alt="Simulação 03 - Cobrança não reconhecida"></a> | **🎯 Objetivo:** Avaliar a postura do agente diante de uma cobrança não reconhecida, considerando segurança, empatia e encaminhamento para atendimento humano.<br><br>**👤 Entrada do Cliente:**<br>"Identifiquei uma cobrança no meu cartão que não reconheço. Não fiz esse pedido e quero saber quem utilizou meus dados!"<br><br>**🤖 Resposta registrada:**<br>O agente demonstrou empatia, informou que encaminharia o caso para atendimento humano e afirmou que as informações já haviam sido registradas.<br><br>**🔍 Análise do resultado:**<br>• **Acerto:** reconheceu a preocupação do cliente e indicou a necessidade de atendimento humano.<br>• **Acerto:** não solicitou senha, CVV ou dados completos do cartão.<br>• **Acerto:** informou que os dados relatados já estavam registrados na conversa, conforme a orientação do prompt.<br><br>**Conclusão:** o agente demonstrou uma postura adequada diante de uma situação sensível, priorizando a segurança e o atendimento humano. |

## 🧪 Testes e avaliação

Foram realizadas simulações manuais para observar o comportamento do Chegô diante de diferentes situações de atendimento ao cliente.

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

Os testes foram avaliados manualmente, com base nas instruções do System Prompt e nas respostas registradas nas simulações. A análise considera os comportamentos observados em cada cenário, sem utilizar métricas automatizadas ou resultados de produção.

## 📚 Estudo de caso

O projeto Chegaê nasceu da proposta de explorar como agentes de Inteligência Artificial podem melhorar a experiência de atendimento ao cliente em plataformas de delivery e conveniência.

O desafio foi desenvolver um agente capaz de compreender diferentes solicitações, responder de forma natural e identificar quando uma situação exige atendimento humano, mantendo regras claras de segurança, precisão e transparência.

A solução foi estruturar o **Chegô**, um agente virtual orientado por Engenharia de Prompt, com identidade, responsabilidades, regras de comportamento e diretrizes de atendimento.

**Principais decisões de desenvolvimento:**

- Definir a identidade, o papel e o contexto de atuação do agente.
- Organizar as instruções em seções específicas para facilitar a compreensão e a manutenção do prompt.
- Estabelecer regras para consultas, pagamentos, cancelamentos e reembolsos.
- Definir situações que exigem encaminhamento para atendimento humano.
- Estabelecer limites para evitar informações inventadas e ações sem confirmação.
- Priorizar a segurança e a proteção dos dados do consumidor.

<p align="center">
  <a href="assets/portfolio/estudo-de-caso.png">
    <img src="assets/portfolio/estudo-de-caso.png" width="85%" alt="Estudo de caso Chegaê">
  </a>
</p>

## 🛠️ Tecnologias e ferramentas

| Tecnologia / Ferramenta | Utilização |
|---|---|
| ChatGPT | Configuração, experimentação e simulação do agente |
| Engenharia de Prompt | Estruturação das instruções, regras e comportamento |
| GitHub | Versionamento e apresentação do projeto |
| Markdown | Documentação técnica |
| Canva / ferramentas gráficas | Desenvolvimento dos materiais visuais |

## 🚀 Próximos passos

O projeto está em sua primeira etapa, focada na construção e avaliação do comportamento do agente por meio de Engenharia de Prompt.

As próximas etapas planejadas são:

- [ ] Ampliar os cenários de teste e avaliar situações mais complexas.
- [ ] Refinar as instruções a partir dos resultados das avaliações.
- [ ] Desenvolver uma versão funcional utilizando Python e uma API de LLM.
- [ ] Criar uma base simulada de pedidos para consultas.
- [ ] Explorar integração com ferramentas (Tool Calling).
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

O desenvolvimento deste projeto permitiu explorar, na prática, como a Engenharia de Prompt pode orientar o comportamento de agentes de Inteligência Artificial.

Durante o processo, foi possível observar que criar um agente não significa apenas definir o que ele deve responder, mas também estabelecer o que ele não pode fazer, como deve lidar com situações inesperadas e quando precisa reconhecer seus próprios limites.

As simulações também demonstraram a importância de avaliar as respostas, identificar inconsistências e aprimorar as instruções para buscar maior clareza, precisão e consistência no atendimento.

## 📌 Status do projeto

**Protótipo em desenvolvimento — Etapa de Engenharia de Prompt e simulações.**

O Chegô foi configurado e avaliado manualmente no ChatGPT. O projeto ainda não possui integração técnica com sistemas reais, API própria, banco de dados conectado ou implantação em produção.

---

<p align="center">
  <strong>Chegaê — Precisou? Chegaê! 💜🧡</strong>
  <br>
  Projeto desenvolvido para estudos e portfólio em Inteligência Artificial e Engenharia de IA.
</p>

