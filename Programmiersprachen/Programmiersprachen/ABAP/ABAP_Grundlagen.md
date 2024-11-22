
# ABAP - Grundlagen

**ABAP** (Advanced Business Application Programming) ist die Programmiersprache von SAP, die hauptsächlich für die Entwicklung von Anwendungen und Geschäftslogik in SAP-Systemen verwendet wird. ABAP wird verwendet, um Geschäftsprozesse zu automatisieren, Reports zu erstellen und SAP-Module zu erweitern.

---

## 1. ABAP - Grundlagen

ABAP basiert auf der Programmiersprachen-Logik, verwendet jedoch spezielle SAP-Datenstrukturen und -Funktionen, um mit SAP-Datenbanken und -Modulen zu interagieren. Die ABAP-Entwicklungsumgebung ist die SAP GUI oder SAP Web IDE.

### **Datenobjekte und Variablen**

ABAP bietet verschiedene Datentypen wie:
- **Character (C)**: Zeichenketten (z. B. `DATA: name TYPE C LENGTH 20`)
- **Integer (I)**: Ganzzahlen (z. B. `DATA: age TYPE I`)
- **Decimal (P)**: Dezimalzahlen (z. B. `DATA: amount TYPE P LENGTH 10 DECIMALS 2`)
- **Date (D)** und **Time (T)**: Datums- und Uhrzeitangaben.
- **Table (T)**: Tabellen, die mehrere Datensätze speichern können.

### **Beispiel: Variablendeklaration in ABAP**
```abap
DATA: name TYPE string,
      age TYPE i,
      amount TYPE p LENGTH 10 DECIMALS 2.
```
- **`DATA`**: Deklariert eine Variable oder ein Datenobjekt.
- **`TYPE`**: Gibt den Datentyp der Variable an.
- **`LENGTH` und `DECIMALS`**: Bestimmen die Länge und die Anzahl der Dezimalstellen bei Dezimalwerten.

---

## 2. ABAP - Struktur und Syntax

Die grundlegende Struktur eines ABAP-Programms umfasst die folgenden Teile:
1. **Deklaration**: Hier werden Variablen und Datenobjekte definiert.
2. **Auswahl (SELECT)**: ABAP ermöglicht den Zugriff auf SAP-Datenbanken mit SQL-ähnlichen Abfragen.
3. **Prozeduren**: Dies umfasst die Definition von Subroutinen (Form-Routinen) und Funktionsbausteinen.

### **Beispiel: Einfache ABAP-Prozedur**
```abap
FORM my_procedure.
  WRITE 'Hello, ABAP World!'. 
ENDFORM.
```
- **`FORM`**: Definiert den Beginn einer Subroutine.
- **`WRITE`**: Gibt Daten auf dem Bildschirm aus.
- **`ENDFORM`**: Beendet die Subroutine.

### **Beispiel: SELECT-Abfrage**

```abap
DATA: lt_data TYPE TABLE OF sflight,
      lv_name TYPE string.

SELECT * FROM sflight
  INTO TABLE lt_data
  WHERE carrid = 'LH' AND connid = '400';
```
- **`SELECT * FROM`**: Führt eine SQL-Abfrage aus, um Daten abzurufen.
- **`INTO TABLE`**: Speichert die Ergebnisse in einer internen Tabelle.

---

## 3. Kontrollstrukturen in ABAP

ABAP unterstützt alle grundlegenden Kontrollstrukturen wie:
- **IF** / **ELSE**: Bedingte Anweisungen
- **LOOP**: Schleifen zur Verarbeitung von Tabellen
- **CASE**: Mehrere Bedingungen prüfen

### **Beispiel: IF / ELSE**
```abap
IF age > 18.
  WRITE 'Adult'.
ELSE.
  WRITE 'Minor'.
ENDIF.
```
- **`IF`**: Bedingte Anweisung, die den Block ausführt, wenn die Bedingung wahr ist.
- **`ELSE`**: Definiert einen alternativen Block für den Fall, dass die Bedingung nicht erfüllt ist.
- **`ENDIF`**: Beendet die Bedingung.

### **Beispiel: LOOP und ENDLOOP**
```abap
LOOP AT lt_data.
  WRITE: / lt_data-carrid, lt_data-connid.
ENDLOOP.
```
- **`LOOP AT`**: Iteriert über alle Elemente in der Tabelle `lt_data`.
- **`ENDLOOP`**: Beendet die Schleife.

### **Beispiel: CASE**
```abap
CASE grade.
  WHEN 1.
    WRITE 'Excellent'.
  WHEN 2.
    WRITE 'Good'.
  WHEN OTHERS.
    WRITE 'Needs Improvement'.
ENDCASE.
```
- **`CASE`**: Überprüft mehrere Bedingungen und führt den passenden Block aus.
- **`WHEN`**: Definiert die zu prüfenden Bedingungen.
- **`OTHERS`**: Fängt alle anderen möglichen Fälle ab.

---

## 4. Funktionsbausteine und Subroutinen

ABAP ermöglicht die Erstellung von **Funktionsbausteinen** und **Subroutinen**, die wiederverwendbare Code-Teile darstellen.

### **Beispiel: Funktionsbaustein**

Ein Funktionsbaustein wird in einem Funktionsmodul definiert und kann in verschiedenen Programmen aufgerufen werden.
```abap
FUNCTION z_calculate_area.
  IMPORTING
    width TYPE i
    height TYPE i
  EXPORTING
    area TYPE i.

  area = width * height.
ENDFUNCTION.
```
- **`FUNCTION`**: Definiert einen Funktionsbaustein.
- **`IMPORTING`**: Definiert Eingabeparameter.
- **`EXPORTING`**: Definiert Ausgabeparameter.

### **Beispiel: Subroutine**

```abap
FORM calculate_area USING width TYPE i
                            height TYPE i
                   CHANGING area TYPE i.
  area = width * height.
ENDFORM.
```
- **`FORM`**: Definiert eine Subroutine.
- **`USING`**: Eingabeparameter, die der Subroutine übergeben werden.
- **`CHANGING`**: Parameter, die in der Subroutine geändert werden können.

---

## 5. ABAP-Datenbankzugriff

ABAP ermöglicht den Zugriff auf SAP-Datenbanken mit **SELECT**-Anweisungen und unterstützt alle grundlegenden SQL-Operationen:

- **SELECT**: Zum Abrufen von Daten.
- **INSERT**: Zum Hinzufügen von Daten.
- **UPDATE**: Zum Ändern von Daten.
- **DELETE**: Zum Löschen von Daten.

### **Beispiel: SELECT-Abfrage**
```abap
DATA: lt_data TYPE TABLE OF sflight,
      lv_name TYPE string.

SELECT * FROM sflight
  INTO TABLE lt_data
  WHERE carrid = 'LH' AND connid = '400';
```

---

## 6. ABAP-Entwicklungsumgebung

ABAP-Programme werden in der **SAP GUI** entwickelt. Es gibt auch die Möglichkeit, ABAP über die **SAP Web IDE** zu entwickeln.

Die wichtigsten Entwicklungswerkzeuge umfassen:
- **SE80**: ABAP-Workbench, in der alle Entwicklungsobjekte organisiert werden.
- **SE11**: Dictionary für die Erstellung und Pflege von Datenbanktabellen und -strukturen.
- **SE37**: Funktionsbausteine verwalten.

---

## 7. Debugging in ABAP

Das Debugging ist ein wichtiger Bestandteil der ABAP-Entwicklung. Mit der SAP-GUI können Entwickler den Code Schritt für Schritt ausführen, um Fehler zu finden.

### **Wichtige Debugging-Techniken**:
- Breakpoints setzen
- Variablen beobachten
- Stack-Traces analysieren

---

## 8. ABAP-Optimierung

Optimierung ist ein wichtiger Aspekt der ABAP-Entwicklung, um sicherzustellen, dass die Programme effizient arbeiten und keine Systemressourcen unnötig beanspruchen.

### **Tipps zur Optimierung**:
1. Vermeidung von **SELECT ***-Abfragen.
2. Verwenden von **inner join** anstelle von mehreren SELECT-Anfragen.
3. Einsatz von **Hash-Tabellen** für große Datenmengen.
4. **Indexe** auf Datenbanktabellen verwenden.

---

Falls du weitere Details oder spezifische Beispiele benötigst, lass es mich wissen! 😊
