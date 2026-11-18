# 02. Arquitetura Conceitual do Agente

Este documento apresenta a arquitetura conceitual e o fluxo lógico de atendimento do agente **Chegô**, assistente virtual da plataforma fictícia **Chegaê**.

A arquitetura foi definida para organizar as etapas de interpretação da solicitação, aplicação das regras de segurança, consulta de informações e elaboração da resposta.

**Importante:** o fluxo representa o modelo de funcionamento planejado. No estágio atual, o protótipo foi desenvolvido e testado por meio de simulações no ChatGPT, sem integração técnica com APIs, bancos de dados ou sistemas externos.

---

## 📐 Fluxo Geral de Atendimento

O fluxo conceitual foi organizado para que cada solicitação passe por etapas de interpretação, validação e aplicação das instruções antes da elaboração da resposta.

```text
[ Cliente Envia Mensagem ]
          │
          ▼
┌─────────────────────────┐
│ Interpretação da        │
│ Solicitação             │
└─────────┬───────────────┘
          │
          ▼
┌─────────────────────────┐
│ Aplicação das Regras    │
│ de Segurança            │
└─────────┬───────────────┘
          │
          ▼
┌─────────────────────────┐
│ Identificação da        │
│ Necessidade do Cliente  │
└─────────┬───────────────┘
          │
          ▼
┌─────────────────────────┐
│ Consulta de Informações │
│ (Sistemas da Plataforma)│
└─────────┬───────────────┘
          │
          ▼
┌─────────────────────────┐
│ Geração da Resposta     │
│ Orientada pelo Prompt   │
└─────────┬───────────────┘
          │
          ▼
[ Resposta ou Encaminhamento ]
```

<p align="center">
  <a href="../assets/portfolio/diagrama-funcionamento.png">
    <img src="../assets/portfolio/diagrama-funcionamento.png" width="90%" alt="Diagrama de funcionamento do agente">
  </a>
</p>

---

## 🧩 Componentes do Sistema

### 1. Interpretação da Solicitação
Responsável por identificar a necessidade principal do consumidor, como:
- Consultar o status de um pedido.
- Relatar atraso ou problema na entrega.
- Solicitar informações sobre reembolso.
- Contestar uma cobrança.
- Solicitar atendimento humano.

### 2. Regras de Segurança e Limites de Atuação
Conjunto de instruções que orienta o comportamento do agente durante o atendimento.

Entre as principais diretrizes estão:
- Não solicitar senhas ou dados financeiros sensíveis.
- Não inventar informações sobre pedidos ou pagamentos.
- Não confirmar operações sem retorno positivo do sistema.
- Identificar situações que exigem intervenção humana.
- Respeitar os limites definidos no System Prompt.

### 3. Consulta de Informações
Na arquitetura planejada, o agente utiliza os sistemas da Chegaê para consultar informações relacionadas aos pedidos, pagamentos e solicitações dos consumidores.

As respostas devem utilizar dados efetivamente retornados pelos sistemas, sem presumir resultados ou simular operações.

Essa etapa depende de uma futura integração técnica com APIs e fontes de dados da plataforma.

### 4. Geração e Encaminhamento da Resposta
O modelo de linguagem utiliza as instruções do prompt para elaborar respostas de acordo com o contexto apresentado pelo consumidor.

Quando a situação ultrapassa os limites de atuação do agente, a arquitetura prevê o encaminhamento para atendimento humano, mediante confirmação do sistema responsável.

---

## 🔄 Evolução Técnica Planejada
A arquitetura poderá evoluir com a implementação de:
- APIs: para consultas de pedidos, pagamentos e solicitações.
- Banco de dados: para armazenamento e recuperação de informações.
- Tool Calling: para permitir que o modelo acione funções externas de maneira controlada.
- RAG: para recuperar informações atualizadas de políticas e procedimentos.
- Testes automatizados: para avaliar a consistência e a segurança das respostas.
