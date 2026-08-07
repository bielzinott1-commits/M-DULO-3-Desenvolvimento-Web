# CURSO COMPLETO DE ENGENHARIA DE SOFTWARE

# Do Zero ao Desenvolvedor Full Stack

# VOLUME 3 — DESENVOLVIMENTO WEB

# CAPÍTULO 28

# Projetos Web Completos — Transformando Conhecimento em Aplicações Reais

> **Objetivo do capítulo:** Ao final deste capítulo, você será capaz de planejar, criar e publicar projetos web completos utilizando HTML5, CSS3, JavaScript, DOM, APIs, Git e GitHub. Este capítulo representa a transição entre aprender conceitos e construir aplicações utilizadas no mercado.

---

# Introdução

Durante os capítulos anteriores aprendemos:

## HTML5

Responsável pela:

* estrutura;
* organização;
* semântica.

---

## CSS3

Responsável por:

* design;
* layouts;
* responsividade;
* animações.

---

## JavaScript

Responsável por:

* lógica;
* interatividade;
* manipulação de dados.

---

## DOM

Responsável por:

* controlar elementos da página;
* criar experiências dinâmicas.

---

## APIs

Responsável por:

* conectar sistemas;
* buscar informações externas.

---

Agora chegou o momento mais importante:

# Criar projetos reais.

Um desenvolvedor não é avaliado apenas pelo que sabe, mas pelo que consegue construir.

---

# O Processo Profissional de Criação de Projetos

Antes de escrever código, desenvolvedores seguem etapas.

---

# 1 — Definição do Projeto

Primeiro devemos responder:

## Qual problema será resolvido?

Exemplo:

Problema:

> Técnicos precisam organizar ordens de serviço.

Solução:

> Criar um sistema de gerenciamento de manutenção.

---

# 2 — Planejamento

Criamos:

* objetivos;
* funcionalidades;
* tecnologias;
* organização.

Exemplo:

Projeto:

Sistema de Assistência Técnica.

Funcionalidades:

✔ Cadastro de clientes
✔ Cadastro de equipamentos
✔ Ordem de serviço
✔ Status do serviço
✔ Pesquisa

---

# 3 — Wireframe

Antes do código criamos o desenho da aplicação.

Exemplo:

```text
+----------------------+

| LOGO        MENU     |

+----------------------+

|                      |

|    CONTEÚDO          |

|                      |

|     BOTÃO            |

+----------------------+

```

Ferramentas:

* Figma;
* papel;
* ferramentas de prototipação.

---

# 4 — Design da Interface

Definir:

* cores;
* fontes;
* componentes;
* espaçamento.

Exemplo:

## Cores

Principal:

```text
Azul
```

Secundária:

```text
Cinza
```

Destaque:

```text
Verde
```

---

# 5 — Desenvolvimento

Agora começamos o código.

Estrutura profissional:

```text
projeto/

├── index.html

├── css/

│   └── style.css

├── js/

│   └── script.js

├── images/

└── README.md
```

---

# Projeto 1

# Landing Page Profissional

Uma Landing Page é uma página criada para apresentar um produto ou serviço.

---

## Estrutura

```text
Landing Page

↓

Header

↓

Hero

↓

Serviços

↓

Depoimentos

↓

Contato

↓

Footer
```

---

# Header

Possui:

* logo;
* menu;
* botão.

Exemplo:

```html
<header>

<img src="logo.png">

<nav>

<a>Início</a>

<a>Serviços</a>

<a>Contato</a>

</nav>

</header>
```

---

# Hero Section

A primeira impressão.

Possui:

* título;
* descrição;
* chamada para ação.

Exemplo:

```text
Crie soluções digitais

Transformamos ideias em tecnologia

[Começar agora]
```

---

# Cards de Serviços

Exemplo:

```text
+-------------+

| Desenvolvimento |

+-------------+

| Design UI/UX |

+-------------+

| Suporte |

+-------------+
```

Criados com:

* HTML;
* CSS Grid;
* Flexbox.

---

# Recursos profissionais

Adicionar:

✔ Animações.

✔ Responsividade.

✔ Formulários.

✔ SEO básico.

---

# Projeto 2

# Portfólio de Desenvolvedor

Todo programador precisa de um portfólio.

Ele demonstra:

* habilidades;
* projetos;
* evolução.

---

# Estrutura:

```text
Portfólio

↓

Apresentação

↓

Sobre mim

↓

Tecnologias

↓

Projetos

↓

Contato
```

---

# Seção de Tecnologias

Exemplo:

```text
HTML5

CSS3

JavaScript

Git

GitHub

React

Node.js
```

---

# Seção de Projetos

Cada projeto deve mostrar:

* imagem;
* descrição;
* tecnologias;
* link GitHub;
* demonstração.

---

# Projeto 3

# Sistema de Login

Um dos projetos mais importantes.

---

## Funcionalidades:

✔ Campo usuário.

✔ Campo senha.

✔ Validação.

✔ Mensagens de erro.

✔ Interface responsiva.

---

Estrutura:

```text
login/

├── index.html

├── style.css

└── script.js
```

---

Exemplo de validação:

```javascript
if(email===""){

alert("Digite seu email");

}
```

---

# Projeto 4

# To-Do List Profissional

Aplicação clássica para aprender lógica.

---

Funcionalidades:

✔ Criar tarefas.

✔ Excluir tarefas.

✔ Marcar concluídas.

✔ Salvar dados.

---

Tecnologias:

* DOM;
* Eventos;
* LocalStorage.

---

# Projeto 5

# Aplicativo Consumindo API

Exemplo:

## Aplicativo de Clima

---

Fluxo:

```text
Usuário

↓

Digite cidade

↓

JavaScript

↓

API

↓

JSON

↓

Resultado na tela
```

---

Aprendizados:

* Fetch;
* Async/Await;
* JSON;
* Tratamento de erros.

---

# Projeto 6

# Loja Virtual Front-End

Um projeto mais avançado.

---

Funcionalidades:

## Produtos

* imagem;
* nome;
* preço.

---

## Carrinho

* adicionar produtos;
* remover;
* calcular total.

---

## Pesquisa

* filtrar produtos.

---

Conceitos usados:

* Arrays;
* Objetos;
* DOM;
* LocalStorage.

---

# Projeto 7

# Sistema de Ordem de Serviço

Projeto próximo do mercado.

---

## Módulos:

### Clientes

Cadastro:

* nome;
* telefone;
* email.

---

### Equipamentos

Dados:

* aparelho;
* marca;
* modelo;
* defeito.

---

### Serviços

Status:

* recebido;
* analisando;
* consertando;
* finalizado.

---

# Organização Profissional com Git

Todo projeto deve possuir versionamento.

---

# Inicializar projeto:

```bash
git init
```

---

Adicionar arquivos:

```bash
git add .
```

---

Criar commit:

```bash
git commit -m "Criando estrutura inicial"
```

---

Enviar para GitHub:

```bash
git push
```

---

# README Profissional

Todo projeto deve explicar:

## Nome

## Descrição

## Tecnologias

## Instalação

## Funcionamento

## Imagens

## Autor

---

# Deploy

Publicar o projeto na Internet.

Ferramentas:

* GitHub Pages;
* Vercel;
* Netlify.

---

# Checklist de Projeto Profissional

Antes de publicar:

## Código

✔ Sem erros.

✔ Organizado.

✔ Comentários necessários.

---

## Interface

✔ Responsiva.

✔ Boa experiência.

✔ Acessível.

---

## GitHub

✔ README.

✔ Commits organizados.

✔ Imagens.

✔ Licença.

---

# Como Criar um Portfólio Forte

Um bom portfólio deve ter:

## 3 a 5 projetos excelentes

Melhor:

```text
5 projetos completos
```

Do que:

```text
30 projetos simples
```

---

# Projetos recomendados para iniciantes

Nível 1:

* Calculadora;
* Relógio digital;
* Lista de tarefas.

---

Nível 2:

* Clima usando API;
* Quiz;
* Conversor de moedas.

---

Nível 3:

* Loja virtual;
* Dashboard;
* Sistema administrativo.

---

Nível 4:

* Aplicação Full Stack completa.

---

# Erros comuns de iniciantes

## Copiar projetos sem entender

Problema:

Não desenvolve raciocínio.

---

## Fazer projetos muito pequenos

Problema:

Não demonstra capacidade.

---

## Não publicar

Problema:

Ninguém conhece seu trabalho.

---

## Não documentar

Problema:

Profissionais precisam entender seu código.

---

# Projeto Final do Capítulo

## Criar um Sistema Web Completo

Tema:

# Plataforma de Serviços Técnicos

Nome exemplo:

**SinalOS**

---

## Front-End:

HTML5

CSS3

JavaScript

---

## Funcionalidades:

### Página inicial

* apresentação;
* serviços.

---

### Cadastro

* clientes;
* equipamentos.

---

### Área de serviços

* criar ordem;
* acompanhar status.

---

### Dashboard

* quantidade de serviços;
* gráficos;
* informações.

---

### Integração:

* API;
* armazenamento local.

---

# Exercícios

1. Por que projetos são importantes?
2. Qual diferença entre aprender e construir?
3. O que é uma Landing Page?
4. Por que criar um portfólio?
5. Qual a importância do Git em projetos?
6. O que deve ter em um README?
7. Explique o processo de criação de software.
8. Por que fazer protótipos?
9. O que é Deploy?
10. Quais projetos você criaria para seu portfólio?

---

# Resumo do Capítulo

Neste capítulo você aprendeu:

✅ Como planejar projetos reais.
✅ Processo profissional de desenvolvimento.
✅ Criação de Landing Pages.
✅ Criação de Portfólios.
✅ Sistemas de Login.
✅ Aplicações com APIs.
✅ Lojas virtuais.
✅ Sistemas administrativos.
✅ Organização com Git/GitHub.
✅ README profissional.
✅ Deploy.
✅ Construção de portfólio.

---

# FIM DO MÓDULO 3 — DESENVOLVIMENTO WEB

Você concluiu:

✅ Capítulo 21 — Como funciona a Internet
✅ Capítulo 22 — HTML5 Completo
✅ Capítulo 23 — CSS3 Completo
✅ Capítulo 24 — Responsividade e UI/UX
✅ Capítulo 25 — JavaScript Básico ao Avançado
✅ Capítulo 26 — DOM e Eventos
✅ Capítulo 27 — APIs e Consumo de Dados
✅ Capítulo 28 — Projetos Web Completos

---

# Próximo Módulo

# MÓDULO 4 — DESENVOLVIMENTO PROFISSIONAL

Próximo:

# CAPÍTULO 29 — TypeScript

Você aprenderá:

* por que TypeScript existe;
* diferenças entre JavaScript e TypeScript;
* tipagem estática;
* interfaces;
* classes avançadas;
* desenvolvimento profissional utilizado em empresas.
