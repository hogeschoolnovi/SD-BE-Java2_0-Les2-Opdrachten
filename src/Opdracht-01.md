# **Opdracht 1: Werken met if-else statements**

## **Doel van de opdracht**
In deze opdracht leer je hoe je beslissingen maakt in Java met behulp van `if`, `if-else` en `else if` statements.

---

## **Stap 1: Een nieuw Java-project aanmaken**
1. Open IntelliJ IDEA en maak een nieuw Java-project aan.
2. Maak een nieuwe Java-class genaamd `Beslissingen`.
3. Voeg een `main`-methode toe.

---

## **Stap 2: Een getal beoordelen**
1. Vraag de gebruiker om een getal in te voeren met `Scanner`.
2. Controleer of het getal:
    - **Positief** is → Print: "Het getal is positief."
    - **Negatief** is → Print: "Het getal is negatief."
    - **Nul** is → Print: "Het getal is nul."


<details>
<summary>Uitwerking</summary>

### **Codevoorbeeld**
```java
import java.util.Scanner;

public class Beslissingen {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Voer een getal in: ");
        int getal = scanner.nextInt();
        
        if (getal > 0) {
            System.out.println("Het getal is positief.");
        } else if (getal < 0) {
            System.out.println("Het getal is negatief.");
        } else {
            System.out.println("Het getal is nul.");
        }
    }
}
```

</details>

---

## **Stap 3: Uitvoeren en testen**
1. Voer het programma uit en probeer verschillende getallen.
2. Controleer of de output correct is.

---

## **Extra uitdaging**
Breid het programma uit zodat:
- Als het getal **even** is, de output ook aangeeft: "Het is een even getal."
- Als het getal **oneven** is, de output aangeeft: "Het is een oneven getal."

### **Hint**
Gebruik de **modulus-operator `%`** om te controleren of een getal deelbaar is door 2.


<details>
<summary>Uitwerking</summary> 

```java
import java.util.Scanner;

public class Beslissingen {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Voer een getal in: ");
        int getal = scanner.nextInt();

        if (getal > 0) {
            System.out.println("Het getal is positief.");
        } else if (getal < 0) {
            System.out.println("Het getal is negatief.");
        } else {
            System.out.println("Het getal is nul.");
        }

        // Controleer of het getal even of oneven is
        if (getal % 2 == 0) {
            System.out.println("Het is een even getal.");
        } else {
            System.out.println("Het is een oneven getal.");
        }
    }
}

```
</details>


Veel succes! 

