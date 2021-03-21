# Funções

````scala
soma(x: Inteiro, y: Inteiro) = x + y    # Declaração de função em uma linha

soma(x, y: Inteiro) = x + y             # Agrupando parâmetros do mesmo tipo

rep(a: Texto, n: Inteiro) = a * n       # Funções com parâmetros de tipos diferentes

a, b = leia_inteiro
c = soma(a, b)                          # Aplicando a função
escreva "{a} + {b} = {c}"

soma(x, y: Inteiro): Inteiro = x + y    # O tipo de retorno pode ser definido explicitamente

soma(x, y: Inteiro)                     # Declaração de função com corpo
  c = x + y
  retorne c                             # A última linha tem o valor de retorno
fim

soma(x, y: Inteiro)                     # Declaração de função com corpo
  c = x + y
  c                                     # A palavra 'retorne' é opcional
fim

fatorial(n: Inteiro): Inteiro           # Função recursiva (tipo de retorno é obrigatório)
  se n <= 1 então
    1
  senão
    n * fatorial(n - 1)
  fim
fim
a = leia_inteiro
escreva "Fatorial de {a} é {fatorial(a)}"

f(a: Inteiro)
  g(b: Inteiro) = b * 2                 # Função interna
  retorne g(a) + 3
fim
````

### Tipo de parâmetros

| Tipo | Exemplo | Aplicação|
| --- | --- | --- |
| `Inteiro` | `proximo(a: Inteiro) = a + 1 `| `proximo(3)` |
| `Real`    | `dobro(a: Real) = a * 2` | `dobro(3.6)` |
| `Texto`   | `inicio(s: Texto) = s.pegue(5)` | `inicio("Olá mundo!")` |
| `Lógico`  | `negacao(a: Lógico) = não a` | `negacao(verdadeiro)` |
| `Caractere` | `id(c: Caractere) = c` | `id('a')` |
| `Tupla` | `f(a : (Inteiro, Texto)) = ...` | `f((10,"ok"))` |
| `Lista` | `soma(a: Lista[inteiro]) = ...` | `soma([1,2,3,4,5])` |
| Função | `f(g: (Inteiro, Inteiro) => Inteiro) = g(2,3)` | `f((a,b) => a + b)` |
| Classe ou Registro | `f(a: T) = ...` | `f(T(...))` |
