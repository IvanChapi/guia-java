# Sintaxi bàsica

## Variables i tipus de dades

Java és de tipat estàtic: cal indicar el tipus en declarar cada variable.

| Tipus | Descripció | Exemple |
|-------|------------|---------|
| `int` | Nombre enter | `int edat = 20;` |
| `double` | Nombre decimal | `double preu = 9.99;` |
| `boolean` | Cert o fals | `boolean actiu = true;` |
| `char` | Un caràcter | `char lletra = 'A';` |
| `String` | Cadena de text | `String nom = "Anna";` |

!!! note "Nota"
    `String` no és un tipus primitiu, sinó una **classe**. Per això s'escriu amb majúscula inicial.

## Estructures condicionals

```java
int nota = 7;

if (nota >= 9) {
    System.out.println("Excel·lent");
} else if (nota >= 5) {
    System.out.println("Aprovat");
} else {
    System.out.println("Suspés");
}
```

## Bucles

=== "for"

    ```java
    for (int i = 1; i <= 5; i++) {
        System.out.println("Volta " + i);
    }
    ```

=== "while"

    ```java
    int i = 1;
    while (i <= 5) {
        System.out.println("Volta " + i);
        i++;
    }
    ```

!!! warning "Compte amb els bucles infinits"
    Si oblides actualitzar la variable de control (`i++`), el bucle `while` **no acabarà mai**.

## Llegir dades per teclat

```java
import java.util.Scanner;

public class Salutacio {
    public static void main(String[] args) {
        Scanner teclat = new Scanner(System.in);
        System.out.print("Com et diuen? ");
        String nom = teclat.nextLine();
        System.out.println("Hola, " + nom + "!");
        teclat.close();
    }
}
```

!!! tip "Bona pràctica"
    Utilitza noms de variables **descriptius** i segueix la convenció *camelCase* (`nomUsuari`, `totalVendes`).

??? example "Exercici proposat"
    Escriu un programa que demane un nombre i mostre la seua **taula de multiplicar** del 1 al 10.
