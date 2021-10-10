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
      return `Dieser Kuchen ist wird mit ${this.flavor} und ${this.eggs} Eiern zubereitet, ${this.method} und als ${this.form} serviert.`;
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
      return console.log (`Dieser ${this.type} wird als ${this.form} ${this.method} und schmeckt gut mit ${this.cover}`);
   }
}
//Dieser Käsekuchen wird als Tarte kaltgestellt und schmeckt gut mit Himbeeren.
```
`super` verweist dabei auf den Kontext von der übergeordneten Klasse.

---

## getters und setters

## static methods

---

:exclamation:Anders als die meisten Deklaration in Javascript werden Klasse nicht nach oben gehoben (hoisted) und müssen darum vor der ersten Benutzung deklariert werden.


---
**mehr Lesematerial**

new keyword to create the object via the constructor (calls the constructor
)
getters and setters control who people can access my property

:point_right:[javascripttutorial - class](https://www.javascripttutorial.net/es6/javascript-class/)\

he constructor() is where you can initialize the properties of an instance. JavaScript automatically calls the constructor() method when you instantiate an object of the class.

static 
called by class prototype


**Youtube Videos**

:point_right:[Web Dev Simplified - What are Classes, Objects, and Constructors?](https://www.youtube.com/watch?v=5AWRivBk0Gw)
:point_right:[Steve Griffith - JavaScript Classes in 2021](https://www.youtube.com/watch?v=tqBP5ZX8F0c)




