# JavaScript Einführung (17.06.2019)

[Codepen JavaScript Einführung](https://codepen.io/vhbeck/pen/KjzxyX?editors=0012)

- Variablen deklarieren mit `let` oder `const`(nicht änderbar, sollte vorzugsweise benutzt werden, werden in Großbuchstaben geschrieben, Bsp `DAYS_OF_YEAR`)
- CamelCase: z.B: `dateOfYear` (Buchstaben werden groß geschrieben)
- Variable kann mit let nur einmal deklariert werden!!
- Um Variable zu ändern ohne `let`
- Werte ausgeben mit `console.log()`
- Pop-Up: `alert(dateOfYear);`

* auskommentieren: eine Zeile `//` mehrere Zeilen Anfang: `/*` Ende: `*/`

Bsp:

```javascript
let sandwichPrice = 8;
let salatPrice = 7;
let wrapPrice = 6.5;
let frenchFriesPrice = 1.2;

let total =
  4 * sandwichPrice +
  6 * salatPricePrice +
  5 * wrapPrice +
  10 * frenchFriesPrice;
let average = total / 25;
console.log(total);
console.log(average);
```

## Datentypen

- Number `1234` oder `0.5` oder auch nur `.5` und `1e6` = `1000000`, string `'asdf'`, Boolean `true` oder `false`, null (nicht verwenden), undefined, Symbol, Objekte (komplexere Datentypen)

## Operatoren

[MDN Doku Operatoren](https://developer.mozilla.org/de/docs/Web/JavaScript/Guide/Ausdruecke_und_Operatoren)

- `%` : zeigt Rest an , 9 % 2; // 1
- `++Variable;` // Variable + 1
- `Variable--;` // Variable - 1
- `===` prüft, ob gleicher Typ und gleicher Wert

* `==` prüft nur nur ob gleicher Wert, Typ egal
* `!=` ungleicher Wert `!==` ungleicher WErt und ungleicher Typ

## input Feld per Pop-up

[Codepen Beispiel IF und Input](https://codepen.io/vhbeck/pen/vqGMmo?editors=1010)

- `let input = prompt()`
