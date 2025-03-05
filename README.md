# Documentação da Linguagem Potigol
[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/potigol/gitpod)
[![Join the chat at https://gitter.im/potigol/Potigol](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/potigol/Potigol?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Follow us](https://img.shields.io/twitter/follow/potigol.svg?style=social)](http://twitter.com/potigol)
![GitHub Org's stars](https://img.shields.io/github/stars/potigol?style=social)
![GitHub all releases](https://img.shields.io/github/downloads/potigol/potigol/total)
[![Versão](https://img.shields.io/badge/Versão-1.0-green)](https://github.com/potigol/Potigol/releases)

<!--a href="hacktoberfest"><img src="https://hacktoberfest.digitalocean.com/_nuxt/img/logo-hacktoberfest-full.f42e3b1.svg" width=250></a-->

<!-- [![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io#https://github.com/potigol/gitpod) -->

<!-- [![IFRN](logo_ifrn_40.png)](https://www.ifrn.edu.br) -->

```tip
Potigol é ...
 Uma linguagem moderna (funcional) para aprender a programar.
```

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/potigol/potigol-image)

:point_up: Quer testar? É só clicar no botão e começar a programar. Ou 
faça o *[Download](https://github.com/potigol/Potigol/releases)* e veja como *[Instalar](https://github.com/potigol/Potigol#como-usar)*


```portugol
# Imperativo
escreva "Olá Mundo!"

# Funcional
ola = (nome: Texto) => "Ola {nome}!"
escreva ola("Mundo")

# Orientado a Objetos
tipo Ola
  nome: Texto
  saudação() = "Olá {nome}!"
fim

olamundo = Ola("Mundo")
escreva olamundo.saudação
```

```portugol
soma(a, b: Inteiro) = a + b

escreva "Digite dois números:"
x, y = leia_inteiro
escreva "{x} + {y} = {soma(x, y)}"
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
 * Tipos Compostos: [Listas](lista_tupla/listas), [Tuplas](lista_tupla/listas)
 * [Classes](tipos)
 * [Programação Funcional](funcional) funções de alta ordem, imutabilidade, casamento de padrões
 * [Programação Orientada a Objetos](objetos) tipos (classes), tipos abstratos (classes abstratas e interfaces), atributos, métodos, herança

## Exemplos
[![Beecrowd](https://www.beecrowd.com.br/judge/img/5.0/logo-beecrowd.png)](https://potigol.github.io/beecrowd/)

[![Soluções](https://img.shields.io/badge/Problemas%20Resolvidos-840-blue)]([https://github.com/potigol/beecrowd/commits/master](https://potigol.github.io/beecrowd/))

 - [Mais de 800 problemas de programação resolvidos na linguagem Potigol](https://potigol.github.io/beecrowd/) 

## Contato

 - Siga-nos no twitter: *[@potigol](https://twitter.com/potigol)*
