# advanced parameters


Wir können beim Aufrufen einer Funktion weniger oder mehr Argumente übergeben, als wie wir Parameter definiert haben. 

- wenn wir weniger Argumente übergeben, sind die restlichen Parameter `undefined`
- wenn wir mehr Argumente übergeben, werden zusätzliche Argumente einfach ignoriert.

```javascript
function ShowMessage(firstName, lastName) {
    alert("Hello " + firstName + " " + lastName);
}

ShowMessage("Steve", "Jobs", "Mr."); // output: Hello Steve Jobs
ShowMessage("Bill"); // output: Hello Bill undefined
ShowMessage(); // output: Hello undefined undefined
```
---
## arguments object 

Das arguments-object ist ein Array-ähnliches Objekt, das auf die übergebenen Parameter einer Funktion verweist.
Es ist eine lokal verfügbare Variable, welche wir aber nur in allen (Nicht-Pfeil-) Funktionen :exclamation:nutzen können. Das Objekt enthält einen Eintrag für jeden übergebenen Parameter der Funktion. 


```javascript
function sumAllArguments(){
    let total = 0;
    for(let i = 0; i<arguments.length; i++){
        total += arguments[i]
    }
    return total
}
//output 248
sumAllArguments(5,9,45,68,11,32,74,4)
```
---
- das arguments-object beinhaltet die Parameter, die einer Funktion übergeben wurden.
- auf die einzelnen Parameter können wir mit dem Index zugreifen.
- mit Hilfe von `arguments.length` können wir die Anzahl der übergebenen Parameter herausfinden.
- über das arguments-object können einzelne Parameter auch verändert werden.
- Wichtig: Das arguments-Object ist kein Array :exclamation:

```javascript
function testFunktion(paramA, paramB, paramC) {

    // output: 'Test1'
    console.log(arguments[0]);
  
    // output: 'Test2'
    console.log(arguments[1]);  
  
    // output: 3
    console.log(arguments[2]);
  
    // Anzahl der übergebenen Parameter anzeigen
    // output: 3
    console.log(arguments.length);  
  
    // Aus 'Test2' wird 'TestZwei'
    // output: 'TestZwei'
    arguments[1] = 'TestZwei';
    console.log( arguments[1]);
  }
  
  testFunktion('Test1', 'Test2', 3);
```
## rest-parameter vs arguments object

- in Pfeil Funktionen können wir nur mit dem rest-paramter arbeiten:exclamation:(sie haben kein arguments object)
- das Arguments-object enthält alle an die Funktion übergebenen Argumente, während der rest-parameter nur diejenigen sind, die keinen anderen Namen erhalten.
- der rest-paramter muss immer am Ende stehen:exclamation:
- rest parameter werden als ein Array representiert, auf dem wir auch Array Methoden anwenden können :exclamation:

```javascript
function sumOfNumbers(name , ...numbers){
       var sum = 0
       for (let num of numbers) 
            sum += num;
       return ( name + " the total sum is " + sum);
}
sumOfNumbers("John" , 1 , 2 , 3 , 4 , 5 , 6);
// output: John the total sum is 21
sumOfNumbers("Rita")
// output: Rita the total sum is 0
```

```javascript
function xyz(x, y, ...z) {
  console.log(z); // output: ["wassup", "goodmorning", "hi", "howdy"]
  console.log(z[0]); // output: wassup
  console.log(z.length); // output: 4
}

xyz("hey", "hello", "wassup", "goodmorning", "hi", "howdy")
```

---
## default parameter

Wenn eine Funktion in JavaScript mit fehlenden Argumenten (weniger als deklariert) aufgerufen wird, werden die fehlenden Werte auf `undefined` gesetzt. 
Mit default parametern können wir die benannten Paramter der Funktion mit Standartwerten (default Werten) initialisieren. Diese werden genutzt, wenn keine Werte oder undefined an die Funktion übergeben werden. Es kann uns helfen, Fehler im code zu vermeiden.

```javascript
function say(message='Hi') {
    console.log(message);
}

say(); // output: 'Hi'
say('Hello') // output: 'Hello'
say(undefined); // output: 'Hi'
```
Der Standardwert wird nur aktiviert, wenn kein Wert oder undefined übergeben wird. 

---
**mehr Lesematerial**

:point_right:[the-arguments-object-in-javascript](https://dev.to/shahab570/the-arguments-object-in-javascript-1a37)\
:point_right:[What-is-the-difference-between-rest-parameters-and-the-arguments-object-in-Javascript](https://www.tutorialspoint.com/What-is-the-difference-between-rest-parameters-and-the-arguments-object-in-Javascript)\
:point_right:[medium -parameters-and-arguments-in-javascript](https://medium.com/swlh/parameters-and-arguments-in-javascript-2260bcbc8d4f)\
:point_right:[javascript-rest-parameters](https://www.javascripttutorial.net/es6/javascript-rest-parameters/)\
:point_right:[setting-default-parameters](https://www.samanthaming.com/tidbits/11-setting-default-parameters/)\
:point_right:[digitalocean understanding-default-parameters-in-javascript](https://www.digitalocean.com/community/tutorials/understanding-default-parameters-in-javascript)\












