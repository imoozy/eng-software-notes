# Aprendendo sobre os desvios condicionais

Vamos aprender a propor algoritmos que levem em conta as variações que podem acontecer no cenário de aplicação!

Vamos fazer o teste de criar um script chamado "tipos_variaveis.py". O código a seguir serve para criar cada uma das variáveis, já atribuindo valores e o comando type exibe o tipo dessas variáveis.

```python
ano = 1989
nome = "Luke Skywalker"
saldo = 50.30
print(("O tipo da variável ano é {}".format(type(ano))))
print(("O tipo da variável nome é {}".format(type(nome))))
print(("O tipo da variável saldo é {}".format(type(saldo))))
```

O resultado da execução desse programa indicará que o tipo da variável ano é int, enquanto a variável nome é do tipo string e a variável saldo é do tipo float.
Quando aprendemos uma nova linguagem de programação é recomendável consultar a documentação para verificar quais são os tipos de variáveis disponíveis 


# VOCÊ DECIDE, COMPUTADOR!

## ALGORITMO: MÉDICA DE 3 NOTAS - APROVAÇÃO E REPROVAÇÃO

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250114224300492.webp]]

```python
#Digitar as 3 notas
n1 = float(input("Digite a Primeira nota: "))
n2 = float(input("Digite a Segunda nota: "))
n3 = float(input("Digite a Terceira nota: "))
#fazer o calculo da média
media = (n1 + n2 + n3) / 3
#laço de repetição para reprovação ou aprovação
if media >= 6:
	print(f"Aprovado com média: {media:.2f}")
else:
	print(f" Reprovado com média: {media:.2f}")
```

A tarefa de olhar para a média final do aluno e informar se ele pode celebrar ou se precisa ficar preocupado exige uma pergunta, ou melhor, uma condição.

Em algoritmos nós chamamos de desvio condicional a estrutura que permite realizar um teste lógico e tomar alguma ação dependendo do resultado do teste. Esse nome é fácil de entender: o algoritmo realizará um desvio na sua execução baseado em uma condição.

Em um fluxograma é fácil entender o funcionamento do desvio condicional:

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250114230107881.webp]]


## Operadores relacionais

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250114230432990.webp]]

Exemplos:

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250114230533942.webp]]
5. falso (toda vez que ler isso, terá que explicar o motivo de falso)

## INSTRUÇÃO DE DECISÃO IF

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250116211706433.webp]]
Entrada: 13       Saída: 13
entrada: -4        Saída: 4

```python
# usuário digita um número
num = int(input(Digite um número))
# se o numero for negativo
if num < 0:
	#transformar em positivo
	soma = num * -1
#apresentar o numero
print(f"O seu número é o: {soma}")
```


## Algoritmo aplicando um desconto simples

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250116213332168.webp]]


```python
valor_compra = float(input("Qual o valor de sua compra?"))

if valor_compra > 300:
	valor_compra = valor_compra * 0.9
else:
	print(f"Não foi possível ter desconto em sua compra de: {valor_compra:.2f}")
	
print(f"O valor de sua compra será de: {valor_compra:.2f}")
```

## Algoritmo: Verificando o maior valor de 3 números

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250116214321810.webp]]


```python
# Ler os 3 primeiros números
n1 = int(input("Digite o primeiro número"))
n2 = int(input("Digite o segundo número"))
n3 = int(input("Digite o terceiro número"))
# Se o primeiro numero for maior que o segundo e o terceiro o primeiro é maior
if n1 > n2 and n1 > n3:
	#exibir o primeiro número
	print(f"O número com maior valor é o: {n1}")
# Se o segundo numero for maior que o primeiro e que o terceiro, o segundo é o maior
elif n2 > n1 and n2 > n3:
	#exibir o segundo número
	print(f"O número com maior valor é o: {n2}")
# senao
else:
	#exibir o terceiro número
	print(f"O número com maior valor é o: {n3}")
```

é possivel que nos deparemos com problemas que exigem ações tanto para o caso de o teste ser verdadeiro quanto para o caso de o teste ser falso. 
![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250116215924573.webp]]

O desvio condicional que é capaz de realizar uma ação para o caso de a condição ser verdadeira e outra ação para o caso de a condição ser falsa, damos o nome de desvio condicional composto.

Resta ainda o último cenário: o que acontece caso dependendo do resultado de uma condição, desejemos realizar um segundo teste? No caso, pode ser que a companhia aérea permita que os clientes premium levem até 28kg de bagagem.

Para resolver esse problema, usamos uma estrutura chamada desvio condicional encadeado:

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250116220217557.webp]]

É menos importante se preocupar com os nomes de cada uma das estruturas do que com as ocasiões em que devem ser usadas. Frequentemente os desvios condicionais serão referidos como ifs. Isso ocorre porque na maior parte das linguagens de programação essa é a palavra que designa um desvio


## If simples em python

Situação hipotética: A FIAP está propondo a formação de um time de esportes para representar a instituição e, para isso, fará um campeonato interno no qual os alunos podem se inscrever. Porém, há uma condição: só podem ser inscritos alunos que são maiores de idade.


```portugol
variáveis
    idade: inteiro
    rm: alfanumérico
início
    Escreva “Por favor, digite seu RM”
    Leia rm
    Escreva “Por favor, digite sua idade”
    Leia idade
    Se idade >=18 então
        Escreva “Sua participação foi autorizada, aluno de RM”, rm
              Escreva “Mais instruções serão enviadas ao seu e-mail cadastrado na FIAP!”
          Fim_se
Fim
```

A estrutura do if exige uma atenção muito especial por parte do programador. Esses 4 espaços em branco que demos entro o inicio da linha de ação que será realizada serva para que o interpretador entenda que aquele conteúdo está dentro do bloco verdadeiro do if.
O programa reescrito fica assim:

```python
rm = input("Insira seu RM")
idade = input("Insira sua idade")
if int(idade) >= 18:
    print("Sua participação foi autorizada, aluno de RM {}!".format(rm))
    print("Mais informações serão enviadas para seu e-mail cadastrado!")
```

Apesar do programa atingir o objetivo proposto, ele tem algumas falhas no quesito experiência do usuário.

## If composto em python

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250121203252896.webp]]

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250121203532055.webp]]
```python
# leitura de idade do usuário
idade = int(input("digite sua idade"))
# bloco de se senão
if idade >= 18:
	print(f"Pode entrar, sua idade atual é de {idade}")
else:
	print("Entrada permitida apenas para maiores de 18 anos")

```

Se levarmos em conta o mesmo problema anterior, seria interessante exibir também uma mensagem para os alunos que são menores de idade.

```
variáveis
    idade: inteiro
    rm: alfanumérico
início
    Escreva “Por favor, digite seu RM”
    Leia rm
    Escreva “Por favor, digite sua idade”
    Leia idade
    Se idade >=18 então
        Escreva “Sua participação foi autorizada, aluno de RM”, rm
        Escreva “Mais instruções serão enviadas ao seu e-mail cadastrado na FIAP!”
    Fim_se
    Se idade <18 então
        Escreva “Sua participação não foi autorizada por causa da sua idade”
    Fim_se
Fim
```

Analise do algoritmo:

Caso um aluno tenha digitado que tem 17 anos, o primeiro desvio condicional não entrará na parte verdadeira e o segundo desvio condicional executará a parte verdadeira.

Parece que o problema está resolvido, mas existe um problema em termos de uso de recursos da máquina nesse caso! Se o aluno digitar que tem 18 anos, o primeiro teste será verdadeiro e as mensagens serão exibidas.

Essa repetição de condições desencerrarias pode ser um fator determinante no desempenho de um programa. Daí a importância de saber usar cada um dos desvios no momento correto.

```
variáveis
    idade: inteiro
    rm: alfanumérico
início
    Escreva “Por favor, digite seu RM”
    Leia rm
    Escreva “Por favor, digite sua idade”
    Leia idade
    Se idade >=18 então
        Escreva “Sua participação foi autorizada, aluno de RM”, rm
              Escreva “Mais instruções serão enviadas ao seu e-mail cadastrado na FIAP!”
          Senão
        Escreva “Sua participação não foi autorizada por causa da sua idade”
          Fim_se
Fim
```


A tarefa foi cumprida usando o bloco senão. No caso do Python, teremos a seguinte sintaxe para esse desvio condicional:

```python
if <condição>:
    <ação a ser realizada se a condição for verdadeira>
else:
    <ação a ser realizada se a condição for falsa>
```

Se for traduzido o algoritmo que foi escrito para a linguagem Python, chegará ao seguinte código no script.

``` python
rm = input("Insira seu RM")
idade = input("Insira sua idade")
if int(idade) >= 18:
    print("Sua participação foi autorizada, aluno de RM {}!".format(rm))
    print("Mais informações serão enviadas para seu e-mail cadastrado!")
else:
    print("Sua participação não foi autorizada por causa da sua idade")
```


## Algoritmo mais de dois valores

```python
n1 = int(input("Digite um número"))
n2 = int(input("Digite um segundo número"))

if n1 > n2:
	print(f"O maior número entre os dois selecionados é o {n1}")
else:
	print(f"O maior número entre os dois selecionados é o {n2}")
```

## Algoritmo aplicando um desconto composto

```python
valor_compra = float(input("Digite o valor da compra"))

if valor_compra >= 300:
	desconto = valor_compra * 0.90
	print(f"valor da compra com desconto será de: {desconto:.2f}")
else:
	desconto = valor_compra * 0.95
	print(f"valor da compra será de: R${valor_compra} e desconto de R$ {desconto:.2f}")
```

## IF encadeado em python

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250121212640571.webp]]
![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250121212952422.webp]]

Modo encadeado certo:
```python
num = int(input("Digite um número: "))

if num > 0
	print("Positivo")
else:
	if num < 0 
		print("negativo")
	else:
		print("Nulo")
```

O que fiz:
```python
n1 = int(input("Digite um número: "))

if n1 > 0:
	print("Positivo")
elif n1 == 0:
	print("Nulo")
else:
	print("Negativo")
```

Ambos estão certos nessa porra.

Grande noticia: Dado o elevado números de alunos com menos de 18 anos interessados em se inscrever no campeonato, a Fiap resolveu abrir vagas para aqueles que possuam autorização escrita dor responsáveis.
Usando a lógica do desvio condicional encadeado, se chega neste entendimento:

```
variáveis
    idade: inteiro
    rm: alfanumérico
    autorizado: caractere
início
    Escreva “Por favor, digite seu nome”
    Leia rm
    Escreva “Por favor, digite sua idade”
    Leia idade
    Se idade >=18 então
        Escreva “Sua participação foi autorizada, aluno de RM”, rm
              Escreva “Mais instruções serão enviadas ao seu e-mail cadastrado na FIAP!”
          Senão
              Escreva “Você possui autorização dos responsáveis para participar? S – SIM ou N – NÃO”
              Leia autorizado
              Se autorizado = “S” então
            Escreva “Sua participação foi autorizada, aluno de RM”, rm
                  Escreva “Mais instruções serão enviadas ao email dos seus responsáveis”
              Senão
            Escreva “Sua participação não foi autorizada por causa da sua idade”
        Fim_se
          Fim_se
Fim
```

Como já se foi feita a sintaxe do if simples e do composto em python, aplicando no script esse código ficaria assim:

```python
rm = input("Insira seu RM")
idade = input("Insira sua idade")
if int(idade) >= 18:
    print("Sua participação foi autorizada, aluno de RM {}!".format(rm))
    print("Mais informações serão enviadas para seu e-mail cadastrado!")
else:
    autorizado = input("Você possui autorização dos responsáveis? S-SIM ou N-NÃO")
    if autorizado == 'S':
        print("Sua participação foi autorizada, aluno de RM {}!".format(rm))
        print("Mais informações serão enviadas para o email dos responsáveis!")
    else:
        print("Sua participação não foi autorizada por causa da sua idade")
```


## O python e o poder do ELIF!

## Operador lógicos validade de nota
![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250121214528405.webp]]

## Operadores lógicos validade de nota com média

```python
nota1 = float(input("Digite uma nota: "))
if nota1 >= 0 and nota1 <= 10:
	nota2 = float(input("Digite uma nota: "))
	if nota2 >= 0 and nota2 <= 10:
		media = (nota1 + nota2) / 2
		print(f"Média = {media:.1f}")
		if media >= 6:
			print("Aprovado")
		else:
			print("Reprovado")
	else:
		print("Nota invalida")
else:
	print("Nota invalida")
```

## Instrução de escolha if elif else

Comando escolha só equipara equidade que no caso seria o switch

```python
dia = int(input("Digite um dia: "))

if dia == 1
	print("Domingo")
elif dia == 2
	print("Segunda-feira")
elif dia == 3
	print("Terça-feira")
elif dia == 4
	print("Quarta-feira")
elif dia == 5
	print("Quinta-feira")
elif dia == 6
	print("Sexta-feira")
elif dia == 7
	print("sabado")
else:
	print("Dia invalido")
```

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250121215936233.webp]]
Menu de programa em python

![[Capitulo 7 - Conceitos avançados de algoritmos e fluxogramas para lógica nas tomadas de decisões-20250121220003821.webp]]
Caso queira deixar o exercício colocar o código dentro da escolha.


Uma situação extremamente comum na vida de um programador precisa testar uma série de condições em sequência.

Se tomarmos por exemplo uma operadora de celular que concede bônus em consumo da franquia de internet dependendo da pontuação dos clientes: clientes que fizerem mais de 1000 pontos recebem 3gb adicionais em sua franquia, clientes que fizerem mais de 500 pontos recebem 1,5gb adicionais em sua franquia e clientes que fizerem mais de 200 pontos recebem 500mb adicionais em sua franquia, os demais não recebem nada.

algoritmo

```python
pontuacao = input("Insira a pontuação do cliente: ")
pontuacao = int(pontuacao)
if pontuacao >= 1000:
    print("O cliente tem direito a receber mais 3gb na sua franquia de internet!")
else:
    if pontuacao >=500:
        print("O cliente tem direito a receber mais 1,5gb na sua franquia de internet!")
    else:
        if pontuacao >=200:
            print("O cliente tem direito a receber mais 500mb na sua franquia de internet!")
        else:
            print("O cliente não receberá bônus.")
```

A solução está correta e funciona muito bem, mas podemos escreve-la de outra maneira.

```python
pontuacao = input("Insira a pontuação do cliente: ")
pontuacao = int(pontuacao)
if pontuacao >= 1000:
    print("O cliente tem direito a receber mais 3gb na sua franquia de internet!")
elif pontuacao >=500:
     print("O cliente tem direito a receber mais 1,5gb na sua franquia de internet!")
elif pontuacao >=200:
     print("O cliente tem direito a receber mais 500mb na sua franquia de internet!")
else:
     print("O cliente não receberá bônus.")
```