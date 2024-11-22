
# HTML, CSS und JavaScript - Interaktives Beispiel

## Erklärung
In diesem Beispiel wird eine einfache Webseite erstellt, die einen Button enthält. Beim Klicken auf den Button wird mithilfe von JavaScript eine Nachricht angezeigt. Die Struktur der Seite wird mit **HTML** definiert, das Styling mit **CSS** hinzugefügt, und die Logik wird durch **JavaScript** bereitgestellt.

### Aufbau der Datei
- **HTML**: Grundlegender Aufbau der Webseite.
- **CSS**: Gestaltung des Buttons und der Nachricht.
- **JavaScript**: Funktionalität, um die Nachricht dynamisch anzuzeigen.

---

## HTML (index.html)
```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interaktiver Button</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <h1>Willkommen auf meiner interaktiven Webseite</h1>
    <button id="messageButton">Klicke mich!</button>
    <p id="message"></p>

    <script src="script.js"></script>
</body>
</html>
```

---

## CSS (styles.css)
```css
body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 20px;
    background-color: #f0f0f0;
}

h1 {
    color: #333;
}

button {
    padding: 10px 20px;
    font-size: 16px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}

#message {
    margin-top: 20px;
    font-size: 18px;
    color: #555;
}
```

---

## JavaScript (script.js)
```javascript
// Funktion, die eine Nachricht anzeigt
document.getElementById("messageButton").addEventListener("click", function() {
    const messageElement = document.getElementById("message");
    messageElement.textContent = "Du hast den Button geklickt! 🎉";
});
```

---

## Funktionsweise
1. **HTML**: Der Button wird durch `<button>` erstellt. Ein `<p>`-Element wird als Platzhalter für die Nachricht definiert.
2. **CSS**: 
   - Der Button erhält eine ansprechende Gestaltung mit Farben und Hover-Effekt.
   - Die Nachricht wird optisch hervorgehoben.
3. **JavaScript**: Ein Event Listener hört auf das Klicken des Buttons und zeigt eine Nachricht im `<p>`-Element an.

---

## Anwendung
Speichere die Dateien `index.html`, `styles.css` und `script.js` im gleichen Verzeichnis. Öffne die `index.html`-Datei in einem Browser, um die interaktive Webseite zu sehen.
