# Tipos Básicos

Os tipos básicos são `Inteiro`, `Real`, `Texto`, `Lógico` e `Caractere`.

```note
Note que os tipos começam com letras maiúsculas.
```

| Tipo | Valores |
| --- | --- |
| Inteiro | `-4`, `0`, `5`, ... |
| Real | `-7.23`, `0.0`, `5.25`, ... |
| Texto | `"texto"`, `"ola"`, `"mundo"`, ... |
| Lógico | `verdadeiro` e `falso` |
| Caractere | `'a'`, `'4'`, `'&'`, ... |


Exemplo

```python
a: Inteiro = 10
r: Real = 3.14
s: Texto = "Programação"
b: Lógico = verdadeiro
c: Caractere = 'z'
```

## Operações Aritméticas

Soma (`+`)
```python
5 + 3         # 8
```

Subtração (`-`)
```python
5 - 3         # 2
```

Multiplicação (`*`)
```python
5 * 3         # 15
```

Divisão Real (`/`)
```python
5 / 3         # 1.66667
```

Divisão Inteira (`div`)
```python
5 div 3       # 1
```

Resto da divisão (`mod`)
```python
5 mod 3       # 2, o resto da divisão de 5 por 3
```

Exponenciação (`^`)
```python
5 ^ 2       # 25.0
```

## Operações Lógicas

Valores lógicos (booleanos): `verdadeiro` e `falso`

### `e` lógico
```python
falso e falso            # falso
falso e verdadeiro       # falso
verdadeiro e falso       # falso
verdadeiro e verdadeiro  # verdadeiro
```

Exemplo
```python
nota_válida = (nota >= 0) e (nota <= 10)
```

### `ou` lógico
```python
falso ou falso            # falso
falso ou verdadeiro       # verdadeiro
verdadeiro ou falso       # verdadeiro
verdadeiro ou verdadeiro  # verdadeiro
```

Exemplo
```python
nota_inválida = (nota < 0) ou (nota > 10)
```

### `não` lógico
```python
não falso            # verdadeiro
não verdadeiro       # falso
```

### Tabela Verdade

| A | B | A `e` B | A `ou` B | `não` A | `não` B |
| --- | --- | --- | --- | --- | --- | 
| falso | falso | falso | falso | verdadeiro | verdadeiro |
| falso | verdadeiro | falso | verdadeiro | verdadeiro | falso |
| verdeiro | falso | falso | verdadeiro | falso | verdadeiro |
| verdadeiro | verdadeiro | verdadeiro | verdadeiro | falso | falso |


## Operações de comparação (relacionais)

### Igualdade (`==`)
```python
2 == 2         # verdadeiro
```

### Desigualdade (`<>`)
```ruby
2 <> 3         # verdadeiro
2 <> 2         # falso
```

### Menor (`<`)
```python
2 < 3          # verdadeiro
2 < 2          # falso
3 < 2          # falso
```

### Menor ou igual (`<=`)
```python
2 <= 3         # verdadeiro
2 <= 2         # verdadeiro
3 <= 2         # falso
```

### Maior (`>`)
```python
2 > 3          # falso
2 > 2          # falso
3 > 2          # verdadeiro
```

### Maior ou igual (`>=`)
```python
2 >= 3         # falso
2 >= 2         # verdadeiro
3 >= 2         # verdadeiro
```
