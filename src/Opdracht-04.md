# **Opdracht 4: Uitbreiding van de Rekenmachine**

## **Doel van de opdracht**
Breid de `Rekenmachine` uit met methodes voor **aftrekken, vermenigvuldigen en delen**. Laat de gebruiker kiezen welke bewerking hij wil uitvoeren en debug de verschillende methodes met **Step Into** (`F7`).

---

## **Stap 1: Voeg nieuwe methodes toe**
Maak de volgende methodes aan in je `Rekenmachine` class:
- `aftrekken(int a, int b)`: Geeft het verschil terug.
- `vermenigvuldigen(int a, int b)`: Geeft het product terug.
- `delen(int a, int b)`: Geeft de deling terug. Zorg ervoor dat **delen door nul** wordt voorkomen!

<details>
<summary>Bekijk hoe je deze methodes maakt</summary>

```java
public static int aftrekken(int a, int b) {
    return a - b;
}

public static int vermenigvuldigen(int a, int b) {
    return a * b;
}

public static double delen(int a, int b) {
    if (b == 0) {
        System.out.println("Delen door nul is niet toegestaan!");
        return 0;
    }
    return (double) a / b;
}
```
</details>

---

## **Stap 2: Laat de gebruiker een bewerking kiezen**
1. Vraag de gebruiker om twee getallen in te voeren.
2. Toon een menu met de opties: **1: Optellen, 2: Aftrekken, 3: Vermenigvuldigen, 4: Delen**.
3. Gebruik een `switch` statement om de juiste methode aan te roepen.

<details>
<summary>Bekijk hoe je de gebruikerskeuze kunt verwerken</summary>

```java
System.out.println("Kies een bewerking: \n1. Optellen \n2. Aftrekken \n3. Vermenigvuldigen \n4. Delen");
int keuze = scanner.nextInt();
int resultaat = 0;

switch (keuze) {
    case 1:
        resultaat = optellen(getal1, getal2);
        break;
    case 2:
        resultaat = aftrekken(getal1, getal2);
        break;
    case 3:
        resultaat = vermenigvuldigen(getal1, getal2);
        break;
    case 4:
        double deling = delen(getal1, getal2);
        System.out.println("Het resultaat is: " + deling);
        return;
    default:
        System.out.println("Ongeldige keuze!");
        return;
}
System.out.println("Het resultaat is: " + resultaat);
```
</details>

---

## **Stap 3: Debugging met Step Into (`F7`)**
### **1. Zet breakpoints op de methode-aanroepen**
- Zet een **breakpoint** op de regel waar de gekozen methode wordt aangeroepen.

### **2. Start de debugger**
- Klik op de **bug-icoon** of druk op `Shift + F9`.

### **3. Gebruik ‘Step Into’ (`F7`)**
- Druk op `F7` om **de methode in te gaan** en te zien hoe de berekening wordt uitgevoerd.
- Controleer de waarden van de parameters (`a` en `b`).

### **4. Debug de deling (edge cases testen)**
- Test wat er gebeurt als de gebruiker **nul** invoert als tweede getal bij deling.
- Zorg ervoor dat de foutmelding correct verschijnt en dat het programma niet crasht.

---

## **Stap 4: Extra uitdaging**
- Breid het programma uit zodat de gebruiker **meerdere bewerkingen** achter elkaar kan uitvoeren zonder het programma opnieuw te starten.
- Laat de gebruiker kiezen of hij een **nieuwe berekening** wil doen of wil stoppen.


<details>
<summary>Uitwerking</summary> 

```java
import java.util.Scanner;

public class Rekenmachine {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        boolean doorgaan = true;

        while (doorgaan) {
            System.out.print("Voer het eerste getal in: ");
            int getal1 = scanner.nextInt();
            System.out.print("Voer het tweede getal in: ");
            int getal2 = scanner.nextInt();

            System.out.println("Kies een bewerking: \n1. Optellen \n2. Aftrekken \n3. Vermenigvuldigen \n4. Delen");
            int keuze = scanner.nextInt();
            int resultaat = 0;

            switch (keuze) {
                case 1:
                    resultaat = optellen(getal1, getal2);
                    break;
                case 2:
                    resultaat = aftrekken(getal1, getal2);
                    break;
                case 3:
                    resultaat = vermenigvuldigen(getal1, getal2);
                    break;
                case 4:
                    double deling = delen(getal1, getal2);
                    System.out.println("Het resultaat is: " + deling);
                    break;
                default:
                    System.out.println("Ongeldige keuze!");
                    continue;
            }

            System.out.println("Het resultaat is: " + resultaat);
            System.out.print("Wil je een nieuwe berekening uitvoeren? (ja/nee): ");
            String antwoord = scanner.next();

            if (!antwoord.equalsIgnoreCase("ja")) {
                doorgaan = false;
            }
        }
        System.out.println("Programma beëindigd.");
    }

    public static int optellen(int a, int b) {
        return a + b;
    }

    public static int aftrekken(int a, int b) {
        return a - b;
    }

    public static int vermenigvuldigen(int a, int b) {
        return a * b;
    }

    public static double delen(int a, int b) {
        if (b == 0) {
            System.out.println("Delen door nul is niet toegestaan!");
            return 0;
        }
        return (double) a / b;
    }
}

```

</details>


Veel succes! 🚀

