# closure

Die Variablen innerhalb der Funktionen entstehen nur, wenn die Funktion ausgeführt wird, und hören auf zu existieren, sobald die Ausführung der Funktion abgeschlossen ist. Die Lebensdauer einer Variablen, die innerhalb einer Funktion definiert ist, ist die Lebensdauer der Funktionsausführung.

## **Aber was ist closure?**


```javascript
function outer() {
    let b = 10;
    const c = 100;
       function inner() {
            
             var a = 20; 
             console.log("a= " + a + " b= " + b);
             a++;
             b++;
        }
       return inner;
    }
    const X = outer();  // outer() invoked the first time
    const Y = outer();  // outer() invoked the second time
    //end of outer() function executions
    X(); // X() invoked the first time  // => OUTPUT a= 20 b= 10
    X(); // X() invoked the second time // => OUTPUT a= 20 b= 11
    X(); // X() invoked the third time  // => OUTPUT a= 20 b= 12
    Y(); // Y() invoked the first time  // => OUTPUT a= 20 b= 10
```

Die innere Funktion kann aufgrund von closures in JavaScript auf die Variablen der umschließenden Funktion zugreifen.
In unserem Beispiel hatte die innere Funktion den Wert von b=10 beibehalten, als die äußere()-Funktion ausgeführt wurde. Der Wert wurde also nach Ausführung der Äußeren Funktion von der inneren Funktion konserviert. (closure)

closure hat drei scope-chains:

- Zugriff auf eigenen Geltungsbereich (scope) – alle Variablen, die zwischen den umschließenden geschweiften Klammern definiert wurden
- Zugriff auf die Variablen der äußeren Funktion (einen Gültigkeitsbereich drüber)
- Zugriff auf die globalen Variablen




---
**mehr Lesematerial**

:point_right::fire:[javascript.info - closure](https://javascript.info/closure)

**Youtube Videos**

:point_right:[Javascript Closure Tutorial | Closures Explained](https://www.youtube.com/watch?v=1S8SBDhA7HA)\
