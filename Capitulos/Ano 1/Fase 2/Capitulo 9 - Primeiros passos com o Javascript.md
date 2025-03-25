
# Primeiros passos

```HTML
<body>
	<script>
		console.log("Olá mundo!!!!")
		alert("Vamos aprender javascript?") <!--Box com alerta de mensagem-->
	</script>
</body>
```

Para trabalharmos com JS na parte do front-end, assim como o CSS, precisamos de uma página HTML; então vamos usar uma ferramenta já conhecida, o editor de código VS Code. Crie uma pasta chamada primeiros_passos, nela, vamos adicionar um arquivo chamado index.html. Uma boa noticia para os projetos WEB é sempre criar pastas de projetos com letras minúsculas e usando o underline para separar as palavras. Quanto ao arquivo inicial HTML referente à nossa página inicial, use sempre index.html, além de ser um padrão de mercado.

# E se eu quiser informar dados para um programa?

## Recebendo e guardando alguns dados

```JS
<script>
	var nome = "lucas"; //var tipo char ou str
	var idade = 18;
	alert("idade dele é de "+idade)
	
	console.log("Bem vindo "+nome+"!!!");
	
	var n1 = 5
	var n2 = 7
	var resultado = n1 + n2
	
	console.log("o resultado é de: "+resultado)
</script>
```

Aqui entramos em uma parte bem interessante e que precisa de muito cuidado. Vamos falar de variáveis. Variáveis nada mais são do que áreas na memória para armazenar dados (ou informações). Tais variáveis podem tanto ter valores previamente atribuídos ou mesmo recebidos de interações com o usuário. Em JS, as variáveis podem assumir quaisquer tipos de valores: numéricos, textos ou mesmo objetos complexos (formados pela combinação de outros tipos de dados).

```JS
var numeroInteiro = 2;
var nome = "JavaScript";
var numeroReal = 2.25;
```

Essas três variáveis foram declaradas (e, portanto, têm um espaço de memória reservado,) porque utilizamos o operador var. Esse operador informa ao browser que precisamos reservar um espaço de memória para armazenar alguma informação. Com isso, podemos utilizar essas variáveis para realizar cálculos, armazenar resultados, receber informações do usuário e assim por diante.

Olha o exemplo chegando. Antes de tudo, sempre pense que as variáveis possuem um nome ( que é seu identificador). Esse nome precisa seguir uma regra: sempre deve começar com uma letra, não pode conter espaços em branco, nem símbolo especiais (símbolo de adição, vírgula, hífen, parênteses).

Então podemos pensar que se tivermos que armazenas 2 notas de alunos para calcularmos a média, como faríamos? Primeiramente, sabemos que a média das notas das provas é obtida pelo resultado da soma dessas notas, e o total dessa soma é dividido por 2. Nessa caso, teríamos o seguinte trecho de código:

```JS
var notaP1 = 8.5;
var notaP2 = 7.0;
var media = (notaP1 + notaP2)/2;
```

Até ai tudo bem, mas e se quisermos exibir essa média calculada?

```JS
console.log(media);
```

Coloca ALERT ou CONSOLE.LOG e seja feliz :LiSmile:

Tudo que vimos até agora pode ajuda, mas não responde definitivamente à pergunta inicial desta seção, que é "Como podemos fazer para o usuário informar dados". Pois bem, vamos responder a essa questão agora. A instrução para receber dados do usuário é a instrução **prompt()**, que recebe entre parênteses uma mensagem para fazer uma pergunta ao usuário. O detalhe é: Onde vamos armazenar essa valor informado (digitado) pelo usuário?

```JS
var notaP1 = prompt("Digite a nota da Prova 1");
```

O resultado dessa instrução pode ser observado na figura abaixo

![[FIAP/Imagens/Capitulo 9 - Primeiros passos com o Javascript-20250219230541422.webp]]

ótimo! Agora temos uma forma de interagir com o usuário e solicitarmos efetivamente as informações necessárias. Se quisermos mudar nosso programa de cálculo de média a partir das notas informadas, precisamos complementar algumas coisas.

```JS
var notaP1 = prompt("Digite a nota da Prova 1");
var notaP2 = prompt("Digite a nota da Prova 2");
var media = (notaP1 + notaP2) / 2;
alert("Media do aluno = "+media);
```

![[FIAP/Imagens/Capitulo 9 - Primeiros passos com o Javascript-20250219231045495.webp]]

Portanto a partir de agora, vamos começar a fazer vários pequenos programas em JS para efetivamente calcularmos valores e gerarmos resultados para os usuários.

# Vamos elaborar um exemplo completo

```html
<body>
	<script>
		var soma = 5 + 7
		console.log(soma)

		var resto = 3 % 2
		console.log(resto)

		var idade = 18
		idade++
		console.log(idade)

		var decremento = 15
		decremento--
		console.log(decremento)

		var distancia = prompt("Digite a distância: ")
		var consumo = prompt("Qual o consumo de seu carro em k/l: ")
		var litros = distancia / consumo
		console.log("Serão gastos "+litros+" litros de combustível na viagem.")
	</script>
</body>

```

Na verdade, não apenas um, mas vários exemplos completos para que entenda como usar esses elementos. 

Nunca se esqueça de que todo e qualquer programa sempre executa de forma sequencial, ou seja, linha após linha. 

Desafio 1: Elabore um programa JS que calcule a área de um trapézio, sendo que o usuário deve informar: a base maior (B), a base menor (b), e a altura (h). A formula é: A= (B+b)xh/2


```html
<body>
	<script>
		var B = prompt("Digite a base maior do trapézio: ");
		var b = prompt("Digite a base menor do trapézio: ");
		var h = prompt("Digite a altura do trapézio: ");
		var a = (B+b)*h/2;
		console.log("A área do trapézio digitado é de"+a);
	</script>
</body>
```

Desafio 2:  Elabore um programa JS que efetue o cálculo do salário líquido de um funcionário. Serão informados pelo usuário: O valor da hora trabalhada, a quantidade de horas e o percentual de desconto do imposto.

```html
<body>
	<script>
		var h_trab = prompt("Digite o valor de sua hora trabalhada: ");
		var q_horas = prompt("Digite a quantidade de horas trabalhadas: ");
		var perc_imposto = prompt("Qual o percentual de desconto de imposto: ");
		var sal_bruto = h_trab * q_horas;
		var imposto = sal_bruto * perc_imposto/100;
		console.log("Seu salário bruto é de: R$"+sal_bruto);
		console.log("Impostos a pagar: R$"+imposto);
	</script>
</body>
```
