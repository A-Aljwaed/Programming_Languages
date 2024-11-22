

## 1. Was ist Python?
Python ist eine vielseitige, interpretierte Programmiersprache, die sich durch einfache Syntax und hohe Lesbarkeit auszeichnet. Sie wird für Webentwicklung, Datenanalyse, KI und mehr eingesetzt.

---

## 2. Variablen und Datentypen
### Variablen deklarieren
```python
name = "Alice"  # Zeichenkette (String)
age = 25        # Ganze Zahl (Integer)
height = 1.75   # Gleitkommazahl (Float)
is_student = True  # Wahrheitswert (Boolean)
```
**Erklärung:**
- In Python wird der Datentyp automatisch erkannt.
- Kein Schlüsselwort wie `let` oder `const` nötig.

---

## 3. Kontrollstrukturen
### If-Else
```python
age = 20
if age >= 18:
    print("Erwachsen")
else:
    print("Nicht erwachsen")
```
**Erklärung:**
- Einrückung (Indentation) ist in Python entscheidend, um Blöcke zu definieren.
- Kein `()` oder `{}` nötig.

### For-Schleife
```python
for i in range(5):  # Wiederholt sich 5 Mal (0 bis 4)
    print(i)
```
**Erklärung:** Die Funktion `range` erzeugt eine Sequenz von Zahlen.

### While-Schleife
```python
count = 0
while count < 5:
    print(count)
    count += 1
```
**Erklärung:** Die Schleife läuft, solange die Bedingung `count < 5` wahr ist.

---

## 4. Listen (Arrays)
### Liste erstellen und verwenden
```python
fruits = ["Apfel", "Banane", "Kirsche"]
print(fruits[0])  # Ausgabe: Apfel
```
**Erklärung:** Listen können Elemente unterschiedlichen Typs enthalten.

### Methoden
```python
fruits.append("Orange")  # Fügt ein Element hinzu
fruits.pop()             # Entfernt das letzte Element
```

---

## 5. Dictionaries (Maps)
```python
person = {"name": "Alice", "age": 25}
print(person["name"])  # Ausgabe: Alice
```
**Erklärung:** Dictionaries speichern Schlüssel-Wert-Paare.

---

## 6. Funktionen
### Funktionsdeklaration
```python
def greet(name):
    return f"Hallo, {name}!"
print(greet("Alice"))  # Ausgabe: Hallo, Alice!
```
**Erklärung:** Funktionen werden mit dem Schlüsselwort `def` definiert.

---

## 7. Klassen und Objekte
```python
class Car:
    def __init__(self, brand, speed):
        self.brand = brand
        self.speed = speed

    def display_info(self):
        print(f"Marke: {self.brand}, Geschwindigkeit: {self.speed}")

my_car = Car("BMW", 120)
my_car.display_info()  # Ausgabe: Marke: BMW, Geschwindigkeit: 120
```
**Erklärung:**
- **`__init__`**: Konstruktor der Klasse.
- **`self`**: Verweist auf die Instanz des Objekts.

---

## 8. Dateien lesen und schreiben
### Datei schreiben
```python
with open("example.txt", "w") as file:
    file.write("Hallo, Welt!")
```
**Erklärung:** Die Methode `open` öffnet eine Datei im Schreibmodus (`w`).

### Datei lesen
```python
with open("example.txt", "r") as file:
    content = file.read()
    print(content)
```
**Erklärung:** `r` steht für den Lesemodus.

---

## 9. Fehlerbehandlung
```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Fehler: Division durch null!")
```
**Erklärung:**
- Der `try`-Block enthält potenziell fehlerhaften Code.
- Der `except`-Block fängt die Ausnahme ab.

---

## 10. Module und Bibliotheken
### Importieren eines Moduls
```python
import math
print(math.sqrt(16))  # Ausgabe: 4.0
```
**Erklärung:** `math` ist ein integriertes Modul für mathematische Funktionen.

### Eigene Funktion in einer Datei importieren
Datei `module.py`:
```python
def greet(name):
    return f"Hallo, {name}!"
```
Hauptdatei:
```python
from module import greet
print(greet("Alice"))  # Ausgabe: Hallo, Alice!
```

---

## 11. Asynchrone Programmierung
### Async/Await
```python
import asyncio

async def fetch_data():
    print("Daten abrufen...")
    await asyncio.sleep(2)
    print("Daten abgerufen!")

asyncio.run(fetch_data())
```
**Erklärung:** `async` und `await` werden für asynchrone Operationen verwendet.

---

## 12. Best Practices
1. Verwende **aussagekräftige Variablennamen**.
2. Nutze Bibliotheken wie `pandas` und `numpy` für komplexe Aufgaben.
3. Halte deinen Code modular und gut strukturiert.
