# callbacks

Funktionen sind Objekte erster Klasse – wir können eine Funktionen auch als Argument in eine andere Funktionen übergeben 

Funktionen, die einer anderen Funktion als Parameter übergeben werden heißen `callback function`.
Callback ist eine Funktion, die als Argument an eine andere Funktion übergeben wird und deren Ausführung verzögert wird, bis die Funktion, in der sie übergeben wurde, ausgeführt wird. 

```javascript
function finishedSpeaking(animal, sound) {
    return `The ${animal} has finished ${sound}ing`;
}
function notFinishedSpeaking(animal, sound) {
    return `The ${animal} has NOT finished ${sound}ing`;
}
function speak(animal, noise, afterSpeaking) {
    console.log(noise.toUpperCase());
    return afterSpeaking(animal, noise);
}
speak('cat', 'meow', finishedSpeaking);
// Result: 'MEOW'
// Result: 'The cat has finished meowing'
speak('dog', 'bark', notFinishedSpeaking);
// Result: 'BARK'
// Result: 'The dog has NOT finished barking'
```

Die Funktionen finishedSpeaking und notFinishedSpeaking werden als Argumente übergeben, sodass wir sie hier nicht wirklich aufrufen, also gibt es keine Klammern ().

---

**array.map (), array.reduce() und array.filter () sind Beispiele für Methoden welche Callback-Funktionen verwenden**

Map mit einer anonymen callback function. 

```javascript
const arr = [1,2, 3,4,5]
const square = (num) => {return num*num}
const newArr = arr.map(square)
```

Map mit einer named callback function. 

```javascript
const arr = [1,2, 3,4,5]
const square = (num) => {return num*num}

const newArr = arr.map(square)
console.log(newArr)
```

Die Funktion square() wird als Argument in .map() übergeben, sodass wir sie hier nicht wirklich aufrufen, also gibt es keine Klammern (). 

---

**mehr Lesematerial**

:point_right:[mediaevent callbacks](https://www.mediaevent.de/javascript/callback-function.html)\
:point_right:[freecodecamp - what-are-callbacks-in-js-and-how-to-use-them](https://www.freecodecamp.org/news/javascript-callback-functions-what-are-callbacks-in-js-and-how-to-use-them/)\
:point_right:[betterprogramming - javascript-callback-functions](https://betterprogramming.pub/thinking-in-javascript-callback-functions-268dd14f2572)


**Youtube Videos**

:point_right:[Steve Griffith - JS Callback Functions](https://www.youtube.com/watch?v=KiLB8sViPMA)

