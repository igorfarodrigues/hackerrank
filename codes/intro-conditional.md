# Dia 03 - Conditional Statements (Condicionais)

---

> **Observação**: _As instruções são baseadas em Java, contudo, você também verá por aqui variações em `Go` `Python`
e `JS`, fique tranquilo._ : )

## Objetivo

Hoje aprendemos sobre declarações condicionais.

**Tarefa:**
Dado um número inteiro, _n_, execute as seguintes ações condicionais:

- Se _n_ é estranho, imprima _**Weird**_
- Se _n_ é par e está na faixa inclusiva depara, imprimir _**Not Weird**_
- Se _n_ é par e está na faixa inclusiva depara, imprimir _**Weird**_
- Se _n_ é par e maior que, imprimir _**Not Weird**_

Preencha o código stub fornecido em seu editor para imprimir ou não _n_ é estranho.

### Formato de entrada

Uma única linha contendo um número inteiro positivo, _n_.

### Formato de saída

Imprima a soma de ambos os números inteiros na primeira linha, 
a soma de ambos os doubles (escalada para 1 casa decimal) na segunda linha e, 
em seguida, as duas strings concatenadas na terceira linha

### Exemplo de entrada

```text
     3
```

### Exemplo de saída

```text
     3
     Weird
     24
     Not Weird
```
<br>

#### Programa: Data Types (Tipos de dados)

**Resposta em Java:**
```java
public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int N = Integer.parseInt(bufferedReader.readLine().trim());

        if(N % 2 == 0){
            if(N < 6) System.out.println("Not Weird");
            else if (N <= 20) System.out.println("Weird");
            else System.out.println("Not Weird");
        } else {
            System.out.println("Weird");
        }

        bufferedReader.close();
    }
}
```