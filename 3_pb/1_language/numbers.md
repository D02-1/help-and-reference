# Numbers
Numbers beinhaltet verschiedene Arten von Zahlen, egal ob sie Dezimalstellen haben, oder nicht.

## Positive oder Negative Zahlen

Du kannst jede Art von Zahl negativ oder positiv darstellen.

```js
// Positive Zahlen:
1;
25;
500;
1.5;
22.4;
8.6472;

// Negative Zahlen:
-3;
-11;
-250;
-2.5;
-10.9;
-31.8876;
```

## Mit sich selbst multiplizierte Zahlen

Wenn du eine Zahl mehrfach mit sich selbst multiplizieren willst, musst du diese Zahl nicht mehrfach schreiben, du kannst sie einfach definieren und durch den Exponent-Operator einstellen wie oft du sie multiplizieren willst.

```js
// Kurz für 3 * 3 * 3 * 3 * 3
3 ** 5;
```

## Punkt vor Strich Rechnung

Wenn du eine Aufgabe wie `1 + 8 / 4 + 5` siehst, 
denkst du vielleicht der Computer rechnet erst `1 + 8` und `4 + 5` zusammen um diese dann zu teilen, aber der Computer rechnet genau wie du es in der Schule gelernt hast, Punkt-vor-Strich rechnung, er sieht also als aufgabe `1 + 2 + 5`, da er die Division als erstes gelöst hat.

```js
// Wird zu:
// 8 / 4 = 2;
// 1 + 2 + 5;
// -----------
// Ergebnis: 8
1 + 8 / 4 + 5;
```

Oft muss dein Code aber anders rechnen, Wenn in bestimmten  Fällen andere Werte berechnet werden müssen. Um dies zu erreichen kannst du Aufgabenteile wie `1 + 8` oder `4 + 5` in Klammern setzen, diese werden dann zusammengerechnet und erst dann verarbeitet.

```js
// Wird zu:
// 1 + 8 = 9
// 4 + 5 = 9
// 9 / 9
// -----------
// Ergebnis: 1
(1 + 8) / (4 + 5);
```

---
**mehr Lesematerial**

:point_right:[w3schools number methods](https://www.w3schools.com/js/js_number_methods.asp)\
:point_right:[10-javascript-methods-of-the-math-object (engl.)](https://javascript.plainenglish.io/top-10-javascript-methods-of-the-math-object-ac69951386a5)\
:point_right:[how-to-do-math-in-javascript-with-operators (engl.)](https://www.digitalocean.com/community/tutorials/how-to-do-math-in-javascript-with-operators)



