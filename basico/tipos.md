# Tipos Básicos

| Tipo | Valores |
| --- | --- |
| Inteiro | `-4`, `0`, `5`, ... |
| Real | `-7.23`, `0.0`, `5.25`, ... |
| Texto | `"texto"`, `"ola"`, `"mundo"`, ... |
| Lógico | `verdadeiro` e `falso` |
| Caractere | `'a'`, `'4'`, `'&'`, ... |


```python
a: Inteiro = 10
r: Real = 3.14
s: Texto = "Programação"
b: Lógico = verdadeiro
c: Caractere = 'z'
```

## Operações Aritméticas

Soma
```
5 + 3         # 8
```

Subtração
```
5 - 3         # 2
```

Multiplicação
```
5 * 3         # 15
```

Divisão Real
```
5 / 3         # 1.66667
```

Divisão Inteira
```
5 div 3       # 1
```

Resto da divisão
```
5 mod 3       # 2, o resto da divisão de 5 por 3
```

## Operações Lógicas e Relacionais

Valores lógicos (booleanos): `verdadeiro` e `falso`

`e`-lógico
```
falso e falso            # falso
falso e verdadeiro       # falso
verdadeiro e falso       # falso
verdadeiro e verdadeiro  # verdadeiro
```

`ou`-lógico
```
falso ou falso            # falso
falso ou verdadeiro       # verdadeiro
verdadeiro ou falso       # verdadeiro
verdadeiro ou verdadeiro  # verdadeiro
```

`não`-lógico
```
não falso            # verdadeiro
não verdadeiro       # falso
```

### Tabela Verdade

| A | B | A `e` B | A `ou` B | `não` A | `não` B |
| falso | falso | falso | falso | verdadeiro | verdadeiro |
| falso | verdadeiro | falso | verdadeiro | verdadeiro | falso |
| verdeiro | falso | falso | verdadeiro | falso | verdadeiro |
| verdadeiro | verdadeiro | verdadeiro | verdadeiro | falso | falso |


## Operações de comparação

2 == 3         # falso
Igualdade (`==`)
```
2 == 2         # verdadeiro
```

Desigualdade (`<>`)
```
2 <> 3         # verdadeiro
2 <> 2         # falso
```

Menor (`<`)
```
2 < 3          # verdadeiro
2 < 2          # falso
3 < 2          # falso
```

Menor ou igual (`<=`)
```
2 <= 3         # verdadeiro
2 <= 2         # verdadeiro
3 <= 2         # falso
```

Maior (`>`)
```
2 > 3          # falso
2 > 2          # falso
3 > 2          # verdadeiro
```

Maior ou igual (`>=`)
```
2 >= 3         # falso
2 >= 2         # verdadeiro
3 >= 2         # verdadeiro
```
