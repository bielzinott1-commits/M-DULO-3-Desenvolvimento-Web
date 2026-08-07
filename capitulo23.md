# CURSO COMPLETO DE ENGENHARIA DE SOFTWARE

# Do Zero ao Desenvolvedor Full Stack

# VOLUME 3 — DESENVOLVIMENTO WEB

# CAPÍTULO 23

# CSS3 Completo — Criando Interfaces Profissionais e Designs Modernos

> **Objetivo do capítulo:** Ao final deste capítulo, você dominará o CSS3, entenderá como estilizar páginas HTML, criar layouts profissionais, desenvolver interfaces responsivas, utilizar Flexbox e Grid, criar animações e aplicar conceitos utilizados por desenvolvedores Front-End no mercado.

---

# Introdução

No capítulo anterior aprendemos que o HTML cria a estrutura de uma página.

Porém, uma página apenas com HTML seria simples:

```text id="8l8h2a"
Título

Texto

Imagem

Botão
```

Ela funciona, mas não possui uma aparência profissional.

É aí que entra:

# CSS

---

# O que é CSS?

CSS significa:

# Cascading Style Sheets

Tradução:

**Folhas de Estilo em Cascata**

Sua função é controlar a aparência dos elementos HTML.

Com CSS podemos definir:

* cores;
* tamanhos;
* fontes;
* posições;
* animações;
* layouts;
* responsividade.

---

# HTML x CSS

Podemos comparar com uma pessoa:

```text id="y7t5c4"
HTML

↓

Corpo da pessoa


CSS

↓

Roupa, estilo e aparência
```

---

# História do CSS

O CSS surgiu em 1996 para separar:

* conteúdo;
* aparência.

Antes dele, os desenvolvedores colocavam estilos diretamente no HTML.

Isso causava:

* códigos gigantes;
* dificuldade de manutenção;
* pouca organização.

---

# Como adicionar CSS ao HTML

Existem três formas.

---

# 1. CSS Inline

Dentro da própria tag.

Exemplo:

```html id="wq2h3f"
<h1 style="color:red">

Título

</h1>
```

Problema:

Difícil de manter.

---

# 2. CSS Interno

Dentro do HTML:

```html id="z6o4c8"
<style>

h1{

color:red;

}

</style>
```

---

# 3. CSS Externo (Profissional)

Arquivo separado:

```text id="v9e4tm"
style.css
```

HTML:

```html id="8qk3pq"
<link 
rel="stylesheet"
href="style.css">
```

Essa é a forma recomendada.

---

# Estrutura de um código CSS

Exemplo:

```css id="j9r4f2"
seletor{

propriedade: valor;

}
```

Exemplo:

```css id="x7r2kz"
h1{

color:blue;

font-size:40px;

}
```

---

# Seletores CSS

Os seletores indicam quais elementos serão estilizados.

---

# Seletor por Tag

Aplica em todas as tags.

HTML:

```html id="9nv3bb"
<p>
Texto
</p>
```

CSS:

```css id="1s9k1t"
p{

color:black;

}
```

---

# Seletor por Classe

Usa:

```text id="g6mq5f"
.
```

HTML:

```html id="2q43kq"
<p class="texto">

Olá

</p>
```

CSS:

```css id="b7p8cg"
.texto{

color:red;

}
```

---

# Seletor por ID

Usa:

```text id="s5l8kj"
#
```

HTML:

```html id="p9w4js"
<div id="menu">

</div>
```

CSS:

```css id="l1z8mr"
#menu{

background:black;

}
```

---

# Classe x ID

Classe:

Pode ser usada várias vezes.

Exemplo:

```text id="0ryv1v"
.botao
```

ID:

Único.

Exemplo:

```text id="k0u4fy"
#header
```

---

# Cores no CSS

Existem várias formas.

---

# Nome

```css id="8r0lfi"
color:red;
```

---

# Hexadecimal

```css id="u5m3n7"
color:#ff0000;
```

---

# RGB

```css id="0ax9ts"
color:rgb(255,0,0);
```

---

# RGBA

Possui transparência:

```css id="o1n7cb"
color:rgba(255,0,0,0.5);
```

---

# Background

Define fundo.

```css id="4p9h3s"
body{

background-color:black;

}
```

---

# Imagens de Fundo

```css id="5z7f7d"
body{

background-image:url("imagem.jpg");

}
```

---

# Gradientes

Criam transições de cores.

```css id="k4m1wo"
background:

linear-gradient(
blue,
purple
);
```

---

# Tipografia

A escolha da fonte influencia muito o design.

---

# Família da fonte

```css id="v2h7dm"
font-family:Arial;
```

---

# Tamanho

```css id="g9f0kp"
font-size:20px;
```

---

# Peso

```css id="8bx8ap"
font-weight:bold;
```

---

# Alinhamento

```css id="cq5mml"
text-align:center;
```

---

# Espaçamento entre letras

```css id="h7b0rj"
letter-spacing:2px;
```

---

# Box Model

Um dos conceitos mais importantes do CSS.

Todo elemento é uma caixa.

Estrutura:

```text id="j8a6cc"
+----------------+

|    Margin      |

| +------------+ |

| | Border     | |

| | +--------+ | |

| | |Padding | | |

| | |Conteúdo| | |

| | +--------+ | |

| +------------+ |

+----------------+
```

---

# Content

Conteúdo.

Exemplo:

Texto ou imagem.

---

# Padding

Espaço interno.

```css id="d6r5a3"
padding:20px;
```

---

# Border

Borda.

```css id="x6u2q8"
border:1px solid black;
```

---

# Margin

Espaço externo.

```css id="7m0o8r"
margin:20px;
```

---

# Width e Height

Largura:

```css id="6k9p6v"
width:300px;
```

Altura:

```css id="l3n5op"
height:200px;
```

---

# Display

Controla como elementos aparecem.

---

# Block

Ocupa toda linha.

Exemplo:

```css id="b8v2fu"
display:block;
```

---

# Inline

Fica na mesma linha.

```css id="j8p4qy"
display:inline;
```

---

# Inline-block

Mistura os dois.

```css id="8o2l2m"
display:inline-block;
```

---

# Position

Controla posicionamento.

---

# Static

Padrão.

---

# Relative

Move em relação ao próprio lugar.

```css id="9o1x9v"
position:relative;
```

---

# Absolute

Posição baseada em outro elemento.

```css id="m6q4yw"
position:absolute;
```

---

# Fixed

Fica fixo na tela.

Exemplo:

Botão de WhatsApp.

```css id="0y4qgx"
position:fixed;
```

---

# Sticky

Fica preso durante rolagem.

```css id="q2h6mz"
position:sticky;
```

---

# Flexbox

Flexbox é uma das ferramentas mais importantes do CSS moderno.

Ele organiza elementos.

Ativar:

```css id="2m5r3v"
.container{

display:flex;

}
```

---

# Direção

Linha:

```css id="j8x3ds"
flex-direction:row;
```

Coluna:

```css id="w8u5qa"
flex-direction:column;
```

---

# Justify-content

Controla eixo principal.

Centro:

```css id="o8n6hv"
justify-content:center;
```

Espaçamento:

```css id="s3y7eu"
justify-content:space-between;
```

---

# Align-items

Controla eixo secundário.

```css id="6v4l6f"
align-items:center;
```

---

# Gap

Espaço entre elementos.

```css id="q7r8nk"
gap:20px;
```

---

# CSS Grid

Grid cria layouts em linhas e colunas.

Exemplo:

```css id="x0d5eq"
.container{

display:grid;

grid-template-columns:

repeat(3,1fr);

}
```

---

Usado em:

* dashboards;
* galerias;
* páginas complexas.

---

# Unidades CSS

## Pixel

```css id="p4f8uy"
20px
```

---

## Porcentagem

```css id="9k5w3t"
50%
```

---

## Rem

Baseado no tamanho da fonte.

```css id="h2z7b8"
2rem
```

---

## Em

Relativo ao elemento pai.

---

## Viewport

Largura:

```css id="u8c9xa"
vw
```

Altura:

```css id="0t5l5p"
vh
```

---

# Variáveis CSS

Permitem reutilizar valores.

Exemplo:

```css id="y7h3u4"
:root{

--cor-principal:blue;

}
```

Usando:

```css id="a9g4k2"
h1{

color:var(--cor-principal);

}
```

---

# Pseudo Classes

Mudam elementos em estados específicos.

Exemplo:

Quando passa o mouse:

```css id="d3v5op"
button:hover{

background:red;

}
```

---

# Outras:

```text id="6v8x5g"
:hover

:focus

:first-child

:nth-child()
```

---

# Pseudo Elementos

Criam partes extras.

Antes:

```css id="8f0r4v"
::before
```

Depois:

```css id="y4z6r1"
::after
```

---

# Sombras

## Texto:

```css id="2x8z5m"
text-shadow:
```

---

## Caixa:

```css id="7x4r5c"
box-shadow:
```

Exemplo:

```css id="n4u9w1"
box-shadow:

0 5px 20px gray;
```

---

# Bordas arredondadas

```css id="5m8s0d"
border-radius:20px;
```

Muito usado em:

* cards;
* botões;
* interfaces modernas.

---

# Transições

Criam mudanças suaves.

Exemplo:

```css id="g8w2tj"
button{

transition:0.3s;

}
```

---

# Animações CSS

Criadas com:

```css id="a5m7kw"
@keyframes
```

Exemplo:

```css id="s8v2po"
@keyframes aparecer{

from{

opacity:0;

}

to{

opacity:1;

}

}
```

---

# Transform

Modifica elementos.

Exemplos:

Mover:

```css id="k9u3ra"
transform:translateX(50px);
```

Girar:

```css id="z4p6hm"
transform:rotate(45deg);
```

Aumentar:

```css id="o7w2kg"
transform:scale(1.2);
```

---

# Design Moderno com CSS

Técnicas utilizadas atualmente:

---

# Glassmorphism

Efeito vidro.

Usa:

* transparência;
* blur;
* sombras.

---

# Neomorphism

Design suave com sombras internas.

---

# Dark Mode

Interfaces escuras.

---

# CSS Responsivo

Um site precisa funcionar em:

* celular;
* tablet;
* computador.

Usamos:

```css id="g4h8q1"
@media
```

Exemplo:

```css id="a2x7k9"
@media(max-width:600px){

.container{

flex-direction:column;

}

}
```

---

# Organização Profissional CSS

Estrutura:

```text id="6d9j8q"
css/

├── reset.css

├── variables.css

├── components.css

└── style.css
```

---

# Metodologias CSS

## BEM

Organização de nomes.

Exemplo:

```text id="m5z8k4"
botao

botao__texto

botao--grande
```

---

# Boas práticas CSS

✔ Use classes claras.

✔ Evite repetir código.

✔ Organize arquivos.

✔ Use variáveis.

✔ Pense em responsividade.

✔ Crie componentes reutilizáveis.

✔ Mantenha consistência visual.

---

# Projeto Prático

## Criar uma Landing Page Profissional

Deve conter:

### Header

* Logo
* Menu

### Hero Section

* Título principal
* Descrição
* Botão

### Cards

* Serviços
* Projetos

### Footer

* Contatos
* Redes sociais

Tecnologias:

✅ HTML5
✅ CSS3

Aplicar:

* Flexbox
* Grid
* Responsividade
* Animações
* Design moderno

---

# Exercícios

1. O que significa CSS?
2. Qual a diferença entre HTML e CSS?
3. Explique o Box Model.
4. Para que serve Flexbox?
5. Para que serve CSS Grid?
6. O que são pseudo classes?
7. O que são variáveis CSS?
8. Explique responsividade.
9. O que é uma media query?
10. Por que organização CSS é importante?

---

# Resumo do Capítulo

Neste capítulo você aprendeu:

✅ O que é CSS3.
✅ Como aplicar estilos.
✅ Seletores.
✅ Cores e fontes.
✅ Box Model.
✅ Display e Position.
✅ Flexbox.
✅ CSS Grid.
✅ Variáveis CSS.
✅ Pseudo classes e elementos.
✅ Animações e transições.
✅ Layouts modernos.
✅ Responsividade básica.
✅ Organização profissional de estilos.

---

# Próximo Capítulo

## Capítulo 24 — Responsividade e UI/UX

No próximo capítulo você aprenderá a criar interfaces realmente profissionais, estudando:

* Mobile First;
* Design responsivo;
* Experiência do usuário (UX);
* Interface do usuário (UI);
* Figma;
* Design Systems;
* Psicologia das cores;
* Tipografia;
* Hierarquia visual;
* Princípios usados por grandes empresas de tecnologia.
