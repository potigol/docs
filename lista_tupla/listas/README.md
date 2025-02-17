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

Seja `a = [2, 4, 6, 8, 10]`

- **Remoção**: `a.remova(4)` → `[2, 4, 6, 10]` (remove o elemento na posição 4)
- **Inserção**: `a.insira(3,5)` → `[2, 4, 5, 6, 8, 10]` (insere `5` na posição 3)
- **Atualização**: `a.atualize(3,5)` → `[2, 4, 5, 8, 10]` (alterar o valor da posição 3)
- **Verificação**: `a.contém(6)` → `verdadeiro` 

### Manipulação de Elementos em Listas Imutáveis

As listas são **imutáveis por padrão**, o que significa que qualquer operação de modificação resulta em uma **nova lista**, mantendo a original inalterada. Isso garante que as estruturas de dados sejam seguras e consistentes. Abaixo estão exemplos de como manipular elementos em listas imutáveis:

#### Exemplo 1: Atualização de Elementos
Quando você deseja modificar um elemento específico de uma lista, a operação não altera a lista original, mas cria uma **nova lista** com a modificação aplicada.

```potigol
var a := [1, 2, 3, 4]
b = a
a := a.atualize(3, 5)  # Atualiza o elemento na posição 3 para o valor 5
escreva a  # [1, 2, 5, 4]
escreva b  # [1, 2, 3, 4] (a lista original permanece inalterada)
```

Neste exemplo:
- `a.atualize(3, 5)` cria uma nova lista onde o elemento na posição 3 é substituído por `5`.
- A lista original `b` permanece inalterada, demonstrando a imutabilidade.


### Operador de atribuição `[ ] :=`

Em Potigol, o conceito de **açúcar sintático** se refere a uma sintaxe simplificada e mais intuitiva que facilita a escrita e a leitura do código, sem alterar a funcionalidade subjacente. No caso da manipulação de listas, a expressão:

```potigol
a[3] := 5
```

é um **açúcar sintático** para a operação:

```potigol
a := a.atualize(3, 5)
```

#### O que isso significa?
- **`a[3] := 5`**: Essa sintaxe sugere que estamos "atualizando" o valor na posição 3 da lista `a` para `5`. No entanto, como as listas são imutáveis, essa operação não modifica a lista original. Em vez disso, ela cria uma **nova lista** com o valor atualizado e a atribui à variável `a`.
- **`a := a.atualize(3, 5)`**: Essa é a forma explícita da operação. O método `.atualize` cria uma nova lista com o valor na posição 3 substituído por `5`, e o resultado é atribuído de volta à variável `a`.

#### Por que usar açúcar sintático?
1. **Simplicidade**: A sintaxe `a[3] := 5` é mais curta e intuitiva, especialmente para quem está acostumado com operações de atualização em listas mutáveis.
2. **Legibilidade**: O código fica mais claro e fácil de entender, sem perder a semântica funcional.
3. **Consistência**: Mantém a imutabilidade das listas, mas oferece uma forma conveniente de "simular" uma atualização.

#### Exemplo 2: Atualização de Elementos usando `[ ] :=`
```potigol
var a := [1, 2, 3, 4]
a[3] := 5  # Açúcar sintático para a := a.atualize(3, 5)
escreva a  # [1, 2, 5, 4]
```

Neste exemplo:
- A expressão `a[3] := 5` cria uma nova lista `[1, 2, 5, 4]` e a atribui à variável `a`.
- A lista original `[1, 2, 3, 4]` não é modificada, mas deixa de ser referenciada por `a`.

#### Exemplo 3: Inserção de Elementos
Para inserir um elemento em uma posição específica, a operação também gera uma nova lista.

```potigol
var a := [1, 2, 3, 4]
b = a
a := a.insira(2, 10)  # Insere o valor 10 na posição 2
escreva a  # [1, 10, 2, 3, 4]
escreva b  # [1, 2, 3, 4] (a lista original permanece inalterada)
```

#### Exemplo 4: Remoção de Elementos
A remoção de um elemento também resulta em uma nova lista, sem afetar a original.

```potigol
var a := [1, 2, 3, 4]
b = a
a := a.remova(2)  # Remove o elemento na posição 2
escreva a  # [1, 3, 4]
escreva b  # [1, 2, 3, 4] (a lista original permanece inalterada)
```

#### Exemplo 5: Concatenação de Listas
A concatenação de listas também cria uma nova lista, sem modificar as originais.

```potigol
var a := [1, 2, 3]
var b := [4, 5, 6]
c = a + b  # Concatena as listas a e b
escreva c  # [1, 2, 3, 4, 5, 6]
escreva a  # [1, 2, 3] (a lista original permanece inalterada)
escreva b  # [4, 5, 6] (a lista original permanece inalterada)
```

Essa abordagem funcional torna Potigol uma linguagem robusta para manipulação de dados, especialmente em cenários onde a imutabilidade é essencial.

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

## 10. **Manipulação de Listas de Objetos em Potigol**

Em Potigol, listas de objetos são uma forma eficiente de gerenciar coleções de dados complexos, combinando a imutabilidade das listas com a flexibilidade de tipos personalizados. Abaixo está um exemplo prático de como criar, manipular e iterar sobre listas de objetos, utilizando o tipo `Pessoa` definido pelo usuário:

---

#### 1. **Definição do Tipo `Pessoa`**
Primeiro, definimos a estrutura do objeto `Pessoa` com atributos e métodos:

```portugol
tipo Pessoa
  nome: Texto
  email: Texto
  ano_nascimento: Inteiro
  idade() = 2025 - ano_nascimento
  adulto() = idade >= 18
fim
```

- **Atributos**: `nome`, `email`, `ano_nascimento`.
- **Métodos**:
  - `idade()`: Calcula a idade com base no ano atual (2025 no exemplo).
  - `adulto()`: Retorna `verdadeiro` se a idade for maior ou igual a 18.

---

#### 2. **Criação da Lista de Objetos**
Usamos um loop `para...gere` para ler dados e gerar a lista de objetos `Pessoa`:

```scala
pessoas = para i de 1 até 5 gere
  nome = leia_texto     # Lê o nome do terminal
  email = leia_texto    # Lê o email do terminal
  ano_nascimento = leia_inteiro  # Lê o ano de nascimento
  Pessoa(nome, email, ano_nascimento)  # Cria um objeto Pessoa
fim
```

- **`para...gere`**: Gera uma lista com 5 objetos `Pessoa`.
- **`leia_texto`/`leia_inteiro`**: Funções para entrada de dados (simuladas ou reais, dependendo do contexto).

---

#### 3. **Iteração e Formatação da Lista**
Podemos iterar sobre a lista e exibir os dados formatados:

```scala
para p em pessoas faça
  escreva "{p.nome formato "%20s"}{p.email formato "%20s"}{p.idade formato "%3d"}"
fim
```

- **`para...faça`**: Itera sobre cada objeto `p` na lista `pessoas`.
- **`formato`**: Formata os valores para alinhamento:
  - `%20s`: Alinha o texto em 20 caracteres.
  - `%3d`: Alinha números inteiros em 3 dígitos.

**Saída esperada** (exemplo):
```
             João        joao@email.com         25
            Maria       maria@email.com         30
             José        jose@email.com         42
```

---

#### 4. **Operações Comuns com Listas de Objetos**
Como as listas são imutáveis, qualquer operação retorna uma **nova lista**. Exemplos:

##### a) **Filtrar Pessoas Adultas**
```scala
adultos = pessoas.selecione(p => p.adulto())
escreva "Adultos: {adultos.tamanho}"
```

##### b) **Mapear Emails**
```scala
emails = pessoas.mapeie(p => p.email)
escreva emails  # ["joao@email.com", "maria@email.com", ...]
```

##### c) **Atualizar um Objeto na Lista**
```scala
var pessoas := ...
# Altera a pessoa na posição 1
pessoas[1] := Pessoa("Nome da Pessoa", "oemail@email.com", 2005)
# Atualiza o email da pessoa na posição 2
pessoas[2] := Pessoa(pessoas[2].nome, "novo_email@teste", pessoas[2].ano_nascimento)
```

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
