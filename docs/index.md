# Documentação da Linguagem Potigol

<div class="grid" markdown>
![Logo Potigol](assets/favicon.ico){ align=left width=200}

:fontawesome-solid-language: **Linguagem moderna** para aprender a programar.  
:fontawesome-solid-heart: **Multiparadigma**: Funcional, Imperativo e Orientado a Objetos  
:fontawesome-solid-graduation-cap: **Foco educacional**: Sintaxe intuitiva em português  

</div>

---

## :material-feature-search-outline: Principais Recursos

<div class="grid cards" markdown>

- :material-school-outline: **Para Iniciantes**  
  Sintaxe intuitiva · Erros descritivos · Debugging fácil

- :flag_br: **Sintaxe em Português**  
  `escreva` · `leia_inteiro` · `verdadeiro` · `escolha`

- :material-function-variant: **Programação Funcional**  
  Imutabilidade · Funções puras · Recursão · Casamento de Padrões

- :material-cube-outline: **Tipagem Forte**  
  Inferência de tipos · Conversão segura · Checagem estática

</div>

---

## :material-code-json: Olá Mundo Multiparadigma

=== ":material-flash: Imperativo"
    ```poti
    # Estilo tradicional
    escreva "Olá Mundo!"
    ```

=== ":material-function: Funcional"
    ```poti
    # Abordagem declarativa
    saudação = (nome: Texto) => "Ola {nome}!"
    escreva saudação("Mundo")
    ```

=== ":material-cube: Orientado a Objetos"
    ```poti
    # Uso de classes
    tipo Ola
      nome: Texto
      saudação() = "Olá {nome}!"
    fim

    olamundo = Ola("Mundo")
    escreva olamundo.saudação
    ```

---

## :material-play-box-multiple: Experimente Agora

<div class="grid" markdown>

[![Abrir no Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/potigol/potigol-image){ .md-button .md-button--primary }

:fontawesome-solid-download: **[Download v1.0](https://github.com/potigol/Potigol/releases)**  
:fontawesome-solid-book: **[Guia de Instalação](instalacao.md)**

</div>

    # Exemplo de execução
    $ potigol ola.poti
    Olá Mundo!

---

## :material-book-open-page-variant: Tópicos da Documentação

1. **Básico**
    - [Instalação](instalacao.md)
    - [Primeiros Passos](basico/primeiros_passos.md)
    - [Variáveis](basico/variaveis.md)
    - [Tipos Básicos](basico/tipos_basicos.md)

2. **Estruturas**
    - [Condicionais](estruturas/decisao/README.md)
    - [Repetição](estruturas/repeticao/README.md)
    - [Funções](funcoes/README.md)

3. **Paradigmas**
    - [Programação Funcional](funcional/README.md)
    - [Orientação a Objetos](objetos/README.md)

4. **Avançado**
    - [Pattern Matching](funcional/README.md)
    - [Funções de Alta Ordem](funcional/README.md)


---

## :material-frequently-asked-questions: FAQ Rápido

??? question "Para quem é o Potigol?"
    Ideal para estudantes brasileiros iniciantes em programação e educadores que querem ensinar conceitos modernos de forma acessível.

??? question "Posso usar em produção?"
    Foco educacional, mas adequado para scripts simples. Para sistemas complexos, considere linguagens como Elixir ou Python.

??? question "Como comparar com Portugol?"
    ## :material-scale-balance: Comparação Detalhada: Potigol vs Portugol

    <div class="grid" markdown>

    | **Característica**         | **Potigol** :material-new-box:               | **Portugol** :classical_building:      |
    |---------------------------|------------------------------------|----------------------------------------|
    | **Paradigmas**            | Multiparadigma (Funcional, OO, Imperativo) | Principalmente Imperativo           |
    | **Sistema de Tipos**      | Estático com Inferência de tipos          | Estático sem Inferência                       |
    | **Sintaxe**               | Moderna com palavras-chave em PT-BR<br>`escreva`, `para`, `caso` | Tradicional baseada em pseudocódigo<br>`escreva`, `leia`, `se` |
    | **Recursos Avançados**    | :material-check: Pattern Matching<br>:material-check: Funções de Alta Ordem<br>:material-check: Imutabilidade | :material-close: Foco em estruturas básicas |
    | **Orientação a Objetos**  | Classes, Herança, Polimorfismo     | Não suportado                         |
    | **Ambiente de Desenvolvimento** | [Gitpod](https://gitpod.io), VS Code, CLI | IDEs locais (Visualg, Portugol Studio) |
    | **Casos de Uso**          | Educação moderna, prototipagem rápida | Introdução absoluta à programação    |

    </div>

    ---

    ### :material-code-braces: Exemplo Comparativo

    === "Potigol (Funcional)"
        ```poti
        # Cálculo fatorial com recursão e pattern matching
        fatorial(n: Inteiro): Inteiro = escolha n
          caso 0 => 1
          caso _ => n * fatorial(n - 1)
        fim
        
        escreva fatorial(5)  # 120
        ```

    === "Portugol (Imperativo)"
        ```portugol
        algoritmo "Fatorial"
        var
            n, resultado: inteiro
        inicio
            resultado <- 1
            leia(n)
            para i de 1 ate n faca
                resultado <- resultado * i
            fimpara
            escreva(resultado)
        fimalgoritmo
        ```

    ---

    ### :material-chart-bar: Quando Escolher?

    | **Escolha Potigol se...**               | **Prefira Portugol para...**        |
    |----------------------------------------|-------------------------------------|
    | Quer ensinar conceitos modernos         | Introdução absoluta à lógica        |
    | Precisa de recursos funcionais/OO       | Apenas algoritmos imperativos       |
    | Deseja integração com ferramentas atuais | Ambientes educacionais tradicionais |
    | Busca comunidade ativa para suporte     | Material didático consolidado       |

    :fontawesome-solid-lightbulb: **Dica:** Potigol é excelente para transição entre programação básica e linguagens profissionais como Python ou JavaScript.
