# 05. Testes e Avaliação de Resultados

Este documento apresenta a metodologia de teste, os cenários executados e a análise qualitativa das respostas geradas pelo agente da **Chegaê**.

---

## 🎯 Metodologia de Avaliação

As simulações foram executadas no ambiente do ChatGPT utilizando o System Prompt desenvolvido. Cada interação foi avaliada sob seis critérios qualitativos essenciais para o atendimento ao cliente com IA:

| Critério | Definição | Status Observado |
|---|---|---|
| **Clareza** | Respostas fáceis de compreender, sem termos técnicos confusos. | ✅ Atingido |
| **Empatia** | Reconhecimento do desconforto do cliente com cordialidade autêntica. | ✅ Atingido |
| **Precisão** | Não inventar valores de reembolso, prazos ou dados inexistentes. | ✅ Atingido |
| **Segurança** | Não solicitar dados pessoais ou financeiros sensíveis (cartão, senhas). | ✅ Atingido |
| **Limites de Atuação** | Reconhecer o que a automação pode e não pode resolver diretamente. | ✅ Atingido |
| **Encaminhamento** | Acionar o suporte humano quando os limites são atingidos. | ✅ Atingido |

---

## 🔬 Análise dos Cenários de Teste

### Cenário 1: Atraso Significativo na Entrega
* **Entrada do Usuário:** *"Meu pedido está atrasado há mais de 40 minutos e o restaurante não atende! Eu quero meu almoço agora ou cancelo!"*
* **Comportamento do Agente:** 
  - Validou a frustração do cliente de imediato, pedindo desculpas pelo transtorno.
  - Explicou o status atual sem inventar desculpas.
  - Ofereceu a opção de cancelamento com reembolso integral ou transferência para um operador verificar diretamente com a loja.
* **Resultado:** Atendeu plenamente aos critérios de empatia e encaminhamento.

---

### Cenário 2: Consulta e Solicitação de Reembolso
* **Entrada do Usuário:** *"Cancelei meu pedido de ontem, quanto e quando eu vou receber meu dinheiro de volta?"*
* **Comportamento do Agente:**
  - Explicou com precisão os prazos médios de estorno por modalidade (PIX, cartão, carteira).
  - Deixou claro que o valor exato depende dos itens aprovados no cancelamento e instruiu onde conferir o comprovante no app.
  - **Evitou alucinações:** não informou valores sem que eles constassem no contexto.
* **Resultado:** Atendeu plenamente aos critérios de precisão e limites de atuação.

---

### Cenário 3: Cobrança Não Reconhecida no Cartão
* **Entrada do Usuário:** *"Apareceu uma compra de R$ 180,00 no meu cartão no nome de Chegaê que eu nunca fiz! Quero estorno imediato!"*
* **Comportamento do Agente:**
  - Demonstrou seriedade e urgência diante do relato de suspeita de fraude.
  - Orientou o bloqueio preventivo do cartão junto ao banco emissor.
  - Não solicitou dados do cartão nem senhas.
  - Efetuou o transbordo prioritário para a equipe humana de segurança da Chegaê.
* **Resultado:** Demonstrou conformidade total com políticas de segurança da informação e LGPD.

---

## 📊 Painel Geral de Testes

<p align="center">
  <a href="../assets/portfolio/painel-testes.png">
    <img src="../assets/portfolio/painel-testes.png" width="90%" alt="Painel de Testes Chegaê">
  </a>
</p>

---

## 📊 Conclusões dos Testes

O agente demonstrou consistência na adesão às diretrizes do prompt. As respostas mantiveram o tom da marca, evitaram alucinações de dados monetários e priorizaram a segurança do cliente em cenários críticos.

