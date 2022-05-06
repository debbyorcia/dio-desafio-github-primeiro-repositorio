## Introdução

Markdown é uma linguagem de marcação leve e simples criada por [John Gruber](https://daringfireball.net/projects/markdown/) em 2004, e que hoje em dia é uma das linguagens de marcação mais populares do mundo.

### Linguagens de marcação

Linguagens de marcação (também muito conhecidas pelo seu termo em inglês: *markup language*) são uma forma de anotação (ou marcação) de um texto simples sem formatação (também conhecido como *plain text*) de modo que ele se torne sintaticamente distinguível e possa ser manipulado por algum software.

Linguagens de marcação são utilizadas para definir formatos, maneiras de exibição e padrões dentro de um documento qualquer. Normalmente, elas não possuem qualquer estrutura de controle como as linguagens de programação tradicionais, e servem basicamente para definir como um determinado conteúdo será exibido na tela ou como os dados estarão estruturados ao trafegar entre os diferentes módulos de um sistema. As marcações normalmente são omitidas na versão final do documento, que é exibida para o usuário ou é impressa.

Exemplos de marcações são instruções de definição de tipo como existem no LaTeX, e marcadores estruturais tais como as tags XML ou HTML. LaTeX, XML e HTML são diferentes linguagens de marcação.

Algumas linguagens de marcação, tal como HTML, possuem semântica de apresentação, o que significa que sua especificação prescreve como o dado estruturado será mostrado.

#### Exemplos de linguagens de marcação

Cada linguagem de marcação possui sua própria sintaxe, a forma como as marcações são distinguidas do texto em si, com diferentes funcionalidades e propósitos.

O LaTex, por exemplo, que é uma linguagem de marcação que inclui recursos destinados à produção de documentação técnica e científica, é muito conhecida por sua sintaxe para exibição de expressões matemáticas, que possui marcações como `\frac{}{}` para definir uma fração e `\sqrt{}` para raiz quadrada. Neste sentido, o seguinte trecho em LaTeX:

```
x = \frac{1}{2}\left(\frac{1}{\sqrt{5}}\right)
```

Será apresentado da seguinte forma:

x=12(15)

Já o HTML, que é a linguagem de marcação utilizada na Web, utiliza os sinais `<>` (chevron, ou “menor que” e “maior que”, ou *angle brackets*) para envolver as *tags* de marcação que, por sua vez, devem envolver o texto que será marcado. As *tags* HTML `<p>` e `</p>`, por exemplo, são as *tags* de abertura e fechamento, respectivamente, de parágrafo. Neste sentido, o seguinte trecho em HTML:

```
<p>Este é um parágrafo com uma palavra em <b>negrito</b> e outra em <i>itálico</i>.</p>
```

Será apresentado da seguinte forma:

Este é um parágrafo com uma palavra em **negrito** e outra em *itálico*.

O Markdown, por fim, é uma linguagem de marcação bastante leve e simples, criada originalmente para escritores Web, para ser convertido em HTML válido, mas cuja sintaxe é muito menos *verbosa* e muito mais legível. Neste sentido, para obtermos o mesmo resultado do exemplo em HTML acima, a sintaxe em Markdown seria a seguinte:

```
Este é um parágrafo com uma palavra em **negrito** e outra em *itálico*.
```

Vamos ver mais sobre a sintaxe básica do Markdown mais adiante.

## Markdown

A sintaxe de formatação do Markdown foi criada com o objetivo de ser o mais legível possível. A ideia é que um documento formatado em Markdown pode ser publicável como está, como texto simples, sem parecer que foi marcado com *tags* ou instruções de formatação. ([CONE, 2018](https://www.amazon.com.br/Markdown-Guide-English-Matt-Cone-ebook/dp/B07G7JB641?__mk_pt_BR=ÅMÅŽÕÑ&dchild=1&keywords=The+Markdown+Guide&qid=1622315308&s=books&sr=1-1&linkCode=ll1&tag=inteligenci0a-20&linkId=98021054d25420fbbfbd469263cfad7c&language=pt_BR&ref_=as_li_ss_tl))

Em Markdown não é necessário usar *tags* de abertura e fechamento como em HTML, nem é preciso criar estilos de formatação, embora muitos editores Markdown tenham estilos predefinidos que podem ser simplesmente aplicados para a formatação do conteúdo. ([ALAM, 2018](https://www.amazon.com.br/Learn-Markdown-Complete-Guide-Formatting/dp/1980616493?__mk_pt_BR=ÅMÅŽÕÑ&dchild=1&keywords=Learn+Markdown%3A+The+Complete+Guide+on+Markdown+Formatting&qid=1622314672&s=books&sr=1-1&linkCode=ll1&tag=inteligenci0a-20&linkId=83f5768f50ca3a498ba77cb442ceba68&language=pt_BR&ref_=as_li_ss_tl))

O documento escrito com Markdown é formatado em uma única fonte e pode ser facilmente convertido em vários formatos, incluindo `.html`, `.docx`, `.pdf` e diversos outros formatos com o apoio de diferentes ferramentas gratuitas e *open source*, com diferentes propósitos e funcionalidades adicionais.

Neste momento eu estou escrevendo este artigo em Markdown, em um “dialeto” (uma variante com sintaxe estendida) chamado *Kramdown*, que possui uma sintaxe com funcionalidades adicionais muito úteis para utilização na Web.

### Vantagens do Markdown

Porque utilizar Markdown em vez de um editor *WYSIWYG* (um editor de textos estilo Microsoft Word ou LibreOffice Writer)? Por que escrever em Markdown em vez de pressionar botões em uma interface para formatar um texto? Existem alguns motivos diferentes para se usar o Markdown em vez de um editor WYSIWYG, na sequência listamos algumas.

- **Markdown pode ser usado para tudo.** Para criar sites, documentos, notas, livros, apresentações, mensagens de e-mail, documentação técnica, documentação acadêmica, etc;
- **Markdown é portátil.** Arquivos de texto escritos em Markdown podem ser abertos com praticamente qualquer aplicativo, o que contrasta fortemente com os aplicativos de processamento de texto do tipo WYSIWYG, que bloqueiam seu conteúdo em um formato de arquivo proprietário;
- **Markdown é independente de plataforma.** Texto formatado em Markdown pode ser criado em qualquer dispositivo que execute qualquer sistema operacional;
- **Markdown é à prova de futuro.** Se o aplicativo que você está usando parar de funcionar em algum momento no futuro, um texto formatado em Markdown ainda poderá ser lido e editado usando qualquer outro aplicativo de edição de texto. Essa é uma consideração importante quando se trata de livros, teses universitárias e outros documentos importantes que precisam ser preservados indefinidamente;
- **Markdown está em toda parte.** Inúmeros sites da Web suportam Markdown, e muitos aplicativos de desktop e baseados na Web o suportam. Existem conversores de Markdown para virtualmente todos os formatos existentes no mundo.

### Como o Markdown funciona

Quando escrevemos em Markdown o texto é armazenado em um arquivo de texto simples com extensão `.md` ou `.markdown`.

Para que um arquivo Markdown seja convertido em HTML ou em um documento pronto para impressão precisamos de um aplicativo Markdown capaz de processar o arquivo.

Existem inúmeros aplicativos disponíveis - tudo, desde scripts simples de linha de comando até aplicativos de desktop que se parecem com Word, passando por aplicativos baseados na Web. Apesar de diferentes, todos fazem a mesma coisa, convertem texto formatado em Markdown em HTML para que possa ser exibido em navegadores da Web ou convertido em outro formato (o que pode ser feito diretamente também).

Os aplicativos Markdown usam algo chamado de processador Markdown (também chamado de “analisador” - ou parser - ou de “implementação markdown”) para ler o texto Markdown e reescrevê-lo no formato HTML. E então o documento pode ser visualizado em um navegador da Web ou combinado com uma folha de estilos e ser impresso.

Sinteticamente, este é um processo de quatro partes:

1. Criar um arquivo Markdown usando um editor de texto ou um aplicativo Markdown dedicado. O arquivo deve ter uma extensão `.md` ou `.markdown`;
2. Abrir o arquivo Markdown em um aplicativo Markdown;
3. Usar o aplicativo Markdown para converter o arquivo Markdown em um documento HTML;
4. Visualizar o arquivo HTML em um navegador da web ou usar o aplicativo Markdown para convertê-lo em outro formato de arquivo, como PDF por exemplo.

O ponto de vista de um usuário sobre processo pode variar conforme a ferramenta utilizada, muitas das quais podem condensar estas etapas em praticamente uma, outras podem adicionar complexidade e funcionalidades extras, tudo conforme o propósito.

### Editor Markdown

Um documento Markdown pode ser escrito em qualquer editor de texto simples, pode ser escrito no bloco de notas do Windows, por exemplo. O que, todavia, não seria a forma mais inteligente de fazê-lo.

Como Markdown serve a muitos propósitos, existem editores mais e menos adequados a depender do que se está fazendo, de qual variação ou dialeto de Markdown está sendo utilizado, qual será o formato - ou formatos - finais, quais funcionalidades são necessárias, etc.

Neste artigo o objetivo é apenas fazer esta introdução conceitual e apresentar a sintaxe básica da linguagem. Nos artigos subsequentes da série apresentarei as principais ferramentas que uso no meu trabalho (para escrever este artigo, para escrever e automatizar o processo de escrita de laudos e documentos técnicos, etc) e no meu mestrado (para escrever a dissertação e gerenciar a bibliografia). Se inscreva em nossa [newsletter](https://www.inteligenciaurbana.org/2021/04/markdown-parte1.html#feed) para ser notificado da publicação de textos novos.

Para aqueles menos familiarizados e que queiram experimentar um pouco do Markdown sem precisar instalar nada no computador existem diferentes aplicativos baseados na Web. Destes, o que eu considero mais fácil, simples e completo é o [Dillinger](https://dillinger.io/). Podemos ver sua interface na [figura 1](https://www.inteligenciaurbana.org/2021/04/markdown-parte1.html#fig1).

![Dillinger-img-01](https://1.bp.blogspot.com/-CO6hE0uOp5g/YGkJX-JjHEI/AAAAAAAABEU/ggf9pLB4T2QmPEskAm_F1ZJXSQWP22c7ACLcBGAsYHQ/s0/markdown-dillinger-1-.jpg)

Interface do Dillinger - editor markdown online

O Dillinger possui uma interface dividida em duas partes, à esquerda escrevemos em Markdown e à direita temos um *preview* em tempo real do Resultado. O *preview* à direita pode ser alternado entre a visão de texto formatado, conforme [figura 1](https://www.inteligenciaurbana.org/2021/04/markdown-parte1.html#fig1) e a visão em HTML, que podemos ver na [figura 2](https://www.inteligenciaurbana.org/2021/04/markdown-parte1.html#fig2), clicando-se no botão na parte superior direita com o símbolo `</>`.

![Dillinger-img-02](https://1.bp.blogspot.com/-wCVx_kK1ZU4/YGkJYCfPFvI/AAAAAAAABEY/1JImj1JZSQg6h2IHkaTHh97p1NeUwMfzACLcBGAsYHQ/s0/markdown-dillinger-2-.jpg)

Interface do Dillinger - editor markdown online

Para retornar o `preview` à visão de texto formatado é só clicar no botão com desenho de olho no canto superior direito.

Com o Dillinger é possível exportar e salvar o documento em HTML, HTML estilizado, Markdown e PDF. Também é possível importar texto Markdown que tenha sido escrito em outro editor.

## Sintaxe básica

Praticamente todos os aplicativos Markdown suportam a sintaxe básica conforme descrita no documento original de [John Gruber](https://daringfireball.net/projects/markdown/). Na sequência apresentamos esta sintaxe.

Assim como no HTML, no Markdown os elementos são separados entre elementos bloco (*Block*) e elementos em linha (*inline* ou *span*).

**Elementos bloco** ocupam todo o espaço horizontal disponível e iniciam uma nova linha no documento. Novos elementos irão começar na próxima linha livre. Elementos bloco podem conter elementos em linha e, às vezes, outros elementos bloco.

**Elementos em linha** ocupam apenas o espaço necessário e não iniciam uma nova linha. São chamados elementos em linha justamente por aparecer na mesma linha que outros elementos, caso seja possível. Geralmente, elementos em linha podem conter apenas conteúdo e outros elementos em linha. Não é possível colocar elementos bloco dentro de elementos em linha.

### Elementos bloco

#### Títulos

O Markdown permite marcar títulos de nível 1 (o título principal) até títulos de nível 6 (o menor nível de subtítulo possível), assim como no HTML. Para marcar um título de nível 1 basta adicionar um `#` (*hash*, ou *sharp*, sustenido, jogo da velha, tralha, cerquilha, como preferir) seguido por um espaço antes texto do título. Para adicionar um título de nível 2 basta adicionar `##` (dois *hashes*) e assim por diante. Desta forma, o seguinte trecho em Markdown:

```
# Título 1: Cidade

## Título 2: Zona

### Título 3: Bairro

#### Título 4: Logradouro

##### Título 5: Edificação

###### Título 6: Unidade
```

Vai produzir o seguinte HTML:

```
<h1>Título 1: Cidade</h1>

<h2>Título 2: Zona</h2>

<h3>Título 3: Bairro</h3>

<h4>Título 4: Logradouro</h4>

<h5>Título 5: Edificação</h5>

<h6>Título 6: Unidade</h6>
```

E vai gerar um resultado semelhante a este:

Título 1: Cidade

Título 2: Zona

Título 3: Bairro

Título 4: Logradouro

Título 5: Edificação

Título 6: Unidade

Ainda existe uma sintaxe alternativa para os títulos de nível 1 e nível 2, com sinais de `=` (igual) e de `-` (subtração ou hífen) na linha de baixo do texto do título, da seguinte maneira:

```
Título 1: Cidade
================

Título 2: Zona
--------------
```

#### Parágrafos

A marcação de parágrafos em Markdown é extremamente sutil e consiste simplesmente em separar um parágrafo de outro ou de qualquer outro elemento bloco com uma linha vazia. Assim, o seguinte trecho em Markdown:

```
Este é um parágrafo.

Este é outro parágrafo.
Este ainda é o segundo parágrafo.
```

Se converte no seguinte HTML:

```
<p>Este é um parágrafo.</p>
<p>Este é o outro parágrafo. Este ainda é o segundo parágrafo.</p>
```

E gera um resultado semelhante a este:

Este é um parágrafo.

Este é o segundo parágrafo. Este ainda é o segundo parágrafo.

#### Quebras de linha

Para gerar uma quebra de linha dentro de um mesmo parágrafo é preciso deixar dois espaços em branco após o fim da primeira linha e nenhuma linha em branco entre elas. Conforme o seguinte trecho em Markdown (não será possível enxergar os espaços em branco após o fim da primeira linha, mas imaginem):

```
Este é um parágrafo.  
Esta é a segunda linha do mesmo parágrafo.
```

Isto será convertido no seguinte HTML:

```
<p>Este é um parágrafo.<br/>  
Esta é a segunda linha do mesmo parágrafo.</p>
```

E irá produzir algo semelhante a isto:

Este é um parágrafo.
Esta é a segunda linha do mesmo parágrafo.

#### Listas

##### Listas não ordenadas

A sintaxe para criar uma lista não ordenada em Markdown também é bastante simples e intuitiva, quase como se não estivéssemos fazendo uma “marcação” propriamente. Existem três opções, cada item da lista deve ser precedido por um sinal de `-` (subtração ou hífen) ou de `+` (adição) ou um `*` (asterisco) seguidos de um espaço e o texto do item da lista. Da seguinte forma:

```
- Primeiro item da lista  
- Segundo item da lista

+ Primeiro item da outra Lista
+ Segundo item da outra Lista

* Primeiro item da terceira Lista
* Segundo item da terceira lista
```

Este trecho irá produzir o seguinte HTML:

```
<ul>
  <li>Primeiro item da lista</li>  
  <li>Segundo item da lista</li>
</ul>

<ul>
  <li>Primeiro item da outra Lista</li>
  <li>Segundo item da outra Lista</li>
</ul>

<ul>
  <li>Primeiro item da terceira Lista</li>
  <li>Segundo item da terceira lista</li>
</ul>
```

- Primeiro item da lista
- Segundo item da lista

- Primeiro item da outra Lista
- Segundo item da outra Lista

- Primeiro item da terceira Lista
- Segundo item da terceira lista

##### Listas ordenadas

Para criar uma lista ordenada basta adicionar um número seguido de um ponto e de um espaço antes do texto de cada item da lista. Pode ser qualquer número, em qualquer ordem, ou pode mesmo ser sempre o mesmo número, que o resultado será uma lista ordenada, conforme o seguinte trecho de Markdown:

```
1. Primeiro item da lista  
1. Segundo item da lista
1. Terceiro item da Lista

3. Primeiro item da outra Lista
7. Segundo item da outra Lista
2. Terceiro item da outra lista
```

Que produz o HTML a seguir:

```
<ol>
  <li>Primeiro item da lista</li>
  <li>Segundo item da lista</li>
  <li>Terceiro item da Lista</li>
</ol>

<ol>
  <li>Primeiro item da outra Lista</li>
  <li>Segundo item da outra Lista</li>
  <li>Terceiro item da outra lista</li>
</ol>
```

1. Primeiro item da lista
2. Segundo item da lista
3. Terceiro item da Lista

1. Primeiro item da outra Lista
2. Segundo item da outra Lista
3. Terceiro item da outra lista

##### Aninhamento de Listas

Para aninhar listas dentro de itens de outra lista, ou seja, criar subitens, basta indentar a lista aninhada com um tab ou quatro espaços. Isto vale tanto para listas ordenadas quanto para listas não ordenadas e também é possível aninhar listas ordenadas em listas não ordenadas e vice versa. Conforme o seguinte trecho:

```
- Primeiro item da lista não ordenada
    - Subitem
- Segundo item da lista não ordenada

1. Primeiro item da lista ordenada
    1. Subitem
1. Segundo item da lista ordenada

- Primeiro item da lista não ordenada
    1. Subitem ordenado
    1. Outro subitem ordenado
- Segundo item da lista não ordenada
```

Que gera o seguinte HTML:

```
<ul>
  <li>Primeiro item da lista não ordenada
    <ul>
      <li>Subitem</li>
    </ul>
  </li>
  <li>Segundo item da lista não ordenada</li>
</ul>

<ol>
  <li>Primeiro item da lista ordenada
    <ol>
      <li>Subitem</li>
    </ol>
  </li>
  <li>Segundo item da lista ordenada</li>
</ol>

<ul>
  <li>Primeiro item da lista não ordenada
    <ol>
      <li>Subitem ordenado</li>
      <li>Outro subitem ordenado</li>
    </ol>
  </li>
  <li>Segundo item da lista não ordenada</li>
</ul>
```

E produz um resultado semelhante a este:

- Primeiro item da lista não ordenada
  - Subitem
- Segundo item da lista não ordenada

1. Primeiro item da lista ordenada
   1. Subitem
2. Segundo item da lista ordenada

- Primeiro item da lista não ordenada
  1. Subitem ordenado
  2. Outro subitem ordenado
- Segundo item da lista não ordenada

Também é possível aninhar outros elementos dentro de itens de lista com o mesmo método de indentação, da seguinte forma:

```
- Primeiro item da lista

  Parágrafo que faz parte do primeiro item da lista

- Segundo item da lista
- Terceiro item da lista
```

Este trecho produz o HTML a seguir:

```
<ul>
  <li>Primeiro item da lista
    <p>Parágrafo que faz parte do primeiro item da lista</p>
  </li>
  <li>Segundo item da lista</li>
  <li>Terceiro item da lista</li>
</ul>
```

E resulta no seguinte:

- Primeiro item da lista

  Parágrafo que faz parte do primeiro item da lista

- Segundo item da lista

- Terceiro item da lista

#### Blocos de citação

Outro elemento útil que pode ser marcado em Markdown são blocos de citação, derivados do elemento HTML `<blockquote>`, que tem a função original de incluir no texto uma citação longa, uma seção dentro de um documento que é citada de outra fonte. Um bloco de citação - ou *blockquote* - normalmente é visualmente representado por um recuo à esquerda e eventualmente uma formatação diferente do texto, isto pode ser estilizado via CSS no HTML ou através de alguma opção de configuração no aplicativo Markdown utilizado.

Para marcar um trecho como bloco de citação em Markdown basta inserir um sinal de `>` (“maior que”, ou chevron) antes de cada linha que faça parte do bloco e também na linha em branco caso o bloco de citação possua mais de um parágrafo. Conforme o seguinte trecho em Markdown:

```
Este é um parágrafo antes da citação:

> Este é um bloco de citação com dois parágrafos. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing.

Este é um parágrafo depois da citação.
```

Este trecho converte-se no seguinte HTML:

```
<p>Este é um parágrafo antes da citação:</p>

<blockquote>
  <p>Este é um bloco de citação com dois parágrafos. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.</p>
  <p>Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing.</p>
<blockquote>

<p>Este é um parágrafo depois da citação.</p>
```

E gera um resultado parecido com este, a depender da configuração visual utilizada:

Este é um parágrafo antes da citação:

> Este é um bloco de citação com dois parágrafos. Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse id sem consectetuer libero luctus adipiscing.

Este é um parágrafo depois da citação.

#### Blocos de código (literal)

Outro elemento que pode ser marcado em Markdown são blocos de código pré-formatados.

Os blocos de código pré-formatados são usados para escrever sobre programação ou código-fonte, que foi uma das principais funções para as quais o Markdown foi criado originalmente e para a qual é utilizado até hoje.

Neste próprio guia passo a passo estou utilizando a marcação de blocos de código para mostrar cada trecho em Markdown “cru” e em HTML “cru” de cada elemento sintático apresentado.

Em vez de formar parágrafos e outros elementos normais da linguagem de marcação ou programação utilizada, o texto de um bloco de código é interpretado literalmente (como faz a *tag* HTML `<pre>`), e formatado como código (como faz a *tag* HTML `<code>`), o que geralmente significa utilizar fonte monoespaçada e, eventualmente, realce de sintaxe através de cores, o que dependerá de configurações específicas do documento ou página da Web.

Para inserir um bloco de código em Markdown basta indentar cada linha do bloco com pelo menos quatro espaços ou um tab. Assim, o seguinte trecho em Markdown:

```
Este é um parágrafo antes do bloco de código:

    <h1>Título em HTML</h1>
    <p>Parágrafo em HTML</p>

Este é um parágrafo depois do bloco de código.
```

Produz um HTML assim:

```
<p>Este é um parágrafo antes do bloco de código:</p>

<pre>
  <code>
    &lt;h1&gt;Título em HTML&lt;/h1&gt;
    &lt;p&gt;Parágrafo em HTML&lt;/p&gt;
  </code>
</pre>

<p>Este é um parágrafo depois do bloco de código.</p>
```

E gera um resultado semelhante a este:

Este é um parágrafo antes do bloco de código:

```
<h1>Título em HTML</h1>
<p>Parágrafo em HTML</p>
```

Este é um parágrafo depois do bloco de código.

#### Linhas Horizontais

Para criar uma linha horizontal, o equivalente ao elemento HTML `<hr/>`, são três opções: basta colocar três ou mais sinais de `***` (asteriscos), ou `---` (subtração ou hífen), ou `___` (*underline*/sublinhado) em uma linha isolada. Assim:

```
Parágrafo antes das linhas.

***

---

___

Parágrafo após as linhas.
```

Este é o HTML convertido:

```
<p>Parágrafo antes das linhas.</p>
<hr/>
<hr/>
<hr/>
<p>Parágrafo após as linhas.</p>
```

E o resultado é semelhante a este:

Parágrafo antes das linhas.

------

------

------

Parágrafo após as linhas.

### Elementos em Linha

#### Ênfase

##### Itálico

Para marcar um texto como em itálico, o equivalente à *tag* HTML de ênfase semântica `<em>`, basta envolver o texto com `*` (asteriscos) ou com `_` (*underline*/sublinhado). Da seguinte maneira:

```
*Inteligência* _Urbana_
```

O que produz o seguinte HTML:

```
<p><em>Inteligência</em> <em>Urbana</em></p>
```

E gera um resultado semelhante a este:

*Inteligência* *Urbana*

##### Negrito

Para marcar um texto como negrito, o equivalente à *tag* HTML de “forte ênfase” semântica `<strong>`, basta envolver o texto com dois `**` (asteriscos) ou com dois `__` (*underline*/sublinhado). Da seguinte maneira:

```
**Inteligência** __Urbana__
```

O que produz o seguinte HTML:

```
<p><strong>Inteligência</strong> <strong>Urbana</strong></p>
```

E gera um resultado semelhante a este:

**Inteligência** **Urbana**

##### Itálico e negrito

Para marcar um texto como negrito e itálico simultaneamente basta envolver o texto com três `***` (asteriscos) ou com três `___` (*underline*/sublinhado). Da seguinte maneira:

```
***Inteligência***  ___Urbana___
```

O que produz o seguinte HTML:

```
<p><strong><em>Inteligência</em></strong> <strong><em>Urbana</em></strong></p>
```

E gera um resultado semelhante a este:

***Inteligência\*** ***Urbana\***

#### Código em linha (literal)

Para indicar um trecho de código em linha é só envolver o código com sinais ```` (crases), e é o equivalente à *tag* HTML `<code>`.

Ao contrário de um bloco de código pré-formatado, um código em linha indica um trecho de código dentro de um parágrafo normal. Por exemplo:

```
Itálico em HTML é feito `<em>assim</em>`.
```

Este trecho será convertido neste HTML:

```
<p>Itálico em HTML é feito <code>&lt;em&gt;assim&lt;/em&gt;</code>.</p>
```

E produzirá um resultado parecido com este:

Itálico em HTML é feito `<em>assim</em>`.

#### Links

Para criar um *link* diretamente basta colocar o texto âncora do *link* entre colchetes `[]` e, na sequência, colocar o URL do link entre parêntesis `()`. Opcionalmente, se quiser colocar o atributo HTML `title` (título) ao *link* (um texto que aparece quanto se passa o mouse sobre o texto âncora do *link* em uma página da Web), basta colocar o texto do `title` entre aspas `""`, após o URL, ainda dentro dos parêntesis. Conforme o seguinte trecho de exemplo em Markdown:

```
Visite o site [Inteligência Urbana](https://www.inteligenciaurbana.org/ "conteúdo, dados e informações sobre cidades")
```

Que será convertido no HTML a seguir:

```
<p>Visite o site <a href="https://www.inteligenciaurbana.org/" title="conteúdo, dados e informações sobre cidades">Inteligência Urbana</a></p>
```

E produzirá um resultado semelhante a este:

Visite o site [Inteligência Urbana](https://www.inteligenciaurbana.org/)

Também é possível inserir *links* com identificadores de referência, uma funcionalidade bastante útil quando se precisa inserir um mesmo *link* diversas vezes na mesma página ou documento.

A referência do *link* pode ser inserida em qualquer parte do documento. Basta definir um identificador único qualquer, que deve ser colocado entre colchetes `[]` , seguidos do sinal de `:` (dois pontos), um espaço e o URL do *link*. Opcionalmente o atributo `title` pode ser adicionado, entre aspas `""`, após o URL, separado deste por um espaço. Da seguinte maneira:

```
[linkid]: https://www.inteligenciaurbana.org/ "conteúdo, dados e informações sobre cidades"
```

E então, no corpo do texto, o texto âncora do *link* deve ser colocado entre colchetes `[]` seguido pelo identificador único de referência do link, também entre colchetes `[]`, da seguinte forma:

```
Visite o site [Inteligência Urbana][linkid]
```

E isto irá produzir os mesmos resultados do primeiro exemplo de *link*.

Uma terceira forma de inserir *links*, quando o texto âncora puder ser a própria URL do *link* é simplesmente colocar a URL entre `<>` (chevrons, ou sinais de “menor que” e “maior que”). Da seguinte maneira:

```
Visite <https://www.inteligenciaurbana.org/>
```

Que produzirá o seguinte HTML:

```
<p>Visite <a href="https://www.inteligenciaurbana.org/">https://www.inteligenciaurbana.org/</a></p>
```

E gera um resultado semelhante a este:

Visite https://www.inteligenciaurbana.org/

#### Imagens

Para inserir imagens basta utilizar a mesma sintaxe dos *links* precedida por um sinal `!` (exclamação). No lugar do texto âncora do link vai o atributo `alt` (texto alternativo) da imagem, e a URL pode ser simplesmente o caminho para o arquivo da imagem (no caso de um documento impresso, por exemplo). Assim como com os links, as imagens também podem, opcionalmente, receber o atributo `title` e também podem ser inseridas diretamente ou via identificador de referência. Tudo conforme o trecho a seguir:

```
Imagem 01 inserida diretamente:

![imagem 01](https://1.bp.blogspot.com/-_Pt10SpvllA/YAiDIo7cF5I/AAAAAAAAAyI/NUo0OsunsPIK-CaIUhBIUfP0zylr05MmgCLcBGAsYHQ/s0/Inteligencia-urbana-imagem-1.jpg "logotipo branco")

Imagem 02 inserida via identificador de referência:

![imagem 02][idimg2]

[idimg2]: https://1.bp.blogspot.com/-DR0mDeycVoE/YAiDIl_NBZI/AAAAAAAAAyE/KL05izDqTKkaWPRUN1grl7GQXI3zRGqlACLcBGAsYHQ/s0/Inteligencia-urbana-imagem-2.jpg "logotipo branco"
```

Que irá produzir o seguinte HTML:

```
<p>Imagem 01 inserida diretamente:</p>
<p><img src="https://1.bp.blogspot.com/-_Pt10SpvllA/YAiDIo7cF5I/AAAAAAAAAyI/NUo0OsunsPIK-CaIUhBIUfP0zylr05MmgCLcBGAsYHQ/s0/Inteligencia-urbana-imagem-1.jpg" alt="imagem 01" title="logotipo branco"/></p>

<p>Imagem 02 inserida via identificador de referência:</p>

<p><img src="https://1.bp.blogspot.com/-DR0mDeycVoE/YAiDIl_NBZI/AAAAAAAAAyE/KL05izDqTKkaWPRUN1grl7GQXI3zRGqlACLcBGAsYHQ/s0/Inteligencia-urbana-imagem-2.jpg" alt="imagem 02" title="logotipo preto"/></p>
```

E gerará um resultado semelhante a este:

Imagem 01 inserida diretamente:

![imagem 01](https://1.bp.blogspot.com/-_Pt10SpvllA/YAiDIo7cF5I/AAAAAAAAAyI/NUo0OsunsPIK-CaIUhBIUfP0zylr05MmgCLcBGAsYHQ/s0/Inteligencia-urbana-imagem-1.jpg)

Imagem 02 inserida via identificador de referência:

![imagem 02](https://1.bp.blogspot.com/-DR0mDeycVoE/YAiDIl_NBZI/AAAAAAAAAyE/KL05izDqTKkaWPRUN1grl7GQXI3zRGqlACLcBGAsYHQ/s0/Inteligencia-urbana-imagem-2.jpg)

### Escape de símbolos

O Markdown permite que você use “escapes” com o sinal de `\` (barra invertida) para gerar caracteres literais que, de outra forma, teriam algum significado especial na sintaxe de formatação do Markdown. Por exemplo:

```
Este é um termo *em itálico* e este é um termo \*entre asteriscos\*.
```

Este trecho será convertido neste HTML:

```
<p>Este é um termo <em>em itálico</em> e este é um termo *entre asteriscos*.</p>
```

E produzirá um resultado parecido com este:

Este é um termo *em itálico* e este é um termo *entre asteriscos*.

Os seguintes símbolos podem ser “escapados” com o uso da `\` barra invertida:

- **\**  barra invertida
- **`**  aspas
- *****  asterisco
- **_**  underline / sublinhado
- **{}**  chaves
- **[]**  colchetes
- **<>**  chevron / menor que e maior que
- **()**  parêntesis
- **#**  hash / sustenido
- **+**  sinal de adição
- **-**  sinal de subtração / hífen
- **.**  ponto
- **!**  sinal de exclamação
- **|**  pipe / barra vertical

### HTML

Para qualquer marcação que não seja coberta - ou mesmo que seja - pela sintaxe do Markdown, pode-se simplesmente utilizar o próprio HTML. Não é necessário precedê-lo por nada ou delimitá-lo com nada para indicar que se está mudando de Markdown para HTML, basta utilizar as tags HTML normalmente. Conforme o seguinte exemplo:

```
Este é um termo **em negrito** e este é um termo <strong>em negrito também</strong>.
```

Que se converterá no seguinte HTML:

```
<p>Este é um termo <strong>em negrito</strong> e este é um termo <strong>em negrito também</strong>.</p>
```

E produzirá um resultado semelhante a este:

Este é um termo **em negrito** e este é um termo **em negrito também**.

## Dialetos (ou sabores) de Markdown

Um aspecto relativamente confuso do Markdown é que praticamente todos os aplicativos Markdown implementam uma versão ligeiramente diferente da linguagem. Essas variantes do Markdown são normalmente chamadas de “sabores”.

Para entender o conceito de *sabores* de Markdown, pode ser útil pensar neles como “dialetos” de linguagem.

Cada dialeto - ou sabor - de Markdown, além de umas pequenas diferenças de sintaxe em relação a esta sintaxe básica, às vezes um pouco arbitrárias e aleatórias (é mais comum que sejam um pouco mais permissivas, então se seguir o apresentado neste guia tudo dará certo), também apresentam funcionalidades adicionais, também sob a forma de marcação, com uma sintaxe própria para estas “extensões”, mas em geral seguindo a mesma filosofia.

Alguns dialetos diferentes tem foco em propósitos diferentes, e portanto apresentam funcionalidades estendidas um pouco diferentes.

Alguns exemplos de dialetos Markdown com sintaxe estendida são:

- CommonMark Markdown;
- Github-Flavored Markdown;
- MultiMarkdown;
- Markdown PHP Extra;
- Pandoc’s Markdown.

Estes *sabores* listados acima são os suportados pelo [Pandoc](https://www.inteligenciaurbana.org/2021/04/markdown-parte2-pandoc.html), que é um software gratuito e open-source conversor entre diversos tipos de linguagens de marcação e arquivos de texto, a respeito do qual tratamos no [próximo artigo](https://www.inteligenciaurbana.org/2021/04/markdown-parte2-pandoc.html) desta série.

## Conclusão

Neste artigo trouxemos uma introdução conceitual rápida sobre **Markdown** e linguagens de marcação e apresentamos a lógica de seu funcionamento e sua sintaxe básica.

Em artigos subsequentes apresentaremos o que consideramos ser as melhores ferramentas e *dialetos* - ou *sabores* - de Markdown conforme diferentes propósitos, principalmente para produção de documentos técnicos, produção de documentos acadêmicos e produção de textos para Web.

Além do blog, a plataforma [Inteligência Urbana](https://www.inteligenciaurbana.org/) disponibiliza páginas com referências para [livros](https://www.inteligenciaurbana.org/p/livros.html), [cursos](https://www.inteligenciaurbana.org/p/cursos.html) e [leis e normas](https://www.inteligenciaurbana.org/p/leis-e-normas.html) relacionadas aos temas que tratamos aqui. Caso você tenha interesse pode conferir nossos [serviços](https://www.inteligenciaurbana.org/p/servicos.html) oferecidos e entrar em contato quando quiser. Se quiser ser alertado da publicação de material novo pode assinar a nossa [newsletter](https://www.inteligenciaurbana.org/2021/04/markdown-parte1.html#feed), e muito obrigado pela atenção até aqui!