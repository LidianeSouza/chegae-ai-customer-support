# 04. Construção e Engenharia de Prompt

Este documento explica as decisões técnicas, a metodologia e as iterações adotadas no desenvolvimento do System Prompt do agente da **Chegaê**.

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

## 🔍 Detalhamento das Camadas do Prompt

### 1. Definição da Persona
Definiu-se uma persona acolhedora e prestativa, identificada com as cores e o lema da marca (*"Peça. Receba. Resolva. 🛵"*). A identidade clara previne que o modelo responda como um assistente genérico de propósito geral.

### 2. Guardrails Anti-Alucinação
Modelos de linguagem tendem a "agradar" o usuário prometendo prazos ou inventando valores caso não encontrem esses dados no contexto. Para mitigar esse comportamento:
- Inclusão da regra explícita: *"NUNCA invente prazos, valores monetários, descontos ou status que não constem no contexto fornecido."*
- Diferenciação deliberada entre **orientar** o cliente sobre um procedimento e **afirmar que a ação já foi concluída**.

### 3. Proteção e Privacidade (LGPD)
Para evitar riscos de conformidade:
- O agente é explicitamente proibido de solicitar números completos de cartão, códigos CVV ou senhas bancárias.
- Em casos de contestação de cobrança, ele orienta o canal correto sem coletar credenciais sensíveis no chat.

### 4. Transbordo Humano Inteligente (Human Handoff)
Muitos chatbots falham ao prender o usuário em loops infinitos. O prompt inclui gatilhos de saída imediata para atendimento humano sempre que:
- O cliente solicita expressamente falar com uma pessoa;
- Há suspeita de fraude ou ameaça à segurança;
- A situação requer negociação financeira fora dos limites de política.

---

## 🔄 Ciclo de Refinamento e Aprendizados

Durante os testes iniciais, observou-se que:
1. **Prolixidade:** O modelo gerava textos longos explicando termos e condições. **Ajuste:** Adicionou-se a restrição de objetividade e limite de parágrafos.
2. **Promessas de Estorno:** Em testes de cancelamento, o modelo às vezes afirmava "já estornei seu dinheiro". **Ajuste:** Reforçou-se a instrução de que o agente não possui autorização operacional direta de estorno financeiro.

