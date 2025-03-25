
Já conhecemos o poder das divs e como elas podem nos ajudar no desenvolvimento de nossos layouts organizando o conteúdo. Elas facilitam muito a vida de todo desenvolvedor front end e com o uso de CSS podemos deixa-las da forma que quisermos.

O problema esta justamente ai: quando falamos de apenas uma div, mas e quando tivermos várias em nossa página? Sabemos que se fizermos a declaração de uma regra CSS para um seletor de tag, e se o código HTML possuir a mesma tag repetidas vezes a formatação será aplicada a todas elas, sendo assim, se existirem várias tags div, todas elas ficaram exatamente iguais.

```html
<body>
    <div>Conteúdo da div</div>
    <div>Conteúdo da div</div>
    <div>Conteúdo da div</div>    
</body>
```

```CSS
div {
    width: 200px;
    height: 50px;
    margin: 10px;
    padding: 10px;
    border: 1px solid #DC143C;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250206214059457.webp]]

Olhando dessa forma pode até parecer errado usar divs para a construção de nossas páginas. Pode parecer, mas não é. A DIV é elemento muito importante e faz parte da estrutura do layout da página, então, use a vontade. O que podemos fazer é usar seletores mais inteligentes para o seletor de tag, e assim aplicarmos formatações diferentes para elementos iguais. ID e CLASS.

## Seletor de ID

representado pelo sinal de hashtag(#) seguido de um nome, o id é um seletor muito importante no desenvolvimento de nossas páginas e servirá como um identificador para as tags HTML. Ele é bem usado tanto na parte de CSS como também na parte de JavaScript. Poderá ser usado por outras linguagens para ajudar a executar várias tarefas, como a formatação de algum elemento.

Para atribuir um id uma tag basta usar o atributo id seguido do sinal de igualdade e um valor. O mesmo valor de um id não pode ser utilizado por dois ou mais elementos na mesma página.

Toda tag HTML pode receber um id, porém o seu uso não é obrigatório. Como boa prática e padrão do HTML, sempre escreva os valores dos IDS  de suas tags em letras minúsculas. 

```html
<body>
    <div>Conteúdo da div</div>
    <div id="container">Conteúdo da div</div>
    <div class="texto">Conteúdo da div</div>    
</body>
```

```css
div {
    width: 200px;
    height: 50px;
    margin: 10px;
    padding: 10px;
    border: 1px solid #DC143C;
}
   
#container {
    width: 300px;
    border: 10px solid #060646;
}

.texto{
	background-color: #ccc;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250206215031747.webp]]

Você deve ter percebido que a segunda div ficou diferente das demais. Isso aconteceu porque os atributos de id, quando declarados em conjunto com uma tag, têm maior especificidade do que os seletores de tag. A especificidade é a forma usada para que os browsers definam quais valores das propriedades são mais importantes para os elementos quando eles apresentarem algum conflito.
No exemplo a cima, a segunda div utiliza o "id container", sendo, assim, as regras dele sobrescrevem as regras definidas para a tag div. Nesse caso,, as bordas e largura da div serão exibidas conforme o que foi declarado no "id container".

## Seletor de classe

Representado pelo sinal de ponto no final (.) seguido de um nome, a classe é o seletor mais importante no desenvolvimento de nossas regras CSS. A ideia principal é que elas sejam usadas para criar formatações que podem ser aplicadas a vários elementos ao mesmo tempo, isso significa que elas podem ser  reutilizadas.
Diferente dos seletores de id, os seletores de classe podem e devem ser usados por diferentes elementos HTML inseridos na mesma página.

Todo elemento HTML pode fazer uso de várias classes ao mesmo tempo, para isso, basta usar o atributo class seguido do sinal de igualdade ( = ) e os nomes das classes correspondentes. Caso alguma alteração seja feita em alguma dessas classes, ela será replicada automaticamente para todas as tags que a utilizam.

```html
<body>
    <div class="container box__um">Conteúdo da div</div>
    <div class="container box__dois">Conteúdo da div</div>
    <div class="container box__tres">Conteúdo da div</div> 
</body>
```

```CSS
.container {
    width: 300px;
    height: 50px;
    margin: 10px;
    padding: 10px;
    border: 1px solid #000000;
    color: #ffffff;
}

.box__um {
    background-color: rgb(209, 27, 63);
}

.box__dois {
    background-color: rgb(17, 60, 129);
}

.box__tres {
    background-color: rgb(32, 6, 12);
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250211213909227.webp]]

Foi criada uma classe mais genérica chamada container, que possui as regras que deveriam ser repetidas em todas as três divs. Também foram criadas as classes mais especialistas com as cores que devem ser aplicadas às divs. Temos algumas vantagens codificando dessa maneira:

- Código genérico replicado a todas as divs
- Caso precise mudar uma cor, basta alterar a classe específica.
- Caso precise mudar algum outra regra, basta alterar a classe genérica.
- As classes específicas podem receber novas formatações sem comprometer as outras.

## Seletores especiais

Além de usar os seletores de tag, id e class, podemos fazer a formatação dos elementos de nossa página usando alguns seletores especiais.

### Seletor * (ASTERISCO)

Com o uso do sinal de asterisco ( * ) podemos aplicar formatações a todos os elementos de uma página. Bem utilizado quando queremos resetar alguns padrões que os navegadores sempre aplicam assim que renderizam alguma página.

```html
<div class="container">
    <h1>Projeto Traveller</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequuntur alias ipsam, sint fuga modinesciunt cumque
        quam eum. Possimus, veniam!
    </p>
    <h2>Atrações de São Paulo</h2>
    <ul>
        <li>Teatro Municipal</li>
        <li>Parque do Ibirapuera</li>
        <li>Zoológico</li>
    </ul>
</div>
```

```CSS
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

No código fonte "Código CSS - seletor asterisco", todas as tags terão seuas margens externas e internas zeradas, e, caso seja aplicado algum valor ao padding, eles não serão adicionados ao tamanho dos elementos.

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250211221151057.webp]]

### Seletor de descendência

Usado quando você deseja formatar um elemento que esteja dentro de outro, ou seja, um descendente. Exemplo: formatar os elementos **li** de um **ul**.

```html
<ul>                
   <li>Teatro Municipal</li>
   <li>Parque do Ibirapuera</li>
   <li>Zoológico</li>               
</ul>
```

```css
ul li{
    color: #08347a;
    font-size: 25px;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250211221411975.webp]]

## Seletor adjacente

Representado pelo sinal de adição (+), deve ser usado quando você deseja formatar o próximo elemento após o elemento citado. EX:

```html
<p>Atrações de São Paulo</p>
<ul>
    <li>Teatro Municipal</li>
    <li>Parque do Ibirapuera</li>
    <li>Zoológico</li>
</ul>
<p>Atrações de São Paulo</p>
```

```css
ul + p{
    color: #DC143C;
    font-size: 25px;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217140018247.webp]]


## Seletor de irmão

Representado pelo sinal de til (~), deve ser usado quando você formatar todos os elementos após o elemento citado. Ex:

```html
<div class="box">
    <p>Projeto Traveller</p>
    <p>Projeto Traveller</p>
</div>
<p>Projeto Traveller</p>
<p>Projeto Traveller</p>
<p>Projeto Traveller</p>
```

```css
div ~ p {
    font-size: 25px;
    color: #DC143C;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217140140201.webp]]

## Seletor de filhos diretos

Representado pelo sinal de maior que (>), deve ser usado quando você deseja formatar apenas os descendentes diretos do elemento. Ex:

```html
<div class="container">
  <p>Projeto Traveller</p>                
  <div class="box">
     <p>Projeto Traveller</p>
     <p>Projeto Traveller</p>
   </div>     
   <p>Projeto Traveller</p>
</div>
```

```css
.container > p {
    font-size: 25px;
    color: #DC143C;
}
```

## PSEUDOCLASSES

Ao lado do nome do seletor, podemos colocar algumas palavras-chave que ajudarão na formatação do elemento conforme o seu estado.

### Pseudoclasse hover

Aplica uma formatação ao elemento quando o mouse passar sobre ele, assim que o mouse sair desse elemento, ele voltará ao seu estado normal. EX: mudar a cor da fonte assim que o mouse passar nas tags A.

```html
<ul>
  <li><a href="bares.html">Bares</a></li>
  <li><a href="restaurantes.html">Restaurantes</a></li>
  <li><a href="cinema.html">Cinemas</a></li>
  <li><a href="museus.html">Museus</a></li>
</ul>
```

```css
ul a:hover {
    color: #DC143C;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217141913657.webp]]

### Pseudoclasse nth-child

Aplica uma formatação a um elemento conforme a sua posição dentro de um grupo. Exemplo: deixar o quarto paragrafo com as cores de fundo e fonte diferentes dos demais.

```html
<div class="box">
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
</div>
```

```css
.box p:nth-child(4) {
    background-color: #DC143c;
    color: #fff;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217145442534.webp]]
Podemos também usar as palavras chave odd (**impar**) e even (**par**) para aplicar formatações para elementos nessas posições. Exemplo: deixar os parágrafos pares com cor de fundo azul e os ímpares com cor de fundo vermelha.

```html
<div class="box">
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
</div>
```

```css
.box p:nth-child(odd){
    background-color: #DC143c;
}

.box p:nth-child(even){
    background-color: #5681DF;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217145638374.webp]]

### Pseudoclasse first-child

Aplica uma formatação ao primeiro elemento de um grupo. Ex: Deixar o primeiro parágrafo com o texto centralizado e cores de fundo e de texto diferentes dos demais.

```html
<div class="box">
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
</div>
```

```css
.box p:first-child {
    text-align-center
    background-color: #DC143c;
    color: #fff;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217214142039.webp]]

### Pseudoclasse Last-child

Aplica uma formatação ao último elemento de um grupo. Exemplo: deixar o último parágrafo com o texto centralizado e cores de fundo e de texto diferentes dos demais.

```html
<div class="box">
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
   <p>Projeto Traveller</p>
</div>
```

```css
.box p:last-child{
    text-align-center
    background-color: #DC143c;
    color: #fff;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217214302188.webp]]

## Pseudoelementos

São palavras chave que podem ser adicionadas a qualquer seletos CSS, permitindo, assim, a formatação de uma parte específica do elemento referenciado. Quando você utilizar os pseudoelementos, lembre-se colocar o sinal de dois pontos duas vezes ( :: ), isso distinguirá os pseudoelementos das pseudoclasses.

Você deve usar apenas pseudoelementos em cada seletor.

Consulta de pseudoelementos: https://caniuse.com

```html
<div class="box">
    <h2>Projeto Traveller</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Error, doloribus voluptatibus placeat, exercitationem non animi enim possimus officiis ipsam quasi nam, ipsa impedit facere in temporibus provident earum atque consequuntur.</p>                 
</div>
```

```css
.box p::first-line{
    background-color: #dc143c;  
    color: #fff;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217214603311.webp]]
### Pseudoelementos After e Before

É muito legal usar esses pseudoelementos, pois permitem que algum conteúdo seja inserido antes ou depois do elemento a ele associado. Essa inserção é feita pela CSS, utilizando a propriedade content. Um conteúdo inserido de forma dinâmica e que pode sofrer ações da formatação.

```html
<div class="box">
   <h2>Visite em São Paulo</h2>            
   <ul>
        <li>Teatro Municipal</li>
        <li>Parque do Ibirapuera</li>
        <li>Zoológico</li>
        <li>Planetário</li>
        <li>Masp</li>
   </ul>           
</div>
```

```css
h2::after {
    content: '';
    width: 150px;
    height: 3px;
    background-color: #FFF;       
    margin: 20px auto 10px;
    display: block;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217214816516.webp]]

Caso queira mudar a regra CSS para utilizar o pseudoelemento before, então, a linha ficará posicionada antes do elemento h2

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217214933348.webp]]

---
### Pseudoelemento selection

Aplicará uma formatação diferente assim que alguma parte do seu conteúdo for selecionada

```html
<div class="container">
   <h1>Projeto Traveller</h1>
   <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eius delectus aspernatur id rem? Fugit id molestias voluptatum magni…<p>
</div>
```

```css
.container p::selection{
    background-color: #1f1f68;
    color: #fff;        
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217215349080.webp]]

fontes awesome: https://fontawesome.com
pesquisar por cdn

A tag i permite colocar um texto no estilo itálico, as letras ficam inclinadas. Essa tag era utilizada nos primórdios da internet, antes do surgimento das boas práticas, quando era comum misturar conteúdo e formatação. No caso da Font Awesome, eles usam essa tag como um container para as classes que exibirão os ícones. não insira conteúdo nesse elemento. 

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217220033415.webp]]
Para que os ícones sejam visíveis na tela, precisamos de alguém que entenda essas classes que estão nas tag i. No próprio site da Font Awesome, você pode fazer seu cadastro, que lhe enviará um link com o endereço de algum servidor que disponibiliza esse serviço.

Caso você não queira cadastrar, pode utilizar o https://cdnjs.com/libraries/font-awesome , ele também disponibilizará o endereço de algum servidor que tenha esses ícones

```html
<body>
    <div class="container">
        <img src="./images/droneMavic3.jpg" class="drone__imagem" alt="Suite master do Wonderful drone">
        <div class="drone">
            <h2 class="drone__titulo">The Wonderful drone</h2>
            <p class="drone__localizacao">São Paulo - SP</p>
            <p class="drone__avaliacao">
                <i class="fas fa-star drone__estrelas">
                    <i class="fas fa-star drone__estrelas">
                        <i class="fas fa-star drone__estrelas">
                            <i class="fas fa-star drone__estrelas">
                                <i class="fas fa-star drone__estrelas drone__estrelas__cinza">
            </p>
            <h3>Descrição</h3>
            <p class="drone__descricao">
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Suscipit repellendus ratione maiores
                voluptate, nam ullam, ad et dolor porro aperiam laborum consequatur ab, maxime dolorum provident
                libero nobis? Nulla adipisci voluptatem quam.
            </p>
            <h3>Facilidades</h3>
            <p class="drone__facilidades">
                <i class="fas fa-wifi drone__facilidades_icone">
                    <i class="fas fa-dolly-flatbed drone__facilidades_icone">
                        <i class="fas fa-coffee drone__facilidades_icone">
                            <i class="fas fa-spa drone__facilidades_icone">
                                <i class="fas fa-bed drone__facilidades_icone">
                                    <i class="fas fa-parking drone__facilidades_icone">
            </p>
            <p class="drone__reservas"><a href="" class="drone__botao__reserva">Reservar</a></p>
        </div>
    </div>
</body>
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217220845062.webp]]


```css
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@300&family=Open+Sans+Condensed:wght@300&display=swap');

html {
    font-family: 'Lato', sans-serif;
}

.container{
    width: 600px;
    margin: 0 auto;
}

h3{
    font-weight: 900;
    font-size: 25px;
    color: rgb(62, 68, 153);
}

.drone__imagem{
    width: 100%;
    height: 150px;
}

.drone{
    border: 1px solid #ccc;
    padding: 0 10px;
}

h3,
.drone__titulo,
.drone__localizacao,
.drone_descricao,
.drone__estrelas,
.drone__facilidades {
    margin: 10px 0;  
}

.drone__titulo {
    font-size: 40px;
    color: rgb(6, 6, 83);
    font-weight: 900;
}

.drone__localizacao {
    font-size: 20px;
    font-weight: 700;
}

.drone__estrelas {
    font-size: 18px;
    color: #333;
}

.drone__avaliacao i:last-child {
    color: #999;
}

.drone__descricao {   
    font-size: 18px;
    text-align: justify;
    line-height: 25px;
}

.drone__facilidades_icone {
    font-size: 18px;
    margin: 10px;
    color: #666;
    padding: 10px;
    border: 1px solid #666;
    border-radius: 50%;
}

.drone__reservas {
    margin: 30px 0;
}

.drone__botao__reserva {
    padding: 15px 40px;
    background-color: rgb(62, 68, 153);
    border: 1px solid rgb(62, 68, 153);
    color: #fff;
    text-decoration: none;
    border-radius: 5px;
    text-transform: uppercase;    
}

.drone__botao__reserva:hover {
    color: rgb(62, 68, 153);
    background-color: #FFF;
}
```

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217220901467.webp]]

![[FIAP/Imagens/Capitulo 6 - Aprender o front integrado e não integrado para a entrega das sprints-20250217220913376.webp]]

