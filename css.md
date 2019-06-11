# CSS (Cascading Style Sheet)

## Style im Body:

`<style> body { background: red; } </style>`

- body = Selektor
- background = Property

## richtiges CSS einbinden:

- neue Datei namens styles.css erstellen
- im Head einbinden über `<link rel="stylesheet" href="/styles.css" />`

* für class: `.h1`
* für ID: `#example`
* für alles geltend: `*`
* `:` Pseudo-Selektor

# Eingabemöglichkeiten

- px , z.B. `100px;`
- % , z.B. `80%;'`
- em , z.B. `1em;` (relativ zur font-size des Eltern-Elements, 1 em bedeutet gleiche Größe wie font des Eltern-Elements. 1.5em ist 1.5-fache Größe der font-size)
- rem , z.B. `1rem;` (relativ zur Basis Font-Size, meistens 16px. z.B. 1.5rem = 24px)
- vw (viewport width), z.B. `100vw;` : Breite im Abhängigkeit zur Bildschirmgröße
- vh (viewport height), z.B. `100vh;` : Höhe in Abhängigkeit zur Bildschirmgröße

# Inline und Block-Elemente

- Inline-Elemente: Höhe wird nicht berücksichtigt, nur die Breite (z.B. bei `<span>`)
- Block-Elemente: `h1, h2 ..., p`
- Verhaltensweise von block-Elementen zu Inline-Elementen
  `display: inline;`
- Verhaltensweise von inline-Elementen zu Block-Elementen ändern: `display: inline-block;` `display: block;`

# Farben

- `rgb(255, 255, 255)` (red, green, blue) Farbe im Binärsystem, Werte 0-255
- `rgba(255, 255, 255, .5)` wie rgb nur mit Transparenz, festgelegt mit Wert zwischen 0 - 1
- `#FFFFFF` Farbe im Hexadezimalsystem, Werte zwischen 0 und F

* `hsl(360, 360, 100)` (h, satiration, lightness)
* `hsla()` mit Transparenz

# Besonderheiten

- **collapsing margin**: margin-top und margin-bottom von untereinander stehenden Elementen kannibalisieren sich - es gilt nur der größere!

* `box-sizing: border-box;`: Padding und Margin werden nach innen berechnet und nicht mehr nach außen
* `margin 0 auto;` automatisch zentrieren
* body background: immer nur so hoch wie der Content --> für Background Color `html` als selektor verwenden

# Flex

- `justify-content` : horizontal anordnen
- `align-items`: vertikal anordnen
- abhängig von `flex-direction`! bei Row wie oben genannt, bei column umgekehrt
- Hilfe: [CSS Tricks Flex](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- `flex-grow: 1;` Wachstum einer Box im Verhältnis, wenn mehr Platz zur Verfügung ist, als benötigt
- `flex-shrink: 1;` Schrumpft im Verhältnis, wenn weniger Platz zur Verfügung ist

* Kurzschreibweise: `flex: 1 0 150px` 1 = grow , 0 = shrink , 150px = Basis-Größe

# Parents + Children

- Parent muss flex sein, damit Child angeordnet werden kann --> child bekommt dann eine Position
