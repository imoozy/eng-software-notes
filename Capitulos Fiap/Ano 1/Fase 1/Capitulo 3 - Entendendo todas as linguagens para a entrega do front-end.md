
# INTERNET:

## Metodologia para html:
onde a ancora vai puxar --> <a href="#quadrinhos">quadradinhos</a>
Hyperlink --> <a href="http://www.fiap.com.br" target="_blank">fiap</a> A função target blank faz com que uma pagina nova apareça e não feche a anterior
Hyperlink de e-mail--> <a href="mailto:lucal7421@gmail.com">teste de email</a>
Ancora --> <a name="quadrinhos">quadrinhos</a>


# A origem do HTML

O HTML foi criado no inicio de 1990 como padrão que deveria ser seguido por centros de pesquisa para a exibição de relatórios e documentos científicos entre os pesquisadores. Quem foi a mente por trás dessa tecnologia foi John Berners-Lee, físico britânico do CERN.

Tim era o cientista responsável por várias pesquisas que estavam sendo realizadas pelo CERN em diversas partes do mundo. Os relatórios gerados pelos pesquisadores não possuíam o mesmo padrão, então a análise de resultados levava mais tempo do que deveria. Como base, ele utilizou as linguagens SGML e HyTime, que já possuíam uma padronização, fosse para a formatação de textos (SGML), fosse para hiperligações.

<a href="https://caniuse.com"> Site para a ver se um marcador deve ou não ser utilizado</a>

# HTML A LINGUAGEM QUE MARCA

A maioria das tags deve ser aberta e fechada, assim você definirá onde começa e termina o conteúdo inserido. Existem algumas tags que não precisam de fechamento, que são chamadas de elementos vazios.

![[Pasted image 20241015221232.png]]


# HTML O FOCO É CONTEÚDO

Uma das coisas mais importantes na criação de uma página web é o conteúdo. Ele deve ser apresentado de uma forma clara, objetiva e não trazer nenhum tipo de dúvida ao internauta. Precisamos também que ele esteja bem-organizado para que o usuário sempre encontre a informação procurada. Esse alerta significa que precisamos planejar muito bem antes de começar a codificá-lo

Um projeto web costuma ser separado em três camadas básicas: o conteúdo, a apresentação e o comportamento, representando HTML, o CSS e o JavaScript, respectivamente. Não é uma boa prática misturar as camadas, muito menos nossos arquivos.

## Camada de conteúdo

É onde deve-se inserir tudo aquilo que desejamos em nosso site. É redundante dizer mas na camada de conteúdo temos conteúdo. É aqui que iremos montar o código-fonte HTML, incluindo toda a estrutura de tags necessárias para exibir nossa pagina
![[Pasted image 20241015222137.png]]

## Camada de apresentação

É aqui que vamos deixar nossa página bonita, Esta camada irá formatar nosso conteúdo, tarefa para a qual contaremos com uma linguagem de formatação fantástica: o Cascading StyleSheet (CSS). Apenas com HTML sua aplicação não chamará, visualmente, a atenção do usuário. Ele não foi criado para formatar nada, então, precisaremos de alguém que saiba fazer esta tarefa. 
Vale ressaltar um frase que resume a dobradinha HTML + CSS:
![[Pasted image 20241015222427.png]]

## Camada de comportamento

Aqui a página fica mais interativa ao usuário. Utilizaremos nela a maravilhosa linguagem de programação JS (javascript), que irá fazer coisas que o HTML sozinho não é capaz de fazer. Como já foi dito anteriormente, ele é apenas uma linguagem de marcação.  
![[Pasted image 20241015222618.png]]

As três camadas em conjunto, e funcionando corretamente, irão proporcionar uma feliz experiência ao usuário. Pensar no usuário é fundamental para seu projeto, pois ele ficando feliz voltará ao seu site, recomendará para os amigos, consumirá mais o conteúdo e até mesmo os produtos, se esse for o caso. Então ele deve ter uma experiência fenomenal com o seu site a qual chamamos de user experience (UX)

# O PRINCIPIO DO FRONT-END

![[Pasted image 20241015224902.png]]
 Para criar o front-end e agradar a todo mundo, você precisará conhecer e usar três tecnologias básicas: HTML (Camada de conteúdo), CSS (Camada de apresentação) E JavaScript (Camada de comportamento).

# Estrutura básica HTML

Todo documento HTML deverá possuir uma estrutura básica de tags que irá ajudar o navegador a interpretar e renderizar o código existente na página da melhor forma possível.

Deve-se iniciar seu código com esta estrutura. Os editores de código ajudarão muito, pois a entregam praticamente pronta, mas é muito importante que saibamos o que significa cada uma das suas tags.

```HTML
<html lang=”pt-br”>
	<head>
		<meta charset="utf-8">
    <meta name="viewport" 
    content="width=device-width, initial-scale=1">
		<title></title>    
	</head>
	<body>
   Aqui vem o conteúdo da página		
	</body>
</html>
```

## Estruturando o HTML

```HTML
< !DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- comentário -->
</body>
</html>
```

< !DOCTYPE HTML>

A declaração !DOCTYPE não é uma tag HTML, mas, sim, uma instrução para o navegador sobre qual a versão HTML ou qual o tipo de linguagem que a página foi escrita. Deve ser escrita na primeira linha da marcação. Não pode haver linhas em branco antes da linha que contém a declaração.

HTML LANG="PT-BR"

É o elemento raiz. mostra o início do código. Todos os elementos existentes na página deverão ser alocados abaixo desta tag. Devemos também informar o idioma principal do documento através do atributo "Lang". No nosso caso, "pt-br" indica que o conteúdo da página está em língua portuguesa. Ao final do documento , encontramos o fechamento desta tag, representado por /html.

meta charset="UTF-8"

Esta metatag, que sempre deverá ficar na seção head, indica qual a cadeia de caracteres o documento usará. como nosso idioma possui letras com acentuação, a utf-8 é a cadeia de caracteres correta, ajudando o browser a exibir a palavra de forma correta.

meta name="viewport" content="width=device-width, initial-scale=1.0"

Esta metatag, que também deve ficar na seção head, é importante quando pensamos em design responsivo. Através dela o navegador detecta o tamanho exato da área disponível para a exibição do conteúdo no dispositivo que você está fazendo o acesso 


## Listas

```HTML
<!-- Lista não ordenada -->
<ul>
	<li>Teste 1</li>
</ul>

<!-- Lista ordenada -->

<ol>
	<li>Teste 2</li>
</ol>
```

# Inserindo Títulos


```HTML
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Projeto Traveller - São Paulo</title>
</head>
<body>
  <h1>São Paulo - a maior cidade do Brasil</h1>
  <h2>São Paulo - a maior cidade do Brasil</h2>
  <h3>São Paulo - a maior cidade do Brasil</h3>
  <h4>São Paulo - a maior cidade do Brasil</h4>
  <h5>São Paulo - a maior cidade do Brasil</h5>
  <h6>São Paulo - a maior cidade do Brasil</h6>
</body>
</html>
```

Por boa prática é que devemos usar apenas um único elemento H1 em cada página. Ele deve conter o assunto principal, muitas vezes o seu respectivo título. Os robôs de indexação de conteúdo dos buscadores utilizam essa tag em suas pesquisas para retornar os resultados encontrados.

# Parágrafos 

``` html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projeto Traveller - São Paulo</title>
</head>
<body>
    <h1>São Paulo - a maior cidade do Brasil</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero vel quidem saepe quasi hic? Dicta rerum aliquid non, qui magni, facere fuga labore odio, tempore hic recusandae nemo eveniet quas?
	</p>
	<br>
	<p>Ta foda bichão</p>
	<hr> <!-- tag de risco no meio do nada fi ou risco horizontal -->
</body>
</html>
```

## Formatação de texto 

```html
tag <b> --> bold/negrito
tag <strong> --> da mais força ao texto/negrito
tag <i> --> italico
tag <u> --> sublinhado
```

# Imagens

![[Pasted image 20241022205506.png]]
``` html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projeto Traveller - São Paulo</title>
</head>
<body>
    <h1>São Paulo - a maior cidade do Brasil</h1>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero vel quidem saepe quasi hic? Dicta rerum aliquid non, qui magni, facere fuga labore odio, tempore hic recusandae nemo eveniet quas?
</p>
<h2>O que conhecer em São Paulo</h2>
   <a href="link"></a><img src="./images/foto1.jpg" alt="Avenida Paulista" title="Avenida Paulista">
   <img src="./images/foto2.jpg" alt="Parque do Ibirapuera" title="Parque do Ibirapuera" widht="500px" height="400px">
   <img src="./images/foto3.jpg" alt="Mercadão Municipal" title="Mercadão Municipal">
</body>
</html>
```

[[Capitulo 2 - Entendendo e aprendendo o front-End com projetos]] Capitulo anterior
[[Capitulo 4 - Develop Enviromnment Desenvolver ou primeiro mapear]] Próximo capitulo