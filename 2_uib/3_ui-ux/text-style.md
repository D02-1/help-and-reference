# Fonts & Text Styling

### Schriftgröße

Die CSS-Eigenschaft `font-size` spezifiziert die Schriftgöße. Wir können die Schrift in absoluten oder in relativen Einheiten bestimmen. Am häufigsten werden pixel (`px`), `rem` und `em` genutzt.




Root (HTML) Default Schriftgröße beträgt 16px. 

`rem`:wird immer relative zum Root Element (HTML tag) (1rem = 16px) berechnet\
`em`: wird relative zum Elternelement berechnet. Achtung durch nesting der Elemente kann es mit `em` sehr unübersichtlich werden

<img src="rem-vs-em.png" alt="rem-vs-em" width="60%"> 

---
### Text ausrichten

CSS `text-align` richtet Texte und Inline-Elemente wie Bilder innerhalb eines Blockelements rechtsbündig, linksbündig, zentriert oder im Blocksatz aus.

`text-align`:`center`, `left`,`center`, `right`, `justify`

<img src="text-align.png" alt="text-align" width="70%">

---

### Schriftart

Mit der Eigenschaft `font-family` können wir die zu verwendende Schriftart bestimmen. 

<img src="font-family.png" alt="font-family" width="60%"> 

---
### Schriftart

Mit `font-weight`können wir die Schriftdicke bestimmen.

<img src="font-weight.png" alt="font-weight" width="40%"> 


### Text dekorieren

Die folgenden Werte können wir für `text-decoration` verwenden.

`none` (Ohne Dekoration)
`overline` (Oberstrich)
`underline` (Unterstrich)
`line-through` (Durchgestrichen)

<img src="text-deco.png" alt="text-deco" width="50%"> 

---

### Zeilenabstand

mit `line-height` können wir die Höhe einer Zeile bestimmen. Das sorgt für eine bessere Lesbarkeit.

<img src="line-height.png" alt="line-height" width="50%"> 

### Buchstabenabstand

mit `letter-spacing` können wir den Abstand zwischen den Buchstaben verändern.

<img src="letter-spacing.png" alt="letter-spacing" width="60%"> 

---

### Text transformieren `text-transform`

* `text-transform`:`capitalize` (setzt den ersten Buchstaben des Wortes auf Großschreibung)
* `text-transform`:`uppercase` (setzt das gesamte Wort auf Großschreibung)
* `text-transform`:`lowercase` (setzt das gesamte Wort auf Kleinschreibung)

---


<img src="formatting.png" alt="formatting" width="50%"> 






**mehr Lesematerial**

:point_right:[font und Text Styling Deutsch](https://wiki.selfhtml.org/wiki/CSS/Eigenschaften/font-size)\
:point_right:[Medium Artikel rem vs em units in css](https://medium.com/@hossam.hilal0/rem-vs-em-units-in-css-96d5ac15878e)\
:point_right:[css-tricks](https://css-tricks.com/almanac/properties/f/font-size/)\
:point_right:[tips for using 3rd party fonts](https://www.afasterweb.com/2018/04/11/two-tips-for-using-3rd-party-fonts/)\
:point_right:[font-display](https://css-tricks.com/almanac/properties/f/font-display/)



