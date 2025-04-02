---
sort: 65
---

# Tipos (Registros e Classes)

## Registro

```portugol
tipo Pessoa
  nome: Texto
  email: Texto
  idade: Inteiro
fim

joao = Pessoa("Joao", "jo@gmail.com", 20)
escreva joao.nome
escreva joao.idade
escreva joao
```


```portugol
tipo Pessoa
  nome: Texto
  email: Texto
  var idade: Inteiro
fim

joao = Pessoa("Joao", "jo@gmail.com", 20)
escreva joao.nome
escreva joao.idade
joao.idade := 21
escreva joao
```
