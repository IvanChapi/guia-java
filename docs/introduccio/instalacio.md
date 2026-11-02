# Instal·lació

## 1. Descarregar el JDK

Pots instal·lar una distribució del JDK com **Eclipse Temurin** (OpenJDK) des de [adoptium.net](https://adoptium.net/){ target=_blank } o la d'[Oracle](https://www.oracle.com/java/technologies/downloads/){ target=_blank }.

!!! warning "Versió recomanada"
    Utilitza una versió **LTS** (suport a llarg termini), com Java **17** o **21**.

## 2. Instal·lar-lo segons el sistema

=== "Windows"

    Descarrega l'instal·lador `.msi` i segueix l'assistent. Marca l'opció d'afegir `JAVA_HOME` al *PATH*.

=== "Linux (Ubuntu/Debian)"

    ```bash
    sudo apt update
    sudo apt install openjdk-21-jdk
    ```

=== "macOS"

    ```bash
    brew install openjdk@21
    ```

## 3. Verificar la instal·lació

```bash
java -version
javac -version
```

!!! success "Tot correcte"
    Si els dos comandos mostren la versió instal·lada, ja pots programar en Java.

!!! failure "Error: `javac` no es reconeix"
    Significa que el JDK no està en el *PATH*. Revisa la variable d'entorn `JAVA_HOME`.

## 4. El teu primer programa

Crea un arxiu `HolaMon.java`:

```java title="HolaMon.java" linenums="1"
public class HolaMon {
    public static void main(String[] args) {
        System.out.println("Hola, món!");
    }
}
```

Compila'l i executa'l:

```bash
javac HolaMon.java
java HolaMon
```

!!! danger "Atenció"
    El nom de l'arxiu ha de **coincidir exactament** amb el nom de la classe pública (`HolaMon.java`), respectant majúscules i minúscules.
