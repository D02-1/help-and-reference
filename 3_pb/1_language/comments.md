# Comments
Du kannst auf verschiedenste weise Kommentare in deinen Code einfügen, das hilft dir bei der übersichtlichkeit und strukturierung, aber auch beim erklären, was in deinem code alles passiert. Kommentare helfen auch anderen menschen, deinen code zu lesen.

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

Eine weitere, speziellere Kommentar-art ist das sogenannte JSDoc layout. Hiermit können wir in mehreren zeilen verschiedenste informationen einfügen, die wir dann mit der software jsdoc in einer HTML datei ausgeben können.

JSDoc könnt ihr [hier](https://jsdoc.app/) herunterladen.

## JSDoc kompatible Kommentare:

```js
    /**
     * @method .ToLowerCase();
     * @description Mit dieser Methode können wir Strings zu kleinbuchstaben umwandeln.
     * @returns { string }
     */
```

Probiert gerne ein paar JSDoc parameter aus, zum beispiel:
- @see - Hiermit könnt ihr einen link einfügen
- @description - Eine beschreibung des kommentars
- @example - hier könnt ihr beispiele zur nutzung eures codes einfügen.