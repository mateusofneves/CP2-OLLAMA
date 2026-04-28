# 🤖 NuAssist: Assistente Virtual Bancário com Ollama

**Domínio Escolhido:** Setor Financeiro / Atendimento ao Cliente.  
Este projeto consiste na criação de um assistente especializado para um banco digital, focado em resolver dúvidas sobre conta corrente, rendimentos e segurança de forma ágil, moderna e segura.

---

## 👥 Integrantes do Grupo

| Nome Completo | RM | GitHub |
| :--- | :--- | :--- |
| **Mateus de Oliveira Fernandes Neves** | 572431 | [mateusofneves](https://github.com/mateusofneves) |
| **Paulo Henrique Lira Bilac de Araujo** | 569496 | [Patohabitant](https://github.com/Patohabitant) |
| **Olavo Dadario Vianna Barreto** | 569272 | [Dadario343](https://github.com/Dadario343) |
| **Pedro Soares de Souza** | 571285 | [pedrosoaresdesouza03-rgb](https://github.com/pedrosoaresdesouza03-rgb) |
| **Jhon Cutile Titirico** | 571976 | [jhoncutiletitirico](https://github.com/jhoncutiletitirico) |

---

## 💡 Justificativa
Escolhemos o domínio bancário devido à necessidade de uma comunicação que equilibre **proximidade** e **segurança**. No cenário atual, os bancos digitais precisam de IAs que traduzam termos técnicos ("bancuês") para uma linguagem acessível, garantindo que o cliente entenda seus benefícios (como rendimentos) e protocolos de segurança sem fricção.

---

## 📊 Dataset
O dataset foi construído utilizando a técnica de *Few-shot Prompting*, inserida diretamente no `Modelfile`.
* **Quantidade:** 10 pares de Pergunta/Resposta.
* **Construção:** Mapeamos as dúvidas mais frequentes em FAQs de bancos digitais reais, focando em:
    1. Visualização de extrato e saldo.
    2. Procedimentos de emergência (perda de cartão).
    3. Explicação de rendimentos (CDI vs Poupança).
    4. Suporte para novos produtos financeiros.

---

## 🧠 System Prompt & Decisões
O comportamento da IA foi moldado através do seguinte System Prompt:

```text
SYSTEM "Você é o NuAssist, um assistente de banco digital. Seja transparente e direto. 
Regras: 1. Nunca peça senhas ou dados sensíveis. 2. Use português brasileiro simples. 
3. Se não souber algo, direcione para o chat humano."
PARAMETER temperature 0.3
