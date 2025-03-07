# **Opdracht 3: Methodes en Debugging met Step Into**

## **Doel van de opdracht**
In deze opdracht leer je hoe je **methodes** gebruikt om je code overzichtelijker te maken en hoe je met de debugger **Step Into** (`F7`) gebruikt om methodes stap voor stap te doorlopen.

---

## **Stap 1: Een nieuwe class maken**
1. Open je bestaande project.
2. Maak een nieuwe Java-class genaamd `Rekenmachine`.
3. Voeg een `main`-methode toe.

---

## **Stap 2: Een methode maken voor optellen**
### **1. Vraag input van de gebruiker**
- Gebruik een `Scanner` om de gebruiker **twee getallen** te laten invoeren.
- Sla deze waarden op in variabelen.

### **2. Maak een methode om de som te berekenen**
- De methode heet `optellen` en accepteert **twee parameters** van het type `int`.
- De methode geeft de **som** van de twee getallen terug.

### **3. Roep de methode aan vanuit `main`**
- Roep `optellen` aan met de twee getallen die de gebruiker heeft ingevoerd.
- Sla het resultaat op en print het in de console.

<details>
<summary>Bekijk de volledige code</summary>

```java
import java.util.Scanner;

public class Rekenmachine {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Voer het eerste getal in: ");
        int getal1 = scanner.nextInt();
        System.out.print("Voer het tweede getal in: ");
        int getal2 = scanner.nextInt();
        
        int resultaat = optellen(getal1, getal2);
        System.out.println("De som is: " + resultaat);
    }
    
    public static int optellen(int a, int b) {
        return a + b;
    }
}
```
</details>

---

## **Stap 3: Debugging met ‘Step Into’**
### **1. Zet een breakpoint bij de methode-aanroep**
- Zet een **breakpoint** op de regel waar `optellen(getal1, getal2)` wordt aangeroepen.

### **2. Start de debugger**
- Klik op de **bug-icoon** of druk op `Shift + F9`.

### **3. Gebruik ‘Step Into’ (`F7`)**
- Wanneer de debugger stopt bij `optellen(getal1, getal2)`, druk op `F7`.
- De debugger springt **in** de `optellen` methode.
- Stap door de methode en controleer hoe de waarden van `a` en `b` veranderen.

### **4. Controleer de variabelen**
- Gebruik de **Variables** tab onderaan IntelliJ om te zien hoe de waarden zich ontwikkelen.
- Je kunt ook **Watches** gebruiken om specifieke variabelen te volgen.

Veel succes! 

