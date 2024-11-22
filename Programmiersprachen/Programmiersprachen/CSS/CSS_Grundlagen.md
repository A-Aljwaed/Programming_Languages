
# CSS Grundlagen

## 1. Was ist CSS?
CSS (Cascading Style Sheets) ist eine Sprache, die verwendet wird, um das Erscheinungsbild und Layout von HTML-Dokumenten zu gestalten. CSS steuert Farben, Schriftarten, Abstände, Größen, Layouts und mehr.

---

## 2. CSS-Syntax
```css
selector {
    property: value;
}
```
**Erklärung:**
- **`selector`**: Wählt das HTML-Element aus, das gestylt werden soll.
- **`property`**: Beschreibt die Eigenschaft, die geändert wird (z. B. `color`).
- **`value`**: Gibt den Wert der Eigenschaft an (z. B. `blue`).

**Beispiel:**
```css
h1 {
    color: blue;         /* Textfarbe */
    font-size: 24px;     /* Schriftgröße */
}
```

---

## 3. Arten, CSS einzubinden
### 1. Inline-CSS
```html
<h1 style="color: red;">Dieser Text ist rot</h1>
```
**Erklärung:** Styling wird direkt im HTML-Tag angewendet.

### 2. Internes CSS
```html
<head>
    <style>
        p {
            font-family: Arial, sans-serif;
            color: green;
        }
    </style>
</head>
```
**Erklärung:** CSS wird in einem `<style>`-Block im `<head>`-Bereich definiert.

### 3. Externes CSS
```html
<link rel="stylesheet" href="styles.css">
```
**Erklärung:** CSS wird in einer separaten Datei gespeichert und mit `<link>` eingebunden.

---

## 4. Selektoren
CSS-Selektoren bestimmen, welche HTML-Elemente gestylt werden.

### Grundlegende Selektoren
| Selektor       | Beschreibung                      | Beispiel               |
|----------------|-----------------------------------|------------------------|
| `*`            | Wählt alle Elemente              | `* { margin: 0; }`     |
| `element`      | Wählt alle `<element>`            | `p { color: blue; }`   |
| `.class`       | Wählt Elemente mit Klasse         | `.intro { font-size: 14px; }` |
| `#id`          | Wählt ein Element mit ID          | `#header { text-align: center; }` |

**Beispiel:**
```css
/* Wählt alle Absätze mit der Klasse "highlight" */
p.highlight {
    background-color: yellow;
}
```

---

## 5. Farben und Hintergründe
### Farben definieren
```css
p {
    color: #ff5733;        /* Hexadezimal */
    background-color: rgb(255, 255, 0); /* RGB */
}
```
**Erklärung:**
- **`color`**: Textfarbe.
- **`background-color`**: Hintergrundfarbe.

### Transparenz mit RGBA
```css
div {
    background-color: rgba(0, 0, 0, 0.5); /* 50% transparent */
}
```

---

## 6. Box-Modell
Das CSS-Box-Modell beschreibt, wie der Platz eines Elements berechnet wird.

### Box-Modell-Aufbau:
1. **Content**: Der Inhalt des Elements.
2. **Padding**: Innenabstand um den Inhalt.
3. **Border**: Rand des Elements.
4. **Margin**: Außenabstand zum nächsten Element.

**Beispiel:**
```css
div {
    width: 300px;
    height: 100px;
    padding: 10px;
    border: 2px solid black;
    margin: 20px;
}
```
**Erklärung:**
- **`width`** und **`height`**: Bestimmen die Größe des Inhalts.
- **`padding`**: Fügt Abstand innerhalb des Elements hinzu.
- **`border`**: Fügt einen Rand hinzu.
- **`margin`**: Abstand außerhalb des Elements.

---

## 7. Schriftarten und Text
### Schriftart und Größe
```css
p {
    font-family: Arial, sans-serif;
    font-size: 16px;
}
```
**Erklärung:**
- **`font-family`**: Definiert die Schriftart.
- **`font-size`**: Bestimmt die Schriftgröße.

### Textausrichtung
```css
h1 {
    text-align: center;
}
```
**Erklärung:** **`text-align`** zentriert den Text horizontal.

### Textdekoration
```css
a {
    text-decoration: none; /* Entfernt Unterstrich */
}
```

---

## 8. Layout mit Flexbox
Flexbox ist ein Layout-Modell, das das Anordnen von Elementen erleichtert.

**Beispiel:**
```css
.container {
    display: flex;
    justify-content: center; /* Zentriert horizontal */
    align-items: center;    /* Zentriert vertikal */
    height: 100vh;
}
```
**Erklärung:**
- **`display: flex`**: Aktiviert Flexbox.
- **`justify-content`**: Horizontale Ausrichtung.
- **`align-items`**: Vertikale Ausrichtung.

---

## 9. CSS-Grid
CSS-Grid ist ein leistungsstarkes Layout-System.

**Beispiel:**
```css
.container {
    display: grid;
    grid-template-columns: 1fr 2fr;
    grid-gap: 10px;
}
```
HTML:
```html
<div class="container">
    <div>Box 1</div>
    <div>Box 2</div>
</div>
```
**Erklärung:**
- **`display: grid`**: Aktiviert Grid-Layout.
- **`grid-template-columns`**: Definiert die Breite der Spalten.
- **`grid-gap`**: Fügt Abstand zwischen den Zellen hinzu.

---

## 10. Animationen
### Übergänge
```css
button {
    transition: background-color 0.3s;
}
button:hover {
    background-color: blue;
}
```
**Erklärung:** Die Hintergrundfarbe wechselt sanft, wenn der Mauszeiger über den Button fährt.

### Keyframe-Animation
```css
@keyframes move {
    from { transform: translateX(0); }
    to { transform: translateX(100px); }
}

div {
    animation: move 2s infinite;
}
```
HTML:
```html
<div>Ich bewege mich!</div>
```
**Erklärung:** Das Element bewegt sich horizontal von 0px auf 100px.

---

## 11. Responsive Design
### Media Queries
```css
@media (max-width: 600px) {
    body {
        background-color: lightblue;
    }
}
```
**Erklärung:** Wenn die Bildschirmbreite 600px oder weniger beträgt, wird der Hintergrund hellblau.

---

## 12. Best Practices
1. Verwende **klare Klassen- und ID-Namen**.
2. Vermeide **Inline-CSS**. Nutze externe Stylesheets.
3. Gruppiere und organisiere ähnliche Regeln.
