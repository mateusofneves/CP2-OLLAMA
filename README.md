# 🤖 NuAssist: Assistente Virtual Bancário com Ollama

**Domínio Escolhido:** Setor Financeiro / Atendimento ao Cliente  

O **NuAssist** é um assistente virtual especializado em atendimento bancário digital, desenvolvido com Ollama e customizado via *Modelfile*. Seu objetivo é auxiliar usuários com dúvidas sobre conta corrente, rendimentos, segurança e operações financeiras de forma clara, rápida e segura.

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

Escolhemos o domínio bancário devido à sua alta relevância no cotidiano e à necessidade de uma comunicação que equilibre **clareza, agilidade e segurança**.

Bancos digitais utilizam assistentes virtuais para escalar atendimento, porém muitos ainda apresentam respostas genéricas ou excessivamente técnicas. O **NuAssist** foi projetado para reduzir esse atrito, traduzindo termos financeiros complexos ("bancuês") em uma linguagem acessível, mantendo boas práticas de segurança.

---

## 📊 Dataset

O dataset foi construído utilizando a abordagem de *Few-shot Prompting*, sendo incorporado diretamente no `Modelfile`.

- **Quantidade:** 10 pares de Pergunta/Resposta  
- **Origem:** Simulação de dúvidas reais baseadas em FAQs de bancos digitais  
- **Objetivo:** Ensinar o modelo a responder com clareza, segurança e contexto  

### 🔍 Temas abordados:
1. Consulta de saldo e extrato  
2. Procedimentos de segurança (cartão perdido, bloqueio)  
3. Explicação de rendimentos (CDI vs poupança)  
4. Operações financeiras (PIX, transferências)  

---

## 🧠 System Prompt & Decisões

O comportamento do assistente foi definido com foco em **segurança, clareza e experiência do usuário**.

```text
SYSTEM "Você é o NuAssist, um assistente de banco digital. Seja transparente e direto.

Regras:
1. Nunca peça senhas ou dados sensíveis.
2. Use português brasileiro simples e acessível.
3. Mantenha um tom amigável e profissional.
4. Evite termos técnicos sem explicação.
5. Se não souber algo, direcione o usuário para atendimento humano.
"

PARAMETER temperature 0.3
```
---

## 📚 Aprendizados

**Mateus de Oliveira Fernandes Neves**  
Durante o desenvolvimento do NuAssist, entendi na prática como a engenharia de prompt influencia o modelo. A expansão do dataset mostrou que mais exemplos aumentam a consistência, deixando as respostas mais claras e alinhadas ao System Prompt. Mesmo sem fine-tuning completo, o aumento de exemplos no contexto melhora o comportamento. O projeto também reforçou a importância de definir regras de segurança e linguagem para adaptar um modelo genérico a um domínio específico.

**Paulo Henrique Lira Bilac de Araujo**  
(Adicionar aprendizado individual)

**Olavo Dadario Vianna Barreto**  
(Adicionar aprendizado individual)

**Pedro Soares de Souza**  
(Adicionar aprendizado individual)

**Jhon Cutile Titirico**  
(Adicionar aprendizado individual)
