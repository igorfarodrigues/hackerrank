# Dia 06 - Review loop (Revisão: laços)

---

> **Observação**: _As instruções são baseadas em Java, contudo, você também verá por aqui variações em `Go` `Python`
e `JS`, fique tranquilo._ : )

## Objetivo

Hoje vamos aprofundar o nosso conhecimento sobre _strings_, combinando-o com o que já aprendemos sobre _loops_.

**Tarefa:**
Dada uma string, _S_, de comprimento _N_ que é indexado de _0_ para _N - 1_, imprima seus caracteres indexados 
pares e ímpares comos _2_ _strings_ separadas por espaço em uma única linha (veja o exemplo abaixo para mais detalhes).

Observação: _0_ é considerado um índice par.

Exemplo

```text
     s = adbecf
```

```text
     Imprimir: abc def
```

### Formato de entrada

A primeira linha contém um número inteiro, _**T**_ (o número de casos de teste) e o _**T**_
cada linha _**i**_ do _**T**_ as linhas subsequentes contém uma _string_ _**S**_.


### Formato de saída

Para cada sequência _**S^ĵ**_ (onde _0 <= j <= T -1_), imprimir _**S^ĵ**_ caracteres indexados pares , seguidos por 
um espaço, seguido por _**S^ĵ**_ caracteres indexados ímpares.

### Exemplo de entrada

```text
     2
     Hacker
     Rank
```

### Exemplo de saída

```text
     Hce akr
     Rn ak
```

### Explicação

Caso de teste 0: _**S = "Hacker"**_
```text
     S[0] = "H"
     S[1] = "a"
     S[2] = "c"
     S[3] = "k"
     S[4] = "e"
     S[5] = "r"
```

Os índices pares são, 0, 2 e, 4 e os índices ímpares são 1, 3, e 5. 
Em seguida, imprimimos uma única linha de 2 _strings_ separadas por espaço; 
a primeira _string_ contém os caracteres ordenados de _S_ índices pares (_**Hce**_),
e a segunda _string_ contém os caracteres ordenados de _S_ índices ímpares (_**akr**_).

Caso de teste 1: _**S = "Rank"**_
```text
     S[0] = "R"
     S[1] = "a"
     S[2] = "n"
     S[3] = "k"
```

Os índices pares são 0 e 2, e os índices ímpares são 1 e 3. 
Em seguida, imprimimos uma única linha de 2 _strings_ separadas por espaço; 
a primeira _string_ contém os caracteres ordenados de _S_ índices pares (_**Rn**_), 
e a segunda _string_ contém os caracteres ordenados de _S_ índices ímpares (_**ak**_).


<br>

#### Programa: Data Types (Tipos de dados)

**Resposta em Java:**
```java
public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();

        in.nextLine();

        for(int i = 0; i < n; i++){
            String lineChars = in.nextLine();
            char[] charArray = lineChars.toCharArray();

            for(int j = 0; j < charArray.length; j++){
                if(j % 2 == 0){
                    System.out.print(charArray[j]);
                }
            }

            System.out.print(" ");

            for (int l = 0; l < charArray.length; l++){
                if(l % 2 != 0){
                    System.out.print(charArray[l]);
                }
            }

            System.out.println();
        }

    }
}
```