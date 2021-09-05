# Strings
Ein String ist eine Ansammlung von Buchstaben und Zeichen. Dies können zum Beispiel Sätze, Wörter oder eine IBAN Adresse sein.

## Unterschiede zwischen Quotes

Es gibt keinen sprachbedingten Unterschied zwischen Strings mit Single-Quotes oder Double-Quotes, wenn du dich aber für eine der beiden Schreibweisen entschieden hast, musst du sie am Anfang und am Ende deines Strings benutzen.

**Falsch**

```js
'Hello World";
"Hello World';
```

**Richtig**

```js
// Single Quotes:
'Hello World';

// Double Quotes:
"Hello World';
```

## Leerzeichen

Du kannst sowohl einzelne Leerzeichen per `' ' + ' '` hinzufügen, aber auch Strings mit Leerzeichen beginnen oder enden lassen.

```js
// String + Leerzeichen + String 
'Dies' + ' ' + 'ist' +  ' ' + 'ein' + ' ' + 'String';

// String + String
'Dies ' + 'ist' + ' ein ' + 'String';
```

## Strings escapen

Wenn wir einen String in mehrere Zeilen schreiben wollen können wir ihn mit "Newline" Escapen:
```js
// Newline: \n
'Dies ist ein\nMultiline-String'
// Dies ist ein
// Multiline-String

// Tabulator: \t
'Dies\tist\tein\tString'
// Dies     ist     ein     String
```

## Multiple concats

Du kannst mehrere Strings zu einem Einzelnen hinzufügen, indem du `.concat()` verwendest, und dann mehrere Strings per Komma trennst.

```js
'Dies'.concat('ist', ' ', 'ein', ' String');
```

## Single oder Double Quotes?

Die meisten bekannten JavaScript-Frameworks benutzen Single-Quotes, da sie leserlicher sind und man sich das "Escapen" von Sonderzeichen sehr schnell angewöhnt, auch wenn es momentan umständlich zu sein scheint. 

Geschrieben in Single-Quotes:
- node: 98% des codes
- express: 92% des codes
- React: 90% des codes

---
**mehr Lesematerial**

:point_right:[26-string-methods-in-javascript (engl.)](https://betterprogramming.pub/26-string-methods-in-javascript-6957500cf03f)