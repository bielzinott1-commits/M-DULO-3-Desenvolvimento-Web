# CURSO COMPLETO DE ENGENHARIA DE SOFTWARE

# Do Zero ao Desenvolvedor Full Stack

## VOLUME 3 — DESENVOLVIMENTO WEB

# CAPÍTULO 22

# HTML5 Completo — Construindo a Estrutura Profissional da Web

> **Objetivo do capítulo:** Ao final deste capítulo, você entenderá profundamente o HTML5, saberá criar páginas profissionais, utilizar elementos semânticos, construir formulários completos, trabalhar com multimídia, aplicar boas práticas de SEO e acessibilidade, além de organizar projetos seguindo padrões profissionais.

---

# Introdução

No capítulo anterior aprendemos como a Internet funciona.

Agora vamos começar a construir páginas reais.

Todo site que existe na Internet possui uma base:

# HTML

HTML é a estrutura de uma página.

Ele define:

* textos;
* imagens;
* botões;
* links;
* formulários;
* vídeos;
* organização do conteúdo.

Podemos comparar uma página web com uma casa:

```text
Casa

↓

HTML = Estrutura da casa

CSS = Pintura e decoração

JavaScript = Eletricidade e funcionalidades
```

---

# O que significa HTML?

HTML significa:

# HyperText Markup Language

Tradução:

**Linguagem de Marcação de Hipertexto**

Ele é responsável por marcar e organizar conteúdos.

---

# HTML é linguagem de programação?

Não.

HTML não possui:

* condições;
* loops;
* funções;
* cálculos.

Ele é uma linguagem de marcação.

Sua função é informar ao navegador:

"Este conteúdo é um título."

"Este conteúdo é uma imagem."

"Este conteúdo é um botão."

---

# História do HTML

O HTML foi criado em 1991 por:

Tim Berners-Lee

Com o objetivo de compartilhar documentos científicos.

Com o tempo evoluiu:

## HTML 1

Primeiras páginas simples.

---

## HTML 4

Adicionou recursos mais avançados.

---

## HTML5

Versão moderna utilizada atualmente.

Trouxe:

* multimídia;
* elementos semânticos;
* APIs;
* melhor estrutura.

---

# Como funciona uma página HTML?

O navegador lê o código:

```text
Código HTML

↓

Interpretação

↓

DOM

↓

Página visual
```

---

# Estrutura básica do HTML5

Todo documento HTML5 começa assim:

```html
<!DOCTYPE html>

<html>

<head>

<title>Minha página</title>

</head>


<body>

<h1>Olá Mundo</h1>

</body>

</html>
```

---

# Entendendo cada parte

## DOCTYPE

```html
<!DOCTYPE html>
```

Informa ao navegador que estamos usando HTML5.

---

# Tag HTML

```html
<html>
</html>
```

É o elemento principal da página.

Tudo fica dentro dela.

---

# Tag HEAD

```html
<head>

</head>
```

Contém informações invisíveis:

* título;
* configurações;
* links;
* metadados.

---

# Tag BODY

```html
<body>

</body>
```

É tudo aquilo que aparece para o usuário.

---

# Metadados

Metadados são informações sobre a página.

Exemplo:

```html
<meta charset="UTF-8">
```

Define a codificação dos caracteres.

Permite:

* acentos;
* símbolos;
* idiomas diferentes.

---

# Responsividade

Meta importante:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Ela faz o site funcionar corretamente em celulares.

---

# Título da página

```html
<title>
Meu Site
</title>
```

Aparece na aba do navegador.

---

# Estrutura de Pastas Profissional

Um projeto organizado:

```text
meu-site/

│

├── index.html

│

├── css/

│   └── style.css

│

├── js/

│   └── script.js

│

├── images/

│

└── assets/
```

---

# Tags de Texto

## Títulos

HTML possui seis níveis:

```html
<h1>Título Principal</h1>

<h2>Subtítulo</h2>

<h3>Seção</h3>

<h4></h4>

<h5></h5>

<h6></h6>
```

---

# Importância do H1

O H1 deve representar o assunto principal da página.

Exemplo:

```html
<h1>Curso de Programação</h1>
```

Normalmente utilizamos apenas um H1 por página.

---

# Parágrafos

```html
<p>
Este é um texto.
</p>
```

Usado para textos comuns.

---

# Formatação de texto

Negrito:

```html
<strong>
Texto importante
</strong>
```

---

Ênfase:

```html
<em>
Texto destacado
</em>
```

---

Texto pequeno:

```html
<small>
Observação
</small>
```

---

Texto marcado:

```html
<mark>
Importante
</mark>
```

---

# Quebra de linha

```html
<br>
```

---

# Linha horizontal

```html
<hr>
```

---

# Links

Links usam:

```html
<a>
```

Exemplo:

```html
<a href="https://github.com">

Meu GitHub

</a>
```

---

# Atributos importantes de links

Abrir nova aba:

```html
target="_blank"
```

Exemplo:

```html
<a 
href="site.com"
target="_blank">

Abrir

</a>
```

---

# Imagens

Tag:

```html
<img>
```

Exemplo:

```html
<img src="foto.jpg">
```

---

# Atributo ALT

Muito importante:

```html
<img 
src="foto.jpg"
alt="Foto do usuário">
```

Serve para:

* acessibilidade;
* SEO;
* descrição da imagem.

---

# Áudio

HTML5 permite áudio:

```html
<audio controls>

<source src="musica.mp3">

</audio>
```

---

# Vídeo

```html
<video controls>

<source src="video.mp4">

</video>
```

---

# Elementos Semânticos HTML5

Antes:

```html
<div>
```

era usado para tudo.

HTML5 trouxe elementos com significado.

---

# Header

Cabeçalho da página.

```html
<header>

Logo

Menu

</header>
```

---

# Navigation

Área de navegação.

```html
<nav>

Links

</nav>
```

---

# Main

Conteúdo principal.

```html
<main>

Conteúdo

</main>
```

---

# Section

Uma seção da página.

```html
<section>

Sobre nós

</section>
```

---

# Article

Conteúdo independente.

Exemplo:

* notícia;
* postagem.

```html
<article>

Texto

</article>
```

---

# Aside

Conteúdo lateral.

Exemplo:

* propaganda;
* informações extras.

---

# Footer

Rodapé.

```html
<footer>

Direitos reservados

</footer>
```

---

# Por que usar HTML semântico?

Melhora:

## SEO

Motores de busca entendem melhor a página.

---

## Acessibilidade

Leitores de tela conseguem interpretar.

---

## Organização

Código mais profissional.

---

# Listas

## Lista ordenada

Com números:

```html
<ol>

<li>HTML</li>

<li>CSS</li>

</ol>
```

Resultado:

1. HTML
2. CSS

---

## Lista não ordenada

Com pontos:

```html
<ul>

<li>JavaScript</li>

<li>React</li>

</ul>
```

---

# Tabelas

Estrutura:

```html
<table>

<tr>

<th>Nome</th>

<th>Idade</th>

</tr>


<tr>

<td>Davi</td>

<td>15</td>

</tr>

</table>
```

---

# Formulários HTML5

Formulários permitem receber informações.

Exemplo:

```html
<form>

</form>
```

---

# Input

Campo de entrada:

```html
<input>
```

---

# Tipos de Input

Texto:

```html
<input type="text">
```

---

Senha:

```html
<input type="password">
```

---

Email:

```html
<input type="email">
```

---

Número:

```html
<input type="number">
```

---

Data:

```html
<input type="date">
```

---

Arquivo:

```html
<input type="file">
```

---

Checkbox:

```html
<input type="checkbox">
```

---

Radio:

```html
<input type="radio">
```

---

# Labels

Relacionam texto com campos.

Exemplo:

```html
<label>

Nome:

</label>

<input type="text">
```

---

# Textarea

Área de texto grande:

```html
<textarea>

</textarea>
```

Usado para:

* mensagens;
* comentários.

---

# Select

Lista de opções:

```html
<select>

<option>

Brasil

</option>

</select>
```

---

# Botões

```html
<button>

Enviar

</button>
```

---

# Validação HTML5

HTML possui validações próprias.

Obrigatório:

```html
required
```

---

Exemplo:

```html
<input 
type="email"
required>
```

---

# SEO no HTML

SEO significa:

# Search Engine Optimization

São técnicas para melhorar o posicionamento nos buscadores.

---

# Meta Description

```html
<meta 
name="description"
content="Curso completo de programação">
```

---

# Estrutura correta de títulos

Ruim:

```html
<h1>
Título
</h1>

<h1>
Outro título
</h1>
```

Melhor:

```html
<h1>

Título principal

</h1>

<h2>

Subtítulo

</h2>
```

---

# Acessibilidade

A web deve ser acessível para todos.

Inclui pessoas utilizando:

* leitores de tela;
* teclado;
* tecnologias assistivas.

---

# Boas práticas

Use:

✔ ALT em imagens.

✔ HTML semântico.

✔ Labels em formulários.

✔ Contraste adequado.

✔ Textos descritivos nos links.

---

# HTML e CSS

Normalmente HTML se conecta ao CSS:

```html
<link 
rel="stylesheet"
href="style.css">
```

---

# HTML e JavaScript

Conexão:

```html
<script src="script.js">

</script>
```

---

# Projeto Prático do Capítulo

## Criar um site profissional de apresentação

Estrutura:

```text
portfolio/

├── index.html

├── css/

│   └── style.css

├── images/

└── js/

    └── script.js
```

---

O site deve possuir:

## Header

* Nome;
* Logo;
* Menu.

## Sobre

* Apresentação pessoal.

## Projetos

* Lista de trabalhos.

## Contato

* Formulário.

## Footer

* Redes sociais.

---

# Exercícios

1. O que significa HTML?
2. HTML é uma linguagem de programação?
3. Qual a função do DOCTYPE?
4. Qual diferença entre HEAD e BODY?
5. Para que serve a tag ALT?
6. Explique HTML semântico.
7. Qual diferença entre SECTION e ARTICLE?
8. Para que servem formulários?
9. O que é SEO?
10. Por que acessibilidade é importante?

---

# Resumo do Capítulo

Neste capítulo você aprendeu:

✅ História do HTML.
✅ Estrutura HTML5.
✅ Tags principais.
✅ Textos e links.
✅ Imagens, áudio e vídeo.
✅ Elementos semânticos.
✅ Formulários completos.
✅ SEO básico.
✅ Acessibilidade.
✅ Organização profissional de projetos.

---

# Próximo Capítulo

## Capítulo 23 — CSS3 Completo

No próximo capítulo você aprenderá a transformar páginas HTML simples em interfaces profissionais, dominando:

* seletores;
* cores;
* fontes;
* Box Model;
* Flexbox;
* Grid;
* animações;
* transições;
* layouts modernos;
* padrões utilizados por designers e desenvolvedores profissionais.
