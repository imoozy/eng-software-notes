
Sabemos que o Bootstrap é um framework CSS para construção do front-end de aplicações web e que utiliza um sistema de grid responsivo, esse sistema permite desenvolver com grande facilidade páginas que se adaptam aos diferentes tamanhos de tela.

Exemplo de código utilizando Bootstrap:

```html
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


Para desenvolver este exemplo, iremos utilizar o código que está disponível na CDN (Content Delivery Network), onde o jsDelivr fornece suporte a CDN para CSS e JS do Bootstrap

```html
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
```


# Formulários


Os formulários são um meio muito utilizado de enviar informações, existem várias formas de disponibilizarmos os dados e os diferentes tipos de campo. Agora, vamos então demonstrar como construir um formulário e utilizar seus componentes.

```html
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
    <form>
        <!--Label de entrada para email do usuário-->
        <div class="mb-3">
            <label for="idEmail" class="form-label">Email:</label>
            <input type="email" class="form-control" id="idEmail">
        </div>
        <!--Label de entrada para senha do usuário-->
        <div class="mb-3">
            <label for="idPassword" class="form-label">Senha:</label>
            <input type="password" class="form-control" id="idPassword">
        </div>
        <!--botão de entrada para envio das labels-->
        <button type="submit" class="btn btn-primary">Enviar</button>
    </form>
</body>
</html>
```

## Visão geral

Os controles de formulários do Bootstrap melhoraram os vários elementos existentes.

fieldset = Não possuem bordar, preenchimentos ou margens para que possam ser facilmente usados como wrappers para entradas individuais ou grupos de entradas.

legend = como fieldset, também foram modificados para serem exibidos como um tipo de cabeçalho.

label = são definidos para display: inline-block permitir margin na aplicação.

![[FIAP/Imagens/Capitulo 2 - Um pouco mais de Bootstrap-20250318142341633.webp]]
![[FIAP/Imagens/Capitulo 2 - Um pouco mais de Bootstrap-20250318142354366.webp]]
![[FIAP/Imagens/Capitulo 2 - Um pouco mais de Bootstrap-20250318142403691.webp]]

Certifique-se de usar um atributo apropriado em todas as entradas a fim de aproveitar os controles de entrada mas recentes, como verificação de e-mail, seleção de número e muito mais.


exemplo:

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Formulário Básico</title>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
        <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
      </head>
<body>
    <form>
        <div class="mb-3">
          <label for="idEmail" class="form-label">Email</label>
          <input type="email" class="form-control" id="idEmail" aria-describedby="emailHelp">
          <div id="emailHelp" class="form-text">Preencha corretamente o campo email</div>
        </div>
        <div class="mb-3">
          <label for="idPassword" class="form-label">Senha</label>
          <input type="password" class="form-control" id="idPassword">
        </div>
        <button type="submit" class="btn btn-primary">Enviar</button>
      </form>    
</body>
</html>
```



# Notação

Utilitários de espaçamento que se aplicam a todos os breakpoints, não possuem abreviações. Isso acontece porque essas classes são usadas de min-width: 0 para cima, sem media queries limitantes. No entanto, os demais utilitários possuem abreviações de breakpoint.

As classes são definidas usando o formato {propriedade}{lados}--{tamanho} para o breakpoint xs e propriedade}{lados}-{breakpoint}-{tamanho} para sm, md, lg e xl

o campo propriedade pode ser 

- m - para usar margin;
- p  - para usar padding.


## Botões

Os botões têm um papel relativamente relevante dentro de um form; por meio deles podemos enviar  dados para outra página, porém aqui veremos como podemos utilizar as classes para mudar o visual desse componente.

```html
<button type="button" class="btn">Básico</button>
<button type="button" class="btn btn-primary">Primário</button>
<button type="button" class="btn btn-secondary">Secundário</button>
<button type="button" class="btn btn-success">Sucesso</button>
<button type="button" class="btn btn-info">Informativo</button>
<button type="button" class="btn btn-warning">Alerta</button>
<button type="button" class="btn btn-danger">Atenção</button>
<button type="button" class="btn btn-dark">Escurso</button>
<button type="button" class="btn btn-light">Claro</button>
<button type="button" class="btn btn-link">Link</button>
```

![[FIAP/Imagens/Capitulo 2 - Um pouco mais de Bootstrap-20250319151001682.webp]]


## Formulário empilhado

Todos os elementos textuais input e textarea com classe .form-control obtém um estilo de forma adequado:

```html
<form action="">
    <div class="mb-3 mt-3">
      <label for="email">Email:</label>
      <input type="email" class="form-control" id="email" placeholder="Digite o email" name="email">
    </div>
    <div class="mb-3">
      <label for="pwd">Password:</label>
      <input type="password" class="form-control" id="pwd" placeholder="Digite a senha" name="pswd">
    </div>
    <div class="form-check mb-3">
      <label class="form-check-label">
        <input class="form-check-input" type="checkbox" name="remember"> Armazenar informação
      </label>
    </div>
    <button type="submit" class="btn btn-primary">Enviar</button>
  </form>
```


![[FIAP/Imagens/Capitulo 2 - Um pouco mais de Bootstrap-20250324103921904.webp]]
Com uma classe .form-lavel para cada elemento de rótulo, irá ocorrer um preenchimento correto para os elementos.

As caixas de seleção possuem marcações diferentes. Elas são agrupadas por meio de um elemento de contêiner chamado .form-check, os rótulos têm uma classe .form-check-label, enquanto as caixas de seleção e os botões de opção utilizam .form-check-input

# Área de texto

