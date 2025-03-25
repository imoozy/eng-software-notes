
# Memórias

## Bit

Você sabia que o bit (Binary digit) é a menor unidade de informação possível? Ele pode assumir apenas dois valores ou, pensando de outra forma, assume dois estados ligado ou desligado.

Se pensarmos em termos de software, falamos em estado lógico, sendo assim, podemos simbolizar os estados por 0 e 1. Agora se for pensarmos em termos de hardware, estaremos falando em estado físico, ou seja, o bit é visto com valor de tensão, sendo assim, o estado lógico 0 é associado ao valor de tensão 0 V ou até mesmo 12 V (Em alguns vasos), e o estado lógico 1 estará associado ao valor de tensão 5V ou até mesmo -12V (também em alguns casos)

Um único bit não resolve muita coisa! Contudo, vamos lá, suponhamos que desejemos criar uma representação por meio de bits para os seguintes Símbolos: **A, B, C e D**. Nossa primeira tentativa seria usar apenas um bit, porém surgiria um problema:

a= 0; b=1; c=?;e d=??

Apenas com um bit teríamos como representar apenas os símbolos A e B. É como se vivêssemos em um mundo onde as pessoas só pudessem responder "sim"(1) ou "não"(0)

Vamos tentar de outra forma:

a=00; b=01; c=10; d=11 Sucesso!

- **Byte:** O byte é definido como o grupamento de 8 bits. Da mesma maneira que uma dúzia de bananas corresponde a 12 bananas, o byte corresponde a 8bits

- **Nibble:** O nibble é definido como o grupamento de 4 bits. Tem sua importância porque é a quantidade de bits necessária para representar os símbolos dos dígitos da base 10, ou seja, na base numérica que utilizamos

- **Word:** É um padrão criado pela intel e segundo a empresa, o word é o grupamento de 16 bits. Em computação, word corresponde a uma quantidade de bits ou bytes utilizada para codificar algum elemento de informação.

> No códio ASCII, a palavra possui 8 bits ou um byte: a = 0110 0001<sub>2</sub>


> [!NOTE] explicação
> Matematicamente, uma palavra com n bits pode representar até 2<sup>n</sup>  elementos. Essa relação equivale a afirmação de que uma palavra de n bits pode ter 2<sup>n</sup> formas distintas ou ainda n bits podem ter arrumados de 2<sup>n</sup> formas diferentes.

Em arquivos de áudio do tipo .wav, o som é codificado por uma palavra de 16 bits ou 2 bytes. As cores em um arquivo de foto podem ser codificadas em palavras de até 64 bits ou 4 bytes.


# Origem dos dados

Qual é a origem das palavras nos sistemas computacionais? A palavra, que também é uma informação, pode entrar no sistema computacional de diversas formas.

## Pelo teclado

Quando pressionamos uma tecla, o teclado envia ao computador uma sequência de bits que identifica o a tecla pressionada, sem nos preocuparmos com letras maiúsculas ou minúsculas ou com sequências mais complexas que podem ocorrer.

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250226195911371.webp]]

Na figura a cima temos os seguintes dados:

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250226200001167.webp]]
![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250226200013085.webp]]

O código HEX para cada uma das teclas do teclado:

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250226200042396.webp]]

## Por uma placa de áudio:

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250226200231854.webp]]

As placas de áudio geram códigos que correspondem à intensidade do sinal (som) aplicado no microfone. Em (A) temos um microfone que ao ser estimulado pela voz de uma pessoa, produz um sinal de saida (V<sub>mic</sub>) cuja intensidade é mostrada em (b).

Na placa de áudio de um computador, este sinal é aplicado a um componente chamado conversos analógico/digital. EM intervalos de tempos iguais, a intensidade deste sinal é comparada com dois valores de referência, V<sub>ref</sub> + (5,0V) e V<sub>ref</sub> = (0V) e, a partir dessa comparação, o conversor A/D gera um byte que é enviado para a memória do computador.

Em (d) temos a relação entre alguns valores de V<sub>mic</sub> e o código gerado.

## Por uma câmera digital

Em uma câmera digital, a imagem de um objeto é captada por um sensor eletrônico e a partir dela, a imagem é fragmentada em pequenas unidades (pixels).

Depois, por meio de um conversor A/D, a cor de cada fragmento é associada a um código binário de 8 bits, Essa é apenas uma explicação inicial sobre sistemas de digitalização de imagens.

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250226200633299.webp]]

# Função

A função básica da memória é guardar informação. A informação é guardada na memória em forma de bits. 


# Endereçamento

Quando o sistema deseja salvar ou resgatas algum dado na memória, ele deve especificar o endereço onde está o dado desejado. Tal como: você mora em um endereço e se alguém desejar enviar uma encomenda para você precisará do seu endereço.

O endereçamento no computador é feito por uma variável binária de n bits, desse modo é possível especificar 2<sup>n</sup> endereços distintos. Em uma memória, os dados nela armazenados são acessados especificamente ou apontando o endereço de leitura ou escrita.

A figura a baixo apresenta memórias nas quais em (a), o endereçamento é feito com apenas um bit, com isso, podemos especificar apenas dois endereços, um quando o bit de endereçamento vale 0 e outro quando o bit de endereçamento vale 1.

Em (b) o endereçamento é feito com dois bits, assim podemos especificar quatro endereços cada um deles associados a uma combinação de valores dos bits de endereçamento. E, em (c), com 4 bits de endereçamento, podemos especificar 16 endereços.

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250226202245351.webp]]

É por isso então que há equivalência de números!

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250226202845397.webp]]
![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250226202854546.webp]]
![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250226202907974.webp]]

# Classificação das memórias

As memórias estão presentes em diversos componentes do computador, algumas permitem leitura e escrita; enquanto outras, apenas leitura. A algumas temos acesso direto e no caso de outras, não; algumas são expansíveis, isto é podemos aumentar sua quantidade mas outras não; algumas usam eletricidade para guardar os bits, outras usam dipolos magnéticos e outras ainda usam propriedades ópticas.

## Classificação das memórias segundo a tecnologia ou mídia utilizada para sua fabricação;

### Memórias semicondutoras

São memórias que utilizam componentes eletrônicos, principalmente semicondutores (diodos e transistores), para sua construção, dizemos que elas utilizam mídias semicondutoras.

Rigorosamente falando com relação a "memórias semicondutoras", nos referimos somente ao chip de memória e não ao dispositivo de armazenamento ao qual ela está associada. Nas mídias semicondutoras, o nível lógico do bit (1 ou 0) é representado pela presença ou ausência de cargas elétricas, corrente elétrica ou tensão elétrica.

Onde as memórias semicondutoras são utilizadas? Elas são encontradas em pen drivers, memória principal (RAM), bancos de memória cache e bancos de registradores (presente no interior da CPU).

### Memórias magnéticas

São memórias para as quais o nível lógico do bit é representado pela ausência ou presença de magnetismo. Memórias magnéticas estão presentes em dispositivos de armazenamento de massa como HDs e fitas DAT. 

### Memórias ópticas

São memórias em que o nível lógico do bit é representado pelo padrão de reflexão da luz. Memórias ópticas são a base dos CDs , DVDs e discos Blu-Ray.

## Classificação quanto a volatilidade

Volatilidade é uma característica das memórias que está relacionada à capacidade ou não de reter a informação quando a memória deixa de ser alimentada eletricamente (energizada). Ou seja, a informação somente é armazenada enquanto a memória é alimentada eletricamente. Quanto a volatilidade, as memórias podem ser dos seguintes tipos:

- Memórias voláteis: São aquelas que perdem seu conteúdo quando deixar de ser alimentadas.
- Memórias não voláteis: São aquelas que não perdem seu conteúdo quando deixar de ser alimentadas eletricamente.

## Classificação quanto a volatilidade, sua posição ou função em um sistema computacional

Sempre que vamos escolher ou indicar um computador, nos deparamos com informações apresentando a quantidade de memória cache presente no processador, a quantidade de memória RAM, do modelo e a quantidade de memória em disco rígido, presentes no computador desejado.
As memórias presentes no computador também podem ser classificadas seguindo a sua localização ou função em um sistema computacional:

### Registradores

São memórias localizadas somente dentro da CPU, estas memórias estão espalhadas pela eletrônica dessa unidade e estão sempre muito próximas da unidade que as utilizam, sendo assim, são as de mais rápido acesso, no entanto, de baixa capacidade de armazenamento.

São utilizadas junto aos componentes que executam as instruções (ULA - Unidade Lógica Aritmética) ou armazenam as informações do status do processamento. São conhecidas também como memórias de rascunho.

Mas tal como a memória RAM, posso escolher a sua capacidade e modelo? De certo modo sim, mas essa escolha está sempre atrelada ao próprio processador escolhido, pois elas fazem parte dele. São sempre memórias semicondutoras e voláteis.

### Memória cache

Também são memórias encontradas somente dentro dos processadores e são organizadas em bancos. O primeiro banco de memória é a memória cache L1. Ela é a mais rápida de todas, pois opera na mesma frequência do processador, ou seja é muito rápida, os outros bancos de memória cache operam em frequências inferiores, mas mesmo assim são muito rápidas e possuem baixo tempo de latência. Estas memórias também são semicondutoras e voláteis. 

A memória cache destina-se a guardar os dados que serão imediatamente utilizados pelo processador ou os dados que acabaram de ser tratados e devem ser enviados para a memória principal (RAM). Na prática sua função é a mesma da memória principal.

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250227095157577.webp]]

A memória cache é importante para usuários que mantêm muitos programas de baixo custo computacional, ou seja, que usam pouco processamento, abertos ao mesmo tempo, por exemplo, vários arquivos de Word, Excel, etc.

### Memória principal

Também chamadas, erroneamente de RAM. Trata-se de uma memória de acesso rápido, utilizada com o objetivo de guardar os processos (programas e dados) que estão sendo executados pelo processador ou que acabaram de ser utilizados pelo processador. Estas memórias são semicondutoras e voláteis.

Na hora de aumentar a quantidade de memória principal, o especialista deve saber que o tipo dessa memória o computador suporta. Na atualidade, a maioria dos bons computadores utiliza as memórias principais do tipo DDR5.

Computadores ainda em ampla utilização podem aceitar somente memórias do tipo DDR4 ou até mesmo DDR3. Mesmo que a máquina a ser melhorada já disponha de memória do tipo DDR5, você ainda pode utilizar a memória por um modelo de clock mais rápido, sempre observando se a memória desejada é compatível com a placa-mãe.

Memórias de servidores ou workstations podem dispor de um recurso chamado ECC (Error Correction Code - Código de Correção de Erros), que permitem a recuperação de dados que se corrompem durante sua manipulação. Isso evita a necessidade de reenvio de dados corrompidos e até mesmo o risco de processamento de dados errados.

Outra característica que podemos observar quando especificar uma memória principal, é a presença de buffer no módulo da memória. Quando as memórias possuem buffer, dizemos que elas são do tipo registradas.

O buffer faz com que a memória trabalhe com menos corrente no barramento de dados, isto por sua vez faz com que mais módulos de memórias possam ser instalados na mesma máquina.

Vamos entender o que é RAM! Ram vem de Random Access Memory, memórias deste tipo levam o mesmo tempo para acessar o dado, esteja ele no endereço em que estiver.

Em um computador há na verdade várias memórias que podemos denominar como RAM, além de memória principal, assim RAM refere-se a apenas uma das muitas características das memórias principais. 

E quanto de memória principal preciso em um computador?

Depende da aplicação do seu computador. Se você executa jogos "Pesado", se você executa programas que efetuam grande quantidade de contar com volume elevado de dados (valores), se você mantém muitas abas do navegador abertas etc, a quantidade é de pelo menos 16gb. Mas existem capacidades maiores, como: 32GB, 64GB ou até capacidades ainda maiores. (Computadores de uso específico para servidores.)

Sabemos que a função dessa memória, no caso a memória principal é armazenar dados e programas que estão sendo usados pelo computador ou que foram usados há pouco tempo. Um computador poderia até funcionar sem memória RAM, porém os dados da memória RAM acabariam ficando nas memórias de armazenamento em massa e como a velocidade dessas memórias é relativamente baixa, o desempenho do computador seria tão ruim que tornaria praticamente inviável sua utilização.

### Definição de quantidade de memória RAM

Na memória RAM, ficam armazenados os dados e programas que estão sendo usados pelo computador ou que acabaram de ser usados há pouco tempo. Eles permanecem na memória RAM, pois é muito como, logo que fechamos um programa, resolvermos abri-lo novamente, assim, se eles ainda estiverem lá, o processo de abertura fica muito mais rápido. O sistema operacional administra o tempo em que os programas permanecem na RAM após serem fechados.

O que define quanto precisamos de memória RAM? São os programas que executamos no computador e a maneira como os executamos.

Um computador para uma pessoa que não abre muitos programas ao mesmo tempo e além disso utiliza programas relativamente pequenos irá exigir pouca memória RAM, apenas 4GB de memória atendem as necessidades desse usuário.

Já um usuário que frequentemente possui mais do que cinco abas do navegador abertas, faz pesquisa para compra de produtos, possui um ou dois mais documentos do WORD abertos e possui ainda uma ferramenta de comunicação como por exemplo, o WPP.
Um funcionário como esse deve ter uma máquina com pelo menos 8GB de RAM. Se o computador será usado pela equipe de desenvolvimento de software ou por uma equipe de design que trabalha com imagens e vídeos, talvez 8GB não sejam suficientes.

### Escolha do tipo de memória RAM

Até pouco tempo, para montarmos uma máquina, deveríamos escolher entre usar uma memória RAM DDR3 ou DDR4. Hoje não faz mais sentido comprar uma máquina com DDR3, pois já não temos tantas placa-mãe de qualidade boa ou mediana que usam essas memórias e além disso as memórias DDR5 já chegaram ao mercado e logo se tornarão o padrão do mercado, sendo o tipo de memória mais comercializado.

### Diferenças entre as memórias DDR4

- **Frequência de clock**

As memórias DDR5 podem diferir umas das outras com relação a vários aspectos. Consideremos o principal, a saber: a frequência de operação. A memória RAM troca dados com o sistema comandada por sinal de clock.

Um sinal de clock. 6 é um sinal de tensão que oscila entre dois valores, sendo um deles 0V e o outro definido pela placa-mãe, podendo inclusive ser modificado em algumas placa-mãe.

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250227112046801.webp]]

> [!NOTE] Explicação
> Observer as mudanças de níveis lógicos: em 1 segundo, 3 oscilações completas ocorrem, ou, de forma, o sial se repete 3 vezes; dizemos então que a frequência deste sinal é de 3hz.

Quanto maior o número de oscilações por segundo do sinal de clock, maior será a velocidade da memória RAM. O número de oscilações é medido em Hertz (Hz), no caso do sinal da Figura apresentada temos 3 oscilações em 1 segundo e a frequência do sinal é de 3Hz.

As memórias DDR operam com sinais de clock que vão de 1.866 até 5.266MHZ, ou seja, de 1.866.000.000 oscilações por segundo até 5.266.000.000 oscilações por segundo.

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250227112438564.webp]]

- **Capacidade do pente**
As memórias principais são construídas pela montagem de chips em um módulo chamado de pente. A tecnologia DDR4 possui um limite de capacidade em seus chips, de modo que um pente de memória RAM pode ter no máximo 16GB de espaço.



# Pirâmide hierárquica de memória

A piramide hierárquica de memória mostra a relação entre vários tipos de memória. Tais memórias são categorizadas entre si pela comparação de suas características. De acordo com a pirâmide, quanto mais ao topo, maior seu custo por Byte, maior sua velocidade e menor sua quantidade disponível no computador

![[FIAP/Imagens/Capitulo 3 - Mais um pouco de hardware-20250227112924603.webp]]

A Intel lançou um novo tipo de memória chamada Optane. Para que o usuário possa desfrutar dessa memória, a placa-mãe deve ser compatível. Trata-se de uma memória semicondutora, não volátil e baseada na tecnologia 3D Xpoint, o que torna sua velocidade superior a das memórias do tipo NAND flash presente nos SSDs.

Essa memória fica entre o HD e a memória principal, e sua função é guardar os programas e os dados mais utilizados pelo usuário, com isso, o acesso a esses dados, utilizados com maior frequência, torna-se mais rápido.

# Módulos de entrada e Saída (E/S)

Além da CPU e do conjunto de módulos de memória, um terceiro elemento de grande importância em um sistema de computação é o conjunto de módulos de E/S. Cada módulo de conecta ao barramento do sistema ou computador central e controla um ou mais dispositivos periféricos.

# Modulo (E/S)

%% É muito comum ver outras pessoas chamarem o módulo E/S de I/O, pois este é o termo em inglês, Input/Output, para E/S. Em algumas placas também vemos o termo GPIO (General Purpose Input/Output), que é a mesma coisa %%

Nos computadores atuais um módulo E/S é por exemplo um slot PCI Express, o que inclui desde o slot propriamente dito, as trilhas que o conectam ao Chipset e o próprio Chipset. Um dispositivo periférico conectado a um módulo de E/S pode ser uma placa de vídeo, uma placa de expansão para USB, etc.

# Largura de banda

A largura de banda ou em inglês "Bandwidth" é a medida de transmissão de um certo meio, conexão ou rede, determinando a velocidade em que os dados passam por meio dessa rede específica. Ela é medida em bits, e não em Bytes.

Todas as medidas de largura de banda são basicamente feitas  em bits por segundo.

Dito isso, um módulo de E/S não é simplesmente um conjunto de conectores mecânicos que ligam um dispositivo fisicamente ao barramento do sistema, mais do que isso, o módulo de E/S contém uma lógica para realizar uma função de comunicação entre o periférico e o barramento.

Os sistemas de E/S podem ser divididos em dois componentes: os próprios dispositivos de E/S e os barramentos.

Para mais:
![[1ESO - Fase 3 - Cap03 - Mais um pouco de hardware.docx_RevFinal.pdf]]


