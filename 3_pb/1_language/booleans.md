# Booleans
Ein Boolean, oder Bool ist ein Operator dessen Ergebnis entweder wahr, oder falsch ist.

## Ist nur der Wert gleich, oder auch der Typ?

Wenn du eine Nummer als Zahl mit einer Nummer als String vergleichst, kann es zu unbeabsichtigten Fehlern kommen, du kannst mit dem sogenannten "Identity Operator" prüfen ob nicht nur der Wert, sondern auch der Datentyp beider Werte übereinstimmt.

```js
// Die Zahl ist die gleiche, aber nicht der typ, deswegen ist hier das Ergebnis FALSE.
6 === "6";

// Die Zahl und der Typ sind identisch, deswegen ist diese Prüfung TRUE.
2 === 2;
```