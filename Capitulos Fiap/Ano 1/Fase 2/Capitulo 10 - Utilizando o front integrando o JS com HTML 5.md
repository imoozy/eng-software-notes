
# Importância e motivação

Processar textos na linguagem de JS é uma função que ajuda o desenvolvedor a trabalhar de forma bastante eficiente, utilizando recursos nativos na linguagem de programação. Em programação, denominamos o tipo de dado "Texto" como strings, que são basicamente sequências de caracteres delimitadas. Os delimitadores possíveis para Strings em JS são três: Apóstrofe ('), ou aspas simples; as próprias Aspas("), também conhecidas como Aspas duplas; ou acento grave para delimitar Strings com múltiplas linhas.

```JS
var str1 = 'Exemplo de String com aspas simples';
var str2 = "Exemplo de String com aspas duplas";
var str3 = 'Exemplo de String com acento grave
  			que permite escrevê-la em
			várias linhas';
```

O que podemos fazer com String? Além e armazenar textos, podemos também realizar várias operações dentre elas:
- Concatenação;
- Determinação de quantidade de caracteres de uma String;
- Delimitação de subpalavras (substrings);
- Encontro de ocorrências de palavras;
- Criação de textos por substituição.


# Vamos falar das principais operações

## Concatenação

![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144041424.webp]]
## Busca de palavras

![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144119082.webp]]

```JS
var posicao = roteiro.search("Parque do Ibirapuera");
console.log(posicao);
```

Exemplo:
![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144326633.webp]]

![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144148685.webp]]

## Prefixos e sufixos

![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144633397.webp]]
```JS
var resultado = texto.endsWith("Paulista");
console.log(resultado); // o resultado será FALSE
```

## Subpalavras

![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144721904.webp]]
![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144733571.webp]]
Nesse caso o resultado exibido será Gasolina.

## Extração de conjuntos de palavras

![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144810396.webp]]
![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144822468.webp]]
![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144836028.webp]]

## Substituindo palavras

![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144856972.webp]]
![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144918233.webp]]
![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144930567.webp]]

## Um tipo de substituição especial

![[Capitulo 10 - Utilizando o front integrando o JS com HTML 5-20250224144959264.webp]]
