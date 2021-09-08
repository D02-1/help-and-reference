# Conditional Statements
Conditional Statments kontrollieren das Verhalten von Code in JavaScript, indem sie entscheiden ob Code ausgeführt wird oder nicht.

Es gibt gibt 3 verschiedene Arten von Conditional Statements in Javascript:

- `if`: Wenn die Kondition `true` ergibt, wird der Code innerhalb des "if-Blocks" ausgeführt.
- `else if`: Wenn auf eine weitere Kondition getestet wird, und die erste Kondition false ist, wird dieser block ausgeführt.
- `else`: Wenn die oben angegebene Kondition `false` ergibt wird der Code innerhalb des "else-Blocks" ausgeführt.

<img src="if_else_syntax.png" alt="align-items" width="40%">

Beispiel:

```js
const testValue = 25;

// If-Statement:
if(testValue > 5)
{
    console.log(`${ testValue } ist größer als 5`);
}
// ergibt: 25 ist größer als 5

// Else-Statement:
if(testValue === 5)
{
    console.log(`${ testValue } ist gleich 5`);
}
else
{
    console.log(`${ testValue } ist nicht 5`);
}
// ergibt: 25 ist nicht 5

// Else-if Statement:
if(testValue === 5)
{
    console.log("testValue ist 5");
}
else if(testValue === 10)
{
    console.log("testValue ist 10");
}
else
{
    console.log("testValue ist eine andere Zahl");
}
// ergibt: testValue ist eine andere zahl
```

## Und, Oder in Conditional-Statements

Um mehrere Werte zu vergleichen, kann man einen Operator mit in seine if-clause einfügen.
- `||` Der oder Operator
- `&&` Der und Operator


**mehr Lesematerial**

:point_right:[confusion-around-the-slice-splice-split-methods-in-javascript (engl.)](https://www.freecodecamp.org/news/lets-clear-up-the-confusion-around-the-slice-splice-split-methods-in-javascript-8ba3266c29ae/)\
:point_right:[w3schools javascript array methods](https://www.w3schools.com/js/js_array_methods.asp)