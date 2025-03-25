# QUE NEGÓCIO É ESSE DE PROGRAMAÇÃO?

## Conceito de algoritmo

Algoritmo são os passos para a resolução de um problema

Problema para algoritmo:

![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250107223044900.webp]]

E se no passo pegar a escada não tem escada??

![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250107223107638.webp]]
O bug é apenas um passo do seu algoritmo onde ele não foi concluído com êxito ou foi travado. Talvez ou foi mal previsto estando a mais ou a menos causando uma falha.

Do inicio

O algoritmo na etimologia, descobrimos que a palavra deriva do nome de um matemático persa do Século 9, Al-Khwarizmi. A esse matemático são atribuídas as construções dos primeiros processos para realização de operações aritméticas.
Outro matemático famoso a criar um algoritmo foi Euclides, responsável por estruturar o processo para o cálculo do Máximo Divisor Comum.
Algoritmo é uma sequência ordenada de instruções que visa resolver um determinado problema.

## TODO ALGORITMO É UM PROGRAMA DE COMPUTADOR?

No meio da computação duas das formas mais comuns de representação algorítmica são os fluxogramas (Também conhecidos como diagramas de blocos) e os pseudocódigos (que podem ter diferentes versões, como o Portugol).

Exemplo, construa um algoritmo que recebe 2 valores do usuário e realiza a soma entre eles. Ao final deve exibir o resultado dessa soma.
A representação através de um fluxograma contém uma sequencia de blocos, indicando a ordem em que os eventos ocorrerão. Já a representação através de um pseudocódigo é feita através de texto, com uma linguagem que não é uma linguagem de programação. mas que apresenta uma estrutura formal.
![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250107224154580.webp]]


```
algoritmo "Soma"
variáveis
    valor1, valor2, resultado: inteiro
início
    Escreva "Digite o primeiro valor"
    Leia valor1
    Escreva "Digite o segundo valor"
    Leia valor2
    resultado = valor1 + valor2
    Escreva resultado
Fim
```

Este algoritmo apresentado em duas formas distintas (fluxograma e pseudocódigo) e nenhum programa de computador foi escrito até esse momento.

```python
valor1 = input("Digite o primeiro valor ")
valor2 = input("Digite o segundo valor ")
resultado = int(valor1) + int(valor2)
print(resultado)
```

# CONHECENDO ALGUNS COMANDOS

```python
"""
int = inteiro
float = real
str = texto
bool = logica
"""

valor1 = int(8475.56)
valor2 = int(45.1)
valor3 = int(34955.95847)

# Formato raiz
print("Valor1=",valor1, "\nValor 2 = " ,valor2, "\nValor 3 = " ,valor3)
"""
\n força a mudança de linha no mesmo print
:.2f ---> Isto formata com duas casas decimais e por ai vai
:10.2f --> Vai jogar para a direita jogando a informação em 10bits
:010.2f --> O mesmo de cima só que com os zeros a esquerda
:5d --> coloca 5 bits no inteiro jogando o numero para a direita
:05d --> co mesmo de cima só que com 0 presente
%o --> transforma o numero em octal
"""
#Formato format()
print("Valor1= {:10.2f} \nValor 2 = {:10.2f} \nValor 3 = {:10.2f}".format(valor1, valor2, valor3))

#Outro forma de format()
print("Valor1= {0} \nValor 2 = {1} \nValor 3 = {2}".format(valor1, valor2, valor3))

#Outro forma de format()
print("Valor1= {v1:10.2f} \nValor 2 = {v2} \nValor 3 = {v3}".format(v1=valor1, v2=valor2, v3=valor3))

#formato via printF
print(f"Valor1= {valor1} \nValor 2 = {valor2} \nValor 3 = {valor3}")

#printF formatado
print(f"Valor1= {valor1:10.1f} \nValor 2 = {valor2:10.1f} \nValor 3 = {valor3:10.1f}")

#printF em %
print(f"Valor1= %d \nValor 2 = %d \nValor 3 = %d" % (valor1, valor2, valor3))

```

## Variáveis de memória e casting

Variavel é algo que muda e memória é algo que armazena
Mas a variável de memória é o local do computador onde se armazena uma informação

![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250108232312703.webp]]

```python
nome = "Lucas"
idade = 25
salario = 2000
casado = True

print("Ola pessoal")
print("Nome:", nome)
print("Idade>", idade)
print("Salário", salario)
print("Casado:", casado)

#Casting serve para modificar o conteúdo

valor = 10
print("Valor = ", valor , type(valor))
valor = Lucas
print("Valor = ", valor , type(valor))
valor = 10.95
print("Valor = ", valor , type(valor))
valor = True
print("Valor = ", valor , type(valor))

valor = 10
x = bool(valor) # 0 falso e qualquer outro valor é true
print(x, type(x))
```

Variável é um espaço que um programa pode reservar na memória RAM do computador para armazenas temporariamente alguns dados, como algo que o usuário tenha digitado ou o resultado de um cálculo.

Para permitir que o usuário digitem informações dentro de variáveis, devemos utilizar o comando input(). Em sua sintaxe, o comando input() exige a presença de uma variável antes do comande e de uma mensagem de texto entre parênteses.

```python
nome = input("Por favor, digite seu nome: ")
print(nome + " é um programador incrível!")
```

## Instrução de entrada de dados

```python
# Saída de dados: Interação do sistema com o usuário: Print
# Entrada de dados: Interação do Usuário com o sistema: Input

valor = input("Digite um valor:")
valor = int(valor)

resposta = valor + valor
print("Resultado: ", resposta)
```

```python
# Saída de dados: Interação do sistema com o usuário: Print
# Entrada de dados: Interação do Usuário com o sistema: Input

valor = float(input("Digite um valor:")) # Sempre le essa merda em String
print("Dobro =", valor + valor)

```


# A CALCULADORA!

![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250113223155358.webp]]
![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250113223351461.webp]]
![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250113223427715.webp]]
![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250113223534421.webp]]
![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250113223616900.webp]]

## Operadores aritméticos

![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250113225125912.webp]]
![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250113225150968.webp]]
![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250113230030573.webp]]

## Algoritmo: Calculando o delta

```PYTHON
# Ler o valor de A
a = int(input("Digite o valor de A:"))
# Ler o valor de B
b = int(input("Digite o valor de B:"))
# Ler o valor de C
c = int(input("Digite o valor de C:"))
# Calcular o delta
delta = b ** 2 - 4 * a * c
# Exibir o delta
print(f"Delta = {delta:.1f}")
```

## Algoritmo: Porcentagem em programação

![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250114213441922.webp]]


```Python
# FORMA TRADICIONAL DE CALCULAR A PORCENTAGEM
valor = 1000
percentual = 20
resposta = valor * percentual / 100
print(resposta)

#forma simplificada
valor = 1000
print(valor * 0.2)

#forma acrescimo
valor = 1000
print(valor * 1.2)

#forma desconto
valor = 1000
print(valor * 0.8)
```

Situação lógica para uma calculadora

![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250114214739712.webp]]

## Algoritmo múltiplo de 5:

```python
#ler um numero dado pelo usuário
num = int(input("Digite um numero: "))
mult = int(input("Digite um multiplo: "))
#calcular o proximo multiplo de 5
prox_mult_5 = num // mult * mult + mult
#exibir o proximo multiplo de 5
print(prox_mult_5)
```

## Algoritmo: Cédulas 

![[Capitulo 6 -  Primeiros passos de utilização de algoritmos e fluxogramas-20250114220157675.webp]]

```python
#Digitar a quantia
quantia = int(input("Digita a quantia: R$ "))
#calcular a quantidade de cedulas de 100
ced100 = quantia // 100
#atualizar a quantia
quantia = quantia % 100
#calcular a quantidade de cedulas de 50
ced50 = quantia // 50
#atualizar a quantia
quantia = quantia % 50
#calcular a quantidade de cedulas de 20
ced20 = quantia // 20
#atualizar a quantia
quantia = quantia % 20
#calcular a quantidade de cedulas de 10
ced10 = quantia // 10
#atualizar a quantia
quantia = quantia % 10
print(f"R$ 100.00 = {ced100}\n" 
		f"R$ 500.00 = {ced50}\n" 
		f"R$ 20.00 = {ced20}\n"
		f"R$ 10.00 = {ced10}\n")

```

# Patinete elétrico

```Python
print("Esse programa calcula a velocidade média de um patinete")
distancia = input("Qual foi a distância em metros percorrida pelo patinete? ")
tempo = input("Quantos minutos o patinete demorou para percorrer essa distância? ")
velocidade_media = float(distancia) / float(tempo)
print("O patinete atingiu uma velocidade de {} m/min".format(velocidade_media))

```