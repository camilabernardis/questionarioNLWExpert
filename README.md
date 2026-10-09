<div align="center">

# 🧠 Questionário NLW Expert

**Teste seus conhecimentos de JavaScript e acompanhe seus acertos em tempo real.**

Projeto desenvolvido durante a imersão **NLW Expert**.

<br />

[![Ver online](https://img.shields.io/badge/🌐_Ver_projeto_online-8257e5?style=for-the-badge&labelColor=1a1a1a)](https://camilabernardis.github.io/questionarioNLWExpert/)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-222222?style=flat-square&logo=github&logoColor=white)

</div>

---

## 📖 Sobre o projeto

O **Questionário NLW Expert** é um quiz interativo com **10 perguntas sobre os fundamentos do JavaScript**. A cada resposta marcada, o placar de acertos é atualizado na hora (por exemplo: *"Acertos 3 de 10"*).

Foi feito durante a imersão **NLW Expert**, e é o projeto em que dei meus primeiros passos usando o **JavaScript "por trás das câmeras"**: o HTML tem só um modelo de pergunta, e é o código que monta a página inteira.

## ✨ Funcionalidades

- 10 perguntas de múltipla escolha sobre JavaScript (variáveis, DOM, callbacks, closures, JSON e mais)
- Perguntas e respostas geradas dinamicamente pelo JavaScript
- Contador de acertos atualizado em tempo real
- Possibilidade de trocar a resposta: o placar se ajusta automaticamente

## ⚙️ Como funciona por trás das câmeras

Toda a lógica está no `index.js`, e funciona em poucos passos:

**1. As perguntas são dados, não HTML.** Ficam em uma lista de objetos, cada um com a pergunta, as opções de resposta e o índice da resposta correta:

```js
{
  pergunta: "O que é o DOM em JavaScript?",
  respostas: ["Data Object Model", "Document Object Model", "Dynamic Object Model"],
  correta: 1
}
```

**2. O HTML tem só um modelo.** Uma tag `<template>` serve de molde para uma pergunta.

**3. Um laço de repetição monta tudo.** Para cada pergunta da lista, o código:

- copia o molde com `cloneNode`
- troca o título pelo texto da pergunta
- cria uma opção de resposta para cada alternativa e agrupa todas elas na mesma pergunta
- adiciona o resultado na tela com `appendChild`

**4. Os acertos são controlados com um `Set`.** Quando a pessoa marca uma resposta, o evento `onchange` verifica se ela é a correta. A pergunta é sempre removida do conjunto antes e só entra de novo se a resposta estiver certa. Assim, mudar de ideia não duplica nem perde pontos. Por fim, o texto do placar é atualizado com o tamanho do conjunto.

> Para adicionar uma nova pergunta, basta incluir mais um objeto na lista. Não precisa mexer no HTML. 🎯

## 🛠️ Tecnologias

- **HTML5**: estrutura da página e `<template>` das perguntas
- **CSS3**: estilização, incluindo a propriedade `content`
- **JavaScript**: arrays, objetos, laços de repetição, eventos e manipulação do DOM

## 📂 Estrutura do projeto

```
questionarioNLWExpert/
├── index.html    # Estrutura da página e template das perguntas
├── style.css     # Estilos
├── index.js      # Lista de perguntas e lógica do questionário
└── README.md
```

## 🚀 Como rodar localmente

```bash
# 1. Clone o repositório
git clone https://github.com/camilabernardis/questionarioNLWExpert.git

# 2. Entre na pasta
cd questionarioNLWExpert

# 3. Abra o index.html no navegador
```

Não precisa instalar nada, é só abrir o `index.html`. 😉

## 💡 Maiores aprendizados

- **Laços de repetição** para criar vários elementos a partir de uma lista de dados
- **Manipulação do DOM**: `querySelector`, `cloneNode`, `appendChild` e `textContent`
- **Eventos** (`onchange`) para reagir às respostas da pessoa
- **`Set`** para controlar os acertos sem duplicidade
- **CSS `content`** para inserir conteúdo direto pelo CSS
- Publicação de um projeto com **GitHub Pages**

Apesar de ser um projeto simples, foi um dos que mais me ajudaram a enxergar como o JavaScript dá vida às páginas.

## 🙏 Agradecimentos

À equipe da **NLW Expert** pela imersão e por tornar o aprendizado tão prático e divertido.

## 👩‍💻 Autora

**Camila Bernardi**

[![GitHub](https://img.shields.io/badge/GitHub-camilabernardis-181717?style=flat-square&logo=github)](https://github.com/camilabernardis)

---

<div align="center">

Feito com 💜 durante a imersão.

⭐ Se gostou do projeto, deixa uma estrelinha!

</div>
