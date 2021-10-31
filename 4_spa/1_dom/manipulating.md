# Manipulating - Changing the DOM tree

---

- ## classList

Die `classList` ist ein `DOMTokenList`-Objekt, welche als Inhalt die Klassenattribute von Elementen darstellt.
Die enthaltenen Klassen dieser `classList`, können wir mit verschiedenen Methoden bearbeiten.

```html
<div id="content" class="main red">JavaScript classList</div>  
```
```javascript
let div = document.querySelector('#content');
for (let cssClass of div.classList) {
    console.log(cssClass);
}
//OUTPUT => main red
```
### Methoden

**Add (hinzufügen) Klassen zur classList eines Elementes**

```javascript
div.classList.add('info');
div.classList.add('info','visible','block');
```
**Remove Klassen von der classList eines Elementes (entfernen)**

```javascript
div.classList.remove('visible');
div.classList.remove('block','red');
``` 
**Replace eine existierende Klasse durch eine andere Klasse (ersetzen)**

```javascript
div.classList.replace('info','warning');
```
**contains ein Element eine bestimmte Klasse? (beinhaltet?)**

```javascript
div.classList.contains('warning'); // true
```

**Toggle einer Klasse (umschalten)**

wenn die Klassenliste eines Elements einen angegebenen Klassennamen enthält, wird dieser entfernt.\
Wenn die Klassenliste den Klassennamen nicht enthält, wird dieser der Klassenliste hinzugefügt.
```javascript
div.classList.toggle('visible');
```
---

- ## creating Elements

```javascript
const e = document.createElement('div');//=> erstellt ein div
e.innerHTML = '<strong>Hi there!</strong> JavaScript DOM';//=> füllt das div mit text
document.body.appendChild(e);//=> hängt das neue Element im DOM-Tree an
```

**Alternativ zu innerHTML können wir auch die createTextNode() Methode nutzen**

```javascript
const e = document.createElement('div')
const textnode = document.createTextNode('Hi there! JavaScript DOM');
e.appendChild(textnode); 
document.body.appendChild(e)
```
---
- ## innerHTML, innerText und textContent

In Javascript gibt es drei Eigenschaften, die verwendet werden können, um den Inhalt eines HTML-Elements im DOM zu setzen oder zurückzugeben: `innerHTML`, `innerText` und `textContent`.

`innerHTML`

```javascript
document.getElementById(“example”).innerHTML = “And <strong> NOW </strong> the contents have been changed!”;
```
***Da mit innerHTML der Inhalt einer Seite verändert werden kann, können gefährliche `<script>`-Tags und andere JavaScript-Angriffe ausgeführt werden.***

`innerText` 
- wenn Elemente mit CSS ausgeblendet werden (indem Sie so etwas wie die Eigenschaften "display" oder "visibility" verwenden), kann innerText nicht darauf zugreifen
- innerText gibt NICHT den Inhalt von `<script>`- oder `<style>`-Elementen zurück

`textContent`
- gibt den Textinhalt aller Elemente zurück, einschließlich `<script>` und `<style>`
- gibt den Text von Elementen zurück, die mit CSS versteckt sind

Alle `Node-Objekte` haben `textContent`, während **nur** `HTMLElement-Objekte` `innerText` haben.

---
**mehr Lesematerial**

:point_right:[javascripttutorial - innerhtml-vs-createelement](https://www.javascripttutorial.net/javascript-dom/javascript-innerhtml-vs-createelement/)\
:point_right:[javascript.info - document](https://javascript.info/document)\
:point_right:[javascript.info - insertion methods](https://javascript.info/modifying-document)\
:point_right:[wiki.selfhtml.org (deutsch) - Was ist das DOM](https://wiki.selfhtml.org/wiki/JavaScript/Tutorials/DOM/Was_ist_das_DOM)





