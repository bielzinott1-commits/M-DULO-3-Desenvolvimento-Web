# CURSO COMPLETO DE ENGENHARIA DE SOFTWARE

# Do Zero ao Desenvolvedor Full Stack

# VOLUME 3 — DESENVOLVIMENTO WEB

# CAPÍTULO 24

# Responsividade e UI/UX — Criando Interfaces Profissionais para Todos os Dispositivos

> **Objetivo do capítulo:** Ao final deste capítulo, você entenderá como criar interfaces modernas, adaptáveis e agradáveis para usuários. Aprenderá conceitos de UI (User Interface), UX (User Experience), Mobile First, Design Responsivo, acessibilidade, prototipação, Figma, Design Systems e princípios utilizados por empresas profissionais.

---

# Introdução

Nos capítulos anteriores aprendemos:

* HTML → estrutura da página;
* CSS → aparência e estilo.

Agora precisamos responder uma pergunta:

> Como criar uma interface que funcione bem em qualquer dispositivo e seja agradável para o usuário?

A resposta envolve dois conceitos fundamentais:

# UI e UX

---

# O que é UI?

UI significa:

# User Interface

(Interface do Usuário)

É tudo aquilo que o usuário vê e utiliza.

Exemplos:

* botões;
* cores;
* menus;
* fontes;
* ícones;
* imagens;
* animações.

A UI é responsável pela aparência.

---

# O que é UX?

UX significa:

# User Experience

(Experiência do Usuário)

É como o usuário se sente ao utilizar um produto.

Envolve:

* facilidade de uso;
* velocidade;
* organização;
* clareza;
* satisfação.

---

# Diferença entre UI e UX

Imagine um aplicativo de banco.

## UI:

* botão bonito;
* cores profissionais;
* ícones modernos.

## UX:

* encontrar o botão de pagar facilmente;
* realizar uma transferência sem dificuldade;
* entender cada etapa.

Uma interface pode ser bonita e ter uma experiência ruim.

---

# O Design Perfeito

Um bom produto precisa unir:

```text
UI

+

UX

=

Experiência profissional
```

---

# O que é Design Responsivo?

Design responsivo significa criar páginas que se adaptam automaticamente aos diferentes tamanhos de tela.

Um site precisa funcionar em:

* smartphones;
* tablets;
* notebooks;
* monitores grandes;
* televisões.

---

# Exemplo de problema

Site sem responsividade:

```text
Computador:

[ MENU  CONTEÚDO  IMAGEM ]


Celular:

[MENU]

[CONTEÚDO CORTADO]

[IMAGEM FORA DA TELA]
```

---

Site responsivo:

```text
Computador:

[ MENU ][ CONTEÚDO ][ IMAGEM ]


Celular:

[ MENU ]

[ CONTEÚDO ]

[ IMAGEM ]
```

---

# Por que Responsividade é importante?

Atualmente grande parte dos acessos vem de celulares.

Um site não adaptado causa:

* usuários saindo;
* baixa confiança;
* menor posicionamento no Google;
* dificuldade de navegação.

---

# Mobile First

Mobile First significa:

# Criar primeiro para dispositivos móveis.

Depois expandir para telas maiores.

Fluxo:

```text
Celular

↓

Tablet

↓

Desktop
```

---

# Por que Mobile First?

Porque celulares possuem:

* menos espaço;
* menor processamento;
* internet variável.

Isso força o desenvolvedor a criar experiências mais eficientes.

---

# Exemplo Mobile First

CSS:

```css
.container{

display:flex;

flex-direction:column;

}
```

Depois:

```css
@media(min-width:768px){

.container{

flex-direction:row;

}

}
```

---

# Breakpoints

São pontos onde o layout muda.

Exemplo:

## Celular

```text
0px - 600px
```

---

## Tablet

```text
601px - 1024px
```

---

## Desktop

```text
1025px+
```

---

# Media Queries

Permitem criar estilos diferentes.

Exemplo:

```css
@media(max-width:600px){

.menu{

display:none;

}

}
```

---

# Unidades Responsivas

## %

Relativo ao tamanho do elemento pai.

---

## vw

Viewport Width.

Exemplo:

```css
width:50vw;
```

---

## vh

Viewport Height.

Exemplo:

```css
height:100vh;
```

---

## rem

Baseado no tamanho da fonte.

Exemplo:

```css
font-size:2rem;
```

---

# Layouts Responsivos

As principais ferramentas:

## Flexbox

Ideal para:

* menus;
* cards;
* alinhamentos.

---

## CSS Grid

Ideal para:

* layouts completos;
* dashboards;
* galerias.

---

# Exemplo de Grid Responsivo

```css
.cards{

display:grid;

grid-template-columns:

repeat(auto-fit,minmax(250px,1fr));

}
```

Esse código adapta automaticamente os cards.

---

# Imagens Responsivas

Problema:

Imagem grande pode quebrar a página.

Solução:

```css
img{

max-width:100%;

height:auto;

}
```

---

# UX Design

Agora vamos aprofundar a experiência.

---

# Princípio 1 — Simplicidade

O usuário não deve precisar pensar demais.

Exemplo ruim:

```text
10 botões diferentes na tela inicial
```

Melhor:

```text
3 ações principais
```

---

# Princípio 2 — Consistência

Elementos iguais devem funcionar iguais.

Exemplo:

Todos os botões:

* mesma cor;
* mesmo formato;
* mesmo comportamento.

---

# Princípio 3 — Feedback

O sistema deve responder ao usuário.

Exemplos:

Ao clicar:

```text
Salvando...
```

Depois:

```text
Salvo com sucesso!
```

---

# Princípio 4 — Hierarquia Visual

Nem tudo possui a mesma importância.

Exemplo:

Título:

```text
Grande
```

Descrição:

```text
Menor
```

Botão:

```text
Destaque
```

---

# Princípio 5 — Menos esforço

O usuário deve conseguir completar tarefas rapidamente.

Exemplo:

Comprar online:

Ruim:

```text
8 telas até finalizar
```

Melhor:

```text
3 etapas simples
```

---

# Psicologia das Cores

As cores influenciam emoções.

---

# Azul

Transmite:

* confiança;
* segurança;
* tecnologia.

Muito usado por:

* bancos;
* empresas de tecnologia.

---

# Vermelho

Transmite:

* energia;
* urgência;
* atenção.

---

# Verde

Relacionado a:

* natureza;
* sucesso;
* aprovação.

---

# Preto

Transmite:

* luxo;
* elegância;
* profissionalismo.

---

# Branco

Transmite:

* limpeza;
* simplicidade;
* organização.

---

# Tipografia

A fonte influencia a percepção.

---

# Fontes Sans Serif

Exemplo:

Arial

Características:

* modernas;
* simples;
* digitais.

---

# Fontes Serif

Características:

* tradicionais;
* elegantes.

---

# Regras de Tipografia

Evite:

❌ Muitas fontes diferentes.

❌ Textos pequenos demais.

❌ Baixo contraste.

Prefira:

✔ Uma fonte para títulos.

✔ Uma fonte para textos.

✔ Boa leitura.

---

# Espaçamento

Um erro comum:

Colocar tudo muito junto.

Uma boa interface utiliza:

* margens;
* espaços;
* áreas vazias.

O espaço vazio também é design.

---

# Figma

O Figma é uma ferramenta profissional para criar interfaces.

Usado para:

* protótipos;
* wireframes;
* design de aplicativos;
* sistemas completos.

---

# Processo Profissional de Design

## 1. Pesquisa

Entender:

* público;
* objetivo;
* problema.

---

## 2. Wireframe

Modelo simples:

```text
[Logo]

[Título]

[Imagem]

[Botão]
```

---

## 3. Protótipo

Modelo funcionando.

---

## 4. Desenvolvimento

Transformar design em código.

---

# Design System

Um Design System é um conjunto de padrões.

Ele define:

* cores;
* componentes;
* botões;
* espaçamentos;
* fontes.

---

# Exemplo:

Botão padrão:

```text
Cor: Azul

Raio: 10px

Altura: 40px

Fonte: 16px
```

Todos usam o mesmo padrão.

---

# Componentes Reutilizáveis

Em projetos profissionais criamos componentes.

Exemplo:

Botão:

```html
<button class="primary">
Enviar
</button>
```

Esse botão pode aparecer em várias páginas.

---

# Acessibilidade

Uma interface profissional deve funcionar para todos.

Inclui:

* pessoas com deficiência visual;
* usuários utilizando teclado;
* leitores de tela.

---

# Boas práticas:

✔ Contraste adequado.

✔ Textos alternativos em imagens.

✔ Botões identificáveis.

✔ Navegação pelo teclado.

✔ Campos de formulário claros.

---

# Ferramentas importantes para UI/UX

## Design

* Figma
* Adobe XD
* Sketch

## Desenvolvimento

* Chrome DevTools
* Lighthouse
* WebPageTest

## Inspiração

* Dribbble
* Behance
* Awwwards

---

# Projeto Prático

## Criar o Design de um Aplicativo

Tema:

**Sistema de Ordem de Serviço para Assistência Técnica**

Criar:

### Tela Login

* Logo
* Email
* Senha
* Botão entrar

### Dashboard

* Serviços pendentes
* Clientes
* Equipamentos

### Cadastro

* Cliente
* Produto
* Defeito

---

Etapas:

1. Criar wireframe.
2. Criar protótipo no Figma.
3. Definir cores.
4. Criar componentes.
5. Desenvolver com HTML e CSS.
6. Tornar responsivo.

---

# Exercícios

1. Explique a diferença entre UI e UX.
2. O que significa Design Responsivo?
3. Explique Mobile First.
4. Para que servem Media Queries?
5. Por que espaçamento é importante?
6. O que é Design System?
7. Qual a função do Figma?
8. Por que acessibilidade é importante?
9. Explique hierarquia visual.
10. O que torna uma interface profissional?

---

# Resumo do Capítulo

Neste capítulo você aprendeu:

✅ Conceitos de UI e UX.
✅ Design Responsivo.
✅ Mobile First.
✅ Breakpoints.
✅ Media Queries.
✅ Layouts adaptáveis.
✅ Psicologia das cores.
✅ Tipografia.
✅ Espaçamento e hierarquia visual.
✅ Figma e prototipação.
✅ Design Systems.
✅ Acessibilidade.
✅ Processo profissional de criação de interfaces.

---

# Próximo Capítulo

# Capítulo 25 — JavaScript do Básico ao Avançado

No próximo capítulo começaremos a programação de verdade no navegador, aprendendo:

* variáveis;
* tipos de dados;
* operadores;
* funções;
* objetos;
* arrays;
* classes;
* ES6+;
* programação assíncrona;
* promises;
* async/await;
* criação de aplicações interativas.
