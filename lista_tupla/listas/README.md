# Listas

Em Potigol, **listas** são estruturas de dados fundamentais que permitem armazenar e manipular coleções ordenadas de elementos.
- São imutáveis por padrão, o que significa que, uma vez criadas, não podem ser alteradas diretamente, garantindo segurança e consistência em operações funcionais.
- São altamente versáteis, suportando desde operações básicas, como acesso a elementos e verificação de tamanho, até transformações avançadas, como mapeamento, filtragem e redução.
- Sintaxe intuitiva e alinhada ao paradigma funcional, as listas são uma ferramenta poderosa para lidar com dados de forma eficiente e expressiva.
- Oferece suporte a listas mutáveis para casos específicos, bem como estruturas multidimensionais, como matrizes e cubos, ampliando ainda mais suas possibilidades de uso.

## 1. **Criação de Listas**
- **Lista literal**: `[2, 4, 6, 8, 10]`
- **Adição de elementos**: `2 :: [4, 6, 8, 10]` → `[2, 4, 6, 8, 10]`  
- **Lista preenchida**: `Lista(5, 0)` → `[0, 0, 0, 0, 0]`
- **Lista vazia tipada**: `Lista.vazia[Inteiro]` → `[]` 

---

## 2. **Operações Básicas**
| Método/Operação | Exemplo | Resultado | Descrição |
|-----------------|---------|-----------|-----------|
| `.tamanho` | `[2,4,6,8,10].tamanho` | `5` | Retorna o número de elementos |
| `.cabeça` | `[2,4,6,8,10].cabeça` | `2` | Primeiro elemento da lista |
| `.cauda` | `[2,4,6,8,10].cauda` | `[4,6,8,10]` | Lista sem o primeiro elemento |
| `.último` | `[2,4,6,8,10].último` | `10` | Último elemento da lista |
| Acesso por índice | `a[3]` | `6` (índices começam em 1) |  |

---

## 3. **Manipulação de Elementos**
- **Remoção**: `a.remova(4)` → `[2, 4, 6, 10]` (remove o elemento na posição 4)
- **Inserção**: `a.insira(3,5)` → `[2, 4, 5, 6, 8, 10]` (insere `5` na posição 3)
- **Atualização**: `a.atualize(3,5)` → `[2, 4, 5, 8, 10]` (alterar o valor da posição 3)
- **Verificação**: `a.contém(6)` → `verdadeiro` 

---

## 4. **Transformação de Listas**
| Método | Exemplo | Resultado | Descrição |
|--------|---------|-----------|-----------|
| `.inverta` | `[2,4,6,8,10].inverta` | `[10,8,6,4,2]` | Inverte a ordem |
| `.ordene` | `[2,6,8,10,4].ordene` | `[2,4,6,8,10]` | Ordenação padrão |
| `.ordene` customizado | `[1,15,2,...].ordene(- _)` | `[40,15,10,2,2,1]` | Ordenação decrescente usando lambda `- _`  |
| `.junte` | `[2,4,6].junte(", ")` | `"2, 4, 6"` | Concatena elementos com separador |

---

## 5. **Combinação de Listas**
- **Concatenação**: `[2,4,6] + [8,10]` → `[2,4,6,8,10]`
- **Divisão**: `[2,4,6,8,10].descarte(2)` → `[6,8,10]` (remove os primeiros 2 elementos)
- **Seleção**: `[2,4,6,8,10].pegue(2)` → `[2,4]` (pega os primeiros 2 elementos) 

---

## 6. **Funções de Alta Ordem**
| Método | Exemplo | Resultado | Descrição |
|--------|---------|-----------|-----------|
| `.selecione` | `[2,4,6,8,10].selecione(n => n mod 4 == 0)` | `[4,8]` | Filtra elementos que satisfazem a condição |
| `.mapeie` | `[2,4,6,8,10].mapeie(n => n div 2)` | `[1,2,3,4,5]` | Transforma cada elemento |
| `.injete` | `[2,4,6].injete(0)((a,b) => a + b)` | `12` | Acumula valores (equivalente a `reduce`)  |

---

## 7. **Matrizes e Cubos**
- **Matriz 2D**: `a = [[1,2], [3,4]]`  
  - Acesso: `a[2][1]` → `3`  
- **Cubo 3D**: `Cubo.imutável(2,2,2,"-")` → Estrutura 2x2x2 preenchida com `"-"` 

---

## 8. **Listas Mutáveis**
- Criação: `a = Lista.mutável(5, 0)` → `[0,0,0,0,0].mutável`  
- Modificação: `a[3] := 5` → `[0,0,5,0,0]`  
  *(Obs: Potigol prioriza imutabilidade, mas oferece essa opção para casos específicos)* 

---

## 9. **Casos Especiais**
- **Divisão condicional**: `[2,2,3,3,3,6,5,6].divida_quando((a,b) => a <> b)` → `[[2,2],[3,3,3],[6],[5],[6]]`  
- **Ordenação por critério**: `[[1], [10,10], ...].ordene(_.tamanho)` → Ordena listas pelo tamanho 

---

## Resumo de Características
- **Imutabilidade**: Listas são imutáveis por padrão, garantindo segurança em operações funcionais .
- **Flexibilidade**: Suporta desde operações básicas até funções avançadas como mapeamento e redução.
- **Sintaxe intuitiva**: Palavras-chave em português facilitam o aprendizado .



---


### Sintaxe
````scala
[2, 4, 6, 8, 10]                         # lista literal
2 :: [4, 6, 8, 10]                       # [2, 4, 6, 8, 10]
[2, 4, 6, 8, 10].tamanho                 # 5
[2, 4, 6, 8, 10].cabeça                  # 2
[2, 4, 6, 8, 10].cauda                   # [4, 6, 8, 10]
[2, 4, 6, 8, 10].último                  # 10
[2, 4, 6, 8, 10].pegue(2)                # [2, 4]
[2, 4, 6, 8, 10].descarte(2)                # [6, 8, 10]


[2, 4, 6, 8, 10].inverta                      # [10, 8, 6, 4, 2]
[2, 6, 8, 10, 4].ordene                       # [2, 4, 6, 8, 10]
[1, 15, 2, 10, 2, 40].ordene(- _)             # [40, 15, 10, 2, 2, 1]
[[1], [10,10], [3,3],[40]].ordene(_.tamanho)  # [[1], [40], [10, 10], [3, 3]]
[2, 4, 6] + [8, 10]                           # [2, 4, 6, 8, 10]
[2, 4, 6].junte                               # "246"
[2, 4, 6].junte(", ")                         # "2, 4, 6"
[2, 4, 6].junte("[", ", ", "]")               # "[2, 4, 6]"

a = [2, 4, 6, 8, 10]
a[3]                                     # 6
a.posição(6)                             # 3
a.posição(12)                            # 0
a.contém(6)                              # verdadeiro
a.contém(12)                             # falso
a.remova(4)                              # [2, 4, 6, 10]
a.insira(3,5)                            # [2, 4, 5, 6, 8, 10]

Lista.imutável(5, 0)                     # [0, 0, 0, 0, 0]
Lista.vazia[Inteiro]                     # []   - Lista vazia de inteiros

# Matrizes e Cubos
a = [[1, 2], [3, 4]]                     # Matriz 2x2
a[2]                                     # [3, 4]
a[2][1]                                  # 3
b = Matriz.imutável(2, 2, 0)             # b == [[0, 0], [0, 0]]
c = Cubo.imutável(2, 2, 2, "-")          # c == [[["-", "-"],["-", "-"]],[["-", "-"],["-", "-"]]]
c[1][2][1]                               # "-"

# Listas mutáveis
a = Lista.mutável(5, 0)                      # [0, 0, 0, 0, 0].mutável
a[3] := 5                                    # a == [0, 0, 5, 0, 0].mutável

# Funções de alta-ordem
[2, 4, 6, 8, 10].selecione(n => n mod 4 == 0)       # [4, 8]
[2, 4, 6, 8, 10].mapeie(n => n div 2)               # [1, 2, 3, 4, 5]
[2, 4, 6].injete(0)((a, b) => a + b)                # 0 + 2 + 4 + 6 == 12
[2, 4, 6].injete((a, b: Inteiro) => a + b)          # 2 + 4 + 6 == 12
[2, 4, 6, 2, 4].pegue_enquanto(n => n < 6)          # [2, 4]
[2, 4, 6, 2, 4].descarte_enquanto(n => n < 6)       # [6, 2, 4]
[2,2,3,3,3,6,5,6].divida_quando((a, b) => a <> b)   # [[2,2],[3,3,3],[6],[5],[6]]
````
