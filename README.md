
# Responsive Design mit HTML5 und CSS3

Enno Hyttrek, November 2024

https://ehy-classroom.github.io/responsive-design-introduction/
https://ehy-classroom.github.io/responsive-design-introduction/responsive-design-erste-schritte/

---

### Was ist Responsive Design und warum ist es wichtig?

**Responsive Design** bezeichnet eine Technik im Webdesign, bei der Websites so gestaltet werden, dass sie auf unterschiedlichen Endgeräten (Desktop, Tablet, Smartphone) optimal dargestellt werden. Das Design passt sich flexibel an die jeweilige Bildschirmgröße, Auflösung und Ausrichtung an. 

Die Idee wurde populär, als Smartphones und Tablets immer häufiger zum Surfen im Internet verwendet wurden. Da Benutzer verschiedene Geräte mit unterschiedlich großen Bildschirmen nutzen, ist es notwendig, Websites entsprechend anzupassen.

---

### Grundlagen von HTML5 und CSS3 für Responsive Design

#### HTML5-Grundlagen für Responsive Design

HTML5 bietet die Möglichkeit, semantische Elemente zu verwenden und moderne Inhalte einfacher zu strukturieren. 

- **Viewport-Meta-Tag**: Mit dem Viewport-Tag wird das Verhalten der Seite auf mobilen Geräten gesteuert.

  Beispiel:
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```

  - `width=device-width`: Die Breite entspricht der Gerätegröße.
  - `initial-scale=1.0`: Die Anfangszoomstufe wird festgelegt.

#### CSS3-Grundlagen für Responsive Design

CSS3 bietet Werkzeuge wie **Media Queries**, **Flexbox** und **Grid**, um Layouts flexibel zu gestalten.

1. **Media Queries**:
   Mit Media Queries können CSS-Regeln für bestimmte Bildschirmgrößen oder Geräte definiert werden.

   Beispiel:
   ```css
   @media (max-width: 600px) {
       body {
           background-color: lightblue;
       }
   }
   ```

   - `max-width: 600px`: Die Regel greift, wenn die Bildschirmbreite 600px oder kleiner ist.

2. **Flexible Layouts**:
   Flexible Layouts nutzen relative Maßeinheiten wie Prozent (`%`) oder `em` statt fester Pixel-Werte.

   Beispiel:
   ```css
   .container {
       width: 100%;
       padding: 2%;
   }
   ```

3. **Bilder und Videos skalieren**:
   Bilder und Videos sollten so angepasst werden, dass sie sich der Breite des Containers anpassen.

   Beispiel:
   ```css
   img {
       max-width: 100%;
       height: auto;
   }
   ```

---

### Das Prinzip der „Mobile First“-Strategie

**Mobile First** ist eine Designstrategie, bei der die Entwicklung zuerst für kleinere Bildschirme (z. B. Smartphones) erfolgt und anschließend für größere Geräte angepasst wird. Dies erleichtert das Layout und sorgt für eine optimale Performance auf Mobilgeräten.

Beispiel:

```css
/* Grundlayout für mobile Geräte */
body {
    font-size: 14px;
}

/* Anpassungen für größere Bildschirme */
@media (min-width: 768px) {
    body {
        font-size: 16px;
    }
}
```

---

### Praktische Beispiele: Responsive Design

#### 1. Eine einfache responsive Website mit Media Queries

```html
<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Design</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        h1 {
            text-align: center;
        }
        .container {
            display: flex;
            flex-direction: column;
            padding: 20px;
        }
        @media (min-width: 768px) {
            .container {
                flex-direction: row;
                justify-content: space-around;
            }
        }
    </style>
</head>
<body>
    <h1>Responsive Design</h1>
    <div class="container">
        <div>Box 1</div>
        <div>Box 2</div>
        <div>Box 3</div>
    </div>
</body>
</html>
```

- **Erklärung**: Auf kleineren Geräten werden die Boxen untereinander angezeigt, auf größeren Bildschirmen nebeneinander.

#### 2. Bilder skalieren

```html
<img src="beispielbild.jpg" alt="Responsive Bild" style="max-width: 100%; height: auto;">
```

- Bilder passen sich flexibel der Container-Breite an.

---

### Zusammenfassung

- **Responsive Design** passt Websites an verschiedene Geräte und Bildschirmgrößen an.
- Das **Viewport-Tag** ist entscheidend für eine korrekte Darstellung auf mobilen Geräten.
- Mit **CSS Media Queries**, **Flexbox** und **Grid** lassen sich flexible Layouts erstellen.
- Die **Mobile First**-Strategie ist eine bewährte Methode, um eine optimale Benutzererfahrung sicherzustellen.

---

Quellen/Links:

#### Deutsch

https://wiki.selfhtml.org/wiki/CSS/Tutorials/Responsive_Design

https://developer.mozilla.org/de/docs/Web/Guide/CSS/Media_queries

#### Englisch

https://www.w3schools.com/css/css_rwd_intro.asp  
https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design
