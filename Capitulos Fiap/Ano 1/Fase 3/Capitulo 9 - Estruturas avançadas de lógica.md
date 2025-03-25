
# Quer que eu repita?

Imagine que todos os alunos estejam cadastrados em um único arquivo de texto, no formato csv e que, munido dessa lista, você deve disparar um e-mail para todos os alunos menores de idade.

Em um cálculo rápido, se o arquivo tiver 10k linhas, você precisará de 10k ifs para verificar se cada aluno em cada das linhas é maior ou menor de idade.

```PSEUDOCÓDIGO
se <condição para a 1ª linha> então
    //o que ocorrerá se o aluno for menor
fim_se
se <condição para a 2ª linha> então
    //o que ocorrerá se o aluno for menor
fim_se
se <condição para a 2ª linha> então
    //o que ocorrerá se o aluno for menor
fim_se
...
se <condição para a 10.000ª linha> então
    //o que ocorrerá se o aluno for menor
fim_se
```

Além de ser contraproducente fazer a inserção manual de cada um desses bloco, o programa fica mais suscetível a falhas por conta do desenvolvedor e menos passível de manutenção.

Um loop é uma estrutura que permite indicar a repetição de uma tarefa em um determinado número de vezes. Dessa maneira conseguimos fazer com que o programa repita a tarefa de verificar a idade para cada uma das linhas do arquivo:

```PSEUDOCÓGIDO
para linha de 1 até 10000 passo 1 faça
    se <condição para linha> então
        //o que acontecerá se o aluno for menor
    fim_se
fim_para
```

Resumidamente, uma estrutura de repetição é utilizada em um algoritmo todas as vezes que um trecho do código for redundante, ou seja, quando parte do seu código "clamar" por repetição.

Como saber se o trecho do programa necessita de repetição?

Vamos utilizar um exemplo mais simples para definirmos a necessidade ou não de utilização de laços: Imagine que alguém queira exibir um número na tela. Para tal usaríamos:

**Escreva N**

Este problema não sugere uma repetição.

Mudando o contexto deste problema: e se precisássemos exibir os números de 1 a 100 na tela. Com um novo problema de mostrar 100 números. Sim, esta rotina sugere repetição; então vamos estruturar uma laço que de 100 voltas e dentro dele colocaremos apenas um comando Escreva:

```Pseudocódigo
para n de 1 até 100 passo 1 faça
    Escreva n
Fim_para
```

Em lógica de programação há três estruturas de repetição

- Laço contador para **for**
![[FIAP/Imagens/Capitulo 9 - Estruturas avançadas de lógica-20250310214947492.webp]]
- Laço pré-condicional Enquanto-Faça **While**
![[FIAP/Imagens/Capitulo 9 - Estruturas avançadas de lógica-20250310214608710.webp]]
- Laço pós condicional Faça-Enquanto
![[FIAP/Imagens/Capitulo 9 - Estruturas avançadas de lógica-20250310214815301.webp]]

## Enquanto for verdade vamos repetir

A primeira estrutura de repetição que veremos é o laço pré-condicional Enquanto-faça (while). Exemplo logo a cima

Comparando o laço pós-condicional Faça-Enquanto com o laço pré-condicional Enquanto-Faça a condição inverte, ou seja, no Faça-Enquanto primeiro é executado o bloco de repetição e depois é analisada a condição para prosseguir no laço ou não, ao contrário do laço pré-condicional.

Representação do laço pós-condicional Faça-Enquanto no pseudocódigo:

```PSEUDOCÓDIGO
Faça
    Bloco de Repetição
Enquanto Condição
```

Na teoria, para os programadores, o laço pós-condicional também é conhecido como Repita até que(repeat until):

```PSEUDOCÓDIGO
Repita  // Repeat
    Bloco de Repetição
Até que Condição // until
```

A linguagem C e suas derivadas (C++, C#, Java, JavaScript...) utilizam o comando **do while()** para representar o Faça-Enquanto, enquanto a linguagem de programação Delphi e a sua nativa Pascal (entre outras), utilizam o Repeat Until para representar o Repita até que.

A estrutura Faça-Enquanto executa o laço enquanto a condição resultar verdade e a estrutura Repita-Até que, executa a repetição até que a condição seja verdadeira, ou seja, executa enquanto a condição for **falsa.**

Esta comparação foi feita apenas para que você pudesse perceber que as linguagens tem formas diferentes de tratar o mesmo comando, seja por sintaxe ou detalhes do funcionamento ou até não existir como no caso com o Python.

Falando de conceito. O que o comando Faça-Enquanto tem de diferente do comando Enquanto-faça? O segundo, como vimos, primeiro analisa a condição e depois executa o bloco de repetição caso a condição resulte verdade, enquanto o primeiro incialmente executa o bloco de repetição e depois analisa através da condição se deve continuar.

Isso faz com que o laço faça-enquanto tenha a característica 1, N; ou seja, executa ao menos uma vez o bloco de repetição (diferente do Enquanto-faça que pode executar nenhuma vez o bloco de repetição: 0, N) e executa no máximo várias vezes o bloco de repetição.

Em qual situação privilegiamos o laço Faça-Enquanto aos outros? Em situações em que o bloco de repetição tenha que ser executado ao menos uma vez.

Exemplificando: considere que um algoritmo leia números, efetue a somatória e no final exiba o total da soma. Concorda que para este caso ao menos um número deverá ser digitado. Então vamos utilizar este programa para demonstramos o funcionamento do faça-enquanto.

Quando estamos aprendendo a usar laços, a maior dificuldade é sabermos "o que fica dentro do laço e o que fica fora". Para facilitar este entendimento, vamos usar a descrição narrativa do algoritmo:

![[FIAP/Imagens/Capitulo 9 - Estruturas avançadas de lógica-20250311212443132.webp]]
Primeiro vamos definir os passos importantes:

- Ler os números
- Somar os números 
- Exibir a soma dos números

Agora analise cada passo individualmente e pergunte: Este laço requer repetição? Se a resposta for sim, ele estará dentro do laço, senão ficará fora do laço.

Vamos lá:

1. Ler números requer repetição? Sim
2. Somar os números requer repetição? Sim
3. Exibir a soma dos números requer repetição? Não

Assim, o primeiro e segundo passos formarão o bloco de repetição porque requerem repetição, enquanto o terceiro passo será colocado no algoritmo depois do término do laço.

```PSEUDOCÓDIGO
Programa Ex_Faca_Enquanto
Var
    somatoria,num: Real
Início
    somatoria = 0
    Escreva “Digite números ou 0 para finalizar...”
    Faça
1.      Leia num
2.      somatoria = somatoria + num
    Enquanto num != 0
3.  Escreva “Somatória = “, Somatória
```

Reparem que no pseudocódigo foi colocado o número que representa cada passo da descrição narrativa para a visualização de onde cada passo deve estar. Concluímos que os dois primeiros passos devem estar dentro do laço e o terceiro fora.

Como ficaria esta construção no Python?

```Python
somatoria = 0
print("Digite números ou 0 para finalizar...")
while True:
    num = float(input())
    somatoria = somatoria + num
    if num == 0:
        break
    print(f"Somatoria = {somatoria}")
```

Nesta simulação, colocamos o comando while True: que quer dizer "faça infinitamente", assim, chegando neste comando entra no laço incondicionalmente. Para simular a condição no final do laço, colocamos o if num == 0: para caso o usuário tenha digitado 0, o break força a saída do laço.

Assim, contemplamos o conceito do laço faça-enquanto no Python. Foi executado ao menos uma vez o bloco e a condição de saída ou continuidade do laço foi colocada no final da estrutura de repetição.

Mas, antes de chegarmos a esses problemas mais elaborados, vamos continuar explorando o While. Então, o que podemos fazer se quisermos controlar quantas repetições serão realizadas?

É aí que entra em cena a figura da variável contadora. Ela nada mais é do que uma variável que será usada como condição do nosso loop, sendo incrementada a cada volta realizada.

Para que tenhamos uma repetição de 10 voltas, podemos pensar em um algoritmo próximo ao seguinte:

```PSEUDOCÓDIGO
Variáveis:
    i: inteiro
Início
    i = 0
    Enquanto (i<10) faça
        Escreva “Mais uma mensagem, com i valendo: ”, i
        i = i + 1
    Fim_enquanto
Fim
```

Perceba que a cada volta, fazemos o incremento da variável i (i = i+1), aumentando o seu valor para que, eventualmente, ela atinja o limite estipulado na condição do laço (i<10)

Em Python seria:

```PYTHON
#criação da variável com um valor inicial
i = 0
#enquanto a variável contadora não chegar ao limite
while (i<10):
    #para cada uma das repetições uma mensagem é exibida
    print("Mais uma mensagem, com i valendo: {}".format(i))
    i = i + 1
```

Da mesma forma como realizamos o incremento na variável i, poderíamos ter realizado um decremento.


> [!NOTE] nota
> Algumas linguagens de programação suportam notações como "i++" ou "i+1" para a operação de incremento na variável contadora.

![[FIAP/Imagens/Capitulo 9 - Estruturas avançadas de lógica-20250311214907463.webp]]

```PYTHON
cont = 0
while cont < 10
	print("Comando 1")
	print("Comando 2")
	print("Comando 3")
	if cont == 5:
		cont = cont + 1
		break
		print("Comando 4")
		print("Comando 5")
		print("Comando 6")
		print("Comando 7")
		print("Comando 8")
	cont = cont + 1
else
	print("O laço foi executado sem interrupção!)
	
```

## Para lá e para cá

Já sabemos que um loop serve para repetir a execução de um determinado trecho do nosso programa, e podemos até mesmo utilizar o while aliado a uma variável contadora para controlar o número de vezes que isso vai acontecer.

Quando estamos diante de um problema que exige um número determinado de repetições, há uma estrutura mais apropriada do que o loop while: o laço de repetição para

A ideia de funcionamento do laço de repetição para é baseada em determinarmos um ponto inicial e um ponto final para a repetição, sendo que a própria estrutura se encarregará de controlar o número de voltas.

A estrutura no laço contador PARA (for):

![[FIAP/Imagens/Capitulo 9 - Estruturas avançadas de lógica-20250311215552474.webp]]

Analisando a sintaxe em pseudocódigo, conseguimos entender bem esse funcionamento:
```PSEUDOCÓDIGO
para <contadora> de <valor inicial> até <valor final> passo <incremento> faça
    //instruções que serão repetidas
fim_para
```

A estrutura de loop for é frequentemente utilizda pelos programadores pela sua facilidade de compreensão e implementação

Se quisermos uma repetição de 10x em linguagem Python, podemos fazer uso de uma função chamada range que definirá um intervalo de valores para a nossa variável contadora assumir.

```Python
#a variável contadora deverá assumir valores no intervalo entre 0 e 9
for x in range(10):
    #para cada um desses valores, vamos printar o valor da variável
    print(x)
```

Se traduzirmos a escrita do código usando rudimentos de inglês instrumental, poderemos ler: "para a variável x no intervalo entre 0 e 9, faça:"

Mas vamos supor que você não queira que a sua variável contadora inicie com o valor 0.

Isso é possível alterando a função range com a inclusão de outro argumento. Se escrevermos range(1,15), por exemplo, o valor inicial da variável será de 1 e o valor final da variável contadora será 14.

```Python
#a variável contadora deverá assumir valores no intervalo entre 1 e 14
for x in range(1,15):
    #para cada um desses valores, vamos printar o valor da variável
    print(x)
```

Se escrevermos range (1,10,2), a variável assumirá o valor inicial como sendo 1, o valor final como sendo 9, e a cada volta ela somará 2. Portanto terá os valores: 1, 3, 5 ,7 e 9

```Python
#a variável contadora deverá assumir valores no intervalo entre 1 e 9 com incremento 2
for x in range(1,10,2):
    #para cada um desses valores, vamos printar o valor da variável
    print(x)
```

o loop for é extremamente simples de usar, e com o passar do tempo, ele estará presente em quase todos os programas.


# Aplicando isso tudo


Para todos os algoritmos que envolvam laços, conseguimos resolver todos os estilos e laços, mas sempre há um laço mais apropriado para cada problema:

- Enquanto-Faça (while): Para situações condicionais (voltas indeterminadas), em que pode ocorrer de não executar nenhuma vez o bloco de repetição
- Faça-Enquanto (while True): para situações condicionais (voltar indeterminadas), em que deve ao menos executar uma vez o bloco de repetição.
- Para (for): Para situações de contagem determinadas de voltar (finitas), em que o programador tem o maior poder de manipulação do intervalo das voltas através do contador.

![[FIAP/Imagens/Capitulo 9 - Estruturas avançadas de lógica-20250317200216145.webp]]


```python
soma = 0

while True:
	n = float(input("Digite um número: "))
	soma = soma + n
	if n == 0:
		break
print("Somatória: ", soma)
		
```



![[FIAP/Imagens/Capitulo 9 - Estruturas avançadas de lógica-20250317201330955.webp]]


```
tab = int(input("Digite a tabuada"))
for volta in range (1, 11, 1):
	mult = tab * volta
	print(f"{tab} x {volta} = mult")
```



```
n1 = int(input("Digite um número: "))
n1 = int(input("Digite outro número: "))

for volta in range(n1, n2, 1):
	print(volta)
```

## Eu preciso de um menu!

Uma das frustrações mais comuns nos nossos primeiros programas é que eles "acabam". Para solucionarmos esse problema, uma excelente solução é criar uma estrutura de menus, na qual o usuário possa escolher se pretende continuar executando o programa ou se quer finalizar o ciclo.

Com esse loop podemos estabelecer a lógica: enquanto o usuário não pressionar uma determinada opção, o menu continua sendo exibido.

```python
#variável que servirá para receber a opção do usuário
op = -1
#enquanto o usuário não digitar a opção de saída
while op!=4:
    #exibição das opções do menu
    print("SUPER PROGRAMA MARAVILHOSO")
    print("1 - Rodar código 1")
    print("2 - Rodar código 2")
    print("3 - Rodar código 3")
    print("4 - Sair do programa")
    op = int(input("Informe sua opção: "))
    
    #verificação das opções disponíveis
    if op == 1:
        #O que ocorrerá se a opção 1 for selecionada
        print("CÓDIGO 1 RODANDO!")
    elif op == 2:
        #O que ocorrerá se a opção 2 for selecionada
        print("CÓDIGO 2 RODANDO!")
    elif op == 3:
        #O que ocorrerá se a opção 3 for selecionada
        print("CÓDIGO 3 RODANDO!")
#Quando o looping terminar de rodar, exibir essa mensagem
print("OK! O programa está encerrado...")
```

## A média de pesos!

No caminhão de uma empresa de transportes cabem exatamente 100 caixas de iguais dimensões. O peso dessas caixas, porém pode variar dependendo do seu conteúdo.

Como alguns caminhões tem se desgastado mais do que outros, você foi convocado para criar algoritmo que calcule o peso total das caixas que serão colocadas em um caminhão e que exiba o peso médio das caixas.

A solução mais simples para isso é pedir que o usuário vá digitando o peso das caixas á medida que elas são colocadas no caminhão. Como sabemos que se trata de 100 caixas, podemos utilizar o loop for para nos ajudar.

```python
#variavel para armazenar o peso total das caixas
peso_total = 0.0
#loop para repetir por 100 vezes a solicitação de peso
for x in range(1,101):
    #para cada volta do loop, solicitar o peso da caixa
    peso_atual = float(input("Informe o peso da caixa atual:"))
    #para cada peso solicitado, somar ao peso total
    peso_total = peso_total + peso_atual
#ao final do loop, calcular a média aritmética
media = peso_total/100
#exibição dos resultados!
print("O peso total de caixas é {}. 
A média de peso é {}".format(peso_total, media))
```

## Contagem de alunos aprovados!

Vamos considerar em uma turma da FIAP tenha 40 alunos. O algoritmo deverá ler todas as notas de todos os alunos de um determinada disciplina. Os critérios para a aprovação é o seguinte:

- 3 Checkpoints (tirando a menor nota) - 20%
- 2 sprint (Challange) - 20%
- 1 prova semestral - 60%

Este critério é para cada semestre. O que diferencia um semestre do outro é que a média do primeiro vale 40% da média final enquanto, a média do segundo semestre vale 60%.

Depois de lidas as notas, deve-se efetuar o cálculo das médias de cada aluno, exibi-las com o status 'Aprovado' (média de ao menos 6) ou 'Não aprovado' e contar quantos alunos foram aprovados direto.

```python
n1 = float(input("digite a nota 1: "))
n2 = float(input("digite a nota 2: "))

media = (n1 + n2) / 2

```


```python
contagemAprovados = 0
qtdAlunos = 40
aluno = 1
while aluno <= qtdAlunos:
    # P R I M E I R O   S E M E S T R E
    print(f"------------------------------- ALUNO: {aluno}")
    print("PRIMEIRO SEMESTRE")
        
    # Leitura dos checkpoints
    chk1 = float(input("Digite o Checkpoint 1:"))
    chk2 = float(input("Digite o Checkpoint 2:"))
    chk3 = float(input("Digite o Checkpoint 3:"))
            
    # Verificando o Checkpoint de menor valor
    menor = chk1
    if chk2 < menor:
        menor = chk2
    if chk3 < menor:
        menor = chk3
            
    # Calculando a média dos Checkpoints
    mediaChk = (chk1 + chk2 + chk3 - menor) / 2
            
    # Leitura dos Sprints
    sprint1 = float(input("Digite o Sprint 1:"))
    sprint2 = float(input("Digite o Sprint 2:"))
            
    # Calculando a média dos Sprints
    mediaSprint = (sprint1 + sprint2) / 2
            
    # Leitura da prova semestral
    semestral = float(input("Digite prova semestral:"))
            
    # Ponderando os valores das médias
    pontosChk = mediaChk * 0.2
    pontosSprints = mediaSprint * 0.2
    pontosSemestral = semestral * 0.6
            
    # Cálculo da media do primeiro semestre
    mediaPrimeiroSemestre = (pontosChk + pontosSprints + pontosSemestral)
            
    # Pontos obtidos no primeiro semestre
    pontosPrimeiroSemestre = mediaPrimeiroSemestre * 0.4
        
    # S E G U N D O   S E M E S T R E
    print("SEGUNDO SEMESTRE")
    
    # Leitura dos checkpoints
    chk1 = float(input("Digite o Checkpoint 1:"))
    chk2 = float(input("Digite o Checkpoint 2:"))
    chk3 = float(input("Digite o Checkpoint 3:"))
            
    # Verificando o Checkpoint de menor valor
    menor = chk1
    if chk2 < menor:
        menor = chk2
    if chk3 < menor:
        menor = chk3
            
    # Calculando a média dos Checkpoints
    mediaChk = (chk1 + chk2 + chk3 - menor) / 2
    
    # Leitura dos Sprints
    sprint1 = float(input("Digite o Sprint 1:"))
    sprint2 = float(input("Digite o Sprint 2:"))
           
    # Calculando a média dos Sprints
    mediaSprint = (sprint1 + sprint2) / 2
            
    # Leitura da prova semestral
    semestral = float(input("Digite prova semestral:"))
            
    # Ponderando os valores das médias
    pontosChk = mediaChk * 0.2
    pontosSprints = mediaSprint * 0.2
    pontosSemestral = semestral * 0.6
            
    # Cálculo da media do segundo semestre
    mediaSegundoSemestre = (pontosChk + pontosSprints + pontosSemestral)
            
    # Pontos obtidos no segundo semestre
    pontosSegundoSemestre = mediaSegundoSemestre * 0.6
        
            
    # Exibiçao da media do primeiro semetre
    print (f"
Média do Primeiro Semestre: {mediaPrimeiroSemestre:.1f}")
            
    # Exibiçao da media do segundo semetre
    print (f"Média do Segundo Semestre: {mediaSegundoSemestre:.1f}")
            
    # Cálculo da média final
    mediaFinal = pontosPrimeiroSemestre + pontosSegundoSemestre
    print (f"Média Final: {mediaFinal:.1f} - ", end="")
            
    if mediaFinal >= 6:
        contagemAprovados += 1
        print("Aprovado!")
    else:
        print("Não Aprovado!")
        aluno += 1
        
# Exibição da Quantidade de Alunos Aprovados
print("Quantidade de aprovados: ", contagemAprovados)

```

Feito o algoritmo com o laço Enquanto-Faça, agora faremos o mesmo código com o laço Faça-Enquanto lembrando que esse laço nao existe explicitamente em Python:

```python
contagemAprovados = 0
qtdAlunos = 40
aluno = 1

# Simulação do laço Faça-enquanto
while True:
    # P R I M E I R O   S E M E S T R E
    print(f"------------------------------- ALUNO: {aluno}")
    print("PRIMEIRO SEMESTRE")
        
    # Leitura dos checkpoints
    chk1 = float(input("Digite o Checkpoint 1:"))
    chk2 = float(input("Digite o Checkpoint 2:"))
    chk3 = float(input("Digite o Checkpoint 3:"))
            
    # Verificando o Checkpoint de menor valor
    menor = chk1
    if chk2 < menor:
        menor = chk2
    if chk3 < menor:
        menor = chk3
            
    # Calculando a média dos Checkpoints
    mediaChk = (chk1 + chk2 + chk3 - menor) / 2
            
    # Leitura dos Sprints
    sprint1 = float(input("Digite o Sprint 1:"))
    sprint2 = float(input("Digite o Sprint 2:"))
            
    # Calculando a média dos Sprints
    mediaSprint = (sprint1 + sprint2) / 2
            
    # Leitura da prova semestral
    semestral = float(input("Digite prova semestral:"))
            
    # Ponderando os valores das médias
    pontosChk = mediaChk * 0.2
    pontosSprints = mediaSprint * 0.2
    pontosSemestral = semestral * 0.6
            
    # Cálculo da media do primeiro semestre
    mediaPrimeiroSemestre = (pontosChk + pontosSprints + pontosSemestral)
            
    # Pontos obtidos no primeiro semestre
    pontosPrimeiroSemestre = mediaPrimeiroSemestre * 0.4
        
    # S E G U N D O   S E M E S T R E
    print("SEGUNDO SEMESTRE")
    
    # Leitura dos checkpoints
    chk1 = float(input("Digite o Checkpoint 1:"))
    chk2 = float(input("Digite o Checkpoint 2:"))
    chk3 = float(input("Digite o Checkpoint 3:"))
            
    # Verificando o Checkpoint de menor valor
    menor = chk1
    if chk2 < menor:
        menor = chk2
    if chk3 < menor:
        menor = chk3
            
    # Calculando a média dos Checkpoints
    mediaChk = (chk1 + chk2 + chk3 - menor) / 2
    
    # Leitura dos Sprints
    sprint1 = float(input("Digite o Sprint 1:"))
    sprint2 = float(input("Digite o Sprint 2:"))
           
    # Calculando a média dos Sprints
    mediaSprint = (sprint1 + sprint2) / 2
            
    # Leitura da prova semestral
    semestral = float(input("Digite prova semestral:"))
            
    # Ponderando os valores das médias
    pontosChk = mediaChk * 0.2
    pontosSprints = mediaSprint * 0.2
    pontosSemestral = semestral * 0.6
            
    # Cálculo da media do segundo semestre
    mediaSegundoSemestre = (pontosChk + pontosSprints + pontosSemestral)
            
    # Pontos obtidos no segundo semestre
    pontosSegundoSemestre = mediaSegundoSemestre * 0.6
        
            
    # Exibiçao da media do primeiro semetre
    print (f"
Média do Primeiro Semestre: {mediaPrimeiroSemestre:.1f}")
            
    # Exibiçao da media do segundo semetre
    print (f"Média do Segundo Semestre: {mediaSegundoSemestre:.1f}")
            
    # Cálculo da média final
    mediaFinal = pontosPrimeiroSemestre + pontosSegundoSemestre
    print (f"Média Final: {mediaFinal:.1f} - ", end="")
            
    if mediaFinal >= 6:
        contagemAprovados += 1
        print("Aprovado!")
    else:
        print("Não Aprovado!")
        aluno += 1
        
# Exibição da Quantidade de Alunos Aprovados
print("Quantidade de aprovados: ", contagemAprovados)
```

Simulação pós condicional Faça-Enquanto. 

Por fim mas não menor importante, vamos utilizar o laço contador for. Este laço é o mais apropriado para esta situação porque sabemos a quantidade de alunos, e consequentemente a quantidade de voltas.

```python
contagemAprovados = 0
qtdAlunos = 40
aluno = 1

# Simulação do laço Faça-enquanto
for aluno in range(0, qtdAlunos, 1):
    # P R I M E I R O   S E M E S T R E
    print(f"------------------------------- ALUNO: {aluno + 1}")
    print("PRIMEIRO SEMESTRE")
    # Leitura dos checkpoints
    chk1 = float(input("Digite o Checkpoint 1:"))
    chk2 = float(input("Digite o Checkpoint 2:"))
    chk3 = float(input("Digite o Checkpoint 3:"))
    # Verificando o Checkpoint de menor valor
    menor = chk1
    if chk2 < menor:
        menor = chk2
    if chk3 < menor:
        menor = chk3
    # Calculando a média dos Checkpoints
    mediaChk = (chk1 + chk2 + chk3 - menor) / 2
    # Leitura dos Sprints
    sprint1 = float(input("Digite o Sprint 1:"))
    sprint2 = float(input("Digite o Sprint 2:"))
    # Calculando a média dos Sprints
    mediaSprint = (sprint1 + sprint2) / 2
    # Leitura da prova semestral
    semestral = float(input("Digite prova semestral:"))
    # Ponderando os valores das médias
    pontosChk = mediaChk * 0.2
    pontosSprints = mediaSprint * 0.2
    pontosSemestral = semestral * 0.6
    # Cálculo da media do primeiro semestre
    mediaPrimeiroSemestre = (pontosChk + pontosSprints + pontosSemestral)
    # Pontos obtidos no primeiro semestre
    pontosPrimeiroSemestre = mediaPrimeiroSemestre * 0.4

    # S E G U N D O   S E M E S T R E
    print("SEGUNDO SEMESTRE")
    # Leitura dos checkpoints
    chk1 = float(input("Digite o Checkpoint 1:"))
    chk2 = float(input("Digite o Checkpoint 2:"))
    chk3 = float(input("Digite o Checkpoint 3:"))
    # Verificando o Checkpoint de menor valor
    menor = chk1
    if chk2 < menor:
        menor = chk2
    if chk3 < menor:
        menor = chk3
    # Calculando a média dos Checkpoints
    mediaChk = (chk1 + chk2 + chk3 - menor) / 2
    # Leitura dos Sprints
    sprint1 = float(input("Digite o Sprint 1:"))
    sprint2 = float(input("Digite o Sprint 2:"))
    # Calculando a média dos Sprints
    mediaSprint = (sprint1 + sprint2) / 2
    # Leitura da prova semestral
    semestral = float(input("Digite prova semestral:"))
    # Ponderando os valores das médias
    pontosChk = mediaChk * 0.2
    pontosSprints = mediaSprint * 0.2
    pontosSemestral = semestral * 0.6
    # Cálculo da media do segundo semestre
    mediaSegundoSemestre = (pontosChk + pontosSprints + pontosSemestral)
    # Pontos obtidos no segundo semestre
    pontosSegundoSemestre = mediaSegundoSemestre * 0.6

    # Exibiçao da media do primeiro semetre
    print (f"
Média do Primeiro Semestre: {mediaPrimeiroSemestre:.1f}")
    # Exibiçao da media do segundo semetre
    print (f"Média do Segundo Semestre: {mediaSegundoSemestre:.1f}")
    # Cálculo da média final
    mediaFinal = pontosPrimeiroSemestre + pontosSegundoSemestre
    print (f"Média Final: {mediaFinal:.1f} - ", end="")
    if mediaFinal >= 6:
        contagemAprovados += 1
        print("Aprovado!")
    else:
        print("Não Aprovado!")
# Exibição da Quantidade de Alunos Aprovados
print("Quantidade de aprovados: ", contagemAprovados)
```

![[FIAP/Imagens/Capitulo 9 - Estruturas avançadas de lógica-20250317211443946.webp]]












![[1ESO - Fase 3 - Cap09 - Estruturas avancadas de logica_RevFinal.pdf]]

[^1]: 
