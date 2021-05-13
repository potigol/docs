# Variáveis

Há dois tipos de variáveis em Potigol.
A diferença é se o valor atribuído a cada variável pode mudar ou não.

As variáveis que não mudam de valor são constantes.
O valor é atribuído à variável no momento da declaração e não pode ser alterado.

```python
x = 10           # Declaração de um valor fixo (não pode ser alterado)
```
As variáveis que podem mudar de valor são declaradas com `var` e `:=`.

```python
var y := 10      # Declaração de uma variável alterável
y := 12
```

```note
Note que essas variáveis podem receber novas atribuições mas o tipo não muda.
Se na declaração a variável recebe um inteiro, seu tipo será sempre inteiro.
```

O nome das variáveis deve começar com uma letra seguida de letras, números e '_'. Nomes válidos: `idade`, `endereço`, `nota1` e `salário_bruto`. Nome inválidos: `a idade` e `1nota`. Apesar de não ser uma imposição, os nomes das variáveis geralmente começam com uma letra minúscula.

## Atribuição paralela

As atribuições podem ser realizadas simultaneamente.

```python
y, z = 20              # Mais de uma variável recebe o mesmo valor y = 20 e z = 20
a, b, c = 1, 2, 3      # Declaração paralela: a = 1, b = 2 e c = 3

var a, b, c := 1, 2, 3 # Declaração paralela: var a := 1, var b := 2 e var c := 3
a, b, c := b, a, 4     # Atribuição paralela: a := 2, b := 1 e c := 4
```

```tip
A atribuição paralela é útil para permutar os valores de variáveis.
```

```python
var a, b := 10, 20        # a == 10, b == 20
b, a := a, b              # a == 20, b == 10
```
