# Tuplas

*(Coleções ordenadas e imutáveis de elementos heterogêneos)*  

---

### **O que são Tuplas?**  
Em Potigol, **tuplas** são estruturas de dados que armazenam coleções **ordenadas** e **imutáveis** de elementos, podendo conter valores de tipos diferentes. Elas são ideais para agrupar dados relacionados de forma fixa, como coordenadas, registros ou retornos múltiplos de funções.

---

### **Características Principais**  
- **Imutáveis**: Não podem ser alteradas após a criação.  
- **Heterogêneas**: Aceitam elementos de tipos diferentes.  
- **Tamanho fixo**: O número de elementos é definido na criação.  
- **Acesso por posição**: Elementos são acessados via métodos como `.primeiro`, `.segundo`, etc.  

---

### **Criação de Tuplas**  
```potigol
# Tupla com 3 elementos (Inteiro, Texto, Real)
t = (2015, "potigol", 1.0)  
```

---

### **Operações Básicas**  

#### **Acesso a Elementos**  
Use métodos como `.primeiro`, `.segundo`, `.terceiro`, etc., conforme a posição:  
```potigol
t = (2015, "potigol", 1.0)  
t.primeiro    # 2015  
t.segundo     # "potigol"  
t.terceiro    # 1.0  
```

---

### **Casos de Uso Comuns**  

#### **Retorno Múltiplo de Funções**  
```potigol
função divisão_segura(a: Inteiro, b: Inteiro) -> (Inteiro, Texto)  
  se b == 0 então  
    (0, "Erro: divisão por zero")  
  senão  
    (a div b, "Sucesso")  
  fim  
fim  

resultado = divisão_segura(10, 2)  
escreva resultado.primeiro   # 5  
escreva resultado.segundo    # "Sucesso"  
```

#### **Agrupamento de Dados**  
```potigol
ponto = (3.5, 4.2)  # Coordenada (x, y)  
usuario = ("Ana", 30, "ana@email.com")  
```

---

### **Vantagens das Tuplas**  
- **Segurança**: Garantia de que os dados não serão modificados acidentalmente.  
- **Semântica clara**: Indicam que os elementos têm um relacionamento fixo (ex: coordenadas x e y).  
- **Eficiência**: São otimizadas para leitura em comparação a listas mutáveis.  

---

### **Exemplo Completo**  
```potigol  
# Definição e uso de uma tupla  
config = ("Potigol", 2023, 2.7)  

escreva "Linguagem: {config.primeiro}"  
escreva "Ano: {config.segundo}"  
escreva "Versão: {config.terceiro}"  

# Saída:  
# Linguagem: Potigol  
# Ano: 2023  
# Versão: 2.7  
```  

--- 

✂️ **Dica**: Use tuplas quando precisar garantir a integridade de dados agrupados ou retornar múltiplos valores de forma organizada!

