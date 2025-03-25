
# Tags são caixas

Conceito de caixas

```html
<body>
	<h1>Toca</h1>
	<p>xano</p>
	<h2>posicionamento de caixas</h2>
	<p>lorem15</p>
	<!-- TESTE DE COMENTÁRIO -->
	<img src="endereco.jpg" alt="seh loco cachorrão">
	<img src="endereco.jpg" alt="seh loco cachorrão">
	<img src="endereco.jpg" alt="seh loco cachorrão">
	<img src="endereco.jpg" alt="seh loco cachorrão">
	
</body>
```

por padrão, as tags se comportam de duas formas

## Tags de bloco (BLOCK):

Ocupam todo o espaço da linha em que estão posicionadas, e dessa forma, não permitem que outras caixas (tags) sejam exibidas ao seu lado. São exemplos de tags que possuem esse comportamento: P, H1, LI, entre outras.

## Tags de linha (IN-LINE):

Ocupam apenas o tamanho do seu conteúdo, permitindo que outras caixas seja exibidas ao seu lado, caso exista espaço suficiente para isso. São exemplos que possuem esse comportamento: A, IMG, e mais algumas outras.

```css
img {
    display: block;
}
```

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250130214758527.webp]]

# DIV

```html
<body>
	<!-- Conteúdo inicial -->
	<div>
		<h2> Ta foda </h2>
		<p> mais um teste disso </p>
	</div>
	
	<!-- Conteúdo Secundário -->
	<div>
		<h2> Ta foda 2 </h2>
		<p> mais um teste disso </p>
	</div>
</body>

```
```css
div {
	width: 250px;
	height: 200px;
	background-color: #CCC;
	overflow: hidden;
}
```


## Introdução ao CSS

Só é css inline, externo e interno

```html

<!-- Conteúdo HTML -->
<body>
	<h1> Tá foda </h1>
	<h2> daora </h2>
	<p> mim de papai </p>
</body>
```

```css
h1 {
	color: #225599
	font-family: Calibri, Verdana, Tahoma;
	font-size: 40px;
	text-transform: capitalize;
	letter-spacing: 1px;
	word-spacing: 50px;
}

h2 {
	font-size: 25px;
}

p {
	font-family: Verdana;
	font-size: 18px;
	color: #666666;
}
```

Quando são criadas, as divs e as tags tem o tamanho exato do conteúdo, com a CSS podemos definir um novo tamanho para elas, basta usar as propriedades width e height. Elas devem receber um valor válido de uma medida CSS; os valores mais comuns são: %, em, rem e pixel.

# Box model


```html
<body>
	<h1>Box model</h1>
	<div>Div 1</div>
	<div>Div 2</div>
</body>
```


```css
div {
	width: 200px;
	height: 250px;
	background-color: gray;
	margin: 100px;
	/*border-width: 10px;
	border-style: solid;
	border-color: #369;*/
	border: 1px solid #999;
	border: 1px dashed #999; /* riscadinha pontilhada */
	border: 1px dotted #999; /* pontilhada */
	border: 1px double #999; /* dupla */
	border-radius: 10px;
	
}
```

para mais tipos de bordas:

https://www.w3schools.com/cssref/playdemo.php?filename=playcss_border-style&preval=dashed

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250202132605154.webp]]

Não esquecer esse layout para margin, border e padding sendo padding espaçamento interior, border borda e margin exterior.

Exemplificação do que está a cima.
![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250202132821123.webp]]

O Box model descreve como as divs devem ser montadas em nossa página, ele é composto por quatro elementos: margin, border, padding e content. Essas quatro propriedades, em conjunto com a largura e altura definirão como ficará o seu container

## Margin

Define a margem externa da div. Entenda como o distanciamento que a div terá dos demais elementos que formam a página.

## Border

Define a borda (contorno) da div ou de qualquer outro elemento. As bordas são opcionais e é muito comum entrarmos elementos sem elas, inclusive as divs.

## Padding

Define a margem interna (preenchimento) da div. Entenda essa margem como o distanciamento que o conteúdo terá das bordas ou das extremidades da div.

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203202814078.webp]]

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203202823436.webp]]

Usar padding dava um trabalhão, então foi criado a propriedade box-sizing, que em conjunto com o valor border-box, altera o comportamento dos elementos com padding, permitindo o espaçamento interno seja aplicado, sem alterar a altura e a largura do container.

```CSS
div {
    width: 300px;
    height: 100px;
    margin: 20px;
    border: 5px solid #dc143c;
    padding: 20px;
    box-sizing: border-box;
}
```

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203203058987.webp]]

# O conteúdo da DIV

O content é o seu conteúdo dentro da div (caixa) e, como veremos, poderá ser controlado de diversas formas pela CSS

# Mais propriedades para DIVS

Podemos criar as divs usando: largura, altura, margin, border e padding. Mas existem mais propriedades que podem nos ajudar, e muito nessa tarefa.

## Limitando altura e largura

Podemos definir altura e a largura, máxima e mínima, que um elemento pode ter quando exibido na janela do navegador. Essas propriedades podem ser bem úteis quando utilizadas em dispositivos móveis, pois podem ajudar na exibição do conteúdo.

Temos as seguintes propriedades:

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203203535651.webp]]

```css
div {
    max-width: 300px;
    min-width: 100px;
    max-height: 300px;
    min-height: 200px; 
    border: 5px solid #dc143c;
    padding: 10px;
    box-sizing: border-box;
}
```

## Overflow

Define o que acontecerá quando o conteúdo inserido em uma div for maior que ela. E possui as seguintes propriedades:

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203203635501.webp]]
![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203203648403.webp]]

## Box-shadow

Insere uma sombra em volta de uma caixa. Podemos definir várias características para elas, sendo que os valores devem ser declarados na seguinte ordem:

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203203736075.webp]]
```css
div{
	box-shadow: 10px 10px 10px 10px #000; 
}
```

Imagine que temos uma div com 300px de largura, 250px de altura, 10 de padding e borda e 5px, sólida na cor vermelha, veja como essa div ficará aplicando padrões de sombra diferentes:

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203203956994.webp]]

## Border-radius

quando inserimos uma borda em uma caixa, os cantos sempre terão ângulos retos, e podemos arredonda-los utilizando a propriedade border-radius um valor e alguma unidade de medida valida, sendo mais comum o pixel.

```css
div {
    border-radius: 10px;
}
```

## Cor de fundo

Podemos aplicar uma cor de fundo para cada elemento HTML, para isso, basta usar a propriedade background-color tendo como valor a cor desejada. A cor pode ser declarada usando código hexadecimais, código RGB ou até mesmo o nome da cor em inglês.

```css
body {
    background-color: rgb(200, 200, 200);
}

div {
    background-color: #DC143C;
    color: #FFFFFF;
}
```

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203204354644.webp]]

site para mais cores:
https://color.adobe.com/pt/create/color-wheel

## Imagem de fundo

```html
<body>
	<h1>imagem de fundo</h1>
	<div>
		<h2>Fundo</h2>
		<p>Lorem50</p>
	</div>

</body>
```

```css
div{
	w: 400px;
	h: 400px;
	margin: 10px auto;
	background-color: black; /*usa rbga para ter transparencia do elemento*/
	padding: 10px;
	box-sizing: border-box;
	color: #ffffff
}

body{
	background-image: url(../image/teste.jpg);
	background-repeat: no-repeat;
	background-size: cover;	
}
```

Da mesma forma que inserimos cores, podemos colocar imagens de fundo tanto no body da página, quanto em qualquer outro HTML.

Por padrão, quando inserimos imagens de fundo, elas serão repetidas para ocupar todo o espaço do elemento. Podemos usar a propriedade. background-repeat, como o valor no-repeat, para mudar esse padrão. Assim que ela for alterada, a imagem ficará posicionada na parte superior esquerda do elemento e não repetirá.

```css
div {
    width: 400px;
    height: 300px;    
    border: 1px solid #000;
    background-image: url(../images/icone.png);
    background-repeat: no-repeat;
}
```

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203210058114.webp]]

Caso você necessite, podemos fazer com que as imagens repitam apenas em um determinado eixo da caixa, eixo x, para a largura, ou eixo y para a altura. Para isso usamos a propriedade background-repeat com os valores repeat-x ou repeat-y.

```css
div {
    background-repeat: repeat-x;
}

div {
    background-repeat: repeat-y;
}
```

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203211450903.webp]]

As imagens de fundo, quando não repetidas, poderão ter um posicionamento específico dentro da caixa. Para isso, basta usar a propriedade background-position, seguida de algum valor válido:

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203211619618.webp]]
![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203211628255.webp]]
![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203211636298.webp]]

```CSS
div {
    background-repeat: no-repeat;
    background-position: 50px 30px;
}
   
div {
    background-repeat: no-repeat;
    background-position: 70% 80%;
}

div {
    background-repeat: no-repeat;
    background-position: top center;
}
```

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203211726869.webp]]

As imagens de fundo podem ser configuradas para que fiquem fixas na tela ou acompanhem o seu scroll, para isso usaremos a propriedade background-attachment, com os seguintes valores:

* Fixed: a imagem ficará sempre fixa na tela, independente do scroll que for realizado.
* Scroll: a imagem acompanhará o scroll da tela e só ficará visível na área em que foi posicionada.

```css
div {
    background-repeat: no-repeat;
    background-position: center 50px;
    background-attachment: fixed;
}

div {
    background-repeat: no-repeat;
    background-position: center 50px;
    background-attachment: scroll;
}
```

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203211933732.webp]]

As imagens de fundo também poderão ter seu tamanho redimensionado, para isso, usamos a propriedade background-size, que pode receber os seguintes valores: 

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203212041510.webp]]
![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203212049179.webp]]
![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203212057174.webp]]

```css
div {
    background-repeat: no-repeat;
    background-position: center center;
    background-size: 100px 100px;
}

div {
    background-repeat: no-repeat;
    background-position: center 50px;
    background-size: contain;
}

div {
    background-repeat: no-repeat;
    background-position: center 50px;
    background-size: cover;
}
```

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203212119090.webp]]

# Pedidos do cliente

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./css/style.css">
    <title>Conheça o novo Drone da DJI</title>
</head>
<body>
    <div>
        <h1>DJI MAVIC 3</h1>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quasi ducimus natus quae sapiente temporibus, quam
            ea consequatur unde cum nulla, modi culpa accusantium, qui doloribus reprehenderit minima.
        </p>
        <p>
            <a href="droneDJI3.html">Veja Mais</a>
        </p>
    </div>
</body>
</html>
```

## Criando links

```html
<!-- Criando links -->
<p id="titulo">
	<a href="link aqui" target= "_blank">Veja onde se hospedar</a> <!--A de ancora-->
	<a href="link da img"><img src="imagem" alt="descriçao"></a>
	<p><a href="#titulo">Ancora</a></p>
</p>
```

```css
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@300&family=Open+Sans+Condensed:wght@300&display=swap');

html {
    font-family: 'Lato', sans-serif;
}

body {
    background-image: url(../images/ibirapueraimg/baixados.jpg);
    background-repeat: no-repeat;
    background-size: cover; 
    font   
}

div {
    width: 400px;
    height: 300px;
    margin: 175px 150px105px 60px;
    padding: 20px;
    box-sizing: border-box;
    background-color: rgba(28, 58, 149, 0.9);rgb(1 1 1 / 55%);
    border-radius: 20px;
    border: 4px solid #ad9898;
}

h1 {
    color: #fff;
    font-size: 30px;
    text-transform: uppercase;
    font-weight: 200;
    font-weight: bolder;
}

p {
    color: #fff;
    font-size: 16px;
    text-align: justify;
    line-height: 25px;
    margin-bottom: 40px;
}

a {
    color: rgb(28, 58, 149);
    text-decoration: none;
    font-weight: 900;
    border: 1px solid #fff;
    background-color: #fff;
    padding: 10px 30px;
    box-sizing: border-box;
}
```

para mais fontes:
https://fonts.google.com

![[FIAP/Imagens/Capitulo 2 - Continuando a imersão do conhecimento no front-end-20250203213953242.webp]]

