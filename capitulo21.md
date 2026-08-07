# CURSO COMPLETO DE ENGENHARIA DE SOFTWARE

## Volume 3 — Desenvolvimento Web

# CAPÍTULO 21

# Como Funciona a Internet: Da Digitação de um Endereço até o Carregamento de um Site

> **Objetivo do capítulo:** Ao final deste capítulo, você entenderá profundamente como a Internet funciona, desde o momento em que um usuário digita um endereço no navegador até a exibição completa da página. Você conhecerá protocolos, servidores, DNS, IP, HTTP, HTTPS, SSL/TLS, cookies, cache, CDNs e diversos conceitos fundamentais para qualquer desenvolvedor.

---

# Introdução

Hoje usamos a Internet diariamente para:

* assistir vídeos;
* acessar redes sociais;
* jogar online;
* estudar;
* trabalhar;
* fazer compras;
* conversar com pessoas do outro lado do mundo.

Mas você já parou para pensar no que realmente acontece quando digita:

```text
https://www.google.com
```

Em menos de um segundo, milhares de processos acontecem.

Como programador, entender esse funcionamento é essencial para criar aplicações rápidas, seguras e escaláveis.

---

# O que é a Internet?

A Internet é uma gigantesca rede mundial de computadores conectados entre si.

Ela permite que dispositivos troquem informações utilizando protocolos padronizados.

Imagine uma enorme cidade.

Cada casa representa um computador.

As ruas representam os cabos e conexões.

Os carros representam os dados.

Todos conseguem se comunicar porque seguem regras de trânsito.

Na Internet acontece exatamente a mesma coisa.

---

# Breve História da Internet

### Década de 1960

O governo dos Estados Unidos criou um projeto chamado:

```text
ARPANET
```

Objetivo:

Criar uma rede resistente que continuasse funcionando mesmo se parte dela fosse destruída.

---

### Década de 1980

Foi criado o protocolo:

```text
TCP/IP
```

Até hoje ele é a base da Internet.

---

### 1989

O cientista britânico:

**Tim Berners-Lee**

criou a:

```text
World Wide Web (WWW)
```

Ele também criou:

* HTML
* HTTP
* URLs

Esses três elementos revolucionaram a Internet.

---

# Internet x Web

Muitas pessoas pensam que são a mesma coisa.

Não são.

## Internet

É toda a infraestrutura:

* cabos;
* satélites;
* roteadores;
* servidores;
* computadores.

---

## Web (WWW)

É apenas um dos serviços que utilizam a Internet.

Outros exemplos:

* E-mail
* FTP
* Jogos online
* Chamadas de vídeo
* Streaming

---

# Como um Site é Carregado?

Imagine que você digite:

```text
https://meusite.com
```

O processo acontece aproximadamente nesta ordem:

```text
Você

↓

Navegador

↓

DNS

↓

Endereço IP

↓

Servidor

↓

Banco de Dados

↓

Servidor gera resposta

↓

HTML

↓

CSS

↓

JavaScript

↓

Página exibida
```

Cada etapa possui uma função específica.

---

# O Navegador

O navegador é o programa responsável por interpretar páginas web.

Exemplos:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari
* Opera

Ele entende:

* HTML
* CSS
* JavaScript

Depois transforma tudo em uma interface gráfica.

---

# URL (Uniform Resource Locator)

É o endereço de um recurso na Internet.

Exemplo:

```text
https://www.exemplo.com/produtos/notebook
```

Vamos dividir:

```text
https://
```

Protocolo.

---

```text
www.exemplo.com
```

Domínio.

---

```text
/produtos/notebook
```

Caminho do recurso.

---

# Domínio

É o nome que identifica um site.

Exemplos:

```text
google.com

youtube.com

github.com
```

Muito mais fácil lembrar isso do que um endereço IP.

---

# O que é um IP?

Cada computador conectado à Internet possui um endereço.

Chamado:

```text
IP
```

Exemplo IPv4:

```text
192.168.1.20
```

Na Internet:

```text
142.250.219.46
```

Esse número identifica exatamente qual computador responderá.

---

# IPv4

Formato:

```text
192.168.0.1
```

Possui aproximadamente:

```text
4 bilhões
```

de combinações.

Hoje já é insuficiente.

---

# IPv6

Foi criado para resolver esse problema.

Exemplo:

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

Possui uma quantidade gigantesca de endereços disponíveis.

---

# DNS (Domain Name System)

DNS é conhecido como:

# A agenda telefônica da Internet

Você digita:

```text
google.com
```

O DNS responde:

```text
142.250.219.46
```

Agora o navegador sabe para onde enviar a solicitação.

---

# O que é um Servidor?

Servidor é um computador preparado para atender requisições de outros computadores.

Ele permanece ligado continuamente.

Pode armazenar:

* sites;
* APIs;
* bancos de dados;
* arquivos;
* imagens;
* vídeos.

---

# Cliente e Servidor

Na web existe um modelo chamado:

```text
Cliente → Servidor
```

Cliente:

Você utilizando o navegador.

Servidor:

Computador que responde às solicitações.

---

# Requisição (Request)

Quando você abre um site, seu navegador envia um pedido.

Exemplo:

```text
Quero abrir a página inicial.
```

---

# Resposta (Response)

O servidor responde:

```text
Aqui está o HTML.

Aqui está o CSS.

Aqui está o JavaScript.
```

---

# HTTP

HTTP significa:

```text
HyperText Transfer Protocol
```

É o protocolo utilizado para comunicação entre navegador e servidor.

Ele define como as mensagens são enviadas.

---

# HTTPS

HTTPS é:

```text
HTTP + Criptografia
```

Hoje praticamente todos os sites utilizam HTTPS.

Exemplo:

```text
https://
```

---

# Por que HTTPS é importante?

Imagine enviar uma senha.

Sem HTTPS:

```text
Senha

↓

Internet

↓

Pode ser interceptada
```

Com HTTPS:

```text
Senha

↓

Criptografada

↓

Somente o servidor consegue ler
```

---

# SSL/TLS

São protocolos responsáveis pela criptografia das comunicações.

Eles utilizam certificados digitais.

Quando vemos:

```text
🔒
```

Ao lado do endereço do site,

significa que a conexão está protegida.

---

# Certificados Digitais

Um certificado comprova que o servidor é realmente quem diz ser.

Ele evita ataques como falsificação de sites.

---

# Métodos HTTP

Os principais são:

## GET

Buscar informações.

Exemplo:

```text
Abrir página inicial.
```

---

## POST

Enviar informações.

Exemplo:

```text
Cadastro.
```

---

## PUT

Atualizar dados.

---

## PATCH

Atualizar parcialmente.

---

## DELETE

Excluir informações.

---

# Código de Status HTTP

Sempre que um servidor responde, ele envia um código.

## 200

Tudo certo.

---

## 201

Recurso criado.

---

## 301

Redirecionamento permanente.

---

## 400

Erro na requisição.

---

## 401

Não autorizado.

---

## 403

Acesso proibido.

---

## 404

Página não encontrada.

---

## 500

Erro interno do servidor.

---

# Cookies

Cookies são pequenos arquivos armazenados no navegador.

Eles guardam informações como:

* login;
* idioma;
* preferências;
* carrinho de compras.

---

# Sessões (Sessions)

Enquanto os cookies ficam no navegador, as sessões normalmente ficam armazenadas no servidor.

Elas identificam o usuário durante sua navegação.

---

# Cache

Cache é uma memória temporária.

Ele armazena arquivos para acelerar o carregamento.

Exemplo:

Você acessa um site pela primeira vez.

O navegador salva:

* imagens;
* CSS;
* JavaScript.

Na próxima visita tudo abre muito mais rápido.

---

# CDN (Content Delivery Network)

Imagine um servidor localizado apenas no Japão.

Um usuário brasileiro demoraria para receber os dados.

Uma CDN resolve isso.

Ela distribui cópias do site em servidores espalhados pelo mundo.

Assim o conteúdo é entregue pelo servidor mais próximo do usuário.

Exemplos de conteúdo distribuído:

* imagens;
* vídeos;
* arquivos JavaScript;
* folhas de estilo.

---

# Firewall

Firewall funciona como um porteiro.

Ele controla quem pode acessar um servidor.

Bloqueia conexões suspeitas.

---

# Balanceador de Carga (Load Balancer)

Grandes sites recebem milhões de acessos.

Um único servidor não suporta tudo.

O balanceador distribui as requisições.

Exemplo:

```text
Usuários

↓

Load Balancer

↓

Servidor A

Servidor B

Servidor C
```

---

# Banco de Dados

Quando você faz login:

O servidor consulta o banco.

Exemplo:

```text
Email

Senha

↓

Banco de Dados

↓

Usuário encontrado
```

---

# Como o HTML chega ao navegador?

O servidor envia:

```text
HTML
```

Depois:

```text
CSS
```

Depois:

```text
JavaScript
```

O navegador monta a página.

---

# Renderização

Renderizar significa transformar código em interface visual.

O navegador:

1. Lê HTML.
2. Constrói o DOM.
3. Lê CSS.
4. Calcula estilos.
5. Executa JavaScript.
6. Desenha tudo na tela.

---

# O que acontece quando clicamos em um botão?

Exemplo:

```text
Clique

↓

JavaScript

↓

Requisição

↓

Servidor

↓

Banco

↓

Resposta

↓

Atualização da tela
```

---

# Como Funciona uma API?

Uma API é uma ponte entre sistemas.

Exemplo:

Seu aplicativo pede:

```text
Temperatura de Joinville
```

A API responde:

```json
{
  "temperatura": 19,
  "condicao": "Nublado"
}
```

Seu aplicativo apenas exibe a informação.

---

# Segurança na Internet

Boas práticas:

* Sempre utilizar HTTPS.
* Nunca armazenar senhas em texto puro.
* Validar dados enviados pelos usuários.
* Utilizar autenticação.
* Atualizar sistemas regularmente.
* Fazer backups frequentes.

---

# Ferramentas que Todo Desenvolvedor Deve Conhecer

* Navegadores modernos (Chrome, Edge, Firefox).
* DevTools (Ferramentas do Desenvolvedor).
* Terminal.
* Git.
* GitHub.
* Editores de código (como Visual Studio Code).
* Serviços de teste de APIs (como Postman ou Insomnia).

---

# Boas Práticas para Desenvolvedores Web

✔ Minimize o tamanho de imagens.

✔ Utilize cache quando possível.

✔ Prefira HTTPS.

✔ Organize seus arquivos.

✔ Proteja dados sensíveis.

✔ Compreenda como o navegador renderiza páginas.

✔ Aprenda os protocolos da Internet antes de desenvolver aplicações complexas.

---

# Exercícios

1. Explique a diferença entre Internet e Web.
2. O que é uma URL?
3. Qual a função do DNS?
4. O que é um endereço IP?
5. Explique a diferença entre HTTP e HTTPS.
6. O que é SSL/TLS?
7. O que faz um servidor?
8. O que é cache?
9. Para que serve uma CDN?
10. Explique o fluxo completo desde a digitação de uma URL até a exibição da página no navegador.

---

# Projeto Prático

## Objetivo

Criar um diagrama explicando o funcionamento da Internet.

Seu diagrama deve conter:

```text
Usuário
      │
      ▼
 Navegador
      │
      ▼
 DNS
      │
      ▼
 Endereço IP
      │
      ▼
 Servidor Web
      │
      ▼
 Aplicação
      │
      ▼
 Banco de Dados
      │
      ▼
 Resposta (HTML, CSS e JavaScript)
      │
      ▼
 Navegador Renderiza a Página
```

Depois, escreva um relatório explicando o papel de cada componente e publique o projeto em um repositório do GitHub com um `README.md` bem documentado.

---

# Resumo do capítulo

Neste capítulo você aprendeu:

✅ O que é a Internet e como ela surgiu.
✅ A diferença entre Internet e World Wide Web.
✅ Como funcionam URLs, domínios e endereços IP.
✅ O papel do DNS.
✅ A arquitetura Cliente-Servidor.
✅ Como funcionam HTTP e HTTPS.
✅ O que são SSL/TLS e certificados digitais.
✅ Métodos HTTP e códigos de status.
✅ Cookies, sessões e cache.
✅ O papel das CDNs e balanceadores de carga.
✅ Como o navegador renderiza páginas.
✅ Como APIs participam da comunicação entre aplicações.

---

## Próximo capítulo

No **Capítulo 22**, você aprenderá **HTML5 Completo**, desde a estrutura básica até recursos avançados como elementos semânticos, formulários complexos, acessibilidade (ARIA), SEO, multimídia e organização de páginas profissionais, construindo uma base sólida para o desenvolvimento Front-End.
