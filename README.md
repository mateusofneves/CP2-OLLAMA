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
## Descrição Curta

O NuAssist é um assistente virtual bancário desenvolvido com Ollama, projetado para oferecer suporte rápido, claro e seguro aos usuários de bancos digitais. Utilizando técnicas de few-shot prompting, o sistema responde dúvidas comuns sobre operações financeiras, segurança e investimentos, traduzindo termos complexos em uma linguagem acessível. Seu foco está na experiência do usuário, garantindo respostas objetivas sem comprometer boas práticas de segurança.

## Descrição Longa

O NuAssist é um assistente virtual inteligente voltado para o setor financeiro, desenvolvido com o uso do Ollama e customizado por meio de um Modelfile. O projeto tem como principal objetivo melhorar a comunicação entre usuários e serviços bancários digitais, oferecendo respostas rápidas, compreensíveis e seguras para dúvidas comuns do dia a dia.

Diferente de muitos assistentes tradicionais, que utilizam linguagem excessivamente técnica ou respostas genéricas, o NuAssist foi projetado com foco em acessibilidade. Ele traduz conceitos financeiros — como rendimento baseado em CDI, transferências e uso de PIX — para uma linguagem simples, mantendo a precisão das informações. Isso reduz barreiras de entendimento e melhora a experiência do usuário, especialmente para pessoas com menor familiaridade com o sistema financeiro.

O modelo foi estruturado utilizando a abordagem de few-shot prompting, com um conjunto de perguntas e respostas inspirado em situações reais de atendimento bancário. Esse dataset permite que a IA compreenda diferentes formas de formular uma mesma dúvida, aumentando sua capacidade de interpretação e resposta. Além disso, o comportamento do assistente é guiado por um system prompt que define regras essenciais, como a proibição de solicitar dados sensíveis, o uso de linguagem clara e a orientação ao atendimento humano quando necessário.

Outro ponto fundamental do projeto é a ênfase em segurança. O NuAssist foi projetado para nunca solicitar informações confidenciais, reforçando boas práticas digitais e protegendo o usuário contra possíveis riscos. Essa preocupação é essencial no contexto bancário, onde confiança e proteção de dados são prioridades.

Em resumo, o NuAssist demonstra como é possível adaptar modelos de linguagem para um domínio específico, combinando engenharia de prompt, curadoria de dados e definição de regras para criar um assistente eficiente, seguro e centrado no usuário.

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
Neste projeto, aprendi a utilizar o Ollama para criar um chatbot com IA local, entendendo como o system prompt e os exemplos influenciam diretamente nas respostas do modelo. Também desenvolvi a integração com a API e organizei a estrutura do código, incluindo histórico de conversa e menu interativo, melhorando a experiência do usuário. Além disso, compreendi na prática como adaptar um modelo genérico para um contexto específico, como o atendimento bancário, aplicando conceitos de engenharia de prompt e organização de dados.

**Pedro Soares de Souza**  
Neste projeto, aprendi a usar o Modelfile do Ollama para personalizar o modelo de IA. Configurei o modelo base, defini regras com o system prompt e utilizei exemplos (few-shot) para ensinar o assistente a responder como um suporte de banco digital.
Percebi que o modelo não aprende sozinho permanentemente, mas segue as instruções fornecidas. Por isso, a qualidade depende do dataset e das regras definidas.

**Jhon Cutile Titirico**  
Após o Desenvolvimento do projeto do NuAssist, compreendi como o modelo de IA pode ser influenciado por conversas, dados e treinos para oferecer suporte e dados aos usuarios que utilizam o chatbot, um modelo que se adapta com base nas intruções fornecidas com o dataset, deixando mais consciente das suas falas sendo alinhadas ao banco de dados do banco, sendo importante definir regras rigidas de segurança e linguagem pra comunicar e se adaptar em frente a comunicação humana para não causar erros e vulnerabilidades.
