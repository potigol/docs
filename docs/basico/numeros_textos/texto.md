# Texto
````scala
"abc".qual_tipo                   # "Texto"
"123".inteiro                     # 123
"12abc3".inteiro                  # 12
"abc".inteiro                     # 0
"abc"[2]                          # 'b' (caractere na posição 2)

"12.3".real                       # 12.3
"12a.3".real                      # 12.0
"abc".real                        # 0.0

"ab" + "cd"                       # "abcd"  (concatenação)
"abcb" - "bd"                     # "acb"   (subtração)

"abc".tamanho                     # 3
"abc".posição('b')                # 2 (posição de 'b' em "abc")
"abc".posição('d')                # 0
"abc".contém('a')                 # verdadeiro (testa de 'a' está em "abc")
"abc".contém('d')                 # falso

"Abc".maiúsculo                   # "ABC"
"Abc".minúsculo                   # "abc"
"Abc".inverta                     # "cbA"
"cab".ordene                      # "abc"
"abc".junte("-")                  # "a-b-c"
"abc".junte("[", ", ", "]")       # "[a, b, c]"

"Um texto".divida                 # ["Um", "texto"]
"Um texto".divida("t")            # ["Um ", "ex", "o"]
"Um texto".lista                  # ['U', 'm', ' ', 't', 'e', 'x', 't', 'o']

"abc".cabeça                      # 'a'  (primeiro caractere de "abc")
"abc".cauda                       # "bc" ("abc" sem o primeiro caractere)
"abc".último                      # 'c'  (último caractere de "abc")
"abcde".pegue(3)                  # "abc" (primeiros 3 caracteres)
"abcde".descarte(3)               # "de"  (sem os primeiros 3 caracteres)

"abcb".selecione(letra => letra <> 'c')          # "abb" ("abcb" sem 'c')
"abc".injete(0)((x,y) => x + y)                # 294   (97 + 98 + 99)
"abc".injete("")((x,y) => x + "-" + y)         # "-a-b-c"

"abcb".descarte_enquanto(letra => letra<> 'c')  # "cb" (descarte caracteres antes de 'c')
"abcb".pegue_enquanto(letra => letra< 'c')      # "ab" (pegue caracteres antes de 'c')

x = "abc".remova(2)               # x = "ac"  (remove o caractere na posição 2)
y = "abc".insira(3, 'd')          # y = "abdc" (insere 'd' na posição 2)
z = "abc".insira(3, "def")        # z = "abdefc" (insere "def" na posição 2)
````
