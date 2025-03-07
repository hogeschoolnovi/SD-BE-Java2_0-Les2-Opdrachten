# **Opdracht 2: Werken met loops en debugging**

## **Doel van de opdracht**
In deze opdracht leer je werken met **loops** in Java en krijg je uitgebreide tips om te **debuggen** in IntelliJ IDEA.

---

## **Stap 1: Een nieuwe class maken**
1. Open je bestaande project.
2. Maak een nieuwe Java-class genaamd `TafelVan`.
3. Voeg een `main`-methode toe.

---

## **Stap 2: De tafel van een getal tonen**
1. Vraag de gebruiker om een getal in te voeren met `Scanner`.
2. Gebruik een **for-loop** om de tafel van dat getal te berekenen (van 1 tot 10).

### **Structuur van een for-loop:**
```java
for (int i = 1; i <= 10; i++) {
    // Hier bereken je de tafel
}
```

3. Print de resultaten in de console.

<details>
<summary>Volledige code</summary>

```java
import java.util.Scanner;

public class TafelVan {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Voer een getal in: ");
        int getal = scanner.nextInt();
        
        System.out.println("De tafel van " + getal + ":");
        for (int i = 1; i <= 10; i++) {
            System.out.println(getal + " x " + i + " = " + (getal * i));
        }
    }
}
```
</details>

---

## **Stap 3: Debugging in IntelliJ IDEA**
Tijdens het programmeren kunnen er fouten optreden. Volg deze stappen om je code te debuggen:

### **1. Zet een breakpoint**
- Klik in IntelliJ links van de regelnummering naast een regel code om een **rode stip** te zetten (een breakpoint).
- Dit betekent dat de debugger stopt bij deze regel wanneer het programma wordt uitgevoerd.

### **2. Start de debugger**
- In plaats van op de **groene play-knop**, klik je op de **bug-icoon** of gebruik je `Shift + F9`.
- Het programma wordt nu stap voor stap uitgevoerd en stopt bij breakpoints.

### **3. Gebruik ‘Step Over’ en ‘Step Into’**
- `F8 (Step Over)`: Voert de volgende regel uit zonder in methodes te duiken.
- `F7 (Step Into)`: Gaat **in een methode** zodat je kunt zien wat daar gebeurt.

### **4. Bekijk variabelen en de ‘Watches’ tab**
- Onderaan IntelliJ zie je de **Variables** tab. Hier zie je de actuele waarden van je variabelen.
- Voeg een variabele toe aan **Watches** (rechtsklik → Add to Watches) om hem beter te volgen.

### **5. Debug een fout (voorbeeld)**
Stel dat de code **verkeerde tafels** berekent. Probeer dan:
- Breakpoints te zetten op de `for`-loop.
- De waarde van `i` en `getal` te controleren.
- Stap voor stap door de berekening te gaan en te kijken of `getal * i` klopt.

---

## **Stap 4: Extra uitdaging**
Breid het programma uit zodat:
- De gebruiker zelf kan kiezen tot welk getal de tafel moet gaan (bijv. tot 15 in plaats van 10).
- Als de gebruiker een negatief getal invoert, de code blijft vragen om een **positief** getal voordat de berekening start.

### **Hint**
Hiervoor kun je een **while-loop** gebruiken!


<details>
<summary>Hint</summary> 


```java
while (getal < 0) {
    System.out.print("Voer een positief getal in: ");
    getal = scanner.nextInt();
}
```
</details>

Veel succes! 🚀

