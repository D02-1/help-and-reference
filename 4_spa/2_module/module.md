# Module

**:exploding_head: Problem :exploding_head:**

- Wenn wir mehrere skript-tags in unsere HTML Datei einbinden wollen, die alle voneinander abhängig sind, kann es sehr leicht passieren, das wir den Code versehentlich beschädigen, wenn wir die scripts in der falschen Reihenfolge im HTML einbinden. 


- JS Variablen aus all unseren Dateien sind global, sodass das versehentliche Überschreiben von Variablen zwischen mehreren JS-Dateien wirklich sehr leicht passieren kann. 

```javascript
// user.js
let userCount = 0

class User {
  constructor(name, age) {
    this.name = name
    this.age = age
    userCount++
  }
}

function printName(user) {
  console.log(`User has the name ${user.name}`)
}

function printAge(user) {
  console.log(`${user.name} is ${user.age} years old`)
}



// script.js
const user = new User("Kyle", 26)
printName(user)
// User has the name Kyle
printAge(user)
// Kyle is 26 years old
```

**:bangbang: in unserer index.html müssen wir die user.js vor der script.js laden :bangbang:**

```html
<!-- index.html -->
<script src="user.js"></script>
<script src="script.js"></script>
```
---

**:bulb: Lösung :bulb:**

Um dieses Problem zu beheben, können wir auf ES6-Module zurückgreifen. ES6-Module ermöglichen es uns, bestimmte Informationen aus einer Datei zu exportieren und dann in eine andere Datei zu importieren.

:red_circle: im script, welches wir in der HTML Datei einbinden setzen wir den type auf module
Wir brauchen kein extra script-tag für user.js mehr, da wir den code von user.js exportieren und in script.js importieren werden

```html
<!-- index.html -->
<script src="script.js" type="module"></script>
```


## Exporting

so::point_down:

```javascript
// user.js
let userCount = 0

class User {
  constructor(name, age) {
    this.name = name
    this.age = age
    userCount++
  }
}

function printName(user) {
  console.log(`User has the name ${user.name}`)
}

function printAge(user) {
  console.log(`${user.name} is ${user.age} years old`)
}

export default User
export printName
export printAge
```
am Ende der user.js deklarieren wir unseren export. wir können in einer Datei immer nur einen export default haben, aber mehrere sogenannte named exports. Wir können den export entweder ganz unten in der Datei deklarieren oder setzten das keyword export direkt auf die selbe Zeile, wo die Funktion/ Klasse deklariert wird. (siehe im folgenden Beispiel)

oder so::point_down:

```javascript
// user.js
let userCount = 0

export default class User {  constructor(name, age) {
    this.name = name
    this.age = age
    userCount++
  }
}

export function printName(user) {
  console.log(`User has the name ${user.name}`)
}

export function printAge(user) {
  console.log(`${user.name} is ${user.age} years old`)
}
```
---
## Importing

```javascript
// script.js
import User, { printAge, printName } from './User.js'

const user = new User("Kyle", 26)
printName(user)
// User has the name Kyle
printAge(user)
// Kyle is 26 years old
```
import keyword gefolgt vom default import, wenn wir einen default export haben. Danach ein Komma und es folgen alle benannten Exporte in geschweiften Klammern. Danach folgt das keyword from gefolgt vom Pfad zur Datei. Der Dateipfad für die importierte Datei ist relativ zu der Datei, die den Import durchführt und muss ./ am Anfang des Pfads haben.

---
### Beispiel für nur default Import

```javascript
import User from './User.js'
```
### Beispiel für nur named Import

```javascript
import { printAge } from './User.js'
```
---
## Imports umbenennen

Manchmal kann es nötig sein, die Funktionen/Klassen/Variablen, die wir aus einer anderen Datei importieren, umzubenennen, zum Beispiel wenn wir bereits eine andere Variable mit demselben Namen haben oder einen eindeutigeren Namen verwenden möchten. 

- ### Import defaults umbenennen

```javascript
import Person from './User.js'

const user = new Person("Kyle", 26)
```
In diesem Beispiel haben wir den default export von User in Person umbenannt. Der Grund, warum wir dies so tun können, ist, dass Sie immer nur einen default export gibt, sodass JavaScript weiß, welchen Namen wir dem default export geben, der dem einzigen default export aus der Datei entspricht.

- ### named Imports umbenennen

```javascript
// script.js
import User, { printName as printUserName } from './User.js'
const user = new User("Kyle", 26)
printUserName(user)
// User has the name Kyle
```

Das Umbenennen von named exports ist etwas schwieriger, da JavaScript den Namen des Exports verwendet, um zu wissen, welchen Export Sie importieren. Aus diesem Grund müssen wir beim Umbenennen eines named exports den Namen des Exports gefolgt vom keyword as und dann den neuen Namen den wir verwenden möchten.

---

**mehr Lesematerial**

:point_right:[webdevsimplified - es6-modules](https://blog.webdevsimplified.com/2021-11/es6-modules/)\
:point_right:[medium - how-to-use-npm-and-import-export-modules-in-javascript](https://javascript.plainenglish.io/how-to-use-npm-and-import-export-modules-in-javascript-31a7f66a2064)


