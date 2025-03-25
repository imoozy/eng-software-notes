
# Introdução

O Bootstrap é um framework bastante utilizado atualmente, ele é sim um dos principais frameworks CSS para a construção do front-end de aplicações web.

introdução ao Bootstrap: https://getbootstrap.com/docs/5.0/getting-started/introduction/

Por que o Bootstrap é um framework muito utilizado? Simples, por meio desse framework podemos deixar nosso projeto com um visual profissional, customizar elementos como tamanho, cores, fontes ou seja, deixar o site realmente da maneira como o cliente gostaria que fosse.

# Bootstrap 5 vs Bootstrap 3 e 4

Bootstrap 5 é a versão mais recente desse framework; nessa versão foram criados novos componentes, folhas de estilo mais eficazes e com mais capacidade de resposta.

Além dos novos recursos, o Bootstrap 5 suporta as versões mais recentes e estáveis de todos os principais navegadores e plataformas. Só há um ponto a ser observado: O internet Explorer 11 e as versões anteriores desse navegador não são mais suportadas.

As principais diferenças entre o Bootstrap 5 e o 3, 4 é que o 5 utiliza JS em vez de JQuery

# O que é Bootstrap?

Bootstrap é um framework front-end gratuito, para desenvolvimento web mais rápido, fácil e podemos dizer também que é simples de usar.

O Bootstrap inclui modelos de design baseado em HTML e CSS para tipografia, formulários, botões, tabelas, navegação, modais, carrosséis de imagens e muitos outros, bem como plug-in JS opcionais.

O Bootstrap também oferece a capacidade de criar facilmente designs responsivos.

# O que é web design responsivo?

Você sabe o que é web design responsivo? Bom, um web design responsivo diz respeito à criação de sites que se ajustam automaticamente para ter uma boa aparência em quaisquer dispositivos, desde pequenos smartphones até grandes desktops.

EX:
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap 5 Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
<div class="container-fluid p-5 bg-primary text-white text-center">
  <h1>My First Bootstrap Page</h1>
  <p>Resize this responsive page to see the effect!</p> 
</div>
  
<div class="container mt-5">
  <div class="row">
    <div class="col-sm-4">
      <h3>Column 1</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
      <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...</p>
    </div>
    <div class="col-sm-4">
      <h3>Column 2</h3>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
      <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...</p>
    </div>
    <div class="col-sm-4">
      <h3>Column 3</h3>        
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit...</p>
      <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris...</p>
    </div>
  </div>
</div>
</body>
</html>
```

- O Bootstrap adiciona elementos HTML e propriedades CSS que requerem o DOCTYPE HTML 5.
- Sempre inclua o tipo do documento HTML5 no início da página, junto com o atributo lang e o titulo e conjunto de caracteres incorretos.
- ![[Capitulo 2 - Front-end design e mais-20250224154135404.webp]]
- ![[Capitulo 2 - Front-end design e mais-20250224154147340.webp]]

# Containers

Como explicado a cima, O Bootstrap requer um elemento de contenção para encapsular o conteúdo do site, pois bem, os containers são usados para preencher o conteúdo dentro deles. Podemos realizar isso de duas maneiras:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.bundle.min.js" integrity="sha384-MrcW6ZMFYlzcLA8Nl+NtUVF0sA7MsXsP1UyJoMp4YLEuNSfAP+JcXn/tWtIaxVXM" crossorigin="anonymous"></script>
</head>
<body>
    <div class="container-sm"></div>
    <div class="conteiner-md"></div>
    <div class="container-lg"></div>
    <div class="container-xl"></div>
    <div class="container-xll"></div>
    <div class="container-fluid"></div>
</body>
</html>
```

1. A classe .container fornece um contêiner de largura fixa responsivo.
2. A classe .container-fluid fornece um contêiner de largura total, abrangendo toda a largura da janela de visualização.
## Container fixo 

A classe .container é utilizada para criar um contêiner responsivo de largura fixa.

Observe que sua largura (max-width) mudará em diferentes tamanhos da tela:

![[Capitulo 2 - Front-end design e mais-20250224161650040.webp]]

## Borda e cor do contêiner

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="    https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
    <div class="conteiner border">
        <h1>título</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis architecto repellat enim ex ipsam. Quas.</p>
    </div>

    <div class="conteiner border bg-dark text-white">
        <h1>título</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officiis architecto repellat enim ex ipsam. Quas.</p>
    </div>
</body>
</html>
```

## Contêiner Responsivo

Para criar um layout responsivo, podemos usar as classes .container-sm/md/lg/xl para determinar quando o contêiner deve ser responsivo.

O conteúdo do max-width mudará em diferentes tamanhos de tela de visualização, dessa forma o que determinará a responsividade será a combinação dos elementos a cima.

![[Capitulo 2 - Front-end design e mais-20250224202424332.webp]]

# Bootstrap grid system

## Contêiner responsivo e grid system

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="    https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
    <div class="conteiner-fluid">
        <div class="conteiner">
            <div class="row">
                <div class="col-sm-3 border">ta foda</div>
                <div class="col-sm-3 border">ta foda</div>
                <div class="col-sm-3 border">ta foda</div>
                <div class="col-sm-3 border">ta foda</div>
            </div>
    </div>
    <br>
    <div class="conteiner-sm">
        <div class="row">
            <div class="col-md-6 border">ta foda</div>
            <div class="col-md-6 border">ta foda</div>
        </div>
        <div class="row">
            <div class="col-md-4 border">ta foda</div>
            <div class="col-md-4 border">ta foda</div>
            <div class="col-md-4 border">ta foda</div>
        </div>
        <div class="row">
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
            <div class="col-md-1 border">ta foda</div>
        </div>
    </div>
</body>
</html>
```

# Classes de GRID

O sistema de grid do Bootstrap tem seis classes:

![[Capitulo 2 - Front-end design e mais-20250224203627915.webp]]

# Estrutura básica de um grid

```html
<!-- Controle a largura das colunas e como elas devem aparecer em diferentes dispositivos -->
<div class="row">
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
</div>
<div class="row">
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
</div>
<!-- deixe o Bootstrap lidar automaticamente com o layout -->
<div class="row">
  <div class="col"></div>
  <div class="col"></div>
  <div class="col"></div>
</div>
```

Primeiro exemplo: crie uma linha (div class="row"), em seguida adicione o número desejado de colunas (tags com .col). O primeiro asterisco representa a capacidade de resposta: sm, md, lg, xl ou xxl, enquanto o segundo asterisco representa um número, que deve somar 12 para cada linha.

Segundo exemplo: em vez de adicionar um número a cada col, deixe o Bootstrap manipular o layout para criar colunas de largura igual: dois "col" elementos = 50% de largura para cada coluna, enquanto três colunas = 33,33% de largura para cada coluna. Quatro colunas = 25% de largura etc. Você também pode usar .col para tornar as colunas responsivas.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap FIAP</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
  
<div class="container-fluid">
  <h1>Três colunas iguais</h1>
  <div class="row">
    <div class="col bg-primary text-white">.col</div>
    <div class="col bg-dark text-white">.col</div>
    <div class="col bg-primary text-white">.col</div>
  </div>
  <h1>Colunas Responsivas</h1>
  <p>As colunas serão empilhadas automaticamente umas sobre as outras quando a tela tiver menos de 576 pixels de largura</p>
  <div class="row">
    <div class="col-sm-3 bg-primary text-white">.col</div>
    <div class="col-sm-3 bg-dark text-white">.col</div>
    <div class="col-sm-3 bg-primary text-white">.col</div>
    <div class="col-sm-3 bg-dark text-white">.col</div>
  </div>
  <h1>Duas colunas responsivas de tamanhos diferentes</h1>
  <p>As colunas serão empilhadas automaticamente umas sobre as outras quando a tela tiver menos de 576 pixels de largura</p>
  <div class="row">
    <div class="col-sm-4 bg-primary text-white">.col</div>
    <div class="col-sm-8 bg-dark text-white">.col</div>
  </div>
</div>
</body>
</html>
```

# Cores do texto

O Bootstrap 5 tem algumas classes contextuais que podem ser usadas para fornecer "significado por meio das cores".

As classes para cores de texto são:
  
As classes para cores de fundo são: .bg-primary, .bg-success, .bg-info, .bg-warning, .bg-danger, .bg-secondary, .bg-dark e .bg-light.

veja como seria a aplicação desses elementos no código-fonte:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap FIAP</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
<div class="container">
  <h2>Padrões de cores</h2>
  <p>Contextualize as frase por meio das cores:</p>
  <p class="text-muted">O texto é opaco.</p>
  <p class="text-primary">O texto é importante.</p>
  <p class="text-success">O texto indica sucesso.</p>
  <p class="text-info">O texto representa alguma informação.</p>
  <p class="text-warning">O texto representa um aviso.</p>
  <p class="text-danger">O texto representa um perigo.</p>
  <p class="text-secondary">Texto secundário.</p>
  <p class="text-dark">O texto é cinza escuro.</p>
  <p class="text-body">Cor padrão do body.</p>
  <p class="text-light">O texto é cinza claro.</p>
  <p class="text-white">O texto é branco.</p>
</div>
</body>
</html>
```

Observe que as cores e fundo não definem a cor do texto, portanto, em alguns casos, você desejará usá-las junto com uma text classe de cores.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap FIAP</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
<div class="container mt-3">
  <h2>Cores de background</h2>
  <p>Observe que você também pode adicionar uma classe .text-* se desejar uma cor de texto diferente:</p>
  <p class="bg-primary text-white">O fundo é importante.</p>
  <p class="bg-success text-white">O fundo indica sucesso.</p>
  <p class="bg-info text-white">O fundo representa alguma informação.</p>
  <p class="bg-warning text-white">O fundo representa um aviso.</p>
  <p class="bg-danger text-white">O fundo representa um perigo.</p>
  <p class="bg-secondary text-white">Fundo secundário.</p>
  <p class="bg-dark text-white">Fundo é cinza escuro.</p>
  <p class="bg-light text-dark">O fundo é cinza claro.</p>
</div>
</body>
</html>
```

## tabela básica

Como utilizar então o framework para customizar as tabelas:

![[Capitulo 2 - Front-end design e mais-20250224204613439.webp]]

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap FIAP</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
    <div class="container">
        <table class="table">
            <thead>
                <th>Nome</th>
                <th>Sobrenome</th>
                <th>Email</th>
            </thead>
            <tbody>
                <tr>
                    <td>Lucas</td>
                    <td>Magalhães</td>
                    <td>lucal7421@gmail.com</td>
                </tr>
                <tr>
                    <td>Laura</td>
                    <td>Suikuni</td>
                    <td>lucal7421@gmail.com</td>
                </tr>
                <tr>
                    <td>Lucas</td>
                    <td>Magalhães</td>
                    <td>lucal7421@gmail.com</td>
                </tr>
            </tbody>
        </table>

        <table class="table table-striped">
            <thead>
                <th>Nome</th>
                <th>Sobrenome</th>
                <th>Email</th>
            </thead>
            <tbody>
                <tr>
                    <td>Lucas</td>
                    <td>Magalhães</td>
                    <td>lucal7421@gmail.com</td>
                </tr>
                <tr>
                    <td>Laura</td>
                    <td>Suikuni</td>
                    <td>lucal7421@gmail.com</td>
                </tr>
                <tr>
                    <td>Lucas</td>
                    <td>Magalhães</td>
                    <td>lucal7421@gmail.com</td>
                </tr>
            </tbody>
        </table>
    </div>
</body>
</html>
```


# Formas de imagem

Bootstrap possui algumas classes que nos auxiliam na formatação de elmentos do tipo imagem, são classes que podem utilizar para aplicar efeitos de arredondamento, estilo polaroid etc.:

![[Capitulo 2 - Front-end design e mais-20250224214617280.webp]]

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap FIAP</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
    <div class="container"><!--mostra como jogar nas extremidades-->
        <div class="row">
            <div class="col-md-6 border">
                <h1>Imagem 142</h1>
                <img src="150926165742__85730600_monkey2.jpg.webp" alt="macaco sorrindo para camera" class="float-start">    
            </div>
            <div class="col-md-6 border">
                <h1>Imagem 143</h1>
                <img src="150926165742__85730600_monkey2.jpg.webp" alt="macaco sorrindo para camera" class="foat-end">    
            </div>
        </div>
    </div>  

    <div class="container"><!--mostra como centraliza-->
        <div class="row">
            <div class="col-md-6">
                <h1>Imagem 132</h1>
                <img src="150926165742__85730600_monkey2.jpg.webp" alt="macaco sorrindo para camera" class="mx-auto">    
            </div>
            <div class="col-md-6">
                <h1>Imagem 133</h1>
                <img src="150926165742__85730600_monkey2.jpg.webp" alt="macaco sorrindo para camera">    
            </div>
        </div>
    </div>

    <div class="container"> <!--Essa parte do código mostra as bordas das imagens-->
        <div class="row">
            <div class="col-sm-12">
                <h1>Imagem 1</h1>
                <img src="150926165742__85730600_monkey2.jpg.webp" alt="macaco sorrindo para camera" class="rounded border">
            </div>
            <div class="col-sm-6">
                <h1>Imagem 1</h1>
                <img src="150926165742__85730600_monkey2.jpg.webp" alt="macaco sorrindo para camera" class="border">
            </div>
        </div>
        <div class="row">
            <div class="col-sm-12">
                <h1>Imagem 2</h1>
                <img src="150926165742__85730600_monkey2.jpg.webp" alt="macaco sorrindo para camera" class="rounded-circle">
            </div>
        </div>
    </div>
</body>
</html>
```

## Imagem centralizada 

Para centralizar uma imagem, podemos adicionar as classes mx-auto (margin:auto) e d-block (display:block) a imagem

## Alertas

O Bootstrap 5 fornece uma maneira fácil de criar mensagens que servem como aviso ou alertas predefinidos no framework

Os alertas são criados com a classe .alert, seguidos pelo informativo a baixo:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
<div class="container">
  <h2>Alerts</h2>
  <div class="alert alert-success">
    <strong>Sucesso!</strong> Esta caixa de alerta pode indicar uma ação bem-sucedida ou positiva.
  </div>
  <div class="alert alert-info">
    <strong>Informação!</strong> Esta caixa de alerta pode indicar uma mudança ou ação informativa neutra.
  </div>
  <div class="alert alert-warning">
    <strong>Aviso!</strong> Esta caixa de alerta pode indicar um aviso que pode precisar de atenção.
  </div>
  <div class="alert alert-danger">
    <strong>Perigo!</strong> Esta caixa de alerta pode indicar uma ação perigosa ou potencialmente negativa.
  </div>
  <div class="alert alert-primary">
    <strong>Primário!</strong> Indica uma ação importante.
  </div>
  <div class="alert alert-secondary">
    <strong>Secundário!</strong>  Indica uma ação um pouco menos importante.
  </div>
  <div class="alert alert-dark">
    <strong>Escuro!</strong> Alerta cinza escuro.
  </div>
  <div class="alert alert-light">
    <strong>Leve!</strong> Alerta cinza claro.
  </div>
</div>
</body>
</html>
```

