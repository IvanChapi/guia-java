# Programació orientada a objectes

La **POO** organitza el programa en **objectes** que combinen *dades* (atributs) i *comportament* (mètodes).

## Classes i objectes

Una **classe** és el pla; un **objecte** és una instància concreta d'eixa classe.

```java title="Persona.java"
public class Persona {
    // Atributs
    private String nom;
    private int edat;

    // Constructor
    public Persona(String nom, int edat) {
        this.nom = nom;
        this.edat = edat;
    }

    // Mètodes
    public String getNom() {
        return nom;
    }

    public void saludar() {
        System.out.println("Hola, sóc " + nom + " i tinc " + edat + " anys.");
    }
}
```

Crear i utilitzar un objecte:

```java
Persona p = new Persona("Anna", 20);
p.saludar();
```

## Els 4 pilars de la POO

1. **Encapsulació**: ocultar els atributs (`private`) i accedir-hi amb *getters* i *setters*.
2. **Herència**: una classe pot heretar d'una altra amb `extends`.
3. **Polimorfisme**: un mateix mètode pot comportar-se de formes diferents.
4. **Abstracció**: mostrar només el que és essencial.

## Herència

```java
public class Estudiant extends Persona {
    private String cicle;

    public Estudiant(String nom, int edat, String cicle) {
        super(nom, edat);
        this.cicle = cicle;
    }
}
```

!!! abstract "Resum"
    - La classe fill (`Estudiant`) **hereta** atributs i mètodes de la classe pare (`Persona`).
    - `super(...)` crida al constructor de la classe pare.

!!! tip "Per què `private`?"
    Declarar els atributs com a `private` protegeix les dades: només es poden modificar mitjançant els mètodes que tu controles.

!!! bug "Error habitual"
    Oblidar `new` en crear un objecte, o utilitzar-lo sense haver-lo inicialitzat, provoca una `NullPointerException`.

??? example "Exercici proposat"
    Crea una classe `Cotxe` amb els atributs `marca` i `velocitat`, i els mètodes `accelerar()` i `frenar()`.
