# 02. Arquitetura Conceitual do Agente

Este documento descreve a arquitetura conceitual e o fluxo lógico de decisão do agente **Chegô**, assistente de atendimento da plataforma **Chegaê**.

---

## 📐 Fluxo Geral de Atendimento

O fluxo foi desenhado para assegurar que cada interação passe por camadas de validação, segurança e conferência de contexto antes da geração da resposta final.

```
[ Cliente Envia Mensagem ]
          │
          ▼
┌─────────────────────────┐
│  Interpretação e NLP    │ ◄── Classificação de Intenção e Sentimento
└─────────┬───────────────┘
          │
          ▼
┌─────────────────────────┐
│   Camada de Segurança   │ ◄── Detecção de Fraude / Dados Sensíveis / Injection
└─────────┬───────────────┘
          │
          ├─► [Crítico / Fraude / Risco] ──► [ Encaminhamento Humano Imediato ]
          │
          ▼
┌─────────────────────────┐
│ Consulta de Contexto e  │ ◄── Status do Pedido, Políticas e Regras de Negócio
│     Base de Regras      │
└─────────┬───────────────┘
          │
          ▼
┌─────────────────────────┐
│ Geração Guiada (Prompt) │ ◄── Empatia, Clareza, Instruções Anti-Alucinação
└─────────┬───────────────┘
          │
          ▼
[ Resposta ao Cliente / Próximo Passo ]
```

<p align="center">
  <a href="../assets/portfolio/diagrama-funcionamento.png">
    <img src="../assets/portfolio/diagrama-funcionamento.png" width="90%" alt="Diagrama de funcionamento do agente">
  </a>
</p>

---

## 🧩 Componentes do Sistema

### 1. Camada de Interpretação (NLU/NLP)
- Identifica o objetivo principal do cliente (ex.: rastrear pedido, contestar cobrança, relatar item faltante).
- Avalia o nível de estresse ou insatisfação para calibrar o tom da resposta.

### 2. Camada de Segurança e Guardrails
- **Filtro de Dados Sensíveis:** Impede que o agente solicite ou armazene números de cartão, CVV ou senhas.
- **Detecção de Fraude/Urgência:** Gatilho prioritário que interrompe a automação e passa o caso para analistas de segurança.
- **Defesa contra Prompt Injection:** Instruções explícitas no system prompt para manter a persona e não executar comandos que tentem desviar o comportamento do agente.

### 3. Motor de Regras e Políticas
- Avalia a situação contra as políticas da Chegaê:
  - Tempo de atraso tolerável.
  - Prazos legais e internos para estorno.
  - Janelas de cancelamento (antes ou depois do início do preparo pelo parceiro).

### 4. Camada de Geração e Resposta
- Aplica as diretrizes de voz e tom da Chegaê.
- Fornece instruções acionáveis de autoatendimento no aplicativo ou conclui com o encaminhamento seguro para a fila de suporte humano.

