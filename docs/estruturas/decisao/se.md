# Se
````scala
x = leia_inteiro

# se ... então ... fim
se x > 5 então
  escreva "Maior do que cinco."
fim

# se ... então ... senão ... fim
se x > 5 então
  escreva "Maior do que cinco."
senão
  escreva "Menor ou igual a cinco."
fim

se verdadeiro então                # escreva "verdadeiro"
  escreva "verdadeiro"
senão
  escreva "falso"
fim

se falso então                     # escreva "falso"
  escreva "verdadeiro"
senão
  escreva "falso"
fim

# se ... então ... senãose ... senão ... fim
se x > 8 então
  escreva "Maior do que oito."
senãose x > 6 então
  escreva "Maior do que seis."
senãose x > 4 então
  escreva "Maior do que quatro."
senãose x > 2 então
  escreva "Maior do que dois."
senão
  escreva "Menor ou igual a dois."
fim

# usando se como uma expressão
a = se x mod 2 == 0 então "par" senão "ímpar" fim

maior = se a >= b e a >= c então a senãose b > c então b senão c fim
````
