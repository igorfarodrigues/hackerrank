# Dia 05 - Loops (Laços de repetição)

---

> **Observação**: _As instruções são baseadas em Java, contudo, você também verá por aqui variações em `Go` `Python`
e `JS`, fique tranquilo._ : )

## Objetivo

Neste desafio, usaremos loops para fazer algumas contas.

**Tarefa:**
Dado um número inteiro, _**N**_, imprima seu primeiro _10_ múltiplos. 
Cada múltiplo _n X i_ (onde _1 <= i <= 10_) deve ser impresso em uma nova linha no formato: _n x i = result_.

### Formato de entrada

Um único número inteiro, _**N**_.

### Formato de saída

Imprimir _10_ linhas de saída; cada linha _i_ (onde _1 <= i <= 10_) contém o _result_ de _n X i_ na forma:
_**n x i = result**_.

### Exemplo de entrada

```text
     2
```

### Exemplo de saída

```text
    2 x 1 = 2
    2 x 2 = 4
    2 x 3 = 6
    2 x 4 = 8
    2 x 5 = 10
    2 x 6 = 12
    2 x 7 = 14
    2 x 8 = 16
    2 x 9 = 18
    2 x 10 = 20
```
<br>

#### Programa: Data Types (Tipos de dados)

**Resposta em Java:**
```java
public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(bufferedReader.readLine().trim());

        int i = 1;
        while (i <= 10){
            System.out.println(n + " x " + i + " = " + n * i);
            i++;
        }

        bufferedReader.close();
    }
}
```