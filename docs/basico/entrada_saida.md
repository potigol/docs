# Entrada e Saída

:fontawesome-solid-terminal: **Comunicação básica** entre programa e usuário

<div class="grid cards" markdown>

- :material-keyboard-outline: **Saída formatada**  
  `#!potigol escreva` e `#!potigol imprima`

- :material-keyboard-return: **Entrada de dados**  
  `#!potigol leia_*` para diferentes tipos

- :fontawesome-solid-list-ol: **Múltiplos Valores**  
  Atribuição paralela e listas

- :material-code-brackets: **Interpolação**  
  Inserção dinâmica de valores

</div>

---

## :material-keyboard-return: Comandos de Entrada

### Leitura Básica

#### Sintaxe

```potigol
valor = leia_tipo
```

Onde `tipo` pode ser:

- `inteiro`: Para números inteiros
- `real`: Para números decimais  
- `texto`: Para strings

#### Funcionamento

Cada comando lê uma linha completa da entrada padrão e tenta converter para o tipo especificado. Aguarda o usuário pressionar Enter.

```potigol
# Exemplo completo
escreva "Digite sua idade:"
idade = leia_inteiro  # Aguarda um número inteiro

escreva "Digite seu salário:"
salario = leia_real  # Aguarda um número decimal

escreva "Digite seu nome:"
nome = leia_texto  # Aguarda texto
```

---

### Leitura Múltipla

#### Sintaxe

```potigol
var1, var2, ..., varN = leia_tipo
```

#### Funcionamento

Lê N valores do tipo especificado, um por linha. Útil quando se conhece antecipadamente a quantidade de valores.

```potigol
# Lendo 3 inteiros (um por linha)
x, y, z = leia_inteiro

# Lendo 2 textos
nome, sobrenome = leia_texto
```

---

### Leitura de Listas

#### Sintaxe

```potigol
lista = leia_tipos(quantidade)
lista = leia_tipos(separador)
```

#### Funcionamento

- Com número: Lê N valores do tipo, um por linha
- Com separador: Lê uma linha e divide pelo caractere especificado

```potigol
# 5 números em linhas separadas
notas = leia_inteiros(5) 

# Valores separados por vírgula na mesma linha
coordenadas = leia_reais(",")  # Ex: "3.5,2.7,4.1"

# Múltiplas listas de textos
nomes, emails = leia_textos(3)  # Lê duas listas de 3 textos cada
```

---

## :material-keyboard-outline: Comandos de Saída

### `escreva` vs `imprima`

#### Sintaxe

```potigol
escreva expressão  # Adiciona quebra de linha
imprima expressão  # Mantém cursor na mesma linha
```

#### Diferenças

| Comando    | Quebra Linha | Uso Típico               | Exemplo               |
|------------|--------------|--------------------------|-----------------------|
| `escreva`  | Sim          | Resultados finais        | `escreva "Média: {media}"` |
| `imprima`  | Não          | Progresso e animações    | `imprima "."` (loading) |

```potigol
# Exemplo combinado
imprima "Processando"
para i de 1 até 5 faça
  imprima "."
  espera(0.5)
fim
escreva " Concluído!"
```

---

### Formatação Avançada

#### Sintaxe

```potigol
escreva "Texto {expressão formato "padrão"}"
```

#### Padrões Comuns

| Tipo     | Exemplo     | Descrição               |
|----------|-------------|-------------------------|
| Decimal  | `%.2f`      | 2 casas decimais        |
| Inteiro  | `%04d`      | Preenche com zeros      |
| Texto    | `%-10s`     | Alinhamento à esquerda  |

```potigol
preço = 49.9
quantidade = 3

# Formatação monetária
escreva "Total: R$ {(preço * quantidade) formato "%8.2f"}"  
# Saída: "Total: R$   149.70"

# Formatação condicional
escreva "Status: {se quantidade > 2 então "OK" senão "ESTOQUE BAIXO" fim}"
```

---


## :material-code-braces: Interpolação de Textos

### Sintaxe Básica

```potigol
"Texto {expressão} mais texto"
```

### Recursos Avançados

- **Expressões arbitrárias**: `{a + b * c}`
- **Chamada de funções**: `{calcular_total()}`
- **Formatação**: `{valor formato "padrão"}`
- **Condicionais**: `{se condição então X senão Y fim}`

```potigol
# Exemplo completo
nome = "Maria"
saldo = 1250.75
limite = 1000

escreva "
Cliente: {nome.maiúsculo}
Saldo: R$ {saldo formato "%.2f"}
Status: {se saldo > limite então "Dentro" senão "Fora" fim} do limite
"
```

---

## :material-alert-octagon: Armadilhas Comuns

### 1. Tipo Incorreto na Leitura

```poti
# Erro ao ler texto como número
var entrada := leia_inteiro  # Se usuário digitar "abc"
```

### 2. Esquecer que `imprima` não quebra linha

```poti
imprima "Carregando"
para i de 1 até 3 faça
  imprima "."  # Saída: Carregando...
fim
# Adicione quebra manual
escreva ""
```

### 3. Leitura mista

```poti
# Leitura mista requer cuidado
escreva "Digite nome e idade:"
nome = leia_texto      # Lê linha inteira!
idade = leia_inteiro   # Nunca executado

# Solução: ler tudo como texto e converter
dados = leia_texto.divida
nome = dados[1]
idade = dados[2].inteiro
```

---

## :material-book-open: Exemplo Completo

```potigol
# Calculadora de IMC
escreva "CALCULADORA DE IMC"
escreva "-----------------"

imprima "Digite peso (kg): "
peso = leia_real

imprima "Digite altura (m): "
altura = leia_real

imc = peso / (altura ^ 2)

escreva """
Resultado:
- Peso: {peso formato "%.1f"} kg
- Altura: {altura formato "%.2f"} m
- IMC: {imc formato "%.1f"}
"""
```
