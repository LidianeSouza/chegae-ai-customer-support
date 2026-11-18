# 04. Construção e Engenharia de Prompt

Este documento explica as decisões técnicas, a metodologia e as iterações adotadas no desenvolvimento do System Prompt do agente **Chegô**, assistente virtual da **Chegaê**.

---

## 🏗️ Metodologia de Construção

A criação do prompt seguiu o framework estruturado de Engenharia de Prompt para Agentes Conversacionais:

```
┌──────────────────────────────────────┐
│ 1. Papel & Identidade (Role)         │
├──────────────────────────────────────┤
│ 2. Contexto de Negócio (Context)     │
├──────────────────────────────────────┤
│ 3. Tom de Voz & Estilo (Tone/Style)  │
├──────────────────────────────────────┤
│ 4. Regras e Limites (Guardrails)     │
├──────────────────────────────────────┤
│ 5. Tratamento de Exceções & Transbordo│
├──────────────────────────────────────┤
│ 6. Formatação de Saída (Output Spec) │
└──────────────────────────────────────┘
```

---

## 🔍 Estrutura do Prompt de Instruções

O prompt oficial está versionado em [`prompts/agente-atendimento-chegae.md`](../prompts/agente-atendimento-chegae.md) e foi estruturado nas seguintes seções:

1. **Papel e Contexto:** Identificação como agente **Chegô** e escopo da plataforma **Chegaê** (delivery de refeições, mercado, farmácia e lojas parceiras).
2. **Quem fala com você:** Caracterização do público (consumidores com dúvidas ou problemas durante/após a compra).
3. **Escopo de Resolução:** Status de pedidos, problemas de entrega, cobrança/reembolso e dúvidas gerais.
4. **Objetivo:** Atendimento rápido, cordial e resolutivo.
5. **Tom e Formato:**
   - Cordial, simpático e profissional.
   - Máximo de 5 linhas por resposta para evitar respostas prolixas.
   - Listas numeradas para procedimentos multi-etapas.
   - Empatia explícita diante de problemas relatados.
   - Pergunta de encerramento para confirmar resolução.
6. **Regras Invioláveis (Guardrails):**
   - Nunca solicitar senhas, códigos ou dados financeiros sensíveis.
   - NUNCA inventar valores, taxas, prazos ou protocolos.
   - Não confirmar cancelamento/reembolso sem confirmação real do sistema.
   - Diferenciar orientação de ação efetivamente executada.
7. **Encaminhamento Humano:** Gatilhos objetivos de transbordo (fraude, contestação, reincidência, pedido explícito do cliente).
8. **Instrução Final:** Regra de transparência ("se faltar informação, faça uma pergunta objetiva antes; nunca invente dados para completar uma resposta").

---

## 🔄 Ciclo de Refinamento e Aprendizados

Durante os testes iniciais, observou-se que:
1. **Prolixidade:** O modelo gerava textos longos explicando termos e condições. **Ajuste:** Adicionou-se a restrição de objetividade e limite de parágrafos.
2. **Promessas de Estorno:** Em testes de cancelamento, o modelo às vezes afirmava "já estornei seu dinheiro". **Ajuste:** Reforçou-se a instrução de que o agente não possui autorização operacional direta de estorno financeiro.

