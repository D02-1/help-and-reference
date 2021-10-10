# classes

Wenn wir mehrere Objekte erstellen wollen, können uns Klassen dabei helfen, das wir unseren Code nicht ständig wiederholen müssen.
Mit Klassen können wir einen Bauplan anlegen, welche Eigenschaften und Methoden unser Objekt haben soll.


```javascript
class Cake {
   constructor (flavor, method, form, eggs) {
      this.flavor = flavor;
      this.method = method;
      this.form = form;
      this.eggs = eggs;
   }
   cakeRecipe() {
      return `Dieser Kuchen ist wird mit ${this.flavor} und ${this.eggs} Eiern zubereitet, 
      ${this.method} und als ${this.form} serviert.`;
   }
}
```
## Erstellen einer Instanz

mit dem Keyword `new` können wir eine `Instanz` aus unserem `Prototyp` (Bauplan) erzeugen
Es wird die `constructor`Methode aufgerufen und dieser werden die Werte übergeben für das neue Objekt übergeben

```javascript
const schoko = new Cake ("Schoko", "gebacken", "Kastenform", 4);
console.log (schoko.cakeRecipe());
//Dieser Kuchen ist wird mit Schoko und 4 Eiern zubereitet, gebacken und als Kastenform serviert.
```
---
Wenn wir unserer Klasse noch weitere Eigenschaften hinzufügen würden, würden alle bereits erstellten Instanzen diese Eigenschaft automatisch erben.

---

## Extends

Eine weitere Klasse, die um Eigenschaften und Methoden erweitert werden soll, kennzeichnet diese mit dem Schlüsselwort extends. Das stellt sicher, dass die neue Klasse dieselben Eigenschaften wie ihr Prototyp hat und dazu ihre individuellen Eigenschaften und Methoden.

```javascript
class Cheesecake extends Cake {
   constructor (flavor, method, form, eggs, cover, type, cakeRecipe) {
      super ( flavor, method, form, eggs, cakeRecipe);
      this.cover = cover;
      this.type = "Käsekuchen";
   }
	
   cakeGarnish () {
      return console.log (`Dieser ${this.type} wird als ${this.form} ${this.method} 
      und schmeckt gut mit ${this.cover}`);
   }
}
//Dieser Käsekuchen wird als Tarte kaltgestellt und schmeckt gut mit Himbeeren.
```
`super` verweist dabei auf den Kontext von der übergeordneten Klasse.

---

## getters und setters

`getters` - um auf Eigenschaften eines Objektes zuzugreifen - 
`setters` - um Eigenschaften eines Objektes zu ändern bzw. zu verwandeln

Mit den Schlüsselwörtern `get`(read only/ function ohne Argumente) und `set` (function mit einem Argument) erstellen wir Methoden.
Mit getters und setters können wir Logic ausführen. So können wir Inputs bspw. erst auf Richtigkeit Kontrollieren bzw Daten zur Rausgabe aufbereiten.
Sie sind im Wesentlichen Funktionen, die beim Abrufen und Setzen eines Werts ausgeführt werden, aber für einen externen Code wie normale Eigenschaften aussehen.

```javascript
let user = {
  name: "John",
  surname: "Smith",

  get fullName() {
    return `${this.name} ${this.surname}`;
  }
};

alert(user.fullName); // John Smith
```
---
## static methods

Statische Methoden werden von allen Instanzen einer Klasse gemeinsam genutzt. Somit sind sie der Klasse zugeordnet, nicht einer bestimmten Instanz dieser Klasse. Die statischen Methoden werden über den Klassennamen aufgerufen, nicht über die Instanzen der Klasse. 

```javascript
class Person {
	constructor(name) {
		this.name = name;
	}
	getName() {
		return this.name;
	}
	static createAnonymous(gender) {
		let name = gender == "male" ? "John Doe" : "Jane Doe";
		return new Person(name);
	}
}

let anonymous = Person.createAnonymous("male");
console.log(anonymous);
//Person { name: 'John Doe' }
```
---

:exclamation::exclamation::exclamation:Anders als die meisten Deklaration in Javascript werden Klasse nicht nach oben gehoben (hoisted) und müssen darum vor der ersten Benutzung deklariert werden.


---
**mehr Lesematerial**

:point_right:[javascripttutorial - class](https://www.javascripttutorial.net/es6/javascript-class/)

**Youtube Videos**

:point_right:[Web Dev Simplified - What are Classes, Objects, and Constructors?](https://www.youtube.com/watch?v=5AWRivBk0Gw)\
:point_right:[Steve Griffith - Intro to JavaScript Classes](https://www.youtube.com/watch?v=_D6ilsRB9tw)\
:point_right:[JavaScript Getters and Setters | Mosh](https://www.youtube.com/watch?v=bl98dm7vJt0&t=314s)






