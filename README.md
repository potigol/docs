# Documentação da Linguagem Potigol
[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/potigol/gitpod)
[![Join the chat at https://gitter.im/potigol/Potigol](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/potigol/Potigol?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Follow us](https://img.shields.io/twitter/follow/potigol.svg?style=social)](http://twitter.com/potigol)
![GitHub Org's stars](https://img.shields.io/github/stars/potigol?style=social)
![GitHub all releases](https://img.shields.io/github/downloads/potigol/potigol/total)
[![Versão](https://img.shields.io/badge/Versão-1.0-green)](https://github.com/potigol/Potigol/releases)

<!--a href="hacktoberfest"><img src="https://hacktoberfest.digitalocean.com/_nuxt/img/logo-hacktoberfest-full.f42e3b1.svg" width=250></a-->

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io#https://github.com/potigol/gitpod)
[![IFRN](logo_ifrn_40.png)](https://www.ifrn.edu.br)


```tip
Potigol é ...
 Uma linguagem moderna (funcional) para aprender a programar.
```

Faça o *[Download](https://github.com/potigol/Potigol/releases)* e veja como *[Instalar](https://github.com/potigol/Potigol#como-usar)*

## Exemplos

 - [Mais de 700 problemas de programação resolvidos na linguagem Potigol](https://potigol.github.io/beecrowd/)


```python
# Imperativo
escreva "Olá Mundo!"

# Funcional
ola(a: Texto) = escreva "Ola {a}!"
ola("Mundo")

# Orientado a Objetos
tipo Ola
  nome: Texto
  saudação() = "Olá {nome}!"
fim

olamundo = Ola("Mundo")
escreva olamundo.saudação
```

```python
frutas = ["maçã", "banana", "morango"]
escreva frutas.ordene                                # ["banana", "maçã", "morango"]
escreva frutas.selecione(fruta => fruta > "goiaba")  # ["maçã", "morango"]
```

## Características
 * Projetada para ser usada por alunos iniciantes
 * Tipagem estática com inferência de tipos
 * Palavras-chave em português
 * Multiparadigma
 * Estímulo ao paradigma funcional: valores imutáveis, casamento de padrões, funções como valores

## Topicos

 * [Instalação](instalacao)
 * [Básico](basico) entrada, saída, tipos básicos, variáveis
 * [Números e Textos](numeros_textos)
 * [Estruturas de Decisao](estruturas/decisao) se, escolha
 * [Estruturas de Repetição](estruturas/repeticao) para, enquanto
 * [Funções](funcoes)
 * [Tipos Compostos](lista_tupla) listas, tuplas
 * [Classes](tipos)
 * [Programação Funcional](funcional) funções de alta ordem, imutabilidade, casamento de padrões
 * [Programação Orientada a Objetos](objetos) tipos (classes), tipos abstratos (classes abstratas e interfaces), atributos, métodos, herança  

## Contato

 - Siga-nos no twitter: *[@potigol](https://twitter.com/potigol)*
