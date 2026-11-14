# 06. Estudo de Caso — Agente de Atendimento Chegaê

## 📖 Resumo Executivo

O atendimento ao cliente em aplicativos de entrega opera sob alta volatilidade e pressão de tempo. Problemas como atrasos, extravios e falhas de pagamento exigem respostas imediatas para preservar a lealdade da marca e evitar churn.

O projeto **Chegaê — AI Customer Support** demonstra como uma abordagem estruturada de **Engenharia de Prompt** permite construir uma camada inteligente de primeiro nível de atendimento com IA generativa, reduzindo o tempo de resposta e garantindo conformidade com regras corporativas e de segurança.

<p align="center">
  <a href="../assets/portfolio/estudo-de-caso.png">
    <img src="../assets/portfolio/estudo-de-caso.png" width="90%" alt="Estudo de Caso Chegaê">
  </a>
</p>

---

## 🎯 Desafio de Negócio

Em grandes operações de entrega:
- **Volume:** Milhares de mensagens simultâneas em horários de pico (almoço e jantar).
- **Sensibilidade do Cliente:** Fome e atrasos aumentam a carga emocional do contato.
- **Risco de Conformidade:** IAs que alucinam prazos incorretos ou prometem valores de ressarcimento geram passivos operacionais e jurídicos.

---

## 💡 Decisões Estratégicas de Design do Agente

1. **Separação Clara entre Orientação e Transação:**
   - O agente informa status e ensina a utilizar fluxos nativos do aplicativo, sem disparar ações financeiras irreversíveis sem autorização humana.
2. **Priorização da Segurança da Informação:**
   - Casos com risco de fraude são tratados como exceções críticas com handoff humano em zero toques desnecessários.
3. **Comunicação Empática sem Submissão:**
   - O tom de voz valida o sentimento do cliente sem concordar com premissas inverídicas ou acusar parceiros de forma precipitada.

---

## 📈 Impacto Esperado e Benefícios

* **Redução do Tempo Médio de Espera (TME):** Resolução e triagem instantânea para mais de 60% das dúvidas comuns de status e políticas.
* **Qualificação do Transbordo Humano:** Quando a solicitação chega ao atendente humano, o contexto já foi classificado e pré-validado.
* **Padronização e Governança:** Garantia de que políticas de reembolso e prazos comunicados seguem estritamente as diretrizes da empresa.

---

## 🚀 Próximas Evoluções

- Implementação de **Tool Calling (Function Calling)** para consultas reais em APIs de pedidos e rastreamento de entregadores.
- Arquitetura **RAG (Retrieval-Augmented Generation)** conectada à base de conhecimento dinâmica de lojas parceiras e termos de serviço.
- Criação de suíte de testes automatizados com avaliações LLM-as-a-Judge.

