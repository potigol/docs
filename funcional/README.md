# Programação Funcional

### Valores (constantes)
````ruby
nome = "potigol"
````

### Listas
````ruby
lista1 = [1,2,3,4]
lista2 = 0::lista1
````

### Operações com listas (filter, fold, map)
````ruby
numeros = [1, 2, 3, 4, 5, 6, 7, 8]
pares = numeros.selecione(n => n mod 2 == 0)    # filtro
soma = numeros.injete(0)((a,b) => a + b)        # fold
dobro = numeros.mapeie(n => n * 2)              # map
````

### Expressões lambda
````ruby
x = (a: Inteiro) => a * 2
escreva x(4)
````

### "list comprehension"
````ruby
y = para i de 1 até 10,
         j de i + 1 até 10 gere
           i+j
    fim
escreva y
````

### Funções de Alta ordem
````scala
f(g: Inteiro => Inteiro, a: Inteiro) = g(a)
sucessor(n: Inteiro) = n + 1
escreva f(sucessor, 5)
````

### Currying
````scala
soma(a: Inteiro) = ((b: Inteiro) => a + b)
escreva soma(2)(3)
suc = soma(1)
escreva suc(4)
````

### Recursão em cauda otimizada
````scala
h(a, cont: Inteiro): Inteiro = escolha a
  caso 0 => cont
  caso n => h(a-1, cont+1)
fim
escreva h(1000,0)
````

### Casamento de Padrões
````scala
# QuickSort
quicksort(num: Lista[Inteiro]): Lista[Inteiro] =
  escolha num
    caso []  => []
    caso pivo::resto =>
      menores = resto.selecione( _ <= pivo )
      maiores = resto.selecione( _ >  pivo )
      quicksort(menores) + pivo::quicksort(maiores)
  fim

escreva "Digite alguns números separados por espaços"
numeros = leia_inteiros(" ")
escreva "Os números ordenados:"
escreva quicksort(numeros)
````
