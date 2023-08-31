# Dia 01 - Data types (Tipos de dados)

---

> **Observação**: _As instruções são baseadas em Java, contudo, você também verá por aqui variações em `Go` `Python`
e `JS`, fique tranquilo._ : )

## Objetivo

Hoje estamos discutindo tipos de dados. Veja o que são tipos de dados:
* [Tipos de dados em Java](https://www.javatpoint.com/pt/tipo-de-dado-em-java);
* [Tipos de dados em Go](https://astaxie.gitbooks.io/build-web-application-with-golang/content/pt-br/02.2.html);
* [Tipos de dados em Python](https://pythonacademy.com.br/blog/tipos-de-variaveis-no-python);
* [Tipos de dados em JS](https://ricardo-reis.medium.com/tipos-de-dados-javascript-a1f6f498a7d4);

**Tarefa:**
Complete o código no editor abaixo. As variáveis, i, d e s já estão declarados e inicializados para você. Você deve:

1. Declarar 03 variáveis: uma do tipo int, uma do tipo double e uma do tipo String. 
2. Ler 3 linhas de entrada do stdin (de cordo com a sequência fornecida na seção Formato de entrada abaixo) 
e inicialize suas 3 variáveis. 

3. Use o operador (+) para realizar as seguintes operações:
- 1. Imprima a somar de _i_ mais sua variável int em uma nova linha.
- 2. Imprima a soma de _d_ mais sua variável dupla em uma escala de uma casa decimal em uma nova linha.
- 3. Concatenar _s_ com a string que você leu como entrada e imprime o resultado em uma nova linha.

### Formato de entrada

A primeira linha contém um número inteiro que você deve somar com o _i_.
A segunda linha contém um **double** que você deve somar com o _d_.
A terceira linha contém uma string com o qual você deve concatenar com o _s_.

### Formato de saída

Imprima a soma de ambos os números inteiros na primeira linha, 
a soma de ambos os doubles (escalada para 1 casa decimal) na segunda linha e, 
em seguida, as duas strings concatenadas na terceira linha

### Exemplo de entrada

```text
     12
     4.0
     is the best place to learn and practice coding!
```

### Exemplo de saída

```text
     16
     8.0
     HackerRank is the best place to learn and practice coding!
```
<br>

#### Programa: Data Types (Tipos de dados)

**Resposta em Java:**
```java
public class Solution {

    public static void main(String[] args) {
        int i = 4;
        double d = 4.0;
        String s = "HackerRank ";

        Scanner scan = new Scanner(System.in);

        /* Declare second integer, double, and String variables. */
        int i2 = 0;
        double d2 = 0.0;
        String s2 = null;

        /* Read and save an integer, double, and String to your variables.*/

        i2 = scan.nextInt();
        d2 = scan.nextDouble();

        scan.nextLine();
        s2 = scan.nextLine();

        // Note: If you have trouble reading the entire String, please go back and review the Tutorial closely.

        /* Print the sum of both integer variables on a new line. */
        System.out.println(i + i2);

        /* Print the sum of the double variables on a new line. */
        System.out.println(d + d2);
        
        /* Concatenate and print the String variables on a new line; 
        	the 's' variable above should be printed first. */
        System.out.println(s.concat(s2));

        scan.close();
    }
}
```