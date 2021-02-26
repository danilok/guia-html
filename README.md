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
  9. Praticando
  10. Caracteres Reservados
  11. Anatomia Documento
  12. Criando Projetos


* Trabalhando com Elementos
  1. Semântica
  2. Títulos e Parágrafos
  3. Listas
  4. Citações
  5. Abreviações
  6. Detalhes de contato
  7. Lista de descrição
  8. Representação de código
  9. Elementos Genéricos

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

# Conceitos
## 1. Abertura

Vamos aprender nesse curso sobre o que é HTML.

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

## 3. O que é HTML

HTML = Hypertext Markup Language ou linguage de marcação de hipertexto.

Não é uma linguagem de programação e sim de marcação (por conta das tags). Tem sua própria sintaxe e semântica.

O hipertexto se refere a elementos além do texto escrito, como links, imagens, etc o que enriquece o documento html.

## 4. Comentários

Para utilizar comentários em HTML, é necessário utilizar as marcações `<!--` para iniciar o comentário e `-->` para finalizar o comentário. O que estiver entre as marcações de comentários não será renderizado.

Comentários são bem úteis para colocar observações ou para testes que são feitos ao longo do desenvolvimento.

Exemplo:

```
<!--
Aqui vai um comentário que não aparecerá na página renderizada
-->
```

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

## 6. Atributos

Atributos de tags HTML podem ser informações extras ou configurações. Os atributos podem necessitar de um conteúdo ou ser um atributo booleano.

Atributos com conteúdo tem o formato `<tag atributo="conteudo">` onde `atributo` é o nome do atributo e `"conteudo"` é o valor do conteúdo.

O conteúdo de um atributo deve ser informado depois do sinal de igual (`=`) e o mesmo pode estar envolto de aspas simples(`''`), duplas(`""`) ou até mesmo sem nada.

Exemplos:
  - `<a href=http://www.google.com>Link 1</a>`
  - `<a href='http://www.google.com'>Link 2</a>`
  - `<a href="http://www.google.com">Link 3</a>`

Atributos booleanos só necessitam ter o atributo na tag HTML para ter efeito. Exemplo: `<input disabled>`, neste caso, só de ter a presença do atributo `disabled` é o suficiente para desabilitar a tag `<input>`.

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

## 8. Aninhamento Hierarquia

Alguns aspectos com relação ao aninhamento de tags que são importantes saber:
- Hierarquia
- Fluxo
- Posicionamento dos elementos

<br><br>
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

[1]: https://developer.mozilla.org/pt-BR/docs/Web/HTML/Global_attributes