# Escolha

````scala
x = leia_inteiro
escolha x
  caso 1 => escreva "Um"               # se x == 1
  caso 2 => escreva "Dois"             # se x <> 1 e x == 2
  caso 3 => escreva "Três"             # se x <> 1 e x <> 2 e x == 3
  caso _ => escreva "Outro valor"      # se x <> 1 e x <> 2 e x <> 3
fim

# escolha com condições
escolha x
  caso n se n < 0        => escreva "{n} é negativo"
  caso n se n mod 2 == 0 => escreva "{n} é par"
  caso n                 => escreva "{n} é ímpar"
fim

# usando escolha como uma expressão
é_zero = escolha x
  caso 0 => verdadeiro
  caso _ => falso
fim

sinal = escolha x               # escolha retorna um número: -1, 0 ou 1
  caso n se n < 0 => -1
  caso n se n > 0 =>  1
  caso _          =>  0
fim
````
