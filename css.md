# CSS (Cascading Style Sheet)

## Style-Tags im Body (ohne explizites CSS-Sheet):

```css
<style>
body {
    background: red;
    }
</style>
```

- body = Selektor
- background = Property

## richtiges CSS einbinden:

- neue Datei namens styles.css erstellen
- im Head einbinden über `<link rel="stylesheet" href="/styles.css" />`

* für class: `.h1`
* für ID: `#example`
* für alles geltend: `*`

```css
* {
}
```

- `:` Pseudo-Selektor, Bsp:

```css
.box:first-child {
  background: rgb(255, 255, 0);
}
```

# Eingabemöglichkeiten

- px , z.B. `100px;`
- % , z.B. `80%;'`
- em , z.B. `1em;` (relativ zur font-size des Eltern-Elements, 1 em bedeutet gleiche Größe wie font des Eltern-Elements. 1.5em ist 1.5-fache Größe der font-size)
- rem , z.B. `1rem;` (relativ zur Basis Font-Size, meistens 16px. z.B. 1.5rem = 24px)
- vw (viewport width), z.B. `width: 100vw;` : Breite im Abhängigkeit zur Bildschirmgröße
- vh (viewport height), z.B. `height: 100vh;` : Höhe in Abhängigkeit zur Bildschirmgröße

# Inline und Block-Elemente

- Inline-Elemente: Höhe wird nicht berücksichtigt, nur die Breite. Werden automatisch immer horizontal angeordnet. (z.B. bei `<span>`)
- Block-Elemente werden automatisch vertikal angeordnet: `h1, h2 ..., p`
- Verhaltensweise von block-Elementen zu Inline-Elementen
  `display: inline;`
- Verhaltensweise von inline-Elementen zu Block-Elementen ändern: `display: inline-block;` `display: block;`

# Farben

- `rgb(255, 255, 255)` (red, green, blue) Farbe im Binärsystem, Werte 0-255
- `rgba(255, 255, 255, .5)` wie rgb nur mit Transparenz, festgelegt mit Wert zwischen 0 - 1
- `#FFFFFF` Farbe im Hexadezimalsystem (Hex-Code genannt), Werte zwischen 0 und F, kann abgekürzt werden in `#FFF`

* `hsl(360, 360, 100)` (h, satiration, lightness)
* `hsla()` mit Transparenz
* Farbverlauf: `background: linear-gradient(Farbe1, Farbe2);`

# Besonderheiten

- **collapsing margin**: margin-top und margin-bottom von untereinander stehenden Elementen kannibalisieren sich - es gilt nur der größere!

* `box-sizing: border-box;`: Padding und Margin werden nach innen berechnet und nicht mehr nach außen
* `margin 0 auto;` automatisch zentrieren
* body background: immer nur so hoch wie der Content --> für Background Color `html` als selektor verwenden
* Kreis machen: `border-radius: 50%`

# Flex

- notwendig, um Flex anzuwenden (nur im Parent-Element!!): `display: flex`

* Element ausblenden: `display: none`
* Element unsichtbar machen: `visibility: hidden`

* `justify-content` : horizontal anordnen
* `align-items`: vertikal anordnen
* abhängig von `flex-direction`: bei Row wie oben genannt, bei column umgekehrt

- `flex-wrap` Element nimmt bei Bedarf auch mehrere Zeilen ein

- `align-self` gilt für nur ein Element

* Hilfe: [CSS Tricks Flex](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
* `flex-grow: 0;` Wachstum einer Box im Verhältnis, wenn mehr Platz zur Verfügung ist, als benötigt
* `flex-shrink: 1;` Schrumpft im Verhältnis, wenn weniger Platz zur Verfügung ist

- `order: 1, -1, 0, +1;` : Reihenfolge von Elementen verändern
- Kurzschreibweise: `flex: 1 0 150px` 1 = grow , 0 = shrink , 150px = Basis-Größe

* `overflow: auto;` oder `overflow: scroll` für scrollbaren Content

* **Achtung:** Parent muss flex sein, damit Child angeordnet werden kann --> child bekommt dann nur noch eine Position [Beispiel in Codepen](https://codepen.io/vhbeck/pen/QXWRvE?editors=0100)

# BEM (Block, Element, Modifier methodology)

- Block component

```html
.btn {}
```

- Element that depends upon the block

```html
.btn__price {}
```

- Modifier that changes the style of the block

```html
.btn--orange{} .btn--big {}
```

[Link zu CSS Tricks BEM](https://css-tricks.com/bem-101/)
[Beispiele für CSS](https://codepen.io/vhbeck/pen/qzEYVR?editors=0100)

## CSS Selektors

```CSS
b {
 color: teal;
}

section > b {
 color: crimson;
}

section + div {
 color: peachpuff;
}
```
