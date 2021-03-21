# Programação Orientada a Objetos

lasses são definidas através de tipos. Os tipos são compostos por atributos e métodos (funções). Todos elementos de um tipo são públicos, mas não é possível alterar diretamente um atributo.

### Declaração de um Tipo (Classe)
````scala
tipo «Tipo»
  «[var]» «lista de atributos do construtor» : «tipo»
  «[var]» «atributos» = «valor»
  «métodos»
fim

«obj» = «Tipo»(«lista de valores do construtor»)
«obj».«atributo»
«obj».«método»
````

#### Exemplo

````ruby
tipo Quadrado
  lado: Inteiro
  area() = lado * lado
  perimetro() = 4 * lado
fim

q1 = Quadrado(10)
escreva q1.area
escreva q1.perimetro
````
