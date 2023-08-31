# Dia 00 - Hello World (Olá Mundo)

---

> **Observação**: _As instruções são baseadas em Java, contudo, você também verá por aqui variações em `Go` `Python`
e `JS`, fique tranquilo._ : )

## Objetivo

Neste desafio, revimos alguns conceitos básicos que ajudarão você a começar esta série. Você precisará usar a mesma
sintaxe (ou semelhante) para ler a entrada e escrever a saída em desafios em todo o HackerRank.

**Tarefa**
Para completar este desafio, você deve salvar uma linha de entrada de stdin em uma variável, imprimir `Hello, World`
numa única linha e, finalmente, imprimir o valor da sua variável numa segunda linha.

### Formato de entrada

Uma única linha de texto denotando _inputString_ (a variável cujo conteúdo deve ser impresso).

### Formato de saída

Imprima `Hello, World` na primeira linha e o conteúdo de _inputString_ na segunda linha.

### Exemplo de entrada

```text
     Welcome to 30 Days of Code!
```

### Exemplo de saída

```text
     Hello, World.
     Welcome to 30 Days of Code!
```


#### Programa: Hello World (Olá Mundo)

**Resposta em Java:**
```java
public class Solution {
    public static void main(String[] args) {
        // Create a Scanner object to read input from stdin.
        Scanner scan = new Scanner(System.in);

        // Read a full line of input from stdin and save it to our variable, inputString.
        String inputString = scan.nextLine();

        // Close the scanner object, because we've finished reading 
        // all of the input from stdin needed for this challenge.
        scan.close();

        // Print a string literal saying "Hello, World." to stdout.
        System.out.println("Hello, World.");
        System.out.print(inputString);
    }
}
```