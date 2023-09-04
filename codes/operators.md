# Dia 01 - Data types (Tipos de dados)

---

> **Observação**: _As instruções são baseadas em Java, contudo, você também verá por aqui variações em `Go` `Python`
e `JS`, fique tranquilo._ : )

## Objetivo

Hoje vamos trabalhar com operadores aritiméticos. 

**Tarefa:**
Dado o preço da refeição (custo base de uma refeição), 
a porcentagem da gorjeta (a porcentagem do preço da refeição adicionada como gorjeta) e a porcentagem do imposto 
(a porcentagem do preço da refeição adicionada como imposto) para uma refeição, encontre e imprima o custo total da refeição . 
Arredonde o resultado para o número inteiro mais próximo.


### Formato de entrada

Há 3 linhas de entrada numérica:
A primeira linha tem um double, _meal_cost_ (custo da refeição antes de impostos e gorjeta).
A segunda linha tem um número inteiro,_tip_percent_ (a porcentagem desendo adicionado como dica).
A terceira linha tem um número inteiro, _tax_percent_ (a porcentagem desendo adicionado como imposto).

### Exemplo de entrada

```text
     12.00
     20
     8
```

### Exemplo de saída

```text
     15
```
<br>

#### Programa: Operators (Operadores)

**Resposta em Java:**
```java
class Result {

    /*
     * Complete the 'solve' function below.
     *
     * The function accepts following parameters:
     *  1. DOUBLE meal_cost
     *  2. INTEGER tip_percent
     *  3. INTEGER tax_percent
     */

    public static void solve(double meal_cost, int tip_percent, int tax_percent) {
        // Write your code here
        double total_cost = 0.0;
        double tip = meal_cost * tip_percent / 100;
        double tax = meal_cost * tax_percent / 100;

        total_cost = meal_cost + tip + tax;

        System.out.println((int) Math.round(total_cost));
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        double meal_cost = Double.parseDouble(bufferedReader.readLine().trim());

        int tip_percent = Integer.parseInt(bufferedReader.readLine().trim());

        int tax_percent = Integer.parseInt(bufferedReader.readLine().trim());

        Result.solve(meal_cost, tip_percent, tax_percent);

        bufferedReader.close();
    }
}
```