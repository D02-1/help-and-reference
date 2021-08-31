# Primitives
In JavaScript kannst du, abgesehen von Arrays, 6 verschiedene Arten von werten nutzen, diese sind:
- Boolean: `bool`
- Null: `null`
- Undefined: `undefined`
- Number: `number`
- String: `string`
- Symbol: `symbol`

## Null vs. Undefined

Es liegt nahe zu denken das `null` und `undefined` das Gleiche sind, aber es gibt subtile Unterschiede:

`null` ist ein leerer, nicht existierender Wert, und kann einer Variable zugeordnet werden.

```js
let a = null;
// null
```

`undefined` ist der Wert einer Variable die deklariert, aber nicht definiert wurde.

```js
let b;
// undefined
```