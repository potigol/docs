# Variáveis

Há dois tipos de variáveis em Potigol.
A diferença é se o valor atribuído a cada variável pode mudar ou não.

As variáveis que não mudam de valor são constantes.
O valor é atribuído à variável no momento da declaração e não pode ser alterado.

```python
x = 10           # Declaração de um valor fixo (não pode ser alterado)
```
As variáveis que podem mudar de valor são declaradas com `var`.

```python
var y := 10      # Declaração de uma variável alterável
y := 12
```

```note
Note que essas variáveis podem receber novas atribuições mas o tipo não muda.
Se na declaração a variável recebe um inteiro, seu tipo será sempre inteiro.
```

## Atribuição paralela

```python
y, z = 20              # Mais de uma variável recebe o mesmo valor y = 20 e z = 20
a, b, c = 1, 2, 3      # Declaração paralela: a = 1, b = 2 e c = 3

var a, b, c := 1, 2, 3 # Declaração paralela: var a := 1, var b := 2 e var c := 3
a, b, c := b, a, 4     # Atribuição paralela: a := 2, b := 1 e c := 4
```
