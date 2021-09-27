# Comments
Du kannst auf verschiedenste Weise Kommentare in deinen Code einfügen, das hilft dir bei der Übersichtlichkeit und Strukturierung, aber auch beim Erklären, was in deinem Code alles passiert. Kommentare helfen auch anderen Menschen, deinen Code zu lesen.

Es gibt 3 verschiedene Kommentar-arten:

## Einzeilige Kommentare:

```js
    // Dies ist ein einzeiliger Text
```

## Mehrzeiliges Kommentar:

```js
    /*
        Dies ist
        ein mehrzeiliger
        Text
    */
```

Eine weitere, speziellere Kommentar-art ist das sogenannte JSDoc layout. Hiermit können wir in mehreren Zeilen verschiedenste Informationen einfügen, die wir dann mit der Software jsdoc in einer HTML Datei ausgeben können.

JSDoc könnt ihr [hier](https://jsdoc.app/) herunterladen.

## JSDoc kompatible Kommentare:

```js
    /**
     * @method .ToLowerCase();
     * @description Mit dieser Methode können wir Strings zu kleinbuchstaben umwandeln.
     * @returns { string }
     */
```

Probiert gerne ein paar JSDoc Parameter aus, zum Beispiel:
- @see - Hiermit könnt ihr einen link einfügen
- @description - Eine beschreibung des kommentars
- @example - hier könnt ihr beispiele zur nutzung eures codes einfügen.


---

**mehr Lesematerial**

:point_right:[JSDoc documentation](https://jsdoc.app/index.html)



**Youtube Videos**

:point_right:[Steve Griffith - Enhance your Coding with JSDoc](https://www.youtube.com/watch?v=3RIaH0NnG64)
