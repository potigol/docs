# Para
````scala
para i de 1 até 10 faça            # escreve os números de 1 a 10
  escreva i
fim

var soma := 0
para i de 1 até 10 faça            # soma os números de 1 a 10
  soma := soma + i
fim
escreva "A soma é {soma}."

para i de 1 até 10 passo 2 faça    # escreve os números ímpares de 1 a 10
  escreva i
fim

# Para decrescente
para i de 10 até 1 passo -1 faça   # escreve os números de 10 a 1
  escreva i
fim

# Para com mais de um gerador
para i de 1 até 4,
     j de 1 até 3 faça             # escreve a tabuada {1..4} x {1..3}
  escreva "{i} * {j} == {i * j}"
fim

# Para com listas
cores = ["azul", vermelho", "verde"]
para cor em cores faça
  escreva cor
fim

# Para gerando uma lista
numeros = para i de 1 até 5 gere i fim             # [1, 2, 3, 4, 5]

pares = para i de 1 até 10 se i mod 2 == 0 gere i  # [2, 4, 5, 6, 8, 10]

````
