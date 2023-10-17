---
sort: 10
---

# Instalação local do Potigol

As instruções a seguir permitem que você instale o Potigol localmente em um ambiente Debian GNU/Linux, usando a linha de comandos do sistema. Ocasionalmente, são incluídas alternativas de comandos para Windows.

Ao final, você deve conseguir escrever códigos Potigol e executá-los localmente.

## 🕑 Pré-requisitos

Para que o Potigol funcione corretamente, temos antes que instalar algumas coisas.

- [Java Runtime Enviroment](https://www.java.com/pt-BR/download/): o sistema do Potigol é escrito em Java e compactado no formato Jar. É a JRE que vai permitir com que as instruções escritas em Potigol sejam interpretadas corretamente.
- [Unzip](https://linux.die.net/man/1/unzip): quando o download do Potigol é feito, o arquivo baixado é zipado. Usaremos o Unzip na linha de comandos para descompactá-lo.


## 🦐 Instalação do Potigol 

### 🧪 Teste do Java

Antes de seguir, é importante verificar se o JDK foi instalá-do corretamente. Na linha de comandos, digite:

```terminal
java -version
```

#### 🖥️ comportamento esperado

Espera-se que o Terminal retorne a versão da JRE instalada no sistema:

```terminal
openjdk version "17.0.7" 2023-04-18 LTS
OpenJDK Runtime Environment Microsoft-7626293 (build 17.0.7+7-LTS)
OpenJDK 64-Bit Server VM Microsoft-7626293 (build 17.0.7+7-LTS, mixed mode, sharing)
```

Caso não tenha recebido algo parecido, verifique se a JRE foi instalada corretamente e reinstale-a, caso necessário.

### ⬇️ Download do Potigol
Baixe a [versão mais recente do Potigol](https://github.com/potigol/Potigol/releases/latest).

Descompacte o arquivo recém-baixado digitando o seguinte comando no Terminal:

```terminal
unzip potigol.zip
```

#### 🖥️ comportamento esperado
```terminal
Archive:  potigol.zip
  inflating: configpotigol.bat       
  inflating: exec.bat                
  inflating: exec.sh                 
  inflating: potigol.bat             
  inflating: potigol.css             
  inflating: potigol.ico             
  inflating: potigol.jar             
  inflating: potigol.png    
```

## Escrevendo em Poti 🦐
Para executar o Editor de Código Potigol, digite na linha de comandos:

```terminal
java -jar epotigol.jar
```

- No Windows basta executar `epotigol.bat`.

#### 🦐 Teste de execução

Para verificar se tudo correu bem até aqui, considere criar um arquivo chamado `olamundo.poti` e adicionar o seguinte conteúdo a ele:

```potigol
escreva "Olá, mundo! 🦐"
```

Este é um pequeno programa Potigol. Para executá-lo, digite o seguinte comando no Terminal:

```terminal
java -jar potigol.jar olamundo.poti
```

- No Windows basta usar `potigol olamundo.poti`.


#### 🖥️ comportamento esperado
```terminal
Olá, mundo! 🦐
```

Se a linha de comandos agiu como esperado, você acabou de se livrar da maldição e tem um ambiente pronto para desenvolver em Potigol 🦐.

🤝