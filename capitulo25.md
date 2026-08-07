# CURSO COMPLETO DE ENGENHARIA DE SOFTWARE

# Do Zero ao Desenvolvedor Full Stack

# VOLUME 3 — DESENVOLVIMENTO WEB

# CAPÍTULO 25

# JavaScript do Básico ao Avançado — A Linguagem que Dá Vida à Web

> **Objetivo do capítulo:** Ao final deste capítulo, você entenderá profundamente o JavaScript, aprenderá desde os fundamentos até conceitos avançados, será capaz de criar aplicações interativas, manipular dados, trabalhar com lógica, programação orientada a objetos e compreender como aplicações modernas funcionam no navegador.

---

# Introdução

Nos capítulos anteriores aprendemos:

* HTML → estrutura;
* CSS → aparência;
* UI/UX → experiência.

Agora falta a parte que dá **comportamento e inteligência** para uma página:

# JavaScript

Sem JavaScript, um site seria apenas uma página estática.

Com JavaScript podemos criar:

* menus interativos;
* jogos;
* sistemas de login;
* validações;
* animações;
* aplicações completas;
* sistemas web.

---

# O que é JavaScript?

JavaScript é uma linguagem de programação criada para tornar páginas web interativas.

Ela executa principalmente no navegador, mas atualmente também pode rodar no servidor através de tecnologias como Node.js.

---

# História do JavaScript

O JavaScript foi criado em 1995 por:

Brendan Eich

Inicialmente seu nome era:

```text
LiveScript
```

Depois passou a se chamar:

```text
JavaScript
```

Ele foi criado para adicionar interação às páginas da Web.

---

# JavaScript é igual Java?

Não.

Apesar dos nomes parecidos, são linguagens diferentes.

| JavaScript               | Java                                 |
| ------------------------ | ------------------------------------ |
| Linguagem Web            | Linguagem geral                      |
| Muito usada no Front-End | Muito usada em sistemas corporativos |
| Interpretada             | Compilada                            |
| Sintaxe mais flexível    | Mais rígida                          |

---

# Onde JavaScript é usado?

Hoje JavaScript está presente em:

## Front-End

Criar interfaces:

* sites;
* aplicativos web;
* jogos.

Tecnologias:

* React;
* Angular;
* Vue.

---

## Back-End

Com:

* Node.js;
* Express.

---

## Mobile

Com:

* React Native;
* Ionic.

---

## Desktop

Com:

* Electron.

---

# Como executar JavaScript

Existem três formas.

---

# 1. Dentro do HTML

```html
<script>

alert("Olá mundo");

</script>
```

---

# 2. Arquivo externo

Estrutura:

```text
projeto/

├── index.html

└── script.js
```

HTML:

```html
<script src="script.js"></script>
```

---

# 3. Console do navegador

Abra:

```text
F12

↓

Console
```

Digite:

```javascript
console.log("Olá");
```

---

# Primeiro código

```javascript
console.log("Olá mundo!");
```

Resultado:

```text
Olá mundo!
```

---

# Comentários

Comentários são textos ignorados pelo JavaScript.

Uma linha:

```javascript
// comentário
```

Várias linhas:

```javascript
/*
comentário
de várias linhas
*/
```

---

# Variáveis

Variáveis armazenam informações.

Exemplo:

```javascript
let nome = "Davi";
```

---

# Formas de criar variáveis

Existem três:

* var;
* let;
* const.

---

# var

Forma antiga.

```javascript
var idade = 15;
```

Atualmente é pouco utilizada.

---

# let

Valor pode mudar.

Exemplo:

```javascript
let pontos = 0;

pontos = 10;
```

---

# const

Valor não muda.

Exemplo:

```javascript
const pi = 3.14;
```

---

# Regras para nomes de variáveis

Correto:

```javascript
nomeUsuario

idade

totalCompra
```

Errado:

```javascript
1nome

nome usuário
```

---

# Tipos de Dados

JavaScript possui vários tipos.

---

# String

Texto.

```javascript
let nome = "Davi";
```

---

# Number

Números.

```javascript
let idade = 15;
```

---

# Boolean

Verdadeiro ou falso.

```javascript
let aprovado = true;
```

---

# Undefined

Valor não definido.

```javascript
let teste;
```

---

# Null

Ausência intencional de valor.

```javascript
let usuario = null;
```

---

# Object

Objetos.

```javascript
let pessoa = {

nome:"Davi",

idade:15

};
```

---

# Array

Lista de valores.

```javascript
let jogos = [

"Minecraft",

"Roblox",

"GTA"

];
```

---

# Verificando tipo

Usamos:

```javascript
typeof
```

Exemplo:

```javascript
typeof nome;
```

Resultado:

```text
string
```

---

# Operadores

## Matemáticos

```javascript
+

-

*

/

%
```

Exemplo:

```javascript
let soma = 5 + 5;
```

---

# Operadores de comparação

Maior:

```javascript
>
```

Menor:

```javascript
<
```

Igual:

```javascript
==
```

Igual absoluto:

```javascript
===
```

Diferente:

```javascript
!=
```

---

# Operadores lógicos

E:

```javascript
&&
```

Ou:

```javascript
||
```

Negação:

```javascript
!
```

---

# Entrada de dados

Usando:

```javascript
prompt()
```

Exemplo:

```javascript
let nome = prompt("Digite seu nome");
```

---

# Saída de dados

Console:

```javascript
console.log(nome);
```

Tela:

```javascript
alert(nome);
```

---

# Template Strings

Forma moderna de juntar textos.

Antes:

```javascript
"Olá " + nome
```

Agora:

```javascript
`Olá ${nome}`
```

Exemplo:

```javascript
let nome="Davi";

console.log(`Olá ${nome}`);
```

---

# Estruturas Condicionais

Permitem tomar decisões.

---

# IF

```javascript
if(condição){

}

```

Exemplo:

```javascript
let idade=18;

if(idade>=18){

console.log("Maior de idade");

}
```

---

# ELSE

```javascript
if(){

}else{

}
```

---

# ELSE IF

Várias condições:

```javascript
if(nota>=7){

}else if(nota>=5){

}else{

}
```

---

# SWITCH

Quando existem várias opções.

Exemplo:

```javascript
switch(dia){

case 1:

console.log("Segunda");

break;

}
```

---

# Estruturas de Repetição

Servem para repetir código.

---

# FOR

Quando sabemos a quantidade.

```javascript
for(let i=0;i<10;i++){

console.log(i);

}
```

---

# WHILE

Enquanto uma condição for verdadeira.

```javascript
while(condicao){

}
```

---

# DO WHILE

Executa pelo menos uma vez.

```javascript
do{

}while(condicao);
```

---

# Funções

Funções são blocos reutilizáveis.

Exemplo:

```javascript
function saudacao(){

console.log("Olá");

}
```

Executando:

```javascript
saudacao();
```

---

# Parâmetros

Recebem valores.

```javascript
function soma(a,b){

return a+b;

}
```

---

# Return

Retorna um valor.

```javascript
return resultado;
```

---

# Arrow Functions

Forma moderna:

Antes:

```javascript
function soma(a,b){

return a+b;

}
```

Depois:

```javascript
const soma=(a,b)=>{

return a+b;

}
```

---

# Arrays

Coleções de dados.

Exemplo:

```javascript
let frutas=[

"maçã",

"banana"

];
```

---

# Acessando valores

```javascript
frutas[0];
```

Resultado:

```text
maçã
```

---

# Métodos de Arrays

Adicionar:

```javascript
push()
```

Remover:

```javascript
pop()
```

Tamanho:

```javascript
length
```

---

# Map

Transforma elementos.

```javascript
array.map()
```

---

# Filter

Filtra dados.

```javascript
array.filter()
```

---

# Reduce

Reduz valores.

```javascript
array.reduce()
```

---

# Objetos

Representam entidades.

Exemplo:

```javascript
const usuario={

nome:"Davi",

idade:15,

ativo:true

};
```

---

# Acessando propriedades

Ponto:

```javascript
usuario.nome;
```

Colchetes:

```javascript
usuario["nome"];
```

---

# Desestruturação

Forma moderna:

```javascript
const {nome,idade}=usuario;
```

---

# JSON

Formato usado para comunicação entre sistemas.

Exemplo:

```json
{
"nome":"Davi",
"idade":15
}
```

---

# Programação Orientada a Objetos

JavaScript suporta POO.

Conceitos:

* classes;
* objetos;
* métodos;
* herança.

---

# Classe

```javascript
class Pessoa{

constructor(nome){

this.nome=nome;

}

}
```

---

# Criando objeto

```javascript
let pessoa=new Pessoa("Davi");
```

---

# Herança

Uma classe pode aproveitar outra.

```javascript
class Aluno extends Pessoa{

}
```

---

# Tratamento de Erros

Usamos:

```javascript
try{

}catch(erro){

}
```

Exemplo:

```javascript
try{

codigo();

}catch(error){

console.log(error);

}
```

---

# Programação Assíncrona

Muitas tarefas demoram:

* buscar dados;
* acessar API;
* carregar arquivos.

JavaScript utiliza:

* callbacks;
* promises;
* async/await.

---

# Callback

Uma função executada depois.

---

# Promise

Representa uma operação futura.

Estados:

```text
Pending

↓

Fulfilled

ou

Rejected
```

---

# Async/Await

Forma moderna.

Exemplo:

```javascript
async function buscar(){

let dados = await fetch(url);

}
```

---

# Event Loop

JavaScript é baseado em eventos.

Ele consegue executar várias tarefas utilizando:

* Call Stack;
* Web APIs;
* Callback Queue.

---

# Módulos

Permitem dividir código.

Exportar:

```javascript
export
```

Importar:

```javascript
import
```

---

# Boas práticas JavaScript

✔ Use nomes claros.

✔ Evite código repetido.

✔ Utilize const quando possível.

✔ Organize arquivos.

✔ Faça comentários quando necessário.

✔ Aprenda ES6+.

✔ Utilize ferramentas modernas.

---

# Projeto Prático

## Criar um Sistema de Cadastro de Usuários

Funcionalidades:

* adicionar usuários;
* remover usuários;
* listar usuários;
* pesquisar usuários.

Utilizar:

✅ Variáveis
✅ Funções
✅ Arrays
✅ Objetos
✅ Condições
✅ Loops
✅ Manipulação de dados

---

# Exercícios

1. O que é JavaScript?
2. Qual diferença entre let e const?
3. Explique tipos de dados.
4. Para que servem funções?
5. O que é um array?
6. Explique objetos.
7. Qual diferença entre == e ===?
8. O que é uma Promise?
9. Para que serve async/await?
10. Explique o Event Loop.

---

# Resumo do Capítulo

Neste capítulo você aprendeu:

✅ História do JavaScript.
✅ Como executar JavaScript.
✅ Variáveis.
✅ Tipos de dados.
✅ Operadores.
✅ Condições.
✅ Loops.
✅ Funções.
✅ Arrays.
✅ Objetos.
✅ JSON.
✅ Programação Orientada a Objetos.
✅ Tratamento de erros.
✅ Programação assíncrona.
✅ Conceitos modernos do JavaScript.

---

# Próximo Capítulo

# Capítulo 26 — DOM e Eventos

No próximo capítulo você aprenderá a controlar páginas HTML com JavaScript, criando:

* alterações dinâmicas;
* botões interativos;
* formulários inteligentes;
* validações;
* animações;
* aplicações completas no navegador.
