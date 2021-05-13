# Entrada e Saída

Lendo valores do teclado e escrevendo na tela.

## Entrada

Números e Textos podem ser lidos do teclado usando as intruções:
 - `leia_inteiro` para ler um número inteiro
 - `leia_real` para ler um número real (float)
 - `leia_texto` para ler um texto

````scala
a = leia_inteiro                # lê um número inteiro do teclado
b = leia_real                   # lê um número real do teclado
c = leia_texto                  # lê um texto do teclado
````

```tip
Para ler vários valores do mesmo tipo em sequência podemos usar `a, b, c, ... = leia_inteiro`
```
As três linhas a seguir

````scala
x = leia_inteiro
y = leia_inteiro
z = leia_inteiro
````

podem ser escritas

````scala
x, y, z = leia_inteiro
````

## Instruções para ler listas de valores

- `leia_inteiros(n)` para ler `n` números inteiro, um por linha
- `leia_reais(n)` para ler `n` números reais, um por linha
- `leia_textos(n)` para ler `n` linhas de texto

````scala
números = leia_inteiros(5)      # lê um lista de 5 números inteiros, um por linha
````

- `leia_inteiros(s)` para ler vários números inteiros em uma mesma linha usando `s` como separador
- `leia_reais(s)` para ler vários números reais em uma mesma linha usando `s` como separador
- `leia_textos(s)` para ler vários textos em uma mesma linha usando `s` como separador

````scala
números = leia_inteiros(",")    # lê uma lista de números inteiros separados por vírgula
````

## Saída

Para exibir algo na tela usamos `escreva` ou `imprima`. A diferença é que `escreva` exibe um valor na tela e depois pula de linha. A instrução `imprima` exibe um valor na tela e continua na mesma linha.

````ruby
escreva "Olá Mundo"   # Escreve e passa para a próxima linha
imprima "Olá "        # Escreve e continua na mesma linha
escreva "Mundo"
````

### Interpolação de textos

Para inserir valores dentro de um texto podemos usar `{` e `}`.

````ruby
nome = "Mundo"
escreva "Olá {nome}!"  # "Olá Mundo!"
````
