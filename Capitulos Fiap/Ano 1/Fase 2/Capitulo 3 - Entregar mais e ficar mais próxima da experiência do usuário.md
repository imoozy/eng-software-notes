
# Criando uma tabela

## Tag table

Para criarmos nossas tabelas em HTML, usamos a tag table. É dentro dela que deve ficar todo o conteúdo que formará a tabela.

```html
<table>
   Conteúdo da tabela…
   Conteúdo da tabela…
   Conteúdo da tabela…
</table>
```

## Tag caption

A tag caption insere um título na tabela. Esse título poderá ser usado para identificar o conjunto de dados que a tabela representa. Pensando na usabilidade, empregue sempre essa tag após a abertura da table.

```html
<table>
   <caption> Título da tabela</caption>
   Conteúdo da tabela…
   Conteúdo da tabela…
   Conteúdo da tabela…
</table>
```

## Tag TR

Utilizada para a criação das linhas que existirão na tabela. Dentro de cada linha, teremos as respectivas colunas com seus conteúdos. A sigla tr significa "Table row"

```html
<table>
   <caption> Título da tabela </caption>
   <tr> Linha da tabela… </tr>
   <tr> Linha da tabela… </tr>
   <tr> Linha da tabela… </tr>
</table>
```

## Tag TD

Utilizada para a criação das colunas na tabela. Elas devem ficar dentro da tag tr para possibilitar a exibição dos dados. É dentro da td que as informações devem ser inseridas. A sigla td significa "Table data".

```html
<table>
   <caption> Título da tabela </caption>
   <tr>
      <td> dado da tabela </td>
      <td> dado da tabela </td>
      <td> dado da tabela </td> 
   </tr>
</table>
```

## Tag TH

A primeira linha de dados da tabela é considerada uma das mais importantes porque nela são definidos os nomes das colunas, dessa forma, o usuário identificará o conjunto de informações que está armazenado em cada uma dela. Para isso podemos substituir a tag ***td*** pela tag ***th*** , a diferença visual é que ele deixará o nome da coluna centralizado e com estilo negrito. Mas a principal diferença será a acessibilidade: para pessoas com leitores de tela, ele informará o que significa cada uma das colunas.

```html
<table>
   <caption> Título da tabela </caption>
   <tr>
      <th> Nome para a coluna </th>
      <th> Nome para a coluna </th>
      <th> Nome para a coluna </th> 
   </tr>
</table>
```

## ELEMENTOS NA TABELA

Você poderá dividir o conteúdo da sua tabela em cabeçalho, corpo e rodapé. Eles não são obrigatórios, mas poderão ajudar a agrupar os dados existentes na tabela de uma forma mais organizada e ajudar na hora da formatação com o CSS. para fazer essa divisão, você deve usar as tags: **thead, tbody e tfoot**.

## TAG THEAD

Após o uso da tag **caption**, podemos criar o que chamamos de cabeçalho na tabela utilizando a tag **thead**. Ele servirá para identificar a primeira linha da tabela, aquela que provavelmente terá os nomes de cada coluna de dados. Em tabelas muito grandes e que forem impressas, essa linha sempre será repetida no inicio de uma nova página impressa, facilitando assim a identificação dos dados ali exibidos.


```html
<table>
   <caption> Lista de Drones da Chulamis </caption>
   <thead>
      <tr>
         <th> Nome do Drone </th>
         <th> Tipo </th>
         <th> Qualidade Vídeo </th>
         <th> Valor </th> 
      </tr>
   </thead>
</table>
```

## TAG TBODY

Podemos inserir todas as linhas e colunas de dados em elementos ***tbody***, o corpo da tabela. A ideia é a organização dos dados agrupando-os em uma área específica da tabela.

```html
<tbody>
   <tr>
      <td>DJI Mini 3 Pro </td>
      <td>Drone de profissional</td>
      <td>Vídeos em HDR em 4K </td>
      <td>R$ 10.899,00 </td>
   </tr>
   <tr>
      <td>DJI Mini 3 PRO </td>
      <td> Drone semi-profissional </td>
      <td>Vídeos em HDR em 3K </td>
      <td>R$ 5.000,00</td>
   </tr>
</tbody>
```

## TAG TFOOT

A tag **tfoot** representará a linha de rodapé da sua tabela. Seu uso é totalmente opcional e muitas vezes você encontrará tabelas sem esse elemento.
Na maioria das vezes, usamos o tfoot como uma linha para alguma observação sobre os dados: um comentário, marca de rodapé, algo nesse sentido.
A documentação oficial especifica que a tag tfoot deverá ser inserida em nosso código logo após a tag thead, abaixo dela deverá vir a tag tbody com seu conteúdo. Pode parecer estranho, mas o navegador conseguirá fazer a renderização da forma correta.

```html
<tfoot>
   <tr>
      <td> Dados atualizados em Agosto/2022 </td>
   </tr>
</tfoot>
```

## MESCLANDO LINHAS E COLUNAS

As vezes, precisamos juntar linhas ou colunas em uma tabela, para isso podemos usar os atributos colspan e rowspan

## Atributo COLSPAN 

O atributo colspan define o número de colunas que devem ser mescladas. Imagine que temos uma linha **TR** com quatro colunas e que desejamos que o conteúdo fique em uma única coluna, para isso basta inserir na primeira **TD** dessa linha o atributo **COLSPAN** com o número de colunas que desejamos mesclar.

```html
<tfoot>
   <tr>
      <td colspan="4">Dados atualizados em Agosto/2020</td>
   </tr>
</tfoot>
```

![[Capitulo 3 - Entregar mais e ficar mais próxima da experiência do usuário-20250206161500557.webp]]

## Atributo ROWSPAN

O atributo rowspan define o número de linhas que devem ser mescladas. Imagine que você quer uma coluna com apenas um valor para todas as três linhas de uma tabela. Basta inserir na primeira **TD** dessa linha o atributo rowspan com o número de linhas que deseja mesclar, nesse caso 3.
```html
<tr>
   <td rowspan="3">Vídeos em HDR</td>
</tr>
```
![[Capitulo 3 - Entregar mais e ficar mais próxima da experiência do usuário-20250206162909224.webp]]


# Estilizando a tabela

```html
<table border="1">
    <caption> Lista de Drones da Chulamis </caption>
    <thead>
        <tr>
            <th> Nome do Drone </th>
            <th> Tipo </th>
            <th> Qualidade Vídeo </th>
            <th> Valor </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>DJI Mini 3 Pro </td>
            <td>Drone de profissional</td>
            <td rowspan="3">Vídeos em HDR</td>
            <td>R$ 10.899,00 </td>
        </tr>
        <tr>
            <td>DJI Mini 2 </td>
            <td> Drone semi-profissional </td>
            <td>R$ 5.000,00</td>
        </tr>
        <tr>
            <td>DJI Drone Mini SE Fly </td>
            <td>O compacto, porém poderoso </td>
            <td>R$ 4.500,00</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="4"> Dados atualizados em Agosto/2022 </td>
        </tr>
    </tfoot>
</table>
```

```css
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@300&amp;family=Open+Sans+Condensed:wght@300&amp;display=swap');
html {
   font-family: 'Lato', sans-serif;
}

table {    
   margin: 10px auto;
   font-size: 18px;
   width: 800px;
   border-collapse: collapse;
}

caption {
   font-size: 30px;
   color: rgb(42, 98, 172);
   text-align: center;
   font-weight: 900;
   margin-bottom: 10px;
}

thead tr {
   background: rgb(42, 98, 172);
   color: #fff;
   text-align: left;
}

th, td {
   padding: 15px;
   box-sizing: border-box;
}

tbody tr {
   border-bottom: 1px solid #ccc;
}

tbody tr:nth-child(even) {
   background: #f9f9f9;
}

tbody tr:last-child {
   border-bottom: 20px solid rgb(42, 98, 172);
}

tbody tr:hover {
   font-weight: 900;
   color: rgb(42, 98, 172);
   cursor: pointer;
}

tfoot {
   text-align: center;
   font-size: 13px;
   font-weight: 900;
}
```

Vamos entender o que está acontecendo nesse css estilizado

* Aqui eu não entendi então esta a explicação.

Foi usado pseudoclasse para as linhas de dados pares, tbody tr:nth-child(even), nesse caso, elas devem ficar com cor de fundo f9f9f9. As pseudoclasses permitem aplicar formatações a algumas condições de um elemento, veremos mais sobres elas em breve. Esse efeito aplicado as linhas pares deixara a tabela como se estivesse zebrada, facilitando a leitura para o usuário.

A ultima linha do tbody também recebeu  tr:last-child, nesse caso, teremos uma borda inferior em 20px, estilo sólida na cor rgb.
![[Capitulo 3 - Entregar mais e ficar mais próxima da experiência do usuário-20250206165737124.webp]]