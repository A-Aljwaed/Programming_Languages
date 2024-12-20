
# Java Grundlagen

## 1. Was ist Java?
Java ist eine objektorientierte Programmiersprache, die plattformunabhängig ist (Dank der Java Virtual Machine). Es wird häufig für Backend-Systeme, mobile Anwendungen (Android) und mehr verwendet.

---

## 2. Grundstruktur eines Java-Programms
```java
public class HelloWorld {          // Definition einer Klasse
    public static void main(String[] args) {  // Hauptmethode, Einstiegspunkt des Programms
        System.out.println("Hello, World!");  // Ausgabe von Text in der Konsole
    }
}
```
**Erklärung:**
1. **`public class HelloWorld`**: Definiert eine Klasse namens `HelloWorld`. Der Dateiname muss `HelloWorld.java` sein.
2. **`public static void main(String[] args)`**: Die Hauptmethode, die beim Programmstart ausgeführt wird.
3. **`System.out.println`**: Gibt den Text `Hello, World!` in der Konsole aus.

---

## 3. Variablen und Datentypen
### Deklaration und Initialisierung

```java
int age = 25;         // Ganze Zahl
double price = 19.99; // Dezimalzahl
String name = "Alice";// Zeichenkette
boolean isStudent = true; // Wahrheitswert
```
**Erklärung:**
- **`int`**: Speichert ganze Zahlen.
- **`double`**: Speichert Dezimalzahlen.
- **`String`**: Speichert Text.
- **`boolean`**: Speichert `true` oder `false`.

---

## 4. Kontrollstrukturen
### If-Else
```java
int age = 20;
if (age >= 18) {
    System.out.println("Erwachsen");
} else {
    System.out.println("Nicht erwachsen");
}
```
**Erklärung:**
- Die Bedingung **`age >= 18`** wird geprüft. Ist sie wahr, wird `"Erwachsen"` ausgegeben, sonst `"Nicht erwachsen"`.

### For-Schleife
```java
for (int i = 0; i < 5; i++) {
    System.out.println("Zahl: " + i);
}
```
**Erklärung:**
- **`int i = 0`**: Startwert.
- **`i < 5`**: Schleife läuft, solange `i` kleiner als 5 ist.
- **`i++`**: Erhöht `i` nach jeder Iteration um 1.

### While-Schleife
```java
int count = 0;
while (count < 5) {
    System.out.println(count);
    count++;
}
```
**Erklärung:**
- Solange die Bedingung **`count < 5`** wahr ist, wird der Codeblock ausgeführt.

---

## 5. Arrays
```java
int[] numbers = {1, 2, 3, 4, 5};
System.out.println(numbers[0]); // Gibt das erste Element aus
```
**Erklärung:**
- **`int[]`**: Deklariert ein Array von Ganzzahlen.
- **`numbers[0]`**: Zugriff auf das erste Element des Arrays.

---

## 6. Methoden
```java
public int addNumbers(int a, int b) {
    return a + b;
}
```
**Erklärung:**
1. **`public`**: Zugriff von überall.
2. **`int`**: Gibt eine Ganzzahl zurück.
3. **`addNumbers`**: Name der Methode.
4. **`(int a, int b)`**: Parameter der Methode.

Aufruf:
```java
int result = addNumbers(5, 10);
System.out.println(result); // Ausgabe: 15
```

---

## 7. Klassen und Objekte
### Klassendeklaration und Objekterstellung
```java
public class Car {
    String brand;
    int speed;

    public void displayInfo() {
        System.out.println("Marke: " + brand + ", Geschwindigkeit: " + speed);
    }
}

Car myCar = new Car();
myCar.brand = "BMW";
myCar.speed = 120;
myCar.displayInfo(); // Ausgabe: Marke: BMW, Geschwindigkeit: 120
```
**Erklärung:**
- Die Klasse **`Car`** definiert Eigenschaften (`brand`, `speed`) und Methoden (`displayInfo`).
- **`myCar`** ist ein Objekt der Klasse.

---

## 8. Vererbung
```java
class Animal {
    public void makeSound() {
        System.out.println("Animal makes a sound");
    }
}

class Dog extends Animal {
    @Override
    public void makeSound() {
        System.out.println("Dog barks");
    }
}

Dog dog = new Dog();
dog.makeSound(); // Ausgabe: Dog barks
```
**Erklärung:**
- **`extends`**: Dog erbt von Animal.
- **`@Override`**: Methode der Basisklasse wird überschrieben.

---

## 9. Exception Handling
```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Fehler: Division durch null!");
}
```
**Erklärung:**
- Der `try`-Block enthält Code, der fehlschlagen könnte.
- Der `catch`-Block behandelt die Ausnahme.

---

## 10. Java Collections Framework
### ArrayList
```java
import java.util.ArrayList;

ArrayList<String> names = new ArrayList<>();
names.add("Alice");
names.add("Bob");
System.out.println(names);
```
**Erklärung:**
- **`ArrayList`**: Dynamisches Array.
- **`add`**: Fügt ein Element hinzu.

### HashMap
```java
import java.util.HashMap;

HashMap<Integer, String> map = new HashMap<>();
map.put(1, "Alice");
map.put(2, "Bob");
System.out.println(map.get(1)); // Ausgabe: Alice
```
**Erklärung:**
- **`HashMap`**: Speichert Schlüssel-Wert-Paare.
- **`get`**: Zugriff auf einen Wert über den Schlüssel.

---

## 11. Streams und Lambdas
```java
import java.util.List;

List<Integer> numbers = List.of(1, 2, 3, 4, 5);
numbers.stream()
       .filter(n -> n % 2 == 0)
       .forEach(System.out::println); // Ausgabe: 2, 4
```
**Erklärung:**
- **`stream()`**: Erstellt einen Datenstrom.
- **`filter`**: Filtert Elemente.
- **`forEach`**: Führt eine Aktion für jedes Element aus.

---

## 12. JSON-Verarbeitung
```java
import com.google.gson.Gson;

class Person {
    String name;
    int age;
}

Person person = new Person();
person.name = "Alice";
person.age = 25;

Gson gson = new Gson();
String json = gson.toJson(person);
System.out.println(json); // Ausgabe: {"name":"Alice","age":25}
```

---

## 13. Best Practices
1. Nutze **aussagekräftige Namen** für Klassen, Methoden und Variablen.
2. Halte den Code modular und klein.
3. Behandle mögliche Fehler mit **try-catch**.
