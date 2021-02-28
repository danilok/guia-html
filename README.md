# Guia Estelar de HTML da Rocketseat

* Conceitos
  1. [Abertura](#1-abertura)
  2. [Instalando plugin de preview HTML](#2-instalando-plugin-de-preview-html)
  3. [O que é HTML](#3-o-que-é-html)
  4. [Comentários](#4-comentários)
  5. [Anatomia das Tags](#5-anatomia-das-tags)
  6. [Atributos](#6-atributos)
  7. [Atributos Globais](#7-atributos-globais)
  8. [Aninhamento Hierarquia](#8-aninhamento-hierarquia)
  9. [Praticando](#9-praticando)
  10. [Caracteres Reservados](#10-caracteres-reservados)
  11. [Anatomia Documento](#11-anatomia-documento)
  12. [Criando Projetos](#12-criando-projetos)


* Trabalhando com Elementos
  1. [Semântica](#1-semântica)
  2. [Títulos e Parágrafos](#2-títulos-e-cabeçalhos)
  3. [Listas](#3-listas)
  4. [Citações](#4-citações)
  5. [Abreviações](#5-abreviações)
  6. [Detalhes de contato](#6-detalhes-de-contato)
  7. [Lista de descrição](#7-lista-de-descrição)
  8. [Representação de código](#8-representação-de-código)
  9. [Elementos Genéricos](#9-elementos-genéricos)

* Links
  1. [Conhecendo a tag âncora](#1-conhecendo-a-tag-âncora)
  2. [Utilizando a tag âncora](#2-utilizando-a-tag-âncora)
  3. [Conteúdos dentro do elemento a](#3-conteúdos-dentro-do-elemento-a)
  4. [Caminhos e URLS](#4-caminhos-e-urls)
  5. [Como navegar pelos diretórios](#5-como-navegar-pelos-diretórios)
  6. [Caminhos absolutos vs relativos](#6-caminhos-absolutos-vs-relativos)
  7. [Apresentação do exercício](#7-apresentação-do-exercício)
  8. [Resolução do exercício](#8-resolução-do-exercício)

* Tabelas
  1. [Tabelas](#1-tabelas)
  2. [Tabela básica](#2-tabela-básica)
  3. [Organizando Tabelas](#3-organizando-tabelas)
  4. [Tabela complexa](#4-tabela-complexa)
  5. [THead complexo](#5-thead-complexo)
  6. [TBody complexo](#6-tbody-complexo)
  7. [Melhorando o aspecto com colgroup](#7-melhorando-o-aspecto-com-colgroup)
  8. [Melhorando acessibilidade](#8-Melhorando-acessibilidade)

* Cabeçalho
  1. Head
  2. Meta
  3. Favicon
  4. Meta SEO
  5. Meta Social

-----------------------

<details open>
<summary><strong>Conceitos</strong></summary>
<br>

## 1. Abertura

Vamos aprender nesse curso sobre o que é HTML.
<br><br>

## 2. Instalando plugin de preview HTML

Instalar a extensão do VS Code: html preview (Thomas Haakon Townsend)

Ao utilizar essa extensão, as alterações são refletidas no preview e isso ajuda em tempo de desenvolvimento.

Vamos criar nosso primeiro arquivo html que será chamado de `index.html`.

Dicas para nomenclatura do arquivo:
- Não usar acentuação como ã, é, õ, entre outros.
- Evitar usar caracteres especiais como ç, @, #, %, entre outros
- Usar extensão `.html`.
- Não usar espaço no nome do arquivo, utilizar o `_`.
  - Exemplo do que não fazer: `minha pagina.html`
  - Exemplo correto: `minha_pagina.html`
<br><br>

## 3. O que é HTML

HTML = Hypertext Markup Language ou linguage de marcação de hipertexto.

Não é uma linguagem de programação e sim de marcação (por conta das tags). Tem sua própria sintaxe e semântica.

O hipertexto se refere a elementos além do texto escrito, como links, imagens, etc o que enriquece o documento html.
<br><br>

## 4. Comentários

Para utilizar comentários em HTML, é necessário utilizar as marcações `<!--` para iniciar o comentário e `-->` para finalizar o comentário. O que estiver entre as marcações de comentários não será renderizado.

Comentários são bem úteis para colocar observações ou para testes que são feitos ao longo do desenvolvimento.

Exemplo:

```
<!--
Aqui vai um comentário que não aparecerá na página renderizada
-->
```
<br>

## 5. Anatomia das Tags

As tags no HTML em geral tem a seguinte anatomia:
- Abertura da tag: `<tag>`
- Fechamento da tag: `</tag> ou <tag/>`
- Conteúdo: O que está entre as tags de abertura e fechamento
    - Exemplo: `<tag>titulo</tag>`, nesse caso, `titulo` é o contéudo entre as tags de abertura e fechamento
- Elementos: O conjunto entre a abertura, conteúdo e fechamento constitui um elemento HTML.
    - Exemplo: abaixo é um elemento HTML
    ```
    <tag>
      titulo
    </tag>
    ```
- Elementos vazio: Alguns elementos HTML não precisam ter conteúdo e não é necessário ter a tag de fechamento.
    - Exemplo: as tags `<input>` e `<img>`.
<br><br>

## 6. Atributos

Atributos de tags HTML podem ser informações extras ou configurações. Os atributos podem necessitar de um conteúdo ou ser um atributo booleano.

Atributos com conteúdo tem o formato `<tag atributo="conteudo">` onde `atributo` é o nome do atributo e `"conteudo"` é o valor do conteúdo.

O conteúdo de um atributo deve ser informado depois do sinal de igual (`=`) e o mesmo pode estar envolto de aspas simples(`''`), duplas(`""`) ou até mesmo sem nada.

Exemplos:
  - `<a href=http://www.google.com>Link 1</a>`
  - `<a href='http://www.google.com'>Link 2</a>`
  - `<a href="http://www.google.com">Link 3</a>`

Atributos booleanos só necessitam ter o atributo na tag HTML para ter efeito. Exemplo: `<input disabled>`, neste caso, só de ter a presença do atributo `disabled` é o suficiente para desabilitar a tag `<input>`.
<br><br>

## 7. Atributos globais
Todas as tags possuem atributos globais em comum, entre eles:
  - class
  - contenteditable
  - data-*
  - hidden
  - id
  - style
  - tabindex
  - title

Para mais atributos globais, é possível encontrá-los no seguinte [link][1].
<br><br>

## 8. Aninhamento Hierarquia

Alguns aspectos com relação ao aninhamento de tags que são importantes saber:
- Hierarquia
- Fluxo
- Posicionamento dos elementos

<br>

Com relação a hierarquia, as tags podem ser aninhadas, ou seja, uma tag estar dentro de outra, tendo uma relação de tag pai e tag filha.
```
<div>
  <p>Um texto <em>enfatizado</em>.</p>
</div>
```
Neste exemplo `<div>` é uma tag raiz, que é pai da tag `<p>` que é pai da tag `<em>`. `<em>` é tag filha da tag `<p>` que é filha da tag `<div>`.
<br><br>
A hierarquia entre as tags teria a seguinte árvore:
```
1. <div>
  2. <p>
    3. <em>
```
<br><br>
O fluxo de renderização das tags HTML é feita de cima pra baixo, da esquerda pra direita. Portanto uma tag que aparece primeiro no arquivo será renderizada antes que qualquer outra tag abaixo (claro, sem levar em conta modificadores como classes css ou atributos).
```
<p>Texto 1 <em>enfatizado</em></p>
<p>Texto 2 <strong>negrito</strong></p>
<p>Texto 3</p>
```
As tags acima sempre renderizará:
```
Texto 1 enfatizado
Texto 2 negrito
Texto 3
```
<br><br>
Quanto ao posicionamento dos elementos HTML, existem elementos que serão renderizados em linha e outros não, podendo quebrar linha ou outras formas de exibição.

```
<p>Texto 1 <em>enfatizado</em></p>
```
Saída:
```
Texto 1 enfatizado
```
Neste exemplo, o texto todo é renderizado em uma linha apenas.
<br><br>
```
<p>
  Texto 1 
  <em>
    enfatizado
  </em>
</p>
```
Saída:
```
Texto 1 enfatizado
```
E isso acontecerá mesmo que eu quebre linhas dentro da tag `<p>`.
<br><br>
```
<p>Texto 1 <em>enfatizado</em> com<p>outro parágrafo</p></p>
```
Saída:
```
Texto 1 enfatizado com
outro parágrafo
```
No exemplo acima, mesmo que eu escreva tudo em uma linha, haverá uma quebra de linha devido a tag `<p>` pois ela é renderizada em outro bloco de texto.
<br><br>
```
<p>
  Texto 1 

  <em>enfatizado</em>
  com

  <p

    >outro parágrafo

  </p>
  
</p>
```
Saída:
```
Texto 1 enfatizado com
outro parágrafo
```
Mesmo que eu quebre muito mais linhas, a saída será a mesma do exemplo anterior.
<br><br><br>
É interessante perceber este comportamento pois isso impactará em como o documento HTML será renderizado.

E uma tag disponivel para conseguirmos quebrar a linha dentro de uma tag `<p>` é utilizando a tag `<br>` (ou `<br/>`), que vem de `break`, do inglês "quebra".

```
<p>Texto 1 <em>enfatizado</em> com <br>outro parágrafo</p>
```
Saída:
```
Texto 1 enfatizado com
outro parágrafo
```
A saída terá uma quebra de linha, mas atente-se que não foi gerado um novo parágrafo  ou bloco de texto, é apenas uma quebra de linha.
<br><br>
Estes 3 aspectos são bem importantes para entender como os elementos serão exibidos, qual a relação entre eles e em que ordem serão renderizados.
<br><br>
## 9. Praticando

Execício para escrever 2 parágrafos, dando ênfase e importância para algumas palavras. Ao final, adicione um link de saiba mais.

Requisitos:
- use a tag `em` para ênfase
- use a tag `string` para importância
- o link pode ser para o google

<details>
  <summary>Sugestão</summary>
  <p>

    <p>Olá, esse é o resultado da prática, pois a <em>prática leva a perfeição</em>!!</p>

    <p>Você sabe como alcançar o próximo nível? <strong>É praticando!!</strong></p>

    <a href="http://www.google.com">Saiba mais, clicando aqui</a>

  </p>
</details>
<br><br>

## 10. Caracteres Reservados

Alguns símbolos especiais são caracteres reservados na linguagem HTML e eles podem ser interpretados de forma que você não espera e gerar alguns problema na visualizar a sua página.

Exemplos desses caracteres reservados são: `<`, `>`, `"`, `'`. 

Um motivo bem óbvio é que esses caracteres fazem parte das tags HTML.

Caso deseje utilizar alguns deles dentro de um conteúdo de texto é necessário trocá-los por códigos específicos que são interpretados pelo HTML, como por exemplo:
- `<` - `&lt;`
- `>` - `&gt;`
- `"` - `&quot;`
- `'` - `&apos;`
- `&` - `&amp;`
<br><br>

## 11. Anatomia Documento

Até agora vimos vários conceitos que são necessários para começar a criar um documento HTML, porém ainda não sabemos qual a estrutura básica de um documento HTML.

Todo documento HTML começa com a tag `<html>` que é a tag raiz. Podemos ter uma marcação para o HTML5 que é o `<!DOCTYPE html>` antes da tag principal do documento.

Existem duas tags filhas principais do `html` que são: `head` e `body`.

A tag `<head>` é responsável por conter diversas tags com configurações da página, como título, charset, estilos, scripts, metadados diversos, entre outros.

A tag `<body>` é onde estarão as tags de conteúdo da página que o usuário visualizará como textos, tabelas, imagens, links, entre outros.

Um documentos simples e básico pode ser descrito da seguinte forma:
```
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
  </body>
</html>
```

Utilizando o emmet `!` do VS Code, é criado um template básico de um documento HTML.
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  
</body>
</html>
```
Com isso, temos um básico para começar a criar páginas HTML.
<br><br>

## 12. Criando Projetos

Para iniciar um projeto, bastar criar um arquivo `index.html` em qualquer diretório do seu computador (onde você tenha permissão para alterar, como a pasta Documentos).

Para desenvolver uma página HTML é necessário apenas um editor de texto, que pode ser qualquer um, até mesmo o bloco de notas do Windows. Para projetos maiores que necessitam de controle de versão e outros utilitários, uma recomendação é utilizar o [VS Code][2], um editor gratuito.
****
</details>
<br>

<details open>
<summary><strong>Trabalhando com Elementos</strong></summary>
<br>

## 1. Semântica

A função da semântica é dar significado aos elementos HTML utilizados no documento. Para tornar o documento mais semântico é necessário utilizar elementos semânticos. 

A linguagem HTML fornece vários elementos semânticos que possibilitam tornar um documento HTML mais fácil de ser consumido tanto por humanos quantos pelos robôs dos motores de busca. 

Ao começar a escrever um documento HTML é interessante pensar em como estruturá-lo de forma que cada elemento seja apresentado de forma que fique mais fácil de ser interpretado. Por exemplo, destacar os tópicos com tags de cabeçalho (`<h1>`, `<h2>`...), apresentar listas com elementos ordenados ou sem ordem, citações, blocos de código  e também temos alguns elementos genéricos que podem ser utilizados para melhorar a semântica.

<br>

## 2. Títulos e cabeçalhos

Tags de título são `<h1>`, `<h2>`, `<h3>`, até `<h6>` e tag de parágrafo `<p>`.

Para um leitor, faz diferença em como um texto é apresentado. Se é uma tripa de letras ou está bem formatado. As tags acima podem ser utilizadas para deixar mais legível um texto.

Exemplo de um texto sem elementos semânticos:
```
Título
primeiro parágrafo
subtítulo
segundo parágrafo
```

Saída em HTML:
<blockquote>
Título
primeiro parágrafo
subtítulo
segundo parágrafo
</blockquote>
<br>
Exemplo de texto com elementos semânticos:

```
<h1>Título</h1>
<p>primeiro parágrafo</p>
<h2subtítulo</h2>
<p>segundo parágrafo</p>
```

Saída em HTML:
<blockquote>
<h1>Título</h1>
<p>primeiro parágrafo</p>
<h2>subtítulo</h2>
<p>segundo parágrafo</p>
</blockquote>

Veja que há uma boa diferença e isso facilita o leitor a interpretar o que é um título e o que é um parágrafo.

<br>
As tags de cabeçalho tem uma diferença visual que ajudam a destacar o texto.

<blockquote>
<h1>h1</h1>
<h2>h2</h2>
<h3>h3</h3>
<h4>h4</h4>
<h5>h5</h5>
<h6>h6</h6>
</blockquote>
<br>

## 3. Listas

Temos dois tipos de listas que podem ser usados: lista ordenada e lista não-ordenada.

As listas ordenadas terão um número antes de cada item e devem ser usadas quando a ordem é um fator importante da informação, por exemplo, uma sequência de passos de um algoritmo. Usamos a tag `<ol>` (ordered list).

As listas não-ordenadas terão apenas um marcador antes de cada item e devem ser utilizadas quando a ordem dos itens não tem relevância, como em uma lista de ingredientes de um bolo, onde todos os ingredientes são necessários para fazer a receita. Usamos a tag `<ul>` (unordered list).

Cada item da lista é representado pela tag `<li>` (list item), para os dois tipos de lista.

```
<h2>Ingredientes</h2>
<ul>
  <li>Ovo</li>
  <li>Sal</li>
  <li>Óleo</li>
</ul>

<h2>Instruções</h2>
<ol>
  <li>Pegue uma frigideira e jogue um pouco de óleo em fogo baixo</li>
  <li>Quebre o ovo e jogue na frigideira</li>
  <li>Deixe o ovo fritar e retire antes que queime</li>
  <li>Tempere com sal a gosto</li>
</ol>
```

Saída em HTML:

<h2>Ingredientes</h2>
<ul>
  <li>Ovo</li>
  <li>Sal</li>
  <li>Óleo</li>
</ul>

<h2>Instruções</h2>
<ol>
  <li>Pegue uma frigideira e jogue um pouco de óleo em fogo baixo</li>
  <li>Quebre o ovo e jogue na frigideira</li>
  <li>Deixe o ovo fritar e retire antes que queime</li>
  <li>Tempere com sal a gosto</li>
</ol>
<br>

## 4. Citações

Temos as seguintes opções para fazer citações:
 - `<blockquote>`
 - `<cite>`
 - `<q>`

 ```
 <blockquote cite="https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/blockquote">
  O <strong>Elemento HTML <code>&lt;blockquote&gt;</code></strong> (ou <em>HTML Block Quotation Element</em>) indica que um texto externo foi citado.
 </blockquote>

 <p>De acordo com <a href="https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/blockquote">
  <cite>página MDN blockquote</cite></a>:
 </p>

 <p>O elemento quote - <code>&lt;q&gt;</code> - é <q cite="https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/q">usado para citações curtas que não precisam de parágrafos ou quebras de linha.</q> -- <a href="https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/q"><cite>MDN q page</cite></a>.</p>

 ```
<br>

## 5. Abreviações

A tag `<abbr>` (_abbreviation_) é usada para abreviações, esta tag coloca um estilo diferenciado em seu conteúdo para informar ao usuário que ela é uma abreviação e descansando o mouse em cima dela, é possível ver o atributo `title` da tag.

```
<p>Usamos <abbr title="Hypertext Markup Language">HTML</abbr> para estruturar nossos documentos web.</p>
```
<br>

## 6. Detalhes de contato
A tag `<address>` é utilizada para detalhes de contato de quem criou a página. Não serve para informar um endereço qualquer.
<br><br>

```
<address>
  <p>Danilo Yorinori<br>
  <strong>Curitiba - PR</strong>
</address>
```

Esta tag tem mais um significado semântico do que visual.
<br><br>

## 7. Lista de descrição

A tag `<dl>` (_description list_) é usada para uma lista de descrição, como um glossário.
As tags filhas são `<dt>` (_description term_) para os termos e `<dd>` (_description detail_) para a explicação do termo.

```
<dl>
  <dt>Description term</dt>
  <dd>Description detail</dd>
</dl>
```

A lista de descrição tem uma formatação bem específica como podemos ver a seguir:
<blockquote>
  <dl>
    <dt>Description term</dt>
    <dd>Description detail</dd>
  </dl>
</blockquote>
<br>

## 8. Representação de código

Temos duas tags para representar código no HTML:
 - `<code>`
 - `<pre>`

A tag `<code>` é utilizada para trechos simples de código, partes genéricas ou apenas para destacar algum termo no texto.

Quando for necessário exibir um trecho de código onde identação e várias linhas de código são relevantes, é melhor utilizar a tag `<pre>`.
<br><br>

Exemplos:
```
<code>document.querySelector("body")</code>
```
<blockquote>
Código simples<br>
<code>document.querySelector("body")</code>
</blockquote>
<br>

```
<code>
document
  .querySelector("body")
</code>
```
<blockquote>
Código com quebra de linha<br>
<code>
document
  .querySelector("body")
</code>
</blockquote>
<br>

```
<code>
<pre>
document
  .querySelector("body"
</pre>
</code>
```
<blockquote>
Código com quebra de linha
<code>
<pre>
document
  .querySelector("body"
</pre>
</code>
</blockquote>
Pelos exemplos observamos que quando é necessário mostrar um trecho de código grande de código, é usar uma combinação das duas tags.

Um detalhe importante é que caso seja necessário exibir um código HTML dentro de um documento HTML, é necessário usar os caracteres especiais (`&gt;`, `&lt;`), caso contrário o HTML pode ser renderizado com alguns problemas.

Por questão de curiosidade mas que deve ser evitada é a utilização da tag `<xmp>`, dentro desta tag não é necessário traduzir os símbolos reservados do HTML.


```
<xmp>
<pre>
  <code>
document
  .querySelector("body")
  </code>
</pre>
</xmp>
```
<br>

## 9. Elementos genéricos

Temos dois elementos genéricos que podem ser utilizados e são bem utilizados em desenvolvimentos que são as tags:
- `<div>`
- `<span>`

A tag `<div>` (_division_) é utilizada para agrupar conteúdo e traz uma ideia de bloco.

A tag `<span>` é utilizada para agrupar texto e será renderizada em linha.

```
<div>
  texto qualquer
  <span>com outro</span>
</div>
<span>texto</span>
qualquer
```

<blockquote>
<div>
  texto qualquer
  <span>com outro</span>
</div>
<span>texto</span>
qualquer
</blockquote>

O que ficou dentro do `<div>` ficou renderizado em linha, mas está em um bloco diferente do que está fora da mesma tag.

Estas duas tags são bem utilizadas pois permitem customizar cada uma das tags com os atributos globais como `id`, `class`. São fundamentais para criação de páginas utilizando Javascript e CSS.
***
</details>

<details open>
  <summary>Links</summary>
<br>

## 1. Conhecendo a tag âncora
A tag `<a>` (_anchor_) é uma das principais tags do HTML, ela que possibilita o _link_ entre os documentos. A partir do _link_ de um documento, você pode navegar para outro com um clique.

Esta tag tem uma série de atributos que são comumente utilizados, alguns dos principais são:
- `href`
- `download`
- `target`

O atributo `href` (_hyperlink reference_) é o principal atributo da tag `<a>` e este atributo pode ter diversas funções como:
- Apontar para outro documento HTML
- Apontar para um fragmento no mesmo documento HTML
- Enviar um email
- Iniciar uma chamada telefônica (dependendo da plataforma)
- Outras funções

O atributo `download` informa que deverá ser realizado o download do que está sendo referenciado no atributo `href`. O valor desta tag é o nome padrão do arquivo que será baixado.

O atributo `target` informa onde deve ser disponibilizado o conteúdo da âncora, o valor padrão deste atributo (quando não informado) é o `_self`.
- `_self` indica que o conteúdo deverá ser aberto na mesma aba
- `_blank` indica que o conteúdo deverá ser aberto em uma nova aba 
<br><br>

## 2. Utilizando a tag âncora

Para detalhar melhor o atributo `href`, ele pode receber diversos valores e alguns com funções bem específicas.

A utilização mais comum é apontar para outro documento HTML. E o valor pode ser uma URL completa ou utilizar um caminho relativo para o documento. Quando o atributo `href` estiver vazio, a referência é o próprio documento.

Ao utilizar o prefixo `mailto:` podemos em seguida informar um e-mail e ao clicar no link o gerenciador de e-mails abrirá e permitirá o envio para o endereço configurado na tag.

Ao utilizar o prefixo `tel:` seguido do número de um telefone, é possível iniciar uma ligação telefônica. Isso depende da plataforma. Geralmente é melhor utilizado no caso de abrir a página em um smartphone.

Para exemplificar os usos desta tag:
```
<ul>
  <li><a href="">Homepage</a></li>
  <li><a href="https://www.google.com">Google</a></li>
  <li><a href="mailto:daniloksy@gmail.com">Email</a></li>
  <li><a href="tel:+5541999999999">Telefone</a></li>
</ul>
```

Outra utilização possível é apontar para um fragmento de uma página, por exemplo, um título, uma imagem. O prefixo utilizado para este caso é o `#`. Qualquer outro elemento dentro da página que contenha o `id` especificado com o prefixo `#` será exibido ao clicar no link.
```
<ul>
  <li><a href="">Homepage</a></li>
  <li><a href="#secao1">Seção 1</a></li>
  <li><a href="#secao2">Seção 2</a></li>
  <li><a href="#secao3">Seção 3</a></li>
</ul>

<h2 id="secao1">Seção 1</h2>
<h2 id="secao2">Seção 2</h2>
<h2 id="secao3">Seção 3</h2>
```
No exemplo acima, ao clicar no link da Seção 1, iremos direto pro título com `id` igual a `secao1`.

Para documentos com um índice, este recurso de link apontando para um fragmento de página é comumente utilizado.
<br><br>

## 3. Conteúdos dentro do elemento a
Dentro da tag `<a>` é possível utilizar outras tags, como `<h1>`, `<img>`, não apenas um texto puro. Podemos até mesmo utilizar mais de uma tag dentro da tag `<a>`.
```
<a href="https://www.google.com"><h1>Google</h1></a>
<a href="https://www.google.com"><img src="https://www.google.com.br/images/branding/googlelogo/2x/googlelogo_color_160x56dp.png" alt="google"></img></a>

<a href="https://www.google.com">
  <h1>Google</h1>
  <img src="https://www.google.com.br/images/branding/googlelogo/2x/googlelogo_color_160x56dp.png" alt="google"></img>
  <p> Vamos para o google?
</a>
```
<br>

## 4. Caminhos e URLS

Um link utiliza uma URL (_Uniform Resource Locator_) para saber a localização de um recurso para ser exibido ou baixado ao ser clicado. Uma URL é uma string que define onde algo está localizado na web. O recurso pode estar dentro do próprio projeto ou em algum lugar externo.

Caso o recurso esteja dentro do próprio projeto, usa-se o caminho do arquivo para acessá-lo. Exemplo: `caminho-para-arquivo/arquivo.html`.

Caso o recurso não esteja dentro do próprio projeto, é necessário informar a URL completa para poder acessá-lo. Exemplo: `http://www.facebook.com`.
<br><br>

## 5. Como navegar pelos diretórios

Para informar a localização exata de um recurso dentro de um projeto é necessário informar o caminho para este recurso e não é necessário que o recurso esteja no mesmo diretório da página que está sendo exibida.

Para informar o caminho do arquivo ao navegador, usamos a seguinte notação:
- recurso no mesmo diretório: sem prefixo `nome-recurso` ou com prefixo `./nome-recurso`
- arquivo em diretório dentro do diretório atual: `<nome_dir>/nome-recurso`
- arquivo em diretórior anterior ao diretório atual: `../<nome_dir>/nome-recurso`

Claro que podemos ter encadeamento dessas notações para poder informar a localização exata de um arquivo como:
- `../src/app/component/index.html`
- `../../../assets/file.png`
- `../../app/components/item-detail/controller.ts`

É importante conhecer esta notação para conseguir informar o caminho de um recurso, caso contrário, ao tentar acessá-lo informando o caminho incorreto, será exibida uma mensagem de erro 404 para o usuário.
<br><br>


## 6. Caminhos absolutos vs relativos

Temos que diferenciar o que é caminho absoluto de caminho relativo:
- Caminho absoluto é aquele onde informados a URL completa para acessar determinado recurso, com protoloco e nome do domínio. Sempre apontará para o mesmo local não importa em que lugar dentro do projeto ele esteja sendo referenciado.
- Caminho relativo é o caminho relativo ao recurso atual, ou seja, posso ter mesma referência em diversas páginas dentro de um projeto, mas cada página pode abrir um recurso diferente.
<br><br>

## 7. Apresentação do exercício

Para testar os conhecimentos obtidos até agora, faça o seguinte exercício:

### **Criando naveção entre arquivos**
- Crie um projeto contendo
  - 2 arquivos no diretório principal (`index.html` e `contact.html`)
  - 1 diretório de nome: `files`
    - dentro desse diretório, adicione 2 imagens da sua preferência e 1 arquivo de nome  `image.html`, que listará as imagens.
<br><br>

### **Dentro de cada arquivo .html, você deverá colocar:**
1. Título `<h1>` da página
2. Menu de navegação com uma lista `<li>` não ordenada `<ul>`.
3. Um ou mais parágrafos `<p>` com informações da página.
<br><br>

### **A navegação**
Para o menu de navegação, use a tag `<nav>` e coloque a lista não ordenada como conteúdo da tag.

O conteúdo de cada item da lista `<li>` deverá conter um link `<a>`.

O conteúdo do link deverá ser o nome da página .html que existe no projeto, sendo que para cada página, iremos ter um link.

Ao clicar no link, deveremos ser direcionados à página clicada.
<br><br>

### **Página images.html**

Como conteúdo desta página, além do que foi pedido, adicionar também:
1. As duas imagens que você tem na pasta
2. Use a tag `<p>` para colocar a tag `<img>`

*obs:* imagens de tamanho muito grande poderão não se adaptar bem, mas não se preocupe com isso agora, pois logo aprenderemos como melhorar isso.
<br><br>

### **Página contact.html**

Como conteúdo desta página, além do que foi perdido, adicionar também:
1. Colocar suas informações de contato: email e telefone
2. Cada informação deverá estar dentro de um link que quando clicado, abrirá a respectiva informação de contato (email ou telefone)
<br><br>

### **Dicas**

Para o conteúdo da tag `<p>`, se desejar, poderá fazer uso do atalho `lorem` que existe no VS Code.<br>
Para isso, digite `lorem` e em seguida aperte tab.<br>
Atenção: em alguns computadores isso pode não funcionar, portanto, não se atenhe a isso e continue o exercício sem essa dica.
<br><br>

## 8. Resolução do exercício

Resolvido na pasta `exercicio_links` deste repositório.

  ***
</details>
<br>

<details open>
<summary>Tabelas</summary>
<br>

## 1. Tabelas

O elemento `<table>` é importante para organizar os dados para uma melhor visualização pois ele pode estruturar os dados em linhas e colunas.

As vantagens de utilizar uma tabela é que ela provê uma melhor visualização das informações via linhas e colunas. Tem uma boa acessibilidade para leitura dos dados.

Algumas desvantagens são a pouca flexibidade e a necessidade de uma estilização para melhorar a visualização dos dados (a organização em linhas e colunas de forma simples pode não ser o suficiente).

Não deve-se usar tabelas para criar layouts (elas já foram utilizadas antigamente para construir layouts mas hoje em dia existem outras técnicas muito melhores e mais flexíveis).
<br><br>

## 2. Tabela básica

Para criar uma tabela simples, precisamos das seguintes tags:
- `<tr>` - Indica a criação de uma linha da tabela (_table row_)
- `<th>` - Indica uma coluna de cabeçalho (_table header_)
- `<td>` - Indica o dado, valor, descrição de uma coluna (_table data_)

Com essas tags, um exemplo simples de tabela seria:
```
<table>
  <tr>
    <th>Editora</th>
    <th>Super-herói</th>
  </tr>
  <tr>
    <td>DC</td>
    <td>Superman</td>
  </tr>
  <tr>
    <td>Marvel</td>
    <td>Homem-aranha</td>
  </tr>  
</table>
```

O código acima gerará uma tabela similar a seguinte:
Editora | Super-herói
--------|------------
DC      | Superman
Marvel  | Homem-aranha

<br><br>


## 3. Organizando Tabelas

Para deixar nossa tabela ainda mais organizada e semântica, vamos utilizar mais algumas tags:
- `<thead>` - Organiza o conteúdo de cabeçalho da tabela 
- `<tbody>` - Organiza o conteúdo do corpo da tabela
- `<tfoot>` - Organiza o conteúdo do rodapé da tabela
- `<caption>` - Descreve o título da tabela 

```
<table>

  <caption>
    Tabela de editora x super-herói
  </caption>

  <thead>
    <tr>
      <th>Editora</th>
      <th>Super-herói</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>DC</td>
      <td>Superman</td>
    </tr>
    <tr>
      <td>Marvel</td>
      <td>Homem-aranha</td>
    </tr>  
  </tbody>
    <tr>
      <td>Total:</td>
      <td>2 super-heróis</td>
    </tr>    
  <tfoot>
  </tfoot>
</table>
```

O código acima gerará uma tabela similar a seguinte:

<caption>
  Tabela de editora x super-herói
</caption>

Editora | Super-herói
--------|------------
DC      | Superman
Marvel  | Homem-aranha
Total   | 2 super-heróis

<br><br>

## 4. Tabela complexa

Para exemplificar uma tabela complexa, vamos partir de um exemplo que á construção de uma tabela de 2 lojas com a relação de produtos produzidos e vendidos, onde a linha abaixo da coluna com o nome da loja deve ter duas colunas com os produtos produzidos e vendidos.

A tabela deve ficar como o exemplo a seguir:
```
|          |         loja 1          |           loja 2         |
|          | produzidos | vendidos   |  produzidos | vendidos   |
-----------------------------------------------------------------
| prod1    |    qtd     |     qtd    |      qtd    |   qtd      |
| prod2    |    qtd     |     qtd    |      qtd    |   qtd      |
-----------------------------------------------------------------
```

<br>

## 5. THead complexo

Por passos, vamos criar nosso cabeçalho.

Definir a tabela e uma caption:
```
<table>
  <caption>Produzidos e vendidos por loja</caption>
</table>
``` 

Primeira linha do cabeçalho com o nome das lojas:
```
<table>
  <caption>Produzidos e vendidos por loja</caption>
  <thead>
    <tr>
      <th></th>
      <th>Loja 1</th>
      <th>Loja 2</th>
    </tr>
  </thead>
</table>
``` 

Segunda linha do cabeçaho:
```
<thead>
  <tr>
    <th></th>
    <th>Loja 1</th>
    <th>Loja 2</th>
  </tr>
  <tr>
    <th>Produzidos</th>
    <th>Vendidos</th>
    <th>Produzidos</th>
    <th>Vendidos</th>    
  </tr>
</thead>
``` 
<br>

Após adicionar a segunda linha, vemos que a tabela não está ficando do jeito que queremos.
```
|            | loja 1   | loja 2     |
| produzidos | vendidos | produzidos | vendidos |
```

Precisamos fazer com que a primeira coluna da primeira linha, ocupe tanto a primeira coluna da primeira linha como a segunda linha também. Para isso podemos usar o atributo `rowspan`. Esse atributo informa quantas linhas uma coluna deve ocupar.
```
<tr>
  <th rowspan="2"></th>
  <th>Loja 1</th>
  <th>Loja 2</th>
</tr>
```

Ao adicionar o `rowspan`, a tabela deve ficar da seguinte forma:
```
|            |   loja 1   | loja 2   |
|            | produzidos | vendidos | produzidos | vendidos |
```

Ainda não está do jeito que queremos. Agora é necessário fazer as colunas com nome das lojas ocuparem 2 colunas cada usando o atributo `colspan`.
```
<tr>
  <th rowspan="2"></th>
  <th colspan="2">Loja 1</th>
  <th colspan="2">Loja 2</th>
</tr>
```

Agora o resultado estará assim:
```
|            |         loja 1        |        loja 2         |
|            | produzidos | vendidos | produzidos | vendidos |
```
<br>

## 5. TBody complexo

Para adicionar as linhas com informações dos produtos, podemos usar a tag `<tbody>`.
```
<tbody>
  <tr>
    <th>Produto 1</th>
    <td>50</td>
    <td>40</td>
    <td>30</td>
    <td>30</td>
  </tr>
  <tr>
    <th>Produto 2</th>
    <td>10</td>
    <td>10</td>
    <td>25</td>
    <td>20</td>
  </tr>
</tbody>
```

Usamos a tag `<th>` no corpo da tabela para destacar que uma coluna também contém uma informação chave.

Teremos algo assim no momento:
<blockquote>
  <table>
    <caption>Produzidos e vendidos por loja</caption>
    <thead>
      <tr>
        <tr>
          <th rowspan="2"></th>
          <th colspan="2">Loja 1</th>
          <th colspan="2">Loja 2</th>
        </tr>
      </tr>
      <tr>
        <th>Produzidos</th>
        <th>Vendidos</th>
        <th>Produzidos</th>
        <th>Vendidos</th>    
      </tr>
    </thead>
    <tbody>
      <tr>
        <th>Produto 1</th>
        <td>50</td>
        <td>40</td>
        <td>30</td>
        <td>30</td>
      </tr>
      <tr>
        <th>Produto 2</th>
        <td>10</td>
        <td>10</td>
        <td>25</td>
        <td>20</td>
      </tr>
    </tbody>
  </table>
</blockquote>
<br>

## 7. Melhorando o aspecto com colgroup

A tabela está organizada, mostrando os dados conforme o pedido, porém podemos deixar a informação ainda mais visívl estilizando as colunas. Para esta necessidade, podemos utilizar a tag `<colgroup>` que deve ficar após a tag `<caption>` e antes da tag `<thead>`.

Na tabela temos 3 grandes colunas principais apesar de na realidade termos 5 colunas. Para deixar ainda mais claro as informações de cada loja, pode-se estilizar as colunas de cada loja.

```
...
<caption>Produzidos e vendidos por loja</caption>

<colgroup>
  <col>
  <col style="background-color: red">
  <col style="background-color: blue">
</colgroup>

<thead>
...
```

Ao fazer isso, a tabela não vai ficar do jeito esperado, pois a segunda e terceira foram estilizadas e a intenção era colorir a segunda e terceira com a cor vermelha e a quarta e quinta com azul.

Pode-se repetir a estilização para fica do jeito que desejado.
```
<colgroup>
  <col>
  <col style="background-color: red">
  <col style="background-color: red">
  <col style="background-color: blue">
  <col style="background-color: blue">
</colgroup>
```

Mas há uma alternativa sem precisar repetir linhas de códigos, que no caso é fazer o `span` das estilizações para mais colunas. Diferentemente da tag `<th>`, não temos um atributo `colspan`, mas sim apenas `span` pois já estamos tratando com colunas no `colgroup`.
```
<colgroup>
  <col>
  <col span="2" style="background-color: red">
  <col span="2" style="background-color: blue">
</colgroup>
```
<br>

## 8. Melhorando acessibilidade
Para tornar a tabela mais semântica e melhorar a acessibilidade, pode-se informar o atributo `scope` nas tags `<th>`. Este atributo pode receber os seguintes valores:
- `col` - escopo de coluna
- `row` - escopo de linha
- `colgroup` - escopo de agrupamento de coluna
- `rowgroup` - escopo de agrupamento de linha

```
<thead>
  <tr>
    <tr>
      <th rowspan="2"></th>
      <th colspan="2" scope="colgroup">Loja 1</th>
      <th colspan="2" scope="colgroup">Loja 2</th>
    </tr>
  </tr>
  <tr>
    <th scope="col">Produzidos</th>
    <th scope="col">Vendidos</th>
    <th scope="col">Produzidos</th>
    <th scope="col">Vendidos</th>    
  </tr>
</thead>
<tbody>
  <tr>
    <th scope="row">Produto 1</th>
    ...
  </tr>
  <tr>
    <th scope="row">Produto 2</th>
    ...
  </tr>
</tbody>
```

***

</details>

[1]: https://developer.mozilla.org/pt-BR/docs/Web/HTML/Global_attributes
[2]: https://code.visualstudio.com