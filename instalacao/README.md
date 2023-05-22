---
sort: 10
---

As instruções abaixo ajudam a instalar o Potigol.

## Pré-requisitos
- [Java Runtime Enviroment](https://www.java.com/pt-BR/download/)
- [Unzip](https://linux.die.net/man/1/unzip)

## Instalação

- Verifique se o Java foi instalado corretamente digitando `java -version` no Terminal.
#### 🖥️ comportamento esperado

Espera-se que o Terminal retorne a versão do JDK instalada no sistema:

```terminal
openjdk version "17.0.7" 2023-04-18 LTS
OpenJDK Runtime Environment Microsoft-7626293 (build 17.0.7+7-LTS)
OpenJDK 64-Bit Server VM Microsoft-7626293 (build 17.0.7+7-LTS, mixed mode, sharing)
```

Caso não tenha recebido algo parecido, verifique se o JDK foi instalado corretamente e reinstale-o, caso necessário.

### Download do Potigol
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
Para executar o Editor de Código Potigol, digite no Terminal:

```terminal
java -jar epotigol.jar
```

- No Windows basta executar `epotigol.bat`.

#### Teste dos coomedores de camarão

Para verificar se tudo correu bem até aqui, considere criar um arquivo chamado `olamundo.poti` e adicionar o seguinte conteúdo a ele:

```potigol
escreva "Olá, mundo! 🦐"
```

Este é um pequeno programa Potigol. Para executá-lo, digite o seguinte comando no Terminal:

```terminal
java -jar potigol.jar arquivo.poti
```

- No Windows basta usar `potigol arquivo.poti`.


#### 🖥️ comportamento esperado
```terminal
Olá, mundo! 🦐
```
