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
  1. Conhecendo a tag âncora
  2. Utilizando a tag âncora
  3. Conteúdos dentro de elemento a
  4. Caminhos e URLS
  5. Como navegar pelos diretórios
  6. Caminhos absolutos vs relativos
  7. Exercício de apresentação
  8. Exercício de resolução

* Tabelas
  1. Tabela básica
  2. Organizando Tabelas
  3. Tabela complexa
  4. THead complexa
  5. TBody complexo
  6. Melhorando o aspecto com colgroup
  7. Melhorando acessibilidade

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

</details>


[1]: https://developer.mozilla.org/pt-BR/docs/Web/HTML/Global_attributes
[2]: https://code.visualstudio.com