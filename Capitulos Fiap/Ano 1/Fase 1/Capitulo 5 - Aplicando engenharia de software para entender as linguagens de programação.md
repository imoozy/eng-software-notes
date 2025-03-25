
# Estilo é necessário

O HTML, Hypertext Markup Language, funciona muito bem na finalidade para a qual ele foi criado: Estruturar a página com o uso de suas tags, permitindo a inserção de todo e qualquer tipo de conteúdo. Por ser uma linguagem de marcação, ele não consegue fazer mais nada além disso. Então é necessário outras linguagens para ajudar nessa tarefa.

Uma dessas linguagens é a CSS, Cascading Style Sheets.

Os estilos criados são aplicados a um elemento ou grupo de elementos existentes na página. Devemos indicar qual elemento será formatado, o que queremos estilizar e como ele deverá ficar, isso é chamado de regra CSS. Podemos ter regras para todos os elementos. Elas devem ficar em um arquivo com a extensão .css.

Antes do lançamento das primeiras versões do CSS que foi em 96, as formatações eram feitas dentro das tags HTML, através de atributos. Misturavam-se conteúdo e formatação, as linhas de código.


# Tipos de CSS

A estilização de nossas páginas web com CSS poderá ser feita de três formas diferentes: Através de CSS inline, CSS interno, CSS externo. Em qualquer uma delas, teremos de identificar qual elemento queremos formatar, o que desejamos formatar e como ele deve ficar.

## CSS inline

A CSS Inline consiste na inserção de código CSS dentro da tag do elemento HTML que desejamos formatar. O que é possível com o uso do atributo style.

```HTML
<h2 style=”color: red;”>Conheça São Paulo</h2>
<h3 style=”color: red;”>Parques</h3>
<h3 style=”color: red;”>Cinemas</h3>
<h3 style=”color: red;”>Restaurantes</h3>
```

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20241031215903685.webp]]

No código-fonte "Estilização CSS Inline", as tags h2 e h3 receberam o atributo ***Style***, contendo a regra que define a cor do texto color. Essa parte da regra é chamada de propriedade. Foi atribuída a palavra red, que indica a cor em que o texto ficará. Essa parte da regra é chamada de valor. Como todo têm a mesma regra, os quatro elementos terão seus textos exibidos na cor vermelha.

Devemos sempre usar o sinal de dois pontos (**:**) para separar a propriedade e o valor. Após o valor, existe o sinal de ponto e vírgula (***;***), representando que aquela formatação foi finalizada. Esses dois sinais são obrigatórios para que a formatação seja aplicada.

A utilização do CSS Inline ***não é uma boa prática***.

## CSS Interno

O uso de CSS interno é caracterizado pela criação das regras dentro da seção ***HEAD*** da página. A regra CSS interna melhor que a Inline, mas também possui algumas restrições que podem indisponibilizar seu uso:

- As regras ali criadas afetarão apenas a página em que ela estiver inserida.
- Continuamos a ter o conteúdo da página misturado com formatação, embora em seções diferentes, estarão no mesmo arquivo.
- Temos aumento no tempo de carregamento da página
- Quando necessitarmos dar manutenção em um site que foi montado dessa forma, teremos de fazer as mesma alterações em várias páginas. 

Uma declaração de regra CSS interna deve possuir: um seletor, uma propriedade e um valor.


Vídeo fiap sobre CSS
```CSS
body{
	margin: 0;
	padding: 0;
	background-color: black;
	background-image: url(../img/teste.jpg);
	background-attachment: fixed;
	background-size: cover;
	font-family: arial, verdana, tahoma;
	font-size: 14px;
}
```

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20241031222049840.webp]]

Para que o navegador entenda que ali teremos a formatação da página, é preciso colocar as regras CSS dentro da tag ***Style***. Como boa prática, devemos também usar o atributo type, que indicara o tipo de mídia de internet que será usado. O valor padrão é ***text/css***.


## Container

```HTMl
	<div id="container">
		conteúdo aqui dentro
	</div>
```

```CSS
#container{
	width: 900px;
	border: 1px solid black;
	margin: auto;
	padding: 20px;
	background-color: rgb(235, 173, 59 / 80%);
	color: #d76868;
}
```

## BANNER

```HTML
<body>
	<div class="banner"></div>
</body>

```

```CSS
.banner{
	background-image: url(../img/nomebaner.jpg);
	width: 100%;
	height: 260px;
	border: 1px solid #000;
	border-radius: 20px 0px 20px 0px;
	background-size: cover; /*deixa a imagem ajustado com o fundo de tela */
	background-position: 0px -190px; /*Deixa ajustado a posição X e Y */
}
```

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20241217205607502.webp]]

## Seletor de classe e ID

```HTML
	<h1 id="titulo">titulo</h1>
	<p class="ajusteA">pipipipopopo</p>
	<p class="ajusteB">pipipipopopo</p>

```

```CSS
p{
	color: green;
}

.ajusteA{
	color: red;
}

.ajusteB{
	color: blue;
}

#titulo{
	color: orange;
}
```

![[Capitulo 5 - Representação do código.webp]]
![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20241217210229886.webp]]

## Ajustando parágrafo

```HTML
<body>
	<p>Olá estou <u>Testando</u> para saber se está certo nesse codigo <span>The walking dead</span></p>
</body>
```

```css
p{
	margin: 10px 10px 30px 10px;
	text-indent: 20px; /* Cria uma margem de identação */
}

p span{
	background-color: rgb(255 255 0 / 51%);
	color: black;
	padding: 0px 10px 3px 10px;
	border-radius: 10px;
	border-bottom: 1px solid orange;
}
```

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20241217211554657.webp]]

## Ajustando o cabeçalho

```CSS
h1, h2, h3, h4, h5, h6{
	font-family: tahoma, verdana, arial;
	color: tomato;
}
```

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20241217212447130.webp]]
```CSS
h1{
	text-align: center;
	text-transform: uppercase;
	font-size: 35px;
}

h2{
	background-color: rgb(255 0 0 / 21%);
	font-style: italic;
	border-radius: 0px 30px 30px 0px;
	border-bottom: 3px solid red;
}

h3, h4{
	color: #994be4;
}

h3{
	border-bottom: 1px solid pink;
	display: inline-block;
	margin-top: 33px;
	margin-bottom: 20px;
}

h4{
	font-size: 13px;
	margin: 70px 0px 9px 10px;
}
```

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20241217212631735.webp]]
![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20241217212908967.webp]]

# CSS EXTERNO

O uso do CSS externo é caracterizado pela criação das regras dentro de um novo arquivo que será a folha de estilo (CSS). é muito comum encontrar o nome do arquivo CSS como style.css. 

Para que a página seja desenvolvida, deve-se fazer o uso de um link do HTML com o CSS, na seção ***HEAD*** com o uso da tag ***LINK***. Esta tag deverá possuir o atributo ***REL***, que define que o link é relativo a uma folha de estilos. outro atributo obrigatório é o ***HREF***, que deve conter o endereço e o nome do arquivo CSS

# Especificidade

Especificidade define qual seletor é mais especifico que outro, ou seja, determina qual regra deve ser aplicada. Esta condição existe entre tags, seletores e modos de inserção de CSS.

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20241217215732733.webp]]

# LINKS PARA PÁGINAS DO MESMO SITE: LINKS INTERNOS

Para criarmos os links entre as páginas, utilizamos a tag ***a***, que deve ser seguida do atributo HREF.

Podemos fazer o link entre páginas do mesmo site, basta referenciar o arquivo HTML desejado dentro do atributo href, contido na tag ***a***.

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20250106215938007.webp]]

## Listas ordenadas

Devem ser criadas com o uso da tag ***ol***. cada item da lista deverá estar dentro da tag **li**.

```HTML
<body>   
<h2>As melhores pizzarias de São Paulo</h2>
        <ol>
            <li>Pizzaria do Angelo</li>
            <li>1900 Pizzaria</li>
            <li>Famiglia Mancini</li>
            <li>Veridiana</li>
            <li>Braz Pizzaria</li>
        </ol>
</body>
```

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20250106220834876.webp]]

## Lista não ordenadas

Devem ser criadas com o uso da tag ***ul***, cada item da lista deverá estar dentro da tag li.
Listas não ordenadas serão de grande uso na criação dos menus de navegação em nossas páginas.

```HTML
<body>   
<h2>O que fazer em São Paulo?</h2>
        <ul>
            <li>Passear no Ibirapuera</li>
            <li>Conhecer o Beco do Batman</li>
            <li>Vila Madalena e sua boêmia</li>
            <li>Se encantar com o MASP</li>
            <li>Visitar Theatro Municipal</li>
        </ul>
</body>
```

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20250106221404537.webp]]

## Listas de definição

Permitem a criação de um conjunto de termos e as suas respectivas definições. Devem ser criadas com o uso da tag ***dl***. Cada termo da lista a ser definido deverá estar dentro da tag ***DT***. A definição do termo precisa estar  dentro da tag ***DD***.

```HTML
<body>   
<h2>Entenda as gírias paulistanas</h2>
        <dl>
            <dt>Ibira</dt>
            <dd>O Parque do Ibirapuera</dd>
            <dt>Daora</dt>
            <dd>Bom, bacana, muito legal</dd>
            <dt>Na faixa</dt>
            <dd>Grátis</dd>
            <dt>Osso</dt>
            <dd>Difícil, complicado, complexo</dd>
        </dl>
</body>
```

![[Capitulo 5 - Aplicando engenharia de software para entender as linguagens de programação-20250106221602058.webp]]

## Tabelas internas com hover

```CSS
table{
	margin: auto;
}

table img{
	border: 5px solid tomato;
	border-radius: 20px;
}

table img:hover{
	border: 5px solid #e800ff;
}
```

# Font-family

text-aling: Define o alinhamento do texto

```CSS
p{
    text-align: center;
}
```

text-decoration: A decoração do texto consiste em uma linha poderá ficar acima (overline), abaixo(underline) ou no meio(line-through) do conteúdo. é comum nos links tag ***a*** por padrão eles ficam sublinhados. Usando o valor none, podemos retirar a decoração dele.

```CSS
a{
    text-decoration: none;
}
h2{
    text-decoration: underline;
}
```


text-transform: Define que os textos ficarão em letras maiúsculas (uppercase) ou minusculas (lowercase). Podemos, ainda, definir se apenas a primeira letra de cada palavra fica maiúscula (capitalize).

```CSS
h1{
    text-transform: uppercase;
}
p{
    text-transform: lowercase;
}
```

text-indent: Define a indentação de um parágrafo:

```CSS
p{
    text-indent: 25px;
}
```

***Voltar no criando o menu.***