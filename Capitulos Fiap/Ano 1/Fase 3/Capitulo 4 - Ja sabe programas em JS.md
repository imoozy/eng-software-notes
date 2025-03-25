# A decisão Simples

A decisão simples é aquela que, ao realizar um teste lógico, executa um conjunto de instruções. Sua sintaxe é dada pelo comando if.

```JS
if ( teste lógico ){
  comando 1
  comando 2
  ...
}
```

Quais testes lógicos e quais operações podemos incluir nesse teste lógico?

![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250227200107729.webp]]
![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250227200117253.webp]]

Entendemos como é a estrutura do comando if e quais operadores podemos usar. Mas como fazer isso na prática?

Imagine que você tenha que fazer um programa em JS para mostrar para um turista o que ele pode fazer em um passeio no Ibirapuera. Pergunte inicialmente o nome dele e mostre uma mensagem de boas vinda ao parque. Em seguida, pergunte se ele leva alguma valor em dinheiro.

Pensando em uma solução inicial:

- Perguntaremos o nome do nosso visitante
- Exibimos a mensagem de boas vindas
- Perguntamos se ele leva algum valor em dinheiro
- Se o valor for superior a R$ 10,00 indicamos o quiosque
- Exibimos uma mensagem de "Bom passeio".

Código:

```JS
var nomeTurista;
var valor;
nomeTurista = prompt("Olá! Qual seu nome?");
valor = Number(prompt("Quanto você traz em dinheiro?"));
if (valor > 10){
    alert("Aproveite os Quiosques de água de coco");
}
alert ("Bom passeio");
```

Nesse código-fonte, podemos ver que a mensagem "Aproveite os Quiosques de água de coco" só é exibida se o valor digitado for acima de 10 reais. Caso contrário, a instrução é ignorada e já pulamos é ignorada e já pulamos para a instrução seguinte ao bloco if. Também é possível visualizar o mesmo código graficamente.

![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250310094308043.webp]]

```js
var nomeTurista;
var valor;
nomeTurista = prompt("Olá! Qual seu nome?");
valor = Number(prompt("Quanto você traz em dinheiro?"));
if (valor > 10){
    alert("Aproveite os Quiosques de água de coco");
}
else{
	alert("Prestigie as barracas de artesanato");
}
alert ("Bom passeio");
```

![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250310101200069.webp]]

![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250310101341068.webp]]

Certo, mas como utiliza-los? Suponha as seguintes condições para decidir-se é possível ir a um passeio pelo centro da cidade, num sábado:

- Condição c1: Faz sol? (possíveis respostas: sim ou não/ true ou false)
- Condição c2: Tem combustível no carro? (possíveis respostas: sim ou não)

Baseado no operador AND (&&), que será nosso primeiro estudo, temos os quadro-verdade:

![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250310101634547.webp]]

O resultado do operador AND só é verdadeiro na situação em que ambas as condições são verdadeiras.
De forma análoga, temos o operador OR para analisar. nesse caso, diferentemente do AND, basta, para o OR que uma das condições seja verdadeira para o resultado ser verdadeiro.

![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250310102014535.webp]]

Por fim, temos o operador NOT (!) que nega (ou inverte) o resultado de uma condição lógica. 

![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250310102102165.webp]]

# A decisão alinhada

Sabemos que a instrução IF-ELSE trata apenas situações em que temos uma ação em caso verdadeiro e outra ação em caso falso. E como tratar nosso exemplo anterior no qual temos quatro diferentes situações:

![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250310102325923.webp]]

```JS
visitantes = Number(prompt("Olá! Quantos visitantes?"));
if (visitantes <= 5){
  alert("O preço do ingresso é R$ 20,00");
} else if (visitantes <= 15){
  alert("O preço do ingresso é R$ 15,00");
} else if (visitantes <= 30){
  alert("O preço do ingresso é R$ 10,00");
} else{
  alert("O preço do ingresso é R$ 8,00");
}
```

![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250310102603665.webp]]

# A seleção Múltipla

O operador de seleção múltipla, representado pelo Switch é um operador bastante elegante que permite realizar seleções para comparação de igualdades.

Imagine a situação de um aplicativo para Fast Food, no qual você digita o número do combo desejado e ele exibe os itens desse combo e o preço:

![[FIAP/Imagens/Capitulo 4 - Ja sabe programas em JS-20250310102821964.webp]]

Estrutura do Switch:

```js
switch(variável){
  case VALOR1:
    comando1;
    comando2;
    break;
  case VALOR2:
    comando3;
    break;
…
  default:
    comando4;
}
```

v1:

```JS
var combo = prompt("Qual o combo desejado?");
	switch(combo){
	  case "1":
	      alert("Hamburguer, Refri e Fritas. R$ 20,00");
	      break;
	  case "2":
	      alert("Chesseburger, Refri e Salada. R$ 22,00");
	      break;
	  case "3":
	      alert("Misto Quente, Suco e Salada. R$ 15,00");
	      break;
	   default:
	      alert("Opção inválida");
	}
```

v2:

```JS
var combo = prompt("Qual o combo desejado?");
	var combo2 = parseInt(combo); // faço a conversão
	switch(combo2){
	  case "1":
	      alert("Hamburguer, Refri e Fritas. R$ 20,00");
	      break;
	  case "2":
	      alert("Chesseburger, Refri e Salada. R$ 22,00");
	      break;
	  case "3":
	      alert("Misto Quente, Suco e Salada. R$ 15,00");
	      break;
	   default:
	      alert("Opção inválida");
	}
```


#  Criando funções

```JS
    <script>
        function aviso(){
            alert("A função aceita várias linhas de código")
            alert("e podemos chamar só quando precisarmos...")
        }

        aviso()

        var nu1 = Number(prompt("Digite o primeiro número: "))
        var nu2 = Number(prompt("Digite o segundo número: "))

        function somar(n1, n2){
            return n1 + n2;
        }

        somar(nu1, nu2)
    </script>
```

# Acessando os elementos HTML pelo ID

Como fazer para pegar os dados que os usuários inserem nas páginas? E como vamos fazer para devolver as respostar para eles?

No HTML, além dos nomes das Tags, que dão o seu significado, podemos ter também outros dois tipos de identificação. O id é um valor único e individual, que podemos atribuir a apenas um elemento da página, é como o nosso número de CPF, somente nós o possuímos. Nas tags, ele deve ser inserido assim:

```HTML
<body>
     <h2 id=” tituloSp”>São Paulo</h2>
</body>
```

Para acessar as propriedades deste elemento dentro do JS, precisamos indicar o  caminho até chegar a ele. Com o seguinte código:

```html
<body>
     <h2 id=”tituloSp”>São Paulo</h2>

     <script>
         document.getElementById(“tituloSp”).innerHTML = “SP”
      </script>
</body>
```

Repare que iniciamos a nossa instrução na linha 5 com a palavra reservada "Document", que faz referência a nossa página HTML, em seguida, temos o método "getElementById", que significa que estamos pegando um elemento pelo seu ID e dentro de seu construtor o id que queremos utilizar.

Essa parte do código nos dá acesso ao elemento completo, com todas as suas propriedades. Já o complemento "innerHTML" diz que o valor que está sendo atribuído a frente substituirá o valor original do elemento.

Exemplo:
```html
<body>
     <h1 id=”titulo”>Olá pessoal</h1>

    Título novo: <input type=”text” id=”texto”>
     <button onClick=”mudar()”>Mudar</button>

     <script>
        function mudar(){
        var novo = document.getElementById(“texto”).value
        document.getElementById(“titulo”).innerHTML = novo
      }
     </script>
</body>
```

```html
<body>

    <h1 id="titulo">Titulo da página</h1>
    <label for="texto">Texto:</label>
    <input type="text" id="texto">
    <button onclick="mudar()">Mudar</button>

    <script>
        var titulo = document.getElementById("titulo")
        var texto = document.getElementById("texto")
 

        function mudar(){
            titulo.innerHTML = texto.value
        }
 
        console.log(titulo.innerHTML)
    </script>
</body>
```

```html
<body>

    <h2>Meses do ano</h2>

    <ul>
        <li class="mes">Janeiro</li>
        <li class="mes">Fevereiro</li>
        <li class="mes">Março</li>
        <li class="mes">Abril</li>
        <li class="mes">Maio</li>
    </ul>

    <label for="posicao">Posição:</label>
    <input type="number" id="numero" min="1" max="5">
    <button onclick="escolher()">Escolher</button>
    <p>Mês escolhido <span id="resultado"></span></p>
  
    <script>
        function escolher(){
            var num = document.getElementById("numero").value -1
            var mes = document.getElementsByClassName("mes")[num].innerHTML
            document.getElementById("resultado").innerHTML = mes
        }
    </script>
</body>
```


# Acessando os elementos HTML pela classe