# Manipulating - Changing the DOM tree

## classList

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

**Toggle einer Klasse (umschalten) **\

wenn die Klassenliste eines Elements einen angegebenen Klassennamen enthält, wird dieser entfernt.\
Wenn die Klassenliste den Klassennamen nicht enthält, wird dieser der Klassenliste hinzugefügt.
```javascript
div.classList.toggle('visible');
```
---

## creating Elements



---
**mehr Lesematerial**

:point_right:[javascripttutorial - innerhtml-vs-createelement](https://www.javascripttutorial.net/javascript-dom/javascript-innerhtml-vs-createelement/)\


