
## 1. Was ist HTML?
HTML (HyperText Markup Language) ist die Standard-Auszeichnungssprache für das Erstellen von Webseiten. Sie definiert die Struktur und den Inhalt einer Webseite mithilfe von Elementen (Tags).

---

## 2. Grundstruktur einer HTML-Seite
```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meine Webseite</title>
</head>
<body>
    <h1>Willkommen auf meiner Webseite</h1>
    <p>Dies ist ein einfacher Absatz.</p>
</body>
</html>
```
**Erklärung:**
1. **`<!DOCTYPE html>`**: Deklariert den Dokumenttyp als HTML5.
2. **`<html>`**: Der Wurzel-Tag, der das gesamte HTML-Dokument umschließt.
3. **`<head>`**: Enthält Metadaten wie den Titel oder Links zu Stylesheets.
4. **`<body>`**: Enthält den sichtbaren Inhalt der Webseite.

---

## 3. Wichtige HTML-Tags
### Überschriften
```html
<h1>Größte Überschrift</h1>
<h2>Zweitgrößte Überschrift</h2>
<h3>Drittgrößte Überschrift</h3>
```
**Erklärung:** Es gibt 6 Ebenen von Überschriften (`<h1>` bis `<h6>`), wobei `<h1>` die wichtigste ist.

### Absätze und Textformatierung
```html
<p>Dies ist ein Absatz.</p>
<b>Fett</b> und <i>Kursiv</i>
```
**Erklärung:**
- **`<p>`**: Definiert einen Absatz.
- **`<b>`**: Macht Text fett.
- **`<i>`**: Macht Text kursiv.

### Links
```html
<a href="https://example.com">Ein Link</a>
```
**Erklärung:**
- **`<a>`**: Erstellt einen Hyperlink.
- **`href`**: Gibt die Ziel-URL an.

### Bilder
```html
<img src="bild.jpg" alt="Beschreibung des Bildes" width="200">
```
**Erklärung:**
- **`<img>`**: Fügt ein Bild ein.
- **`src`**: Gibt die Bildquelle an.
- **`alt`**: Beschreibung, falls das Bild nicht geladen werden kann.

---

## 4. Listen
### Ungeordnete Liste
```html
<ul>
    <li>Element 1</li>
    <li>Element 2</li>
</ul>
```
### Geordnete Liste
```html
<ol>
    <li>Element 1</li>
    <li>Element 2</li>
</ol>
```
**Erklärung:**
- **`<ul>`**: Ungeordnete Liste (Punkte).
- **`<ol>`**: Geordnete Liste (Nummern).
- **`<li>`**: Listenelement.

---

## 5. Tabellen
```html
<table>
    <tr>
        <th>Name</th>
        <th>Alter</th>
    </tr>
    <tr>
        <td>Max</td>
        <td>25</td>
    </tr>
</table>
```
**Erklärung:**
- **`<table>`**: Erstellt eine Tabelle.
- **`<tr>`**: Definiert eine Zeile.
- **`<th>`**: Kopfzelle.
- **`<td>`**: Zelle mit Daten.

---

## 6. Formulare
```html
<form action="/submit" method="post">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name">
    <input type="submit" value="Senden">
</form>
```
**Erklärung:**
- **`<form>`**: Erstellt ein Formular.
- **`action`**: Ziel, wohin die Daten gesendet werden.
- **`method`**: Übertragungsmethode (`get` oder `post`).
- **`<input>`**: Eingabefeld.

---

## 7. Semantische Tags
```html
<header>
    <h1>Meine Webseite</h1>
</header>
<nav>
    <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#about">Über uns</a></li>
    </ul>
</nav>
<section>
    <article>
        <h2>Artikelüberschrift</h2>
        <p>Artikeltext...</p>
    </article>
</section>
<footer>
    <p>&copy; 2024 Meine Webseite</p>
</footer>
```
**Erklärung:**
- **`<header>`**: Kopfbereich einer Webseite.
- **`<nav>`**: Navigation.
- **`<section>`**: Abschnitt.
- **`<article>`**: Einzelner Artikel.
- **`<footer>`**: Fußbereich.

---

## 8. Meta-Tags
```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Dies ist eine Beispielwebseite.">
```
**Erklärung:**
- **`charset`**: Zeichensatz (UTF-8 ist Standard).
- **`viewport`**: Responsives Design für mobile Geräte.
- **`description`**: Beschreibung der Webseite für Suchmaschinen.

---

## 9. Medien
### Audio
```html
<audio controls>
    <source src="audio.mp3" type="audio/mpeg">
    Ihr Browser unterstützt kein Audioelement.
</audio>
```
### Video
```html
<video controls width="400">
    <source src="video.mp4" type="video/mp4">
    Ihr Browser unterstützt kein Videoelement.
</video>
```
**Erklärung:** Ermöglicht die Einbettung von Audio- und Videodateien.

---

## 10. Attribute
### Globale Attribute
| Attribut      | Beschreibung                       |
|---------------|-----------------------------------|
| `id`          | Eindeutige ID für ein Element     |
| `class`       | Klassennamen für CSS/JS           |
| `style`       | Inline-CSS                       |
| `title`       | Tooltip-Text                     |

**Beispiel:**
```html
<p id="intro" class="highlight" style="color: red;" title="Dieser Text ist wichtig!">Wichtiger Text</p>
```

---

## 11. Responsive Design
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
**Erklärung:** Dieses Meta-Tag sorgt dafür, dass die Webseite auf mobilen Geräten korrekt angezeigt wird.

---

## 12. Best Practices
1. Verwende **semantische Tags**, um die Struktur klarer zu machen.
2. Nutze **alt**-Attribute für Bilder, um Barrierefreiheit zu gewährleisten.
3. Trenne Inhalt (HTML), Präsentation (CSS) und Verhalten (JavaScript).
