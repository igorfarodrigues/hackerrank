# Dia 04 - Class Vs. Instance (Classes Vs. Instâncias)

---

> **Observação**: _As instruções são baseadas em Java, contudo, você também verá por aqui variações em `Go` `Python`
e `JS`, fique tranquilo._ : )

## Objetivo

Neste desafio aprenderemos a diferença entre uma classe e uma instância; 
por ser um conceito Orientado a Objetos.

**Tarefa:**
Escreva uma classe Person com uma variável de instância, _**age**_, 
e um construtor que recebe um número inteiro, _**initialAge**_, como parâmetro. 
O construtor deve atribuir _**initialAge**_ para _**age**_ depois de confirmar o argumento passado comonão é negativo; 
se um argumento negativo for passado como _**initialAge**_, o construtor deve definir _**age**_para _**0**_ e 
imprimir _**Age is not valid, setting age to 0.**_. Além disso, você deve escrever os seguintes métodos de instância:

1. yearPasses() deve aumentar o _**age**_ variável de instância por _**1**_. 
2. amIOld() deve executar as seguintes ações condicionais:
- Se, _**age < 13**_ imprimir _**You are young.**_. 
- See, _**age >= 13 and age < 18**_ imprimir _**You are a teenager.**_. 
- Caso contrário, imprima _**You are old.**_.

Para ajudá-lo a aprender por exemplo e completar este desafio, 
grande parte do código é fornecida para você, mas você escreverá tudo no futuro. 
O código que cria cada instância da sua classe Person está no método principal. 
Não se preocupe se você ainda não entendeu tudo!

### Formato de entrada

A entrada é tratada pelo código stub no editor.

A primeira linha contém um número inteiro, _**T**_ (o número de casos de teste) e o _**T**_ 
cada linha subsequente contém um número inteiro denotando o _**age**_ de uma instância _**Person**_.

### Formato de saída

Preencha as definições de métodos fornecidas no editor para que atendam às especificações descritas acima; 
o código para testar seu trabalho já está no editor. 
Se seus métodos forem implementados corretamente, cada caso de teste imprimirá _2_ ou _3_ linhas 
(dependendo se um valor válido ou não _**initialAge**_ foi passado para o construtor).

### Exemplo de entrada

```text
    4
   -1
   10
   16
   18
```

### Exemplo de saída

```text
     Age is not valid, setting age to 0.
     You are young.
     You are young.
     
     You are young.
     You are a teenager.
     
     You are a teenager.
     You are old.
     
     You are old.
     You are old.
```
<br>

#### Programa: Data Types (Tipos de dados)

**Resposta em Java:**
```java
public class Person {
    private int age;

    public Person(int initialAge) {
        // Add some more code to run some checks on initialAge
        if(initialAge < 0) {
            initialAge = 0;
            System.out.println("Age is not valid, setting age to 0.");
        }
        this.age = initialAge;
    }

    public void amIOld() {
        // Write code determining if this person's age is old and print the correct statement:
        if (age < 13){
            System.out.println("You are young.");
        } else if (age < 18){
            System.out.println("You are a teenager.");
        } else {
            System.out.println("You are old.");
        }
    }

    public void yearPasses() {
        age += 1;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int T = sc.nextInt();
        for (int i = 0; i < T; i++) {
            int age = sc.nextInt();
            Person p = new Person(age);
            p.amIOld();
            for (int j = 0; j < 3; j++) {
                p.yearPasses();
            }
            p.amIOld();
            System.out.println();
        }
        sc.close();
    }
}
```