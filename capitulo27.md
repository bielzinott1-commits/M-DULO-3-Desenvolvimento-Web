# CURSO COMPLETO DE ENGENHARIA DE SOFTWARE

# Do Zero ao Desenvolvedor Full Stack

# VOLUME 3 — DESENVOLVIMENTO WEB

# CAPÍTULO 27

# APIs e Consumo de Dados — Conectando Aplicações com o Mundo Real

> **Objetivo do capítulo:** Ao final deste capítulo, você entenderá o que são APIs, como sistemas se comunicam, como consumir dados externos utilizando JavaScript, trabalhar com JSON, requisições HTTP, autenticação, tratamento de erros e criar aplicações conectadas a serviços reais.

---

# Introdução

Até agora aprendemos a criar páginas e aplicações que funcionam no navegador.

Porém, aplicações modernas precisam de informações externas.

Exemplos:

* aplicativo de clima precisa da previsão do tempo;
* loja virtual precisa dos produtos;
* banco precisa consultar contas;
* redes sociais precisam carregar publicações.

Como esses sistemas trocam informações?

A resposta é:

# APIs

---

# O que é uma API?

API significa:

# Application Programming Interface

Tradução:

**Interface de Programação de Aplicações**

Uma API é uma ponte que permite que dois sistemas conversem.

Exemplo:

```text id="7j9v1q"
Aplicativo

↓

API

↓

Servidor

↓

Banco de Dados
```

---

# Exemplo do Mundo Real

Imagine um restaurante.

Você é o cliente.

A cozinha é o servidor.

O garçom é a API.

Você não entra na cozinha.

Você faz um pedido ao garçom.

A API faz exatamente isso:

Recebe uma solicitação e entrega uma resposta.

---

# Por que APIs existem?

Sem APIs:

* cada aplicativo precisaria criar tudo sozinho;
* sistemas não conseguiriam compartilhar informações;
* aplicações seriam mais lentas para desenvolver.

Com APIs:

* reutilizamos serviços;
* conectamos sistemas;
* criamos aplicações maiores.

---

# Tipos de API

Existem vários tipos.

---

# API Web

Usada através da Internet.

Exemplo:

```text id="2v4r8z"
Aplicação Web

↓

API HTTP

↓

Servidor
```

---

# API REST

É o padrão mais utilizado atualmente.

REST significa:

# Representational State Transfer

Ela utiliza:

* HTTP;
* URLs;
* métodos de requisição.

---

# API SOAP

Modelo mais antigo.

Muito usado em sistemas empresariais antigos.

---

# API GraphQL

Permite solicitar exatamente os dados necessários.

Criada pelo:

Meta Platforms

---

# Como uma API funciona?

Fluxo:

```text id="h0g8q6"
Usuário

↓

Front-End

↓

Requisição HTTP

↓

API

↓

Servidor

↓

Banco de Dados

↓

Resposta JSON

↓

Interface atualizada
```

---

# Requisições HTTP

As aplicações conversam usando HTTP.

Principais métodos:

---

# GET

Buscar informações.

Exemplo:

```text id="7j0l0p"
Buscar produtos
```

---

# POST

Enviar dados.

Exemplo:

```text id="j9v7n2"
Criar usuário
```

---

# PUT

Atualizar completamente.

Exemplo:

```text id="0c4b5a"
Atualizar perfil
```

---

# PATCH

Atualizar parcialmente.

Exemplo:

```text id="8m4d0r"
Alterar apenas nome
```

---

# DELETE

Remover dados.

Exemplo:

```text id="4y8z2f"
Excluir conta
```

---

# Estrutura de uma URL de API

Exemplo:

```text id="8x6s4p"
https://api.site.com/users
```

Dividindo:

```text id="u8m2hw"
https://

↓

Protocolo


api.site.com

↓

Servidor


/users

↓

Recurso
```

---

# JSON

JSON significa:

# JavaScript Object Notation

É o formato mais usado para enviar dados.

Exemplo:

```json
{
 "nome":"Davi",
 "idade":15,
 "curso":"Programação"
}
```

---

# JSON x Objeto JavaScript

Objeto:

```javascript
const usuario={

nome:"Davi"

};
```

JSON:

```json
{
"nome":"Davi"
}
```

A aparência é parecida, mas possuem diferenças.

---

# Convertendo JSON

Objeto para JSON:

```javascript
JSON.stringify()
```

JSON para objeto:

```javascript
JSON.parse()
```

---

# Fetch API

O JavaScript possui uma ferramenta nativa para acessar APIs:

```javascript
fetch()
```

---

# Primeira requisição

Exemplo:

```javascript
fetch("https://api.exemplo.com")

.then(response => {

return response.json();

})

.then(data => {

console.log(data);

});
```

---

# Entendendo o código

Primeiro:

```javascript
fetch()
```

Faz o pedido.

---

Depois:

```javascript
response.json()
```

Transforma resposta em objeto.

---

Finalmente:

```javascript
console.log(data)
```

Mostra os dados.

---

# Async/Await com Fetch

Forma moderna:

```javascript
async function buscarDados(){

const resposta =
await fetch(url);

const dados =
await resposta.json();

console.log(dados);

}
```

---

# Tratamento de Erros

Nem toda requisição funciona.

Pode acontecer:

* servidor desligado;
* Internet falhar;
* endereço errado.

Usamos:

```javascript
try {

}

catch(error){

}
```

Exemplo:

```javascript
async function buscar(){

try{

const resposta =
await fetch(url);

}

catch(error){

console.log(error);

}

}
```

---

# Status HTTP em APIs

A resposta possui códigos.

---

## 200

Sucesso.

---

## 201

Criado.

---

## 400

Dados inválidos.

---

## 401

Usuário não autenticado.

---

## 403

Sem permissão.

---

## 404

Não encontrado.

---

## 500

Erro no servidor.

---

# Headers

Headers carregam informações extras.

Exemplo:

```text id="6k5m0e"
Tipo de conteúdo

Autorização

Idioma
```

---

# Content-Type

Define o formato enviado.

Exemplo:

```text id="7t2k4v"
application/json
```

---

# APIs com Autenticação

Muitas APIs precisam saber quem está acessando.

Existem métodos:

---

# API Key

Uma chave simples.

Exemplo:

```text id="9p8q4w"
API_KEY=123456
```

---

# Bearer Token

Usado no Header.

Exemplo:

```http
Authorization:
Bearer TOKEN
```

---

# JWT

JSON Web Token.

Formato:

```text id="5m1r7z"
Header

.

Payload

.

Signature
```

Muito usado em sistemas de login.

---

# CORS

Significa:

# Cross-Origin Resource Sharing

É uma proteção do navegador.

Exemplo:

Seu site:

```text
meusite.com
```

Quer acessar:

```text
api.com
```

O servidor precisa permitir.

---

# Consumindo uma API Pública

Exemplo de aplicações:

## Clima

Recebe:

* temperatura;
* localização;
* previsão.

---

## Filmes

Recebe:

* título;
* imagem;
* avaliação.

---

## Notícias

Recebe:

* manchetes;
* categorias.

---

# Criando uma Aplicação com API

Exemplo:

## Aplicativo de Clima

Fluxo:

```text id="9d6j3m"
Usuário digita cidade

↓

JavaScript envia GET

↓

API responde JSON

↓

Dados aparecem na tela
```

---

# Exemplo de Código

HTML:

```html
<input id="cidade">

<button id="buscar">

Buscar

</button>

<div id="resultado"></div>
```

JavaScript:

```javascript
buscar.onclick = async()=>{

const cidade =
document.querySelector("#cidade").value;


const resposta =
await fetch(url);


const dados =
await resposta.json();


resultado.innerHTML =
dados.temperatura;

}
```

---

# Axios

Além do Fetch existe o Axios.

Ele é uma biblioteca JavaScript.

Instalação:

```bash
npm install axios
```

---

# Exemplo Axios

```javascript
axios.get(url)

.then(response=>{

console.log(response.data);

});
```

---

# Fetch x Axios

| Fetch                           | Axios                              |
| ------------------------------- | ---------------------------------- |
| Nativo do navegador             | Biblioteca externa                 |
| Mais simples                    | Mais recursos                      |
| Precisa tratar JSON manualmente | Faz automaticamente                |
| Menos código                    | Mais utilizado em projetos grandes |

---

# Boas práticas ao trabalhar com APIs

✔ Nunca exponha chaves secretas.

✔ Sempre trate erros.

✔ Valide dados recebidos.

✔ Documente suas APIs.

✔ Use HTTPS.

✔ Controle permissões.

✔ Não confie totalmente nos dados externos.

---

# Documentação de APIs

Todo desenvolvedor precisa saber ler documentação.

Ela informa:

* URL;
* parâmetros;
* métodos;
* respostas;
* autenticação.

---

# Ferramentas para APIs

## Postman

Permite testar APIs.

---

## Insomnia

Alternativa ao Postman.

---

## Swagger

Documentação automática de APIs.

---

# Projeto Prático

## Criar um Aplicativo de Previsão do Tempo

Tecnologias:

* HTML5
* CSS3
* JavaScript
* API REST

Funcionalidades:

✅ Campo para cidade
✅ Botão pesquisar
✅ Consumo de API
✅ Exibir temperatura
✅ Mostrar condição climática
✅ Tratar erros

Estrutura:

```text
clima-app/

├── index.html

├── style.css

└── script.js
```

---

# Exercícios

1. O que significa API?
2. Explique o funcionamento de uma API REST.
3. Qual diferença entre GET e POST?
4. O que é JSON?
5. Para que serve fetch?
6. O que é uma Promise?
7. Explique async/await.
8. O que são tokens?
9. O que significa CORS?
10. Por que documentação de API é importante?

---

# Resumo do Capítulo

Neste capítulo você aprendeu:

✅ O conceito de API.
✅ Comunicação entre sistemas.
✅ Arquitetura REST.
✅ Métodos HTTP.
✅ JSON.
✅ Fetch API.
✅ Async/Await.
✅ Tratamento de erros.
✅ Status HTTP.
✅ Headers.
✅ Autenticação.
✅ JWT.
✅ CORS.
✅ Axios.
✅ Testes de APIs.
✅ Criação de aplicações conectadas.

---

# Próximo Capítulo

# Capítulo 28 — Projetos Web Completos

No próximo capítulo você aplicará tudo que aprendeu criando projetos reais:

* Landing Page profissional;
* Portfólio;
* Sistema de login;
* Dashboard;
* Loja virtual;
* Blog;
* Sistema de Ordem de Serviço;
* Aplicações consumindo APIs;
* Projetos preparados para GitHub e portfólio profissional.
