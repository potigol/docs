# Números

### Número (Inteiro e Real)
````scala
12345.qual_tipo                   # "Inteiro"
12345.real                        # 12345.0
12345.texto                       # "12345"
97.caractere                      # 'a'
12345 formato "%8d"               # "   12345"

12345.678.qual_tipo               # "Real"
12345.678.inteiro                 # 12345
12345.678.texto                   # "12345.678"
12345.678.arredonde               # 12346
12345.678.arredonde(2)            # 12345.68
123.45 formato "%.1f"             # "123.4"

12345.678.piso                    # 12345.0 (arredonda para baixo)
12345.678.teto                    # 12346.0 (arredonda para cima)
12345.678.inteiro                 # 12345
````
