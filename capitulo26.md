# CURSO COMPLETO DE ENGENHARIA DE SOFTWARE

# Do Zero ao Desenvolvedor Full Stack

# VOLUME 3 — DESENVOLVIMENTO WEB

# CAPÍTULO 26

# DOM e Eventos — Controlando e Criando Interfaces Dinâmicas com JavaScript

> **Objetivo do capítulo:** Ao final deste capítulo, você entenderá como o JavaScript se comunica com o HTML através do DOM, aprenderá a modificar elementos da página, criar interações, controlar eventos, validar formulários e desenvolver aplicações web dinâmicas.

---

# Introdução

No capítulo anterior aprendemos JavaScript.

Porém, uma pergunta importante:

> Como o JavaScript consegue alterar uma página HTML que já está aberta no navegador?

A resposta é:

# DOM

---

# O que é DOM?

DOM significa:

# Document Object Model

Tradução:

**Modelo de Objetos do Documento**

O DOM é uma representação da página HTML em forma de árvore de objetos.

Ele permite que o JavaScript:

* encontre elementos;
* altere textos;
* modifique estilos;
* crie novos elementos;
* remova conteúdos;
* responda a ações do usuário.

---

# HTML sem DOM

Imagine:

```html
<h1>
Olá Mundo
</h1>
```

O navegador apenas exibe.

---

# HTML com DOM

O navegador transforma:

```text
HTML

↓

DOM

↓

JavaScript consegue manipular
```

---

# Como funciona a árvore DOM?

Exemplo HTML:

```html
<html>

<body>

<h1>Título</h1>

<p>Texto</p>

</body>

</html>
```

Representação:

```text
Document

 └── html

      └── body

            ├── h1

            └── p
```

Cada elemento é um objeto.

---

# Objeto Document

O JavaScript acessa a página através de:

```javascript
document
```

Exemplo:

```javascript
console.log(document);
```

Mostra toda a estrutura da página.

---

# Selecionando elementos

Para modificar algo primeiro precisamos encontrar o elemento.

---

# getElementById()

Busca pelo ID.

HTML:

```html
<h1 id="titulo">
Olá
</h1>
```

JavaScript:

```javascript
const titulo =
document.getElementById("titulo");
```

---

# getElementsByClassName()

Busca por classe.

HTML:

```html
<p class="texto">
Texto
</p>
```

JavaScript:

```javascript
document.getElementsByClassName("texto");
```

---

# getElementsByTagName()

Busca pela tag.

Exemplo:

```javascript
document.getElementsByTagName("p");
```

---

# querySelector()

Forma moderna.

Busca o primeiro elemento encontrado.

ID:

```javascript
document.querySelector("#titulo");
```

Classe:

```javascript
document.querySelector(".texto");
```

Tag:

```javascript
document.querySelector("p");
```

---

# querySelectorAll()

Busca todos os elementos.

Exemplo:

```javascript
document.querySelectorAll(".card");
```

---

# Alterando conteúdos

## innerHTML

Permite alterar HTML interno.

Exemplo:

```javascript
titulo.innerHTML="Novo título";
```

Resultado:

```text
Novo título
```

---

# textContent

Altera apenas texto.

Exemplo:

```javascript
titulo.textContent="Olá";
```

Mais seguro para textos.

---

# Alterando atributos

HTML:

```html
<img id="foto" src="a.jpg">
```

JavaScript:

```javascript
foto.src="b.jpg";
```

---

# Alterando classes

Muito utilizado em interfaces.

Adicionar:

```javascript
elemento.classList.add("ativo");
```

Remover:

```javascript
elemento.classList.remove("ativo");
```

Alternar:

```javascript
elemento.classList.toggle("ativo");
```

---

# Alterando CSS pelo JavaScript

Exemplo:

```javascript
titulo.style.color="red";
```

Outro exemplo:

```javascript
caixa.style.backgroundColor="blue";
```

---

# Criando elementos

JavaScript pode criar HTML.

Exemplo:

```javascript
const p =
document.createElement("p");
```

Adicionar texto:

```javascript
p.textContent="Novo texto";
```

Adicionar na página:

```javascript
document.body.appendChild(p);
```

---

# Removendo elementos

Exemplo:

```javascript
elemento.remove();
```

---

# Navegação pelo DOM

É possível acessar elementos relacionados.

Pai:

```javascript
elemento.parentElement;
```

Filhos:

```javascript
elemento.children;
```

Irmãos:

```javascript
elemento.nextElementSibling;
```

---

# Eventos

Eventos são ações que acontecem na página.

Exemplos:

* clique;
* teclado;
* movimento do mouse;
* envio de formulário;
* carregamento.

---

# Clique (click)

HTML:

```html
<button id="botao">
Clique
</button>
```

JavaScript:

```javascript
botao.onclick=function(){

alert("Clicou!");

}
```

---

# addEventListener()

Forma profissional.

Estrutura:

```javascript
elemento.addEventListener(
evento,
função
);
```

Exemplo:

```javascript
botao.addEventListener(
"click",
()=>{
alert("Olá");
}
);
```

---

# Eventos de Mouse

## click

Clique.

```javascript
click
```

---

## dblclick

Dois cliques.

```javascript
dblclick
```

---

## mouseover

Mouse entra.

```javascript
mouseover
```

---

## mouseout

Mouse sai.

```javascript
mouseout
```

---

# Eventos de Teclado

## keydown

Tecla pressionada.

```javascript
keydown
```

---

## keyup

Tecla liberada.

```javascript
keyup
```

---

Exemplo:

```javascript
document.addEventListener(
"keydown",
(event)=>{

console.log(event.key);

});
```

---

# Evento Submit

Usado em formulários.

HTML:

```html
<form id="form">

<input>

<button>

Enviar

</button>

</form>
```

JavaScript:

```javascript
form.addEventListener(
"submit",
(e)=>{

e.preventDefault();

});
```

---

# preventDefault()

Impede o comportamento padrão.

Exemplo:

Formulário normalmente recarrega a página.

Com:

```javascript
e.preventDefault();
```

Ele não recarrega.

---

# Objeto Event

Todo evento possui informações.

Exemplo:

```javascript
botao.addEventListener(
"click",
(event)=>{

console.log(event);

});
```

Ele informa:

* elemento;
* posição;
* tecla;
* tipo do evento.

---

# Propagação de Eventos

Eventos podem se espalhar pela árvore DOM.

Exemplo:

```text
Div

 └── Botão
```

Clicar no botão pode ativar o pai.

Isso é chamado:

# Bubbling

---

# Capturing

O evento começa no elemento superior e desce.

Fluxo:

```text
Document

↓

Body

↓

Botão
```

---

# Delegação de Eventos

Técnica profissional.

Em vez de adicionar eventos em vários elementos:

```javascript
item1
item2
item3
```

Colocamos no pai:

```javascript
lista.addEventListener()
```

Benefícios:

* melhor desempenho;
* código menor.

---

# Formulários Dinâmicos

Exemplo:

Campo:

```html
<input id="nome">
```

Capturar valor:

```javascript
nome.value;
```

Alterar:

```javascript
nome.value="Davi";
```

---

# Validação de Formulários

Exemplo:

```javascript
if(nome.value===""){

alert("Digite seu nome");

}
```

---

# Expressões Regulares (Regex)

Usadas para validar padrões.

Exemplo:

Email:

```text
usuario@email.com
```

Telefone:

```text
(47)99999-9999
```

---

# LocalStorage

Permite guardar dados no navegador.

Salvar:

```javascript
localStorage.setItem(
"nome",
"Davi"
);
```

Buscar:

```javascript
localStorage.getItem("nome");
```

---

# Remover dados:

```javascript
localStorage.removeItem("nome");
```

---

# SessionStorage

Parecido com LocalStorage.

Diferença:

* LocalStorage permanece;
* SessionStorage desaparece ao fechar a aba.

---

# JSON e LocalStorage

Normalmente salvamos objetos:

Objeto:

```javascript
{
nome:"Davi",
idade:15
}
```

Converter:

```javascript
JSON.stringify()
```

Voltar:

```javascript
JSON.parse()
```

---

# Exemplo de Aplicação DOM

## Lista de tarefas

HTML:

```html
<input id="tarefa">

<button id="adicionar">

Adicionar

</button>

<ul id="lista">

</ul>
```

JavaScript:

```javascript
adicionar.onclick=function(){

let texto=tarefa.value;

lista.innerHTML +=
`<li>${texto}</li>`;

}
```

Resultado:

Uma lista funcionando.

---

# Animações com DOM

Exemplo:

Adicionar classe:

```javascript
elemento.classList.add("mostrar");
```

CSS:

```css
.mostrar{

opacity:1;

}
```

---

# Boas práticas DOM

✔ Evite alterar muitos elementos ao mesmo tempo.

✔ Utilize classes CSS em vez de muito style direto.

✔ Organize seus eventos.

✔ Use nomes claros.

✔ Separe HTML, CSS e JavaScript.

✔ Evite código repetido.

---

# Projeto Prático

## Criar um Sistema de Lista de Tarefas (To-Do List)

Funcionalidades:

✅ Adicionar tarefa
✅ Remover tarefa
✅ Marcar como concluída
✅ Salvar no LocalStorage
✅ Filtrar tarefas

Utilizar:

* HTML5
* CSS3
* JavaScript
* DOM
* Eventos

Estrutura:

```text
todo-list/

├── index.html

├── style.css

└── script.js
```

---

# Exercícios

1. O que significa DOM?
2. Como o JavaScript acessa o HTML?
3. Qual diferença entre querySelector e querySelectorAll?
4. Para que serve innerHTML?
5. O que é um evento?
6. Explique addEventListener.
7. Para que serve preventDefault?
8. O que é LocalStorage?
9. Explique Event Bubbling.
10. Crie um botão que altera uma mensagem na tela.

---

# Resumo do Capítulo

Neste capítulo você aprendeu:

✅ O conceito de DOM.
✅ Árvore de elementos HTML.
✅ Seleção de elementos.
✅ Manipulação de conteúdo.
✅ Alteração de estilos.
✅ Criação e remoção de elementos.
✅ Eventos JavaScript.
✅ addEventListener.
✅ Eventos de mouse e teclado.
✅ Formulários e validações.
✅ LocalStorage e SessionStorage.
✅ Delegação de eventos.
✅ Criação de aplicações interativas.

---

# Próximo Capítulo

# Capítulo 27 — APIs e Consumo de Dados

No próximo capítulo você aprenderá como conectar suas aplicações com serviços externos, trabalhando com:

* APIs;
* REST;
* JSON;
* Fetch API;
* Axios;
* métodos HTTP;
* autenticação;
* tokens;
* integração com dados reais.
